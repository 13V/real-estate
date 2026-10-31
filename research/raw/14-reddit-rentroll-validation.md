# Reddit grassroots validation: rent roll / property management picks

Date: 31 Oct 2026. Tool: Agent Reach 1.6 `reddit search` (about 27 searches). Subreddits that returned useful Australian
material: r/AusPropertyChat, r/AusProperty, r/Adelaide, r/AusLegal, r/AusFinance, r/AusRenters, r/shitrentals, r/australia.
US material from r/PropertyManagement, r/AiAutomations, r/PptyMgmtSoftware. No post from r/AusLandlords surfaced in any search
(not verified whether it exists or is searchable).

## How to read this (limits)
- Search returns the post body plus a few top comments, truncated. I could not open full threads, so I did not see most
  replies or outcomes. Quotes below are verbatim from what the search returned.
- Reddit skews to people with a problem. Almost all the Australian voices are **landlords and tenants describing agency
  failures**. Very few are principals or PMs describing what they would pay to fix. So this validates the **pain**, not the
  **willingness to pay**. No principal in these results asked for a tool.
- The AI-in-property threads are mostly vendor or builder self-promotion (MagicDoor, Wattle, a "Nik" fishing for ideas, replies
  by accounts that read like marketing). I flag these; do not treat them as grassroots proof.
- Dates are post dates. Law-specific points (SA water 30 days, Form A1) are what commenters said, not verified law.

---

## Verdict table

| Idea | Verdict | One-line reason |
|---|---|---|
| Landlord churn radar | **STRONG** | Dozens of landlord posts naming exactly the signals (no reply, no inspections, slow repairs, PM turnover, long vacancy) and the moments they switch (re-let, vacancy, PM leaves). |
| PM maintenance autopilot | **STRONG on pain, SOME on solution** | Maintenance/approval/quote delay is the single most common landlord and tenant complaint. The real delay is the landlord-approval and quote loop, not triage. Few real operator AI results. |
| Property memory | **STRONG on pain** | PM turnover plus "nobody told me, new PM knows nothing, old agency won't hand over history" appears repeatedly. Nobody asked for a product. |
| Sale-leak radar | **SOME** | Agencies visibly fight for the sale-to-retain-management link; sale causing PM loss is confirmed; no one describes a prediction tool. |
| SA tenancy clock engine | **SOME** | Water (3 SA threads in 12 months) and rent-increase notice errors are real. Form A1 only indirect. Bond/SACAT is tenant-side. |
| Arrears engine | **SOME** | Wrong or sloppy arrears notices and ledger errors are common (not SA); landlords say arrears chasing is "slow / reactive". |
| Takeover audit | **SOME** | Rent-roll transfers leave landlords with short deadlines, mismatched agreements and lost files. No operator describing an audit. |
| Fee leakage audit | **WEAK / NO for "find fees to charge"; SOME for fee accuracy** | Landlords are already angry about fee stacks and surprise charges, and one near-churned over a wrongly applied fee. No agency voice says it under-charges. SA agent says fees are discounted on purpose to win listings. |

---

## 1. Why landlords leave, and how fast

**Service signals that actually appear (Australian landlord voices):**
- No reply and no inspections:
  - "I was paying a management fee ($175/mo) for basically no service and lack of response." (NSW landlord, 2026) https://www.reddit.com/r/AusPropertyChat/comments/1so1n3r/my_pm_ghosted_me_for_2_years_now_i_have_a_rotting/
  - "no routine inspection and places pressure on LL to fix and repair every minor damage clearly caused by the tenant." https://www.reddit.com/r/AusPropertyChat/comments/1d63b9g/changing_agents_mid_lease/
- Silence while vacant:
  - "It's been 23 days since the real estate company that is managing my investment property listed the property on the rental market. And I have not heard anything from the Property Manager yet". Top reply: "Absolutely that is piss week management. They should be ringing you every week. Deadset absolute minimum." https://www.reddit.com/r/AusProperty/comments/1r607m1/23_days_and_have_not_heard_anything_yet/
- Service decay as an agency grows:
  - "As the agency grew over the last 5 years, the service has really dropped off." Also: "the PM left the lease renewal to the absolute last minute, it genuinely felt like they forgot to send it." (overseas NSW landlord, 12 years with the agency, May 2026) https://www.reddit.com/r/AusPropertyChat/comments/1t7qg6j/time_to_ditch_my_pm_does_a_local_real_estate/
