# Patient Travel Support Foundation (PTSF) — Lab Scenario Brief

> **Source:** Trailhead Academy — Technical Architect Program · Official Evaluation Practice Scenario.
> **Use:** This is the fictional customer brief the Quantum Leap Lab runs against. Feed it to Scopezilla in Stage 2; it will carry through every subsequent stage of the lab.

---

## Project Overview

The Patient Travel Support Foundation (PTSF) is a not-for-profit organization that helps people (patients) in remote regions access medical treatments that aren't available locally. PTSF subsidizes patient travel costs (bus, train, or plane fare).

PTSF is headquartered in Singapore and operates across the APAC, EMEA, and AMER regions. PTSF has 10 satellite offices in each of their regions that cover a defined geographical area. In those satellite offices, applications for travel are received, approved, and booked.

PTSF has grown to 3.5 million patients during their 5 years of operation. With their current processes managed by bespoke systems that run locally at each satellite office, PTSF understands that their current systems and processes will not scale any further and would like to move appropriate data and processes to the Salesforce platform.

## Users of the System

**Customers & partners:**

1. Patients that apply for transport subsidies.
2. 4,000 Medical Practitioners that assess the candidate's eligibility for the medical treatment.

**Internal users (~500):**

1. Assessors that review subsidy applications and assessments from Medical Practitioners.
2. Managers that look after Assessors and can approve more expensive subsidy applications, plus the supporting management hierarchy.

## Current Systems

1. **TAMS (Travel Application Management System)** — bespoke system that stores all subsidy applications. Deployed locally at each satellite office; each office has customized to their unique needs.
2. **Static website** — provides static content, downloadable PDF medical assessment forms, and FAQs for patients and Medical Practitioners.
3. **Active Directory** — each region maintains a separate AD instance. The new system should authenticate internal users using credentials from their appropriate AD instance.
4. **Health Insurance Checker** — global API service that verifies a patient's health insurance entitlements. Useful, but during peak times can take up to **15 seconds** to return results.

## Business Process Requirements

### Patient Onboarding

1. Patients must be able to create an account using their email address and password as well as Facebook.
2. On first login, Patients must step through an onboarding wizard to complete their personal profile (name, email, date of birth, address, language preference, insurance).
   - a. PTSF would like to prepopulate personal profile data with attributes returned by the Health Insurance Checker.
   - b. PTSF would like to validate the physical address input by the patient.
   - c. The patient cannot apply for a subsidy until the onboarding process is completed.
   - d. Patients should receive a welcome email in their language of preference that explains the subsidy application process after onboarding is complete.

### Requesting Travel Assistance

1. PTSF supports travel assistance for over **500 treatment types**. Subsidy applications require a treatment type, the reason for the request, and medical history information.
2. Medical history information previously provided by the patient must be verified with each subsidy application.
3. PTSF checks with the patient's health insurance to see if any travel costs can be covered. If the health insurance provider covers travel costs, the subsidy application should be **automatically rejected**.
4. When a subsidy application is created, a medical practitioner registered for that treatment type should automatically be allocated. Allocation is based on the **closest distance** between the medical practitioner's practice and the patient's address.
5. The medical practitioner must accept the application within **3 business days**; if no response or declined, reassign to another practitioner using the same logic.
6. Patients and medical practitioners should be able to **chat with a PTSF assessor** throughout the process. PTSF is also keen to deflect support requests for common questions.

### Patient Assessment and Subsidy Application Approval

1. Currently, the Medical Practitioner downloads a PDF medical assessment form from the website, assesses the patient, then returns the completed PDF via email. Some are printed, filled out by hand, scanned, and manually entered. PTSF wants to **improve this error-prone process**.
2. If an assessment is still "pending" 15 days after assignment, the system should escalate to Team Managers.
3. A Medical Practitioner may need an additional specialist to assess a particular aspect of the patient and should be able to request additional assessments.
4. If approved, the assessor enters a subsidy amount granted. The system should help the assessor determine the appropriate amount given the distance traveled and expected transportation type(s) (air, train, taxi, etc.).

## Data

1. PTSF has 5 million patients distributed evenly across regions; expects 50% growth each year over the next 5 years. On average, **20% of total patients request a subsidy each year**.
2. All existing patients, subsidy applications, and assessments should be migrated to the new system.
3. Any existing subsidy applications should be completed in the current system; on average the application process is completed in 1 month.

## Visibility & Accessibility

- Medical Practitioners can see all assessments for patients related to a subsidy application they are assigned to.
- Medical Practitioners can only see the patient's name, phone, and email, plus the patient description of services needed from the subsidy application.
- Medical Practitioners can see medical history for patients **only during the period where they have an open assigned assessment**. PTSF internal users **cannot see medical history at all**.
