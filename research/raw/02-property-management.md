# 02. Property management (rent roll side): AI automation ideas for an Adelaide agency

Researched 31 Oct 2026. Sources: Reddit (r/PropertyManagement, r/AusPropertyChat, r/AusFinance, r/AusRenters, r/PM_Nerdcore via Arctic Shift and Exa), Australian rent-roll trade sources, vendor sites, CBS SA and sa.gov.au.
Confidence labels: "seen" = I read the page. "vendor claim" = marketing number, not independently verified. "estimate" = my arithmetic.
r/Landlord and r/RealEstate returned little useful AU content. r/AusPropertyChat was the best AU subreddit. Reddit PMs are mostly American, so US ideas are flagged as such.

## Big picture facts that make the pitch (all seen)

- **Rent roll attrition in Australia is 14.2% a year**: 8% uncontrollable (sale, owner move-in) and 6.2% controllable (lost to other agencies or poor service). Source: Real Estate Dynamics, 29 Sep 2026, built on 3,296 rent roll principals spoken to in 30 days. https://realestatedynamics.com.au/were-doing-okay-why-so-many-rent-roll-principals-have-stopped-trying-to-grow-and-how-its-killing-their-business/
- **Rent rolls are valued as a multiple of annual management commission.** Commission is typically 7-10% of rent ex GST. Multiples were roughly $2.90-4.10 per $1 of commission in late 2023 (Sydney 3.3-4.1, Melbourne 3.3-4.0, Perth 2.9-3.6). Adelaide was not in the snippet I saw. Data quality, arrears level and ownership spread all move the multiple. Source: https://bsale.com.au/article-display/valuation-of-residential-real-estate-rent-rolls,1565 (Dec 2023).
  - Implication: every door kept is worth about 3x its yearly fee in business value, not just one year of income.
- **PM staff burnout is the root cause.**
  - Real estate employee turnover is 28.3% a year. 53% of PMs report mental health struggles. 23% want to leave the industry. 31% of PMs with 200+ doors say the job is "far too busy". The sources are the MRI "Voice of the Property Manager 2021" report and Domain data, quoted in an ITC NSW document: https://www.itc.nsw.edu.au/file/641/download?token=7sz-dCgE
  - :Different repeats the MRI stats (53% mental health, 23% leaving, 63% say workload is too busy): https://different.com.au/agency-blog/property-manager-burnout/