- PM turnover and no continuity:
  - Adelaide thread, PM-insider reply: "They have a massive turnover rate. Average lifespan is 12-18 months. They just get overloaded, like say a few hundred properties per agent, the KPI's are just insane" (u/hal0eight) https://www.reddit.com/r/Adelaide/comments/w8ccz5/frequent_change_of_property_managers/
  - Same thread, landlord: "a lot of them do not do their job properly slow to react to issues etc. I wished that they got in contact with me earlier like issues that affected the tennant like needing a new hot water system." (u/lingerie_fiend)
  - Same thread, SA agent: "People last 12 months or 20 years. It's pretty competitive and there's always a shortage." (u/Jerratt24)
- Money lost plus vacancy: "poor communication, lost 13 weeks of rent from a tenant who stopped paying, and no real support." "All three units have been vacant for 6 months while I've been doing repairs, and the agency hasn't done anything during that time." (franchise changed owners; they now face a $500 break fee) https://www.reddit.com/r/AusPropertyChat/comments/1opukxw/property_management_break_fee/

**How fast they decide.** There are two speeds:
- *Slow drift, then a trigger.* The Chatswood landlord tolerated about five years of decline. Most threads show a single trigger event pushing a long-simmering annoyance over the line: a vacancy, a lease renewal, a repair that stalls, a PM who leaves.
- *Fast exits at specific moments:*
  - PM leaves the business, three weeks before lease end: "all of a sudden the property manager is not responding my emails, and her phone is disconnected... the PM left the business" and the landlord asks whether to manage directly. https://www.reddit.com/r/AusProperty/comments/xitzri/tenants_hope_to_renew_the_lease_can_i_manage_the/
  - Switching timed to the re-let: top comment "I'd switch before. If you're not happy with the current manager, you shouldn't trust them to find a good tenant." https://www.reddit.com/r/AusPropertyChat/comments/1ulxgjy/property_investors_better_to_switch_property/
  - Competitor discount at the one-year mark: "tenant service requests go unanswered for a long time and I have had duplicated charges throughout the year. Another agent in the area has offered me a significant discount on the property management rate I'm paying if I switch." https://www.reddit.com/r/AusPropertyChat/comments/1fif03s/shifting_property_managers/
  - One post is a landlord trying to leave "after signing with them for 2 weeks". https://www.reddit.com/r/AusPropertyChat/comments/1uggs44/property_manager_trying_to_scam/
- *Pricing and vacancy disagreement.* A PM (US sub, Sept 2026) lost an owner this way: "Owner didn't want to reduce the price of the listing and I kept telling him the price is too high, the property staying vacant... he said to me this new company assured him that the price is okay and they'll get it leased." https://www.reddit.com/r/PropertyManagement/comments/1w6xl00/how_do_you_deal_with_losing_a_managementbusiness/
- *Exit friction gives a warning window.* Landlords hit notice periods and break fees: an SA landlord whose "letter to terminate property management agency" was REFUSED (agreement had "several months to run") https://www.reddit.com/r/AusPropertyChat/comments/1cv8pwv/landlords_letter_to_terminate_property_management/ ; a tenant-landlord pair told "120 day notice period for ending their agreement" https://www.reddit.com/r/AusPropertyChat/comments/1fcga4f/advice_needed_re_transferring_from_rental_via_rea_to_direct_with_same_landlord/ . So a landlord who has decided to go often still has weeks to months in the agency's hands: the radar has time to act.
- Adelaide landlords choose by word of mouth and responsiveness: recommendation threads praise "plenty of communication" and "Very responsive", and one tenant says a large agency gave "3 different property managers... in the year" and "required a lot of follow ups". https://www.reddit.com/r/Adelaide/comments/1eyar3m/property_manager_recommendations/ and https://www.reddit.com/r/Adelaide/comments/1kyx5m1/real_estate_recommendation_for_renting_out/

**Verdict, landlord churn radar: STRONG.** Best three quotes: the 23-days post, the Adelaide turnover thread, and the "PM left the business" post.
One design implication from the data: the best predictor is *silence during a vacancy or repair*, which is measurable from
PM-software timestamps (days since last owner contact, open jobs, days vacant). Tenants even note the PM changing without notice
(see property memory).

---

## 2. Landlords selling through a different agent than their PM agency

