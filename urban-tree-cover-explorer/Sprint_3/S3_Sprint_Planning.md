# Sprint Planning (Sprint 3)

### 🛠️ Baseline User Story Example

**User Story:** As a registered user, I want to log into the system using my registered account so that I can access the interactive map, and identify suitable locations for PhD student meet-ups.

- **Estimated Story Points:** 34 (based on Fibonacci sequence)
- **Rationale:** This task involves authentication logic, form validation, a map lookup, and a database lookup.  This means making it is quite complex.  However, much of this work is already complete, downgrading the estimated story points for this baseline user story in this sprint.

### 🌳 Access Parks and Places of Interest

**User Story:** As a PhD student or client teaching team member, I want to search for Parks and Places of Interest around Melbourne Connect so that I can find a location that meets my requirements.

- **Relative Complexity Comparison:**
  - Building off our understanding of map functionality implemented in Sprints 1 and 2, this task involves further configuring to the WP Go Map plugin to display an alternate dataset (of Parks, rather than trees);
  - Including an additional option for individual users to add further data to the map (and providing for category, image and description datapoints);
  - Building off our understanding of the filter functionality in Sprint 2, implementing a filter option to filter Parks and Places of Interest based on selected categories;
  - Displaying detailed information for University Square, Lincoln Square, Argyle Square and Carlton Gardens (each including a category tag, 3+ images and a written description) by default; and
  - Display a YouTube videos demonstrating at least two of University Square, Lincoln Square, Argyle Square and Carlton Gardens.
- **Estimated Story Points:** 13 (based on Fibonacci sequence)
- **Rationale:** This story is more complex than the baseline story given it includes implementation of a further map and dataset, including detailed data points for each Park/Place of Interest.

### ✏️ User-Generated Markers

**User Story:** As a PhD student or client teaching team member, I want to be able to add additional Parks and Places of Interest around Melbourne Connect (and additional details about them) to the map so that I can share my thoughts on certain locations.

- **Relative Complexity Comparison:**
  - Building off our understanding of map functionality implemented in Sprints 1 and 2 (and US6), this task involves further configuring to the WP Go Map plugin to display user-generated content
  - Including an additional option for individual users to add further data to the map (and providing for category, image and description datapoints);
  - Building off our understanding of the filter functionality in Sprint 2, to ensure user-generated markers can be filtered;
- **Estimated Story Points:** 5 (based on Fibonacci sequence)
- **Rationale:** This story is more complex than the baseline story given it includes implementation of more advanced functionality, such as user-generated data points.


### 📍 Users access a walking itinerary

**User Story:** As a PhD student or client teaching team member, I want to access a guided walking tour across Melbourne so that I can explore the city and visit notable locations, while learning about the density of tree cover nearby.

- **Relative Complexity Comparison:**
  - Building off our understanding of map functionality implemented in Sprints 1 and 2, this task involves further configuring to the WP Go Map plugin to include a pre-defined walking route, and heatmap;
  - Pre-fill a walking itinerary, giving users directions from/to University of Melbourne Old Quad, Lincoln Square, State Library of Victoria, Melbourne Central, Federation Square, State Parliament Building, Treasury Gardens, Cook's Cottage, Model Tudor Village, Carlton Gardens and Melbourne Connect;
  - Enable functionality for users to pause the walking tour at each location; and
  - Overlay a heatmap of <3000 nearby trees over the walking route.
- **Estimated Story Points:** 21 (based on Fibonacci sequence)
- **Rationale:** This story is more complex than the baseline story given it includes implementation of a new style of map (i.e. heatmap), and logging of a walking route.

### _DEPRIORITISED_ ⭐️ User-Generated Ratings 

**User Story:** As a client teaching team member, I want to be able to see the ratings students gave for a particular location so that I can use it as a reference for next meeting.

- **Relative Complexity Comparison:**
  - Building off our understanding of map functionality implemented in Sprints 1 and 2, this task involves further configuring to the WP Go Map plugin to display rating on markers
  - Enable and configure the rating function so that it display 1-10 rating options
  - The average of the user-generated ratings should be reflected on the map markers for every user.
- **Estimated Story Points:** 5 (based on Fibonacci sequence)
- **Rationale:** This story is not complex if the Wp Go Map plugin works accordingly.

---
# Sprint 3 Planning for Urban Tree Cover Explorer

## 🏆 Sprint Goal
Build a map displaying Parks and Places of Interest as well as user generated content, and a second map displaying a pre-defined walking route against a heatmap of trees around the City of Melbourne.

## ✅ Commitment
The team commits to completing each map capability by the end of this sprint.

# Selected User Stories
### User Story: 🌳 Access Parks and Places of Interest
As a PhD student or client teaching team member, I want to search for Parks and Places of Interest around Melbourne Connect so that I can find a location that meets my requirements.

### Acceptance Criteria:
- Park and Place of Interest information displays accurately on the map, as with tree data in Sprints 1 and 2;
- As with Sprint 2, users can filter Parks and Places of Interest based on their chosen category; and
- The map page includes detailed information for University Square, Lincoln Square, Argyle Square and Carlton Gardens (each including a category tag, 3+ images and a written description), as well as YouTube videos demonstrating at least 2 of those sites.

