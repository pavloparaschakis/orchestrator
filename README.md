# Orchestrate Work

A Codex skill for ongoing development with you directing the product and Codex coordinating delivery. Send ideas, screenshots, priorities and feedback in normal chat; implementation agents handle the technical work.

Read the [skill instructions](skills/orchestrate-work/SKILL.md).

## Working agreement

- The main agent reads the project's instructions and current handoff, briefs an implementation agent, then immediately returns the conversation to you so you can send the next task.
- Independent tasks run in parallel when capacity permits, with explicit file ownership and coordinated shared files. Implementation agents own their assigned implementation, checks, cleanup and documentation.
- The orchestrator manages requirements, integration and acceptance, and reports completion with the actual preview or deployment status. It should not hold your turn open just to supervise running agents.
- Source, preview and production stay clearly distinguished. Production actions follow your authorization and the project's rules.
- Precise project documentation and a compact task register preserve decisions, evidence, ownership and unfinished work between sessions.

The skill defaults major features, complex backend work and substantial independent reviews to `gpt-6-astra / max`, and medium or visual changes to `gpt-6.1-sol / xhigh`. Your explicit choices take precedence. The agent checks available models and concurrency rather than assuming those capabilities exist.

## Install

In a Codex session with `$skill-installer`, paste:

```text
Use $skill-installer to install the orchestrate-work skill from https://github.com/pavloparaschakis/orchestrator/tree/main/skills/orchestrate-work.
```

If the skill does not appear after installation, restart Codex. [Official OpenAI skill documentation](https://learn.chatgpt.com/docs/build-skills) explains invocation and local installation.

Install it on each host where you want to use it. Installing on one server does not install it on another computer.

## Start a session

Paste this after installation:

```text
Use $orchestrate-work for this session. Read this project's instructions and current handoff, reconcile ongoing tasks, and use the same working agreement for all tasks I send next. For each authorized task, launch an adequately briefed implementation agent and return control to me immediately. Give the implementation agent ownership of its implementation, checks, cleanup and documentation; notify me when it finishes with the actual preview or deployment status.
```

Then send tasks and screenshots through normal chat. This workflow needs an environment with agent delegation; requested models, previews and device controls depend on that environment's available tools.

For a session where the skill is not installed, make [SKILL.md](skills/orchestrate-work/SKILL.md) available and ask Codex to read and follow it. A project can point to the skill from its own `AGENTS.md` when you explicitly want that startup behavior.

## Contents

```text
skills/orchestrate-work/
  SKILL.md
  agents/openai.yaml
```

The skill instructions and existing UI metadata are preserved as supplied. The package contains no application code, credentials or project-specific configuration.
