# 🚀 Risk Monitoring for Sprint 1 (Urban Tree Cover Explorer)    

In this project, risk management is integrated into the Scrum framework to ensure timely identification, tracking, and mitigation of risks throughout Sprint 1. The team uses Scrum ceremonies and Sprint Backlog risk stories to handle risks proactively.

---

## ✅ 1. Risk Monitoring Approach

| **Scrum Ceremony**        | **Risk Monitoring Strategy**                                                                                                                                     |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sprint Planning**       | High-priority risks (e.g. dataset compatibility, 2FA complexity) were reviewed. Where needed, mitigation tasks were converted into Sprint Backlog risk stories. |
| **Stand-Ups**       | The team checks if any identified risks have occurred, e.g., delays in dataset access or workflow bottlenecks. Mitigation efforts are discussed and implemented (and, where necessary, enhanced).        |
| **Sprint Review**         | Team reviews if risks have affected Sprint deliverables and documents any impacts (e.g., feature delays or technical trade-offs).  Team identifies any flow-on effects for future sprints.                                |
| **Sprint Retrospective**  | Reflection on the effectiveness of risk responses and discussion of improvements for upcoming sprints. For example, better collaboration to reduce blockers.     |

---

## ⚠️ 2. Risk Stories in Sprint 1 Backlog

_This section draws on the risks identified in our Risk Management Guide, as applicable to Spring 1._

### 📌 Risk Story – ID 101: Dataset Compatibility Delays

**Risk:** Compatibility issues with the urban tree dataset could delay testing of key features and overall project delivery.

**Risk Story:**
> As a development team, we want to create mock data and evaluate dataset compatibility early so that we can test core features without being blocked by external data delays.

**Acceptance Criteria:**
- Dataset reviewed and evaluated by Day 2 of Sprint 1.
- Mock dataset created if compatibility issues are detected.
- Mock dataset supports testing of the search and sort feature.

**Backlog Details:**

| Field           | Description                          |
|----------------|--------------------------------------|
| **Priority**    | High                                |
| **Estimation**  | 3 Story Points                      |
| **Owner**       | Backend Developer                   |
| **Dependencies**| Urban tree dataset documentation    |
| **Notes**       | Mock dataset should replicate realistic structure for continuity. |

---

### 📌 Risk Story – ID 102: Workflow Design & Dependencies

**Risk:** Poor workflow sequencing may result in delays and reduced QA/testing time, leading to implementation flaws.

**Risk Story:**
> As a development team, we want to assign interdependent tasks carefully and schedule collaboration sessions so that we maintain workflow integrity and ensure sufficient testing time.

**Acceptance Criteria:**
- All high-dependency tasks reviewed and sequenced during sprint planning.
- Developers assigned logically grouped tasks to minimize context switching.
- At least two scheduled collaboration sessions for dependent tasks.

**Backlog Details:**

| Field           | Description                         |
|----------------|-------------------------------------|
| **Priority**    | High                               |
| **Estimation**  | 3 Story Points                     |
| **Owner**       | Scrum Master & Tech Lead           |
| **Dependencies**| Sprint Backlog task structure      |
| **Notes**       | QA planning should begin once 80% of dependent tasks are implemented. |

---

### 📌 Risk Story – ID 103: Inefficient 2FA Implementation (DEPRIORITISED)

**Risk:** Inefficient implementation of two-factor authentication may delay development and reduce time for other features.

**Risk Story:**
> As a development team, we want an experienced developer to implement 2FA and consult WordPress documentation so that we avoid schedule delays and ensure secure login functionality.

**Acceptance Criteria:**
- 2FA functionality implemented using WordPress-compliant methods.
- Code reviewed by at least one other team member.
- 2FA feature tested and verified before end of sprint.

**Backlog Details:**

| Field           | Description                          |
|----------------|--------------------------------------|
| **Priority**    | High                                |
| **Estimation**  | 5 Story Points                      |
| **Owner**       | Backend Developer                   |
| **Dependencies**| WordPress Plugin Documentation      |
| **Notes**       | Implementation should be reusable for future feature enhancements. |

---

### 📌 Risk Story – ID 104: Team Inexperience with Scrum

**Risk:** Lack of familiarity with Scrum may lead to unresolved blockers, preventing sprint completion.

