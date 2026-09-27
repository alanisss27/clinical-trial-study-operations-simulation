# Study assumptions and canonical simulation baseline

**Independent Simulation.** All study information, organizations, sites, participants, dates, and outcomes below are invented for portfolio and learning purposes. Names do not refer to real entities. This document demonstrates project-management and study-operations reasoning; it is not a clinical protocol or guidance for conducting a real trial.

This is the source of truth for future connected artifacts. Milestone IDs and scenario references are reserved here for later use; this document is not a timeline tracker, RACI, issue log, vendor tracker, or status report. The scenario's resolution is a scripted future outcome, not evidence of work performed.

## 1. Study overview

| Item | Simulation assumption |
|---|---|
| Study ID | SIM-001 (fictional); a study identifier, not an investigational-product code |
| Phase / product | Phase I, first-in-human investigational vaccine study; no exact vaccine dose quantities or platform are specified |
| High-level objective / population | Describe initial safety, tolerability, and exploratory immune response in adults. These are PM-added assumptions, not verified REDCap eligibility criteria or scientific objectives; scientific design is outside this portfolio's scope |
| Sponsor | Avenrix Study Sponsor, a fictional organization |
| Delivery model | Sponsor-managed, with defined CRO support and outsourced central-laboratory services |
| Participants / groups | 36 total participants; three dose groups (high, medium, low), each with 12 participants: 9 active + 3 placebo. Total: 27 active + 9 placebo. Screening failures are outside the enrolled count |
| Geography / sites | Four fictional U.S. sites; site geography, names, codes, and enrollment allocations are PM-added operational assumptions |
| Duration | Operational baseline: 2027-01-11 through 2027-12-17, approximately 11 months, from startup kickoff through archival handoff; revised archival forecast: 2027-12-21 |
| Participant window | Screening at Week -1; baseline / initial administration at Week 0; boosters at Weeks 4 and 8; EOS at Week 16 relative to baseline, approximately 112 days. The scheduling model uses exactly 112 calendar days |
| Operational scope | Startup, site readiness and activation, recruitment and follow-up coordination, sample collection/shipment, vendor deliverables, data cleaning, database lock, analysis handoff, site closeout, and document reconciliation |

### Planned site enrollment

| Site | Fictional site name | Planned participants |
|---|---|---|
| AV-S01 | Northlake Research Unit | 12 |
| AV-S02 | Cedarfield Research Unit | 10 |
| AV-S03 | Meadowcrest Research Unit | 8 |
| AV-S04 | Harborvale Research Unit | 6 |
| Total | Four sites | 36 |

Dose groups do not correspond to sites. The three 12-participant groups are study-wide treatment allocations; the 12/10/8/6 site targets are independent operational allocations. No site-by-group allocation or exact dose quantity is prescribed here.

### Canonical visit and administration schedule

| REDCap event | Study Operations visit | Week relative to baseline | Calendar-day offset | Scheduled administration |
|---|---|---|---|---|
| Screening | Screening / enrollment for eligible participants | -1 | -7 | None |
| Baseline | Baseline / initial administration | 0 | 0 | Initial administration |
| Followup 1 | Follow-up | 1 | 7 | None |
| Followup 2 | Booster 1 | 4 | 28 | Booster 1 |
| Followup 3 | Follow-up | 5 | 35 | None |
| Followup 4 | Booster 2 | 8 | 56 | Booster 2 |
| Followup 5 | Follow-up | 9 | 63 | None |
| Followup 6 | Follow-up | 12 | 84 | None |
| Followup 7 | Follow-up | 14 | 98 | None |
| EOS | End of Study / final safety review | 16 | 112 | None |

This ten-visit structure is shared across the three dose groups. Administration includes assigned vaccine or placebo. The all-complete simulation plans 108 administrations: 36 initial administrations and 72 boosters. Week 16 is measured from baseline, not from the last booster.

Specimen collection is planned across baseline, the seven follow-up events, and EOS, aligned with the configured REDCap collection-instrument mapping. Traceability links participant, specimen type, visit, and aliquot. This does not assert that every specimen type is collected at every visit or prescribe collection at screening. Exact specimen requirements and identifier syntax remain outside this PM baseline; inconsistent REDCap example punctuation and prefixes are not copied.

