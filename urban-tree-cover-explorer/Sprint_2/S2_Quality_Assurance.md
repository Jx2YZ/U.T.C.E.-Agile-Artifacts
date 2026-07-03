# 🚀 Quality Assurance Strategy

This document set out our **Quality Assurance (QA) Strategy** for the Sprint 2 of **Urban Tree Cover Explorer** project.

It documents the status of testing activities we have planned for this sprint, helping us ensure each sprint delivers a **fully functional and thoroughly tested feature**.

---

## 🏆 Definition of Done (DoD)

A feature is considered **Done** only when:  
1. All test cases for the feature pass successfully.  
2. The feature meets its **Acceptance Criteria**.  
3. Bugs identified in the sprint are **fixed and retested**.  
4. The deliverable is **deemed approved** in Sprint Review.

---

## ✅ **Test Cases**  
 
### User Story 2 🔎 - Map search 
_"As a client teaching team member, I want to search for trees around a certain location on the map, so that I can quickly find the perfect location that meets my requirements."_

✅ **Acceptance Criteria:**  
1. Tree data appears accurately on the map, as per Sprint 1;
2. Users can enter a search location;
3. Once users enter a search location, the map will only display results matching that criterion, within a selected given radius of their location;
4. Tree markers not meeting the selected search location/radius criteria are no longer displayed on the map;
5. The map defaults to use Melbourne Connect as the search location, with a default search radius of 1km;
6. Details of all search results are diplayed below the map, on successive pages of 10 results based on proximity to the search location; and
7. The map uses kilometre units.

📌 **Test Cases**

| **Test ID** | **User Story** | **Scenario (BDD Syntax)** | **Test Result** | **Tested By** | **Test Date** | **Comments** |
|------------|---------------|--------------------------|--------------|------------|------------|------------|
| TEST-US3-001  | Map search | **Given** a user wants to search for trees within a given radius on the map, **When** the user click the “Urban Tree Explorer Sprint 2 Search” link at the top of the website, **Then** the system should direct them to a new page displaying an interactive map that can be searched. |Pass|QA Engineer|6 May 2025| The site successfully redirected to the searchable map's page.|
| TEST-US3-002  | Map search | **Given** a user wants to search for trees within a given radius on the map, **When** the accesses the map search page (TEST-US2-001), **Then** the map should display the searchable map, centred on Melbourne Connect and displaying trees within 1km of that location, **and** include a field to input a new search address, and a drop-down selection box to select a new search radius. |Pass|QA Engineer|6 May 2025| Successfully displayed the input field for entering a new address and selection box for choosing the display distance and with the 1km default distance after entering the website.|
| TEST-US3-003  | Map search | **Given** a user want to search for the tree near a specific location in the map, **When** the user enters a new valid location as input (as validated by the map plugin), **and** clicks the search button, **Then** the system should update the map display to reflect the new search location, **and** display trees around that location. |Pass|QA Engineer|6 May 2025| Using many example inputs, the system successfully updated the map display, centring around chosen search location.|
| TEST-US3-004  | Map search | **Given** a user wants to search for trees in the map within a different radius around their chosen location, **When** the user clicks the search distance drop-down box, **and** selects a new radius, **and** clicks the search button,  **Then** the system should update the map display to reflect trees within the newly selected radius of their location. |Pass |QA Engineer|6 May 2025|When users change the search radius, the map will also scale proportionally according to the chosen search distances, and display trees within the search range by a green circle on the map.|
| TEST-US3-005  | Map search | **Given** a user wants to know the distribution of trees near the input location, **When** the user enters a new valid  location as a search input, **and** clicks the search button, **Then** the system should mark all trees meeting the search condition on the map. |Pass|QA Engineer|6 May 2025|After searching, the system marks all the trees meeting the search condition (i.e. within the chosen radius of a location). As with Sprint 1, users can get more detail by zooming into the map, or clicking on a marker. |
| TEST-US3-006  | Map search | **Given** a user wants to know detailed information of trees within their chosen search location, **When** the user enters a new valid location as input (as validated by the map plugin), **and** clicks the search button, **Then** the system should display the 10 nearest trees with their details below the map **and** allow the user to click through to additional search result pages to see details regarding trees that are further away. |Pass|QA Engineer|6 May 2025| After searching, information of all the trees meeting the search condition is listed under the map. They are divided in many pages, each displaying 10 trees' details.  Trees are ordered on pages by distance to the search location.|
| TEST-US3-007  | Map search | **Given** a user wants to know the precise location of the nearest search results, **When** the user clicks the frame of the tree’s detailed information in the search results at the base of the , **Then** the view of the page should return to the map, and show the precise location of the selected tree. |Pass|QA Engineer|6 May 2025| After clicking the information box, the page will move to ensure that the corresponding information can be fully displayed on the map, and the map centre will shift toward that target, ensuring the marker information is displayed in the centre of the map. Clicking the information box again will zoom in (if the marker has been clustered with other markers) until the marker is displayed individually on the map.|
| TEST-US3-008  | Map search | **Given** a user wants to search for a tree in specific place in the map, **When** the user enters a invalid location as input (as determined by the map plugin), **and** clicks the search button, **Then** the system should keep the map at the original location, and display an error message to inform the user that they entered a invalid location. |Pass|QA Engineer|6 May 2025| Only addresses inside of Australia are valid. If an address outside of Australia is entered, the system will display an error message saying 'This address could not be found'.|
| TEST-US3-009  | Map search | **Given** a user wants to search for a tree in specific place in the map, **When** the user enters a new valid location as input (as determined by the map plugin), **and** there are no trees in the selected range of their chosen location, **and** the click the search button, **Then** the system should update the map display to reflect the new search location, and display an error message to inform the user that there are no trees found within their search location/radius. | Pass|QA Engineer|6 May 2025| If there is no data near the input address/within the chosen radius, the system will display a corresponding prompt reading 'Sorry, such tree is not found'. The input address and search range will still be displayed on the map. |

