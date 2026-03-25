# 🏥 VitalID — Smart Emergency Health Identity & Record Exchange Platform

> Transforming Healthcare, One Smart Identity at a Time

VitalID is a privacy-first platform that gives every patient a unique health ID and QR code, enabling authorized hospitals to instantly access critical medical records — even during emergencies when the patient is unconscious.

---

## 🚨 The Problem

When a patient arrives at a new hospital, doctors often have no access to their previous medical history. Missing information about allergies, chronic conditions, current medications, or past surgeries can delay treatment and cause serious harm — especially in emergencies.

- Patients lose paper records or forget critical details
- Hospitals cannot share data across facilities
- Doctors waste precious minutes gathering basic history
- Unknown drug allergies can trigger fatal reactions

---

## 💡 Our Solution

VitalID assigns every patient a **unique, encrypted health ID** linked to their complete medical history. Verified hospitals can retrieve this data in seconds using the ID or a QR scan.

```
Patient Registers → Gets Unique ID + QR Code → Hospital Scans → Doctor Sees Full Summary
```

In normal situations, access requires **patient consent**. In emergencies, an **override mode** provides immediate access to life-saving details when the patient cannot respond.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 🪪 Unique Patient ID | One identifier links all records across hospitals |
| 📲 QR-Based Access | Instant patient identification via scan |
| 🏥 Verified Hospital Login | Only accredited facilities receive credentials |
| 🔐 Consent-Based Access | Patient approval required for normal record viewing |
| 🚨 Emergency Mode | Immediate access when patient is unconscious |
| 🤖 AI Safety Alerts | Automated warnings for drug conflicts or allergies |
| 🕵️ Anonymous Search | Records retrieved by ID, never by personal name |
| 📋 Audit Logs | Every access attempt logged with timestamp and user |
| 🔒 Role-Based Permissions | Doctors see only relevant patient information |

---

## 🗂️ What Doctors See in an Emergency

- Blood group
- Known allergies (drugs and food)
- Current medications and dosages
- Chronic conditions (diabetes, hypertension, etc.)
- Past surgeries and complications
- Emergency contact information

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React.js |
| Backend | Python (FastAPI) |
| Database | Supabase (PostgreSQL) |
| Auth | Supabase Auth with role-based access control |
| Security | Encrypted data at rest and in transit, audit trails |
| QR Engine | QR-based patient identification system |

---

## 🏗️ Architecture Overview

```
User / Hospital Interface
        │
        ▼
  Frontend (React.js)
        │
        ▼
  Backend (FastAPI)
        │
   ┌────┴────┐
   ▼         ▼
Supabase   Auth Module
(PostgreSQL) (RBAC)
        │
   ┌────┴────┐
   ▼         ▼
Audit Logs  QR ID Engine
```

---

## 🔐 Security & Privacy

- **Encrypted at rest and in transit** — medical records are never stored in plain text
- **Verified access only** — hospitals must be accredited to receive credentials
- **Anonymous lookup** — records are found by patient ID, not by name
- **Consent-first** — normal access always requires patient approval
- **Emergency override** — activates only when patient is unconscious or unable to communicate
- **HIPAA-aligned** — designed to comply with healthcare data regulations
- **Full audit trail** — every login, access, and override is logged

---

## 🚀 Getting Started

### Prerequisites

- Node.js v18+
- Python 3.10+
- Supabase account

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/vitalid.git
cd vitalid

# Frontend setup
cd frontend
npm install
npm run dev

# Backend setup
cd ../backend
pip install -r requirements.txt
uvicorn main:app --reload
```

### Environment Variables

Create a `.env` file in the `/backend` directory:

```env
SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_anon_key
SECRET_KEY=your_jwt_secret
```

Create a `.env.local` file in the `/frontend` directory:

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
VITE_API_BASE_URL=http://localhost:8000
```

---

## 📁 Project Structure

```
vitalid/
├── frontend/               # React.js application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Patient, Hospital, Doctor views
│   │   └── utils/          # QR generation, API helpers
├── backend/                # FastAPI application
│   ├── routers/            # Auth, patients, hospitals, records
│   ├── models/             # Database models
│   ├── services/           # Business logic
│   └── main.py
└── README.md
```

---

## 🌐 How It Works — User Flow

1. **Patient Registration** — Creates a secure profile with verified identity
2. **ID Generation** — System issues an encrypted unique health ID + QR code
3. **Record Upload** — Verified hospitals upload patient medical data
4. **Hospital Login** — Doctor logs in with accredited credentials
5. **QR Scan** — Patient QR is scanned at point of care
6. **Consent or Emergency** — Patient approves, or emergency override activates
7. **Instant Summary** — Doctor views complete one-screen patient overview

---

## 🔭 Future Scope

- National health ID integration
- Wearable device sync (smartwatch emergency access)
- Multilingual support for rural healthcare
- Telemedicine integration
- Government health database API connectivity
- Offline emergency mode (cached critical data)

---

## 👥 Benefits

**For Patients** — Faster treatment, fewer repeated tests, full control over data access

**For Doctors** — Instant history, allergy awareness, medication conflict alerts

**For Hospitals** — Reduced medical errors, improved outcomes, efficient workflows

**For the System** — Connected records, standardized access, data-driven insights

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

---

## 👨‍💻 Team

| Name |
|---|
| Aditya Katare |
| Aryan Khade |
| Kedar Nimbalkar |
| Niraj Kausadikar |

---

## 🏆 Built For

This project was built for **[Your College Name] Hackathon 2025**.

---

*VitalID — Because in an emergency, every second and every detail matters.*
