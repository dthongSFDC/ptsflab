## INTENT FOR
Practitioners, assessors, and operations managers running daily assessment operations

## INTENT OUTCOME
Operationalize assignment, collaboration, and escalation workflows so assessments move quickly with clear ownership.

## INTENT MEASURED BY
Assignment and support interactions route correctly, SLA breaches are visible, and managers can act on escalation signals.

## INTENT MUST NOT
Must not allow collaboration channels or reassignment flows to bypass traceable work records.

## PRE-DECIDED
- Assignment depends on treatment eligibility and proximity input.
- Collaboration routing must bind to formal work records.
- Regional visibility and escalation reporting are required, not optional.

## PLAN-MODE QUESTIONS
- [ ] What deterministic geospatial method and tie-break order governs assignment?
- [ ] Which channel architecture is final for external collaboration intake?
- [ ] What region-specific operating-hour and language constraints apply to support routing?

## BUILD-MODE QUESTIONS
- How should unresolved reassignment attempts terminate when no suitable practitioner is found?
- What thresholds trigger manager escalation for collaboration backlog?

## DATA MODEL
Add assignment, reassignment, escalation, and collaboration tracking fields that preserve ownership history and support regional operations reporting.

## AUTOMATION
See INT-005 and INT-006. Implement practitioner assignment logic, reassignment and escalation automation, and collaboration routing into assessor queues with traceable handoffs.

## UI
Provide assessor and manager workspaces for queue handling, escalation action, and collaboration context linked directly to the underlying application records.

## SECURITY
Enforce role-based access and transcript visibility limits so collaboration data is usable for operations without exposing restricted sensitive details.

## REPORTS
See INT-007. Deliver manager dashboards for overdue assessments, reassignment churn, collaboration backlog, and regional SLA performance.

## SAMPLE DATA
Load scenarios with multi-practitioner paths, declined assignments, overdue escalations, and multilingual support interactions.

## DATA SOURCES
| Source | Use |
| --- | --- |
| practitioner directory and treatment mapping | assignment and reassignment logic |
| collaboration channel events | queue routing and transcript-linked operations |

## ACCEPTANCE USER
- [ ] An eligible case is assigned, reassigned when required, and escalated when SLA conditions are met.
- [ ] An assessor can process a collaboration request tied to the correct application record.

## ACCEPTANCE METADATA
- [ ] Assignment and escalation automations run deterministically under test scenarios.
- [ ] Manager dashboard surfaces overdue and escalated records with current ownership.