### User Story 4 🗺️ - Map filtering 
_"As a client teaching team member, I want to filter through trees around a certain location on the map based on available criteria, so that I can quickly find the perfect location that meets my requirements."_

✅ **Acceptance Criteria:**  
1. Tree data appears accurately on the map as per Sprint 1;
2. Users can enter filter criteria, based on the location, distance from the location, and genus and age of a tree (being features in the City of Melbourne dataset);
3. Once users enter filter criteria, the map will only display results matching those criteria;
4. Tree markers not meeting the selected filter criteria are no longer displayed on the map;
5. The default filter values of location = Lincoln Square, Distance = 1km, Genus = Ficus, and Location_In = Park;
6. Trees of a different genus must be different colours for visbility. Trees of the same genus must be the same colour; and
7. The map must use kilometre units.

| **Test ID** | **User Story** | **Scenario (BDD Syntax)** | **Test Result** | **Tested By** | **Test Date** | **Comments** |
|------------|---------------|--------------------------|--------------|------------|------------|------------|
| TEST-US4-001  | Map filtering | **Given** a user wants to search for trees meeting certain criteria within a chosen location, **When** the user click the “Urban Tree Explorer Sprint 2 Filter” link at the top of the website, **Then** the website should direct them to a new page displaying an interactive map that can be filtered.|Pass|QA Engineer|6 May 2025|The site successfully redirected to the filterable map's page.|
| TEST-US4-002  | Map filtering | **Given** a user wants to search for trees meeting certain criteria within a chosen location, **When** the user click the “Urban Tree Explorer Sprint 2 Filter” link at the top of the website, **Then** the displayed page should include an interactive map that can be filtered by selecting check boxes, centred by default on Lincoln Square, and displaying results meeting the following criteria within 1km: location = Lincoln Square, Distance = 1km, Genus = Ficus, and Location_In = Park.|Pass|QA Engineer|6 May 2025|Successfully displayed all components with correct default parameters, correctly displayed on the map, with all small branches of each major category fully listed rather than shown in a check-box.|
| TEST-US4-003  | Map filtering | **Given** a user wants to filter by a single attribute, **When** the user selects a single category filter (such as "Located in", "Genus", or "Age description") from the appropriate check-box list, **and** clicks the search button, **Then** the system should update the map display to show only trees matching the selected category criteria, **and** display their details in a list below the map. |Pass|QA Engineer|6 May 2025|After testing, the map generally supports single attribute filtering. All filtered results can be correctly displayed on the map and the list below the map.|
| TEST-US4-004  | Map filtering | **Given** a user wants to filter by multiple attributes, **When** the user selects a combination of two or more category filters (combinations of located in, genus, and age description), **and** clicks the search button, **Then** the system should update the map display to show only trees matching the selected category criteria, **and** display their details in a list below the map.|Pass|QA Engineer|6 May 2025| After testing, the system fully supports filtering by multiple attributes, and the map will make corresponding updates to reflect trees meeting the selected criteria. The relationship between sub-options of a single category is 'and' rather than 'or', so if two options from the same category are selected, the filter will become ineffective. |
| TEST-US4-005  | Map filtering | **Given** a user wants to know the precise location of a result meeting their filter criteria, **When** the user clicks the frame of the tree’s detailed information in the list below the map, **Then** the page should show the precise location of the selected tree on the map. |Pass|QA Engineer|6 May 2025|After testing, when clicking on a tree's detailed information below the map, the view will return to the map and display the marker and related information on the map. Clicking on the detailed information again will zoom in on that marker's location of the map. |
| TEST-US4-006  | Map search | **Given** a user want to search for a tree in a specific place on the map, **When** the user enters a new valid  location as input (as determined by the map plugin), **and** clicks the search button, **Then** the system should update the map display to reflect trees meeting filter critera within that new search location. |Pass|QA Engineer|6 May 2025|  Using many example inputs, the system successfully updated the map display, with the centre point at the new input location.|
| TEST-US4-007  | Map search | **Given** a user wants to search for trees in different distance radius on the map, **When** the user modifies the search distance, **and** clicks the search button,  **Then** the system should update the map display to reflect filter results within the new search radius. |Pass |QA Engineer|6 May 2025|When users change the search radius, the map will also scale proportionally according to different search distances, and display filter results within the search range with a green circle on the map.|
| TEST-US4-008  | Map search | **Given** a user wants to know the distribution of trees near their chosen location, **When** the user enters a new valid location as input (as determined by the map plugin), **and** clicks the search button, **Then** the system should mark all trees within the chosen search radius on the map.|Pass|QA Engineer|6 May 2025| After searching, the system marks all the trees meeting the search location/radius criteria. As in Sprint 1, users can identify further details when they zoom into the map.  |
| TEST-US4-009  | Map search | **Given** a user wants to search for a tree in specific place in the map, **When** the user enters a new valid location as input (as determined by the map plugin), **and** there are no trees in the selected range of their chosen location, **and** the click the search button, **Then** the system should update the map display to reflect the new search location, and display an error message to inform the user that there are no trees found within their search location/radius that meet their criteria. | Pass|QA Engineer|6 May 2025| If there is no data near the input address/within the chosen radius, the system will display a corresponding prompt reading 'Sorry, such tree is not found'. The input address and search range will still be displayed on the map. |

