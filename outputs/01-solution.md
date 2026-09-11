# PTSF Solution Architecture

## Architecture Foundations

### Org Strategy
Use a single Salesforce org for onboarding, subsidy lifecycle, practitioner operations, and assessor operations, with regional controls handled through sharing and federation. This keeps operating data unified while residency/legal isolation requirements are confirmed. `[assumption: validate legal requirement for org-level regional isolation]`

### Identity And Access
Use Experience Cloud login and self-registration for patients, with policy-controlled social sign-in where approved. `[KB:experience_cloud_4-2-2026.md:2033-2175]`  
Use Security Assertion Markup Language federation for internal users from Active Directory. `[KB:experience_cloud_4-2-2026.md:27414-27466] [KA-11429]`

### Service Operations Backbone
Use Service Cloud queues and Omni-Channel routing for assessor work distribution, prioritization, and escalation visibility. `[KB:service_cloud_3-27-2026.md:49-50] [KB:service_cloud_3-27-2026.md:300-322]`

### Integration Baseline
Use synchronous API checks for in-journey eligibility decisions, and asynchronous patterns for non-blocking downstream updates and reconciliation. `[assumption: validate health-insurance API latency and retry contract]`

### DevOps And Governance
Use source-driven development with controlled sandbox promotion and release governance, with named owners for identity, eligibility-rule, and support-channel decisions. `[extends: source-driven Salesforce multi-team delivery pattern]`

## Solution By Business Process

### Patient Identity And Onboarding Experience (E01)
**Business context**: Patients need a trusted registration and onboarding experience before any subsidy request can proceed.  
**Solution approach**: Use Experience Cloud for registration, authentication, multilingual onboarding steps, and completion gating. `[KB:experience_cloud_4-2-2026.md:2033-2175]`  
**Supporting architecture**: Keep a canonical patient identity record and prevent duplicate identity fragmentation across email/password and social login. `[assumption: validate duplicate-account prevention policy]`

### Subsidy Application Lifecycle And Eligibility Decisions (E02)
**Business context**: PTSF needs consistent application intake, policy checks, and explainable outcomes across regions.  
**Solution approach**: Implement a stateful subsidy application lifecycle with declarative automation first, plus targeted Apex for complex orchestration and exception handling. `[KB:sales_einstein_implementation_guide.md:153-227] [extends: workflow-driven lifecycle automation]`  
**Supporting architecture**: Model treatment, entitlement outcome, decision reason, and appeal path explicitly so policy changes are governable.

### Practitioner Assignment And Assessment Operations (E03)
**Business context**: Assignment and specialist escalation must be timely, fair, and traceable against service targets.  
**Solution approach**: Build automated assignment by treatment eligibility plus proximity, with SLA-aware acceptance/reassignment/escalation flows. `[KB:service_cloud_3-27-2026.md:647-652]`  
**Supporting architecture**: External geospatial matching may be required depending on address quality and distance-calculation policy. `[assumption: validate geo-matching provider and tie-break rules]`

### Assessor Work Management And Collaboration Support (E04)
**Business context**: Assessors need a single operating model for internal handling and external collaboration.  
**Solution approach**: Use Service Cloud work queues and escalation pathways, with digital collaboration channels for patient/practitioner support. `[KB:service_cloud_3-27-2026.md:94-95]`  
**Supporting architecture**: Channel pattern remains a decision fork (enhanced chat vs embedded messaging vs form-first); finalize based on operating hours, concurrency, and transcript-governance needs. `[assumption: validate channel architecture and routing policy]`

### Migration, Security, And Regional Operating Model (E05)
**Business context**: Migration and security controls must protect continuity and sensitive data during transition.  
**Solution approach**: Run phased migration with explicit in-flight case handling, identity federation alignment, and auditable access controls for sensitive fields. `[KB:experience_cloud_4-2-2026.md:13864-13980]`  
**Supporting architecture**: Expose verification outcomes to internal teams while restricting raw medical-history visibility to approved roles and windows. `[assumption: validate compliance-approved evidence model]`

## Open Architecture Decisions
- Regional residency and legal isolation model (single-org with controls vs org-level partitioning).
- External collaboration channel architecture and deflection governance model.
- Geospatial assignment engine design and fallback logic.
- Medical-history verification evidence model for internal assessor decisioning.

## Initial Complexity Posture
This architecture implies medium-to-high complexity overall due to identity policy forks, lifecycle orchestration, queue-based operations, cross-system dependencies, and migration/security controls. Final per-epic T-shirt sizing follows after estimate review.
