# 13 - Wildcards: strange, specific, under-copied AI plays in real estate

Researched 31 Oct 2026 (Exa search/fetch, Reddit). Honest note on evidence: most rare ideas are sold by vendors, so "results" are vendor claims unless I say otherwise. I mark each source as vendor claim, operator post, or official data. Several "results" pages looked marketing-fabricated and I flag them.

---

### 1. Council / DA / rezoning radar that turns planning news into listing conversations
- **What it does:** A scheduled job watches council agendas, minutes and development application registers (SA, plus other states). An LLM extracts the address, what is proposed, zoning change, unit count and stage. It matches this against the agency's database (past vendors, appraisals, neighbours within ~400-500 m, investors) and drafts a short "what this means for your street" note for the agent to approve and send, or letterbox.
- **Money:** Makes money. A rezoning or a DA next door is a natural reason to call 50-200 owners with something useful to say. It also finds developer-site and amalgamation listings before they hit the market (higher commission, off-market). No conversion numbers found. Any figure would be my estimate.
- **How rare:** Rare for agencies. Common for developers and brokers (tools exist), but I found no agency-specific build. This is the cleanest "nobody else in Adelaide does this" pitch I found.
- **Evidence:**
  - GoSiteHunt DA Watch: "A DA on a street is a listing conversation with every neighbour." Covers SA among other registers, so SA data access exists (vendor claim). https://gositehunt.com/da-watch
  - Agenda Insider reads every planning commission and council agenda with LLM pipelines. It lists "pitch owners before listings hit the market" as a broker use case (US, vendor). https://agendainsider.com/
  - Rostra Develop does the same, with parcel threading and relevance scoring (US, vendor). https://rostraiq.com/develop/
  - STRATUM claims weekly snapshots of 537 Australian LGAs and "91% rezoning probability". The claims are unverified and the page looks like an early-stage or possibly exaggerated product. Treat the numbers as unproven. https://withstratum.app/
  - Planning Alerts (free neighbour alerts) shows the data is public. https://planningalerts.com.au/
- **SA fit:** Strong. SA's PlanSA portal and council agenda PDFs are public. Adelaide infill (Housing Diversity, Greater Adelaide "Planning and Design Code" changes, Playford/Gawler growth areas) generates constant news. Compliance: use public data only, send under Spam Act rules (existing relationship or inferred consent, with unsubscribe). Check that PlanSA terms permit scraping or use the official feeds.
- **Build notes:** n8n or Make plus a scraper (Apify or Firecrawl) for council agendas, Claude to extract structured fields, then a geo-match against the CRM export. Draft emails or letters go to the agent for approval. Medium difficulty. The hard part is agenda coverage across ~19 metro councils. Start with the agency's 3-5 core suburbs.

### 2. "Likely to list" prospecting stack (portal propensity score + own-data score + AI outreach)
- **What it does:** Combines REA's Likely to List score (address-level, 0-99, uploaded to the CRM) with the agency's own signals (past appraisal, lease expiry on an investor owner, long tenure, DA nearby, email opens on market reports). An AI writes a personalised touch for each tier, and the agent gets a Monday "call these 15 owners" list.
- **Money:** REA's own data: roughly 1 in 3 "Very High" addresses list within 3 months, 1 in 8 "High", 1 in 24 "Medium" (REA internal data, 90-day window, official page). Even a modest edge over random farming is a big saving on letterbox and door-knock waste. The figure for the value of one extra listing is your estimate (commission x average price).
- **How rare:** Emerging. The REA tool is a beta limited to select suburbs. Almost nobody layers their own data and AI-written outreach on top.
- **Evidence:**
  - REA Likely to List, beta for select suburbs. https://customer.realestate.com.au/residential/likely-to-list/
  - Propic (Australian) markets AI prospecting built on the same idea. https://www.propic.ai/real-estate-prospecting
- **SA fit:** Check REA beta access for Adelaide suburbs through the agency's REA rep. Privacy Act: score files are enriched address data, so keep outreach to people with an existing relationship or use letterbox and doorknock channels.
- **Build notes:** Mostly a CRM export, a scoring sheet and an n8n flow. Low-medium. The value Lumen adds is the layering and the weekly call list, not the score.

