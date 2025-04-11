# Task Specification: TASK_20250405_FE003 - Implement Destination Booking Form

**Date Created:** 2025-04-05
**Assigned Role/Area:** Frontend Dev
**Related Core Docs:**
* Project Description: [`../../2_Project_Description.md`](../../2_Project_Description.md) (Section 2.1)
* Technical Plan: [`../../3_Technical_Plan.md`](../../3_Technical_Plan.md)
* Data Source: `src/data/destinations.ts` (for available dates, prices)
* Related TSDs (if any): Assumes individual destination pages exist (or are part of this task if scoped broadly). Let's assume page exists.

---

## 1. Goal

* Implement the interactive booking form component on the individual destination detail pages, allowing users to select options and see calculated prices.

## 2. Scope

### In Scope:

* Develop a form component for booking a trip to a specific destination.
* Include form elements for:
    * Date selection (using `availableDates` from the destination data).
    * Number of travelers input (e.g., simple number input).
    * Seat class selection (Economy, Business, Luxury using radio buttons or dropdown).
* Implement dynamic price calculation based on selected seat class and number of travelers.
* Display the calculated total price clearly.
* Include a "Book Now" / "Confirm Booking" button (functionality behind button is out of scope).
* Ensure basic form validation (e.g., date selected, travelers > 0).
* Integrate this component into the individual destination page layout.
* Ensure the form is responsive.

### Out of Scope:

* Actual booking submission logic / API integration.
* Payment processing.
* User authentication integration.
* Saving booking details.
* Complex validation rules beyond basic presence/range checks.

---

## 3. Acceptance Criteria (AC)

* [x] Booking form component renders on individual destination pages.
* [x] Date selector only shows available dates for the specific destination.
* [x] User can input the number of travelers (e.g., 1 or more).
* [x] User can select one seat class (Economy, Business, Luxury).
* [x] Total price dynamically updates based on selected class * number of travelers, using prices from destination data.
* [x] Basic validation prevents submission if required fields (date, travelers) are empty or invalid.
* [x] "Book Now" button is present.
* [x] Form layout is responsive and usable on mobile, tablet, and desktop.
* [x] Form elements are accessible (labels, keyboard navigation).
* [x] All relevant QA checks (`pnpm project:qa`) MUST pass.

---

## 4. Technical Notes / Constraints

* This component will likely need to be a Client Component due to its interactive nature.
* State management for form inputs and calculated price needed (e.g., React `useState`).
* Use data types/interfaces from `src/data/destinations.ts`.
* Style using Tailwind CSS.

---

## 5. Required Deliverables

* [x] Code for the booking form component and integration into destination page committed.
* [x] Confirmation of passed `pnpm project:qa` check.
* [x] This TSD file moved to `../../Tasks/Completed/`.

---
