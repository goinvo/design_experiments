# Wave: Post-Stroke Rehabilitation Management System

## Project Overview

Wave is a design experiment applying dynamic time-unit project management principles to post-stroke rehabilitation. This prototype reimagines how clinicians coordinate patient care by organizing recovery into milestone-driven "waves" rather than rigid calendar-based protocols.

**Project Type:** Design experiment / High-fidelity interactive prototype  
**Timeline:** Week-long design sprint  
**Primary Users:** Speech-language pathologists (SLP), physical therapists (PT), occupational therapists (OT)  
**Healthcare Context:** Inpatient and outpatient post-stroke rehabilitation

---

## The Problem We're Solving

### Current State Pain Points

Post-stroke rehab clinicians face significant workflow challenges with existing Electronic Health Record (EHR) systems:

**1. Dual System Management**
- Clinicians maintain **separate Excel caseload documents** as workarounds
- Excel tracks: who to see, when, and bare minimum context
- EHR used only for detailed notes and background
- This exists because EHR doesn't provide adequate "working dashboard"

**2. Information Fragmentation**
- Before seeing each patient, clinicians must check **3+ sources**:
  - Excel caseload (scheduling + quick reference)
  - EHR notes (colleague updates, treatment history)  
  - Electronic + physical charts (new medical orders, labs, medications)
- **5-10 minutes per patient** just gathering information
- With 8-12 patients/day = **40-80 minutes of non-clinical time**

**3. Discipline Silos**
- PT, OT, SLP document in separate note sections
- Must manually read each other's notes to stay coordinated
- Weekly team meetings are only sync point - too infrequent
- Critical information gets missed (e.g., PT safety concern not seen by SLP)

**4. No Decision Support**
- Transition decisions (discharge, level-of-care changes) based on intuition + insurance timelines
- Can't easily answer: "How long do similar patients typically need?"
- Difficult to justify extensions or modifications to standard protocols

**5. Rigid Protocols vs. Variable Recovery**
- Standard protocols: "3 weeks inpatient rehab," "6 weeks outpatient PT"
- But stroke recovery is highly variable
- Some patients ready earlier, others need more time
- System doesn't adapt well - forces patients into fixed timelines

### Seven Core EHR Limitations

1. **Calendar-centric, not milestone-centric** - organized by dates rather than achievements
2. **Fragmented multi-disciplinary view** - each discipline works in isolation
3. **No predictive or pattern-recognition capability** - decisions based solely on individual clinical judgment
4. **Transition points are documentation events, not decision support** - no systematic readiness assessment
5. **Progress visibility requires active excavation** - must read through notes to understand trajectory
6. **Rigid templates don't accommodate patient variability** - one-size-fits-all approach
7. **No support for non-linear recovery** - setbacks and regressions treated as "failures" rather than normal variance

---

## The Wave Solution

### Core Concept

**Wave** = A milestone-driven phase of recovery with:
- Defined goals and outcomes (not just duration)
- Flexible timeline (extends/compresses based on patient progress)
- Multi-disciplinary coordination (all teams work toward shared milestones)
- Systematic transition criteria (data-driven, not arbitrary)

### Four Recovery Waves

**Wave 1: Acute Stabilization**
- **Duration:** 3-7 days (typically)
- **Setting:** Acute hospital
- **Goals:** Medical stability, prevent complications, baseline assessments
- **Team:** Neurologist, nurses, initial SLP swallow assessment
- **Transition:** Medically stable, swallow cleared, ready for intensive rehab

**Wave 2: Early Intensive Rehabilitation**
- **Duration:** 2-4 weeks (milestone-driven)
- **Setting:** Inpatient rehab facility
- **Goals:** Maximize neuroplasticity window, regain basic mobility/communication, prevent secondary complications
- **Team:** Physiatrist, PT, OT, SLP, rehab nurses (intensive daily therapy)
- **Transition:** Plateau in rapid gains OR achieved modified independence in basic activities

**Wave 3: Functional Training**
- **Duration:** 4-8 weeks (highly variable)
- **Setting:** Home health or outpatient
- **Goals:** Real-world skill application, home safety, caregiver training
- **Team:** Outpatient therapists, home health nurses, case manager
- **Transition:** Safe at home with supports, functional goals met for current level

**Wave 4: Community Reintegration**
- **Duration:** 3-6 months (can be ongoing)
- **Setting:** Outpatient, community
- **Goals:** Return to meaningful activities, optimize long-term independence
- **Team:** Outpatient therapists, support groups, vocational rehab (if applicable)
- **Transition:** Achieved maximum functional recovery OR transitioned to maintenance