### Calendar, enrollment, and source boundaries

All dates use YYYY-MM-DD. PM activities use a Monday-Friday working calendar. This simulation baseline excludes weekends but does not exclude federal holidays; this is a fictional staffing/calendar convention, not a statement about actual vendor availability. Any later holiday exclusions require an explicit calendar revision and impact assessment. Participant visits use calendar-day offsets and may occur outside the PM calendar when clinically scheduled.

For this scheduling simulation, informed consent and screening eligibility confirmation permit enrollment at the Week -1 visit, seven calendar days before initial administration. This is a PM-added milestone convention, not a verified REDCap enrollment definition. Screening failures are not enrolled; participant-specific eligibility and medical readiness are reconfirmed before administration. The all-complete scenario assumes all 36 enrolled participants receive all three assigned administrations and complete Week 16 EOS, without withdrawals, replacements, extension visits, or off-schedule visits. It does not establish protocol completion or withdrawal rules.

The separate SIM-001 REDCap repository was inspected read-only. Its presentation establishes Phase I first-in-human vaccine framing, three groups of 12 with 9 active + 3 placebo per group, ten visits, and Week 16 EOS (pages 3-6 and 13). The Study Operations simulation selects Weeks 4 and 8 as its canonical booster scheduling assumption to align with the configured REDCap event structure on pages 5-6. The REDCap summary on page 4 instead lists Weeks 3 and 6; that reference-source discrepancy is disclosed, not silently resolved or edited. The selected PM schedule is authoritative for future Study Operations artifacts.

Four sites, organizations, calendar dates, governance, enrollment timing, capacity, and lab acceptance gates are PM-added assumptions. REDCap randomization is a demonstration/placeholder, not evidence of production allocation functionality. PM lab transfers and reconciliation do not imply an existing validated automated lab-to-EDC interface. Formal eligibility and withdrawal definitions and exact sample-ID syntax are not established by the available REDCap materials.

## 2. Fictional operational roles and responsibilities

These are responsibilities inside the fictional study. Alanis is the portfolio author, not the person represented as performing any of these professional roles.

| Role / fictional organization | Responsibilities and boundaries |
|---|---|
| Sponsor — Avenrix Study Sponsor | Accountable for study oversight, funding, vendor agreements, and approval of material schedule or scope changes. Authorizes site activation after documented prerequisites. Retains accountability when activities are delegated. |
| Sponsor Clinical Project Manager / Study Lead | Integrates the schedule, coordinates dependencies and deliverable acceptance, maintains issue/action visibility, and prepares escalation and decision requests. Can coordinate approved recovery work; cannot waive clinical, safety, or quality prerequisites. |
| CRO — Brindlepath Clinical Support | Provides startup coordination, readiness evidence collection, monitoring support, site follow-up, and closeout documentation. Recommends readiness to the sponsor; does not independently authorize site activation. |
| Four clinical sites | Site investigators retain clinical decisions and participant safety responsibilities. Site teams manage consent, recruitment, visits, specimen collection/labeling, shipment preparation, source records, and query responses under the fictional approved study documents. |
| Central laboratory — Orivelle Central Laboratory | Owns study-specific specimen instructions, kit configuration and release, accessioning readiness, sample receipt/testing, reconciliation, and agreed result/data deliveries. Its quality function releases its package; sponsor review confirms operational acceptance. |
| Sample/logistics provider — Parcelgrove Clinical Logistics | Supplies scheduled pickup and shipment tracking under the lab's service arrangement. Sites prepare shipments; the provider transports them; the lab confirms receipt and exceptions. Included because shipment readiness is part of the activation gate. |
| Data management — dedicated Brindlepath function | Owns electronic data capture (EDC) setup, query coordination, lab data import checks, reconciliation tracking, and database-lock execution after required sign-offs. Does not release lab kits or make clinical assessments. |
| Biostatistics — sponsor-appointed statistical function | Reviews analysis data requirements, confirms analysis readiness with data management, and delivers the planned summary output after lock. Does not own site activation or the lab readiness release. |
| Safety/pharmacovigilance — sponsor safety function | Owns safety review and reporting processes and safety-data reconciliation with sites/data management. Sponsor medical oversight and investigators decide clinical progression; project staff cannot override their decisions. |

