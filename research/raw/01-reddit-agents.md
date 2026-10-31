# 01 Reddit, sales agents' side: automation ideas for an Adelaide agency

Researched 31 Oct 2026 via Arctic Shift (Reddit archive), Exa and Reddit page fetches. Subs covered: r/realtors, r/RealEstate, r/RealEstateTechnology, r/AusProperty, r/AusPropertyChat, r/AI_Agents, r/n8n, r/automation, r/RealEstateAdvice, r/CommercialRealEstate. r/realestateinvesting and an Aussie "RealEstateAU" sub returned nothing useful.

## Read this first: how trustworthy is Reddit evidence here?

- r/realtors is hostile to AI and builders. Mods remove tech and vendor discussion ("Try r/RealEstateTechnology"), and top comments on "what would you automate?" threads are things like "You're here to sell something." Most "AI worked for me" posts are written by people selling an automation or a tool. Treat every number below as a vendor or builder claim unless noted.
- Genuine agents mostly say AI helps with the blank page (listing copy, vendor letters, market reports, tour schedules), not with replacing relationships. Commenters repeatedly warn about E&O insurance and liability when AI touches contracts.
- Australian consumer subs (r/AusProperty, r/AusPropertyChat) react badly to AI-sounding outreach ("Cool ad brother", "Written using AI"). A past-buyer complaint about 38 messages and four calls from a second agency after an EOI is a live reputational and Spam Act/Privacy Act risk for any outbound idea.
- The best AU-specific proof is not on Reddit. It is on Australian vendor sites (Aidan, Voqo, AxonEstate, AiVARE, Agent AI, Valenor), all marketing claims, none independently verified.

Ideas are ordered with the rarest and most Adelaide-specific first. Anything with no evidence of anyone doing it is marked "gap, no evidence of anyone doing it".

---

### 1. PM-to-sales "about to sell" signal engine (landlord sell-signals)
- **What it does:** Reads property management data (lease end and non-renewal, tenant vacating, owner complaints about rates or repair bills, repeated arrears, big maintenance quotes, rent reviews that show weak yield) and scores each landlord for likelihood to sell. High scores create a task for a sales agent with a talking-points brief (suggested appraisal range, recent street sales, vacant-possession vs tenanted pitch).
- **Money:** Each converted landlord is a listing plus a commission. An LJ Hooker PM head quoted by Real Estate Business says a typical referred sale averages about $15,000 commission and that she reports "145,000 in GCI" per quarter to sales from PM referrals. Also protects the rent roll: if the landlord sells to an owner-occupier you lose the management, so catching it early lets you list it yourself or find an investor buyer who keeps the tenant.
- **How rare:** Rare. The industry advice is manual ("keep them across all of that", a quick email between teams). I found no tool or case study that mines PM notes for sell-signals automatically.
- **Evidence:** REB "Perfect partnership: the untapped opportunity between PM and sales" https://www.realestatebusiness.com.au/industry/32334-perfect-partnership-the-untapped-opportunity-between-pm-and-sales (also cites NAB Performance Era 2026: PM and sales opportunities rated 64% and 68%). Automation itself: gap, no evidence of anyone doing it.
- **SA fit:** Strong for any Adelaide agency with a rent roll. Uses data the agency already owns (PropertyMe / Console / PropertyTree notes, ledgers, inspection reports), so Privacy Act risk is low (internal use, existing relationship). Keep it as an internal prompt to a human, not auto-outreach.
- **Build notes:** Medium. Nightly export or API pull from the PM system, an LLM to read free-text notes and classify, a scoring sheet, push to the sales CRM (AgentBox/VaultRE/Rex) as a task. n8n plus Claude. Difficulty depends on PM-software API access; PropertyMe and Console have APIs, PropertyTree and Ailo less clear (unverified).

