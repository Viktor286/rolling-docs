# Role Instructions: Framework Guardian Workflow

This document outlines the step-by-step process for the Framework Guardian role operating within the SGR framework.

*(Refer to `Description.md` for role scope/responsibilities. The goal is to maintain and improve the SGR framework itself.)*
[AI: Your primary focus is the integrity and evolution of the documentation within the `../../` directory, excluding `Tasks/`. Strict adherence to process is crucial.]

## Workflow Steps:

### A. Initial Setup / Session Start

1.  **Review Core Framework:** Refresh understanding by reviewing `../../0_About_Framework.md` and `../../1_Onboarding_Guide.md`.
2.  **Review Own Role:** Review your `Description.md` and these `Instructions.md`.
3.  **Check Assigned Tasks:** Examine `../../Tasks/Planned/` for any Task Specifications assigned specifically to the Framework Guardian role.
4.  **Check Ongoing Tasks:** Review any Task Specifications already assigned to you residing in `../../Tasks/Progress/`.
5.  **Contextual Scan (Optional):** Briefly review recent entries in `../../Tasks/Completed/` to understand recent project activity and potential impacts on the framework.

### B. Ongoing Responsibilities (During Development Cycles)

1.  **Monitor Framework Health:**
    * Periodically review key framework documents for clarity, consistency, and accuracy.
    * Identify potential ambiguities, outdated information, or areas for improvement. If significant improvements are needed, create a new Task Specification in `../../Tasks/Planned/` assigned to yourself detailing the proposed change.

2.  **Process Framework Change Tasks:**
    * **Task Acquisition:** When ready to work on an assigned framework change Task, move the `TASK_...md` file from `../../Tasks/Planned/` to `../../Tasks/Progress/`.
    * **Understand & Analyze:** Thoroughly read the Task Specification. Analyze the requested change against SGR principles (`../../0_About_Framework.md`) and its potential impact on other documents or roles.
    * **Clarify (If Needed):** If the request is unclear or potentially problematic, engage with the requester (via comments within the Task file or other agreed communication channels) for clarification *before* implementing. [AI: Do not implement ambiguous framework changes.]
    * **Implement Changes:** Modify the relevant SGR file(s) within the `../../` directory (e.g., update `3_Technical_Plan.md`, refine a `Roles/.../Instructions.md`, update a template in `Templates/`). Ensure changes are clear and well-documented within the file itself if necessary.
    * **Verify Consistency:** After changes, check related documents for any required consequential updates to maintain consistency (e.g., update references in `1_Onboarding_Guide.md` if a file name changes).
    * **Tooling Checks (If Applicable):** Run any relevant tooling checks defined in `../../4_Global_Tooling.md` for documentation (e.g., markdown linting, link checking, if configured).
    * **Task Completion & Status Update:** Once changes are implemented, verified, and meet the Task Specification's AC: Move the `TASK_...md` file from `Progress/` to `Completed/`.
    * **Commit & Finalize Deliverables:** Stage the modified framework document(s) AND the moved Task Specification file using `git add`. Commit changes following project conventions. Ensure all Deliverables from the Task Specification are met.
    * **Communicate Changes:** Announce significant framework changes to relevant roles according to defined project communication protocols (e.g., team chat message, meeting announcement - specify protocol here or in `Description.md`).

3.  **Onboarding & Support:**
    * Respond to contributor questions regarding SGR processes or documentation clarity.
    * Guide new contributors to the relevant documentation (`1_Onboarding_Guide.md`, role-specific docs).

4.  **Process Auditing (If Part of Defined Role):**
    * Periodically review the state of `../../Tasks/` folders (e.g., are Tasks moving correctly? Are completed Tasks fully delivered?).
    * Check commit history or other logs for adherence to key processes (e.g., QA checks before completion).
    * Report findings or suggest process clarifications via new Tasks assigned to the Guardian role.

### C. End of Session / Cycle

1.  Ensure all active Guardian Tasks are correctly placed in `../../Tasks/Progress/` or `../../Tasks/Completed/`.
2.  Commit any pending changes to framework documentation.
