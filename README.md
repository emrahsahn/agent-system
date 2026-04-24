# Agent Workflow Starter Kit

This repository is a starter kit for running a platform-agnostic, agent-based workflow.



## Folders

| Folder | Content |
|---|---|
| `agents/` | 4 agent definitions (`planner`, `ui-agent`, `builder`, `reviewer`) |
| `skills/` | Example skill sets (`tdd`, `code-review`, `ui-ux-pro-max`) |
| `cursor-agent-system/` | Scalable, domain-agnostic agent + skill system |

## Quick Setup

### 1) Copy agents into your agent platform

```bash
cp agents/*.md <your-agent-directory>/
```

### 2) Copy skills into your skill directory

```bash
cp -r skills/tdd <your-skills-directory>/
cp -r skills/code-review <your-skills-directory>/
cp -r skills/ui-ux-pro-max <your-skills-directory>/
```

### 3) Test in your assistant environment

Run a task using your orchestrator and specialist agents:

```text
"Build a new pricing page. First plan it, then prepare the UI brief, then implement it, and finally review it."
```

Expected flow: `planner` -> `ui-agent` -> `builder` -> `reviewer`.

## Extended System (`wshobson/agents` Inspired)

Clone the reference ecosystem:

```bash
gh repo clone wshobson/agents
```

Based on that model, this repo includes `cursor-agent-system/` in a platform-neutral structure.

### Use immediately

```bash
cp cursor-agent-system/agents/*.md <your-agent-directory>/
cp -r cursor-agent-system/skills/* <your-skills-directory>/
```

### System roles

- Orchestration: `universal-orchestrator`
- Engineering: `software-architect`, `frontend-engineer`, `backend-engineer`, `devops-engineer`, `qa-engineer`, `security-auditor`
- Product and growth: `product-manager`, `growth-marketer`, `content-strategist`
- Analysis and discovery: `researcher`, `data-analyst`

## Role Breakdown in This Starter Set

- `planner`: Creates implementation steps and identifies risks/dependencies.
- `ui-agent`: Produces UI/UX decisions and component briefs.
- `builder`: Writes implementation code with a TDD-first approach.
- `reviewer`: Performs quality + security review and severity-based findings.

## Recommended Usage

- Keep tool permissions minimal per agent.
- Separate planning, implementation, and review responsibilities.
- Keep orchestration centralized in one coordinator agent to reduce context drift.

## License

MIT
