# Awesome Automotive ToDo MCP

**English** | [日本語](README.ja.md)

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of GitHub resources for an automotive-development ToDo system: break a requirement tree into ToDos, assign owners and change milestones dynamically, run PDCA to revise rules and accumulate know-how, and operate it all through MCP (Model Context Protocol).

Maintained under the **shvtech** brand. ⭐ badges show live GitHub star counts (via shields.io); release badges show the date of the latest GitHub release (YYYY/MM/DD, as of the last refresh); last-commit badges show live commit activity (via shields.io). Categorization reflects search results and the maintainer's judgment.

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
- [License](#license)
- [shvyac's awesome lists](#shvyacs-awesome-lists)

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

- [doorstop](https://github.com/doorstop-dev/doorstop) ![GitHub stars](https://img.shields.io/github/stars/doorstop-dev/doorstop?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F10-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/doorstop-dev/doorstop?style=flat) - Manage requirements in Git with traceability.
- [TestLink](https://github.com/TestLinkOpenSourceTRMS/testlink-code) ![GitHub stars](https://img.shields.io/github/stars/TestLinkOpenSourceTRMS/testlink-code?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/TestLinkOpenSourceTRMS/testlink-code?style=flat) - Test and requirements management system.

For managing very large requirement trees (whole vehicle, whole corporate systems), post-development updates (as-built sync, baselines), and AI/MCP operation, see the sibling list [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-requirements-system-ai?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/shvyac/awesome-requirements-system-ai?style=flat).

## 2. ToDo & Project Management

- [OpenProject](https://github.com/opf/openproject) ![GitHub stars](https://img.shields.io/github/stars/opf/openproject?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/opf/openproject?style=flat) - A leading open-source PM tool. Parent/child tasks and Gantt. Built-in MCP server since 17.2.
- [Kaneo](https://github.com/usekaneo/kaneo) ![GitHub stars](https://img.shields.io/github/stars/usekaneo/kaneo?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/usekaneo/kaneo?style=flat) - Board and Gantt, GitHub integration, time tracking, MCP support.
- [Plane](https://github.com/makeplane/plane) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/makeplane/plane?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/makeplane/plane?style=flat) - Open-source Jira / Linear alternative: work items, cycles (sprints), modules, pages and a timeline (Gantt) view. Self-hostable.
- [Planka](https://github.com/plankanban/planka) ![GitHub stars](https://img.shields.io/github/stars/plankanban/planka?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F05-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/plankanban/planka?style=flat) - Self-hosted kanban.
- [Kanboard](https://github.com/kanboard/kanboard) ![GitHub stars](https://img.shields.io/github/stars/kanboard/kanboard?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F31-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/kanboard/kanboard?style=flat) - Lightweight kanban.
- [Leantime](https://github.com/Leantime/leantime) ![GitHub stars](https://img.shields.io/github/stars/Leantime/leantime?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Leantime/leantime?style=flat) - Goal-driven project management.
- [Taiga](https://github.com/taigaio/taiga-back) ![GitHub stars](https://img.shields.io/github/stars/taigaio/taiga-back?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/taigaio/taiga-back?style=flat) - Agile (Scrum / Kanban).

## 3. Schedules & Milestones

- [OpenProject](https://github.com/opf/openproject) ![GitHub stars](https://img.shields.io/github/stars/opf/openproject?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/opf/openproject?style=flat) - Gantt with dependencies.
- [Kaneo](https://github.com/usekaneo/kaneo) ![GitHub stars](https://img.shields.io/github/stars/usekaneo/kaneo?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/usekaneo/kaneo?style=flat) - Lightweight Gantt view.

## 4. Dynamic Assignment & Workload Analysis

- [Paca](https://github.com/Paca-AI/paca) ![GitHub stars](https://img.shields.io/github/stars/Paca-AI/paca?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Paca-AI/paca?style=flat) - Humans and AI agents collaborate on the same board and sprints; Gantt view and refinement drafts by an analyst agent. MCP support.
- [scrumboy](https://github.com/markrai/scrumboy) ![GitHub stars](https://img.shields.io/github/stars/markrai/scrumboy?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F13-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/markrai/scrumboy?style=flat) - Cross-project workload and flow analysis. MCP / agent automation.

## 5. PDCA, Rule Revision & Know-how Accumulation

- [atlas-mcp-server](https://github.com/cyanheads/atlas-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/cyanheads/atlas-mcp-server?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/cyanheads/atlas-mcp-server?style=flat) - Three-tier Projects / Tasks / Knowledge structure (Neo4j); close to ToDo plus know-how accumulation. No updates since July 2025.
- [storybloq](https://github.com/Storybloq/storybloq) ![GitHub stars](https://img.shields.io/github/stars/Storybloq/storybloq?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F13-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Storybloq/storybloq?style=flat) - Keeps plans, handovers, and review evidence in the repo so work resumes across sessions. Records rulings (decisions), capabilities and a glossary.
- [Task Orchestrator](https://github.com/jpicklyk/task-orchestrator) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/jpicklyk/task-orchestrator?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F11-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/jpicklyk/task-orchestrator?style=flat) - MCP server with persistent work items, dependency graphs, quality gates and actor attribution; schemas define what agents must produce before a step is accepted.

## 6. MCP Servers

- [Plane MCP Server](https://github.com/makeplane/plane-mcp-server) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/makeplane/plane-mcp-server?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/makeplane/plane-mcp-server?style=flat) - Official MCP server for Plane (work items, cycles, modules, projects).
- [openproject-mcp-server (AndyEverything)](https://github.com/AndyEverything/openproject-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/AndyEverything/openproject-mcp-server?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/AndyEverything/openproject-mcp-server?style=flat) - Integrates with OpenProject API v3.
- [openproject-mcp (kar-thik)](https://github.com/kar-thik/openproject-mcp) ![GitHub stars](https://img.shields.io/github/stars/kar-thik/openproject-mcp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F29-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/kar-thik/openproject-mcp?style=flat) - 89 tools (work packages, time tracking, reports, etc.).
- [openproject-ce-mcp (jtauschl)](https://github.com/jtauschl/openproject-ce-mcp) ![GitHub stars](https://img.shields.io/github/stars/jtauschl/openproject-ce-mcp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F08-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/jtauschl/openproject-ce-mcp?style=flat) - For OpenProject Community Edition.
- [todoist-mcp-server](https://github.com/abhiz123/todoist-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/abhiz123/todoist-mcp-server?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/abhiz123/todoist-mcp-server?style=flat) - Todoist integration. No updates since April 2025.
- [mcp-tasks (flesler)](https://github.com/flesler/mcp-tasks) ![GitHub stars](https://img.shields.io/github/stars/flesler/mcp-tasks?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/flesler/mcp-tasks?style=flat) - Task management in Markdown / JSON / YAML.

## 7. Obsidian Integration

- [obsidian-tasks](https://github.com/obsidian-tasks-group/obsidian-tasks) ![GitHub stars](https://img.shields.io/github/stars/obsidian-tasks-group/obsidian-tasks?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/obsidian-tasks-group/obsidian-tasks?style=flat) - Task management plugin for Obsidian.

## 8. General ToDo & Task Management

- [Vikunja](https://github.com/go-vikunja/vikunja) ![GitHub stars](https://img.shields.io/github/stars/go-vikunja/vikunja?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F05-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/go-vikunja/vikunja?style=flat) - ToDo-centric, REST API.
- [tududi](https://github.com/chrisvel/tududi) ![GitHub stars](https://img.shields.io/github/stars/chrisvel/tududi?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F17-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/chrisvel/tududi?style=flat) - GTD-oriented task and project management.
- [Super Productivity](https://github.com/super-productivity/super-productivity) ![GitHub stars](https://img.shields.io/github/stars/super-productivity/super-productivity?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F06-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/super-productivity/super-productivity?style=flat) - With timeboxing and time tracking; integrates with Jira / GitLab / GitHub / OpenProject / Azure DevOps.
- [Taskwarrior](https://github.com/GothenburgBitFactory/taskwarrior) ![GitHub stars](https://img.shields.io/github/stars/GothenburgBitFactory/taskwarrior?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/GothenburgBitFactory/taskwarrior?style=flat) - Command-line task manager.

## Related Awesome Lists

- [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-requirements-system-ai?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/shvyac/awesome-requirements-system-ai?style=flat) - OSS for managing and updating hierarchical requirement trees (whole vehicle, corporate IT) with AI/MCP. (Sibling list)
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) ![GitHub stars](https://img.shields.io/github/stars/awesome-selfhosted/awesome-selfhosted?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2023%2F08%2F22-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/awesome-selfhosted/awesome-selfhosted?style=flat) - Has "Task Management & To-do Lists" and "Software Development - Project Management" categories.
- [awesome-project-management (shahedbd)](https://github.com/shahedbd/awesome-project-management) ![GitHub stars](https://img.shields.io/github/stars/shahedbd/awesome-project-management?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/shahedbd/awesome-project-management?style=flat) - General PM resources.
- [awesome-project-management (brianjking)](https://github.com/brianjking/awesome-project-management) ![GitHub stars](https://img.shields.io/github/stars/brianjking/awesome-project-management?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/brianjking/awesome-project-management?style=flat)
- [awesome-agile-essentials](https://github.com/SaadAAkash/awesome-agile-essentials) ![GitHub stars](https://img.shields.io/github/stars/SaadAAkash/awesome-agile-essentials?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/SaadAAkash/awesome-agile-essentials?style=flat) - Agile resources.

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

## shvyac's awesome lists

All curated lists maintained by [shvyac](https://github.com/shvyac):

- [awesome-ai-dev-tools](https://github.com/shvyac/awesome-ai-dev-tools) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ai-dev-tools?style=flat&label=%E2%AD%90)
- [awesome-AI-Powered-Executive-Dashboards](https://github.com/shvyac/awesome-AI-Powered-Executive-Dashboards) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-AI-Powered-Executive-Dashboards?style=flat&label=%E2%AD%90)
- [awesome-ai-tool-for-mechanical-engineering](https://github.com/shvyac/awesome-ai-tool-for-mechanical-engineering) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ai-tool-for-mechanical-engineering?style=flat&label=%E2%AD%90)
- [awesome-audio-softwares](https://github.com/shvyac/awesome-audio-softwares) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-audio-softwares?style=flat&label=%E2%AD%90)
- [awesome-automotive-cae](https://github.com/shvyac/awesome-automotive-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-automotive-cae?style=flat&label=%E2%AD%90)
- [awesome-automotive-todo-mcp](https://github.com/shvyac/awesome-automotive-todo-mcp) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-automotive-todo-mcp?style=flat&label=%E2%AD%90)
- [awesome-azure-ai-dynamics365-security](https://github.com/shvyac/awesome-azure-ai-dynamics365-security) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-azure-ai-dynamics365-security?style=flat&label=%E2%AD%90)
- [awesome-ballroom-dance](https://github.com/shvyac/awesome-ballroom-dance) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ballroom-dance?style=flat&label=%E2%AD%90)
- [awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat&label=%E2%AD%90)
- [awesome-cms-ai](https://github.com/shvyac/awesome-cms-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cms-ai?style=flat&label=%E2%AD%90)
- [awesome-dashboards-visualization](https://github.com/shvyac/awesome-dashboards-visualization) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-dashboards-visualization?style=flat&label=%E2%AD%90)
- [awesome-ghost-artists](https://github.com/shvyac/awesome-ghost-artists) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ghost-artists?style=flat&label=%E2%AD%90)
- [awesome-hamradio](https://github.com/shvyac/awesome-hamradio) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hamradio?style=flat&label=%E2%AD%90)
- [awesome-hpc](https://github.com/shvyac/awesome-hpc) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hpc?style=flat&label=%E2%AD%90)
- [awesome-iso27001-isms-tools](https://github.com/shvyac/awesome-iso27001-isms-tools) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-iso27001-isms-tools?style=flat&label=%E2%AD%90)
- [awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90)
- [awesome-m5stack-arduino](https://github.com/shvyac/awesome-m5stack-arduino) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-m5stack-arduino?style=flat&label=%E2%AD%90)
- [awesome-map-gis](https://github.com/shvyac/awesome-map-gis) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-map-gis?style=flat&label=%E2%AD%90)
- [awesome-mcp-ai](https://github.com/shvyac/awesome-mcp-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-mcp-ai?style=flat&label=%E2%AD%90)
- [awesome-meshless-cae](https://github.com/shvyac/awesome-meshless-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-meshless-cae?style=flat&label=%E2%AD%90)
- [awesome-online-services](https://github.com/shvyac/awesome-online-services) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-online-services?style=flat&label=%E2%AD%90)
- [awesome-open-source-solvers](https://github.com/shvyac/awesome-open-source-solvers) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-open-source-solvers?style=flat&label=%E2%AD%90)
- [awesome-osint-ai](https://github.com/shvyac/awesome-osint-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-osint-ai?style=flat&label=%E2%AD%90)
- [awesome-quantum](https://github.com/shvyac/awesome-quantum) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-quantum?style=flat&label=%E2%AD%90)
- [awesome-redmine-ai](https://github.com/shvyac/awesome-redmine-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-redmine-ai?style=flat&label=%E2%AD%90)
- [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-requirements-system-ai?style=flat&label=%E2%AD%90)
- [awesome-trading-stock](https://github.com/shvyac/awesome-trading-stock) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-trading-stock?style=flat&label=%E2%AD%90)
- [awesome-web-app-design](https://github.com/shvyac/awesome-web-app-design) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-web-app-design?style=flat&label=%E2%AD%90)