### Estimation (using Fibonacci sequence)
| Factor              | Consideration |
|---------------------|--------------|
| Complexity         | High - Need to enable the display of multimedia content in this new map, and configure related map settings. |
| Uncertainty        | Medium - The team now understands the general nature of the WP GO Maps plugin, but is not yet aware of how to richer data (e.g. images, video). |
| Dependencies      | Medium - Relies on WPGo Map plugin and associated database capabilities, with these capabilities generally being quite limited, and reliant on the client's selected technologies. |
| Risk              | Medium - Reliance on the WPGo Map plugin's limited functioanlity may render this map of lower quality, or unusuable.  Past experience using the plugin during Sprints 1 & 2 may help mitigate this risk.  |
| Estimated Story Points | **13** (based on team discussion) |


### User Story: ✏️ User-Generated Markers
As a PhD student or client teaching team member, I want to be able to add additional Parks and Places of Interest around Melbourne Connect (and additional details about them) to the map so that I can share my thoughts on certain locations.

### Acceptance Criteria:
- Park and Place of Interest information displays accurately on the map, as with tree data in Sprints 1 and 2 (see US6); and
- Users can submit a marker for a new Park or Place of Interest, including a category tag, image(s) of it, and a written description.

### Estimation (using Fibonacci sequence)
| Factor              | Consideration |
|---------------------|--------------|
| Complexity         | Medium - Need to enable the display of multimedia user-generated content in this new map, and configure related map settings. |
| Uncertainty        | Medium - The team now understands the general nature of the WP GO Maps plugin, but is not yet aware of how to implement user-generated content functionalities. |
| Dependencies      | Medium - Relies on WP Go Map plugin and associated database capabilities, with these capabilities generally being quite limited, and reliant on the client's selected technologies. |
| Risk              | High - User-generated content is unpredictable, and may be of low quality |
| Estimated Story Points | **5** (based on team discussion) |

### User Story: 📍 Users access a walking itinerary
As a PhD student or client teaching team member, I want to access a guided walking tour across Melbourne so that I can explore the city and visit notable locations, while learning about the density of tree cover nearby.

### Acceptance Criteria:
- The walking itinerary appears accurately on the map;
- The tree data appears accurately on the map as a heatmap;and
- Users can identify directions along the walking itinerary, and pause their journey; 

### Estimation (using Fibonacci sequence)
| Factor              | Consideration |
|---------------------|--------------|
| Complexity         | High - Need to enable the display of a walking itinerary and heat map being functions that have not been explored in previous sprints. |
| Uncertainty        | Medium - The team now understand the general nature of the WP GO Maps plugin, but not yet confirm the method of implementing data as heatmap and exnable direction feature with waypoints. |
| Dependencies      | Medium - Relies on WP Go Map plugin and associated database capabilities, with these capabilities generally being quite limited, and reliant on the client's selected technologies. |
| Risk              | High - Path search results are unpredictable, and may be of low quality. |
| Estimated Story Points | **21** (based on team discussion) |

### User Story: ⭐️ User-Generated Ratings
As a client teaching team member, I want to be able to see the ratings students gave for a particular location so that I can use it as a reference for next meeting.

### Acceptance Criteria:
- Users can see ratings 1-10 on the markers;
- Users can select ratings on the markers; and
- Average ratings that users gave for a marker will be available to other users;

### Estimation (using Fibonacci sequence)
| Factor              | Consideration |
|---------------------|--------------|
| Complexity         | Medium - Need to enable the rating function on Web Page 4 and 5 |
| Uncertainty        | Medium - The team now understand the general nature of the WP GO Maps plugin, but plugin can be bug-prone |
| Dependencies      | Medium - Relies on WP Go Map plugin and associated database capabilities, with these capabilities generally being quite limited, and reliant on the client's selected technologies. |
| Risk              | High - Plugins can be unreliable |
| Estimated Story Points | **5** (based on team discussion) |



---

## 📋 Sprint Backlog Tasks
| Task | Assigned To | Estimated Hours |
|------|------------|----------------|
|Implement an interactive map on a new webpage displaying park and other places of interest in the City of Melbourne |Product Owner | 3 |
|Add a filter function to show/hide user-submitted markers. |Product Owner | 2|
|By default, include detailed information for University Square, Lincoln Square, Argyle Square and Carlton Gardens (each including a category tag, 3+ images and a written description). |Product Owner | 2|
|Embed YouTube videos demonstrating at least two of the locations mapped in US6_T6. |Product Owner | 2|
|Allow users to submit new markers for Parks or Places of Interest (each including a category tag, image(s) of the Park or Place of Interest, and a written description). |Product Owner | 2|
|Implement an interactive map on a new webpage capable of displaying a pre-defined walking itinerary through the Melbourne CBD. |Dev A | 3 |
|Pre-fill the walking itinerary, giving users directions to/from the following sites in order when the map loads: University of Melbourne Old Quad, Lincoln Square, State Library of Victoria, Melbourne Central, Federation Square, State Parliament Building, Treasury Gardens, Cook's Cottage, Model Tudor Village, Carlton Gardens, Melbourne Connect. |Dev A | 2 |
|Overlay the itinerary map with a heatmap of tree locations in the City of Melbourne (using <3000 instances of the relevant dataset). |Dev A | 5 |
| _DEPRIORITISED_ enable the rating function on map 4 and 5 | Product Owner and Dev A | 2 |
