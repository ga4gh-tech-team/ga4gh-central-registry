# GA4GH Registry Project Plan Template

## 1. Project Overview

| Item | Description |
|----------|-------------|
| Project Name | GA4GH Registry |
| Vision | Centralise the registries from GA4GH into a single registry holding standards (specs), implementations, organisations, and people |
| Sponsor(s) | Sasha Siegel (GA4GH Chief Product Officer) |
| Product Owner(s) | Jimmy Payyappilly |
| Delivery Lead(s) | Jimmy Payyappilly |
| Technical Lead(s) | Jimmy Payyappilly |
| Start Date | 20 May 2026 |
| Target Completion | |
| Current Phase | <ul><li>- [x] Requirements gathering </li><li>- [x] Initial development </li><li>- [ ] Demo and validation </li><li>- [ ] Initial release </li><li>- [ ] Enhancements </li></ul> |

---

## 2. Stakeholder & Persona Map

| Persona | Role | Goals |
|----------|------|---------|
| Collaborator | Data consumer | Discover standards (specs), implementations, schemas, organisations and people |
| Collaborator | Data provider | Register datasets |
| NIF member | Data consumer | Discover standards (specs), implementations, schemas, organisations and NIF members |
| Administrator | Governance | Monitor data validity. Design enhancements |
| GA4GH Secretariat | Data consumer, governance | Track adoption. Data validation |

---

## 3. Solution Landscape

### Core Components

| Component | Purpose | System/technology |
|------------|----------|---------|
| Portal/UI | User interaction | React UI |
| API Layer | System integration | Java, Sprint Boot|
| Authentication | Identity & access | GA4GH Passport |
| Metadata Service | Discovery | Attio |
| Reporting Service | Analytics | Attio |

### Key Endpoints

| Endpoint | Description | Consumer |
|-----------|-------------|------------|
| `/api/service-info` | The implementation of the GA4GH [Service Info spec](https://github.com/ga4gh/ga4gh-service-info). | Researchers |
| `/api/organisations` | All the organisations with implementations registered in the registry. | Researchers, (web) Applications/programs |
| `/api/deployments` | Any codebase that works with one or more GA4GH standards. | Data Stewards, Researchers, (web) Applications/programs |
| `/api/services` | A running web server serving genomic data according to a GA4GH API specification. | Data Stewards, Researchers, (web) Applications/programs |
| `/api/standards` | GA4GH standards (specification). | Data Stewards, Researchers, (web) Applications/programs |

---

## 4. Use Case Catalogue

| ID | Use Case | Primary Persona | Priority |
|----|-----------|----------------|----------|
| UC-01 | Discover data | Collaborator/public | High |
| UC-02 | Submit data | Collaborator/Data Steward | High |
| UC-03 | Retrieve metadata through API | Collaborator/public | High |
| UC-04 | People collaboration/discovery | NIF member | High | 
| UC-05 | People collaboration/discovery | Collaborator/Community member | Medium |
| UC-06 | Authentication and authorisation | All | High |

---

## 5. Milestone Roadmap (Primary View)

| Milestone | Date | Event/Outcome | Personas Impacted | Key Use Cases | Success Criteria |
|------------|--------|----------------|-------------------|---------------|------------------|
| M1 | 24 July 2026 | NIF member collaboration/discovery initial requirements gathering | NIF member | UC-01, UC-02, UC-04 | Finalise the collaboration/discovery requirements |
| M2 | 26 Aug 2026 | Initial demo of the revamped/redesigned registry | All personas | UC-01 to UC-04 | NIF member workflows (without login) operational. Personal profile, search and view fellow NIF members demonstrated |
| M3 | 18 Sep 2026 | Authentication and authorisation for login | All personas | UC-01 to UC-04, UC-06 | Following workflows are operational - public view, login; for NIF member: edit/submit data/profile, search members |
| M4 | 28 Sep 2026 | Plenary | All personas | UC-01 to UC-04, UC-06 | Demo version with NIF member workflows operational |

---

## 6. Milestone Details

### M1 — NIF member collaboration/discovery initial requirements gathering 

#### Objective

Capture the clarifications and decisions made during the requirements validation session, incorporating feedback on the initial requirements. 

#### Event

**2 July 2026**

#### Personas Served

- Collaborator
- Administrator
- GA4GH Secretariat

#### Use Cases Included

| Use Case |
|-----------|
| UC-04 People collaboration/discovery (NIF member) |
| UC-06 Authentication and authorisation |

#### Deliverables

| Deliverable | Status |
|-------------|---------|
| Requirements validation workshop summary | Done |


#### Acceptance Criteria

- All the requirements on the NIF member collaboration/discovery is discussed and recorded in a document.
- The record (summary) document shared with stakeholders for review.
- Review feedback accepted and updated in design.

#### Dependencies

| Dependency | Owner |
|------------|--------|
| Availability | All project team members |

#### Risks

| Risk | Mitigation |
|--------|-------------|
|  |  |
|  |  |


---

## 7. Agile Delivery Mapping

| Milestone | Sprint | Planned Outcome |
|------------|---------|-----------------|
| M1 | Sprint 62 | Requirements validation workshop. Requirements discussed and understood. Summary of changes shared for review. |
| M1, M3 | Sprint 63 | Summary of changes - complete review. Authentication and authorisation design - Passport visa types. Internal discussion and formalise outcome. |
| M2, M3 | Sprint 64 | Evaluate and finalise code to be reused from implementation registry. Start development to handle |
| M1 | Sprint 4 | Demonstration preparation |
| M2 | Sprint 5-12 | Federated capabilities |

---

## 8. Traceability Matrix

| Use Case | Persona | Endpoint | Milestone | Issues/PRs |
|-----------|----------|-----------|------------|-------------|
| UC-01 | Researcher | `/search` | M1 | GH Issues |
| UC-02 | Data Steward | `/submit` | M2 | GH Issues |
| UC-03 | Developer | `/metadata` | M1 | GH Issues |
| UC-04 | Administrator | `/reporting` | M2 | GH Issues |

---

## 9. Progress Dashboard

| Metric | Current | Target |
|----------|---------|----------|
| Milestones completed | | |
| Use cases delivered | | |
| Open issues | | |
| Closed issues | | |
| Participating organisations | | |

---

## Recommended Visual Structure

```text
Personas
    ↓
Use Cases
    ↓
Capabilities
    ↓
Endpoints / Components
    ↓
Milestones (Events)
    ↓
Sprint Delivery
```

This structure keeps stakeholders focused on outcomes and milestones while allowing delivery teams to trace work down to epics, issues, pull requests, releases, and sprint activities.