### 3. Rent roll "about to walk" detector (landlord churn + sale-conversion)
- **What it does:** Reads PM software data (arrears, overdue inspections, vacancy days, fee complaints, tenure, last contact, owner emails with negative tone) and scores each landlord for churn risk. It also flags investors likely to sell (long hold, rent below market, big maintenance bill) so the sales team gets a listing lead. The BDM gets an alert and an AI-drafted check-in.
- **Money:** Rent roll is the agency's recurring-revenue asset, and its value rises with retention. A concrete clue: one Australian vendor's sample dashboard shows "For Sale by our Agency" as 45.2% of lost management reasons, followed by "For sale by competitor" at 12.9%. That means a big share of "churn" is a sale event, and a sale you win is also a listing. The vendor's sample also shows $202k lost vs $473k gained across 31/44 properties (demo data, not a real client). Rent roll sale multiples are my estimate territory, so I haven't quoted one.
- **How rare:** Emerging in AU (REcalibrate, OurProperty). Rare as a custom build tied to the sales team.
- **Evidence:**
  - REcalibrate: landlord happiness/risk tiers, revenue left on the table. https://recalibrate.au/
  - OurProperty tracks 40+ data points, colour-coded risk tiers. https://www.ourproperty.com.au/proactive-property-management-to-reduce-landlord-churn/
  - Vendor-tier claim only; no independent results found.
- **SA fit:** Works with PropertyMe/Console/PropertyTree exports. SA Residential Tenancies Act obligations (rent increase notice periods, inspections) are easy to wire as "overdue" signals. Compliance low risk (internal analysis of own client data), though the Privacy Act requires use consistent with the collection purpose.
- **Build notes:** CSV or API export, a scoring rubric, Claude to read email tone, Slack/Telegram alert. Medium.

### 4. Facebook community-group listener for movers and sellers
- **What it does:** Monitors suburb and community Facebook groups (local buy/swap/sell, "Adelaide Hills Mums", relocation and newcomer groups) and alerts the agent within minutes when someone says "thinking of selling", "relocating to Adelaide", "mum is moving into care, need to sell", "what's our house worth". An LLM scores intent 0-100, drafts a genuinely helpful reply with one local fact, and the agent posts it by hand.
- **Money:** Makes money by being first with a useful reply. No conversion data published. I found only product pages and a template, no case results.
- **How rare:** Rare. Exists as an off-the-shelf alert service (US) and as a DIY n8n template aimed at investors. Almost no AU agencies run it.
- **Evidence:**
  - Groups Watcher: 60-second alerts, 0-100 intent score, webhook into Zapier/Make/n8n. Lists examples like "Mom is moving into assisted living and we need to sell her house." https://www.groupswatcher.com/for/real-estate-agents
  - n8n template: scrapes 6 Facebook groups every 4 hours, GPT-4o extracts and classifies, Twilio SMS alert. https://n8n.io/workflows/15431-find-real-estate-deals-from-facebook-groups-with-gpt-4o-and-twilio-sms-alerts/
- **SA fit:** Weak-to-moderate. Scraping Facebook breaches Meta's terms of service, and the risk is on the agency's accounts. Safer variant: the agent joins groups and pastes or forwards posts, or uses a vendor that manages the risk. Do not auto-reply or auto-DM (Spam Act, group rules). Treat as an experiment, not a core offer.
- **Build notes:** Vendor tool plus webhook to n8n to Telegram and CRM. Low if bought off-the-shelf. Pitch caution: sell it as an add-on, not a headline.

