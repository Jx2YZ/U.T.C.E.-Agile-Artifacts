# Sprint Planning (Sprint 2)

### 🛠️ Baseline User Story Example

**User Story:** As a registered user, I want to log into the system using my registered account so that I can access the interactive map, and identify suitable locations for PhD student meet-ups.

- **Estimated Story Points:** 34 (based on Fibonacci sequence)
- **Rationale:** This task involves authentication logic, form validation, a map lookup, and a database lookup.  This means making it is quite complex.  However, much of this work is already complete, downgrading the estimated story points for this baseline user story in this sprint.

### 🔎 Teaching team search and filter by distance map

**User Story:** As a client teaching team member, I want to search for trees around a certain location on the map, so that I can quickly find the perfect location that meets my requirements.

- **Relative Complexity Comparison:**
  - Building off a base map created in Sprint 1, this task involves further configuring to the WP Go Map plugin, including an additional data display through search results, and hiding of markets irrelevant to search criteria;
  - Enabling and configuring UI components for search input (e.g. form, including location and search radius from location); and
  - Additional components are required for displaying search results.
- **Estimated Story Points:** 8 (based on Fibonacci sequence)
- **Rationale:** This story is less complex than the baseline story given it includes only part of the total complexity of this sprint (i.e. requiring introduction of search capabilities on a previously implemented map).  This does however require more configurations on WP GO Map plugin.

### 🗺️ Teaching team search and filter by genus, age description and location map

**User Story:**  As a client teaching team member, I want to filter through trees around a certain location on the map based on available criteria, so that I can quickly find the perfect location that meets my requirements.

- **Relative Complexity Comparison:**
  - Building off a base map created in Sprint 1, this task involves further customising a map plugin, including an additional data display through filtered results, and hiding of markets irrelevant to filter criteria.
  - Review the City of Melbourne dataset for Wordpress filter compatibility, and clean dataset as required;
  - Enabling and configuring a UI component to enable filtering results based on location, genus and age; and
  - Designing a results list, displaying tree details meeting filter criteria.
- **Estimated Story Points:** 21 (based on Fibonacci sequence)
- **Rationale:** This story is less complex than the baseline story given it includes only part of the total complexity of this sprint (i.e. requiring introduction of filtering capabilities on a previously implemented map).  This does however require management of search/filter variables pre-determined by an external dataset, rather than only development using Wordpress' plugins.


### 🔐 Teaching team secure their access with an email and password

**User Story:** As a client teaching team member, I want to securely access the Urban Tree Cover Explorer application using my username/email and password, so that the risk of data leakage can be reduced.

- **Relative Complexity Comparison:**
  - This task involves adding an additional layer of security to the Product, including managing a user database and validating credentials.
  - Implement a login form, with a customised UI;
  - Configure an authentication controller to process login requests, based on registered user information;
  - Create a redirect mechanism for unauthorised access; and
  - Design and implement error messaging for failed logins.
- **Estimated Story Points:** 5 (based on Fibonacci sequence)
- **Rationale:** This story is less complex than the baseline story given it relates to only part of the whole intended user story for this Sprint.  Comparatively, the introduction of a login feature should be less complex than introducing the entire map functionality, in particular given Wordpress provides a built-in login function.  However, we estimate complexity in ensuring this technology is integrated appropriately, in particular ensuring that redirect end error messaging behaves as expected.

---
# Sprint 2 Planning for Urban Tree Cover Explorer

## 🏆 Sprint Goal
Build search and filter functionality in the interactive map, and implement a secure login process.

## ✅ Commitment
The team commits to completing the map search and filter capabilities and login feature by the end of this sprint.

# Selected User Stories
### User Story: 🔎 Teaching team search and filter by distance map
As a client teaching team member, I want to search for trees around a certain location on the map, so that I can quickly find the perfect location that meets my requirements.

### Acceptance Criteria:
- Tree data appears accurately on the map, as per Sprint 1;
- Users can enter a search location;
- Once users enter a search location, the map will only display results matching that criterion, within a selected given radius of their location;
- Tree markers not meeting the selected search location/radius criteria are no longer displayed on the map;
- The map defaults to use Melbourne Connect as the search location, with a default search radius of 1km;
- Details of all search results are diplayed below the map, on successive pages of 10 results based on proximity to the search location; and
- The map uses kilometre units

