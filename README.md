# Awesome Automotive ToDo MCP

**English** | [日本語](README.ja.md)

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of GitHub resources for an automotive-development ToDo system: break a requirement tree into ToDos, assign owners and change milestones dynamically, run PDCA to revise rules and accumulate know-how, and operate it all through MCP (Model Context Protocol).

Maintained under the **shvtech** brand. Star counts are from GitHub search results as of 2026-10-31. Categorization reflects search results and the maintainer's judgment.

## Contents

- [Concept](#concept)
- [1. Requirements Tree & Traceability](#1-requirements-tree--traceability)
- [2. ToDo & Project Management](#2-todo--project-management)
- [3. Schedules & Milestones](#3-schedules--milestones)
- [4. Dynamic Assignment & Workload Analysis](#4-dynamic-assignment--workload-analysis)
- [5. PDCA, Rule Revision & Know-how Accumulation](#5-pdca-rule-revision--know-how-accumulation)
- [6. MCP Servers](#6-mcp-servers)
- [7. Obsidian Integration](#7-obsidian-integration)
- [8. General ToDo & Task Management](#8-general-todo--task-management)
- [Related Awesome Lists](#related-awesome-lists)
- [Gaps](#gaps)
- [Contributing](#contributing)

## Concept

```
INPUT (requests, designs, drawings) ──▶ ToDo ──▶ OUTPUT (minutes, reports, data, drawings, specs)
                                         ▲ ▲
                       Rule / Guide / Know-how   Tools / Resources
                                  │
   PDCA (assignee → reviewer/chief → manager/leader) → Rule revision / Tool improvement
```

| Element | Description |
|---|---|
| Requirement tree | Decompose market requirements into a multi-level tree and manage it as a hierarchy diagram |
| ToDo | Defined by four elements: Input / Rule & know-how / Tools / Output |
| Dynamic operation | Change assignees and milestones as the situation changes |
| PDCA | Revise rules and improve tools from results, accumulated across all vehicle models |
| Knowledge delivery | From "knowledge you search for" (system = Passive, user = Active) to "knowledge that reaches you" (system = Active, user = Passive). Don't list everything; curate and deliver only what the current ToDo needs. Humans make the final call |
| MCP | An AI (e.g., Claude) reads, writes, and re-plans all of the above |

## 1. Requirements Tree & Traceability

- [doorstop](https://github.com/doorstop-dev/doorstop) - Manage requirements in Git with traceability. (690★)
- [TestLink](https://github.com/TestLinkOpenSourceTRMS/testlink-code) - Test and requirements management system. (1.6k★)

For managing very large requirement trees (whole vehicle, whole corporate systems), post-development updates (as-built sync, baselines), and AI/MCP operation, see the sibling list [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai).

## 2. ToDo & Project Management

- [OpenProject](https://github.com/opf/openproject) - A leading open-source PM tool. Parent/child tasks and Gantt.
- [Kaneo](https://github.com/usekaneo/kaneo) - Board and Gantt, GitHub integration, MCP support. (9.6k★)
- [Planka](https://github.com/plankanban/planka) - Self-hosted kanban. (12.6k★)
- [Kanboard](https://github.com/kanboard/kanboard) - Lightweight kanban. (9.9k★)
- [Leantime](https://github.com/leantime/leantime) - Goal-driven project management.
- [Taiga](https://github.com/taigaio/taiga-back) - Agile (Scrum / Kanban).

## 3. Schedules & Milestones

- [OpenProject](https://github.com/opf/openproject) - Gantt with dependencies.
- [Kaneo](https://github.com/usekaneo/kaneo) - Lightweight Gantt view.

## 4. Dynamic Assignment & Workload Analysis

- [Paca](https://github.com/Paca-AI/paca) - Humans and AI agents collaborate on the same board and sprints. MCP support. (2.0k★)
- [scrumboy](https://github.com/markrai/scrumboy) - Cross-project workload and flow analysis. MCP / agent automation. (448★)

## 5. PDCA, Rule Revision & Know-how Accumulation

- [atlas-mcp-server](https://github.com/cyanheads/atlas-mcp-server) - Three-tier Projects / Tasks / Knowledge structure (Neo4j); close to ToDo plus know-how accumulation. (478★)
- [storybloq](https://github.com/Storybloq/storybloq) - Keeps plans, handovers, and review evidence in the repo so work resumes across sessions. (785★)

## 6. MCP Servers

- [openproject-mcp-server (AndyEverything)](https://github.com/AndyEverything/openproject-mcp-server) - Integrates with OpenProject API v3. (91★)
- [openproject-mcp (kar-thik)](https://github.com/kar-thik/openproject-mcp) - 89 tools (work packages, time tracking, reports, etc.).
- [openproject-ce-mcp (jtauschl)](https://github.com/jtauschl/openproject-ce-mcp) - For OpenProject Community Edition.
- [todoist-mcp-server](https://github.com/abhiz123/todoist-mcp-server) - Todoist integration. (392★)
- [mcp-tasks (flesler)](https://github.com/flesler/mcp-tasks) - Task management in Markdown / JSON / YAML.

## 7. Obsidian Integration

- [obsidian-tasks](https://github.com/obsidian-tasks-group/obsidian-tasks) - Task management plugin for Obsidian. (4.0k★)

## 8. General ToDo & Task Management

- [Vikunja](https://github.com/go-vikunja/vikunja) - ToDo-centric, REST API. (5.9k★)
- [tududi](https://github.com/chrisvel/tududi) - GTD-oriented task and project management. (3.5k★)
- [Super Productivity](https://github.com/johannesjo/super-productivity) - With timeboxing and time tracking; integrates with Jira / GitLab / GitHub.
- [Taskwarrior](https://github.com/GothenburgBitFactory/taskwarrior) - Command-line task manager.

## Related Awesome Lists

- [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) - OSS for managing and updating hierarchical requirement trees (whole vehicle, corporate IT) with AI/MCP. (Sibling list)
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) - Has "Task Management & To-do Lists" and "Software Development - Project Management" categories.
- [awesome-project-management (shahedbd)](https://github.com/shahedbd/awesome-project-management) - General PM resources. (813★)
- [awesome-project-management (brianjking)](https://github.com/brianjking/awesome-project-management)
- [awesome-agile-essentials](https://github.com/SaadAAkash/awesome-agile-essentials) - Agile resources. (92★)

## Gaps

At the time of research, no repository was found that combines all of the following:

- [ ] Automatic milestone recalculation (reflecting dependencies, workload, and delays)
- [ ] Automatic assignment (considering skills, workload, and dependencies)
- [ ] Reflecting PDCA results into rules with version control (e.g., Rule 1.0 → 1.1 → 1.2)
- [ ] A cross-model results DB with search
- [ ] Automatic expansion of a requirement tree into ToDos
- [ ] Automatically delivering only the rules and know-how each ToDo needs, curated

## Contributing

Pull requests and issues are welcome. Added resources should meet at least one of:

- Deals with requirements, ToDos, schedules, assignment, PDCA, or know-how
- Supports MCP, or can be operated through MCP

## License

This work is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Credit: **shvtech**.

[![CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)