### 5. Voice memo after the open home -> CRM notes + vendor update + buyer follow-ups, in one pass
- **What it does:** The agent speaks a 60-90 second voice memo in the car after an open home. AI transcribes it, splits it into: (a) a structured vendor feedback summary, (b) a personalised follow-up per hot attendee (using their sign-in details and what they said), (c) CRM notes and tasks, (d) a price-feedback tally for the weekly report.
- **Money:** Saves time and protects vendor relationships. Vendor-reporting vendors claim 3-4 hours saved per listing per week (AxonEstate) and ~4 hours/week for an agent with 8 listings (Saabai), both unverified vendor claims. I'd treat 1-2 hours per agent per week as realistic (my estimate).
- **How rare:** Emerging, with AU vendors (EstateOS, Hutly) and generic voice-note tools. Rare as a single flow wired to open-home attendee lists.
- **Evidence:**
  - Homesy playbook for voice notes into vendor reports, with controls (consent, human approval). https://homesyai.com/blog/voice-notes-to-real-estate-vendor-report
  - SalesMemo voice notes from viewings. https://www.salesmemo.sk/en/for-real-estate-agents
  - EstateOS vendor weekly updates: "Vendor communication is the most-skipped agent obligation." https://estateos.au/features/vendor-weekly-updates
  - AxonEstate: "Vendors don't withdraw because the price is wrong. They withdraw because they feel ignored." https://axonestate.com/vendor-reporting-agent/
  - Hutly's open-home follow-up: tracks interest level and flags hot buyers. https://hutly.com/how-sammy-works
- **SA fit:** Strong. Auction and open-home heavy market, vendors expect weekly feedback. Keep recordings of the agent only, not of buyers, to avoid SA surveillance-device and consent questions. Agent approves before anything is sent.
- **Build notes:** Telegram or WhatsApp voice note -> Whisper/Deepgram -> Claude -> AgentBox/VaultRE/Rex API or email drafts. Medium. Good fit for Lumen's existing Telegram experience.

### 6. AI buyer-to-listing matcher that emails the right 100-200 past enquirers within minutes of a listing going live
- **What it does:** When a new listing goes live, AI reads the listing, matches it against everyone who enquired or attended an inspection (not an old saved search), and emails a personal "why this one suits you" note in the agent's name. The listing agent then gets a vendor-ready results email: buyers reached, opened, clicked.
- **Money:** The vendor-facing report is itself a listing-win tool ("here's how many buyers we reached before the first portal enquiry"). Sample report: 184 buyers reached, 122 opened, 39 clicked (a demo sample, not a real client). Propic says 232K matches made for Australian agencies and 730K+ profiles behind the matching (vendor claim).
- **How rare:** Emerging. Propic is an AU product already doing this, so Lumen would be a custom competitor, not first. The twist that is rarer: pairing it with off-market and "coming soon" matching before portal launch.
- **Evidence:** https://www.propic.ai/ai-buyer-matching (vendor claim, AU). Hutly also lists prospecting and database reactivation. https://hutly.com/how-sammy-works
- **SA fit:** Spam Act: needs consent or an inferred relationship (enquiry counts as an inferred relationship in most readings, but keep unsubscribe and sender ID). Check the CRM actually holds permission-to-contact flags.
- **Build notes:** CRM export or API, embeddings for buyer profiles, Claude to write copy, email via SES or the CRM's own sender. Medium.

### 7. Past-client "home equity / suburb update" engine (Homebot-style) tuned for Australia
- **What it does:** A monthly personalised digest to every past client and appraisal contact: estimated value and movement, nearby sales, a one-line AI-written commentary. It tracks opens and clicks and flags "who's thinking of selling" (repeated value checks, clicks on "what is my home worth") so the agent calls only the hot ones.
- **Money:** Homebot claims: one US agent attributes about $30k+ commissions in six months to three clients who asked for their home value from digests, 78% open rate; others claim 58% engagement on 2,500 homeowners, 73-80% open rates. All are Homebot's own customer stories and are cherry-picked. Treat as directional only. Value for Adelaide is mostly in database nurture and referral.
- **How rare:** Common in the US, rare in AU in an agent-branded form. Most AU agencies do manual or generic market-update email.
- **Evidence:**
  - https://homebot.ai/customer-stories/homebot-generated-30k-in-less-than-six-months-for-this-real-estate-agent
  - https://homebot.ai/customer-stories/how-this-real-estate-agent-uses-homebot-to-connect-with-a-database-of-2500-clients
  - Reddit operator post: an agent used an AI agent to check in with 200+ ghosted past clients and reported 4 referrals in 3 months (unverifiable, possible promo). https://www.reddit.com/r/RealEstateTechnology/comments/1nrhzy6/i_tried_letting_ai_call_my_past_clients_to_checkin/
