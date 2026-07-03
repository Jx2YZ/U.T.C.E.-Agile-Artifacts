# 🚀 Risk Monitoring for Sprint 3 (Urban Tree Cover Explorer)    

In this project, risk management is integrated into the Scrum framework to ensure timely identification, tracking, and mitigation of risks throughout Sprints 1 and 2. The team uses Scrum ceremonies and Sprint Backlog risk stories to handle risks proactively.

---

## ✅ 1. Risk Monitoring Approach

| **Scrum Ceremony**        | **Risk Monitoring Strategy**                                                                                                                                     |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sprint Planning**       | High-priority risks (e.g. dataset compatibility, 2FA complexity) were reviewed. Where needed, mitigation tasks were converted into Sprint Backlog risk stories. |
| **Stand-Ups**       | The team checks if any identified risks have occurred, e.g., delays in dataset access or workflow bottlenecks. Mitigation efforts are discussed and implemented (and, where necessary, enhanced).        |
| **Sprint Review**         | Team reviews if risks have affected Sprint deliverables and documents any impacts (e.g., feature delays or technical trade-offs).  Team identifies any flow-on effects for future sprints                                |
| **Sprint Retrospective**  | Reflection on the effectiveness of risk responses and discussion of improvements for upcoming sprints. For example, better collaboration to reduce blockers.     |

---

## ⚠️ 2. Risk Stories in Sprint 3 Backlog

_This section draws on the risks identified in our Risk Management Guide, as applicable to Sprint 3._

### 📌 Risk Story – ID 101: Dataset Compatibility Delays

**Risk:** Compatibility issues with the urban tree dataset could delay testing of key features and overall project delivery.

**Risk Story:**
> As a development team, we want to review heat map, location routing and user-generate content capabilities in Wordpress and the WP GO Maps plugin to identify any issues in integrating these functions with the City of Melbourne datasets for this Sprint, so that we can clean/re-import any necessary data to support our mapping requirements.

**Acceptance Criteria:**
- Parks Dataset reviewed and evaluated by the end of week 1 of Sprint 3 (noting the Trees dataset has already been reviewed in Sprint 1 & 2).
- Mock dataset created if compatibility issues were detected.
- Mock dataset supports testing of the heatmap feature based on a separate map page, to avoid interfering with existing Increments.
- Sample page created to identify user-generated content functionality, and interplay with the WP GO Maps plugin.

**Backlog Details:**

| Field           | Description                          |
|----------------|--------------------------------------|
| **Priority**    | High                                |
| **Estimation**  | 8 Story Points                      |
| **Owner**       | Product Owner                    |
| **Dependencies**| Park dataset and WP GO Maps documentation|
| **Notes**       | Mock dataset should replicate realistic structure for continuity. |

---

### 📌 Risk Story – ID 102: Workflow Design & Dependencies

**Risk:** Poor workflow sequencing may result in delays and reduced QA/testing time, leading to implementation flaws.

**Risk Story:**
> As a development team, we want to assign interdependent tasks carefully and schedule collaboration sessions so that we maintain workflow integrity and ensure sufficient testing time.

**Acceptance Criteria:**
- All high-dependency tasks reviewed and sequenced during sprint planning.
- Developers assigned logically grouped tasks to minimise context switching (noting previous development experience during Sprint 1 and 2, while balancing the need for the team to work flexibly).
- At least two scheduled collaboration sessions for dependent tasks.

**Backlog Details:**

| Field           | Description                         |
|----------------|-------------------------------------|
| **Priority**    | Medium                               |
| **Estimation**  | 8 Story Points                     |
| **Owner**       | Scrum Master           |
| **Dependencies**| Sprint Backlog task structure      |
| **Notes**       | QA planning should begin once 80% of dependent tasks are implemented. |

---

### 📌 Risk Story – ID 104: Team Inexperience with Scrum

**Risk:** Lack of familiarity with Scrum may lead to unresolved blockers, preventing sprint completion.

**Risk Story:**
> As a Scrum team, we want to proactively resolve blockers and escalate major issues to the client so that we meet the definition of done.

**Acceptance Criteria:**
- All blockers identified during bi-weekly stand-ups.
- All major disputes resolved within 24 hours or escalated to client.
- Retrospective includes reflection on dispute resolution effectiveness.

**Backlog Details:**

| Field           | Description                          |
|----------------|--------------------------------------|
| **Priority**    | High                                |
| **Estimation**  | 5 Story Points                      |
| **Owner**       | Scrum Master                        |
| **Dependencies**| Communication Plan                  |
| **Notes**       | Team to document disputes and resolution time, where any arise. |

---

### 📌 Risk Story – ID 105: Client-Provided Technology Limitations

**Risk:** Limitations in the client’s chosen technology stack may prevent the final product from being rolled out, despite meeting project specifications (such as where the map plugin is incapable of search/filter capabilities, or login features are unavailable).

**Risk Story:**
> As a development team, we want to continuously engage with the client regarding their chosen technology stack so that the MVP is aligned with their expectations, and technical limitations are transparent.

**Acceptance Criteria:**
- Client limitations identified and documented/notified to the client by mid-sprint (or as soon as possible).
- MVP is functionally complete and aligns with client's provided tools and expectations.
- Any major limitations are highlighted in the Sprint Showcase for client consideration.

**Backlog Details:**

| Field           | Description                          |
|----------------|--------------------------------------|
| **Priority**    | Medium                              |
| **Estimation**  | 3 Story Points                      |
| **Owner**       | Product Owner / Scrum Master       |
| **Dependencies**| Client communication channels       |
| **Notes**       | Client will ultimately decide on MVP implementation feasibility. |

---

### 📌 Risk Story – ID 106: External Map Service Failure

