RollingDocs Framework - Session Context Summary (April 10, 2025)

1. Introduction
   This document summarizes the collaborative design process and resulting structure of the RollingDocs framework, developed during the conversational session on April 10, 2025. The goal was to create a system for effectively managing software development projects, particularly those involving collaboration between human experts and AI contributors (interchangeable roles). This summary serves as a detailed context memory, capturing the evolution of ideas and the final agreed-upon framework.

2. Initial Context & Problem Definition
   Starting Point: The session began with reviewing an existing project structure (coding-challenge-march) for a Space Travel Booking Platform, along with several markdown files defining the project, technical plan, implemented features, and initial operational instructions for an AI agent (CLAUDE.md, system-bootsrtap.md).
   Core Challenge Identified: The need for a robust, explicit system to manage AI agent contributions within a software development lifecycle, ensuring clarity, alignment, quality, and effective collaboration, especially given the potentially stateless nature of AI interactions.
3. Evolution of the RollingDocs Framework
   Through iterative discussion and refinement, we evolved the initial concept into the RollingDocs framework:

Framework Naming: Explored various names (SADF, CRF) before settling on RollingDocs to reflect the dynamic, document-driven nature.
Core Philosophy: Established the framework's purpose: using structured, version-controlled documentation as a communication protocol and operational guide for interchangeable human and AI contributors performing defined Roles.
Documentation Structure (The Cascade):
Rejected overly long filename prefixes.
Adopted a dedicated RollingDocs/ folder for framework definition documents.
Established a hierarchical structure (cascade) with numbered top-level files for consistent ordering.
Defined key document categories: Core (0_About..., 2_Project..., 3_TechPlan...), Onboarding (1_Onboarding...), Global Tooling (4_Global_Tooling...), Role-Specific (Roles/...), Templates (Templates/...), and Task Management (Tasks/...).
Role Definition:
Shifted focus from "agent" to abstract "Role" performable by human or AI.
Standardized role documentation within RollingDocs/Roles/[RoleName]/ into:
Description.md: Defines scope, responsibilities (RACI alignment).
Instructions.md: Defines step-by-step workflow and processes.
Defined key roles, including Developer (split by area like Frontend/Backend), QA, PM, and the crucial Framework Guardian.
Framework Guardian Role: Explicitly defined this role to oversee the RollingDocs framework itself – maintaining documentation integrity, managing changes to the framework (via assigned Tasks), ensuring consistency, and onboarding contributors.
Task Management:
Replaced "TSD" acronym with "Task Specification" or "Task".
Established a Kanban-like system using subfolders within RollingDocs/Tasks/:
Planned/: For defined but unstarted Task Specifications.
Progress/: For Task Specifications currently being worked on.
Completed/: For successfully finished and verified Task Specifications.
This replaces separate status markdown files (STATUS_WIP.md, STATUS_Completed_Deliverables.md). The location of the TASK_...md file indicates its status.
Formalized a Task_Specification.md template within RollingDocs/Templates/.
AI-Specific Considerations:
Acknowledged the need for explicit instructions for AI.
Introduced the [AI: ...] markup convention for mandatory AI-specific directives within documentation.
Conceptualized an AI_Bootstrap.md file/process as the absolute first context for an AI, explaining the framework and the [AI: ...] convention before it accesses the RollingDocs/ structure.
Integration of Project Management Principles: Consciously aligned the framework with concepts like RACI (via Role Descriptions), Deliverables (in Task Specs), Work Breakdown Structure (via Task Specs), Scope Management (in Task Specs), Acceptance Criteria (AC in Task Specs), Quality Management (integrated QA checks), Status Tracking (via Tasks/ folders), and Change Management (via Guardian role).
4. Final RollingDocs Structure Diagram
   [PROJECT_ROOT]/
   ├── (AI_Bootstrap.md)              # Conceptual/Loaded First: Explains [AI:...] tag & points to RollingDocs
   │
   ├── RollingDocs/
   │   ├── 0_About_Framework.md      # Detailed philosophy, principles (Extended A-Z)
   │   ├── 1_Onboarding_Guide.md     # Entry point for Role Performers
   │   ├── 2_Project_Description.md
   │   ├── 3_Technical_Plan.md
   │   ├── 4_Global_Tooling.md       # Shared commands, tools, environment
   │   │
   │   ├── Roles/                    # Role-specific Definitions & Instructions
   │   │   ├── Developer/
   │   │   │   ├── Description.md
   │   │   │   └── Instructions.md
   │   │   ├── QA/
   │   │   │   ├── Description.md
   │   │   │   └── Instructions.md
   │   │   ├── Framework_Guardian/
   │   │   │   ├── Description.md
   │   │   │   └── Instructions.md
   │   │   └── ... [Other Roles]
   │   │
   │   ├── Templates/                # Templates for framework documents
   │   │   └── Task_Specification.md
   │   │
   │   └── Tasks/                    # Task Management (Status via folder location)
   │       ├── Planned/
   │       │   └── TASK_[ID]_[Desc].md
   │       ├── Progress/
   │       │   └── TASK_[ID]_[Desc].md
   │       └── Completed/
   │           └── TASK_[ID]_[Desc].md
   │
   ├── src/                         # Source code
   ├── README.md                    # Points to RollingDocs/1_Onboarding_Guide.md
   ├── ...                          # Other project files (package.json, etc.)
5. Key Document Content Highlights (Generated during session)
   0_About_Framework.md: Provides a comprehensive explanation of the RollingDocs philosophy, core principles, structure, key concepts (Roles, Tasks, Guardian, Interchangeability, AI Instructions), and benefits. Includes a TL;DR.
   1_Onboarding_Guide.md: The main entry point for contributors, explaining the overall structure and the core task-driven workflow, emphasizing status updates via file movement and mandatory QA. Includes notes on the [AI: ...] convention.
   2_Project_Description.md: Adapted from the original project brief, defining project goals and high-level features, framed within the RollingDocs context with pointers to other documents.
   3_Technical_Plan.md: Adapted from the original technical plan, outlining architecture, stack, standards (Accessibility, Responsive Design, Performance), testing strategy, and build/deployment approach, with references to tooling and role rulebooks.
   4_Global_Tooling.md: Consolidates shared technical stack info, environment setup, crucial development/QA commands (esp. pnpm project:qa), version control guidelines, and path alias conventions. Includes warnings for AI environments.
   Templates/Task_Specification.md: A standardized template for defining individual work units (Tasks) including Goal, Scope (In/Out), Acceptance Criteria (AC), Technical Notes, and required Deliverables.
   Role Examples (Developer-Fullstack, PM, Framework_Guardian): Generated Description.md (scope, responsibilities, interactions, skills) and Instructions.md (detailed step-by-step workflow including task file movement, QA checks, specific commands, and AI instructions) for these roles.
6. Conclusion
   The RollingDocs framework, as designed in this session, represents a detailed and structured approach to managing software development in a hybrid human-AI environment. By leveraging clear documentation, defined roles, explicit task management, and integrated quality checks, it aims to provide a predictable, collaborative, and flexible system capable of orchestrating complex projects while allowing for the interchangeability of human and AI contributors.
