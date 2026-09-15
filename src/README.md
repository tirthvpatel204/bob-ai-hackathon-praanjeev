# PRAANJEEV — Source Code

This folder contains the source code of **PRAANJEEV — AI Emergency Response & Hospital Coordination System**.

PRAANJEEV is designed to coordinate patients, ambulances, verified hospitals and critical medical resources during emergencies using AI-powered decision support.

## Project Structure

```text
src/
│
├── frontend/
│   ├── index.html
│   ├── css/
│   ├── js/
│   ├── assets/
│   └── components/
│
├── backend/
│   ├── api/
│   ├── services/
│   ├── models/
│   ├── routes/
│   └── app.*
│
├── ai/
│   ├── emergency_assessment/
│   ├── hospital_matching/
│   ├── resource_intelligence/
│   └── anomaly_detection/
│
├── database/
│   ├── schema/
│   ├── seed/
│   └── queries/
│
└── README.md
```

> The exact folders and filenames should match the implementation present in this repository.

---

# Main Application Components

## Frontend

The frontend provides the user interface for:

* Emergency information entry
* Patient / paramedic workflow
* Location selection
* Hospital recommendations
* Hospital resource information
* Emergency case status
* Ambulance route and ETA
* Hospital pre-alert information
* Hospital dashboard
* Admin dashboard

---

## Backend

The backend manages the core application logic, including:

* Emergency request processing
* Patient and hospital information
* Hospital matching
* Resource management
* Emergency Case ID generation
* Consent handling
* Hospital pre-alert
* API communication
* Data validation

---

## AI Modules

The AI layer supports decision-making during emergencies.

### AI Emergency Assessment

Analyzes the provided emergency information and identifies the urgency and required medical capabilities.

**Important:** PRAANJEEV provides **decision support** and does not claim to diagnose medical conditions.

### AI Hospital Matching

Ranks hospitals using factors such as:

* Patient emergency requirements
* Required medical capabilities
* Hospital resources
* Hospital verification status
* Distance
* Traffic
* Estimated travel time

### Resource Intelligence

Considers hospital resources such as:

* ICU beds
* Emergency beds
* Oxygen
* Medicines
* Blood availability
* Specialists
* Emergency equipment

### Data Validation & Anomaly Detection

Helps identify:

* Inconsistent information
* Duplicate records
* Impossible values
* Suspicious resource information
* Potentially unreliable hospital data

---

# Database

The database stores application information such as:

```text
Hospitals
Hospital Verification
Hospital Resources
Emergency Cases
Patient Emergency Information
Routes / ETA Information
Consent Records
Application Status
```

Sensitive information must not be committed directly to the repository.

---

# Environment Variables

Create a local `.env` file using `.env.example` as the template.

Example:

```text
API_KEY=your_api_key
DATABASE_URL=your_database_url
MAPS_API_KEY=your_maps_api_key
AI_API_KEY=your_ai_api_key
```

**Never commit the actual `.env` file or real API keys to GitHub.**

Only variable names and safe example values should be present in `.env.example`.

---

# Dependencies

The appropriate dependency file should be included depending on the implemented technology.

For Python:

```text
requirements.txt
```

For JavaScript / Node.js:

```text
package.json
```

All required dependencies should be documented so another developer can install and run the project.

---

# Running the Application

Refer to:

```text
docs/setup-guide.md
```

for the complete installation and execution instructions.

The source code should be run using the same commands and environment configuration described in the setup guide.

---

# Demo Data

If simulated hospitals, resources or emergency cases are used for the hackathon demonstration, they must be clearly identified as:

> **Demo / Simulated Data**

Demo data should not be presented as real-time verified medical resource availability.

---

# Security Rules

The following information must never be committed to this repository:

* API keys
* Passwords
* Database credentials
* Access tokens
* Private certificates
* Real patient personal information
* Other sensitive credentials

Use environment variables and `.env.example` instead.

---

# Development Principles

PRAANJEEV follows these principles:

```text
INPUT
  ↓
UNDERSTAND
  ↓
MATCH
  ↓
DECIDE
  ↓
COORDINATE
  ↓
ROUTE
  ↓
PREPARE
  ↓
RESPOND
```

The system is designed to support emergency coordination while keeping human medical professionals responsible for clinical decisions.

---

# Source Code Checklist

Before submission, verify:

* [ ] All application source code is inside `src/`
* [ ] `requirements.txt` or `package.json` is included
* [ ] `.env.example` is included
* [ ] No real `.env` file is committed
* [ ] No API keys or passwords are committed
* [ ] No `node_modules/` is committed
* [ ] No `venv/` is committed
* [ ] No `__pycache__/` is committed
* [ ] No unnecessary build artifacts are committed
* [ ] Application runs successfully
* [ ] AI features used in the presentation are implemented
* [ ] Demo data is clearly identified as simulated when applicable
