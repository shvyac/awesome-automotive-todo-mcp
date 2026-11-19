# Awesome Automotive ToDo MCP

[English](README.md) | **日本語**

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> 自動車開発の要件ツリーから ToDo を展開し、担当・マイルストーンを動的に変更し、PDCA で Rule・ノウハウを蓄積する仕組みを、MCP(Model Context Protocol)で運用するための GitHub リソース集です。

Maintained under the **shvtech** brand. ⭐ バッジは GitHub のスター数をリアルタイム表示します(shields.io)。release バッジは GitHub の最新リリース日(YYYY/MM/DD、最終更新時点)を示します。last commit バッジは最新コミット日をリアルタイム表示します(shields.io)。分類は検索結果とメンテナの判断に基づきます。

## Contents

- [コンセプト](#コンセプト)
- [1. 要件ツリー・トレーサビリティ](#1-要件ツリートレーサビリティ)
- [2. ToDo・プロジェクト管理](#2-todoプロジェクト管理)
- [3. 工程表・マイルストーン](#3-工程表マイルストーン)
- [4. 担当の動的割当・負荷分析](#4-担当の動的割当負荷分析)
- [5. PDCA・Rule 改訂・ノウハウ蓄積](#5-pdcarule-改訂ノウハウ蓄積)
- [6. MCP サーバ](#6-mcp-サーバ)
- [7. Obsidian 連携](#7-obsidian-連携)
- [8. ToDo・タスク管理(汎用)](#8-todoタスク管理汎用)
- [Awesome リスト(関連)](#awesome-リスト関連)
- [Gaps(未解決の領域)](#gaps未解決の領域)
- [Contributing](#contributing)
- [License](#license)
- [shvyac の awesome リスト](#shvyac-の-awesome-リスト)

## コンセプト

```
INPUT情報 ──▶ ToDo ──▶ OUTPUT成果物
(要求・デザイン・図面)  ▲ ▲   (議事録・レポート・データ・図面・仕様書)
        Rule/Guide/KnowHow   Tools/Resources
              │
   PDCA(担当者 → レビュアー/チーフ → マネージャー/リーダー)→ Rule改訂・Tool改良
```

| 要素 | 内容 |
|---|---|
| 要件ツリー | 市場要求から要件を多階層に分解し、系統図で管理 |
| ToDo | Input / Rule・ノウハウ / Tools / Output の4要素で定義 |
| 動的運用 | 担当割当とマイルストーンを状況に応じて変更 |
| PDCA | 結果から Rule 改訂・Tool 改良を行い、全車種で蓄積 |
| 知識の届け方 | 「探す知識」(システム=Passive、ユーザー=Active)から「届く知識」(システム=Active、ユーザー=Passive)へ。全部を並べず、いまの ToDo に必要なものだけを厳選して届ける。判断は人が行う |
| MCP | AI(Claude など)が上記を読み書き・再計画する |

## 1. 要件ツリー・トレーサビリティ

- [doorstop](https://github.com/doorstop-dev/doorstop) ![GitHub stars](https://img.shields.io/github/stars/doorstop-dev/doorstop?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F10-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/doorstop-dev/doorstop?style=flat) - Git で要件を管理し、トレーサビリティを確保する。
- [TestLink](https://github.com/TestLinkOpenSourceTRMS/testlink-code) ![GitHub stars](https://img.shields.io/github/stars/TestLinkOpenSourceTRMS/testlink-code?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/TestLinkOpenSourceTRMS/testlink-code?style=flat) - テストと要件の管理システム。

車両全体・社内システム全体といった大規模な要件ツリーの管理、開発後の更新(as-built 同期、ベースライン)、AI/MCP での運用については、姉妹リスト [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-requirements-system-ai?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/shvyac/awesome-requirements-system-ai?style=flat) も参照してください。

## 2. ToDo・プロジェクト管理

- [OpenProject](https://github.com/opf/openproject) ![GitHub stars](https://img.shields.io/github/stars/opf/openproject?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/opf/openproject?style=flat) - 主要なオープンソース PM ソフト。親子タスクとガントに対応。17.2 から MCP サーバを標準搭載。
- [Kaneo](https://github.com/usekaneo/kaneo) ![GitHub stars](https://img.shields.io/github/stars/usekaneo/kaneo?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/usekaneo/kaneo?style=flat) - ボードとガント、GitHub 連携、時間記録、MCP 対応。
- [Plane](https://github.com/makeplane/plane) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/makeplane/plane?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/makeplane/plane?style=flat) - Jira / Linear のオープンソース代替。ワークアイテム、サイクル(スプリント)、モジュール、ページ、タイムライン(ガント)表示。自前運用可。
- [Planka](https://github.com/plankanban/planka) ![GitHub stars](https://img.shields.io/github/stars/plankanban/planka?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F05-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/plankanban/planka?style=flat) - 自前運用できるカンバン。
- [Kanboard](https://github.com/kanboard/kanboard) ![GitHub stars](https://img.shields.io/github/stars/kanboard/kanboard?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F31-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/kanboard/kanboard?style=flat) - 軽量カンバン。
- [Leantime](https://github.com/Leantime/leantime) ![GitHub stars](https://img.shields.io/github/stars/Leantime/leantime?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Leantime/leantime?style=flat) - 目標ドリブンなプロジェクト管理。
- [Taiga](https://github.com/taigaio/taiga-back) ![GitHub stars](https://img.shields.io/github/stars/taigaio/taiga-back?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/taigaio/taiga-back?style=flat) - アジャイル向け(Scrum / Kanban)。

## 3. 工程表・マイルストーン

- [OpenProject](https://github.com/opf/openproject) ![GitHub stars](https://img.shields.io/github/stars/opf/openproject?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/opf/openproject?style=flat) - ガントと依存関係を扱える。
- [Kaneo](https://github.com/usekaneo/kaneo) ![GitHub stars](https://img.shields.io/github/stars/usekaneo/kaneo?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/usekaneo/kaneo?style=flat) - 軽量なガント表示。

## 4. 担当の動的割当・負荷分析

- [Paca](https://github.com/Paca-AI/paca) ![GitHub stars](https://img.shields.io/github/stars/Paca-AI/paca?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Paca-AI/paca?style=flat) - 人と AI エージェントが同じボード・スプリントで協働する。ガント表示、アナリスト役エージェントによるタスク下書き(Refinement)。MCP 対応。
- [scrumboy](https://github.com/markrai/scrumboy) ![GitHub stars](https://img.shields.io/github/stars/markrai/scrumboy?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F13-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/markrai/scrumboy?style=flat) - プロジェクト横断の負荷・フロー分析。MCP/エージェント自動化に対応。

## 5. PDCA・Rule 改訂・ノウハウ蓄積

- [atlas-mcp-server](https://github.com/cyanheads/atlas-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/cyanheads/atlas-mcp-server?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/cyanheads/atlas-mcp-server?style=flat) - Projects / Tasks / Knowledge の3層構造(Neo4j)。ToDo とノウハウの蓄積に近い設計。2025年7月以降更新なし。
- [storybloq](https://github.com/Storybloq/storybloq) ![GitHub stars](https://img.shields.io/github/stars/Storybloq/storybloq?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F13-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Storybloq/storybloq?style=flat) - 計画・引き継ぎ・レビュー証跡を repo 内に保持し、セッションをまたいで再開できる。決定事項(ruling)・機能一覧・用語集も記録できる。
- [Task Orchestrator](https://github.com/jpicklyk/task-orchestrator) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/jpicklyk/task-orchestrator?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F11-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/jpicklyk/task-orchestrator?style=flat) - 永続的なワークアイテム、依存グラフ、品質ゲート、実行者の記録を備えた MCP サーバ。エージェントが出すべき成果物をスキーマで定義し、満たさない呼び出しはブロックする。

## 6. MCP サーバ

- [Plane MCP Server](https://github.com/makeplane/plane-mcp-server) ![New](https://img.shields.io/badge/-NEW-red?style=flat) ![GitHub stars](https://img.shields.io/github/stars/makeplane/plane-mcp-server?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/makeplane/plane-mcp-server?style=flat) - Plane 公式の MCP サーバ(ワークアイテム、サイクル、モジュール、プロジェクト)。
- [openproject-mcp-server (AndyEverything)](https://github.com/AndyEverything/openproject-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/AndyEverything/openproject-mcp-server?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/AndyEverything/openproject-mcp-server?style=flat) - OpenProject API v3 と連携。
- [openproject-mcp (kar-thik)](https://github.com/kar-thik/openproject-mcp) ![GitHub stars](https://img.shields.io/github/stars/kar-thik/openproject-mcp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F29-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/kar-thik/openproject-mcp?style=flat) - 89 ツール(work package、時間記録、レポートなど)。
- [openproject-ce-mcp (jtauschl)](https://github.com/jtauschl/openproject-ce-mcp) ![GitHub stars](https://img.shields.io/github/stars/jtauschl/openproject-ce-mcp?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F08-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/jtauschl/openproject-ce-mcp?style=flat) - OpenProject Community Edition 向け。
- [todoist-mcp-server](https://github.com/abhiz123/todoist-mcp-server) ![GitHub stars](https://img.shields.io/github/stars/abhiz123/todoist-mcp-server?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/abhiz123/todoist-mcp-server?style=flat) - Todoist 連携。2025年4月以降更新なし。
- [mcp-tasks (flesler)](https://github.com/flesler/mcp-tasks) ![GitHub stars](https://img.shields.io/github/stars/flesler/mcp-tasks?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/flesler/mcp-tasks?style=flat) - Markdown / JSON / YAML 形式のタスク管理。

## 7. Obsidian 連携

- [obsidian-tasks](https://github.com/obsidian-tasks-group/obsidian-tasks) ![GitHub stars](https://img.shields.io/github/stars/obsidian-tasks-group/obsidian-tasks?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/obsidian-tasks-group/obsidian-tasks?style=flat) - Obsidian 用のタスク管理プラグイン。

## 8. ToDo・タスク管理(汎用)

- [Vikunja](https://github.com/go-vikunja/vikunja) ![GitHub stars](https://img.shields.io/github/stars/go-vikunja/vikunja?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F05-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/go-vikunja/vikunja?style=flat) - ToDo 中心、REST API 対応。
- [tududi](https://github.com/chrisvel/tududi) ![GitHub stars](https://img.shields.io/github/stars/chrisvel/tududi?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F17-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/chrisvel/tududi?style=flat) - GTD 志向のタスク・プロジェクト管理。
- [Super Productivity](https://github.com/super-productivity/super-productivity) ![GitHub stars](https://img.shields.io/github/stars/super-productivity/super-productivity?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F06-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/super-productivity/super-productivity?style=flat) - タイムボクシングと時間記録つき。Jira / GitLab / GitHub / OpenProject / Azure DevOps と連携。
- [Taskwarrior](https://github.com/GothenburgBitFactory/taskwarrior) ![GitHub stars](https://img.shields.io/github/stars/GothenburgBitFactory/taskwarrior?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/GothenburgBitFactory/taskwarrior?style=flat) - コマンドライン型。

## Awesome リスト(関連)

- [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-requirements-system-ai?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/shvyac/awesome-requirements-system-ai?style=flat) - 階層的な要件ツリー(車両全体・社内IT全体)の管理と更新、AI/MCP での運用に使える OSS の一覧。(姉妹リスト)
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) ![GitHub stars](https://img.shields.io/github/stars/awesome-selfhosted/awesome-selfhosted?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2023%2F08%2F22-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/awesome-selfhosted/awesome-selfhosted?style=flat) - 「Task Management & To-do Lists」「Software Development - Project Management」カテゴリあり。
- [awesome-project-management (shahedbd)](https://github.com/shahedbd/awesome-project-management) ![GitHub stars](https://img.shields.io/github/stars/shahedbd/awesome-project-management?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/shahedbd/awesome-project-management?style=flat) - PM 全般のリソース集。
- [awesome-project-management (brianjking)](https://github.com/brianjking/awesome-project-management) ![GitHub stars](https://img.shields.io/github/stars/brianjking/awesome-project-management?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/brianjking/awesome-project-management?style=flat)
- [awesome-agile-essentials](https://github.com/SaadAAkash/awesome-agile-essentials) ![GitHub stars](https://img.shields.io/github/stars/SaadAAkash/awesome-agile-essentials?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/SaadAAkash/awesome-agile-essentials?style=flat) - アジャイル関連。

## Gaps(未解決の領域)

調査時点で、次の機能をまとめて備えたリポジトリは見つかっていません。

- [ ] マイルストーンの自動再計算(依存・負荷・遅延を反映)
- [ ] 担当の自動割当(スキル・負荷・依存を考慮)
- [ ] PDCA 結果から Rule への反映と版管理(例: Rule 1.0 → 1.1 → 1.2)
- [ ] 全車種横断の結果 DB と検索
- [ ] 要件ツリー(系統図)から ToDo を自動展開する仕組み
- [ ] ToDo ごとに、必要な Rule・ノウハウだけを厳選して自動で届ける仕組み

## Contributing

Pull request や issue を歓迎します。追加するリソースは、次のいずれかに当てはまるものにしてください。

- 要件・ToDo・工程・割当・PDCA・ノウハウのいずれかを扱う
- MCP 対応、または MCP 経由で操作できる

## License

This work is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Credit: **shvtech**.

[![CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)

## shvyac の awesome リスト

[shvyac](https://github.com/shvyac) が管理しているキュレーションリストの一覧:

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
