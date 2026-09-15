# PRAANJEEV — Setup Guide

## 1. Overview

This document explains how to set up and run the PRAANJEEV AI Emergency Response & Hospital Coordination System locally.

PRAANJEEV is designed to coordinate emergency patients, ambulances, verified hospitals, hospital resources and emergency information using AI-powered decision support.

> **Important:** PRAANJEEV is a hackathon prototype. AI recommendations are intended as decision support and must not be treated as medical diagnosis or a guarantee of hospital resource availability.

---

## 2. Prerequisites

Before running PRAANJEEV, make sure the following are installed:

* Git
* A modern web browser such as Google Chrome, Microsoft Edge or Firefox
* Node.js and npm if the project uses a Node.js-based frontend
* Python 3.x if the project uses the Python backend
* A code editor such as Visual Studio Code
* Internet connection for external APIs and AI services used by the project

Check the installed versions:

```bash
git --version
node --version
npm --version
python --version
```

If a particular technology is not used in the current implementation, that prerequisite can be ignored.

---

## 3. Clone the Repository

Clone the PRAANJEEV repository:

```bash
git clone https://github.com/tirthvpatel204/bob-ai-hackathon-praanjeev.git
```

Move into the project directory:

```bash
cd bob-ai-hackathon-praanjeev
```

---

## 4. Project Structure

The hackathon repository follows the required structure:

```text
bob-ai-hackathon-praanjeev/
│
├── submission.yaml
├── README.md
│
├── src/
│   ├── .env.example
│   ├── README.md
│   └── application source code
│
├── docs/
│   ├── problem-statement.md
│   ├── solution-overview.md
│   ├── architecture.md
│   └── setup-guide.md
│
├── demo/
│   ├── demo-video-link.txt
│   ├── live-demo-url.txt
│   └── screenshots/
│
├── presentation/
│   └── slides.pdf
│
├── CONTRIBUTING.md
├── .gitignore
│
└── .github/
    └── workflows/
        └── validate.yml
```

All application source code should remain inside the `src/` directory.

---

## 5. Environment Variables

PRAANJEEV may require environment variables for external services such as AI services, maps/routing services or backend configuration.

The project provides:

```text
src/.env.example
```

Create the local environment file required by the implementation.

For example:

```bash
cp src/.env.example src/.env
```

Then open the `.env` file and provide the required values.

Example structure:

```env
AI_API_KEY=your_ai_api_key
MAPS_API_KEY=your_maps_api_key
```

> Use the exact variable names present in the project's `src/.env.example`.

### Security

Never commit the real `.env` file to GitHub.

Do not place API keys directly inside source code.

The repository should contain only `.env.example` with placeholder values.

---

## 6. Install Dependencies

### Frontend

If the frontend contains a `package.json`, enter the appropriate frontend directory and run:

```bash
npm install
```

### Backend

If the backend contains a Python dependency file such as `requirements.txt`, create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

Activate it on macOS/Linux:

```bash
source .venv/bin/activate
```

Then install the dependencies:

```bash
pip install -r requirements.txt
```

> If the current implementation does not use Python, skip this section.

---

## 7. Run the Application

Run the frontend and backend using the commands provided by the actual project implementation.

### Frontend

For a standard Node.js frontend:

```bash
npm run dev
```

or:

```bash
npm start
```

### Backend

For a Python/Flask backend, the application may be started using:

```bash
python app.py
```

or the project's configured backend command.

> Use the command that matches the actual files and scripts in `src/`.

---

## 8. Open PRAANJEEV

After starting the application, open the local URL shown in the terminal.

A typical development frontend may run at:

```text
http://localhost:3000
```

A backend may run at:

```text
http://localhost:5000
```

The exact port depends on the project configuration.

---

## 9. Verify That the Application Works

Use the following test flow to verify PRAANJEEV.

### Step 1 — Open the application

Confirm that the PRAANJEEV interface loads successfully.

### Step 2 — Enter emergency information

Enter a simulated emergency case.

Example:

```text
Patient Age: 45
Location: Anand
Heart Rate: 118
SpO2: 89%
Blood Pressure: 90/60
Symptoms: Severe chest pain
```

> This is a simulated demonstration scenario and must not be interpreted as real medical advice.

### Step 3 — Emergency Assessment

Verify that the AI emergency assessment processes the provided information and identifies the urgency level.

The system should present the result as decision support rather than claiming a medical diagnosis.

### Step 4 — Hospital Matching

Verify that PRAANJEEV considers:

* Patient condition
* Required medical capabilities
* Hospital verification
* Hospital resources
* Distance
* Estimated travel time
* Traffic/routing information when available

The recommended hospital should not be selected using distance alone.

### Step 5 — Hospital Selection

Select a recommended hospital.

The system should generate an Emergency Case ID and request/record the required consent before sharing emergency information.

### Step 6 — Hospital Pre-Alert

