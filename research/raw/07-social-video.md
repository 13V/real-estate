# 07 - Social video and creator content: what real estate / property management automations are being shown

Researched 31 Oct 2026. Tools: yt-dlp YouTube search (about 45 queries, view counts as at search time), Exa web_search / web_fetch (video descriptions and some transcripts, TikTok / Instagram / Facebook pages, vendor pages). No transcripts or logins; view counts for TikTok / Instagram / Facebook mostly were not retrievable, so popularity is measured on YouTube only. Anything I could not confirm is marked "unverified".

## 1. The saturation map (what everyone shows vs what almost nobody shows)

Pattern: view counts follow how generic the idea is. Generic "Claude / ChatGPT for agents" tutorials draw 50-120K views. The specific, operational ideas (PM dispatch, buyer-match alerts, lead-source audits) have 2 to 3,000 views. Low views here means "rare", not "bad".

### SATURATED (dozens of videos, every creator shows them) - mention only, don't pitch as special
| Automation | Examples (YouTube views at search time) |
|---|---|
| Claude / ChatGPT "for real estate agents" generic tutorials (listing copy, emails, social posts, skills) | Coffee & Contracts 76,430 (https://www.youtube.com/watch?v=oUIxPCagoQU); Zubair Trabzada property-analysis tool 53,298 (https://www.youtube.com/watch?v=Vc9I6q-yOiw); Mike Sherrard 52,084 (https://www.youtube.com/watch?v=jtyC-EBl9Eo); Andy Lo Claude Code RE ad workflow 56,081 (https://www.youtube.com/watch?v=iI_rAephmic) |
| CMA / property report with ChatGPT | Brendan Bartic 121,487 (https://www.youtube.com/watch?v=hae4u0_ivTk) |
| n8n / Make "AI real estate agent": lead qualification, property recommendations, follow-up email, WhatsApp bot | Eric Tech 29,156 (https://www.youtube.com/watch?v=2OD6MVPVVCg); Mike Seitz 21,337 (https://www.youtube.com/watch?v=Ly52XZiAoTA); AI Pathways 18,405 (https://www.youtube.com/watch?v=k32GdAFaZXo); Dementry WhatsApp 9,086 (https://www.youtube.com/watch?v=JO2VB7EqriM); 6+ more under 6K |
| Voice AI receptionist / speed-to-lead call (Vapi / Retell + n8n) | Anthony Ton 9,152 (https://www.youtube.com/watch?v=1euQ5QtGZlc); Mohit Tanwar "$2,800 outbound agent" 7,228 (https://www.youtube.com/watch?v=HPqdZjC3rEE); Mike Seitz, Brandon Upright, Efran, Anthony Shoosh (all 1-3K) |
| Database reactivation (SMS / voice to old leads), mostly GoHighLevel | GHL Wizard 5,176 (https://www.youtube.com/watch?v=MasQp-qoJFY); Austin Automates 4,502 (https://www.youtube.com/watch?v=8LDHDR5FzR8); Tech Tomlet 2,043; Josh Irwin ~1.6K |
| Listing photos to AI virtual staging / cinematic walkthrough video | Joel Van Beek 327,519 (https://www.youtube.com/watch?v=aMLKJQYr1Pk); Market U (Higgsfield + Kling) 110,895 (https://www.youtube.com/watch?v=ReASV_e1mwc); n8n versions at 260-507 views |
| Instagram comment-to-DM qualification bots (ManyChat / Make) | Mike Sherrard 11,505 (https://www.youtube.com/watch?v=BOI6n9DfyCc); Gannon Meyer 10,541; vendor case studies (Dezy, JS Tech Labs, Vasilkoff) |
| Marketing-collateral generators from one form | Nico "Steal my $2,000 automation" 95,919 (https://www.youtube.com/watch?v=FciK9Qq79Os) |
| AI "viral" TikTok pitch format: "Estate agents waste hours on every new instruction. This takes the photos and info, prices it against local sales, writes the listing, pushes it to Rightmove and Zoopla, and opens viewing slots. Comment below if you want a copy." | https://www.tiktok.com/@dan_automation.x/video/7634078992802286870 (same creator posts one for insurance, dental, gyms, accountants: it is a lead-magnet template, not a real-estate specialist) |

### EMERGING (a handful of serious creators; real operators)
- Claude-agent chains running a property management department (maintenance, vendors, owner approval, invoices).
- Claude Code / agent workspaces replacing node-based Make workflows for PM firms.
- Listing-intake "skills" that do the whole paperwork-to-CRM chain.
- AI inbox triage for PMs (needs attention / FYI / noise).

### RARE (almost no video coverage, tiny view counts)
- First-text new-listing buyer-match alerts (Sold By Systems, 2 views).
- Monthly lead-source ROI audit that tags closed deals by true origin (Sold By Systems, 7 views).
- Appraisal-defence comparable grid (one agent's own page).
- Failed / expired listing diagnostic call that asks WHY the listing failed.
- Rent-roll health / sale-readiness auditing (only discussed on a podcast, no automation shown).

## 2. Creators who claim client results (read with scepticism; none independently verified)
| Creator | Claim | Quality of evidence |
|---|---|---|
| Liam Tietjens (AI for Hospitality), https://www.youtube.com/watch?v=VFKNbQbRZPk | Property-management voice agent: ~21,000 calls/yr, ~1,500 human hours saved, "about $31,000 conservatively", AI costs "a couple hundred bucks a month"; says higher conversion because leads are called within seconds but "we didn't track that in the AI". Headline "$260,000" is multi-client / multi-build. Demo company is fictional ("Vamp Properties"), real client blurred. | Dashboard shown, client anonymous. Unverified. |
| Acel Cortex (Property Management AI), https://www.youtube.com/watch?v=T-GLHm120Kg and https://www.youtube.com/watch?v=cHZtgKYkKOc | Owns an ~800-unit US PM firm: "went from working over 60 hours down to 15 hours per week"; maintenance request "2 to 3 hours per request" manually vs "a couple seconds" to approve. | Own business, self-reported, but the strongest operator-level evidence found. |
| Smart Alex press release (voice AI, entering Australia Oct 2026), https://presswireau.com/releases/smartalex-brings-100m-voice-ai-success-to-australian-real-estate | London agency database campaign: 1,771 called in 5 days, 707 answered, 47 "positive outcomes", only 2 viewings booked; enquiries on homes worth GBP 33.6-40.2m; calls cost US$106; claims "approximately" GBP 504-603K potential fees at 1.5%. | Vendor PR. The 2 booked viewings is the honest number: potential, not realised. |
| Austin Automates GHL, https://www.youtube.com/watch?v=8LDHDR5FzR8 | Concrete company: 400 old leads -> 12 quotes in under 5 days; "$100K selling database reactivation". | Not real estate; self-reported. |
| REN AI client testimonial, https://www.youtube.com/watch?v=fDV9c46-zu4 | US agent: 12 leads, 1 listing appointment + 1 buyer in 2 weeks; US$1,000/mo ad spend; "one closing pays for this for an entire year". | Vendor-hosted testimonial, 6 weeks in. Early. |
| Ben Whetstone (eXp agent, Tampa), https://aiopsforrealestate.com/ | Listing intake 2-3 hrs -> 15 min; MLS entry 45 min -> generated; "100% success rate on properties appraising at value or higher since implementation"; monthly cost "$20 for Claude Pro" vs $3-5K assistant. | Self-reported, but the page publishes real (sanitised) skill files. Not a vendor. |
| Nico, AI Ranking, https://www.youtube.com/watch?v=FciK9Qq79Os | Sold the project-collateral automation "a couple of times for over $2,000". | Shows the price point for generic Make builds: low. |

## 3. Competitive reality in Australia (matters for pricing a high-ticket build)
- Alira (Perth), "AI coworker built for Australian real estate": Pro $69.99/month, agency plan custom, drafts only ("Nothing sends without you"), Australian data residency. https://www.usealira.ai , Instagram @usealira.ai (4,162 followers).
- Reel AI Australia, AI receptionist for property management (maintenance triage against your emergency rules, SMS for photos, writes to PM software), from $99/month. https://reelai.com.au/industries/real-estate/property-management
- SmartAlex (UK) launching in Australia, press release dated 16 Oct 2026: voice AI for instant enquiry response and database activation (link in table above). Short at https://www.youtube.com/watch?v=5NUJ-nOVTDw (3 views).
- PropertyMe "AiMe": Reply with AiMe (arrears / inspection / supplier email drafts), AiMe Comply (state-specific compliance Q&A), Bills AI (invoice extraction), and AiMe Connect (announced 9 Oct 2026) which lets PMs connect their PropertyMe data to Claude or ChatGPT to ask questions, produce reports and dashboards, flag stale jobs and brief the PM before an owner call. Read-only for now, Manage PM Advanced plan only. https://www.propertyme.com.au/blog/propertyme/our-biggest-step-in-ai-yet-aime-connect and https://www.propertyme.com.au/aime
- Mantis Property already sends automated weekly vendor reports (non-AI), so a plain "weekly vendor update" is table stakes in some Australian CRMs. https://www.youtube.com/watch?v=IZxUgXlWnbg . Rex also markets vendor reports + auto-reply (https://www.youtube.com/watch?v=kTewxlc5ihQ, not fetched).
- Mark Kentwell (Australian agency coach) is telling owners that the front door should be "voice AI mobile and landline" plus conversational chat bots, then AI triage -> discovery -> label buyers browsing / inspecting / offering. https://www.youtube.com/watch?v=S3zW3Svsg84 (144 views). He also has a Short called "An Australian AI platform just automated the entire property management operation. All of it." (https://www.youtube.com/shorts/7Hp0U6gre-w); the platform name was not retrievable.
- Implication: instant-reply, receptionist and read-only reporting are being commoditised at $70-$100 a month. A high-ticket build needs to be bespoke, multi-system, write-capable and tied to revenue or staff hours.

## 4. Ideas

### 1. Four-agent property-management maintenance chain with owner-approval gate
- **What it does:** Tenant request (email / text / portal) triggers agent 1 to read it, ask the tenant for photos and basic troubleshooting. Agent 2 picks a vetted vendor, gets availability and a quote. Owner / PM approves with one tap (Yes / Edit / Cancel). Agent 3 books the calendar, sends the entry notice and updates the PM software task. Agent 4 waits for the invoice, confirms completion with the tenant, and asks the PM to release payment. Each agent has one job; corrections ("wrong vendor") are saved to memory.
- **Money:** Saves PM time on the most repetitive workload in the department. Claim: "typical process is about 2 to 3 hours per request" manually vs a few seconds approving (Acel Cortex, self-reported). Same creator says weekly hours fell from 60+ to 15. Estimate for Adelaide: if a PM handles dozens of jobs a week, hours saved convert to either fewer hires or a larger rent roll per PM (more fee income per head). Not verified for Australia.
- **How rare:** Emerging. Two serious operators showing it (Acel Cortex 2,518 / 542 views; Liam Tietjens 2,323 views) but almost nobody building it in Australia. Voice-only receptionists are common; the vendor-dispatch and invoice-approval half is not.
- **Evidence:** https://www.youtube.com/watch?v=cHZtgKYkKOc (Claude running an 800-unit PM business, full walkthrough of the four agents and the approval step); https://www.youtube.com/watch?v=T-GLHm120Kg (three layers: intake -> intelligence -> execution, Gmail labels needs attention / FYI / noise); https://www.youtube.com/watch?v=7MQuYrnvPBw (Liam: voice + email AI, maintenance AI that "decides which contractor to dispatch", overnight log). Stack named: n8n or Make trigger, Claude, Gmail, Google Calendar, a text-message tool for entry notices, PM software with API access.
- **SA fit:** Software matters: PropertyMe, Console Cloud, Ailo, PropertyTree etc. have different API openness (not checked here). PropertyMe's AiMe Connect is read-only, so write steps may need email / task-inbox workarounds. Entry notices and urgent-repair timeframes come from the Residential Tenancies Act SA; the approval gate should hard-code those rules, and the agent should never close or pay anything itself. Tenant data falls under the Privacy Act.
- **Build notes:** n8n + Claude + Gmail/Calendar + SMS (Twilio / MessageMedia). Medium-high: the build is easy, the vendor list, owner spending limits and PMS integration are the work. Start by logging into Troy-controlled sandbox flows; shadow mode first.

### 2. "Overnight activity log" command centre for the agency (packaging idea)
- **What it does:** A single dashboard / morning email listing what the AIs did overnight (tenant leak handled, boiler job booked, 214 transactions matched). The PM or principal reviews exceptions only.
- **Money:** It is mainly a selling device that makes the automation visible and justifies a retainer; it also gives the principal a record to audit. No standalone dollar figure.
- **How rare:** Rare as a deliverable; most creators show only the workflow.
- **Evidence:** Liam Tietjens shows it on screen: https://www.youtube.com/watch?v=7MQuYrnvPBw . Ben Whetstone's "Transaction Monitor Daily" gives a numbered action queue and "gets smarter every run by logging what I actually acted on": https://aiopsforrealestate.com/
- **SA fit:** Good for principals who are licensed (Land Agents Act SA) and want visibility over a team. Careful with the accounting example: Liam's agent "reconciled 214 transactions". Trust-account reconciliation is heavily regulated for agents, so keep the AI to flagging, never posting.
- **Build notes:** Sheet / Supabase log written by each workflow, a simple page in Lumen's own web stack. Low-medium.

### 3. Database / rent-roll reactivation by voice or SMS, with a diagnostic script
- **What it does:** AI calls or texts the agency's old appraisal enquiries, past vendors, unsuccessful buyers, and landlords who enquired about management. It establishes intent, answers questions, and only hands over warm ones to the agent.
- **Money:** Best concrete numbers found: SmartAlex London campaign, 1,771 calls in 5 days, 707 answered, 47 positive, 2 viewings, US$106 cost, with GBP 33.6-40.2m of property interest. Austin Automates: 400 leads -> 12 quotes (concrete). Josh Irwin claims "$10k+" extra from a dead-lead list. Treat all as optimistic; the only realised result in the SmartAlex case is two viewings.
- **How rare:** Common as a concept (GoHighLevel crowd), rare in a sophisticated form. The clever part, from the AI IntelliCall expired-listing page: the call does not ask "still want to sell?" but "why did the listing fail?" (price, condition, marketing, access, financing) and writes it to the record: https://www.aiintellicallsolutions.com/expired-listings-ai-campaign (voice at US$0.23 a minute, per that page).
- **Evidence:** https://www.youtube.com/watch?v=8LDHDR5FzR8 ; https://www.youtube.com/watch?v=IP9uG1x7v4Y ; SmartAlex release above ; ClinchRev "AI calls day-of expiry" (https://clinchrev.com/for/real-estate).
- **SA fit (my inference, not from a source):** The Adelaide equivalents of "expired listings" are withdrawn listings, properties passed in at auction, and landlords whose lease with another agency is ending. Passed-in auction follow-up is a strong, local angle since auctions are common in Adelaide. Compliance risk is real: Do Not Call Register, Spam Act (consent for SMS), telemarketing calling hours and AI-voice disclosure. Calls to existing clients are lower risk than cold lists, but get this checked. SmartAlex is now entering Australia, so speed matters.
- **Build notes:** Vapi / Retell + Twilio AU number, n8n, CRM export (AgentBox / Rex / VaultRE). Medium. Offer as a fixed-fee campaign with a success fee.

### 4. New-listing "first text" to matched buyers before portal alerts
- **What it does:** Buyer opts in once with area, budget and must-haves. When a new listing is entered, the AI matches against the buyer database, texts only the right handful within minutes with the key facts and a viewing link, and logs the response.
- **Money:** Makes money by winning viewings and offers earlier and by showing vendors a hot buyer list. Cites the "21x more likely to qualify within 5 minutes" statistic attributed to Oldroyd / HBR (as quoted by the creator, not checked). No agency case study.
- **How rare:** Rare: one tiny channel (Sold By Systems, 2 views) shows it. Many Australian CRMs already have buyer matching, so the differentiated part is the AI-written, personalised, opted-in text, not the matching itself.
- **Evidence:** https://www.youtube.com/watch?v=xhlUFQZBNzQ
- **SA fit:** Spam Act consent is the key rule: buyer must have opted in, with unsubscribe. Works well with off-market / "coming soon" listings, which Adelaide agents use. Check what the CRM's own matching already does before pitching.
- **Build notes:** n8n + CRM API (Rex / AgentBox / VaultRE) + SMS. Low-medium.

### 5. Monthly lead-source audit ("where do your deals really come from")
- **What it does:** Nightly pull of closed and pending deals, AI infers missing lead sources from enquiry history and flags uncertain ones for a 2-minute human check, then a monthly sheet shows conversion by source, speed-to-first-response by source, and cost per signed client per channel.
- **Money:** Redirects marketing spend (portal upgrades, ads, signage) to channels that convert. The creator's line is "Your marketing budget is being allocated by memory and memory is the worst accountant you have ever hired." No result figures.
- **How rare:** Rare (7 views, one channel). Almost everyone sells lead generation; almost nobody sells measurement.
- **Evidence:** https://www.youtube.com/watch?v=kkgmP_w-7O4 . This also fits Lumen's existing Meta ads / tracking strength.
- **SA fit:** Matches agencies that spend on REA / Domain depth products and Meta ads. Data is internal, so low compliance risk.
- **Build notes:** n8n + CRM export + Google Sheet + Claude. Low. Good "foot in the door" retainer.

### 6. Listing intake end-to-end skill (one upload, one approval)
- **What it does:** Reads the signed listing agreement, pulls property data from public records, writes the description and remarks, renames and files the documents, creates the transaction, adds key dates to the calendar, and texts the agent a confirmation.
- **Money:** Claimed 2-3 hours down to 15 minutes per listing; the same agent says MLS entry takes 45 minutes manually. On Australian numbers: if a team lists 100 properties a year, 2 hours saved each is about 200 hours (estimate).
- **How rare:** Emerging. One agent publishes it as sanitised skill files; commercial agencies mostly sell the listing-copy fragment only.
- **Evidence:** https://aiopsforrealestate.com/ (Ben Whetstone, eXp agent, 45 production skills, page explicitly says it is not a course). Related: "Transaction Monitor Daily", "Showing Tour Builder" (builds a ShowingTime tour from saved favourites).
- **SA fit:** Translate to the SA process: exclusive agency agreement, Form 1 vendor statement, REA / Domain upload, auction or private-treaty paperwork. The browser-driving part (his MLS entry) is fragile and the portals' terms of use need checking. Keep a human approval step before anything goes live.
- **Build notes:** Claude Code / Cowork skills, or n8n + document parsing. Medium-high because of portal and CRM entry.

### 7. Appraisal-defence comparable grid (price protection)
- **What it does:** Generates an appraiser-ready comparable-sales grid with adjustments to support the contract price, sent to the valuer before the site visit.
- **Money:** Prevents deals falling over on a low valuation. The agent claims "100% success rate on properties appraising at value or higher since implementation" (self-reported, small sample, unverified).
- **How rare:** Rare: single mention.
- **Evidence:** https://aiopsforrealestate.com/
- **SA fit:** In Australia the equivalent is a lender / bank valuation shortfall on a sold property. Comparable data would come from CoreLogic / PropTrack / RP Data licences, so access and licensing are a constraint. Worth checking with Troy's contact whether valuation shortfalls actually happen in their market.
- **Build notes:** Claude + a licensed data feed. Medium, data licensing is the blocker.

### 8. Rent-roll health and sale-readiness audit (my synthesis; demand evidence only)
- **What it does:** Ongoing AI sweep of every tenancy: lease expiries, rents below market, overdue routine inspections, missing documents, arrears patterns, owners with open issues, with a ranked action list and a "rent roll cleanliness score".
- **Money:** The rent roll is the agency's saleable asset. Beau Miller (Australian PM operator, sold her business) says even when she thought she was sale-ready it "still wasn't as clean as I suppose it needed to be... it took about 2 years", and that they grew the roll by 60 properties during that time (https://www.youtube.com/watch?v=U06ErdOeAT8, Rent Roll Queen podcast, 18 views). No multiple or dollar figure was given; any valuation uplift is my estimate and must be checked.
- **How rare:** Rare as automation. PropertyMe's AiMe Connect now covers some of it (flag items stale for 30+ days, lease renewals, team workload) in read-only form, so this is a gap only if the build goes beyond reporting (draft the renewal, book the inspection, chase the document).
- **Evidence:** PropertyMe AiMe Connect example prompts (https://www.propertyme.com.au/blog/propertyme/our-biggest-step-in-ai-yet-aime-connect); US analogues: Upnex AI lease renewals (https://www.youtube.com/watch?v=W5qIP_93OBc, 35 views); DoorLoop AI inspections (https://www.youtube.com/watch?v=8iRxQJcQJGQ, 1,345 views).
- **SA fit:** Directly relevant to SA RTA compliance and rent-increase notice rules, which should be encoded as checks, not guessed. Draft-only for owner and tenant communication; Peter Lohmann specifically warns about using AI to write owner emails (see quotes).
- **Build notes:** Claude connected to PMS data (AiMe Connect where the agency is on Manage PM Advanced, otherwise exports) + n8n scheduled jobs. Medium.

### 9. Failed-listing and passed-in-auction diagnostic follow-up
- **What it does:** Triggers when a listing is withdrawn or passes in, with a short AI call or text to the vendor and to buyers who inspected, asking what blocked the sale, and logging reasons so the agent walks into the next conversation informed.
- **Money:** Win back the listing or the next appraisal. No Australian figures.
- **How rare:** Rare in Australia (my adaptation of the US "expired listings" script above).
- **Evidence:** US version: https://www.aiintellicallsolutions.com/expired-listings-ai-campaign ; ClinchRev https://clinchrev.com/for/real-estate . The auction angle is my inference, not from a source.
- **SA fit:** Auctions are common in Adelaide; consent and DNCR rules still apply. Vendors who just spoke to your agency are an existing-relationship contact.
- **Build notes:** Same stack as idea 3; trigger from the CRM listing status. Low-medium.

### 10. Instagram property-specific DM agent with human approval
- **What it does:** A comment on a listing reel triggers a reply and a DM conversation with context specific to that property (villa vs land), qualifies name, phone, budget and requirements, and routes hot leads for inspection booking. Option: replies go to the manager for approve / edit / reject before sending.
- **Money:** Faster first response on social leads; no hard numbers. JS Tech Labs says it runs on a client account with 100,000+ followers; Vasilkoff's results are qualitative.
- **How rare:** Common as a concept; the per-post context and approval path are the better versions.
- **Evidence:** https://jstechlabs.com/work/instagram-automation ; https://vasilkoff.com/portfolio/realestate-sales-workflow ; https://www.dezysolutions.com/case-studies/instagram-ai-lead-agent
- **SA fit:** Meta Business API only. Low priority for a local agency compared with portal enquiries.
- **Build notes:** ManyChat / Meta API + n8n + OpenAI/Claude. Medium.

### 11. Agent Workspace for PM firms (Claude Code replacing node workflows)
- **What it does:** One workspace centralising company data (emails, PMS exports, vendor list, policies) that an agent works across, instead of dozens of fragile Make / n8n nodes.
- **Money:** Lower build and maintenance cost per client; a creator says the same system sold to PM firms is now being built this way.
- **How rare:** Rare to emerging.
- **Evidence:** TikTok @sirakinb, https://www.tiktok.com/@sirakinb/video/7664786916872670477 ("Several months ago I posted a automation system that I built for a property management company using Make.com. That same system we're now doing for property management companies using Claude Code and Codex, moving away from the node-based workflows"). Peter Lohmann on OpenClaw instability and moving to commercial agents: https://www.youtube.com/watch?v=Mw2CKsZHs_o .
- **SA fit:** Hosting and data location need an answer (Alira advertises Australian data residency, so clients will ask).
- **Build notes:** Claude Code / Cowork, MCP connectors. Medium-high; reliability caution from Lohmann.

### 12. Commodity layer (brief, don't lead with these)
- AI receptionist and after-hours maintenance line (Reel AI from $99/mo; Weblo, MonkSpaces and others).
- Voice speed-to-lead calls and tenant enquiry qualification.
- Listing descriptions, social posts, virtual staging, photo-to-video.
- Generic chatbot and lead-qualification flows in n8n.

## 5. Things the creators say don't work (useful warnings)
- Peter Lohmann (runs a PM business): do not use AI to write owner emails; the bottleneck is usually process or policy, not tech; he stopped running OpenClaw because it kept breaking. https://www.youtube.com/watch?v=MZ0ped_d9wU , https://www.youtube.com/watch?v=Mw2CKsZHs_o
- Liam Tietjens: items like "AI legal risk detection" and insurance claim negotiation were hard to build and saved little time; the big wins were dispatch / maintenance voice, speed-to-lead, and an internal "AI co-founder". https://www.youtube.com/watch?v=VFKNbQbRZPk
- Ben Whetstone: automations that drive the browser to enter MLS data need a silent capability test and a manual fallback when Chrome is unavailable. https://aiopsforrealestate.com/

## Best 3 from my angle (for a high-ticket pitch)
1. **Four-agent PM maintenance chain with approval gate and overnight log (ideas 1 + 2).** The only automation shown by operators running real PM businesses, with stated hour savings, a clear approval design that handles risk, and a clear recurring-revenue story (PM fees). Few Australians are building it; the commodity receptionist products sit around it at $99/mo, which makes a bespoke dispatch + owner-approval + invoice layer the more defensible and higher-priced piece. Risk: PMS write access and RTA SA rules.
2. **Database / rent-roll reactivation with the failed-listing and passed-in-auction diagnostic (ideas 3 + 9).** The most measurable revenue play, with one credible set of numbers (1,771 calls, 47 positive, 2 viewings, US$106). Pitch it as a fixed-fee campaign with a success fee and honest expectations. Move fast: SmartAlex is entering Australia. Needs a compliance review (DNCR, Spam Act) first.
3. **Rent-roll health and sale-readiness audit (idea 8), anchored by the lead-source audit (idea 5).** Rare, fits the agency's most valuable asset, and avoids direct competition with PropertyMe's read-only AiMe Connect only if it takes actions and drafts. Evidence is weaker (podcast story + vendor move into the space), so it is my synthesis; the lead-source audit is the cheap first engagement that earns access to the data.

## Notable quotes
1. "Phone used to be ringing all the time, and we were constantly dealing with chaos, tenant complaints, owner complaints, and vendor coordination. It was just crazy." (Acel Cortex, 800-unit PM operator) https://www.youtube.com/watch?v=T-GLHm120Kg
2. "...the typical process is about 2 to 3 hours per request, just a lot of back and forth, a lot of admin work." (Acel Cortex on a maintenance request) https://www.youtube.com/watch?v=cHZtgKYkKOc
3. "I literally went from working over 60 hours down to 15 hours per week." (Acel Cortex) https://www.youtube.com/watch?v=T-GLHm120Kg
4. "...businesses are often making the mistake of solving process problems or even policy problems with technology." (Peter Lohmann, PM owner) https://www.youtube.com/watch?v=MZ0ped_d9wU
5. "...when the time actually came along that I'd made a decision that I wanted to sell, it still wasn't as clean as I suppose it needed to be ready to go. So, it was a pretty long journey. It took about 2 years." (Beau Miller, former Australian PM business owner, on selling her rent roll) https://www.youtube.com/watch?v=U06ErdOeAT8
6. "Buyers ring at 8pm and on Sundays, often to several agencies at once, and the first to pick up usually gets the viewing." (SmartAlex, vendor) https://www.youtube.com/watch?v=5NUJ-nOVTDw
7. "Cold calling till your brain melts, templated scripts, spray and prey marketing, waiting for your prop tech CRM to update. That era is dead." (Mark Kentwell, Australian agency coach) https://www.youtube.com/watch?v=S3zW3Svsg84
8. "Email blast to lead database: Skipped most days." (Ben Whetstone, in his "old way" list) https://aiopsforrealestate.com/

## Gaps and caveats
- TikTok, Instagram and Facebook posts surfaced through Exa had no reliable view counts; Facebook group threads found were mostly 2023-2024 US generalist threads and added nothing beyond the YouTube picture. No Australian agent Facebook posts with specifics were found.
- No YouTube transcripts were available; evidence is video descriptions and Exa page extracts (some of which include transcripts). Kentwell's Short on the "Australian AI platform" returned only its title.
- Most "results" above are creator or vendor claims. Treat dollar figures as marketing until a reference client is spoken to.
