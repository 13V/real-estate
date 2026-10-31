# Research tool sheet (Agent Reach, tested on this machine 31 Oct 2026)

Agent Reach is installed. In this cloud container some channels are blocked; use exactly these working routes.
Run commands from /tmp (cd /tmp first). Never create files anywhere except your assigned output file.

## 1. Web search: Exa via mcporter (WORKS, best general tool)
cd /tmp && timeout 90 mcporter call exa.web_search_exa query="<describe the ideal page in natural language>" objective="<what to rank first, what facts to pull>" numResults=8
Read full pages:
cd /tmp && timeout 90 mcporter call exa.web_fetch_exa urls='["https://...","https://..."]' maxCharacters=6000
Tip: Exa indexes Reddit, Instagram, Facebook, LinkedIn, YouTube, X pages. Put the platform in the query,
e.g. query="reddit thread where a real estate agent explains an AI automation that saved them hours".
For Instagram/Facebook/TikTok/LinkedIn (no login available here), Exa + WebSearch are the ONLY routes.

## 2. Reddit: Arctic Shift archive API (WORKS; reddit.com itself blocks this server)
RATE LIMITED: one request at a time, `sleep 3` between calls; on "Timeout. Maybe slow down" wait 10s and retry (max 4).
Posts (query= searches title+body, needs subreddit):
curl -s -m 60 "https://arctic-shift.photon-reddit.com/api/posts/search?subreddit=realtors&query=automation&limit=25&fields=id,title,score,num_comments,created_utc,selftext"
Title-only (lighter): ...&title=AI
Comments (body search): curl -s -m 60 "https://arctic-shift.photon-reddit.com/api/comments/search?subreddit=realtors&body=AI%20assistant&limit=25&fields=body,score,link_id"
Comments of one post: curl -s -m 60 "https://arctic-shift.photon-reddit.com/api/comments/search?link_id=<post id without t3_>&limit=50&fields=body,score"
Date filter: &after=2025-06-01 ; sort: &sort=desc
Post URL format for citations: https://www.reddit.com/comments/<id>
Pipe through `python3 -c` / `jq` (if present) to trim. Truncate selftext to keep output small, e.g. `| head -c 6000`.
If Arctic Shift is down, fall back to Exa with "reddit" in the query.

## 3. YouTube: search titles WORKS, transcripts BLOCKED
cd /tmp && timeout 60 yt-dlp "ytsearch10:<query>" --flat-playlist --print "%(title)s | %(view_count)s | %(url)s"
For a video's content use Exa web_fetch_exa on the YouTube URL (description) or search for a written summary.

## 4. Built-in WebSearch / WebFetch tools: also fine to use (load via ToolSearch "select:WebSearch,WebFetch").

## Not available here: Twitter/X CLI (needs cookies), Facebook/Instagram CLI (needs desktop Chrome), rdt (blocked).
