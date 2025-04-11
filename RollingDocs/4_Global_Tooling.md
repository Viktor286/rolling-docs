# 4_Global_Tooling.md: Global Tooling & Commands Guide

## 1. Introduction

This document lists common tools, commands, environment details, and conventions relevant to **all roles** working on the Space Travel Booking Platform within the RollingDocs framework. Specific roles may have additional tooling details or nuanced usage instructions documented in their respective `Roles/[RoleName]/Tooling.md` or `Roles/[RoleName]/Instructions.md` files.

*(Refer to `1_Onboarding_Guide.md` for the overall workflow context and `3_Technical_Plan.md` for architectural context.)*

## 2. Core Technologies & Stack

* **Language:** TypeScript
* **Framework:** Next.js 15 (App Router) / React 19
* **Styling:** Tailwind CSS v4 (Note: `2_Project_Description.md` originally mentioned v3, but v4 is installed)
* **Package Manager:** pnpm

*(Detailed versions are managed in `package.json` and `pnpm-lock.yaml`.)*

## 3. Environment Setup

* **Node.js:** Requires Node.js (version >=18 recommended based on typical Next.js requirements - verify specific needs if issues arise).
* **Dependencies:** Install project dependencies from the project root directory using:
    ```bash
    pnpm install
    ```
  *(Based on common pnpm usage)*

## 4. Key Development & Quality Commands

Execute these commands from the project root directory (`coding-challenge-march/app/`).

### 4.1. Development Server

* `pnpm dev --turbopack`: Starts the Next.js development server with Turbopack for fast updates.
* **[AI: IMPORTANT WARNING]** As noted in foundational instructions, **NEVER run `pnpm dev`, `pnpm start`, or `pnpm project:hard-start` if operating within a restricted execution environment** where long-running processes might cause hangs or instability. Consult your role-specific instructions (`Roles/[RoleName]/Instructions.md`) for guidance on development environments.

### 4.2. Code Formatting (Prettier)

* `pnpm format`: Automatically formats code according to Prettier rules defined in the project.
* `pnpm format:check`: Checks if code formatting is correct without modifying files. Useful in CI/QA checks.

### 4.3. Linting / Static Analysis (ESLint)

* `pnpm lint`: Runs ESLint to identify potential code quality issues, style violations, and errors based on rules in `eslint.config.mjs`.
* `pnpm lint:fix`: Runs ESLint and automatically fixes fixable issues.

### 4.4. Type Checking (TypeScript)

* `pnpm typecheck`: Runs the TypeScript compiler (`tsc --noEmit`) to check for type errors based on `tsconfig.json`.

### 4.5. Combined Quality Checks

* `pnpm project:autofix`: Convenience script that runs `pnpm format` and `pnpm lint:fix`.
* `pnpm project:check`: Runs `project:autofix`, then verifies results with `pnpm lint`, `pnpm format:check`, and `pnpm typecheck`.

### 4.6. Production Build

* `pnpm build`: Creates an optimized production build of the Next.js application in the `.next/` directory.

### 4.7. MANDATORY Quality Assurance (QA) Check

* **Command:** `pnpm project:qa`
* **Action:** This script runs `project:check` and then `pnpm build`.
* **Requirement:** This command **MUST pass successfully** before any task involving code changes can be considered complete (i.e., before moving a Task Specification to `RollingDocs/Tasks/Completed/`).
* **Configuration Note:** Ensure TypeScript build error checking is enabled (`typescript.ignoreBuildErrors: false` in `next.config.ts`) during QA phases, as recommended in `3_Technical_Plan.md`.

## 5. Version Control (Git)

* **System:** Git is assumed.
* **Staging:** Use `git add [files]` to stage changes. Remember to include:
    * All modified/new source code files (`src/`, etc.).
    * The moved Task Specification file (now in `RollingDocs/Tasks/Completed/`).
    * Any other documentation files updated as part of the task deliverables. *(Based on workflow)*
* **Branching/Commits:** (Define project-specific strategy here or reference a dedicated section/document if complex. E.g., feature branches, Conventional Commits).

## 6. Path Aliases

* Use the `@/*` alias for imports referencing the root of the `app/` or `src/` directory (as configured in `tsconfig.json`). Example: `import { SomeComponent } from '@/components/SomeComponent';`

---

This document provides the essential global tooling context. Remember to consult your specific Role documentation (`Roles/[RoleName]/...`) for workflow integration and role-specific details.