### User Story 5 🔐 - Login Requirements 
_"As a client teaching team member, I want to securely access the Urban Tree Cover Explorer application using my username/email and password, so that the risk of data leakage can be reduced."_

✅ **Acceptance Criteria:**  
1. User credentials are stored securely.
2. Registered users can log in securely using their credentials, via a visually appealing login form.
3. Users with incorrect login details receive an error message.
4. Users who are not logged in are redirected to the login page.
5. The login page must, at a minimum, have a username/password form.

| **Test ID** | **User Story** | **Scenario (BDD Syntax)** | **Test Result** | **Tested By** | **Test Date** | **Comments** |
|------------|---------------|--------------------------|--------------|------------|------------|------------|
| TEST-US5-001  | Login Requirements  | **Given** a user wants to access the website, **When** they open the website, **and** the user is not logged in, **Then** a UI composed with account and password input fields and a login button should be displayed.|Pass|QA Engineer|7 May 2025| Successfully displayed the login page, including an input field for entering a username / email and password, a 'Remember Me' option, and a login button.|
| TEST-US5-002  | Login Requirements  | **Given** a user wants to login to the website, **When** they input a valid username/email and password combination, **and** they click the login button, **Then** the system should successfully authenticate the user's credentials and grant them access to the website. |Pass|QA Engineer|7 May 2025|After entering the correct inputs, the page successfully redirects to the website.|
| TEST-US5-003  | Login Requirements  | **Given** a user wants to login to the website, **When** they input a invalid username/email and password, **and** they click the login button, **Then** the system should display an error message noting their credentials are invalid, **and** the system should continue to display the login page to permit the user to correct their credentials.|Pass|QA Engineer|7 May 2025|When an invalid username/email is entered, the system will display an error message saying 'The username not registered on this site'. When the username/email is valid but an incorrect password is entered, the system will display an error message saying 'The password you entered for the username _[username]_ is incorrect.'|
| TEST-US5-004  | Login Requirements  | **Given** a user is not logged in, **When** the user attempts to access any part of the website, **Then** the system should redirect the user to the login page. |Pass|QA Engineer|7 May 2025| Testing shows that if logged out, it is still possible to perform operations on the current page, such as zooming the map, viewing detailed information of items, etc. However, if attempting to switch to other pages, it will force entry into the login interface, and once in the login interface, it is impossible to return to the original page unless successfully logged in. |
| TEST-US5-005  | Login Requirements  | **Given** a user is not logged in, **When** the user attempts to access a specific page ,  **And** the system should redirect the user to the login page，**And** the user enters valid credentials and logs in successfully, **Then** the system should redirect the user to the originally requested page|Pass|QA Engineer|24 May 2025| Through testing, the system ultimately redirects the user to the dashboard interface, where users can navigate to their desired interface on their own. |

