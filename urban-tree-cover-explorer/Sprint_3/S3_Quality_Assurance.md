# 🚀 Quality Assurance Strategy

This document set out our **Quality Assurance (QA) Strategy** for the Sprint 3 of **Urban Tree Cover Explorer** project.

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
 
### User Story 6 - 🌳 Access Parks and Places of Interest
_"As a PhD student or client teaching team member, I want to search for Parks and Places of Interest around Melbourne Connect so that I can find a location that meets my requirements."_

✅ **Acceptance Criteria:**  
1. Park and Place of Interest information displays accurately on the map, as with tree data in Sprints 1 and 2;
2. As with Sprint 2, users can filter Parks and Places of Interest based on their chosen category; and
3. The map page includes detailed information for University Square, Lincoln Square, Argyle Square and Carlton Gardens (each including a category tag, 3+ images and a written description), as well as YouTube videos demonstrating at least 2 of those sites.

📌 **Test Cases**

| **Test ID** | **User Story** | **Scenario (BDD Syntax)** | **Test Result** | **Tested By** | **Test Date** | **Comments** |
|------------|---------------|--------------------------|--------------|------------|------------|------------|
| TEST-US6-001  | Access Parks and Places of Interest | **Given** a user wants to explore Parks and Places of Interest, **When** the user clicks through to the Parks and Places of Interest page, **Then** the system will display a map of Parks and Places of interest centred on "Lincoln Square".|Pass|QA Engineer|22 May 2025 |The system successfully loaded all page components, with special locations (University Square, Lincoln Square, Argyle Square, Carlton Gardens) highlighted in special colours (orange, blue, pink, light purple).|
| TEST-US6-002  | Access Parks and Places of Interest | **Given** a user wants to identify specific Parks and Places of Interest, **When** the user clicks through to the Parks and Places of Interest page, **Then** the system will provide them with the option of filtering map markers, to target the display of only those markers the user wishes to see.|Pass|QA Engineer|22 May 2025 |The system successfully loaded all page components, including the filtering option.|
| TEST-US6-003  | Access Parks and Places of Interest | **Given** a user wants to learn more about a Park or Place of Interest, **When** the user clicks on a park or place of interest marker, **Then** there will be a popup with detailed information about the Park or Place of Interest at that marker (including space to display its category, description, and an image).|Pass|QA Engineer|22 May 2025 |After clicking the marker, a popup is successfully displayed, containing the marker's title, category, description, and other related information (including, if applicable, an image).|
| TEST-US6-004  | Access Parks and Places of Interest | **Given** a user wants to check the information of default locations (University Square, Lincoln Square, Argyle Square, Carlton Gardens), **When** the user clicks on the marker for one of those default locations, **Then**  there will be a popup with the corresponding detail (TEST-US6-003) pre-filled for those default locations.|Pass|QA Engineer|22 May 2025 |Through testing, the special locations all successfully displayed more detailed information (with introduction and related scene images additionally added to the information shown by regular markers). The pre-uploaded images cycle at 5-second intervals. Some special scenes have added YouTube-related video playback functionality (Lincoln Square, Carlton Gardens) for further information.|
| TEST-US6-005  | Access Parks and Places of Interest | **Given** a user wants to learn more about a default Park or Place of Interest (TEST-US6-004) **When** the user clicks on the marker for one of those default locations, **And** the user clicks on the video / video section, **Then** a video relating to that park/place of interest will start playing.|Pass|QA Engineer|22 May 2025 |Through testing, videos have been included for Lincoln Square and Carlton Gardens.  These are played successfully when clicked.|
| TEST-US6-006  | Access Parks and Places of Interest | **Given** a user wants to play a video about a Park or Place of Interest (TEST-US6-004) **When** the user clicks on the video / video section (TEST-US6-005) **and** the video plays, **Then** the user can adjust the video's sound, pause playback or access the original video on a linked platform (e.g. YouTube).|Pass|QA Engineer|22 May 2025 |Through testing, users can perform operations such as turning sound on/off, pausing playback, and jumping to the original video. After the video ends, users can manually choose to replay it.|
| TEST-US6-007  | Access Parks and Places of Interest | **Given** a users want to display Park or Place of Interest markers meeting specific criteria, **When** the user selects a filter category at the top of the map, **Then** the system will reload the map and only display markers that match the user's selected category.|Pass|QA Engineer|22 May 2025 |Through testing, all filtering functions operate normally.|
| TEST-US6-008  | Access Parks and Places of Interest | **Given** a users want to distinguish between default and user-generated Park or Place of Interest markers, **When** the user selects the relevant filter (e.g. user-generated or non-user generated), **Then** the system will reload the map and only display markers that match the user's selected category.|Pass|QA Engineer|22 May 2025 |"User-generated markers" and "Non-user generated markers" have an "and" relationship with other filter categories, meaning users can simultaneously select one of the former along with the latter to toggle on/off, allowing them to only see the markers they wish to see on the map.|


