# 05 - Listing and vendor side: where agencies win or lose listings

Researched 31 Oct 2026 (Exa web search and fetch, Reddit via Exa). About 30 tool calls.

**Big picture finding.** The generic parts of this angle are being commoditised by the platforms agents already pay for:
- REA's **Campaign Assist** is an AI chat inside Ignite that gives vendor talking points, price-conversation comps and next steps.
- **Rex AI Assist** logs feedback and drafts vendor emails.
- Rex also has **Rex Hub for Vendors**, and REA has **Pitch by Realtair**.
- REA now shows prospective vendors an **AI summary of an agent's reviews**.

A one-agent "write me a vendor update" prompt is no longer worth a high-ticket fee. The sellable part is the cross-system build: agency data (CRM, appraisal history, buyer database, past sales) joined to portal data, run on triggers, with a human approving before anything goes out.

Claims taken from vendor sales pages are marked **(vendor claim)**. They are not independent proof.

---

### 1. Pre-appraisal intelligence brief + auto-built listing presentation
- **What it does:** When an appraisal is booked (calendar or CRM), an overnight job pulls street-level sales, competing listings and days on market, then counts how many buyers in the agency's own database match the price band. It drafts the agency-branded presentation, with a one-page "what to say about this street" brief, in the agent's inbox by 6am. The agent edits in 10 minutes and walks in with "we already have 27 buyers with finance looking for exactly this."
- **Money:** Each listing is worth thousands in commission, so a few extra wins a year pays for the build. Time saved is quoted at 2-3 hrs per pitch **(AxonEstate, vendor claim)**. The same page claims +25% appraisal-to-listing and 70% conversion for "database-intelligence" agents. Treat those as unverified marketing numbers. A US brokerage owner reports a pitch deck going from "a few hours, plus a few more on numbers" to under 30 minutes, and hitting an annual goal in about 4 months (his own figures, not audited).
- **How rare:** Emerging in the US, rare in AU as a bespoke build. REA's Pitch by Realtair is a template tool, not generative or database-aware. The "buyers in your own database matching this property" number is the differentiator. I found no AU agency advertising it.
- **Evidence:**
  - https://axonestate.com/listing-presentation-prep-agent/ (6am brief, buyer pool count)
  - https://www.onewave-ai.com/services/success-stories/michael-rand (Zillow link to property site plus deck, Claude-built)
  - https://www.calish.com/workflows/seller-cma-and-listing-presentation-for-residential-real-estate-team-lead/
  - https://www.realanalytica.com/solutions/listing-appointments (AI-scored comps plus AVM)
  - https://help.realestate.com.au/hc/en-us/articles/900006263423-What-is-Pitch-by-Realtair
  - r/realtors, Dec 2025: "Recently started using AI for them. Can run entire presentation house specific in seconds" (https://www.reddit.com/r/realtors/comments/1pbveh9/what_does_a_listing_presentation_look_like/)
  - Agent-built example, US, Krem Institute write-up: Claude plus ChatGPT used to define the "ideal buyer" for an overpriced vacant home, 36 showings in a week, sold at full price with a 1% concession (agent's own account): https://times.krem.ai/blog-posts/sean-stewart-drove-36-showings-in-one-week-using-ai
- **SA fit:**
  - Comps come from REA CMA, Domain, or the agency's own sales history. Check licence terms before scraping portals. The safe route is the agency's own CRM sales plus any CoreLogic/PriceFinder-type licence they already hold.
  - The "buyer pool" number has to be defensible. Quote only counts the database can back up.
  - SA price rule applies: any price range shown must follow the Land and Business (Sale and Conveyancing) Act (see item 4).
- **Build notes:** n8n or Make trigger from calendar or CRM (Rex/AgentBox/VaultRE API), data pull, Claude for the narrative, then Google Slides or PDF templating. Human review step. Difficulty: medium. The data licensing is the hard bit, not the AI.

### 2. Honest weekly vendor report with an AI "price-expectation" narrative
- **What it does:** Each week the system compiles portal stats (REA/Domain views, saves, enquiries), open-home counts, private inspections, contract requests, buyer feedback themes and moved comps. Claude writes a cover verdict ("slightly behind: here is the one number that proves it"), a comps section and a recommendation. The agent edits and sends it as a branded PDF or vendor-hub link. The commentary is deliberately built to condition the vendor toward a price conversation: week 1 sets the benchmark, week 2 shows the gap, week 3 shows what moved.
- **Money:** Defends listings from being lost to a competitor and speeds price resets, which reduces days on market and fall-through. Agents quoted as spending ~30 min per listing per report, so ~4 hrs a week for 8 listings **(Saabai, vendor claim)**. The real value is a better vendor experience: poor communication is the top complaint in the Reddit threads below.
- **How rare:** Basic AI-drafted reports are common (prompt packs, REA Campaign Assist, Rex AI Assist). A report that is data-fed and has a built-in price-conditioning arc is rare. Vendors reading the hard truth in writing, weekly, is exactly what most agents avoid.
- **Evidence:**
  - https://www.prompt-porter.com/prompt/7fc805ab-1886-4134-aeb0-0a6e4c2b4043 (AU English weekly vendor report agent prompt, Jun 2026)
  - https://realsaturday.com/ and https://qpiq.app/ (AU micro-products that auto-draft the owner report from open-home data; both appear to be very new)
  - https://lockedon.com/features/vendor-reporting (scheduled reports, vendor portal)
  - https://customer.realestate.com.au/residential/nextgen-listings/ (Campaign Assist: "vendor-ready summaries and talking points grounded in exclusive realestate.com.au data")
  - https://help.realestate.com.au/hc/en-us/articles/58140944417177-How-to-use-Campaign-Assist (prompt examples include "Market conditions have shifted since we launched and enquiry has dropped... so I can have a data-backed pricing conversation with my vendor")
  - https://www.saabai.ai/for-real-estate (AU automation shop selling this)
- **SA fit:** Works with AgentBox/Rex/VaultRE exports. Guardrails: the AI must never suggest an advertised range outside the SA rules (item 4), and must never reveal one buyer's offer terms to another buyer. Report goes to the vendor only.
- **Build notes:** Scheduled n8n flow, portal stats (REA Ignite and Domain reports, usually email or CSV), CRM feedback, Claude narrative with a fixed structure and an "evidence ledger" (every claim cites a number). Approval step by the agent. Difficulty: low-medium. Competes with free portal features, so sell the integrated, agency-branded, price-conditioning version, not "reports".

### 3. Buyer-sourced open-home feedback (ask the buyer, rank the callbacks, feed the vendor report)
- **What it does:** QR check-in at the door, plus a 60-90 second SMS or web survey to every attendee. AI scores intent (hot/warm/cool), tags the price reaction, themes the objections, and produces a ranked call list by Monday 7am. The same answers fill the vendor report with real quotes, so the agent isn't reconstructing the open from memory.
- **Money:** Better follow-up on hot buyers means more contracts and offers. It also gives the vendor real buyer evidence for a price change, which is much harder to dismiss than an agent's opinion. No hard numbers found. Mark as qualitative.
- **How rare:** Emerging in AU. Two small products launched, both very new. CRMs have a "feedback" box that the agent fills from memory (qpIQ's pitch). Most agencies don't do it.
- **Evidence:** https://qpiq.app/ ("the one thing VaultRE, Rex and the rest don't do"; data stored in AU, contact details deleted 90 days after campaign close); https://realsaturday.com/ (buyers never named in owner's report, "what the Privacy Act expects"); https://lockedon.com/features/vendor-reporting
- **SA fit:** Privacy Act APPs and the Spam Act matter here: a survey SMS to someone who attended is arguably a related service message, but have the check-in consent wording reviewed. Do not name buyers in the vendor report. Retention rule (delete after N days) is a selling point.
- **Build notes:** Form tool plus Twilio or an SMS gateway, Claude to score and theme free text, write back to the CRM. Difficulty: low-medium. Risk: these small SaaS products could be bought off the shelf, so the pitch is customisation into the agency's own CRM and templates.

### 4. Price-guide conditioning with a compliance guardrail
- **What it does:** A checker sits on every listing draft and every vendor communication. It compares the advertised range against the agency's estimate in the sales agency agreement and the recent sale comps, flags underquoting risk, and drafts the "why the guide must move" comparison for the vendor (comps that sold, pass-ins, days on market). When a listing hits a pre-agreed trigger (for example 2 opens with low attendance and under-benchmark portal views), it prompts the agent to run the price conversation and pre-writes the talking points.
- **Money:** Protects the agency from penalties and loss of commission, and shortens campaigns. SA law: the upper figure of a range must not exceed 110% of the lower, the lower must not be less than the agent's estimate in the sales agency agreement, and penalties include losing commission and expenses (Land and Business (Sale and Conveyancing) Act 1994 s 24A, per SA Law Handbook).
- **How rare:** Rare. I found tools for pricing conversations (REA Campaign Assist) but no one selling an automated compliance check on ranges and AI-written vendor copy. This is my synthesis of a gap, not a product I saw.
- **Evidence:** https://www.lawhandbook.sa.gov.au/ch23s08s03s03.php (the 110% rule and no-symbols rule); REA Campaign Assist prompts above; Zillow research on benchmark engagement vs time to sell (US data, but the benchmark concept transfers): https://www.zillow.com/research/save-shares-views/ (250+ views/day means about a week to pending; 5+ saves/day typically accepts an offer in a week).
- **SA fit:** Directly SA-specific. The agency's own estimate sits in the sales agency agreement, which the system must read or be given. Have a conveyancer or the agency's licensee confirm the rules before sale, because I only read the Law Handbook summary.
- **Build notes:** Claude with structured fields (agreement estimate, current range, comps), simple rule check done in code, not by the LLM. Difficulty: low for the rule check, medium for the comps narrative.

### 5. "Listing win-back radar": appraised-not-listed nurture plus stalled and withdrawn listings
- **What it does:** Two feeds into one call list. (a) Every past appraisal gets an approved nurture cadence (summary email at 24h, market update at 5 days, check-in at 2 weeks, then quarterly "what's sold on your street"), with an alert when the owner replies or a nearby sale lands. (b) A watcher on the agency's suburbs flags withdrawn listings, stale listings, price drops and auction pass-ins, then cross-checks against the agency's own appraisals ("we appraised this in March") and drafts the opener for the agent.
- **Money:** This is where listings are most often lost: the owner lists with whoever stayed in touch. MyTurn claims 73% of vendors who pull a listing still want to sell within 12 months **(vendor claim, unverified)**. Saabai claims 5 hrs/week recovered per agent from automated follow-up **(vendor claim)**. No audited conversion data found.
- **How rare:** Nurture sequences after appraisal are emerging in AU (Saabai, Briick, YMA). The alert feed is a live AU product (MyTurn, 200+ agents, with a Grange SA example on its page). Joining the two with the agency's own appraisal history and an AI-written opener per situation, is rare.
- **Evidence:**
  - https://myturn.property/ and https://myturn.property/realtors (withdrawn, stale, price-drop, pass-in alerts; example opener "Auction day didn't go to plan. Want a second opinion on price?")
  - https://www.saabai.ai/for-real-estate (appraisal follow-up: "the vendor has signed with someone else who stayed in contact")
  - https://www.briick.com/automations/ai-that-follows-up-every-past-appraisal-until-the-owner-is-ready-to-sell
  - https://www.ymaagency.com/blog/vendor-listings-automation-real-estate (Oct 2026)
- **SA fit:** Do Not Call Register applies to calls to withdrawn-listing owners (check if the number is listed, and consider whether the "existing relationship" exception applies, which it usually does not for a cold call). The Spam Act requires consent or an inferred relationship for SMS and email, and an unsubscribe. A past appraisal is a real relationship, which makes it the safer half of this idea. Keep humans on any call.
- **Build notes:** CRM appraisal export, MyTurn-style feed or a lighter in-house scraper (portal terms of use risk, so buy rather than scrape), Claude drafts messages, SMS/email via compliant sender. Difficulty: medium. Very strong for a retainer since it runs weekly.

### 6. Auction campaign manager (bidder scoring, pre-auction offers, reserve conversation, pass-in recovery)
- **What it does:** From registration to hammer: track registered bidders and their engagement (views, enquiries, inspections), flag the likely active bidders, remind everyone the day before, and build the vendor's reserve conversation pack the week of the auction. If the property passes in, within an hour the system drafts the vendor message, the follow-up to every registered bidder, and the negotiation plan.
- **Money:** Auctions are common in Adelaide, and a pass-in is the moment the vendor's agent is most exposed. Fast, structured pass-in recovery is where the sale is saved or lost. No hard results found.
- **How rare:** Emerging in AU. Teylo's auction tool says "AI predicts likely active bidders". Realtair runs the auction platform (not the AI layer). Openn is a transparent online bidding alternative. The vendor-conditioning and pass-in recovery workflow is not something I found sold as a system.
- **Evidence:** https://agent.teylo.com.au/features/auction-management; https://realtair.com/product/online-auctions/; https://www.openn.com/en-au/our-products/openn-negotiation
- **SA fit:** Under the SA Law Handbook an agent must not disclose offer terms to other purchasers before sale and must keep copies of offers. The system must keep one buyer's pre-auction offer out of any buyer-facing message. Check SA auction rules and the cooling-off position with a conveyancer.
- **Build notes:** CRM plus registration form data, scoring in code with an LLM drafting messages, SMS reminders. Difficulty: medium. Good as an add-on module, not a first offer.

### 7. Offer comparison summary for vendors
- **What it does:** When multiple offers come in, the agent uploads the offer documents. AI extracts price, deposit, settlement date, finance and building/pest conditions, special conditions and deadlines into a side-by-side one-pager the vendor can read on their phone, with risks flagged ("subject to sale of buyer's property, 60 days").
- **Money:** Helps close faster and with fewer errors when multiple offers land at once. It also gives the vendor a record. No AU results found.
- **How rare:** Rare in AU, existing in the US as small tools. Both US tools are manual-entry comparators; neither is an extraction pipeline.
- **Evidence:** https://clovia.ai/features/offer-comparison; https://offersummary.com/ (US, adjusted price after concessions, escalation and leaseback terms). Rex AI Assist can log an offer as buyer feedback and draft the vendor email (https://www.rexsoftware.com/articles/10-prompts-to-try-with-ai-assist) but does not compare terms.
- **SA fit:** Offers in SA can be signed contracts or "not a contract" documents, so extraction needs to handle both. Offer details are confidential from other buyers. Sensitive documents mean Australian data hosting and a clear privacy statement. Do not let the AI recommend which offer to accept: present, do not decide.
- **Build notes:** PDF extraction with Claude, a fixed schema, human check of the extracted fields before it reaches the vendor. Difficulty: medium.

### 8. AI walkthrough video from listing photos
- **What it does:** Upload 10-38 photos, AI plans camera moves, animates each scene, and produces a 16:9 walkthrough plus 9:16 reels in 20-40 minutes. Can be wired to fire when a listing's photos land in the CRM.
- **Money:** Replaces a videographer for lower-priced listings. Pay-per-video: **$249 per walkthrough (ReelView, Brisbane)**; **from $270 (720p) and $338 (1080p) (Vinto)**. I did not find AU videographer prices or engagement-lift data, so the saving is an estimate to check with the agency.
- **How rare:** Common as a product (several AU options), rare as something wired into the listing workflow with auto-posting to socials.
- **Evidence:** https://reelview.com.au/ ; https://vinto.com.au/. ReelView offers an optional "AI-Animated from Real Images" disclosure. ABC News, 14 Oct 2026: AI use in listings is growing and regulators want disclosure (https://www.abc.net.au/news/2026-10-14/artificial-intelligence-ai-real-estate-house-listings/107192522).
- **SA fit:** Australian Consumer Law applies: animation must not create a false impression of the property. Disclose AI use. Low value to build custom since it is available off the shelf.
- **Build notes:** Reselling and wiring only. Difficulty: low. Do not lead with this.

### 9. Virtual staging and renovation preview for the vendor pitch
- **What it does:** Before listing, the agent shows the vendor staged or renovated renders of their own rooms ("what a $15k cosmetic update could look like") alongside comparable sales, to justify a price or a pre-sale spend. A second use is staged images in the ad.
- **Money:** Helps win the listing and lift the sale price. No audited numbers found.
- **How rare:** Staging for ads is common. Renovation preview in the listing pitch is rare.
- **Evidence:** ABC News 14 Oct 2026 reports AI-altered furniture, families and even removal of "less attractive" features in AU listings, and quotes the REIA president: "be absolutely explicit that you have done and why you've done that." ACCC says AI images must not create an "overall false impression"; Queensland Fair Trading has issued a best-practice guide. https://www.abc.net.au/news/2026-10-14/artificial-intelligence-ai-real-estate-house-listings/107192522 ; NSW advertising guidance: https://www.nsw.gov.au/housing-and-construction/property-professionals/working-as-an-agent/advertising-guidelines
- **SA fit:** Label every altered image. Never remove defects, power lines, or neighbouring structures. Keep original images on file. A compliance gate in the pipeline (auto-watermark "AI staged", log of originals) is the sellable part.
- **Build notes:** Use an off-the-shelf image model, build the label-and-log workflow. Difficulty: low. A compliance wrapper could be the angle rather than the staging itself.

### 10. Floor plan and room-measurement extraction (and a listing QA check)
- **What it does:** Pulls room labels, areas, dimensions, bedroom/bathroom counts and windows out of a floor plan PDF or image into structured data. A QA step then compares the plan to the listing text and photo captions and flags mismatches ("copy says 4 bedrooms, plan shows 3 plus study").
- **Money:** Mostly risk reduction: avoids misleading-representation complaints and re-work. Time saved is small. The mismatch check is my idea, not a product I saw.
- **How rare:** Extraction tools exist (A-Space, Draftie). Using it as a listing QA gate is rare.
- **Evidence:** https://www.a-space.ai/ ; https://draftie.co/floor-plan-from-image/
- **SA fit:** SA has the Form 1 vendor's statement and ACL representation duties. Treat as a low-priority add-on.
- **Build notes:** Vision model plus rules. Difficulty: low-medium. Low money, so bundle only.

### 11. "Just sold" automation for neighbours
- **What it does:** When a contract goes unconditional in the CRM, the flow picks the nearest addresses, writes the copy using only verified facts (result, days on market, street), builds the card or email, and either orders print and delivery or queues SMS/email to the agency's own database and past appraisals. It then books a follow-up offer ("want to know what yours is worth?").
- **Money:** Feeds the next appraisal. US guide claims a campaign sent within 48 hours of settlement catches peak neighbourhood attention **(vendor guide, not independent)**. AU letterbox drops are priced at about **$140-195 per 1,000 homes**, so a 500-home street is roughly $70-100 plus print (estimate from that price band).
- **How rare:** Common in the US (PostcardMania, Lofty trigger-based mailing, plus DIY guides). Rare as an automated CRM-triggered flow in AU, where agents design cards by hand.
- **Evidence:** https://www.postcardmania.com/services/just-sold-and-just-listed/ ; https://lofty.com/own-your-zip-code ; https://ustechautomations.com/resources/blog/automate-just-sold-postcard-campaign-real-estate-2026 ; AU delivery pricing https://servicesvictoria.com.au/letterbox-distribution/for-real-estate-agents/
- **SA fit:** Get the vendor's consent before naming an address or price. Results claims ("highest price", "record") must be accurate and provable under ACL. Check SA sale-price disclosure and the licensee's own policy before publishing. Pair with Spam Act rules for any email or SMS.
- **Build notes:** CRM webhook, address list from a data provider, Claude for copy, Canva or an HTML-to-PDF template, a print or letterbox partner. Difficulty: low-medium. Easy to demo, and fits Lumen's design skills.

---

## Reviews as a listing-win asset (brief)
REA now publishes an AI summary of an agent's ratings and reviews to prospective vendors (https://customer.realestate.com.au/residential/nextgen-listings/, Apr 2026). That makes review capture at unconditional or settlement, while the vendor is happiest, a direct listing-win lever. This is a common pattern, so mention it only as a module.

## Best 3 from my angle

1. **Appraisal-to-listing engine (ideas 1 and 5 together).** Pre-appraisal brief and deck, plus nurture of past appraisals, plus withdrawn/stale/pass-in alerts matched to the agency's own appraisals. This hits the money directly (each extra listing is thousands in commission), runs weekly, and the agency's own database is the moat. Few AU agencies have it. It is the strongest high-ticket pitch: "which of the last 100 appraisals should we be calling this week?"
2. **Vendor campaign system (ideas 2, 3, 4).** Buyer-sourced feedback, the weekly honest vendor report, and the SA-compliant price-conditioning triggers, all wired to the agency's CRM. This is where vendors say agents fail (see quotes), and it is what makes an agent look different in the next listing presentation. Pitch it as a retention and referral system. The risk is that REA Campaign Assist and Rex Hub cover the basics, so the integration and the pricing arc must be the product.
3. **CRM-triggered "just sold" and auction pass-in machine (ideas 11 and 6).** Easy to demo, tied to design work Lumen already does, and the pass-in recovery module is an uncommon but concrete money play in Adelaide's auction market.

Not worth leading with: AI video (cheap off-the-shelf), floor plan extraction (low value), virtual staging (compliance wrapper only).

## Notable quotes

- "I've messaged him twice this week asking for the realestate.com.au listing metrics and haven't received a reply at all, which I find pretty poor." (first-time seller, r/AusPropertyChat, Jul 2026) https://www.reddit.com/r/AusPropertyChat/comments/1um3gbp/firsttime_seller_are_my_expectations_of_my_real/
- "You are paying your agent a shit tonne of money, plus marketing costs. A basic level of customer service & communication should be an absolute bare minimum requirement." (u/ItsThePeach, who says he is an agent and business owner with ~20 years' experience, same thread)
- "after ever single open he would call from the car on the way to his next open and give me a run down on the numbers. Monday afternoon id get an email and detailed report on all the follow up calls, downloads, re and domain clicks and email enquires etc... I went with him because he was the one that turned up with the most tangible data when we had the initial interviews." (vendor, same thread; this is the listing-win mechanism in one quote)
- "They were very warm and attentive the first three weeks or so, and then I could feel her losing interest as more properties entered her books." (vendor, same thread)
- "He does reply to messages, but it often takes days, and phone calls almost always go unanswered. I feel like I'm constantly chasing him just to get basic updates." (vendor, r/AusPropertyChat, Sep 2025) https://www.reddit.com/r/AusPropertyChat/comments/1nt5jqo/agent_replies_but_super_slow_3_months_on_market/
- "We have only received weekly updates/reports and are clueless if they have actively followed up on the people that had expressly interest... and have no idea what's their strategy." (vendor, PropertyChat, Sep 2024) https://www.propertychat.com.au/community/threads/not-responsive-agent-and-poor-viewings.79919/
- "The painful stuff is still the boring connective tissue: chasing documents, copying data between emails and CRMs, updating statuses, repetitive follow-ups, and spreadsheet archaeology." (r/AusProperty, Aug 2026; a useful warning to keep the pitch practical, not "revolutionary") https://www.reddit.com/r/AusProperty/comments/1vl6bo0/people_working_in_australian_real_estate_what/
- "Every CRM already has a feedback box. The agent fills it in from memory." (qpIQ marketing line, not an agent quote, but it names the gap) https://qpiq.app/

## Caveats
- Result figures (+25%, 70%, 73%, 5 hrs/week) come from vendor marketing pages and are unverified.
- I did not find audited AU case studies with listing-win numbers for any of these ideas, so the pitch to the agency should be framed as a pilot with a measured baseline (appraisal-to-listing rate, hours, days on market).
- SA legal points come from the SA Law Handbook summary and the ABC/NSW pages, not a lawyer. Check with the agency's licensee or a conveyancer before building anything customer-facing.