Verify that the selected hospital receives the minimum necessary emergency information.

The hospital should be able to see the incoming emergency case and prepare the required resources.

### Step 7 — Emergency Routing

Verify that PRAANJEEV provides the ambulance with an appropriate emergency route and ETA.

### Step 8 — Emergency Status

Verify the emergency coordination status and hospital preparation information.

Possible resource statuses include:

```text
Requested
Accepted
Preparing
Ready
Patient Arrived
```

---

## 10. Expected End-to-End Flow

The complete demonstration flow is:

```text
Patient / Paramedic
        ↓
Emergency Information
        ↓
AI Emergency Assessment
        ↓
Location Analysis
        ↓
Verified Hospital Search
        ↓
Hospital Resource Analysis
        ↓
AI Hospital Matching & Ranking
        ↓
Hospital Recommendation
        ↓
Patient / Paramedic Selection
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
Patient Arrival
```

---

## 11. Location Verification

PRAANJEEV uses location information to make hospital recommendations relevant to the patient's actual location.

For example, if a demonstration patient is located in Anand, the system should prioritize suitable hospitals in Anand or nearby areas rather than unrelated locations.

The application should also provide an option to change or search another location when appropriate.

---

## 12. Hospital Resource Data

PRAANJEEV can use hospital resource information such as:

* ICU beds
* Emergency beds
* Oxygen availability
* Medicines
* Blood availability
* Medical equipment
* Specialists
* Emergency-care capabilities

Resource information should include freshness or update information when available.

If data is outdated, the application should avoid presenting it as guaranteed real-time availability.

---

## 13. Demo / Simulated Data

If hospital information, resources, traffic or emergency cases are simulated for the hackathon demonstration, clearly identify them as:

```text
Demo Data
```

or:

```text
Simulated Data
```

Do not present simulated information as real hospital availability.

---

## 14. AI Safety and Responsible Use

PRAANJEEV provides AI-powered decision support.

The system must not claim:

* 100% accurate medical decisions
* Guaranteed hospital bed availability
* Guaranteed oxygen availability
* Guaranteed ambulance arrival time
* Medical diagnosis
* Guaranteed treatment outcome

The AI recommendation should help users make an informed coordination decision while keeping humans in control.

---

## 15. Troubleshooting

| Problem                             | Possible Cause                              | Solution                                                             |
| ----------------------------------- | ------------------------------------------- | -------------------------------------------------------------------- |
| Application does not start          | Dependencies are missing                    | Run the project's dependency installation command                    |
| `npm` command not found             | Node.js is not installed                    | Install Node.js and restart the terminal                             |
| `python` command not found          | Python is not installed                     | Install Python 3.x                                                   |
| API request fails                   | Environment variable/API key is missing     | Check `src/.env` against `.env.example`                              |
| AI response fails                   | AI service configuration problem            | Verify the configured AI API credentials and service settings        |
| Map/routing does not load           | Maps/routing API configuration problem      | Check the configured maps/routing service credentials                |
| Hospital data is empty              | Database/demo data is unavailable           | Verify the configured data source                                    |
| Port already in use                 | Another application is using the port       | Stop the conflicting process or use the configured alternative port  |
| GitHub Action fails                 | Required submission file/content is missing | Open the GitHub Actions run and follow the reported validation error |
| Page loads but features do not work | Backend/API is not running                  | Start the required backend service                                   |

---

## 16. GitHub Submission Verification

Before submitting the hackathon entry, verify:

```text
[ ] Repository is Public
[ ] Official hackathon template is used
[ ] submission.yaml is complete
[ ] README.md is complete
[ ] docs/problem-statement.md exists
[ ] docs/solution-overview.md exists
[ ] docs/architecture.md exists
[ ] docs/setup-guide.md exists
[ ] src/ contains the actual source code
[ ] src/.env.example is updated
[ ] No real .env/API keys are committed
[ ] Demo video link is added
[ ] At least 3 screenshots are added
[ ] Presentation is added
[ ] Validate Submission GitHub Action is GREEN
```

The official template requires the repository to be public and the validation action to pass before submission.

---

## 17. Final Test

Before submission, perform the setup from a fresh terminal or clean environment.

Confirm that:

1. The repository can be cloned.
2. Dependencies can be installed.
3. Environment variables can be configured using `.env.example`.
4. The application starts successfully.
5. The emergency workflow can be completed.
6. AI functionality produces the expected output.
7. Hospital matching works.
8. Emergency Case ID is generated.
9. Hospital pre-alert works.
10. Routing functionality works when configured.
11. The application does not expose secret credentials.

---

## 18. Important Note

PRAANJEEV is a hackathon prototype demonstrating an AI-powered emergency coordination concept.

Real-world deployment would require additional validation, medical governance, verified hospital integrations, privacy/security controls, reliable real-time resource feeds, regulatory compliance, and production-grade infrastructure.
