# CyberGuard AI: Adversarial Attacks and Defenses Platform

An end-to-end AI-driven threat intelligence dashboard and threat vector analysis platform for ABC Corporation.

---

## Project Components
1. **React Frontend**: Premium dark mode dashboard with glassmorphism layout, live alerts feed, NLP email scanner, malware static file sandbox, access log auditor, and audit trail vault.
2. **Flask Backend API**: Python REST API loading pre-trained Scikit-Learn models and communicating with a database.
3. **Database**: Relational database logging user roles, security incidents, and system audit logs.
4. **Machine Learning Engines**:
   - **Phishing Detection**: TF-IDF + Logistic Regression NLP model.
   - **Malware Analysis**: Random Forest PE header metadata classifier.
   - **Access Guard**: Random Forest authentication anomaly analyzer.

---

## Folder Directory Structure
```text
adversarial-attacks-defenses/
├── README.md
├── docs/                         # Strategic and Architectural documentation
├── backend/                      # Flask API & ML scripts
│   ├── app/                      # App source code
│   │   ├── models/               # ML loaders & database schemas
│   │   ├── routes/               # API endpoint blueprints
│   │   └── utils/                # Data generation & training utilities
│   ├── requirements.txt          # Python dependencies
│   └── run.py                    # Server entry script
├── frontend/                     # React Single Page App
└── ml_models/                    # Serialized pickle ML model binaries
```

---

## Setup & Running Instructions

### 1. Backend Setup
1. Open a terminal in the project directory:
   ```bash
   cd C:\Users\PARTH\.gemini\antigravity\scratch\adversarial-attacks-defenses
   ```
2. Activate the virtual environment:
   - On Windows PowerShell:
     ```powershell
     .\venv\Scripts\Activate.ps1
     ```
   - On Linux/macOS:
     ```bash
     source venv/bin/activate
     ```
3. Run the synthetic data generator & train the AI/ML models:
   ```bash
   python backend/app/utils/data_generator.py
   python backend/app/utils/trainer.py
   ```
4. Run the Flask backend server:
   ```bash
   python backend/run.py
   ```
   *The server runs locally on `http://localhost:5000`.*

### 2. Frontend Setup
1. Open a new terminal in the frontend directory:
   ```bash
   cd C:\Users\PARTH\.gemini\antigravity\scratch\adversarial-attacks-defenses/frontend
   ```
2. Install Node dependencies:
   ```bash
   npm install
   ```
3. Launch the React local development server:
   ```bash
   npm run dev
   ```
   *The client dashboard opens locally on `http://localhost:5173`.*

---

## Verification Guide
- **Login Portal**: Click "Create Account" to register a `SOC Threat Analyst` account. 
- **Phishing Scanner**: Paste an email containing terms like "verify account immediately" or "urgent crypto wire transfer" to trigger alerts.
- **Malware Sandbox**: Drag a file (e.g. name containing `patch.exe` or `crack.exe`) into the drop zone to analyze simulated high entropy, suspicious sections, and API calls.
- **Access Guard**: Run the preloaded "Out-of-Hours Brute Force" scenario to view anomaly analysis.
- **Log Vault**: Review threat logs, inspect metrics, and update mitigation status (from *Pending* to *Mitigated*, *Investigated*, or *False Positive*).
