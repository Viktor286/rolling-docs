# Role Instructions: Developer - Fullstack Workflow

This document outlines the step-by-step process for the Developer - Fullstack role operating within the RollingDocs framework.

*(Refer to `Description.md` for role scope/responsibilities and `Rulebook.md` for detailed standards.)*
[AI: Strict adherence to these steps, especially QA checks and status updates, is mandatory.]

## Development Cycle Steps:

1.  **Task Acquisition:**
    * Monitor `../../Tasks/Planned/` for newly assigned Task Specifications or receive assignment notification.
    * When ready to begin work, **move** the relevant `TASK_...md` file from `Planned/` to `../../Tasks/Progress/`.
    * [AI: Verify the task scope aligns with the Fullstack Developer role as defined in `Description.md` and project needs.]

2.  **Understand & Plan:**
    * Thoroughly read the entire Task Specification (`TASK_...md`) in the `Progress/` folder.
    * Review all linked sections in `../../2_Project_Description.md`, `../../3_Technical_Plan.md`, and any other referenced documents.
    * Consult `Rulebook.md` for relevant coding standards, patterns, or specific technical guidelines.
    * Plan your implementation approach, considering component design, data flow, testing strategy, and potential interactions.
    * [AI: Identify any ambiguities or required interactions with other roles (e.g., Security, Content) based on the Task Specification and request clarification or initiate consultation if necessary, following defined protocols.]

3.  **Implement Code:**
    * Write or modify code within the `src/` directory (or other designated source code locations).
    * Strictly adhere to the architecture (`../../3_Technical_Plan.md`), coding standards (`Rulebook.md`), and the specific requirements and Acceptance Criteria (AC) defined in the Task Specification.
    * Use path aliases (`@/*`) as specified in `../../4_Global_Tooling.md`.

4.  **Local Testing:**
    * Implement and run necessary unit and/or integration tests alongside your code, as required by the project's testing strategy (`../../3_Technical_Plan.md`) and `Rulebook.md`.
    * Perform manual testing during development as needed to verify functionality.

5.  **Apply Code Standards:**
    * Run the combined auto-fixing command: `pnpm project:autofix` (from `../../4_Global_Tooling.md`).
    * Manually address any remaining linting or style issues reported by `pnpm lint` that were not auto-fixed.

6.  **Type Check:**
    * Run the type checking command: `pnpm typecheck` (from `../../4_Global_Tooling.md`).
    * [AI: You MUST resolve ALL reported TypeScript errors before proceeding.]

7.  **Mandatory QA Check:**
    * Run the full project quality assurance command: `pnpm project:qa` (from `../../4_Global_Tooling.md`).
    * [AI: This command MUST pass successfully. Analyze any failures (lint, type check, build), fix the root cause in the code, and re-run `pnpm project:qa` until it passes cleanly. Ensure build error checking is enabled (`ignoreBuildErrors: false` in `next.config.ts`). DO NOT proceed if this check fails.]

8.  **Task Completion & Status Update:**
    * Once the mandatory QA check passes AND all Acceptance Criteria in the Task Specification are met:
    * **Move** the `TASK_...md` file from `../../Tasks/Progress/` to `../../Tasks/Completed/`.
    * [AI: This file move is the primary signal that the task is complete from the development perspective.]

9.  **Commit & Finalize Deliverables:**
    * Stage **all** relevant changes using `git add`. This MUST include:
        * All new or modified source code files.
        * The Task Specification file now located in `../../Tasks/Completed/`.
    * Commit the changes (follow commit conventions if defined in `Rulebook.md` or `../../4_Global_Tooling.md`).
    * Ensure all other deliverables listed in the Task Specification are met and accessible (e.g., links to deployed previews if required).

10. **Notify / Handoff:**
    * Follow any notification or handoff procedures defined in this document or the `Rulebook.md` (e.g., notify the QA role that a task is ready for verification, update a project management tool if used).

---

*Remember to consult `Rulebook.md` for detailed standards and `../../4_Global_Tooling.md` for command references.*

