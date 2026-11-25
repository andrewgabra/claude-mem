# Life Team — Personal AI Agents

13 Claude Code subagents defined in `.claude/agents/`. All understand English and Arabic.

## Org chart
```
chief-of-staff (orchestrator)
├── executive-assistant   tasks · Gmail · Google Calendar
├── personal-trainer      workouts · progress
├── nutritionist          meals · macros
├── medical-advisor       supplements · interactions · labs
├── project-manager       projects · milestones · risks
└── head-of-engineering
    ├── software-architect
    ├── backend-engineer
    ├── frontend-engineer
    ├── qa-engineer
    ├── devops-engineer
    └── code-reviewer
```

## How to use
| Goal | Command / prompt |
|---|---|
| Daily life (recommended) | `claude --agent chief-of-staff` then "brief me" / "رتب لي يومي" |
| Big dev project | `claude --agent head-of-engineering` (lets it delegate to its team directly) |
| One specialist | In any session: "use the nutritionist to plan my meals this week" |
| Use in every project | Copy the files to `~/.claude/agents/` |

## Requirements
- Gmail, Google Calendar and Google Drive connectors connected in Claude.
- Personal data is stored in your Google Drive folder **"Life OS"** (created on first use) — never in this repo, because the repo is public.

## Safety rules built in
- No email sent, invite accepted, event deleted, deployment or spending without your approval.
- Medical advisor is decision support; physician review flagged where needed.
- Subagents can't spawn subagents, so the head of engineering returns a task plan when called as a subagent.