### User Story 7 - ✏️ User-Generated Markers
_"As a PhD student or client teaching team member, I want to be able to add additional Parks and Places of Interest around Melbourne Connect (and additional details about them) to the map so that I can share my thoughts on certain locations"_

✅ **Acceptance Criteria:**  
1. Park and Place of Interest information displays accurately on the map, as with tree data in Sprints 1 and 2 (see US6); and
2. Users can submit a marker for a new Park or Place of Interest, including a category tag, image(s) of it, and a written description.

📌 **Test Cases**

| **Test ID** | **User Story** | **Scenario (BDD Syntax)** | **Test Result** | **Tested By** | **Test Date** | **Comments** |
|------------|---------------|--------------------------|--------------|------------|------------|------------|
| TEST-US7-001  | User-Generated Markers | **Given** a user wants to select the location where they want to add a new map marker, **When** the user right-clicks on the desired location on the map, or enters a detailed address in the "Marker Address or GPS" area below the map, **Then** a special marker will be displayed at the corresponding location on the map.|Pass|QA Engineer|22 May 2025 |When right-clicking on the corresponding location on the map, the "Marker Address or GPS" field below the map automatically provides the corresponding coordinate position. Alternatively, users can input specific coordinates or place names in the Marker Address or GPS field to automatically locate their chosen marker location.|
| TEST-US7-002  | User-Generated Markers | **Given** a user wants to add a marker with additional information (title, description, category etc.), **When** the user selects their desired location (as in TEST-US7-001), **then** the user will be prompted to add the corresponding title, description and category for their chosen marker.|Pass|QA Engineer|22 May 2025 | The title and description boxes are able to be completed by the user.|
| TEST-US7-003  | User-Generated Markers | **Given** a user wants to add a marker with additional information (title, description, category etc.), **When** the user selects their desired location (as in TEST-US7-001), **and** enters the corresponding title, description and category for their chosen marker (TEST-US7-003) **and** clicks the "Add marker" button, **Then** the system will reload the map, and the user's new marker will be included on the map.|Pass|QA Engineer|22 May 2025 |After inputting the title and description, users need to additionally check "Please tick this box to prove you are human." After clicking "add marker," a marker is successfully created at the specified location.|
| TEST-US7-004  | User-Generated Markers | **Given** a user has created a new marker (TEST-US7-003), **When** the user clicks on that new marker, **Then** the content they input (title, description, category etc.) appears with the title displayed in bold above the description. |Pass|QA Engineer|22 May 2025 |When clicking the market, the input content appears with the title displayed in bold above the description. If nothing is input and coordinates are created directly, it will still be created successfully, with the coordinate information containing only its coordinate position. During the selection process, multiple categories can be checked, and when filtering, multiple categories can also be used to filter related markers. Note that "User-generated markers" needs to be manually checked during creation in order to be filtered by this category type in the filter. If only the Marker Category is used as input when creating a marker, clicking it will display the marker's coordinates.|
| TEST-US7-005  | User-Generated Markers | **Given** a user wants to add a marker (TEST-US7-002 and TEST-US7-003) that includes a link to additional information, **When** the user selects their desired location (as in TEST-US7-001), **and**  user enters a valid URL address in the input box (as validated by the WP GO Maps plugin), **and** clicks the "Add marker" button, **Then** the system will reload the map, the newly added marker will be included, and clicking the marker (TEST-US6-003) will include a "More detail" link that can be clicked to redirect the browser to the corresponding URL.|Pass|QA Engineer|22 May 2025 |After inputting a valid URL, a marker is successfully created. When clicking the marker, a "More details" link appears below the introduction. If clicked, it will navigate to the corresponding URL.|
| TEST-US7-006  | User-Generated Markers | **Given** a user wants to add a marker that includes a link to additional information (TEST-US7-005), **When** the user enters an invalid URL address in the input box (as validated by the WP GO Maps plugin), **and** clicks the "Add marker" button, **Then** the system will reload the map, the newly added marker will be included, and clicking the marker (TEST-US6-003) will not show any URL-related content (i.e. no "More detail" link), while other parts display normally.|Pass|QA Engineer|22 May 2025 |When attempting to input some non-existent URLs, no "More details" links are generated on the relevant map markers, effectively omitting that section. If only an invalid URL is input, the marker will display the current coordinates. |
| TEST-US7-007  |  User-Generated Markers | **Given** a user want to add a marker (TEST-US7-002 and TEST-US7-003) that includes an image as additional information, **When** the user selects their desired location (as in TEST-US7-001), **and** clicks the "choose file" button **and** selects the corresponding image file from local storage, **and** clicks the "Add marker" button, **Then** the system will reload the map, the newly added marker will be included, and clicking the marker (TEST-US6-003) will display the user's selected image in the marker's popup.|Pass|QA Engineer|22 May 2025 |Many types of image files can be uploaded. Currently tested JPEG, GIF, and PNG formats all display normally once uploaded. Only one image can be uploaded in total, and the image will be displayed above the title. |
| TEST-US7-008  | User-Generated Markers | **Given** a user wants to add a marker that includes an image as additional information (TEST-US7-007), **When** the user enters an invalid image file type (e.g. PDF, DOC, EXE etc.), **and** clicks the "Add marker" button, **Then** the system will reload the map, the newly added marker will be included, and clicking the marker (TEST-US6-003) will not show any related image content, while other parts display normally.|Pass|QA Engineer|22 May 2025 |Non-image file uploads were tested: PDF, DOC, EXE, etc. Markers can be successfully created, but the image-related content will not be displayed. If a marker is created using only non-image files, the marker will only display the current coordinates.|

