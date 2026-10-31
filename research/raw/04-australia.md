# 04 - Australian market angle (researched 31 Oct 2026)

Scope: what AU proptech already sells (commoditised vs open), which CRMs/PM systems can be integrated, what the trade press says with numbers, and which SA laws create automation demand. All URLs below were seen in search or fetch results this session. Anything I could not verify is marked UNVERIFIED.

---

## A. Market map: what is already sold to AU agencies

### A1. Platform vendors now ship their own AI (so generic "AI inside the CRM" is not a pitch)

| Vendor | AI shipped (dated) | Source |
|---|---|---|
| Box+Dice (MRI) | "Ask Agora AI Assistant" (natural-language CRM actions, Early Access, Sept-Oct 2026); "Next Best Call" contact scoring (Early Access, 8 Sep 2026); "Ai BDM Lead Detection" beta (7 May 2026: scans listing enquiries, strips personal details, flags likely landlords into a BDM list); "AI-assisted Automations Builder" listed under "Things we're working on" | https://helpcenter.boxdice.com.au/hc/en-au/articles/17531993373711-9-9-Release-Notes ; https://helpcenter.boxdice.com.au/hc/en-au/articles/17546642581263-Use-Ask-Agora-AI-Assistant-in-Box-and-Dice ; https://helpcenter.boxdice.com.au/hc/en-au/articles/12999240845327-8-8-Release-Notes |
| Rex | "AI Assist" (formerly AI Admin), a voice/text agent that performs CRM tasks (log contact, book appraisal, log inspection feedback, notify buyers). Live to all customers to trial, May 2026. Photo of business card to contact. | https://www.rexsoftware.com/articles/10-prompts-to-try-with-ai-assist |
| Reapit (Console Cloud + Agentbox) | "RAI": maintenance workflow (reads management agreement, spend limits, past creditors, notes, then recommends next action with a confidence score, drafts quote/work order; June 2026); owner inspection-feedback updates ("a click"); email-thread summaries coming; AI comments from inspection photos coming; "Reapit Verify" KYC/KYB + risk assessment built in (AML); predictive lead scoring planned. Reapit Forms for lease agreements now live in SA. | https://www.reapit.com.au/post/what-we-launched-in-june-2026 ; https://www.reapit.com.au/post/ascend-26 ; https://www.reapit.com.au/post/reapit-ai |
| PropertyMe | "AiMe" family: Reply with AiMe (email drafts), Bills AI (invoice extraction, "20 seconds rather than five minutes"), AiMe Comply (state-law guidance incl. SA), Arrears and Lease Renewal Automations (arrears included in every plan), event-triggered task Automations; Grow CRM has AI Prompts / Next Steps / Follow up with AI. **AiMe Connect (9 Oct 2026)** plugs PropertyMe data into Claude or ChatGPT for reports, dashboards, handover briefs, owner-call briefings, stuck-task flags. | https://www.propertyme.com.au/aime ; https://www.propertyme.com.au/blog/propertyme/our-biggest-step-in-ai-yet-aime-connect ; https://www.propertyme.com.au/blog/propertyme/propertyme-launches-game-changing-automation-suite-for-task-and-arrears-management |
| Ailo | Bills processing, photo-to-inspection-comment reports ("reduces reporting time by up to 50%" - vendor claim) | https://ailo.io/blog/ai-real-estate |
| VaultRE (MRI Vault) | Describes itself as "AI, advanced workflow automation and open API-first"; enquiry event triggers; REA API lead integration ("2700 clients, almost 272,000 data enriched leads" in two months, 2023, LinkedIn post) | https://linkedin.com/company/vaultre |
| Realtair | Digital proposals, e-sign, auctions, online offers. SA client Kate Smith Property (340 sales/yr) says "We're probably saving anywhere from 11 to 15 hours a week" | https://realtair.com/resources/case-study/kate-smith-realtair-success-story/ |

### A2. Point solutions already selling in AU