Honest finding: little direct testimony of landlords saying why they chose another agent. What I found:
- Industry-insider view that PMs are not salespeople: "Property managers are generally terrible salespeople. If they could sell, they'd be selling." (u/fakeuser515357). An agent replies that "Oftentimes, the principal of the company will sell it, and try to sell it to an investor to retain the management - so they don't have to pay the salesperson a cut, and they keep the property." https://www.reddit.com/r/AusPropertyChat/comments/1c0f6j5/selling_ip_with_rea_that_isnt_currently_managing/
- Agencies visibly treat sales as management capture, and it irritates buyers: an agent disclaimer "We do not sell properties to investors who intend to take the management to another agency". https://www.reddit.com/r/AusPropertyChat/comments/1e0ja0w/sale_of_property_conditional_to_retaining_same/
- A PM agency pushing a landlord into a sales agreement just to issue a tenant notice: "Today they sent me the agency agreement contract, and it includes a commission of nearly 3% if the property sells, plus a disclaimer that I could be charged this even if the property doesn't sell." The landlord felt "pushed into a sales contract". https://www.reddit.com/r/AusFinance/comments/1p13xsv/help_selling_investment_property/
- Landlord selling privately to the tenant while managed: "Would I still owe the real estate agency sales commission, since technically they found us the tenant many years ago?" (reply: no, management and sales agreements are different.) https://www.reddit.com/r/AusProperty/comments/1m2z8iy/question_for_agents_do_i_owe_property_managers/
- At sale the buyer takes the management away, and the old PM reacts: "she lowered her fees to 2% to keep the property under her management to which I declined", and the buyer's reason was the "seller agent advising that the old property manager does not manage the properties well". https://www.reddit.com/r/AusProperty/comments/1oc4u7r/property_manager_handover_delay/
- The sale-side agency recommends its own PM to investor buyers ("The vendor's REA suggested a PM who works at same real estate agency"; replies say normal). https://www.reddit.com/r/AusPropertyChat/comments/1jrufom/property_manager_recommended_by_vendors_rea/
- Siloed sales and PM teams: a tenant says the owner sent an appraiser from the same agency, who "called me directly to inform me and arrange a time to visit", while the tenant's third PM in six months did not appear to know. https://www.reddit.com/r/AusProperty/comments/1b3i66t/im_a_tenant_and_my_property_manager_was_changed/ (partial; text cut off).

**Verdict, sale-leak radar: SOME.** Strong on "a sale is a management-loss event and agencies fight over it". Nothing from grassroots about predicting
a sale from PM data; the closest signal is the siloed sales/PM teams and a landlord wanting a tenant out. No Adelaide-specific
thread on this. Note this also hints at a risk: landlords resent being pushed to list with the PM agency, so any nudge must be soft.

---

## 3. Maintenance coordination, tradie dispatch, PM burnout, doors per PM

**The delay is mostly the approval and quote loop.** Quotes:
- "I emailed my property manager back in January to inform them that our dishwasher has stopped working... she stated she was awaiting approval from the landlord. I then didn't hear from her for another 4 weeks... the landlord was not happy with the quote and wanted to arrange another quote." (tenant) https://www.reddit.com/r/AusLegal/comments/1bgtphv/landlord_keeps_ghosting_me/
- "Friday morning comes and the electrician Calls and explains the jobs been cancelled because it never got approved." (tenant; PM said it was approved, electrician said approved 9am that day) https://www.reddit.com/r/AusPropertyChat/comments/1l0q2ur/landlord_agent_ignoring_urgent_repairs/
- Landlord side: "There was a bathroom leakage identified by tenant 6 months ago, and I have been emailing REA back and forth with little to no response... plumber to inspect leakage (cost me $300)... handyman... (cost me $1600)... 3 months later, the same issue is raised again... they have quoted me to do a second plumber inspection and also another handyman fix." https://www.reddit.com/r/AusProperty/comments/1dpees1/real_estate_agent_failing_to_organise_a_fix_for/
- Landlord side: "I asked the agent if they could arrange for two quotes for the work. This was back in April. It's now almost August. Communication has been sporadic." https://www.reddit.com/r/AusFinance/comments/15dmp0s/property_manager_unresponsive/
- Quotes cause friction: "we are being requested to facilitate multiple quotes (all separate companies, all need us to provide access separately)." https://www.reddit.com/r/shitrentals/comments/1eyh6dc/instead_of_simple_repairs_endless_requests_for/ ; a PM-ish reply (Sept 2026): "do you know how hard it is to find three reliable companies, without enormous waiting lists, willing to attend a property and quote for free?" https://www.reddit.com/r/AusPropertyChat/comments/1wbosnb/issues_of_communication_from_landlord_to_rental/
- Tenants use the delay against agencies: coached to "call first then ALWAYS follow up with email" so there is a paper trail for the tribunal. https://www.reddit.com/r/AusPropertyChat/comments/1n16nni/tenant_here_anyone_dealt_with_property_managers/

