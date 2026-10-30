# Awesome Automotive ToDo MCP

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of GitHub resources for an automotive-development ToDo system: break requirements into ToDos, assign owners and change milestones dynamically, run PDCA to revise rules and accumulate know-how, and operate it all through MCP.
>
> 自動車開発の要件ツリーから ToDo を展開し、担当・マイルストーンを動的に変更し、PDCA で Rule・ノウハウを蓄積する仕組みを、MCP(Model Context Protocol)で運用するための GitHub リソース集です。

Maintained under the **shvtech** brand. スター数は 2026-10-31 時点の GitHub 検索結果です。分類は検索結果とメンテナの判断に基づきます。

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

## コンセプト

```
INPUT情報 ──▶ ToDo ──▶ OUTPUT成果物
(要求・デザイン・図面)  ▲ ▲   (議事録・レポート・データ・図面・仕様書)
        Rule/Guide/KnowHow   Tools/Resources
              │
   PDCA(担当 → 研究員/CH/SC → 主研/GL)→ Rule改訂・Tool改良
```

| 要素 | 内容 |
|---|---|
| 要件ツリー | 市場要求から要件(L0〜L7)を分解し、系統図で管理 |
| ToDo | Input / Rule・ノウハウ / Tools / Output の4要素で定義 |
| 動的運用 | 担当割当とマイルストーンを状況に応じて変更 |
| PDCA | 結果から Rule 改訂・Tool 改良を行い、全機種で蓄積 |
| MCP | AI(Claude など)が上記を読み書き・再計画する |

## 1. 要件ツリー・トレーサビリティ

- [doorstop](https://github.com/doorstop-dev/doorstop) - Git で要件を管理し、トレーサビリティを確保する。(690★)
- [TestLink](https://github.com/TestLinkOpenSourceTRMS/testlink-code) - テストと要件の管理システム。(1.6k★)

車両全体・社内システム全体といった大規模な要件ツリーの管理、開発後の更新(as-built 同期、ベースライン)、AI/MCP での運用については、姉妹リスト [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) も参照してください。

## 2. ToDo・プロジェクト管理

- [OpenProject](https://github.com/opf/openproject) - 主要なオープンソース PM ソフト。親子タスクとガントに対応。
- [Kaneo](https://github.com/usekaneo/kaneo) - ボードとガント、GitHub 連携、MCP 対応。(9.6k★)
- [Planka](https://github.com/plankanban/planka) - 自前運用できるカンバン。(12.6k★)
- [Kanboard](https://github.com/kanboard/kanboard) - 軽量カンバン。(9.9k★)
- [Leantime](https://github.com/leantime/leantime) - 目標ドリブンなプロジェクト管理。
- [Taiga](https://github.com/taigaio/taiga-back) - アジャイル向け(Scrum / Kanban)。

## 3. 工程表・マイルストーン

- [OpenProject](https://github.com/opf/openproject) - ガントと依存関係を扱える。
- [Kaneo](https://github.com/usekaneo/kaneo) - 軽量なガント表示。

## 4. 担当の動的割当・負荷分析

- [Paca](https://github.com/Paca-AI/paca) - 人と AI エージェントが同じボード・スプリントで協働する。MCP 対応。(2.0k★)
- [scrumboy](https://github.com/markrai/scrumboy) - プロジェクト横断の負荷・フロー分析。MCP/エージェント自動化に対応。(448★)

## 5. PDCA・Rule 改訂・ノウハウ蓄積

- [atlas-mcp-server](https://github.com/cyanheads/atlas-mcp-server) - Projects / Tasks / Knowledge の3層構造(Neo4j)。ToDo とノウハウの蓄積に近い設計。(478★)
- [storybloq](https://github.com/Storybloq/storybloq) - 計画・引き継ぎ・レビュー証跡を repo 内に保持し、セッションをまたいで再開できる。(785★)

## 6. MCP サーバ

- [openproject-mcp-server (AndyEverything)](https://github.com/AndyEverything/openproject-mcp-server) - OpenProject API v3 と連携。(91★)
- [openproject-mcp (kar-thik)](https://github.com/kar-thik/openproject-mcp) - 89 ツール(work package、時間記録、レポートなど)。
- [openproject-ce-mcp (jtauschl)](https://github.com/jtauschl/openproject-ce-mcp) - OpenProject Community Edition 向け。
- [todoist-mcp-server](https://github.com/abhiz123/todoist-mcp-server) - Todoist 連携。(392★)
- [mcp-tasks (flesler)](https://github.com/flesler/mcp-tasks) - Markdown / JSON / YAML 形式のタスク管理。

## 7. Obsidian 連携

- [obsidian-tasks](https://github.com/obsidian-tasks-group/obsidian-tasks) - Obsidian 用のタスク管理プラグイン。(4.0k★)

## 8. ToDo・タスク管理(汎用)

- [Vikunja](https://github.com/go-vikunja/vikunja) - ToDo 中心、REST API 対応。(5.9k★)
- [tududi](https://github.com/chrisvel/tududi) - GTD 志向のタスク・プロジェクト管理。(3.5k★)
- [Super Productivity](https://github.com/johannesjo/super-productivity) - タイムボクシングと時間記録つき。Jira / GitLab / GitHub と連携。
- [Taskwarrior](https://github.com/GothenburgBitFactory/taskwarrior) - コマンドライン型。

## Awesome リスト(関連)

- [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) - 階層的な要件ツリー(車両全体・社内IT全体)の管理と更新、AI/MCP での運用に使える OSS の一覧。(姉妹リスト)
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) - 「Task Management & To-do Lists」「Software Development - Project Management」カテゴリあり。
- [awesome-project-management (shahedbd)](https://github.com/shahedbd/awesome-project-management) - PM 全般のリソース集。(813★)
- [awesome-project-management (brianjking)](https://github.com/brianjking/awesome-project-management)
- [awesome-agile-essentials](https://github.com/SaadAAkash/awesome-agile-essentials) - アジャイル関連。(92★)

## Gaps(未解決の領域)

調査時点で、次の機能をまとめて備えたリポジトリは見つかっていません。

- [ ] マイルストーンの自動再計算(依存・負荷・遅延を反映)
- [ ] 担当の自動割当(スキル・負荷・依存を考慮)
- [ ] PDCA 結果から Rule への反映と版管理(例: Rule 1.0 → 1.1 → 1.2)
- [ ] 全機種・車種横断の結果 DB と検索
- [ ] 要件ツリー(系統図)から ToDo を自動展開する仕組み

## Contributing

Pull request や issue を歓迎します。追加するリソースは、次のいずれかに当てはまるものにしてください。

- 要件・ToDo・工程・割当・PDCA・ノウハウのいずれかを扱う
- MCP 対応、または MCP 経由で操作できる

## License

This work is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Credit: **shvtech**.

[![CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)
