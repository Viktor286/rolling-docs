# Task Specification: TASK_20250403_FE002 - Create Destinations Listing Page

**Date Created:** 2025-04-03
**Assigned Role/Area:** Frontend Dev
**Related Core Docs:**
* Project Description: [`../../2_Project_Description.md`](../../2_Project_Description.md) (Section 2.1 - Trip Scheduling/Booking)
* Technical Plan: [`../../3_Technical_Plan.md`](../../3_Technical_Plan.md)
* Data Source: `src/data/destinations.ts`
* Related TSDs (if any): TASK_20250401_FE001_HomepageHero.md (as entry point)

---

## 1. Goal

* Develop the main listing page displaying all available space destinations, allowing users to browse options.

## 2. Scope

### In Scope:

* Create the main page layout for `/destinations`.
* Fetch and display destination data from `src/data/destinations.ts`.
* Implement interactive cards for each destination showing key info: Name, Type, Distance, Travel Time, Description (brief), Starting Price (lowest economy price), Image.
* Implement basic filtering controls (e.g., by destination type: orbital, lunar, station).
* Add a "View Details" button on each card linking to the individual destination page (path TBD).
* Ensure the page is responsive (Mobile, Tablet, Desktop).

### Out of Scope:

* Implementation of the individual destination detail pages (separate task).
* Advanced filtering or sorting functionality.
* Pagination (display all destinations initially).
* Real-time availability checking.

---

## 3. Acceptance Criteria (AC)

* [x] Page renders at `/destinations` route.
* [x] All destinations from `src/data/destinations.ts` are displayed as cards.
* [x] Each card displays Name, Type, Distance, Travel Time, Description, Image, and correct starting Economy price.
* [x] Filtering controls allow users to show only destinations of a specific type (orbital, lunar, station).
* [x] "View Details" button exists on each card (link destination TBD, can be `#` initially).
* [x] Page layout is responsive and usable on all target screen sizes.
* [x] Basic accessibility checks pass (semantic structure, keyboard navigation for filters/buttons).
* [x] All relevant QA checks (`pnpm project:qa`) MUST pass.

---

## 4. Technical Notes / Constraints

* Use Next.js App Router conventions. Likely a Server Component for initial load.
* Filtering might require Client Component interaction.
* Use data types/interfaces defined in `src/data/destinations.ts`.
* Style using Tailwind CSS according to project theme.

---

## 5. Required Deliverables

* [x] Code for the destinations listing page and destination card component(s) committed.
* [x] Confirmation of passed `pnpm project:qa` check.
* [x] This TSD file moved to `../../Tasks/Completed/`.

---
