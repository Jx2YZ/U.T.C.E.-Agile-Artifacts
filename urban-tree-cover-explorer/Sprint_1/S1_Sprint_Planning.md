# Sprint Planning (Sprint 1)

### 🛠️ Baseline User Story Example

**User Story:** As a registered user, I want to log into the system using my two-factor authentication so that I can access the interactive map, and identify suitable locations for PhD student meet-ups.

- **Estimated Story Points:** 34 
- **Rationale:** This task involves authentication logic, form validation, a map lookup, and a database lookup.  This means making it is quite complex.

### 🗺️ Teaching team access map

**User Story:** As a client teaching team member, I want a map to view Melbourne's tree coverage with detailed information so that I can identify suitable locations for meetups with PhD students.

- **Relative Complexity Comparison:**
  - This task involves customising a map plugin, including an additional data display through markers (e.g. containing locations, descriptions and categories).
  - Setting up the project environment and Wordpress integrations
  - Designing the map UI/UX
  - Importing and integrating the map dataset
  - Developing tree markers/indicators
  - Implementing a popup displaying tree details
- **Estimated Story Points:** 13
- **Rationale:** This story is less complex than the baseline story given it includes only part of the total complexity of this sprint (i.e. requiring introduction of a map visualising tree locations).  This requires management of an external dataset, rather than only development using Wordpress' plugins.

### _DEPRIORITISED_ 🔐 Teaching team secure their login with 2FA

---
# Sprint 1 Planning for Urban Tree Cover Explorer

## 🏆 Sprint Goal
Build the interactive map functionality, and implement 2FA for users logging in.

## ✅ Commitment
The team commits to completing the interactive map and authentication features by the end of this sprint.

## Selected User Stories
### User Story: 🗺️ Teaching team access map
As a teaching team member, I want a map to view Melbourne's tree coverage with detailed information so that I can identify suitable locations for meetups with PhD students.

### Acceptance Criteria:
- Tree data appears accurately on the map
- Users can interact with the map to move around the Melbourne area.
- Users can click on tree markers to see basic tree information.

### Estimation using Fibonacci Sequence
| Factor              | Consideration |
|---------------------|--------------|
| Complexity         | High - Integrating the City of Melbourne dataset in a visually accessible manner. |
| Uncertainty        | Moderate - The nature of the dataset, and Wordpress map systems is unknown. |
| Dependencies      | Medium - Relies on Wordpress map and database capabilities. |
| Risk              | High - This is core functionality. |
| Estimated Story Points | **5** (based on team discussion) |

### _DEPRIORITISED_ User Story: 🔐 Teaching team secure their login
As a teaching team member. I want the system to further verify my identification other then my user name and password, so that the risk of data leakage can be reduced.

### Acceptance Criteria:
- Users can register with an email and password, and turn on 2FA.
- User credentials are stored securely.
- Registered users can log in securely using their credentials, with the login validated by 2FA.

### Estimation using Fibonacci Sequence
| Factor              | Consideration |
|---------------------|--------------|
| Complexity         | Moderate - Needs 2FA integration and interaction with user dataset. |
| Uncertainty        | Low - 2FA is a common feature. |
| Dependencies      | High - Relies on Wordpress APIs to manage 2FA. |
| Risk              | High - This is core requested functionality and will impact security. |
| Estimated Story Points | **0** (CLIENT DEPRIORITISED) |

---

## 📋 Sprint Backlog Tasks
| Task | Assigned To | Estimated Hours |
|------|------------|----------------|
|Setting up the project environment and WordPress integration | QA Engineer | 4 |
|Designing map interface UI/UX for tree visualization| Dev A |2|
|Importing and integrating the City of Melbourne tree dataset| QA Engineer | 4|
|Development of tree markers/indicators on maps | Dev A | 5 |
|Implemented a popup that displays basic tree details when the marker is clicked. | Dev A | 5 |
|Creating the UI for the login | Jx2 | 4 |
|_DEPRIORITISED_ Examining the Plugin Options WordPress Uses for two Authentication| Jx2 | 4 |
|_DEPRIORITISED_ Install and configure the selected plug-in| QA Engineer | 4|
|_DEPRIORITISED_ Create user database document for plugin settings | Jx2 | 4|
|_DEPRIORITISED_ Testing the two Authentication Function| QA Engineer | 4 |