- **Why landlords leave** (Real Estate Dynamics, Feb 2025): poor communication (hearing only when there is a problem), no proactive management (rent not reviewed for years, maintenance pushed back, no vacancy strategy), surprise fees, and a revolving door of PMs. https://realestatedynamics.com.au/why-landlords-stayand-why-they-leave/
- **Portfolio load.** PropertyChat threads put a healthy load at roughly 80-100 doors per staff member. 150-200+ per PM is common and is what burns people out (https://www.propertychat.com.au/community/threads/more-than-150-properties-by-a-pm-is-it-normal.66549/).
- **Reddit sentiment is split.** The most upvoted answers say boring back-office AI works and customer-facing AI repels people. Prospects "bounce the second they realize its a bot". Tenant-facing chatbots get mixed to hostile reviews. Back-office, PM-in-the-loop AI gets praise. This points the high-ticket pitch at back-office and owner-facing work, with a human sending the message.

---

## Ideas

### 1. Landlord churn radar plus "save call" playbook
- **What it does:** Nightly job pulls PM software data: overdue routine inspections, vacancy days, open maintenance age, disputed invoices, arrears, days since last owner contact, rent below market, number of PM changes in the last 12 months. An LLM turns each owner's risk score into a plain-English reason and a suggested call script, and the principal gets a ranked Monday list. Optional: sentiment flags on inbound owner emails. The PM or principal makes the call and a draft follow-up email is ready afterwards.
- **Money:** Saves rent roll value. Estimate (illustrative inputs, not Adelaide data): a 300-door roll at about $600pw rent and 7.5% commission earns roughly $2,340 per door per year, so about $700k a year in commission. The 6.2% controllable attrition is about 19 doors, which is about $43k a year of fees and about $130k of roll value at a 3x multiple. Saving a third of those pays for a $15-30k build.
- **How rare:** Rare in AU. OurProperty (an AU PM platform) scores landlords with 40+ data points in red/orange/green tiers and logs call tone. Blanket "Super PM" (US) does at-risk owner alerts, retention plans and owner reports. No one is doing this as a bespoke layer over PropertyMe/Console/Ailo for a single agency.
- **Evidence:**
  - OurProperty churn tiers: https://www.ourproperty.com.au/proactive-property-management-to-reduce-landlord-churn/ (seen, 23 May 2025).
  - Blanket Super PM: https://blankethomes.com/super-pm/ (seen, vendor claim).
  - r/AusPropertyChat landlord stories of leaving: https://www.reddit.com/r/AusPropertyChat/comments/1opukxw/ and https://www.reddit.com/r/AusPropertyChat/comments/1kn2kv7/
- **SA fit:** Uses data the agency already owns, so low privacy risk. Keep tenant personal data out of prompts where possible. Check the Privacy Act and the management agreement's data-use terms. Do not auto-send owner emails.
- **Build notes:** n8n or Make on a nightly schedule, PM software API (PropertyMe / Reapit PM) into a Postgres or Airtable table, a Claude scoring and summary prompt, then a Slack/Teams/email digest. Difficulty: medium. The main risk is API access (see the software table below).

### 2. Owner "portfolio narrative" reports (monthly or quarterly) with proactive rent review
- **What it does:** At month end, pull ledger, rent paid, maintenance spend, inspection result and vacancy for each owner. The LLM writes a short personal commentary: what happened, what it cost, what is coming (lease expiry, compliance due, rent review). If the rent is below the suburb median it drafts a rent review recommendation with comparable data. The PM reviews and sends.
- **Money:** Targets the exact reasons landlords leave: silence and "rent not reviewed for years". Also lifts rent, which raises commission. A US vendor, CalderR, prices a similar build at $4k-$8k setup plus $1k-$2.5k a month and claims 8-15 hours saved a month (vendor claim). That is a handy price anchor for a high-ticket quote.
- **How rare:** Emerging in the US, rare in AU as a bespoke build. LORDLY (AU) does rent review with live suburb medians (including SA CBS bond data) and a state legality gate, but it is a landlord tool, not an agency back-office layer.
- **Evidence:**
  - CalderR owner reporting: https://www.calderr.com/build/owner-reporting (seen).
  - LORDLY rent reviews, which cite SA CBS data: https://www.lordly.com.au/services/rent-reviews (seen).
  - A Reddit PM said they use Claude to read onboarding ledgers and leases for red flags and to build expiring-insurance reports: https://www.reddit.com/comments/1xjpvvl
- **SA fit:** SA rules to bake into the legality check: rent cannot rise within 12 months of the agreement start or last increase, including when a fixed term rolls to periodic. SACAT can look at "excessive rent" and tenants have 90 days from the notice to apply. Source: CBS SA https://www.cbs.sa.gov.au/sections/renting/renting/tenancy-reforms-for-landlords-and-agents (seen, Aug 2025). I did not verify the required notice period for a rent increase in SA, so check this before building.
- **Build notes:** PM software API plus a comparables source. The market-rent data source needs checking (REA/Domain terms, CBS bond data, agency's own roll). Claude for narrative; PDF template. Difficulty: medium.

### 3. Entry/exit condition report comparison and bond claim pack
- **What it does:** At vacate, AI lines up the entry condition report items and photos with the exit photos room by room. It lists differences, separates fair wear and tear from damage, drafts the bond claim narrative with photo references, and drafts the owner update. The PM approves before anything is sent.
- **Money:** Exit reports and disputes are hours of PM time each. They also create owner anger when a bond claim fails. Better evidence packs mean fewer lost disputes. No hard numbers found. I would treat any claim as an estimate until the agency measures it.
- **How rare:** Emerging. Tools exist (CondSnap, Rental Evidence). They are standalone apps, not wired into the agency's own inspection platform and bond workflow.
- **Evidence:** CondSnap says the exit report compares to entry side by side and "the changes list becomes your bond claim" (https://condsnap.com/, seen). Rental Evidence compares entry and exit room by room (https://rentalevidence.com.au/, seen).
- **SA fit:** Bonds are lodged with CBS. In SA, CBS bond refunds have 14-day timeframes at the different stages, and disputes go to SACAT (CBS page above). Risk: do not let the AI decide fault. SACAT will want human-verified evidence, so keep the PM's sign-off and the original photos. Keep image metadata.
- **Build notes:** Vision model (Claude or GPT) on paired photos from the inspection app (Inspection Express, Console Inspect, etc.), n8n orchestration, output as Word/PDF. Needs the inspection platform to give image access, which may need exports. Difficulty: medium-high (image alignment and the SACAT narrative format).

### 4. Routine inspection: voice/photo to owner report, work orders and upsell leads
- **What it does:** The PM walks through and dictates or photographs. AI turns it into the inspection report, a list of defects by severity, draft maintenance work orders, and the owner's summary. It also updates the asset register (hot water system age, smoke alarm expiry) from what it sees.
- **Money:** Report writing is the PM's most hated recurring task. In the AusPropertyChat "biggest time drain" thread the PM answer was "Conducting routine inspections without a doubt" (https://www.reddit.com/r/AusPropertyChat/comments/1mqq0bh/). A maintenance work order that comes out of the inspection is also a revenue event if the agency earns a margin on maintenance (check disclosure rules before building any upsell).
- **How rare:** Emerging, with AU-specific products: EasyInspect (https://easyinspect.com.au/) and PropertyInspection.ai (https://propertyinspection.ai/, with 200+ defect categories and a compliance calendar, vendor claim). Reddit example: a self-managing landlord dictates the inspection into a voice app and gets the report and the work order in one step (https://www.reddit.com/r/PropertyManagement/comments/1rz0zjx/).
- **SA fit:** SA allows at most 4 inspections a year, with 7 to 28 days' notice (CBS page above). The scheduler should refuse to book a 5th, or to book with notice outside 7-28 days.
- **Build notes:** Mobile form or voice note (WhatsApp/Telegram) to Whisper to Claude to the PM software API or a PDF. Difficulty: low-medium. Competing with EasyInspect on the report alone is hard, so the value is the integration into this agency's own system and owner report.

### 5. Maintenance intake with pattern memory (repeat faults, asset age, quote vs invoice)
- **What it does:** Tenant request (email, SMS, form, photo) is classified (emergency/urgent/routine, trade type). The part that is not common: it checks the property's history. It flags repeat faults ("third leak call from the same stack"), asset age and warranty (e.g. a 3-year-old hot water system), duplicate requests across a strata block, quote vs invoice variance and approval-limit breaches. It then proposes the tradie, with the PM approving anything over the owner's limit.
- **Money:** Triage alone is common. The pattern layer is what avoids paying twice, avoids a ceiling collapse, and gives owners repair-vs-replace advice. A Reddit PM called the triage-plus-grouping use the one that works: "sorting incoming requests by urgency and catching the third leak call from the same stack before it turns into a ceiling."
- **How rare:** Basic triage: common. Tapi claims to automate 70% of tenant conversations with a 24/7 chatbot and cut maintenance admin by 60% (vendor claim, https://tapihq.com/integrations/propertyme). Pattern/asset memory across tools: rare. Also warn: a Reddit PM said AI "mis-sorts urgent communications as non-urgent" in their experience, so keep emergency keywords as hard rules, not just LLM judgement.
- **Evidence:** https://www.reddit.com/comments/1xjpvvl (the thread above); n8n templates exist (https://n8n.io/workflows/14292-triage-and-escalate-tenant-complaints-from-gmail-or-forms-to-slack-with-claude-ai/, seen); r/PropertyManagement idea of tenants doing guided troubleshooting before dispatch, "might save 20% of maintenance trips" (https://www.reddit.com/r/PropertyManagement/comments/1ktkter/, a poster's guess, not measured).
- **SA fit:** If the agency uses Tapi, build alongside it, not against it. SA landlords must meet minimum housing standards (Housing Improvement Act 2016) before occupation (CBS page above), so some fault categories are compliance, not just maintenance.
- **Build notes:** n8n, Claude, PM API, tradie list. Difficulty: medium. Hard-code emergency rules and approval limits.

### 6. Arrears engine: early-warning ranking, SA-correct breach notice, escalation to SACAT pack
- **What it does:** Daily, rank tenants by payment pattern change (a decline in payment regularity, change of payment method). Day 1: SMS reminder. After that: voice or SMS follow-up with payment-plan capture. At the legal threshold, auto-draft the SA breach notice with the right dates and unpaid periods, then assemble the SACAT application evidence (ledger, notices, comms log) for the PM to approve.
- **Money:** Arrears hurt owners and feed churn (one AusPropertyChat landlord left over "lost 13 weeks of rent from a tenant who stopped paying"). US numbers: EliseAI case study reports a 52% delinquency reduction, 954 hours saved and $16.9M collected by the AI over a quarter at Peakmade (vendor case study). A property operator posted on LinkedIn that AI calls got 79% pickup vs 21% email open, with late payments down 38% at $0.12/min (self-reported, not verified).
- **How rare:** PropertyMe already has "Arrears Automations" (reminders, status updates) built in (https://www.propertyme.com/aime, 27 Jun 2026). Voice agents for arrears are emerging in the US/UK (LetOps Theodore, Retell template). The SA notice and SACAT pack layer is rare.
- **Evidence:** EliseAI PDF (https://info.eliseai.com/hubfs/Peakmade_Delinquency_Centralization_CaseStudy_042224.pdf), LetOps (https://www.letops.ai/agents/rent-arrears.html), LinkedIn post (https://www.linkedin.com/posts/bera-cogenli_studenthousing-propertymanagement-aiautomation-activity-7404901542010765314-juMt). RentSense (Camden Council, UK) prioritises arrears cases by payment pattern (https://www.gov.uk/algorithmic-transparency-records/camden-council-rentsense).
- **SA fit:** sa.gov.au: a tenant is in breach when more than 14 days behind. The breach notice must list each unpaid period and the total, and is invalid if wrong. Two arrears breach notices in 12 months lets the landlord apply to SACAT without a further notice. Possession needs a SACAT order. Source: https://www.sa.gov.au/topics/housing/renting-and-letting/renting-privately/ending-a-tenancy/Breach-of-agreement-and-eviction (seen). Risk: voice AI calling tenants. Under SA surveillance law, recording needs consent (from my knowledge, not verified in this session). Check the Spam Act for SMS and disclose AI on calls. Never let the AI make threats.
- **Build notes:** Retell/Vapi + Twilio AU number, n8n, PM API for ledger, Claude for notice draft; date calculator in code, not in the LLM. Difficulty: medium-high.

### 7. Rental application screening with document forensics and income reconciliation
- **What it does:** Applicant uploads (or the PM drops) PDFs from Snug/2Apply/Ignite. AI extracts payslips, bank statements and IDs, flags tampering or AI generation, and reconciles employer name, net pay and bank deposits. It also scans rental ledgers for prior arrears. Output is a one-page risk summary for the PM, who decides.
- **Money:** One bad tenant is months of arrears plus a tribunal process. Also saves screening hours when SA agents must now use the standard Form A1 application (a separate application per prospective tenant, from 1 Jan 2026).
- **How rare:** Emerging. AppCheck is an AU vendor (https://appcheck.com.au/, vendor claim: "signs of digital tampering or AI generation"). CheckFile.ai blog (27 Sep 2026) frames it as reconciliation across three documents rather than hunting forgeries.
- **Evidence:** Reddit has the US view: Snappt (document fraud screening) appears in a 2026 complaint thread (https://www.reddit.com/comments/1x7rrwz) and a poster describes automating application screening (https://www.reddit.com/comments/1wyxs2b).
- **SA fit:** Form A1 mandatory from 1 Jan 2026 (CBS page; REA/Ignite support page https://help.realestate.com.au/hc/en-us/articles/48516369036441-Rental-law-changes-South-Australia says applications pause if the extra property details are missing). Privacy Act risk is highest here: IDs and bank statements. Use AU-hosted processing, minimise retention, disclose use. Do not let AI reject applicants on its own (discrimination risk).
- **Build notes:** Document AI, Claude, n8n. Difficulty: medium. Buy-vs-build question: AppCheck exists, so the pitch is integration and privacy-safe hosting.

### 8. Takeover audit: AI reads every lease, ledger and management agreement of a new or acquired rent roll
- **What it does:** When the agency wins or buys a batch of managements, AI ingests the PDFs: management agreements (term, fee, termination, exclusivity), leases (expiry, rent, special conditions), ledgers (arrears, rent history), insurance and compliance certificates. It outputs a red-flag list, a clean data import file and a renewal and fee-review calendar.
- **Money:** Agencies "buy up" stretched rolls: Real Estate Dynamics says efficient, scalable rolls are buying operationally stretched ones at a rate they have never seen. Faster, cleaner onboarding is the bottleneck to growth. A Reddit PM director says: "We use it when onboarding new properties to read all the ledgers, leases, etc to show up the biggest red flags we need to focus on" (https://www.reddit.com/comments/1xjpvvl).
- **How rare:** Rare as an agency service. The ledger/lease abstraction tools exist in the US commercial space (an r/PropertyManagement poster lists "automated lease abstracts and COI verification", https://www.reddit.com/r/PropertyManagement/comments/1idqhrk/). I found no AU vendor doing it for residential roll acquisitions.
- **SA fit:** Valuable for Adelaide agencies that grow by roll acquisition. Check the management agreement assignment clauses (bsale lists "ability to successfully assign to a new rent roll owner" as a value factor). Any privacy notification needed on a change of agent is a legal question, not an AI one.
- **Build notes:** Claude long-context on PDFs, structured JSON output, spreadsheet or PM import. Difficulty: medium. A one-off paid project plus the repeatable service.

### 9. Compliance register: smoke alarms, minimum standards, certificates, expiry nagging
- **What it does:** AI reads invoices, certificates and inspection notes (smoke alarm test, electrical, pool, gas, insurance) and keeps a per-property compliance calendar. Before expiry it books the tradie, notifies the owner and records the evidence.
- **Money:** Avoids fines and owner liability, and cuts the "did we check?" admin. The Reddit claim, unverified: "Imagine how many man hours we have saved by automating the entire compliance process for 180 properties" (https://www.reddit.com/comments/1xjpvvl). Another PM said the operations manager built a compliance site with Claude that tracks violations and certifications and pulls from the city website, and he may sell it.
- **How rare:** Rare to emerging. PropertyMe has "AiMe Comply" for legislation guidance (https://www.propertyme.com/aime). A compliance calendar built from the agency's own data is not a product I found.
- **SA fit:** SA smoke alarm rules depend on purchase date and build date (mains-powered or 10-year sealed, interconnection for new work, fines up to $750): https://www.sa.gov.au/topics/housing/keeping-your-property-safe/smoke-alarms (seen). Landlords should check alarms at routine inspections. Minimum housing standards (s67A) apply from before the tenant enters. I did not verify SA pool-safety rules here.
- **Build notes:** Vision/OCR on certificates, Postgres or Airtable, n8n reminders. Difficulty: low-medium. Good as an add-on to #4 and #5.

### 10. Rent roll growth engine: private-landlord prospecting and sale-to-management cross-sell
- **What it does:** Builds a ranked prospect list: privately managed landlords, rent below market, owners of multiple properties, buyers from the agency's own sales who are investors, owners whose competitor agreements are about to expire. AI drafts a personal opener and follow-up cadence. For sales: after settlement or an appraisal it nudges at 1 and 6 months with a rental appraisal.
- **Money:** At 14.2% attrition the roll shrinks without new doors. Each door is about $2k+ a year (estimate above) and roughly 3x that in roll value. The agency's own sales database is the cheapest lead source.
- **How rare:** Rare. CrayonsCRM (AU) previews "Lead intelligence" with a score and suggested opener, but labels it "coming soon" (https://crayonscrm.com.au/, seen). Rex Software's cross-sell guide is an advice article, not automation (https://www.rexsoftware.com/articles/cross-selling-property-management). Axtec "MyHomeVault" targets converting sellers into management clients (https://axtec.com.au/product/ownership-property-management/).
- **SA fit:** Use only the agency's own customer data and lawful public sources. Spam Act consent for email and SMS, Do Not Call Register for cold calls, and Privacy Act apply. Cold outreach to private landlords is the compliance risk, so default to warm contacts.
- **Build notes:** CRM (AgentBox/Rex/VaultRE) export, n8n, Claude for openers, calendar tasks for the BDM. Difficulty: low-medium.

### 11. "Property memory": email-thread-to-property-file summaries, so a PM leaving does not take the knowledge
- **What it does:** Every tenant, owner and tradie email or SMS is summarised into the property file (what was promised, what is pending). On handover the new PM gets a one-page brief per property and a "what did we last tell Unit 12 about the leak?" search.
- **Money:** Staff turnover is 28.3% a year. Each departure strands a portfolio, and landlord frustration compounds when the PM changes ("multiple property managers due to staff turnover"). Directly attacks the burnout/churn pair.
- **How rare:** Rare. An r/PropertyManagement poster describes the exact problem, with vendor threads living in someone's Outlook and unreachable after they leave (https://www.reddit.com/r/PropertyManagement/comments/1xf80qu/). A founder says they built AI to stop "losing critical info every time someone quit" (https://www.reddit.com/r/PropertyManagement/comments/1l6z4s0/).
- **SA fit:** Privacy Act access and retention rules. Keep data in AU regions. Note the trust-accounting and record-keeping duties of the agency.
- **Build notes:** Microsoft 365/Gmail connector, a vector store or structured notes, Claude. Difficulty: medium.

### 12. After-hours AI voice receptionist for tenants and owners (obvious one, brief)
- **What it does:** Answers calls 24/7, grades urgency, texts the on-call tradie for real emergencies, logs the rest for morning.
- **Money:** Fewer after-hours calls to PMs (a stress driver: PMs are "on call 24/7").
- **How rare:** Common-emerging in AU already: Frontly (https://www.frontly.com.au/property-management) and Realcall (https://realcall.au/, vendor claim "60% of repair calls land after hours").
- **SA fit:** Disclose AI. Hand off to a human. Do not use it for sales prospects unless tested, since Reddit prospects dislike bots.
- **Build notes:** Retell/Vapi + Twilio. Low-medium. Include only as a bundle item.

---

## AU PM software and APIs (what I could verify)

| Software | API status | Notes |
|---|---|---|
| **PropertyMe** | Public OpenAPI (Swagger 2.0) at https://app.propertyme.com/api/swagger-ui/ and /api/openid; per an api-evangelist summary it covers 75 paths, 86 operations. OAuth client credentials must be requested from PropertyMe (no self-serve signup), and each call is scoped to one agency's connected portfolio. | Source: https://github.com/api-evangelist/propertyme (seen, generated 26 Jul 2026). Has built-in AiMe (AI replies, Bills AI invoice reading, Arrears Automations, AiMe Comply): https://www.propertyme.com/aime. Integrates with Tapi. Overlap risk: some of the ideas above are partly native to PropertyMe. |
| **Console Cloud, now Reapit PM** | Public "Console OpenAPI" docs at https://api.console.com.au/api-docs/index.html with modules for IAM, Organisation, BI, Maintenance, Compliance, Tenant Application, Inspection, Form, Accounts Payable. | Best-documented API I found. Marketplace shows Tapi, InspectRealEstate, AgentBox, Console Pay and more (https://www.console.com.au/integrate). Access terms not verified. |
| **PropertyTree (MRI)** | A "One" developer portal with sandbox and production API management was in early access in June 2024 (LinkedIn post by Duncan Abbott). Help article "Integrate with an inspection partner (via API)" dated 6 Oct 2026. InspectRealEstate documents a PropertyTree webhook endpoint. | Partner-style access. Confirm current availability with MRI. |
| **Tapi** | No public API docs found. Integrates with PropertyMe, Console and MRI Property Tree. | Treat Tapi as a competitor or partner to work around, not an API target. |
| **Ailo** | Unverified. A Saaskart listing says "API available", but it is an auto-generated, unclaimed listing, so I would not rely on it. | Ask Ailo directly. |
| **Kolmeo** | Unverified. Kolmeo's Snug integration works via an activation key from Kolmeo support (https://help.snug.com/hc/en-us/articles/9529617329679-Activate-Kolmeo-integration), which suggests partner-style integrations rather than an open API. | Ask Kolmeo directly. |

Practical read: PropertyMe and Reapit PM are the easiest to automate against. If the agency is on Ailo, Kolmeo or PropertyTree, plan for partner approval or a CSV/email-export fallback, and quote the discovery phase separately.

---

## Traps and things Reddit PMs hate (so Lumen does not build them)

- **Recording showings and scoring staff with AI.** A US PM says management wants AI trained on pocket-recorded showings with staff "graded somehow": "privacy invasion with extra steps and a performance review attached" (https://www.reddit.com/comments/1xizyi7). Avoid anything that surveils staff or tenants.
- **Tenant-facing bots that pose as humans.** "prospective tenants definitely bounce the second they realize its a bot, makes the whole building feel unstaffed" (https://www.reddit.com/comments/1xjpvvl). Always disclose and escalate.
- **AI diagnosing faults from tenant text.** "if it doesn't save my techs a trip or a callback, it's a demo, not a tool."
- **Tenant AI emails.** PMs now receive long AI-written tenant messages. One says they tell tenants to "use the same AI to summarize it". An inbound email summariser that extracts the ask is a safe small add-on.
- **Auto-sending anything legal.** Breach notices, rent increases and bond claims should be draft-only with a human sending.

---

## Best 3 from my angle

1. **Landlord churn radar plus owner narrative reports (ideas 1 and 2 as one package).** The strongest money story: 6.2% controllable attrition, rolls valued at about 3x commission, and the same data feeds the reports. It uses the agency's own data and a human makes every call, so risk is low. A good price anchor is the CalderR range ($4-8k setup plus $1-2.5k a month, US vendor claim), and an Adelaide principal can see the maths on their own roll. Pitch it as protecting the asset that is on their balance sheet.
2. **Takeover audit and onboarding pack (idea 8), sold as a one-off project plus repeatable service.** Rare, high-ticket, easy to demo on a real batch of PDFs, and aimed at the growth bottleneck rolls face. Good fit if the owner is thinking about buying a roll or winning managements. Weak spot: demand depends on a pipeline of new managements.
3. **Arrears engine with SA-correct notices and SACAT pack (idea 6).** Arrears are the clearest dollars-and-hours pain, and the SA-specific notice and tribunal-pack layer is what generic tools lack. Needs the most care on call recording, Spam Act and drafting-only rules, so scope it in stages: ranking and drafts first, voice later.

Runner-up: the property memory idea (11) as a pitch to the principal about turnover. Cheap to build and very relatable, but harder to put a dollar figure on.

---

## Notable quotes

1. "Seen lots of AI use. All of it was supposed to increase productivity, all I have seen it do is make resolution longer. It mis-sorts urgent communications as non-urgent, Whereas before a person would triage, or it would trust the form input for severity." (r/PropertyManagement, https://www.reddit.com/comments/1xjpvvl)
2. "The AI that's actually helped on the maintenance side is the boring stuff, like sorting incoming requests by urgency and catching the third leak call from the same stack before it turns into a ceiling." (same thread, https://www.reddit.com/comments/1xjpvvl)
3. "Claude for reporting. ... We use it when onboarding new properties to read all the ledgers, leases, etc to show up the biggest red flags we need to focus on." (same thread)
4. "Many companies have a high staff turn over (think up to 30% a year) because they churn through staff and burn them out." (r/AusFinance, a strata-software designer, May 2022, https://www.reddit.com/r/AusFinance/comments/up7oou/any_property_or_strata_managers_here_what_does/)
5. "The more properties per person the more profit, but to do that requires the tech and the support staff which both cost money. In turn equals higher fees or make a loss, or neither and the PM gets burnt out and leaves." (PropertyChat, https://www.propertychat.com.au/community/threads/more-than-150-properties-by-a-pm-is-it-normal.66549/)
6. "...the management has become terrible — poor communication, lost 13 weeks of rent from a tenant who stopped paying, and no real support." (landlord, r/AusPropertyChat, Nov 2025, https://www.reddit.com/r/AusPropertyChat/comments/1opukxw/)
7. "In one year I have had 3 different property managers. All of which have been terrible at communicating with both me and the tenant." (landlord, r/AusPropertyChat, May 2025, https://www.reddit.com/r/AusPropertyChat/comments/1kn2kv7/)
8. "Repair and vendor threads live in someone's Outlook. The next PM can't find 'what did we last tell Unit 12 about the leak?' without IT restoring a mailbox or hunting a PST on a laptop." (r/PropertyManagement, https://www.reddit.com/r/PropertyManagement/comments/1xf80qu/)
