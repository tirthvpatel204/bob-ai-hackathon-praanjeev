# PRAANJEEV — Presentation

Place the PRAANJEEV presentation slide deck in this folder.

## Accepted Formats

```text
slides.pdf      ← Preferred (universally viewable)
slides.pptx     ← Acceptable
slides.key      ← Acceptable (macOS Keynote)
```

Rename the final presentation to:

```text
slides.pdf
```

or

```text
slides.pptx
```

so the hackathon evaluation pipeline can locate it reliably.

---

# Recommended Slide Structure

## Slide 1 — Title

### PRAANJEEV

**AI Emergency Response & Hospital Coordination System**

> **“In the race against time, we choose life.”**

Include:

* Team Name: **Praanjeev**
* Track: **AI**
* IBM BoB AI Innovation Hackathon 2026
* CHARUSAT
* Team members

Visual direction:

Use a cinematic emergency-response visual showing an ambulance, patient/family and hospital/medical team.

---

## Slide 2 — The Problem

### The Emergency Is Not Just About Finding a Hospital

During a medical emergency:

* Families may not know which hospital is actually suitable.
* The nearest hospital may not have the required ICU, oxygen, specialist or emergency resources.
* Ambulances can lose valuable time because of traffic.
* Hospitals may receive little or no information before the patient arrives.
* Hospital resource information can become outdated or unreliable.

### Core Problem Statement

> **How can AI intelligently coordinate patients, ambulances, hospitals and critical medical resources during emergencies to reduce response and treatment delays?**

---

## Slide 3 — Our Solution

### PRAANJEEV

PRAANJEEV connects:

**Patient → AI → Verified Hospitals → Resources → Ambulance → Hospital**

The system:

1. Understands the emergency information.
2. Identifies required medical capabilities.
3. Finds nearby verified hospitals.
4. Checks hospital resources and capabilities.
5. Ranks hospitals using multiple factors.
6. Helps select the most suitable hospital.
7. Shares minimum necessary emergency information with consent.
8. Sends a hospital pre-alert.
9. Provides emergency routing and ETA.
10. Helps the hospital prepare before patient arrival.

### USP

> **“PRAANJEEV doesn't just find the nearest hospital. It helps find the RIGHT VERIFIED hospital, securely shares the RIGHT emergency information, and gives the hospital time to prepare BEFORE the patient arrives.”**

---

## Slide 4 — How It Works / Architecture

### End-to-End Emergency Coordination

```text
Patient / Paramedic
        ↓
Emergency Information
        ↓
AI Emergency Assessment
        ↓
Required Medical Capabilities
        ↓
Location + Verified Hospital Network
        ↓
Hospital Resource Intelligence
        ↓
AI Hospital Matching & Ranking
        ↓
Best-Matched Hospital
        ↓
Consent + Emergency Case ID
        ↓
Hospital Pre-Alert
        ↓
Hospital Preparation
        ↓
Smart Emergency Routing
        ↓
Ambulance Navigation
        ↓
Patient Arrival & Treatment
```

Also show:

* Hospital Verification
* Resource Updates
* Data Validation
* Anomaly Detection
* Admin Monitoring

Keep the architecture visual rather than using large paragraphs.

---

## Slide 5 — Key Feature / Demo

### AI Hospital Matching

PRAANJEEV does **not** simply choose the closest hospital.

Example demo scenario:

```text
Patient Age: 45
Location: Anand
Condition: Severe Chest Pain
Heart Rate: 118 BPM
SpO₂: 89%
Blood Pressure: 90/60
```

The AI identifies the case as **CRITICAL decision-support output** and considers:

* Required medical capabilities
* ICU availability
* Oxygen availability
* Emergency facilities
* Specialist capability
* Hospital verification
* Distance
* Traffic
* Estimated arrival time

### Result

A hospital that is slightly farther away can be recommended if it is significantly more suitable for the emergency.

Show an actual PRAANJEEV screenshot here.

---

