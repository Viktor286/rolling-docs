# The RollingDocs (experimental) Framework

A role-based, document-driven, Human-AI collaborative system of development orchestration.

It could be used for improved workflow of agentic LLM tools like:
- [Claude Code](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview)
- [Aider](https://aider.chat/)
- [Cline](https://cline.bot/) / [Roo](https://roocode.com/)
- [Google (ADK)](https://google.github.io/adk-docs/)
- [crewAI](https://www.crewai.com/)

**TL;DR**

* **What:** RollingDocs manages human/AI software development via structured docs (`RollingDocs/` folder). **Crucially, it provides a clear onboarding path for stateless AI sessions.**. It's like prompt template on ~~steroids~~ markdown files with kanban features. Version-based AI/Person instructions and project management documentation.
* **How:** Defines **Roles** (`Roles/...`) via markdown documents, and assigned **Tasks** moved through folders (`Planned, Progress, Completed`), relies on core docs (`Project_Description.md`, etc.) & tooling guides (`Global_Tooling.md`).
* **Why:** Clarity, Quality, Alignment, Traceability, and **Human-AI Interchangeability**.
* **Goal:** Effective, high-quality collaboration in hybrid human-AI teams.

## 1. Introduction: Purpose & Philosophy

**RollingDocs** is a structured framework designed to manage and facilitate collaborative software development projects involving contributions from both **human experts and specialized AI models like agentic LLMs**.

**Core Philosophy:** The framework leverages a version-controlled, document-driven system stored directly within the project repository (primarily within this `RollingDocs/` directory). These documents serve as a shared knowledge base, a precise communication protocol, and an operational guide for all contributors.

**Goals:** RollingDocs aims to achieve:

* **Clarity:** Unambiguous definition of project goals, technical plans, roles, responsibilities, processes, and tasks.
* **Alignment:** Ensuring all contributions (human or AI) consistently align with project objectives and standards.
* **Quality:** Integrating mandatory quality assurance checks directly into the workflow.
* **Traceability:** Maintaining a clear record of completed work and task progression.
* **Flexibility & Interchangeability:** Defining roles based on processes and interfaces, allowing humans and AI to fulfill roles interchangeably based on capability and need.
* **Effective Collaboration:** Providing a structured environment for seamless teamwork between diverse contributors.

## 2. Core Principles of RollingDocs

The framework operates based on these fundamental principles:

* **Role-Based Work:** Tasks are assigned to specific Roles (e.g., Developer, QA, Framework Guardian), each defined by its scope, responsibilities, and operational instructions.
* **Document-Driven Context:** All necessary context (project goals, technical plans, standards, tooling, task specifics) is provided through version-controlled markdown documents within the defined structure. Contributors rely on these documents as the source of truth. By default, all documents are written for both AI Agent and Person but some files or texts are for AI Agents ONLY.
* **Human-AI Interchangeability:** Roles are defined abstractly by their processes and required interactions with the documentation system, allowing either humans or capable AI models to perform them effectively.
* **Explicit Task Management:** Work is broken down into discrete Task Specifications, managed through a clear lifecycle (Planned -> Progress -> Completed) represented by their location within the file structure.
* **Integrated Quality Assurance:** QA checks are a mandatory, non-negotiable step within the workflow for relevant roles (e.g., Development).
* **Process Guardianship:** A dedicated "Framework Guardian" role (AI Agent or Person) ensures the integrity, consistency, and evolution of the RollingDocs framework itself.
* **Stateless Onboarding:** The framework provides a predictable discovery path (starting from initial context like `AI_Bootstrap.md` -> `1_Onboarding_Guide.md` -> Role-specific docs) ensuring any contributor, especially AI models starting sessions without prior context, can reliably acquire necessary project information and operational instructions.

## 3. Documentation Structure Overview

RollingDocs uses a cascaded structure primarily within this directory:

```
[PROJECT_ROOT]/
├── RollingDocs/
│   ├── 0_About_Framework.md        # This document. Explaining the overall system.
│   ├── 1_Onboarding_Guide.md       # The primary entry point for any contributor; outlines the core workflow.
│   ├── 2_Project_Description.md    # Defines project-specific "What" and "Why" – goals, features, vision.
│   ├── 3_Technical_Plan.md         # Defines the conceptual "How" – architecture, technical principles.
│   ├── 4_Global_Tooling.md         # Specifies shared tools, commands, and environment setup.
│   ├── AI_Bootstrap.md             # Entry point info/prompt for AI (presumably, for the start of brand-new session).
│   │
│   ├── Roles/                      # Role-specific Definitions & Instructions.
│   │   ├── Developer_Fullstack/            # Role reflects area of expertise.
│   │   │   ├── Description.md      # Describes the role scope, responsibilities, guidelines.
│   │   │   └── Instructions.md     # Details the step-by-step workflow and operational procedures for the role.
│   │   └── ...
│   │
│   ├── Templates/                  # Holds templates for framework documents, e.g. `Task_Specification.md`.
│   │   └── Task_Specification.md   # Defines the shape of the Task (e.g. could be JIRA compatible)
│   │
│   └── Tasks/                      # Task Management similar to kanban; status managed by file system folder
│       ├── Planned/
│       │   └── TASK_[ID]_[Desc].md # individual Task Specification markdown file prepared by/for AI/Person
│       ├── Progress/
│       │   └── TASK_[ID]_[Desc].md
│       └── Completed/
│           └── TASK_[ID]_[Desc].md
```


## 4. Key Concepts

* **Roles:** Abstract definitions of functions within the project (e.g., Developer, QA, PM, Framework Guardian). Each role has clearly documented responsibilities (`Description.md`) and processes (`Instructions.md`).
* **Task Specifications (`TASK_...md`):** The atomic unit of work. Each Task is defined in its own markdown file using the template in `Templates/`. Key elements include Scope, Acceptance Criteria (AC), and Deliverables. Tasks move between `Tasks/Planned/`, `Tasks/Progress/`, and `Tasks/Completed/` folders to indicate status.
* **Framework Guardian:** A crucial role responsible for maintaining the RollingDocs framework documents themselves. Changes to guides, templates, or core project/technical docs require a Task assigned to the Guardian for review and implementation, ensuring process integrity. The Guardian also aids onboarding and suggests framework improvements.
* **Human-AI Interchangeability:** Enabled by the focus on documented processes. If a contributor (human or AI) can understand and follow the `Instructions.md` for a role and interact with the required documents (e.g., read a Task Specification, run commands from `4_Global_Tooling.md`, update Task location), they can fulfill that role. This allows leveraging the best contributor for the task, promoting hybrid teams. (Analogous to the Dependency Inversion Principle in SOLID).
* **AI-Specific Instructions (`[AI: ...]`)**: Where necessary for extreme clarity for AI contributors, instructions may be embedded within markdown using the `[AI: ...]` syntax. Any AI operating within this framework MUST be bootstrapped (e.g., via an initial `AI_Bootstrap.md` context) to recognize and strictly follow these specific directives.

## 5. Benefits Summary

Implementing the RollingDocs framework provides:

* **Enhanced Clarity & Reduced Ambiguity** for all contributors.
* **Improved Consistency & Alignment** with project goals and standards.
* **Integrated Quality Control** through mandatory process steps.
* **Clear Traceability & Status Tracking** via the `Tasks/` folder structure.
* **Unprecedented Flexibility** through human-AI role interchangeability.
* **Structured Collaboration** within hybrid teams.
* **Scalability** by providing a clear structure for adding new roles and managing complex workflows.

## 6. Conclusion

RollingDocs provides a robust, adaptable system for structuring and managing software development in a new era of human-AI collaboration. By emphasizing clear documentation, defined roles, and verifiable processes, it aims to enable teams to build high-quality software effectively and predictably.
