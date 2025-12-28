# 🇩🇪🇫🇷 KP Assist  
**AI-Assisted Clinical Documentation & Case Preparation for the Kenntnisprüfung (Germany)**

---

## 1. Project Overview

**KP Assist** is an AI-powered training and documentation system designed to help **foreign-trained doctors** prepare effectively for the **Kenntnisprüfung (KP)** in Germany.

The system transforms **rough, non-native clinical notes** into **KP-ready German medical documentation**, structured oral case presentations, and examiner-style questions — exactly as expected in German hospitals and KP exams.

> **Core principle**  
> KP Assist does **not** replace medical knowledge or clinical judgment.  
> It trains **structure, documentation, clinical reasoning, and medical German**, which are the most frequent causes of KP failure.

---

## 2. Problem Statement

Germany relies heavily on foreign-trained physicians, yet many candidates:
- Fail or delay the KP due to **language and documentation issues**
- Struggle with:
  - German clinical structure (Anamnese, Status, DD, Diagnostik, Therapie)
  - Correct use of **Konjunktiv I**
  - Examiner-style oral presentation
  - Understanding *what examiners expect* vs *what they penalize*

Existing preparation methods are:
- Passive (PDFs, scripts)
- Expensive (courses €2,000–€5,000)
- Non-personalized
- Not output-focused

KP Assist directly targets this gap.

---

## 3. Target Users

### Primary (B2C)
- Foreign doctors preparing for the **Kenntnisprüfung**
- Doctors during Hospitation or early Assistenzarzt months
- Candidates in **Internal Medicine & Surgery**

### Secondary (future – B2B)
- KP preparation schools
- Medical language institutes
- Hospitals onboarding international doctors

---

## 4. Scope & Positioning

### What KP Assist **IS**
- A **KP preparation and documentation training tool**
- A **German clinical language & structure transformer**
- A **simulation environment for KP-style cases**

### What KP Assist **IS NOT**
- ❌ A diagnosis engine  
- ❌ A patient-facing medical tool  
- ❌ A medication dosing calculator  
- ❌ A chat-based “AI doctor”  

Strict scope ensures **safety, focus, and exam relevance**.

---

## 5. MVP Scope (Version 1.0 – Locked)

### 5.1 User Input

Users complete **one structured case form**:

1. Patient demographics (age, sex)
2. Hauptbeschwerde
3. Aktuelle Anamnese (free text)
4. Relevante Vorerkrankungen
5. Aktuelle Medikation
6. Allergien
7. Vegetative Anamnese
8. Klinischer Status (free text)
9. Eigene Verdachtsdiagnose (optional)

> No lab uploads, no imaging, no real patient identifiers.

---

### 5.2 System Output

For each case, KP Assist generates **exactly four outputs**:

#### 1️⃣ Structured Written Documentation (KP-konform)
- Anamnese  
- Klinischer Status  
- Arbeitsdiagnose  
- Differentialdiagnosen  
- Diagnostikplan  
- Therapieplan  
- Disposition / Verlauf  

#### 2️⃣ Oral Case Presentation (KP style)
- 90s / 2min / 4min versions
- Examiner-friendly structure
- Concise, professional medical German

#### 3️⃣ KP Examiner-Style Questions
- 5–10 questions per case
- Focus on DD, next steps, reasoning

#### 4️⃣ PDF Export
- Printable
- Suitable for memorization and offline study

---

## 6. High-Yield KP Case Library (MVP)

### Internal Medicine
1. Acute dyspnea – Pneumonia  
2. Chest pain – Acute Coronary Syndrome  
3. Syncope  
4. Sepsis / Fever of unknown origin  
5. Acute Kidney Injury  
6. Stroke / TIA  
7. Gastrointestinal bleeding  
8. Electrolyte disorder (Hyponatremia / Hyperkalemia)  
9. Diabetic emergency (Hypoglycemia / DKA / HHS)