For this simulation, the Study Lead coordinates a weekly cross-functional meeting. A prerequisite forecast to miss its due date and move a dependent milestone is escalated to the sponsor decision owner within one business day. The lab issue uses daily recovery checks until the blocking deliverable is accepted. Detailed governance and RACI will be built later.

## 3. Lifecycle and major workstreams

Startup establishes the approved operational baseline and site prerequisites. Lab readiness and first-site readiness evidence enable sponsor activation of AV-S01. Eligible participants enroll after site activation at Week -1. A separate first-dose readiness check then enables the first initial-administration milestone at Week 0. Other sites activate in a rolling sequence. Enrollment, initial administrations, boosters, and follow-up overlap with ongoing data review. After the last participant's final visit, final data/safety reconciliation enables database lock and analysis handoff. Site closeout and final document reconciliation lead to archival handoff.

| Workstream | Scope needed for later PM artifacts |
|---|---|
| Integrated planning and governance | Baseline dependencies, ownership, escalation thresholds, decisions, actions, and reporting |
| Startup and site readiness | Study-document readiness, approvals and agreements, training, EDC access, product availability, activation evidence |
| Lab, specimens, and logistics | Lab readiness package, kit delivery, collection instructions, pickup readiness, receipt exceptions, and lab data transfers |
| Enrollment and conduct | Recruitment pacing, visit completion, monitoring follow-up, and emerging operational issues |
| Data, safety, and analysis readiness | Rolling queries, lab/clinical/safety reconciliation, lock approvals, and analysis output |
| Closeout and records | Site closeout, investigational-product accountability, outstanding-action closure, and study-file reconciliation/archive handoff |

External deliverables are limited to CRO readiness/monitoring/closeout outputs, the lab readiness package and data transfers, logistics readiness evidence, and data-management/statistical outputs. No separate technology implementation or additional vendor program is assumed.

## 4. Key milestones and dependencies

The baseline below is the corrected SIM-001 fictional plan for 36 participants and Week 16 EOS. It replaces the earlier participant-count and single-administration assumptions. Within this corrected scenario, the baseline remains visible alongside forecasts.

Post-issue means after priority lab recovery but before enrollment-capacity mitigation; it is not the wholly unmitigated lab option. Revised includes both measures selected in DEC-01 on 2027-03-15. Scripted outcomes confirm M03-M06 only; later dates remain conditional forecasts. M08A and M08B are reserved additions that preserve the existing M09-M15 references.

