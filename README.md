# mwh_bi

# 🛡️ Decentralized Identifier (DID) System with Dataverse

A scalable, GDPR-compliant DID system designed for integration with [Dataverse](https://dataverse.org/), empowering users in cultural heritage domains. The project adheres to W3C DID, DOI, and Handle specifications, aiming to decentralize metadata control using AI and cryptographic standards.

---

## 🚀 Project Goals

- ✅ Develop a decentralized identity system  
- ✅ Integrate with Dataverse (Java-based research data repository)  
- ✅ Ensure GDPR compliance  
- ✅ Demonstrate AI-driven metadata validation or enhancement  
- ✅ Follow W3C DID standards  

---

## 🧩 Technologies Used

### ✅ Core Dependencies
- `cryptography` – Key generation, signature verification  
- `requests` – API interaction (e.g., with DID resolvers or blockchains)  
- `Java + Payara/GlassFish` – Required by Dataverse backend  
- `PostgreSQL` – Dataverse data storage  
- `py-did`, `did-resolver` (optional) – For DID spec compliance  

---

## 🏗️ Installation

### 1. Python Dependencies
```bash
pip install cryptography requests
```
2. External Dependencies (for Dataverse)
These are not installed in the notebook directly:

 Java 11+

 Payara Server or GlassFish

 PostgreSQL 13+

 Solr (for search indexing)

---

### 📁 Folder Structure
```bash
mwh_bi.ipynb        # Main notebook (development + documentation)
.env                # Environment file for secure keys (if any)
README.md           # Project overview and setup guide
```

---

### 🛠️ Key Functional Blocks
🔐 DID Specification (W3C)
DID Subject

DID Document

Verification Methods (e.g., public keys)

Service Endpoints

Controllers & Resolution

---

### 📡 Libraries Explored
py-did: DID creation and resolution

didkit, identity.com: Optional external integrations

---

### 📌 Example Use Case
Researcher logs in using a self-sovereign DID.

Metadata about cultural assets is validated and signed.

DID document stores endpoints for the data repository.

System ensures GDPR compliance by user-controlled metadata visibility.

---

### 📈 Future Work
🔗 Integrate with IPFS or blockchain (e.g., Ceramic, Solana)

🧠 Use AI to tag or classify datasets based on metadata

🔐 Add support for VC (Verifiable Credentials)

---
### 🤝 License
MIT License – Open Source & Community Driven

---

### 👨‍💻 Contributors
DevManoj19  – DID Architecture & Research

Eshrathsubhani – Documentation & Testing
