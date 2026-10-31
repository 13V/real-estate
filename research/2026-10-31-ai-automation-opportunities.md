# AI automation opportunities for an Adelaide real estate agency

Research for Lumen adl, 31 October 2026. Goal: find automations that save an Adelaide agency money or make it
money, favouring niche plays few people are doing, so Lumen can pitch high-ticket builds.

**How this was done.** 13 research agents each took one angle (Reddit agents, property management, automation
builders, the Australian proptech market, listings and vendors, prospecting data, social video, case studies,
back office and AML, leasing and rent roll, voice AI, pricing and pitfalls, wildcards). They used Agent Reach:
Reddit through the Arctic Shift archive, Exa web search (which also reaches Instagram, Facebook, LinkedIn, X and
TikTok pages), YouTube search, and trade press. A second pass with Agent Reach 1.6 checked each pick against
Reddit in full text (section 4b). The full notes, with every source URL, are in `raw/`.

**Read this first.** Almost every results figure in this space is a vendor's or builder's own claim. None of it
is audited. Figures marked *(vendor)* or *(self-reported)* are claims; figures marked *(estimate)* are our maths.
Pitch with a measured baseline and a pilot, not with other people's numbers.

---

## 1. The short version

1. **The money is in the rent roll, not the enquiry inbox.** Instant replies, AI receptionists, listing copy,
   virtual staging and "likely to list" scores are now cheap or built into the agency's software. What nobody in
   Australia sells well is protecting and growing the property management book, which is the agency's recurring
   income and a sellable asset (each managed property is worth roughly $4,500 to $6,500 of rent-roll value).
