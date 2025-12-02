# RollingDocs: Document-driven operating system for Human-AI development

**Author:** [Victor Anderson](https://www.linkedin.com/in/justviktor/)

[![Status](https://img.shields.io/badge/status-experimental-orange)](https://github.com/Viktor286/rolling-docs)

## Introduction

**RollingDocs is an experimental, role-based, document-driven operating system for Human-AI development.**

At a high level, it transforms a code repository into a self-managing database where **everything is a document** and **everything is a prompt**.

This framework explores a structured approach where project management, architecture, and code contributions are handled interchangeably by Humans and specialized AI Agents. It utilizes a system of version-controlled markdown documents to serve as a shared knowledge base and operational guide, allowing AI agents to understand *how* to work, not just *what* to code.

It is designed to improve the workflow of agentic LLM tools like:

- [Claude Code](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview)
- [OpenAI Codex CLI](https://github.com/openai/codex)
- [Gemini CLI](https://github.com/google-gemini/gemini-cli)
- [Cursor](https://github.com/cursor/cursor)
- [Cline](https://cline.bot/) / [Roo](https://roocode.com/)
- and others...

## The Problem Space

Modern AI models offer significant potential in software development, but effectively integrating them into complex workflows presents challenges:

* **Context Amnesia:** AI models operate in stateless sessions. They often lack the "Big Picture" stored in external tools like Jira or Trello.
* **Process Adherence:** Ensuring AI contributions consistently follow project standards, architecture, and quality checks without constant human hand-holding.
* **Management Overhead:** Humans often spend more time prompting and organizing AI outputs than coding.
* **True Interchangeability:** Most workflows treat AI as a "tool" and Humans as "managers." RollingDocs aims for a system where **roles (including Project Management and QA) can be flexibly filled by either Humans or AI Agents.**

## Key Concepts of RollingDocs

* **Role-Based Abstraction:** Work is defined by abstract **Roles** (e.g., *Developer*, *QA*, *Product Owner*, *Framework Guardian*). Each role has a `Description.md` and `Instructions.md`. An AI agent simply reads the instructions to "become" that role.
* **Document-Driven Context:** All necessary context—requirements, status, and architectural decisions—resides in the `RollingDocs/` directory. The file system *is* the source of truth.
* **Agentic Project Management:** The **Project Manager** and **Framework Guardian** roles are designed to be fulfillable by AI. This means an AI agent can be responsible for organizing the Kanban board, cleaning up stale files, and enforcing repository rules.
* **Task Management via File System:** Individual work units (**Task Specifications**) are managed as markdown files. Moving a file from `Planned/` to `Progress/` is a native file-system operation, allowing agents to manage state without external API integrations.
* **Integrated QA:** Quality assurance checks are a mandatory, defined step in the workflow, executable by a specialized QA Agent.
* **AI-Specific Directives:** Includes a convention (`[AI: ...]`) for embedding system prompts directly into the project documentation.

## Structure Overview

The core framework documentation resides within the `/RollingDocs` directory:

* `0_About_Framework.md`: The "Constitution" of the project—philosophy, principles, and structure.
* `1_Onboarding_Guide.md`: The starting point for any contributor (Human or Artificial).
* `2_Project_Description.md` & `3_Technical_Plan.md`: Define the specific project context.
* `Roles/`: Contains the specific `Instructions.md` that allow an Agent to adopt a persona (e.g., "You are now the Framework Guardian").
* `Templates/`: Boilerplate for creating new Task Specifications.
* `Tasks/`: The file-system Kanban board containing `Planned/`, `Progress/`, and `Completed/` folders.

*(For a full breakdown, please see `RollingDocs/0_About_Framework.md`)*

## Example Project: Space Travel Booking Platform 🚀

This repository includes an initial example project to demonstrate the *application* of the RollingDocs framework in a live scenario.

## Getting Started

1.  Explore the structure within the `RollingDocs/` directory.
2.  Read `RollingDocs/0_About_Framework.md` for a deep dive into the philosophy.
3.  Review `RollingDocs/1_Onboarding_Guide.md` to understand the core workflow.

## Status & Contribution

RollingDocs is currently **experimental**. Feedback, ideas, and contributions—whether from biological or digital entities—are welcome.

-----