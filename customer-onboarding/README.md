# Recruitment Process - BPMN 2.0 Model

## 📌 Overview
This project models a complex, end-to-end recruitment lifecycle. It focuses on the high-interaction "ping-pong" communication between a Candidate and Company X. The model maps every stage from the initial CV submission to the final job offer or technical rejection.

## 🖼️ Diagram

## ⚙️ Process Logic
The process is divided into three main operational phases:
1. **Initial Screening & Technical Review**: HR coordinates with the Technical Manager to validate the applicant's profile.
2. **The Scheduling Loop**: A sophisticated coordination phase for interview dates, featuring timeout handling (3-day wait) and automatic reminders to prevent process stagnation.
3. **Interview & Final Decision**:
   - **The Interview**: The Technical Manager conducts the meeting and provides a binary (Positive/Negative) decision.
   - **Closing the Loop**: In the case of a positive result, HR prepares and sends the official Job Offer.
   - **The End State**: The process concludes when the candidate either accepts the offer (Acquired Job) or is formally rejected.

## 👥 Participants (Pools/Lanes)
**Pool 1: Candidate Expanded Pool)**: Manages documentation, negotiates availability, and responds to the final offer.

**Pool 2: Company X (Internal Pool)**:
- **HR Department (Lane)**: Acts as the communication hub, managing scheduling, reminders, and offer preparation.
- **Technical Manager (Lane)**: Owns the technical evaluation, interview performance, and final hiring recommendation.

##💡 Technical Highlights
1. **Message Exchange**: Extensive use of Message Flows (dashed lines) to represent cross-pool communication (emails/notifications).
2. **Event-Driven Logic**: Uses Event-based Gateways to wait for candidate responses or interview results.
3. **Exception & Timeout Management**: Includes Intermediate Timer Events to handle cases where candidates do not respond within 3 days.
4. **Diverse End States**: Uses multiple End Events to clearly distinguish between a successful hire, a CV rejection, and a technical rejection.

## 🛠️ Tools Used
- **[bpmn.io](https://bpmn.io)** - Web-based modeling tool (Camunda's toolkit).
- **BPMN 2.0 Standard** - Universal notation for business process modeling.

## 🚀 How to Open
1. Download the `.bpmn` file from this repo.
2. Import it into any BPMN 2.0 compliant tool.
