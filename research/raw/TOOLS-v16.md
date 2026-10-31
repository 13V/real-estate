# Agent Reach 1.6 tool sheet (tested 31 Oct 2026 on this server)

Run from /tmp (cd /tmp first). Output is one JSON object; content is in .items[] (title, url, author, published_at, text).

## Reddit search (WORKS, no login, returns post bodies)
cd /tmp && timeout 150 agent-reach reddit search "<query>" --limit 10
Trim output, e.g.:
cd /tmp && timeout 150 agent-reach reddit search "property manager AI maintenance" --limit 10 | python3 -c "import sys,json;d=json.load(sys.stdin);print(d.get('ok'),(d.get('error') or {}).get('code'));[print('##',i['title'],'|',i['url'],'|',i.get('published_at'),'\n',(i.get('text') or '')[:1500]) for i in d.get('items',[])]"
- Concurrency: max 2 Reddit calls at once across ALL agents, searches start >=10s apart, the rest queue. Don't run calls in parallel yourself.
- Put the subreddit or "Australia"/"Adelaide" in the query to focus it.
- On RATE_LIMITED: wait retry_after_seconds, don't loop. On UPSTREAM_BROKEN: wait 2 minutes, try once more, then fall back.
- Reading a single thread (agent-reach read <reddit url>) is BLOCKED by Reddit here. Search results are your text.
## Fallbacks
- Arctic Shift archive comments search (slow, rate-limited): curl -s -m 60 "https://arctic-shift.photon-reddit.com/api/comments/search?subreddit=realtors&body=AI%20assistant&limit=25&fields=body,score,link_id"  (sleep 5 between calls)
- Exa: cd /tmp && timeout 90 mcporter call exa.web_search_exa query="..." objective="..." numResults=8
## Not available here: Facebook / Instagram / X (need a browser extension + login), YouTube transcripts (rate-limited).