2. **The best three to pitch:**
   - **Rent Roll Protection system.** Flags landlords about to leave and landlords about to sell, and catches
     managed properties that sell through a competitor (using SA's own title alerts). Rare in Australia.
     Measurable in dollars. Landlords on Reddit name the exact warning signs it watches for (see section 4b).
   - **Property management desk assistant**, starting with maintenance. An AI handles routine requests, chases
     quotes and landlord approvals, and dispatches tradies, and a person approves anything with money or legal
     effect. Adelaide's own Toop+Toop has built this in-house (HARLI), which proves the value and that the
     agency's competitors are moving. Keep it behind the property manager, not in front of tenants.
   - **Appraisal-to-listing engine.** Builds the pre-appraisal brief, re-scores every past appraisal against what
     actually sold, and recaptures withdrawn, stale and passed-in listings. Ties straight to commission.
3. **The best foot in the door:** a paid "Agency Leak Audit" (A$2,500 to $4,500, credited to the build), or a
   cheap, clearly valuable first build such as a payment-redirection fraud guard or a weekly rent-roll briefing.
4. **SA-specific openings that interstate vendors ignore:** Form 1 pre-checks, the SA tenancy law clocks (Form A1
   data deletion, 30-day water invoicing, rent increase rules), post-auction recapture, and Land Services SA title
   alerts.
5. **Compliance shapes every build.** AML/CTF has applied to sales agents since 1 July 2026, the Privacy Act's
   automated-decision rule starts 10 December 2026, SA needs every party's consent to record a call, and the Spam
   Act and Do Not Call Register limit outbound. Design for human approval on anything sent to clients.

---

## 2. What's already taken (mention, don't lead with)

These are common, cheap, or now built into the agency's own software:

| Automation | Why it's not a high-ticket pitch |
|---|---|
| Missed-call text back, instant enquiry reply, chatbots | Australian sellers price these at A$1k to $3.2k setup plus A$149 to $500 a month (Backbone Automation, The Ai Impact). Lumen already sells instant replies. |
| AI receptionist / after-hours phone answering | At least 7 Australian vendors target agencies (Voqo, Voxworks, Realcall, Frontly, SyncID, Briick, Nyuvo). Some start at A$70 to $99 a month. |
| Listing copy, photo-to-video, virtual staging | Off the shelf (ReelView, Vinto from about $250). An ABC story on 14 Oct 2026 about AI-altered listing photos makes staging a risk. |
| "Likely to list" prediction scores | Propic, realestate.com.au's "Likely to List" (beta), AiVARE and Rex AI Prospecting already sell it. |
| AI inside the CRM / PM software | Rex AI Assist, Box+Dice Ask Agora, Reapit RAI and PropertyMe AiMe all shipped AI in 2026. PropertyMe's AiMe Connect (Oct 2026) plugs PropertyMe data straight into Claude or ChatGPT, read-only. |
| AML ID checks | easyAML, First AML, PEXA Clear ($40 to $65 per transaction), AML Guard, Reapit Verify and PropertyMe already do the ID check itself. |
| Database reactivation by SMS/AI calls | Strongest claimed results in Australia, but no longer rare: Voqo and Aidan sell it to Ray White, Belle, McGrath and Stone offices. Still worth including inside a bigger system (see 4.6). |

**The read-across:** a high-ticket build has to be custom, write back into the agency's own systems, and be tied
to listings won, managements kept or staff hours. Generic AI is a commodity now.

---

## 3. The numbers a principal already thinks in

Use these units in the pitch, not "hours saved".

| Unit | Figure | Source |
|---|---|---|
| One extra sale listing | About A$27k gross commission (SA median commission 2.9% on about A$950k) *(estimate)* | realestate.com.au / bRight Agent, Feb 2026; Cotality |
| One managed property, income | About A$1,500 to $2,200 a year management income in Adelaide listings | Real Estate Dynamics and Adelaide rent roll listings |
| One managed property, asset value | Rent rolls sell at 2.5x to 3.5x annual management income, so about A$4,500 to $6,500 per property *(estimate)*. FY26 national deals averaged about A$5,095 per property. | Ventas Asset, PMVA, Real Estate Dynamics FY26 report |
| Rent roll attrition | 14.2% of properties leave a year; 6.2% is preventable | Real Estate Dynamics, Sep 2026 |
| Attrition on a 300-property book | About 43 properties, A$77k income and A$230k of asset value a year *(estimate at A$1,800 and 3.0x)* | Our maths |
| Why landlords leave | Of every 100 lost managements, 60 were sold, and about 25 of those sold through a competitor, at about A$20k commission each. 20% moved to another agency. | Ailo, tracing 180,000 lost managements (2016-2019 data, so dated) |
| PM capacity | Average PM looks after about 150 properties. LJ Hooker's head of PM says 250 to 500 is possible with a coordinator layer and technology. 5,300 PM jobs were vacant on Seek in April 2026. | Kolmeo via realestate.com.au; Real Estate Business |
| Admin cost | Adelaide sales admin roles advertise A$65k to $90k; about A$50 an hour loaded *(estimate)* | Seek listings |
| Payment-redirection scams | Australians reported A$16.2m lost in 2023; real estate among the most targeted sectors | ACCC |

---

## 4. The plays, ranked

Each play: what it does, the money, how rare it is, SA fit, build notes. Ranked by fit for a high-ticket pitch
to an Adelaide agency that has both sales and property management. If the agency has no PM department, skip to
4.6.

### Tier 1: protect and grow the rent roll (rarest, most measurable)

#### 4.1 Rent-roll "sale leak" radar
- **What it does:** Every night it reads the PM system and the sales CRM and scores each landlord for "may sell":
  years held, a tenant giving notice, rising repair bills, arrears, a landlord asking what the place is worth,
  rate or cost complaints in emails, a nearby sale. Each morning the sales principal gets the top five with the
  reason, and the property manager gets a one-line prompt to mention the sales team. When a management ends, it
  checks who sold the property and logs the real reason.
- **Money:** Ailo found about 25 of every 100 lost managements sold through a competitor. Capturing 5 more of
  those a year at A$12k to $20k commission is A$60k to $100k a year *(estimate)*. An LJ Hooker PM head puts an
  average referred sale at about A$15k commission.
- **How rare:** Rare. Sales-side scorers exist, but we found no Australian vendor scoring sell-intent from PM
  data (maintenance, arrears, notices, landlord emails).
- **SA add-on, Land Services SA Property Watch:** Land Services SA lets you subscribe to alerts on titles, in
  bulk by area or list. It fires on transfers, mortgages, caveats and Priority Notices (lodged up to 60 days before
  a sale settles). A Priority Notice on a managed property means it's selling elsewhere: call the landlord and the
  tenant today. A transfer in the farm area means a new owner: offer management. We found nobody using this.
  Subscription pricing and any limits on marketing use are unverified; ask Land Services SA first.
- **Compliance:** Using landlord data for sales approaches is a secondary use. Add a line to the management
  agreement and privacy notice, and keep the output as an internal alert to a person, not an automatic message.
- **Build:** n8n, Claude reading notes and emails, PM software API or export, output to the CRM or a daily email.
  Medium difficulty; API access is the hard part. Sources: ailo.io/blog/the-billion-dollar-question-who-profits-from-your-rent-roll,
  landservices.com.au/our-resources/land-services-property-watch-faqs.

#### 4.2 Landlord churn radar
- **What it does:** A weekly score for every landlord on service signals: maintenance jobs open over 30 days, no
  owner contact in 90 days, vacancy longer than the book's average, tenant non-renewals, overdue rent reviews,
  repeat complaints. Monday morning the principal gets the "top 15 at risk" with the cause named and a drafted
  call script. It separates "unhappy with service" from "likely to sell" (4.1), because they need different
  plays.
- **Money:** Targets the preventable 6.2% a year. Saving 1 in 3 preventable losses on 300 properties is about 6
  properties, A$11k income and A$32k of asset value a year, before re-let and renewal fees *(estimate)*. US data
  (Property Meld) shows first-year owner churn of 18% and that churn is visible in year-one maintenance data.
- **How rare:** Rare in Australia. A UK roll-up (Dwelly) lists it as a build goal in a job ad. A Real Estate
  Business writer says most Australian agencies measure landlord retention "very lightly".
- **Watch out:** PropertyMe published exactly these prompts for Claude/ChatGPT on 26 Oct 2026, and says an
  "agentic" AiMe is coming. For PropertyMe agencies, the value has to be the scoring, the playbook and the
  follow-through (draft the email, book the call, log the result), not the data access. For agencies on
  PropertyTree, Console or Ailo it's more open.
- **Build:** Read-only data pull, rules plus Claude reading notes, weekly digest by email. Low to medium
  difficulty, so it's a good low-risk first project.

#### 4.3 Fee-leakage audit (reframe as a fee-accuracy audit)
- **Reddit check:** weak as "charge more". No agency on Reddit says it under-charges, one SA agent discounts fees
  on purpose to win business, and landlords scrutinise fee stacks closely (one nearly left over one wrongly
  charged fee). Pitch it as fee accuracy plus plain-English agreements, with found revenue as a bonus.
- **What it does:** Reads every management agreement and 12 months of fee history, lists which fees each landlord
  authorised (letting, renewal, inspection, advertising, tribunal, admin), and shows every fee that was allowed but
  never charged. Flags out-of-date agreements for renewal and produces a monthly income-by-fee report.
- **Money:** Direct and measurable. An extra A$100 a year per property on 300 properties is A$30k a year and
  A$75k to $105k of rent-roll value *(estimate)*. Rent roll consultants sell this manually; PMVA calls the gap
  between authorised and raised fees "your immediate revenue opportunity".
- **How rare:** Rare as an AI product. We found no Australian tool automating the agreement-versus-ledger check.
- **Compliance:** Fix going forward only; billing landlords retrospectively is a relationship and legal risk. Run
  on an export in a secure environment. The principal signs off.
- **Build:** PDF extraction with Claude, compare with a ledger export, output a fix list. One-off project fee plus
  a monthly report. Medium difficulty. Also a strong story if the owner ever plans to sell the rent roll: raising
  income per property raises the sale price.

#### 4.4 Property management desk assistant, starting with maintenance
- **Reddit check:** the real delay landlords and tenants complain about is the quote and landlord-approval loop,
  not the first reply, so lead with the approval and quote chaser. Tenant-facing bots draw backlash (one company's
  tour closing rate reportedly fell about 10% after a leasing bot), so don't call it "autopilot" in the pitch.
- **What it does:** Tenant maintenance requests (email, SMS, portal, after-hours call) are classified, matched to
  the property and lease, and handled: troubleshooting questions, photos requested, the right tradie picked, quotes
  chased, the landlord asked to approve within their limit, the tenant updated, the job closed and the invoice
  checked against the quote. A person approves anything involving money, legal notices or judgement. An overnight
  activity log shows the PM what was done.
- **Money:** Lifts the number of properties each PM can carry, which matters with 5,300 PM vacancies. Avoiding
  two PM hires is about A$140k to $170k a year *(estimate)*. Examples, all self-reported: Toop+Toop's HARLI does
  1,325 admin tasks a day and cut maintenance response to 1.3 days; a US owner of an 800-unit PM business says his
  four-agent maintenance chain took his week from 60+ hours to 15; a Melbourne builder (FlowWorks) quotes a A$12k
  build for a 320-property agency claiming 35 hours a week saved and arrears down 42%.
- **How rare:** Rare in Australia as something an agency can buy. Toop+Toop spent years building HARLI with its own
  engineers (from 2012, AI from 2018). Voice receptionists are common; agents that actually do the work are not.
  None of the Australian vendors we found build on SA tenancy law.
- **Local angle:** Toop+Toop (Norwood, Goodwood, Stirling) won an "Innovator of the Year" award for HARLI. Expect
  the agency owner to know the name. "Toop built theirs in-house over years; we can give you the core of it in
  weeks" is a strong line.
- **Build:** PM software API, mailbox listener, Claude, n8n, approval step by SMS or Teams. High difficulty. Start
  with maintenance only and prove it, then add arrears (4.5) and lease renewals.
  Source: toop.com.au/propertymanagementinsights/journey-to-harli-revolutionising-property-management-with-artificial.

#### 4.5 SA tenancy-law clock engine
- **What it does:** Watches the deadlines SA law sets and the PM software doesn't check:
  - **Water:** a tenant isn't liable if the water invoice isn't passed on within 30 days of SA Water issuing it
    (Residential Tenancies Act 1995 (SA) s73(3), confirmed on sa.gov.au). The engine reads incoming SA Water
    bills, separates the tenant's share from the landlord's, drafts the tenant invoice, flags any it's about to
    miss, and flags usage spikes or a second account early. An Adelaide tenant on Reddit (Jan 2026) faced about
    $1,500 from an unbilled second water account and a leak; that's the demo story.
  - **Rent increases:** at least 12 months since the last increase and 60 days' written notice. Every rent review is
    checked before it goes out, with a market evidence pack for the landlord.
  - **Rental applications (Form A1, mandatory from 1 Jan 2026):** unsuccessful applicants' data must be destroyed
    30 days after the property is let (6 months with consent); successful tenants' data 3 years after the tenancy
    ends. The engine checks applications for prohibited material and schedules deletion with a log.
  - **Termination notices:** checked against the prescribed grounds, notice periods and the 6-month re-let ban.
- **Money:** Missed water recharges are unrecoverable. Price it on 12 months of the agency's own bills versus what
  was recharged. The rest is risk removal and fewer landlord complaints.
- **How rare:** Rare. Bill reading is common (PropertyMe Bills AI), but we found no vendor checking the SA rules.
  REISA runs a standalone water invoicing course, which shows agents find it hard.
- **Compliance:** Rules in code, not left to the AI. A person sends anything that affects a tenant's rights. Do not
  rank rental applicants with AI (Privacy Act automated-decision rule from 10 Dec 2026).
- **Build:** Medium difficulty. Sources: cbs.sa.gov.au/sections/renting/renting/tenancy-reforms-for-landlords-and-agents,
  sawater.com.au managing agents page.

Other rent-roll plays worth knowing:
- **Takeover audit.** When the agency wins a batch of managements or buys a rent roll, AI reads every lease, ledger
  and management agreement and flags problems (expired leases, missing compliance, fee terms, arrears). One PM
  director on Reddit already does this by hand with Claude; we found no Australian vendor. Strong fit if the owner
  is growing by acquisition.
- **Arrears engine with SA-correct notices.** In SA a tenant is in breach once more than 14 days behind, and the
  breach notice is invalid if the unpaid periods or total are wrong (sa.gov.au). PropertyMe already sends basic
  reminders, so the value is the correct notice and a SACAT evidence pack, drafted for a person to send.
- **Property memory.** Summarises each property's email history into its file, so a PM leaving doesn't take the
  knowledge with them. Real estate staff turnover runs at about 28% a year (MRI report), and landlords complain
  about changing PMs. Cheap to build and easy to relate to.
- **Personal monthly owner updates** instead of generic statements, with a plain-English note on rent, repairs and
  the market. A US vendor (CalderR) prices a similar build at US$4k to $8k plus US$1k to $2.5k a month.
- **Investor-buyer handover**: spot investor buyers at contract and pitch management before settlement (we found
  nobody automating it). Also **rent review packs** for landlords, and an **instant rental appraisal funnel** that
  fits Lumen's existing website, SEO and ads work.

PMs on Reddit push back on tenant-facing bots and AI diagnosing repairs from tenant texts. Keep the AI on the back
office and owner side, with a person sending anything that matters.

### Tier 2: win more listings

#### 4.6 Appraisal-to-listing engine
- **What it does:** Three parts working from the agency's own data.
  1. **Pre-appraisal brief:** before every appraisal, a one-page brief and draft presentation: the owner's history
     with the agency, local comparable sales, and how many buyers in the agency's own database match the property.
  2. **Appraisal replay:** re-scores every past appraisal that didn't list against what has since sold nearby, and
     drafts a personal note quoting the old CRM notes for the agent to approve ("When we met in March you were
     waiting for the kids to finish school...").
  3. **Win-back radar:** alerts when an appraised-but-lost property is listed, withdrawn, goes stale, drops price
     or passes in with another agent, so the agent can offer a second opinion.
- **Money:** One extra listing is about A$27k gross commission *(estimate)*. MyTurn (Australian, 200+ agents) sells
  withdrawn-listing alerts; AxonEstate sells briefs; Saabai and Briick sell appraisal nurture. A coaching firm
  (Property-Agent) claims recorded and scored appraisals lift conversion from 50% to 80% *(self-reported)*.
- **How rare:** The pieces exist separately from small vendors. Joined up on the agency's own data, it looks rare
  in Australia.
- **Compliance:** Human-approved messages; Spam Act opt-out; check the Do Not Call Register before calls. Avoid
  scraping realestate.com.au or Domain (terms of use). Address any cold letters to "The Owner".
- **Build:** CRM API (Rex and VaultRE have open APIs), comparable sales data the agency already licenses, Claude,
  n8n. Medium difficulty.

#### 4.7 Post-auction recapture
- **What it does:** At the hammer or pass-in, the agent taps the result into a form. Underbidders get flagged for an
  immediate call and matched to current and upcoming stock. Registered non-bidders get a same-day personal
  message. Open-home attendees from the campaign get a market update. The vendor gets a debrief and referral
  sequence. On a pass-in, a structured follow-up plan starts.
- **Money:** Voqo argues one auction should produce three to five listing conversations within 48 hours, since
  underbidders often own a home to sell *(vendor)*. One agent on Reddit: "Most agents don't send [an underbidder
  letter] at all."
- **How rare:** Emerging, and specific to Australia (the US barely uses auctions). Only Voqo pitches it.
- **SA fit:** Strong. Adelaide's eastern and inner suburbs are auction-heavy. Everyone contacted registered or
  attended, so there's an existing relationship.
- **Build:** Low to medium difficulty. Form or SMS command, CRM tags, Twilio or MessageMedia, Claude drafting.

#### 4.8 Open home to vendor report, hands-free
- **What it does:** After an open home the agent records a 60-second voice memo in the car. The AI writes the CRM
  notes, drafts personal follow-ups to each attendee, and adds the feedback to the vendor's weekly report.
  Attendees also get a short "what did you think?" text, and their answers rank the agent's callbacks. Each week
  the vendor gets an honest report built from real numbers (portal views, enquiries, attendance, feedback) with a
  plain-English read on price, which helps the price conversation.
- **Money:** Vendors' top complaint is no updates; one vendor said he picked his agent because he "turned up with
  the most tangible data". Keeps listings from walking and lifts referrals. Saves agents several hours a week
  *(estimate)*.
- **How rare:** Emerging. qpIQ and Real Saturday (new Australian micro-products) do buyer feedback; CRM Buddy (US)
  does voice-to-CRM. realestate.com.au's Campaign Assist covers some vendor talking points, so make this
  cross-system.
- **SA compliance guardrail to sell:** price guides in SA can't have a top figure more than 110% of the lower, and
  the lower can't be below the estimate in the agency agreement. The report generator can check this.
- **Build:** Low to medium difficulty. Fast to demo, low risk, and agents feel it on day one.

### Tier 3: compliance and back office (non-discretionary spend)

#### 4.9 Form 1 pre-check
- **What it does:** The vendor or admin uploads the title search, rates notice, SA Water bill, Emergency Services
  Levy notice, land tax and strata or community title documents. The AI pulls out every field the Form 1 needs,
  cross-checks them (owner name against the title, rates periods, levy arrears, easements, zoning), lists what's
  missing and produces a "ready to certify" checklist for whoever prepares it. It tracks amendments and serve
  dates.
- **Money:** A defective or unserved Form 1 is an offence (up to A$10,000), delays cooling-off and can let a buyer
  rescind until settlement. Saves 1 to 2 admin hours per listing *(estimate)* and gets listings to market faster.
- **How rare:** Rare. AI "Section 32" tools target Victoria. We found nothing aimed at SA agents. Preparers (The Form
  1 Company from $385, Eckermann) do the form; nobody does the collect-check-chase layer around them.
- **Compliance:** The AI never certifies; a licensed person signs. Test on 20 past files with a conveyancer first.

#### 4.10 AML/CTF operations layer
- **What it does:** Sits around whichever ID-check tool the agency already uses. Starts due diligence when an agency
  agreement is signed (seller) and when a contract is signed (buyer, within 15 days of exchange in AUSTRAC's
  example). Chases people who haven't completed checks, unpacks company, trust and SMSF buyers, keeps a log of the
  steps taken for people who won't cooperate, reconciles the CRM against the due-diligence records nightly, and
  drafts suspicious matter reports for the compliance officer to review. Auction bidder registration can double as
  buyer ID intake.
- **Money:** The Real Estate Conversation estimates A$30k to $50k of staff time in year one for a small or mid
  agency *(estimate)*. AUSTRAC issued its first infringement notices on 30 Sep 2026 (A$21,840 for companies) and
  says it will target programs "not applied in daily operations". Admins are struggling ("AML=FML", Reddit).
- **How rare:** The ID check is commoditised; the workflow around it is not, from what we found.
- **Compliance:** Highest liability of anything here. Partner with an AML adviser and frame it as workflow and
  record-keeping, never as compliance advice.

#### 4.11 Payment-redirection guard (best first project)
- **What it does:** Watches the agency's inbox and payment approvals for bank details or "we've changed our bank
  account" language, compares them with a verified payee list (conveyancers, vendors, tradies), holds anything new,
  and requires a logged call-back to a known number. Also flags lookalike sender domains.
- **Money:** Loss avoidance; one stopped diversion of a deposit or rent payout pays for it many times over. Agents
  hold trust money under the Land Agents Act, so a misdirected payment is a licence-level problem.
- **How rare:** Rare for agencies. Conveyancing automation shops offer it; we found nothing packaged for agencies.
- **Build:** Low to medium difficulty (Microsoft 365 or Google Workspace, Claude, a payee table). Cheap, quick and
  obviously valuable, which makes it a good way to earn trust before a bigger build.

Other back-office plays: a **contract-to-settlement tracker** that chases conveyancers and brokers and flags sales
going quiet (check Autopilot, autopilot.com.au, which claims 130+ agencies); a **deal-aware inbox** that files
emails to the right transaction; and **commission statement prep** for splits and referral fees.

### Wildcards (less proven, worth knowing)

- **Council and development application radar.** Reads PlanSA and council agendas, matches new DAs and rezonings to
  the agency's database and neighbours within about 500 m, and drafts "what this means for your street" letters.
  GoSiteHunt's DA Watch covers SA registers but is aimed at developers. Very demo-able; no conversion data.
- **First text to matched buyers.** When a listing goes live, the right 100 to 200 past enquirers get a personal
  message within minutes, before portal alerts. Propic does matching at scale, so keep it simple and fast.
- **AI roleplay coaching** for new agents (appraisal and objection practice). Cheap and no compliance risk.
- **Listing fact guard.** Checks AI-written listing copy against the actual facts before it goes live. An LJ
  Hooker branch once published a listing naming two schools that don't exist (Guardian, Nov 2024).
- **Multilingual buyer handling** (Mandarin, Hindi, Vietnamese) for Adelaide's migrant buyers.
- **AI search visibility tracker** for agents, which fits Lumen's SEO retainer.
- **Facebook group listener** for people saying they're moving. Breaks Meta's terms; avoid.

---

## 4b. Reddit check (second pass, Agent Reach 1.6)

Agent Reach 1.6 added full-text Reddit search, so three more agents checked each pick against what landlords,
tenants, vendors, buyers and agents actually say. This confirms the pain, not that agencies will pay: most voices
are clients complaining about agencies, not principals asking for tools. r/AusPropertyChat is heavily seeded by
AI vendors, so those posts were discounted. Notes: `raw/14-`, `raw/15-` and `raw/16-`.

| Pick | Reddit evidence | Best quote |
|---|---|---|
| Landlord churn radar (4.2) | **Strong.** Landlords name the exact signals: silence while vacant, no inspections, slow repairs, PM turnover. They switch at a vacancy, a re-let, when their PM leaves, or for a rival's fee discount. | "It's been 23 days since [the agency] listed the property on the rental market. And I have not heard anything from the Property Manager yet." Top reply: "They should be ringing you every week." ([r/AusProperty](https://www.reddit.com/r/AusProperty/comments/1r607m1/23_days_and_have_not_heard_anything_yet/)) |
| Sale-leak radar (4.1) | **Some.** Agencies visibly fight to keep managements when a property sells; nobody describes predicting it. Still rare. | |
| PM desk assistant (4.4) | **Strong on the pain.** The quote and approval loop is the delay. No Australian operator result found. | |
| SA tenancy clocks (4.5) | **Some.** Water is the best SA signal (three Adelaide threads, Jul 2025 to Jan 2026). Tenants cite the 12-month and 60-day rent rules and spot agency notice errors. Form A1 never comes up. | "an accumulated charge of approximately $1,500" from an unbilled second water account ([r/Adelaide](https://www.reddit.com/r/Adelaide/comments/1qd7ofk/rental_advice/)) |
| Property memory | **Strong on the pain.** "Never told, new PM knows nothing, old agency won't hand over history" recurs. | |
| Fee-leakage audit (4.3) | **Weak as framed.** See 4.3: pitch accuracy, not "charge more". | |
| AML ops layer (4.10) | **Strong.** Admins carry it, ownership is confused, AUSTRAC wants proof of the work. Check fees seen from $6 to $400. | "it's just been added to my workload as the admin... AML=FML." ([r/AusPropertyChat](https://www.reddit.com/r/AusPropertyChat/comments/1u5e3mg/amlctf_changes_how_are_real_estate_agencies/)); "Since late August, AUSTRAC has been sending out section 167 notices... They want to see the work behind it." |
| Payment-redirection guard (4.11) | **Strong problem.** Repeated Australian losses (a $500K deposit, 10% deposits, lookalike domains), including an agency's own mailbox being hacked. The only defence people mention is a phone call-back. | |
| Vendor report (4.8) | **Strong on the pain**, with a twist: agents say clients want the "why", not charts, and won't send stats unchecked. Make it an agent-reviewed draft with a written read on price, not a dashboard. | "Our agent would call every Monday with 'feedback from the weekend.' It was always vibes." ([r/AusPropertyChat](https://www.reddit.com/r/AusPropertyChat/comments/1unm3l5/sellers_whove_been_through_a_campaign_recently/)) |
| Post-auction recapture (4.7) | **Some.** Underbidders say agents go quiet afterwards; no agent says it costs them listings. | |
| Appraisal-to-listing engine (4.6) | **Some.** Vendors shop agents and distrust the highest appraisal; no agent voices the lost-appraisal follow-up pain. | |
| Form 1 pre-check (4.9) | **Weak.** Only buyer-side confusion about cooling-off timing; no admin describes the burden. Validate with the agency before pitching. | |

**New ideas from the Reddit pass worth adding:**
- **Condition report and bond-claim evidence engine.** The PM records a short video at the ingoing and outgoing
  inspections; AI writes a specific room-by-room report (not "good" for every room), pairs ingoing with outgoing
  evidence, separates likely wear and tear from damage, and drafts a bond-claim pack for SACAT, for a person to
  review. Tenants say agents write "good" everywhere and it decides bond disputes. One US operator says
  video-to-report cut documentation from about an hour to 12 minutes per unit *(self-reported)*.
- **Offer register.** Logs every offer with a timestamp and confirms to the vendor that it was presented. One
  vendor's higher offer "went to spam" and was never presented. Cheap, and protects the agency's licence.
- **Weekly vacancy digest for landlords.** A short automatic update while a property is vacant (enquiries,
  inspections, applications, feedback). Directly answers the "23 days and not heard anything" complaint; a quick
  first win inside the churn radar.
- **Approvals and quote chaser.** The first module of 4.4: chases tradie quotes and landlord approvals until done.
- **"Your buyer's AI will read your contract" scan.** Buyers already run contracts through AI tools, so check the
  vendor's documents for anything a buyer's AI would flag before listing. An extension of 4.9.
- **Agency-wide read-only data layer.** One connector across the PM system, sales CRM and mailbox, so staff's
  own Claude can answer questions across all of it. PropertyMe's AiMe Connect only sees PropertyMe. Treat it as
  infrastructure under the other builds, not a headline.

**Reddit's main warning:** goodwill toward AI is for back-office work. Backlash is about visible client-facing
errors (a pasted ChatGPT prompt left in a listing, invented schools, doctored photos) and AI-sounding outreach.
Buyers also cite the Spam Act and treat "contact agent" listings as data harvesting, so build consent in first.

---

## 5. How to sell it

**Offer ladder** (price points above A$7.5k are our estimates; no published Australian real estate build above
about A$7.5k was found, so test them on the first deal):

| Step | What | Price (estimate) |
|---|---|---|
| 1. Agency Leak Audit | 2 weeks, fixed fee, credited to the build if signed within 60 days. Principal interview on money, short interviews with agents, PMs and admin, a one-week time log, a 50-record data check, one real job traced end to end. Output: ranked list with dollars per workflow, a "don't automate" list, a named owner for each item, fixed quotes for the top three. | A$2,500 to $4,500 |
| 2. First build | Payment guard, weekly rent-roll briefing, or the open-home voice memo flow. Fast, visible, low risk. | A$3k to $8k |
| 3. Core system | Rent Roll Protection (4.1 to 4.3) or the Appraisal-to-listing engine (4.6) | A$15k to $30k plus A$1k to $2.5k a month |
| 4. Flagship | PM desk assistant (4.4 plus 4.5) | A$25k to $50k plus retainer |

Comparable paid audits: Finyki US$1.5k or US$7.5k, Mindflows €3,500, Numoru US$8k to $15k, all credited to the
build. Avoid revenue share on commission (messy, and a trust-account grey area).

**Framing that works:**
- Ask "what does it cost you when this doesn't happen?" and write the number down with the principal.
- Compare with the hire they'd otherwise make (a PM or admin), not with software.
- Sell an outcome in their units: listings won, managements kept, properties per PM.
- Lead with one specific pain, not a list of features.

**Why these projects fail (design against each):**
1. Agents won't use "another app". Put the output where they already are: SMS, email, the CRM.
2. Messy or empty CRM data. Check data quality in the audit and charge to fix it first.
3. Integrations break silently (one builder's lead webhook died for 4 days unnoticed). Add monitoring and a
   "no leads processed today" alarm, and sell that as part of the retainer.
4. Nobody owns it after handover. Write a named internal owner into the contract.
5. Invisible value leads to churn. Send a monthly one-page report in dollars.
6. AI errors embarrass the brand. Answer only from supplied facts; human approval on anything going to vendors,
   landlords or tenants.
7. Vague retainer scope. List what's included and what costs extra.

---

## 6. SA compliance cheat sheet (check with the agency's lawyer)

- **Spam Act:** consent, identify the agency, easy opt-out on every SMS and email.
- **Do Not Call Register and Telemarketing Standard:** calls Mon to Fri 9am to 8pm, Sat 9am to 5pm, never Sunday or
  public holidays. Open-home sign-in with a clear tick-box can give consent. Check current ACMA guidance on whether
  appraisal and post-open-home calls count as telemarketing.
- **Call recording:** SA's Surveillance Devices Act 2016 needs every party's consent. Say it's AI and that the call
  is recorded in the first sentence. No law requires AI disclosure yet, but a Colliers AI caller drew ABC coverage
  in June 2026 for not disclosing.
- **Privacy Act:** from 10 Dec 2026, privacy policies must disclose automated decisions that significantly affect
  people (APP 1.7). Don't let AI rank tenants or make decisions about people.
- **AML/CTF:** sales agents are reporting entities since 1 July 2026; buyers and sellers are both customers. Property
  management is out of scope.
- **SA tenancy law:** Form A1 data deletion, 30-day water invoicing, 12-month and 60-day rent increase rules.
- **Form 1:** a licensed person certifies; AI only checks.
- **Data licensing:** Cotality data can't be used for direct marketing; don't scrape the portals.

---

## 7. Questions for the first meeting

These decide which build to lead with:

1. How many properties do you manage, and how many PMs? How many sales a year? Share of auctions?
2. Which software: sales CRM (Rex, VaultRE, AgentBox, Box+Dice) and PM system (PropertyMe, PropertyTree, Console,
   Ailo)?
3. How many managements did you lose last year, and do you know why? How many of those sold, and through whom?
4. What happens to an appraisal that doesn't list? Is anyone following them up?
5. Where do your PMs' days go? What would you do with one more PM's worth of time?
6. How are you handling AML checks since July? Who chases the buyers?
7. Who on your team would own a new system day to day?
8. Have you tried any AI or automation already? What happened?

---

## 8. Sources and raw notes

Full notes with every source URL are in `raw/` (one file per research angle). Key sources:
- Toop+Toop HARLI interview: https://www.toop.com.au/propertymanagementinsights/journey-to-harli-revolutionising-property-management-with-artificial
- Ailo lost-management analysis: https://ailo.io/blog/the-billion-dollar-question-who-profits-from-your-rent-roll
- PropertyMe AiMe Connect prompts (26 Oct 2026): https://www.propertyme.com.au/blog/property-management/aime-connect-10-propertyme-mcp-prompts-every-bdm-should-be-using
- Real Estate Dynamics rent roll attrition (Sep 2026): https://realestatedynamics.com.au/were-doing-okay-why-so-many-rent-roll-principals-have-stopped-trying-to-grow-and-how-its-killing-their-business/
- Rent roll valuation guide: https://ventasasset.com.au/guides/buying-a-rent-roll
- Land Services SA Property Watch: https://www.landservices.com.au/our-resources/land-services-property-watch-faqs/
- CBS SA tenancy reforms: https://www.cbs.sa.gov.au/sections/renting/renting/tenancy-reforms-for-landlords-and-agents
- AUSTRAC real estate guidance: https://www.austrac.gov.au/new-austrac/designated-services-newly-regulated-entities/real-estate-designated-services
- SA Law Handbook on Form 1: https://www.lawhandbook.sa.gov.au/ch23s09s01.php
- Voqo post-auction follow-up: https://www.voqo.ai/blog/post-auction-follow-up-real-estate
- Backbone Automation pricing (AU): https://backboneautomation.com.au/real-estate
- ACCC payment redirection scams: https://www.accc.gov.au/media-release/beware-of-fake-invoices-from-scammers-impersonating-businesses

Gaps: the second pass (Agent Reach 1.6) searched Reddit in full text, but single threads couldn't be opened, so
quotes come from search results and some are cut short. Adelaide and SA voices are thin. Facebook, Instagram and X
were reached through web search only, not logged-in browsing (`HANDOFF-social-research.md` has a prompt to run
that part on Troy's computer). YouTube transcripts were rate-limited, so videos were judged from titles and
descriptions. SA legal points come from public summaries (SA
Law Handbook, CBS, AUSTRAC), not legal advice.
