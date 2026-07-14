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
| Current Phase | <ul><li>- [x] Requirements gathering </li><li>- [ ] Initial development </li><li>- [ ] Demo and validation </li><li>- [ ] Initial release </li><li>- [ ] Enhancements </li></ul> |

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
| M3 | 18 Sep 2026 | Authentication and authorisation for login | All personas | UC-01 to UC-04, UC-06 | All workflows are operational - public view, login, edit/submit data/profile, search members |
| M4 | TBD | Future milestone | TBD | TBD | TBD |

---

## 6. Milestone Detail Pages

### M1 — Initial Discovery Demonstration

#### Objective

Demonstrate a usable discovery experience and API access.

#### Event

**15 September 2026**

#### Personas Served

- Researcher
- Developer

#### Use Cases Included

| Use Case |
|-----------|
| UC-01 Discover datasets |
| UC-03 Retrieve metadata |

#### Deliverables

| Deliverable | Status |
|-------------|---------|
| Search API | |
| Discovery UI | |
| Metadata service | |

#### Acceptance Criteria

- Search returns expected results.
- Metadata accessible through API.
- Demonstration completed with stakeholders.

#### Dependencies

| Dependency | Owner |
|------------|--------|
| Metadata model | |
| Infrastructure | |
| Authentication | |

#### Risks

| Risk | Mitigation |
|--------|-------------|
| Delayed API development | Reduce scope for demonstration |
| Metadata inconsistencies | Validation process |

---

### M2 — Federated Collaboration Release

#### Objective

Support cross-organisational collaboration workflows.

#### Event

**April 2027**

#### Personas Served

- Researcher
- Data Steward
- Developer
- Administrator

#### Use Cases Included

- UC-01
- UC-02
- UC-03
- UC-04

#### Success Criteria

- Federated workflows demonstrated.
- Multiple organisations participating.
- Governance reporting available.

---

## 7. Agile Delivery Mapping

| Milestone | Sprint | Planned Outcome |
|------------|---------|-----------------|
| M1 | Sprint 1 | Architecture established |
| M1 | Sprint 2 | Search API MVP |
| M1 | Sprint 3 | Metadata retrieval |
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
