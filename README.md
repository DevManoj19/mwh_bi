# mwh_bi

# Decentralized Identifier (DID) System with Dataverse & Verifiable Credentials

A scalable, GDPR-compliant decentralized identity system built to integrate with Dataverse and empower users in cultural heritage, academic research, and decentralized ecosystems. The project adheres to [W3C DID](https://www.w3.org/TR/did-core/), DOI, and Handle specifications, leveraging **DIDKit**, **cryptographic standards**, and optional **AI-driven metadata enhancement**.

---

## 🚀 Project Goals

- Develop a decentralized identity (DID) system
- Integrate with Dataverse (Java-based research data repository)
- Ensure GDPR compliance (user-controlled visibility)
- Implement W3C-compliant DID Documents & Verification Methods
- Demonstrate AI-assisted metadata validation or enhancement
- Sign and verify Verifiable Credentials (VCs)
- Prepare for integration with decentralized storage/payment systems like IPFS or USDFC

---

## 🧩 Technologies Used

### 🛠 Core Libraries
| Tool | Purpose |
|------|---------|
| `didkit` | DID & Verifiable Credentials (VCs) generation |
| `pyld` | JSON-LD processing |
| `requests` | API interaction (Dataverse, DID resolvers) |
| `cryptography` | Key generation, signature verification |
| `asyncio` | Asynchronous DID operations |
| `py-did` / `did-resolver` (optional) | DID resolution abstraction |

### 🧱 Dataverse Backend (External Dependencies)
- Java 11+
- Payara Server / GlassFish
- PostgreSQL 13+
- Solr (for indexing/search)

---

## 📁 Folder Structure

project-root/
│
├── mwh_bi.ipynb # Main Jupyter notebook (code + documentation)
├── .env # Optional environment file for secure config
├── README.md # This project overview and setup guide


---

## 🏗️ Installation Guide

### 1. Python Dependencies

Install required Python libraries:

```bash
pip install didkit pyld requests cryptography
```
---

### Dataverse Backend Setup (manual)
Required for full Dataverse API integration.

Install Java 11+

Deploy Payara Server or GlassFish

Setup PostgreSQL 13+ with Dataverse schema

Configure Solr for search indexing

Configure .env if needed for API keys

---
### 🔐 Key Functional Blocks
W3C DID Concepts Implemented
DID Subject

DID Document (with context and verificationMethod)

Verification Methods (Ed25519 public keys)

Service Endpoints (optional)

DID Resolution & Controllers
---

### 📋 Verifiable Credential Workflow
Generate Ed25519 key using DIDKit

Create a DID and DID Document

Define a credentialSubject and metadata (e.g., contribution, role)

Sign VC using DIDKit

Verify using DIDKit (errors: [] if success)

Optionally link to Filecoin/IPFS for permanent storage
---

### 📡 Example Use Case
A researcher logs in using a self-sovereign DID.

Metadata about cultural datasets is validated using AI or manually entered.

The metadata is signed as a verifiable credential and linked to the DID.

DID Document stores service endpoints pointing to Dataverse.

GDPR-compliance is achieved by user-controlled visibility of metadata.
---

### 📦 Sample Credential Output
```bash
json
{
  "@context": ["https://www.w3.org/2018/credentials/v1"],
  "type": ["VerifiableCredential"],
  "issuer": "did:key:z6Mk...",
  "issuanceDate": "2025-07-05T00:00:00Z",
  "credentialSubject": {
    "id": "did:key:z6Mk...",
    "contribution": "Digitised 19th-century manuscript"
  },
  "proof": {
    "type": "Ed25519Signature2020",
    "created": "...",
    "proofPurpose": "assertionMethod",
    "verificationMethod": "...",
    "jws": "..."
  }
}
```
---

### 📈 Future Work
🔗 Integrate with IPFS or blockchain (e.g., Filecoin, Ceramic, Solana)

🧠 Use AI to classify or enrich metadata (e.g., NLP tagging)

💳 Add stablecoin payment logic (e.g., USDFC or token-gated VC issuance)

🔐 Expand VC types: academic credentials, contribution proofs, etc.

📘 Publish full DID Documents on-chain
---

### 🧪 How to Run
Open the mwh_bi.ipynb notebook in Jupyter or Google Colab.

Install required Python packages.

Run each cell step-by-step to:

Generate DID + VC

Interact with Dataverse

Sign and verify credential

For full deployment, run backend using Dataverse (Java) stack.
---

### 🤝 License
MIT License – Open Source & Community Driven.
---

### 👨‍💻 Contributors
DevManoj19 – DID Architecture & Research

Eshrath Subhani – Documentation, Testing, and Integration