### 2. Sales-to-rent-roll capture at contract (investor-buyer detection)
- **What it does:** When a sale goes unconditional, the system checks whether the buyer is an investor or "may rent it out" (from the contract, buyer questions at the inspection, or the sign-in sheet), then sends a human-sounding message with a rental appraisal offer, and creates a task for the PM business-development person with the settlement date. A second branch reverses it: recently managed tenants who ask about buying get routed to the sales team.
- **Money:** Every captured management is recurring PM fee income plus letting fees and future sale rights. LJ Hooker's Cathie Crampton says to introduce the PM team "at the very point of viewing" and again at contract. This automation makes that consistent. (Value per management in $ not sourced; estimate only.)
- **How rare:** Rare as an automation. The behaviour is known and preached; I found no reports of it being automated.
- **Evidence:** Same REB piece as above; REB "Why buyer's agents are becoming central to the battle for rent rolls" https://www.realestatebusiness.com.au/property-management/31212-why-buyer-s-agents-are-becoming-central-to-the-battle-for-rent-rolls . Automation: gap, no evidence of anyone doing it.
- **SA fit:** Very strong; this is the sales-to-PM bridge most agencies leak. Buyer consent is simple because it is part of the transaction relationship. Add AML/CTF data from idea 7 so the same intake feeds both.
- **Build notes:** Low to medium. Trigger from CRM stage change, a short questionnaire (text or email), an LLM to draft the message, and a PM-system lead.

### 3. Post-auction and passed-in recapture (underbidders, registered-but-didn't-bid, open home attendees)
- **What it does:** At the hammer or pass-in, the agent taps the result into a form. The system flags underbidders for an immediate agent call, sends same-day personalised messages to registered non-bidders, sends a market-context message to open home attendees from that campaign, and starts a vendor-debrief and referral sequence. Matches each underbidder to live and coming-soon stock.
- **Money:** Voqo argues one auction should generate three to five listing conversations in 48 hours; underbidders are motivated buyers who often also own a property to sell. A Reddit agent says underbidder letters are underused: "Most agents don't send one at all." No conversion numbers are given (vendor claims only).
- **How rare:** Emerging, and Australian-specific (US MLS-style sales do not have auctions). Only one vendor (Voqo) is explicitly pitching it.
- **Evidence:** Voqo "Post-auction follow-up" https://www.voqo.ai/blog/post-auction-follow-up-real-estate ; r/AusPropertyChat https://www.reddit.com/r/AusPropertyChat/comments/1s0lk3o/i_tracked_every_writing_task_i_do_as_an_agent_for/ (underbidder letters and vendor update letters). Reddit sentiment on AI-written outreach to buyers is negative, so keep a human voice and callback.
- **SA fit:** Excellent. Adelaide is auction-heavy, especially eastern and inner suburbs. Contact only people who registered or attended (existing relationship), include opt-out, check Spam Act consent and DNCR before calls.
- **Build notes:** Low to medium. Form or WhatsApp command to log result, CRM tags, SMS via Twilio or Message Media, LLM drafting, callback alert to the agent.

