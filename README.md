# Project PRCL-0012: Intelligent ITSM Optimization

## Problem Statement
Optimizing IT Service Management (ITSM) for "ABC Tech," which manages over 46K+ incidents. The project aims to replace manual triage with predictive insights to prevent SLA breaches and inefficient staffing during peak surges.

## Domain Analysis
The dataset contains 46,609 incident records tracking the lifecycle of IT support tickets:
  - **ID/ID_status:** Unique ticket identifier and its current state (Active, Awaiting User, Closed).
  - **Active:** Binary flag indicating if the ticket is currently being processed.
  - **Count_reassign/Count_opening/Count_updated:** Measures of ticket "churn" and how many times a ticket was reopened or reassigned.
  - **ID_caller/Opened_by/Created_by/Updated_by:** Audit trail of the users and technicians involved.
  - **Opened_at/Created_at/Updated_at:** Timestamps used to identify "weekly heartbeat" volume surges.
  - **Contact_number/Location/Category/Sub_category:** Categorical data about the user and the nature of the issue.
  - **U_priority_confirmation:** A manual check flag for ticket priority.
  - **Impact/Urgency/Priority (Target):** The core triage metrics; Priority is derived from the intersection of Impact and Urgency.
  - **CI_Cat (Configuration Item):** The specific asset category (e.g., Server, Software) that failed.

## Results & Takeaways
- Achieved over **80% seasonal accuracy** for infrastructure resilience.
- Identified that the Configuration Item is a better predictor of priority than the user's report alone.

## Technologies Used
- Python, Pandas
- Machine Learning (Classification & Forecasting)