### Key Principles

**Milestone-Driven, Not Time-Driven**
- Progress measured by achievements, not calendar dates
- Example: "Wave 2 ends when patient achieves 75% of mobility + communication milestones OR reaches 21 days with plateau"
- Can extend wave if patient still making rapid gains
- Can compress wave if patient progressing faster than typical

**Multi-Disciplinary Coordination**
- All disciplines (PT, OT, SLP, Nursing) document against same wave milestones
- Shared visibility into what each team accomplished
- Automatic alerts when one discipline flags concern relevant to others
- Unified view eliminates need to read multiple note sections

**Predictive Insights**
- Compare patient to cohort of similar cases (stroke type, severity, age)
- Answer questions like: "Patients with left MCA stroke + moderate aphasia average 18 days in Wave 2"
- Identify patients progressing unusually slow/fast early
- Data-driven timeline estimation for patient/family expectations

**Systematic Transition Support**
- Readiness assessed via checklist, not gut feeling
- Example criteria: milestones met, team assessment complete, no active safety concerns, caregiver trained
- System suggests "extend Wave 2 by 7 days" with auto-justification from milestone data
- Receiving team inherits incomplete goals, builds on previous wave's work

**Customizable Templates**
- Different wave structures for mild vs moderate vs severe strokes
- Adjust intensity: Standard (15 sessions/week) vs Modified (10 sessions/week due to fatigue)
- Add custom milestones: "+ Fall risk management" for patient with balance issues
- System tracks: "Severe stroke patients need X vs mild patients need Y"

**Non-Linear Recovery Support**
- Setbacks documented as normal part of recovery, not failures
- Example: Patient in Wave 3 has fall → temporarily resume Wave 2 intensity protocols → return to Wave 3 when ready
- Recovery timeline visualizes: setback → intervention → recovery
- Pattern recognition: "Patients with falls in Wave 3 often need brief Wave 2 protocols"

---

## Notes for Claude Code

**When building/modifying this prototype:**
- Prioritize clarity over complexity - this is a concept demo, not production software
- Focus on realistic, clinically grounded examples (avoid generic "Lorem Ipsum" data)
- Maintain professional healthcare aesthetic (trust is critical in medical software)
- Make interactions smooth and polished (this will be shown to real clinicians)
- Component structure should support easy Figma sync/iteration
- All patient data is fictional but based on realistic stroke rehabilitation scenarios

**Reference this file** whenever working in this project directory to maintain consistency with the core vision and design principles.

---

## Figma

**Target file:** Design Experiments
**File key:** `yUKPCFiqbv87LmiQn7H3Rn`
**Target page:** Week 2: Healthcare + Waves
**Node ID:** `445:234`
**URL:** https://www.figma.com/design/yUKPCFiqbv87LmiQn7H3Rn/Design-Experiments?node-id=445-234

**When sending screens to Figma**, always use `outputMode: existingFile`, `fileKey: yUKPCFiqbv87LmiQn7H3Rn`, and `nodeId: 445:234` so captures land on the correct page.

**Screen variants** (each is a separate HTML file served via `python3 -m http.server 8080 --directory /Users/maverickchan/maverickchan/design_experiments/wave-stroke-rehab`):
- `stroke-recovery-platform.html` — Dashboard (overview)
- `stroke-recovery-patient.html` — Patient Detail: Overview tab
- `patient-tab-milestones.html` — Patient Detail: Milestones tab
- `patient-tab-team.html` — Patient Detail: Team Notes tab
- `patient-tab-cohort.html` — Patient Detail: Cohort Insights tab
- `patient-tab-timeline.html` — Patient Detail: Timeline & Calendar tab
- `patient-tab-transition.html` — Patient Detail: Transition tab
- `wave-manager.html` — Manager / Team view
- `wave-calendar.html` — Calendar: Week view
- `calendar-month.html` — Calendar: Month view
- `wave-archive.html` — Archive view
- `wave-design-system.html` — Design system (colors, typography, spacing, components)

**Capture notes:**
- App screens use React + Babel standalone — requires `figmadelay=6000` (6s compile time)
- Design system page is pure HTML — `figmadelay=4000` is sufficient
- Capture sequentially (one browser tab at a time) to avoid timeout from resource contention
- Server must be running before opening capture URLs (`lsof -i :8080` to check)
- Always start server with `--directory` pointing to this folder, not from `cd`