| ID | Milestone | Baseline | Post-issue | Revised forecast | Required predecessor / completion condition |
|---|---|---|---|---|---|
| M01 | Startup kickoff | 2027-01-11 | 2027-01-11 | 2027-01-11 | Sponsor authorizes planning scope and resources |
| M02 | Operational baseline approved | 2027-02-05 | 2027-02-05 | 2027-02-05 | M01; study documents, responsibilities, vendor scope, and schedule assumptions agreed |
| M03 | Central-lab readiness package accepted | 2027-03-19 | 2027-04-02 | 2027-04-02 | M02; released manual and kits, accepted accessioning test, first-site kit receipt, and shipment-readiness evidence |
| M04 | First site activated: AV-S01 | 2027-04-02 | 2027-04-09 | 2027-04-09 | M03 plus site approvals, agreement, training, EDC access, product availability, and sponsor authorization |
| M05 | First-dose readiness confirmed | 2027-04-09 | 2027-04-16 | 2027-04-16 | M04; complete supplies, trained staff, visit coordination, and required medical/safety readiness |
| M06 | First participant receives initial administration | 2027-04-12 | 2027-04-19 | 2027-04-19 | M05; participant enrolled at Week -1 (baseline 2027-04-05; forecast 2027-04-12), with participant-specific readiness reconfirmed |
| M07 | All four sites activated | 2027-04-23 | 2027-04-23 | 2027-04-23 | M03 and M04; each remaining site's prerequisites and sponsor authorization completed |
| M08 | Enrollment complete | 2027-05-14 | 2027-05-21 | 2027-05-18 | M04 and M07; 36 eligible, consented participants enrolled across all groups/sites at their Week -1 visits; no administration-completion claim |
| M08A | Initial-dose completion | 2027-05-21 | 2027-05-28 | 2027-05-25 | M06 and M08; all 36 receive their initial assigned administration, seven calendar days after their respective enrollment visits |
| M09 | Interim data-cleaning review complete | 2027-06-25 | 2027-07-02 | 2027-06-29 | M08A plus 35 calendar days; data through initial administration reviewed, due lab transfers loaded, remaining follow-up queries assigned |
| M08B | Full scheduled administration completion | 2027-07-16 | 2027-07-23 | 2027-07-20 | M08A plus 56 calendar days for the last baseline participant; all 36 complete initial administration and both boosters (108 administrations total) |
| M10 | Last participant last visit (LPLV) | 2027-09-10 | 2027-09-17 | 2027-09-14 | M08A plus 112 calendar days; final participant completes Week 16 EOS; M08B complete under the all-complete assumption; not gated by M09 |
| M11 | Final data and safety reconciliation complete | 2027-10-08 | 2027-10-15 | 2027-10-12 | M09 and M10; final lab transfer accepted 14 days after M10, then 14 days for final reconciliation, material query resolution, and safety sign-off |
| M12 | Database locked | 2027-10-15 | 2027-10-22 | 2027-10-19 | M11 plus 7 calendar days; sponsor, data management, statistical, and required clinical/safety sign-offs |
| M13 | Statistical summary delivered | 2027-11-12 | 2027-11-19 | 2027-11-16 | M12 plus 28 calendar days; locked data received and planned summary reviewed |
| M14 | All site closeout activities complete | 2027-11-26 | 2027-12-03 | 2027-11-30 | M11 and M12; 42 calendar days after M12 for monitoring findings, product accountability, and required site records |
| M15 | Final study-file reconciliation and archival handoff | 2027-12-17 | 2027-12-24 | 2027-12-21 | M13 and M14; 21 calendar days after M14; required deliverables accepted and outstanding operational actions closed |

Enrollment completion, initial-dose completion, full scheduled administration completion, and LPLV are four independently trackable milestones with separate completion evidence and dates. M08 is not a dosing milestone. M08A is not completion of the full regimen. M08B does not imply EOS completion.

### Site capacity and enrollment mitigation

These are aggregate fictional appointment-capacity assumptions, not participant records. Consent, eligibility, treatment allocation, and medical progression remain conditional; no new dose-escalation or between-group release rule is inferred from REDCap.

- AV-S01 plans 12 participants: two initial-administration appointments per week, on Monday and Friday, for the six weeks beginning 2027-04-12 through 2027-05-17. Its final baseline appointments are 2027-05-17 and 2027-05-21. Enrollment/screening appointments occur seven days earlier, so its final baseline enrollment is 2027-05-14.
- AV-S02, AV-S03, and AV-S04 activate by 2027-04-23, begin enrollment no earlier than 2027-04-26, and initial administration no earlier than 2027-05-03. Their planned initial-administration counts in the weeks beginning May 3 / May 10 / May 17 are respectively 4/4/2, 3/3/2, and 2/2/2. This gives 10, 8, and 6 participants; all finish enrollment by 2027-05-14 and initial administration by 2027-05-21.
- Independent approvals/agreement checks, EDC access checks, and product preparation continue during the lab delay. AV-S01 lab-specific training and readiness review finish during 2027-04-05 through 2027-04-09, followed by activation on April 9, first enrollment on April 12, readiness confirmation on April 16, and first initial administration on April 19. Other sites retain their activation and capacity plans.
- Moving AV-S01's opening initial administrations from April 12/16 to April 19/23 loses two opening-week appointments. Six Monday/Friday pairs now run from the week of April 19 through the week of May 24. Its final pair becomes May 24/28, with enrollment on May 17/21. The post-issue study enrollment forecast is therefore **2027-05-21**, and initial-dose completion is **2027-05-28**, each seven calendar days behind baseline.
- The selected mitigation adds **one staffed initial-administration appointment on 2027-05-25**, supported by an added Week -1 enrollment/screening appointment on **2027-05-18**. It brings forward the May 28 administration and May 21 enrollment; the May 24 administration and May 17 enrollment remain. Revised study enrollment completion is **2027-05-18** and initial-dose completion is **2027-05-25**.
- This recovers three calendar days from the post-issue forecast and leaves **four calendar days of residual baseline variance**, equivalent to two Monday-Friday working days. No earlier additional slot is available within the scenario. The mitigation changes neither participant totals nor visit intervals.
- Recurring appointment capacity reserves staff and supplies for all ten visits and specimen pickup for the collection visits, including Week 4/8 boosters and Week 16 EOS. Existing follow-up and booster bookings cannot be displaced to create extra initial-administration capacity. The added appointment requires separate investigator/staff coverage and confirmation of its full follow-up series: June 1, June 22 (booster 1), June 29, July 20 (booster 2), July 27, August 17, August 31, and September 14 (EOS). The three dose groups share this schedule.
- ACT-05 must confirm both the May 18 enrollment and May 25 initial-administration appointments and their downstream capacity. If unavailable, retain May 21 enrollment and May 28 initial-dose completion, and use the post-issue column throughout. Revised dates are forecasts, not achieved outcomes.

