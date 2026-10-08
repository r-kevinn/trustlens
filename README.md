# TrustLens — Full-Interaction Credibility & Deception Assessment Engine

> **Unique Angle**: Unlike traditional security tools that only inspect an isolated link or message, **TrustLens evaluates the trustworthiness of an entire online interaction** across online sellers, job offers, rental listings, and service providers.

---

## 🌟 Key Features
- **Holistic Multi-Signal Analysis**: Cross-examines communication transcripts, claimed corporate entities, contact domains, payment rails, and urgency cues.
- **Inconsistency & Deception Detection**: Detects discrepancies between claimed identity and technical reality (e.g., claiming enterprise affiliation while communicating via free public webmail, or offering high wages for low-complexity entry tasks).
- **Domain-Specific Scam Pattern Recognition**:
  - **Online Marketplace**: Flags off-platform shifts, unbacked gift card/P2P payments, and fake shipping narratives.
  - **Employment / Job Offers**: Detects "fake check for home office equipment" scams, chat-only interviews, and premature PII requests.
  - **Rental Listings**: Flags "absentee missionary landlord" narratives, deposit demands before physical walkthroughs, and wire transfer pressures.
  - **Service Providers**: Detects unlicensed contractor risks, 100% upfront payment demands, and lack of milestone contracts.
- **Instant Trust Report with Calibrated Trust Index (0–100)**: Color-coded verdict (Safe, Proceed With Caution, High Risk, Fraud Alert).
- **Evidence Breakdown**: Categorized findings detailing claim-vs-reality inconsistencies, red flags with severity ratings, and positive credibility anchors.
- **Actionable Pre-Payment Verification Playbook**: Prioritized, step-by-step checklist guiding the user on exact verification actions before paying or sharing personal data.

---

## 🚀 Quickstart & Setup Steps

### Prerequisites
- Node.js (v18.0.0 or higher)
- No external heavy dependencies or complex database setup required (runs out-of-the-box).

### 1. Installation
Clone the repository and enter the directory:
```bash
git clone https://github.com/your-username/trustlens.git
cd trustlens
```

### 2. Environment Variables
TrustLens operates with zero mandatory external environment variables out of the box. You can optionally configure:
```bash
PORT=3000                 # Port number for the HTTP server (default: 3000)
NODE_ENV=development     # Environment mode (development / production)
```

Create a `.env` file (optional):
```env
PORT=3000
NODE_ENV=production
```

### 3. Start the Application
Run the zero-dependency web server:
```bash
npm start
```
Or directly:
```bash
node server.js
```
Open your web browser at:
```
http://localhost:3000
```

---

## 🧪 Running Automated Test Suite
TrustLens includes an automated verification test suite verifying all 4 domain scenarios:
```bash
npm test
```
Or directly:
```bash
node tests/run_tests.js
```

### Test Suite Output:
- Verifies classification accuracy across Employment, Rental, Marketplace, and Service Provider scenarios.
- Verifies Trust Index calculations, inconsistency extraction, and generation of the verification checklist.

---

## 📂 Repository Structure
```
trustlens/
├── package.json              # Project definition & scripts
├── server.js                 # HTTP server & REST API gateway (/api/analyze, /api/presets)
├── engine/
│   ├── analyzer.js           # Multi-signal cross-examination engine
│   └── scenarios.js          # Domain knowledge base & indicator weights
├── public/
│   ├── index.html            # Responsive, accessible user interface
│   ├── style.css             # Polished CSS styles, badges & layout
│   └── app.js                # Frontend reactivity & report renderer
├── sample_data/
│   └── test_cases.json       # Curated real-world interaction test cases
├── tests/
│   └── run_tests.js          # Automated end-to-end evaluation tests
├── ARCH_DOCS.md              # Technical Design Document with Mermaid diagrams
├── LICENSE                   # Open-source MIT License
└── README.md                 # Complete documentation & setup instructions
```

---

## 📄 Documentation Checklist
- [x] **README** with setup steps & environment variables
- [x] **Technical Design Document** with architectural diagrams (`ARCH_DOCS.md`)
- [x] **Sample Data / Test cases** (`sample_data/test_cases.json`)
- [x] **License file** (`LICENSE` - MIT)

---

## ⚖️ License
Distributed under the open-source [MIT License](LICENSE).
