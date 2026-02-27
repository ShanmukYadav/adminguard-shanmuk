# Research Notes: AdmitGuard Project

**Date:** February 27, 2026  
**Project:** Admission Data Validation & Compliance System (IIT Gandhinagar)

---

## 1. Google AI Studio: Build Mode & Vibe Coding

### Concept
Vibe coding allows me to describe the application in plain English while the AI handles code generation.

### Build Mode
This is the primary interface for generating the application structure from a single descriptive prompt.

### Annotation Mode
I can use point-and-click editing to refine specific UI elements or logic without rewriting entire prompts.

### Iteration Strategy
The key is to refine and add features through conversation rather than attempting a "big bang" build.

---

## 2. Prompting Framework: R.I.C.E.

To ensure high-quality code generation, I will follow the R.I.C.E. framework for every sprint:

### Role
Define the AI as a senior full-stack engineer.

### Intent
Clearly state the specific feature being built (e.g., "Create an 11-field form").

### Constraints
Set technical boundaries like "no external frameworks" and "card-based layout".

### Examples
Provide valid and invalid data cases to guide the validation logic.

---

## 3. Core Logic Requirements

I have categorized the institutional requirements into two distinct validation tiers:

### Strict Rules (Hard Blocks)
Zero tolerance for errors in:
- Name
- Email
- Phone (10 digits starting 6–9)
- Aadhaar (12 digits)
- Workflow-dependent fields like Interview Status

### Soft Rules (Override Required)
Benchmarks for:
- Age (18–35)
- Graduation Year (2015–2025)
- Academic Scores (≥60% or 6.0 CGPA)

### Exception Handling
Soft rule violations must require a structured rationale (minimum 30 characters) containing keywords like:
- "approved by"
- "waiver granted"

---

## 4. Technical Architecture Goals

### Configurable Engine
Refactor rules into a `rules.json` file so eligibility criteria can be updated without touching code.

### Auditability
Every submission must be logged with:
- Timestamp
- Field values
- Any exceptions used for compliance tracking

### Deployment
The final solution must be a lightweight, client-side app shared via a link.
