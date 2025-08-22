---
layout: post
title: "Hackathon Project: SYRESS Dashboard – AI-Powered Secure Resource Management"
date: 2025-05-10 12:00:00 +0000
categories: hackathon hacknbiz
tags: [AI, Blockchain, GDPR, Hybrid Cloud, React, FastAPI, Okta, AWS, OpenStack]
---

## Overview
During the **HACK'N'BIZ Hackathon (May 2025)**, our team **0x4Fun** developed **SYRESS**, an AI-powered platform for secure enterprise resource management. The project integrates **AI/ML models, blockchain storage, and hybrid cloud deployment** to ensure data integrity, automation, and GDPR compliance. Below are the key components and outcomes.

![Hackathon Participation Certificate](/images/competitions/syress/hacknbiz.jpg)  
*Certificate of Participation*

---

## System Architecture
SYRESS is built as a multi-layered system with the following components:

### Architecture Diagram
![SYRESS Architecture Diagram](/images/competitions/syress/architecture_diagram.png)  
*Figure 1: High-level architecture of SYRESS Dashboard*

### Key Layers
1. **User Interaction**  
   - **Okta SSO** for secure access (RBAC + MFA).  
   - System Admins interact via a React-based dashboard.

2. **Application Layer**  
   - **React Frontend**: Responsive UI for resource management.  
   - **FastAPI Backend**: Orchestrates data flow and API requests.

3. **AI/ML Layer**  
   - **RAG Engine**: Handles forecasting, classification, and reporting.  
   - **CV Model**: OCR for document structuring.

4. **Data & Security Layer**  
   - **Hyperledger Fabric**: Blockchain storage for immutable records.  
   - **AWS KMS + AES-256/TLS 1.3**: Encryption for data at rest/transit.

5. **Deployment Layer**  
   - **Hybrid Cloud**: AWS (EC2, Lambda, S3) + OpenStack (private cloud).

---

## Use Case Scenario
A multinational corporation uses SYRESS to:  
1. Upload financial documents via the React UI.  
2. Automate OCR and classification via the CV Model.  
3. Generate forecasts using the RAG Engine.  
4. Store hashes in Hyperledger Fabric with AWS KMS encryption.  
5. Ensure GDPR compliance via Okta RBAC and audit logs.

---

## Advantages
- **Security**: Blockchain + Okta + AES-256/TLS 1.3.  
- **Automation**: AI-driven insights (RAG + CV).  
- **Scalability**: Hybrid cloud (AWS + OpenStack).  
- **Compliance**: GDPR-ready design.

---

## Technical Stack
| Layer               | Technology Used          |
|---------------------|--------------------------|
| Frontend            | React                    |
| Backend             | FastAPI                  |
| AI/ML               | RAG Engine, CV Model     |
| Storage             | Hyperledger Fabric       |
| Security            | Okta SSO, AWS KMS        |
| Deployment          | AWS EC2/Lambda, OpenStack|

---

## Hackathon Learnings
- **Team Collaboration**: Agile development under time constraints.  
- **Tech Integration**: Bridging AI, blockchain, and cloud services.  
- **GDPR Compliance**: Balancing functionality with regulatory requirements.

---

## Future Improvements
- Add **multi-tenant support**.  
- Integrate **Twilio for SMS alerts**.  
- Expand AI models for **predictive analytics**.

---

## Conclusion
SYRESS demonstrates how **AI, blockchain, and hybrid cloud** can solve enterprise challenges in security and compliance. The hackathon was a great opportunity to innovate and deliver a production-ready architecture.

**Team 0x4FUN**  
*Hackathon Winners (Security Track)*  

### Project Documentation
1. [Hackathon Certificate](/images/competitions/syress/hacknbiz.jpg)  
2. [SYRESS Technical Report](/images/competitions/syress/technical_report.pdf)  
3. [SYRESS Project Brief](/images/competitions/syress/SyRess.pdf)  
4. [SYRESS Detailed Documentation](/images/competitions/syress/SyRess_doc.pdf)  