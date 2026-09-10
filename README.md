# MediCase AI — Intelligent Digital Patient Case-Taking Software

> **Concept:** *"From Manual Case Taking to Intelligent Digital Clinical Documentation"*  
> **Presentation Edition:** Smart India Hackathon (SIH 2026) Prototype

---

## 1. Problem Statement
Manual, paper-based patient case-taking in healthcare environments is fraught with critical challenges:
- **Illegibility & Data Loss:** Hand-written prescriptions and fragmented case sheets result in lost clinical history and potential medication errors.
- **Cognitive Overload:** Physicians spend up to 40% of consultation time on manual handwriting rather than patient interaction.
- **Broken Care Continuity:** Patient records are scattered across visits with no longitudinal view of clinical progression or chronic conditions.
- **Queue Chaos:** Outpatient departments lack synchronized token systems, resulting in crowd congestion and uncertain wait times.
- **Language Barriers:** In multilingual regions like India, healthcare staff require intuitive localization across English, Telugu, and Hindi.

---

## 2. Objectives & Proposed Solution
**MediCase AI** digitizes and streamlines the complete outpatient clinical journey:
1. **Guided 14-Step Clinical Case Taking:** A progressive stepped wizard navigating through Chief Complaints, HPI, Past History, Medications, Allergies, Family & Social History, ROS, Vitals, Physical Exam, Investigations, Assessments, Prescriptions, AI Digest, and Final Review.
2. **AI Clinical Case Summarization:** Automated synthesis of structured clinical parameters into concise narrative summaries with mandatory physician review and ethical medical safety disclaimers.
3. **Voice-to-Text Clinical Dictation:** Native hands-free speech recognition allowing doctors to dictate examination notes and clinical findings directly into form fields.
4. **Multilingual Localization:** Instant trilingual interface switching between **English (EN)**, **Telugu (తెలుగు - TE)**, and **Hindi (हिंदी - HI)**.
5. **Longitudinal Patient Timeline:** An interactive vertical timeline connecting all lifetime consultations, diagnostic test uploads, prescription changes, and follow-up milestones chronologically.
6. **Live Queue & Token Announcer:** Real-time token generation, estimated wait time calculation, and pleasant Web Audio synthesizer chimes for token announcements.
7. **Official PDF Case Reports:** Certified, printable electronic case records and prescriptions with hospital branding and doctor signature stamps.
8. **Immutable Audit Trails & Security:** Comprehensive logging of all clinical actions, role-based route protection, and patient duplicate detection.

---

## 3. Demo Credentials & User Roles

| Role | Demo Email | Demo Password | Primary Responsibilities |
|---|---|---|---|
| **Doctor** | `doctor@demo.com` | `Doctor@123` | Patient search, live queue caller, 14-step case taking, AI summaries, voice dictation, prescription builder, PDF reports. |
| **Receptionist / Staff** | `staff@demo.com` | `Staff@123` | Patient registration, duplicate detection, appointment scheduling, check-in, token generation, queue management. |
| **Administrator** | `admin@demo.com` | `Admin@123` | System analytics, department distribution, user management, immutable audit logs, system configuration. |

*Quick 1-click login buttons are directly available on the Landing Page and Login Screen for fast SIH demonstration.*

---

## 4. Rapid 2-Minute SIH Demonstration Flow
1. **Step 1 (Receptionist):** Login as Staff (`staff@demo.com`) ➔ Register a new patient (or search existing) ➔ Issue OPD Token `#18`.
2. **Step 2 (Doctor Queue):** Switch to Doctor (`doctor@demo.com`) ➔ View Live OPD Queue with Audio Chime ➔ Click **"Start Consultation"**.
3. **Step 3 (14-Step Case Taking):** 
   - Step 1: Review Patient Demographics & Allergy Alert.
   - Step 2–3: Add Chief Complaints & Click **🎤 Dictate Notes** for voice-to-text input into HPI.
   - Step 4–7: Document Past History, Active Medications, Allergies, and Review of Systems (ROS).
   - Step 8–10: Record Vitals (Auto-calculated BMI), Physical Exam signs (Pallor/Edema), and Diagnostic Labs.
   - Step 11–12: Add Clinical Assessment (Provisional Diagnosis) and formulate Prescription (Rx) with follow-up date.
   - Step 13: Click **"Generate AI Summary"** ➔ Review 4-quadrant summary with mandatory Doctor Review badge.
   - Step 14: Review case ➔ Click **"Finalize & Complete Visit"** (Confetti celebration!).
4. **Step 4 (Reports & Timeline):** Click **"Download PDF"** for the official medical report ➔ Open **Patient Profile** to view the newly added consultation on the **Longitudinal Patient Timeline**.

---

## 5. Technology Stack

- **Frontend:** React 18 with TypeScript, Vite
- **Styling:** Tailwind CSS, PostCSS, Autoprefixer (Clinical design tokens)
- **Icons:** Lucide React
- **Analytics & Data Visualizations:** Recharts (Area charts, Bar charts, Donut charts)
- **PDF Generation & Printing:** jsPDF, html2canvas, CSS Print Stylesheets
- **Voice Recognition:** Web Speech API (`webkitSpeechRecognition`) + Intelligent Fallback
- **Sound Effects:** Web Audio API (Dual-tone synthesizer chimes)
- **Backend API:** Node.js, Express.js, CORS
- **Persistence:** LocalStorage Synchronized Repository + REST Endpoints

---

## 6. Installation & Local Setup

### Prerequisites
- **Node.js**: v18.0.0 or higher
- **npm**: v9.0.0 or higher

### Steps to Run Locally

```bash
# 1. Clone repository and navigate to root directory
cd CaseTakingSystem

# 2. Install all dependencies
npm install

# 3. Start the application (Vite Dev Server + Express Backend API)
npm run dev

# 4. Open in browser:
# Frontend URL: http://localhost:5173
# Backend API:  http://localhost:5000/api/health
```

---

## 7. Environment Variables (`.env.example`)

```env
PORT=5000
VITE_API_BASE_URL=http://localhost:5000/api
VITE_APP_ENV=development
```

---

## 8. Medical Safety & Ethical AI Framework
- **Non-Autonomous Principle:** The artificial intelligence assistant strictly formats, extracts, and summarizes doctor-entered parameters. It **never** autonomously makes medical diagnoses or prescribes medications.
- **Mandatory Review Tag:** All AI summaries carry an explicit tag: *"AI-Generated Summary — Requires Attending Physician Review"*.
- **Physician Authority:** Final clinical diagnosis and treatment plans remain the exclusive legal and professional responsibility of the licensed medical practitioner.

---

## 9. License & Team
Developed for **Smart India Hackathon (SIH 2026)**. All sample patient data in this prototype is fictional and intended exclusively for demonstration purposes.
