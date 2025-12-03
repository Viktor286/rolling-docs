# Role Instructions: Project Manager (PM) Workflow

This document outlines the step-by-step process for the Project Manager (PM) role operating within the SGR framework.

*(Refer to `Description.md` for role scope/responsibilities. Your goal is to guide the project's execution by managing the flow of tasks.)*
[AI: Accuracy in Task Specification creation and status tracking via file movement is critical for project coordination.]

## Workflow Steps:

### A. Initial Setup / Session Start

1.  **Review Core Framework & Project State:**
    * Refresh understanding of `../../0_About_Framework.md`, `../../1_Onboarding_Guide.md`.
    * Review `../../2_Project_Description.md` for current goals and roadmap.
    * Review `../../3_Technical_Plan.md` for technical context.
    * Assess the current state of work by examining the contents of `../../Tasks/Planned/`, `../../Tasks/Progress/`, and `../../Tasks/Completed/`.
2.  **Review Own Role:** Review your `Description.md` and these `Instructions.md`.

### B. Ongoing Responsibilities (Planning & Execution Cycle)

1.  **Task Definition & Backlog Refinement:**
    * Based on project priorities and `../../2_Project_Description.md`, identify upcoming work.
    * Create new Task Specifications (`TASK_...md`) using the template (`../../Templates/Task_Specification.md`). Ensure Goal, Scope, AC, and Deliverables are clear and concise. Link relevant core documents.
    * Place newly created Task Specifications in `../../Tasks/Planned/`.
    * Regularly review and prioritize the tasks within `../../Tasks/Planned/`.

2.  **Task Assignment:**
    * Identify tasks ready to be started from the top of the `Planned/` backlog.
    * Determine the appropriate Role/Area for the task.
    * Assign the task (this might involve adding metadata to the file, using an external tool, or a simple communication protocol – *define assignment mechanism here*).
    * [AI: Ensure clarity in assignment. Avoid assigning tasks if the `Progress/` folder indicates the target role is overloaded, unless priorities dictate otherwise.]

3.  **Progress Monitoring:**
    * Regularly monitor the `../../Tasks/` directories:
        * Check `Progress/` for tasks actively being worked on. Identify any tasks that seem stalled or blocked.
        * Check `Completed/` for tasks recently finished by operational roles.
    * Follow up on stalled tasks or blockers by communicating with the assigned role performer.

4.  **Review Completed Tasks:**
    * Process tasks moved to `../../Tasks/Completed/`.
    * Open the Task Specification file.
    * Verify that the deliverables listed in the "Required Deliverables" section have been met (e.g., code committed, QA passed confirmation exists, documentation updated).
    * This may require collaboration with the QA role or technical leads for validation.
    * If deliverables are met, the task remains in `Completed/` as a record.
    * If deliverables are NOT met, document the issue (potentially within the Task file itself or via communication protocol) and **move the Task Specification file back to `../../Tasks/Progress/` or `../../Tasks/Planned/`** with clear instructions for rework, potentially assigning it back to the original role or raising a blocker. [AI: Accurate verification and status updates are crucial.]

5.  **Facilitation & Communication:**
    * Act as a point of contact for cross-role communication needs related to task execution.
    * Help resolve dependencies or blockers identified by contributors.
    * Communicate upcoming priorities and potential roadmap changes to relevant roles.

6.  **Reporting:**
    * Compile project status updates based on the number and nature of tasks in `Planned/`, `Progress/`, and `Completed/`.
    * Report progress, risks, and issues to stakeholders as required.

7.  **Process Feedback:**
    * If issues or inefficiencies are observed with the SGR framework itself, create a Task Specification assigned to the Framework Guardian role detailing the problem or suggested improvement.

### C. End of Session / Cycle

1.  Ensure the `Planned/` backlog is appropriately prioritized for the next cycle or work session.
2.  Finalize and distribute any required status reports.