**Risk Story:**
> As a Scrum team, we want to proactively resolve blockers and escalate major issues to the client so that we meet the definition of done.

**Acceptance Criteria:**
- All blockers identified during daily stand-ups.
- All major disputes resolved within 24 hours or escalated to client.
- Retrospective includes reflection on dispute resolution effectiveness.

**Backlog Details:**

| Field           | Description                          |
|----------------|--------------------------------------|
| **Priority**    | High                                |
| **Estimation**  | 3 Story Points                      |
| **Owner**       | Scrum Master                        |
| **Dependencies**| Communication Plan                  |
| **Notes**       | Team to document disputes and resolution time. |

---

### 📌 Risk Story – ID 105: Client-Provided Technology Limitations

**Risk:** Limitations in the client’s chosen technology stack may prevent the final product from being rolled out, despite meeting project specifications.

**Risk Story:**
> As a development team, we want to continuously engage with the client regarding their chosen technology stack so that the MVP is aligned with their expectations and technical limitations are transparent.

**Acceptance Criteria:**
- Client limitations identified and documented by mid-sprint.
- MVP is functionally complete and aligns with client's provided tools and expectations.
- Any major limitations are highlighted in the Sprint Review for client consideration.

**Backlog Details:**

| Field           | Description                          |
|----------------|--------------------------------------|
| **Priority**    | Medium                              |
| **Estimation**  | 2 Story Points                      |
| **Owner**       | Client Liaison / Scrum Master       |
| **Dependencies**| Client communication channels       |
| **Notes**       | Client will ultimately decide on MVP implementation feasibility. |

---

### 📌 Risk Story – ID 106: External Map Service Failure

**Risk:** If the external map service cannot provide required data, the client may not receive key functionality or acceptable performance, impacting project success.

**Risk Story:**
> As a development team, we want to review map service documentation and plan fallbacks so that we can adapt if the external service fails to meet expectations.

**Acceptance Criteria:**
- Map service documentation reviewed during the first half of the sprint.
- Any missing or incomplete data sources identified and communicated in sprint planning or reviews.
- Team logs any service limitations and provides alternatives or workarounds where feasible.

**Backlog Details:**

| Field           | Description                          |
|----------------|--------------------------------------|
| **Priority**    | Low                                 |
| **Estimation**  | 1 Story Point                       |
| **Owner**       | Frontend Developer                  |
| **Dependencies**| Access to external map service API  |
| **Notes**       | Document findings and escalate any blockers early in sprint. |

---

## 📈 3. Ongoing Risk Tracking Table (Sprint 1 Focus)

| **Risk ID** | **Summary**                                            | **Sprint 1 Relevance**     | **Risk Story Created?** |
|-------------|--------------------------------------------------------|-----------------------------|--------------------------|
| 101         | Urban tree dataset delay → Feature testing impacted    | High — Search feature depends on data | ✅ Yes (Mock dataset story) |
| 102         | Workflow dependencies → QA bottlenecks                 | Medium — May arise mid-sprint         | ❌ Planned for monitoring only |
| 103         | Complex 2FA → Dev schedule impact                      | Low — Client deprioritised            | ✅ Yes (Evaluate WordPress 2FA) |
| 104         | Scrum inexperience → Blockers unresolved               | Medium — Monitored in daily stand-ups | ❌ No (tracked via retrospective) |
| 105         | Client tech limitations → Unusable MVP                | High — Reliant on client-identified 2FA system and map dataset        | ✅ Yes (both stories above rely on testing of selected features/capabilities)                       |
| 106         | External map failure → Incomplete feature              | High - directly connected to dataset integration (ID 101)          | ✅ Yes (Mock dataset story)                        |

---

## 🛠 4. Summary of Mitigation in Sprint 1

- **Proactive Planning:** Four high-risk areas (ID 101 and ID 103, which both affect ID 105; ID 106 directly connected to ID 101) were translated into Sprint Backlog items.
- **Team Awareness:** Regular stand-ups ensure everyone is monitoring Risk 102 (workflow bottlenecks).
- **Preparedness:** Risk 104 is mitigated through early communication habits and escalation procedures.
- **Deprioritisation:** Risk 103 has been deprioritised by the client (noting third party software limitations), and will not affect this Sprint 1.
---
