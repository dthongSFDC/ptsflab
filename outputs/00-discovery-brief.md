# Discovery Brief — Patient Travel Support Foundation (PTSF)

## Executive Summary
Patient Travel Support Foundation (PTSF) needs to replace fragmented, office-level bespoke systems with a scalable Salesforce-based platform that can support high growth and sensitive patient-facing operations. The scope centers on patient onboarding, subsidy request processing, practitioner assessment workflows, and internal case handling, with clear integration and migration complexity. Discovery confirms strong functional direction but leaves key planning inputs open, including funding posture, named executive sponsors, and measurable success targets.

## Company And Industry Context
- PTSF is a not-for-profit focused on subsidized patient travel for medical treatment access in remote regions.
- Headquarters is in Singapore with operations across APAC, EMEA, and AMER.
- Regional operating model includes satellite offices handling intake, approval, and booking.
- Scale indicators are high: millions of patients and continued growth pressure on current processes.

## Current Vs. Target Salesforce Landscape
### Current State
- Existing process backbone is TAMS (Travel Application Management System), customized separately by local offices.
- Current web channel is static and relies on downloadable medical assessment forms.
- Internal identity is split across region-specific Active Directory instances.
- Health Insurance Checker API is already in use but exhibits peak latency.

### Target State (Discovery-Level)
- Move core patient subsidy processes to Salesforce for scalability and standardization.
- User-confirmed target scope: Experience Cloud plus Sales and Service capabilities.
- Digital onboarding and application workflows replace PDF and email-heavy operational steps.
- Patient and practitioner interactions include conversational support with assessor access.

## Project Scope And Objectives
### Confirmed Scope
- Patient account creation and onboarding with profile completion and language preference handling.
- Subsidy request lifecycle with treatment capture, insurance validation, practitioner assignment, reassignment, and escalation.
- Medical assessment orchestration, including specialist involvement and manager escalation rules.
- Internal assessor support for subsidy amount determination based on travel context.
- Visibility controls for patient and practitioner access boundaries.

### Business Objectives
- Improve scalability beyond current bespoke regional systems.
- Reduce manual errors in medical assessment handling.
- Improve cycle-time reliability through automation and escalation logic.
- Increase operational consistency across regions.

## Data, Security, And Compliance Considerations
- Data migration is broad: patients, subsidy applications, and assessments are all in scope.
- In-flight application rule is defined: existing active applications complete in current system.
- Internal authentication direction currently set to internal single sign-on only; patient login approach remains open.
- No named regulatory framework has been confirmed yet; baseline enterprise security posture assumed until clarified.
- Medical history access rules are explicit and should be treated as sensitive-data design constraints.

## Research Findings And Market Context
- Document-only discovery was used for this pass (no external web research requested).
- Problem shape aligns with high-scale public-benefit or healthcare-adjacent service modernization: fragmented regional operations, legacy workflow constraints, and rising demand growth.
- Integration reliability and data-access controls are expected to be major design drivers in downstream scoping.

## Extraction Audit
| Area | Status | Evidence / Basis |
|------|--------|------------------|
| Company identity | Confirmed | "Patient Travel Support Foundation (PTSF)... headquartered in Singapore... APAC, EMEA, AMER." |
| Salesforce current state | Confirmed | Current systems are bespoke TAMS + static website + regional Active Directory; move to Salesforce requested. |
| Target solution | Confirmed | User confirmed target scope as Experience Cloud + Sales + Service capabilities. |
| User count and personas | Confirmed | 4,000 medical practitioners, ~500 internal users, and large patient population. |
| Timeline and go-live | Unknown | No committed launch date provided; user confirmed no fixed date yet. |
| Business objectives | Confirmed | Scalability and reduction of error-prone manual assessment process explicitly stated. |
| Core business processes | Confirmed | Detailed onboarding, subsidy request, assessment, and approval workflows provided. |
| Integrations | Confirmed | Active Directory and Health Insurance Checker API are explicit; address validation implied. |
| Data migration | Confirmed | Full migration for patients, applications, and assessments stated. |
| Compliance / regulatory | Assumed | No named regulation provided; baseline enterprise controls assumed by user. |
| Budget and funding | Unknown | No budget range, funding source, or approval mechanics provided. |
| Stakeholders | Assumed | Role-level stakeholders identified (assessors, managers), but no named sponsors/decision owners. |
| Risks and constraints | Confirmed | API latency, regional customization drift, and manual document process risks are explicit. |
| Handoff signals | Assumed | Lab scenario appears pre-delivery scoping oriented; delivery handoff path not yet chosen. |
| Experience design signals | Assumed | Onboarding wizard, multilingual communications, and chat support imply user experience design workload. |
| Governance signals | Unknown | No explicit governance model, change management structure, or decision-rights framework identified. |

## Open Questions
1. What is the approved budget envelope and funding path (for example, single program budget vs. staged release funding)?
2. Who are the named executive sponsor, business owner, and technology decision owner for final scope and prioritization decisions?
3. What measurable outcome targets define success at go-live (for example processing time, error-rate reduction, reassignment rate, satisfaction outcomes)?
4. Should patient authentication include social sign-in and native credentials as originally requested, or should internal single sign-on direction influence customer login strategy?
5. Is there a formal data residency, healthcare privacy, or audit standard that must shape architecture choices by region?

## Delivery Signals For Next Skills
- High migration volume and growth trajectory suggest early data strategy and phased cutover planning.
- Integration behavior and latency tolerance should be validated before process automation finalization.
- Sensitive-field access constraints should be tested early against role design and sharing models.
- Clarifying governance and success metrics will materially improve requirements and roadmap defensibility.
