![RollingDocs banner](Assets/rd-banner-temp.jpg)

# RollingDocs: An Experimental Framework for Human-AI Collaborative Development

**Author:** [Victor Anderson](https://www.linkedin.com/in/justviktor/)

[![Status](https://img.shields.io/badge/status-experimental-orange)](https://github.com/Viktor286/rolling-docs)

## Introduction

**RollingDocs is an experimental, role-based, document-driven, Human-AI team & collaborative system of development orchestration.**

_On a very high-level, it's a combination of Project/Team Management where everything is a document, everything is a prompt._

This framework explores a structured approach to managing software development projects where contributions may come from both Human experts and specialized AI models. It utilizes a system of version-controlled markdown documents stored directly within the project repository to serve as a shared knowledge base, communication protocol, and operational guide.

It could be used for improved workflow of agentic LLM tools like:
- [Claude Code](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview)
- [Aider](https://aider.chat/)
- [Cline](https://cline.bot/) / [Roo](https://roocode.com/)
- [Google (ADK)](https://google.github.io/adk-docs/)
- [crewAI](https://www.crewai.com/)
- [OpenAI Codex CLI](https://github.com/openai/codex)

## The Problem Space

Modern AI models offer significant potential in software development, but effectively integrating them into complex workflows presents challenges:

* **Context Management:** AI models often operate in stateless sessions, requiring a reliable way to load necessary project context each time.
* **Process Adherence:** Ensuring AI contributions consistently follow project standards, architecture, and quality checks.
* **Collaboration:** Facilitating seamless teamwork and handoffs between Human and AI contributors.
* **Interchangeability:** Creating a system where roles can be flexibly filled by either Humans or AI based on the task requirements and capabilities.

RollingDocs attempts to address these challenges through structured documentation and defined processes.

## Key Concepts of RollingDocs

* **Role-Based:** Work is defined by abstract **Roles** (e.g., Developer, QA, PM, Framework Guardian), each with documented responsibilities (`Description.md`) and workflows (`Instructions.md`).
* **Document-Driven:** All necessary context – project goals, technical plans, standards, tooling, task specifics – resides in version-controlled markdown files within the `RollingDocs/` directory.
* **Human-AI Interchangeability:** By defining roles via process and documentation interfaces, any capable contributor (Human or AI) can fulfill a role.
* **Task Management via File System:** Individual work units (**Task Specifications**) are managed as markdown files moved through status folders (`RollingDocs/Tasks/Planned/`, `Progress/`, `Completed/`).
* **Integrated QA:** Quality assurance checks are a mandatory, defined step in relevant workflows.
* **Framework Guardian:** A dedicated role maintains the integrity and evolution of the RollingDocs framework itself.
* **AI-Specific Directives:** Includes a convention (`[AI: ...]`) for providing explicit, mandatory instructions to AI contributors within the documentation.

## Structure Overview

The core framework documentation resides within the `/RollingDocs` directory:

* `0_About_Framework.md`: Detailed explanation of the philosophy, principles, and structure.
* `1_Onboarding_Guide.md`: The starting point for any contributor joining the workflow.
* `2_Project_Description.md` & `3_Technical_Plan.md`: Define the specific project context.
* `4_Global_Tooling.md`: Outlines shared tools and commands.
* `Roles/`: Contains subdirectories defining each specific role.
* `Templates/`: Includes templates for documents like Task Specifications.
* `Tasks/`: Contains the `Planned/`, `Progress/`, and `Completed/` subdirectories holding Task Specification files.

*(For a full breakdown, please see `RollingDocs/0_About_Framework.md`)*

## Example Project: Space Travel Booking Platform 🚀

This repository includes an initial example project, which demonstrates the *application* of the RollingDocs framework.

## Getting Started

1.  Explore the structure within the `RollingDocs/` directory.
2.  Read `RollingDocs/0_About_Framework.md` for a deep dive into the concepts.
3.  Review `RollingDocs/1_Onboarding_Guide.md` to understand the core workflow.

## Status & Contribution

RollingDocs is currently **experimental**. Feedback, ideas, and contributions are welcome.

---
