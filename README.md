# Skill Home 技能库

**中文** | [English](README.en.md)

这是一个包含 **212 个 agent 技能**的个人技能库，每个技能一个 `.zip`。本页是技能目录：每个技能都写明了**它能做什么**、**怎么用**以及**最适合什么场景**，并按领域分组，方便你快速找到合适的技能。

- `00_212项压缩包清单.csv` —— 原始清单（技能名称、压缩包、类型、文件数、入口文件、SHA-256）。
- `00_使用说明.txt` —— 原始打包说明。
- 每个压缩包里的 `00_入口说明.txt` 写明了该技能的入口文件。

## 目录

- [快速查找：“我想要……”](#quick-finder)
- [如何安装技能](#how-to-install)
- [打包说明与注意事项](#packaging-notes)
- [按类别浏览](#catalog)
  - [AI 视频、影视与分镜](#cat-video) (24)
  - [编剧与讲故事](#cat-story) (14)
  - [AI 图像与摄影](#cat-image) (23)
  - [视觉风格分析与反推提示词](#cat-aesthetics) (7)
  - [3D 与产品渲染](#cat-image3d) (2)
  - [广告、产品演示与幻灯片](#cat-marketing) (4)
  - [社交媒体与创作者运营](#cat-social) (4)
  - [写作、作者文风与去 AI 味](#cat-writing) (4)
  - [调研、搜索与情报](#cat-research) (12)
  - [想法、产品管理与策略](#cat-product) (13)
  - [前端、UI 与设计系统](#cat-frontend) (15)
  - [架构、后端与数据](#cat-backend) (10)
  - [编程语言与项目模板](#cat-languages) (7)
  - [测试、调试与代码质量](#cat-testing) (7)
  - [DevOps、发布与可靠性](#cat-devops) (5)
  - [安全](#cat-security) (4)
  - [Git 与开源贡献](#cat-git) (5)
  - [编程 agent：Claude Code、Codex 与多 agent 协作](#cat-agents) (20)
  - [构建与管理技能](#cat-skills) (10)
  - [本地模型、GPU 与 API 网关](#cat-ai-infra) (3)
  - [网络与代理排障](#cat-network) (6)
  - [电脑与编辑器维护](#cat-system) (4)
  - [效率、知识库与报告](#cat-productivity) (4)
  - [学习与辅导](#cat-learning) (2)
  - [家居、旅行与生活](#cat-lifestyle) (3)

<a id="quick-finder"></a>
## 快速查找：“我想要……”

| 我想要…… | 可以先用 |
|---|---|
| 为一个镜头或场景写 Seedance 提示词 | [`seedance-clean`](#s-seedance-clean), [`Mx-Shell_Prompts`](#s-mx-shell-prompts), [`cinematic-fight-director`](#s-cinematic-fight-director) |
| 把剧本变成分镜和视频提示词 | [`storyboard-forge-20-25`](#s-storyboard-forge-20-25), [`script-scene-visual-storyboard`](#s-script-scene-visual-storyboard), [`mr-li-seedance-25`](#s-mr-li-seedance-25), [`分镜设计大师阶段1：导演设计器`](#s-zh-a4f0e6a7) |
| 用自己的角色翻拍参考视频 | [`scenerelay-reverse`](#s-scenerelay-reverse), [`motionprint-reverse`](#s-motionprint-reverse) |
| 从一个想法做出完整的 AI 短片或漫剧 | [`motion-drama-foundry`](#s-motion-drama-foundry), [`short-drama-producer`](#s-short-drama-producer), [`解说漫制片教练`](#s-zh-8927f55c) |
| 检查镜头之间的连续性 | [`jingqiao-continuity-supervisor`](#s-jingqiao-continuity-supervisor), [`AI视频空间调度导演`](#s-zh-b603f88d) |
| 剪辑真实视频文件（剪切、字幕、切片） | [`video-studio`](#s-video-studio), [`talking-head-fx-packager`](#s-talking-head-fx-packager), [`agentic-video-director`](#s-agentic-video-director) |
| 写电影或短剧剧本 | [`screenplay-factory`](#s-screenplay-factory), [`hollywood-omni-screenplay-master`](#s-hollywood-omni-screenplay-master), [`mass-appeal-super-screenwriter`](#s-mass-appeal-super-screenwriter), [`微短剧剧本创作`](#s-zh-b6e6af54) |
| 按原作风格续写小说或故事 | [`author-style-continuation`](#s-author-style-continuation), [`story-forge-engine`](#s-story-forge-engine), [`story-dynamics-workbench`](#s-story-dynamics-workbench) |
| 让角色、服装或产品在多张图里保持一致 | [`asset-continuity-imagegen`](#s-asset-continuity-imagegen), [`public-character-continuity`](#s-public-character-continuity), [`threadlock-wardrobe-skill-v1.0.0`](#s-threadlock-wardrobe-skill-v1-0-0) |
| 修图、修复或放大图片 | [`portrait-retouch`](#s-portrait-retouch), [`realistic-social-selfie-retouch`](#s-realistic-social-selfie-retouch), [`pic-fix-oneshot`](#s-pic-fix-oneshot), [`fidelity-4k-upscale-skill-v1.0`](#s-fidelity-4k-upscale-skill-v1-0) |
| 把参考图变成提示词或借用它的风格 | [`strong-image-reverse-prompt`](#s-strong-image-reverse-prompt), [`reference-rendering-reader`](#s-reference-rendering-reader), [`photographic-atmosphere-reconstruction`](#s-photographic-atmosphere-reconstruction), [`reverse-anything`](#s-reverse-anything) |
| 写小红书或其他社交内容 | [`xiaohongshu`](#s-xiaohongshu), [`xiaohongshu-netfeel-guardian`](#s-xiaohongshu-netfeel-guardian), [`creator-ops-os`](#s-creator-ops-os), [`topic-insight-writing`](#s-topic-insight-writing) |
| 做广告、海报或产品视频 | [`narrative-ad-engine`](#s-narrative-ad-engine), [`brand-short-drama`](#s-brand-short-drama), [`beetle-poster-director`](#s-beetle-poster-director), [`build-product-demo`](#s-build-product-demo) |
| 调研市场、行业或某个问题 | [`industry-intelligence-engine`](#s-industry-intelligence-engine), [`universal-research-architect`](#s-universal-research-architect), [`consulting-analysis`](#s-consulting-analysis), [`multi-ai-research`](#s-multi-ai-research) |
| 从一个原始想法走到 PRD | [`idea-team`](#s-idea-team), [`idea-to-product`](#s-idea-to-product), [`product-discovery`](#s-product-discovery), [`prd-master`](#s-prd-master) |
| 构建或重新设计网页 UI | [`frontend-design`](#s-frontend-design), [`frontend-art-director`](#s-frontend-art-director), [`ui-ux-pro-max`](#s-ui-ux-pro-max), [`figma-to-code`](#s-figma-to-code) |
| 新建一个代码库 | [`repo-scaffold`](#s-repo-scaffold), [`python-project`](#s-python-project), [`typescript-project`](#s-typescript-project), [`golang-web`](#s-golang-web), [`rust-project`](#s-rust-project) |
| 调试或审计代码 | [`systematic-debugging`](#s-systematic-debugging), [`codebase-audit`](#s-codebase-audit), [`project-health-auditor`](#s-project-health-auditor) |
| 搭建或整理 AGENTS.md / CLAUDE.md | [`agentsmd-scaffold`](#s-agentsmd-scaffold), [`repo-agent-context-audit`](#s-repo-agent-context-audit), [`agentsmd-optimize`](#s-agentsmd-optimize) |
| 在 Claude Code 里使用 Codex | [`codex`](#s-codex), [`codex-agent`](#s-codex-agent) |
| 创建、修复或整理技能 | [`skill-creator`](#s-skill-creator), [`skill-reforge-foundry`](#s-skill-reforge-foundry), [`self-evolution`](#s-self-evolution), [`skill-archive-manager`](#s-skill-archive-manager) |
| 解决代理或网络问题 | [`clash-doctor`](#s-clash-doctor), [`network-reconnect-repair`](#s-network-reconnect-repair), [`optimize-network`](#s-optimize-network), [`ip-check`](#s-ip-check) |
| 释放磁盘空间或让电脑变快 | [`storage-gc-guardian`](#s-storage-gc-guardian), [`disk-cleaner`](#s-disk-cleaner), [`system-doctor`](#s-system-doctor), [`vscode-doctor`](#s-vscode-doctor) |

<a id="how-to-install"></a>
## 如何安装技能

本仓库里有两种包。

**标准技能（202 个压缩包）**包含 `SKILL.md`，可用于 Claude Code、Codex 以及其他支持 Agent Skills 的运行环境。

1. 解压文件，打开 `00_入口说明.txt`（或查看 CSV 中的入口文件一列），找到入口 `SKILL.md`。
2. 把包含该 `SKILL.md` 的文件夹——连同它的 `references/`、`scripts/`、`assets/` 等——复制到你的 agent 技能目录。Claude Code 的个人技能目录是 `~/.claude/skills/<技能名>/`，项目技能目录是项目里的 `.claude/skills/<技能名>/`（[Claude Code 技能文档](https://code.claude.com/docs/en/skills)）。Codex 或其他运行环境请使用它们要求的技能目录（这里有好几个技能默认使用 `~/.agents/skills/`）。
3. 如果入口是单个文件，比如 `skills/brainstorming.SKILL.md`，就新建一个以技能名命名的文件夹，把文件放进去并改名为 `SKILL.md`。
4. 安装该技能“怎么用”里列出的依赖（Python 依赖、命令行工具、MCP 服务器、API key）。

大多数技能在你描述相应任务时会自动启用。少数技能只有点名时才会运行，条目里已注明。

**提示词型技能（10 个压缩包）**没有 `SKILL.md`。把入口文件作为系统提示词、自定义指令或第一条消息粘贴到任意聊天 AI，然后发送你的材料即可。下文中标为*提示词型*。

<a id="packaging-notes"></a>
## 打包说明与注意事项

**Spellbook 技能。** 其中 106 个压缩包来自 [Spellbook](https://github.com/majiayu000/spellbook) 技能库（前身为 Claude Arsenal）。这些压缩包每一个都包含*完整的* `spellbook-main/` 仓库（约 650 个文件）；技能本身只是入口路径处的那个文件夹或 `*.SKILL.md` 文件。如果想一次性安装整个库，Spellbook 也自带 `install.sh`。有几个 Spellbook 技能会把工作交给同系列的技能（例如 `idea-team` → `idea-research`、`idea-devils-advocate`、`idea-analogist`），这些最好一起安装。

**包含多个副本或版本的压缩包**

| 技能 | 包含内容 | 建议使用 |
|---|---|---|
| `huazhao-portrait-director` | v5.0.0 和 v6.0.0 | v6.0.0（更新） |
| `reverse-anything` | v1.0（`reverse-anything/`）和 v2.0（`reverse-anything__不同内容_0d88a8ba/`） | v2.0（覆盖更广，证据驱动） |
| `skill-reforge-foundry` | v5.1.0（英文）和更新的中文版 | 都可以；中文版侧重把对话萃取成技能 |
| `h3-video-editing-prompt` | `SKILL.md`（英文）和 `SKILL.cn.md`（中文） | 同一技能的两种语言 |
| `xuanshu-agent` | 完整的 xuanshu-skill 仓库，含两个入口文件 | `skills/xuanshu-agent/SKILL.md` 是完整指南 |
| `feishu-rent-billing` | 当前技能和一份备份 | 根目录的 `feishu-rent-billing/SKILL.md` |
| `app-ui-design`、`figma-to-react`、`frontend-design`、`ui-design-system`、`idea-analogist`、`idea-devils-advocate`、`idea-research`、`idea-team`、`idea-to-product`、`rust-best-practices` | 一份核心版和一份 Spellbook 插件版 | 只装一份，避免重复触发 |

**重叠。** `figma-to-code` 和 `figma-to-react` 是同一个生成器的两个名字。`anysearch`、`consulting-analysis`、`research-guide` 和 `research-hub` 这几个压缩包里都是同一个 `大调查` 调研包。

**使用前需要调整**

- `gpu-use` —— `SKILL.md` 里默认的 SSH 服务器是原作者的，请换成你自己的。
- `weekly` —— 写死了某个项目的前端和后端仓库（“om-generator”），请修改仓库名和路径。
- `meta-timing` —— 声明依赖的技能（`agent-harness-loop`、`scr-judgment`）不在本仓库中。
- `react-hooks-best-practices` —— 需要搭配的 `typescript-best-practices` 技能不在本仓库中。
- `research-hub` —— 它路由到的 video-download、book-ingest 和 knowledge-* 技能不在本仓库中。
- `skill-archive-manager` —— 属于 `archive-center-suite` 套件，依赖该套件的工具。
- `分镜设计大师阶段2` / `分镜设计大师阶段3` —— 两个压缩包*里面*的文件名互换了。压缩包名是对的：阶段 2 的压缩包里是阶段 2 装配器，阶段 3 的压缩包里是阶段 3 转换器。

<a id="catalog"></a>
# 按类别浏览

每个类别先有一张一句话概览表，后面是完整条目。

<a id="cat-video"></a>
## AI 视频、影视与分镜

AI 视频（Seedance、MiniMax H3、即梦等）的导演与提示词、分镜、连续性、剪辑和全流程生产。

| 技能 | 最适合 |
|---|---|
| [`agentic-video-director`](#s-agentic-video-director) | 交付物必须是渲染好的视频文件（而不只是提示词）的端到端制作。 |
| [`atmospheric-character-short-director`](#s-atmospheric-character-short-director) | 竖屏人物氛围短片。 |
| [`cinematic-fight-director`](#s-cinematic-fight-director) | 看得清、物理上可信的 AI 视频打斗编排。 |
| [`fengyun-jue-rebuilder`](#s-fengyun-jue-rebuilder) | 用新的视觉风格重新演绎这部动画电影的同人创作。 |
| [`h3-video-editing-prompt`](#s-h3-video-editing-prompt) | 用 MiniMax H3 做精确的遮罩区域和物体替换编辑。 |
| [`interactive-film-ui-fusion`](#s-interactive-film-ui-fusion) | 在互动视频上加一层干净、有电影感的交互。 |
| [`jingqiao-continuity-supervisor`](#s-jingqiao-continuity-supervisor) | 在花额度生成视频之前抓出连续性错误。 |
| [`live-mv-weaver`](#s-live-mv-weaver) | 带观众故事线的现场演出 MV。 |
| [`motion-drama-foundry`](#s-motion-drama-foundry) | 把漫剧或 AI 短片从想法推进到可直接生成的制作包。 |
| [`motionprint-reverse`](#s-motionprint-reverse) | 还原参考视频“怎么动”，而不只是“长什么样”。 |
| [`mr-li-seedance-25`](#s-mr-li-seedance-25) | 从定稿剧本出发，逐段忠实地用 Seedance 制作。 |
| [`Mx-Shell_Prompts`](#s-mx-shell-prompts) | 从粗糙的叙事文字写出 Seedance 2.0 提示词。 |
| [`scenerelay-reverse`](#s-scenerelay-reverse) | 在 Seedance 2.5 里用你自己的角色和世界翻拍参考视频。 |
| [`script-scene-visual-storyboard`](#s-script-scene-visual-storyboard) | 把文字场景变成一组可信的画面序列。 |
| [`seedance-clean`](#s-seedance-clean) | 干净的单条 Seedance 2.0 镜头和场景提示词。 |
| [`short-drama-producer`](#s-short-drama-producer) | 一套可直接用于即梦的完整短剧制作包。 |
| [`storyboard-forge-20-25`](#s-storyboard-forge-20-25) | 规划一段可生成、可剪辑的 AI 视频序列。 |
| [`talking-head-fx-packager`](#s-talking-head-fx-packager) | 为口播类视频做有品位的特效和字幕包装。 |
| [`video-studio`](#s-video-studio) | 通过聊天在本地剪辑口播视频和直播切片。 |
| [`AI视频空间调度导演`](#s-zh-b603f88d) | 让多镜头 AI 视频里的房间布局、人物站位和镜头路线保持一致——面向不懂技术的创作者。 |
| [`分镜设计大师阶段1：导演设计器`](#s-zh-a4f0e6a7) | 在生成任何分镜图之前先把导演设计锁定。 |
| [`分镜设计大师阶段2：分镜图Skill装配器`](#s-zh-18d9bfd6) | 把锁定的导演设计变成风格一致的分镜图。 |
| [`分镜设计大师阶段3：视频提示词转换器`](#s-zh-5a8eb463) | 从已定稿的分镜得到忠实的逐镜视频提示词。 |
| [`解说漫制片教练`](#s-zh-8927f55c) | 零基础学生一步一步制作解说漫。 |

<a id="s-agentic-video-director"></a>
### agentic-video-director

[agentic-video-director.zip](agentic-video-director.zip) · 入口：`agentic-video-director-v1.0.0/SKILL.md`

- **能做什么：** 让编程 agent 真正产出视频文件：把意图转成带时间的镜头合同，选择最轻的制作路线，渲染后检查实际画面和音频，修复问题并交付文件。包含针对 Claude Opus 5.5 和 GPT-6 的说明、MV 卡点、质量闸门、脚本和模板。
- **怎么用：** 在 Claude Code 或 Codex 里，让它制作、剪辑、修复或完成视频、MV、宣传片、发布片、讲解视频或动态图形；提供素材、音乐和目标时长。
- **最适合：** 交付物必须是渲染好的视频文件（而不只是提示词）的端到端制作。

<a id="s-atmospheric-character-short-director"></a>
### atmospheric-character-short-director

[atmospheric-character-short-director.zip](atmospheric-character-short-director.zip) · 入口：`视频分镜skill导演.md`

- **能做什么：** 执导 5–15 秒、以人物为中心的 AI 氛围短片——角色展示、美妆/服装氛围片、古风人像、克制的浪漫、竖屏社交宣传。把一个想法或参考图变成镜头设计和可直接使用的视频提示词，并在单镜头连续表演、一次生成的短多镜头、分别生成再剪辑之间做选择。
- **怎么用：** 入口文件是 `视频分镜skill导演.md`。描述人物、氛围和发布平台（可附参考图）。不适合长剧情、多人对话或打斗场面。
- **最适合：** 竖屏人物氛围短片。

<a id="s-cinematic-fight-director"></a>
### cinematic-fight-director

[cinematic-fight-director.zip](cinematic-fight-director.zip) · 入口：`cinematic-fight-director-public-v4.0.0/SKILL.md`

- **能做什么：** 以导演思维为先的 AI 打斗戏提示词编译器，针对 Seedance 2.5 优化，也可适配其他模型。用“动作包”和六把锁（身份、空间、物理、节奏、镜头、风格）、动作密度设置、动量连续、冲击层级以及多敌人/腾空规则，让动作快速、有物理感且连贯。
- **怎么用：** 提供打斗构想、剧本片段、角色图、分镜或动作参考，得到可直接用于制作的视频提示词（可选克制 / 动感 / 超高密度）。
- **最适合：** 看得清、物理上可信的 AI 视频打斗编排。

<a id="s-fengyun-jue-rebuilder"></a>
### fengyun-jue-rebuilder

[fengyun-jue-rebuilder.zip](fengyun-jue-rebuilder.zip) · 入口：`fengyun-jue-rebuilder/SKILL.md`

- **能做什么：** 重建或重新演绎《风云决》的角色、场景、打斗、预告片和音乐驱动片段。使用三个相互独立的引擎——叙事、打斗和风格——只在镜头包处汇合，人物身份作为固定不变量。模式：CHARACTER_ASSET、SHOT_REPLICA、NARRATIVE_REBUILD、COMBAT_REBUILD、MUSIC_REBUILD、TRAILER_REBUILD。
- **怎么用：** 选择模式，提供原片场景或角色，以及单独定义的目标视觉风格；最终生成前有审批关卡。
- **最适合：** 用新的视觉风格重新演绎这部动画电影的同人创作。

<a id="s-h3-video-editing-prompt"></a>
### h3-video-editing-prompt

[h3-video-editing-prompt.zip](h3-video-editing-prompt.zip) · 入口：`h3-video-editing-prompt/SKILL.md` · `h3-video-editing-prompt/SKILL.cn.md`

- **能做什么：** 用全参考 Ref2VA 六段格式编写 MiniMax H3 视频编辑提示词：换脸与身份替换、服装、手持或场景物体、背景、画内文字、材质、光照、物体移除或新增以及视频续写。核心规则：描述最终视频里看到什么，而不是操作本身（不写“swap”“remove”）。包含可见行为与动作迁移清单和场景配方；有英文和中文两个版本；也可作为 ComfyUI 节点的提示词使用。
- **怎么用：** 提供源视频描述和参考素材，说明要改什么（“把苹果换成这个西瓜”“把这张脸放进视频”“改成黄昏光”）。默认只输出英文提示词正文。
- **最适合：** 用 MiniMax H3 做精确的遮罩区域和物体替换编辑。

<a id="s-interactive-film-ui-fusion"></a>
### interactive-film-ui-fusion

[interactive-film-ui-fusion.zip](interactive-film-ui-fusion.zip) · 入口：`interactive-film-ui-fusion-v1.1.0/SKILL.md`

- **能做什么：** 为互动电影、FMV、分支 AI 视频、可玩短片、H5 体验和电影化游戏设计可见的交互层：HUD/UI 素材、热点、QTE 呈现、交互反馈、贴合视频的叠加层、动效状态、空间锚点、分镜/预演评审和运行时 UI 交接。剧情和分支状态仍由上游制作系统负责。
- **怎么用：** 提供分支图或节点列表以及视频背景；它会产出标准事件时间线、UI 组件和可交给渲染端的交接文档。只加载当前任务需要的参考文件。
- **最适合：** 在互动视频上加一层干净、有电影感的交互。

<a id="s-jingqiao-continuity-supervisor"></a>
### jingqiao-continuity-supervisor

[jingqiao-continuity-supervisor.zip](jingqiao-continuity-supervisor.zip) · 入口：`jingqiao-continuity-supervisor/SKILL.md`

- **能做什么：** “镜桥 2.0”——AI 视频分镜提示词和生成片段的连续性监督。把每个镜头看作“进入状态 → 事件 → 离开状态”，在整个序列中检查身份、持续状态（道具、服装、伤痕）、动作衔接、时空和因果，区分合法省略、故意硬切和真正的穿帮。用最小改动修复；支持 Seedance 2.0 多镜头和续写。
- **怎么用：** 粘贴两条到几十条镜头提示词（或片段），说“检查连续性”或“修好跳接”。它会返回标出的问题切口和修正后的提示词，要求时给出完整修正版。
- **最适合：** 在花额度生成视频之前抓出连续性错误。

<a id="s-live-mv-weaver"></a>
### live-mv-weaver

[live-mv-weaver.zip](live-mv-weaver.zip) · 入口：`live-mv-weaver/SKILL.md`

- **能做什么：** 制作或重建这样的音乐 MV：一首完整的现场演唱作为主时间线，穿插反复出现的观众反应、场内对白、乐队细节、前后呼应和同一地点的小剧情。REPLICA 模式复刻参考 MV 的结构；REPLICA_PLUS 保留语法，同时提升表演、连续性、音频和剪辑。
- **怎么用：** 提供歌曲（含起止时间），最好附上参考 MV；它会产出锁定的歌曲时间线、镜头计划和生成包。
- **最适合：** 带观众故事线的现场演出 MV。

<a id="s-motion-drama-foundry"></a>
### motion-drama-foundry

[motion-drama-foundry.zip](motion-drama-foundry.zip) · 入口：`motion-drama-foundry/SKILL.md`

- **能做什么：** 一体化漫剧 / AI 视频生产：从一句话故事、剧本或现有素材出发，完成故事开发、剧本、人物/场景/道具资产定义、分镜、跨镜连续性、视频生成提示词以及声音/剪辑交接。全程只认一份“项目账本”作为事实来源。
- **怎么用：** 模式自动判定：FULL RUN（“从这个故事一路做完”）、TAKEOVER（从你已有的内容继续）、STAGE ONLY（只做某一步）、REPAIR（修复跑偏的图、视频或提示词）。说明书见 `使用说明书.pdf`。
- **最适合：** 把漫剧或 AI 短片从想法推进到可直接生成的制作包。

<a id="s-motionprint-reverse"></a>
### motionprint-reverse

[motionprint-reverse.zip](motionprint-reverse.zip) · 入口：`MOTIONPRINT-REVERSE-1.1/SKILL.md`

- **能做什么：** 把任意 AI 视频反推成高执行度的视频提示词，重点还原运动、运镜、节奏、空间和环境响应（七枚“动态指纹”），而不是堆砌画面标签。模式：快速、完整、多镜头、对比修补（只修最大的三处偏差）和增强重构。
- **怎么用：** 上传视频、片段或关键帧序列；默认输出完整的动态指纹卡以及 Core、Directed 和平台版提示词。把你生成的结果也上传，就能进入对比修补循环。
- **最适合：** 还原参考视频“怎么动”，而不只是“长什么样”。

<a id="s-mr-li-seedance-25"></a>
### mr-li-seedance-25

[mr-li-seedance-25.zip](mr-li-seedance-25.zip) · 入口：`mr-li-seedance-25/SKILL.md`

- **能做什么：** “李先生 Seedance 通用创作规则”——按真实表演容量，把一份权威中文剧本拆成可直接提交的 Seedance 分段提示词，一次只写一个自然生成段。区分文戏和动作戏的写法，处理视觉基调、素材绑定与资产制作、结果返工和交付审阅，不擅自改写对白或剧情。
- **怎么用：** 第一次使用时会说明七个阶段（锁定剧本、制作范围、创作基调、资产、分段提示词、返工、收束）；之后用“确认继续”“跳过资产”“做 1-1”“继续下一段”“只改站位”等话控制流程。如果宿主只能加载一个文件，用 `references/universal-runtime.md`。
- **最适合：** 从定稿剧本出发，逐段忠实地用 Seedance 制作。

<a id="s-mx-shell-prompts"></a>
### Mx-Shell_Prompts

[Mx-Shell_Prompts.zip](Mx-Shell_Prompts.zip) · *提示词型* · 入口：`内层包/Mx-Shell_Prompts_v1.5/Mx-Shell_Prompts_v1.5.md`

- **能做什么：** 把故事大纲、剧本片段、分镜草稿、小说段落或口播文案转成结构化、影视级的 Seedance 2.0 视频提示词，时间轴精确到秒，采用“物理优先”（非文学化）的描述。支持一镜到底和多机位分镜两种模式。
- **怎么用：** 把 `Mx-Shell_Prompts_v1.5.md` 作为提示词加载。它会依次询问模式、角色/道具/场景描述（有参考图时简短，没有时详细）、氛围与画质、声音规则、对白/画外音和画面内容，然后输出完整提示词。
- **最适合：** 从粗糙的叙事文字写出 Seedance 2.0 提示词。

<a id="s-scenerelay-reverse"></a>
### scenerelay-reverse

[scenerelay-reverse.zip](scenerelay-reverse.zip) · 入口：`scenerelay-reverse/SKILL.md`

- **能做什么：** “SceneRelay Reverse 3.1”——把参考视频改编成可直接进入 Seedance 2.5 的制作：逐镜反推、拆解戏剧功能，替换人物、场景或道具时自动计算“替换涟漪”，写出因果闭合的新版镜头剧本，交付真实的参考图包（每张图的职责和上传顺序），并为每个生成段给出一段可直接复制的 Seedance 正文。生成跑偏时修复最早的偏差。支持多轮项目接续。
- **怎么用：** 上传参考视频和（现在或稍后）你的替换人物/场景/道具；说“分析完直接给我参考图和 Seedance 提示词”。
- **最适合：** 在 Seedance 2.5 里用你自己的角色和世界翻拍参考视频。

<a id="s-script-scene-visual-storyboard"></a>
### script-scene-visual-storyboard

[script-scene-visual-storyboard.zip](script-scene-visual-storyboard.zip) · 入口：`script-scene-visual-storyboard-v1.0.0/SKILL.md`

- **能做什么：** 把剧本、场景、故事段落或对白转成空间连贯、有情绪目的的分镜：场景真相 → 可见证据 → 空间模型 → 压力曲线 → 画面设计，配合锚点/支撑/标点镜头、连续性规则和与模型无关的分镜图提示词。模式：直接分镜、镜头设计、视觉分镜板、预演/连续性。
- **怎么用：** 粘贴场景或剧本，要求分镜、镜头列表、走位或分镜图提示词。
- **最适合：** 把文字场景变成一组可信的画面序列。

<a id="s-seedance-clean"></a>
### seedance-clean

[seedance-clean.zip](seedance-clean.zip) · 入口：`higg导演/SKILL.md`

- **能做什么：** 以“只写看得见的东西”为核心的 Seedance 2.0 提示词写作系统：把情绪翻译成可观察的动作、光线和镜头；涵盖素材标注、上下文隔离、分布式风格、剪辑与时长、导演调度、光学（景别、焦段/视场角锚点）、特殊规程和写前检查清单。始终输出一条放在代码块里的独立提示词。
- **怎么用：** 说“写一条 Seedance 提示词……”“做一个……的镜头”，或询问 Seedance 写法。包的文件夹是 `higg导演/`；里面还有一个打包好的 `seedance-clean_v2.skill` 文件。
- **最适合：** 干净的单条 Seedance 2.0 镜头和场景提示词。

<a id="s-short-drama-producer"></a>
### short-drama-producer

[short-drama-producer.zip](short-drama-producer.zip) · 入口：`short-drama-producer/SKILL.md`

- **能做什么：** 面向 AI 视频的短剧全流程生产：剧本、分镜表、人物/道具/场景资产卡和即梦视频提示词，带 AI 自检和交付清单。支持单集（3–5 分钟）和多集系列。
- **怎么用：** 可从主题（模式 A）、大纲（模式 B）或已有剧本（模式 C）开始。模式 A/B 会先询问题材、角色、情绪基调、集数和品牌限制。
- **最适合：** 一套可直接用于即梦的完整短剧制作包。

<a id="s-storyboard-forge-20-25"></a>
### storyboard-forge-20-25

[storyboard-forge-20-25.zip](storyboard-forge-20-25.zip) · 入口：`storyboard-forge-20-25-v2.0.0/SKILL.md`

- **能做什么：** 面向 Seedance 2.0/2.5 和其他 AI 视频工具的导演级分镜与镜头规划。把剧本、概念、广告、动作戏、对话戏、MV/演出、产品片、预告片、恐怖、喜剧、动漫和纪录片简报转成按模型路由的分镜、镜头合同、连续性锁定、参考图方案、生成提示词、重拍计划和剪辑交接。
- **怎么用：** 提供剧本或简报（如有参考图一并提供）；它会先推断再提问，并按你需要的模式输出。可直接调用。
- **最适合：** 规划一段可生成、可剪辑的 AI 视频序列。

<a id="s-talking-head-fx-packager"></a>
### talking-head-fx-packager

[talking-head-fx-packager.zip](talking-head-fx-packager.zip) · 入口：`talking-head-fx-packager-v1.0.0/SKILL.md`

- **能做什么：** 口播、vlog、知识讲解、测评和教程视频的包装导演：把讲稿、逐字稿、SRT/VTT 或粗剪时间线变成克制、可直接交给剪辑的方案——字幕、重点字卡、标注、推镜、叠加层、B-roll 提示词、UI 卡片、转场和音效——带密度预算和“防过度包装”检查。不改写内容。
- **怎么用：** 提供讲稿或字幕，说“把这条口播包装一下”或“加字幕和重点字卡，别太花”。适用于 9:16、1:1 和 16:9，以及剪映、Premiere、After Effects、DaVinci 或 Remotion。
- **最适合：** 为口播类视频做有品位的特效和字幕包装。

<a id="s-video-studio"></a>
### video-studio

[video-studio.zip](video-studio.zip) · 入口：`video-studio/skills/video-studio/SKILL.md`

- **能做什么：** 在 Claude Code 里本地、对话式地剪辑和生成视频（ffmpeg + Python，HyperFrames 把 HTML 转成 MP4）：口播精剪（去口癖、重录和空白，推镜，烧录中文字幕）、直播切片（在几小时的直播里找高光，批量切 9:16 片段并配标题、封面和文案），以及用代码生成带 TTS 配音的数据/产品讲解动画。还支持 16:9 转 9:16、字幕、背景音乐闪避、响度和各平台导出（抖音、视频号、小红书、B 站、YouTube）。
- **怎么用：** 每台电脑先做一次设置（见 SKILL.md；安装 `requirements.txt`），然后说“剪掉口误”“从这场直播里切高光”“加字幕”“做一个竖屏版”或“做一个数据动画”。基于逐字转写工作，渲染前会先确认。
- **最适合：** 通过聊天在本地剪辑口播视频和直播切片。

<a id="s-zh-b603f88d"></a>
### AI视频空间调度导演

[AI视频空间调度导演.zip](AI%E8%A7%86%E9%A2%91%E7%A9%BA%E9%97%B4%E8%B0%83%E5%BA%A6%E5%AF%BC%E6%BC%94.zip) · *提示词型* · 入口：`AI视频空间调度导演-开源傻瓜版-v1.0/02-完整主提示词.md`

- **能做什么：** 一套通俗易懂的提示词包，把剧本整理成 AI 视频制作方案：3×3 九宫格空场景提示词、俯视人物与摄影机调度图提示词、建议镜头数（1–4 个）及理由、每个镜头可直接复制的视频提示词，以及最可能失败的三个地方和补救词。
- **怎么用：** 不是 SKILL.md 技能。把 `02-完整主提示词.md` 粘贴到任意文本大模型，再用 `03-客户填写模板.md` 发送剧本。生成出问题时用 `04-失败诊断器.md`；`05` 是完整示例。
- **最适合：** 让多镜头 AI 视频里的房间布局、人物站位和镜头路线保持一致——面向不懂技术的创作者。

<a id="s-zh-a4f0e6a7"></a>
### 分镜设计大师阶段1：导演设计器

[分镜设计大师阶段1：导演设计器.zip](%E5%88%86%E9%95%9C%E8%AE%BE%E8%AE%A1%E5%A4%A7%E5%B8%88%E9%98%B6%E6%AE%B51%EF%BC%9A%E5%AF%BC%E6%BC%94%E8%AE%BE%E8%AE%A1%E5%99%A8.zip) · *提示词型* · 入口：`内层包/分镜设计大师/分镜设计大师/01_阶段1_导演设计器_项目交接包A.txt`

- **能做什么：** 三阶段 AI 视频预演流水线的第一阶段：根据你的剧情、角色、场景、参考图、镜头数量、画布比例和风格要求，完成完整的导演设计（核心美学、统一影像母版、角色与空间锁定、画布与排版锁定、镜头节奏、每一镜的关键帧），并输出【项目交接包 A】——阶段 2 和阶段 3 唯一的上游源文件。
- **怎么用：** 提示词型：把 `01_阶段1_导演设计器_项目交接包A.txt` 粘贴到文本大模型，再发送你的故事和要求。把交接包 A 带到阶段 2。
- **最适合：** 在生成任何分镜图之前先把导演设计锁定。

<a id="s-zh-18d9bfd6"></a>
### 分镜设计大师阶段2：分镜图Skill装配器

[分镜设计大师阶段2：分镜图Skill装配器.zip](%E5%88%86%E9%95%9C%E8%AE%BE%E8%AE%A1%E5%A4%A7%E5%B8%88%E9%98%B6%E6%AE%B52%EF%BC%9A%E5%88%86%E9%95%9C%E5%9B%BESkill%E8%A3%85%E9%85%8D%E5%99%A8.zip) · *提示词型* · 入口：`内层包/分镜设计大师/分镜设计大师/03_阶段3_分镜图转Seedance视频提示词转换器.txt`

- **能做什么：** 读取【项目交接包 A】，在不重新设计任何内容的前提下，把它压缩成图像模型可以执行的分镜板总提示词（自适应画布、排版、信息条），生成前做继承自校，生成后做图像质检，然后输出【项目交接包 B】。
- **怎么用：** 提示词型：把提示词文件和交接包 A 一起粘贴到文本大模型。注意：这个压缩包里的文件名是 `03_阶段3_分镜图转Seedance视频提示词转换器.txt`，但内容其实是阶段 2 装配器——阶段 2 和阶段 3 的内部文件名互换了，压缩包名是对的。
- **最适合：** 把锁定的导演设计变成风格一致的分镜图。

<a id="s-zh-5a8eb463"></a>
### 分镜设计大师阶段3：视频提示词转换器

[分镜设计大师阶段3：视频提示词转换器.zip](%E5%88%86%E9%95%9C%E8%AE%BE%E8%AE%A1%E5%A4%A7%E5%B8%88%E9%98%B6%E6%AE%B53%EF%BC%9A%E8%A7%86%E9%A2%91%E6%8F%90%E7%A4%BA%E8%AF%8D%E8%BD%AC%E6%8D%A2%E5%99%A8.zip) · *提示词型* · 入口：`内层包/分镜设计大师/分镜设计大师/02_阶段2_自适应画布分镜图Skill装配器_项目交接包B.txt`

- **能做什么：** 读取【项目交接包 B】，在原始剧情、导演设计、分镜图提示词和最终分镜板的共同约束下，逐镜写出 Seedance / AI 视频提示词——让运动服从设计，而不是看图即兴发挥。
- **怎么用：** 提示词型：把提示词文件和交接包 B 一起粘贴到文本大模型。注意：这个压缩包里的文件名是 `02_阶段2_自适应画布分镜图Skill装配器_项目交接包B.txt`，但内容其实是阶段 3 转换器（与阶段 2 的文件名互换了）。
- **最适合：** 从已定稿的分镜得到忠实的逐镜视频提示词。

<a id="s-zh-8927f55c"></a>
### 解说漫制片教练

[解说漫制片教练.zip](%E8%A7%A3%E8%AF%B4%E6%BC%AB%E5%88%B6%E7%89%87%E6%95%99%E7%BB%83.zip) · *提示词型* · 入口：`解说漫生产系统_v3.0_完整管理版_RELEASE/学生公开运行时/00_直接发给AI.md`

- **能做什么：** “解说漫生产系统 v3.0”——把原始故事编译成解说漫：剧情账本 → 高质量解说稿（四遍自动改稿、内部双稿竞争、100 分硬验收）→ 镜头生产卡和角色/场景连续性 → 图片任务 → 动态视频任务 → 配音、字幕和剪辑 → 成片终检。专为完全零基础的学生设计：每轮只显示“现在做到哪 / AI 已完成什么 / 你现在只做什么 / 复制什么 / 正确结果长什么样”。
- **怎么用：** 提示词型：把 `00_直接发给AI.md` 和你的原作资料一起发给能读长文件的聊天 AI，然后说“开始制作”。只需要六句话：开始制作、下一步、我不会、检查这个、只修这个 + 编号、准备交付。包里还有学生极速上手和常见问题文件。
- **最适合：** 零基础学生一步一步制作解说漫。

<a id="cat-story"></a>
## 编剧与讲故事

电影长片、短剧、情景喜剧、小说续写和故事世界模拟。

| 技能 | 最适合 |
|---|---|
| [`audience-psychology-engine`](#s-audience-psychology-engine) | 在开拍前或粗剪后检验预期的情绪点是否真的能打动观众。 |
| [`brand-short-drama`](#s-brand-short-drama) | 品牌/植入类短剧和本地商家剧情广告。 |
| [`fanqie-shortstory-forge`](#s-fanqie-shortstory-forge) | 适合番茄读者的高完成度短篇小说。 |
| [`genre-writer`](#s-genre-writer) | 需要先做扎实设计再动笔的长篇类型故事。 |
| [`hollywood-omni-screenplay-master`](#s-hollywood-omni-screenplay-master) | 结构扎实、对白令人难忘的电影长片剧本。 |
| [`mass-appeal-super-screenwriter`](#s-mass-appeal-super-screenwriter) | 让故事一上来就抓住大众观众。 |
| [`screenplay-factory`](#s-screenplay-factory) | 尊重电影与短剧差异的剧本开发。 |
| [`screenwriting-master`](#s-screenwriting-master) | 任何格式下有引导、分步骤的剧本创作。 |
| [`story-dynamics-workbench`](#s-story-dynamics-workbench) | 因果和人物心理都必须保持一致的长篇复杂故事。 |
| [`story-forge-engine`](#s-story-forge-engine) | 以令人信服的因果逻辑续写已有故事。 |
| [`viral-framework-analyzer`](#s-viral-framework-analyzer) | 弄清某个类型里头部作品到底强在哪里。 |
| [`writing-ensemble-sitcoms`](#s-writing-ensemble-sitcoms) | 对白自然、而不是舞台式抖包袱的固定班底喜剧。 |
| [`微短剧剧本创作`](#s-zh-b6e6af54) | 为短视频平台写一部完整的付费微短剧。 |
| [`故事世界模拟-v4.0.0`](#s-zh-a64c64af) | 严谨、不破坏正史地模拟复杂的故事世界。 |

<a id="s-audience-psychology-engine"></a>
### audience-psychology-engine

[audience-psychology-engine.zip](audience-psychology-engine.zip) · 入口：`audience-psychology-engine/SKILL.md`

- **能做什么：** 面向 AI 电影、影视、短剧和漫剧的“观众心理审判层”。模拟一个不知道后文、注意力和记忆都有限的真实观众，跟踪“观众状态时间线”，检验开场钩子、悬念、反转、角色投入和粗剪，再把每个问题归因到编剧、导演或剪辑并给出反馈包。绝不编造观众数据。
- **怎么用：** 给它剧本、分镜或粗剪，问“观众看得懂吗？”“观众会在哪里流失？”或“这个反转成立吗？”。可以和编剧、导演、剪辑类技能联动。
- **最适合：** 在开拍前或粗剪后检验预期的情绪点是否真的能打动观众。

<a id="s-brand-short-drama"></a>
### brand-short-drama

[brand-short-drama.zip](brand-short-drama.zip) · 入口：`短剧植入技能包/brand-short-drama/SKILL.md`

- **能做什么：** 写带产品或本地服务植入的爆款短剧（电商商品、温泉、漂流、餐饮、景区、民宿酒店、门店）。拆解卖点，把目标人群匹配到热门题材，设计植入方式，再写分集大纲、正文剧本，并做双重质检（爆款感和植入自然度）。核心原则：产品是故事里的“金手指”或“命门”——角色永远不替它念广告。
- **怎么用：** 提供产品或门店、目标人群和集数（“给我的温泉度假村写一部品牌短剧”）。它会交付产品拆解卡、三个方案及推荐、人物小传、情绪曲线、剧本、质检报告以及拍摄与合规备注。
- **最适合：** 品牌/植入类短剧和本地商家剧情广告。

<a id="s-fanqie-shortstory-forge"></a>
### fanqie-shortstory-forge

[fanqie-shortstory-forge.zip](fanqie-shortstory-forge.zip) · 入口：`fanqie-shortstory-forge-v1.1.0/SKILL.md`

- **能做什么：** 番茄短故事专用的创作与审稿技能：选题、卖点、开篇钩子、情绪曲线、短篇结构、人物、正文、标题简介、平台化审查、改编潜力和返工。支持多种题材（都市情感、复仇逆袭、悬疑、现实治愈、古言、玄幻、科幻、规则怪谈等）。
- **怎么用：** 提供脑洞、大纲或旧稿，可附字数、题材、受众和情绪。它会自动路由：脑洞成文、出大纲、写全文、改写、审稿、对标拆解或平台风向（被要求时会联网核实当前平台规则）。
- **最适合：** 适合番茄读者的高完成度短篇小说。

<a id="s-genre-writer"></a>
### genre-writer

[genre-writer.zip](genre-writer.zip) · 入口：`genre-writer/SKILL.md`

- **能做什么：** 类型小说与剧本创作系统，覆盖悬疑推理、奇幻、科幻、剧本（影视、短剧、剧本杀）和世界观设计。流程：立项契约 → 拆解对标作品并建立文风档案 → 设计（真相表、规则代价表、核心变量推演、场景表）→ 逐章写作 → 分角色审稿和去 AI 味检查脚本。所有状态都存在 `story/` 文件夹里，换会话也能接上。
- **怎么用：** 说你想写小说或剧本、设计诡计、搭建力量体系或世界观、拆解对标作品、提取文风、检查一致性或去 AI 味。
- **最适合：** 需要先做扎实设计再动笔的长篇类型故事。

<a id="s-hollywood-omni-screenplay-master"></a>
### hollywood-omni-screenplay-master

[hollywood-omni-screenplay-master.zip](hollywood-omni-screenplay-master.zip) · 入口：`好莱坞全能电影剧本大师系统-v3.0.0/SKILL.md`

- **能做什么：** “好莱坞全能电影剧本大师”，面向电影长片：在长片、短片、剧集、单场修稿和对白手术之间自动路由，然后运行流水线：需求锁定、故事核心、结局方向、大纲、长片结构（中点反转、危机抉择、高潮归属）、反派自主性、场景引擎、排练式对白、故事状态追踪、伏笔回收、改稿实验室和最终审计。核心规则：因果高于节拍、对手同样聪明、对白即行动、只修失败的那一层。
- **怎么用：** 提供故事前提、大纲或已有剧本，说明是要开发、写完整初稿、改写、诊断还是打磨对白。
- **最适合：** 结构扎实、对白令人难忘的电影长片剧本。

<a id="s-mass-appeal-super-screenwriter"></a>
### mass-appeal-super-screenwriter

[mass-appeal-super-screenwriter.zip](mass-appeal-super-screenwriter.zip) · 入口：`mass-appeal-super-screenwriter-v1.0.0/SKILL.md`

- **能做什么：** 面向大众的编剧：理解成本低、情绪电压高、冲突即刻出现、每集有强钩子，摆脱重复的 AI 式剧情。八个引擎（从“核爆式开场”开始）和多道关卡；工作流包括想法成故事、分集写作、诊断与抢救、改写。
- **怎么用：** 提供故事前提、分集简报或已有草稿，说明要创作、写作、诊断还是改写。适用于短剧、电影、剧集、竖屏视频和剧情广告。
- **最适合：** 让故事一上来就抓住大众观众。

<a id="s-screenplay-factory"></a>
### screenplay-factory

[screenplay-factory.zip](screenplay-factory.zip) · 入口：`screenplay-factory/SKILL.md`

- **能做什么：** 双引擎剧本工厂：先判断作品是 FEATURE_FILM（电影长片）还是 SHORT_DRAMA（短剧、微短剧、漫剧），再使用对应引擎的结构、节奏、人物变化、信息释放和结局——人物、场景、对白、因果、改编和格式共享同一底层。可开发、改编（如小说改剧本）、写作、续写、重写和审稿。只做文本，不做分镜或媒体生成。
- **怎么用：** 提供点子、小说、梗概、人物或已有剧本，说明你需要什么（大纲、分集、场景表、完整剧本、重写、去 AI 味、审查）。
- **最适合：** 尊重电影与短剧差异的剧本开发。

<a id="s-screenwriting-master"></a>
### screenwriting-master

[screenwriting-master.zip](screenwriting-master.zip) · 入口：`screenwriting-master/SKILL.md`

- **能做什么：** “山音超级编剧大师”（由 @山音 设计）：全格式编剧，从 1–3 分钟概念短片（how-to-tell / what-if）、5–10 分钟叙事短片，到 90 分钟长片和多集剧集，覆盖人物设计、结构（Save the Cat、Story Circle、McKee）、场景拆解和完整剧本。严格红线：不写心理描写、不写解释性台词，一切都必须能被摄影机拍到。
- **怎么用：** 说“写剧本 / 短片 / 电影 / 剧集”“帮我想个故事”或“这场戏不对”。它按步骤推进，每步完成后等你批准；说“[自检]”可查看它的检查清单评估。
- **最适合：** 任何格式下有引导、分步骤的剧本创作。

<a id="s-story-dynamics-workbench"></a>
### story-dynamics-workbench

[story-dynamics-workbench.zip](story-dynamics-workbench.zip) · 入口：`story-dynamics-workbench-v2.0.0/SKILL.md`

- **能做什么：** 模拟叙事状态的长篇小说和剧本工作台：人物的生活、随时间变化的世界状态、每个角色知道什么和相信什么、社会与观众状态、带独立角色推演的因果剧情模拟、连续性、改编和场景写作——草稿与正史分开保存。
- **怎么用：** 模式：DISCOVER、CHARACTER、SIMULATE、NOVEL、SCREENPLAY、ADAPT、AUDIT、REPAIR。说“续写这部小说”“规划下一段剧情”“模拟接下来会发生什么”“塑造这个角色”“小说改剧本”或“连续性检查”。
- **最适合：** 因果和人物心理都必须保持一致的长篇复杂故事。

<a id="s-story-forge-engine"></a>
### story-forge-engine

[story-forge-engine.zip](story-forge-engine.zip) · 入口：`story-forge-engine/SKILL.md`

- **能做什么：** “剧情推演引擎”：根据你提供的角色、世界规则、前文和大纲整理故事圣经，再从每个角色的目标、所知与误信、行动代价以及对手的反应推演后续。交付走向、卷章大纲、场景、小说正文或剧本，检查连续性，还能导出这部作品专属的续写技能。
- **怎么用：** 说“推演剧情”“这些人物接下来会怎么做？”“根据前文排后续大纲”“按这些设定接着写”或“导出这部作品的续写 skill”。需要已有的故事材料。
- **最适合：** 以令人信服的因果逻辑续写已有故事。

<a id="s-viral-framework-analyzer"></a>
### viral-framework-analyzer

[viral-framework-analyzer.zip](viral-framework-analyzer.zip) · 入口：`viral-framework-analyzer-v2.0.0/SKILL.md`

- **能做什么：** “爆款框架分析工厂”：接收一批短剧、AI 短剧、漫剧、解说剧或短篇内容（剧本、字幕、链接、榜单数据），自动建立样本库，逐部拆解，跨样本对比，做反事实检验，提炼出该类型可复用的爆款框架，并给出前三集、前十集和长线升级模板——同时说明哪些不能照搬、哪些结论证据不足。
- **怎么用：** 上传这批资料，说“分析这批作品”。它会根据数量自动选择单作、全量批量、分层、map-reduce 或语料库模式。见 `QUICKSTART.md`。
- **最适合：** 弄清某个类型里头部作品到底强在哪里。

<a id="s-writing-ensemble-sitcoms"></a>
### writing-ensemble-sitcoms

[writing-ensemble-sitcoms.zip](writing-ensemble-sitcoms.zip) · 入口：`sitcom-writers-room-public-v1.0/SKILL.md`

- **能做什么：** 编写、规划、修改和诊断群像情景喜剧：把情景喜剧看作承受新压力的稳定社交系统，配有剧集、单集、场景和对白四个引擎，以及鲜明的角色声音、源于关系的幽默、因果驱动的场景转折、可拍摄的动作和连续性账本。
- **怎么用：** 提供剧集设定和角色（或已有剧集），要求写一集、一场戏、打磨对白或做诊断。
- **最适合：** 对白自然、而不是舞台式抖包袱的固定班底喜剧。

<a id="s-zh-b6e6af54"></a>
### 微短剧剧本创作

[微短剧剧本创作.zip](%E5%BE%AE%E7%9F%AD%E5%89%A7%E5%89%A7%E6%9C%AC%E5%88%9B%E4%BD%9C.zip) · *提示词型* · 入口：`短剧编剧SKILL.md`

- **能做什么：** 带你从选题一直写到完整的 50–100 集微短剧：题材选择（13 种题材及出海题材）、开篇法则、付费卡点设计、节奏曲线、五大爽点类型、四层反派体系、钩子和合规清单。进度保存在项目文件夹中，下次自动恢复。
- **怎么用：** 提示词型文件 `短剧编剧SKILL.md`，使用斜杠命令：`/start`、`/plan`、`/characters`、`/outline`、`/episode {N}`、`/review {N}`、`/compliance`、`/export`。最好在能读写文件的 agent 里使用。
- **最适合：** 为短视频平台写一部完整的付费微短剧。

<a id="s-zh-a64c64af"></a>
### 故事世界模拟-v4.0.0

[故事世界模拟-v4.0.0.zip](%E6%95%85%E4%BA%8B%E4%B8%96%E7%95%8C%E6%A8%A1%E6%8B%9F-v4.0.0.zip) · 入口：`故事世界模拟-v4.0.0/SKILL.md`

- **能做什么：** “故事世界模拟 4.0”——由工具支撑的故事引擎，把事实、角色所知、角色的解释、候选未来和已接受的正史分开。SIMULATE 只提出结构化意图和候选事件（绝不直接写入正史），角色只能根据当时确实已获得的信息行动，世界规则和资源由工具检查，STEER 以一定代价改变外部条件，NOVEL/SCREENPLAY 从选定的事件路径渲染，COMMIT 之前必须先审计。
- **怎么用：** 从 README（命令说明）和 `project.json` 开始；要求分析、续写、推演、改编或审计一个故事。附带 schema、工具和测试。
- **最适合：** 严谨、不破坏正史地模拟复杂的故事世界。

<a id="cat-image"></a>
## AI 图像与摄影

图像导演、人像与时尚、角色和资产一致性、修图与修复。

| 技能 | 最适合 |
|---|---|
| [`aquamuse-swimwear-editorial-v1.0.0`](#s-aquamuse-swimwear-editorial-v1-0-0) | 泳装、度假和泳池边的时尚影像。 |
| [`asset-continuity-imagegen`](#s-asset-continuity-imagegen) | 需要保持一致性的多图项目——分镜、产品组图、角色设定图。 |
| [`character-asset-capture-kit`](#s-character-asset-capture-kit) | 把已在画面或作品中出现的角色变成后续生成可用的一致资产。 |
| [`fantasy-life-force-portrait-photography`](#s-fantasy-life-force-portrait-photography) | 让日常人像看起来像社交平台上的抓拍大片。 |
| [`fashion-shoot-twin`](#s-fashion-shoot-twin) | 借用某种摄影风格拍摄的服装电商套图。 |
| [`fidelity-4k-upscale-skill-v1.0`](#s-fidelity-4k-upscale-skill-v1-0) | 得到一份必须与原图完全一致的高清“存档版”。 |
| [`guided-image-director`](#s-guided-image-director) | 想要果断的创意方向，而不是一堆提示词选项。 |
| [`huazhao-portrait-director`](#s-huazhao-portrait-director) | 身份和服装都可控、可信且一致的人像系列。 |
| [`huazhao-portrait-engine`](#s-huazhao-portrait-engine) | 服装逻辑和真实感都很重要的汉服 / 古典美人写真。 |
| [`image-factory`](#s-image-factory) | 适用于多种题材、与模型无关的通用生图工作流。 |
| [`mj-aesthetic-lab-v2.0.0`](#s-mj-aesthetic-lab-v2-0-0) | 系统化地探索和编写 Midjourney 提示词。 |
| [`nexuswear-persona-fashion-director`](#s-nexuswear-persona-fashion-director) | 原创服装概念和角色衣橱。 |
| [`photoreal-face-asset-engine`](#s-photoreal-face-asset-engine) | 在图像和视频项目中可复用、保持一致的写实人物脸。 |
| [`pic-fix-oneshot`](#s-pic-fix-oneshot) | 修复 AI 生成的分镜图和插画而不发生漂移。 |
| [`portrait-retouch`](#s-portrait-retouch) | 让人像更好看、更有人味，但不变成另一个人。 |
| [`public-character-continuity`](#s-public-character-continuity) | 日常的“同一个角色，新的一张图”需求。 |
| [`realistic-social-selfie-retouch`](#s-realistic-social-selfie-retouch) | 自然的“还是我，但更好看”的社交平台自拍。 |
| [`style-composition-lora-forge`](#s-style-composition-lora-forge) | 当单靠提示词无法还原某种视觉风格时，用 LoRA 把它固定下来。 |
| [`threadlock-wardrobe-skill-v1.0.0`](#s-threadlock-wardrobe-skill-v1-0-0) | 让服装在不同角色、姿势和镜头之间完全一致。 |
| [`wardrobe-extractor-skill-v1.0.0`](#s-wardrobe-extractor-skill-v1-0-0) | 把参考图里的一套衣服提取成可复用的服装表。 |
| [`zhuangbi-portrait`](#s-zhuangbi-portrait) | 低调而有力量感的身份写真，而不是炫富模板图。 |
| [`刺猬星球superi的超级skill`](#s-zh-b5e804a7) | 电影感国风古装剧剧照和图生视频短片。 |
| [`古风短剧场景设计师`](#s-zh-8fa780ee) | 为古装短剧提供风格统一的场景设计参考。 |

<a id="s-aquamuse-swimwear-editorial-v1-0-0"></a>
### aquamuse-swimwear-editorial-v1.0.0

[aquamuse-swimwear-editorial-v1.0.0.zip](aquamuse-swimwear-editorial-v1.0.0.zip) · 入口：`aquamuse-swimwear-editorial-v1.0.0/SKILL.md`

- **能做什么：** 面向成人（21+）高端泳装与度假装大片的提示词规划技能，让画面像真实摄影而不是 AI 网红图。使用七层引擎（大片主题、人物、服装逻辑、身体动作、镜头几何、光线、真实感检查）、反 AI 闸门和提示词编译器，有三种模式：清爽度假、电影感海岸人像、时尚广告。
- **怎么用：** 填写一键简报（地点、造型、氛围、目标模型、可选参考图），它会返回编译好的提示词、避免清单和质检要点。
- **最适合：** 泳装、度假和泳池边的时尚影像。

<a id="s-asset-continuity-imagegen"></a>
### asset-continuity-imagegen

[asset-continuity-imagegen.zip](asset-continuity-imagegen.zip) · 入口：`asset-continuity-imagegen-v1.0.0/skills/asset-continuity-imagegen/SKILL.md`

- **能做什么：** 让反复出现的人物、道具、产品、服装、载具和地点在生成或编辑的多张图里保持可辨认的一致。建立资产登记表（不可变锚点 / 受控变量 / 自由变量），编写镜头合同，规范参考图的使用，并诊断和修复“漂移”。
- **怎么用：** 提供参考图，要求生成新镜头、变体或多资产场景，或让它修复已经漂移的图。有内置生图工具时会优先使用。
- **最适合：** 需要保持一致性的多图项目——分镜、产品组图、角色设定图。

<a id="s-character-asset-capture-kit"></a>
### character-asset-capture-kit

[character-asset-capture-kit.zip](character-asset-capture-kit.zip) · 入口：`character-asset-capture-kit-v1.0.0/SKILL.md`

- **能做什么：** 从现有图片、截图、参考图组或视频中提取可复用的人物资产，同时保留可见的身份特征、身体比例、服装、个人道具和原始画风——是提取，不是重新设计。流程：扫描 → 捕获 → 规范化 → 打包 → 复用。
- **怎么用：** 命令：`/人物提取`（提取人物档案或抠图）、`/人物资产`（建立完整资产包或资产板）、`/批量提取`（从视频批量提取）。被遮挡的部分会标为“未确认”或“补全候选”。
- **最适合：** 把已在画面或作品中出现的角色变成后续生成可用的一致资产。

<a id="s-fantasy-life-force-portrait-photography"></a>
### fantasy-life-force-portrait-photography

[fantasy-life-force-portrait-photography.zip](fantasy-life-force-portrait-photography.zip) · 入口：`fantasy-life-force-portrait-photography-main/SKILL.md`

- **能做什么：** “生命感”人像摄影工作流：把游客照、随手拍或参考人像变成色彩鲜明、镜头亲密、阳光真实、适合分享的作品，像摄影师抓拍到的真实瞬间。模式 A 严格锁定身份地升级照片，模式 C 变成氛围感大片，模式 B 生成原创样片。包含构图、面部、发丝、服装和色彩标准。
- **怎么用：** 上传照片并选择模式，或描述场景生成原创作品。参考图只用于分析，不会被重绘成别人；公众人物特征会被脱敏处理。
- **最适合：** 让日常人像看起来像社交平台上的抓拍大片。

<a id="s-fashion-shoot-twin"></a>
### fashion-shoot-twin

[fashion-shoot-twin.zip](fashion-shoot-twin.zip) · 入口：`fashion-shoot-twin/SKILL.md`

- **能做什么：** 为你的服装复刻某位摄影师的拍摄语言：根据风格参考（A 组）、服装图（B 组）以及可选的模特（C 组）和地点（D 组）参考，归纳摄影师的光线、镜头、构图、调色和组照节奏，建立服装证据图谱，规划 6–8 张新照片——像同一摄影师、同一天、在相连场景里拍的——同时更会卖衣服。可路由到 GPT Image 或 ComfyUI，按“锚定 → 覆盖 → 修复”生成，并做三层质检。
- **怎么用：** 上传 4–12 张风格参考，加上服装正面、背面、侧面和细节图。生成前只有一个确认点。
- **最适合：** 借用某种摄影风格拍摄的服装电商套图。

<a id="s-fidelity-4k-upscale-skill-v1-0"></a>
### fidelity-4k-upscale-skill-v1.0

[fidelity-4k-upscale-skill-v1.0.zip](fidelity-4k-upscale-skill-v1.0.zip) · 入口：`fidelity-4k-upscale-skill-v1.0/SKILL.md`

- **能做什么：** 纯保真的高清放大：把图片变大变清楚，但不改变任何内容——人脸、文字、Logo、商品、颜色，甚至瑕疵和水印都保持原样。如果“更清楚”会改变内容，就保留原样。
- **怎么用：** 上传图片，要求高清版 / 4K / 提高分辨率。修图、换背景、去水印或改风格不在范围内（请用修图类技能）。
- **最适合：** 得到一份必须与原图完全一致的高清“存档版”。

<a id="s-guided-image-director"></a>
### guided-image-director

[guided-image-director.zip](guided-image-director.zip) · 入口：`guided-image-director/SKILL.md`

- **能做什么：** 果断的图像导演：把模糊的意图转成一个统一的视觉决定，并用目标图像模型能执行的语言写出来。会在概念、参考图引导、商业制作（广告、海报、封面、产品）、系列图和修图之间自动选择路线；只有缺失的信息会改变核心主体时才提问。
- **怎么用：** 描述你想要什么（如有参考图一并提供）和目标模型；它会给出明确的推荐和编译好的提示词，或对现有图片做定点修复。
- **最适合：** 想要果断的创意方向，而不是一堆提示词选项。

<a id="s-huazhao-portrait-director"></a>
### huazhao-portrait-director

[huazhao-portrait-director.zip](huazhao-portrait-director.zip) · 入口：`huazhao-portrait-director-v5.0.0-public/SKILL.md` · `huazhao-portrait-director-v6.0.0-public/SKILL.md`

- **能做什么：** “华照写真导演”——面向人物写真、古风和时装人像、身份与服装参考图以及系列组图的外发版导演系统。产出结构化拍摄规格、参考图职责分配、镜头与空间逻辑、光线/材质约束、连续性账本、质检和定点返修决定；不分发底层生成文本。压缩包里有 v5.0 和 v6.0。
- **怎么用：** 直接描述人物、场景和正在发生的事（加上参考图）。除非需要 v5，否则用 v6.0（更新，增加了工具能力匹配和镜头变化表）。环境里有生图工具时会直接出图并复核；没有时交付拍摄规格。
- **最适合：** 身份和服装都可控、可信且一致的人像系列。

<a id="s-huazhao-portrait-engine"></a>
### huazhao-portrait-engine

[huazhao-portrait-engine.zip](huazhao-portrait-engine.zip) · 入口：`huazhao-portrait-engine-v1.1.0/SKILL.md`

- **能做什么：** “华照写真系统 · Vitality 1.1”——把中国风人像、汉服和国风时装的生图当作一场有导演的拍摄，分别控制人物、动作、空间、光线/材质、生命感和系列一致性。模式涵盖纯文字简报、人物参考等。
- **怎么用：** 描述想要的写真或系列，可附人物或服装参考；它会输出拍摄方案和生成提示词，也能修复或扩展已有图片。见 `QUICKSTART.md`。
- **最适合：** 服装逻辑和真实感都很重要的汉服 / 古典美人写真。

<a id="s-image-factory"></a>
### image-factory

[image-factory.zip](image-factory.zip) · 入口：`image-factory-skill-v1.0.0/SKILL.md`

- **能做什么：** 把生图需求、参考图、简报、剧情节点或产品要求转成结构化提示词、镜头计划、受控变体、质检关卡和定点修复指令。把每个任务拆成六层（意图、场景、镜头、外观、约束、质检/修复），并为电影剧照、写实人像、产品、动漫/插画、概念设计、建筑/室内和图片编辑提供领域配方。
- **怎么用：** 描述你想要的图（如有参考图一并提供）；它会返回编译好的提示词和变体，生成效果不好时告诉你该修哪一层。
- **最适合：** 适用于多种题材、与模型无关的通用生图工作流。

<a id="s-mj-aesthetic-lab-v2-0-0"></a>
### mj-aesthetic-lab-v2.0.0

[mj-aesthetic-lab-v2.0.0.zip](mj-aesthetic-lab-v2.0.0.zip) · 入口：`mj-aesthetic-lab-v2.0.0/SKILL.md`

- **能做什么：** 把 Midjourney 变成可控的视觉开发实验室（“先搜索再定型”）：美学升级、风格搜索、提示词编译、图片评析与修复、对照实验、风格 DNA 一致性和角色选角。使用九轴美学扫描、三杠杆原则、九层提示词编译器、反套路规则，以及针对当前 Midjourney 参数（截至 2026 年 8 月）的适配器。
- **怎么用：** 选择模式（A–G）或直接描述图片；适用于人像、电影剧照、时尚、产品、建筑、概念设计、插画和 Niji。见 `INSTALL.md`。
- **最适合：** 系统化地探索和编写 Midjourney 提示词。

<a id="s-nexuswear-persona-fashion-director"></a>
### nexuswear-persona-fashion-director

[nexuswear-persona-fashion-director.zip](nexuswear-persona-fashion-director.zip) · 入口：`nexuswear-persona-fashion-director/SKILL.md`

- **能做什么：** 先设计“处在情境中的人”，再设计让这个人显得可信的衣服：原创的潮流服装、T 恤、完整角色造型、穿搭、胶囊系列和画册/大片提示词，适用于男性、女性或中性穿着者，并保证服装呈现一致。
- **怎么用：** 描述穿着者、受众、场合、对潮流的接受度和限制；它会还原需求、锁定人设，并交付服装设计和画面方向。
- **最适合：** 原创服装概念和角色衣橱。

<a id="s-photoreal-face-asset-engine"></a>
### photoreal-face-asset-engine

[photoreal-face-asset-engine.zip](photoreal-face-asset-engine.zip) · 入口：`photoreal-face-asset-engine-v1.1.0/SKILL.md`

- **能做什么：** 把一张原创或经授权的写实人脸建立成可长期复用的身份资产：生成差异足够大的候选脸，锁定选中的一张为母身份并生成指纹，精确编辑参数，编译结构与真人材质合同，产出多视角资产图和完整人物资产包——带身份和真实感关卡。仅限成年人、摄影写实风格。
- **怎么用：** 按 SKILL.md 中的流程：生成候选 → `lock` 锁定一张 → 精细编辑 → 编译 → 多视角图集 → 一键资产包。脚本和 schema 都已附带。
- **最适合：** 在图像和视频项目中可复用、保持一致的写实人物脸。

<a id="s-pic-fix-oneshot"></a>
### pic-fix-oneshot

[pic-fix-oneshot.zip](pic-fix-oneshot.zip) · 入口：`pic-fix-oneshot/SKILL.md`

- **能做什么：** “改图一把过”，面向漫剧分镜、插画、海报和电商图：体检 → 多轮修复（每轮最多三项，先结构后细节）→ 每轮复检 → 修坏就回退或换方法 → 择优交付。处理透视/构图、AI 崩坏、手部、面貌漂移、道具和多分镜连贯性。
- **怎么用：** 上传图片（加上参考图），使用口令如“全修”“只体检”“只修手”“只修透视”“只修脸”“建档”“连贯检查”“继续”“退回”“换个方法”。不用于从零创作新图、视频修复或真人换脸。
- **最适合：** 修复 AI 生成的分镜图和插画而不发生漂移。

<a id="s-portrait-retouch"></a>
### portrait-retouch

[portrait-retouch.zip](portrait-retouch.zip) · 入口：`portrait-retouch-skill-v2.0.0/SKILL.md`

- **能做什么：** 用对话式图像编辑模型（GPT 类）修饰现有的 AI 或摄影人像，让人更好看、更鲜活、更可信，同时保持身份、年龄、身体结构、表情、姿势、镜头和场景不变。快速分诊缺陷，写明确的编辑合同（硬锁定与允许修改），用“真人感栈”（皮肤、眼睛、嘴唇、头发、与场景融合、镜头可信度）处理，并在不改变身份的前提下提升美感。
- **怎么用：** 上传人像，说出哪里不满意（或直接说“修一下”）。模式：直接编辑（默认）、只出提示词、无目标图。
- **最适合：** 让人像更好看、更有人味，但不变成另一个人。

<a id="s-public-character-continuity"></a>
### public-character-continuity

[public-character-continuity.zip](public-character-continuity.zip) · 入口：`public-character-continuity-skill-v1.0.0/SKILL.md`

- **能做什么：** 轻量、以参考图为主的方法，让既有角色在多次生图和编辑中保持可辨认：选出当前最好的参考，把请求拆成“保持”和“修改”两部分，写简洁的修改提示词，角色漂移时按简单的顺序恢复。
- **怎么用：** 提供参考图，要求同一个角色出现在新场景、新服装、新姿势、新表情或新角度。更重的多资产工作用 `asset-continuity-imagegen`。
- **最适合：** 日常的“同一个角色，新的一张图”需求。

<a id="s-realistic-social-selfie-retouch"></a>
### realistic-social-selfie-retouch

[realistic-social-selfie-retouch.zip](realistic-social-selfie-retouch.zip) · 入口：`realistic-social-selfie-retouch/SKILL.md`

- **能做什么：** 为一张随手自拍制作六部分的小红书/Pinterest 风格精修方案和中文 AI 修图提示词：皮肤更干净但保留真实纹理，妆容、光线和色彩更好，有社交平台的精致感——同时保持同一个人、五官比例、表情、姿势、服装、发型方向和场景。
- **怎么用：** 上传自拍，说“小红书网感精修”“Pinterest 自拍精修”“自然真实变美”等。不用于换脸、修身形、换场景、cosplay 或性感化修图。
- **最适合：** 自然的“还是我，但更好看”的社交平台自拍。

<a id="s-style-composition-lora-forge"></a>
### style-composition-lora-forge

[style-composition-lora-forge.zip](style-composition-lora-forge.zip) · 入口：`style-composition-lora-forge-v1.0.0/SKILL.md`

- **能做什么：** 构建并验证以风格为重点的 LoRA 训练项目（例如某位画家的油画），同时通过推理时独立的结构通道（在 ComfyUI 中类似 ControlNet）保持构图可控：数据集整理与审计、打标、试训、各训练后端的起始文件、验证矩阵和选出最优模型。
- **怎么用：** 准备一组风格统一的参考图和你的训练后端；从 `BOOT.md` 开始。附带 ComfyUI 工作流。
- **最适合：** 当单靠提示词无法还原某种视觉风格时，用 LoRA 把它固定下来。

<a id="s-threadlock-wardrobe-skill-v1-0-0"></a>
### threadlock-wardrobe-skill-v1.0.0

[threadlock-wardrobe-skill-v1.0.0.zip](threadlock-wardrobe-skill-v1.0.0.zip) · 入口：`threadlock-wardrobe-skill-v1.0.0/SKILL.md`

- **能做什么：** 适用于动漫和写实工作流、与模型无关的服装资产系统：一件衣服是带证据和不变量的资产，而不是一段提示词文字。模式有 EXTRACT（提取）、RECONSTRUCT（重建被遮挡部分而不随意重新设计）、DESIGN（设计）、RENDER（渲染）和 VIDEO（视频），带锁定级别、后端路由和连续性关卡。附带一个 Python 包（`threadlock`）、简单命令行、schema 和测试。
- **怎么用：** 提供服装参考图，说明需要什么——提取、重建被挡住的部分、把同一套衣服穿到另一个角色身上，或在多个镜头和视频中保持一致。命令行用法见 `README.md`。
- **最适合：** 让服装在不同角色、姿势和镜头之间完全一致。

<a id="s-wardrobe-extractor-skill-v1-0-0"></a>
### wardrobe-extractor-skill-v1.0.0

[wardrobe-extractor-skill-v1.0.0.zip](wardrobe-extractor-skill-v1.0.0.zip) · 入口：`wardrobe-extractor-skill-v1.0.0/SKILL.md`

- **能做什么：** 把含有一个或多个人物/角色的参考图变成干净的服装与配饰提取表——适用于照片、电影剧照、动漫、漫画、游戏画面、概念设计、历史服饰，甚至低清或局部图。每个细节都标注为直接可见、强烈暗示或未知，而不是编造；处理层次和遮挡，支持忠实提取或现实材质化两种模式。
- **怎么用：** 上传图片，要求“提取服装 / 服饰”。多人图会为每个人分别列出清单。
- **最适合：** 把参考图里的一套衣服提取成可复用的服装表。

<a id="s-zhuangbi-portrait"></a>
### zhuangbi-portrait

[zhuangbi-portrait.zip](zhuangbi-portrait.zip) · 入口：`zhuangbi-portrait/SKILL.md`

- **能做什么：** “装逼写真”——让一位明确成年的人物在照片里显得有位置、有权限、有影响力，却不靠炫富符号（没有豪车、钻石、香槟）。每张照片由一句令人难忘的“传闻”、恰好两项可信的“通行证”、对画外小事的“迟到反应”、刻意的留白、镜头权力关系、面部辨识度和生活痕迹构成。
- **怎么用：** 只有明确要求时才使用：`$zhuangbi-portrait`、“装逼写真”“排面写真”“有位置感”，或“我的照片看起来像租来的 / 用力过猛，重做”。信息很少也能工作；按顺序读取 `cards/`。
- **最适合：** 低调而有力量感的身份写真，而不是炫富模板图。

<a id="s-zh-b5e804a7"></a>
### 刺猬星球superi的超级skill

[刺猬星球superi的超级skill.zip](%E5%88%BA%E7%8C%AC%E6%98%9F%E7%90%83superi%E7%9A%84%E8%B6%85%E7%BA%A7skill.zip) · *提示词型* · 入口：`人物skill.md`

- **能做什么：** 创作者个人风格技能：用大白话就能生成接近该账号作品的画面——真实质感、电影感的国风古装剧画面（古装、像剧中关键剧情帧、竖屏构图），并能把生成好的古装人物图变成 5 秒剧情化的图生视频提示词。包含创作者风格卡、生图和图生视频工作流，以及针对 ChatGPT、nano banana pro、可灵和即梦的适配建议。
- **怎么用：** 提示词型：把 `人物skill.md` 粘贴到你的聊天 AI，然后用大白话描述画面，或上传生成好的古装图来获取视频提示词。
- **最适合：** 电影感国风古装剧剧照和图生视频短片。

<a id="s-zh-8fa780ee"></a>
### 古风短剧场景设计师

[古风短剧场景设计师.zip](%E5%8F%A4%E9%A3%8E%E7%9F%AD%E5%89%A7%E5%9C%BA%E6%99%AF%E8%AE%BE%E8%AE%A1%E5%B8%88.zip) · *提示词型* · 入口：`3x3场景_skill.md`

- **能做什么：** 为古风女频短剧生成影视级场景提示词：一套 3×3 九宫格，涵盖建筑外观、庭院、入口、室内全景、主位、借景关系、家具陈设、道具特写以及平面布局/鸟瞰图。通过引导式提问（场景类型、人物身份、剧情功能、朝代美学、视觉记忆点、季节与时间、整体气质、输出模式）收集需求。只生成场景图片提示词，不生成视频提示词。
- **怎么用：** 提示词型：把 `3x3场景_skill.md` 粘贴到你的聊天 AI 并回答它的问题。它设计为与人物技能（`刺猬星球superi的超级skill`）和短剧编剧技能（`微短剧剧本创作`）配合使用。
- **最适合：** 为古装短剧提供风格统一的场景设计参考。

<a id="cat-aesthetics"></a>
## 视觉风格分析与反推提示词

弄清参考图为什么好看，并把它变成可复用的提示词。

| 技能 | 最适合 |
|---|---|
| [`aesthetic-stress-extractor`](#s-aesthetic-stress-extractor) | 在用图像模型复刻之前，先真正理解并忠实还原一种电影感画面。 |
| [`cinematic-style-compiler`](#s-cinematic-style-compiler) | 在新镜头中复刻整部影片的视觉系统，而不只是一帧。 |
| [`color-dna-card-extractor`](#s-color-dna-card-extractor) | 把参考画面变成可复用的配色，用于电影美术、AI 视频、角色、场景或品牌板。 |
| [`photographic-atmosphere-reconstruction`](#s-photographic-atmosphere-reconstruction) | 在新图片上还原某种摄影调色和氛围。 |
| [`reference-rendering-reader`](#s-reference-rendering-reader) | 把一种视觉处理方式借给新主体，而不复制原图内容。 |
| [`reverse-anything`](#s-reverse-anything) | 从你欣赏的内容或网站中提炼可复用的模板。 |
| [`strong-image-reverse-prompt`](#s-strong-image-reverse-prompt) | 用于忠实复刻和受控编辑的图生提示词。 |

<a id="s-aesthetic-stress-extractor"></a>
### aesthetic-stress-extractor

[aesthetic-stress-extractor.zip](aesthetic-stress-extractor.zip) · 入口：`aesthetic-stress-extractor/SKILL.md`

- **能做什么：** 通过“压力测试”找出一帧电影画面的美感到底靠什么：每次只削弱一个视觉条件（色彩、影调范围、平衡、留白区、细节、视觉焦点），判断美感是否还在，给敏感度排序，最后输出“最小存活集”、可安全改变的清单和精简的复刻简报。附带实验脚本和表单。
- **怎么用：** 给它一帧（快速扫描）或多帧（组合运行），问这个画面的美感取决于什么，或要一份复刻提示词；也能对照参考图诊断生成结果。它不会凭一帧去猜摄影器材或整部片子的风格。
- **最适合：** 在用图像模型复刻之前，先真正理解并忠实还原一种电影感画面。

<a id="s-cinematic-style-compiler"></a>
### cinematic-style-compiler

[cinematic-style-compiler.zip](cinematic-style-compiler.zip) · 入口：`cinematic-style-compiler/SKILL.md`

- **能做什么：** 从一部电影、剧集、短剧或广告的多张静帧或片段中建立可解释的 FILM_AESTHETIC_MODEL（逐镜十轴分析、叙事阶段、镜头功能语法、锚点联动），再编译成用于新内容的 REPLICATION_SPEC，并在之后检验相似度。
- **怎么用：** 提供多帧或片段，要求“提取影视美学锚点”“分析镜头语法”或“把这部片的美学迁移到新内容”，也可以问为什么生成图只有色调像。不用于单条最终提示词、单图严格复刻或简单调色。
- **最适合：** 在新镜头中复刻整部影片的视觉系统，而不只是一帧。

<a id="s-color-dna-card-extractor"></a>
### color-dna-card-extractor

[color-dna-card-extractor.zip](color-dna-card-extractor.zip) · 入口：`COLOR-DNA-CARD-EXTRACTOR-v1.0/SKILL.md`

- **能做什么：** 从单张参考图中提取影视/设计级的功能性色彩系统——区分光色与物色、明暗层级以及小面积但关键的强调色，每种颜色都有功能名称——并编译成一条能生成专业色卡展示页的提示词。
- **怎么用：** 提供一张图；可选项目名、色卡数量（6、9 或 13 色，默认 13）、用途和标题语言。输出提取结果和可直接使用的生图提示词（默认 16:9 扁平 Figma 风格展示页）。
- **最适合：** 把参考画面变成可复用的配色，用于电影美术、AI 视频、角色、场景或品牌板。

<a id="s-photographic-atmosphere-reconstruction"></a>
### photographic-atmosphere-reconstruction

[photographic-atmosphere-reconstruction.zip](photographic-atmosphere-reconstruction.zip) · 入口：`photographic-atmosphere-reconstruction/SKILL.md`

- **能做什么：** 反推一张照片为什么看起来是那样——亮暗秩序、整体色倾向、颜色之间的关系、明暗响应、材质观感和空气感——并改写成可迁移的调色与氛围指令。可以基于单张参考、一组参考（找出稳定共有的观感）或参考图 + 目标图，并诊断“颜色差不多但感觉不像”。会保护肤色。
- **怎么用：** 提供一张或多张参考照片（迁移时再加目标图），要求提取、迁移、对比或诊断观感。说“只要提示词”可跳过分析过程。
- **最适合：** 在新图片上还原某种摄影调色和氛围。

<a id="s-reference-rendering-reader"></a>
### reference-rendering-reader

[reference-rendering-reader.zip](reference-rendering-reader.zip) · 入口：`reference-rendering-reader/SKILL.md`

- **能做什么：** 谨慎的单图风格读取器：把图里画的内容（要忽略的）和可迁移的渲染决策分开——构图、线条与边缘、明暗塑造、光影、表面、细节分布、色彩和影调关系——并返回可复用的风格提示词、风格限制提示词和可靠性说明。不猜测身份、作者或制作手法。
- **怎么用：** 上传一张参考图，说“提取画风”“分析这张图的风格”或“image to style prompt”。
- **最适合：** 把一种视觉处理方式借给新主体，而不复制原图内容。

<a id="s-reverse-anything"></a>
### reverse-anything

[reverse-anything.zip](reverse-anything.zip) · 入口：`reverse-anything/SKILL.md` · `reverse-anything__不同内容_0d88a8ba/SKILL.md`

- **能做什么：** “万能逆向”：把别人做得好的东西变成你可以复用的东西。对图片和视频，反推母版提示词（固定骨架、变量槽、风格锚点、有效参数）；对标杆网站，拆解定位、功能、流程和技术栈，给出实现方案和分步 vibe coding 提示词。每条结论都标注为证据 / 推断 / 猜测。压缩包里有 v1.0 和 v2.0（证据驱动，也覆盖产品和工作流，并做复现验证）。
- **怎么用：** 提供一组提示词、一条提示词加成品、只有成品，或一个网址（“逆向这张图的提示词”“这个网站是怎么做的？”“我想做一个像 X 的产品”）。Hermes 风格的技能；脚本在 `scripts/`。优先用 v2.0。
- **最适合：** 从你欣赏的内容或网站中提炼可复用的模板。

<a id="s-strong-image-reverse-prompt"></a>
### strong-image-reverse-prompt

[strong-image-reverse-prompt.zip](strong-image-reverse-prompt.zip) · 入口：`strong-image-reverse-prompt/SKILL.md`

- **能做什么：** 把一张或多张参考图变成清晰、可控的生成或编辑提示词——复刻构图、保留产品或人物身份而更换场景，或对比多张参考——每张图都会被分配角色（主体、风格、版式、对比）。输出快速简报或制作简报，包含视觉指纹、可用提示词、控制说明和模型适配（GPT Image、Midjourney、Flux、SDXL）。
- **怎么用：** 上传图片，说“把这张图反推成提示词”或“用我的产品复刻这个版式”。
- **最适合：** 用于忠实复刻和受控编辑的图生提示词。

<a id="cat-image3d"></a>
## 3D 与产品渲染

3D 资产外观开发和电商产品渲染。

| 技能 | 最适合 |
|---|---|
| [`3d-high-fidelity-asset-forge-skill-v2.1.0`](#s-3d-high-fidelity-asset-forge-skill-v2-1-0) | 为已有的风格化 3D 动画世界扩充新资产，并保证风格完全一致。 |
| [`ecommerce-3d-render-assistant`](#s-ecommerce-3d-render-assistant) | 手机、平板、耳机、外设、相机、充电器和可穿戴设备的产品图。 |

<a id="s-3d-high-fidelity-asset-forge-skill-v2-1-0"></a>
### 3d-high-fidelity-asset-forge-skill-v2.1.0

[3d-high-fidelity-asset-forge-skill-v2.1.0.zip](3d-high-fidelity-asset-forge-skill-v2.1.0.zip) · 入口：`3d-high-fidelity-asset-forge-skill-v2.1.0/SKILL.md`

- **能做什么：** 把参考 3D 动画（视频或关键帧）的视觉风格锁定为最高权威，再生产新的人物、场景、道具和资产板，让它们看起来像是从同一部高规格 3D 动画电影里直接延伸出来的。按阶段流水线运行（导入 → 风格权威 → 类别拆分 → 外观开发 → 提示词编译 → 风格闸门 → 质检），附带 schema、脚本和测试。
- **怎么用：** 从 `START-HERE.md` 开始。提供参考视频或关键帧，以及需要的资产清单；它会输出外观开发说明和生成提示词，并用风格闸门检查每个结果（防止滑向照片级 CG、游戏美术或“泛化 3D 卡通”）。
- **最适合：** 为已有的风格化 3D 动画世界扩充新资产，并保证风格完全一致。

<a id="s-ecommerce-3d-render-assistant"></a>
### ecommerce-3d-render-assistant

[ecommerce-3d-render-assistant.zip](ecommerce-3d-render-assistant.zip) · 入口：`ecommerce-3d-render-skill-public-v1.0.0/SKILL.md`

- **能做什么：** 针对已有 3D 模型或基础渲染图的电商产品渲染助手：优化材质、灯光、反射、棚拍背景和成片质感，同时锁定产品结构和相机。自动识别材质（阳极氧化、拉丝或抛光金属、玻璃、光学镜片、塑料、橡胶、陶瓷、织物），提供五种一键预设（商城白底、官网高级白棚、黑棚科技等）。
- **怎么用：** 提供 Blender/C4D/KeyShot 场景、白模或基础渲染图，或只给文字描述。只说“渲染高级一点”会采用合理默认值并返回可直接复制的提示词；给场景时返回材质、灯光和渲染设置。
- **最适合：** 手机、平板、耳机、外设、相机、充电器和可穿戴设备的产品图。

<a id="cat-marketing"></a>
## 广告、产品演示与幻灯片

海报、剧情广告、产品演示视频和幻灯片背景。

| 技能 | 最适合 |
|---|---|
| [`beetle-poster-director`](#s-beetle-poster-director) | 比“产品使用场景图”更出人意料的创意型广告海报。 |
| [`build-product-demo`](#s-build-product-demo) | 不拖沓地展示每项关键能力的精良软件演示视频。 |
| [`narrative-ad-engine`](#s-narrative-ad-engine) | 让观众一直看到产品出现的短视频广告。 |
| [`slides`](#s-slides) | 口播 / 出镜讲解视频的背景幻灯片。 |

<a id="s-beetle-poster-director"></a>
### beetle-poster-director

[beetle-poster-director.zip](beetle-poster-director.zip) · 入口：`beetle-poster-director-v2.6.0/SKILL.md`

- **能做什么：** “甲壳虫式海报创意导演”——把真实的产品、品牌、服务、活动或想法做成一张完整的广告海报，借鉴经典大众甲壳虫广告的思路：用画面证明观点而不是直白展示产品、自嘲式文案、把缺点反转成优点、干净的留白。会联网核实产品、建立《产品事实账本》、写创意契约并做阅读测试。没有生成最终海报图片就不算完成。
- **怎么用：** 它会先让你选 A（共创模式，每步确认）或 B（全程接管）。然后提供产品名、品牌、图片或商品链接。必须联网搜索。用自带的 `install.sh` 安装。
- **最适合：** 比“产品使用场景图”更出人意料的创意型广告海报。

<a id="s-build-product-demo"></a>
### build-product-demo

[build-product-demo.zip](build-product-demo.zip) · 入口：`spellbook-main/skills/build-product-demo/SKILL.md`

- **能做什么：** 策划、制作或诊断以真实证据为基础的产品演示视频和录屏讲解。把演示当作对产品的“可验证声明”：证据清单、功能覆盖、导演阐述、脚本、节拍计划、可重复的录制工具、节奏剪辑和最终核验。诊断模式会找出最先出问题的那一层（真实性、故事、可见的状态变化、解说同步、录制、编码）。
- **怎么用：** 要求做产品演示、发布视频、功能展示或 App 讲解，或说“去掉这个演示里的空档 / 修好解说节奏”。选择策划、制作或诊断模式。
- **最适合：** 不拖沓地展示每项关键能力的精良软件演示视频。

<a id="s-narrative-ad-engine"></a>
### narrative-ad-engine

[narrative-ad-engine.zip](narrative-ad-engine.zip) · 入口：`narrative-ad-engine-v1.1.0/SKILL.md`

- **能做什么：** 生成高留存的剧情广告：原创短剧广告、电影解说式商业植入、UGC 叙事广告和转化脚本，让“注意力 → 好奇 → 欲望 → 选择 → 商品价值 → 行动”沿同一条因果链推进。模式：CREATE（只给产品）、RECAP（解说感）、GRAFT（给现有故事加商业内容）、DIAGNOSE（诊断）、VARIANT（A/B 方向）。
- **怎么用：** 只给产品就能自动运行，也可以提供现有剧情或解说稿。新手从 `START-HERE.md` 开始。面向抖音/TikTok、Reels、Shorts、B 站和小红书。
- **最适合：** 让观众一直看到产品出现的短视频广告。

<a id="s-slides"></a>
### slides

[slides.zip](slides.zip) · 入口：`spellbook-main/skills/slides/SKILL.md`

- **能做什么：** 生成 16:9 PNG 序列的幻灯片。口播模式（默认，20–40 页）为口播视频制作极简的“一页一观点”背景，有 13 种背景主题、语义颜色强调、按内容类型（人物、教程、新闻、观点）的策略和缩略图式封面系统。演示模式（5–8 页）制作更丰富的卡片式幻灯片。
- **怎么用：** 带主题或讲稿文件路径运行，例如“为这份口播稿做幻灯片”。
- **最适合：** 口播 / 出镜讲解视频的背景幻灯片。

<a id="cat-social"></a>
## 社交媒体与创作者运营

小红书和多平台内容、选题，以及地道的中文文案。

| 技能 | 最适合 |
|---|---|
| [`creator-ops-os`](#s-creator-ops-os) | 用数据而不是猜测来规划和迭代创作者账号内容。 |
| [`topic-insight-writing`](#s-topic-insight-writing) | 不知道写什么、或者内容总是跑题的创作者。 |
| [`xiaohongshu`](#s-xiaohongshu) | 从选题到发布、带调研和配图的小红书笔记。 |
| [`xiaohongshu-netfeel-guardian`](#s-xiaohongshu-netfeel-guardian) | 让中文社交内容读起来地道，而不是翻译过来的。 |

<a id="s-creator-ops-os"></a>
### creator-ops-os

[creator-ops-os.zip](creator-ops-os.zip) · 入口：`creator-ops-os-v1.0.0/SKILL.md`

- **能做什么：** 把创作者账号当作由证据驱动的系统来运营：实时市场证据和自有账号数据 → 选题板 → 平台原生内容包 → 发布前检查 → 发布简报 → 表现诊断 → 经验记忆。小红书和抖音最强；也支持 B 站、快手、微信公众号、微博、知乎、TikTok、YouTube、Instagram 和 X。从不编造市场数据。
- **怎么用：** 选择模式（例如 QUICK_SHOT 出 3–5 个选题和一份完整内容包，MARKET_SCAN 做更大范围扫描）。提供你的赛道、可用的账号数据导出和目标平台。
- **最适合：** 用数据而不是猜测来规划和迭代创作者账号内容。

<a id="s-topic-insight-writing"></a>
### topic-insight-writing

[topic-insight-writing.zip](topic-insight-writing.zip) · 入口：`topic-insight-writing-skill-v1.0.0/SKILL.md`

- **能做什么：** 面向自媒体的精准选题：受众语境 → 真实信号 → 痛点 → 具体候选选题 → 提炼观点 → 找反例与查证 → 和你讨论并锁定选题 → 结构 → 分段写作 → 事实与表达终审。适用于视频、图文和播客；除非你要求，否则在选题确定前不会写成稿。
- **怎么用：** 说“给我选题”“我有点想法但观点讲不清”或“做一期关于 X 的视频”。它会给出 2–3 个方向真正不同的选题卡，以及一个需要你拍板的关键问题。
- **最适合：** 不知道写什么、或者内容总是跑题的创作者。

<a id="s-xiaohongshu"></a>
### xiaohongshu

[xiaohongshu.zip](xiaohongshu.zip) · 入口：`spellbook-main/skills/xiaohongshu/SKILL.md`

- **能做什么：** 端到端的小红书笔记生产：了解需求 → 竞品调研并存入本地数据库 → 8–10 个标签 → 用 HTML 样式生成 3:4（1080×1440）封面和配图并做溢出检查 → 在平台限制内写文案（标题 ≤20 字，正文 ≤1000 字）→ 发布 → 验证。每篇笔记存放在独立的 `YYYYMMDD-<slug>` 文件夹里。
- **怎么用：** 带主题或素材运行（“写一篇关于我们新功能的小红书”）。把 `.env.example` 复制成 `.env` 并安装 `requirements.txt`；发布需要配置好的发布工具。
- **最适合：** 从选题到发布、带调研和配图的小红书笔记。

<a id="s-xiaohongshu-netfeel-guardian"></a>
### xiaohongshu-netfeel-guardian

[xiaohongshu-netfeel-guardian.zip](xiaohongshu-netfeel-guardian.zip) · 入口：`spellbook-main/skills/xiaohongshu-netfeel-guardian/SKILL.md`

- **能做什么：** 修复 Claude 写中文内容时的翻译腔——句式僵硬、西式框架、长文写到一半冒出“In conclusion”式的跑偏。先强制用纯中文做内部构思，检测初稿中的英文泄露，用真实的网络语感重写，输出多个版本并做最终自检，还能生成可长期使用的守护片段。不会改动你在 CLAUDE.md / AGENTS.md 里已有的人设要求。
- **怎么用：** 说“小红书翻译腔太重”“去除 Claude 翻译腔”“公众号写着写着变英文了”，或贴一篇笔记让它改成纯中文网感。与 `xiaohongshu` 搭配效果最好。
- **最适合：** 让中文社交内容读起来地道，而不是翻译过来的。

<a id="cat-writing"></a>
## 写作、作者文风与去 AI 味

用特定作者的文风写作，并去除机器写作的痕迹。

| 技能 | 最适合 |
|---|---|
| [`author-style-continuation`](#s-author-style-continuation) | 必须读起来像原作者写的续写和同人作品。 |
| [`cat-distillation-skill`](#s-cat-distillation-skill) | 从某位创作者的作品中打造可复用的写作搭档（小说、剧本、专栏、营销文案）。 |
| [`humanizer`](#s-humanizer) | 给读起来像机器写的稿子做最后润色。 |
| [`magic-style-dna`](#s-magic-style-dna) | 以统一个人风格写长文、专栏和口播稿。 |

<a id="s-author-style-continuation"></a>
### author-style-continuation

[author-style-continuation.zip](author-style-continuation.zip) · 入口：`author-style-continuation/SKILL.md`

- **能做什么：** 从原文或聊天记录中学习作者的文风并用它续写——下一章、番外、结局、角色接话或聊天体续写。会建立文风卡、人物声音卡、剧情账本和续写计划，再用只依赖标准库的 Python 脚本提取文风指纹、对比草稿与原文并标出“AI 味”表达。
- **怎么用：** 粘贴或上传原文，说明要写什么（“按原文风格续写”“接着往下写”）。中英文都支持；安装 `jieba` 可提高中文分析精度。
- **最适合：** 必须读起来像原作者写的续写和同人作品。

<a id="s-cat-distillation-skill"></a>
### cat-distillation-skill

[cat-distillation-skill.zip](cat-distillation-skill.zip) · 入口：`cat-distillation-skill-v1.0.1-STABLE/SKILL.md`

- **能做什么：** “猫咪蒸馏”——把经授权的小说、剧本、文章、访谈、聊天和工作材料编译成一个可运行的创作协作者。它学习可追溯的“爪印原子”（作者先注意什么、怎么判断、采取什么动作、产生什么效果、何时不该用），并和弱样本及题材惯例做对照。运行模式：MAKE（创作）、REWORK（改稿）、PLAN（策划）、TALK（协作对话）。明确不宣称复制某个人。
- **怎么用：** 输入某位创作者经授权的材料，然后让它按此人的创作方式写作、改稿或策划。证据不足的地方会标出来，而不是编造。
- **最适合：** 从某位创作者的作品中打造可复用的写作搭档（小说、剧本、专栏、营销文案）。

<a id="s-humanizer"></a>
### humanizer

[humanizer.zip](humanizer.zip) · 入口：`spellbook-main/skills/humanizer/SKILL.md`

- **能做什么：** 依据维基百科的“AI 写作特征”指南去除文字中的 AI 痕迹——夸大的象征意义、推销腔、浅薄的“-ing”式分析、含糊的出处、破折号过多、三段式排比、AI 常用词、否定式排比——同时保留原意和语气。
- **怎么用：** 指定一段文字或文件，让它改得更像人写的、更自然。
- **最适合：** 给读起来像机器写的稿子做最后润色。

<a id="s-magic-style-dna"></a>
### magic-style-dna

[magic-style-dna.zip](magic-style-dna.zip) · 入口：`magic-style-dna-v1.0.0/SKILL.md`

- **能做什么：** “魔法文风 · 写作 DNA”——从作者自己的文章中学习可观察的写作规律（以“写作转移图”呈现：场景 → 写作选择 → 读者感受 → 证据），写出读起来像这位作者、但内容全新的原创文章，并配上标题、开头和封面文字。根据你的反馈迭代文风包；附离线分析脚本。拒绝冒充真实作者用于欺骗。
- **怎么用：** 把样本文章放进 `samples/`，让它建立文风包，然后给出新文章的主题和素材。说“这里不像”来继续打磨。
- **最适合：** 以统一个人风格写长文、专栏和口播稿。

<a id="cat-research"></a>
## 调研、搜索与情报

联网搜索工具、调研方法、行业和 AI 资讯情报、原理讲解。

| 技能 | 最适合 |
|---|---|
| [`ai-intel-officer`](#s-ai-intel-officer) | 用可核实的来源、不带炒作地跟进 AI 新发布。 |
| [`anysearch`](#s-anysearch) | 给没有内置联网搜索的 agent 加上搜索和网页提取能力。 |
| [`ask-opencli`](#s-ask-opencli) | 不用 API key，快速听听 Grok 或 Gemini 的第二意见。 |
| [`consulting-analysis`](#s-consulting-analysis) | 有清晰分析框架的正式市场、行业或竞品报告。 |
| [`github-trending`](#s-github-trending) | 发现真正在上升的开源项目和技术趋势。 |
| [`industry-intelligence-engine`](#s-industry-intelligence-engine) | 在做商业决策前快速搞懂一个陌生行业。 |
| [`multi-ai-research`](#s-multi-ai-research) | 独立来源的一致结论比单个深度回答更重要的深度调研。 |
| [`research-guide`](#s-research-guide) | 严谨、引用充分的调研。 |
| [`research-hub`](#s-research-hub) | 在装齐全套调研技能时，作为所有调研请求的统一入口。 |
| [`universal-research-architect`](#s-universal-research-architect) | 想要方法、而不只是一堆链接的任何调研问题。 |
| [`universal-web-harvester`](#s-universal-web-harvester) | 可靠地从网站（包括动态网站）采集内容。 |
| [`xray`](#s-xray) | 为自己或团队制作有证据支撑的复杂系统讲解。 |

<a id="s-ai-intel-officer"></a>
### ai-intel-officer

[ai-intel-officer.zip](ai-intel-officer.zip) · 入口：`ai-intel-officer-v1.0.0/SKILL.md`

- **能做什么：** 高信噪比的 AI 资讯与情报，以一手来源（发布说明、论文、代码仓库、价格页）为准而不是网红，严格不用 X/Twitter。会核实说法、去重并排序。模式：每日简报、每周雷达、核查台、开源侦察、价格与配额监控。
- **怎么用：** 说“给我今天的 AI 简报”“agent 工具的每周雷达”“核实一下关于某模型的传闻”或“追踪 API 价格和下线通知”。需要联网。
- **最适合：** 用可核实的来源、不带炒作地跟进 AI 新发布。

<a id="s-anysearch"></a>
### anysearch

[anysearch.zip](anysearch.zip) · 入口：`大调查/anysearch.md`

- **能做什么：** 通过 AnySearch 服务进行实时搜索——网页搜索、垂直领域搜索、并行批量搜索和网页转 Markdown 提取——使用自带的跨平台命令行工具（无需 MCP 服务器）。这个包（`大调查`）还同时带有 `consulting-analysis`、`research-guide` 和 `research-hub` 的配套文件。
- **怎么用：** 安装该文件夹后，agent 需要实时信息时会自动调用命令行工具。可选的 `ANYSEARCH_API_KEY`（写在 `.env` 或环境变量里）可提高频率上限，不填也能匿名使用。接口不清楚时运行命令行的 `doc` 命令。
- **最适合：** 给没有内置联网搜索的 agent 加上搜索和网页提取能力。

<a id="s-ask-opencli"></a>
### ask-opencli

[ask-opencli.zip](ask-opencli.zip) · 入口：`spellbook-main/skills/ask-opencli/SKILL.md`

- **能做什么：** 通过 `opencli` 驱动你已登录的 Chrome 去问 Grok 或 Gemini——不花 API 费用。
- **怎么用：** 准备：`npm install -g @jackwener/opencli`（Node ≥20），运行 `opencli doctor` 安装 Chrome 桥接扩展，在 grok.com 和 gemini.google.com 各登录一次，并设置 `OPENCLI_BROWSER_COMMAND_TIMEOUT=300`。然后说“问 grok ……”/“ask gemini ……”。多模型调研请用 `multi-ai-research`。
- **最适合：** 不用 API key，快速听听 Grok 或 Gemini 的第二意见。

<a id="s-consulting-analysis"></a>
### consulting-analysis

[consulting-analysis.zip](consulting-analysis.zip) · 入口：`大调查/consulting-analysis.md`

- **能做什么：** 生成 Markdown 格式的咨询级研究报告——市场、消费者、品牌、财务、行业、竞争情报、投资尽调。第一阶段设计分析框架（模型、章节骨架、每章数据需求、图表规划）；收集数据后，第二阶段写出带结构化叙述、内嵌图表和战略洞察的最终报告。有严格的数据真实性规则。
- **怎么用：** 要求就某个主题写研究报告。两个阶段之间搭配搜索/采集类技能（`anysearch`、`research-hub`）。它和 `anysearch` 在同一个 `大调查` 包里；入口是 `大调查/consulting-analysis.md`。
- **最适合：** 有清晰分析框架的正式市场、行业或竞品报告。

<a id="s-github-trending"></a>
### github-trending

[github-trending.zip](github-trending.zip) · 入口：`spellbook-main/skills/github-trending/SKILL.md`

- **能做什么：** GitHub Trending 探索与分析，把这个榜单当作被炒作污染的数据来看待：用脚本获取结构化数据（绝不直接抓原始 HTML），筛选真实的 star 增长，并为每个入选项目写出真正的看点。按语言或主题生成日报/周报。
- **怎么用：** 问“今天 GitHub 什么火了？”“本周热门 Rust 项目”或“AI/agent 方向的 trending 报告”。先安装 `requirements.txt` 里的脚本依赖。把结果改写成帖子或深度调研属于其他技能。
- **最适合：** 发现真正在上升的开源项目和技术趋势。

<a id="s-industry-intelligence-engine"></a>
### industry-intelligence-engine

[industry-intelligence-engine.zip](industry-intelligence-engine.zip) · 入口：`industry-intelligence-engine/SKILL.md`

- **能做什么：** 只需一个行业名（“宠物殡葬”“工业机器人”“短剧行业到底怎么赚钱？”），就能建立一个有证据支撑的行业运作模型：谁付钱给谁、利润和话语权在哪里、需求由什么驱动、现在正在发生什么变化、摩擦和机会在哪里，以及入局打法——并用反面证据检验。
- **怎么用：** 说出行业名和你要做的决定（了解、入局、投资、合作）。需要联网调研；输出结构化的行业真实模型和建议。
- **最适合：** 在做商业决策前快速搞懂一个陌生行业。

<a id="s-multi-ai-research"></a>
### multi-ai-research

[multi-ai-research.zip](multi-ai-research.zip) · 入口：`spellbook-main/skills/multi-ai-research/SKILL.md`

- **能做什么：** 并行多 AI 交叉验证调研：拆解问题，同时派出多个内部子 agent 加上 Grok 和 Gemini（通过 opencli），交叉验证答案，按置信度分级（强共识 / 部分共识 / 冲突 / 证据不足），并生成带仲裁的分级行动清单。
- **怎么用：** 说“多 AI 调研……”“交叉验证一下”或“三脑调研”。需要按 `ask-opencli` 的说明配置好 opencli。不适合简单事实或代码推理。
- **最适合：** 独立来源的一致结论比单个深度回答更重要的深度调研。

<a id="s-research-guide"></a>
### research-guide

[research-guide.zip](research-guide.zip) · 入口：`大调查/research-guide.md`

- **能做什么：** 调研“总指挥”：给意图分类（求事实、对比、趋势、系统建模、探索），设定深度（L1–L3），执行信源层级、迭代证据循环、冲突处理、交叉验证和引用规范，并把交付物（报告、竞品分析）路由给子技能。
- **怎么用：** 搜索、查事实、对比和基于证据的交付任务时自动激活。和 `anysearch`、`consulting-analysis`、`research-hub` 同属 `大调查` 包；入口是 `大调查/research-guide.md`。
- **最适合：** 严谨、引用充分的调研。

<a id="s-research-hub"></a>
### research-hub

[research-hub.zip](research-hub.zip) · 入口：`大调查/research-hub.md`

- **能做什么：** 统一的搜索研究入口，只负责路由：为意图打分，把请求交给 `anysearch`、`research-guide`、`consulting-analysis` 或视频下载 / 书籍导入 / 知识库检索 / 知识库导入等子技能，选择快查、半正式或深研通道，并带置信度标签和引用规则。
- **怎么用：** 说“搜索 / 查找 / 调研 / 分析 / 写报告 / 下载这个视频 / 导入这本书”。它引用的几个子技能（video-download、book-ingest、knowledge-*）不在本仓库中。入口是 `大调查/research-hub.md`。
- **最适合：** 在装齐全套调研技能时，作为所有调研请求的统一入口。

<a id="s-universal-research-architect"></a>
### universal-research-architect

[universal-research-architect.zip](universal-research-architect.zip) · 入口：`universal-research-architect/SKILL.md`

- **能做什么：** 把一句话问题变成站得住脚的调研过程和交付物——调研报告、问卷或访谈设计、市场或行业分析、装修或项目调研、产品/供应商对比、文献综述、事实核查。先选方法再找答案，设定深度（快速 / 标准 / 深入），追踪证据状态，并在合适的时候停止。
- **怎么用：** 用大白话提问（“帮我研究一下全屋装修，预算 15 万”“帮我做一份食堂满意度问卷”“网上这个说法是真的吗？”）。新手可以从 `START-HERE.md` 开始。
- **最适合：** 想要方法、而不只是一堆链接的任何调研问题。

<a id="s-universal-web-harvester"></a>
### universal-web-harvester

[universal-web-harvester.zip](universal-web-harvester.zip) · 入口：`universal-web-harvester-v2.1.0-PURE/SKILL.md`

- **能做什么：** 面向 Codex 的自适应网站采集：抓取、爬取、下载、归档并结构化公开页面、重 JavaScript 网站、分页列表和文件中的内容，也包括你有权登录的网站。先探测，选最省事又能拿到内容的路线，必要时才升级到浏览器，处理媒体、图库和样式表，报告前先核验输出。
- **怎么用：** 说“抓取 / 归档 / 下载这个网站的全部内容”，并提供网址和你要的内容。按需安装核心、浏览器和归档依赖（见 `INSTALL.md`）；会遵守访问边界。
- **最适合：** 可靠地从网站（包括动态网站）采集内容。

<a id="s-xray"></a>
### xray

[xray.zip](xray.zip) · 入口：`spellbook-main/skills/xray/SKILL.md`

- **能做什么：** 调查某个东西实际上是怎么运作的——概念、代码路径、应用、网络流程、系统、事故、文档或本地文件——然后交付一份两层深度的可视化 HTML 讲解：先是极简的全局图景，背后是有来源支撑的技术细节。先调查后讲解；页面是经过验证的理解的呈现。对你有权分析的应用做安全的只读静态检查。
- **怎么用：** 调用 `$xray`，或问“X 底层是怎么工作的？”“追踪这个请求在各服务之间的流转并讲清楚”。不用于一句话定义或完整代码审计。
- **最适合：** 为自己或团队制作有证据支撑的复杂系统讲解。

<a id="cat-product"></a>
## 想法、产品管理与策略

头脑风暴、想法压力测试、PRD、产品发现、数据分析和思维框架。

| 技能 | 最适合 |
|---|---|
| [`brainstorming`](#s-brainstorming) | 通过对话把粗糙的想法变成清晰的设计。 |
| [`elon-musk-perspective`](#s-elon-musk-perspective) | 成本拆解、挑战行业默认假设、制定激进但可迭代的计划。 |
| [`idea-analogist`](#s-idea-analogist) | 从其他领域为一个想法找新角度。 |
| [`idea-devils-advocate`](#s-idea-devils-advocate) | 在投入之前给想法做压力测试。 |
| [`idea-research`](#s-idea-research) | 为一个想法打下事实基础。 |
| [`idea-team`](#s-idea-team) | 在下决定之前，快速从多个角度审视一个想法。 |
| [`idea-to-product`](#s-idea-to-product) | 把原始想法变成范围清楚、用户友好的 MVP 定义。 |
| [`infinite-canvas-function-architect`](#s-infinite-canvas-function-architect) | 理清庞杂的功能集，看清还缺什么。 |
| [`prd-master`](#s-prd-master) | 清晰、可衡量的产品需求文档。 |
| [`product-analytics`](#s-product-analytics) | 正确地搭建产品指标和实验。 |
| [`product-discovery`](#s-product-discovery) | 在动手做之前判断什么值得做。 |
| [`product-manager-toolkit`](#s-product-manager-toolkit) | 需要小脚本辅助的实操型产品工作。 |
| [`creative-ideation（网页脑洞）`](#s-zh-f33b17b8) | 在普通聊天窗口里跳出套路，为故事、设定、产品或活动想点子。 |

<a id="s-brainstorming"></a>
### brainstorming

[brainstorming.zip](brainstorming.zip) · 入口：`spellbook-main/skills/brainstorming.SKILL.md`

- **能做什么：** 苏格拉底式的设计打磨（来自 obra/superpowers）：一次只问一个问题来理解想法，给出 2–3 种方案并推荐一种，然后分步呈现设计，同时砍掉不需要的东西（YAGNI 原则）。
- **怎么用：** 在写代码之前说“我们来头脑风暴一下 X”“帮我设计这个功能”或“和我一起想想架构”。不适合实现方式显而易见的机械任务。入口文件是 spellbook 包里的 `skills/brainstorming.SKILL.md`。
- **最适合：** 通过对话把粗糙的想法变成清晰的设计。

<a id="s-elon-musk-perspective"></a>
### elon-musk-perspective

[elon-musk-perspective.zip](elon-musk-perspective.zip) · 入口：`elon-musk-skill/SKILL.md`

- **能做什么：** 马斯克的“思维操作系统”，提炼自传记、播客、推文、法庭证词和批评者的资料：五个心智模型（渐近极限、五步算法、存在主义锚定、垂直整合即物理、快速迭代）、八条决策启发式和他的表达风格。一次免责声明后以第一人称回答。
- **怎么用：** 说“用马斯克的视角”“马斯克会怎么看”“从第一性原理算算这个成本”或“白痴指数”。说“退出”离开角色。不擅长政治、需要共情的问题和时间预估。
- **最适合：** 成本拆解、挑战行业默认假设、制定激进但可迭代的计划。

<a id="s-idea-analogist"></a>
### idea-analogist

[idea-analogist.zip](idea-analogist.zip) · 入口：`spellbook-main/skills/idea-analogist/SKILL.md` · `spellbook-main/plugins/idea-coach/skills/idea-analogist/SKILL.md`

- **能做什么：** 想法群聊室里的“类比者”角色：只做跨界类比和 yes-and 扩展——不评判、不挑刺、不要求证据。由 `idea-team` 调用，也可单独使用。
- **怎么用：** 说“类比一下”“别的行业有没有这样做的？”“yes-and 扩展这个想法”或“跨界启示”。单独使用时返回 5–7 个跨界类比。
- **最适合：** 从其他领域为一个想法找新角度。

<a id="s-idea-devils-advocate"></a>
### idea-devils-advocate

[idea-devils-advocate.zip](idea-devils-advocate.zip) · 入口：`spellbook-main/skills/idea-devils-advocate/SKILL.md` · `spellbook-main/plugins/idea-coach/skills/idea-devils-advocate/SKILL.md`

- **能做什么：** 想法群聊室里的“反方”角色：找漏洞、隐藏假设和反例（包括历史上的失败案例），不软化，但也不全盘否定。
- **怎么用：** 说“给我反方意见”“这个想法为什么会失败？”“找漏洞”。单独使用时返回 5–8 个挑刺点和三个你必须答得上来的问题。
- **最适合：** 在投入之前给想法做压力测试。

<a id="s-idea-research"></a>
### idea-research

[idea-research.zip](idea-research.zip) · 入口：`spellbook-main/skills/idea-research/SKILL.md` · `spellbook-main/plugins/idea-coach/skills/idea-research/SKILL.md`

- **能做什么：** 想法群聊室里的“调研员”角色：联网获取当前的事实、竞品和数据并注明来源，明确列出搜不到的内容，从不评判或给建议。
- **怎么用：** 说“调研一下 X”“X 的现状 / 竞品 / 数据是什么？”。需要联网搜索。
- **最适合：** 为一个想法打下事实基础。

<a id="s-idea-team"></a>
### idea-team

[idea-team.zip](idea-team.zip) · 入口：`spellbook-main/skills/idea-team/SKILL.md` · `spellbook-main/plugins/idea-coach/skills/idea-team/SKILL.md`

- **能做什么：** 想法群聊室的主持人：把一句话想法交给三人小组（调研员、反方、类比者），他们按回合发言、互相 @，你可以随时插话。最后产出 `team-report.md`，包含事实、漏洞、类比和你可能漏掉的角度。它是扩展想法的工具，不打分也不否决。
- **怎么用：** 说“组个团队聊一下 X”“群聊一下 X”，或作为插件安装时运行 `/idea-coach:idea-team <想法>`。如果已经决定要做、需要 PRD，用 `idea-to-product`。
- **最适合：** 在下决定之前，快速从多个角度审视一个想法。

<a id="s-idea-to-product"></a>
### idea-to-product

[idea-to-product.zip](idea-to-product.zip) · 入口：`spellbook-main/skills/idea-to-product/SKILL.md` · `spellbook-main/plugins/idea-coach/skills/idea-to-product/SKILL.md`

- **能做什么：** 端到端产品教练，带你把一句话想法经过七个阶段做成 PRD 和可点击的 HTML 原型。会故意顶嘴、强制砍功能，并用 Nielsen + Norman 原则做可用性检查。会保存进度，可以恢复、列出和导出项目。
- **怎么用：** 说“我有一个想法……”“做个 MVP”“写 PRD”，或作为插件安装时运行 `/idea-coach:idea <想法>`（以及 `resume`、`list`、`export <slug>`）。不适合已经有 PRD 在跑的团队，也不适合纯头脑风暴。
- **最适合：** 把原始想法变成范围清楚、用户友好的 MVP 定义。

<a id="s-infinite-canvas-function-architect"></a>
### infinite-canvas-function-architect

[infinite-canvas-function-architect.zip](infinite-canvas-function-architect.zip) · 入口：`infinite-canvas-function-architect-v1.1.0/SKILL.md`

- **能做什么：** 把杂乱的产品笔记、功能清单或工作流整理成结构化、可编辑的无限画布，展示目标、模块、功能、流程、数据、集成、约束、风险、依赖、缺口和优先级。先建立规范的图模型，诊断问题（孤立功能、目标缺口、缺少验收标准、隐藏前置条件、循环依赖），再渲染成可移植的单文件画布或 React Flow 应用。
- **怎么用：** 粘贴笔记或功能清单，要求“整理成画布 / 系统地图”。选择渲染方式（便携画布、React Flow 应用、白板优先）。
- **最适合：** 理清庞杂的功能集，看清还缺什么。

<a id="s-prd-master"></a>
### prd-master

[prd-master.zip](prd-master.zip) · 入口：`spellbook-main/skills/prd-master/SKILL.md`

- **能做什么：** PRD 与产品定义指南：先讲问题的结构、量化目标（不允许含糊指标）、符合 INVEST 的用户故事、验收标准、RICE/MoSCoW 优先级，以及完整 PRD 模板（摘要、背景、目标、用户画像、故事、需求、不做什么、设计、技术考虑、发布计划、风险）。
- **怎么用：** 写 PRD、用户故事或验收标准，或给功能排优先级时触发。
- **最适合：** 清晰、可衡量的产品需求文档。

<a id="s-product-analytics"></a>
### product-analytics

[product-analytics.zip](product-analytics.zip) · 入口：`spellbook-main/skills/product-analytics/SKILL.md`

- **能做什么：** 产品分析与增长：北极星指标、AARRR 漏斗、埋点设计（object_action 命名、不含个人隐私信息）、同期群和留存分析、统计严谨的 A/B 测试，以及模板。
- **怎么用：** 设计埋点、定义指标或看板、规划实验或分析留存时触发。
- **最适合：** 正确地搭建产品指标和实验。

<a id="s-product-discovery"></a>
### product-discovery

[product-discovery.zip](product-discovery.zip) · 入口：`spellbook-main/skills/product-discovery/SKILL.md`

- **能做什么：** 产品发现与市场调研：持续发现习惯、Jobs-to-be-Done、Kano 模型、价值主张画布、Cagan 的十个机会评估问题、用户访谈、假设验证和机会地图。硬性规则：先问题后方案、基于证据决策、假设必须可证伪。
- **怎么用：** 验证想法、规划访谈、评估机会或做竞品分析时触发。
- **最适合：** 在动手做之前判断什么值得做。

<a id="s-product-manager-toolkit"></a>
### product-manager-toolkit

[product-manager-toolkit.zip](product-manager-toolkit.zip) · 入口：`spellbook-main/skills/product-manager-toolkit/SKILL.md`

- **能做什么：** 带脚本的产品经理工具箱：`rice_prioritizer.py` 用 RICE（含团队容量）给功能 CSV 打分，`customer_interview_analyzer.py` 分析访谈记录，另有 PRD 模板、发现框架（机会-方案树、假设模板）和上市策略指导。
- **怎么用：** 要求做功能优先级排序（提供含 name、reach、impact、confidence、effort 的 CSV）、访谈分析或按模板写 PRD。
- **最适合：** 需要小脚本辅助的实操型产品工作。

<a id="s-zh-f33b17b8"></a>
### creative-ideation（网页脑洞）

[creative-ideation（网页脑洞）.zip](creative-ideation%EF%BC%88%E7%BD%91%E9%A1%B5%E8%84%91%E6%B4%9E%EF%BC%89.zip) · *提示词型* · 入口：`网页脑洞Skill-.md`

- **能做什么：** “网页脑洞”——Hermes `creative-ideation` 技能的网页聊天独立版：一个按场景路由的创意方法库，配有“反套路”规则（否掉前三个想法、强制具体、怪异预算、使用真实专有名词）。根据你所处阶段和领域选择方法，产出具体、不泛泛的点子。
- **怎么用：** 不是 SKILL.md 技能：把 `网页脑洞Skill-.md` 作为系统提示词、自定义指令或第一条消息粘贴到任意网页 AI，然后给出你的题材、设定、人物或剧情需求。
- **最适合：** 在普通聊天窗口里跳出套路，为故事、设定、产品或活动想点子。

<a id="cat-frontend"></a>
## 前端、UI 与设计系统

网页和移动端 UI 设计、设计系统、Figma 转代码、React 和 UX 评审。

| 技能 | 最适合 |
|---|---|
| [`app-ui-design`](#s-app-ui-design) | 有原生质感、无障碍友好的移动应用界面。 |
| [`css-debug`](#s-css-debug) | “这个元素为什么被裁掉 / 位置不对 / 看不见？”这类问题。 |
| [`figma-to-code`](#s-figma-to-code) | 用 Tailwind 忠实地把 Figma 设计实现为 React/Next.js。 |
| [`figma-to-react`](#s-figma-to-react) | 同 `figma-to-code`——按你的环境选一个名字即可。 |
| [`frontend-art-director`](#s-frontend-art-director) | 既要有作者感、不像模板，又要经得起生产环境考验的高要求网页 UI。 |
| [`frontend-design`](#s-frontend-design) | 视觉风格鲜明、有意图的网页和组件。 |
| [`personal-profile-mini-program-builder`](#s-personal-profile-mini-program-builder) | 在微信里做一个精致的个人主页或作品集。 |
| [`product-ux-expert`](#s-product-ux-expert) | 结构化的 UX 评审和无障碍检查。 |
| [`react-best-practices`](#s-react-best-practices) | React/Next.js 应用的性能评审。 |
| [`react-hooks-best-practices`](#s-react-hooks-best-practices) | 避免 React 中与 Effect 相关的 bug 和不必要的重渲染。 |
| [`ui-design-system`](#s-ui-design-system) | 从一个品牌色快速生成设计 token。 |
| [`ui-designer`](#s-ui-designer) | 做一个外观与参考设计一致的 MVP。 |
| [`ui-ux-pro-max`](#s-ui-ux-pro-max) | 任何技术栈都能参考的全面 UI/UX 指南。 |
| [`web-artifacts-builder`](#s-web-artifacts-builder) | 内容丰富、像应用一样的 claude.ai artifact。 |
| [`web-asset-generator`](#s-web-asset-generator) | 补齐网站的图标和社交预览素材。 |

<a id="s-app-ui-design"></a>
### app-ui-design

[app-ui-design.zip](app-ui-design.zip) · 入口：`spellbook-main/skills/app-ui-design/SKILL.md` · `spellbook-main/plugins/spellbook-ui/skills/app-ui-design/SKILL.md`

- **能做什么：** iOS 和 Android 移动应用 UI 设计：Material Design 3 与苹果 HIG、颜色 token、字体层级、8 点间距网格、触控区域、深色模式和无障碍。压缩包里有两份相同的副本（核心版和 `spellbook-ui` 插件版）。
- **怎么用：** 让它设计或评审 App 页面、搭建移动端设计系统，或检查无障碍和平台规范。
- **最适合：** 有原生质感、无障碍友好的移动应用界面。

<a id="s-css-debug"></a>
### css-debug

[css-debug.zip](css-debug.zip) · 入口：`spellbook-main/skills/css-debug/SKILL.md`

- **能做什么：** 诊断 CSS 和前端布局问题：定位、溢出裁剪、Tailwind 类不生效、z-index 层叠、Flexbox/Grid 问题以及 React 组件不渲染或不显示。给出诊断结论、背后的 CSS 机制和修复方法。
- **怎么用：** 调用 `/css-debug` 或描述问题；提供 HTML 结构、该元素及父元素的 computed styles，最好附截图。
- **最适合：** “这个元素为什么被裁掉 / 位置不对 / 看不见？”这类问题。

<a id="s-figma-to-code"></a>
### figma-to-code

[figma-to-code.zip](figma-to-code.zip) · 入口：`spellbook-main/skills/figma-to-code/SKILL.md`

- **能做什么：** 通过 Figma MCP 提取 Figma 设计，生成可上线的 React/Next.js 组件（TypeScript + Tailwind CSS），像素级还原。严格规则：绝不截断 MCP 输出、展平 `absolute contents` 容器、从元数据取尺寸、映射字体、内联 SVG。
- **怎么用：** 提供 Figma 链接或画框，要求转成代码。需要已连接 Figma MCP 服务器。
- **最适合：** 用 Tailwind 忠实地把 Figma 设计实现为 React/Next.js。

<a id="s-figma-to-react"></a>
### figma-to-react

[figma-to-react.zip](figma-to-react.zip) · 入口：`spellbook-main/skills/figma-to-react/SKILL.md` · `spellbook-main/plugins/spellbook-ui/skills/figma-to-react/SKILL.md`

- **能做什么：** 与 `figma-to-code` 相同的 Figma 转 React/Next.js 生成器（TypeScript + Tailwind，完整使用 Figma MCP 输出，展平 `absolute contents`，按元数据取尺寸，内联 SVG），只是用了 `spellbook-ui` 插件里的名字。压缩包里有核心版和插件版两份。
- **怎么用：** 提供 Figma 链接，要求生成 React/Next.js 组件；需要 Figma MCP 服务器。`figma-to-code` 和 `figma-to-react` 只装一个，避免重复触发。
- **最适合：** 同 `figma-to-code`——按你的环境选一个名字即可。

<a id="s-frontend-art-director"></a>
### frontend-art-director

[frontend-art-director.zip](frontend-art-director.zip) · 入口：`frontend-art-director/SKILL.md`

- **能做什么：** 全方位的前端艺术指导、UX、设计系统维护、视觉质检和生产加固。推断需求、写变更合同，用“七把锁”构建统一的视觉世界，处理边缘状态，然后运行严格的预检、确定性检测器（`detector_rules.json`）、浏览器验证和最终关卡。附带区块库和反模板规则。
- **怎么用：** 可用 `[command] [target]` 调用（标准和扩展命令见 SKILL.md），或直接要求新网站、仪表盘、改版、提取设计系统、视觉审计、深色模式或响应式适配。
- **最适合：** 既要有作者感、不像模板，又要经得起生产环境考验的高要求网页 UI。

<a id="s-frontend-design"></a>
### frontend-design

[frontend-design.zip](frontend-design.zip) · 入口：`spellbook-main/skills/frontend-design/SKILL.md` · `spellbook-main/plugins/spellbook-ui/skills/frontend-design/SKILL.md`

- **能做什么：** 构建有辨识度、可上线的网页界面，避免千篇一律的“AI 味”审美——大胆的设计思考、字体、颜色、动效和构图，并实现为真正可运行的代码。只适用于浏览器渲染的网页 UI（不适用于原生、GPU、游戏或终端界面）。压缩包里有核心版和 `spellbook-ui` 版。
- **怎么用：** 明确要求构建或大幅重新设计网页组件、页面或应用；说明用途、受众和约束。
- **最适合：** 视觉风格鲜明、有意图的网页和组件。

<a id="s-personal-profile-mini-program-builder"></a>
### personal-profile-mini-program-builder

[personal-profile-mini-program-builder.zip](personal-profile-mini-program-builder.zip) · 入口：`personal-profile-mini-program-builder/SKILL.md`

- **能做什么：** 把零散的个人资料（旧简历、聊天记录、项目清单）变成原生微信小程序——个人主页、简历、作品集、创作者名片或定向介绍——使用单一资料源、隐私投影、专业的信息层级和视觉系统。绝不编造公司、学历、数字或奖项。
- **怎么用：** 提供你的资料以及受众/用途。它会整理出 `profile.json`，运行 `scripts/compile_profile.py`，再生成可直接导入微信开发者工具的 WXML/WXSS/JS。也能扩展、修复或评审已有小程序。
- **最适合：** 在微信里做一个精致的个人主页或作品集。

<a id="s-product-ux-expert"></a>
### product-ux-expert

[product-ux-expert.zip](product-ux-expert.zip) · 入口：`spellbook-main/skills/product-ux-expert/SKILL.md`

- **能做什么：** UX 评审与交互设计：Nielsen 十大启发式原则及严重程度评级、认知负荷和关键 UX 定律、格式塔原则、用户旅程地图、WCAG 2.2 AA 无障碍检查、微交互和动效设计。
- **怎么用：** 要求对某个页面或流程做启发式评估、UX 评审、旅程地图或无障碍审计。
- **最适合：** 结构化的 UX 评审和无障碍检查。

<a id="s-react-best-practices"></a>
### react-best-practices

[react-best-practices.zip](react-best-practices.zip) · 入口：`spellbook-main/skills/react-best-practices/SKILL.md`

- **能做什么：** 提炼自 Vercel 工程团队指南的 React 和 Next.js 性能手册，按优先级：消除数据请求瀑布、控制包体积、优先服务端处理、控制重渲染、优化渲染路径、清理 JS 热点。附评审清单。
- **怎么用：** 构建、评审或重构 React/Next.js 代码以优化性能时触发。
- **最适合：** React/Next.js 应用的性能评审。

<a id="s-react-hooks-best-practices"></a>
### react-hooks-best-practices

[react-hooks-best-practices.zip](react-hooks-best-practices.zip) · 入口：`spellbook-main/skills/react-hooks-best-practices/SKILL.md`

- **能做什么：** React Hooks 与组件模式：Effect 只是“逃生舱”（派生状态、`useMemo`、用 key 重置、用事件处理代替 Effect），正确处理依赖（不要关掉 lint、使用更新函数、`useEffectEvent`），清理与请求竞态，以及 ref 和 `useImperativeHandle`。
- **怎么用：** 阅读或编写使用 Hook 或 Effect 的 React 组件时触发。它要求搭配一个 `typescript-best-practices` 技能，但本仓库里没有。
- **最适合：** 避免 React 中与 Effect 相关的 bug 和不必要的重渲染。

<a id="s-ui-design-system"></a>
### ui-design-system

[ui-design-system.zip](ui-design-system.zip) · 入口：`spellbook-main/skills/ui-design-system/SKILL.md` · `spellbook-main/plugins/spellbook-ui/skills/ui-design-system/SKILL.md`

- **能做什么：** 设计系统工具箱：`design_token_generator.py` 从品牌色生成调色板、模块化字号层级、8 点间距网格、阴影、动画和响应式 token（modern / classic / playful 三种风格；输出 JSON、CSS 或 SCSS），另有组件架构、无障碍和开发交接文档。压缩包里有核心版和 `spellbook-ui` 版。
- **怎么用：** 运行 `python scripts/design_token_generator.py <品牌色> <风格> <格式>`，或要求创建或维护设计系统。
- **最适合：** 从一个品牌色快速生成设计 token。

<a id="s-ui-designer"></a>
### ui-designer

[ui-designer.zip](ui-designer.zip) · 入口：`spellbook-main/skills/ui-designer/SKILL.md`

- **能做什么：** 从参考 UI 截图或设计稿中提取设计系统（配色、字体、间距、组件），需要时生成 MVP 的 PRD，并组合成可直接实现的 UI 提示词，之后还能用 React 把界面做出来。
- **怎么用：** 提供一个参考图文件夹并描述应用；它会依次完成提取 → PRD → 最终提示词 → 实现，使用 `assets/` 里的模板。
- **最适合：** 做一个外观与参考设计一致的 MVP。

<a id="s-ui-ux-pro-max"></a>
### ui-ux-pro-max

[ui-ux-pro-max.zip](ui-ux-pro-max.zip) · 入口：`spellbook-main/skills/ui-ux-pro-max/SKILL.md`

- **能做什么：** 高标准的 UI/UX 指导，覆盖产品模式、落地页、仪表盘、图表选择、视觉风格、配色、字体与字体搭配、UX 规则以及九种技术栈（React、Next.js、Vue、Svelte、SwiftUI、React Native、Flutter、Tailwind、shadcn/ui），还能生成设计系统和做交付前评审。
- **怎么用：** 几乎所有 UI 工作都会触发——规划、构建、评审或修复页面和组件；细节见 `references/full-guide.md`。
- **最适合：** 任何技术栈都能参考的全面 UI/UX 指南。

<a id="s-web-artifacts-builder"></a>
### web-artifacts-builder

[web-artifacts-builder.zip](web-artifacts-builder.zip) · 入口：`spellbook-main/skills/web-artifacts-builder/SKILL.md`

- **能做什么：** 用 React 18、TypeScript、Vite、Tailwind CSS 和 shadcn/ui 构建复杂的多组件 claude.ai HTML artifact：用 `scripts/init-artifact.sh` 初始化，开发，再用 `scripts/bundle-artifact.sh` 打包成单个 HTML 文件，然后分享并可选测试。附防“AI 味”的样式规则。
- **怎么用：** 需要带状态、路由或大量组件的复杂 artifact 时使用。简单的单文件 HTML/JSX 不需要它。
- **最适合：** 内容丰富、像应用一样的 claude.ai artifact。

<a id="s-web-asset-generator"></a>
### web-asset-generator

[web-asset-generator.zip](web-asset-generator.zip) · 入口：`spellbook-main/skills/web-asset-generator/SKILL.md`

- **能做什么：** 从 Logo、emoji 或文字标语生成网站 favicon、PWA 应用图标和社交分享图（Open Graph），适用于 Facebook、Twitter/X、WhatsApp 和 LinkedIn，自动调整尺寸并提供 HTML meta 标签。
- **怎么用：** 要求“用我的 Logo 生成 favicon”“做一个 emoji favicon”或“用这句标语做 OG 图”；它会先问几个问题，再运行自带脚本（需安装 `requirements.txt`）。
- **最适合：** 补齐网站的图标和社交预览素材。

<a id="cat-backend"></a>
## 架构、后端与数据

架构决策、API、数据库、数据契约、性能、日志和技术规格。

| 技能 | 最适合 |
|---|---|
| [`api-design`](#s-api-design) | 设计新的 API 及其契约。 |
| [`architecture-foundation`](#s-architecture-foundation) | 实现前的规格与边界决策，尤其适合 Rust 和 Go。 |
| [`architecture-research`](#s-architecture-research) | 需要有据可查、而不是一张功能对比表的技术选型。 |
| [`data-contract-migrations`](#s-data-contract-migrations) | 一旦静默出错代价很高的 schema 和数据结构变更。 |
| [`database-patterns`](#s-database-patterns) | 设计 Postgres schema 和 Redis 缓存层。 |
| [`dev-architecture-playbook`](#s-dev-architecture-playbook) | 按正确顺序、用正确技能把项目从产品意图推进到上线。 |
| [`elegant-architecture`](#s-elegant-architecture) | 从设计上让代码库保持模块化、文件小巧。 |
| [`performance-capacity`](#s-performance-capacity) | 把“让它更快”变成预算和经过验证的改进。 |
| [`structured-logging-lite`](#s-structured-logging-lite) | 让应用可诊断的最小日志契约。 |
| [`technical-spec`](#s-technical-spec) | 团队真的会读、以决策为中心的工程文档。 |

<a id="s-api-design"></a>
### api-design

[api-design.zip](api-design.zip) · 入口：`spellbook-main/skills/api-design/SKILL.md`

- **能做什么：** 观点鲜明的 REST / GraphQL / gRPC API 设计指南：契约优先、OpenAPI 3.2、带 Sunset 头的 URL 版本化、幂等键、游标分页、RFC 7807 错误格式、GraphQL 联邦和 gRPC 流式。附带模板。注意它的立场：直接删除而不是标记废弃。
- **怎么用：** 设计接口、编写 OpenAPI 规范、在 REST/GraphQL/gRPC 之间做选择或评审现有 API 契约时触发。
- **最适合：** 设计新的 API 及其契约。

<a id="s-architecture-foundation"></a>
### architecture-foundation

[architecture-foundation.zip](architecture-foundation.zip) · 入口：`spellbook-main/skills/architecture-foundation/SKILL.md`

- **能做什么：** 先设计架构再写代码：明确的边界、契约、验证关卡和小而具体的执行计划。涵盖 Rust/Go 的 crate、包、模块、运行时和服务边界，对比成熟项目，避免堆叠一次性 PR，以及迁移债务审计。
- **怎么用：** 问“这个项目该用什么架构？”“写代码前先出一份完整规格”或“这是不是堆叠式的一次性工作？”。在已有仓库里它会先解释当前架构。
- **最适合：** 实现前的规格与边界决策，尤其适合 Rust 和 Go。

<a id="s-architecture-research"></a>
### architecture-research

[architecture-research.zip](architecture-research.zip) · 入口：`spellbook-main/skills/architecture-research/SKILL.md`

- **能做什么：** 基于证据的架构调研：领域全景研究、源码级系统考古、自建还是采购（采用/改造/自建）决策、开源与商业方案对比。产出一份由证据台账支撑的决策记录。中文请求如“架构调研”“技术选型”也会触发。
- **怎么用：** 问“X 是怎么构建的？”“Y 应该采用还是自己做？”或“对比 Z 的开源替代方案”。不适合小改动，也不适合方向已定后的详细设计（那用 `architecture-foundation`）。
- **最适合：** 需要有据可查、而不是一张功能对比表的技术选型。

<a id="s-data-contract-migrations"></a>
### data-contract-migrations

[data-contract-migrations.zip](data-contract-migrations.zip) · 入口：`spellbook-main/skills/data-contract-migrations/SKILL.md`

- **能做什么：** 设计并验证数据契约变更：schema 变更、迁移、回滚、回填、兼容窗口、租户隔离以及 API 到数据库的字段映射。字段不存在就当作不存在，不编造兜底字段。
- **怎么用：** 修改数据库 schema、事件载荷、存储文档、分析表或多租户边界时触发。它会先收集读写方、数据量和停机约束再提方案。
- **最适合：** 一旦静默出错代价很高的 schema 和数据结构变更。

<a id="s-database-patterns"></a>
### database-patterns

[database-patterns.zip](database-patterns.zip) · 入口：`spellbook-main/skills/database-patterns/SKILL.md`

- **能做什么：** PostgreSQL + Redis 数据建模：数据类型、schema 设计、索引策略、JSONB 用法、查询优化、连接池、Redis 数据结构与键命名、TTL、旁路缓存/写穿、失效、防击穿与防穿透、冷热分层存储以及锁。
- **怎么用：** 设计表、索引或缓存，或评审缓存一致性时触发。
- **最适合：** 设计 Postgres schema 和 Redis 缓存层。

<a id="s-dev-architecture-playbook"></a>
### dev-architecture-playbook

[dev-architecture-playbook.zip](dev-architecture-playbook.zip) · 入口：`spellbook-main/skills/dev-architecture-playbook/SKILL.md`

- **能做什么：** spellbook 工程类技能的生命周期路由器：先给请求分类（想法、架构、API/数据/安全契约、实现、测试、发布、运维），挑选最小的技能组合，并设置关卡，确保在必要的契约存在之前不开始实现。
- **怎么用：** 要求“为这个想法/仓库做一套完整的开发架构”或问“这件事该组合哪些技能？”。它会交给 `product-discovery`、`prd-master`、`architecture-foundation`、`api-design`、`release-engineering` 等。
- **最适合：** 按正确顺序、用正确技能把项目从产品意图推进到上线。

<a id="s-elegant-architecture"></a>
### elegant-architecture

[elegant-architecture.zip](elegant-architecture.zip) · 入口：`spellbook-main/skills/elegant-architecture/SKILL.md`

- **能做什么：** 每个文件严格不超过 200 行的整洁架构纪律：先规划，先定接口，把大文件拆成文件夹，使用依赖注入/工厂/策略模式，测试真实行为而不用 Mock。
- **怎么用：** 开始新功能、重构大文件或规划模块结构时触发。
- **最适合：** 从设计上让代码库保持模块化、文件小巧。

<a id="s-performance-capacity"></a>
### performance-capacity

[performance-capacity.zip](performance-capacity.zip) · 入口：`spellbook-main/skills/performance-capacity/SKILL.md`

- **能做什么：** 先让性能可度量，再做优化：基线（p50/p95/p99、数据规模、并发、资源上限）、按界面划分的性能预算、压测、容量估算、瓶颈假设、缓存与查询效率、队列吞吐和回归关卡。
- **怎么用：** 某个功能可能很慢、系统需要扩容、怀疑性能回退，或上线取决于吞吐、成本或延迟时触发。
- **最适合：** 把“让它更快”变成预算和经过验证的改进。

<a id="s-structured-logging-lite"></a>
### structured-logging-lite

[structured-logging-lite.zip](structured-logging-lite.zip) · 入口：`spellbook-main/skills/structured-logging-lite/SKILL.md`

- **能做什么：** 根据仓库证据设计、审计或实现应用的结构化日志：要不要记、在哪里记，选择或迁移日志库，统一事件名、字段、级别和脱敏，HTTP 访问日志和 panic 日志，以及为什么生产日志回答不了某个事故问题。除非要求实现，否则只读。
- **怎么用：** 问“我们应该在哪里加日志？”“统一我们的日志字段”或“昨晚的事故日志解释不了”。不用于实时查看日志或完整的可观测性建设（那用 `observability-sre`）。
- **最适合：** 让应用可诊断的最小日志契约。

<a id="s-technical-spec"></a>
### technical-spec

[technical-spec.zip](technical-spec.zip) · 入口：`spellbook-main/skills/technical-spec/SKILL.md`

- **能做什么：** 技术设计文档、RFC 和架构决策记录（ADR）：问题陈述、方案、必须列出的备选方案、必需的图（C4 模型、图即代码）、成功指标、风险与应对，以及技术选型评估框架。附模板。
- **怎么用：** 写设计文档、RFC 或 ADR，或比较技术方案时触发。
- **最适合：** 团队真的会读、以决策为中心的工程文档。

<a id="cat-languages"></a>
## 编程语言与项目模板

Go、Python、TypeScript、Rust、Zig 和鸿蒙的项目模板与惯用写法。

| 技能 | 最适合 |
|---|---|
| [`golang-web`](#s-golang-web) | 快速搭起一个整洁、地道的 Go 服务。 |
| [`harmonyos-app`](#s-harmonyos-app) | 原生鸿蒙应用。 |
| [`python-project`](#s-python-project) | 快速搭起一个整洁、现代的 Python 项目。 |
| [`rust-best-practices`](#s-rust-best-practices) | 编写和评审地道的 Rust 代码。 |
| [`rust-project`](#s-rust-project) | 搭起一个结构良好的 Rust 项目。 |
| [`typescript-project`](#s-typescript-project) | 搭起一个整洁的 TypeScript 代码库。 |
| [`zig-project`](#s-zig-project) | 搭起一个地道的 Zig 项目。 |

<a id="s-golang-web"></a>
### golang-web

[golang-web.zip](golang-web.zip) · 入口：`spellbook-main/skills/golang-web/SKILL.md`

- **能做什么：** 现代 Go Web 架构指南：标准 `cmd/internal/pkg` 布局、在 `main.go` 里显式装配依赖、在使用方定义接口、错误包装、Viper 配置、优雅关闭、Makefile 和检查清单。观点鲜明：不保留向后兼容层，LLM 调用统一走 LiteLLM 代理。
- **怎么用：** 新建 Go Web 项目、API 或微服务时触发。
- **最适合：** 快速搭起一个整洁、地道的 Go 服务。

<a id="s-harmonyos-app"></a>
### harmonyos-app

[harmonyos-app.zip](harmonyos-app.zip) · 入口：`spellbook-main/skills/harmonyos-app/SKILL.md`

- **能做什么：** HarmonyOS NEXT（API 12+）应用开发：严格类型的 ArkTS、声明式 ArkUI 与状态装饰器、只用 Stage 模型（UIAbility）、分布式与多设备设计、元服务、项目结构和组件模式（LazyForEach、自定义弹窗）。
- **怎么用：** 开发或评审鸿蒙应用时触发。
- **最适合：** 原生鸿蒙应用。

<a id="s-python-project"></a>
### python-project

[python-project.zip](python-project.zip) · 入口：`spellbook-main/skills/python-project/SKILL.md`

- **能做什么：** 现代 Python 项目架构：用 uv 管理包和 Python 版本，用 Ruff 做检查和格式化，用 Pydantic 和 mypy 管类型，src 布局，只用 pyproject.toml，FastAPI，全链路异步，LLM 调用走 LiteLLM 代理。观点鲜明：直接删除而不是标记废弃。
- **怎么用：** 新建 Python API、命令行工具或数据管道时触发；附模板。
- **最适合：** 快速搭起一个整洁、现代的 Python 项目。

<a id="s-rust-best-practices"></a>
### rust-best-practices

[rust-best-practices.zip](rust-best-practices.zip) · 入口：`spellbook-main/skills/rust-best-practices/SKILL.md` · `spellbook-main/plugins/rust-dev/skills/rust-best-practices.SKILL.md`

- **能做什么：** 遵循微软 Pragmatic Rust 指南的地道 Rust：类型驱动设计、所有权、库用 `thiserror` 而应用用 `anyhow`、库中不 panic、构建者模式、newtype、`impl Trait`、性能、异步和测试。压缩包里有核心版和 `rust-dev` 插件版。
- **怎么用：** 在任何 Rust 编辑或评审之前调用，或在被生命周期、借用检查器、异步 Rust 困住时使用。
- **最适合：** 编写和评审地道的 Rust 代码。

<a id="s-rust-project"></a>
### rust-project

[rust-project.zip](rust-project.zip) · 入口：`spellbook-main/skills/rust-project/SKILL.md`

- **能做什么：** 现代 Rust 项目架构：单 crate 与 Cargo workspace、Web 框架和 ORM 选择、`main.rs`/`lib.rs`/`error.rs`/handlers/services 分层、Tokio + tracing、命令行结构和测试。观点鲜明：直接删除而不是标记废弃；LLM 调用走 LiteLLM 代理。
- **怎么用：** 新建 Rust 命令行工具、Web 服务或库时触发；附模板。
- **最适合：** 搭起一个结构良好的 Rust 项目。

<a id="s-typescript-project"></a>
### typescript-project

[typescript-project.zip](typescript-project.zip) · 入口：`spellbook-main/skills/typescript-project/SKILL.md`

- **能做什么：** 现代 TypeScript 项目架构：严格类型、不用 `any`、Zod 运行时校验、Node 22+ 或 Bun 上的 ESM、`lib/services/adapters` 分层、每个文件不超过 200 行、用 Vitest/Bun test 且尽量少用 Mock、直接删除而不是标记废弃、LLM 调用走 LiteLLM 代理。
- **怎么用：** 新建 TS 项目、配置或设计结构时触发；附模板。
- **最适合：** 搭起一个整洁的 TypeScript 代码库。

<a id="s-zig-project"></a>
### zig-project

[zig-project.zip](zig-project.zip) · 入口：`spellbook-main/skills/zig-project/SKILL.md`

- **能做什么：** 现代 Zig 项目架构：没有隐藏的内存分配或控制流，显式传递分配器（arena 模式），用 comptime 代替宏，用错误联合配合 try/catch/errdefer，内联测试、构建系统和项目结构。观点鲜明：直接删除而不是标记废弃；LLM 调用走 LiteLLM。
- **怎么用：** 新建 Zig 命令行工具、系统程序、游戏开发或高性能服务时触发；附模板。
- **最适合：** 搭起一个地道的 Zig 项目。

<a id="cat-testing"></a>
## 测试、调试与代码质量

测试策略、TDD、调试方法、QA 和代码库审计。

| 技能 | 最适合 |
|---|---|
| [`app-user-story-qa`](#s-app-user-story-qa) | 对整个 App 做一次全面、系统的 QA。 |
| [`codebase-audit`](#s-codebase-audit) | 定期对整个项目做深度体检。 |
| [`comprehensive-testing`](#s-comprehensive-testing) | 建立或改进项目的测试方法。 |
| [`playwright-automation`](#s-playwright-automation) | 脚本化的浏览器检查和界面测试。 |
| [`project-health-auditor`](#s-project-health-auditor) | 快速了解一个仓库的质量和技术债状况。 |
| [`systematic-debugging`](#s-systematic-debugging) | 有纪律地排查 bug。 |
| [`test-driven-development`](#s-test-driven-development) | 强制执行真正的测试先行开发。 |

<a id="s-app-user-story-qa"></a>
### app-user-story-qa

[app-user-story-qa.zip](app-user-story-qa.zip) · 入口：`spellbook-main/skills/app-user-story-qa/SKILL.md`

- **能做什么：** 把“测试这个 App 的每个功能”变成可控的循环：从代码中盘点功能，把预期行为写进统一的跟踪表格，逐个测试用户故事，给缺陷分类，（仅在授权时）修复并复测。
- **怎么用：** 在 App 的仓库里说“审计每个功能”“测试所有用户路径”或“修复并复测记录在案的 UX 缺陷”。
- **最适合：** 对整个 App 做一次全面、系统的 QA。

<a id="s-codebase-audit"></a>
### codebase-audit

[codebase-audit.zip](codebase-audit.zip) · 入口：`spellbook-main/skills/codebase-audit/SKILL.md`

- **能做什么：** 全代码库审计，按你的技术栈调整并行分析 agent：前后端契约、数据完整性、异常处理与安全、架构与技术债、配置与缓存。严重和高危问题会经过对抗式验证，结果与上一次审计对比，最终得到按严重程度排序的报告和分阶段修复路线图。有快速体检模式。严格只读。
- **怎么用：** 说“审计这个代码库”“健康检查”“找隐藏 bug / 静默降级”“全面审查”或“快速体检”。
- **最适合：** 定期对整个项目做深度体检。

<a id="s-comprehensive-testing"></a>
### comprehensive-testing

[comprehensive-testing.zip](comprehensive-testing.zip) · 入口：`spellbook-main/skills/comprehensive-testing/SKILL.md`

- **能做什么：** 完整的测试策略：TDD 流程、测试金字塔、单元/集成/端到端/属性测试、Jest、Vitest 和 pytest 最佳实践、Mock 策略以及 CI 集成。
- **怎么用：** 写测试、评审测试质量或制定团队测试规范时触发。
- **最适合：** 建立或改进项目的测试方法。

<a id="s-playwright-automation"></a>
### playwright-automation

[playwright-automation.zip](playwright-automation.zip) · 入口：`spellbook-main/skills/playwright-automation/SKILL.md`

- **能做什么：** 用 Playwright 做浏览器自动化和测试：编写脚本来检查页面、截图、填写表单、测试响应式视图，以及收集控制台和网络证据。
- **怎么用：** 要求测试网页应用、自动化浏览器任务、截图或验证界面行为；细节在 `references/full-guide.md`。
- **最适合：** 脚本化的浏览器检查和界面测试。

<a id="s-project-health-auditor"></a>
### project-health-auditor

[project-health-auditor.zip](project-health-auditor.zip) · 入口：`spellbook-main/skills/project-health-auditor/SKILL.md`

- **能做什么：** 多维度的代码库健康检查：代码质量（大文件、长函数、深嵌套、重复、死代码）、依赖（过期、有漏洞、未使用、包体积）、安全（密钥、硬编码凭据）、测试覆盖、文档和架构，并给出评分报告。
- **怎么用：** 问“评估一下这个项目的健康状况”或“找出我们的技术债”。比 `codebase-audit` 更轻量。
- **最适合：** 快速了解一个仓库的质量和技术债状况。

<a id="s-systematic-debugging"></a>
### systematic-debugging

[systematic-debugging.zip](systematic-debugging.zip) · 入口：`spellbook-main/skills/systematic-debugging/SKILL.md`

- **能做什么：** 来自 obra/superpowers 的四阶段调试框架：根因调查（读错误、复现、查最近改动、收集证据）→ 模式分析 → 假设与验证 → 实现修复，并有“三次修复失败就停下重新思考”的规则。
- **怎么用：** 遇到 bug、报错或异常行为、想避免乱改时触发。
- **最适合：** 有纪律地排查 bug。

<a id="s-test-driven-development"></a>
### test-driven-development

[test-driven-development.zip](test-driven-development.zip) · 入口：`spellbook-main/skills/test-driven-development.SKILL.md`

- **能做什么：** 来自 obra/superpowers 的严格 TDD：铁律“没有失败的测试就不写生产代码”，红 → 绿 → 重构，每一步都必须验证，列出必须拒绝的借口和需要重来的危险信号。
- **怎么用：** 写功能、修 bug 或重构、想坚持测试先行时触发。入口是 spellbook 包里的 `skills/test-driven-development.SKILL.md`。
- **最适合：** 强制执行真正的测试先行开发。

<a id="cat-devops"></a>
## DevOps、发布与可靠性

CI/CD、配置与密钥、可观测性、SLO 和发布。

| 技能 | 最适合 |
|---|---|
| [`config-secrets-environments`](#s-config-secrets-environments) | 在各环境中做到干净、经过校验的配置与密钥管理。 |
| [`devops-excellence`](#s-devops-excellence) | 安全、现代的 CI/CD 和基础设施配置。 |
| [`incident-slo-runbook`](#s-incident-slo-runbook) | 把监控指标变成真正可执行的值班和事故流程。 |
| [`observability-sre`](#s-observability-sre) | 设计一套按用户真实感受来告警的监控体系。 |
| [`release-engineering`](#s-release-engineering) | 安全、可重复的发布。 |

<a id="s-config-secrets-environments"></a>
### config-secrets-environments

[config-secrets-environments.zip](config-secrets-environments.zip) · 入口：`spellbook-main/skills/config-secrets-environments/SKILL.md`

- **能做什么：** 设计、审计和验证配置与密钥：环境隔离（本地/开发/预发/生产）、配置 schema 与校验、BYOK 流程、密钥轮换和漂移检查。从不打印真实密钥。
- **怎么用：** 新增环境变量、修改运行时配置、处理 API key 或用户自带 key、排查配置漂移或准备发布配置时触发。
- **最适合：** 在各环境中做到干净、经过校验的配置与密钥管理。

<a id="s-devops-excellence"></a>
### devops-excellence

[devops-excellence.zip](devops-excellence.zip) · 入口：`spellbook-main/skills/devops-excellence/SKILL.md`

- **能做什么：** DevOps 与 CI/CD 指南，附硬性规则：用 OIDC 代替固定云凭据、容器不用 root、镜像里不放密钥、生产部署受保护。涵盖 GitHub Actions、Docker、Kubernetes、Terraform、GitOps、渐进式发布和部署策略选择，附模板。
- **怎么用：** 搭建流水线、容器化应用、部署到 Kubernetes 或选择发布策略时触发。
- **最适合：** 安全、现代的 CI/CD 和基础设施配置。

<a id="s-incident-slo-runbook"></a>
### incident-slo-runbook

[incident-slo-runbook.zip](incident-slo-runbook.zip) · 入口：`spellbook-main/skills/incident-slo-runbook/SKILL.md`

- **能做什么：** 创建或审计 SLO 与 SLI、燃烧率告警、事故响应步骤、升级路径、事后复盘、运维手册和对客户影响的沟通——为每条关键用户路径把可观测性和实际行动连接起来。
- **怎么用：** 定义生产可靠性、准备上线就绪评审、处理故障、编写运维手册、调整告警或收尾一次事故时触发。
- **最适合：** 把监控指标变成真正可执行的值班和事故流程。

<a id="s-observability-sre"></a>
### observability-sre

[observability-sre.zip](observability-sre.zip) · 入口：`spellbook-main/skills/observability-sre/SKILL.md`

- **能做什么：** 可观测性与 SRE 指南：用 Prometheus、Grafana 和 OpenTelemetry 做指标、日志和链路追踪；硬性规则包括只对症状告警、标签低基数、基于 SLO 的错误预算、日志里带 trace 上下文；分层 Prometheus 架构和事故响应实践。附模板。
- **怎么用：** 搭建监控、日志或链路追踪，定义 SLO 或处理事故时触发。
- **最适合：** 设计一套按用户真实感受来告警的监控体系。

<a id="s-release-engineering"></a>
### release-engineering

[release-engineering.zip](release-engineering.zip) · 入口：`spellbook-main/skills/release-engineering/SKILL.md`

- **能做什么：** 把“可以合并”变成受控的发布：先给发布分类（补丁、功能、API/SDK、数据库迁移、配置/密钥、基础设施），再套用对应关卡——版本号、变更日志、发布分支、功能开关、金丝雀、迁移关卡、回滚证明、部署检查。
- **怎么用：** 准备发布、上线有风险的 PR、协调应用/后端/数据库的发布、从糟糕的部署中恢复或制定仓库发布策略时触发。
- **最适合：** 安全、可重复的发布。

<a id="cat-security"></a>
## 安全

身份认证、威胁建模、服务器加固和供应链检查。

| 技能 | 最适合 |
|---|---|
| [`auth-security`](#s-auth-security) | 构建或审计身份认证与令牌管理。 |
| [`npm-supply-chain-check`](#s-npm-supply-chain-check) | npm 供应链事件爆发时的快速应对。 |
| [`security-threat-model`](#s-security-threat-model) | 在代码上线前发现安全风险。 |
| [`server-security`](#s-server-security) | 加固 VPS 或自建服务器。 |

<a id="s-auth-security"></a>
### auth-security

[auth-security.zip](auth-security.zip) · 入口：`spellbook-main/skills/auth-security/SKILL.md`

- **能做什么：** 遵循 RFC 9700 的 OAuth 2.1 与 JWT 安全实践：全面使用 PKCE、短时效访问令牌、刷新令牌轮换、HttpOnly Cookie 存储、显式校验算法、DPoP、令牌撤销，以及最后的检查清单。
- **怎么用：** 实现登录、API 授权或令牌处理，或评审现有认证代码时触发。
- **最适合：** 构建或审计身份认证与令牌管理。

<a id="s-npm-supply-chain-check"></a>
### npm-supply-chain-check

[npm-supply-chain-check.zip](npm-supply-chain-check.zip) · 入口：`spellbook-main/skills/npm-supply-chain-check/SKILL.md`

- **能做什么：** 只读扫描仓库、锁文件和 `node_modules`，查找已知的恶意 npm 包版本和安装时供应链攻击迹象（如 Shai-Hulud、Keyv/cacheable 事件、可疑的 preinstall 脚本、窃取凭据的包）。区分“依赖里引用了它”和“恶意代码确实执行过”，从不打印密钥值。附带带日期的 IOC 列表和确定性扫描器。
- **怎么用：** 说“这个项目有没有受到 Shai-Hulud npm 攻击影响？”或“检查有没有被投毒的 npm 包”。默认只扫描当前仓库，除非你扩大范围。不是通用 CVE 或许可证审计。
- **最适合：** npm 供应链事件爆发时的快速应对。

<a id="s-security-threat-model"></a>
### security-threat-model

[security-threat-model.zip](security-threat-model.zip) · 入口：`spellbook-main/skills/security-threat-model/SKILL.md`

- **能做什么：** 为功能、API、数据流、密钥、权限、供应链变更、认证边界和高风险代码路径做威胁建模：梳理资产、角色、信任边界和入口，运行威胁清单并列出必需的控制措施。与 `auth-security` 和 `server-security` 互补。
- **怎么用：** 在开发或评审涉及认证、授权、支付、密钥、用户数据、上传、Webhook、管理后台、`innerHTML`/`eval`/`exec`、依赖升级或跨租户访问的改动之前或期间触发。
- **最适合：** 在代码上线前发现安全风险。

<a id="s-server-security"></a>
### server-security

[server-security.zip](server-security.zip) · 入口：`spellbook-main/skills/server-security/SKILL.md`

- **能做什么：** 通过 SSH 做服务器安全审计和可回退的加固：SSH 配置、防火墙、暴露端口、用户、服务、文件权限、暴力破解尝试和更新状况，生成报告并提供一键修复。
- **怎么用：** 带 SSH 目标运行（如 `root@1.2.3.4`），说“审计 / 加固这台服务器”。修复只在你确认后执行；细节见 `references/full-guide.md`。
- **最适合：** 加固 VPS 或自建服务器。

<a id="cat-git"></a>
## Git 与开源贡献

提交、仓库搭建和为别人的项目做贡献。

| 技能 | 最适合 |
|---|---|
| [`contribution-architect`](#s-contribution-architect) | 从修小 bug 进阶到架构级贡献或成为模块负责人。 |
| [`contributor`](#s-contributor) | 给别人的项目做贡献，避免常见的被拒原因。 |
| [`git-commit-smart`](#s-git-commit-smart) | 保持一致、描述清楚的提交历史。 |
| [`push-all`](#s-push-all) | 带安全网的快速“全部上线”提交。 |
| [`repo-scaffold`](#s-repo-scaffold) | 给新仓库或原型仓库打下扎实基础。 |

<a id="s-contribution-architect"></a>
### contribution-architect

[contribution-architect.zip](contribution-architect.zip) · 入口：`spellbook-main/skills/contribution-architect/SKILL.md`

- **能做什么：** 开源架构导师，帮你跳出“新手友好 issue”，找到高价值的贡献：复杂度热点、高耦合或无人维护的模块、测试缺口和 TODO/HACK 技术债。产出战略投资清单（高回报、速赢、长期）并起草 RFC 和设计提案。
- **怎么用：** 在想参与的项目里说“分析这个项目，找有意义的活”或“为 X 起草一份 RFC”。
- **最适合：** 从修小 bug 进阶到架构级贡献或成为模块负责人。

<a id="s-contributor"></a>
### contributor

[contributor.zip](contributor.zip) · 入口：`spellbook-main/skills/contributor/SKILL.md`

- **能做什么：** 从 GitHub 仓库地址到提交 PR 的端到端开源贡献流程：扫描 issue，检查是否有竞争 PR 或应改在上游，先在 issue 下贴解决思路，fork 并配置仓库，遵守贡献指南和 CI，实现带测试的最小修复，并按规范提交。
- **怎么用：** 说“我想给 <仓库地址> 做贡献”“找 good first issue”或“帮我修 #123 并提 PR”。需要 `git` 和 GitHub CLI。
- **最适合：** 给别人的项目做贡献，避免常见的被拒原因。

<a id="s-git-commit-smart"></a>
### git-commit-smart

[git-commit-smart.zip](git-commit-smart.zip) · 入口：`spellbook-main/skills/git-commit-smart/SKILL.md`

- **能做什么：** 分析已暂存的改动，写出有意义的 Conventional Commit 提交信息（类型、范围、主题、正文、脚注、破坏性变更），附示例和反面案例。
- **怎么用：** 暂存改动后说“提交一下”或“写提交信息”。
- **最适合：** 保持一致、描述清楚的提交历史。

<a id="s-push-all"></a>
### push-all

[push-all.zip](push-all.zip) · 入口：`spellbook-main/skills/push-all.SKILL.md`

- **能做什么：** 在安全检查后暂存全部改动、提交并推送：遇到密钥（`.env`、私钥、证书、真实 API token）和大文件会停下来警告，请你确认，再按仓库风格写提交信息。
- **怎么用：** 只有你明确要求时使用，例如“全部提交并推送”。入口是 spellbook 包里的 `skills/push-all.SKILL.md`。
- **最适合：** 带安全网的快速“全部上线”提交。

<a id="s-repo-scaffold"></a>
### repo-scaffold

[repo-scaffold.zip](repo-scaffold.zip) · 入口：`spellbook-main/skills/repo-scaffold/SKILL.md`

- **能做什么：** 搭建或规范一个可上线的仓库：规格文档（`PRODUCT.md`、`TECH.md`、ADR）、源码布局、测试、CI、agent 上下文、配置示例、发布说明和运维手册——沿用已有约定，不另起平行目录。
- **怎么用：** 新建仓库、把原型变成可维护项目或补齐缺失的基础设施时触发。只需要 AGENTS.md 时用 `agentsmd-scaffold`。
- **最适合：** 给新仓库或原型仓库打下扎实基础。

<a id="cat-agents"></a>
## 编程 agent：Claude Code、Codex 与多 agent 协作

agent 指令（AGENTS.md / CLAUDE.md）、Codex 集成、护栏、编排和会话维护。

| 技能 | 最适合 |
|---|---|
| [`agentsmd-optimize`](#s-agentsmd-optimize) | 已经变得杂乱或自相矛盾的指令集。 |
| [`agentsmd-scaffold`](#s-agentsmd-scaffold) | 让一个仓库适合 Codex / Claude Code 等 agent 上手工作。 |
| [`claude-code-reverse`](#s-claude-code-reverse) | 验证本地工具的内部行为，或查看两个版本之间改了什么。 |
| [`codex`](#s-codex) | 在 Claude Code 里把编程任务交给 Codex。 |
| [`codex-agent`](#s-codex-agent) | 在 Claude Code 里做跨模型代码评审。 |
| [`codex-fluent`](#s-codex-fluent) | Codex 会话的日常维护。 |
| [`codex-log-guard`](#s-codex-log-guard) | 阻止 Codex 悄悄大量写盘。 |
| [`codex-retrospective`](#s-codex-retrospective) | 让 Codex 逐渐适应你的风格和工作流。 |
| [`flowguard`](#s-flowguard) | 跨越大量文件、工具、会话或多个 agent 的长时间 agent 工作。 |
| [`meta-timing`](#s-meta-timing) | 设计不让人厌烦的通知和主动 agent 时机。 |
| [`multi-model-orchestrator`](#s-multi-model-orchestrator) | 需要共享计划和审计记录的多 agent 项目。 |
| [`overengineering-brake`](#s-overengineering-brake) | 防止 agent 把简单请求做得过于复杂。 |
| [`persona-team`](#s-persona-team) | 用 Hermes 搭建分工明确的多 agent 团队。 |
| [`recap`](#s-recap) | 每周反思你实际是怎么使用编程 agent 的。 |
| [`repo-agent-context-audit`](#s-repo-agent-context-audit) | 检查一个仓库是否方便编程 agent 工作。 |
| [`review-agent-harness`](#s-review-agent-harness) | 诊断仓库中系统性的 agent 失败。 |
| [`review-gate`](#s-review-gate) | 让人始终参与 agent 做出的改动。 |
| [`sol-luna-router`](#s-sol-luna-router) | 可审计的“委派 + 验证”式编程，配合独立的 worker agent。 |
| [`threads`](#s-threads) | 在 Codex 中安全地并行处理一批 issue 或 PR。 |
| [`vibeguard`](#s-vibeguard) | 不依赖重型工具，让 AI 辅助的工作保持范围清楚、实事求是。 |

<a id="s-agentsmd-optimize"></a>
### agentsmd-optimize

[agentsmd-optimize.zip](agentsmd-optimize.zip) · 入口：`spellbook-main/skills/agentsmd-optimize/SKILL.md`

- **能做什么：** 审计并整理 AI 编程 agent 的指令——AGENTS.md、CLAUDE.md、技能和 agent 定义。找出互相冲突的规则、导致频繁请求批准的原因、触发范围过宽的技能、重复的指导和失效的引用。除非你授权修改，否则只读。
- **怎么用：** 说“审计我的 AGENTS.md / CLAUDE.md”“为什么 agent 老是停下来问我”或“清理我的技能触发词”。如果要它直接改，请明确说出来。
- **最适合：** 已经变得杂乱或自相矛盾的指令集。

<a id="s-agentsmd-scaffold"></a>
### agentsmd-scaffold

[agentsmd-scaffold.zip](agentsmd-scaffold.zip) · 入口：`spellbook-main/skills/agentsmd-scaffold/SKILL.md`

- **能做什么：** 根据仓库里的真实证据生成或更新该仓库专用的 AGENTS.md：根目录文件加各子目录的分区文件，包含验证命令、生成文件边界和简短的上手导航。
- **怎么用：** 在仓库里说“为这个仓库创建 AGENTS.md”或“按目录拆分 AGENTS.md”。它先给方案，只有你要求应用时才写文件。如果只想体检，用 `repo-agent-context-audit`。
- **最适合：** 让一个仓库适合 Codex / Claude Code 等 agent 上手工作。

<a id="s-claude-code-reverse"></a>
### claude-code-reverse

[claude-code-reverse.zip](claude-code-reverse.zip) · 入口：`spellbook-main/skills/claude-code-reverse/SKILL.md`

- **能做什么：** 对你拥有或获得授权的本机可执行文件做只读静态逆向——Claude Code 和其他 CLI、Mach-O、ELF、PE、Wasm 或打包应用：文件身份、字符串、符号、依赖、段表，以及版本间对比。从不运行目标，拒绝破解、绕过许可或计费。
- **怎么用：** 需要明确提出，例如“逆向一下这个 CLI 的这段界面文字来自哪里”或“对比这两个 Claude Code 版本”。使用自带的 `extract.sh`，按 SHA-256 缓存。
- **最适合：** 验证本地工具的内部行为，或查看两个版本之间改了什么。

<a id="s-codex"></a>
### codex

[codex.zip](codex.zip) · 入口：`spellbook-main/skills/codex/SKILL.md`

- **能做什么：** 在 Claude Code 里运行 OpenAI Codex CLI（`codex exec`、`codex resume`）做分析、重构或自动编辑，带有安全的提示词传递、最小必要沙箱（只读或工作区可写）、批量成本闸门和后续跟进处理。
- **怎么用：** 说“用 Codex 跑这个”或“让 Codex 重构 X”。它会先检查 `codex --version`，只使用你已安装版本支持的参数。
- **最适合：** 在 Claude Code 里把编程任务交给 Codex。

<a id="s-codex-agent"></a>
### codex-agent

[codex-agent.zip](codex-agent.zip) · 入口：`spellbook-main/skills/codex-agent/SKILL.md`

- **能做什么：** 让 Claude Code 调用 OpenAI 的 Codex CLI 做第二意见评审、在 Claude 实现之后交叉验证、调试分析以及提供替代实现。Codex 只读评审；只有你要求时 Claude 才会应用修复。
- **怎么用：** 需要已安装并登录 Codex CLI（`npm i -g @openai/codex` 或 Homebrew）。说“让 Codex 评审这个 diff / 文件 / 项目”或“让 Codex 再检查一遍”。
- **最适合：** 在 Claude Code 里做跨模型代码评审。

<a id="s-codex-fluent"></a>
### codex-fluent

[codex-fluent.zip](codex-fluent.zip) · 入口：`spellbook-main/skills/codex-fluent/SKILL.md`

- **能做什么：** 在长期高强度使用后让 Codex 保持轻快：诊断会话膨胀，为有价值的工作创建必须的交接文档，把旧会话归档（从不删除）并保留清晰的恢复路径，然后验证效果。
- **怎么用：** 说“Codex 变慢 / 变臃肿了”或“清理我的 Codex 会话”。先出报告；也可以设置定期提醒。
- **最适合：** Codex 会话的日常维护。

<a id="s-codex-log-guard"></a>
### codex-log-guard

[codex-log-guard.zip](codex-log-guard.zip) · 入口：`spellbook-main/skills/codex-log-guard/SKILL.md`

- **能做什么：** 诊断 Codex 本地 SQLite 诊断日志（`logs_2.sqlite` 及其 WAL 文件）写入过多、可能损耗 SSD 的问题。默认只读；可以安装并验证 `block_log_inserts` 防护，只有在你明确要求时才会在备份后清理。
- **怎么用：** 提到 `logs_2.sqlite`、SSD/TBW 损耗，或要求保护、清理、验证、恢复 Codex 日志。模式：仅诊断（默认）、保护、清理、恢复。
- **最适合：** 阻止 Codex 悄悄大量写盘。

<a id="s-codex-retrospective"></a>
### codex-retrospective

[codex-retrospective.zip](codex-retrospective.zip) · 入口：`spellbook-main/skills/codex-retrospective/SKILL.md`

- **能做什么：** Codex 的自我改进循环：回顾它最近一段时间（最近 N 天或指定时期）的历史，找出反复出现的摩擦和失败，提出最小但高价值的 AGENTS.md 更新和小型可复用技能——经你批准后才应用。
- **怎么用：** 说“对最近 7 天做一次 Codex 复盘”。可与 `codex-fluent` 搭配。
- **最适合：** 让 Codex 逐渐适应你的风格和工作流。

<a id="s-flowguard"></a>
### flowguard

[flowguard.zip](flowguard.zip) · 入口：`spellbook-main/skills/flowguard/SKILL.md`

- **能做什么：** 长时间、模糊或有状态的 agent 工作的统一入口，用来防止“跑偏”：先给任务分流，核实当前仓库/运行状态而不是轻信摘要，在明确的停止条件下分段执行，设置验证和评审关卡，并留下可恢复的交接文档。它协调其他技能，而不是取代它们。
- **怎么用：** 多步骤任务、自主循环、仓库改动、PR 就绪检查、上下文压缩交接、从之前的上下文恢复或成本检查点时触发（“从昨天的交接继续这个任务”）。
- **最适合：** 跨越大量文件、工具、会话或多个 agent 的长时间 agent 工作。

<a id="s-meta-timing"></a>
### meta-timing

[meta-timing.zip](meta-timing.zip) · 入口：`内层包/meta-timing-migration-v2.0.0/meta-timing/SKILL.md`

- **能做什么：** 元级“何时行动”框架：决定什么时候打断、静默浮现、提醒、自主行动、等待、批量或升级。把“做什么”（显式内容门）和“何时做”（确定性时机策略：硬性禁推窗口 + 精确的可推窗口）分开，按人适配，并输出标准的“时机决策契约”。
- **怎么用：** 设计通知、提醒、主动 agent 行为或打断策略时调用（“这个什么时候推？”“通知策略”）。它声明依赖 `agent-harness-loop` 和 `scr-judgment`，这两个不在本仓库中。
- **最适合：** 设计不让人厌烦的通知和主动 agent 时机。

<a id="s-multi-model-orchestrator"></a>
### multi-model-orchestrator

[multi-model-orchestrator.zip](multi-model-orchestrator.zip) · 入口：`spellbook-main/skills/multi-model-orchestrator/SKILL.md`

- **能做什么：** 用一份交接文档作为唯一事实来源，轻量地协调多个 AI agent（Claude 各模型、Codex 或其他）完成复杂工作：拆解 → 并行执行 → 汇总反馈，全程可追溯。附带用于 Claude Code 和 Codex 的模板。
- **怎么用：** 要求“把这件事分给多个 agent 做”或“为这个项目建一份交接文档”；按 SKILL.md 里的快速开始操作。
- **最适合：** 需要共享计划和审计记录的多 agent 项目。

<a id="s-overengineering-brake"></a>
### overengineering-brake

[overengineering-brake.zip](overengineering-brake.zip) · 入口：`overengineering-brake/skills/overengineering-brake/SKILL.md`

- **能做什么：** 让 agent 的工作完整但不过度：把你的请求变成有边界的任务契约，把“回答 / 评审 / 监控”视为只读，后来更严格的指令立即覆盖之前更宽的范围，砍掉推测性的附加项、重复验证、不必要的依赖、哈希、备份、报告和子 agent——同时不阻碍必要的工作。
- **怎么用：** 作为常驻防护安装；适用于普通任务、技能创建、维护、迁移、审计和多阶段工作。入口是 `overengineering-brake/skills/overengineering-brake/SKILL.md`。
- **最适合：** 防止 agent 把简单请求做得过于复杂。

<a id="s-persona-team"></a>
### persona-team

[persona-team.zip](persona-team.zip) · 入口：`persona-team/SKILL.md`

- **能做什么：** 给多 agent 团队（Hermes profile）配岗位人格：每个岗位一张人格卡（五个工作维度、职责、禁区），编译成该 profile 的 SOUL.md；按岗位匹配人格（可用 MBTI 输入）；用看板协议协作；用探针检验人格是否立住。默认六个岗位：调度、研究、创意、执行、审核、裁决。
- **怎么用：** 说“搭一个 agent 团队”“我的审核 bot 该配什么性格？”“给我一个 INTJ 的审核员”或“这个 bot 不像它该有的样子”。人格卡存放在 `~/.hermes/personas/`；需要终端权限。
- **最适合：** 用 Hermes 搭建分工明确的多 agent 团队。

<a id="s-recap"></a>
### recap

[recap.zip](recap.zip) · 入口：`spellbook-main/skills/recap/SKILL.md`

- **能做什么：** 从原始会话文件（而不是你的记忆）回顾你最近 N 天的 Claude Code 使用情况：按主题分组，对照个人“操作系统”覆盖表，输出模式、风险以及工作流的增删建议。可选跨机器汇总。
- **怎么用：** 运行 `/recap` 或说“看看我这几天用 Claude 做了什么”。周回顾用 `scripts/extract_sessions.py --days 7`；`--json` 输出结构化数据。
- **最适合：** 每周反思你实际是怎么使用编程 agent 的。

<a id="s-repo-agent-context-audit"></a>
### repo-agent-context-audit

[repo-agent-context-audit.zip](repo-agent-context-audit.zip) · 入口：`spellbook-main/skills/repo-agent-context-audit/SKILL.md`

- **能做什么：** 只读审计并评分一个仓库面向 agent 的上下文：AGENTS.md、CLAUDE.md、WARP.md、CONTRIBUTING.md、`.agents/skills` 以及 `specs/PRODUCT.md` / `TECH.md`。推荐向三层标准（简短路由文件、任务技能、规格文档）靠拢的最小有效改动。
- **怎么用：** 问“评审 / 打分我们的 agent 指令”或“统一各仓库的 agent 上下文规范”。要生成 AGENTS.md 文件时，它会交给 `agentsmd-scaffold`。
- **最适合：** 检查一个仓库是否方便编程 agent 工作。

<a id="s-review-agent-harness"></a>
### review-agent-harness

[review-agent-harness.zip](review-agent-harness.zip) · 入口：`spellbook-main/skills/review-agent-harness/SKILL.md`

- **能做什么：** 评估一个仓库的编程 agent 支撑体系——规则、技能、钩子、记忆、验证和恢复循环——能否可靠地把工作从意图推进到受控执行、验证、交付和学习。三次相互隔离的取证，再合并结论；模式：静态（默认）、情节（加上授权的会话日志）和纵向（与台账对比）。
- **怎么用：** 问“这个仓库适合 agent 工作吗？”“为什么 agent 在这里老是失败？”或“修复支撑体系后有没有改善？”。不用于只看代码或只看 AGENTS.md 的审计。
- **最适合：** 诊断仓库中系统性的 agent 失败。

<a id="s-review-gate"></a>
### review-gate

[review-gate.zip](review-gate.zip) · 入口：`spellbook-main/skills/review-gate/SKILL.md`

- **能做什么：** agent 生成的改动在提交、推送、开 PR、合并或应用到你的文件之前的最后一道安全检查：生成简洁的评审包（风险和验证情况），并阻止落地，直到人明确批准（或批准但要求修改）。
- **怎么用：** 用“review gate”“落地前先批准”“先看 diff 再落地”触发，或让它在提交/推送/PR 之前自动运行。模板在 `assets/review-pack-template.md`。
- **最适合：** 让人始终参与 agent 做出的改动。

<a id="s-sol-luna-router"></a>
### sol-luna-router

[sol-luna-router.zip](sol-luna-router.zip) · 入口：`spellbook-main/skills/sol-luna-router/SKILL.md`

- **能做什么：** 把较大的编程或仓库评审工作交给两阶段流程：“Sol”（当前 agent）作为指挥和验证者，另一个“Luna Max”命令行 worker 通过自带的运行器完成一项有边界的实现或调查，之后由 Sol 评审并要求修正。也可以只读查看路由器的配置和效率。
- **怎么用：** 只有你明确要求 Sol 指挥 Luna，或明确要求使用这个路由器时才用；小任务留在主 agent 里。需要 Luna 命令行工具和自带脚本。
- **最适合：** 可审计的“委派 + 验证”式编程，配合独立的 worker agent。

<a id="s-threads"></a>
### threads

[threads.zip](threads.zip) · 入口：`spellbook-main/skills/threads/SKILL.md`

- **能做什么：** Codex 原生编排：把一个大请求或 GitHub issue/PR 队列拆成受控的并行子线程，带明确的分道、文件归属、worktree、按依赖派发、验证预算、评审与合并关卡、运行日志和收尾审计。没有原生子 agent 能力时，退化为输出提示词包。
- **怎么用：** 只有你明确要求时才用，例如 `$threads`、“开几个子 agent”或“并行处理这个 issue 队列”。仅适用于 Codex 运行环境。
- **最适合：** 在 Codex 中安全地并行处理一批 issue 或 PR。

<a id="s-vibeguard"></a>
### vibeguard

[vibeguard.zip](vibeguard.zip) · 入口：`spellbook-main/skills/vibeguard/SKILL.md`

- **能做什么：** 针对三个时刻的轻量防幻觉护栏：开工前的任务契约清单、按证据给评审发现排序的打分矩阵，以及每周回归复盘模板。不安装钩子，也不运行脚本。
- **怎么用：** 要求“护栏”“任务契约”“给这些发现打风险分”或“做一次回归复盘”。
- **最适合：** 不依赖重型工具，让 AI 辅助的工作保持范围清楚、实事求是。

<a id="cat-skills"></a>
## 构建与管理技能

创建、审计、修复、归档和统计技能——也可用来维护本仓库。

| 技能 | 最适合 |
|---|---|
| [`capability-distill`](#s-capability-distill) | 在丢失之前，保存强模型或某次会话中来之不易的决策规则。 |
| [`self-evolution`](#s-self-evolution) | 修复表现不佳或臃肿的技能，同时不丢掉原本好用的部分。 |
| [`skill-archive-manager`](#s-skill-archive-manager) | 让一个大型个人技能库（比如本仓库）有版本、可审计。 |
| [`skill-audit`](#s-skill-audit) | 决定要做哪些技能以及它们如何配合。 |
| [`skill-creator`](#s-skill-creator) | 有测试、可量化改进地正确构建技能。 |
| [`skill-ecosystem-doctor`](#s-skill-ecosystem-doctor) | 理清同一批技能在多个 agent 和范围里的安装情况。 |
| [`skill-lifeguard`](#s-skill-lifeguard) | 必须稳定发挥的高价值工作流技能。 |
| [`skill-recaster`](#s-skill-recaster) | 把提示词和 SOP 转成干净的技能。 |
| [`skill-reforge-foundry`](#s-skill-reforge-foundry) | 把你刚做完的工作流保存下来，以后不必再重复同样的纠正。 |
| [`skill-usage-stats`](#s-skill-usage-stats) | 找出技能库里的“死重”。 |

<a id="s-capability-distill"></a>
### capability-distill

[capability-distill.zip](capability-distill.zip) · 入口：`spellbook-main/skills/capability-distill/SKILL.md`

- **能做什么：** 从经批准的强模型访谈或真实任务记录中提取不明显的判断规则（“为什么在两个合理选项中选 A 而不是 B”），打包成可审计的“judgment packet”——之后由 `skill-audit` 和 `skill-creator` 把它变成技能。
- **怎么用：** 说“蒸馏这个模型的判断力”“把这次任务的关键决策固化下来”或“模型窗口要关了，保留它在这类场景的判断”。它只读取你批准的材料。不用于直接写 SKILL.md 或泛泛的最佳实践。
- **最适合：** 在丢失之前，保存强模型或某次会话中来之不易的决策规则。

<a id="s-self-evolution"></a>
### self-evolution

[self-evolution.zip](self-evolution.zip) · 入口：`self-evolution/SKILL.md`

- **能做什么：** “自我进化”——审计、诊断、改进、精简、重建、清理和验证 agent 技能（SKILL.md 包）：锁定原始意图，扫描整个包，诊断根本原因，在局部修补、结构修复和完全重建之间选择，在声称改进之前先验证行为，并准备干净的对外发布版本。
- **怎么用：** 指定一个技能，说“审计这个技能”“它的输出为什么很弱？”“精简它”或“让它可以安全分享”。
- **最适合：** 修复表现不佳或臃肿的技能，同时不丢掉原本好用的部分。

<a id="s-skill-archive-manager"></a>
### skill-archive-manager

[skill-archive-manager.zip](skill-archive-manager.zip) · 入口：`archive-center-suite/skill-archive-manager/SKILL.md`

- **能做什么：** 用户级技能集合的治理中枢：发现技能、登记进归集中心、管理版本和发布状态、维护索引和哈希、审计完整性、裁决冲突、跟踪问题直到闭环、刷新管理页面，并把整个归集中心打包迁移到另一台电脑。五阶段流水线：归集 → 校验 → 冲突处理 → 刷新 → 随迁。
- **怎么用：** 说“把这些技能归档 / 登记”“审计技能归档”“处理这个版本冲突”“刷新管理页”或“做一个迁移包”。用 `install.py` 安装。它位于 `archive-center-suite/` 中，依赖该套件的内部工具。
- **最适合：** 让一个大型个人技能库（比如本仓库）有版本、可审计。

<a id="s-skill-audit"></a>
### skill-audit

[skill-audit.zip](skill-audit.zip) · 入口：`spellbook-main/skills/skill-audit/SKILL.md`

- **能做什么：** 基于 Anthropic 文章《Lessons from building Claude Code: How we use skills》（2026 年 6 月）的战略层面技能设计与评审：判断一个工作流是否值得做成技能，给它分类，起草技能简报，设计渐进式披露和运行细节，规划技能库结构、分发和使用度量，然后交给 `skill-creator`。
- **怎么用：** 问“这个该做成技能吗？”“评审这个技能”“规划我们的技能库”或“帮我写一个更好的触发描述”。
- **最适合：** 决定要做哪些技能以及它们如何配合。

<a id="s-skill-creator"></a>
### skill-creator

[skill-creator.zip](skill-creator.zip) · 入口：`spellbook-main/skills/skill-creator/SKILL.md`

- **能做什么：** 创建新技能并迭代改进已有技能：明确意图、访谈、编写 SKILL.md、在有/无技能两种情况下运行测试提示词、在评测查看器中打分和汇总结果、迭代改进、支持盲测对比，并优化描述以提高触发准确率。
- **怎么用：** 说“为 X 创建一个技能”“改进这个技能”“给我的技能跑评测”或“优化技能描述”。评测脚本需要安装 `requirements.txt`。
- **最适合：** 有测试、可量化改进地正确构建技能。

<a id="s-skill-ecosystem-doctor"></a>
### skill-ecosystem-doctor

[skill-ecosystem-doctor.zip](skill-ecosystem-doctor.zip) · 入口：`spellbook-main/skills/skill-ecosystem-doctor/SKILL.md`

- **能做什么：** 审计并安全修复跨运行时的技能治理：哪个副本是正本、不同工具之间分叉或重复的投影、暴露范围和预算、生命周期漂移、隔离和退役。确定性审计 → 分类结论 → 修复计划 → 只执行已批准的修复 → 跨运行时验证。从不无人值守运行。
- **怎么用：** 明确要求跨运行时或跨范围的技能治理时使用（“我的技能在 Claude Code 和 Codex 里不一样”“哪个副本才是正本？”）。看使用统计用 `skill-usage-stats`。
- **最适合：** 理清同一批技能在多个 agent 和范围里的安装情况。

<a id="s-skill-lifeguard"></a>
### skill-lifeguard

[skill-lifeguard.zip](skill-lifeguard.zip) · 入口：`spellbook-main/skills/skill-lifeguard/SKILL.md`

- **能做什么：** 通过加上“可靠技能契约”让脆弱或漂移的技能变可靠：明确的反面示例、验证检查点、机器可检查的完成条件、回放或冒烟测试钩子以及漂移信号——并把失败日志转成技能补丁。
- **怎么用：** 说“这个技能老是失败”“让这个技能更可靠”或“把这份失败日志变成技能补丁”。契约模板在 `assets/` 里。
- **最适合：** 必须稳定发挥的高价值工作流技能。

<a id="s-skill-recaster"></a>
### skill-recaster

[skill-recaster.zip](skill-recaster.zip) · 入口：`skill-recaster-v1.0.0/SKILL.md`

- **能做什么：** 把重复任务、旧提示词、SOP 或失控的技能重构成边界清楚、可安装、可维护的 agent 技能：任务契约 → 决策地图（该触发/不该触发、冲突、停止条件）→ 行为路径 → 刚好够用的文件结构 → 场景攻防（正常、缺失、模糊、近邻、冲突、压力），并如实标注成熟度。
- **怎么用：** 说“把这个提示词 / SOP 做成技能”“修复我的 SKILL.md”或“设计触发边界”。入口会自动识别：从零成型、旧稿重铸或修复既有技能。
- **最适合：** 把提示词和 SOP 转成干净的技能。

<a id="s-skill-reforge-foundry"></a>
### skill-reforge-foundry

[skill-reforge-foundry.zip](skill-reforge-foundry.zip) · 入口：`skill-reforge-foundry-v5.1.0/SKILL.md` · `skill-reforge-foundry/SKILL.md`

- **能做什么：** 从目标、粗糙的提示词、SOP、已有技能、失败报告——或你刚在对话中展示的经验（“把刚才的经验做成 skill”）——构建、重建、测试并打包可复用的 agent 技能。适合新手的七步流程，可以生成一小组技能，编写真实的测试用例并产出发布用的 ZIP。压缩包里有 v5.1.0（英文，侧重构建）和更新的中文版（侧重从对话中萃取技能）。
- **怎么用：** 说“把刚才的经验做成 skill”“turn this chat into a skill”“帮我做 / 升级 / 修补一个 skill”，或提供旧技能或失败报告。
- **最适合：** 把你刚做完的工作流保存下来，以后不必再重复同样的纠正。

<a id="s-skill-usage-stats"></a>
### skill-usage-stats

[skill-usage-stats.zip](skill-usage-stats.zip) · 入口：`spellbook-main/skills/skill-usage-stats/SKILL.md`

- **能做什么：** 两个只读扫描器：`agent_health.py` 检查可在本地验证的 Claude Code 和 Codex 配置健康状况，`skill_usage_report.py` 报告技能调用证据和低使用候选（包括已启用的插件）。报告支持中文或英文。
- **怎么用：** 要求“agent 健康检查”“技能使用排行”或“哪些技能我从来没用过？”。治理和修复用 `skill-ecosystem-doctor`。
- **最适合：** 找出技能库里的“死重”。

<a id="cat-ai-infra"></a>
## 本地模型、GPU 与 API 网关

运行本地模型、查看 GPU 服务器和 API 计费。

| 技能 | 最适合 |
|---|---|
| [`cliproxy-newapi-stack`](#s-cliproxy-newapi-stack) | 给自建的 CLIProxyAPI 部署加上计费和分用户令牌。 |
| [`gemma4-local-deploy`](#s-gemma4-local-deploy) | 在 Mac 上运行本地 Gemma 4 模型服务。 |
| [`gpu-use`](#s-gpu-use) | 快速查看共享服务器上“谁在用哪张卡”。 |

<a id="s-cliproxy-newapi-stack"></a>
### cliproxy-newapi-stack

[cliproxy-newapi-stack.zip](cliproxy-newapi-stack.zip) · 入口：`spellbook-main/skills/cliproxy-newapi-stack/SKILL.md`

- **能做什么：** 在已验证可用的 CLIProxyAPI 上游之前部署 NewAPI（`calciumion/new-api`）计费、限流和多用户令牌层，把 Codex/Claude/Gemini/Qwen 订阅账号包装成可计费的 OpenAI 兼容 API。涵盖 Docker 部署、容器到宿主机桥接（172.17.0.1）、模型计费倍率、额度修正、OAuth 凭据热加载和双路径验证。
- **怎么用：** 提供 SSH 目标（如 `root@1.2.3.4`）和端口。“给现有 cliproxy 加 NewAPI”“NewAPI 价格不对”等说法会触发。它不负责安装裸 CLIProxyAPI，在安装容器或修改生产额度前会先征求同意。
- **最适合：** 给自建的 CLIProxyAPI 部署加上计费和分用户令牌。

<a id="s-gemma4-local-deploy"></a>
### gemma4-local-deploy

[gemma4-local-deploy.zip](gemma4-local-deploy.zip) · 入口：`spellbook-main/skills/gemma4-local-deploy/SKILL.md`

- **能做什么：** 在 Mac / Apple Silicon 本地部署 Gemma 4 12B：安装或升级 llama.cpp，下载 GGUF 量化模型，用 `llama-server`（或 Ollama）提供 OpenAI 兼容 API，在 tmux 中后台运行并只监听 127.0.0.1，验证健康检查、问答、资源占用和常见故障。预设：默认 Q4_K_M、64K/128K 长上下文、QAT Q4_0 @ 256K、左右对比演示。
- **怎么用：** 说“本地部署 Gemma 4”，可指定量化、端口和是否后台运行。默认：`ggml-org/gemma-4-12B-it-GGUF`、Q4_K_M、`http://127.0.0.1:8080`、32K 上下文。
- **最适合：** 在 Mac 上运行本地 Gemma 4 模型服务。

<a id="s-gpu-use"></a>
### gpu-use

[gpu-use.zip](gpu-use.zip) · 入口：`spellbook-main/skills/gpu-use/SKILL.md`

- **能做什么：** 通过 SSH 查看远程服务器的 GPU 使用情况：每张卡的显存和利用率、正在运行的进程及其所属 Docker 容器、单容器多实例服务和空闲资源，并给每张卡标注状态。
- **怎么用：** 带参数 `user@host -p port` 运行，或不带参数使用默认服务器——注意 SKILL.md 里写死的是原作者的服务器，使用前要改成你自己的。说“查看 GPU 使用”或“显存占用”。
- **最适合：** 快速查看共享服务器上“谁在用哪张卡”。

<a id="cat-network"></a>
## 网络与代理排障

Clash / mihomo、IP 质量、断线重连、网络调优和远程桌面。

| 技能 | 最适合 |
|---|---|
| [`clash-doctor`](#s-clash-doctor) | 修复和管理 Clash Verge 代理配置，尤其是 AI 工具的分流。 |
| [`clash-routes`](#s-clash-routes) | 快速回答“这个应用到底走的是哪个代理？”。 |
| [`ip-check`](#s-ip-check) | 在用于 AI 服务之前先验收代理或 VPS 的 IP。 |
| [`network-reconnect-repair`](#s-network-reconnect-repair) | “一直在重连”的问题，尤其是代理后面的 AI 工具。 |
| [`optimize-network`](#s-optimize-network) | 在 Mac 上基于证据调优网络，又不破坏你的代理配置。 |
| [`rustdesk-doctor`](#s-rustdesk-doctor) | 运行 Clash Verge 的电脑上的 RustDesk 问题。 |

<a id="s-clash-doctor"></a>
### clash-doctor

[clash-doctor.zip](clash-doctor.zip) · 入口：`spellbook-main/skills/clash-doctor/SKILL.md`

- **能做什么：** Clash Verge / mihomo 的诊断与配置管理：代理失败、AI 工具分流、本地 Hub 拓扑、多机对齐、TUN 绕过、克隆或切换订阅，以及同步后配置未生效。诊断和对齐是只读的；写入前需要你确认。
- **怎么用：** 参数包括 `status`、`profiles`、`hub`、`align`、`roles`、`switch-check <name>`、`clone <src> <dst>`、`setup-ai <name>`、`switch <name>`、`bypass <IP>`。看单个进程的线路用 `clash-routes`；查出口 IP 质量用 `ip-check`。
- **最适合：** 修复和管理 Clash Verge 代理配置，尤其是 AI 工具的分流。

<a id="s-clash-routes"></a>
### clash-routes

[clash-routes.zip](clash-routes.zip) · 入口：`spellbook-main/skills/clash-routes/SKILL.md`

- **能做什么：** 只读查看本机每个进程当前走的是哪条 mihomo 代理链（规则 → 策略组 → 真实出口）——例如 Claude、Codex、Gemini、ChatGPT 或浏览器是否走了预期的代理。
- **怎么用：** 可带一个进程名参数（默认显示所有活跃连接）。读取 Clash Verge 控制接口时不会打印密钥。修改配置交给 `clash-doctor`。
- **最适合：** 快速回答“这个应用到底走的是哪个代理？”。

<a id="s-ip-check"></a>
### ip-check

[ip-check.zip](ip-check.zip) · 入口：`spellbook-main/skills/ip-check/SKILL.md`

- **能做什么：** 检测 IP 或住宅/机房代理节点的质量：注册库与地理库是否一致、ASN/机构、信誉和黑名单、住宅真实性、BGP 宣告、Grok/Claude/ChatGPT 解锁情况以及延迟三角定位——识破“物理在一个国家、纸面在另一个国家”的 IP（会导致区域锁）。只读。
- **怎么用：** 说“查这个 IP”，或给出 SOCKS5 代理凭证；它会运行 `ipcheck.py` 并给出评分卡。切换节点交给 `clash-doctor`。
- **最适合：** 在用于 AI 服务之前先验收代理或 VPS 的 IP。

<a id="s-network-reconnect-repair"></a>
### network-reconnect-repair

[network-reconnect-repair.zip](network-reconnect-repair.zip) · 入口：`network-reconnect-repair/SKILL.md`

- **能做什么：** 诊断并修复 Windows、macOS 和 Linux 上反复重连、间歇断网、DNS 失败、流式响应失败或某个应用连不上的问题——包括 Codex 网络错误。先定位真正的断点（链路、应用、长连接、VPN/TUN 切换、解析器），再做最小修复，而不是一键重置。
- **怎么用：** 描述受影响的应用和设备、系统、接入方式、VPN/代理状态以及何时开始出问题；它会先直接检查能检查的，只询问缺少的关键信息。
- **最适合：** “一直在重连”的问题，尤其是代理后面的 AI 工具。

<a id="s-optimize-network"></a>
### optimize-network

[optimize-network.zip](optimize-network.zip) · 入口：`spellbook-main/skills/optimize-network/SKILL.md`

- **能做什么：** 安全地诊断并改善本机网络速度、延迟、抖动、DNS、Wi-Fi/有线、macOS 网络服务和缓冲膨胀：先做只读基线，再做小的可回退实验，并验证前后效果。明确保护 Clash Verge、Mihomo、Shadowrocket、Tailscale、V2Ray、Surge 和公司 VPN。
- **怎么用：** 参数：`diagnose`、`optimize`、`report`，可加目标域名。或者说“让我的网络更快”“Wi-Fi 为什么慢？”“Codex 一直卡”。
- **最适合：** 在 Mac 上基于证据调优网络，又不破坏你的代理配置。

<a id="s-rustdesk-doctor"></a>
### rustdesk-doctor

[rustdesk-doctor.zip](rustdesk-doctor.zip) · 入口：`spellbook-main/skills/rustdesk-doctor/SKILL.md`

- **能做什么：** 诊断 RustDesk 连接问题——连不上、ID 不显示、注册失败——依次检查客户端进程、配置和日志，Clash/Mihomo 干扰（fake-IP DNS、TUN 路由），网络连通性，自建服务器（能 SSH 时）以及本机 IP 误判问题。
- **怎么用：** 可带自建服务器 IP 参数运行，说“RustDesk 连不上”。它会按顺序执行各步骤并给出综合诊断。
- **最适合：** 运行 Clash Verge 的电脑上的 RustDesk 问题。

<a id="cat-system"></a>
## 电脑与编辑器维护

磁盘清理、电脑卡顿诊断和编辑器性能。

| 技能 | 最适合 |
|---|---|
| [`disk-cleaner`](#s-disk-cleaner) | 在开发机上回收 `node_modules`、`target`、缓存和旧安装包占用的空间。 |
| [`storage-gc-guardian`](#s-storage-gc-guardian) | 空间不足时安全、可回退的清理。 |
| [`system-doctor`](#s-system-doctor) | 快速找出是什么拖慢了你的 Mac。 |
| [`vscode-doctor`](#s-vscode-doctor) | 找到编辑器变慢的真正原因。 |

<a id="s-disk-cleaner"></a>
### disk-cleaner

[disk-cleaner.zip](disk-cleaner.zip) · 入口：`spellbook-main/skills/disk-cleaner/SKILL.md`

- **能做什么：** 扫描磁盘占用，找出可以安全删除的缓存、编译产物和安装包，然后用编号菜单（高价值 / 中等 / 仅供参考）交互式释放空间并验证结果。会发现真实的项目根目录，而不是假定固定的文件夹名。
- **怎么用：** 可带一个路径参数（默认主目录），例如“清理我的磁盘”或 `disk-cleaner ~/code`。只删除你选中的项目。
- **最适合：** 在开发机上回收 `node_modules`、`target`、缓存和旧安装包占用的空间。

<a id="s-storage-gc-guardian"></a>
### storage-gc-guardian

[storage-gc-guardian.zip](storage-gc-guardian.zip) · 入口：`storage-gc-guardian/SKILL.md`

- **能做什么：** 事务式的磁盘清理：审计过期临时文件、可重建的包缓存和诊断残留，建立有证据依据的计划，先把项目移到可恢复的隔离区，只有你明确提交时才永久删除。把未知数据视为“不是垃圾”，绝不凭推断去动项目、下载文件夹、个人媒体、应用数据或 Codex 状态。基于标准库的 Python 引擎。
- **怎么用：** 说“释放磁盘空间”或“清理缓存”。它会先给出计划；在提交之前都可以恢复。
- **最适合：** 空间不足时安全、可回退的清理。

<a id="s-system-doctor"></a>
### system-doctor

[system-doctor.zip](system-doctor.zip) · 入口：`spellbook-main/skills/system-doctor/SKILL.md`

- **能做什么：** 诊断电脑卡顿：负载与运行时间、内存压力、Swap、CPU 和内存前 20 名、按应用分组（例如把所有 Chrome 渲染进程合并统计）、僵尸进程和异常，然后给出结构化报告、建议和可选的交互操作。
- **怎么用：** 说“电脑好卡”“什么在占我的 CPU / 内存？”。无需参数。命令针对 macOS。
- **最适合：** 快速找出是什么拖慢了你的 Mac。

<a id="s-vscode-doctor"></a>
### vscode-doctor

[vscode-doctor.zip](vscode-doctor.zip) · 入口：`spellbook-main/skills/vscode-doctor/SKILL.md`

- **能做什么：** 以证据为先诊断 VS Code 类编辑器（VS Code、Cursor 等）变慢或卡死：打字延迟、界面冻结、扩展宿主卡住、文件监听噪音、CPU/内存占用高，或把编辑器当作大文件夹的文件浏览器。不写死路径、不预设扩展黑名单或根因；按本次采集的证据排序，并验证前后效果。
- **怎么用：** 说“VS Code / Cursor 很卡”，可附工作区根目录。从简单的只读模式开始。
- **最适合：** 找到编辑器变慢的真正原因。

<a id="cat-productivity"></a>
## 效率、知识库与报告

知识库、聊天日报、周报和小型业务系统。

| 技能 | 最适合 |
|---|---|
| [`feishu-rent-billing`](#s-feishu-rent-billing) | 在飞书里分摊水电和收租的小房东。 |
| [`library-steward`](#s-library-steward) | 把一文件夹的参考资料变成可检索、有版本的资料库。 |
| [`wechat-group-daily-digest`](#s-wechat-group-daily-digest) | 快速补上热闹微信群的聊天内容。 |
| [`weekly`](#s-weekly) | 根据提交和 agent 会话自动起草每周工作报告。 |

<a id="s-feishu-rent-billing"></a>
### feishu-rent-billing

[feishu-rent-billing.zip](feishu-rent-billing.zip) · 入口：`feishu-rent-billing/SKILL.md` · `feishu-rent-billing/deployment/chg-001/backup/local/SKILL.md`

- **能做什么：** 在飞书多维表格里搭建上下两层出租屋的收租计费系统：抄表登记（总表 + 上层表，下层 = 总 − 上层）、租约、公摊、计费批次和费用明细；处理月中入住/退租折算、空置费由房东承担、公摊“暂按 0”与“确认为 0”的区别、防重复计费和纯文字账单报告。附带离线核算器用于对账，以及锁定的规则集（R1–R12）。
- **怎么用：** 三种模式：搭建（配置表、字段、公式、表单、工作流）、核算/出报告（提供读数和入住情况，得到账单）、排错（找出飞书算出的数不对的原因）。使用根目录的 `feishu-rent-billing/SKILL.md`；`deployment/chg-001/backup/` 下的是旧备份。不适用于多户公寓、商业物业、税务或合同。
- **最适合：** 在飞书里分摊水电和收租的小房东。

<a id="s-library-steward"></a>
### library-steward

[library-steward.zip](library-steward.zip) · 入口：`library-steward/SKILL.md`

- **能做什么：** 接入并管理本地知识库、资料库、风格库、素材库或相册：先摸清全貌、和你商量用法，然后负责检索、精确定位（行号或页码）、整组取出使用、入库、来源登记、快照、回滚和校验。一个只依赖标准库的 Python 脚本，基于 SQLite 全文检索（中文可直接搜）。
- **怎么用：** 指定库的根目录（`--root` 或 `STEWARD_ROOT`），然后说“帮我找……”“在哪一页……”“把这个入库”“做快照 / 回滚”。可选安装 `pypdf opencc-python-reimplemented` 以支持 PDF 正文和繁简互通检索。
- **最适合：** 把一文件夹的参考资料变成可检索、有版本的资料库。

<a id="s-wechat-group-daily-digest"></a>
### wechat-group-daily-digest

[wechat-group-daily-digest.zip](wechat-group-daily-digest.zip) · 入口：`wechat-group-daily-digest/SKILL.md`

- **能做什么：** “月兔爬楼”——把你有权读取的微信群聊整理成可核验的 AI 日报：只读，先做证据包，再总结，最后才推进“上次读到哪里”的标记，方便你从上次继续。隐私模式可保留昵称，或替换成成员 A/B/C。
- **怎么用：** 输入方式：JSON/JSONL 导出（`--input`）、经授权的 Windows 离线快照（`--snapshot`），或通过单独安装的 `yichen-wechat-local-vault` 读取 Mac 本地微信。先运行 `doctor`，再运行 `prepare`。说“爬楼”“群聊日报”或“从上次继续”。
- **最适合：** 快速补上热闹微信群的聊天内容。

<a id="s-weekly"></a>
### weekly

[weekly.zip](weekly.zip) · 入口：`spellbook-main/skills/weekly.SKILL.md`

- **能做什么：** 为指定日期范围生成周报，整合 Git 提交、Claude Code 会话、Codex 会话和可选的本机记忆记录，并分类为重构、新功能、修复、调研和其他。注意：它写死了某个项目（“om-generator”的前端和后端仓库）。
- **怎么用：** 带日期范围运行，如 `2-1到2-7`（默认本周一到今天）。要用于自己的项目，请修改 `weekly.SKILL.md` 里的仓库名和路径。
- **最适合：** 根据提交和 agent 会话自动起草每周工作报告。

<a id="cat-learning"></a>
## 学习与辅导

系统课程和一对一辅导。

| 技能 | 最适合 |
|---|---|
| [`ai-visual-generation-foundation-course`](#s-ai-visual-generation-foundation-course) | 想学真本事而不是背“神词”的完全新手。 |
| [`feynman-learning-coach`](#s-feynman-learning-coach) | 真正学会一个主题或一份资料，而不是走马观花。 |

<a id="s-ai-visual-generation-foundation-course"></a>
### ai-visual-generation-foundation-course

[ai-visual-generation-foundation-course.zip](ai-visual-generation-foundation-course.zip) · 入口：`ai-image-foundation-course-skill-v1.0.0/SKILL.md`

- **能做什么：** 一套系统的 AI 生图零基础课程（从 L0 视觉识别到 L4 项目交付）。教的是“观察 → 控制 → 生成 → 诊断 → 修正”，每次只教一个新概念，配有课程、练习、作业和批改。跨模型通用。
- **怎么用：** 说“从零教我 AI 生图”“下一课”“帮我批改作业图”，或选择模式：小白模式（默认）、教师模式、诊断模式、速成模式、作业批改模式。课程地图和练习册都在包里。
- **最适合：** 想学真本事而不是背“神词”的完全新手。

<a id="s-feynman-learning-coach"></a>
### feynman-learning-coach

[feynman-learning-coach.zip](feynman-learning-coach.zip) · 入口：`feynman-learning-coach/SKILL.md`

- **能做什么：** 一对一费曼学习教练：根据你的目标、基础、每天可用时间和截止日期制定个人计划，然后循环“先讲懂 → 让你讲给它听 → 追问找漏洞 → 补洞 → 用起来 → 间隔复习”。“学习接力卡”让你可以跨会话接着学。
- **怎么用：** 说“我想学 Python，零基础，每天 30 分钟”“帮我学懂这份讲义的第三章”“考考我复利”或“继续学”（把接力卡发回去）。不替你写作业或考试答案。
- **最适合：** 真正学会一个主题或一份资料，而不是走马观花。

<a id="cat-lifestyle"></a>
## 家居、旅行与生活

室内设计、旅行规划和术数工具。

| 技能 | 最适合 |
|---|---|
| [`home-design-director`](#s-home-design-director) | 装修规划、布局探索和风格切换。 |
| [`trip-planner`](#s-trip-planner) | 实用、拿来就能照着走的旅行计划。 |
| [`xuanshu-agent`](#s-xuanshu-agent) | 由工具精确计算的术数和占星排盘与报告。 |

<a id="s-home-design-director"></a>
### home-design-director

[home-design-director.zip](home-design-director.zip) · 入口：`home-design-director/SKILL.md`

- **能做什么：** 面向新手的室内设计：把户型图、房间照片和大白话需求变成基于几何的房间模型（Room Model）、2–3 套布局方向、逐个房间的设计决定和锁定几何的效果图简报（风格可以装饰，但绝不挪动墙、门、窗）。不知道的尺寸就保持未知。
- **怎么用：** 先上传户型图或开发商给的户型截图（有尺寸最好），然后每次最多回答三个关键问题。没有户型图也能给概念建议，但不能当施工尺寸。
- **最适合：** 装修规划、布局探索和风格切换。

<a id="s-trip-planner"></a>
### trip-planner

[trip-planner.zip](trip-planner.zip) · 入口：`spellbook-main/skills/trip-planner/SKILL.md`

- **能做什么：** 详细的旅行行程：行程概览，每天上午/下午/晚上的安排和主题，地址、营业时间、预订链接、时长、交通时间、“今晚准备”提示，以及速查区（已预订项目、需离线下载的内容、当地好去处），节奏安排切合实际。
- **怎么用：** 提供目的地、日期、同行人、兴趣、预算和节奏，要求做行程。
- **最适合：** 实用、拿来就能照着走的旅行计划。

<a id="s-xuanshu-agent"></a>
### xuanshu-agent

[xuanshu-agent.zip](xuanshu-agent.zip) · 入口：`xuanshu-skill-2.0.0/.agents/skills/xuanshu-agent/SKILL.md` · `xuanshu-skill-2.0.0/skills/xuanshu-agent/SKILL.md`

- **能做什么：** “玄枢”的 agent 使用指南。玄枢是一个本地术数引擎，包含 110 种技法：西方占星（本命、回归、推运、主限、卜卦、择日、生时校正、AstroCartoGraphy）、八字、紫微斗数、大六壬、奇门遁甲、太乙、六爻、梅花易数、塔罗、天文地占、老黄历等。核心规则：绝不手算——每个盘都必须在确认出生时间、地点、时区等设置后，由玄枢 MCP 工具或命令行算出。压缩包里是完整的 xuanshu-skill 2.0.0 仓库（AGPL-3.0）。
- **怎么用：** 安装本地服务（Python 3.12 + `uv` + 离线运行时），并注册为 MCP 服务器，例如 `uv run --directory <repo>/xuanshu-skill xuanshu-skill client config --format codex`（见仓库 README）。然后说“排盘”“起卦”“看我的本命盘”。新手从 `xuanshu_beginner_guide` → `xuanshu_full_reading` 开始。
- **最适合：** 由工具精确计算的术数和占星排盘与报告。