### Schedule propagation and calendar allowances

- M03 requires released initial kits received at AV-S01 plus a supply plan for all sites; other sites receive kits and complete lab training before their own activation. M04 to M05 retains one week for first-dose preparation; M06 follows the next Monday. No required review is removed.
- The last baseline initial administration on 2027-05-21 produces final booster completion on 2027-07-16 (+56 days) and LPLV on 2027-09-10 (+112 days). The revised last initial administration on 2027-05-25 produces final booster completion on **2027-07-20** and LPLV on **2027-09-14**. Earlier participants complete earlier under the fixed-offset, all-complete assumption.
- Final lab transfer acceptance is baseline **2027-09-24**, post-issue **2027-10-01**, and revised **2027-09-28**, 14 calendar days after the respective LPLV. Two additional weeks support M11. Final cleaning starts during conduct; it does not wait for LPLV.
- The table preserves all stated elapsed-time allowances after initial-dose completion and LPLV, with no downstream compression. M09, M08B, and M10-M15 retain the four-calendar-day residual variance after mitigation. Each PM milestone falls Monday-Friday under the stated calendar.
- M09 reviews data through initial administration while boosters and follow-up continue; it does not freeze incomplete follow-up data. M13 is a limited summary deliverable, not a full clinical study report or regulatory submission. M14 runs alongside analysis work after lock. Activity-level resource loading will be developed in the future integrated timeline.

## 5. Core operational scenario: central-lab readiness delay

### Original deliverable and discovery

**Deliverable LAB-D01:** a complete study-specific central-laboratory readiness package, due **2027-03-19**, supporting M03. Acceptance requires a quality-released collection/shipping manual, verified kit and label configuration, a successful test of the kit manifest against the lab accessioning system, shipment/pickup instructions, initial released kits received at AV-S01, and a supply plan for the other sites. Sponsor operational acceptance follows lab quality release and CRO/site readiness confirmation.

On **2027-03-12**, the lab's scheduled pre-release test finds that kit barcode identifiers do not map correctly to the configured study visit codes. The lab reports the failed test and forecast delay at the vendor readiness review. The cause is an outdated visit-code mapping used by the kit-assembly team after a configuration handoff; the handoff lacked a documented version check. This is a setup/configuration issue, not an assay-performance failure.

The lab holds release of the affected kits and manual appendices pending correction, relabeling, repeat testing, and quality approval. No participant samples have been collected, and no patient data or safety event is involved in this issue. The initial unmitigated forecast is **2027-04-09** for the complete accepted package.

### Dependency and impact

LAB-D01 acceptance is M03, a mandatory gate to first-site activation (M04). Without released kits and verified specimen identifiers, the site cannot demonstrate that required first-dose samples can be collected and received correctly. A partial manual or shipping promise does not satisfy this gate.

