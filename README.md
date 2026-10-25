# Mon Saathi (মনৰ সংগী)
### Offline-First Cultural Cognitive Engagement, Daily Routine Assistance, and Caregiver Telemetry Platform for Elderly Dementia Care in Rural North Eastern Region

[![Smart India Hackathon 2026](https://img.shields.io/badge/SIH-2026-orange.svg)](https://sih.gov.in)
[![Team Helix](https://img.shields.io/badge/Team-Helix%20(ID%3A%20144294)-0284c7.svg)](#)
[![Ministry](https://img.shields.io/badge/Ministry-MDoNER-green.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python: 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](#)

---

## 🌟 Executive Summary
**Mon Saathi (মনৰ সংগী)** is an offline-first assistive healthcare platform designed specifically for rural elderly individuals living with early-to-moderate dementia across the North Eastern Region (NER) of India. 

Addressing an acute healthcare vacuum where remote hill districts often have less than **1 practicing neurologist per million citizens**, Mon Saathi bridges the diagnostic and care divide through a zero-failure Montessori errorless interface for elders, combined with an encrypted edge telemetry pipeline and clinical decision support for family caregivers and visiting Accredited Social Health Activists (ASHA workers).

---

## 🏗️ Project Architecture
```text
mon_saathi/
├── backend/
│   ├── app/
│   │   ├── api/
│   │   │   ├── assessments.py    # AD8 & Mini-Cog test recording
│   │   │   ├── routines.py       # Routine compliance logging
│   │   │   └── sync.py           # Delta synchronization (<10 KB batching)
│   │   ├── core/
│   │   │   ├── config.py         # Application settings & CORS
│   │   │   └── database.py       # SQLAlchemy engine & session maker
│   │   ├── models/
│   │   │   └── entities.py       # Patient, Event, Assessment, Routine tables
│   │   └── schemas/
│   │       └── pydantic_models.py# Validation schemas
│   ├── main.py                   # FastAPI server entry point
│   └── requirements.txt          # Production dependencies
├── frontend/
│   └── index.html                # Mon Saathi responsive single-page application
├── docs/
│   ├── architecture.md           # Technical blueprint
│   └── portal_registration.md    # SIH 2026 official registration narrative
└── .github/workflows/
    └── tests.yml                 # Automated testing workflow
```

---

## 🚀 Quick Start Guide

### 1. Prerequisites
- Python 3.10+ installed
- Modern web browser (Chrome, Edge, Firefox, or Safari)

### 2. Backend Setup
```bash
# Navigate to backend directory
cd backend

# Create and activate virtual environment
python -m venv venv

# On Windows:
venv\Scripts\activate
# On Linux/macOS:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run the FastAPI server
python main.py
```
*The interactive API documentation will be available at `http://localhost:8000/docs`.*

### 3. Frontend Setup
Open `frontend/index.html` directly in any browser, or serve it locally:
```bash
cd frontend
python -m http.server 3000
```
Open `http://localhost:3000` to interact with Mon Saathi.

---

## 🛡️ Regulatory & Clinical Standards
- **CDSCO Classification:** Class A Non-Diagnostic Software as a Medical Device (SaMD) Wellness Companion.
- **Privacy Compliance:** Local-first architecture compliant with India's **Digital Personal Data Protection (DPDP) Act 2023** (zero raw audio or facial imagery leaves the client device).
- **Clinical Validation:** Integrates Washington University AD8 Informant Interview and Mini-Cog Delayed 3-Word Recall scoring frameworks.
