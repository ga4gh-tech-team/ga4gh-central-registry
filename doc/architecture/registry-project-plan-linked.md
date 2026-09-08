# GA4GH Registry Project Plan - Plenary 2026 (Singapore)

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
| Target Completion | 25 September 2026 |
| Current Phase | <ul><li>- [x] Requirements gathering </li><li>- [x] Initial development </li><li>- [x] Demo and validation </li><li>- [ ] Initial release </li><li>- [ ] Enhancements </li></ul> |

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
| API Layer | System integration | Java, Spring Boot|
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


### M2 — Initial demo of the revamped/redesigned registry 

#### Objective

Demonstrate the NIF member workflows (without login) operational. Personal profile, search and view fellow NIF members demonstrated 

#### Event

**28 August 2026**

#### Personas Served

- NIF members

#### Use Cases Included

| Use Case |
|-----------|
| UC-04 People collaboration/discovery (NIF member) |

#### Deliverables

| Deliverable | Status |
|-------------|---------|
| Demo to the stakeholders | Done |


#### Acceptance Criteria

- All the features for the NIF member collaboration/discovery is demonstrated.
- The meeting summary document is used to update the requirements and create issues where the requirements have been updated.
- Review feedback accepted and updated in the design.

#### Dependencies

| Dependency | Owner |
|------------|--------|
| Availability | All project team members |


---

## 7. Agile Delivery Mapping

| Milestone | Sprint | Planned Outcome |
|------------|---------|-----------------|
| M1 | Sprint 62 | Requirements validation workshop. Requirements discussed and understood. Summary of changes shared for review. |
| M1, M3 | Sprint 63 | Summary of changes - complete review. Authentication and authorisation design - Passport visa types. Internal discussion and formalise outcome. |
| M2, M3 | Sprint 64, 65 | Evaluate and finalise code to be reused from implementation registry. Start development to handle |
| M2 | Sprint 66 | Demonstration |
| M4 | Sprint 67 | Plenary prep including screenshots, and poster |

---

## 8. Traceability Matrix

| Use Case | Persona | Milestone | Issues/PRs |
|-----------|----------|-----------|------------|
| UC-01 | Researcher | M1 | [#24](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/24), [#16](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/16), [#20](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/20) |
| UC-02 | Data Steward | M2 | [#14](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/14) |
| UC-03 | Developer | M1 | [#16](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/16), [#17](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/17), [#19](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/19), [#20](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/20), [#23](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/23) |
| UC-04 | Administrator | M2 | [#11](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/11) |

---





---

## 9. Related GitHub Issues


### Epics

- [#2](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/2) Epic: Standards
  - [#8](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/8) User Story: discover GA4GH standards
    - [#16](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/16) Feature: /api/standards endpoint
- [#3](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/3) Epic: Organisations
  - [#9](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/9) User Story: discover organisations
    - [#17](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/17) Feature: /api/organisations endpoint
- [#4](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/4) Epic: Schemas
  - [#10](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/10) User Story: discover schemas
    - [#18](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/18) Spike: scope /api/schemas requirements
- [#5](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/5) Epic: People
  - [#11](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/11) User Story: NIF member search/view
  - [#12](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/12) User Story: community member collaboration
- [#6](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/6) Epic: Implementations
  - [#13](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/13) User Story: discover deployments/services
    - [#19](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/19) Feature: /api/deployments endpoint
    - [#20](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/20) Feature: /api/services endpoint
  - [#14](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/14) User Story: register datasets/implementations
- [#7](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/7) Epic: Authentication & Authorisation (cross-cutting)
  - [#15](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/15) User Story: login & manage own data
    - [#21](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/21) Feature: Passport integration & login flow
    - [#22](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/22) Spike: Passport visa types

### Standalone / cross-cutting

- [#23](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/23) Feature: /api/service-info endpoint
- [#24](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/24) Feature: unified cross-component discovery UI

### Milestone tracking

- [#25](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/25) Write M2 milestone detail section
- [#26](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/26) Write M3 milestone detail section
- [#27](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/27) Write M4 milestone detail section

### Documentation / process gaps

- [#28](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/28) Set project Target Completion date
- [#29](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/29) Reconcile sprint numbering inconsistency
- [#30](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/30) Replace placeholder GH Issues entries in Traceability Matrix
- [#31](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/31) Fix 'Sprint Boot' typo in Core Components table

### Open questions

- [#32](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/32) Confirm Attio as Metadata Service / Reporting Service backend
- [#33](https://github.com/ga4gh-tech-team/ga4gh-central-registry/issues/33) Scope 'Federated capabilities' (Sprint 5-12, M2)