The main downstream milestone at risk is **M06: first participant receives initial administration**, originally **2027-04-12**. The immediate impact is a blocked activation prerequisite, extra lab corrective work, and rescheduling pressure on AV-S01 training and first-participant preparation. Other startup work continues. An unmitigated 2027-04-09 package acceptance would move activation to approximately 2027-04-16 and first dosing to approximately 2027-04-26 under the retained readiness sequence.

### Stakeholders, escalation, and options

The Study Lead coordinates the sponsor decision owner, lab project/quality leads, CRO startup lead, AV-S01 investigator/coordinator, logistics provider, and data-management lead. Sponsor safety/medical oversight confirms that the revised operational plan preserves required readiness; biostatistics is informed because enrollment and final-data forecasts change.

**Escalation trigger:** the lab cannot demonstrate delivery by 2027-03-19 and the missed prerequisite is forecast to move M04/M06. The trigger is met on 2027-03-12; the Study Lead escalates that day. The sponsor decides on **2027-03-15**.

Options considered:

1. Accept the unmitigated delay and reset dependent dates, with first dosing approximately 2027-04-26.
2. Fund priority correction/retesting and expedited shipment, while completing independent site startup work in parallel. Target package acceptance 2027-04-02 and first dosing 2027-04-19. Add a staffed May 18 enrollment/screening appointment and its May 25 initial-administration appointment, moving enrollment completion from May 21 to May 18 and initial-dose completion from May 28 to May 25. Confirm capacity for the associated boosters and Week 16 EOS.
3. Evaluate another lab. New setup, agreements, and readiness testing would not provide a credible near-term recovery, so this option is rejected for this isolated configuration issue.

**Decision required:** approve priority recovery effort and incremental expedited-shipping cost within a fictional sponsor contingency, and approve revised M03-M06 targets, the enrollment-slot mitigation, and the resulting M08, M08A, M08B, and M09-M15 forecasts. No dollar estimate is modeled. Approval does not authorize use of unreleased kits or omission of required reviews.

### Selected response, actions, and resolution

On **2027-03-15**, the sponsor selects option 2. The original baseline remains visible; approved revised targets and eventual outcomes are tracked separately in later artifacts.

- **ACT-01 — Lab:** correct the controlled visit-code mapping, verify affected kit labels, repeat the accessioning test, and obtain quality release by **2027-03-26**. Evidence: approved version record and passing test/release record.
- **ACT-02 — Lab and logistics provider:** ship released initial kits to AV-S01, confirm receipt, and complete package evidence for sponsor acceptance by **2027-04-02**. Remaining sites receive supplies before their activation gates.
- **ACT-03 — CRO and AV-S01, coordinated by Study Lead:** continue independent startup tasks, then finish package-specific training/readiness review during **2027-04-05–2027-04-09**. Sponsor authorizes activation on **2027-04-09**.
- **ACT-04 — Study Lead:** record the approved targets on **2027-03-15**, notify the study team within the fictional scenario, and monitor recovery daily through M03. Confirm first-dose readiness with AV-S01 by **2027-04-16**. Carry enrollment and downstream forecast changes into reporting.

- **ACT-05 - AV-S01 investigator/coordinator, supported by CRO and logistics:** reserve the additional May 18 enrollment/screening and May 25 initial-administration appointments by **2027-04-23**. Confirm staff, investigator, pickup, participant availability, and the complete downstream visit series by **2027-05-14**; document eligibility at enrollment and reconfirm medical readiness before initial administration. The Study Lead retains May 18 enrollment and May 25 initial-dose completion as conditional forecasts until confirmation. If unavailable, use May 21 enrollment and May 28 initial-dose completion and the post-issue downstream dates. This action remains open after lab issue closure.

In the scripted outcome, the lab passes retesting and releases the corrected package on 2027-03-26. AV-S01 confirms kit receipt and the sponsor accepts LAB-D01 on **2027-04-02**. The issue is resolved that day with acceptance evidence; dependent recovery actions remain open until completed. M04 occurs on 2027-04-09, M05 on 2027-04-16, and M06 on **2027-04-19**, seven calendar days later than baseline. M07 retains its April 23 forecast because the other sites complete their own readiness gates. M08 remains forecast for May 18 and M08A for May 25, with M08B and M09-M15 shifted as shown above; no enrollment completion or later outcome is asserted. The lab adds a version check to future configuration handoffs.

