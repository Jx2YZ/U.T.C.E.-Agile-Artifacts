# 🚀 Quality Assurance Strategy

This document set out our **Quality Assurance (QA) Strategy** for the Sprint 1 of **Urban Tree Cover Explorer** project.

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
 
### User Story 1 🗺️ - Map Access 
_"As a member of the client teaching team I want an interactive map that visualises urban tree data and allows users to view tree locations with markers and basic details."_

✅ **Acceptance Criteria:**  
1. Tree data appears accurately on the map.
2. Users can interact with the map to move around the Melbourne area.
3. Users can click on tree markers to see basic tree information.

📌 **Test Cases**

| **Test ID** | **User Story** | **Scenario (BDD Syntax)** | **Test Result** | **Tested By** | **Test Date** | **Comments** |
|------------|---------------|--------------------------|--------------|------------|------------|------------|
| TEST-US1-001  | Map Access | **Given** a user wants to access the tree cover map, **When** the user accesses the map page, **Then** the system should display a map of marked trees in Melbourne, centred on the user's general position. |Pass|QA Engineer|18 Apr 2025|Successfully displayed the map after entering the website, with the centre point at the user's current location.|
| TEST-US1-002  | Map Access | **Given** a user wants to zoom into the map, **When** the user hovers their cursor on the map, **and** presses control/command, **and** scrolls on their mouse/trackpad in an upward direction, **then** the map zooms in, centred on the cursor. |Pass|QA Engineer|18 Apr 2025|Successfully zoomed in on the map approximately centred on the mouse cursor when using the described operation.|
| TEST-US1-003  | Map Access | **Given** a user wants to zoom out of the map, **When** the user hovers their cursor on the map, **and** presses control/command, **and** scrolls on their mouse/trackpad in a downward direction, **then** the map zooms out, centred on the cursor. |Pass |QA Engineer|18 Apr 2025|Successfully zoomed out on the map approximately centred on the mouse cursor when using the described operation.|
| TEST-US1-004  | Map Access | **Given** a user is viewing the map with individual tree markers visible, **When** the user zooms out of the map to view a larger area, **then** nearby tree markers should automatically merge into cluster icons to reduce visual clutter, and show the number of marker merged|Pass|QA Engineer|18 Apr 2025|When zooming out the map, adjacent tree markers successfully merged into cluster icons and displayed the specific number of markers within the cluster.|
| TEST-US1-005  | Map Access | **Given** a user wants to look at clustered tree markers in more detail, **When** the user clicks on a cluster icon, **then** the tree markers contained in the cluster will spread out for visibility. |Pass|QA Engineer|18 Apr 2025|When clicking on a cluster, the markers within the cluster successfully spread out on the map.|
| TEST-US1-006  | Map Access | **Given** a user is viewing a map with clustered tree markers, **When** the user zooms in sufficiently on the map, **then** the clusters should be decomposed into individual tree markers. |Pass|QA Engineer|18 Apr 2025|Clusters successfully dispersed into different markers when zooming in.|
| TEST-US1-007  | Map Access | **Given** a user wants to move around the map (up, down, left, right), **When** the user hovers their cursor on the map **and** holds a left click on the map **and** drags their mouse/trackpad, **Then** the map should move in the direction of their cursor. |Pass|QA Engineer|18 Apr 2025|Successfully able to move the map and update markers in a timely manner.|
| TEST-US1-008  | Map Access | **Given** a user identifies a marked tree for which they require further information, **When** the user left clicks the marker for that tree, **Then** a popup containing additional information about that tree should appear. | Pass|QA Engineer|18 Apr 2025|Successfully displayed popup when clicking on markers, and the view adjusted accordingly.|
| TEST-US1-009  | Map Access | **Given** a user identifies a marked tree for which they require further information, **When** the user left clicks the marker for that tree to display a popup, **Then** the popup (TEST-US1-005) should display the name, ID, genus/family, diameter, breadth height, year/date planted, age description, useful life expectancy value, and location. |Pass|QA Engineer|18 Apr 2025|Randomly selected 20 markers, all popups successfully displayed all the required information.|
| TEST-US1-0010  | Map Access | **Given** a user has already opened a popup of details about a particular tree but wishes to view details about another tree, **When** the user left clicks the marker for that other tree, **Then** the existing popup displayed is replaced with a popup relevant to that other tree. |Pass|QA Engineer|18 Apr 2025|View successfully transfers when clicking on different markers.|
| TEST-US1-0011  | Map Access | **Given** a user has already opened a popup of details about a particular tree but wishes to close the popup, **When** the user left clicks the 'x' at the top right corner of the popup, **Then** the popup closes. |Pass|QA Engineer|18 Apr 2025|Popup successfully closes when clicking the 'x' in the top right corner.|

---

## 📋 **Sprint 1 QA Tracking**  

| **Test ID** | **Feature** | **Status** | **Last Updated** |
|------------|------------|------------|----------------|
| TEST-US1-001  | Map Access  | ✅finish  | 18 Apr 2025 |
| TEST-US1-002  | Map Access  | ✅finish  | 18 Apr 2025 |
| TEST-US1-003  | Map Access | ✅finish | 18 Apr 2025 |
| TEST-US1-004  | Map Access | ✅finish | 18 Apr 2025 |
| TEST-US1-005  | Map Access | ✅finish | 18 Apr 2025 |
| TEST-US1-006  | Map Access |✅ finish| 18 Apr 2025 |
| TEST-US1-007  | Map Access | ✅finish | 18 Apr 2025 |
| TEST-US1-008  | Map Access | ✅finish | 18 Apr 2025 |
| TEST-US1-009  | Map Access | ✅finish | 18 Apr 2025 |
| TEST-US1-0010  | Map Access | ✅finish | 18 Apr 2025 |
| TEST-US1-0011  | Map Access | ✅finish | 18 Apr 2025 |
