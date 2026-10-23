<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Redwood Valley | Public Health Crisis</title>

<style>
:root {
  --navy: #182d3b;
  --teal: #25675f;
  --gold: #d3b67d;
  --paper: #f5f5f1;
  --ink: #253844;
  --muted: #64717a;
  --line: #dce0df;
}

* { box-sizing: border-box; }

body {
  margin: 0;
  background: var(--paper);
  color: var(--ink);
  font: 15px/1.65 Arial, sans-serif;
}

h1, h2, h3 {
  color: var(--navy);
  line-height: 1.25;
}

h1, h2 {
  font-family: Georgia, serif;
  font-weight: normal;
}

h1 { font-size: clamp(34px, 5vw, 58px); }
h2 { font-size: 28px; }
h3 { font-size: 15px; }
p { margin-top: 0; }

button, input, textarea, select { font: inherit; }
button { cursor: pointer; }

button:focus-visible,
input:focus-visible,
textarea:focus-visible,
select:focus-visible,
summary:focus-visible {
  outline: 3px solid var(--gold);
  outline-offset: 3px;
}

.exercise {
  background: #e9e6dd;
  padding: 8px 5%;
  font-size: 10px;
  letter-spacing: 1.3px;
}

header {
  background: #fff;
  border-bottom: 1px solid var(--line);
  padding: 22px 5%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
}

.brand {
  display: flex;
  gap: 13px;
  align-items: center;
  font-size: 14px;
  letter-spacing: 1.5px;
  font-weight: bold;
}

.seal {
  background: var(--navy);
  color: var(--gold);
  padding: 12px;
  font: 22px Georgia, serif;
}

.brand small {
  display: block;
  font-size: 11px;
  font-weight: normal;
  letter-spacing: .3px;
  color: var(--muted);
}

.eyebrow {
  font-size: 10px;
  letter-spacing: 1.6px;
  text-transform: uppercase;
  font-weight: bold;
}

main {
  max-width: 1320px;
  margin: auto;
  padding: 32px 24px 55px;
}

.hero {
  background: var(--navy);
  color: #fff;
  padding: 44px;
  display: grid;
  grid-template-columns: 1.4fr 1fr;
  gap: 35px;
  align-items: center;
}

