# Risk Management Strategy :closed_book:

This document sets out our approach to managing key risks when developing the Urban Tree Cover Explorer (**UTCE**). We will use it to:

1. **Identify** risks proactively;
   
2. **Quantify** their impact; and
   
3. **Develop** a mitigation strategy to manage each risk.

---

## Identified Risks

### 📌 Risk ID: 101 

**Risk Statement:** 
"Delayed utilisation of urban tree dataset due to compatibility issues → Search and sort feature cannot be tested on time  -> Delay in project delivery"

- **Probability:** 30.0%  
- **Impact:** 8 (0-10 scale)  
- **Exposure:** 30.0% x 8 = **2.4**
- **Mitigation Strategy:** **Mitigate**
- **Mitigation Plan:** 
    - Review and evaluate dataset at the beginning of Sprint 1;
    - Create mock data for early testing (where feasible); and
    - Review any documentation provided by the developers of the urban tree cover dataset.

### 📌 Risk ID: 102
**Risk Statement:**
"Poor workflow design means prior task dependencies are incomplete/inaccurate at required times → Insufficient time for comprehensive quality assurance and testing → Product released with implementation flaws"

- **Probability:** 65.0%
- **Impact:** 8 (0-10 scale)
- **Exposure:** 80% x 8 = **6.4**
- **Mitigation Strategy:** **Mitigate**
- **Mitigation Plan:**
    - Set fixed deadlines for individual tasks; 
    - Tasks that form a logical sequence should be assigned to a single team member when possible (subject to QA); and
    - Developers can schedule joint collaboration sessions for interdependent tasks with tight deadlines.

### 📌 Risk ID: 103
**Risk Statement:**
"Inefficient implementation of two factor authentication for logins → Delay in development schedule → Less time for other feature development"

- **Probability:** 90.0%
- **Impact:** 9 (0-10 scale)
- **Exposure:** 90% x 9 = **8.1**
- **Mitigation Strategy:** **Avoid**
- **Mitigation Plan:**
    - The client has deprioritised this feature due to plugin issues and integration with their broader environment.

### 📌 Risk ID: 104
**Risk Statement:**
"The development team is inexperienced in scrum development processes and dispute resolution → a number of blockers arise, and cannot be rectified → The team fails to meet the 'definition of done' at the end of the sprint."

- **Probability:** 90.0%
- **Impact:** 9 (0-10 scale)
- **Exposure:** 90% x 9 = **8.1**
- **Mitigation Strategy:** **Avoid**
- **Mitigation Plan:**
    - The team must actively communicate in accordance with the Communication Plan to identify blockers early, and work to resolve disputes promptly; and 
    - Large disputes as to desired implementation must be escalated to the client promptly to ensure the project is not delayed while awaiting client instructions.

### 📌 Risk ID: 105
**Risk Statement:**
"The development team relies on client-provided technology → There are limitations due to the technology, meaning the product is not readily able to be rolled out → the client has access to a MVP that meets their specifications, but may not wish to implement the product in practice due to these limitations."

- **Probability:** 40.0%
- **Impact:** 5 (0-10 scale)
- **Exposure:** 40% x 5 = **2**
- **Mitigation Strategy:** **Accept**
- **Mitigation Plan:**
    - The team will continuously communicate with the client to identify limitations of the client's chosen approach; and
    - The MVP will be delivered to spec.  It will be for the client to decide if it then wishes to implement the MVP in practice, notwithstanding any such limitations.

### 📌 Risk ID: 106
**Risk Statement:**
"The external map service fails to identify required information → Required data cannot be displayed, and the client cannot receive the information it requires → The project fails to meet the 'definition of done'."

- **Probability:** 5.0%
- **Impact:** 10 (0-10 scale)
- **Exposure:** 5% x 10 = **0.5**
- **Mitigation Strategy:** **Accept**
- **Mitigation Plan:**
    - The team will review all available documentation for the external map service; and
    - Where feasible, the team will promptly document and work to mitigate limitations of the external map service.

### 📌 Risk ID: 107
**Risk Statement:**
"Users produce low quality user-generated content when adding Park or Place of Interest markets, or ratings → the content does not accurately reflect the reality of a Park or Place of Interest → The Product does not present useful information to support accurate decision making about ideal Parks or Places of Interest."

- **Probability:** 60.0%
- **Impact:** 10 (0-10 scale)
- **Exposure:** 60% x 10 = **6**
- **Mitigation Strategy:** **Accept**
- **Mitigation Plan:**
    - The client has not identified an appetite to moderate content;
    - User-generate content will be permitted to be generated freely for now, subject to clear constraints as to required information;
    - The client may elect to revisit this process in future.

### 📌 Risk ID: 108
**Risk Statement:**
"The external map service fails to allow users to submit ratings for pre-defined or user-generated markers → the content does not reflect any ratings _or_ does not reflect accurate ratings for a Park or Place of Interest, or walking route location → The Product does not present useful information to support accurate decision making about ideal Parks or Places of Interest, or walking route locations."

- **Probability:** 60.0%
- **Impact:** 10 (0-10 scale)
- **Exposure:** 60% x 10 = **6**
- **Mitigation Strategy:** UPDATE: **Avoid**
- **Mitigation Plan:**
    - The client has confirmed this feature should be deprioritised due to plugin issues;
    - The client may elect to revisit this process in future.

---

## 📌 **Ongoing Risk Tracking**  

| **Risk ID** | **Risk Statement (Summary)**                     | **Probability (%)** | **Impact (0-10)** | **Exposure** | **Mitigation Strategy** |
|------------|--------------------------------------------------|---------------------|------------------|-------------|---------------------|
| 101        | Delayed utilisation of urban tree dataset due to compatibility issues | 30.00%               | 8                | 2.4         | Mitigate 🟡         |
| 102 | Poor workflow design which subsequent tasks are dependent upon prior task completion by other team members  | 80.00% | 8 | 6.4 | Mitigate 🟡  |
| 103 | Inefficient implementation of two factor authentication logins  | 90.00% | 9 | 8.1 | Avoid 🔴 (Deprioritised) |
| 104 | Team inexperienced with scrum development and dispute resolution  | 90.00% | 9 | 8.1 | Avoid 🔴  |
| 105 | Development team relied on client-provided technology | 40.00% | 5 | 2 | Accept 🟢  |
| 106 | External Map Service Failure | 5% | 10 | 0.5 | Accept 🟢 |
| 107 | Low-quality user generated content | 60% | 10 | 6 | Accept 🟢 |
| 108 | Marker raiting failure | 60% | 10 | 6 | Avoid 🔴 (Deprioritised)|

## 📌 **Legend for Mitigation Strategies**  

- **Accept** 🟢 → Acknowledge the risk but take no preventive action.  
- **Ignore** 🔵 → Considered low priority with minimal impact.  
- **Mitigate** 🟡 → Take action to reduce probability or impact.  
- **Avoid** 🔴 → Change project approach to eliminate the risk.  