---

## 📋 **Sprint 2 QA Tracking**  

| **Test ID** | **Feature** | **Status** | **Last Updated** |
|------------|------------|------------|----------------|
| TEST-US3-001  | Map Search | ✅ Complete | 6 May 2025 |
| TEST-US3-002  | Map Search | ✅ Complete| 6 May 2025 |
| TEST-US3-003  | Map Search | ✅ Complete| 6 May 2025 |
| TEST-US3-004  | Map Search | ✅ Complete| 6 May 2025 |
| TEST-US3-005  | Map Search | ✅ Complete| 6 May 2025 |
| TEST-US3-006  | Map Search | ✅ Complete| 6 May 2025 |
| TEST-US3-007  | Map Search | ✅ Complete| 6 May 2025 |
| TEST-US3-008  | Map Search | ✅ Complete| 6 May 2025 |
| TEST-US3-009  | Map Search | ✅ Complete| 6 May 2025 |
| TEST-US4-001  | Map Filter | ✅ Complete| 6 May 2025 |
| TEST-US4-002  | Map Filter | ✅ Complete| 6 May 2025 |
| TEST-US4-003  | Map Filter | ✅ Complete| 6 May 2025 |
| TEST-US4-004  | Map Filter | ✅ Complete| 6 May 2025 |
| TEST-US4-005  | Map Filter | ✅ Complete| 6 May 2025 |
| TEST-US4-006  | Map Filter | ✅ Complete| 6 May 2025 |
| TEST-US4-007  | Map Filter | ✅ Complete| 6 May 2025 |
| TEST-US4-008  | Map Filter | ✅ Complete| 6 May 2025 |
| TEST-US4-009  | Map Filter | ✅ Complete| 6 May 2025 |
| TEST-US5-001  | Login Requirements | ✅ Complete| 7 May 2025 |
| TEST-US5-002  | Login Requirements | ✅ Complete| 7 May 2025 |
| TEST-US5-003  | Login Requirements | ✅ Complete| 7 May 2025 |
| TEST-US5-004  | Login Requirements| ✅ Complete| 7 May 2025 |
| TEST-US5-005  | Login Requirements| ✅ Complete| 24 May 2025 |