## Slide 6 — IBM Technologies & AI Integration

### IBM + PRAANJEEV

Explain specifically where IBM technology is used in the implemented system.

Potential areas:

* **IBM BoB** — AI-powered application development/integration
* **watsonx.ai / IBM AI services** — emergency understanding and intelligent decision support, if implemented
* AI-based emergency assessment
* AI hospital matching and ranking
* Explainable AI recommendations

### Important

Only mention IBM technologies that are **actually implemented and demonstrated in the repository**.

Do not present IBM logos or technology names without showing how they contribute to PRAANJEEV.

---

## Slide 7 — Impact & Future Scope

### What Success Looks Like

PRAANJEEV aims to improve emergency coordination by reducing:

* Hospital selection delay
* Ambulance routing delay
* Communication delay
* Hospital preparation delay
* Uncertainty about hospital capabilities

### Impact

**Patient**

→ Faster and more suitable hospital selection

**Ambulance**

→ Practical emergency route and ETA

**Hospital**

→ Early emergency information and preparation time

**Healthcare Network**

→ Better coordination of critical resources

### Future Scope

* Real-time hospital resource synchronization
* Advanced traffic-aware dynamic routing
* Ambulance service integration
* Multi-city and state-wide hospital networks
* Historical emergency-response analytics
* More advanced anomaly detection
* Real-time monitoring and audit systems

Do not claim numerical improvements unless they are measured using real evaluation data.

---

## Slide 8 — Team

# Team Praanjeev

### Tirth Patel

**Team Lead**

* AI architecture
* Project integration
* AI hospital matching
* Documentation

### Neev Patel

* Application development
* Emergency workflow
* UI / frontend

### Tanmay Patel

* Backend / data handling
* Hospital resources
* Emergency coordination

### Kashyap Modi

* AI / testing
* Demo preparation
* Documentation / presentation

---

# Presentation Design Guidelines

## Visual Style

Use a premium, cinematic healthcare-tech theme:

* Dark navy / black background
* Cyan / blue / purple accents
* Clean white typography
* Emergency-response visuals
* Hospital, ambulance, patient and medical-team imagery
* Subtle glowing UI elements
* Clean diagrams
* Minimal text

## Storytelling

The presentation should follow:

```text
HUMAN LIFE
     ↓
EMERGENCY
     ↓
UNCERTAINTY
     ↓
AI
     ↓
COORDINATION
     ↓
RIGHT HOSPITAL
     ↓
HOSPITAL PREPARATION
     ↓
HOPE
```

## Slide Rules

* Keep slides visual.
* Prefer diagrams over paragraphs.
* Use **24pt or larger** text wherever possible.
* One major idea per slide.
* Use screenshots from the actual PRAANJEEV application.
* Do not paste large code blocks.
* Reference the GitHub repository for implementation details.
* Clearly label simulated/demo hospital and resource data.
* Do not use fake statistics.
* Do not claim AI diagnosis.
* Present AI as **decision support**, not a replacement for medical professionals.

---

# Recommended Demo Story

Use one consistent emergency scenario throughout the presentation:

**45-year-old patient in Anand**

```text
Severe Chest Pain
HR: 118
SpO₂: 89%
BP: 90/60
```

Then demonstrate:

```text
Emergency Input
      ↓
AI Assessment
      ↓
CRITICAL
      ↓
Required Capabilities
      ↓
Verified Hospital Matching
      ↓
Resource Check
      ↓
Hospital Selection
      ↓
Patient Consent
      ↓
Emergency Case ID
      ↓
Hospital Pre-Alert
      ↓
Smart Route
      ↓
Hospital Preparation
```

This gives the judges a single clear story from **problem → AI → decision → coordination → impact**.

---

# Presentation File

The final folder should contain:

```text
presentation/
│
├── README.md
│
└── slides.pdf
```

or:

```text
presentation/
│
├── README.md
│
└── slides.pptx
```

The preferred submission format is:

**`slides.pdf`**
****
