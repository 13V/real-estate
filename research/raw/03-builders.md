# 03 - What automation builders are selling to real estate clients (Reddit, n8n community/templates, vendor sites)

Researched 31 Oct 2026 via Exa (Reddit threads, n8n.io/workflows, n8n community, vendor pages). Arctic Shift was flaky (timeouts, empty results), so most Reddit evidence came through Exa full-thread fetches. Where I only saw a search snippet and not the full thread, I say so. Most "I made $X" posts are self-reported and unverified; several look like lead-gen for the poster's own product. I mark these.

## Headline findings (read this first)

1. The loud, saturated stuff is speed-to-lead, AI receptionists and "full lead-to-contract" systems. The builder threads about them are full of "Workflow" comment-bait, pushback ("this flow doesn't even work", "fake as shit ad") and builders with zero paying clients. Reps selling these to agents report poor close rates (1 sale from 40 calls at $5k).
2. The quiet, credible money is in **property management back-office** (inbox, arrears, maintenance dispatch, lease and document ingestion). There are working Australian vendors already (RealBud, Simplify AI (NSW), FlowWorks), which proves demand and gives a script for the pitch. They are mostly "draft, a human approves", which is also the compliant design.
3. The most common cause of churn is not price. It is **non-adoption** (nobody opens the dashboard, agents won't download another app) and **silent breakage** (webhook dies, nobody notices for 4 days). Anything that lives in email, SMS or the existing CRM and needs zero behaviour change survives; anything that adds a login dies.
4. Real pricing sits well below "high ticket" for single workflows: roughly $450 to $4,000 setup and $300 to $800 per month. The high-ticket examples are **bundles with a measurable revenue outcome** ($3,000 setup + usage with a claimed $96k commission outcome; $12,000 AU PM-agency project with claimed $91k labour savings). The pitch for Troy is a priced bundle tied to rent-roll economics, not one workflow.

## Pricing seen (what builders and vendors actually charge)

| Source | What | Price | Notes |
|---|---|---|---|
| r/Entrepreneur https://www.reddit.com/r/Entrepreneur/comments/1ombt5d/made_450_automating_some_realtors_lead_responses/ | Webhook + auto-reply + Sheet + SMS alert for one realtor | $450 one-off | Claimed one $12k commission lead. Commenters said he undercharged; suggested $99/mo SaaS or $999/mo zip-code exclusivity. |
| r/AI_Agents https://www.reddit.com/r/AI_Agents/comments/1u8m13n/i_automated_a_real_estate_teams_entire_lead_flow/ | Zapier + GPT lead reply for 4-person team | $4,000 build + $800/mo | Sold to 3 more teams after referrals. Lessons list below. |
| r/n8n_ai_agents https://www.reddit.com/r/n8n_ai_agents/comments/1o3o2sh/an_ai_sdr_call_center/ | Retell AI caller: new leads + old-lead revival | $3,000 setup, no retainer, monthly usage fees | Claims 14 seller appointments in 3 months, $96k commissions. Self-reported. |
| r/automation https://www.reddit.com/r/automation/comments/1lspw8h/built_a_full_real_estate_automation_system_for/ | "Full" brokerage system (n8n, GPT-4, Airtable, Twilio, DocuSign) | $500/mo | Heavy pushback (see quotes). |
| r/n8nbusinessautomation https://www.reddit.com/r/n8nbusinessautomation/comments/1retwim/charging_2500_for_this/ | AI receptionist for real estate + medspa | $2,500 setup + $497/mo (asker); commenter says market is $500-1,500 setup + $300-800/mo | Another commenter: 2.5k is what "5-8 callers" cost, so ROI is doubted. |
| r/n8n https://www.reddit.com/r/n8n/comments/1lbocv0/do_real_estate_agencies_even_use_email_that_much/ | Gmail chatbot -> Sheets -> Docs client profiles for luxury agencies | Asked: $5k + $400/mo | Top reply: over-specialised single tools are dying; sell a suite after interviewing agencies. |
| r/highticket_sales https://www.reddit.com/r/highticket_sales/comments/1so4krj/re_ai_agency_seeking_advice/ | AI agency for RE agents, 3-month service | $5k paid-in-full | Closed 1 of ~40 calls (a free trial). "Need to think about it". |
| r/n8nbusinessautomation https://www.reddit.com/r/n8nbusinessautomation/comments/1rn8z38/ (title only seen) | WhatsApp tenant/lease/invoice bot for student-housing landlord | $850 | One-off, small. |
| r/gohighlevel https://www.reddit.com/r/gohighlevel/comments/1l5t5cu/built_a_real_estate_automation_snapshot_that/ | White-label GHL snapshot for RE | $3-5k per client | Template product, not custom. |
| Yaakov.AI https://yaakov.ai/industries/ai-automation-for-real-estate | Menu: maintenance triage from $1,200; rent reminders/delinquency from $800; listing copy from $600; lease abstraction from $1,800; missed-call text-back from $450; AI phone receptionist from $1,500 | Per-build "from" prices (USD) | Good model for a priced menu. |
| FlowWorks (AU) https://flowworks.com.au/blog/ai-for-real-estate | Melbourne 320-property PM agency: tenant comms AI + inspection scheduling + arrears | $12,000 total (case study) | Claims 35 admin hrs/week saved, arrears down 42%, $91k+/yr labour. Vendor case study, unverified. |
| BookEveryCall (AU) https://bookeverycall.com/ai-receptionist-for-real-estate-and-property-management-australia/ | AI receptionist for AU agents/PMs | $297 / $597 / $897 per month + setup fee | Names Adelaide. This is the commodity floor. |
| 77 Productions (AU) https://77productions.com.au/ai-voice-agent/real-estate/ | AI voice agent for agents | from $950 setup + $350/mo | Pitches missed-call cost vs $8-20k commission. |
| PropPromote (US) via https://www.reddit.com/r/RealEstateTechnology/comments/1mtqj03/my_224mo_software_stack_after_3_years_as_an_agent/ | Listing video/staging/social from MLS data | $99/mo | Shows off-the-shelf competition for listing-content builds. |

Takeaway for pricing: single workflows cap around $1-4k setup. To sell high ticket, bundle 3-4 PM back-office automations and tie to rent-roll hours saved (FlowWorks $12k is the nearest AU anchor). Treat that anchor as a vendor claim.

## Lessons on what clients churned from or didn't use

- Monitoring: Zillow webhook changed, leads "just vanishing", nobody noticed for 4 days. Builder now adds a dead-man's switch (alert if no lead processed in X hours on business days). (r/AI_Agents 1u8m13n)
- Disqualification filter first: bot enthusiastically replied to "asdf" phone numbers at 2am; agents complained.
- Over-engineering: built a commercial-vs-residential branch for 5 hours; 11 leads in 8 months used it. Rule: do not automate anything that happens fewer than 5 times a week.
- Retainer scope: "maintenance and monitoring" was vague; broker assumed new open-house follow-up sequence was included. Write "included / costs extra".
- Dashboard nobody opened: a CRM reporting view nobody looked at for 2 months. Do a training call on delivery day.
- Over-personalised first reply is no better than "got your enquiry, free at X, does that work?" and risks a hallucinated price. (A commenter flagged fair-housing/misrepresentation risk; in AU the equivalent is misleading price representation under consumer law/agents' conduct rules.)
- Bots that punt hard questions: Appfolio's LISA leasing assistant raised guest-card-to-tour conversion by 5% but cut tour close ratio by nearly 10% because it never pre-qualified or handed over to a human. (https://www.reddit.com/r/PropertyManagement/comments/1novbsy/sharing_my_companies_experience_with_lisa_the/)
- AI appointment setter pulled after a week as "too robotic" (r/pwru 1ok0nrd, poster sells an RE tool, so treat as marketing).
- Adoption beats capability: a broker-owner's first AI platform failed because agents refused to download "just another app"; the fix was to meet them in text and voice. (https://www.housingwire.com/articles/why-agents-will-ignore-your-expensive-ai-tool-and-how-to-fix-it/)
- A London real-estate AI founder lost ~$180/mo subscribers who bought, were trained, then never used it; the winning model was "send us the spreadsheet, we return the finished work". (https://blue222.com/client-cancelled-subscription-and-sent-a-spreadsheet/)
- Reality check: one builder spent 35 days and got zero paying clients selling instant lead reply to US agents (https://www.reddit.com/r/AI_Sales/comments/1uokngj/trying_to_sell_an_ai_automation_service_to_us/). Lumen already sells instant enquiry replies, so do not make that the high-ticket pitch.

---

## Ideas (unique first)

### Compliance-guarded property management inbox co-pilot (draft-only, grounded in lease + agency policy)
- **What it does:** Watches the PM mailbox. For each tenant or owner email it identifies the property, tenant and lease, classifies it (maintenance, rent query, owner statement, notice, dispute), drafts a reply in the agency's voice grounded in the lease and agency rules, checks it against tenancy legislation, and queues it for one-click approval. Low-risk replies (e.g. "where is my statement") can auto-send. Everything is logged.
- **Money:** Saves PM hours (vendor claims "three or four hours a day lost to the inbox"; FlowWorks case study claims tenant emails were 15+ hrs/week for 4 PMs, response time 6 hrs -> 8 mins). Also reduces legal exposure from wrong notice periods and helps retain owners. Estimate: 2-5 hrs/PM/week is plausible; at ~$40-60/hr loaded cost that is $4-15k/PM/year. Estimate, not measured.
- **How rare:** Emerging. Two Australian products exist (below), but both are new, small and NSW-law-based. No SA-law-grounded version seen. Builders on Reddit mostly sell lead bots instead.
- **Evidence:** Simplify AI (AU, NSW law, "You stay in control") https://www.simplifyai.com.au/ ; RealBud (AU "AI admin worker", approval before anything consequential, arrears + owner updates + inbox) https://realbud.app/ ; FlowWorks AU case study https://flowworks.com.au/blog/ai-for-real-estate ; PM_Nerdcore "10-minute zero inbox" owner-statement auto-reply https://www.reddit.com/r/PM_Nerdcore/comments/1pnkft1/the_10minute_zero_inbox_workflow_for_pms_works/ ; n8n community comment: PM software APIs are basic but 60-70% of routine admin is automatable (https://www.reddit.com/r/n8n/comments/1l9oyd5/anyone_using_n8n_in_property_management/).
- **SA fit:** Strong. Residential Tenancies Act (SA) notice periods, bond via CBS, PropertyMe/PropertyTree/Ailo/:Different mailboxes. A SA-grounded rule set (notice types, timeframes, breach steps) is the differentiator vs the NSW tool. Risk: AI-drafted legal notices; keep human approval for anything that is a notice, breach or dispute. Privacy Act: tenant data to US LLM APIs; use AU-region or zero-retention endpoints and state it.
- **Build notes:** Microsoft 365/Gmail trigger -> n8n -> RAG over lease PDFs and policy doc -> Claude drafts -> approval in Teams/Outlook drafts. Medium. Biggest effort is the SA rules library and test set. Pull data via PropertyMe API or report exports; some systems need scheduled CSV exports.

### Maintenance triage and trade dispatch with owner-approval thresholds
- **What it does:** Tenant reports an issue by SMS, email or portal. AI asks the same questions a PM would (what, where, water involved, urgency), classifies it, checks the owner's approval limit and preferred trade, messages the trade for availability, books it, updates tenant and owner. Emergencies escalate to a human or on-call phone immediately; non-emergencies get a Slack/Teams approval.
- **Money:** Maintenance is a large share of PM time (Yaakov.AI estimates ~8 hrs/week for triage; vendor estimate). Faster dispatch reduces damage and owner complaints. Priced by one vendor at "from $1,200" for the build.
- **How rare:** Emerging/common in templates, rare in AU delivery. Free n8n versions exist, which caps what you can charge for the workflow alone; value is in tying it to the agency's trades list and owner thresholds.
- **Evidence:** n8n "Tenant Repair Request Dispatcher" (urgency routing, human-in-loop, WhatsApp AI agent, Redis memory; builder admits "may not be production grade") https://www.reddit.com/r/n8n/comments/1ujzjqg/i_built_an_automated_tenant_repair_request/ ; Yaakov.AI menu https://yaakov.ai/industries/ai-automation-for-real-estate ; Simplify AI matches job to owner's preferred tradesperson https://www.simplifyai.com.au/ ; student-housing WhatsApp build with structured maintenance logging https://www.reddit.com/r/n8nbusinessautomation/comments/1rmdsp7/i_built_a_full_property_management_app_inside/ ; AusPropertyChat reply: AI categorises requests, identifies urgency, drafts work orders https://www.reddit.com/r/AusPropertyChat/comments/1ti2oox/do_you_use_ai_to_help_manage_your_properties_yet/ .
- **SA fit:** Good. SA urgent repair obligations under the RTA; agencies often use Tapi or email/phone for maintenance, so build around email/SMS intake, not a new portal. Spam Act: transactional tenant messages are fine; keep marketing out of them.
- **Build notes:** Twilio SMS/AU number, n8n, Claude, Google Sheets or PropertyMe API for owner limits. Medium. Needs emergency keyword/rule layer that does not rely on the LLM alone.

### Arrears watch: ledger-aware early chase with reply classification
- **What it does:** Pulls the daily arrears report/ledger, matches bank lines to tenants, sends friendly pre-due and day-1 reminders, classifies replies ("paid", "hardship", "dispute", "promise to pay"), pauses or escalates, and drafts (never serves) the breach notice for the PM. Monday arrears report to the PM.
- **Money:** Directly protects rent-roll income. FlowWorks claims arrears down 35-50% / 42% in a case study (vendor claim, unverified). Estimate only: if the agency's average days-in-arrears falls even a few days, owner trust improves and PM chasing time drops.
- **How rare:** Emerging. n8n has a template; RealBud shows the AU "draft but never serve" pattern.
- **Evidence:** n8n template "Collect and reconcile rent with Google Sheets, Gmail, Twilio, and OpenAI" https://n8n.io/workflows/20381-collect-and-reconcile-rent-with-google-sheets-gmail-twilio-and-openai/ ; RealBud arrears table with "Breach notice drafted. Never served by Bud" https://realbud.app/ ; Yaakov.AI "from $800" https://yaakov.ai/industries/ai-automation-for-real-estate .
- **SA fit:** SA breach and termination processes are time-bound and tribunal-linked (SACAT); a wrongly-timed notice is a real risk, so notice generation must be human-approved. Trust accounting stays in PropertyMe/Console; this only reads reports.
- **Build notes:** Scheduled export -> n8n -> Claude classification -> Twilio/Outlook drafts. Low-medium; the hard part is a reliable report export from the PM software.

### Past-client and lapsed-lead reactivation (SMS first, consent-aware) tied to appraisal booking
- **What it does:** Pulls contacts marked dead/no-response or past clients not contacted in 6-18 months, sends a short, human-sounding SMS ("still thinking about selling or renting in the next few months?"), classifies replies, and books appraisals or hands warm replies to the agent. Not-now replies drop into a 90-day check-in.
- **Money:** The best revenue numbers in the builder threads. Claims: 847 dead leads -> 288 conversations -> 67 still interested -> 11 appointments in week one, run cost under $400 (self-reported, US team; https://www.reddit.com/r/RealEstateTechnology/comments/1sgal90/i_built_a_voice_ai_followup_system_that/). $3,000 setup system claiming 14 seller appointments and $96k commission in 3 months (https://www.reddit.com/r/n8n_ai_agents/comments/1o3o2sh/an_ai_sdr_call_center/). Flairr case study: 43% response rate from cold leads by SMS (vendor, unverified) https://flairr.co/case-studies/database-reactivation . Agent anecdote: ghosted 200+ past clients, AI check-ins produced 4 referrals in 3 months (single agent, poster sells RE tools; https://www.reddit.com/r/RealEstateTechnology/comments/1nrhzy6/i_tried_letting_ai_call_my_past_clients_to_checkin/). One agent's ~$12k commission = big payback on the build.
- **How rare:** Emerging globally; under-sold in AU. Obvious cousin of "generic CRM follow-up", so frame it as vendor-pipeline and rent-roll reactivation with an appraisal booking goal, not a nurture sequence.
- **Evidence:** URLs above. Pushback in the same thread: "This would be illegal in the US right?" and "You got consent from all those folks to AI/bulk call them? If not, one lawsuit = game over."
- **SA fit:** Compliance is the whole game. Spam Act 2003 requires consent (express or inferred from an existing relationship), identification and an unsubscribe on commercial SMS/email; Do Not Call Register applies to marketing calls. Past clients with a recent transaction generally have an inferred relationship; old portal enquirers are weaker. Do not copy the "double-call to bypass DND" tactic from the US thread: that would be an obvious breach risk in AU. AI voice calls to cold lists are the risky part; SMS to existing contacts with opt-out is the defensible version. Get a consent audit of the list first and sell that as a paid step.
- **Build notes:** CRM export (AgentBox/VaultRE/Rex) -> n8n -> Twilio AU SMS -> Claude reply classification -> calendar. Low-medium. Quiet hours, opt-out handling and a suppression list are mandatory.

### Vendor weekly report generator (draft-only, from real numbers)
- **What it does:** Every Friday, reads each active listing's enquiries, inspections, feedback and portal stats from a sheet/CRM, has AI write a short plain-English update with a recommendation, and saves it as an email draft for the agent to review. "Use only the figures given; leave pricing and offers for the agent."
- **Money:** Vendor retention and listing-referral tool; saves agents the weekly reporting hour per listing. One vendor blog claims about 12 agent-hours per week recovered, and that it only pays off above about 10 active listings (vendor claim, not verified).
- **How rare:** Common as a free template, rare as a sold product. Almost no one sells it in AU with REA/Domain stats pulled in.
- **Evidence:** n8n template for UK estate agents https://n8n.io/workflows/21103-draft-weekly-vendor-update-emails-with-google-sheets-openai-and-gmail/ ; n8n community 5-workflow set including weekly seller report https://community.n8n.io/t/real-estate-follow-up-on-one-google-sheet-5-n8n-workflows-from-first-enquiry-to-weekly-seller-report/318764 ; https://ustechautomations.com/resources/blog/how-to-weekly-seller-activity-report-delivery-2026 .
- **SA fit:** Weekly vendor reports with campaign metrics and buyer feedback are standard agent practice; Adelaide auction campaigns have a fixed timeline, so a pre-auction countdown report fits. Pulling REA/Domain performance data usually means scheduled emails/CSV or manual entry; I did not verify an open API for agencies. Keep price commentary human-written (misleading-pricing risk).
- **Build notes:** Sheets/CRM -> n8n -> Claude -> Outlook drafts. Low.

### Open-home sign-in capture and off-market buyer matching
- **What it does:** Photo or QR sign-in at an open home becomes a structured buyer record (budget, areas, finance status). New "off-market" or pre-market listings are matched to buyer records and a digest goes only to matched buyers, never alerting twice and excluding listings that have gone public.
- **Money:** Turns open-home attendees into a monetised buyer database; helps close vendors on pre-market campaigns. No hard dollar figures seen; this is revenue-side, not labour saving.
- **How rare:** Rare as a sold product. One freelancer portfolio shows exactly this (vision parse of open-house sheets, listing-email ingestion, rule-based matching). The matching logic is also in an n8n community post.
- **Evidence:** Freelancer portfolio (prospective client, no outcome numbers) https://www.freelancer.com/u/triilok/portfolio/real-estate-lead-listing-automatio-14067658 ; n8n community "new listing alerts" workflow (budget tolerance, areas, beds, digest per buyer) https://community.n8n.io/t/real-estate-follow-up-on-one-google-sheet-5-n8n-workflows-from-first-enquiry-to-weekly-seller-report/318764 ; n8n open-house template (SignSnapHome, lead scoring "has agent / no agent / buyer agreement") https://n8n.io/workflows/9121-automate-open-house-lead-management-with-signsnaphome-discord-and-twilio/ .
- **SA fit:** Good: Adelaide agents use private/off-market buyer lists heavily (my understanding; not sourced here). Spam Act: a sign-in form must include consent wording for follow-up marketing. Do not let AI claim a property is "off-market" unless the vendor has agreed.
- **Build notes:** n8n + Claude vision or form + Sheets/CRM. Low-medium.

### Voice-note-to-CRM (dictate after an appraisal, inspection or open home)
- **What it does:** Agent sends a voice note by SMS/WhatsApp/phone after an appraisal or inspection. AI transcribes, extracts contact, property, price expectation, tasks and next-contact date, and writes them to the CRM with a confirmation reply.
- **Money:** Fixes the thing agents never do: CRM data entry. Better data feeds every other automation. No dollar figures seen.
- **How rare:** Rare in AU; exists in US as CRM Buddy (Follow Up Boss) and as standalone apps. The adoption evidence supports it: agents will text or call but won't open another app.
- **Evidence:** CRM Buddy help page https://help.followupboss.com/hc/en-us/articles/39397366783127-CRM-Buddy ; HousingWire on agents refusing a new app and preferring text/voice https://www.housingwire.com/articles/why-agents-will-ignore-your-expensive-ai-tool-and-how-to-fix-it/ ; thin Reddit interest (e.g. https://www.reddit.com/r/PptyMgmtSoftware/comments/1rpi1on/built_a_voice_note_to_structured_text_app_does_it/ got 0 comments).
- **SA fit:** AgentBox/VaultRE/Rex have APIs but access may be restricted by plan or partner agreement; check before promising. Call recording consent laws in SA (Surveillance Devices Act) matter if you record calls, but a voice note the agent records themselves is fine.
- **Build notes:** Twilio/WhatsApp inbound audio -> Whisper/AssemblyAI -> Claude extraction -> CRM API. Medium (CRM API access is the risk).

### Lease, condition-report and document ingestion into the PM system
- **What it does:** New signed lease or agreement arrives (email/Drive). AI extracts dates, rent, bond, special conditions, break/renewal terms, and creates or updates the record and a compliance calendar (rent review, lease expiry, smoke alarm checks) with discrepancies flagged for review.
- **Money:** Removes PM data entry and errors. FlowWorks claims 3-5 hrs/week saved; Yaakov.AI prices it "from $1,800" (~14 hrs/mo). Commercial PMs on Reddit say lease abstraction "works pretty well".
- **How rare:** Common for commercial leases in builder posts, rare as an AU residential PM product. The "compliance calendar from lease terms" angle is less common.
- **Evidence:** n8n lease abstraction with text-quality gating after community feedback https://www.reddit.com/r/n8n/comments/1vz9yyw/update_fixed_the_real_estate_lease_abstraction/ ; https://www.reddit.com/r/PropertyManagement/comments/1lihtbw/commercial_pms_what_are_we_using_ai_for/ ; https://flowworks.com.au/blog/ai-for-real-estate ; RealBud "Smoke alarm check due" calendar example https://realbud.app/ .
- **SA fit:** Residential agreements and condition reports are standard-form in SA, so extraction is reliable; scanned or handwritten forms need quality gating. Also fits sales: auto-chase and tabulate Form 1 and contract documents (my idea, no builder evidence found).
- **Build notes:** Drive/Outlook trigger -> OCR/PDF text -> Claude structured output -> PM system API or sheet. Medium. Do not silently overwrite existing data.

### Entry vs exit condition-report photo comparison (bond dispute evidence pack)
- **What it does:** Reads the entry condition report photos and the exit/routine inspection photos, flags differences room by room, and prepares an evidence pack with side-by-side images for the PM to confirm before any bond claim.
- **Money:** Bond disputes and compensation claims are a tribunal-risk area; one vendor claims 70% less inspection labour and "zero deposit arbitration losses" (vendor marketing, unverified). A tool that cuts routine inspection time addresses the PM pain point most often named on AusPropertyChat ("Conducting routine inspections without a doubt").
- **How rare:** Rare/emerging. n8n photo analysis templates exist; commercial products are US. PM commenters distrust AI judging photos ("recipe for disaster"), so it must be assistive.
- **Evidence:** Prokta (US) https://www.prokta.com/property-inspection ; n8n inspection template https://n8n.io/workflows/12431-automate-property-inspections-and-reporting-with-openai-google-sheets-and-slack/ ; LinkedIn n8n photo-analysis post https://www.linkedin.com/posts/rrohden_automation-ai-n8n-activity-7325886460320964610-t1kW ; skeptic thread https://www.reddit.com/r/PropertyManagement/comments/170dby3/ai_for_property_condition_reports/ ; AusPropertyChat https://www.reddit.com/r/AusPropertyChat/comments/1mqq0bh/property_managers_whats_your_biggest_time_drain/ .
- **SA fit:** Strong. Bond claims go through CBS and disputes to SACAT, so evidence quality matters. Apps like Inspection Express produce the photos; the AI step reads their exported report. Liability: AI must not decide damage; human signs off.
- **Build notes:** Export PDF/photos -> vision model per room -> diff -> report. Medium-high; accuracy testing on real reports is required.

### WhatsApp/SMS "no-app" tenant and owner self-service
- **What it does:** Tenants and owners text a number and get a role-based menu: copy of lease, balance, invoice or statement, report an issue. n8n looks up Airtable/Sheet/PM data, generates PDFs and logs maintenance.
- **Money:** Removes repetitive "send me my lease/statement" contacts. One builder got $850 for a student-housing version; the owner had been spending 20+ hours a week chasing rent and texts (his claim).
- **How rare:** Rare for sale; mostly student-housing and short-stay. Interesting because it avoids the "another app" adoption failure.
- **Evidence:** https://www.reddit.com/r/n8nbusinessautomation/comments/1rmdsp7/i_built_a_full_property_management_app_inside/ ; https://www.reddit.com/r/n8n/comments/1rn8z38/ (title and summary only seen).
- **SA fit:** SMS or email beats WhatsApp for most Adelaide tenants and owners; same pattern with an Aus number. PM data needs a read API or nightly export.
- **Build notes:** Twilio, n8n, Airtable/Sheets, PDF generator. Medium. Low price ceiling unless bundled.

### Free response-time "mystery shop" audit as the door-opener
- **What it does:** Before pitching, Troy submits test enquiries (sales and rental) to the agency and competitors, times and scores responses, and delivers a short report. The audit is a sales tool, and the agency's own numbers do the pitching.
- **Money:** Not a saving; it lowers sales cost. Elise AI (a US property-management AI vendor) offers free mystery shopping of agents' responsiveness; a PM noticed a fake lead named "Justine Testing" and recognised it as that vendor's sales motion.
- **How rare:** Rare among small builders. Note: Lumen retired its website teardown on 25 Oct 2026, so this is a separate, narrower offer.
- **Evidence:** https://www.reddit.com/r/PropertyManagement/comments/1ow6dzr/elsie_ai/ (thread title spells it "Elsie"; post text says Elsie AI offers free mystery shopping). The PM there was annoyed and "marked it as an AI", so disclose the audit to the owner up front, not covertly.
- **SA fit:** Do the first one openly with the owner who already wants AI. Do not mystery-shop competitors using false identities without thinking through misleading-conduct risk.
- **Build notes:** Mostly manual plus a timing sheet. Low.

### Private-landlord and FSBO prospecting for the rent roll
- **What it does:** Finds owner-listed rentals and for-sale-by-owner properties, scores them, drafts personalised outreach to the owner for the agent's approval.
- **Money:** A rent roll is a recurring asset; each landlord won is multiple years of PM fees. No outcome numbers seen.
- **How rare:** Rare; US tools exist (Brivano, Tracerfy). I found no AU builder doing it.
- **Evidence:** https://www.brivano.io/ and https://www.tracerfy.com/lead-builder-service (vendor pages, US data).
- **SA fit:** Weak/risky. Scraping Gumtree, Facebook Marketplace or portals likely breaches their terms, and cold outreach to people's private numbers hits Spam Act/DNCR. Treat as speculative; do not lead with it.
- **Build notes:** High risk, medium effort. Probably skip.

### Listing photo-to-video and social packs (commodity, mention only)
- **What it does:** Turns listing photos and details into short videos, captions and posts. Builders chain Calico/Veo, ChatGPT and ElevenLabs.
- **Money:** Saves agent time but sells for around $99/mo as off-the-shelf software (PropPromote), so a custom build is hard to price high.
- **How rare:** Common.
- **Evidence:** https://www.reddit.com/r/automation/comments/1rjsj3w/i_built_an_ai_pipeline_that_turns_static_zillow/ ; https://www.reddit.com/r/RealEstatePhotography/comments/1rgjifa/agents_who_do_video_for_every_listing_how_are_you/ .
- **SA fit:** Fine; check REA/Domain video spec. Not a high-ticket pitch.
- **Build notes:** Low.

### Obvious ones (brief)
Speed-to-lead replies, missed-call text-back, AI receptionists, 52-week nurture sequences, generic GHL snapshots, "lead to contract" mega-workflows. All widely sold, all with visible pushback. Lumen already sells instant enquiry replies. Only worth including as the entry layer of a bigger bundle.

---

## Best 3 from my angle

1. **PM back-office bundle: compliance-guarded inbox co-pilot + maintenance triage/dispatch + arrears watch.** Rent roll is the agency's recurring asset, work is repetitive and measurable, AU competitors already prove demand but none (that I found) is built on SA law, and draft-and-approve design is both compliant and what clients adopt. Anchor: FlowWorks $12k AU case (vendor claim), Yaakov.AI menu ($800-$1,800 per module). Price as setup plus monthly retainer with defined scope and a dead-man's-switch monitoring clause.
2. **Past-client and lapsed-lead reactivation, SMS-first, with a paid consent audit.** Strongest claimed revenue payoff in the builder threads (appointments booked from forgotten contacts; $3k setup with a claimed $96k commission outcome; one vendor-appraisal-sized win pays for the project). Must be sold as compliant (Spam Act, DNCR), not the US-style double-dial tactic. Distinct from instant replies Lumen already sells.
3. **Vendor retention pack: weekly vendor reports + open-home sign-in capture + off-market buyer matching.** Rare as a sold product, low build risk, draft-only, and ties to sales-side revenue (listing retention, pre-market campaigns). Fits Adelaide auction timelines. Lower evidence of dollar outcomes, so pilot with one agent and measure.

Honourable mention: entry/exit photo comparison for bond evidence (rare, high perceived value, but needs accuracy testing and a heavily human-in-the-loop design).

## Notable quotes

- "Since we implemented LISA, our closing ratio on leasing tours dropped by nearly 10%." - property manager on Appfolio's AI leasing assistant. https://www.reddit.com/r/PropertyManagement/comments/1novbsy/sharing_my_companies_experience_with_lisa_the/
- "I've looked into several of these AI agents and they seem to either a) solve a problem that doesn't really exist (or solve a self-invented problem) or b) take away like 20% of someone's responsibilities that you have to have anyway for 40-50% of their salary." - u/AffectionateKey7126, same thread.
- "Makes me wonder if all the new startups based on AI agents are this built on sand" - u/Master_Mastadon, same thread.
- "The main gotcha is most PM software APIs are pretty basic, but once you've got the connections sorted, you can usually automate about 60-70% of the routine admin tasks." - u/Y0gl3ts. https://www.reddit.com/r/n8n/comments/1l9oyd5/anyone_using_n8n_in_property_management/
- "...they didn't want to download just another app. That's not where their mind goes when they have a pressing question." - Tyler Morton, broker-owner, REMAX Victory + Affiliates. https://www.housingwire.com/articles/why-agents-will-ignore-your-expensive-ai-tool-and-how-to-fix-it/
- "Conducting routine inspections without a doubt" - u/Jerratt24, answering "what's your biggest time drain" on an Australian property sub. https://www.reddit.com/r/AusPropertyChat/comments/1mqq0bh/property_managers_whats_your_biggest_time_drain/
- "Then Zillow changed something minor on their end and the webhook stopped firing. Leads were coming in and just vanishing. Nobody noticed for 4 days." - builder (u/Warm-Reaction-456). https://www.reddit.com/r/AI_Agents/comments/1u8m13n/i_automated_a_real_estate_teams_entire_lead_flow/
- "You got consent from all those folks to AI/bulk call them? If not, one lawsuit = game over." - u/s1dest3p on the dead-lead reactivation post. https://www.reddit.com/r/RealEstateTechnology/comments/1sgal90/i_built_a_voice_ai_followup_system_that/
- "No way Estate Agents are using Slack, also! Teams, perhaps." - u/AstronautSorry7596, doubting a builder's claim (relevant to AU: build into Outlook/Teams/SMS, not Slack). https://www.reddit.com/r/automation/comments/1lspw8h/built_a_full_real_estate_automation_system_for/
