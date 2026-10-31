# Social research hand-off (run on Troy's computer)

Paste the prompt below into a Claude Code session running on your own computer (Claude desktop app, Code tab).
It needs your computer because Facebook, Instagram and X only work with your own logged-in browser.

---

Clone or pull https://github.com/13V/real-estate (branch `claude/inspiring-bell-736hr2`) and read
`research/2026-10-31-ai-automation-opportunities.md`. It's research for Lumen adl (Adelaide) on niche AI
automations for an Adelaide real estate agency. Facebook, Instagram and X couldn't be searched from the cloud,
so fill that gap from here.

1. Install Agent Reach (https://github.com/Panniantong/Agent-Reach, v1.6+) and run `agent-reach setup`.
   Then `agent-reach add facebook`, `agent-reach add instagram`, `agent-reach add twitter`.
   If a search returns NEED_LOGIN, run `agent-reach login <channel>` and I'll log in myself in the window.
   Never ask me for passwords or cookies. Read-only: never post, like, comment or message.
2. Search (Australia and Adelaide first, then anywhere):
   - Facebook: public posts and groups of Australian agents and property managers discussing AI or automation,
     landlords complaining about property managers, vendors complaining about agents, AML ID checks since July 2026.
   - Instagram: automation agencies and tech-forward agents showing real estate AI builds; note which claim
     client results.
   - X: founders and operators posting real estate or property management AI results; Australian proptech.
   Queries to start with: "property manager AI", "real estate automation Australia", "rent roll", "AI agent
   real estate", "landlord switched agency", "AUSTRAC real estate", "Adelaide real estate AI".
3. For each finding, note: what the automation is, who's doing it, any results (mark vendor claims as claims),
   the URL, and whether it's already in our report. Prioritise ideas NOT in the report, and evidence for or
   against the report's top three (Rent Roll Protection, PM autopilot, appraisal-to-listing engine).
4. Write it to `research/raw/17-social-facebook-instagram-x.md`, commit and push to the same branch.
   Cite only URLs you actually saw. Don't include anyone's private details from private groups.