**PM load and burnout:**
- Ex-residential PM in Australia (state not stated): "Properties: Depends on the office, I ranged from 140 to 170"; salary "$45k including super"; hardest thing "Landlords not wanting to spend money on their investment, Kicking out good tenants at the LL's request, Being abused by both sides". https://www.reddit.com/r/AusProperty/comments/tq636b/becoming_a_property_manager/
- Adelaide reply: "a few hundred properties per agent" (see section 1).
- Second-hand news excerpt posted on Reddit (Dec 2022): "the average tenure of a property manager was now just nine months." https://www.reddit.com/r/LandlordLove/comments/zvak9r/wont_someone_think_of_the_property_managers/ (a quote of a news article, not first-hand).
- A strata-software designer (strata, not residential): "Many companies have a high staff turn over (think up to 30% a year) because they churn through staff and burn them out." https://www.reddit.com/r/AusFinance/comments/up7oou/any_property_or_strata_managers_here_what_does/
- US maintenance coordinator (shows the same shape): "I've already got 14 new maintenance requests... we literally have no system. No priority levels, no triage, nothing." and "I have like 60 different owners and every single one of them has different rule..." (text cut). https://www.reddit.com/r/PropertyManagement/comments/1rcmlea/4_years_as_a_maintenance_coordinator_im_running/
- A PM in Aug 2026 (US-style short-term/long-term mix): "90 LTR and 17 STRs with one maintenance and one cleaner under one owner for 48k is killing my soul." https://www.reddit.com/r/PropertyManagement/comments/1vzmtc0/burnt_out/

**Verdict, PM maintenance autopilot: STRONG on pain.** Reframe from "AI triage of tenant texts" to "an approvals-and-quotes chaser": it
targets the stalled-approval problem, which is what landlords and tenants complain about and what causes churn. The SA/AU data
shows tenant-side bots are not what is missing.

---

## 4. Fees: surprise fees and agreement confusion

- SA fee stack from a landlord about to rent out in SA: "They charge 8.8% of all rent for 'management', but then they also charge: 2.2 weeks rent when they find new tenants, 1.1 weeks rent when they renew a lease, $22 for each inspection, $5.5 a month for 'admin', $2.2 each time rent is collected, $179 for a 'promotional package'... $175 for photos". https://www.reddit.com/r/AusProperty/comments/1e8co78/property_management_fee_add_ons/
- A landlord near-churned over a wrong fee: Ailo "compliance cover" auto-signup. "I opted out but they still charged me. I contacted my agent and they said they'd reverse it, but continued getting charged... it was a disheartening experience and I almost changed agents because of this." https://www.reddit.com/r/AusProperty/comments/1bfbnu5/ailo_compliance_cover_what/
- Duplicated charges as a churn reason: "I have had duplicated charges throughout the year." (see section 1, Melbourne).
- Fee irritation pushing landlords to self-manage: "I'm paying almost 3,500$ a year in related management fees for a job I think I could do with a lovely tenant. It comes out at almost 10% of my rental income to these fees." https://www.reddit.com/r/AusPropertyChat/comments/1ngfdzu/changing_property_management_to_self_managed_mid_lease/
- Landlords cannot read the fee schedule: a post lists "Management fees 8%, Letting fee 2.0 weeks, Renewal fee .50 weeks... Tribunal hearings and costs $77..." and asks "Do these terms seem fair or am I being ripped off?" https://www.reddit.com/r/AusPropertyChat/comments/zv7q24/am_i_being_ripped_off/
- Management fee deducted on a tenant reimbursement the landlord believes should not attract one. https://www.reddit.com/r/AusPropertyChat/comments/1sb43iz/question_about_management_fee/
- Fees are negotiated down by agents on purpose (SA agent): "We're on a standard 8.8% which is highish. I'll usually just go 7.7% from the outset if I want the listing or if it's a valuable property drop to 6 even." https://www.reddit.com/r/AusProperty/comments/1obxtfo/property_managers_adelaide/ ; another SA reply: "It will usually cost about the same for a 12 month period no matter who you choose. It depends how's it's packaged and sold to you." https://www.reddit.com/r/Adelaide/comments/10jxcsn/question_rental_management_fees/
- Exit fees: "$500 break fee" on a 20-year-old agreement with a different franchise owner; an exit fee "due to the 'rent collection commission'" on a property with no rent yet.
- Also: PM acted "without authority", with a landlord saying the tenant "signed a new lease with a 6% rent increase. I'm really not happy about this." https://www.reddit.com/r/AusPropertyChat/comments/1api47j/property_management_acting_without_authority/
- US builder framing the same idea ("Lease audit / income leakage: ... missed late fees, pet fees, insurance lapses"). Only a builder planning a product, not an operator result. https://www.reddit.com/r/AiAutomations/comments/1vqdv4v/title_building_out_an_ai_ops_layer_for_property/

