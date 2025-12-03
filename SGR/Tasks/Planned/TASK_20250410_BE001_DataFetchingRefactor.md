# Task Specification: TASK_20250410_BE001 - Refactor Static Data Access

**Date Created:** 2025-04-10
**Assigned Role/Area:** Developer_Fullstack (or potentially Backend Dev if role exists)
**Related Core Docs:**
* Project Description: [`../../2_Project_Description.md`](../../2_Project_Description.md)
* Technical Plan: [`../../3_Technical_Plan.md`](../../3_Technical_Plan.md) (Section 3.2 - Data Management)
* Role Documentation: [`../../Roles/Developer_Fullstack/Instructions.md`](../../Roles/Developer_Fullstack/Instructions.md)
* Related Task Specs (if any): Affects components using static data (e.g., TASK_20250403_FE002_DestListPage.md indirectly)

---

## 1. Goal

* Refactor the current static data access method (importing from `.ts` files in `src/data/`) to simulate a more realistic data fetching pattern, preparing for future API integration.

## 2. Scope

### In Scope:

* Move the static data arrays (destinations, packages, accommodations) from `.ts` files to separate `.json` files (e.g., within a `public/data/` or similar accessible location).
* Create simple utility functions (e.g., `WorkspaceDestinations()`, `WorkspacePackages()`, `WorkspacePackageById(id)`) that read and return data from these JSON files, simulating async API calls (e.g., using `async/await` and potentially a small delay).
* Update existing code (conceptually, where destinations, packages, etc., are displayed or used, like listing pages or detail pages) to use these new fetcher functions instead of direct imports.
* Ensure TypeScript types/interfaces are still correctly used for the fetched data.

### Out of Scope:

* Implementing an actual backend API or database.
* Setting up complex data fetching libraries (like SWR or TanStack Query) at this stage.
* Modifying the data content itself.
* Error handling for fetch failures (can be a future task).

---

## 3. Acceptance Criteria (AC)

* [ ] Static data resides in `.json` files.
* [ ] Utility functions exist to fetch data (all items, specific items by ID) simulating async behavior.
* [ ] Conceptual components/pages previously using direct `.ts` imports now use the fetcher functions.
* [ ] Application behavior remains unchanged (data displayed correctly where it was used before).
* [ ] TypeScript types are correctly applied to the data returned by the fetcher functions.
* [ ] All relevant mandatory QA checks (`pnpm project:qa` from `../../4_Global_Tooling.md`) MUST pass successfully.

---

## 4. Technical Notes / Constraints (Optional)

* Place JSON files in a location accessible for reading during build time or runtime (e.g., `public/data/` might work for simple simulation).
* Use native `Workspace` or simple file reading (if server-side) within the utility functions. Ensure they return Promises.
* Consider potential impact on Server vs. Client Components where data is consumed.

---

## 5. Required Deliverables

* [ ] Code for data files (`.json`), fetcher utility functions, and updated consuming components committed.
* [ ] Confirmation/evidence of passed mandatory QA checks.
* [ ] This Task Specification file (`TASK_...md`) moved to `../Completed/`.
* [ ] Notification sent to QA Role (if applicable).

---
