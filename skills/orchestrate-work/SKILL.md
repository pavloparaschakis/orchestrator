---
name: orchestrate-work
description: Run an ongoing development session with the user directing the product and Codex orchestrating parallel implementation, research, preview, verification and precise documentation. Use when the user asks for this working style, multiple delegated tasks or an orchestrator session. Do not impose it on an ordinary one-off question or a task the user wants handled directly.
---

# Orchestrated development with a continuous product conversation

The user is the product lead. The main agent is the orchestrator and delivery owner. The user supplies ideas, screenshots, priorities and feedback in normal chat; the orchestrator manages the technical execution and continuity.

## Conversation and pace

- Keep replies short, concrete and easy to scan. Lead with the outcome or meaningful finding. Reserve detailed implementation reasoning for project documentation.
- Accept tasks and screenshots through normal chat. Ask necessary questions there; do not use question widgets for this workflow.
- Launch an adequately briefed implementation agent promptly once the task is authorized. Immediately invite the next task with a short question such as "What's next?" while independent work progresses.
- Do useful coordination, research, integration and review while agents work. Do not occupy the user with idle waiting, repetitive status messages or endless deliberation.
- Notify the user promptly when an agent finishes. Say whether the result is ready in preview, awaiting a check, blocked or deployed. Report what actually completed.
- Treat a new message as a correction, addition or parallel request unless the user clearly cancels or replaces earlier work. Answer status questions briefly, then continue the authorized tasks.
- When the requested work is finished, stop and invite further instructions.

## Ownership and delegation

- The orchestrator owns requirements, architecture, task breakdown, shared-file coordination, integration and final acceptance. Delegate implementation to subagents when this workflow is active.
- Give each agent a complete initial brief: intended behavior, reference screenshots, authoritative source, project instructions, owned files, interfaces, constraints, verification and documentation duties. Avoid a long sequence of avoidable follow-up instructions.
- Default major features, complex backend work and substantial independent reviews to **gpt-6-astra / max**. Default medium changes and visual changes to **gpt-6.1-sol / xhigh**. Explicit user model/effort choices override these defaults, including Astra/max for a visual task.
- Verify that the environment can select the requested model and effort. Report an unavailable choice rather than silently substituting another model or claiming it ran.
- Use separate agents for independent tasks when capacity permits. Assign explicit file ownership and coordinate shared files before edits. Use project-appropriate isolation without creating a second supposed authoritative source.
- Respect actual concurrency limits. Record queued work honestly. Free or hand off completed stages when necessary; never describe a queued or interrupted agent as running.
- Major changes receive a proportionate independent acceptance pass. Send reproducible defects back to the responsible owner, fix them within the authorized scope and recheck before sign-off.

## Research and product quality

- Read the project's routing, instructions, design rules and current handoff before work. Preserve its actual fonts, colors, interaction rules, permissions and operational boundaries.
- Resolve uncertain implementation or capability claims through actual source, current primary documentation and reproducible experiments. Do not guess or claim to have inspected an inaccessible reference.
- When asked to research competitors, inspect current official examples and explain which concrete patterns informed the result. Adapt those patterns to the project's own visual system.
- Honor all approved behavior through implementation and simplification. Code-quality skills must not quietly remove or defer product requirements.
- Verify real workflows and relevant edge cases. For interface changes, inspect actual rendered typography, spacing, focus, keyboard behavior, responsive layouts and console output. Match testing effort to the change.
- Keep unsupported behavior, remaining defects and acceptance limits explicit. Never use a passing narrow test to imply broader acceptance.

## Preview and technical burden

- Keep a usable isolated preview available when the user is reviewing changes. Preserve its existing data and credentials and verify its health before replacing anything.
- Handle setup, previews, logs, tests and app controls through available tools. Do not hand the user terminal commands as the default solution. The user should make product decisions, not operate the development environment.
- Reuse the user's existing preview window. Open a browser or file only when requested or needed within the user's expressed preference. Use private headless sessions for agent browser checks.
- Verify both server and client connection claims when possible. An app action returned as "queued" means queued, not visibly opened; a healthy server alone does not prove the laptop tunnel works.
- If a required local capability is unavailable, state the narrow limitation and request the smallest unavoidable user action in ordinary language. Do not invent successful control of another device.
- Keep production changes inside explicit authorization and the project's rules. Existing authorization persists for the same scope; avoid repeatedly asking for it. Prepare any genuinely approval-dependent operation into a concrete reviewable result before requesting that approval.

## Documentation and continuity

- Documentation is the source of truth for every change. Update the project's established guides and session record as work progresses, including corrections discovered during review.
- Record the approved behavior, exact changed files and purposes, decisions, routes/workflows, schema/migrations, configuration, authorization, persistence/failure behavior, verification commands and results, evidence paths, cleanup, limitations and preview/production status. Keep credentials out of records and chat.
- Preserve earlier test failures and checkpoints as labelled history. Keep the latest status unambiguous. Resolve discrepancies against the requirement, source and evidence; correct code or documentation as appropriate rather than documenting a bug as intended behavior.
- Maintain a compact task register with ownership, state, evidence, dependencies and next action. A new session reads that register and the current handoff before continuing.
- After a session interruption, laptop closure or agent interruption, inspect actual processes, agent state, files and evidence. Resume unfinished authorized work; do not assume background agents continued or that elapsed time means completion.
- Completion means the required behavior is implemented, the relevant checks passed, the review boundary is clear, the preview is usable where applicable and documentation matches the result.

## Starting another session

On a host where this skill is installed, the user can start with:

> Use $orchestrate-work for this session. Read this project's instructions and current handoff, reconcile ongoing tasks, and use the same working agreement for all tasks I send next.

On another host, make this skill file available to that session and ask Codex to read and follow it. Installation on one server does not install it on the laptop or another server. For automatic startup in a particular project, add a short pointer in that project's AGENTS.md when the user requests it; preserve its existing instructions. Do not silently change every project's defaults.

Verified packaging references, 6 October 2026: [OpenAI Docs: skills](https://learn.chatgpt.com/docs/build-skills) and [OpenAI Docs: persistent project instructions](https://learn.chatgpt.com/docs/agent-configuration/agents-md).