### Surgery
10. Acute abdomen – Appendicitis  
11. Ileus  
12. Cholecystitis  
13. Acute pancreatitis  
14. Polytrauma (basics)  
15. Postoperative fever / wound infection  

All cases share the **same documentation structure**.

---

## 7. Core MVP Features (EN)

### ✅ Feature 1 — Clinical Documentation Generator
- Converts rough input into **German-standard Klinikdeutsch**
- Enforces structure and register
- Correct use of **Konjunktiv I**

---

### ✅ Feature 2 — Missing Elements & Red Flags Detector
Flags missing KP-critical elements:
- Missing differential diagnosis
- Missing disposition
- Missing life-threatening exclusions

Rule-based in V1 for determinism and safety.

---

### ✅ Feature 3 — KP Rubric Scoring System
Each case is scored on:
- Structure completeness
- German medical phrasing
- Differential diagnosis quality
- Diagnostic appropriateness
- Patient safety coverage
- Oral presentation clarity

Provides:
- Section scores
- Concrete improvement feedback

---

### ✅ Feature 4 — Oral Presentation Trainer
- Time-controlled scripts
- Examiner-style phrasing
- “Avoid saying” guidance for common non-native patterns

---

### ✅ Feature 5 — Bilingual UI (German & French)
- UI language selectable
- **Medical outputs always in German**
- Optimized for Francophone candidates

---

### ✅ Feature 6 — Case History & Progress Tracking
- Save previous attempts
- Track improvement across rubric dimensions
- Identify personal weaknesses (e.g., DD, diagnostics, phrasing)

---

### ✅ Feature 7 — Protocol-to-Training Engine (Core MVP)
- Allows users to upload KP experience reports / protocols (e.g. Baden-Baden, Karlsruhe)
- Extracts examiner focus patterns such as:
  - Imaging intensity
  - Anatomy emphasis
  - Internal Medicine vs Surgery balance
  - Rapid-fire questioning style
- Dynamically adapts:
  - Case emphasis
  - Examiner-style questions
  - Rubric strictness
- Enables location-specific KP preparation without using or reproducing past exams
---

### ✅ Feature 8 — PDF Export
- Export generated cases to printable PDF
- Designed for memorization and offline revision
---

## 8. Technical Stack

- **Frontend:** Next.js (App Router)
- **Backend:** Next.js Server Actions / API routes
- **Database:** PostgreSQL + Prisma
- **Auth:** NextAuth / Clerk
- **AI Layer:** Server-side LLM calls only
- **PDF Export:** HTML → PDF renderer
- **Validation:** Zod (incl. AI JSON validation)

---

## 9. Legal & Safety Guardrails

- Educational / exam-preparation only
- No real patient identifiers allowed
- No medication dosages generated
- Disclaimer accepted on first use
- No patient-facing usage

---

## 10. Future Features (Post-MVP)

### High-Impact Extensions
- Examiner interrogation mode (Q&A drill with grading)
- Specialty modules (Neurology, Cardiology, ICU)
- Comparison with gold-standard cases
- Audio recording & timing analysis
- Hospital onboarding mode (B2B)

### Business Extensions
- Language school licensing
- Institutional dashboards
- KP crash-course case bundles

---

## 11. Success Metrics

- Weekly active usage
- Improved KP simulation performance
- Requests for additional cases/specialties
- Organic referrals in KP communities

---

## 12. Explicit Non-Goals

- No chatbot
- No diagnosis engine
- No medication calculator
- No real-time clinical decision support

**Focus beats scope creep.**

---

## 13. Vision

KP Assist aims to become the **reference training system** for:

> *“How a safe junior doctor documents and presents cases in Germany.”*

Not by replacing doctors —  
but by teaching them **how to think, write, and speak medicine in the German system**.

---

### Status
🚧 MVP in active development  
📦 PDF export included in V1  
🌍 German & French UI supported  
