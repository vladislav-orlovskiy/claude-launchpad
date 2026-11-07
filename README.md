# claude-launchpad

A single place to start your day-to-day work with [Claude Code](https://claude.com/claude-code),
whatever your role: developer, DevOps/SRE, manager, or something else entirely.

The launchpad ships **generic**. You make it yours by running `/setup`: Claude
interviews you about your role, tools, repositories and team, then fills the
launchpad with the commands and context you need. From then on, opening Claude
Code in this repo is how you start work.

> **Status:** early design. The commands described below are the plan, not yet
> implemented. This README will be updated as each one lands.

## How it works

1. **Get your own copy** -- fork this repository (see [Licensing](#licensing)
   before you fork privately).
2. **Open it in Claude Code** and run `/setup`.
3. `/setup` creates a feature branch and asks you a set of questions: your
   role, the tools and connectors you use, the repositories and infrastructure
   you work with, your team and its rules.
4. Your answers become the launchpad's context and commands, committed on that
   branch so you can review them before merging.
5. Start each day with `/start-day`, pick up tickets with `/work-on`, and grow
   the launchpad with the `/add-*` commands as your work changes.

## Roles

`/setup` offers these roles out of the box:

- **Developer** -- repositories, pull requests, tests, local dev commands
- **DevOps / SRE** -- deployments, infrastructure, monitoring, on-call
- **Manager** -- tickets, stand-ups, reports, calendar, team status

The role list is meant to be extended: new roles can be added later without
changing the rest of the launchpad.

## Commands

> Command names are working names and may change.

### Setup and daily work

| Command | What it does |
| --- | --- |
| `/setup` | Creates a feature branch, interviews you and personalises the launchpad. Named `/setup` rather than `/init` so it does not override Claude Code's built-in `/init`. |
| `/start-day` | Your daily brief, pulled from whatever you configured: tickets, PRs, calendar, alerts. |
| `/work-on <ticket>` | Full flow from ticket to pull request: fetch the ticket, create a branch named after it, do the work, open a PR -- pausing for your approval at each step. |

### Extending the launchpad

| Command | What it does |
| --- | --- |
| `/add-command` | Guided creation of a new slash command. |
| `/add-skill` | Guided creation of a new skill. |
| `/add-connector` | Adds an MCP connector, plugin or skill and records how you use it. |
| `/add-context` | Adds knowledge the launchpad should keep: infrastructure, documentation, repositories, company structure, rules. |
| `/update-context` | Re-runs part of the `/setup` interview or edits stored context. |

## Licensing

This project is released under the [GNU GPL v3](LICENSE): free to use, modify
and share as open source under its terms.

If you want to use it in a way the GPL v3 does not allow for you, a commercial
licence is available -- contact: `<CONTACT TBD>`.
