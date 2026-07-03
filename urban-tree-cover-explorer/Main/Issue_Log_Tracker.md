# Project Issue Tracker  

This document tracks **bugs** we identify, planned **fixes**, and our process **resolving** them.  We will:
1. **Document** defects immediately, to keep accurate records;
2. **Classify** defects based on their severity (e.g., Critical, High, Medium, Low);
3. **Resolve** defects in a timely manner, assigning them to responsible developers who must monitor their resolution status; and
4. **Test and Verify** our changes to defective items to ensure they are resolved.

---
## 🚨 Issue Log

### 📅 **Last Updated:** 16 April 2025  

| **Defect ID** | **Date Reported** | **Description**                                  | **Severity** | **Reported By** | **Status** | **Assigned To**   | **Fix Implemented**                           | **Tested By**   | **Test Date**   | **Comments**                           |
|---------------|-------------------|--------------------------------------------------|--------------|-----------------|------------|-------------------|----------------------------------------------|-----------------|-----------------|----------------------------------------|
| DEF-001 | 2025-04-15 | Heavy delay on WordPress | Critical 🔴 | Dev A | Resolved | Product Owner | Clear all unused data and maps from WordPress to reduce server load | Dev A | 2025-04-16 | |
| DEF-002 | 2025-04-15 | Marker Info Box flickering upon clicking | High 🟠 | Dev A | Resolved | Dev A | Disable 'Only load marker within viewport (beta)' option | Dev A | 2025-04-16 | This issue may caused by the pending towards Marker upon Marker-click, causing the map to re-load marker and resetted the open state of Marker Info Box |
| DEF-003       | 2025-04-16      | Marker List Displaying exact data field name while the Marker Info Box preprocessed the field, which removed the underline from the field name, causing confusion for user | Low 🟢 | Dev A | Resolved   | Dev A | Renamed each field name in Maker Fields Setting | Dev A | 2025-04-16    |   |
| DEF-004       | 2025-04-16        | Marker Info Box failed to display due to blocking of Marker Cluster | High 🟠   | Dev A | Resolved   | Dev A | Set maximum zoom for Maker Cluster size smaller than zoom size when Maker is clicked | Dev A | 2025-04-16 | |
| DEF-005 | 2025-05-03 | Unable to set default values for category filter | Medium 🟡 | Product Owner | Resolved | Product Owner | Reimported dataset with updated category values and set filter function using category instead of custom fields | Product Owner | 2025-05-05 | |
| DEF-006 | 2025-05-04 | Map not showing unless marker listing is set as advanced table | High 🟠 | Product Owner | Resolved | Product Owner | Do not set map width using percentage | Product Owner | 2025-05-05 | |
| DEF-007 | 2025-05-14 | Map fails to visualise a pre-determined walking itinerary  | High 🟠 | Dev A | Resolved | Dev A | Switch the Map enginee from OpenLayer to Google | Dev A | 2025-05-14 ||
| DEF-008 | 2025-05-14 | Map fails to visualise a pre-determined walking itinerary  | High 🟠 | Dev A | Resolved | Dev A | Use double quotation instead of single quotation for encapsulating parameters | Dev A | 2025-05-14 | The itinerary visualisation is done by shortcode, where each parameter is encapsulating by single quotation marker at default. However, when we input the waypoints for our itinerary, the location "Cook's Cottage" contains a single quotation, which break the prameter and stop the map from visualisig the walking itinerary. |
| DEF-008 | 2025-05-15 | Attached YouTube video not visible on marker for Web Page 4| Medium 🟡  | Product Owner | Resolved | Product Owner | iframe plugin required and activated | Product Owner | 2025-05-20 | |
| DEF-0010 | 2025-05-20 | Map fails to update ratings for Web Page 4 and 5 | Medium 🟡 | Dev A | Pending for plugin developers to resolve, feature currently deprioritised | Dev A | | |  |  Feature currently deprioritised|


- **Critical 🔴**: A defect that causes the system to crash or results in a complete failure of a critical feature, blocking the functionality entirely.
- **High 🟠**: A significant defect that affects core functionality but can be worked around temporarily, requiring a quick fix.
- **Medium 🟡**: A moderate defect that impacts non-critical functionality and may be deferred without immediate consequences.
- **Low 🟢**: A minor defect that has little to no impact on functionality, typically cosmetic or related to user interface improvements

---
## 📚 ** Key Terms**

Each defect should be logged with the following details:
- **Date Reported**: When the defect was reported;
- **Defect ID**: Unique identifier for the defect;
- **Description**: A short description of the bug;
- **Severity**: High, Medium, Low (Impact of the defect on the project);
- **Reported By**: The person who reported the defect;
- **Status**: Open, In Progress, Resolved, Closed, etc.;
- **Assigned To**: Developer responsible for fixing the defect;
- **Fix Implemented**: Description of the fix or solution;
- **Tested By**: Tester who verified the fix;
- **Test Date**: Date when the fix was tested; and
- **Comments**: Any additional notes or issues related to the defect.