- **SA fit:** Needs an AVM source (PropTrack, Cotality, or a cheaper sales-data API), which costs money. Be careful with "estimated value" wording (misleading-conduct risk if presented as a valuation). Spam Act: consent and unsubscribe.
- **Build notes:** CRM + AVM API + Claude commentary + email platform with click tracking and n8n scoring. Medium-high mostly due to data licensing.

### 8. Suburb market-report content engine (SEO + letterbox + gated lead magnet)
- **What it does:** Every month, pulls sales data per suburb and has AI write a unique, factual suburb page and a printable one-page report. These feed the website (suburb pages), a gated download with an automated follow-up sequence, and a letterbox or email version for the farm area.
- **Money:** Vendors searching "[suburb] property market" are the lead source. A vendor claims people who download market reports are 60-90 days from selling (unverified vendor claim). Zero ad cost per lead once ranked.
- **How rare:** Emerging in AU among web design vendors (CoreWebHub, Humm&Buzz). Rare done well with genuinely local numbers.
- **Evidence:** https://corewebhub.com.au/services/real-estate-agents ; https://www.hummandbuzz.com.au/landing-pages/real-estate (vendor claims).
- **SA fit:** Conflict with Lumen's own rule: Lumen's SEO policy says do not template per-suburb pages without genuine local proof. This works only with real agency sales and data per suburb, so scope it to the agency's actual patch. Do not copy it for Lumen's own site.
- **Build notes:** Data source (sales API or manual feed), Claude to write with fixed fact blocks, human review, static page generator. Medium. Because Lumen builds websites, this is a natural upsell.

### 9. Listing pre-flight checker (photos, floorplan, description, compliance) before it goes live
- **What it does:** Before a listing is pushed to REA/Domain, AI checks: floorplan areas vs stated bedrooms/bathrooms, description vs photos (e.g. "pool" with no pool photo), virtual-staging or edited-photo disclosure, wording that breaches Australian Consumer Law (misleading price/"under offers"), missing Form 1 or required statements. It returns a pass/fail list to the agent.
- **Money:** Saves rework and protects against fines (SA Consumer and Business Services and ACCC attention on underquoting and misleading ads). I found no hard numbers.
- **How rare:** Rare in AU. In the US, California AB-723 (digitally altered images disclosure, effective 1 Jan 2026) created a market for checkers.
- **Evidence:**
  - Coraly Compliance Suite: detects altered/virtually staged images, drafts disclosure text, archives originals (US, vendor). https://coraly.ai/products/compliance-suite
  - Styldod Smart Media Module: compliance scan before publish (US, vendor). https://www.styldod.com/smart-media-module
- **SA fit:** No AB-723 equivalent here, but SA's Land and Business (Sale and Conveyancing) Act and ACL misleading-conduct rules apply. Pitch as risk reduction, not revenue. A principal who has been burned by a complaint will understand it instantly.
- **Build notes:** Vision model (Claude) over listing draft + photos, rules file written with the principal. Low-medium.

### 10. Sales progression chaser (contract to settlement) that flags sales going quiet
- **What it does:** Reads the live pipeline (days at current milestone, overdue finance/B&P/Form 1 items), flags the sales at risk of falling over, and drafts the chase to the conveyancer, broker or buyer for the sales admin to approve.
- **Money:** Saves admin hours and rescues fall-throughs (each lost sale costs the commission plus a relisting). No numbers found beyond the vendor pitch.
- **How rare:** UK: Alto Intelligence launched it in the main UK CRM. AU: emerging (Autopilot, ai-automation.au). Rare as a custom flow on AgentBox/VaultRE.
- **Evidence:** https://www.altosoftware.co.uk/alto-intelligence-get-to-exchange/ (drafts the chase, stops for human approval, uses real record data not generated facts). https://www.autopilot.com.au/ . ai-automation.au describes the milestone idea but is a generic vendor page. https://ai-automation.au/ai-automation-for-real-estate
- **SA fit:** SA specifics: cooling-off period, Form 1 timing, settlement via PEXA, conveyancers (not solicitors) usually run the contract. Human approval before any send.
- **Build notes:** Needs CRM API or a milestone spreadsheet, plus Gmail/Outlook drafts. Medium.