**Risk:** If the external client's chosen map service cannot handle itinerary, heat map or user-generated content capabilities, then the client may not receive key functionality or acceptable performance, impacting project success.

**Risk Story:**
> As a development team, we want to review map service documentation relevant to route, heat map and user-generated content implementation, and plan fallbacks so that we can adapt if the external service fails to meet expectations.

**Acceptance Criteria:**
- Further map service documentation reviewed during the first half of the sprint.
- Any missing or incomplete functionality is identified and communicated in standups.
- The team logs any service limitations and provides alternatives or workarounds for the client where feasible.

**Backlog Details:**

| Field           | Description                          |
|----------------|--------------------------------------|
| **Priority**    | High                                 |
| **Estimation**  | 5 Story Points                      |
| **Owner**       | Frontend Developer                  |
| **Dependencies**| Access to external map service API and Wordpress user-generated content functionality  |
| **Notes**       | Document findings and escalate any blockers to the client as soon as possible in the sprint.|

---
### 📌 Risk Story – ID 107: Low quality user-generated content

**Risk:** If users produce low-quality user-generated content (including map markers and ratings), then the Product may not present useful information to accurately inform other users' decision making.

**Risk Story:**
> As a development team, we want to ensure we have clear constraints on the kind of information required when users create content (including specific pre-determined category tags, and limits on the length/size of other information to be provided), noting that the client does not have an appetite to moderate content at this stage.

**Acceptance Criteria:**
- The marker creation process is constraint to require certain data to create a marker in the first place (e.g. a valid location).
- The marker creation process is constrained to require specific fields of user-generated content (i.e. certain categories, description etc.) to somewhat limit erroneous content.

**Backlog Details:**

| Field           | Description                          |
|----------------|--------------------------------------|
| **Priority**    | Medium                                 |
| **Estimation**  | 3 Story Point                       |
| **Owner**       | Frontend Developer                  |
| **Dependencies**| WP Go Maps and Wordpress functionality to constraint shared content. |
| **Notes**       | Technical constraints will limit the scope for low quality content, noting the client will accept the risk of unmoderated content (for now). |

---
### 📌 Risk Story – ID 108: Marker Rating Failure

_**UPDATE: client deprioritised rating feature due to plugin issues.**_

**Risk:** If the Map fails to update the current user's rating, then the Product will not present the correct ratings for stops on the walking route, or markers on the Parks & Places of Interest map.

**Risk Story:**
> As a development team, we want to attempt to implement these features.  Where issues arise, we want to promptly contact the client to review the importance of this feature, and/or consider whether any issues can be raised with the relevant plugin developer directly for resolution.

**Acceptance Criteria:**
- Further map service documentation reviewed during the first half of the sprint.
- Any missing or incomplete functionality is identified and communicated in standups to consider workarounds.
- The team logs any service limitations and provides alternatives or workarounds for the client where feasible.

**Backlog Details:**

| Field           | Description                          |
|----------------|--------------------------------------|
| **Priority**    | Medium                                 |
| **Estimation**  | 3 Story Point                       |
| **Owner**       | Frontend Developer                  |
| **Dependencies**| WP Go Maps and Wordpress functionality to constraint shared content. |
| **Notes**       | Technical constraints will limit the scope for low quality content, noting the client will accept the risk of unmoderated content (for now). |

---

## 📈 3. Ongoing Risk Tracking Table (Sprint 3 Focus)

| **Risk ID** | **Summary**                                            | **Sprint 3 Relevance**     | **Risk Story Created?** |
|-------------|--------------------------------------------------------|-----------------------------|--------------------------|
| 101 | Parks data set and/or walking route incompatibility → Feature testing impacted    | High —  feature depends on data | ✅ Yes (also Tasks US6_T1 & US7_T3) |
| 102 | Workflow dependencies → QA bottlenecks | Medium — May arise mid-sprint | ❌ Planned for monitoring only, noting acceptable progress in Sprints 1 & 2|
| 104 | Scrum inexperience → Blockers unresolved | Medium — Monitored in daily stand-ups | ✅ Yes (tracked via stand-ups) |
| 105 | Client tech limitations → Unusable MVP | High — Reliant on client-identified login and map system/datasets | ✅ Yes (stories above, and backlog, rely on testing of selected features/capabilities and datasets) |
| 106 | External map failure → Incomplete feature | High - directly connected to dataset integration (ID 101) | ✅ Yes (also Tasks US6_T1 & US7_T3 & escalation to client)|
| 107 | Low quality user-generated content → Inaccurate information in Product | Medium - directly connected to Product quality, but risk accepted by client | ✅ Yes (also Task US6_T2)|
| 108 | Marker Rating Failure → Inaccurate stop ratings | Low - client deprioritised | ❌ Client deprioritised |

---

## 🛠 4. Summary of Mitigation in Sprint 3

- **Proactive Planning:** Three high-risk areas (ID 101, and ID 104 and ID 105 which are directly connected to Risk ID 101) were considered in Sprint 1 and Sprint 2. The development team will review compatibilities as a priority when completing Sprint Backlog tasks under task US6_T1 & US7_T4 (noting variations are likely between the Trees and Parks datasets).
- **Team Awareness:** Regular stand-ups ensure everyone is monitoring Risk 102 (workflow bottlenecks).
- **Preparedness:** Risk 104 is mitigated through early communication habits and escalation procedures.
- **Deprioritisation:** Risk 108 has been deprioritised by the client (noting third party software limitations), and will not affect this Sprint 3. Additionaly, Risk 103 has been deprioritised by the client, and will not affect this Sprint 3.  It is not reflected above on that basis.
- **Technical constraints:** Risk 106 is mitigated by clear technical constraints on user-generated content (i.e users can only implement certain marker categories, descriptions etc.), with the risk otherwise accepted by the client (noting moderation is not planned).
---