### 4. Vendor "anxiety" report plus churn-risk flag
- **What it does:** Every Friday (or Wednesday) it pulls enquiries, inspection attendance and feedback from the CRM, adds REA/Domain stats and recent comparables, and drafts the vendor update in the agent's voice. It also flags listings where the pattern says the vendor is about to withdraw or switch agent (drop in enquiries, no price conversation yet, long time since last call).
- **Money:** Saves the weekly-report writing time (vendors quote 3 to 4 hours per listing per week in AxonEstate's marketing, unverified). The real value is retaining listings that would otherwise go to a competitor.
- **How rare:** Emerging. There are free n8n templates and a few AU vendors, but the "flag churn risk" layer is not in the ones I saw.
- **Evidence:** n8n template for weekly vendor updates https://n8n.io/workflows/21103-draft-weekly-vendor-update-emails-with-google-sheets-openai-and-gmail/ ; n8n community 5-workflow set including weekly seller report https://community.n8n.io/t/real-estate-follow-up-on-one-google-sheet-5-n8n-workflows-from-first-enquiry-to-weekly-seller-report/318764 ; AxonEstate vendor reporting https://axonestate.com/vendor-reporting-agent/ ; Reddit agent: vendor update letters are "where AI saves the most time" (AusPropertyChat link above). Also Aidan lists "vendor and landlord updates": https://www.callaidan.com/case-studies/real-estate .
- **SA fit:** Strong. REA and Domain agent dashboards plus portal emails are the data source; no public API, so the build may rely on email parsing or manual CSV from the portal (unverified, check feasibility). Always draft-for-approval, never auto-send price advice.
- **Build notes:** Medium. n8n, Claude, Gmail/Outlook drafts; portal-stat ingestion is the hard part.

### 5. Dormant database reactivation ("still looking, or should I close your file?")
- **What it does:** Finds contacts untouched for 60+ days (buyers, vendors who never listed, old appraisals, past clients). It sends one low-friction text, classifies replies with an LLM, and pushes interested people back into the CRM as hot tasks with a conversation summary. Optional second step with a voice AI.
- **Money:** Builder claims: a Texas 3-agent team got 11 appointments in week one from 847 dead leads for under $400; another builder says 14 appointments in week one from the text "are you still looking... or should I close your file?" on a 2,100-lead list. In Australia, Aidan claims 934 dormant leads reactivated and 75 appraisals booked across 20 agencies for $2,549 spend (vendor figures, not verified).
- **How rare:** Common in pitch decks, but still rare as an actually-running system in a typical Adelaide agency. Low novelty for Lumen; the angle is doing it well and legally.
- **Evidence:** https://www.reddit.com/r/RealEstateTechnology/comments/1sgal90/i_built_a_voice_ai_followup_system_that/ (commenters flag consent and legality); https://www.reddit.com/r/AI_Agents/comments/1uqtvt9/stop_building_agents_that_find_new_leads_build/ ; https://www.callaidan.com/case-studies/real-estate ; poster "foundersre" says 200+ ghosted past clients led to 4 referrals in 3 months https://www.reddit.com/r/RealEstateTechnology/comments/1nrhzy6/i_tried_letting_ai_call_my_past_clients_to_checkin/ (commenters call the account fake, so low trust).
- **SA fit:** Compliance is the whole game. Spam Act requires consent for commercial SMS/email (inferred consent from an existing relationship can work, but must be recent enough and include unsubscribe); outbound AI voice calls need DNCR checks and AI disclosure. Start with SMS and email to people who gave consent in the past.
- **Build notes:** Low to medium. n8n/Make, CRM API, Twilio, an LLM classifier. Voice via Retell or Vapi adds cost and risk.

### 6. Contract-to-settlement timeline and client updates (SA flavour)
- **What it does:** Upload the signed contract and Form 1. The AI extracts cooling-off end, finance and building-inspection deadlines, deposit date, and settlement date, builds a timeline, and sends scheduled updates and reminders to buyer, seller, conveyancer and broker. The agent approves the timeline first. A shared link means fewer "any update?" texts.
- **Money:** Saves agent and sales-admin hours chasing and answering status questions; protects the commission by catching finance and condition deadlines before a sale falls over. Time saved is unquantified in what I found.
- **How rare:** Rare in Australia. A US startup (Clienti) launched a free beta in Oct 2026 with 30+ agents and 150+ contracts; US agents on r/realtors were sceptical (E&O liability, "my TC handles this instantly").
- **Evidence:** Clienti announcement, r/RealEstateTechnology https://www.reddit.com/comments/1xjxc0i ; skeptic thread https://www.reddit.com/comments/1vlah36 (comment: "This would create significant liability if agents rely on automation instead of actually reading the contract").
- **SA fit:** Medium to strong. SA has a cooling-off period and agents commonly chase settlement progress through conveyancers. Needs SA-specific rule tuning. Present it as a reminders and comms layer, not legal advice.
- **Build notes:** Medium. PDF extraction with Claude vision, human review step, calendar and SMS/email scheduling. Keep a log for liability.

### 7. AML/CTF Tranche 2 onboarding and record-keeping workflow
- **What it does:** When a listing or buyer is engaged, the system collects customer details by secure link, runs identity verification, records beneficial ownership questions, flags politically exposed persons or unusual signals for human review, and stores the evidence with the deal and a retention timer. It then produces an audit-ready compliance file.
- **Money:** Mostly cost and risk avoidance, but it is a legal obligation from 1 July 2026 that many small agencies will find painful. Compliance tooling is paid per transaction: PEXA Clear is $40 + GST per transaction for individuals and from $65 + GST for businesses, so a workflow that cuts staff time per file can be sold on a retainer.
- **How rare:** Emerging, and time-limited. PEXA Clear and VeroID (a Document Verification Service gateway) provide the identity and risk checks. The gap is the glue: collecting data, chasing clients, linking to the CRM, and producing the file. No evidence of anyone selling that glue to agencies yet.
- **Evidence:** AUSTRAC real estate designated services page https://www.austrac.gov.au/new-austrac/designated-services-newly-regulated-entities/real-estate-designated-services ; PEXA Clear pricing https://cfotech.com.au/story/pexa-clear-opens-for-property-aml-compliance-ahead ; VeroID launch https://itwire.com/business-it-news/security/brisbane-brothers-bring-a-new-identity-verification-alternative-to-businesses-navigating-tranche-2 ; AUSTRAC factsheet https://www.austrac.gov.au/sites/default/files/2025-07/AMLCTF_obligations_factsheet_for_tranche_2_REs.pdf .
- **SA fit:** Applies to every SA agency. Lumen must not give legal advice; position as a workflow built on the agency's compliance officer's procedures. High trust and data-security burden (identity documents).
- **Build notes:** Medium to high. Secure form, DVS-gateway API, CRM tasking, encrypted storage. Reputational risk if mishandled.

### 8. Pre-appraisal intelligence brief plus lost-appraisal recapture
- **What it does:** When an appraisal is booked, the system produces a one-page brief at 6am the morning of: street-level sales, competing stock and days on market, likely buyer pool count from the agency's own database, and a draft deck. After the appointment, if the vendor goes quiet or lists elsewhere, a timed follow-up sequence keeps the agency in the conversation.
- **Money:** AxonEstate claims 2 to 3 hours saved per pitch and +25% appraisal-to-listing (marketing claim, no independent evidence). Valenor says automated appraisal scheduling at Mallison Real Estate (Perth) cut booking from 2 to 3 days to the same call, and claims a doubled conversion rate and 15 hours/week saved (case study by the vendor).
- **How rare:** Emerging in AU. Several vendors (AxonEstate, AiVARE, Insitive) sell parts of it, but the "lost appraisal recapture" and database buyer-pool count are less common.
- **Evidence:** https://axonestate.com/listing-presentation-prep-agent/ ; https://aivare.com.au/tools/pre-listing-kit ; https://www.valenor.com.au/case-studies/mallison-real-estate . Reddit evidence: a vendor on r/AusPropertyChat complains that other agencies call within days of an appraisal ("How do real estate agents you've never spoken to know you've had an appraisal done?") https://www.reddit.com/r/AusPropertyChat/comments/16xos5o/ , which shows speed matters but also that the practice annoys people.
- **SA fit:** Good. Sales data from CoreLogic/PropTrack licences the agency already has; check licence terms for automated use. Do not scrape portals.
- **Build notes:** Medium. Calendar trigger, comps via licensed data, LLM brief, Google Slides or Canva deck draft.

### 9. Withdrawn / expired / stale listing monitor (competitor-listing prospecting)
- **What it does:** Watches the agency's target suburbs for listings that disappear, get withdrawn, show long days on market or repeated price drops, enriches the owner from licensed data, and drafts a respectful, personalised first touch for the agent to approve.
- **Money:** A US agent (Neuhaus Realty Group) describes a full system for expired listings running 24/7. Another US builder reports over 10% of expired-listing owners willing to chat after AI text outreach (small sample, 2024). Dollar results not given.
- **How rare:** Emerging in the US. In Australia, I found no one doing it publicly.
- **Evidence:** https://neuhausre.com/ai-seller-outreach-automated-expired-listing-prospecting/ ; https://www.reddit.com/r/n8n/comments/1jnxuyb/realtor_question/ (agent asking how to build exactly this) ; https://www.reddit.com/r/RealEstateTechnology/comments/1cbij56/do_you_reach_out_to_expired_listings_i_created_an/ . Australian privacy backlash example: https://reddit.sentinel-team.org/posts/1tpotsv/snapshots/2026-05-29T21%3A54%3A48.796327Z (ex-agent and consumers describe id4me/CoreLogic-based prospecting and complaints to ACMA/OAIC).
- **SA fit:** Highest compliance risk of the list. Portal data cannot be scraped without breaching terms; owner contact data from CoreLogic has legal limits under the Privacy Act and Spam Act. Safer variant: monitor for human review and send physical letters, not SMS.
- **Build notes:** Medium to high; legal review needed first.

### 10. "Sold ripple": every sale triggers neighbour and database outreach
- **What it does:** The moment a sale is unconditional, it builds a 200 to 500m target list, cross-checks the agency's database for owners and buyers in that zone, drafts a "just sold" SMS, email and letterbox card with the result and local context, and tracks replies as appraisal leads.
- **Money:** Agent AI (an Australian vendor) claims a single sale can generate 5 to 15 inbound appraisal requests in 90 days. No independent figures.
- **How rare:** Emerging. The tactic is old; the automated multi-channel trigger is still uncommon.
- **Evidence:** https://www.agentai.com.au/just-listed-just-sold-marketing-real-estate/ . Reddit shows neighbours find door-knocking after a sale odd but understood as pipeline building: https://www.reddit.com/r/AusPropertyChat/comments/1km4ndf/real_estate_agent_knocking_on_door_to_share/ .
- **SA fit:** Good for Adelaide suburbs. Use letterbox for non-database owners; Spam Act applies to SMS and email.
- **Build notes:** Low to medium. CRM trigger, address radius via Google Maps or open data, print vendor for cards, Twilio.

### 11. AI-visibility (GEO) tracker and fixer for agents
- **What it does:** Each month, it runs a fixed set of prompts ("best real estate agent in [suburb]", "who sells in [suburb]") across ChatGPT, Perplexity and Google AI Overviews, logs which agents, sources and domains are cited, and gives the agency a short action list (reviews, Google Business Profile, local press mentions, directory listings, schema).
- **Money:** A new lead channel: a US agent reports that a buyer asked ChatGPT for the top agents in the county and the agent's name never appeared despite 80+ Google reviews. No conversion numbers. This is a natural retainer for Lumen's SEO work.
- **How rare:** Emerging. Agents are asking how to track it; one commenter's sceptical view is that results vary run to run, so the repeatable-prompt, logged-out method matters.
- **Evidence:** https://www.reddit.com/r/realtors/ thread id 1vrrafp (also at https://www.reddit.com/comments/1vrrafp ), "Anyone tracking whether they actually show up when someone asks ChatGPT/Google AI Overview for a realtor recommendation?" 15 comments, the thread concludes third-party citations (local press, directories) matter most.
- **SA fit:** Good: Lumen already sells SEO. Adelaide's smaller market means a few citations can move results. Low compliance risk.
- **Build notes:** Low to medium. Scheduled prompts via API or browser automation, LLM to parse citations, a dashboard or monthly PDF.

### 12. Voice-note capture at inspections and open homes to CRM, feedback and vendor report
- **What it does:** The agent records a 30-second voice note after each open home or private inspection. The system transcribes it, extracts buyer feedback, price signals and follow-up tasks, writes notes to the CRM contact, and feeds the weekly vendor report (idea 4).
- **Money:** US agents report it saves note-taking and prevents forgetting who liked what; an RLP team says AI generally saves "probably 10-20 hours per month" for them. Value comes from cleaner follow-up and better vendor feedback rather than a single big win.
- **How rare:** Emerging. Plaud and Willow Voice are named by agents; the CRM-specific, AU-flavoured feedback loop is rarer.
- **Evidence:** https://www.reddit.com/r/RealEstate/comments/1rmjccw/started_recording_voice_notes_during_house/ ; https://www.reddit.com/r/realtors/comments/1rix5md/my_toolkit_as_an_agent_who_works_exclusively_with/ ; https://www.reddit.com/r/realtors/comments/1lws0gh/how_do_you_use_ai_as_a_realtor/ .
- **SA fit:** SA recording laws need care: recording a private conversation generally needs consent, so record the agent's own summary, not the buyer's speech. Fits the inspection feedback agents already collect.
- **Build notes:** Low. WhatsApp or phone voice note to n8n to Whisper/Claude to CRM API.

### 13. Post-settlement reviews, referrals and anniversary loop (brief; common)
- **What it does:** A sequence at settlement, one month, and annual equity check-ins; reviews requested the day after closing with a direct link.
- **Money:** A Reddit comment quotes a National Association of Realtors (NAR, US) survey: 87% would use their agent again, but only 12% do (unverified, repeated by a commenter). An agent on r/realtors says he lost three past buyers to other agents this summer after not staying in touch.
- **How rare:** Common; most CRMs offer it.
- **Evidence:** https://www.reddit.com/comments/1wps7o2 ; https://www.reddit.com/comments/1wpsbsw ; https://www.reddit.com/r/realtors/ builder post 1w49q2d ("review request the day after closing").
- **SA fit:** Easy. Cheap add-on, not a headline.
- **Build notes:** Low.

---

## Obvious or already-known items (mentioned only briefly)
- Missed-call text-back, instant lead replies, website chatbot filtering, 5-minute lead response claims (the "21x" figure circulates on AusPropertyChat but I could not verify its source).
- Inspection confirmation and reminder SMS (an AU/Melbourne agent claims it removed no-shows; the thread was mocked as an ad) https://www.reddit.com/r/AusProperty/comments/1mbdar6/real_estate_agents_how_much_time_are_you_wasting/ .
- Listing descriptions, social posts and email drafting in ChatGPT (claims of 3-4 hours/week from one US interview: https://accessible.beehiiv.com/p/interview-with-missy-plunkett-how-a-top-realtor-and-business-owner-uses-chatgpt-in-real-estate, 2024).
- Buyer-to-listing matching and new-stock alerts (an agent's son built it in Make + Airtable; a commenter said the MLS already does it; in AU, the CRM and portal alerts already cover most of it).

## Pain points and wishes that aren't yet an idea (for reference)
- Duplicate data entry across MLS/CRM/Drive, signatures and file naming, tours across multiple calendars, weekly seller updates (r/RealEstateAdvice thread).
- "Make everything work together" after a listing is entered: one button to push to portals, socials, CRM, vendor comms. Gap with a broad promise: one "listing launch" orchestration that triggers all the downstream steps from a single intake form. Gap, no evidence of anyone doing it at agency level in AU; related to what the CRMs offer in pieces.
- PM workload: a property manager can face 100-150 properties each; in Queensland routine inspections mean up to 600 a year per PM (REB). PM automation belongs to other agents' angles, but idea 1 and 2 turn PM data into sales revenue.

---

## Best 3 from my angle

1. **PM-to-sales "about to sell" signal engine (idea 1).** Rarest, uses data the agency already owns, produces listings and protects the rent roll. A strong high-ticket story because the owner can see the dollar link (listing commission, about $15k average referred sale per the LJ Hooker quote). Gap, no evidence of anyone doing it. Pair with idea 2 as one "rent roll and sales flywheel" package.
2. **Post-auction and passed-in recapture (idea 3).** Adelaide is auction-heavy, the moment is time-critical, and the only competitor I found is Voqo's blog pitch. Easy to demo with a real campaign result.
3. **AML/CTF Tranche 2 onboarding workflow (idea 7).** A legal deadline already passed (1 July 2026), so agents have budget and urgency, and the tools (PEXA Clear, VeroID) leave an integration gap. Sell it as compliance plus time saved; needs careful scoping and a compliance sign-off from the agency.

Runner-up for proof of results: dormant database reactivation (idea 5), which has the most numbers but the most competition and compliance risk.

## Notable quotes

1. "Make everything work together. Make stuff easy. I don't want to be a freaking programmer. I sell houses. Give me a push button when I input a listing that will make it go and do everything needed. Reinventing the wheel every dang time is stupid." r/realtors https://www.reddit.com/comments/1tnm0vq
2. "Scheduling pinball, duplicate data entry, and paper-chasing wins for me: entering the same info into MLS/CRM/Drive, wrangling signatures/file names, coordinating tours across five calendars, weekly seller updates, and hunting receipts." r/RealEstateAdvice https://www.reddit.com/r/RealEstateAdvice/comments/1noffiq/least_favourite_admin_tasks_as_a_re/
3. "This is now the third past buyer client just this summer that I've found out sold with someone else and then bought with that same agent." r/realtors https://www.reddit.com/comments/1wps7o2
4. "A lot of these leads said they never heard back after the first call. They weren't dead at all, they just fell through the cracks of a manual process." (builder post) r/RealEstateTechnology https://www.reddit.com/r/RealEstateTechnology/comments/1sgal90/i_built_a_voice_ai_followup_system_that/
5. "Underbidder letters are underrated. Most agents don't send one at all." r/AusPropertyChat https://www.reddit.com/r/AusPropertyChat/comments/1s0lk3o/i_tracked_every_writing_task_i_do_as_an_agent_for/
6. "asked the same question three times in one day and got three different names, none of which were mine." (on AI recommendations of local agents) r/realtors https://www.reddit.com/comments/1vrrafp
7. "Some agencies just burn & churn their staff, by not having enough support staff." (on property manager workloads) PropertyChat https://www.propertychat.com.au/community/threads/more-than-150-properties-by-a-pm-is-it-normal.66549/
8. "This would create significant liability if agents rely on automation instead of actually reading the contract." (agent warning on contract-reading AI) r/realtors https://www.reddit.com/comments/1vlah36
