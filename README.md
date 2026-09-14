# 🚑 PRAANJEEV — AI Emergency Response & Hospital Coordination

> **Every Second. Every Life.** ❤️

---

## 👥 Team

| Field         | Value                                                                       |
| ------------- | --------------------------------------------------------------------------- |
| **Team Name** | Praanjeev                                                                   |
| **Track**     | AI                                                                          |
| **Team Lead** | Tirth Patel — [25aiml058@charusat.edu.in](mailto:25aiml058@charusat.edu.in) |
| **Members**   | Neev Patel, Tanmay Patel, Kashyap Modi                                      |

---

## 🎯 Problem Statement

PRAANJEEV solves the problem of finding the right hospital during a medical emergency by considering the patient’s condition, nearby verified hospital resources, treatment capabilities, traffic, and route time instead of simply choosing the nearest hospital. This problem is experienced by emergency patients and their families, ambulance teams, and hospitals that need timely information to coordinate care and prepare before the patient arrives.

---

## 💡 Solution

We built **PRAANJEEV**, an AI-powered emergency response and hospital coordination platform that connects patients, ambulances, and verified hospitals in real time. It uses AI to understand the patient’s emergency condition, identify the most suitable nearby verified hospital based on medical capabilities and available resources such as ICU beds, oxygen, medicines and emergency facilities, calculate a traffic-aware route, and securely send the patient’s emergency information to the selected hospital so the medical team can prepare before arrival.

This transforms emergency response from simply finding the nearest hospital into **condition-aware, resource-aware and coordinated emergency care**.

---

## ✨ Key Features

* **AI Emergency Assessment** — Analyzes emergency details and patient vitals to assess urgency and identify potentially required medical resources.

* **AI-Powered Hospital Matching** — Recommends the most suitable nearby verified hospital based on patient condition, treatment capabilities, available resources, distance and ETA.

* **Verified Hospital Network** — Hospitals undergo registration and verification of hospital information, licenses/registration details and authorized representatives before receiving a verified status.

* **Hospital Resource Intelligence** — Displays availability of critical resources such as ICU beds, emergency beds, oxygen, medicines, blood and specialist facilities, along with data-freshness indicators.

* **Smart Traffic-Aware Routing** — Calculates a practical emergency route using traffic conditions, ETA and alternate routes, with dynamic rerouting when conditions change.

* **Hospital Pre-Alert & Emergency Case Sharing** — With patient consent, securely shares an Emergency Case ID and essential emergency information with the selected hospital so the medical team can prepare before arrival.

* **Location-Aware Recommendations** — Uses the patient's current location as the default search area. For example, a patient in Anand, Gujarat is recommended suitable verified hospitals around Anand rather than unrelated hospitals in another country.

---

## 🛠️ Tech Stack

| Category              | Technologies                                                                               |
| --------------------- | ------------------------------------------------------------------------------------------ |
| **Languages**         | Python, JavaScript, HTML5, CSS3                                                            |
| **Frameworks**        | Flask, REST API                                                                            |
| **IBM Technologies**  | IBM Bob, watsonx.ai, IBM Cloud                                                             |
| **Databases**         | MySQL, JSON                                                                                |
| **AI / Intelligence** | AI emergency assessment, hospital matching, resource analysis, explainable recommendations |
| **Maps & Routing**    | Traffic-aware Maps/Routing API                                                             |
| **Other**             | GitHub, GitHub Actions, REST APIs, Responsive Web Design                                   |

---

## 🧠 AI Workflow

```text
Patient Emergency Input
        ↓
AI Emergency Assessment
        ↓
Identify Required Medical Resources
        ↓
Find Nearby Verified Hospitals
        ↓
Check Hospital Capability + Resource Availability
        ↓
Analyze Distance + Traffic + ETA
        ↓
AI Hospital Ranking
        ↓
Patient Selects Hospital + Gives Consent
        ↓
Emergency Case Shared Securely
        ↓
Hospital Prepares for Arrival
        ↓
Smart Ambulance Route + Live Updates
```

---

## 🏥 Hospital Verification

PRAANJEEV is designed around a **Verified Hospital Network** to improve trust in emergency recommendations.

Hospital onboarding includes:

1. Hospital registration
2. Hospital information verification
3. Registration/license information
4. Owner/authorized representative information
5. Facility and emergency-service information
6. Document verification
7. Admin verification
8. Continuous monitoring and re-verification

### Verification Status

* 🟡 **Pending**
* 🟢 **Verified**
* 🔴 **Suspended / Re-verification Required**

Hospital resource updates are associated with timestamps and audit information to improve data reliability.

---

## 📍 Location-Aware Hospital Matching

PRAANJEEV prioritizes hospitals according to the patient's actual emergency location.

For example:

```text
Patient Location
Anand, Gujarat, India
        ↓
Nearby Verified Hospitals
        ↓
Condition-Based Filtering
        ↓
ICU / Oxygen / Medicine / Specialist Availability
        ↓
Traffic + Distance + ETA
        ↓
AI Ranking
        ↓
Best Suitable Hospital
```

The system does **not** automatically show unrelated hospitals from distant countries such as the USA when the patient is receiving care in Anand.

A user can optionally choose another location when required.

---

## 🚑 Smart Emergency Routing

After hospital selection, PRAANJEEV calculates the most practical ambulance route.

The routing system considers:

* Current traffic
* Distance
* Estimated arrival time
* Alternate routes
* Ambulance accessibility
* Route changes
* Dynamic rerouting

