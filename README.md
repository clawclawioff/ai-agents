# AI Agents

Claude Code subagent configuration files for the Flagship RTL project.

## Agents

| Agent | Purpose |
|-------|---------|
| `gtm-landing-page-optimizer.md` | Landing page conversion optimization, GTM engineering, and growth work for flagshiprtl.com |
| `sanity-cms-expert.md` | Sanity CMS implementation, schema design, GROQ queries, and Next.js integration |

## Usage

Copy agent files to `.claude/agents/` in your project directory (project-scoped) or `~/.claude/agents/` (user-scoped).

```bash
# Project-scoped (shared with team via git)
cp *.md /path/to/flagship-lp/.claude/agents/

# User-scoped (available in all projects)
cp *.md ~/.claude/agents/
```

Then in Claude Code, the agents will be automatically available for delegation. You can also invoke them directly:

```
Use the gtm-landing-page-optimizer agent to audit the landing page
Use the sanity-cms-expert agent to help with GROQ queries
```

## Format

These files follow the [Claude Code subagent specification](https://code.claude.com/docs/en/sub-agents):
- YAML frontmatter with `name`, `description`, `model`, and `memory` fields
- Markdown body as the system prompt