### Estimation (using Fibonacci sequence)
| Factor              | Consideration |
|---------------------|--------------|
| Complexity         | Moderate - Need to enable searching feature and configure other map setting. |
| Uncertainty        | Medium - The team now understands the nature of the City of Melbourne dataset, yet the functionality of WP Go Map is not yet fully explored. |
| Dependencies      | Medium - Relies on WP Go Map plugin and database capabilities, with these capabilities generally being quite limited. |
| Risk              | Medium - Technical considerations |
| Estimated Story Points | **8** (based on team discussion) |


## Selected User Stories
### User Story: 🗺️ Teaching team search and filter by genus, age description and location map
As a client teaching team member, I want to filter through trees around a certain location on the map based on available criteria, so that I can quickly find the perfect location that meets my requirements.

### Acceptance Criteria:
- Tree data appears accurately on the map as per Sprint 1;
- Users can enter filter criteria, based on the location, distance from the location, and genus and age of a tree (being features in the City of Melbourne dataset);
- Once users enter filter criteria, the map will only display results matching those criteria;
- Tree markers not meeting the selected filter criteria are no longer displayed on the map;
- The default filter values of location = Lincoln Square, Distance = 1km, Genus = Ficus, and Location_In = Park;
- Trees of a different genus must be different colours for visbility. Trees of the same genus must be the same colour; and
- The map must use kilometre units.

### Estimation (using Fibonacci sequence)
| Factor              | Consideration |
|---------------------|--------------|
| Complexity         | Moderate - Introducing search logic based on a user's current location. |
| Uncertainty        | Medium - The team now understands the nature of the City of Melbourne dataset, yet the functionality of WP Go Map is not yet fully explored. |
| Dependencies      | Medium - Relies on Wordpress map and database capabilities, with these capabilities generally being quite limited. |
| Risk              | High - This is core functionality. |
| Estimated Story Points | **21** (based on team discussion) |

### User Story: 🔐 Teaching team secure their access with an email and password

**User Story:** As a client teaching team member, I want to securely access the Urban Tree Cover Explorer application using my username/email and password, so that the risk of data leakage can be reduced. 

### Acceptance Criteria:
- User credentials are stored securely;
- Registered users can log in securely using their credentials, via a visually appealing login form;
- Users with incorrect login details receive an error message;
- Users who are not logged in are redirected to the login page; and
- The login page must, at a minimum, have a username/password form.

### Estimation (using Fibonacci sequence)
| Factor              | Consideration |
|---------------------|--------------|
| Complexity         | Moderate - Needs user database integration. |
| Uncertainty        | Moderate - Login systems are a common feature.  However, Wordpress' login functionality is not well understood by the team. |
| Dependencies      | High - Relies on Wordpress login APIs, forms and systems. |
| Risk              | High - This is core requested functionality and will impact security. |
| Estimated Story Points | **5** (based on team discussion) |

---

## 📋 Sprint Backlog Tasks
| Task | Assigned To | Estimated Hours |
|------|------------|----------------|
|Create an Input component for the user to search for trees within a selected radius of their chosen location.| Dev A | 1 |
|Show a list of results within the selected location radius under the map	| Dev A |1|
|Use kilometre units for the search radius options| Dev A |1|
|Search trees within 1 KM of the search location by default| Dev A |1|
|Set Melbourne Connect as default location for search| Dev A |2|
|Review City of Melbourne dataset for Wordpress filter compatibility, and clean dataset as required.| Product Owner |3|
|Enable and configure a UI component to enable filtering results based on a selected location, distance from that location, an genus and age of tree (based on dataset features).| Product Owner  |8|
|Set up a default filter value of location = Lincoln Square, Distance = 1km, Genus = Ficus, Location_In = Park.| Product Owner  |8|
|	Change the marker colours such that different genus have different colours.| Product Owner |2|
|Implement login form UI.| Jx2 |2|
|Implement an authentication controller for processing login requests.| Jx2 |1|
|Create a redirect mechanism for unauthorised access.| Jx2 |1|
|Design and implement error messaging for failed logins.| Jx2 |1|