The system does not blindly select the shortest road; it aims to select the **fastest practical emergency route**.

---

## 🔐 Patient Privacy & Consent

PRAANJEEV follows a consent-based emergency information-sharing approach.

Before sharing emergency information with the selected hospital:

```text
Patient
   ↓
Hospital Recommendation
   ↓
Hospital Selection
   ↓
Consent
   ↓
Emergency Case ID
   ↓
Essential Emergency Information
   ↓
Receiving Hospital
```

Only the information required for emergency coordination should be shared.

---

## 🏥 Hospital Pre-Alert

Once a patient selects a hospital and provides consent, the hospital receives an incoming emergency case containing relevant information such as:

* Emergency Case ID
* Patient emergency summary
* Vital information provided by the patient/paramedic
* Estimated arrival time
* Required emergency resources
* Selected ambulance route/status

The hospital can then prepare appropriate resources before the patient arrives.

---

## 📊 Emergency Coordination Dashboard

### Patient

* Emergency registration
* Current location
* AI assessment
* Recommended hospitals
* Hospital resource availability
* Hospital selection
* Consent
* Ambulance ETA
* Emergency status tracking

### Hospital

* Hospital verification status
* Resource/stock dashboard
* Incoming emergency cases
* Patient emergency information
* Preparation status
* Resource availability updates
* Emergency case history

### Admin

* Hospital verification
* Document/status review
* Resource anomaly monitoring
* Hospital suspension/re-verification
* Audit logs
* Platform monitoring

---

## 🤖 IBM AI Integration

IBM AI capabilities are used as part of the decision-support workflow rather than as a simple chatbot.

```text
INPUT
Patient Emergency Information
        ↓
AI UNDERSTANDING
Emergency Summary + Required Resources
        ↓
AI DECISION SUPPORT
Hospital Suitability Analysis
        ↓
AI EXPLANATION
Why a Hospital Was Recommended
        ↓
ACTION
Hospital Pre-Alert + Emergency Coordination
```

The AI provides **decision support** and does not replace qualified medical professionals or emergency services.

---

## 📁 Repository Structure

```text
├── src/
│   ├── frontend/
│   ├── backend/
│   └── ai/
│
├── data/
│   └── demo-hospitals.json
│
├── docs/
│   ├── problem-statement.md
│   ├── solution-overview.md
│   ├── architecture.md
│   └── setup-guide.md
│
├── demo/
│   ├── screenshots/
│   ├── demo-video-link.txt
│   └── live-demo-url.txt
│
├── presentation/
│   └── PRAANJEEV.pptx
│
├── README.md
└── submission.yaml
```

---

## ⚡ How to Run

```bash
# Clone the repository
git clone https://github.com/[your-repository-url].git

# Enter the project
cd [repository-name]

# Install dependencies
pip install -r requirements.txt

# Configure environment variables
cp .env.example .env

# Start the application
python app.py
```

> Replace the commands above with the exact commands used by the final implementation.

---

## 🖥️ Demo

| Artifact        | Location                      |
| --------------- | ----------------------------- |
| 📹 Demo Video   | `demo/demo-video-link.txt`    |
| 🌐 Live Demo    | `demo/live-demo-url.txt`      |
| 🖼️ Screenshots | `demo/screenshots/`           |
| 📊 Presentation | `presentation/PRAANJEEV.pptx` |

---

## 🎬 Recommended Demo Scenario

**Emergency Patient:** 45-year-old patient in Anand, Gujarat

```text
Severe chest pain
Heart Rate: 118 BPM
SpO₂: 89%
BP: 90/60
Location: Anand, Gujarat
        ↓
AI Emergency Assessment
        ↓
CRITICAL — Immediate Emergency Care
        ↓
Required:
ICU + Oxygen + Cardiac Emergency Capability
        ↓
Nearby Verified Hospitals
        ↓
Resource + Capability + Traffic Analysis
        ↓
AI Hospital Ranking
        ↓
Patient Selects Hospital
        ↓
Consent Given
        ↓
Hospital Receives Emergency Case
        ↓
Hospital Begins Preparation
        ↓
Ambulance Gets Optimized Route
```

This demonstrates the complete **Input → AI → Decision → Coordination → Action** workflow.

---

## ⚠️ Known Limitations

* Hospital resource availability depends on the accuracy and freshness of data supplied by participating hospitals.
* Demo hospital and resource data may be simulated and should be clearly identified as demo data.
* Traffic and routing functionality depends on the selected mapping/routing service and its available data.
* Hospital document verification may require integration with appropriate official verification systems for production deployment.
* AI recommendations are decision-support outputs and are not a medical diagnosis or replacement for qualified healthcare professionals.
* The prototype is intended for hackathon demonstration and would require additional security, regulatory, clinical and infrastructure validation before real-world deployment.

---

## 🏅 What We're Most Proud Of

We are most proud of building PRAANJEEV as more than a simple hospital-finder. Our system connects **AI emergency assessment, verified hospitals, real-time medical resources, patient consent, hospital pre-alerts and traffic-aware ambulance routing** into one coordinated emergency workflow.

Our core idea is simple:

> **“The nearest hospital is not always the right hospital.”**

PRAANJEEV aims to help identify the **right verified hospital, with the right resources, through the right route — before precious time is lost.**

### ❤️ PRAANJEEV

> **Every Second. Every Life.**
