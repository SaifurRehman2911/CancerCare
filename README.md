# CancerCare — Lab Technician & Diagnosis Management System

CancerCare is a full-stack, ML-powered web application built to support cancer diagnostic labs in managing patients, running predictive analyses, and streamlining the diagnosis-to-report workflow. It combines a machine learning prediction engine with a role-based clinical dashboard, giving lab technicians and doctors a single platform to handle everything from sample intake to final reporting.

Built as a 3rd Semester Data Science project at UET Lahore.

---

## Key Features

- **Authentication & Role Management** — Secure login system with hashed credentials (bcrypt) and JWT-based sessions
- **Lab Dashboard** — Central overview of lab activity, patient load, and system status
- **Single & Batch Prediction** — Run cancer risk/diagnosis predictions on individual samples or process entire batches at once
- **Patient Records & History** — Maintain structured patient profiles with full diagnostic history
- **Doctor Management** — Track doctors, assignments, and case ownership
- **Appointments** — Schedule and manage lab technician appointments
- **Post-Diagnosis Workflow** — Dedicated flow for next steps once a diagnosis is confirmed
- **Analytics Dashboard** — Visual insights into lab performance and diagnostic trends (Plotly / Matplotlib / Seaborn)
- **Report Generation & Export** — Generate and export clinical reports (ReportLab-powered PDFs)
- **Notifications & Messaging** — In-app notifications and internal messaging between staff
- **Search** — Quickly locate patients, doctors, or records across the system

---

## Tech Stack

| Layer | Technology |
|---|---|
| **Frontend / UI** | [Streamlit](https://streamlit.io/) |
| **Backend / ORM** | SQLAlchemy, Alembic (migrations) |
| **Machine Learning** | scikit-learn, imbalanced-learn, pandas, numpy, joblib |
| **Visualization** | Plotly, Matplotlib, Seaborn |
| **Authentication** | bcrypt, PyJWT |
| **Reports & Files** | ReportLab, Pillow |
| **Utilities** | python-dotenv, requests, psutil |

---

## Project Structure

```
CancerCare/
├── app.py                  # Main Streamlit entry point & page router
├── config.py                # App configuration
├── core/                    # Core backend logic
├── data/                    # Application/runtime data
├── data_science/            # ML models & training pipeline (model_1)
├── database/                 # Database models & connection layer
├── database_backup/         # Database backups
├── dsa/                     # Data structures & algorithms utilities
├── frontend/                # Streamlit page modules (UI)
├── scripts/                  # Setup / helper scripts
├── static/                  # Static assets
├── assets/                  # Images, logos, icons
├── uploads/                  # User-uploaded files
├── tests/                    # Test suite
├── requirements.txt          # Full dependency list
└── requirements-minimal.txt  # Minimal dependency set
```

---

## Getting Started

### Prerequisites
- Python 3.9+
- pip

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/SaifurRehman2911/CancerCare.git
   cd CancerCare
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate      # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
   For a lighter setup, use:
   ```bash
   pip install -r requirements-minimal.txt
   ```

4. **Configure environment variables**
   ```bash
   cp .env.example .env
   ```
   Then fill in the required values (database URL, secret keys, etc.).

5. **Run the application**
   ```bash
   streamlit run app.py
   ```

6. Open the app in your browser at `http://localhost:8501`

---

## How It Works

1. Users land on the **landing page** and authenticate through the **auth page**.
2. Once logged in, they're routed to a **role-based dashboard** (Lab Dashboard by default).
3. Lab technicians can run a **single prediction** or **batch process** multiple samples through the trained ML model.
4. Results feed into **patient history**, generate **reports**, and can trigger a **post-diagnosis** workflow.
5. Staff stay in sync via built-in **notifications** and **messaging**, with **analytics** giving a bird's-eye view of lab activity.

---

## Author

**Saif ur Rehman**
Data Science Student, University of Engineering and Technology (UET), Lahore
GitHub: [@SaifurRehman2911](https://github.com/SaifurRehman2911)

---

## License

This project is currently unlicensed. Add a license file if you intend to make usage terms explicit.