**Verdict, fee leakage audit: WEAK to NO as framed ("raise fees you never charged").** Nobody says they under-charge; some fees are discounted
by design; landlords scrutinise fee schedules and one near-left over a wrong fee. **SOME** if reframed as a **fee accuracy and plain-English
agreement audit**: catch duplicate/wrong charges, show each landlord a clear fee summary, and flag agreements that don't match what's charged.
That protects retention rather than squeezing it. Do not pitch retrospective billing.

---

## 5. SA specifics

**Water recharging (best SA signal).** Three Adelaide threads in about 12 months:
- "We are tenants in SA and have suddenly been asked to pay a large water bill after almost one year, with no bills or water-usage notices provided to us during that time... The agent now says notices were sent by the Rewater". Top comment (32 points) quoted the rule: "The tenant doesn't have to pay for water charges if the landlord doesn't provide a copy of the invoice detailing usage incurred by the tenant within 30 days of the invoice being issued." https://www.reddit.com/r/Adelaide/comments/1pnviyo/tenancy_concern/ (Dec 2025)
- "there was a second water account linked to the property. We had never received bills for this second account until that time... an accumulated charge of approximately $1,500", cause an underground leak. https://www.reddit.com/r/Adelaide/comments/1qd7ofk/rental_advice/ (Jan 2026)
- End-of-lease: "Outstanding water... Water to vacate - They calculated a usage estimate for our move-out meter reading, is this...legal?" https://www.reddit.com/r/Adelaide/comments/1m6ekfw/reasonable_endoflease_deductions_diy_water_bill/ (Jul 2025)
- Caution: older commenters in r/australia (2021) said in SA the bill "must be issued no later than 3 months of invoice date", while the 2025 Adelaide commenter said 30 days. Confirm the current rule with CBS before coding it. https://www.reddit.com/r/australia/comments/nq829y/living_one_year_in_a_rental_and_still_no_water/

**Rent increase rules.** Tenants know them well: "Every 12 months with 60 days notice. The extra notice always makes it seem early. If not enough notice then not valid though." https://www.reddit.com/r/Adelaide/comments/1e85kxz/rental/ ; and a tenant: "This government website says that 60 days' notice must be given, yet our tenancy is up in approx. 40 days... I can't imagine a real estate agency making such an egregious mistake (maybe I'm optimistic)." https://www.reddit.com/r/Adelaide/comments/14239ev/landlord_wants_to_increase_rent_by_200_with_less/ ; also a tenant who says the PM stopped replying before the deadline on a negotiated increase. https://www.reddit.com/r/Adelaide/comments/1dfn9er/rental/

**Form A1 / rental applications.** No thread mentions Form A1 by name (search is up to Oct 2026). Adjacent: tenants angry about data collection. "SA regulations require no more than 2 identifying documents, and prohibit asking for details such as car rego or excessive information about employment" about 2Apply https://www.reddit.com/r/Adelaide/comments/1hhcxf7/psa_2apply_asks_for_an_illegal_amount_of/ (Dec 2024); and (r/australia, 130 points) "Their side hustle is Data harvesting. Real estate agents make bank off selling Data." https://www.reddit.com/r/australia/comments/1g2erp3/submitting_an_application_just_to_view_a_rental/ . This supports a data-retention/deletion message to tenants, but nobody describes PM-side pain.

