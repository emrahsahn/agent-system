# Agent System (Platform-Agnostic)

This folder provides a domain-agnostic, scalable agent system.
It is inspired by the `wshobson/agents` ecosystem and adapted for practical multi-agent workflows across platforms.

## Goals

- Provide a shared, reusable core agent set for different teams
- Support easy adaptation across domains (engineering, product, security, data, marketing)
- Improve quality by keeping agent roles explicit and reducing context pollution

## Folder Structure

- `agents/`: Agent definitions ready to import into your agent platform
- `skills/`: Shared skill packages agents can reuse

### Included Skill Packages

- `domain-discovery`
- `decision-matrix`
- `execution-checklist`
- `stakeholder-brief`
- `tdd`
- `code-review`

## Installation

```bash
# Agents
cp cursor-agent-system/agents/*.md <your-agent-directory>/

# Skills
cp -r cursor-agent-system/skills/* <your-skills-directory>/
```

## Recommended Workflow

1. Use `universal-orchestrator` to break down the task.
2. Call specialist agents based on work type:
   - architecture: `software-architect`
   - implementation: `frontend-engineer` / `backend-engineer`
   - quality: `qa-engineer`
   - risk/security: `security-auditor`
   - product: `product-manager`
   - growth/content: `growth-marketer`, `content-strategist`
   - research/data: `researcher`, `data-analyst`
3. Merge outputs back into a single execution plan through `universal-orchestrator`.

## Relation to `wshobson/agents`

This system directly applies two core principles:

- Single-purpose roles (each agent has a clear responsibility)
- Orchestration vs specialization separation (no single agent does everything)

You can extend this folder with domain-specific packs as needed (legal, healthcare, education, e-commerce, finance, etc.).