- **AI voice/answering for PM (crowded, commoditised):** Frontly, SYSTREE, ZemlyAI, Realcall, Valory all sell "AI receptionist for Australian property managers": 24/7 tenant and landlord calls, urgent-maintenance triage, escalation. Examples: https://www.frontly.com.au/property-management ; https://systree.com.au/ai-for-property-managers ; https://zemly.ai/ ; https://realcall.au/ ; https://www.valory.com.au/for/property-management . Earlier: Propic Concierge (2022) priced "about $2 per property under management per month", claims 98.6% of leasing enquiries deflected, ~80-85% of maintenance coordination handled, arrears down 48% in 90 days (vendor claims, Elite Agent): https://eliteagent.com/new-propic-ai-seeks-to-generate-more-leads-and-save-agents-time/
- **Chat/enquiry:** reHeroes "Alex" (acquired by Proptech Labs; ~3,200 PMs, 130,000 properties): https://www.realestatebusiness.com.au/tech/28035-ai-powered-rental-chat-platform-acquired-by-proptech-labs ; CrayonsCRM (AI leasing, "Sophie" chatbot, 90+ languages; BDM lead scoring still "coming soon"): https://crayonscrm.com.au/
- **Digital employee:** Aire "Rita" (2017): Watt Realty says ~780 admin hours and $30,000 a year saved on enquiry handling alone: https://eliteagent.com/automation-nation/ (old, vendor-supplied)
- **Custom builders already pitching AU agencies:** AI Pivot Toolbox claims an 8-agent AU agency got 15 hrs/week back and +22% inspection bookings (vendor case, unnamed client): https://aipivot.com.au/ai-for-real-estate . COEUS claims "Melbourne Property Agency" +40% leads, 15 hrs/week, "380% first quarter ROI" (unnamed, treat as marketing): https://www.coeus-solutions.com/resources/case-studies/au-property-agency-voice-ai
- **AML/CTF tools (new, July 2026):** easyAML (plugs into box+dice, Eagle, VaultRE, Real Time Agent, MantisProperty, Forms Live, GreatForms; biometric ID via Scantek; PEP/sanctions): https://easyaml.com/industries/real-estate-agents/ ; Visibl: https://visibl.com.au/solutions/real-estate ; First AML as REIA's exclusive partner: https://www.reia.com.au/aml-ctf ; Reapit Verify (above).
- **SA Form 1:** Searchlight "Pre-Populated Form1" into REI Forms Live / AIC Forms Live (https://www.searchlighttechnology.com.au/pre-populated-form1); Eckermann Property Forms integrated with reaforms/Greatforms, SA-launched (https://eckermanns.com.au/property-forms/vendor-statements/ ; https://reaforms.com.au/home/greatforms/).

### A3. Verdict: commoditised vs open

| Status | Items |
|---|---|
| **Commoditised (do not lead with these)** | Instant enquiry reply; 24/7 AI phone answering for PM; listing copy; email reply drafting; invoice/bill extraction; arrears reminder sequences; lease-renewal reminders; photo-to-inspection-comments (shipping/announced); chat assistant that does CRM data entry (Rex, Box+Dice); basic Form 1 pre-population; KYC/ID verification widgets. |
| **Emerging (vendors have started; custom build still has a window)** | Landlord/BDM lead detection (Box+Dice beta, CrayonsCRM preview); maintenance next-best-action (Reapit only); data-in-Claude reporting (PropertyMe only); sentiment/churn detection (Propic 2022, little else). |
| **Open territory (nobody found selling it)** | SA statutory-clock engines for PM (water invoicing 30-day rule, rent increase 12-month/60-day rule, Form A1 data destruction schedule, tenanted-sale termination/6-month re-let ban); cross-department (sales to PM) rent-roll capture; AML orchestration across the transaction (buyer CDD at contract, auction-day intake, evidence vault); Form 1 QA before service; rent-roll health/valuation monitoring for the principal. I found no vendor pages for these; absence of evidence, not proof - confirm with a couple of agency owners. |

---

## B. Integration feasibility (custom build)

| System | API / connector | Notes | Source |
|---|---|---|---|
| **VaultRE** | Open REST API v1.3, webhooks, OAuth; Zapier app (trigger: New Property Listing (Sales); action: Create Enquiry in Holding Area, more) | Integrator must register with VaultRE; client creates a token with scopes; 10 req/s and 10,000 req/day per API key; "We can't build your integration for you". Best-documented AU API found. | https://docs.api.vaultre.com.au/basics.html ; https://docs.api.vaultre.com.au/guide.html ; https://zapier.com/apps/vaultre/integrations |
| **Rex** | Open API ("100% of Rex data is accessible via the API"), Zapier app with many connectors incl. Retell AI, Synthflow AI, ChatGPT, AI by Zapier, Code by Zapier, Airtable, Slack | Easiest to wire to n8n/Make/Zapier plus voice agents. | https://www.rexsoftware.com/articles/open-api-opportunities-for-large-real-estate-agencies ; https://zapier.com/find-apps/r/rex |
| **PropertyMe** | OpenAPI/Swagger published anonymously (75 paths, 86 operations), OIDC OAuth with scopes, but no self-serve developer signup: must be issued client credentials by PropertyMe; each agency connects/disconnects its portfolio. Write scope is thin (comments/documents). Plus AiMe Connect for Claude/ChatGPT. | Read-heavy; good for analysis workflows, limited for write-back. The "api-evangelist" page is a third-party analysis, not PropertyMe's own. | https://app.propertyme.com/api/swagger-ui/ ; https://github.com/api-evangelist/propertyme |
| **Agentbox (Reapit)** | REST API with client ID + API key (+ office ID) obtained from Reapit support; endpoints for contacts, enquiries, listings, inspections, notes, tasks, staff, performance reports; Domo connector | Credentials are requested per office via Reapit support (per Auctions Live guide). "API limits: No" per Domo doc (not an authoritative statement). | https://www.domo.com/docs/s/article/6918172885143 ; https://api.auctionslive.com/knowledge-hub/obtaining-reapit-agentbox-api-credentials |
| **Console Cloud (Reapit)** | "Console OpenAPI" with modules: IAM, Organisation, BI, Maintenance, Compliance, Tenant Application, Reapit, Inspection, Form, Accounts Payable | Rich PM surface (maintenance, compliance, tenant application). Access terms not verified. | https://api.console.com.au/api-docs/index.html |
| **Box+Dice** | Pulls PropertyTree data by API on a schedule; support-assisted setup. Public developer docs not found. | UNVERIFIED whether third parties can get API access. Release notes show a Help Centre with detail, not a dev portal. | https://helpcenter.boxdice.com.au/hc/en-au/articles/12857375039119-Integrate-with-Property-Tree |
| Ailo, PropertyTree, :Different, Inspect Real Estate, 2Apply/Snug, Tapi | Not checked this session | UNVERIFIED. | - |

**Practical read:** the strongest build targets are Rex (open + Zapier + voice-agent connectors), VaultRE (open + webhooks), and PropertyMe for read-and-brief workflows. Agentbox and Console are workable but need a Reapit credential request. In SA, one real agency stack is Agentbox (sales) + PropertyMe (PM): OC Ouwens Casserly, https://propertyedge.app/the-property-edge-podcast/episode-5/ . Before pitching any build, ask the Adelaide owner which CRM/PM they run and whether the principal can request API credentials.

---

## C. Trade press and survey numbers on AI use in AU agencies

- **Reapit survey, 147 agencies (REB, 21 Mar 2025):** 49.1% use AI/automation for everyday communications; 48.1% for marketing (descriptions/promotion); 39.6% for customer-service automation; 34.9% to analyse agency performance and client needs; 30% to improve prospecting; Reapit's report also says 58% use ChatGPT to analyse agency data. https://www.realestatebusiness.com.au/tech/29626-surge-in-ai-uptake-among-aussie-agencies ; https://www.realestatebusiness.com.au/industry/31860-how-human-centric-ai-can-protect-trust-in-australian-real-estate (vendor survey, small n)
- **NAB/MYOB SME data via Elite Agent (20 Apr 2026):** "almost 70 per cent" of property services businesses use AI, highest of any industry (SME average 42%). Elite Agent's managing editor Samantha McLean: such figures "likely mask a wide spectrum of usage... Just because an agent is using AI to polish a listing doesn't mean they've actually integrated it into their operations." https://eliteagent.com/property-sector-leads-ai-adoption-at-nearly-70-per-cent/
- **Property Council / Yardi, 236 senior property professionals (commercial/institutional skew, not residential agencies; REB):** 55% implementing or operating AI, only 18% "stable and growing", 44% think AU lags other countries, 41% report increased operational efficiency. https://www.realestatebusiness.com.au/tech/31513-ai-adoption-accelerates-but-confidence-lags-in-property-sector
- **PM workload (REB, "Property manager exodus at all time high", undated in result):** 66% call workload busy or far too busy; 47% work more than 41 hrs/week; 21% more than 51 hrs; 31% of those with 6+ years intend to exit. https://www.realestatebusiness.com.au/industry/28712-property-manager-exodus-at-all-time-high-but-is-the-industry-turning-a-corner
- **:Different (vendor) citing industry reports:** 53% of AU PMs report mental-health struggles; 63% say workload too busy (Voice of the Property Manager); 23% looking to leave. https://different.com.au/agency-blog/property-manager-burnout/
- **PM turnover (recruiter blog, UNVERIFIED methodology):** claims 41% of PMs exit within year one and $22,000-$48,000 cost per exit; portfolio >260 doors halves year-one retention. https://workforceconsultant.io/blog/why-agencies-lose-property-managers . Treat as directional only.
- **US comparison (for translation only):** NAR/RPR survey n=225: 82% use AI, 68% save 1+ hr/week, 34% save 4+ hrs/week; top concern is accuracy (63%) then compliance (49%). https://blog.narrpr.com/tips/real-estate-agents-use-ai/
- **Rent roll economics (for money maths):** Real Estate Dynamics FY25 (eastern seaboard settled sales): median AAMI $1,838, average multiplier 3.00 (2.72 prior year), average management fee 6.30%. Valuer multiple range cited ~2.0-3.3x. SA/ACT settlements only started in FY26 (111 transactions, 16,846 managements, $85.84m). https://www.pmva.com.au/rent-roll/ ; https://realestatedynamics.com.au/2025-rent-roll-insights-median-aami-hits-record-high/ ; https://realestatedynamics.com.au/annual-rent-roll-market-report/ . **Implication (estimate from those figures):** one retained management is worth roughly $1,838 a year income and about $5,500 of rent-roll value at 3.0x; a 300-door roll is about $1.65m (PMVA worked example).
- Elite Agent / REB / TREC / AREC: I did not find an AU article with agency-level hours-saved numbers from an independent source. The numbers above are the best available; hours-saved claims in AU come almost entirely from vendors (Realtair, Propic, Aire, AI Pivot). I did not find AREC talk transcripts.

---

## D. Regulation creating automation demand in SA

**AML/CTF Tranche 2 (in force since 1 July 2026; today is 31 Oct 2026, so agents are already inside it)**
- Applies to sales agents and buyer's agents, plus developers selling direct. Enrolment was due by 29 July 2026 (28 days after first providing a designated service). Program, compliance officer and staff training had to be in place from 1 July. https://www.austrac.gov.au/news-and-media/media-release/anti-money-laundering-and-counter-terrorism-laws-cover-thousands-more-businesses
- **Both buyer and seller are the agent's customers.** Seller's agent starts the service to the seller at signed agency agreement, and to the buyer when the transaction is reasonably expected to proceed (typically contract signed). Example in AUSTRAC's starter kit: initial CDD on the buyer "within 15 days after exchange of contracts, before settlement or as soon as practicable (whatever is earlier)". https://www.austrac.gov.au/new-austrac/designated-services-newly-regulated-entities/real-estate-designated-services ; https://www.austrac.gov.au/reforms/sector-specific-guidance/real-estate-guidance/real-estate-program-starter-kit-examples-dealing-customers
- Obligations: CDD (initial, ongoing, enhanced; PEP/sanctions; source of funds/wealth), suspicious matter reports (within 3 business days; 24 hours for terrorism financing), threshold transaction reports (cash of $10,000+ within 10 business days), records generally kept 7 years, training, independent evaluation (at least every 3 years per REINSW's reading of the Act). https://www.austrac.gov.au/sites/default/files/2025-07/AMLCTF_obligations_factsheet_for_tranche_2_REs.pdf
- **Not covered per REIA:** residential tenancy agreements, property management, commercial leasing; auctioneer services unless provided by the seller's agent alongside the sale. So PM departments are not in AML scope; sales departments are. https://www.reia.com.au/aml-ctf
- **Cost signal:** The Real Estate Conversation (Feb 2026): internal personnel costs alone "could reach $30,000 to $50,000 in year one" (author's estimate, not data); "software alone won't save you". https://www.therealestateconversation.com.au/news/2026/02/09/amlctf-reforms-are-coming-real-estate-and-software-alone-wont-save-you/1770585405 . REINSW worried about cost to small/medium agencies. REISA ran "AML/CTF - In Place & In Practice" (8 July 2026) in its PD calendar.
- Visibl estimates a six-person buyer's agency doing 10-15 settlements a month needs "less than half a day per week" (vendor claim).

**SA tenancy law (Residential Tenancies Act 1995, CBS summary, updated 31 Aug 2025):** https://www.cbs.sa.gov.au/sections/renting/renting/tenancy-reforms-for-landlords-and-agents
- **Form A1 mandatory from 1 Jan 2026**; one application per prospective tenant; max 2 ID documents and 2 ability-to-pay documents; list of prohibited questions (s47B), including social media content, bond source/history, medical records, vehicle rego, pet microchip, reason for moving.
- **s76B data destruction:** unsuccessful applicants' information destroyed 30 days after the tenancy is let (or 6 months with consent); successful tenant's information 3 years after tenancy ends. Tenants can go to SACAT. (Also CBS Tenant Information Guide: https://www.cbs.sa.gov.au/documents/tenancy/guides/Tenant-Information-Guide.pdf)
- No-grounds terminations banned; prescribed reasons only. From 1 Sept 2025 a new ground where the landlord has signed a **sales agency agreement requiring vacant possession**; 60 days' notice for non-renewal of fixed terms (s83A); landlord must not re-let for 6 months after a s81/s83A ground without SACAT consent (s91A).
- Rent: increases need 60 days' written notice and 12 months since last increase; excessive-rent application to SACAT within 90 days (s55/56). Minimum housing standards (Housing Improvement Act 2016) must be met at start of tenancy (s67A); tenant can terminate on 7 days' notice for non-compliance (s85B). Landlord must offer at least one electronic, no-fee rent payment method (s56A).
- **Water:** sewerage charge is always the landlord's; consumption charges per agreement; tenant need not pay if landlord/agent does not give a copy of the invoice detailing usage **within 30 days of the invoice being issued**; landlord bears excessive use caused by a fault if tenant reported it. https://www.sa.gov.au/topics/housing/renting-and-letting/renting-privately/start-of-tenancy/water-charges ; https://www.cbs.sa.gov.au/documents/tenancy/fact-sheets/Energy-and-water-charges.pdf . REISA runs a standalone "Water Invoicing" course (6 Oct 2026), a sign agents find it error-prone. REISA's 2026 calendar also includes "How to Write a Rent Arrears Policy & Procedure", "Tenant Selection Policy", "All the RTA Reforms" (13 Oct and 19 Nov), "Lease Terms Inconsistent with the Act" (10 Nov). https://reisa.com.au/wp-content/uploads/2026/06/Professional-Development-Calendar-Webpage-May-Dec-26-Updated-June-2026-1.pdf

**SA sales law (Land and Business (Sale and Conveyancing) Regulations 2025):**
- **Form 1** is the agent's responsibility to prepare and serve when an agent is engaged. Cooling off is 2 clear business days from the later of Form 1 receipt or contract signing; a missing or inaccurate Form 1 lets the purchaser rescind until settlement; not providing a complete, correct Form 1 at least 10 days before settlement is an offence with fines up to $10,000 (per SA Law Handbook). For auctions, Form 1 must be available at the agent's office for 3 business days before and 30 minutes before the auction. https://www.lawhandbook.sa.gov.au/ch23s09s01.php ; https://www.sa.gov.au/topics/housing-and-property/buying-building-selling/building-or-buying-home/home-sales
- Regulation headings also cover agent certificates, offers to purchase, price representations, auction preliminary actions and records (reg 27), collusive practices. https://www.austlii.edu.au/cgi-bin/viewdb/au/legis/sa/consol_reg/labacr2025442/
- Signed offers must be kept by agents for CBS inspection (sa.gov.au link above).

**Privacy reform:**
- **From 10 Dec 2026**, APP 1.7-1.9: entities that arrange for a computer program to make, or do a thing substantially and directly related to making, a decision that could significantly affect an individual's rights or interests, using personal information, must say so in their privacy policy (kinds of personal information, kinds of decisions made solely by the program, kinds where the program does a related thing). OAIC advises taking a cautious approach if in doubt. https://www.oaic.gov.au/privacy/australian-privacy-principles/australian-privacy-principles-guidelines/chapter-1-app-1-open-and-transparent-management-of-personal-information ; https://www.oaic.gov.au/__data/assets/pdf_file/0021/269013/APP-1.7-1.9-Transparency-Obligation-Fact-Sheet.PDF
- **Implication:** tenant-applicant scoring or ranking by AI, and AI that auto-declines or prioritises applicants, would likely land in scope. This is a compliance point for any build, and a cheap upsell (update the agency's privacy policy). Whether a given small agency is an APP entity (small-business exemption status) is UNVERIFIED here; check with the agency and a privacy lawyer before relying on either view.
- Spam Act / Do Not Call Register apply to outbound SMS/email/calls (general rule from brief; not re-researched).

---

## E. Ideas (unique first)

### 1. SA tenant-data lifecycle guardian (Form A1 intake + automatic destruction)
- **What it does:** Applicant submits Form A1 and documents through a portal or email. AI checks the pack against Form A1 limits (max 2 ID, max 2 ability-to-pay docs), flags prohibited material (e.g. unredacted bank account numbers, social media screenshots, medical docs), redacts, and files it against the application. A scheduler then deletes unsuccessful applicants' files 30 days after the property is let (or at 6 months where consent was recorded) and successful tenants' files 3 years after the tenancy ends, writing a deletion log.
- **Money:** Saves PM admin and removes a statutory exposure the CRM vendors do not appear to address (UNVERIFIED for each vendor). Penalty amounts were not verified. Estimate to validate: a busy PM office handling dozens of applications a week creates a pile of expiry dates nobody tracks. The pitch is risk removal plus fewer manual deletes, priced as a fixed build plus monthly.
- **How rare:** Rare. No AU vendor page found mentioning s76B destruction scheduling; the rules are new (Sept 2024, Form A1 from 1 Jan 2026).
- **Evidence:** CBS reform summary and Form A1 text (note on the form tells applicants their data "must" be destroyed 30 days after the tenancy is signed). https://www.cbs.sa.gov.au/sections/renting/renting/tenancy-reforms-for-landlords-and-agents ; Form A1 PDF https://elders-re-ab-cdn.imgix.net/clients-data/22359/public_html/media/lt/300/300P187326/doc/175946653127336569.pdf?fm=pdf
- **SA fit:** Directly SA-specific, so interstate vendors are slow to serve it. Low AI-regulatory risk if AI only checks and redacts; do NOT rank or score applicants (APP 1.7 from 10 Dec 2026, discrimination rules). Hold files in an SA/AU-hosted store.
- **Build notes:** n8n/Make + Claude (document classification, redaction via OCR) + scheduled jobs + storage with expiry metadata; pull "tenancy let" date from PropertyMe/Rex/Console. Difficulty: medium. Data-handling risk is the main cost, so keep the data inside the agency's own storage.

### 2. SA statutory-clock engine for PM (water invoice, rent increase, termination notices)
- **What it does:** Watches inbound SA Water bills (email or eBill), extracts consumption vs sewerage/statutory lines, applies the SA rules (sewerage and statutory charges stay with the landlord; tenant invoice must include the bill and be issued within 30 days of the water invoice date; fault-related excess flagged to landlord), drafts the tenant invoice with the bill attached, and pushes it into the PM system. The same engine checks every rent review against "12 months since last increase" and "60 days' written notice", and checks termination notices against the prescribed grounds, notice periods and the 6-month re-let ban.
- **Money:** Water recharges missed past the 30-day line are unrecoverable. I could not find a number for how much SA agencies lose. Estimate method: ask the agency for 12 months of water bills vs. recharged amounts, then price on recovered dollars and PM hours. Rent reviews: each uplift missed or invalid delays landlord income and creates owner complaints, which hits retention (one lost management is about $5,500 of rent-roll value, estimate above).
- **How rare:** Rare as a SA-specific rules engine. Extraction alone is commoditised (PropertyMe Bills AI, Console Conversations bill workflow). PropertyMe automations already trigger tasks 120 days before rent review, but they do not check the SA conditions or draft the evidence pack.
- **Evidence:** REISA runs a dedicated "Water Invoicing" course and three RTA-reform courses in Oct-Nov 2026; SA Water page for managing agents (authorise agent on the owner's account; digital approval; five business days) https://sawater.com.au/my-account/information-for-managing-agents-and-tenants/information-for-managing-agents ; sa.gov.au water-charges page above.
- **SA fit:** Pure SA. Statutory rule text must be checked by the agency's compliance lead; the AI drafts, a human sends. Keep legal wording under a REISA/CBS-reviewed template.
- **Build notes:** Gmail/Outlook trigger -> Claude extraction -> rule check in code (not LLM) -> draft in PM system via PropertyMe/Rex/VaultRE API (PropertyMe write scope is thin: may need to create tasks plus attach documents). Difficulty: medium.

### 3. Sales-to-PM "tenanted sale" and investor capture workflow
- **What it does:** When a tenanted property is listed (sales CRM event), the workflow computes the tenancy facts (fixed term end, periodic, notice options, whether the sale needs vacant possession), warns if the termination path is not valid under the new Sept 2025 ground or the 6-month re-let ban, prepares tenant notices for entry/inspection, and coordinates inspection access. At offer/contract stage it flags whether the buyer is an investor and opens a rent-roll lead (keep the tenant and win management) or, when the vendor was a PM client, a retention task before the management is lost.
- **Money:** Rent roll value per retained management about $5,500 (estimate: $1,838 AAMI x 3.0 multiple, eastern-seaboard FY25). Reapit claims its platform has unlocked "more than $1 billion of inter-office referral revenue" (vendor claim, 2025): https://propertymarkets.news/proptech-levels-up-ai-adoption-soars-in-australian-agencies/ . Also reduces sale delays caused by tenancy mistakes.
- **How rare:** Rare as an automated flow. Reapit/Box+Dice have referral features inside their own stacks; I found no SA-specific tenanted-sale logic. REISA runs "Selling a Tenanted Property" twice in 2026, which suggests the process is confusing.
- **Evidence:** CBS s81/s83A/s91A summary; Luke Holden (Ouwens Casserly) says connecting sales and PM data to find cross-business opportunities is a priority and "the connection piece is sometimes the most challenging": https://propertyedge.app/the-property-edge-podcast/episode-5/
- **SA fit:** Strong. Agencies with a sales team and a rent roll under one roof (which is the pitch the owner has) own both sides. Compliance: AI provides prompts and drafts; termination notices and legal choices stay human.
- **Build notes:** Needs both CRMs (e.g. Agentbox/Rex + PropertyMe) -> n8n as the bridge; Claude to read tenancy facts and listing facts. Difficulty: medium-high because of two-system sync.

### 4. AML/CTF "operations layer" for the sales desk (not another KYC widget)
- **What it does:** Orchestrates the AUSTRAC workflow around the existing ID-verification tool: triggers CDD when an agency agreement is signed (seller) and when a contract is signed (buyer, due within 15 days of exchange per AUSTRAC's example); chases buyers and vendors by SMS/email for ID, entity documents and source-of-funds evidence; AI reads trust/company documents and extracts beneficial owners; assigns the risk rating from the agency's own policy; builds an exceptions queue for the compliance officer (red flags, cash, unusual instructions); drafts SMR narratives for human review; maintains a 7-year evidence vault; tracks staff training and annual review dates.
- **Money:** The Real Estate Conversation estimates $30,000-$50,000 internal personnel cost in year one for a small/mid agency (author estimate) and says software alone will not do the heavy lifting. Our angle is hours saved on chasing and file assembly, plus avoiding enforcement ("the alternative is enforcement", AUSTRAC CEO). Non-discretionary spend, so easier to sell than "nice-to-have" AI.
- **How rare:** The KYC step is commoditised (easyAML, Visibl, First AML via REIA, Reapit Verify, Scantek). The cross-system orchestration and evidence trail is less served. Emerging, with a short window.
- **Evidence:** vendor and AUSTRAC links in sections A2 and D. REIA tells members that the agent "is obligated to perform a mandatory process called 'Customer Due Diligence'".
- **SA fit:** Applies to every SA sales agent. Auctions: the seller's agent doing the auction is in scope, so buyer identity is unknown until the hammer; a pre-registration form that doubles as CDD intake is the clever bit (see idea 5). PM is out of scope. Risks: AML program/legal advice must come from a qualified AML adviser; AI must not make the suspicion decision or "tip off" a customer (AUSTRAC has a tipping-off page). Sensitive data - keep inside agency systems.
- **Build notes:** n8n + Claude + the agency's chosen ID vendor API (easyAML has CRM integrations; Reapit Verify is inside Reapit) + forms; difficulty: medium-high (compliance review needed). Partner with a licensed AML consultant rather than selling "compliance" yourself.

### 5. Auction-day bidder registration as CDD intake (SA)
- **What it does:** Online bidder pre-registration (SA regulations require preliminary actions and records for residential auctions) collects ID, entity/trust details and "buying for yourself?" answers, runs the verification vendor, and tags the bidder record "CDD pending/complete". If the bidder buys, the CDD file is ready the moment contracts are signed. AI also reconciles Form 1 availability times, the registered bidders and the cooling-off countdown.
- **Money:** Saves a scramble on auction day and the post-contract chase. Estimate only: 10-20 minutes of admin per buyer; compliance risk reduction is the real value.
- **How rare:** Rare. Realtair and others already do electronic bidder registration (OC describes electronic bidder registrations as normal), but I found none tying it to AML CDD.
- **Evidence:** Regulation 27 title (AustLII link in D); OC podcast; Auctions Live/RE Software integrate with Agentbox for listing data.
- **SA fit:** Auctions are common in Adelaide; REIA says auction services are in scope where provided by the seller's agent. Verify the exact regulation 27 record requirements with the agency's principal before building.
- **Build notes:** Form + verification API + CRM write-back. Difficulty: medium. Likely an add-on to idea 4.

### 6. Form 1 QA agent (check before service, track after)
- **What it does:** When the Form 1 lands from Searchlight/Eckermann/Greatforms, AI cross-checks it against the listing and title details, flags missing or inconsistent items (zoning/overlay, encumbrances, ACP cladding statement, agent's certificate, council/SA Water responses, owner-supplied answers), and produces a plain-English discrepancy list for the agent. After sign-off it tracks service on the purchaser, the 10-clear-days-before-settlement deadline, auction availability (3 business days before), and cooling-off start/end dates, nudging staff and the purchaser.
- **Money:** Protects deals: a defective Form 1 lets the purchaser rescind until settlement and starts no cooling-off period; offence fines up to $10,000. Estimated value is avoided fall-over of even one sale per year (commission figure for Adelaide not verified; Kate Smith Property quotes $10,000-$15,000 average commission per sale in the Realtair case study).
- **How rare:** Rare. Preparation is served by vendors; I found no QA/tracking layer.
- **Evidence:** SA Law Handbook Form 1 page; Searchlight/Eckermann/Greatforms product pages; REISA runs "Form 1" training (26 Aug and 12 Nov 2026), suggesting continuing mistakes.
- **SA fit:** Pure SA. Compliance: output is a check-list for a licensed person, not legal advice; keep the vendor/conveyancer as the preparer.
- **Build notes:** Claude document analysis on PDF + rules in code + reminders. Difficulty: medium. Hard part is getting the structured data (Forms Live / Greatforms may not expose APIs: UNVERIFIED).

### 7. Rent-roll health and valuation monitor for the principal
- **What it does:** Weekly narrative for the principal: management count and income by fee level, fee-discount drift, management agreements nearing expiry, landlords with several doors (concentration), arrears and vacancy trends, landlords showing churn signals (slow replies, complaint sentiment, repeated maintenance disputes), and an indicative rent-roll value using the agency's own AAMI x a conservative multiple range. Flags the three owners to call this week.
- **Money:** Rent roll valued at 2.0-3.3x annual management income (valuer range); FY25 broker average 3.00x. Every point of retention is worth real asset value. Estimate: on a 300-door roll at $1,838 AAMI, losing 10 managements a year loses about $18,400 income and about $55,000 of value at 3.0x.
- **How rare:** Emerging. PropertyMe AiMe Connect now lets a PropertyMe customer ask Claude for these dashboards on their own, so the custom edge is the churn logic, the valuation lens and the scheduled "who to call" brief. Propic's old sentiment analysis (2022) shows the idea exists.
- **Evidence:** PMVA rent roll guide (landlord retention and fees are valuation drivers); Real Estate Dynamics FY25; PropertyMe AiMe Connect.
- **SA fit:** SA rent rolls only began settling through Real Estate Dynamics in FY26, so local benchmark data is thin: say so. 
- **Build notes:** PropertyMe API/AiMe Connect or Rex/VaultRE API -> Claude analysis -> email/Slack digest. Difficulty: low-medium. Good "entry" retainer.

### 8. Landlord prospecting from enquiry streams and public signals
- **What it does:** Scans inbound portal enquiries, referral calls, sales-appraisal notes and owner-occupier sales for people who also own or may own an investment, scores them as management leads and writes the BDM opener.
- **Money:** Each new management is about $1,838/yr income; BDM time is the cost. Box+Dice's beta shows AI landlord detection from enquiries is a real feature.
- **How rare:** Emerging. Box+Dice beta (7 May 2026), CrayonsCRM "coming soon", Propic Advantage (2022). Open for agencies on other CRMs.
- **Evidence:** links above; PMVA prospecting article.
- **SA fit:** Privacy Act and Spam Act apply to outbound; use consent-based contact only. Public ownership data on titles costs money in SA (UNVERIFIED).
- **Build notes:** n8n + Claude classifier on enquiry text + CRM tasks. Difficulty: low-medium.

### 9. Agency-specific policy and legislation copilot (obvious-ish, but proven in Adelaide)
- **What it does:** Staff chatbot grounded in the agency's own SOPs plus SA RTA/CBS documents so new PMs get a cited answer in seconds.
- **Money:** Supports onboarding and reduces mistakes. PropertyMe AiMe Comply covers state guidance for PropertyMe customers, so the custom value is the agency's own policies.
- **How rare:** Emerging. Ouwens Casserly (Adelaide, ~1,300-1,400 sales a year) "built proprietary AI chatbot for internal policy/procedure/legislation guidance".
- **Evidence:** https://propertyedge.app/the-property-edge-podcast/episode-5/
- **SA fit:** Good for new-PM onboarding; high PM turnover (REB exodus piece). Keep a "not legal advice; check CBS" footer and cite sources.
- **Build notes:** RAG over agency documents + CBS PDFs. Difficulty: low.

### 10. Commoditised items (mention only)
- 24/7 AI phone answering with maintenance triage: Frontly, SYSTREE, ZemlyAI, Realcall, Valory, Propic. Retell/Synthflow connect to Rex via Zapier. Sell only as part of a bundle.
- Instant enquiry reply, listing copy, email drafts, bill extraction, arrears sequences, photo-based inspection comments.

---

## F. Gaps: what AU agencies need that local software appears not to do well

1. **SA-specific statutory logic** (water invoice clock, rent increase eligibility, termination grounds, re-let ban). Vendors serve national workflows with state templates (Reapit Forms in SA is new; AiMe Comply gives guidance, not enforcement).
2. **Applicant data retention and deletion** (s76B). CRMs store; nobody advertises timed destruction.
3. **Two-system hand-offs** (sales CRM + PM CRM). OC's own stack is Agentbox + PropertyMe and Luke Holden says the connection is the hardest part.
4. **AML process orchestration around the verification tool**, especially the buyer side and auctions.
5. **Form 1 validation and cooling-off tracking** (preparation is served, QA is not).
6. **Principal-level insight** (rent-roll value, churn). Data exists; PropertyMe has just opened a Claude door, others have not.
7. **Tool sprawl and adoption:** OC cut from 8-9 products to 3-4 and uses implementation specialists; "it's not just about flicking a switch". An automation build that sits on the existing stack and avoids another login fits this mood.

## Risks and cautions for the pitch
- Platform vendors are moving fast (Reapit RAI, PropertyMe AiMe Connect, Rex AI Assist, Box+Dice Ask Agora, all in 2026). Position custom builds as SA-specific glue and compliance logic across systems, not "AI inside the CRM".
- AML: the agency needs a qualified AML adviser; keep suspicion decisions with humans; do not claim Lumen provides compliance advice.
- Privacy: from 10 Dec 2026 automated-decision disclosure; avoid AI ranking of applicants. Keep personal data out of consumer chat tools.
- Many AU success numbers are vendor-supplied and unnamed; label them as such in any client deck.

---

## Best 3 from my angle

1. **SA statutory-clock engine for PM (idea 2), with the tenant-data lifecycle guardian (idea 1) as its second module.** Open territory, pure SA, tied to hard legal deadlines (30-day water invoice, 12 months/60 days rent increases, Form A1 destruction dates) and to rent-roll retention. Simple to explain to an owner ("we make sure you never lose a water recharge or break the new tenancy rules"), priced as a fixed build plus monthly. Works on Rex, VaultRE, PropertyMe.
2. **AML/CTF operations layer plus auction-day CDD intake (ideas 4 and 5).** Non-discretionary spend that began 1 July 2026, expensive for small agencies per the trade press, and the part nobody has solved is orchestration across the transaction, especially buyers and auctions. Partner with an AML adviser and the agency's chosen ID vendor. Highest ticket, highest compliance care.
3. **Tenanted-sale and rent-roll capture workflow (idea 3), with the principal's rent-roll health monitor (idea 7) as the recurring retainer.** Uses the exact feature of the owner's agency that a sales-only or PM-only vendor cannot see (both departments under one roof), with a hard money anchor: about $5,500 of rent-roll value per retained management (estimate from FY25 broker data).

## Notable quotes

1. "Ask agencies what's holding them back, and one answer comes up more than any other: admin falling behind. It's not a discipline problem, it's a capacity problem." - Rex marketing (vendor), https://www.rexsoftware.com/articles/10-prompts-to-try-with-ai-assist
2. "The high adoption rates in Property Services are encouraging, but from my experience with real estate agents, they likely mask a wide spectrum of usage... Just because an agent is using AI to polish a listing doesn't mean they've actually integrated it into their operations." - Samantha McLean, Elite Agent, https://eliteagent.com/property-sector-leads-ai-adoption-at-nearly-70-per-cent/
3. "The connection piece is sometimes the most challenging to be honest." - Luke Holden, Sales Director, OC Ouwens Casserly (Adelaide), https://propertyedge.app/the-property-edge-podcast/episode-5/
4. "The day when a system becomes available or a product available and you just switch it on - it's unreasonable to expect an agent to just sit there and configure the system to work for them. It's not just about flicking a switch." - Luke Holden, OC Ouwens Casserly, https://propertyedge.app/the-property-edge-podcast/episode-5/
5. "We're probably saving anywhere from 11 to 15 hours a week through the automation process." - Kate Smith, Kate Smith Property (SA), https://realtair.com/resources/case-study/kate-smith-realtair-success-story/
6. "The most significant cost is not recurring software licences or even the ongoing software usage charges, but the sales agents', support staff and principals' time." - The Real Estate Conversation on AML/CTF, https://www.therealestateconversation.com.au/news/2026/02/09/amlctf-reforms-are-coming-real-estate-and-software-alone-wont-save-you/1770585405
7. "The nature of property management requires a Property Manager to be on call, therefore it is hard to turn off work. As part of a small office, you don't get to have a weekend off." - PM respondent in the Voice of the Property Manager report, quoted at https://different.com.au/agency-blog/property-manager-burnout/
8. "We are tracking well for enrolments, but many thousands of businesses are still under time pressure... the laws are now in force - the expectation is compliance, and the alternative is enforcement." - Brendan Thomas, AUSTRAC CEO, 1 July 2026, https://www.austrac.gov.au/news-and-media/media-release/anti-money-laundering-and-counter-terrorism-laws-cover-thousands-more-businesses

(Reddit/Facebook AU agent pain quotes were not found in this session; the AU quotes above come from trade press, vendor and institute pages.)