**Bond / SACAT.** Many tenant threads: deductions disputed ("Charge Tenants $110 for contribution towards restoring and repainting door... No evidence given of how much the actual cost was", https://www.reddit.com/r/Adelaide/comments/1evq7cg/thinking_of_taking_rea_to_sacat_any_advice/ ), SACAT ordering a full bond as arrears on an early exit ( https://www.reddit.com/r/Adelaide/comments/1ga3nba/breaking_lease_maximum_loss_of_rent/ ), and a 14-day dispute window quoted ( https://www.reddit.com/r/AusPropertyChat/comments/1oc561k/excessive_bond_deductions_adelaide/ ). Evidence quality is the common weakness, which fits an "evidence pack" idea, but it is tenant voice only.

**Arrears (not SA-specific):**
- Wrong notices: "usually it's because they've gotten you mixed up with someone else" (r/australia reply); a tenant notes arrears appeared "when my rent was increased and they never updated the direct debit" (Canberra). https://www.reddit.com/r/australia/comments/10hnowf/agency_sent_me_a_second_notice_for_arrears_even/ and https://www.reddit.com/r/canberra/comments/xoydk7/just_another_post_about_a_crappy_property_manager/
- A "system error" meant a notice to vacate "was not received by the tenant" and the tenant who gave notice was told to stay another month: a pure process failure. https://www.reddit.com/r/AusPropertyChat/comments/1kklkoq/real_estate_agent_failed_to_send_notice_to_vacate/ (NSW)
- Landlord: "I've asked my property manager to chase it up, but honestly it hasn't improved much and things feel pretty slow / reactive rather than proactive." (VIC) https://www.reddit.com/r/AusPropertyChat/comments/1sxsrv8/vic_tenant_repeatedly_in_arrears_on_periodic/
- Agent insight: "About 6% of Tenants in an agents portfolio will averagely pay late. Mostly by about 1 week." https://www.reddit.com/r/AusProperty/comments/1hrgka8/tenant_is_a_month_late_for_rent_payment/

**Verdicts:**
- SA tenancy clock engine: **SOME**. Water is the standout (recurring, expensive, SA-only); rent-increase notice errors are plausible but only a tenant's suspicion. Form A1 is untested on Reddit.
- Arrears engine: **SOME**. The best angle is "prevent wrong notices" plus "proactive chase", not just "send correct SA notice".

---

## 6. Agencies or PMs using AI/automation, and what happened

No Australian PM or principal reporting a real AI result surfaced. What did:
- AU "Do you use AI to help manage your properties yet?" and "Curious where AI could genuinely help in Australian property workflows" (Apr and May 2026) draw generic, vendor-sounding lists (FAQs, triage, renewals) and no first-hand outcomes. https://www.reddit.com/r/AusPropertyChat/comments/1ti2oox/do_you_use_ai_to_help_manage_your_properties_yet/ and https://www.reddit.com/r/AusPropertyChat/comments/1svcvkl/curious_where_ai_could_genuinely_help_in/
- Vendor posts presented as community content: MagicDoor ("44% of all maintenance has been solved with AI alone", self-reported) https://www.reddit.com/r/PropertyManagement/comments/1ipnucz/property_managment_software/ ; Wattle "Agent for Property Maintenance" https://www.reddit.com/r/PropertyManagement/comments/1imr8uj/launching_wattle_agent_for_property_maintenance/ ; a builder in r/AiAutomations saying an assistant "reduced daily support workload from hours of calls to about an hour of review" https://www.reddit.com/r/AiAutomations/comments/1rmbb87/built_an_ai_tenant_support_system_for_property/
- US operator caveat on AppFolio's Assisted Maintenance: "Where it struggles is vendor relationship management. If you have preferred vendors you want jobs routed to specifically, or vendors with rate agreements, the automated routing can override that unless you configure it carefully." https://www.reddit.com/r/PropertyManagement/comments/1s1r7dp/any_recommendations_for_helpful_application/
- A user of an AI tool (US, could be a plant): "Residents don't realize they're talking to AI on email... knows when to flag things for our team to handle." https://www.reddit.com/r/PropertyManagement/comments/1jvgnbb/ai_for_property_management/
- Commodity warning: an n8n "Automated Tenant Repair Request Dispatcher" was built in "3 hours" and shared free (June 2026). https://www.reddit.com/r/n8n/comments/1ujzjqg/i_built_an_automated_tenant_repair_request/ So generic dispatch is not a moat.
- Lease/ledger work with Claude is happening in US PM and commercial: "I've been using Claude to scan them in. iPhone pics to folder, Claude reviews and attaches them to my accounting system." (receipts to AppFolio, "10hrs/month" manual) https://www.reddit.com/r/PptyMgmtSoftware/comments/1te6m83/expense_management_automation_for_property/ and a Yardi user: Claude "created journal entries" and "entered opening balances" for a migration https://www.reddit.com/r/yardi/comments/1w3t5gj/any_success_with_3rd_party_ai_agentsplatforms/ . These back the takeover/migration-audit idea only loosely.
- Toop+Toop's HARLI did not appear on Reddit; Adelaide threads mention the agency only as a well-regarded agency for renting/selling. https://www.reddit.com/r/Adelaide/comments/1qjo1fq/real_estate_agent_recommendations_east_adelaide/

---

## Per-idea verdicts with best quotes

### Landlord churn radar: STRONG
1. "I have not heard anything from the Property Manager yet" after 23 days listed; reply "They should be ringing you every week." https://www.reddit.com/r/AusProperty/comments/1r607m1/23_days_and_have_not_heard_anything_yet/
2. "They have a massive turnover rate. Average lifespan is 12-18 months. They just get overloaded..." https://www.reddit.com/r/Adelaide/comments/w8ccz5/frequent_change_of_property_managers/
3. "all of a sudden the property manager is not responding my emails, and her phone is disconnected." https://www.reddit.com/r/AusProperty/comments/xitzri/tenants_hope_to_renew_the_lease_can_i_manage_the/

### Sale-leak radar: SOME
1. "Oftentimes, the principal of the company will sell it, and try to sell it to an investor to retain the management" https://www.reddit.com/r/AusPropertyChat/comments/1c0f6j5/selling_ip_with_rea_that_isnt_currently_managing/
2. "she lowered her fees to 2% to keep the property under her management to which I declined" https://www.reddit.com/r/AusProperty/comments/1oc4u7r/property_manager_handover_delay/
3. "We do not sell properties to investors who intend to take the management to another agency" https://www.reddit.com/r/AusPropertyChat/comments/1e0ja0w/sale_of_property_conditional_to_retaining_same/

### Fee leakage audit: WEAK as framed, SOME as fee accuracy
1. "I opted out but they still charged me... I almost changed agents because of this." https://www.reddit.com/r/AusProperty/comments/1bfbnu5/ailo_compliance_cover_what/
2. "We're on a standard 8.8% which is highish. I'll usually just go 7.7% from the outset if I want the listing" https://www.reddit.com/r/AusProperty/comments/1obxtfo/property_managers_adelaide/
3. "Do these terms seem fair or am I being ripped off?" https://www.reddit.com/r/AusPropertyChat/comments/zv7q24/am_i_being_ripped_off/

### PM maintenance autopilot: STRONG on pain, SOME on proof of solutions
1. "she stated she was awaiting approval from the landlord. I then didn't hear from her for another 4 weeks" https://www.reddit.com/r/AusLegal/comments/1bgtphv/landlord_keeps_ghosting_me/
2. "the electrician Calls and explains the jobs been cancelled because it never got approved." https://www.reddit.com/r/AusPropertyChat/comments/1l0q2ur/landlord_agent_ignoring_urgent_repairs/
3. "I've already got 14 new maintenance requests... we literally have no system. No priority levels, no triage, nothing." https://www.reddit.com/r/PropertyManagement/comments/1rcmlea/4_years_as_a_maintenance_coordinator_im_running/

### SA tenancy clock engine: SOME
1. "suddenly been asked to pay a large water bill after almost one year" + the 30-day rule quote. https://www.reddit.com/r/Adelaide/comments/1pnviyo/tenancy_concern/
2. "an accumulated charge of approximately $1,500" from a second water account. https://www.reddit.com/r/Adelaide/comments/1qd7ofk/rental_advice/
3. "I can't imagine a real estate agency making such an egregious mistake (maybe I'm optimistic)." https://www.reddit.com/r/Adelaide/comments/14239ev/landlord_wants_to_increase_rent_by_200_with_less/

### Takeover audit: SOME
1. WA landlord told their PM is "transferring part of their rent roll to another agency", "less than a week to decide", new agreement with a fixed term and liquidated damages where the old one was rolling. https://www.reddit.com/r/AusPropertyChat/comments/1qi3g0n/property_agency_transferring_their_management_to/
2. "The agreement is 20+ years old... We haven't signed anything with the new owners... We don't even know where the old contract is" https://www.reddit.com/r/AusPropertyChat/comments/1opukxw/property_management_break_fee/
3. Landlord not told when the agency was sold: "I have only signed one management contract with the original agency and have not been alerted to anything related to Ray White." https://www.reddit.com/r/AusProperty/comments/1jav8bc/property_manager_changed_company_and_did_not/

### Arrears engine: SOME
1. "I've asked my property manager to chase it up, but honestly it hasn't improved much and things feel pretty slow / reactive rather than proactive." https://www.reddit.com/r/AusPropertyChat/comments/1sxsrv8/vic_tenant_repeatedly_in_arrears_on_periodic/
2. "They say we're in arrears, we ask how much and from when... they never actually send us anything clear outlining where we went wrong" (WA tenant) https://www.reddit.com/r/perth/comments/10kw5cq/our_rental_real_estate_agents_suck_at/
3. "usually it's because they've gotten you mixed up with someone else." https://www.reddit.com/r/australia/comments/10hnowf/agency_sent_me_a_second_notice_for_arrears_even/

### Property memory: STRONG on pain (no sign anyone buys it)
1. "Each time my property manager was changed they've never let me know... I could never tell if the new property manager was aware of them from the previous one." (tenant) https://www.reddit.com/r/AusProperty/comments/1b3i66t/im_a_tenant_and_my_property_manager_was_changed/
2. "My RE agency got bought out by another agency, our agent left, and so did the one that replaced her (I wasn't notified about any of this when it happened)." https://www.reddit.com/r/AusPropertyChat/comments/1cnp9y6/rolling_over_to_period_lease/
3. "after 10s of emails and 100s of unanswered calls the old REA is not providing us the tenant contact details or rental payment history." https://www.reddit.com/r/AusProperty/comments/194sntx/settled_on_house_old_rea_not_transferring_rental/
Also (vendor-ish, US): a former 300-door PM-turned-builder lists "Losing critical info every time someone quit" as a bottleneck. https://www.reddit.com/r/PropertyManagement/comments/1l8f6xk/anyone_using_ai_to_handle_property_management_ops/

---

## New pain points and ideas that emerged
1. **Approval and quote chaser (the real maintenance bottleneck).** Standing spend limits per landlord, auto-chase of "awaiting landlord approval", quote comparison, a log that proves when approval was requested and given. Evidence: sections 3 and the dishwasher/electrician posts.
2. **Water anomaly watch.** Read SA Water bills and flag a spike or a second account within days, before it becomes a $1,500 recharge dispute that the landlord eats. Evidence: Dec 2025 and Jan 2026 Adelaide threads. Fits SA clock engine but is a more specific, more demoable hook.
3. **Wrong-notice guard for arrears and rent reviews.** Before an arrears notice or rent-increase letter goes out, check the ledger against the latest rent change and direct-debit update, and that landlord approval was recorded. Evidence: false arrears after rent increases and PM changes; "acting without authority" 6% increase.
4. **Landlord vacancy digest.** A weekly "enquiries, applications, feedback, what we changed" report while a place is vacant. The 23-days post shows landlords expect a weekly call. Cheap retention play, fed by the churn radar.
5. **Response-time and repair-compliance trail (agency protection).** Tenants are coached on Reddit to build email timelines for SACAT/NCAT. A timestamped log of requests, responses and approvals protects the agency when a dispute is lodged.
6. **PM-change notice and handover pack.** Auto-notify landlord and tenant when the PM changes, with a one-page property summary. Evidence: repeated "never let me know" posts. Part of property memory, but a tangible first deliverable.
7. **Plain-English agreement and fee summary at onboarding.** Fee schedules confuse landlords ("Am I being ripped off?"). A one-page summary reduces fee disputes and the surprise factor behind "almost changed agents".
8. **Competitor-discount defence.** Landlords report rival agents offering "a significant discount" to switch. The churn radar could flag at-risk landlords on a book whose fee sits above the local norm.
9. **Rent-roll transfer onboarding pack.** For agencies buying or absorbing a roll: reconcile each agreement, ledger and key file, and send landlords a clear transfer letter with a sensible decision period. Evidence: WA "less than a week", "didn't notify me" threads.

## Caveats on strength of evidence
- Strongest overall for a pitch: churn radar (landlord voices are plentiful and specific), approval/quote chaser, water and wrong-notice guards.
- Weakest: fee leakage (as "charge more"), Form A1, and any claim that agencies are asking for AI. The AI-for-PM threads here are dominated by vendors.
- Everything above is anecdote from a self-selected sample; use it to choose which pains to verify with the agency's own data in a leak audit.
