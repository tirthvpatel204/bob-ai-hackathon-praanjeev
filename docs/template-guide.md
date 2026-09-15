# Bob AI Innovation Hackathon Submission Template — Complete Guide

This guide explains how to use the `bob-ai-hackathon-submission-template` to structure and submit your hackathon entry.

---

## Table of Contents

1. [Overview](#1-overview)
2. [Getting Started — Use the Template](#2-getting-started--use-the-template)
3. [Repository Structure](#3-repository-structure)
4. [File-by-File Walkthrough](#4-file-by-file-walkthrough)
5. [Automated Validation](#5-automated-validation)
6. [Submission Checklist](#6-submission-checklist)
7. [How Your Entry Is Evaluated](#7-how-your-entry-is-evaluated)
8. [Common Mistakes](#8-common-mistakes)
9. [FAQ](#9-faq)

---

## 1. Overview

The template gives every team a consistent, well-structured repository so that:

* Judges can find what they need without hunting through your repo.
* The automated validation GitHub Action can check your submission is complete.
* Your entry is evaluated fairly against the same rubric as every other team.

**One template → one repo per team. Do not share repos across teams.**

---

## 2. Getting Started — Use the Template

### Step 1 — Create your repo from the template

1. Go to the official hackathon submission template repository.
2. Click the green **"Use this template"** button → **"Create a new repository"**.
3. Use **"Use this template"**, not **"Fork"**.
4. Name your repository:

```text
bob-ai-hackathon-[your-team-name]
```

5. Set repository visibility to **Public**.
6. Click **"Create repository"**.

For PRAANJEEV, the repository name is:

```text
bob-ai-hackathon-praanjeev
```

---

### Step 2 — Clone your new repo locally

```bash
git clone https://github.com/[your-github-username]/bob-ai-hackathon-[your-team-name].git
cd bob-ai-hackathon-[your-team-name]
```

For PRAANJEEV:

```bash
git clone https://github.com/tirthvpatel204/bob-ai-hackathon-praanjeev.git
cd bob-ai-hackathon-praanjeev
```

---

### Step 3 — Fill in your content

Complete the files in the repository with your actual project information.

---

### Step 4 — Push and verify the GitHub Action passes

```bash
git add .
git commit -m "feat: initial submission"
git push
```

Then open:

```text
GitHub Repository → Actions
```

Confirm that:

```text
Validate Submission
```

is **green**.

---

### Step 5 — Submit your repository URL

Submit the public GitHub repository URL through the official hackathon entry form.

---

## 3. Repository Structure

The required structure is:

```text
bob-ai-hackathon-[your-team-name]/
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
│       └── README.md
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

The top-level structure should remain intact because the validation workflow and evaluators depend on these files.

---

## 4. File-by-File Walkthrough

### 4.1 `submission.yaml` — Most Important

This is the first file evaluators read.

Fill it carefully and completely.

Example:

```yaml
team:
  name: "PRAANJEEV"
  track: "AI"
  lead:
    name: "Tirth Patel"
    email: "25aiml058@charusat.edu.in"
  members:
    - name: "Neev Patel"
    - name: "Tanmay Patel"
    - name: "Kashyap Modi"

submission:
  title: "PRAANJEEV — AI Emergency Response & Hospital Coordination System"
  problem_statement: >
    How can AI intelligently coordinate patients, ambulances, hospitals
    and critical medical resources during emergencies to reduce response
    and treatment delays?
  solution_summary: >
    PRAANJEEV is an AI-powered emergency response and hospital coordination
    platform that helps identify suitable verified hospitals based on
    emergency condition, medical capabilities, resources, location and
    travel time while enabling emergency information sharing and hospital
    preparation before patient arrival.
  key_features:
    - "AI Emergency Assessment"
    - "AI-Powered Hospital Matching"
    - "Hospital Resource Intelligence"
    - "Smart Emergency Routing"
    - "Hospital Pre-Alert"
    - "Verified Hospital Network"
    - "Location-Aware Recommendations"
```

### Rules

* Every required field must be filled.
* Blank required fields can fail validation.
* Do not rename `submission.yaml`.

---

### 4.2 `README.md`

The README is the human-readable front page of the repository.

Replace every placeholder with actual project information.

Important sections include:

| Section                      | What to write                                            |
| ---------------------------- | -------------------------------------------------------- |
| **Team**                     | Team name, track, lead and members                       |
| **Problem Statement**        | What problem you solve and who experiences it            |
| **Solution**                 | What you built and how it works                          |
| **Key Features**             | Specific implemented features                            |
| **Tech Stack**               | Languages, frameworks and IBM technologies actually used |
| **How to Run**               | Exact commands from `docs/setup-guide.md`                |
| **Demo**                     | Video, live demo and screenshots                         |
| **Known Limitations**        | Honest limitations                                       |
| **What We're Most Proud Of** | Strongest part of the project                            |

Before submitting, search the README for:

```text
[
```

Any remaining placeholder brackets should be reviewed.

---

### 4.3 `docs/`

The documentation directory contains four required project documents.

#### `docs/problem-statement.md`

Explain:

* The audience affected.
* Why existing solutions do not adequately solve the problem.
* Quantified pain if reliable data is available.
* Why the problem matters now.

#### `docs/solution-overview.md`

Explain:

* The core mechanism.
* What makes the solution different.
* Key design decisions.
* Why those decisions were made.
* The user experience.

#### `docs/architecture.md`

Include:

* A Mermaid diagram or architecture image.
* Component table.
* Technology and responsibilities.
* End-to-end data flow.
* Security considerations.
* Scalability considerations.

#### `docs/setup-guide.md`

This is the project setup guide.

It should include:

* Prerequisites.
* Tools and versions.
* Environment variables.
* Exact installation commands.
* Exact run commands.
* Verification steps.
* Troubleshooting.

Test the setup guide on a clean machine or fresh terminal before submitting.

---

### 4.4 `src/`

Put all application source code inside this directory.

```text
src/
├── .env.example
├── README.md
└── application source code
```

### Rules

* Never commit real credentials.
* Keep `.env` ignored by Git.
* Update `.env.example` with every variable required by the application.
* Do not commit:

```text
node
```