### User Story 8 - 📍 Users access a walking itinerary, and rate stops along the way
_"As a PhD student or client teaching team member, I want to access a guided walking tour across Melbourne so that I can explore the city and visit notable locations, while learning about the density of tree cover nearby."_

✅ **Acceptance Criteria:**  
1. The walking itinerary appears accurately on the map;
2. The tree data appears accurately on the map as a heatmap;
3. Users can identify directions along the walking itinerary, and pause their journey; and
4. Users can rate each stop on the walking tour (1-10 scale).

📌 **Test Cases**

| **Test ID** | **User Story** | **Scenario (BDD Syntax)** | **Test Result** | **Tested By** | **Test Date** | **Comments** |
|------------|---------------|--------------------------|--------------|------------|------------|------------|
| TEST-US8-001  | Walking Itinerary & Heat Map | **Given** a user wants to access a guided walking tour across Melbourne, **When** the user clicks the walking tour web page, **Then** the system should display an interactive map, centred around a proposed walking route. |Pass|QA Engineer|23 May 2025 |The system successfully loaded all page components.|
| TEST-US8-002  | Walking Itinerary & Heat Map | **Given** a user wants to access a guided walking tour across Melbourne, **When** the user clicks the walking tour web page, **Then** the proposed walking route should show a route via 11 markers for default locations (University of Melbourne Old Quad, Lincoln Square, State Library of Victoria, Melbourne Central, Federation Square, State Parliament Building, Treasury Gardens, Cook's Cottage, Model Tudor Village, Carlton Gardens and Melbourne Connect), including directions for the complete walking route. |Pass|QA Engineer|23 May 2025 |The page successfully loaded, displaying 11 specified locations on the map as green markers, and connecting them in sequence with a yellow path, showing the direction of travel.|
| TEST-US8-003  | Walking Itinerary & Heat Map | **Given** a user wants to understand the distribution of trees along the walking route, **When** the user clicks the walking tour web page, **Then** the system should display a heat map around the walking route, using different colours to indicate different tree density levels in the City of Melbourne.|Pass|QA Engineer|23 May 2025 |The heat map changes from blue to green to red, representing increasing tree density. When zooming in on the map, the heat map also changes accordingly, calculating tree density based on the absolute distance on the map.|
| TEST-US8-004  | Walking Itinerary & Heat Map | **Given** a user wants to view a specific stop on the walking itinerary, **When** the user clicks on a specific stop (i.e. market), **Then** the system should display a popup with the name of the stop. |Pass|QA Engineer|23 May 2025 |After clicking the marker, the current stop name is displayed. |

### User Story 9 - ⭐️ User-Generated Ratings
_"As a client teaching team member, I want to be able to see the ratings students gave for a particular location so that I can use it as a reference for next meeting"_

✅ **Acceptance Criteria:**  
1. Users can see ratings 1-10 on the markers;
2. Users can select ratings on the markers; and
3. Average ratings that users gave for a marker will be available to other users;

📌 **Test Cases**

| **Test ID** | **User Story** | **Scenario (BDD Syntax)** | **Test Result** | **Tested By** | **Test Date** | **Comments** |
|------------|---------------|--------------------------|--------------|------------|------------|------------|
| TEST-US9-001  | User-Generated Ratings | **Given** a user wants to understand the popularity of a specific Park or Place of Interest, or stop on the walking itinerary, **When** the user clicks on the relevant marker, **Then** the displayed popup (TEST-US6-003 & TEST-US8-004) should include the average of all user-generated ratings for that location. |N/A|QA Engineer|23 May 2025 |Client deprioritised rating feature due to technical constraints.|
| TEST-US9-002  | User-Generated Ratings | **Given** a user wants to rate a specific Park or Place of Interest, or stop on the walking itinerary, to share their experience with others, **When** the user clicks on the relevant marker, **and** selects the rating they want to give to that location by clicking the corresponding button at the bottom of the popup, **Then** the system will record the user's selected rating, and display it within the average rating (TEST-US9-001). |N/A|QA Engineer| 23 May 2025|Client deprioritised rating feature due to technical constraints |

---

## 📋 **Sprint 3 QA Tracking**  

| **Test ID** | **Feature** | **Status** | **Last Updated** |
|------------|------------|------------|----------------|
| TEST-US6-001  | Access Parks and Places of Interest | ✅ Complete | 22 May 2025 |
| TEST-US6-002  | Access Parks and Places of Interesth | ✅ Complete| 22 May 2025 |
| TEST-US6-003  | Access Parks and Places of Interest | ✅ Complete| 22 May 2025 |
| TEST-US6-004  | Access Parks and Places of Interest | ✅ Complete| 22 May 2025 |
| TEST-US6-005  | Access Parks and Places of Interest | ✅ Complete| 22 May 2025 |
| TEST-US6-006  | Access Parks and Places of Interest | ✅ Complete| 22 May 2025 |
| TEST-US6-007  | Access Parks and Places of Interest | ✅ Complete| 22 May 2025 |
| TEST-US6-008  | Access Parks and Places of Interest | ✅ Complete| 22 May 2025 |
| TEST-US7-001  | User-Generated Markers | ✅ Complete| 22 May 2025 |
| TEST-US7-002  | User-Generated Markers | ✅ Complete| 22 May 2025 |
| TEST-US7-003  | User-Generated Markers | ✅ Complete| 22 May 2025 |
| TEST-US7-004  | User-Generated Markers | ✅ Complete| 22 May 2025 |
| TEST-US7-005  | User-Generated Markers | ✅ Complete| 22 May 2025 |
| TEST-US7-006  | User-Generated Markers | ✅ Complete| 22 May 2025 |
| TEST-US7-007  | User-Generated Markers | ✅ Complete| 22 May 2025 |
| TEST-US7-008  | User-Generated Markers | ✅ Complete| 22 May 2025 |
| TEST-US8-001  | Walking Itinerary & Heat Map | ✅ Complete| 23 May 2025 |
| TEST-US8-002  | Walking Itinerary & Heat Map | ✅ Complete| 23 May 2025 |
| TEST-US8-003  | Walking Itinerary & Heat Map | ✅ Complete| 23 May 2025 |
| TEST-US8-004  | Walking Itinerary & Heat Map | ✅ Complete| 23 May 2025 |
| TEST-US9-001  | User-Generated Ratings | ℹ️ N/A - Deprioritised | 23 May 2025 |
| TEST-US9-002  | User-Generated Ratings | ℹ️ N/A - Deprioritised | 23 May 2025 |
