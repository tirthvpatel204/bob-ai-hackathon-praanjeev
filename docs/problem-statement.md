# Problem Statement

## Background

Medical emergencies are highly time-sensitive situations where delays in reaching the right hospital can directly affect patient outcomes. During an emergency, patients, family members and ambulance teams may need to make hospital decisions while dealing with incomplete information, traffic conditions and uncertainty about hospital capabilities.

A common approach is to identify the nearest hospital. However, the nearest hospital is not always the most appropriate hospital for a particular emergency. A hospital may be closer but may not have the required ICU capacity, oxygen, emergency facilities, specialist support or other critical resources.

PRAANJEEV addresses this coordination gap by combining emergency information, location, hospital capabilities, resource information and route conditions to support a more informed hospital-selection decision.

## The Problem

The core problem addressed by PRAANJEEV is:

> **How can AI intelligently coordinate patients, ambulances, hospitals and critical medical resources during emergencies to reduce response and treatment delays?**

The system focuses on the gap between **finding a nearby hospital** and **finding the right verified hospital for the emergency**.

Instead of considering distance alone, the system considers multiple factors such as:

* Patient emergency information
* Emergency severity
* Required medical capabilities
* Hospital verification status
* ICU and emergency-bed availability
* Oxygen and other critical resources
* Hospital capabilities
* Distance
* Traffic conditions
* Estimated travel time

## Who Is Affected?

### Patients and Families

Patients and their families may have difficulty determining which hospital is appropriate during a stressful emergency.

They may not know:

* Which nearby hospital has the required facilities
* Whether critical resources are available
* Which hospital is better suited to the emergency
* How long the ambulance journey may take

### Ambulance and Emergency Teams

Ambulance teams need to make rapid decisions while transporting patients.

They need information about:

* Patient condition
* Suitable hospitals
* Hospital capabilities
* Current resources
* Route conditions
* Estimated arrival time

### Hospitals

Hospitals may receive emergency patients without sufficient advance information.

This can make it harder for the hospital to prepare:

* ICU beds
* Emergency beds
* Oxygen
* Equipment
* Specialists
* Medical teams

## Why Existing Approaches Can Fall Short

Traditional hospital-finding approaches commonly focus on location or distance.

However:

> **Nearest does not always mean most suitable.**

For example, a hospital may be only 3 km away but lack an appropriate ICU facility or required emergency capability, while another verified hospital 7 km away may be better prepared.

A system that only searches by distance does not provide enough context for emergency coordination.

Similarly, navigation systems can provide routes but do not necessarily coordinate hospital capability, resource readiness and emergency information sharing together.

## Why This Problem Matters

Emergency response involves multiple connected decisions:

```text
Patient Emergency
       ↓
Understand the Condition
       ↓
Identify Required Capabilities
       ↓
Find Suitable Verified Hospitals
       ↓
Check Resources
       ↓
Consider Distance + Traffic
       ↓
Select Hospital
       ↓
Notify Hospital
       ↓
Prepare Before Arrival
       ↓
Emergency Treatment
```

If these steps remain disconnected, valuable time can be lost between the ambulance, patient and hospital.

PRAANJEEV aims to connect these steps into one coordinated emergency workflow.

## Core Problem Statement

PRAANJEEV solves the problem of **fragmented emergency coordination between patients, ambulances and hospitals**.

The system aims to help users move from:

> **"Which hospital is nearest?"**

to:

> **"Which verified hospital is the most suitable for this emergency, and how can we coordinate the journey and hospital preparation?"**

## Scope

PRAANJEEV is designed as an AI-powered decision-support and coordination platform.

It does **not** attempt to replace doctors or provide a medical diagnosis.

AI recommendations are intended to support emergency coordination and hospital selection. Real-world deployment would require integration with verified healthcare networks, reliable hospital resource updates, appropriate privacy controls and clinical validation.