### Reserved traceability references for later artifacts

Use one issue throughout; do not create separate copies of the same underlying problem:

**LAB-D01 -> ISS-01 -> M03-M06, M08/M08A/M08B, and M09-M15 -> ESC-01 / DEC-01 -> ACT-01 through ACT-05 -> status narrative.**

- Vendor Deliverables Tracker: LAB-D01 records original due date, forecast, acceptance criteria, evidence, and actual acceptance; links ISS-01.
- RAID / Issue Log: ISS-01 records the confirmed configuration delay, impacts, owner, and closure evidence; links the affected milestones.
- Integrated Timeline: retain baseline dates alongside the post-issue forecast, selected mitigation, revised forecast, and later scripted actuals. M03-M06, M08/M08A/M08B, and M09-M15 show propagated impact; M07 remains unchanged.
- Escalation / decision records: ESC-01 captures the 2027-03-12 escalation; DEC-01 captures the sponsor's 2027-03-15 approval and rationale.
- Action tracking: ACT-01 through ACT-05 carry owners, due dates, and completion evidence; issue closure does not automatically close dependent actions.
- Dashboard / weekly report: report the first-dose milestone at risk on 2027-03-12, approved one-week movement after DEC-01, lab acceptance on 2027-04-02, and achieved first dosing on 2027-04-19. Show enrollment baseline May 14 -> post-issue May 21 -> mitigation-supported forecast May 18; initial-dose completion May 21 -> May 28 -> May 25; full-administration completion July 16 -> July 23 -> July 20; and LPLV September 10 -> September 17 -> September 14. Carry the residual four-calendar-day variance through archival. Continue showing baseline variance and open enrollment actions after lab issue resolution. Formal status-color rules will be defined later.

## 6. Assumptions, boundaries, and next-design decisions

- This is an **Independent Simulation** using entirely fictional study information. No real patient, site, sponsor, CRO, company, or clinical dataset is used. No participant-level records are created at this stage.
- The project is created for portfolio/learning purposes and demonstrates transferable PM and study-operations reasoning. It does **not** represent professional CTM, CPM, CTA, site-management, CRA, clinical vendor ownership, or vendor-oversight experience by Alanis.
- Required clinical/regulatory approvals, investigator oversight, product availability, and safety processes are assumed to be documented before applicable gates. M02 alone does not authorize enrollment. Approval procedures, regulatory timelines, protocol details, eligibility, statistics, and medical decisions are not designed here.
- No safety hold, product shortage, recruitment failure, additional vendor issue, or protocol amendment is added. Clinical progression remains conditional on appropriate medical/safety authorization; the PM plan cannot override it.
- Screening/enrollment is explicitly scheduled at Week -1 after site activation, with initial administration seven calendar days later. Recruitment is not assumed to guarantee consent or eligibility in a real study.
- The lab package is an explicit simulation activation requirement. Parallel startup work limits the first-dose delay; only the additional May 18 enrollment and May 25 initial-administration appointments partially recover enrollment impact. These are fictional planning assumptions, not claims that every real study uses these rules.
- The study duration measures startup through archival handoff, not each participant's duration. Closeout does not imply a regulatory submission or completion of a full clinical study report.
- Before building the timeline, preserve the Week 4/8 boosters, Week 16 EOS, separate completion milestones, rolling activation order, and the documented capacity assumptions. Validate activity-level staffing, participant visit coverage, and parallel startup tasks against this baseline. Any change to the stated Monday-Friday calendar or capacity requires explicit reforecasting.
- The cross-repository audit is complete for the available reference materials. Shared facts and the selected configured REDCap visit schedule are documented in section 1; absent population/objective details and operational extensions are labeled PM assumptions. The REDCap Week 3/6 summary discrepancy remains in that read-only repository, while Week 4/8 is explicitly canonical here. Exact dose quantities, specimen-by-visit requirements, sample-ID syntax, production randomization, and formal withdrawal definitions are not invented or required to build these PM artifacts.
- Only README.md and this source document are in scope now. Workbooks, the five planned artifact categories, additional templates, PDFs, and presentations will be created only in a later step. No commit or push is part of this step.