### 11. AML/CTF Tranche 2 compliance copilot (customer due diligence at listing and offer stage)
- **What it does:** From 1 July 2026 selling agents became AUSTRAC reporting entities. The tool collects ID and entity/trust documents at listing and offer, extracts and cross-checks the details, flags beneficial-ownership gaps and risk factors, and keeps a seven-year audit trail. A person (compliance officer) makes every decision.
- **Money:** This one is about avoiding penalty and admin time. Many small agencies have nothing yet. A deadline-driven problem is the easiest high-ticket sale: the principal must act and has no in-house expertise.
- **How rare:** Rare right now, because the obligation is new. Only generic vendor articles so far.
- **Evidence:** Solve8 summary of the obligations and the "AI structures and flags, a person decides" boundary. https://solve8.com.au/blog/ai-real-estate-agencies-aml-tranche-2-automation-australia/ . I did not verify AUSTRAC's own guidance in this pass, so the legal details need checking against AUSTRAC before quoting to the agency.
- **SA fit:** Directly relevant. Compliance risk is high: Lumen must not give legal advice or hold ID documents insecurely. Position as workflow and records, with the agency's compliance officer and lawyer owning the program. Privacy Act and secure storage in an Australian region.
- **Build notes:** Form intake + document extraction + checklist + encrypted storage. Medium-high because of data security.

### 12. Multilingual buyer handling (Mandarin / Hindi / Vietnamese) incl. Xiaohongshu and WeChat content
- **What it does:** Replies to enquiries and sends follow-up in the buyer's language, drafts Chinese-language listing posts for WeChat and Xiaohongshu (REDNote), and answers common questions (stamp duty, foreign buyer rules, auction process) in plain language.
- **Money:** Opens a buyer pool most local agents ignore. Fang.com.au sells translated listings from $350 per listing (inc. GST) and claims 1.4M registered members, 200K monthly active users (vendor claim). That price shows the service is valued and a self-run AI version could be cheaper.
- **How rare:** Rare for Adelaide agencies. Dubai has many tools: Reva (WhatsApp AI in Arabic, Hindi, Russian, English, Mandarin) and Ovie (Arabic and English).
- **Evidence:** https://agents.fang.com.au/ ; https://revaagent.com/ ; https://www.ovieai.com/ ; https://www.xaia.ae/industries/real-estate (Dubai voice AI with Do Not Call registry check, calling-hours rules).
- **SA fit:** Adelaide has meaningful Chinese and Indian communities and international students. Foreign Investment Review Board rules limit foreign buyers of established homes, so keep content general and accurate; have the agent confirm all legal statements. Machine translation of contracts is a risk: translate marketing, not legal terms.
- **Build notes:** Claude for translation with a glossary, WhatsApp/WeChat only where official APIs allow. Low-medium for content, high for WeChat messaging.

### 13. Maintenance triage and quote chasing for the PM department
- **What it does:** Reads tenant maintenance emails and photos, identifies the issue and urgency, creates a draft work order, requests quotes from the agency's preferred trades, compares them and presents the approval to the owner.
- **Money:** Saves PM hours (Wattle claims 15-20 hours a week, vendor claim). PMs are the agency's bottleneck, so reducing workload improves retention of staff and landlords.
- **How rare:** Common-to-emerging. Many products exist, so the wildcard is a custom version tied to the agency's own trades panel and owner approval thresholds.
- **Evidence:** Wattle Agent post (vendor, Feb 2025): https://www.reddit.com/r/PropertyManagement/comments/1imr8uj/launching_wattle_agent_for_property_maintenance/ . AI Maintenance Dispatcher with contractor pools and metrics: https://www.reddit.com/r/PropertyManagement/comments/1ljadrb/ai_maintenance_dispatcher/ . LORDLY (AU) does AI triage and video condition reports: https://www.lordly.com.au/ . For strata, StrataAI's maintenance agent has an autonomy dial (under $1,000 approve, bigger jobs to committee vote): https://strataai.app/
- **SA fit:** SA Residential Tenancies Act urgent-repair rules and timeframes must be respected. Never let AI decide urgent versus not without a rule-based override for gas, electrical, flooding and no-hot-water.
- **Build notes:** Email/Tapi/PropertyMe integration, Claude vision, trades panel list. Medium.

