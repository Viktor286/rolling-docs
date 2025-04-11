# Task Specification: TASK_20250410_FE004 - Enhance User Dashboard Upcoming Journeys

**Date Created:** 2025-04-10
**Assigned Role/Area:** Frontend Dev
**Related Core Docs:**
* Project Description: [`../../2_Project_Description.md`](../../2_Project_Description.md) (Section 2.4 - User Dashboard)
* Technical Plan: [`../../3_Technical_Plan.md`](../../3_Technical_Plan.md)
* Implemented Features: [`../../../implemented-features.md`](../../../implemented-features.md) (Mentions upcoming journeys section)
* Role Documentation: [`../../Roles/Developer_Fullstack/Instructions.md`](../../Roles/Developer_Fullstack/Instructions.md) (Assuming Frontend Dev follows similar path)
* Related Task Specs (if any): Assumes basic User Dashboard structure exists.

---

## 1. Goal

* Enhance the "Upcoming Journeys" section of the User Dashboard to display more detailed information for each listed journey, beyond just the countdown timer mentioned in `implemented-features.md`.

## 2. Scope

### In Scope:

* Fetch (using appropriate data access method - potentially the refactored one from TASK_20250410_BE001) mock data representing a user's upcoming journeys.
* For each upcoming journey displayed in the dashboard section, include:
    * Destination Name (linked to destination detail page).
    * Departure Date.
    * Seat Class (Economy, Business, Luxury).
    * (Keep the existing countdown timer if implemented).
* Ensure the layout of the enhanced journey details is responsive.
* Style the new elements according to the project's design system (`../../3_Technical_Plan.md`).

### Out of Scope:

* Implementing the "Manage Booking" functionality.
* Displaying past journeys (this task focuses only on *upcoming*).
* Real-time updates to journey status.
* Creating the initial structure of the User Dashboard page itself (assumed to exist).
* User authentication (assume mock user data).

---

## 3. Acceptance Criteria (AC)

* [ ] User Dashboard's "Upcoming Journeys" section displays mock journey data.
* [ ] Each listed journey shows Destination Name (as link), Departure Date, and Seat Class.
* [ ] The existing countdown timer (if present) is still functional alongside new details.
* [ ] The layout correctly adapts to mobile, tablet, and desktop viewports.
* [ ] Styling matches the established project design language.
* [ ] Basic accessibility checks pass (semantic structure, text contrast).
* [ ] All relevant mandatory QA checks (`pnpm project:qa` from `../../4_Global_Tooling.md`) MUST pass successfully.

---

## 4. Technical Notes / Constraints (Optional)

* Define a clear TypeScript interface for the structure of an "Upcoming Journey" data object.
* Component displaying journey details should be reusable if multiple journeys are shown.
* Use Server or Client Components appropriately based on data fetching needs.

---

## 5. Required Deliverables

* [ ] Code for the enhanced "Upcoming Journeys" component/section committed.
* [ ] Confirmation/evidence of passed mandatory QA checks.
* [ ] This Task Specification file (`TASK_...md`) moved to `../Completed/`.
* [ ] (Optional) Link to deployed preview showing the updated dashboard section.

---