.hero h1 { color: #fff; margin: 18px 0; }
.hero em { color: var(--gold); }
.hero p { color: #c5d1d7; }
.hero .eyebrow { color: var(--gold); }

.brief {
  border: 1px solid #55717b;
  background: #193342;
  padding: 24px;
}

.brief h2 { color: #fff; }

.facts {
  display: flex;
  justify-content: space-between;
  gap: 18px;
}

.facts b {
  display: block;
  font: 28px Georgia, serif;
  color: var(--gold);
}

.facts span { font-size: 10px; color: #c5d1d7; }

.grid {
  display: grid;
  grid-template-columns: 1.15fr 1fr;
  gap: 28px;
  margin-top: 28px;
}

.panel {
  background: #fff;
  border: 1px solid var(--line);
  padding: 25px;
}

.setup { border-top: 3px solid var(--teal); }
.muted, .fine { color: var(--muted); }
.fine { font-size: 11px; }

.callout {
  border-left: 3px solid var(--gold);
  padding: 15px 18px;
  background: #f5f2e8;
  margin: 20px 0;
  font-size: 13px;
}

.callout strong { display: block; color: var(--teal); }

label {
  display: block;
  font-size: 13px;
  font-weight: bold;
  margin: 16px 0 7px;
}

input, textarea, select {
  display: block;
  width: 100%;
  border: 1px solid #c7cecf;
  padding: 12px;
  background: #fff;
  border-radius: 3px;
  color: var(--ink);
}

textarea { min-height: 125px; resize: vertical; }

button.primary, button.secondary {
  padding: 12px 18px;
  min-height: 44px;
  border: 1px solid transparent;
  border-radius: 3px;
  font-size: 13px;
  font-weight: bold;
}

.primary { background: var(--teal); color: #fff; }
.primary:hover { background: #174f48; }

.secondary {
  background: #fff;
  color: var(--navy);
  border-color: #c7cecf !important;
}

.full { width: 100%; margin-top: 20px; }

.actions {
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
  margin-top: 18px;
}

.topline {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
  border-bottom: 1px solid var(--line);
  padding-bottom: 20px;
  margin-bottom: 24px;
}

.topline h1 { font: 24px Arial, sans-serif; margin: 8px 0; }
.clock { font: 23px monospace; }
.timer-tools { display: flex; align-items: center; gap: 12px; }

.workspace {
  display: grid;
  grid-template-columns: 185px minmax(0, 1fr) 220px;
  gap: 22px;
  align-items: start;
}

.phase {
  padding: 14px 0;
  border-bottom: 1px solid var(--line);
  font-size: 12px;
  color: var(--muted);
}

.phase.active { color: var(--teal); font-weight: bold; }

.phase span {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 25px;
  height: 25px;
  border: 1px solid var(--line);
  background: #fff;
  margin-right: 7px;
}

.phase.active span { background: var(--teal); color: #fff; }

.round-head {
  padding: 22px 25px;
  background: #fafbf8;
  border-bottom: 1px solid var(--line);
}

.round-head h2 { margin: 12px 0 0; }

.decision {
  background: #fff;
  border: 1px solid var(--line);
}

.body { padding: 25px; }

.role {
  display: inline-block;
  color: var(--teal);
  background: #eaf0ee;
  border: 1px solid #d7e2db;
  padding: 6px 10px;
  font-size: 11px;
  margin-bottom: 17px;
}

.question { font-size: 16px; font-weight: bold; margin-top: 24px; }

.choice {
  display: flex;
  gap: 12px;
  align-items: flex-start;
  border: 1px solid var(--line);
  border-radius: 3px;
  padding: 15px;
  font-weight: normal;
  cursor: pointer;
}

.choice:has(input:checked) {
  border-color: var(--teal);
  background: #edf5f0;
}

.choice input {
  width: 17px;
  height: 17px;
  flex-shrink: 0;
  margin-top: 4px;
  accent-color: var(--teal);
}

.choice strong { display: block; font-size: 13px; }

.choice small {
  display: block;
  color: var(--muted);
  margin-top: 5px;
  font-size: 12px;
}

.custom {
  background: #f2f5f0;
  border: 1px solid var(--line);
  padding: 17px;
  margin-top: 15px;
}

.metric { border-top: 1px solid var(--line); padding: 13px 0; }

.metric-row {
  display: flex;
  justify-content: space-between;
  gap: 8px;
  font-size: 12px;
}

.metric-row b { font: 20px Georgia, serif; }
.track { height: 5px; background: #e6ebe8; margin-top: 9px; }
.track span { display: block; height: 100%; background: var(--teal); }
.metric.risk .track span { background: #bc8866; }
.direction { font-size: 9px; color: var(--muted); }

.warning {
  background: #fbf0e8;
  border: 1px solid #ebd5c4;
  padding: 12px;
  font-size: 12px;
  margin-bottom: 14px;
}

.error { color: #9d352c; font-size: 13px; }
.outcome { font: 22px/1.6 Georgia, serif; color: var(--navy); }

.section {
  border-top: 1px solid var(--line);
  padding-top: 18px;
  margin-top: 22px;
}

.section h3 {
  color: var(--teal);
  font-size: 11px;
  letter-spacing: 1px;
  text-transform: uppercase;
}

.summary-banner {
  background: var(--navy);
  color: #fff;
  padding: 30px;
  border-top: 3px solid var(--gold);
}

.summary-banner h1 { color: #fff; font-size: 39px; margin: 14px 0; }

.final-grid {
  display: grid;
  grid-template-columns: minmax(0, 1fr) 330px;
  gap: 25px;
  margin-top: 25px;
}

.metric-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 18px;
}

.history {
  background: #fff;
  border: 1px solid var(--line);
  margin: 10px 0;
}

.history summary {
  padding: 17px;
  cursor: pointer;
  font-weight: bold;
  font-size: 13px;
}

.history-body {
  border-top: 1px solid var(--line);
  padding: 20px;
  white-space: pre-wrap;
  overflow-wrap: anywhere;
  font-size: 13px;
}

.export { border-top: 3px solid var(--teal); }
.export button { width: 100%; margin: 7px 0; }
.debrief { font-size: 13px; color: var(--muted); padding-left: 20px; }
.debrief li { margin-bottom: 10px; }
.resume { padding: 15px; background: #edf3ed; margin-bottom: 18px; }

footer {
  max-width: 1272px;
  margin: auto;
  border-top: 1px solid var(--line);
  padding: 22px 24px;
  color: var(--muted);
  font-size: 10px;
  display: flex;
  justify-content: space-between;
  gap: 20px;
}

.notice {
  padding: 12px 16px;
  background: #edf3ed;
  border: 1px solid #c7d7c8;
  margin-bottom: 20px;
  font-size: 12px;
}

#print-report { display: none; }
[hidden] { display: none !important; }

@media (max-width: 1000px) {
  .workspace { grid-template-columns: minmax(0, 1fr) 210px; }
  .timeline { grid-column: 1/-1; display: flex; gap: 14px; flex-wrap: wrap; }
  .phase { flex: 1; }
  .timeline .fine { width: 100%; }
  .final-grid { grid-template-columns: minmax(0, 1fr) 290px; }
}

@media (max-width: 650px) {
  main { padding: 20px 16px; }
  .hero, .grid, .workspace, .final-grid { grid-template-columns: 1fr; }
  .hero { padding: 28px; }
  .hero h1 { font-size: 42px; }
  .brand { font-size: 12px; }
  header > .eyebrow { display: none; }
  .panel, .body { padding: 20px; }
  .phase { font-size: 10px; }
  .phase span { display: block; margin-bottom: 5px; }
  .timer-tools { flex-direction: column; gap: 5px; }
  .topline h1 { font-size: 20px; }
  .metric-grid { grid-template-columns: repeat(2, 1fr); }
  .export { grid-row: 1; }
  .summary-banner h1 { font-size: 32px; }
  footer { flex-direction: column; }
  .timeline { gap: 8px; }
}

@media print {
  body > * { display: none !important; }

  #print-report {
    display: block !important;
    white-space: pre-wrap;
    font: 11pt/1.5 Arial, sans-serif;
    color: #111;
    overflow-wrap: anywhere;
  }

  @page { size: letter; margin: .7in; }
}
</style>
</head>

<body>

<div class="exercise">
  EXERCISE ONLY / Fictional scenario · Educational simulation
</div>

<header>
  <div class="brand">
    <span class="seal">RV+</span>
    <span>
      REDWOOD VALLEY
      <small>Emergency Operations Center</small>
    </span>
  </div>
  <span class="eyebrow muted">
    Executive leadership exercise / RV-PH 01
  </span>
</header>

<main>
  <div id="message" role="status" aria-live="polite"></div>
  <div id="app"></div>
</main>

<footer>
  <span>REDWOOD VALLEY / PUBLIC HEALTH RESPONSE</span>
  <span>Fictional educational simulation. Not medical or legal advice.</span>
</footer>

<div id="print-report"></div>

<script>
"use strict";

/* =========================================================
   SIMULATION CONTENT
   ========================================================= */

const content = {
  metricMeta: {
    severity: "Outbreak severity",
    trust: "Community trust",
    capacity: "Hospital capacity",
    legal: "Legal exposure",
    pressure: "Political pressure",
    equity: "Equity impact",
    morale: "Staff morale"
  },

  initialState: {
    severity: 35,
    trust: 65,
    capacity: 70,
    legal: 20,
    pressure: 30,
    equity: 60,
    morale: 65
  },

  rounds: [
    {
      title: "First Alert",
      role: "County Health Director",
      story: "Redwood Valley confirms 12 measles cases. Several patients visited schools, a crowded community event, and a hospital emergency department while potentially infectious. Vaccination coverage varies substantially across neighborhoods.",
      context: "The hospital can manage its facilities and clinical operations. The county health department must separately assess its statutory authority for public health orders.",
      question: "How should your leadership team respond during the first 24 hours?",
      options: [
        {
          title: "Launch a broad emergency response",
          detail: "Public warning, rapid tracing, expanded testing and vaccination access.",
          result: "Response capacity expands quickly, but some residents question the urgency.",
          stakeholder: "The mayor asks whether the public announcement could create unnecessary panic.",
          legal: "Emergency messaging and resource mobilization do not automatically authorize compulsory restrictions.",
          reflection: "How would you explain the level of uncertainty to the public?",
          effects: {
            severity: -9, trust: -3, capacity: -6,
            legal: 3, pressure: 9, equity: 4, morale: -3
          }
        },
        {
          title: "Use a targeted, coordinated response",
          detail: "Notify affected groups, coordinate clinical response, and expand voluntary services.",
          result: "Targeted action reduces disruption, although some exposures remain unidentified.",
          stakeholder: "A school principal asks why families outside the identified exposure network have not been notified.",
          legal: "Targeting should rely on evidence, consistent criteria, and equitable access.",
          reflection: "What evidence would justify expanding the response?",
          effects: {
            severity: -5, trust: 5, capacity: -3,
            legal: -3, pressure: 2, equity: 4, morale: 2
          }
        },
        {
          title: "Begin with voluntary monitoring",
          detail: "Issue limited guidance and rely on healthcare providers to report new cases.",
          result: "Initial disruption is limited, but additional exposures go undetected.",
          stakeholder: "Emergency clinicians report concern that the response is too slow.",
          legal: "Avoiding restrictions reduces some liberty concerns but does not eliminate institutional duties to respond.",
          reflection: "What is the ethical cost of delay?",
          effects: {
            severity: 13, trust: 1, capacity: -8,
            legal: 5, pressure: 6, equity: -6, morale: -7
          }
        }
      ]
    },

    {
      title: "Isolation Dispute",
      role: "Hospital Legal Counsel",
      story: "A patient with suspected measles refuses recommended isolation and wishes to leave the hospital. Several exposed individuals have also declined voluntary guidance.",
      context: "Legal counsel cautions that clinical recommendations, hospital infection-control policies, and government isolation orders involve different sources of authority.",
      question: "How will your team respond to the patient and the broader exposure risk?",
      options: [
        {
          title: "Seek a formal isolation order",
          detail: "Request public health legal review and pursue compulsory measures if authorized.",
          result: "Transmission risk is reduced, but the intervention attracts scrutiny.",
          stakeholder: "A patient advocate demands information about appeal rights, humane conditions, and access to counsel.",
          legal: "Authority, procedural safeguards, necessity, and least-restrictive alternatives must be assessed under applicable law.",
          reflection: "What procedural protections would make this intervention defensible?",
          effects: {
            severity: -11, trust: -9, capacity: -3,
            legal: 12, pressure: 10, equity: -7, morale: -2
          }
        },
        {
          title: "Negotiate supported voluntary isolation",
          detail: "Offer clear information, assistance, and a defined reassessment process.",
          result: "Most individuals cooperate, but some exposure risk persists.",
          stakeholder: "A social worker requests transportation, food, and income support for affected households.",
          legal: "Voluntary compliance may be more sustainable when meaningful supports address practical barriers.",
          reflection: "What happens if voluntary cooperation fails?",
          effects: {
            severity: -5, trust: 9, capacity: -5,
            legal: -5, pressure: -2, equity: 9, morale: 2
          }
        },
        {
          title: "Avoid compulsory measures",
          detail: "Provide advice and allow individuals to determine whether to comply.",
          result: "Individual autonomy is preserved, but additional contacts are exposed.",
          stakeholder: "A parent of an immunocompromised child argues that the response ignores vulnerable residents.",
          legal: "Respect for autonomy must be balanced against foreseeable harms to others.",
          reflection: "When might nonintervention become ethically unacceptable?",
          effects: {
            severity: 15, trust: -5, capacity: -8,
            legal: 7, pressure: 9, equity: -10, morale: -5
          }
        }
      ]
    },

    {
      title: "Workforce Shortage",
      role: "Hospital Chief Operating Officer",
      story: "Hospital admissions are increasing. Several staff members have been exposed, and others are requesting leave. The emergency department is approaching its operational limits.",
      context: "The hospital must address patient safety, employment obligations, infection control, disability-related accommodations, and equitable access to services.",
      question: "What workforce and service strategy will your team adopt?",
      options: [
        {
          title: "Implement aggressive staffing controls",
          detail: "Restrict leave, reassign personnel, and reduce nonurgent services.",
          result: "Short-term clinical coverage improves, but staff exhaustion and grievances rise.",
          stakeholder: "Nursing leadership challenges the fairness and safety of mandatory reassignments.",
          legal: "Employment rules, safety duties, collective agreements where applicable, and accommodation requirements need review.",
          reflection: "How do you protect staff without compromising patient care?",
          effects: {
            severity: -6, trust: -4, capacity: 12,
            legal: 12, pressure: 5, equity: -7, morale: -15
          }
        },
        {
          title: "Use supported surge staffing",
          detail: "Recruit temporary support, offer accommodations, and prioritize care.",
          result: "The hospital stabilizes more slowly but preserves greater workforce cooperation.",
          stakeholder: "A finance officer warns that temporary staffing and support programs will be expensive.",
          legal: "Document transparent triage and staffing criteria while considering reasonable accommodations.",
          reflection: "How should limited resources be allocated fairly?",
          effects: {
            severity: -5, trust: 5, capacity: 8,
            legal: -4, pressure: 1, equity: 7, morale: 10
          }
        },
        {
          title: "Maintain normal staffing policies",
          detail: "Rely on existing schedules and voluntary overtime.",
          result: "Immediate workplace conflict is limited, but service delays worsen.",
          stakeholder: "An emergency physician reports unsafe wait times and growing burnout.",
          legal: "Maintaining ordinary policies does not remove obligations to address foreseeable safety risks.",
          reflection: "At what point must normal operations be altered?",
          effects: {
            severity: 10, trust: -5, capacity: -17,
            legal: 7, pressure: 7, equity: -8, morale: -7
          }
        }
      ]
    },

    {
      title: "Public Backlash",
      role: "Community Relations Director",
      story: "A social media post alleges that hospital policies favor affluent neighborhoods. A community leader disputes the county's case figures, and reporters demand a public response.",
      context: "Public communication must protect confidential information while addressing misinformation, uncertainty, and legitimate concerns about unequal access.",
      question: "How will your team respond publicly?",
      options: [
        {
          title: "Directly challenge public critics",
          detail: "Issue a strong statement defending the response and correcting disputed claims.",
          result: "The message is clear, but the conflict becomes more visible.",
          stakeholder: "A community organizer says officials are dismissing residents' lived experiences.",
          legal: "Accuracy and privacy are essential. Public disagreement should not become retaliation or unsupported disclosure.",
          reflection: "How can officials correct misinformation without silencing criticism?",
          effects: {
            severity: -2, trust: -12, capacity: 0,
            legal: 5, pressure: 13, equity: -5, morale: 1
          }
        },
        {
          title: "Hold a transparent community briefing",
          detail: "Share verified information, acknowledge gaps, and invite participation.",
          result: "Trust improves, although the team faces difficult public questions.",
          stakeholder: "A local clinician requests translated updates and accessible vaccination services.",
          legal: "Communications should avoid identifiable patient information and unsupported claims.",
          reflection: "How will you show that community input changes policy?",
          effects: {
            severity: -4, trust: 13, capacity: -3,
            legal: -5, pressure: -7, equity: 10, morale: 4
          }
        },
        {
          title: "Limit public comment",
          detail: "Release a brief written statement and avoid further media engagement.",
          result: "The organization avoids immediate confrontation, but rumors intensify.",
          stakeholder: "A reporter questions why leadership is withholding information.",
          legal: "Privacy duties do not generally justify withholding all aggregate public health information.",
          reflection: "What are the risks of remaining silent during uncertainty?",
          effects: {
            severity: 5, trust: -13, capacity: 0,
            legal: 4, pressure: 11, equity: -7, morale: -3
          }
        }
      ]
    },

    {
      title: "Stabilization and Recovery",
      role: "Regional Emergency Coordinator",
      story: "The crisis enters its third week. Transmission appears to be slowing in some areas, but hospital staff are exhausted and residents are demanding a timeline for lifting emergency measures.",
      context: "The leadership team must distinguish temporary emergency actions from long-term policies and determine what evidence supports de-escalation.",
      question: "What recovery strategy will you adopt?",
      options: [
        {
          title: "Maintain broad emergency controls",
          detail: "Continue restrictions until case activity falls substantially.",
          result: "Risk remains controlled, but frustration and resource strain grow.",
          stakeholder: "Business and patient groups demand a clear justification for continuing restrictions.",
          legal: "Emergency measures require ongoing review for necessity, proportionality, and legal authority.",
          reflection: "What objective conditions would trigger repeal?",
          effects: {
            severity: -12, trust: -9, capacity: -8,
            legal: 10, pressure: 12, equity: -5, morale: -9
          }
        },
        {
          title: "Use phased, evidence-based recovery",
          detail: "Set public thresholds, restore services gradually, and audit equity impacts.",
          result: "Recovery progresses with continued monitoring and transparent criteria.",
          stakeholder: "A patient representative requests a public review of delays and unequal treatment.",
          legal: "Documented criteria and review processes can strengthen accountability.",
          reflection: "How will the organization evaluate its emergency decisions?",
          effects: {
            severity: -7, trust: 11, capacity: 10,
            legal: -7, pressure: -7, equity: 10, morale: 9
          }
        },
        {
          title: "End emergency measures immediately",
          detail: "Restore normal operations and leave future precautions voluntary.",
          result: "Some services recover quickly, but renewed transmission becomes a concern.",
          stakeholder: "Infection prevention staff warn that surveillance is insufficient.",
          legal: "The decision should consider available evidence and continuing duties to vulnerable populations.",
          reflection: "How would you respond if cases rise again?",
          effects: {
            severity: 13, trust: 2, capacity: 7,
            legal: 6, pressure: 4, equity: -7, morale: 5
          }
        }
      ]
    }
  ]
};

/* =========================================================
   SIMULATION LOGIC
   ========================================================= */

const { rounds, metricMeta, initialState } = content;
const clamp = n => Math.max(0, Math.min(100, n));

function initial(participant) {
  return {
    version: 1,
    participant,
    started: new Date().toISOString(),
    completed: null,
    round: 0,
    phase: "decision",
    selected: null,
    reasoning: "",
    custom: "",
    strategy: 1,
    metrics: { ...initialState },
    history: [],
    remaining: 2700,
    paused: false,
    checkpoint: Date.now(),
    finalReflection: ""
  };
}

function contextNotes(m) {
  const notes = [];

  if (m.severity >= 60) {
    notes.push(
      "Escalation: transmission is accelerating. The next decision carries greater clinical urgency."
    );
  }

  if (m.trust <= 40) {
    notes.push(
      "Trust crisis: community groups now question official guidance and demand independent review."
    );
  }

  if (m.capacity <= 40) {
    notes.push(
      "Capacity crisis: hospital leadership reports serious constraints on available services."
    );
  }

  if (m.legal >= 55) {
    notes.push(
      "Legal challenge: counsel reports growing requests for documentation and review."
    );
  }

  if (m.equity <= 35) {
    notes.push(
      "Equity warning: underserved neighborhoods report disproportionate barriers to care."
    );
  }

  return notes;
}

function decide(s) {
  if (s.phase !== "decision" || s.history.length !== s.round) {
    throw Error("This decision has already been submitted.");
  }

  if (![0, 1, 2, 3].includes(s.selected)) {
    throw Error("Choose a response before submitting your decision.");
  }

  if (s.reasoning.trim().length < 20) {
    throw Error(
      "Explain your legal and ethical reasoning in at least 20 characters."
    );
  }

  if (s.selected === 3 && s.custom.trim().length < 20) {
    throw Error(
      "Describe your alternative policy in at least 20 characters."
    );
  }

  const index = s.selected === 3 ? Number(s.strategy) : s.selected;

  if (![0, 1, 2].includes(index)) {
    throw Error("Choose a modeled approach for your policy.");
  }

  const round = rounds[s.round];
  const option = round.options[index];
  const before = { ...s.metrics };
  const after = { ...before };
  const warnings = [];

  if (before.severity >= 60) {
    warnings.push(
      "High transmission magnifies the consequences of any delay or gaps in implementation."
    );

    if (index === 2) {
      after.severity = clamp(after.severity + 5);
    }
  }

  if (before.trust <= 40 && index === 0) {
    warnings.push(
      "Low community trust increases resistance to restrictive policies."
    );
    after.trust = clamp(after.trust - 5);
  }

  if (before.capacity <= 40 && s.round >= 2) {
    warnings.push(
      "Existing hospital strain limits the effectiveness of this response."
    );
    after.capacity = clamp(after.capacity - 4);
  }

  for (const k of Object.keys(after)) {
    after[k] = clamp(after[k] + option.effects[k]);
  }

  const entry = {
    round: s.round + 1,
    title: round.title,
    role: round.role,
    story: round.story,
    context: round.context,
    contextNotes: contextNotes(before),
    question: round.question,
    options: round.options.map(o => ({
      title: o.title,
      detail: o.detail
    })),
    selected: s.selected,
    choice: s.selected === 3
      ? "Alternative policy: " + s.custom.trim()
      : option.title,
    custom: s.selected === 3 ? s.custom.trim() : "",
    strategy: option.title,
    reasoning: s.reasoning.trim(),
    before,
    after,
    consequence: option.result,
    stakeholder: option.stakeholder,
    legal: option.legal,
    prompt: option.reflection,
    reflection: "",
    warnings
  };

  return {
    ...s,
    phase: "consequence",
    metrics: after,
    history: [...s.history, entry]
  };
}

function advance(s) {
  if (s.phase !== "consequence") return s;

  if (s.round === rounds.length - 1) {
    return {
      ...s,
      phase: "complete",
      completed: new Date().toISOString()
    };
  }

  return {
    ...s,
    round: s.round + 1,
    phase: "decision",
    selected: null,
    reasoning: "",
    custom: "",
    strategy: 1
  };
}

function narrative(m) {
  return [
    m.severity >= 65
      ? "The outbreak remains difficult to control."
      : m.severity <= 30
        ? "The response has substantially reduced the simulated outbreak severity."
        : "The outbreak shows partial stabilization.",

    m.trust <= 40
      ? "Public trust is fragile, complicating recovery."
      : m.trust >= 70
        ? "Public trust is relatively strong, which supported recovery efforts."
        : "Public trust is mixed, requiring continued communication and accountability.",

    m.capacity <= 40
      ? "Hospital capacity remains a major risk to long-term operations."
      : m.capacity >= 70
        ? "The system has regained enough operational capacity to function more steadily."
        : "Operational capacity is unstable but manageable.",

    m.legal >= 60
      ? "Legal exposure remains elevated and will likely require formal review of decisions."
      : m.legal <= 30
        ? "Legal exposure is relatively contained, though future disputes remain possible."
        : "Legal exposure requires continued attention during recovery."
  ].join(" ");
}

const debrief = [
  "Which decision presented the greatest conflict between public safety and individual rights?",
  "Where did hospital authority end and public health authority begin?",
  "Which groups experienced disproportionate burdens?",
  "How did your communication choices affect trust?",
  "What would you change with better information?",
  "What safeguards would you require before implementing your most restrictive policy?"
];

/* =========================================================
   REPORT CONTENT
   ========================================================= */

function reportBlocks(s) {
  const blocks = [
    ["title", "PUBLIC HEALTH CRISIS"],
    ["subtitle", "Redwood Valley | Executive Leadership Simulation"],
    ["label", "AFTER-ACTION DECISION RECORD"],
    ["body", "Participant(s): " + (s.participant || "Not specified")],
    ["body", "Started: " + new Date(s.started).toLocaleString()],
    ["body", "Completed: " + (
      s.completed
        ? new Date(s.completed).toLocaleString()
        : "In progress"
    )],
    ["body", "Timer remaining: " +
      Math.floor(s.remaining / 60) + ":" +
      String(s.remaining % 60).padStart(2, "0")],
    ["note", "Fictional educational exercise. Indicators are teaching estimates, not epidemiological predictions, legal evaluations, or grades."],
    ["heading", "Executive summary"],
    ["body", narrative(s.metrics)],
    ["heading", "Final indicators"]
  ];

  for (const [k, label] of Object.entries(metricMeta)) {
    blocks.push([
      "body",
      `${label}: ${s.metrics[k]}/100 (initial: ${initialState[k]})`
    ]);
  }

  for (const e of s.history) {
    blocks.push(
      ["round", `Decision ${e.round} | ${e.title}`],
      ["body", "Role: " + e.role],
      ["label", "SCENARIO"],
      ["body", e.story],
      ["body", "Authority briefing: " + e.context]
    );

    if (e.contextNotes.length) {
      blocks.push([
        "body",
        "Situation updates: " + e.contextNotes.join(" ")
      ]);
    }

    blocks.push(
      ["label", "DECISION POINT"],
      ["body", e.question],
      ["label", "AVAILABLE RESPONSES"]
    );

    e.options.forEach((o, i) => {
      blocks.push([
        "body",
        `${String.fromCharCode(65 + i)}. ${o.title} — ${o.detail}`
      ]);
    });

    blocks.push(
      ["body", "D. Propose an alternative or blended policy."],
      ["label", "SELECTED RESPONSE"],
      ["body", e.choice]
    );

    if (e.custom) {
      blocks.push([
        "note",
        "Alternative policy consequences are modeled using: " +
        e.strategy +
        ". The app does not evaluate free-text policy content."
      ]);
    }

    blocks.push(
      ["label", "LEGAL AND ETHICAL REASONING"],
      ["body", e.reasoning],
      ["label", "CONSEQUENCE"],
      ["body", e.consequence],
      ["label", "STAKEHOLDER RESPONSE"],
      ["body", e.stakeholder],
      ["label", "LEGAL AND ETHICAL CONSIDERATIONS"],
      ["body", e.legal]
    );

    if (e.warnings.length) {
      blocks.push(["body", e.warnings.join(" ")]);
    }

    blocks.push(["label", "INDICATOR CHANGES"]);

    for (const [k, label] of Object.entries(metricMeta)) {
      const change = e.after[k] - e.before[k];

      blocks.push([
        "body",
        `${label}: ${e.before[k]} → ${e.after[k]} (${change >= 0 ? "+" : ""}${change})`
      ]);
    }

    blocks.push(
      ["label", "ROUND REFLECTION"],
      ["body", e.prompt],
      ["body", e.reflection || "No round reflection provided."]
    );
  }

  blocks.push(["heading", "Leadership debrief"]);

  debrief.forEach((q, i) => {
    blocks.push(["body", `${i + 1}. ${q}`]);
  });

  blocks.push(
    ["heading", "Final team reflection"],
    ["body", s.finalReflection.trim() || "No final reflection provided."],
    ["note", "Generated from this team's completed simulation. Downloading does not submit work to Canvas."]
  );

  return blocks;
}

function reportText(s) {
  return reportBlocks(s).map(([type, text]) => {
    if (["title", "heading", "round"].includes(type)) {
      return "\n" + text + "\n" +
        "─".repeat(Math.min(65, text.length));
    }

    return text;
  }).join("\n\n");
}

/* =========================================================
   INTERFACE AND LOCAL SAVING
   ========================================================= */

const app = document.getElementById("app");
const $ = id => document.getElementById(id);
const KEY = "redwood-valley-copy-paste-v1";

const esc = value => String(value ?? "").replace(
  /[&<>"']/g,
  c => ({
    "&": "&amp;",
    "<": "&lt;",
    ">": "&gt;",
    '"': "&quot;",
    "'": "&#39;"
  }[c])
);

let state = null;
let saved = null;
let storageOK = true;
let lastTick = Date.now();

try {
  const raw = localStorage.getItem(KEY);

  if (raw) {
    const s = JSON.parse(raw);

    if (
      s.version === 1 &&
      Array.isArray(s.history) &&
      s.metrics &&
      s.round >= 0 &&
      s.round < 5 &&
      ["decision", "consequence", "complete"].includes(s.phase)
    ) {
      saved = s;
    }
  }
} catch {
  storageOK = false;
}

function message(text) {
  $("message").innerHTML = text
    ? `<div class="notice">${esc(text)}</div>`
    : "";
}

function save() {
  if (!state) return;

  state.checkpoint = Date.now();
  saved = state;

  try {
    localStorage.setItem(KEY, JSON.stringify(state));
  } catch {
    if (storageOK) {
      message(
        "Browser saving is unavailable. Keep this tab open and download your record before leaving."
      );
    }

    storageOK = false;
  }
}

function time() {
  return Math.floor(state.remaining / 60) + ":" +
    String(state.remaining % 60).padStart(2, "0");
}

function goTop() {
  window.scrollTo({ top: 0, behavior: "instant" });

  const h = app.querySelector("h1,h2");

  if (h) {
    h.tabIndex = -1;
    h.focus({ preventScroll: true });
  }
}

const directions = {
  severity: "Lower = less severe",
  trust: "Higher = stronger trust",
  capacity: "Higher = more capacity",
  legal: "Lower = less exposure",
  pressure: "Lower = less pressure",
  equity: "Higher = more equitable access",
  morale: "Higher = stronger morale"
};

function metrics() {
  return Object.entries(metricMeta).map(([k, label]) => `
    <div class="metric ${["severity", "legal", "pressure"].includes(k) ? "risk" : ""}">
      <div class="metric-row">
        <span>${esc(label)}</span>
        <b>
          ${state.metrics[k]}
          <small style="font:10px Arial">/100</small>
        </b>
      </div>
      <div class="direction">${directions[k]}</div>
      <div
        class="track"
        role="meter"
        aria-label="${esc(label)}"
        aria-valuenow="${state.metrics[k]}"
        aria-valuemin="0"
        aria-valuemax="100"
      >
        <span style="width:${state.metrics[k]}%"></span>
      </div>
    </div>
  `).join("");
}

function home() {
  state = null;

  app.innerHTML = `
    <section class="hero">
      <div>
        <div class="eyebrow">
          Public health crisis · Executive simulation
        </div>
        <h1>
          The next decision<br>
          changes <em>the response.</em>
        </h1>
        <p>
          An emerging outbreak. A divided community. Five decisions
          that will test how you lead when public health, individual
          rights, and institutional responsibilities collide.
        </p>
        <p class="fine">
          5 decision points · 45-minute suggested time ·
          Individual or team exercise
        </p>
      </div>

      <div class="brief">
        <div class="eyebrow">
          Situation brief 001 / Initial alert
        </div>
        <h2>Redwood Valley</h2>
        <p>
          Suspected measles outbreak<br>
          Regional response activation
        </p>
        <div class="facts">
          <div><b>240k</b><span>RESIDENTS</span></div>
          <div><b>2</b><span>HOSPITALS</span></div>
          <div><b>12</b><span>INITIAL CASES</span></div>
        </div>
        <p class="fine" style="margin:20px 0 0">
          FICTIONAL REGION / EXERCISE DATA
        </p>
      </div>
    </section>

    <div class="grid">
      <section>
        <h2>Your executive briefing</h2>
        <p>
          You are the executive leadership team responsible for
          coordinating a response to an escalating infectious disease
          emergency in fictional Redwood Valley. Several large
          community gatherings have preceded a suspected measles
          outbreak.
        </p>

        <div class="callout">
          <strong>Your mission</strong>
          Protect public health while navigating legal authority,
          patient rights, organizational constraints, equity,
          political pressure, and community trust.
        </div>

        <p>
          There is no single perfect solution. Review each briefing,
          choose a policy, explain its legal and ethical tradeoffs,
          and consider its consequences.
        </p>

        <ol>
          ${rounds.map(r => `<li>${esc(r.title)}</li>`).join("")}
        </ol>

        <p class="fine">
          Use one device per participant or team. Progress stays in
          this browser. At completion, download your decision record
          and submit it in Canvas as directed.
        </p>
      </section>

      <section class="panel setup">
        <div class="eyebrow">Enter the operations center</div>
        <h2>Prepare your response</h2>

        ${saved ? `
          <div class="resume">
            <p>
              ${saved.phase === "complete"
                ? "Your completed decision record is available."
                : `Saved at decision ${saved.round + 1} of 5.`}
            </p>
            <button class="primary" data-action="resume">
              ${saved.phase === "complete"
                ? "Open completed record"
                : "Resume simulation"}
            </button>
          </div>
        ` : ""}

        <form id="start">
          <label for="participant">
            Participant name(s)
            <span class="muted">(optional)</span>
          </label>
          <input
            id="participant"
            name="participant"
            maxlength="250"
            placeholder="Who is completing this exercise?"
            autocomplete="off"
          >
          <button class="primary full" type="submit">
            Begin simulation →
          </button>
        </form>

        <p class="fine">
          The 45-minute timer is a discussion guide. You can pause
          it, and reaching zero does not lock the activity.
        </p>

        <p class="fine">
          ${storageOK
            ? "Progress saves in this browser when storage is available."
            : "Browser saving is unavailable; keep this tab open."}
          Indicators are fictional teaching estimates, not grades
          or clinical predictions.
        </p>
      </section>
    </div>
  `;
}

function choiceHTML() {
  const r = rounds[state.round];

  return `
    <span class="role">YOUR ROLE / ${esc(r.role)}</span>
    <p>${esc(r.story)}</p>

    ${contextNotes(state.metrics).map(n => `
      <div class="warning">${esc(n)}</div>
    `).join("")}

    <div class="callout">
      <strong>Authority & context</strong>
      ${esc(r.context)}
    </div>

    <p class="question">${esc(r.question)}</p>

    <form id="decision">
      <fieldset style="border:0;padding:0;margin:0">
        <legend class="fine">Choose your executive response</legend>

        ${[
          ...r.options,
          {
            title: "Propose an alternative or blended policy",
            detail: "Describe your approach and select the response model to apply."
          }
        ].map((o, i) => `
          <label class="choice">
            <input
              type="radio"
              name="choice"
              value="${i}"
              ${state.selected === i ? "checked" : ""}
            >
            <span>
              <strong>${"ABCD"[i]}. ${esc(o.title)}</strong>
              <small>${esc(o.detail)}</small>
            </span>
          </label>
        `).join("")}
      </fieldset>

      <div
        class="custom"
        id="custom-box"
        ${state.selected === 3 ? "" : "hidden"}
      >
        <label for="policy">Your proposed policy</label>
        <textarea id="policy" maxlength="6000">${esc(state.custom)}</textarea>

        <label for="strategy">Model consequences using</label>
        <select id="strategy">
          ${r.options.map((o, i) => `
            <option
              value="${i}"
              ${Number(state.strategy) === i ? "selected" : ""}
            >
              ${esc(o.title)}
            </option>
          `).join("")}
        </select>

        <p class="fine">
          Your policy text is recorded, but not evaluated.
          Consequences follow the response model you select.
        </p>
      </div>

      <label for="reasoning">
        Explain your legal and ethical reasoning
      </label>
      <textarea
        id="reasoning"
        maxlength="10000"
        placeholder="What authority applies? Who is affected? What tradeoffs are you accepting?"
      >${esc(state.reasoning)}</textarea>

      <p class="fine">
        Required: at least 20 characters. Submitted decisions
        cannot be edited within this run.
      </p>

      <p id="validation" class="error" role="alert"></p>

      <button class="primary" type="submit">
        Submit executive decision →
      </button>
    </form>
  `;
}

function consequenceHTML() {
  const e = state.history.at(-1);

  return `
    <span class="role">DECISION RECORDED / ${esc(e.role)}</span>

    <div class="callout">
      <strong>Your response</strong>
      ${esc(e.choice)}

      ${e.custom ? `
        <p class="fine">
          Modeled using: ${esc(e.strategy)}.
        </p>
      ` : ""}
    </div>

    <h3>Immediate consequences</h3>
    <p class="outcome">${esc(e.consequence)}</p>

    <div class="section">
      <h3>Stakeholder response</h3>
      <p>${esc(e.stakeholder)}</p>
    </div>

    <div class="section">
      <h3>Legal and ethical considerations</h3>
      <p>${esc(e.legal)}</p>

      ${e.warnings.map(w => `
        <div class="warning">${esc(w)}</div>
      `).join("")}
    </div>

    <div class="section">
      <h3>Executive reflection</h3>
      <p>${esc(e.prompt)}</p>

      <label for="round-reflection">
        Capture your reflection (optional)
      </label>
      <textarea
        id="round-reflection"
        maxlength="8000"
      >${esc(e.reflection)}</textarea>
    </div>

    <div class="actions">
      <button class="primary" data-action="next">
        ${state.round === 4
          ? "View final debrief"
          : "Continue to next briefing"} →
      </button>
    </div>
  `;
}

function workspace() {
  app.innerHTML = `
    <div class="topline">
      <div>
        <div class="eyebrow muted">
          Public health crisis / Executive response
        </div>
        <h1>Public health response</h1>
      </div>

      <div class="timer-tools">
        <div>
          <div class="fine" id="clock-label">
            ${state.paused
              ? "Timer paused"
              : "Suggested time remaining"}
          </div>
          <span class="clock" id="clock">${time()}</span>
        </div>
        <button class="secondary" data-action="pause">
          ${state.paused ? "Resume timer" : "Pause timer"}
        </button>
      </div>
    </div>

    <div class="workspace">
      <aside class="timeline">
        ${rounds.map((r, i) => `
          <div
            class="phase ${i === state.round ? "active" : ""}"
            ${i === state.round ? 'aria-current="step"' : ""}
          >
            <span>${i < state.round ? "✓" : i + 1}</span>
            ${esc(r.title)}
          </div>
        `).join("")}

        <p class="fine">
          ${state.history.length} of 5 decisions recorded<br>
          ${storageOK ? "Saved in this browser" : "This tab only"}
        </p>

        <button class="secondary" data-action="restart">
          Start over
        </button>
      </aside>

      <section class="decision">
        <div class="round-head">
          <div class="eyebrow" style="color:var(--teal)">
            Decision ${state.round + 1} of 5
            ${state.phase === "consequence"
              ? " / Consequence briefing"
              : ""}
          </div>
          <h2>${esc(rounds[state.round].title)}</h2>
        </div>

        <div class="body">
          ${state.phase === "decision"
            ? choiceHTML()
            : consequenceHTML()}
        </div>
      </section>

      <aside class="panel">
        <h3>Situation indicators</h3>
        <p class="fine">
          Fictional estimates / 0–100. These are not grades.
        </p>
        ${metrics()}
      </aside>
    </div>
  `;
}

function complete() {
  app.innerHTML = `
    <section class="summary-banner">
      <div class="eyebrow" style="color:var(--gold)">
        After-action review / Response complete
      </div>
      <h1>Five decisions. A record of your leadership.</h1>
      <p>
        All 5 decisions recorded · Ready for reflection and download
      </p>
    </section>

    <div class="final-grid">
      <section>
        <div class="panel">
          <h2>Final situation assessment</h2>
          <p>${esc(narrative(state.metrics))}</p>
          <div class="metric-grid">${metrics()}</div>
          <p class="fine">
            These fictional estimates do not determine a grade
            or a single best response.
          </p>
        </div>

        <h2>Your decision record</h2>

        ${state.history.map(e => `
          <details class="history">
            <summary>${e.round}. ${esc(e.title)}</summary>
            <div class="history-body">
              <strong>Decision point</strong>
              <p>${esc(e.question)}</p>

              <strong>Your response</strong>
              <p>${esc(e.choice)}</p>

              ${e.custom
                ? `<p>Modeled using: ${esc(e.strategy)}</p>`
                : ""}

              <strong>Your reasoning</strong>
              <p>${esc(e.reasoning)}</p>

              <strong>Immediate consequences</strong>
              <p>${esc(e.consequence)}</p>

              <strong>Stakeholder response</strong>
              <p>${esc(e.stakeholder)}</p>

              <strong>Legal and ethical considerations</strong>
              <p>${esc(e.legal)}</p>
              <p>${esc(e.warnings.join(" "))}</p>

              <strong>Reflection</strong>
              <p>${esc(e.prompt)}</p>
              <p>${esc(e.reflection || "No reflection provided.")}</p>
            </div>
          </details>
        `).join("")}
      </section>

      <aside class="panel export">
        <div class="eyebrow">Take your thinking with you</div>
        <h2>Download your record</h2>

        <p class="fine">
          Includes every scenario, decision point, available
          response, chosen policy, rationale, consequence,
          indicator change, and reflection.
        </p>

        <button class="primary" data-action="pdf">
          Download PDF ↓
        </button>

        <button class="secondary" data-action="text">
          Download text (.txt) ↓
        </button>

        <button class="secondary" data-action="print">
          Print / Save as PDF
        </button>

        <p class="fine">
          PDF uses standard Latin characters. The text download
          preserves all characters. Downloads do not submit work
          to Canvas.
        </p>

        <div class="section">
          <h3>Leadership debrief</h3>

          <ol class="debrief">
            ${debrief.map(q => `<li>${esc(q)}</li>`).join("")}
          </ol>

          <label for="final-reflection">
            Final reflection (optional)
          </label>

          <textarea
            id="final-reflection"
            maxlength="15000"
          >${esc(state.finalReflection)}</textarea>

          <p class="fine">
            The latest reflection is included each time you download.
          </p>
        </div>

        <button class="secondary" data-action="restart">
          Start a new simulation
        </button>
      </aside>
    </div>
  `;
}

function render() {
  if (!state) home();
  else if (state.phase === "complete") complete();
  else workspace();
}

function tick() {
  if (!state || state.phase === "complete") return;

  const now = Date.now();
  const elapsed = Math.floor((now - lastTick) / 1000);

  if (elapsed < 1) return;

  lastTick += elapsed * 1000;

  if (!state.paused && state.remaining > 0) {
    state.remaining = Math.max(0, state.remaining - elapsed);

    if ($("clock")) {
      $("clock").textContent = time();
    }

    if (state.remaining === 0) {
      message(
        "The suggested time has elapsed. You can continue and download your completed record."
      );
    }

    save();
  }
}

/* =========================================================
   PDF GENERATOR — NO EXTERNAL LIBRARIES REQUIRED
   ========================================================= */

function buildPDF(text) {
  const ascii = text
    .normalize("NFKD")
    .replace(/[\u0300-\u036f]/g, "")
    .replace(/[\u2018\u2019]/g, "'")
    .replace(/[\u201c\u201d]/g, '"')
    .replace(/[\u2010-\u2015\u2500]/g, "-")
    .replace(/\u2192/g, "->")
    .replace(/\r/g, "")
    .replace(/[^\x20-\x7E\n]/g, "?");

  const lines = [];

  for (let line of ascii.split("\n")) {
    while (line.length > 94) {
      let cut = line.lastIndexOf(" ", 94);

      if (cut < 1) cut = 94;

      lines.push(line.slice(0, cut));
      line = line.slice(cut).trimStart();
    }

    lines.push(line);
  }

  const chunks = [];

  for (let i = 0; i < lines.length; i += 54) {
    chunks.push(lines.slice(i, i + 54));
  }

  const escapePDF = value => value
    .replace(/\\/g, "\\\\")
    .replace(/\(/g, "\\(")
    .replace(/\)/g, "\\)");

  const objects = [
    null,
    "<< /Type /Catalog /Pages 2 0 R >>",
    "",
    "<< /Type /Font /Subtype /Type1 /BaseFont /Courier >>",
    "<< /Type /Font /Subtype /Type1 /BaseFont /Courier-Bold >>"
  ];

  const ids = [];

  chunks.forEach((chunk, i) => {
    const id = objects.length;
    ids.push(id);

    objects.push(
      `<< /Type /Page /Parent 2 0 R /MediaBox [0 0 612 792] ` +
      `/Resources << /Font << /F1 3 0 R /F2 4 0 R >> >> ` +
      `/Contents ${id + 1} 0 R >>`
    );

    const stream =
      "BT /F2 11 Tf 50 762 Td " +
      "(REDWOOD VALLEY / AFTER-ACTION RECORD) Tj ET\n" +
      "BT /F1 9 Tf 12 TL 50 730 Td\n" +
      chunk.map(line => "(" + escapePDF(line) + ") Tj T*").join("\n") +
      "\nET\n" +
      `BT /F1 8 Tf 50 30 Td ` +
      `(EXERCISE ONLY - Page ${i + 1} of ${chunks.length}) Tj ET\n`;

    objects.push(
      `<< /Length ${stream.length} >>\nstream\n${stream}endstream`
    );
  });

  objects[2] =
    `<< /Type /Pages /Count ${ids.length} ` +
    `/Kids [${ids.map(id => id + " 0 R").join(" ")}] >>`;

  let pdf = "%PDF-1.4\n";
  const offsets = [0];

  for (let i = 1; i < objects.length; i++) {
    offsets[i] = pdf.length;
    pdf += `${i} 0 obj\n${objects[i]}\nendobj\n`;
  }

  const start = pdf.length;

  pdf +=
    `xref\n0 ${objects.length}\n` +
    "0000000000 65535 f \n";

  for (let i = 1; i < objects.length; i++) {
    pdf +=
      String(offsets[i]).padStart(10, "0") +
      " 00000 n \n";
  }

  pdf +=
    `trailer\n<< /Size ${objects.length} /Root 1 0 R >>\n` +
    `startxref\n${start}\n%%EOF`;

  return new TextEncoder().encode(pdf);
}

function downloadRecord(bytes, mime, extension) {
  const url = URL.createObjectURL(
    new Blob([bytes], { type: mime })
  );

  const link = document.createElement("a");
  link.href = url;
  link.download = "redwood-valley-decision-record." + extension;

  document.body.append(link);
  link.click();
  link.remove();

  setTimeout(() => URL.revokeObjectURL(url), 15000);

  message(
    "Your " + extension.toUpperCase() + " download has started."
  );
}

/* =========================================================
   EVENT HANDLERS
   ========================================================= */

document.addEventListener("input", event => {
  if (!state) return;

  const id = event.target.id;

  if (id === "reasoning") {
    state.reasoning = event.target.value;
  } else if (id === "policy") {
    state.custom = event.target.value;
  } else if (id === "round-reflection") {
    state.history.at(-1).reflection = event.target.value;
  } else if (id === "final-reflection") {
    state.finalReflection = event.target.value;
  } else {
    return;
  }

  save();
});

document.addEventListener("change", event => {
  if (!state) return;

  if (event.target.name === "choice") {
    state.selected = Number(event.target.value);
    $("custom-box").hidden = state.selected !== 3;
    save();
  }

  if (event.target.id === "strategy") {
    state.strategy = Number(event.target.value);
    save();
  }
});

document.addEventListener("submit", event => {
  if (event.target.id === "start") {
    event.preventDefault();

    if (
      saved &&
      !confirm(
        "Starting a new simulation replaces saved progress in this browser. Continue?"
      )
    ) {
      return;
    }

    const form = new FormData(event.target);
    const participant = String(
      form.get("participant") || ""
    ).trim();

    state = initial(participant);
    lastTick = Date.now();

    save();
    message("");
    render();
    goTop();
  } else if (event.target.id === "decision") {
    event.preventDefault();

    try {
      tick();
      state = decide(state);
      save();
      message("");
      render();
      goTop();
    } catch (error) {
      $("validation").textContent = error.message;
    }
  }
});

document.addEventListener("click", event => {
  const button = event.target.closest("[data-action]");
  if (!button) return;

  const action = button.dataset.action;

  if (action === "resume") {
    state = JSON.parse(JSON.stringify(saved));

    if (state.phase !== "complete" && !state.paused) {
      const elapsed = Math.floor(
        (Date.now() - state.checkpoint) / 1000
      );

      state.remaining = Math.max(0, state.remaining - elapsed);
    }

    lastTick = Date.now();
    save();
    render();
    goTop();

  } else if (action === "pause") {
    tick();
    state.paused = !state.paused;
    lastTick = Date.now();
    save();

    button.textContent = state.paused
      ? "Resume timer"
      : "Pause timer";

    $("clock-label").textContent = state.paused
      ? "Timer paused"
      : "Suggested time remaining";

  } else if (action === "next") {
    tick();
    state = advance(state);
    save();
    render();
    goTop();

  } else if (action === "restart") {
    const confirmed = confirm(
      "Clear this simulation and start over? Download your completed record first if you want to keep it."
    );

    if (!confirmed) return;

    try {
      localStorage.removeItem(KEY);
    } catch {}

    state = null;
    saved = null;
    message("");
    home();
    goTop();

  } else if (
    action === "pdf" &&
    state.phase === "complete"
  ) {
    save();

    downloadRecord(
      buildPDF(reportText(state)),
      "application/pdf",
      "pdf"
    );

  } else if (
    action === "text" &&
    state.phase === "complete"
  ) {
    save();

    downloadRecord(
      "\uFEFF" + reportText(state),
      "text/plain;charset=utf-8",
      "txt"
    );

  } else if (
    action === "print" &&
    state.phase === "complete"
  ) {
    save();
    $("print-report").textContent = reportText(state);
    window.print();
  }
});

window.addEventListener("pagehide", () => {
  tick();
  save();
});

render();
setInterval(tick, 1000);
</script>

</body>
</html>