---

## Smaller or unverified ideas (brief)
- **Buyer-intent scoring from multiple open-home attendances:** products exist (Teylo, a free AU tool, scores views/saves/enquiries/inspection bookings https://agent.teylo.com.au/features/buyer-intent ; INTENTah, US, pre-launch https://intentah.com/ , which also flags "nearby resident" attendees as seller signals). Good small idea: "neighbours who attend your open home are your next listings". No results found.
- **AI call scoring and coaching:** QalyAI (Dubai) scores calls in Arabic and English with compliance flags https://qalyai.net/ ; MaverickRE (US). Could fit an agency with a sales-trainer mindset. Call recording consent required in SA.
- **Probate/estate leads:** US tools monitor court dockets (aramb, Probate Lead Source: "we close 1 in 4 probate leads", vendor claim). Not directly transferable: SA probate notices are public but thinner. Sensitive, so I would not pitch it.
- **Voice AI reactivating old leads:** Reddit operator claims 847 dead leads, 34% answered, 11 appointments in a week for under $400 (self-reported). Commenters flagged consent and legality problems. In Australia this hits the Do Not Call Register and Spam Act, so use text or email to opted-in contacts first. https://www.reddit.com/r/RealEstateTechnology/comments/1sgal90/i_built_a_voice_ai_followup_system_that/
- **UK "Hartley & Partners" case study** (3x valuation appointments, 51% instruction rate, 98% response): treated as marketing; no independently verifiable agency, so do not cite as proof. https://aisalesvoice.com/case-study-real-estate

---

## Best 3 from my angle
1. **Council/DA/rezoning radar (idea 1).** The most unusual, local, and easy to demo (show the agent a DA on their own street). It produces listing conversations from public data nobody else is reading. Weakness: no published conversion data, and agenda coverage takes real build effort.
2. **Rent roll churn + sale-conversion detector (idea 3).** Ties directly to the agency's most valuable recurring asset, and the vendor demo data suggests many "lost" managements are really sales events the agency could win. Easy to justify a high-ticket price against rent roll value.
3. **AML/CTF Tranche 2 compliance workflow (idea 11).** A hard deadline with penalties creates urgency that most AI pitches lack. Very few suppliers, but it carries the highest liability for Lumen, so it needs a legal partner or must be positioned strictly as workflow and records.

Runner-up: the open-home voice memo flow (idea 5) as an easy-to-deliver, low-risk first project that builds trust.

## Notable quotes
- "Vendor communication is the most-skipped agent obligation." EstateOS (vendor copy). https://estateos.au/features/vendor-weekly-updates
- "Vendors don't withdraw because the price is wrong. They withdraw because they feel ignored." AxonEstate (vendor copy). https://axonestate.com/vendor-reporting-agent/
- "Most agents had no system for leads older than 30 days, they'd just sit in the CRM going cold even though the agent already paid $8-15 to acquire each one." u/techtreon, r/RealEstateTechnology. https://www.reddit.com/r/RealEstateTechnology/comments/1sgal90/i_built_a_voice_ai_followup_system_that/
- "My biggest time suck is generating monthly statements and work orders by hand, as part of a statement package." u/girlbffrrr, r/PropertyManagement. https://www.reddit.com/r/PropertyManagement/comments/1lihtbw/commercial_pms_what_are_we_using_ai_for/
- "I'd love for it to do my PO's, track them, auto apply coding info to a received invoice and forward it to our pay system." u/dan3lli, same thread.
- "Extracting data from a bunch of pdf scans of contracts. Renewal dates, escalations, notice periods etc." u/lowresolution (ex-commercial PM), same thread.
- "A sale doesn't tell you it's in trouble. It just goes quiet." Alto Software (vendor copy, UK). https://www.altosoftware.co.uk/alto-intelligence-get-to-exchange/
- "Most inventory companies are terrible. The reports they generate are useless and cannot be used for something as straightforward as deposit dispute." u/RagerRambo, r/uklandlords. https://www.reddit.com/r/uklandlords/comments/1d1dufh/letting_agency_not_doing_their_job/
