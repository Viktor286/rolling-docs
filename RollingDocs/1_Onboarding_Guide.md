# 1_Onboarding_Guide.md: The SGR Core Process

## 1. Welcome & Your Role

Hello! You are an expert contributor tasked with performing a specific **Role** within this software development project. Welcome aboard!

This project utilizes the **SGR** framework – a system designed to manage development using structured documentation as a _shared knowledge base_ and _operational guide_. It supports collaboration between **Human and AI contributors** through clearly defined processes and roles.

It is important that you
1. understand requirements relevant to your Role
2. perform your tasks according to defined processes and standards
3. ensure quality
4. maintain accurate status documentation by managing Task Specification files within the designated structure.

This guide outlines the general SGR process all contributors MUST follow. Please, familiarize yourself with it thoroughly at the start of each work session.

*(Note: If you an AI contributor, you should have first read & processed an initial context file `AI_Bootstrap.md`, explaining the `[AI: ...]` convention used in some documents for specific instructions directed solely at AI.)*
[AI: It is very IMPORTANT that you MUST follow these instructions and the instructions in your Role-specific documents thoroughly!]

## 2. Documentation Structure (The SGR Cascade)

The SGR framework organizes information hierarchically within the `SGR/` directory:

1.  **`SGR/` - Core Framework Definition, Guides, Rules:**
    * `0_About_Framework.md`: Detailed philosophy, principles, and overview of SGR.
    * `1_Onboarding_Guide.md`: This document! Your primary guide to the core workflow.
    * `2_Project_Description.md`: Core project goals, vision, features.
    * `3_Technical_Plan.md`: Architecture, technical principles, design guidelines.
    * `4_Global_Tooling.md`: Common commands, tools, environment details shared across roles.
    * `Roles/`: Contains subfolders for each defined Role (e.g., `Developer/`, `QA/`, `Framework_Guardian/`) holding their specific `Description.md` (Role definition) and `Instructions.md` (Workflow steps).
    * `Templates/`: Contains templates, like `Task_Specification.md`.
    * `Tasks/`: Central hub for task management via subfolders using Task Specification files (`TASK_...md`):
        * `Planned/`: Holds Task Specifications for planned work.
        * `Progress/`: Holds Task Specifications for work currently in progress.
        * `Completed/`: Holds Task Specifications for successfully completed and verified work.

## 3. Roles & The Framework Guardian

This framework supports various specialized Roles (Developer, QA, PM, Security Advisor, etc.). Each Role interfaces via its documents in `SGR/Roles/[RoleName]/`, primarily `Description.md` and `Instructions.md`.

The **Framework Guardian** role is responsible for maintaining the integrity, consistency, and evolution of the SGR framework documentation itself (all files within `SGR/` except the `Tasks/` subfolder). Changes to framework documents require a Task assigned to the Framework Guardian.

[AI: You MUST NOT modify files outside the `SGR/Tasks/` directory unless your assigned Role is Framework Guardian and the Task explicitly requires it.]

## 4. Human-AI Interchangeability

A core feature of SGR is that Roles are defined by documented processes (`Instructions.md`) and responsibilities (`Description.md`). Any contributor (Human expert or capable AI model) that can adhere to the documented protocol for a Role can perform that Role's tasks.

## 5. The Workflow (Role-Centric & Task-Driven)

The building block of work is the **Task Specification** document (`TASK_...md`). We use the `SGR/Tasks/` subfolders (`Planned/`, `Progress/`, `Completed/`) as a Kanban-style board.

1.  **Task Initiation (e.g., PM / Team Lead):** Creates a Task Specification (`TASK_...md`) using the template from `SGR/Templates/` and places it in `SGR/Tasks/Planned/`, assigning it to the relevant Role/*.
2.  **Task Start:** Assigned Role Performer moves the Task Specification file from `Planned/` to `Progress/`. Consult your Role's `Instructions.md` first.
3.  **Context Loading:** Understand the assigned Task Specification and load necessary context by reading linked/referenced documents (`2_Project_Description.md`, `3_Technical_Plan.md`, `4_Global_Tooling.md`, your `Roles/[RoleName]/Instructions.md` & `Roles/[RoleName]/Description.md`).
4.  **Execution Cycle:** Perform the task according to your Role's `Instructions.md` and `Description.md`. Use specified tooling (`4_Global_Tooling.md`). Every development cycle includes mandatory QA checks. Iterate until Acceptance Criteria (AC) in the Task Specification are met and QA passes. [AI: Pay close attention to any `[AI: ...]` instructions in your Role documents.]
5.  **Task Completion & Handoff:** Upon successful completion:
    * Move the Task Specification file from `Progress/` to `Completed/`.
    * Follow notification/handoff protocol defined in your Role's `Instructions.md`.
6.  **Deliverable Finalization:** Commit/store artifacts as specified in the Task Specification's Deliverables section (this usually includes committing code AND the final Task Specification location in `SGR/Tasks/Completed/`).

## 6. Integrated Project Management Concepts
SGR integrates key PM principles: Role Definition, Deliverable Specification, Work Breakdown, Scope Management, Acceptance Criteria, Quality Management, Status Tracking (via Task location), and Change Management (via Guardian role/process).
