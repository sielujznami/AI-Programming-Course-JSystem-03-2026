# Repository Guidelines

This file is the root instruction set for all agents working in this repository. Keep changes aligned with the product, architecture, and design documents, and do not treat a task as done until the changed scope is verified.

## Primary References
- `docs/loan-decision-copilot-prd.md` - product requirements and user flows
- `docs/loan-decision-copilot-adr-and-implementation-plan.md` - architecture decisions and implementation direction
- `docs/nbp-design-system.md` - UI language, brand rules, and design tokens

Read the relevant sections before implementing. If code, comments, config, or docs contradict these files, bring them back into alignment.

## Specialist Instructions
- `backend/AGENTS.md` - backend-specific rules
- `frontend/AGENTS.md` - frontend-specific rules

These files are placeholders today, but agents must check them before working in those areas and follow them once they are populated.

## Current Stack
- Backend: Spring Boot `3.5.9`, Java `21`, Maven, Spring AI `1.1.0`, LangGraph4j `1.8.8`, AG-UI Java SDK `0.0.1`
- Frontend: Next.js `15.4.8`, React `18.3.1`, TypeScript `5`, CopilotKit `1.53.0`, AG-UI client `0.0.35`, Tailwind CSS `4`
- Runtime config: OpenRouter settings come from `.env` and `backend/src/main/resources/application.yml`

## Project Structure
- `backend/` - Spring Boot app, with code in `src/main/java`, config in `src/main/resources`, tests in `src/test/java`
- `frontend/` - Next.js App Router app, currently centered in `src/app`
- `docs/` - PRD, ADR/implementation plan, design system
- `scripts/` - setup and local run scripts for Windows and Bash
- `docker/` - PostgreSQL init assets for `compose.yaml`
- `ag-ui/` - external submodule; do not modify unless the task explicitly requires it

Frontend structure will grow beyond the current starter shape. Keep new code organized and predictable as the app expands: separate route files, reusable UI components, domain logic, and tests instead of letting everything accumulate inside `src/app/page.tsx`.

## Workflow
1. Read the relevant PRD, ADR, and design system sections first.
2. Read the area-specific `AGENTS.md` if the task touches `backend/` or `frontend/`.
3. Define the expected behavior from the specification before changing code.
4. Use TDD for every feature and bug fix.
5. Verify the changed scope completely before committing.
6. Commit only after the scope is in a working state.

Keep commits focused and granular. Do not push to remote unless the user explicitly asks.

## TDD Rules
For every feature or bug fix:
1. Start from the specification, not from the existing implementation.
2. Write or extend tests before production code.
3. Run the new tests and confirm they fail for the expected reason.
4. Implement the minimum code needed to make them pass.
5. Run the relevant full verification for the changed scope.
6. Refactor only with tests still green.

If the project does not yet have suitable test infrastructure for the changed area, add it as part of the task instead of silently skipping tests.

## Test Honesty Rules
Do not make tests pass by weakening them.

Every new or modified test must be specific enough that it would fail if the related production behavior breaks. After tests pass, verify that by intentionally breaking or removing the relevant implementation and confirming the test fails, then restore the code.

Forbidden shortcuts:
- changing assertions to match broken behavior
- removing assertions that expose a real defect
- adding fallback assertions that allow multiple incompatible outputs
- mocking away the unit or flow that is supposed to be tested
- skipping a failing test without a justified reason in the code and task report

If a test fails, fix the production code or rewrite the test because the requirement was wrong or changed. Do not edit the test to accept incorrect behavior.

## Verification Requirements
Before finishing any task, verify all relevant items for the changed scope:
- tests for the changed behavior pass
- existing relevant tests still pass
- lint passes with no errors
- build passes
- the affected app starts correctly if the change impacts runtime behavior
- no warnings, broken flows, or obvious regressions remain

Use the real commands that exist in the repo today:
- Backend tests: `cd backend; .\mvnw.cmd test`
- Backend run check: `cd backend; .\mvnw.cmd spring-boot:run`
- Frontend install: `cd frontend; npm install`
- Frontend lint: `cd frontend; npm run lint`
- Frontend build: `cd frontend; npm run build`
- Frontend run check: `cd frontend; npm run dev`

Do not claim `npm run test` or E2E verification unless that tooling and script actually exist. When user-visible frontend behavior changes, add or update automated tests as the frontend test stack is introduced.

## Coding Standards
- Follow existing conventions in each area instead of inventing a new style.
- Java uses tabs, `PascalCase` classes, and packages under `com.silkycoders1.jsystemssilkycodders1`.
- TypeScript and React use 2-space indentation, `PascalCase` components, and camelCase functions and variables.
- Keep secrets in environment variables only. Never commit credentials, tokens, `.env` secrets, or local database artifacts.
- Remove outdated or misleading instructions when you find them; do not leave contradictory project files behind.

## Completion Criteria
A task is complete only when:
- the implementation matches the relevant PRD, ADR, and design system guidance
- tests were added first and verified honestly
- verification for the changed scope passed
- the repository remains consistent and reviewable
- the change is committed with a focused message
