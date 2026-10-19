# Skill Home

A personal library of **212 agent skills**, one skill per `.zip`. This page is the catalog: for every skill it says **what it does**, **how to use it**, and **what it's best suited for**, grouped by area so you can find the right one quickly.

- `00_212项压缩包清单.csv` — the original manifest (skill name, zip, type, file count, entry file, SHA-256).
- `00_使用说明.txt` — the original packaging note.
- Inside every zip, `00_入口说明.txt` names the entry file(s) for that skill.

## Contents

- [Quick finder: "I want to…"](#quick-finder)
- [How to install a skill](#how-to-install)
- [Packaging notes and caveats](#packaging-notes)
- [Catalog by category](#catalog)
  - [AI video, film & storyboards](#cat-video) (24)
  - [Screenwriting & storytelling](#cat-story) (14)
  - [AI image & photography](#cat-image) (23)
  - [Visual style analysis & reverse prompting](#cat-aesthetics) (7)
  - [3D & product rendering](#cat-image3d) (2)
  - [Ads, product demos & slides](#cat-marketing) (4)
  - [Social media & creator operations](#cat-social) (4)
  - [Writing, author voice & de-AI polish](#cat-writing) (4)
  - [Research, search & intelligence](#cat-research) (12)
  - [Ideas, product management & strategy](#cat-product) (13)
  - [Frontend, UI & design systems](#cat-frontend) (15)
  - [Architecture, backend & data](#cat-backend) (10)
  - [Language & project starters](#cat-languages) (7)
  - [Testing, debugging & code quality](#cat-testing) (7)
  - [DevOps, release & reliability](#cat-devops) (5)
  - [Security](#cat-security) (4)
  - [Git & open-source contribution](#cat-git) (5)
  - [Coding agents: Claude Code, Codex & multi-agent work](#cat-agents) (20)
  - [Building & managing skills](#cat-skills) (10)
  - [Local models, GPUs & API gateways](#cat-ai-infra) (3)
  - [Network & proxy troubleshooting](#cat-network) (6)
  - [Computer & editor maintenance](#cat-system) (4)
  - [Productivity, knowledge & reports](#cat-productivity) (4)
  - [Learning & tutoring](#cat-learning) (2)
  - [Home, travel & lifestyle](#cat-lifestyle) (3)

<a id="quick-finder"></a>
## Quick finder: "I want to…"

| I want to… | Start with |
|---|---|
| Write a Seedance prompt for a shot or scene | [`seedance-clean`](#s-seedance-clean), [`Mx-Shell_Prompts`](#s-mx-shell-prompts), [`cinematic-fight-director`](#s-cinematic-fight-director) |
| Turn a script into storyboards and video prompts | [`storyboard-forge-20-25`](#s-storyboard-forge-20-25), [`script-scene-visual-storyboard`](#s-script-scene-visual-storyboard), [`mr-li-seedance-25`](#s-mr-li-seedance-25), [`分镜设计大师阶段1：导演设计器`](#s-zh-a4f0e6a7) |
| Remake a reference video with my own characters | [`scenerelay-reverse`](#s-scenerelay-reverse), [`motionprint-reverse`](#s-motionprint-reverse) |
| Produce a whole AI short or motion comic from an idea | [`motion-drama-foundry`](#s-motion-drama-foundry), [`short-drama-producer`](#s-short-drama-producer), [`解说漫制片教练`](#s-zh-8927f55c) |
| Check continuity between shots | [`jingqiao-continuity-supervisor`](#s-jingqiao-continuity-supervisor), [`AI视频空间调度导演`](#s-zh-b603f88d) |
| Edit real video files (cuts, captions, clips) | [`video-studio`](#s-video-studio), [`talking-head-fx-packager`](#s-talking-head-fx-packager), [`agentic-video-director`](#s-agentic-video-director) |
| Write a film or short-drama script | [`screenplay-factory`](#s-screenplay-factory), [`hollywood-omni-screenplay-master`](#s-hollywood-omni-screenplay-master), [`mass-appeal-super-screenwriter`](#s-mass-appeal-super-screenwriter), [`微短剧剧本创作`](#s-zh-b6e6af54) |
| Continue a novel or story in the original voice | [`author-style-continuation`](#s-author-style-continuation), [`story-forge-engine`](#s-story-forge-engine), [`story-dynamics-workbench`](#s-story-dynamics-workbench) |
| Keep a character, outfit or product consistent across images | [`asset-continuity-imagegen`](#s-asset-continuity-imagegen), [`public-character-continuity`](#s-public-character-continuity), [`threadlock-wardrobe-skill-v1.0.0`](#s-threadlock-wardrobe-skill-v1-0-0) |
| Retouch, repair or upscale an image | [`portrait-retouch`](#s-portrait-retouch), [`realistic-social-selfie-retouch`](#s-realistic-social-selfie-retouch), [`pic-fix-oneshot`](#s-pic-fix-oneshot), [`fidelity-4k-upscale-skill-v1.0`](#s-fidelity-4k-upscale-skill-v1-0) |
| Turn a reference image into a prompt or borrow its style | [`strong-image-reverse-prompt`](#s-strong-image-reverse-prompt), [`reference-rendering-reader`](#s-reference-rendering-reader), [`photographic-atmosphere-reconstruction`](#s-photographic-atmosphere-reconstruction), [`reverse-anything`](#s-reverse-anything) |
| Write Xiaohongshu or other social content | [`xiaohongshu`](#s-xiaohongshu), [`xiaohongshu-netfeel-guardian`](#s-xiaohongshu-netfeel-guardian), [`creator-ops-os`](#s-creator-ops-os), [`topic-insight-writing`](#s-topic-insight-writing) |
| Make an ad, poster or product video | [`narrative-ad-engine`](#s-narrative-ad-engine), [`brand-short-drama`](#s-brand-short-drama), [`beetle-poster-director`](#s-beetle-poster-director), [`build-product-demo`](#s-build-product-demo) |
| Research a market, industry or question | [`industry-intelligence-engine`](#s-industry-intelligence-engine), [`universal-research-architect`](#s-universal-research-architect), [`consulting-analysis`](#s-consulting-analysis), [`multi-ai-research`](#s-multi-ai-research) |
| Go from a raw idea to a PRD | [`idea-team`](#s-idea-team), [`idea-to-product`](#s-idea-to-product), [`product-discovery`](#s-product-discovery), [`prd-master`](#s-prd-master) |
| Build or redesign a web UI | [`frontend-design`](#s-frontend-design), [`frontend-art-director`](#s-frontend-art-director), [`ui-ux-pro-max`](#s-ui-ux-pro-max), [`figma-to-code`](#s-figma-to-code) |
| Start a new codebase | [`repo-scaffold`](#s-repo-scaffold), [`python-project`](#s-python-project), [`typescript-project`](#s-typescript-project), [`golang-web`](#s-golang-web), [`rust-project`](#s-rust-project) |
| Debug or audit code | [`systematic-debugging`](#s-systematic-debugging), [`codebase-audit`](#s-codebase-audit), [`project-health-auditor`](#s-project-health-auditor) |
| Set up or clean up AGENTS.md / CLAUDE.md | [`agentsmd-scaffold`](#s-agentsmd-scaffold), [`repo-agent-context-audit`](#s-repo-agent-context-audit), [`agentsmd-optimize`](#s-agentsmd-optimize) |
| Use Codex from inside Claude Code | [`codex`](#s-codex), [`codex-agent`](#s-codex-agent) |
| Create, fix or organise skills | [`skill-creator`](#s-skill-creator), [`skill-reforge-foundry`](#s-skill-reforge-foundry), [`self-evolution`](#s-self-evolution), [`skill-archive-manager`](#s-skill-archive-manager) |
| Fix proxy or network problems | [`clash-doctor`](#s-clash-doctor), [`network-reconnect-repair`](#s-network-reconnect-repair), [`optimize-network`](#s-optimize-network), [`ip-check`](#s-ip-check) |
| Free disk space or speed up my computer | [`storage-gc-guardian`](#s-storage-gc-guardian), [`disk-cleaner`](#s-disk-cleaner), [`system-doctor`](#s-system-doctor), [`vscode-doctor`](#s-vscode-doctor) |

<a id="how-to-install"></a>
## How to install a skill

There are two kinds of package in this repo.

**Standard skills (202 zips)** contain a `SKILL.md` and work with Claude Code, Codex and other runtimes that support Agent Skills.

1. Unzip the file and open `00_入口说明.txt` (or check the entry column in the CSV) to find the entry `SKILL.md`.
2. Copy the folder that contains that `SKILL.md` — together with its `references/`, `scripts/`, `assets/` and so on — into your agent's skills folder. For Claude Code that is `~/.claude/skills/<skill-name>/` for personal skills or `.claude/skills/<skill-name>/` inside a project ([Claude Code skills docs](https://code.claude.com/docs/en/skills)). For Codex or other runtimes, use the skills folder that runtime expects (several skills here assume `~/.agents/skills/`).
3. If the entry is a single file such as `skills/brainstorming.SKILL.md`, make a folder named after the skill and save the file inside it as `SKILL.md`.
4. Install anything listed under "How to use" for that skill (Python requirements, CLIs, MCP servers, API keys).

Most skills activate on their own when you describe a matching task. A few only run when you name them explicitly; their entries say so.

**Prompt-type skills (10 zips)** have no `SKILL.md`. Paste the entry file into any chat AI as the system prompt, custom instructions or first message, then send your material. They are marked *prompt-type* below.

<a id="packaging-notes"></a>
## Packaging notes and caveats

**Spellbook skills.** 106 of the zips come from the [Spellbook](https://github.com/majiayu000/spellbook) library (formerly Claude Arsenal). Each of those zips contains the *entire* `spellbook-main/` repository (~650 files); the skill itself is only the folder or `*.SKILL.md` file at its entry path. Spellbook also ships its own `install.sh` if you'd rather install the whole library at once. Several Spellbook skills hand work to siblings (for example `idea-team` → `idea-research`, `idea-devils-advocate`, `idea-analogist`), so install those together.

**Zips that contain more than one copy or version**

| Skill | What's inside | Which to use |
|---|---|---|
| `huazhao-portrait-director` | v5.0.0 and v6.0.0 | v6.0.0 (newer) |
| `reverse-anything` | v1.0 (`reverse-anything/`) and v2.0 (`reverse-anything__不同内容_0d88a8ba/`) | v2.0 (broader, evidence-driven) |
| `skill-reforge-foundry` | v5.1.0 (English) and a newer Chinese-first edition | Either; the Chinese edition focuses on turning conversations into skills |
| `h3-video-editing-prompt` | `SKILL.md` (English) and `SKILL.cn.md` (Chinese) | Same skill in two languages |
| `xuanshu-agent` | Full xuanshu-skill repo with two entry files | `skills/xuanshu-agent/SKILL.md` is the full guide |
| `feishu-rent-billing` | Current skill plus a backup copy | Root `feishu-rent-billing/SKILL.md` |
| `app-ui-design`, `figma-to-react`, `frontend-design`, `ui-design-system`, `idea-analogist`, `idea-devils-advocate`, `idea-research`, `idea-team`, `idea-to-product`, `rust-best-practices` | A core copy and a Spellbook plugin copy | Install only one, to avoid duplicate triggers |

**Overlaps.** `figma-to-code` and `figma-to-react` are the same generator under two names. The `anysearch`, `consulting-analysis`, `research-guide` and `research-hub` zips all contain the same `大调查` research bundle.

**Adjust before use**

- `gpu-use` — the default SSH server in `SKILL.md` is the original author's; replace it with yours.
- `weekly` — hard-wired to one project's front-end and back-end repos ("om-generator"); edit the repo names and paths.
- `meta-timing` — declares dependencies (`agent-harness-loop`, `scr-judgment`) that are not in this repo.
- `react-hooks-best-practices` — expects a `typescript-best-practices` skill that is not in this repo.
- `research-hub` — routes to video-download, book-ingest and knowledge-* skills that are not in this repo.
- `skill-archive-manager` — part of an `archive-center-suite` and relies on that suite's tooling.
- `分镜设计大师阶段2` / `分镜设计大师阶段3` — the file *inside* each zip carries the other stage's file name. The zip names are right: the Stage 2 zip holds the Stage 2 assembler, the Stage 3 zip holds the Stage 3 converter.

<a id="catalog"></a>
# Catalog by category

Each section starts with a one-line overview table; full entries follow it.

<a id="cat-video"></a>
## AI video, film & storyboards

Directing and prompting AI video (Seedance, MiniMax H3, Jimeng and others), storyboards, continuity, editing and full production pipelines.

| Skill | Best suited for |
|---|---|
| [`agentic-video-director`](#s-agentic-video-director) | End-to-end video builds where the deliverable is a rendered file, not just a prompt. |
| [`atmospheric-character-short-director`](#s-atmospheric-character-short-director) | Short vertical character mood films. |
| [`cinematic-fight-director`](#s-cinematic-fight-director) | Readable, physically convincing fight choreography in AI video. |
| [`fengyun-jue-rebuilder`](#s-fengyun-jue-rebuilder) | Fan restagings of this specific animated film in a new visual style. |
| [`h3-video-editing-prompt`](#s-h3-video-editing-prompt) | Precise masked-region and object-replacement edits with MiniMax H3. |
| [`interactive-film-ui-fusion`](#s-interactive-film-ui-fusion) | Adding clean, cinematic interactivity on top of interactive video. |
| [`jingqiao-continuity-supervisor`](#s-jingqiao-continuity-supervisor) | Catching continuity errors before you spend credits generating video. |
| [`live-mv-weaver`](#s-live-mv-weaver) | Live-performance MVs with an audience storyline. |
| [`motion-drama-foundry`](#s-motion-drama-foundry) | Taking a motion comic or AI short from idea to generation-ready package. |
| [`motionprint-reverse`](#s-motionprint-reverse) | Recreating how a reference video moves, not just how it looks. |
| [`mr-li-seedance-25`](#s-mr-li-seedance-25) | Faithful, segment-by-segment Seedance production from a finished script. |
| [`Mx-Shell_Prompts`](#s-mx-shell-prompts) | Writing Seedance 2.0 prompts from rough narrative text. |
| [`scenerelay-reverse`](#s-scenerelay-reverse) | Remaking a reference video with your own cast and world in Seedance 2.5. |
| [`script-scene-visual-storyboard`](#s-script-scene-visual-storyboard) | Turning a written scene into a believable sequence of frames. |
| [`seedance-clean`](#s-seedance-clean) | Clean, single Seedance 2.0 shot and scene prompts. |
| [`short-drama-producer`](#s-short-drama-producer) | A complete Jimeng-ready production pack for a short drama. |
| [`storyboard-forge-20-25`](#s-storyboard-forge-20-25) | Planning a generatable, editable AI video sequence. |
| [`talking-head-fx-packager`](#s-talking-head-fx-packager) | Tasteful effects and subtitle packaging for spoken-content videos. |
| [`video-studio`](#s-video-studio) | Editing talking-head videos and livestream clips locally by chat. |
| [`AI视频空间调度导演`](#s-zh-b603f88d) | Keeping room layout, character positions and camera paths consistent across AI video shots — aimed at non-technical creators. |
| [`分镜设计大师阶段1：导演设计器`](#s-zh-a4f0e6a7) | Locking the director's design before any storyboard image is made. |
| [`分镜设计大师阶段2：分镜图Skill装配器`](#s-zh-18d9bfd6) | Turning a locked director design into consistent storyboard images. |
| [`分镜设计大师阶段3：视频提示词转换器`](#s-zh-5a8eb463) | Faithful shot-by-shot video prompts from approved storyboards. |
| [`解说漫制片教练`](#s-zh-8927f55c) | Beginners producing narrated recap comics (解说漫) step by step. |

<a id="s-agentic-video-director"></a>
### agentic-video-director

[agentic-video-director.zip](agentic-video-director.zip) · entry: `agentic-video-director-v1.0.0/SKILL.md`

- **What it does:** Lets a coding agent produce real video files: turns intent into a timed shot contract, picks the lightest production path, renders, inspects the actual pixels and audio, repairs defects and delivers the file. Has model notes for Claude Opus 5.5 and GPT-6, MV timing, quality gates, scripts and templates.
- **How to use:** In Claude Code or Codex, ask it to create, edit, repair or finish a video, MV, promo, launch film, explainer or motion-graphics piece; supply your assets, music and target length.
- **Best suited for:** End-to-end video builds where the deliverable is a rendered file, not just a prompt.

<a id="s-atmospheric-character-short-director"></a>
### atmospheric-character-short-director

[atmospheric-character-short-director.zip](atmospheric-character-short-director.zip) · entry: `视频分镜skill导演.md`

- **What it does:** Directs 5–15 second, character-centred atmospheric AI videos — character showcases, beauty/fashion mood films, ancient-style portraits, restrained romance, vertical social promos. Turns an idea or reference image into a shot design and a ready-to-use video prompt, choosing between a single take, a short multi-shot or separately generated shots.
- **How to use:** The entry is `视频分镜skill导演.md`. Describe the character, mood and platform (optionally attach a reference image). Not for long plots, multi-character dialogue or fight scenes.
- **Best suited for:** Short vertical character mood films.

<a id="s-cinematic-fight-director"></a>
### cinematic-fight-director

[cinematic-fight-director.zip](cinematic-fight-director.zip) · entry: `cinematic-fight-director-public-v4.0.0/SKILL.md`

- **What it does:** Director-first prompt compiler for AI fight scenes, optimised for Seedance 2.5 and adaptable to other models. Builds "action packets" with six locks (identity, space, physics, tempo, camera, style), motion-density settings, momentum continuity, impact hierarchy and multi-enemy / airborne rules, so action reads as fast, physical and continuous.
- **How to use:** Give a fight idea, script beat, character image, storyboard or motion reference; get a production-ready video prompt (choose measured / kinetic / hyper-dense density).
- **Best suited for:** Readable, physically convincing fight choreography in AI video.

<a id="s-fengyun-jue-rebuilder"></a>
### fengyun-jue-rebuilder

[fengyun-jue-rebuilder.zip](fengyun-jue-rebuilder.zip) · entry: `fengyun-jue-rebuilder/SKILL.md`

- **What it does:** Recreates or restages *Feng Yun Jue / Storm Rider: Clash of the Evils* characters, scenes, fights, trailers and music-driven sequences. Uses three separate engines — narrative, combat and style — that meet only at the shot package, with character identity as a fixed invariant. Modes: CHARACTER_ASSET, SHOT_REPLICA, NARRATIVE_REBUILD, COMBAT_REBUILD, MUSIC_REBUILD, TRAILER_REBUILD.
- **How to use:** Pick a mode, give the source scene or character and a separately defined target visual style; approval gates come before final generation.
- **Best suited for:** Fan restagings of this specific animated film in a new visual style.

<a id="s-h3-video-editing-prompt"></a>
### h3-video-editing-prompt

[h3-video-editing-prompt.zip](h3-video-editing-prompt.zip) · entry: `h3-video-editing-prompt/SKILL.md` · `h3-video-editing-prompt/SKILL.cn.md`

- **What it does:** Writes MiniMax H3 video-editing prompts in the full-reference Ref2VA six-field format: face and identity replacement, costumes, held or scene objects, background, on-screen text, materials, lighting, object removal or addition, and video continuation. Key rule: describe what the final video shows, never the operation ("swap", "remove"). Includes visible-behaviour and motion-transfer checklists and scene recipes; English and Chinese versions; works as a ComfyUI node prompt.
- **How to use:** Provide the source video description and reference material and say what should change ("replace the apple with this watermelon", "put this face into the video", "relight to dusk"). Outputs English prompt text by default.
- **Best suited for:** Precise masked-region and object-replacement edits with MiniMax H3.

<a id="s-interactive-film-ui-fusion"></a>
### interactive-film-ui-fusion

[interactive-film-ui-fusion.zip](interactive-film-ui-fusion.zip) · entry: `interactive-film-ui-fusion-v1.1.0/SKILL.md`

- **What it does:** Designs the visible interaction layer of interactive films, FMV, branching AI video, playable shorts, H5 experiences and cinematic games: HUD/UI assets, hotspots, QTE presentation, interaction feedback, video-attached overlays, motion states, spatial anchors, storyboard/previs review and runtime UI handoff. Story and branch state stay with the upstream production system.
- **How to use:** Provide the branch graph or node list and video context; it produces a canonical event timeline, UI components and renderer-ready handoff. Load only the references the task needs.
- **Best suited for:** Adding clean, cinematic interactivity on top of interactive video.

<a id="s-jingqiao-continuity-supervisor"></a>
### jingqiao-continuity-supervisor

[jingqiao-continuity-supervisor.zip](jingqiao-continuity-supervisor.zip) · entry: `jingqiao-continuity-supervisor/SKILL.md`

- **What it does:** "Jingqiao (Shot Bridge) 2.0" — a continuity supervisor for AI-video storyboard prompts and generated clips. Models each shot as entry state → event → exit state and checks identity, persistent state (props, wardrobe, injuries), motion handoff, space-time and cause across the whole sequence, distinguishing legitimate ellipsis and intentional hard cuts from real breaks. Fixes with the smallest change; supports Seedance 2.0 multi-shot and continuation.
- **How to use:** Paste two or dozens of shot prompts (or clips) and ask "check continuity" or "fix the jumps". It returns flagged cuts and repaired prompts, or a full corrected version on request.
- **Best suited for:** Catching continuity errors before you spend credits generating video.

<a id="s-live-mv-weaver"></a>
### live-mv-weaver

[live-mv-weaver.zip](live-mv-weaver.zip) · entry: `live-mv-weaver/SKILL.md`

- **What it does:** Builds or reconstructs music videos where one continuous live song is the master timeline, intercut with recurring audience reactions, in-world dialogue, band details, callbacks and same-location micro-drama. REPLICA mode copies a reference MV's structure; REPLICA_PLUS keeps the grammar but improves performances, continuity, audio and cuts.
- **How to use:** Supply the song (with start/end times) and, ideally, a reference MV; it produces the locked song timeline, shot plan and generation package.
- **Best suited for:** Live-performance MVs with an audience storyline.

<a id="s-motion-drama-foundry"></a>
### motion-drama-foundry

[motion-drama-foundry.zip](motion-drama-foundry.zip) · entry: `motion-drama-foundry/SKILL.md`

- **What it does:** All-in-one motion-comic / AI-video production: from a one-line story, script or existing assets through story development, script, character/scene/prop asset definitions, storyboard, cross-shot continuity, video-generation prompts and sound/edit handoff. Keeps one Project Ledger as the source of truth.
- **How to use:** Modes are detected automatically: FULL RUN ("do it all from this story"), TAKEOVER (continue from what you have), STAGE ONLY (just one step), REPAIR (fix a broken image, video or prompt). See `使用说明书.pdf` for the manual.
- **Best suited for:** Taking a motion comic or AI short from idea to generation-ready package.

<a id="s-motionprint-reverse"></a>
### motionprint-reverse

[motionprint-reverse.zip](motionprint-reverse.zip) · entry: `MOTIONPRINT-REVERSE-1.1/SKILL.md`

- **What it does:** Reverse-engineers any AI video into a high-fidelity video prompt by recovering motion, camera movement, rhythm, space and environmental response (seven "motion fingerprints") rather than listing visual tags. Modes: quick, full, multi-shot, compare-and-patch (fix the top three deviations) and enhanced rewrite.
- **How to use:** Upload a video, clip or keyframe sequence; default output is a full fingerprint card plus Core, Directed and platform prompts. Upload your generated result too for a compare-and-patch loop.
- **Best suited for:** Recreating how a reference video moves, not just how it looks.

<a id="s-mr-li-seedance-25"></a>
### mr-li-seedance-25

[mr-li-seedance-25.zip](mr-li-seedance-25.zip) · entry: `mr-li-seedance-25/SKILL.md`

- **What it does:** "Mr. Li's Seedance rules" — splits an authoritative Chinese script into submit-ready Seedance segment prompts sized to real performance capacity, one natural generation segment at a time. Handles drama vs action scene writing, visual tone, asset binding and creation, result rework and delivery review, without silently rewriting dialogue or plot.
- **How to use:** On first use it explains its seven stages (lock script, scope, tone, assets, segment prompts, rework, wrap-up); then control it with phrases like "confirm and continue", "skip assets", "do 1-1", "next segment", "only change blocking". If a host takes one file, use `references/universal-runtime.md`.
- **Best suited for:** Faithful, segment-by-segment Seedance production from a finished script.

<a id="s-mx-shell-prompts"></a>
### Mx-Shell_Prompts

[Mx-Shell_Prompts.zip](Mx-Shell_Prompts.zip) · *prompt-type* · entry: `内层包/Mx-Shell_Prompts_v1.5/Mx-Shell_Prompts_v1.5.md`

- **What it does:** Converts a story outline, script excerpt, storyboard draft, novel passage or voice-over copy into structured, film-grade Seedance 2.0 video prompts with second-by-second timelines and physics-first (non-literary) descriptions. Supports one-take mode and multi-camera mode.
- **How to use:** Load `Mx-Shell_Prompts_v1.5.md` as a prompt. It asks for the mode, character/prop/scene descriptions (short if you have reference images, detailed if not), mood and quality settings, sound rules, dialogue/voice-over and the action, then outputs the finished prompt.
- **Best suited for:** Writing Seedance 2.0 prompts from rough narrative text.

<a id="s-scenerelay-reverse"></a>
### scenerelay-reverse

[scenerelay-reverse.zip](scenerelay-reverse.zip) · entry: `scenerelay-reverse/SKILL.md`

- **What it does:** "SceneRelay Reverse 3.1" — adapts a reference video into a Seedance 2.5-ready production: shot-by-shot reverse analysis, dramatic-function breakdown, "replacement ripple" recalculation when swapping characters, scenes or props, a new causally closed shot script, an actual reference-image pack (with each image's role and upload order) and one copy-ready Seedance block per segment. Fixes the earliest deviation when generations drift. Supports multi-round projects.
- **How to use:** Upload the reference video and (now or later) your replacement characters/scenes/props; say "analyse then give me the reference images and Seedance prompts".
- **Best suited for:** Remaking a reference video with your own cast and world in Seedance 2.5.

<a id="s-script-scene-visual-storyboard"></a>
### script-scene-visual-storyboard

[script-scene-visual-storyboard.zip](script-scene-visual-storyboard.zip) · entry: `script-scene-visual-storyboard-v1.0.0/SKILL.md`

- **What it does:** Converts screenplays, scenes, story passages or dialogue into spatially coherent, emotionally purposeful storyboards: scene truth → visible evidence → space model → pressure curve → frame design, with anchor/support/punctuation shots, continuity rules and model-agnostic storyboard image prompts. Modes: direct storyboard, shot design, visual board, previs/continuity.
- **How to use:** Paste the scene or script and ask for storyboards, a shot list, blocking or storyboard-image prompts.
- **Best suited for:** Turning a written scene into a believable sequence of frames.

<a id="s-seedance-clean"></a>
### seedance-clean

[seedance-clean.zip](seedance-clean.zip) · entry: `higg导演/SKILL.md`

- **What it does:** Seedance 2.0 prompt-writing system built on "write the visible": translates mood into observable action, light and camera; covers asset tagging, context isolation, distributed style, cuts and timing, directing, optics (shot sizes, lens/FOV anchors), special protocols and a pre-prompt checklist. Always outputs one standalone prompt in a code block.
- **How to use:** Say "write a Seedance prompt for…", "build a shot where…", or ask about Seedance technique. The package folder is `higg导演/`; it also contains a packaged `seedance-clean_v2.skill` file.
- **Best suited for:** Clean, single Seedance 2.0 shot and scene prompts.

<a id="s-short-drama-producer"></a>
### short-drama-producer

[short-drama-producer.zip](short-drama-producer.zip) · entry: `short-drama-producer/SKILL.md`

- **What it does:** End-to-end short-drama production for AI video: script, storyboard table, character / prop / scene asset cards and Jimeng (即梦) video prompts, with an AI self-check and delivery checklist. Handles single 3–5 minute episodes and multi-episode series.
- **How to use:** Start from a theme (mode A), an outline (mode B) or a finished script (mode C). For A/B it first asks genre, cast, emotional tone, episode count and any brand constraints.
- **Best suited for:** A complete Jimeng-ready production pack for a short drama.

<a id="s-storyboard-forge-20-25"></a>
### storyboard-forge-20-25

[storyboard-forge-20-25.zip](storyboard-forge-20-25.zip) · entry: `storyboard-forge-20-25-v2.0.0/SKILL.md`

- **What it does:** Director-grade storyboarding and shot planning for Seedance 2.0/2.5 and other AI video tools. Turns scripts, concepts, ads, action, dialogue, MV/performance, product films, trailers, horror, comedy, anime and documentary briefs into model-routed storyboards, shot contracts, continuity locks, reference plans, generation prompts, retake plans and edit handoffs.
- **How to use:** Give the script or brief (with references if any); it infers before asking and outputs in the mode you need. Invocable directly.
- **Best suited for:** Planning a generatable, editable AI video sequence.

<a id="s-talking-head-fx-packager"></a>
### talking-head-fx-packager

[talking-head-fx-packager.zip](talking-head-fx-packager.zip) · entry: `talking-head-fx-packager-v1.0.0/SKILL.md`

- **What it does:** Packaging director for talking-head, vlog, explainer, review and tutorial videos: turns a script, transcript, SRT/VTT or rough timeline into a restrained, editor-ready plan of captions, emphasis typography, callouts, punch-ins, overlays, B-roll prompts, UI cards, transitions and SFX — with a density budget and an anti-overpacking pass. Does not rewrite content.
- **How to use:** Give the script or subtitles and say "package this talking-head video" / "加字幕和重点字卡，别太花". Works for 9:16, 1:1 and 16:9 and for CapCut/Jianying, Premiere, After Effects, DaVinci or Remotion.
- **Best suited for:** Tasteful effects and subtitle packaging for spoken-content videos.

<a id="s-video-studio"></a>
### video-studio

[video-studio.zip](video-studio.zip) · entry: `video-studio/skills/video-studio/SKILL.md`

- **What it does:** Local, conversation-driven video editing and generation for Claude Code (ffmpeg + Python, HyperFrames HTML→MP4): talking-head fine cuts (remove fillers, retakes and dead air, punch-in zooms, burned-in Chinese captions), livestream slicing (find highlights in multi-hour streams, batch-cut 9:16 clips with titles, covers and copy) and code-generated data/product explainer animations with TTS. Also reframing 16:9→9:16, subtitles, BGM ducking, loudness and platform exports (Douyin, Channels, Xiaohongshu, Bilibili, YouTube).
- **How to use:** One-time setup per machine (see the SKILL.md; install `requirements.txt`), then say "剪掉口误", "slice highlights from this stream", "add captions", "make a 9:16 version" or "make a data animation". Works from word-level transcripts and confirms before rendering.
- **Best suited for:** Editing talking-head videos and livestream clips locally by chat.

<a id="s-zh-b603f88d"></a>
### AI视频空间调度导演

[AI视频空间调度导演.zip](AI%E8%A7%86%E9%A2%91%E7%A9%BA%E9%97%B4%E8%B0%83%E5%BA%A6%E5%AF%BC%E6%BC%94.zip) · *prompt-type* · entry: `AI视频空间调度导演-开源傻瓜版-v1.0/02-完整主提示词.md`

- **What it does:** "AI Video Spatial Blocking Director" — a plain-language prompt pack that turns a script into an AI-video plan: a 3×3 empty-set grid prompt, a top-down character and camera blocking diagram prompt, a recommended shot count (1–4) with reasons, a copy-ready video prompt per shot, and the three most likely failure points with fix-up phrases.
- **How to use:** Not a SKILL.md skill. Paste `02-完整主提示词.md` (the master prompt) into any text LLM, then send your script using `03-客户填写模板.md`. `04-失败诊断器.md` helps when a generation goes wrong; `05` is a worked example.
- **Best suited for:** Keeping room layout, character positions and camera paths consistent across AI video shots — aimed at non-technical creators.

<a id="s-zh-a4f0e6a7"></a>
### 分镜设计大师阶段1：导演设计器

[分镜设计大师阶段1：导演设计器.zip](%E5%88%86%E9%95%9C%E8%AE%BE%E8%AE%A1%E5%A4%A7%E5%B8%88%E9%98%B6%E6%AE%B51%EF%BC%9A%E5%AF%BC%E6%BC%94%E8%AE%BE%E8%AE%A1%E5%99%A8.zip) · *prompt-type* · entry: `内层包/分镜设计大师/分镜设计大师/01_阶段1_导演设计器_项目交接包A.txt`

- **What it does:** "Storyboard Design Master — Stage 1: Director Designer". First stage of a three-stage AI-video previs pipeline: from your plot, characters, scenes, reference images, shot count, canvas ratio and style needs, it does the full director design (core aesthetic, master visual prompt, character and space locks, canvas and layout lock, shot rhythm, key frame per shot) and outputs "Project Handoff Pack A" — the single source of truth for stages 2 and 3.
- **How to use:** Prompt-type: paste `01_阶段1_导演设计器_项目交接包A.txt` into a text LLM, then send your story and requirements. Carry Pack A into Stage 2.
- **Best suited for:** Locking the director's design before any storyboard image is made.

<a id="s-zh-18d9bfd6"></a>
### 分镜设计大师阶段2：分镜图Skill装配器

[分镜设计大师阶段2：分镜图Skill装配器.zip](%E5%88%86%E9%95%9C%E8%AE%BE%E8%AE%A1%E5%A4%A7%E5%B8%88%E9%98%B6%E6%AE%B52%EF%BC%9A%E5%88%86%E9%95%9C%E5%9B%BESkill%E8%A3%85%E9%85%8D%E5%99%A8.zip) · *prompt-type* · entry: `内层包/分镜设计大师/分镜设计大师/03_阶段3_分镜图转Seedance视频提示词转换器.txt`

- **What it does:** "Storyboard Design Master — Stage 2: Storyboard-Image Skill Assembler". Reads Project Handoff Pack A and, without re-designing anything, compresses it into a master prompt an image model can execute for the storyboard board (adaptive canvas, layout, info strips), runs an inheritance self-check before generation and image QA after, then outputs "Project Handoff Pack B".
- **How to use:** Prompt-type: paste the prompt file into a text LLM together with Pack A. Heads-up: inside this zip the file is named `03_阶段3_分镜图转Seedance视频提示词转换器.txt`, but its content is the Stage 2 assembler — the inner file names of Stage 2 and Stage 3 are swapped; the zip names are correct.
- **Best suited for:** Turning a locked director design into consistent storyboard images.

<a id="s-zh-5a8eb463"></a>
### 分镜设计大师阶段3：视频提示词转换器

[分镜设计大师阶段3：视频提示词转换器.zip](%E5%88%86%E9%95%9C%E8%AE%BE%E8%AE%A1%E5%A4%A7%E5%B8%88%E9%98%B6%E6%AE%B53%EF%BC%9A%E8%A7%86%E9%A2%91%E6%8F%90%E7%A4%BA%E8%AF%8D%E8%BD%AC%E6%8D%A2%E5%99%A8.zip) · *prompt-type* · entry: `内层包/分镜设计大师/分镜设计大师/02_阶段2_自适应画布分镜图Skill装配器_项目交接包B.txt`

- **What it does:** "Storyboard Design Master — Stage 3: Video Prompt Converter". Reads Project Handoff Pack B and writes per-shot Seedance / AI-video prompts constrained by the original plot, director design, storyboard prompt and final storyboard board — so motion follows the design instead of being improvised from the pictures.
- **How to use:** Prompt-type: paste the prompt file into a text LLM together with Pack B. Heads-up: inside this zip the file is named `02_阶段2_自适应画布分镜图Skill装配器_项目交接包B.txt`, but its content is the Stage 3 converter (file names swapped with Stage 2).
- **Best suited for:** Faithful shot-by-shot video prompts from approved storyboards.

<a id="s-zh-8927f55c"></a>
### 解说漫制片教练

[解说漫制片教练.zip](%E8%A7%A3%E8%AF%B4%E6%BC%AB%E5%88%B6%E7%89%87%E6%95%99%E7%BB%83.zip) · *prompt-type* · entry: `解说漫生产系统_v3.0_完整管理版_RELEASE/学生公开运行时/00_直接发给AI.md`

- **What it does:** "Recap-comic Production Coach v3.0" — compiles a source story into a recap-style motion comic: plot ledger → high-quality narration script (four automatic revision passes, internal dual-draft competition, 100-point acceptance) → shot production cards and character/location continuity → image tasks → motion video tasks → voice, subtitles and edit → final check. Built for complete beginners: each turn shows only "where we are / what AI did / what you do now / what to copy / what correct looks like".
- **How to use:** Prompt-type: send `00_直接发给AI.md` together with your source material to a chat AI that can read long files, then say `开始制作`. Only six phrases needed: 开始制作, 下一步, 我不会, 检查这个, 只修这个 + number, 准备交付. Student quick-start and FAQ files are included.
- **Best suited for:** Beginners producing narrated recap comics (解说漫) step by step.

<a id="cat-story"></a>
## Screenwriting & storytelling

Feature films, short dramas, sitcoms, fiction continuation and story-world simulation.

| Skill | Best suited for |
|---|---|
| [`audience-psychology-engine`](#s-audience-psychology-engine) | Checking whether intended emotional beats actually land, before shooting or after a rough cut. |
| [`brand-short-drama`](#s-brand-short-drama) | Branded / product-placement short dramas and local-business story ads. |
| [`fanqie-shortstory-forge`](#s-fanqie-shortstory-forge) | High-completion short fiction tuned to Fanqie readers. |
| [`genre-writer`](#s-genre-writer) | Long-form genre stories that need solid design before prose. |
| [`hollywood-omni-screenplay-master`](#s-hollywood-omni-screenplay-master) | Feature-length screenplays with strong structure and memorable dialogue. |
| [`mass-appeal-super-screenwriter`](#s-mass-appeal-super-screenwriter) | Making stories instantly gripping for a mass audience. |
| [`screenplay-factory`](#s-screenplay-factory) | Script development that respects the difference between films and short dramas. |
| [`screenwriting-master`](#s-screenwriting-master) | Guided, step-by-step screenwriting in any format. |
| [`story-dynamics-workbench`](#s-story-dynamics-workbench) | Long, complex stories where causality and character psychology must stay consistent. |
| [`story-forge-engine`](#s-story-forge-engine) | Continuing an existing story in a causally convincing way. |
| [`viral-framework-analyzer`](#s-viral-framework-analyzer) | Learning what actually makes a genre's top performers work. |
| [`writing-ensemble-sitcoms`](#s-writing-ensemble-sitcoms) | Recurring-cast comedy with natural dialogue rather than stage banter. |
| [`微短剧剧本创作`](#s-zh-b6e6af54) | Writing a full paid micro-drama series for short-video platforms. |
| [`故事世界模拟-v4.0.0`](#s-zh-a64c64af) | Rigorous, canon-safe simulation of complex story worlds. |

<a id="s-audience-psychology-engine"></a>
### audience-psychology-engine

[audience-psychology-engine.zip](audience-psychology-engine.zip) · entry: `audience-psychology-engine/SKILL.md`

- **What it does:** An "audience judge" for AI film, TV, short dramas and motion comics. Simulates a real viewer with no future knowledge and limited attention and memory, tracks a Viewer State timeline, and tests hooks, suspense, twists, character investment and rough cuts, then traces each problem to the writer, director or editor with a feedback packet. Never invents audience statistics.
- **How to use:** Give it a script, storyboard or rough cut and ask "will viewers get this?", "where do they lose interest?", or "does this twist land?". Can plug in alongside writing, directing and editing skills.
- **Best suited for:** Checking whether intended emotional beats actually land, before shooting or after a rough cut.

<a id="s-brand-short-drama"></a>
### brand-short-drama

[brand-short-drama.zip](brand-short-drama.zip) · entry: `短剧植入技能包/brand-short-drama/SKILL.md`

- **What it does:** Writes viral-style short dramas with a product or local service woven in (e-commerce goods, hot springs, rafting, restaurants, scenic spots, hotels, shops). Breaks down selling points, matches audience to trending genres, designs the placement, then writes episode outlines, full scripts and a dual quality check (hook strength and naturalness of placement). Core rule: the product is the story's "cheat code" or "weak spot" — characters never read ad copy.
- **How to use:** Give the product or venue, target audience and number of episodes ("write a branded short drama for my hot-spring resort"). It delivers product cards, three concepts with a pick, character bios, an emotion curve, scripts, a QC report and shooting/compliance notes.
- **Best suited for:** Branded / product-placement short dramas and local-business story ads.

<a id="s-fanqie-shortstory-forge"></a>
### fanqie-shortstory-forge

[fanqie-shortstory-forge.zip](fanqie-shortstory-forge.zip) · entry: `fanqie-shortstory-forge-v1.1.0/SKILL.md`

- **What it does:** Writing and editing skill for short stories on the Fanqie (Tomato) platform: concept, selling point, opening hook, emotion curve, short-form structure, characters, full text, title and blurb, platform review, adaptation potential and rewrites. Handles many genres (urban romance, revenge, suspense, healing realism, period drama, xuanhuan, sci-fi, rule-horror).
- **How to use:** Give an idea, outline or draft plus optional length, genre, audience and mood. It routes automatically: idea → story, outline, full draft, rewrite, review, reference deconstruction or trend check (verifies current platform rules online when asked).
- **Best suited for:** High-completion short fiction tuned to Fanqie readers.

<a id="s-genre-writer"></a>
### genre-writer

[genre-writer.zip](genre-writer.zip) · entry: `genre-writer/SKILL.md`

- **What it does:** Genre fiction and script writing system for mystery, fantasy, sci-fi, screenplays (film, short drama, murder-mystery games) and world-building. Workflow: project contract → dissect reference works and build a style profile → design (truth table, rules-and-costs table, core-variable extrapolation, scene table) → write chapter by chapter → role-based review and an AI-flavour check script. All state lives in a `story/` folder so sessions can resume.
- **How to use:** Say you want to write a novel or script, design a mystery trick, build a magic system or world, dissect a benchmark work, extract a writing style, check consistency or remove AI flavour.
- **Best suited for:** Long-form genre stories that need solid design before prose.

<a id="s-hollywood-omni-screenplay-master"></a>
### hollywood-omni-screenplay-master

[hollywood-omni-screenplay-master.zip](hollywood-omni-screenplay-master.zip) · entry: `好莱坞全能电影剧本大师系统-v3.0.0/SKILL.md`

- **What it does:** "Hollywood all-round screenplay master" for feature films: auto-routes between feature, short, series, scene rewrite and dialogue surgery, then runs a pipeline of brief lock, story core, ending vector, outline, feature architecture (midpoint reframe, crisis choice, climax ownership), antagonist autonomy, scene engine, rehearsal dialogue, story-state tracking, promise–payoff, rewrite lab and final audit. Core rules: causality over beats, smart opposition, dialogue as action, fix only the failing layer.
- **How to use:** Give a premise, outline or existing screenplay and say whether you want development, a full draft, a rewrite, diagnosis or dialogue polish.
- **Best suited for:** Feature-length screenplays with strong structure and memorable dialogue.

<a id="s-mass-appeal-super-screenwriter"></a>
### mass-appeal-super-screenwriter

[mass-appeal-super-screenwriter.zip](mass-appeal-super-screenwriter.zip) · entry: `mass-appeal-super-screenwriter-v1.0.0/SKILL.md`

- **What it does:** Screenwriting for broad audiences: low comprehension cost, high emotional voltage, immediate conflict, strong episode hooks and escape from repetitive AI-style plotting. Eight engines (starting with a "nuclear opening") and gates; workflows for idea → story, episode writing, diagnose & rescue, and rewrite.
- **How to use:** Give a premise, episode brief or existing draft and say whether to create, write, diagnose or rewrite. Works for short drama, film, series, vertical video and narrative ads.
- **Best suited for:** Making stories instantly gripping for a mass audience.

<a id="s-screenplay-factory"></a>
### screenplay-factory

[screenplay-factory.zip](screenplay-factory.zip) · entry: `screenplay-factory/SKILL.md`

- **What it does:** Dual-engine screenplay factory: decides first whether the work is a FEATURE_FILM or a SHORT_DRAMA (short drama, micro-drama, motion comic) and uses that engine's structure, pacing, character change, information release and endings — with shared foundations for character, scene, dialogue, causality, adaptation and format. Develops, adapts (e.g. novel → script), writes, continues, rewrites and reviews. Text only; no storyboards or media.
- **How to use:** Give an idea, novel, synopsis, characters or existing script and say what you need (outline, episode list, scene list, full script, rewrite, de-AI, review).
- **Best suited for:** Script development that respects the difference between films and short dramas.

<a id="s-screenwriting-master"></a>
### screenwriting-master

[screenwriting-master.zip](screenwriting-master.zip) · entry: `screenwriting-master/SKILL.md`

- **What it does:** "Shanyin Super Screenwriter" (by @山音): full-format screenwriting from 1–3 minute concept shorts (how-to-tell / what-if) and 5–10 minute narrative shorts to 90-minute features and multi-episode series, covering character design, structure (Save the Cat, Story Circle, McKee), scene breakdown and full script. Strict red lines: no inner-thought description, no explanatory dialogue, everything must be filmable.
- **How to use:** Say "write a script / short / film / series", "help me come up with a story" or "this scene isn't working". It works step by step and waits for your approval after each step; ask for "[自检]" to see its checklist review.
- **Best suited for:** Guided, step-by-step screenwriting in any format.

<a id="s-story-dynamics-workbench"></a>
### story-dynamics-workbench

[story-dynamics-workbench.zip](story-dynamics-workbench.zip) · entry: `story-dynamics-workbench-v2.0.0/SKILL.md`

- **What it does:** Long-form fiction and screenplay workbench that simulates narrative state: character lives, temporal world state, what each character knows and believes, social and audience state, causal plot simulation with independent actor passes, continuity, adaptation and scene writing — keeping drafts separate from canon.
- **How to use:** Modes: DISCOVER, CHARACTER, SIMULATE, NOVEL, SCREENPLAY, ADAPT, AUDIT, REPAIR. Say "continue this novel", "plot the next arc", "simulate what happens next", "build this character", "novel to screenplay" or "continuity check".
- **Best suited for:** Long, complex stories where causality and character psychology must stay consistent.

<a id="s-story-forge-engine"></a>
### story-forge-engine

[story-forge-engine.zip](story-forge-engine.zip) · entry: `story-forge-engine/SKILL.md`

- **What it does:** "Plot simulation engine": builds a story bible from your characters, world rules, prior text and outline, then projects what happens next from each character's goals, knowledge and misbeliefs, costs and the opposition's reactions. Delivers directions, arc/chapter outlines, scenes, prose or script, checks continuity, and can export a standalone continuation skill for that specific work.
- **How to use:** Say "推演剧情", "what would these characters do next?", "outline what comes after this", "continue with these settings" or "export a continuation skill for this book". Needs existing story material.
- **Best suited for:** Continuing an existing story in a causally convincing way.

<a id="s-viral-framework-analyzer"></a>
### viral-framework-analyzer

[viral-framework-analyzer.zip](viral-framework-analyzer.zip) · entry: `viral-framework-analyzer-v2.0.0/SKILL.md`

- **What it does:** "Viral framework analysis factory": takes a batch of short dramas, AI dramas, motion comics, recap dramas or short fiction (scripts, subtitles, links, ranking data) and automatically builds a sample library, dissects each work, compares across samples, runs counterfactual checks and synthesises the genre's reusable hit framework, with templates for the first 3 / first 10 episodes and long-run escalation — plus what not to copy and where evidence is thin.
- **How to use:** Upload the batch and say "analyse this batch". It picks single, full-batch, tiered, map-reduce or corpus mode based on size. See `QUICKSTART.md`.
- **Best suited for:** Learning what actually makes a genre's top performers work.

<a id="s-writing-ensemble-sitcoms"></a>
### writing-ensemble-sitcoms

[writing-ensemble-sitcoms.zip](writing-ensemble-sitcoms.zip) · entry: `sitcom-writers-room-public-v1.0/SKILL.md`

- **What it does:** Writes, plans, revises and diagnoses episodic ensemble sitcoms: treats a sitcom as a stable social system under fresh pressure, with series, episode, scene and dialogue engines, distinct character voices, relationship-driven humour, causal scene turns, screen-ready action and a continuity ledger.
- **How to use:** Give the series premise and cast (or existing episodes) and ask for an episode, a scene, a dialogue pass or a diagnosis.
- **Best suited for:** Recurring-cast comedy with natural dialogue rather than stage banter.

<a id="s-zh-b6e6af54"></a>
### 微短剧剧本创作

[微短剧剧本创作.zip](%E5%BE%AE%E7%9F%AD%E5%89%A7%E5%89%A7%E6%9C%AC%E5%88%9B%E4%BD%9C.zip) · *prompt-type* · entry: `短剧编剧SKILL.md`

- **What it does:** "Micro short-drama scriptwriting" — guides you from topic to a finished 50–100 episode micro-drama: genre choice (13 genres plus overseas markets), opening rules, paywall cliff design, rhythm curve, five satisfaction-payoff types, four-layer villain system, hooks and a compliance checklist. Saves progress to the project folder and resumes automatically.
- **How to use:** Prompt-type file `短剧编剧SKILL.md` with slash-style commands: `/start`, `/plan`, `/characters`, `/outline`, `/episode {N}`, `/review {N}`, `/compliance`, `/export`. Best used in an agent that can read and write files.
- **Best suited for:** Writing a full paid micro-drama series for short-video platforms.

<a id="s-zh-a64c64af"></a>
### 故事世界模拟-v4.0.0

[故事世界模拟-v4.0.0.zip](%E6%95%85%E4%BA%8B%E4%B8%96%E7%95%8C%E6%A8%A1%E6%8B%9F-v4.0.0.zip) · entry: `故事世界模拟-v4.0.0/SKILL.md`

- **What it does:** "Story World Simulation 4.0" — a tool-backed story engine that separates facts, character knowledge, character interpretation, candidate futures and accepted canon. SIMULATE proposes structured intents and candidate events (never written straight into canon), characters may only act on knowledge they actually have at that time, world rules and resources are checked by tools, STEER changes external conditions with costs, NOVEL/SCREENPLAY render from a chosen event path, and COMMIT requires an audit.
- **How to use:** Start from the README (command reference) and a `project.json`; ask to analyse, continue, simulate, adapt or audit a story. Ships with schemas, tools and tests.
- **Best suited for:** Rigorous, canon-safe simulation of complex story worlds.

<a id="cat-image"></a>
## AI image & photography

Image direction, portraits and fashion, character and asset consistency, retouching and repair.

| Skill | Best suited for |
|---|---|
| [`aquamuse-swimwear-editorial-v1.0.0`](#s-aquamuse-swimwear-editorial-v1-0-0) | Swimwear, resort and poolside fashion imagery. |
| [`asset-continuity-imagegen`](#s-asset-continuity-imagegen) | Multi-image projects that need consistency — storyboards, product sets, character sheets. |
| [`character-asset-capture-kit`](#s-character-asset-capture-kit) | Turning a character that already exists in footage or art into a consistent asset for later generations. |
| [`fantasy-life-force-portrait-photography`](#s-fantasy-life-force-portrait-photography) | Making everyday portraits look like candid editorial photography for social posts. |
| [`fashion-shoot-twin`](#s-fashion-shoot-twin) | Fashion e-commerce lookbook sets in a borrowed photographic style. |
| [`fidelity-4k-upscale-skill-v1.0`](#s-fidelity-4k-upscale-skill-v1-0) | Getting a high-resolution "archival copy" of an image that must stay identical. |
| [`guided-image-director`](#s-guided-image-director) | Getting confident creative direction instead of a menu of prompt options. |
| [`huazhao-portrait-director`](#s-huazhao-portrait-director) | Credible, consistent portrait series with controlled identity and costume. |
| [`huazhao-portrait-engine`](#s-huazhao-portrait-engine) | Hanfu / classical-beauty portraits where costume logic and realism both matter. |
| [`image-factory`](#s-image-factory) | A general-purpose, model-agnostic image prompting workflow across many genres. |
| [`mj-aesthetic-lab-v2.0.0`](#s-mj-aesthetic-lab-v2-0-0) | Systematic Midjourney exploration and prompting. |
| [`nexuswear-persona-fashion-director`](#s-nexuswear-persona-fashion-director) | Original apparel concepts and character wardrobes. |
| [`photoreal-face-asset-engine`](#s-photoreal-face-asset-engine) | A consistent, reusable photoreal character face for image and video projects. |
| [`pic-fix-oneshot`](#s-pic-fix-oneshot) | Repairing AI-generated storyboard frames and illustrations without drifting. |
| [`portrait-retouch`](#s-portrait-retouch) | Making a portrait look better and more human without becoming a different person. |
| [`public-character-continuity`](#s-public-character-continuity) | Everyday "same character, new picture" requests. |
| [`realistic-social-selfie-retouch`](#s-realistic-social-selfie-retouch) | Natural "same me, but better" social-media selfies. |
| [`style-composition-lora-forge`](#s-style-composition-lora-forge) | Capturing a visual style in a LoRA when prompting alone can't reproduce it. |
| [`threadlock-wardrobe-skill-v1.0.0`](#s-threadlock-wardrobe-skill-v1-0-0) | Keeping outfits exactly consistent across characters, poses and shots. |
| [`wardrobe-extractor-skill-v1.0.0`](#s-wardrobe-extractor-skill-v1-0-0) | Pulling an outfit out of a reference image as a reusable sheet. |
| [`zhuangbi-portrait`](#s-zhuangbi-portrait) | Powerful, understated status portraits instead of flex-template images. |
| [`刺猬星球superi的超级skill`](#s-zh-b5e804a7) | Cinematic guofeng period-drama stills and short image-to-video clips. |
| [`古风短剧场景设计师`](#s-zh-8fa780ee) | Consistent set design references for costume short dramas. |

<a id="s-aquamuse-swimwear-editorial-v1-0-0"></a>
### aquamuse-swimwear-editorial-v1.0.0

[aquamuse-swimwear-editorial-v1.0.0.zip](aquamuse-swimwear-editorial-v1.0.0.zip) · entry: `aquamuse-swimwear-editorial-v1.0.0/SKILL.md`

- **What it does:** Prompt-planning skill for premium adult (21+) swimwear and resortwear editorials that read as real photography, not AI glamour. Uses a 7-layer engine (editorial thesis, subject, wardrobe, body action, camera geometry, light, reality pass), an anti-AI gate and a prompt compiler, with three modes: clean resort, cinematic coastal portrait, fashion campaign.
- **How to use:** Fill in the one-click brief (location, look, mood, target model, optional references); it returns the compiled prompt, avoid-list and QA notes.
- **Best suited for:** Swimwear, resort and poolside fashion imagery.

<a id="s-asset-continuity-imagegen"></a>
### asset-continuity-imagegen

[asset-continuity-imagegen.zip](asset-continuity-imagegen.zip) · entry: `asset-continuity-imagegen-v1.0.0/skills/asset-continuity-imagegen/SKILL.md`

- **What it does:** Keeps recurring characters, props, products, costumes, vehicles and locations recognisably the same across generated or edited images. Builds an asset registry (immutable anchors / controlled variables / free variables), writes shot contracts, enforces reference discipline and diagnoses and repairs drift.
- **How to use:** Provide reference images and ask for new shots, variations or multi-asset scenes, or ask it to fix an image that drifted. Uses the built-in image tool when available.
- **Best suited for:** Multi-image projects that need consistency — storyboards, product sets, character sheets.

<a id="s-character-asset-capture-kit"></a>
### character-asset-capture-kit

[character-asset-capture-kit.zip](character-asset-capture-kit.zip) · entry: `character-asset-capture-kit-v1.0.0/SKILL.md`

- **What it does:** Extracts a reusable character asset from an existing image, screenshot, reference set or video while preserving visible identity, body proportions, outfit, personal props and the original visual style — extraction, not redesign. Flow: scan → capture → normalise → package → reuse.
- **How to use:** Commands: `/人物提取` (extract a character record or cutout), `/人物资产` (build a full asset package or board), `/批量提取` (batch extract from video). Hidden areas stay marked as unconfirmed or as completion candidates.
- **Best suited for:** Turning a character that already exists in footage or art into a consistent asset for later generations.

<a id="s-fantasy-life-force-portrait-photography"></a>
### fantasy-life-force-portrait-photography

[fantasy-life-force-portrait-photography.zip](fantasy-life-force-portrait-photography.zip) · entry: `fantasy-life-force-portrait-photography-main/SKILL.md`

- **What it does:** "Life-force" portrait photography workflow: turns tourist snaps, casual phone shots or reference portraits into vivid, intimate, sun-lit, share-worthy portraits that feel like a photographer caught a real moment. Mode A upgrades a photo with strict identity lock, Mode C turns it into an atmospheric hero shot, Mode B creates original sample shots. Includes composition, face, hair, wardrobe and colour standards.
- **How to use:** Upload a photo and choose the mode, or describe a scene for an original. Reference images are analysed but never redrawn into someone else; public-figure features are de-identified.
- **Best suited for:** Making everyday portraits look like candid editorial photography for social posts.

<a id="s-fashion-shoot-twin"></a>
### fashion-shoot-twin

[fashion-shoot-twin.zip](fashion-shoot-twin.zip) · entry: `fashion-shoot-twin/SKILL.md`

- **What it does:** Rebuilds a photographer's shooting language for your garments: from style references (A), garment photos (B) and optional model (C) and location (D) references, it infers the photographer's light, lenses, composition, grading and set rhythm, builds a garment evidence map, and plans 6–8 new shots that look like the same photographer, same day, connected locations — while selling the clothes better. Routes to GPT Image or ComfyUI, with anchor → coverage → repair generation and three-level QC.
- **How to use:** Upload 4–12 style references plus front, back, side and detail garment shots. There is a single confirmation point before generation.
- **Best suited for:** Fashion e-commerce lookbook sets in a borrowed photographic style.

<a id="s-fidelity-4k-upscale-skill-v1-0"></a>
### fidelity-4k-upscale-skill-v1.0

[fidelity-4k-upscale-skill-v1.0.zip](fidelity-4k-upscale-skill-v1.0.zip) · entry: `fidelity-4k-upscale-skill-v1.0/SKILL.md`

- **What it does:** Pure fidelity upscaling: makes an image larger and clearer without changing anything — faces, text, logos, products, colours, even flaws and watermarks stay as they are. If sharpening would alter content, it keeps the original.
- **How to use:** Upload an image and ask for an HD / 4K / higher-resolution version. Requests to retouch, change backgrounds, remove watermarks or restyle are out of scope (use a retouching skill).
- **Best suited for:** Getting a high-resolution "archival copy" of an image that must stay identical.

<a id="s-guided-image-director"></a>
### guided-image-director

[guided-image-director.zip](guided-image-director.zip) · entry: `guided-image-director/SKILL.md`

- **What it does:** A decisive image director: converts vague intent into one coherent visual decision and writes it in language the target image model can execute. Routes silently between concept, reference-guided, production (ads, posters, covers, product), series and repair work; asks only when a missing fact would change the core subject.
- **How to use:** Describe what you want (with references if any) and the target model; it returns a strong recommendation and a compiled prompt, or a focused fix for an existing image.
- **Best suited for:** Getting confident creative direction instead of a menu of prompt options.

<a id="s-huazhao-portrait-director"></a>
### huazhao-portrait-director

[huazhao-portrait-director.zip](huazhao-portrait-director.zip) · entry: `huazhao-portrait-director-v5.0.0-public/SKILL.md` · `huazhao-portrait-director-v6.0.0-public/SKILL.md`

- **What it does:** "Huazhao portrait director" — a public black-box director for portrait shoots, Chinese-style (guofeng) and fashion portraits, identity- and costume-referenced images and series. Produces structured shot specs, reference-role assignment, camera and spatial logic, light/material constraints, a continuity ledger, QA and targeted repair decisions; it does not ship its private underlying prompts. The zip contains v5.0 and v6.0.
- **How to use:** Just describe the person, setting and what's happening (plus references). Use v6.0 (newer, adds tool-capability matching and shot-variation tables) unless you need v5. With an image tool available it generates and reviews; otherwise it delivers the spec.
- **Best suited for:** Credible, consistent portrait series with controlled identity and costume.

<a id="s-huazhao-portrait-engine"></a>
### huazhao-portrait-engine

[huazhao-portrait-engine.zip](huazhao-portrait-engine.zip) · entry: `huazhao-portrait-engine-v1.1.0/SKILL.md`

- **What it does:** "Huazhao Portrait System · Vitality 1.1" — treats Chinese-style portrait, hanfu and guofeng fashion image generation as a directed photo shoot built on separate controls for subject, action, space, light/material, vitality and series consistency. Modes cover text-only briefs, subject references and more.
- **How to use:** Describe the portrait or series, optionally with a person or costume reference; it outputs a shoot plan and generation prompts and can repair or extend existing images. See `QUICKSTART.md`.
- **Best suited for:** Hanfu / classical-beauty portraits where costume logic and realism both matter.

<a id="s-image-factory"></a>
### image-factory

[image-factory.zip](image-factory.zip) · entry: `image-factory-skill-v1.0.0/SKILL.md`

- **What it does:** Translates image requests, references, briefs, story beats or product requirements into structured prompts, shot plans, controlled variants, quality gates and targeted repair instructions. Splits every job into six layers (intent, scene, camera, look, constraints, QA/repair) and has domain recipes for film stills, photoreal portraits, products, anime/illustration, concept art, architecture/interiors and image editing.
- **How to use:** Describe the image you want (with references if any); it returns a compiled prompt plus variants, and after a bad result tells you which layer to fix.
- **Best suited for:** A general-purpose, model-agnostic image prompting workflow across many genres.

<a id="s-mj-aesthetic-lab-v2-0-0"></a>
### mj-aesthetic-lab-v2.0.0

[mj-aesthetic-lab-v2.0.0.zip](mj-aesthetic-lab-v2.0.0.zip) · entry: `mj-aesthetic-lab-v2.0.0/SKILL.md`

- **What it does:** Turns Midjourney into a controlled visual development lab ("search before freeze"): aesthetic upgrades, style search, prompt compiling, image critique and repair, controlled experiments, style-DNA consistency and character casting. Uses a 9-axis aesthetic scan, a three-lever rule, a 9-layer prompt compiler, anti-slop rules and an adapter for current Midjourney parameters (as of Aug 2026).
- **How to use:** Pick a mode (A–G) or just describe the image; works for portraits, cinematic stills, fashion, products, architecture, concept art, illustration and Niji. See `INSTALL.md`.
- **Best suited for:** Systematic Midjourney exploration and prompting.

<a id="s-nexuswear-persona-fashion-director"></a>
### nexuswear-persona-fashion-director

[nexuswear-persona-fashion-director.zip](nexuswear-persona-fashion-director.zip) · entry: `nexuswear-persona-fashion-director/SKILL.md`

- **What it does:** Designs the person-in-context first, then the clothes that make them believable: original trend-aware garments, T-shirts, full character styling, looks, capsule collections and lookbook/editorial prompts for male, female or unisex wearers, with consistent garment presentation.
- **How to use:** Describe the wearer, audience, setting, trend appetite and limits; it reconstructs intent, locks a persona and delivers garment designs plus image direction.
- **Best suited for:** Original apparel concepts and character wardrobes.

<a id="s-photoreal-face-asset-engine"></a>
### photoreal-face-asset-engine

[photoreal-face-asset-engine.zip](photoreal-face-asset-engine.zip) · entry: `photoreal-face-asset-engine-v1.1.0/SKILL.md`

- **What it does:** Builds an original or authorised photoreal human face as a long-term identity asset: generates genuinely diverse candidate faces, locks the chosen one into a mother identity with a fingerprint, edits parameters precisely, compiles a structure-and-skin-realism contract and produces multi-view asset sheets and a full character pack — with identity and realism gates. Adults only, photographic look.
- **How to use:** Follow the workflow in the SKILL.md: generate candidates → `lock` one → fine edits → compile → multi-view atlas → one-click asset pack. Scripts and schemas are included.
- **Best suited for:** A consistent, reusable photoreal character face for image and video projects.

<a id="s-pic-fix-oneshot"></a>
### pic-fix-oneshot

[pic-fix-oneshot.zip](pic-fix-oneshot.zip) · entry: `pic-fix-oneshot/SKILL.md`

- **What it does:** "Fix it in one go" image repair for comic storyboards, illustrations, posters and e-commerce images: health check → multi-round fixes (max three items per round, structure before detail) → re-check after each round → roll back or switch method if a fix fails → deliver the best version. Covers perspective/composition, AI artefacts, hands, face drift, props and multi-panel continuity.
- **How to use:** Upload the image (plus references) and use commands like "全修" (fix all), "只体检" (check only), "只修手" (hands only), "只修透视", "只修脸", "建档" (build an asset card), "连贯检查", "继续", "退回", "换个方法". Not for new creative images, video or real-person face swaps.
- **Best suited for:** Repairing AI-generated storyboard frames and illustrations without drifting.

<a id="s-portrait-retouch"></a>
### portrait-retouch

[portrait-retouch.zip](portrait-retouch.zip) · entry: `portrait-retouch-skill-v2.0.0/SKILL.md`

- **What it does:** Retouches existing AI or photographic portraits with a conversational image-edit model (GPT-style) so they look more attractive, alive and believable while keeping identity, age, anatomy, expression, pose, camera and scene. Fast triage of defects, an explicit edit contract (hard locks vs allowed changes), a human-realism stack (skin, eyes, lips, hair, scene integration, camera credibility) and beauty lift without identity drift.
- **How to use:** Upload the portrait and say what bothers you (or just "retouch this"). Modes: direct edit (default), prompt only, or no target image.
- **Best suited for:** Making a portrait look better and more human without becoming a different person.

<a id="s-public-character-continuity"></a>
### public-character-continuity

[public-character-continuity.zip](public-character-continuity.zip) · entry: `public-character-continuity-skill-v1.0.0/SKILL.md`

- **What it does:** A lightweight, reference-led way to keep an established character recognisable across image generations and edits: pick the best current reference, split the request into "preserve" vs "change", write concise change prompts, and follow a simple recovery order when the character drifts.
- **How to use:** Provide a reference image and ask for the same character in a new scene, outfit, pose, expression or angle. For heavier multi-asset work use `asset-continuity-imagegen`.
- **Best suited for:** Everyday "same character, new picture" requests.

<a id="s-realistic-social-selfie-retouch"></a>
### realistic-social-selfie-retouch

[realistic-social-selfie-retouch.zip](realistic-social-selfie-retouch.zip) · entry: `realistic-social-selfie-retouch/SKILL.md`

- **What it does:** Creates a six-part Xiaohongshu/Pinterest-style retouch plan and a Chinese AI image-edit prompt for a casual selfie: cleaner skin with real texture, better makeup, light and colour, and social-photo polish — while keeping the same person, face proportions, expression, pose, clothing, hair direction and scene.
- **How to use:** Upload a selfie and say e.g. "小红书网感精修", "Pinterest 自拍精修", "自然真实变美". Not for face swaps, body reshaping, scene replacement, cosplay or sexualised edits.
- **Best suited for:** Natural "same me, but better" social-media selfies.

<a id="s-style-composition-lora-forge"></a>
### style-composition-lora-forge

[style-composition-lora-forge.zip](style-composition-lora-forge.zip) · entry: `style-composition-lora-forge-v1.0.0/SKILL.md`

- **What it does:** Builds and validates style-focused LoRA training projects (e.g. one painter's oil works) while keeping composition controllable through a separate inference-time structure channel (ControlNet-style in ComfyUI): dataset curation and audit, captioning, pilot runs, backend starter files, validation matrix and winner selection.
- **How to use:** Bring a coherent set of reference images and your training backend; start from `BOOT.md`. ComfyUI workflows are included.
- **Best suited for:** Capturing a visual style in a LoRA when prompting alone can't reproduce it.

<a id="s-threadlock-wardrobe-skill-v1-0-0"></a>
### threadlock-wardrobe-skill-v1.0.0

[threadlock-wardrobe-skill-v1.0.0.zip](threadlock-wardrobe-skill-v1.0.0.zip) · entry: `threadlock-wardrobe-skill-v1.0.0/SKILL.md`

- **What it does:** Model-agnostic clothing asset system for anime and photoreal workflows: a garment is an asset with evidence and invariants, not prompt text. Modes EXTRACT, RECONSTRUCT (occluded parts without uncontrolled redesign), DESIGN, RENDER and VIDEO, with lock levels, backend routing and a continuity gate. Ships a Python package (`threadlock`) with a minimal CLI, schemas and tests.
- **How to use:** Give reference images of an outfit and say what you need — extract it, rebuild hidden parts, put the same outfit on another character, or keep it consistent across shots or video. See `README.md` for the CLI.
- **Best suited for:** Keeping outfits exactly consistent across characters, poses and shots.

<a id="s-wardrobe-extractor-skill-v1-0-0"></a>
### wardrobe-extractor-skill-v1.0.0

[wardrobe-extractor-skill-v1.0.0.zip](wardrobe-extractor-skill-v1.0.0.zip) · entry: `wardrobe-extractor-skill-v1.0.0/SKILL.md`

- **What it does:** Turns a reference image with one or more people or characters into a clean garment-and-accessory extraction sheet — photos, film stills, anime, manga, game art, concept art, historical costume, even low-res or partial images. Labels each detail as visible, strongly implied or unknown instead of inventing, handles layers and occlusion, and supports faithful or real-world-materialised modes.
- **How to use:** Upload the image and ask to "extract the outfit / costume". Multi-person images get one inventory per wearer.
- **Best suited for:** Pulling an outfit out of a reference image as a reusable sheet.

<a id="s-zhuangbi-portrait"></a>
### zhuangbi-portrait

[zhuangbi-portrait.zip](zhuangbi-portrait.zip) · entry: `zhuangbi-portrait/SKILL.md`

- **What it does:** "Status portrait" — makes a clearly adult subject look like they belong and have real access and influence, without flaunting wealth symbols (no supercars, diamonds or champagne). Each photo is built from one memorable "rumour", exactly two believable "access passes", a delayed reaction to something off-frame, deliberate visual silence, camera politics, facial distinction and lived-in material traces.
- **How to use:** Only on explicit request: `$zhuangbi-portrait`, "装逼写真", "排面写真", "有位置感", or "my photo looks rented / try-hard, redo it". Works from minimal input; reads its `cards/` in order.
- **Best suited for:** Powerful, understated status portraits instead of flex-template images.

<a id="s-zh-b5e804a7"></a>
### 刺猬星球superi的超级skill

[刺猬星球superi的超级skill.zip](%E5%88%BA%E7%8C%AC%E6%98%9F%E7%90%83superi%E7%9A%84%E8%B6%85%E7%BA%A7skill.zip) · *prompt-type* · entry: `人物skill.md`

- **What it does:** "Hedgehog Planet superi's Super Skill" — a creator-style skill that reproduces the account's realistic, cinematic Chinese period-drama look (guofeng costume, key-frame-of-a-drama feel, vertical framing) from plain-language requests, then turns a finished costume image into a 5-second story-style image-to-video prompt. Includes a creator style card, image and image-to-video workflows and adaptation notes for ChatGPT, Nano Banana Pro, Kling and Jimeng.
- **How to use:** Prompt-type: paste `人物skill.md` into your chat AI, then describe the scene in plain words or upload a generated costume image for the video prompt.
- **Best suited for:** Cinematic guofeng period-drama stills and short image-to-video clips.

<a id="s-zh-8fa780ee"></a>
### 古风短剧场景设计师

[古风短剧场景设计师.zip](%E5%8F%A4%E9%A3%8E%E7%9F%AD%E5%89%A7%E5%9C%BA%E6%99%AF%E8%AE%BE%E8%AE%A1%E5%B8%88.zip) · *prompt-type* · entry: `3x3场景_skill.md`

- **What it does:** "Ancient-style Short Drama Scene Designer" — generates film-grade scene prompts for female-oriented costume short dramas: a 3×3 grid covering exterior, courtyard, entrance, interior wide, main seat, borrowed views, furniture details, prop close-ups and floor plan / aerial layout. Asks guided questions (scene type, character status, plot function, dynasty aesthetic, visual hook, season/time, mood, output mode). Scene images only, no video prompts.
- **How to use:** Prompt-type: paste `3x3场景_skill.md` into your chat AI and answer its questions. Designed to work with the character skill (`刺猬星球superi的超级skill`) and the short-drama scriptwriting skill (`微短剧剧本创作`).
- **Best suited for:** Consistent set design references for costume short dramas.

<a id="cat-aesthetics"></a>
## Visual style analysis & reverse prompting

Working out why a reference looks the way it does and turning it into reusable prompts.

| Skill | Best suited for |
|---|---|
| [`aesthetic-stress-extractor`](#s-aesthetic-stress-extractor) | Understanding and faithfully recreating a cinematic look before prompting an image model. |
| [`cinematic-style-compiler`](#s-cinematic-style-compiler) | Replicating a whole film's visual system across new shots, not just one frame. |
| [`color-dna-card-extractor`](#s-color-dna-card-extractor) | Turning a reference frame into a reusable palette for film art, AI video, characters, scenes or brand boards. |
| [`photographic-atmosphere-reconstruction`](#s-photographic-atmosphere-reconstruction) | Matching a photographic colour grade and mood on new images. |
| [`reference-rendering-reader`](#s-reference-rendering-reader) | Borrowing a visual treatment for new subjects without copying the content. |
| [`reverse-anything`](#s-reverse-anything) | Extracting reusable templates from content or sites you admire. |
| [`strong-image-reverse-prompt`](#s-strong-image-reverse-prompt) | Image-to-prompt for faithful recreation and controlled edits. |

<a id="s-aesthetic-stress-extractor"></a>
### aesthetic-stress-extractor

[aesthetic-stress-extractor.zip](aesthetic-stress-extractor.zip) · entry: `aesthetic-stress-extractor/SKILL.md`

- **What it does:** Finds what actually makes a film frame's look work by stress-testing it: weakens one visual condition at a time (colour, tonal range, balance, quiet zones, detail, focal attention), judges whether the look survives, ranks the sensitivities and outputs a "minimum survival set", a safe-to-vary list and a compact reconstruction brief. Includes lab scripts and forms.
- **How to use:** Give it one frame (Quick Sweep) or several frames (Set Run) and ask what the look depends on or for a reconstruction prompt. It can also diagnose a generated image against the reference. It will not guess camera gear or a whole film's style from one frame.
- **Best suited for:** Understanding and faithfully recreating a cinematic look before prompting an image model.

<a id="s-cinematic-style-compiler"></a>
### cinematic-style-compiler

[cinematic-style-compiler.zip](cinematic-style-compiler.zip) · entry: `cinematic-style-compiler/SKILL.md`

- **What it does:** Builds an explainable FILM_AESTHETIC_MODEL from multiple stills or clips of a film, series, short drama or ad (ten-axis per-shot analysis, narrative phases, shot-function grammar, linked anchors), then compiles it into a REPLICATION_SPEC for new content and checks similarity afterwards.
- **How to use:** Give several frames or clips and ask to "extract the film's aesthetic anchors", "analyse its shot grammar" or "transfer this film's look to my new scenes", or ask why a generated image only matches the colour. Not for a single final prompt, strict single-image copies or simple colour grading.
- **Best suited for:** Replicating a whole film's visual system across new shots, not just one frame.

<a id="s-color-dna-card-extractor"></a>
### color-dna-card-extractor

[color-dna-card-extractor.zip](color-dna-card-extractor.zip) · entry: `COLOR-DNA-CARD-EXTRACTOR-v1.0/SKILL.md`

- **What it does:** Extracts a functional, film/design-grade colour system from a single reference image — light colour vs material colour, value hierarchy and small but meaningful accent colours, each with a functional name — and compiles it into a prompt that generates a professional colour-card presentation page.
- **How to use:** Give one image; optionally project name, card size (6, 9 or 13 colours — 13 by default), use case and title language. Outputs the extraction results plus a ready image-generation prompt (16:9 flat Figma-style board by default).
- **Best suited for:** Turning a reference frame into a reusable palette for film art, AI video, characters, scenes or brand boards.

<a id="s-photographic-atmosphere-reconstruction"></a>
### photographic-atmosphere-reconstruction

[photographic-atmosphere-reconstruction.zip](photographic-atmosphere-reconstruction.zip) · entry: `photographic-atmosphere-reconstruction/SKILL.md`

- **What it does:** Reverse-engineers why a photo looks the way it does — tonal order, overall colour bias, colour relationships, contrast response, material feel and air — and rewrites it as transferable grading and atmosphere instructions. Works from one reference, a set (finding the stable shared look) or reference + target, and diagnoses "the colours match but it doesn't feel the same". Protects skin tones.
- **How to use:** Give one or more reference photos (plus a target image if transferring) and ask to extract, transfer, compare or diagnose the look. Ask for "just the prompt" to skip the analysis.
- **Best suited for:** Matching a photographic colour grade and mood on new images.

<a id="s-reference-rendering-reader"></a>
### reference-rendering-reader

[reference-rendering-reader.zip](reference-rendering-reader.zip) · entry: `reference-rendering-reader/SKILL.md`

- **What it does:** Careful single-image style reader: separates what the image depicts (to ignore) from transferable rendering decisions — composition, line and edge, shading, light, surface, detail distribution, colour and tonal relationships — and returns a reusable style prompt, a style-restriction prompt and a reliability note. Avoids guessing identity, author or production technique.
- **How to use:** Upload one reference and say "extract this style" / "提取画风" / "image to style prompt".
- **Best suited for:** Borrowing a visual treatment for new subjects without copying the content.

<a id="s-reverse-anything"></a>
### reverse-anything

[reverse-anything.zip](reverse-anything.zip) · entry: `reverse-anything/SKILL.md` · `reverse-anything__不同内容_0d88a8ba/SKILL.md`

- **What it does:** "Reverse anything": turns great work into something you can reuse. For images and videos it derives the master prompt (fixed skeleton, variable slots, style anchors, effective parameters); for a benchmark website it breaks down positioning, features, flows and tech stack and gives build options plus step-by-step vibe-coding prompts. Every conclusion is labelled evidence / inference / guess. The zip contains v1.0 and v2.0 (evidence-driven, also covers products and workflows, with reproduction checks).
- **How to use:** Give a set of prompts, a prompt + result, just a result, or a URL ("reverse this image's prompt", "how is this site built?", "I want a product like X"). Hermes-style skill; scripts in `scripts/`. Prefer v2.0.
- **Best suited for:** Extracting reusable templates from content or sites you admire.

<a id="s-strong-image-reverse-prompt"></a>
### strong-image-reverse-prompt

[strong-image-reverse-prompt.zip](strong-image-reverse-prompt.zip) · entry: `strong-image-reverse-prompt/SKILL.md`

- **What it does:** Turns one or more reference images into clear, high-control generation or editing prompts — recreating a composition, keeping a product or identity while changing the setting, or comparing references — with each image assigned a role (subject, style, layout, comparison). Outputs a fast brief or a production brief with a visual fingerprint, ready prompt, control notes and model adaptations (GPT Image, Midjourney, Flux, SDXL).
- **How to use:** Upload the image(s) and say "reverse this into a prompt" or "recreate this layout with my product".
- **Best suited for:** Image-to-prompt for faithful recreation and controlled edits.

<a id="cat-image3d"></a>
## 3D & product rendering

3D asset look-dev and e-commerce product renders.

| Skill | Best suited for |
|---|---|
| [`3d-high-fidelity-asset-forge-skill-v2.1.0`](#s-3d-high-fidelity-asset-forge-skill-v2-1-0) | Extending an existing stylized 3D animated world with new assets that must match it exactly. |
| [`ecommerce-3d-render-assistant`](#s-ecommerce-3d-render-assistant) | Product shots for phones, tablets, earbuds, peripherals, cameras, chargers and wearables. |

<a id="s-3d-high-fidelity-asset-forge-skill-v2-1-0"></a>
### 3d-high-fidelity-asset-forge-skill-v2.1.0

[3d-high-fidelity-asset-forge-skill-v2.1.0.zip](3d-high-fidelity-asset-forge-skill-v2.1.0.zip) · entry: `3d-high-fidelity-asset-forge-skill-v2.1.0/SKILL.md`

- **What it does:** Locks the look of a reference 3D animation (video or frames) as the top authority, then produces new characters, environments, props and asset sheets that look like they were lifted from the same high-end animated film. Runs a staged pipeline (ingest → style authority → class split → lookdev → prompt compile → style gates → QA) and ships with schemas, scripts and tests.
- **How to use:** Start with `START-HERE.md`. Give it the reference video or frames plus the list of assets you need; it returns lookdev notes and generation prompts, then checks each result against style gates (no drift into photoreal CG, game art or "generic 3D cartoon").
- **Best suited for:** Extending an existing stylized 3D animated world with new assets that must match it exactly.

<a id="s-ecommerce-3d-render-assistant"></a>
### ecommerce-3d-render-assistant

[ecommerce-3d-render-assistant.zip](ecommerce-3d-render-assistant.zip) · entry: `ecommerce-3d-render-skill-public-v1.0.0/SKILL.md`

- **What it does:** E-commerce product rendering helper for existing 3D models or base renders: improves materials, lighting, reflections, studio backdrops and finish while locking product structure and camera. Auto-identifies materials (anodised, brushed or polished metal, glass, optics, plastics, rubber, ceramic, fabric) and offers five presets (white marketplace, premium white studio, dark tech, etc.).
- **How to use:** Give a Blender/C4D/KeyShot scene, a clay or base render, or just a text description. Saying only "make it look premium" uses a sensible default and returns a copy-ready prompt; with a scene it returns material, lighting and render settings.
- **Best suited for:** Product shots for phones, tablets, earbuds, peripherals, cameras, chargers and wearables.

<a id="cat-marketing"></a>
## Ads, product demos & slides

Posters, story ads, product demo videos and slide backgrounds.

| Skill | Best suited for |
|---|---|
| [`beetle-poster-director`](#s-beetle-poster-director) | Concept-led ad posters that are more surprising than a product-in-use scene. |
| [`build-product-demo`](#s-build-product-demo) | Polished software demo videos that show every key capability without a slow feature tour. |
| [`narrative-ad-engine`](#s-narrative-ad-engine) | Short-video ads that keep viewers watching through the product reveal. |
| [`slides`](#s-slides) | Background slides for voice-over / talking-head videos. |

<a id="s-beetle-poster-director"></a>
### beetle-poster-director

[beetle-poster-director.zip](beetle-poster-director.zip) · entry: `beetle-poster-director-v2.6.0/SKILL.md`

- **What it does:** "Beetle-style poster creative director" — turns a real product, brand, service, event or idea into a finished advertising poster in the spirit of classic VW Beetle ads: visual proof over literal product shots, self-deprecating copy, negative-to-positive reframing, clean white space. Verifies the product online, builds a product fact ledger, writes a creative contract and runs reading tests. The job isn't done until the poster image is generated.
- **How to use:** It first asks you to choose A (co-create, confirm each step) or B (full takeover). Then give the product name, brand, images or a product link. Web search is mandatory. Install with the bundled `install.sh`.
- **Best suited for:** Concept-led ad posters that are more surprising than a product-in-use scene.

<a id="s-build-product-demo"></a>
### build-product-demo

[build-product-demo.zip](build-product-demo.zip) · entry: `spellbook-main/skills/build-product-demo/SKILL.md`

- **What it does:** Plans, produces or diagnoses evidence-backed product demo videos and screen-recorded walkthroughs. Treats the demo as a verifiable claim about the product: evidence inventory, feature coverage, director's treatment, script, beat plan, deterministic capture tooling, pacing edit and final verification. Diagnose mode finds the first broken layer (truth, story, visible state change, narration sync, capture, encoding).
- **How to use:** Ask for a product demo, launch video, feature showcase or app walkthrough, or "fix the dead time / narration pacing in this demo". Pick Plan, Produce or Diagnose mode.
- **Best suited for:** Polished software demo videos that show every key capability without a slow feature tour.

<a id="s-narrative-ad-engine"></a>
### narrative-ad-engine

[narrative-ad-engine.zip](narrative-ad-engine.zip) · entry: `narrative-ad-engine-v1.1.0/SKILL.md`

- **What it does:** Generates high-retention story ads: original short-drama ads, movie-recap-style commercial placements, UGC narrative ads and conversion scripts, keeping attention → curiosity → desire → choice → product value → action on one causal chain. Modes: CREATE (from product only), RECAP, GRAFT (add commerce to an existing story), DIAGNOSE, VARIANT (A/B directions).
- **How to use:** Give just the product to auto-run, or supply an existing plot or recap script. Beginners should start with `START-HERE.md`. Targets Douyin/TikTok, Reels, Shorts, Bilibili and Xiaohongshu.
- **Best suited for:** Short-video ads that keep viewers watching through the product reveal.

<a id="s-slides"></a>
### slides

[slides.zip](slides.zip) · entry: `spellbook-main/skills/slides/SKILL.md`

- **What it does:** Generates slide decks as 16:9 PNG sequences. Voice-over mode (default, 20–40 pages) makes minimalist one-idea-per-slide backgrounds for talking-head videos, with 13 background themes, semantic colour emphasis, content-type strategies (person, tutorial, news, opinion) and a thumbnail-style cover system. Presentation mode (5–8 pages) makes richer card-based slides.
- **How to use:** Run with a topic or script file path, e.g. "make slides for this voice-over script".
- **Best suited for:** Background slides for voice-over / talking-head videos.

<a id="cat-social"></a>
## Social media & creator operations

Xiaohongshu and multi-platform content, topic selection and native-sounding Chinese copy.

| Skill | Best suited for |
|---|---|
| [`creator-ops-os`](#s-creator-ops-os) | Planning and iterating content for a creator account with data, not guesswork. |
| [`topic-insight-writing`](#s-topic-insight-writing) | Creators who don't know what to write or whose pieces keep drifting off-point. |
| [`xiaohongshu`](#s-xiaohongshu) | Researched, illustrated Xiaohongshu posts from topic to publish. |
| [`xiaohongshu-netfeel-guardian`](#s-xiaohongshu-netfeel-guardian) | Making Chinese social posts sound native, not translated. |

<a id="s-creator-ops-os"></a>
### creator-ops-os

[creator-ops-os.zip](creator-ops-os.zip) · entry: `creator-ops-os-v1.0.0/SKILL.md`

- **What it does:** Runs a creator account as an evidence-driven system: live market evidence and your own account metrics → topic board → platform-native content package → preflight → publishing brief → performance diagnosis → learning memory. Strongest for Xiaohongshu and Douyin; also Bilibili, Kuaishou, WeChat Official Accounts, Weibo, Zhihu, TikTok, YouTube, Instagram and X. Never invents market data.
- **How to use:** Choose a mode (e.g. QUICK_SHOT for 3–5 topics and one finished package, MARKET_SCAN for a wider sweep). Provide your niche, account data exports if available, and target platform.
- **Best suited for:** Planning and iterating content for a creator account with data, not guesswork.

<a id="s-topic-insight-writing"></a>
### topic-insight-writing

[topic-insight-writing.zip](topic-insight-writing.zip) · entry: `topic-insight-writing-skill-v1.0.0/SKILL.md`

- **What it does:** Precise topic selection for self-media: audience context → real signals → pain point → concrete candidate topics → sharpened thesis → counter-examples and fact checks → discussion to lock one topic → structure → section-by-section writing → final fact and expression review. Works for video, posts and podcasts; won't write the full piece before you agree on the topic unless you ask.
- **How to use:** Say "give me topics", "I have a vague idea but can't articulate the point", or "make an episode about X". It returns 2–3 genuinely different topic cards and one key question to decide on.
- **Best suited for:** Creators who don't know what to write or whose pieces keep drifting off-point.

<a id="s-xiaohongshu"></a>
### xiaohongshu

[xiaohongshu.zip](xiaohongshu.zip) · entry: `spellbook-main/skills/xiaohongshu/SKILL.md`

- **What it does:** End-to-end Xiaohongshu (RED) note production: understand the brief → competitor research saved to a local database → 8–10 tags → generate 3:4 (1080×1440) cover and content images from HTML styles with overflow checks → write copy within platform limits (title ≤20 characters, body ≤1000) → publish → verify. Each note lives in its own `YYYYMMDD-<slug>` folder.
- **How to use:** Run with a topic or source material ("write a Xiaohongshu post about our new feature"). Copy `.env.example` to `.env` and install `requirements.txt`; publishing needs the configured posting tool.
- **Best suited for:** Researched, illustrated Xiaohongshu posts from topic to publish.

<a id="s-xiaohongshu-netfeel-guardian"></a>
### xiaohongshu-netfeel-guardian

[xiaohongshu-netfeel-guardian.zip](xiaohongshu-netfeel-guardian.zip) · entry: `spellbook-main/skills/xiaohongshu-netfeel-guardian/SKILL.md`

- **What it does:** Fixes translation-ese in Chinese content written by Claude — stiff phrasing, Western framing, "In conclusion"-style drift halfway through long pieces. Forces a Chinese-only planning monologue first, detects English leakage in the draft, rewrites with authentic online tone, produces versions with a final self-check and can generate a persistent guard snippet. Leaves your existing CLAUDE.md / AGENTS.md persona rules intact.
- **How to use:** Say "小红书翻译腔太重", "去除 Claude 翻译腔", "公众号写着写着变英文了", or paste a note to rewrite in natural Chinese. Works best together with `xiaohongshu`.
- **Best suited for:** Making Chinese social posts sound native, not translated.

<a id="cat-writing"></a>
## Writing, author voice & de-AI polish

Writing in a specific author's voice and removing machine-written patterns.

| Skill | Best suited for |
|---|---|
| [`author-style-continuation`](#s-author-style-continuation) | Continuations and fan fiction that must sound like the original author. |
| [`cat-distillation-skill`](#s-cat-distillation-skill) | Building a reusable writing partner from a specific creator's body of work (fiction, scripts, columns, marketing copy). |
| [`humanizer`](#s-humanizer) | Final polish of drafts that read as machine-written. |
| [`magic-style-dna`](#s-magic-style-dna) | Long-form articles, columns and voice-over scripts in a consistent personal voice. |

<a id="s-author-style-continuation"></a>
### author-style-continuation

[author-style-continuation.zip](author-style-continuation.zip) · entry: `author-style-continuation/SKILL.md`

- **What it does:** Learns an author's voice from source text or chat logs and continues in it — next chapter, side story, ending, character replies or chat-style continuations. Builds a style card, character voice cards, a plot ledger and a plan, then uses stdlib Python scripts to fingerprint the style, compare drafts against the original and flag AI-sounding phrasing.
- **How to use:** Paste or attach the original text and say what to write ("continue in the author's voice", "接着往下写"). Works in Chinese and English; installing `jieba` improves Chinese analysis.
- **Best suited for:** Continuations and fan fiction that must sound like the original author.

<a id="s-cat-distillation-skill"></a>
### cat-distillation-skill

[cat-distillation-skill.zip](cat-distillation-skill.zip) · entry: `cat-distillation-skill-v1.0.1-STABLE/SKILL.md`

- **What it does:** "Cat Distillation" — compiles authorised novels, scripts, articles, interviews, chats and work material into a runnable creative collaborator. It learns traceable "pawprint atoms" (what the author notices first, how they judge, what move they make, what effect it has, when not to use it), contrasted against weak samples and genre norms. Run modes: MAKE (create), REWORK (edit), PLAN, TALK. Explicitly does not claim to clone a person.
- **How to use:** Feed it authorised material from a writer, then ask it to write, rework or plan in that person's creative manner. Missing evidence is flagged rather than invented.
- **Best suited for:** Building a reusable writing partner from a specific creator's body of work (fiction, scripts, columns, marketing copy).

<a id="s-humanizer"></a>
### humanizer

[humanizer.zip](humanizer.zip) · entry: `spellbook-main/skills/humanizer/SKILL.md`

- **What it does:** Removes signs of AI-generated writing based on Wikipedia's "Signs of AI writing" guide — inflated symbolism, promotional tone, shallow "-ing" analysis, vague attributions, em-dash overuse, rule of three, AI vocabulary, negative parallelisms — while keeping meaning and voice.
- **How to use:** Point it at a text or file and ask to make it sound human / natural.
- **Best suited for:** Final polish of drafts that read as machine-written.

<a id="s-magic-style-dna"></a>
### magic-style-dna

[magic-style-dna.zip](magic-style-dna.zip) · entry: `magic-style-dna-v1.0.0/SKILL.md`

- **What it does:** "Magic Style · Writing DNA" — learns observable writing patterns from an author's own articles (as a "writing transfer map": situation → choice → reader effect → evidence) and writes new, original articles that read like that author, plus titles, openings and cover text. Iterates the style pack from your feedback; includes offline analysis scripts. Refuses to impersonate a real author for deception.
- **How to use:** Put sample articles in `samples/`, let it build the style pack, then give a topic and facts for a new piece. Say "this part doesn't sound like them" to refine.
- **Best suited for:** Long-form articles, columns and voice-over scripts in a consistent personal voice.

<a id="cat-research"></a>
## Research, search & intelligence

Web search tools, research methods, industry and AI news intelligence, explainers.

| Skill | Best suited for |
|---|---|
| [`ai-intel-officer`](#s-ai-intel-officer) | Staying current on AI releases with verified sources and no hype. |
| [`anysearch`](#s-anysearch) | Giving an agent that lacks built-in web search a search-and-extract tool. |
| [`ask-opencli`](#s-ask-opencli) | Quick second opinions from Grok or Gemini without API keys. |
| [`consulting-analysis`](#s-consulting-analysis) | Formal market, industry or competitor reports with a clear analytical framework. |
| [`github-trending`](#s-github-trending) | Spotting genuinely rising open-source projects and tech trends. |
| [`industry-intelligence-engine`](#s-industry-intelligence-engine) | Getting up to speed on an unfamiliar industry before a business decision. |
| [`multi-ai-research`](#s-multi-ai-research) | Deep research where independent agreement matters more than a single deep answer. |
| [`research-guide`](#s-research-guide) | Rigorous, well-cited research. |
| [`research-hub`](#s-research-hub) | One front door for all research requests when you have the full research skill set installed. |
| [`universal-research-architect`](#s-universal-research-architect) | Any research question where you want a method, not just links. |
| [`universal-web-harvester`](#s-universal-web-harvester) | Reliable content collection from websites, including dynamic ones. |
| [`xray`](#s-xray) | Evidence-backed explainers of complex systems for yourself or a team. |

<a id="s-ai-intel-officer"></a>
### ai-intel-officer

[ai-intel-officer.zip](ai-intel-officer.zip) · entry: `ai-intel-officer-v1.0.0/SKILL.md`

- **What it does:** High-signal AI news and intelligence built on primary sources (release notes, papers, repos, pricing pages) rather than influencers, with a hard no-X/Twitter rule. Verifies claims, dedupes and ranks. Modes: Daily Brief, Weekly Radar, Verification Desk, Open-source Scout, Pricing & Quota Watch.
- **How to use:** Ask "give me today's AI brief", "weekly radar on agent tooling", "verify this rumour about model X", or "track API pricing and deprecations". Needs web access.
- **Best suited for:** Staying current on AI releases with verified sources and no hype.

<a id="s-anysearch"></a>
### anysearch

[anysearch.zip](anysearch.zip) · entry: `大调查/anysearch.md`

- **What it does:** Real-time search through the AnySearch service — web search, vertical-domain search, parallel batch search and URL-to-Markdown extraction — via a bundled cross-platform CLI (no MCP server). This package (`大调查` / "big investigation") also bundles the `consulting-analysis`, `research-guide` and `research-hub` companion files.
- **How to use:** Install the folder; the agent calls the CLI whenever it needs live information. Optional `ANYSEARCH_API_KEY` (in `.env` or env var) raises rate limits; anonymous use works. Run the CLI's `doc` command if the interface is unclear.
- **Best suited for:** Giving an agent that lacks built-in web search a search-and-extract tool.

<a id="s-ask-opencli"></a>
### ask-opencli

[ask-opencli.zip](ask-opencli.zip) · entry: `spellbook-main/skills/ask-opencli/SKILL.md`

- **What it does:** Asks Grok or Gemini through `opencli`, which drives your already-logged-in Chrome — no API cost.
- **How to use:** Setup: `npm install -g @jackwener/opencli` (Node ≥20), run `opencli doctor` to install the Chrome bridge extension, log in to grok.com and gemini.google.com once, and set `OPENCLI_BROWSER_COMMAND_TIMEOUT=300`. Then say "ask Grok …" / "问 gemini …". For multi-model research use `multi-ai-research`.
- **Best suited for:** Quick second opinions from Grok or Gemini without API keys.

<a id="s-consulting-analysis"></a>
### consulting-analysis

[consulting-analysis.zip](consulting-analysis.zip) · entry: `大调查/consulting-analysis.md`

- **What it does:** Produces consulting-grade research reports in Markdown — market, consumer, brand, financial, industry, competitive intelligence, investment due diligence. Phase 1 designs the analysis framework (models, chapter skeleton, per-chapter data requirements, chart plan); Phase 2, after data is collected, writes the final report with structured narrative, embedded charts and strategic insights. Strict data-authenticity rules.
- **How to use:** Ask for a research report on a subject. Pair with a search/collection skill (`anysearch`, `research-hub`) between the two phases. Ships inside the same `大调查` bundle as `anysearch`; entry is `大调查/consulting-analysis.md`.
- **Best suited for:** Formal market, industry or competitor reports with a clear analytical framework.

<a id="s-github-trending"></a>
### github-trending

[github-trending.zip](github-trending.zip) · entry: `spellbook-main/skills/github-trending/SKILL.md`

- **What it does:** GitHub Trending exploration and analysis that treats the list as hype-polluted: pulls structured data via a script (never raw HTML), filters for real star growth and writes a genuine angle for each pick. Produces daily/weekly trend reports by language or topic.
- **How to use:** Ask "what's hot on GitHub today?", "trending Rust projects this week", or "AI/agent trending report". Install the script dependencies from `requirements.txt`. Turning results into posts or deep research belongs to other skills.
- **Best suited for:** Spotting genuinely rising open-source projects and tech trends.

<a id="s-industry-intelligence-engine"></a>
### industry-intelligence-engine

[industry-intelligence-engine.zip](industry-intelligence-engine.zip) · entry: `industry-intelligence-engine/SKILL.md`

- **What it does:** Turns one industry name ("pet funerals", "industrial robots", "how do short dramas make money?") into an evidence-backed model of how the industry really works: who pays whom, where margins and power sit, what drives demand, what's changing now, where the frictions and opportunities are, and an entry playbook — checked against counter-evidence.
- **How to use:** Name an industry and your decision (understand it, enter it, invest, partner). Needs web research; outputs a structured industry reality model and recommendations.
- **Best suited for:** Getting up to speed on an unfamiliar industry before a business decision.

<a id="s-multi-ai-research"></a>
### multi-ai-research

[multi-ai-research.zip](multi-ai-research.zip) · entry: `spellbook-main/skills/multi-ai-research/SKILL.md`

- **What it does:** Parallel multi-AI cross-validation research: decomposes the question, dispatches several internal sub-agents plus Grok and Gemini (via opencli) at once, cross-validates the answers, tiers findings by confidence (strong consensus / partial / conflict / insufficient) and generates tiered action items with arbitration.
- **How to use:** Say "multi-AI research on …", "cross-validate this", "三脑调研". Requires opencli set up as in `ask-opencli`. Not for quick facts or code reasoning.
- **Best suited for:** Deep research where independent agreement matters more than a single deep answer.

<a id="s-research-guide"></a>
### research-guide

[research-guide.zip](research-guide.zip) · entry: `大调查/research-guide.md`

- **What it does:** The research "conductor": classifies intent (fact, comparison, trend, system modelling, exploratory), calibrates depth (L1–L3), and enforces source hierarchy, an iterative evidence loop, conflict resolution, cross-validation and citation standards, routing deliverables (reports, competitive analyses) to sub-skills.
- **How to use:** Activates for searching, fact-finding, comparisons and evidence-based deliverables. Part of the `大调查` bundle with `anysearch`, `consulting-analysis` and `research-hub`; entry is `大调查/research-guide.md`.
- **Best suited for:** Rigorous, well-cited research.

<a id="s-research-hub"></a>
### research-hub

[research-hub.zip](research-hub.zip) · entry: `大调查/research-hub.md`

- **What it does:** A unified search-and-research entry point that only routes: scores intent and sends the request to `anysearch`, `research-guide`, `consulting-analysis`, or video-download / book-ingest / knowledge-search / knowledge-ingest sub-skills, choosing a quick, semi-formal or deep-research channel with confidence labels and citation rules.
- **How to use:** Say "search / look up / research / analyse / write a report / download this video / import this book". Several referenced sub-skills (video-download, book-ingest, knowledge-*) are not in this repo. Entry is `大调查/research-hub.md`.
- **Best suited for:** One front door for all research requests when you have the full research skill set installed.

<a id="s-universal-research-architect"></a>
### universal-research-architect

[universal-research-architect.zip](universal-research-architect.zip) · entry: `universal-research-architect/SKILL.md`

- **What it does:** Turns a one-sentence question into a defensible research process and deliverable — research reports, questionnaire or interview design, market or industry analysis, renovation or project research, product/vendor comparisons, literature reviews, fact-checks. Chooses the method before chasing answers, sets depth (fast / standard / deep), tracks evidence states and stops intelligently.
- **How to use:** Ask in plain language ("research how to renovate my flat on a 150k budget", "design a canteen satisfaction survey", "is this claim true?"). Beginners can start with `START-HERE.md`.
- **Best suited for:** Any research question where you want a method, not just links.

<a id="s-universal-web-harvester"></a>
### universal-web-harvester

[universal-web-harvester.zip](universal-web-harvester.zip) · entry: `universal-web-harvester-v2.1.0-PURE/SKILL.md`

- **What it does:** Adaptive website harvesting for Codex: crawls, scrapes, downloads, archives and structures content from public pages, JavaScript-heavy sites, paginated listings and files, and sites you are authorised to log into. Probes first, picks the cheapest route that works, escalates to a browser only when needed, handles media, galleries and stylesheets, and verifies output before reporting.
- **How to use:** Say "scrape / archive / download everything from this site" with the URL and what you want. Install the core, browser and archive requirements as needed (`INSTALL.md`); respects access boundaries.
- **Best suited for:** Reliable content collection from websites, including dynamic ones.

<a id="s-xray"></a>
### xray

[xray.zip](xray.zip) · entry: `spellbook-main/skills/xray/SKILL.md`

- **What it does:** Investigates how something actually works — a concept, code path, app, network flow, system, incident, document or local artifact — then delivers a two-depth visual HTML explainer: a dead-simple big picture first, with source-backed technical depth behind it. Research comes first; the page is a projection of verified understanding. Safe, read-only static inspection of apps you're entitled to analyse.
- **How to use:** Invoke `$xray` or ask "how does X work under the hood?" / "trace this request across services and explain it". Not for one-line definitions or full code audits.
- **Best suited for:** Evidence-backed explainers of complex systems for yourself or a team.

<a id="cat-product"></a>
## Ideas, product management & strategy

Brainstorming, idea stress-tests, PRDs, discovery, analytics and thinking frameworks.

| Skill | Best suited for |
|---|---|
| [`brainstorming`](#s-brainstorming) | Turning a rough idea into a clear design through dialogue. |
| [`elon-musk-perspective`](#s-elon-musk-perspective) | Cost breakdowns, challenging industry assumptions and aggressive-but-iterable plans. |
| [`idea-analogist`](#s-idea-analogist) | Fresh angles on an idea from other fields. |
| [`idea-devils-advocate`](#s-idea-devils-advocate) | Stress-testing an idea before investing in it. |
| [`idea-research`](#s-idea-research) | A factual baseline for an idea. |
| [`idea-team`](#s-idea-team) | Quickly seeing an idea from several angles before committing. |
| [`idea-to-product`](#s-idea-to-product) | Turning a raw idea into a scoped, user-friendly MVP definition. |
| [`infinite-canvas-function-architect`](#s-infinite-canvas-function-architect) | Making sense of a sprawling feature set and seeing what's missing. |
| [`prd-master`](#s-prd-master) | Clear, measurable product requirements documents. |
| [`product-analytics`](#s-product-analytics) | Setting up product metrics and experiments correctly. |
| [`product-discovery`](#s-product-discovery) | Deciding what is worth building before building it. |
| [`product-manager-toolkit`](#s-product-manager-toolkit) | Hands-on PM work that benefits from quick scripts. |
| [`creative-ideation（网页脑洞）`](#s-zh-f33b17b8) | Breaking out of generic ideas for stories, settings, products or campaigns in a plain chat window. |

<a id="s-brainstorming"></a>
### brainstorming

[brainstorming.zip](brainstorming.zip) · entry: `spellbook-main/skills/brainstorming.SKILL.md`

- **What it does:** Socratic design refinement (from obra/superpowers): understands the idea by asking one question at a time, explores 2–3 approaches with a recommendation, then presents the design incrementally while cutting anything not needed (YAGNI).
- **How to use:** Say "let's brainstorm X", "help me design this feature" or "think through the architecture with me" before any code is written. Not for mechanical tasks with an obvious implementation. Entry file is `skills/brainstorming.SKILL.md` inside the spellbook bundle.
- **Best suited for:** Turning a rough idea into a clear design through dialogue.

<a id="s-elon-musk-perspective"></a>
### elon-musk-perspective

[elon-musk-perspective.zip](elon-musk-perspective.zip) · entry: `elon-musk-skill/SKILL.md`

- **What it does:** An Elon Musk "thinking OS" distilled from biographies, podcasts, posts, court testimony and critics: five mental models (asymptotic-limit thinking, the five-step algorithm, existential anchoring, vertical integration as physics, iterate fast), eight decision heuristics and his expression style. Answers in first person after a one-time disclaimer.
- **How to use:** Say "use Musk's perspective", "what would Musk think", "first principles on this cost" or "idiot index". Say "exit" / "退出" to leave the role. Weak at politics, empathy-heavy problems and timelines.
- **Best suited for:** Cost breakdowns, challenging industry assumptions and aggressive-but-iterable plans.

<a id="s-idea-analogist"></a>
### idea-analogist

[idea-analogist.zip](idea-analogist.zip) · entry: `spellbook-main/skills/idea-analogist/SKILL.md` · `spellbook-main/plugins/idea-coach/skills/idea-analogist/SKILL.md`

- **What it does:** The "analogist" role of the idea group chat: cross-industry analogies and yes-and expansion only — no judging, nitpicking or demands for evidence. Used by `idea-team` or on its own.
- **How to use:** Say "give me analogies", "has another industry done this?", "yes-and this idea" or "跨界启示". Standalone it returns 5–7 cross-domain analogies.
- **Best suited for:** Fresh angles on an idea from other fields.

<a id="s-idea-devils-advocate"></a>
### idea-devils-advocate

[idea-devils-advocate.zip](idea-devils-advocate.zip) · entry: `spellbook-main/skills/idea-devils-advocate/SKILL.md` · `spellbook-main/plugins/idea-coach/skills/idea-devils-advocate/SKILL.md`

- **What it does:** The "devil's advocate" role of the idea group chat: finds holes, hidden assumptions and counter-examples (including historical failures) without softening, but also without dismissing the whole idea.
- **How to use:** Say "devil's advocate this", "why would this fail?", "find the holes". Standalone it returns 5–8 critiques and three questions you must be able to answer.
- **Best suited for:** Stress-testing an idea before investing in it.

<a id="s-idea-research"></a>
### idea-research

[idea-research.zip](idea-research.zip) · entry: `spellbook-main/skills/idea-research/SKILL.md` · `spellbook-main/plugins/idea-coach/skills/idea-research/SKILL.md`

- **What it does:** The "researcher" role of the idea group chat: uses web search to pull current facts, competitors and data with cited sources, explicitly lists what it couldn't find, and never judges or advises.
- **How to use:** Say "research X", "what are the competitors / current data for X?". Needs web search.
- **Best suited for:** A factual baseline for an idea.

<a id="s-idea-team"></a>
### idea-team

[idea-team.zip](idea-team.zip) · entry: `spellbook-main/skills/idea-team/SKILL.md` · `spellbook-main/plugins/idea-coach/skills/idea-team/SKILL.md`

- **What it does:** Moderator of the idea group chat: throws a one-line idea to a three-agent team (researcher, devil's advocate, analogist) who talk in rounds and @ each other while you can interject anytime. Produces a `team-report.md` with facts, holes, analogies and angles you may have missed. It expands ideas; it doesn't score or veto them.
- **How to use:** Say "assemble a team to discuss X", "group review X", or run `/idea-coach:idea-team <idea>` if installed as a plugin. If you've already decided and need a PRD, use `idea-to-product`.
- **Best suited for:** Quickly seeing an idea from several angles before committing.

<a id="s-idea-to-product"></a>
### idea-to-product

[idea-to-product.zip](idea-to-product.zip) · entry: `spellbook-main/skills/idea-to-product/SKILL.md` · `spellbook-main/plugins/idea-coach/skills/idea-to-product/SKILL.md`

- **What it does:** End-to-end product coach that takes a one-line idea through seven stages to a PRD and a clickable HTML prototype. Deliberately pushes back, forces feature cuts and runs a Nielsen + Norman usability check. Saves state so you can resume, list and export projects.
- **How to use:** Say "I have an idea for …", "build an MVP", "write a PRD", or run `/idea-coach:idea <idea>` (also `resume`, `list`, `export <slug>`) if installed as a plugin. Not for teams that already have a running PRD, or for pure brainstorming.
- **Best suited for:** Turning a raw idea into a scoped, user-friendly MVP definition.

<a id="s-infinite-canvas-function-architect"></a>
### infinite-canvas-function-architect

[infinite-canvas-function-architect.zip](infinite-canvas-function-architect.zip) · entry: `infinite-canvas-function-architect-v1.1.0/SKILL.md`

- **What it does:** Turns messy product notes, feature lists or workflows into a structured, editable infinite canvas showing goals, modules, features, flows, data, integrations, constraints, risks, dependencies, gaps and priorities. Builds a canonical graph model first, diagnoses it (orphan features, goal gaps, missing acceptance criteria, hidden prerequisites, circular dependencies), then renders a portable single-file canvas or a React Flow app.
- **How to use:** Paste your notes or feature list and ask to "organise this into a canvas / system map". Pick a rendering lane (portable canvas, React Flow app, whiteboard-first).
- **Best suited for:** Making sense of a sprawling feature set and seeing what's missing.

<a id="s-prd-master"></a>
### prd-master

[prd-master.zip](prd-master.zip) · entry: `spellbook-main/skills/prd-master/SKILL.md`

- **What it does:** PRD and product-definition guide: problem-first structure, quantified goals (no vague metrics), INVEST user stories, acceptance criteria, RICE/MoSCoW prioritisation and a full PRD template (summary, context, goals, personas, stories, requirements, out of scope, design, technical notes, rollout, risks).
- **How to use:** Trigger when writing a PRD, user stories or acceptance criteria, or prioritising features.
- **Best suited for:** Clear, measurable product requirements documents.

<a id="s-product-analytics"></a>
### product-analytics

[product-analytics.zip](product-analytics.zip) · entry: `spellbook-main/skills/product-analytics/SKILL.md`

- **What it does:** Product analytics and growth: North Star metric, AARRR funnel, event tracking design (object_action naming, no PII), cohort and retention analysis, A/B testing with statistical rigour, and templates.
- **How to use:** Trigger when designing event tracking, defining metrics or dashboards, planning experiments or analysing retention.
- **Best suited for:** Setting up product metrics and experiments correctly.

<a id="s-product-discovery"></a>
### product-discovery

[product-discovery.zip](product-discovery.zip) · entry: `spellbook-main/skills/product-discovery/SKILL.md`

- **What it does:** Product discovery and market research: continuous discovery habits, Jobs-to-be-Done, Kano model, Value Proposition Canvas, Cagan's ten opportunity-assessment questions, user interviews, assumption testing and opportunity mapping. Hard rules: problem before solution, evidence-based decisions, falsifiable assumptions.
- **How to use:** Trigger when validating an idea, planning interviews, assessing an opportunity or doing competitive analysis.
- **Best suited for:** Deciding what is worth building before building it.

<a id="s-product-manager-toolkit"></a>
### product-manager-toolkit

[product-manager-toolkit.zip](product-manager-toolkit.zip) · entry: `spellbook-main/skills/product-manager-toolkit/SKILL.md`

- **What it does:** A PM toolkit with scripts: `rice_prioritizer.py` scores a CSV of features with RICE (with team capacity), `customer_interview_analyzer.py` analyses interview transcripts, plus PRD templates, discovery frameworks (opportunity-solution tree, hypothesis template) and go-to-market guidance.
- **How to use:** Ask for feature prioritisation (provide a CSV with name, reach, impact, confidence, effort), interview analysis or a PRD from a template.
- **Best suited for:** Hands-on PM work that benefits from quick scripts.

<a id="s-zh-f33b17b8"></a>
### creative-ideation（网页脑洞）

[creative-ideation（网页脑洞）.zip](creative-ideation%EF%BC%88%E7%BD%91%E9%A1%B5%E8%84%91%E6%B4%9E%EF%BC%89.zip) · *prompt-type* · entry: `网页脑洞Skill-.md`

- **What it does:** "Web brainstorm" — a standalone, web-chat version of the Hermes `creative-ideation` skill: a routed library of named creative methods with anti-slop rules (refuse the first three ideas, force specificity, a weirdness budget, use real proper nouns). Picks a method based on your phase and domain and produces specific, non-generic ideas.
- **How to use:** Not a SKILL.md skill: paste `网页脑洞Skill-.md` as the system prompt, custom instructions or first message of any web AI, then give your topic, setting, characters or plot need.
- **Best suited for:** Breaking out of generic ideas for stories, settings, products or campaigns in a plain chat window.

<a id="cat-frontend"></a>
## Frontend, UI & design systems

Web and mobile UI design, design systems, Figma-to-code, React and UX reviews.

| Skill | Best suited for |
|---|---|
| [`app-ui-design`](#s-app-ui-design) | Native-feeling, accessible mobile app interfaces. |
| [`css-debug`](#s-css-debug) | "Why is this element clipped / mispositioned / invisible?" problems. |
| [`figma-to-code`](#s-figma-to-code) | Faithful Figma-to-React/Next.js implementation with Tailwind. |
| [`figma-to-react`](#s-figma-to-react) | Same as `figma-to-code` — pick whichever name fits your setup. |
| [`frontend-art-director`](#s-frontend-art-director) | Ambitious web UI work that must look authored, not templated, and survive production. |
| [`frontend-design`](#s-frontend-design) | Web pages and components with a strong, intentional visual identity. |
| [`personal-profile-mini-program-builder`](#s-personal-profile-mini-program-builder) | A polished personal profile or portfolio inside WeChat. |
| [`product-ux-expert`](#s-product-ux-expert) | Structured UX critiques and accessibility checks. |
| [`react-best-practices`](#s-react-best-practices) | Performance reviews of React/Next.js apps. |
| [`react-hooks-best-practices`](#s-react-hooks-best-practices) | Avoiding effect-related bugs and needless re-renders in React. |
| [`ui-design-system`](#s-ui-design-system) | Generating design tokens fast from a brand colour. |
| [`ui-designer`](#s-ui-designer) | Building an MVP that matches the look of reference designs. |
| [`ui-ux-pro-max`](#s-ui-ux-pro-max) | A broad UI/UX reference you can lean on for any stack. |
| [`web-artifacts-builder`](#s-web-artifacts-builder) | Rich, app-like claude.ai artifacts. |
| [`web-asset-generator`](#s-web-asset-generator) | Finishing a website's icon and social-preview assets. |

<a id="s-app-ui-design"></a>
### app-ui-design

[app-ui-design.zip](app-ui-design.zip) · entry: `spellbook-main/skills/app-ui-design/SKILL.md` · `spellbook-main/plugins/spellbook-ui/skills/app-ui-design/SKILL.md`

- **What it does:** Mobile app UI design for iOS and Android: Material Design 3 and Apple HIG, colour tokens, typography scales, 8-point spacing grid, touch targets, dark mode and accessibility. The zip holds two identical copies (core and the `spellbook-ui` plugin).
- **How to use:** Ask it to design or review app screens, set up a mobile design system, or check accessibility and platform conventions.
- **Best suited for:** Native-feeling, accessible mobile app interfaces.

<a id="s-css-debug"></a>
### css-debug

[css-debug.zip](css-debug.zip) · entry: `spellbook-main/skills/css-debug/SKILL.md`

- **What it does:** Diagnoses CSS and frontend layout bugs: positioning, overflow clipping, Tailwind classes that don't apply, z-index stacking, Flexbox/Grid issues and React components that don't render or show. Gives a diagnosis, the CSS mechanism behind it and a fix.
- **How to use:** Invoke `/css-debug` or describe the bug; share the HTML structure, computed styles of the element and its parents, and a screenshot if possible.
- **Best suited for:** "Why is this element clipped / mispositioned / invisible?" problems.

<a id="s-figma-to-code"></a>
### figma-to-code

[figma-to-code.zip](figma-to-code.zip) · entry: `spellbook-main/skills/figma-to-code/SKILL.md`

- **What it does:** Extracts Figma designs (via Figma MCP) and generates production-ready React/Next.js components with TypeScript and Tailwind CSS at pixel-level accuracy. Strict rules: never truncate MCP output, flatten `absolute contents` wrappers, take dimensions from metadata, map fonts, inline SVGs.
- **How to use:** Give a Figma URL or frame and ask to convert it to code. Needs the Figma MCP server connected.
- **Best suited for:** Faithful Figma-to-React/Next.js implementation with Tailwind.

<a id="s-figma-to-react"></a>
### figma-to-react

[figma-to-react.zip](figma-to-react.zip) · entry: `spellbook-main/skills/figma-to-react/SKILL.md` · `spellbook-main/plugins/spellbook-ui/skills/figma-to-react/SKILL.md`

- **What it does:** Same Figma-to-React/Next.js generator as `figma-to-code` (TypeScript + Tailwind, lossless use of Figma MCP output, flattened `absolute contents`, metadata-driven dimensions, inlined SVGs) under the name used by the `spellbook-ui` plugin. The zip holds the core and plugin copies.
- **How to use:** Give a Figma URL and ask for React/Next.js components; requires the Figma MCP server. Install only one of `figma-to-code` / `figma-to-react` to avoid duplicate triggers.
- **Best suited for:** Same as `figma-to-code` — pick whichever name fits your setup.

<a id="s-frontend-art-director"></a>
### frontend-art-director

[frontend-art-director.zip](frontend-art-director.zip) · entry: `frontend-art-director/SKILL.md`

- **What it does:** Full-spectrum frontend art direction, UX, design-system stewardship, visual QA and production hardening. Infers the brief, writes a change contract, builds a coherent "visual world" with seven locks, handles edge states, then runs a strict pre-flight, a deterministic detector (`detector_rules.json`), browser verification and a final gate. Includes a block library and anti-template rules.
- **How to use:** Invocable with `[command] [target]` (canonical and extended commands are listed in the SKILL.md), or just ask for a new site, dashboard, redesign, design-system extraction, visual audit, dark mode or responsive pass.
- **Best suited for:** Ambitious web UI work that must look authored, not templated, and survive production.

<a id="s-frontend-design"></a>
### frontend-design

[frontend-design.zip](frontend-design.zip) · entry: `spellbook-main/skills/frontend-design/SKILL.md` · `spellbook-main/plugins/spellbook-ui/skills/frontend-design/SKILL.md`

- **What it does:** Builds distinctive, production-grade web interfaces that avoid generic "AI slop" aesthetics — bold design thinking, typography, colour, motion and composition, implemented as real working code. Only applies when the target is a browser-rendered web UI (not native, GPU, game or terminal UIs). Zip holds core and `spellbook-ui` copies.
- **How to use:** Ask explicitly to build or substantially redesign a web component, page or app; give purpose, audience and constraints.
- **Best suited for:** Web pages and components with a strong, intentional visual identity.

<a id="s-personal-profile-mini-program-builder"></a>
### personal-profile-mini-program-builder

[personal-profile-mini-program-builder.zip](personal-profile-mini-program-builder.zip) · entry: `personal-profile-mini-program-builder/SKILL.md`

- **What it does:** Turns scattered personal material (old CVs, chat logs, project lists) into a native WeChat Mini Program — personal homepage, résumé, portfolio, creator card or targeted introduction — with a single profile source of truth, privacy projection, a professional information hierarchy and a visual system. Never invents employers, degrees, numbers or awards.
- **How to use:** Provide your material and the audience/purpose. It structures a `profile.json`, runs `scripts/compile_profile.py`, then generates WXML/WXSS/JS ready to import into WeChat DevTools. Can also extend, repair or review an existing mini program.
- **Best suited for:** A polished personal profile or portfolio inside WeChat.

<a id="s-product-ux-expert"></a>
### product-ux-expert

[product-ux-expert.zip](product-ux-expert.zip) · entry: `spellbook-main/skills/product-ux-expert/SKILL.md`

- **What it does:** UX review and interaction design: Nielsen's ten heuristics with severity ratings, cognitive load and key UX laws, Gestalt principles, user journey mapping, WCAG 2.2 AA accessibility checks, micro-interactions and motion design.
- **How to use:** Ask for a heuristic evaluation, UX review, journey map or accessibility audit of a screen or flow.
- **Best suited for:** Structured UX critiques and accessibility checks.

<a id="s-react-best-practices"></a>
### react-best-practices

[react-best-practices.zip](react-best-practices.zip) · entry: `spellbook-main/skills/react-best-practices/SKILL.md`

- **What it does:** React and Next.js performance playbook distilled from Vercel Engineering guidance, in priority order: eliminate data-fetch waterfalls, protect bundle size, prefer server work, control re-renders, optimise rendering paths, clean up JS hot spots. Includes a review checklist.
- **How to use:** Trigger when building, reviewing or refactoring React/Next.js code for performance.
- **Best suited for:** Performance reviews of React/Next.js apps.

<a id="s-react-hooks-best-practices"></a>
### react-hooks-best-practices

[react-hooks-best-practices.zip](react-hooks-best-practices.zip) · entry: `spellbook-main/skills/react-hooks-best-practices/SKILL.md`

- **What it does:** React hooks and component patterns: effects as escape hatches only (derived state, `useMemo`, key-based resets, event handlers instead of effects), correct dependencies (never silence the linter, updater functions, `useEffectEvent`), cleanup and fetch races, refs and `useImperativeHandle`.
- **How to use:** Trigger when reading or writing React components with hooks or effects. The skill asks to be paired with a `typescript-best-practices` skill, which is not in this repo.
- **Best suited for:** Avoiding effect-related bugs and needless re-renders in React.

<a id="s-ui-design-system"></a>
### ui-design-system

[ui-design-system.zip](ui-design-system.zip) · entry: `spellbook-main/skills/ui-design-system/SKILL.md` · `spellbook-main/plugins/spellbook-ui/skills/ui-design-system/SKILL.md`

- **What it does:** Design-system toolkit: `design_token_generator.py` generates colour palettes, a modular type scale, an 8-pt spacing grid, shadows, animation and responsive tokens from a brand colour (modern / classic / playful; JSON, CSS or SCSS), plus component architecture, accessibility and dev-handoff docs. Zip holds core and `spellbook-ui` copies.
- **How to use:** Run `python scripts/design_token_generator.py <brand_color> <style> <format>` or ask to create or maintain a design system.
- **Best suited for:** Generating design tokens fast from a brand colour.

<a id="s-ui-designer"></a>
### ui-designer

[ui-designer.zip](ui-designer.zip) · entry: `spellbook-main/skills/ui-designer/SKILL.md`

- **What it does:** Extracts a design system from reference UI screenshots or mockups (palette, typography, spacing, components), generates an MVP PRD if needed and composes an implementation-ready UI prompt, then can build the UI in React.
- **How to use:** Provide a folder of reference images and describe the app; it walks through extraction → PRD → final prompt → implementation, using the templates in `assets/`.
- **Best suited for:** Building an MVP that matches the look of reference designs.

<a id="s-ui-ux-pro-max"></a>
### ui-ux-pro-max

[ui-ux-pro-max.zip](ui-ux-pro-max.zip) · entry: `spellbook-main/skills/ui-ux-pro-max/SKILL.md`

- **What it does:** High-rigour UI/UX guidance across product patterns, landing pages, dashboards, chart choices, visual styles, palettes, typography and font pairing, UX rules and nine stacks (React, Next.js, Vue, Svelte, SwiftUI, React Native, Flutter, Tailwind, shadcn/ui), plus design-system generation and pre-delivery review.
- **How to use:** Triggers broadly on UI work — planning, building, reviewing or fixing pages and components; details in `references/full-guide.md`.
- **Best suited for:** A broad UI/UX reference you can lean on for any stack.

<a id="s-web-artifacts-builder"></a>
### web-artifacts-builder

[web-artifacts-builder.zip](web-artifacts-builder.zip) · entry: `spellbook-main/skills/web-artifacts-builder/SKILL.md`

- **What it does:** Builds elaborate multi-component claude.ai HTML artifacts with React 18, TypeScript, Vite, Tailwind CSS and shadcn/ui: initialise with `scripts/init-artifact.sh`, develop, bundle into a single HTML file with `scripts/bundle-artifact.sh`, then share and optionally test. Includes anti-"AI slop" style rules.
- **How to use:** Ask for a complex artifact with state, routing or many components. Not needed for simple single-file HTML/JSX.
- **Best suited for:** Rich, app-like claude.ai artifacts.

<a id="s-web-asset-generator"></a>
### web-asset-generator

[web-asset-generator.zip](web-asset-generator.zip) · entry: `spellbook-main/skills/web-asset-generator/SKILL.md`

- **What it does:** Generates favicons, PWA app icons and social share (Open Graph) images for Facebook, Twitter/X, WhatsApp and LinkedIn from a logo, an emoji or a text slogan, resizes them properly and provides the HTML meta tags.
- **How to use:** Ask for "favicons from my logo", "an emoji favicon" or "OG images with this slogan"; it asks a few clarifying questions, then runs the bundled scripts (install `requirements.txt`).
- **Best suited for:** Finishing a website's icon and social-preview assets.

<a id="cat-backend"></a>
## Architecture, backend & data

Architecture decisions, APIs, databases, data contracts, performance, logging and specs.

| Skill | Best suited for |
|---|---|
| [`api-design`](#s-api-design) | Designing new APIs and their contracts. |
| [`architecture-foundation`](#s-architecture-foundation) | Pre-implementation specs and boundary decisions, especially for Rust and Go. |
| [`architecture-research`](#s-architecture-research) | Technology selection that needs sourced evidence, not a feature table. |
| [`data-contract-migrations`](#s-data-contract-migrations) | Schema and payload changes where a silent break would be costly. |
| [`database-patterns`](#s-database-patterns) | Designing Postgres schemas and Redis caching layers. |
| [`dev-architecture-playbook`](#s-dev-architecture-playbook) | Planning a project from product intent to production with the right skills in the right order. |
| [`elegant-architecture`](#s-elegant-architecture) | Keeping a codebase modular and small-file by design. |
| [`performance-capacity`](#s-performance-capacity) | Turning "make it faster" into budgets and verified improvements. |
| [`structured-logging-lite`](#s-structured-logging-lite) | The smallest logging contract that makes an app diagnosable. |
| [`technical-spec`](#s-technical-spec) | Decision-focused engineering documents that teams actually read. |

<a id="s-api-design"></a>
### api-design

[api-design.zip](api-design.zip) · entry: `spellbook-main/skills/api-design/SKILL.md`

- **What it does:** Opinionated REST / GraphQL / gRPC API design guide: contract-first with OpenAPI 3.2, URL versioning with Sunset headers, idempotency keys, cursor pagination, RFC 7807 error bodies, GraphQL federation and gRPC streaming. Includes templates. Note its stance: delete rather than deprecate.
- **How to use:** Trigger when designing endpoints, writing an OpenAPI spec, choosing between REST, GraphQL and gRPC, or reviewing an existing API contract.
- **Best suited for:** Designing new APIs and their contracts.

<a id="s-architecture-foundation"></a>
### architecture-foundation

[architecture-foundation.zip](architecture-foundation.zip) · entry: `spellbook-main/skills/architecture-foundation/SKILL.md`

- **What it does:** Designs architecture before code: explicit boundaries, contracts, validation gates and a small execution plan. Covers Rust/Go crate, package, module, runtime and service boundaries, comparison with mature projects, avoiding stacks of one-off PRs, and migration-debt audits.
- **How to use:** Ask "what architecture should this use?", "write a complete spec before we code", or "is this stacked one-off work?". In existing repos it first explains the current architecture.
- **Best suited for:** Pre-implementation specs and boundary decisions, especially for Rust and Go.

<a id="s-architecture-research"></a>
### architecture-research

[architecture-research.zip](architecture-research.zip) · entry: `spellbook-main/skills/architecture-research/SKILL.md`

- **What it does:** Evidence-driven architecture research: landscape studies, source-level system archaeology, build-vs-buy and adopt/adapt/build decisions, open-source vs commercial comparisons. Produces a decision record backed by an evidence ledger. Also triggers on Chinese requests such as 架构调研 / 技术选型.
- **How to use:** Ask "how is X built?", "should we adopt or build Y?", or "compare open-source alternatives to Z". Not for small changes or for detailed design once the direction is fixed (use `architecture-foundation`).
- **Best suited for:** Technology selection that needs sourced evidence, not a feature table.

<a id="s-data-contract-migrations"></a>
### data-contract-migrations

[data-contract-migrations.zip](data-contract-migrations.zip) · entry: `spellbook-main/skills/data-contract-migrations/SKILL.md`

- **What it does:** Designs and verifies data contract changes: schema changes, migrations, rollbacks, backfills, compatibility windows, tenant isolation and API-to-database field mapping. Treats missing fields as absent rather than inventing fallbacks.
- **How to use:** Trigger when changing a database schema, event payloads, stored documents, analytics tables or multi-tenant boundaries. It gathers writers/readers, volume and downtime constraints before proposing a plan.
- **Best suited for:** Schema and payload changes where a silent break would be costly.

<a id="s-database-patterns"></a>
### database-patterns

[database-patterns.zip](database-patterns.zip) · entry: `spellbook-main/skills/database-patterns/SKILL.md`

- **What it does:** PostgreSQL + Redis data modelling: data types, schema design, index strategy, JSONB use, query optimisation, connection pooling, Redis structures and key naming, TTLs, cache-aside / write-through, invalidation, stampede and penetration protection, tiered hot/warm/cold storage and locking.
- **How to use:** Trigger when designing tables, indexes or caching, or reviewing cache consistency.
- **Best suited for:** Designing Postgres schemas and Redis caching layers.

<a id="s-dev-architecture-playbook"></a>
### dev-architecture-playbook

[dev-architecture-playbook.zip](dev-architecture-playbook.zip) · entry: `spellbook-main/skills/dev-architecture-playbook/SKILL.md`

- **What it does:** The lifecycle router for the spellbook engineering skills: classifies a request (idea, architecture, API/data/security contract, implementation, testing, release, operations), picks the minimal skill chain, and sets gates so implementation doesn't start before the required contracts exist.
- **How to use:** Ask for "a complete development architecture for this idea/repo" or "which skills should I combine for this?". It hands off to `product-discovery`, `prd-master`, `architecture-foundation`, `api-design`, `release-engineering`, etc.
- **Best suited for:** Planning a project from product intent to production with the right skills in the right order.

<a id="s-elegant-architecture"></a>
### elegant-architecture

[elegant-architecture.zip](elegant-architecture.zip) · entry: `spellbook-main/skills/elegant-architecture/SKILL.md`

- **What it does:** Clean-architecture discipline with a strict 200-line-per-file limit: plan first, define interfaces, split large files into folders, use DI / factory / strategy patterns, and test real behaviour without mocks.
- **How to use:** Trigger when starting a feature, refactoring a large file or planning module structure.
- **Best suited for:** Keeping a codebase modular and small-file by design.

<a id="s-performance-capacity"></a>
### performance-capacity

[performance-capacity.zip](performance-capacity.zip) · entry: `spellbook-main/skills/performance-capacity/SKILL.md`

- **What it does:** Makes performance measurable before optimising: baselines (p50/p95/p99, data size, concurrency, resource limits), performance budgets per surface, load tests, capacity estimates, bottleneck hypotheses, caching and query efficiency, queue throughput and regression gates.
- **How to use:** Trigger when a feature may be slow, a system must scale, a regression is suspected, or release readiness depends on throughput, cost or latency.
- **Best suited for:** Turning "make it faster" into budgets and verified improvements.

<a id="s-structured-logging-lite"></a>
### structured-logging-lite

[structured-logging-lite.zip](structured-logging-lite.zip) · entry: `spellbook-main/skills/structured-logging-lite/SKILL.md`

- **What it does:** Designs, audits or implements application structured logging from repository evidence: whether and where to log, choosing or migrating a logger, standard event names, fields, levels and redaction, HTTP access and panic logs, and why production logs can't answer an incident question. Read-only unless asked to implement.
- **How to use:** Ask "where should we add logs?", "standardise our log fields", or "our logs couldn't explain last night's incident". Not for tailing logs or a full observability programme (`observability-sre`).
- **Best suited for:** The smallest logging contract that makes an app diagnosable.

<a id="s-technical-spec"></a>
### technical-spec

[technical-spec.zip](technical-spec.zip) · entry: `spellbook-main/skills/technical-spec/SKILL.md`

- **What it does:** Technical design documents, RFCs and Architecture Decision Records: problem statement, proposed solution, mandatory alternatives considered, required diagrams (C4 model, diagrams as code), success metrics, risks and mitigations, and technology evaluation frameworks. Includes templates.
- **How to use:** Trigger when writing a design doc, RFC or ADR, or comparing technology options.
- **Best suited for:** Decision-focused engineering documents that teams actually read.

<a id="cat-languages"></a>
## Language & project starters

Opinionated project templates and idioms for Go, Python, TypeScript, Rust, Zig and HarmonyOS.

| Skill | Best suited for |
|---|---|
| [`golang-web`](#s-golang-web) | Bootstrapping a clean, idiomatic Go service. |
| [`harmonyos-app`](#s-harmonyos-app) | Native HarmonyOS apps. |
| [`python-project`](#s-python-project) | Bootstrapping a clean, modern Python project. |
| [`rust-best-practices`](#s-rust-best-practices) | Writing and reviewing idiomatic Rust. |
| [`rust-project`](#s-rust-project) | Bootstrapping a well-structured Rust project. |
| [`typescript-project`](#s-typescript-project) | Bootstrapping a clean TypeScript codebase. |
| [`zig-project`](#s-zig-project) | Bootstrapping an idiomatic Zig project. |

<a id="s-golang-web"></a>
### golang-web

[golang-web.zip](golang-web.zip) · entry: `spellbook-main/skills/golang-web/SKILL.md`

- **What it does:** Modern Go web architecture guide: standard `cmd/internal/pkg` layout, explicit dependency wiring in `main.go`, consumer-side interfaces, error wrapping, Viper config, graceful shutdown, Makefile and checklist. Opinionated: no backwards-compatibility layers, and LLM calls go through a LiteLLM proxy.
- **How to use:** Trigger when creating a new Go web project, API or microservice.
- **Best suited for:** Bootstrapping a clean, idiomatic Go service.

<a id="s-harmonyos-app"></a>
### harmonyos-app

[harmonyos-app.zip](harmonyos-app.zip) · entry: `spellbook-main/skills/harmonyos-app/SKILL.md`

- **What it does:** HarmonyOS NEXT (API 12+) app development: ArkTS with strict typing, declarative ArkUI and state decorators, Stage model (UIAbility) only, distributed and multi-device design, atomic services, project structure and component patterns (LazyForEach, custom dialogs).
- **How to use:** Trigger when building or reviewing a HarmonyOS app.
- **Best suited for:** Native HarmonyOS apps.

<a id="s-python-project"></a>
### python-project

[python-project.zip](python-project.zip) · entry: `spellbook-main/skills/python-project/SKILL.md`

- **What it does:** Modern Python project architecture: uv for packages and Python versions, Ruff for lint/format, Pydantic and mypy for types, src layout, pyproject.toml only, FastAPI, async all the way, and LLM calls through a LiteLLM proxy. Opinionated: delete rather than deprecate.
- **How to use:** Trigger when creating a Python API, CLI or data pipeline; templates included.
- **Best suited for:** Bootstrapping a clean, modern Python project.

<a id="s-rust-best-practices"></a>
### rust-best-practices

[rust-best-practices.zip](rust-best-practices.zip) · entry: `spellbook-main/skills/rust-best-practices/SKILL.md` · `spellbook-main/plugins/rust-dev/skills/rust-best-practices.SKILL.md`

- **What it does:** Idiomatic Rust following Microsoft's Pragmatic Rust Guidelines: type-driven design, ownership, `thiserror` for libraries and `anyhow` for apps, no panics in libraries, builders, newtypes, `impl Trait`, performance, async and testing. The zip holds the core skill and a `rust-dev` plugin variant.
- **How to use:** Invoke before any Rust edit or review, or when wrestling with lifetimes, the borrow checker or async Rust.
- **Best suited for:** Writing and reviewing idiomatic Rust.

<a id="s-rust-project"></a>
### rust-project

[rust-project.zip](rust-project.zip) · entry: `spellbook-main/skills/rust-project/SKILL.md`

- **What it does:** Modern Rust project architecture: single crate vs Cargo workspace, web framework and ORM selection, `main.rs`/`lib.rs`/`error.rs`/handlers/services layering, Tokio + tracing, CLI structure and testing. Opinionated: delete rather than deprecate; LLM calls through a LiteLLM proxy.
- **How to use:** Trigger when creating a Rust CLI, web service or library; templates included.
- **Best suited for:** Bootstrapping a well-structured Rust project.

<a id="s-typescript-project"></a>
### typescript-project

[typescript-project.zip](typescript-project.zip) · entry: `spellbook-main/skills/typescript-project/SKILL.md`

- **What it does:** Modern TypeScript project architecture: strict types with no `any`, Zod runtime validation, ESM on Node 22+ or Bun, `lib/services/adapters` layering, a 200-line file limit, Vitest/Bun tests with minimal mocks, delete-don't-deprecate, and LLM calls via a LiteLLM proxy.
- **How to use:** Trigger when creating a new TS project, setting up configs or designing structure; templates included.
- **Best suited for:** Bootstrapping a clean TypeScript codebase.

<a id="s-zig-project"></a>
### zig-project

[zig-project.zip](zig-project.zip) · entry: `spellbook-main/skills/zig-project/SKILL.md`

- **What it does:** Modern Zig project architecture: no hidden allocations or control flow, explicit allocator passing (arena patterns), comptime instead of macros, error unions with try/catch/errdefer, inline tests, build system and project structure. Opinionated: delete rather than deprecate; LLM calls via LiteLLM.
- **How to use:** Trigger when creating Zig CLIs, systems code, game-dev or high-performance services; templates included.
- **Best suited for:** Bootstrapping an idiomatic Zig project.

<a id="cat-testing"></a>
## Testing, debugging & code quality

Test strategy, TDD, debugging discipline, QA passes and codebase audits.

| Skill | Best suited for |
|---|---|
| [`app-user-story-qa`](#s-app-user-story-qa) | A full, systematic QA pass over an entire app. |
| [`codebase-audit`](#s-codebase-audit) | Periodic deep health checks of an entire project. |
| [`comprehensive-testing`](#s-comprehensive-testing) | Establishing or improving a project's testing approach. |
| [`playwright-automation`](#s-playwright-automation) | Scripted browser checks and UI tests. |
| [`project-health-auditor`](#s-project-health-auditor) | A quick quality and debt snapshot of a repo. |
| [`systematic-debugging`](#s-systematic-debugging) | Disciplined bug hunting. |
| [`test-driven-development`](#s-test-driven-development) | Enforcing genuine test-first development. |

<a id="s-app-user-story-qa"></a>
### app-user-story-qa

[app-user-story-qa.zip](app-user-story-qa.zip) · entry: `spellbook-main/skills/app-user-story-qa/SKILL.md`

- **What it does:** Turns "test every feature in this app" into a controlled loop: inventories features from the code, derives expected behaviour into a canonical tracker spreadsheet, tests each user story, classifies defects, fixes (only when authorised) and retests.
- **How to use:** In the app's repo, ask "audit every feature", "test all user journeys", or "fix and retest the logged UX defects".
- **Best suited for:** A full, systematic QA pass over an entire app.

<a id="s-codebase-audit"></a>
### codebase-audit

[codebase-audit.zip](codebase-audit.zip) · entry: `spellbook-main/skills/codebase-audit/SKILL.md`

- **What it does:** Whole-codebase audit that adapts parallel analysis agents to your stack: frontend/backend contracts, data integrity, error handling and security, architecture and tech debt, config and caching. Critical and High findings are adversarially verified, results are diffed against the previous audit, and you get a severity-sorted report with a phased repair roadmap. Has a quick health-check mode. Strictly read-only.
- **How to use:** Ask "audit this codebase", "health check", "find hidden bugs / silent degradation", "全面审查" or "快速体检".
- **Best suited for:** Periodic deep health checks of an entire project.

<a id="s-comprehensive-testing"></a>
### comprehensive-testing

[comprehensive-testing.zip](comprehensive-testing.zip) · entry: `spellbook-main/skills/comprehensive-testing/SKILL.md`

- **What it does:** Complete testing strategy: TDD workflow, the test pyramid, unit / integration / E2E / property tests, Jest, Vitest and pytest best practices, mocking strategy and CI integration.
- **How to use:** Trigger when writing tests, reviewing test quality or setting team testing standards.
- **Best suited for:** Establishing or improving a project's testing approach.

<a id="s-playwright-automation"></a>
### playwright-automation

[playwright-automation.zip](playwright-automation.zip) · entry: `spellbook-main/skills/playwright-automation/SKILL.md`

- **What it does:** Browser automation and testing with Playwright: scripts that inspect pages, take screenshots, fill forms, test responsive views and collect console and network evidence.
- **How to use:** Ask to test a web app, automate a browser task, grab screenshots or validate UI behaviour; details live in `references/full-guide.md`.
- **Best suited for:** Scripted browser checks and UI tests.

<a id="s-project-health-auditor"></a>
### project-health-auditor

[project-health-auditor.zip](project-health-auditor.zip) · entry: `spellbook-main/skills/project-health-auditor/SKILL.md`

- **What it does:** Multi-dimensional codebase health check: code quality (large files, long functions, nesting, duplication, dead code), dependencies (outdated, vulnerable, unused, bundle size), security (secrets, hard-coded credentials), test coverage, documentation and architecture, with a scored report.
- **How to use:** Ask "assess the health of this project" or "find our technical debt". Lighter than `codebase-audit`.
- **Best suited for:** A quick quality and debt snapshot of a repo.

<a id="s-systematic-debugging"></a>
### systematic-debugging

[systematic-debugging.zip](systematic-debugging.zip) · entry: `spellbook-main/skills/systematic-debugging/SKILL.md`

- **What it does:** Four-phase debugging framework from obra/superpowers: root-cause investigation (read errors, reproduce, check recent changes, gather evidence) → pattern analysis → hypothesis and testing → implementation, with a "three failed fixes means stop and rethink" rule.
- **How to use:** Trigger whenever you hit a bug, error or unexpected behaviour and want to avoid random fixes.
- **Best suited for:** Disciplined bug hunting.

<a id="s-test-driven-development"></a>
### test-driven-development

[test-driven-development.zip](test-driven-development.zip) · entry: `spellbook-main/skills/test-driven-development.SKILL.md`

- **What it does:** Strict TDD from obra/superpowers: the iron law "no production code without a failing test first", RED → GREEN → REFACTOR with mandatory verification at each step, a list of rationalisations to reject and red flags that force a restart.
- **How to use:** Trigger when writing a feature, fixing a bug or refactoring and you want test-first discipline. Entry is `skills/test-driven-development.SKILL.md` inside the spellbook bundle.
- **Best suited for:** Enforcing genuine test-first development.

<a id="cat-devops"></a>
## DevOps, release & reliability

CI/CD, config and secrets, observability, SLOs and releases.

| Skill | Best suited for |
|---|---|
| [`config-secrets-environments`](#s-config-secrets-environments) | Clean, validated config and secret handling across environments. |
| [`devops-excellence`](#s-devops-excellence) | Secure, modern CI/CD and infrastructure setups. |
| [`incident-slo-runbook`](#s-incident-slo-runbook) | Turning metrics into an actual on-call and incident process. |
| [`observability-sre`](#s-observability-sre) | Designing a monitoring stack that alerts on what users feel. |
| [`release-engineering`](#s-release-engineering) | Safe, repeatable releases. |

<a id="s-config-secrets-environments"></a>
### config-secrets-environments

[config-secrets-environments.zip](config-secrets-environments.zip) · entry: `spellbook-main/skills/config-secrets-environments/SKILL.md`

- **What it does:** Designs, audits and verifies configuration and secrets: environment separation (local/dev/staging/prod), config schemas and validation, BYOK flows, key rotation and drift checks. Never prints real secrets.
- **How to use:** Trigger when adding env vars, changing runtime config, handling API keys or user-supplied keys, diagnosing config drift, or preparing release configuration.
- **Best suited for:** Clean, validated config and secret handling across environments.

<a id="s-devops-excellence"></a>
### devops-excellence

[devops-excellence.zip](devops-excellence.zip) · entry: `spellbook-main/skills/devops-excellence/SKILL.md`

- **What it does:** DevOps and CI/CD guide with hard rules: OIDC instead of static cloud credentials, non-root containers, no secrets in images, protected production deploys. Covers GitHub Actions, Docker, Kubernetes, Terraform, GitOps, progressive delivery and deployment-strategy selection, with templates.
- **How to use:** Trigger when setting up pipelines, containerising an app, deploying to Kubernetes or choosing a release strategy.
- **Best suited for:** Secure, modern CI/CD and infrastructure setups.

<a id="s-incident-slo-runbook"></a>
### incident-slo-runbook

[incident-slo-runbook.zip](incident-slo-runbook.zip) · entry: `spellbook-main/skills/incident-slo-runbook/SKILL.md`

- **What it does:** Creates or audits SLOs and SLIs, burn-rate alerts, incident response steps, escalation paths, postmortems, operational runbooks and customer-impact communication — connecting observability to action for each critical user journey.
- **How to use:** Trigger when defining production reliability, preparing launch readiness, responding to an outage, writing a runbook, tuning alerts or closing out an incident.
- **Best suited for:** Turning metrics into an actual on-call and incident process.

<a id="s-observability-sre"></a>
### observability-sre

[observability-sre.zip](observability-sre.zip) · entry: `spellbook-main/skills/observability-sre/SKILL.md`

- **What it does:** Observability and SRE guide: metrics, logs and traces with Prometheus, Grafana and OpenTelemetry; hard rules such as symptom-based alerts only, low-cardinality labels, SLO-based error budgets and trace context in logs; layered Prometheus architecture and incident-response practice. Includes templates.
- **How to use:** Trigger when setting up monitoring, logging or tracing, defining SLOs or managing incidents.
- **Best suited for:** Designing a monitoring stack that alerts on what users feel.

<a id="s-release-engineering"></a>
### release-engineering

[release-engineering.zip](release-engineering.zip) · entry: `spellbook-main/skills/release-engineering/SKILL.md`

- **What it does:** Turns "ready to merge" into a controlled release: classifies the release (patch, feature, API/SDK, DB migration, config/secret, infra) and applies the right gates — versioning, changelog, release branches, feature flags, canaries, migration gates, rollback proof, deployment checks.
- **How to use:** Trigger when preparing a release, shipping a risky PR, coordinating app/backend/database rollout, recovering from a bad deploy or defining a repo's release policy.
- **Best suited for:** Safe, repeatable releases.

<a id="cat-security"></a>
## Security

Auth, threat modelling, server hardening and supply-chain checks.

| Skill | Best suited for |
|---|---|
| [`auth-security`](#s-auth-security) | Building or auditing authentication and token management. |
| [`npm-supply-chain-check`](#s-npm-supply-chain-check) | Rapid response when an npm supply-chain incident breaks. |
| [`security-threat-model`](#s-security-threat-model) | Catching security risks before code ships. |
| [`server-security`](#s-server-security) | Locking down a VPS or self-hosted server. |

<a id="s-auth-security"></a>
### auth-security

[auth-security.zip](auth-security.zip) · entry: `spellbook-main/skills/auth-security/SKILL.md`

- **What it does:** OAuth 2.1 and JWT security following RFC 9700: PKCE everywhere, short-lived access tokens, refresh-token rotation, HttpOnly cookie storage, explicit algorithm checks, DPoP, revocation and a final checklist.
- **How to use:** Trigger when implementing login, API authorisation or token handling, or when reviewing existing auth code.
- **Best suited for:** Building or auditing authentication and token management.

<a id="s-npm-supply-chain-check"></a>
### npm-supply-chain-check

[npm-supply-chain-check.zip](npm-supply-chain-check.zip) · entry: `spellbook-main/skills/npm-supply-chain-check/SKILL.md`

- **What it does:** Read-only scan of a repository, lockfiles and `node_modules` for known malicious npm package versions and install-time supply-chain indicators (e.g. Shai-Hulud, the Keyv/cacheable incident, suspicious preinstall scripts, credential stealers). Separates "a dependency references it" from "malicious code ran", and never prints secret values. Ships with a dated IOC list and a deterministic scanner.
- **How to use:** Say "was this project exposed to the Shai-Hulud npm attack?" or "check for compromised npm packages". It scans only the current repo unless you widen the scope. Not a general CVE or licence audit.
- **Best suited for:** Rapid response when an npm supply-chain incident breaks.

<a id="s-security-threat-model"></a>
### security-threat-model

[security-threat-model.zip](security-threat-model.zip) · entry: `spellbook-main/skills/security-threat-model/SKILL.md`

- **What it does:** Threat-models features, APIs, data flows, secrets, permissions, supply-chain changes, auth boundaries and risky code paths: maps assets, actors, trust boundaries and entry points, runs a threat checklist and lists required controls. Complements `auth-security` and `server-security`.
- **How to use:** Trigger before or during work touching auth, authorisation, payments, secrets, user data, uploads, webhooks, admin tools, `innerHTML`/`eval`/`exec`, dependency upgrades or cross-tenant access.
- **Best suited for:** Catching security risks before code ships.

<a id="s-server-security"></a>
### server-security

[server-security.zip](server-security.zip) · entry: `spellbook-main/skills/server-security/SKILL.md`

- **What it does:** Server security audit and reversible hardening over SSH: SSH configuration, firewall, exposed ports, users, services, file permissions, brute-force attempts and update posture, with a report and one-step fixes.
- **How to use:** Run with an SSH target (e.g. `root@1.2.3.4`) and say "audit / harden this server". Fixes are applied only after you confirm; details are in `references/full-guide.md`.
- **Best suited for:** Locking down a VPS or self-hosted server.

<a id="cat-git"></a>
## Git & open-source contribution

Commits, repo scaffolding and contributing to other people's projects.

| Skill | Best suited for |
|---|---|
| [`contribution-architect`](#s-contribution-architect) | Moving from bug fixes to architectural contributions or module ownership. |
| [`contributor`](#s-contributor) | Contributing to someone else's project without the usual rejections. |
| [`git-commit-smart`](#s-git-commit-smart) | Consistent, descriptive commit history. |
| [`push-all`](#s-push-all) | Fast "ship it all" commits with a safety net. |
| [`repo-scaffold`](#s-repo-scaffold) | Giving a new or prototype repo a solid foundation. |

<a id="s-contribution-architect"></a>
### contribution-architect

[contribution-architect.zip](contribution-architect.zip) · entry: `spellbook-main/skills/contribution-architect/SKILL.md`

- **What it does:** An open-source architecture mentor that looks past "good first issues" to high-value contributions: complexity hotspots, highly coupled or orphaned modules, test gaps and TODO/HACK debt. Produces a strategic investment list (high-ROI, quick wins, long-term) and drafts RFCs and design proposals.
- **How to use:** In a project you want to contribute to, say "analyse this project and find meaningful work" or "draft an RFC for X".
- **Best suited for:** Moving from bug fixes to architectural contributions or module ownership.

<a id="s-contributor"></a>
### contributor

[contributor.zip](contributor.zip) · entry: `spellbook-main/skills/contributor/SKILL.md`

- **What it does:** End-to-end open-source contribution workflow from a GitHub repo URL to submitted PRs: scans issues, checks for competing PRs and upstream redirection, posts a solution outline first, forks and sets up the repo, follows contribution guidelines and CI, implements a minimal fix with tests and submits with proper commit conventions.
- **How to use:** Say "I want to contribute to <repo URL>", "find good first issues" or "help me fix issue #123 and open a PR". Needs `git` and the GitHub CLI.
- **Best suited for:** Contributing to someone else's project without the usual rejections.

<a id="s-git-commit-smart"></a>
### git-commit-smart

[git-commit-smart.zip](git-commit-smart.zip) · entry: `spellbook-main/skills/git-commit-smart/SKILL.md`

- **What it does:** Analyses staged changes and writes meaningful Conventional Commit messages (type, scope, subject, body, footer, breaking changes), with examples and anti-patterns.
- **How to use:** Stage your changes and say "commit this" or "write the commit message".
- **Best suited for:** Consistent, descriptive commit history.

<a id="s-push-all"></a>
### push-all

[push-all.zip](push-all.zip) · entry: `spellbook-main/skills/push-all.SKILL.md`

- **What it does:** Stages all current changes, commits and pushes after safety checks: stops and warns on secrets (`.env`, keys, certificates, real API tokens) and large files, asks for confirmation, then writes a commit message matching the repo's style.
- **How to use:** Only when you explicitly ask, e.g. "commit and push everything". Entry is `skills/push-all.SKILL.md` inside the spellbook bundle.
- **Best suited for:** Fast "ship it all" commits with a safety net.

<a id="s-repo-scaffold"></a>
### repo-scaffold

[repo-scaffold.zip](repo-scaffold.zip) · entry: `spellbook-main/skills/repo-scaffold/SKILL.md`

- **What it does:** Scaffolds or standardises a production-ready repository: specs (`PRODUCT.md`, `TECH.md`, ADRs), source layout, tests, CI, agent context, config examples, release notes and runbooks — reusing existing conventions instead of creating parallel trees.
- **How to use:** Trigger when starting a new repo, turning a prototype into a maintainable project or filling in missing foundations. For AGENTS.md only, use `agentsmd-scaffold`.
- **Best suited for:** Giving a new or prototype repo a solid foundation.

<a id="cat-agents"></a>
## Coding agents: Claude Code, Codex & multi-agent work

Agent instructions (AGENTS.md / CLAUDE.md), Codex integration, guardrails, orchestration and session hygiene.

| Skill | Best suited for |
|---|---|
| [`agentsmd-optimize`](#s-agentsmd-optimize) | An instruction set that has grown messy or contradictory over time. |
| [`agentsmd-scaffold`](#s-agentsmd-scaffold) | Onboarding a repository for Codex / Claude Code agents. |
| [`claude-code-reverse`](#s-claude-code-reverse) | Verifying how a local tool behaves internally or what changed between versions. |
| [`codex`](#s-codex) | Delegating a coding task to Codex from inside Claude Code. |
| [`codex-agent`](#s-codex-agent) | Cross-model code review inside Claude Code. |
| [`codex-fluent`](#s-codex-fluent) | Ongoing Codex session hygiene. |
| [`codex-log-guard`](#s-codex-log-guard) | Stopping Codex from silently hammering your disk. |
| [`codex-retrospective`](#s-codex-retrospective) | Making Codex gradually fit your style and workflows. |
| [`flowguard`](#s-flowguard) | Long agent sessions that span many files, tools, sessions or agents. |
| [`meta-timing`](#s-meta-timing) | Designing notification and proactive-agent timing that doesn't annoy people. |
| [`multi-model-orchestrator`](#s-multi-model-orchestrator) | Multi-agent projects that need a shared plan and audit trail. |
| [`overengineering-brake`](#s-overengineering-brake) | Stopping agents from gold-plating simple requests. |
| [`persona-team`](#s-persona-team) | Hermes users building role-specialised multi-agent teams. |
| [`recap`](#s-recap) | Weekly reflection on how you actually use your coding agent. |
| [`repo-agent-context-audit`](#s-repo-agent-context-audit) | Checking whether a repo is easy for coding agents to work in. |
| [`review-agent-harness`](#s-review-agent-harness) | Diagnosing systemic agent failures in a repository. |
| [`review-gate`](#s-review-gate) | Keeping a human in the loop for agent-made changes. |
| [`sol-luna-router`](#s-sol-luna-router) | Auditable delegate-and-verify coding with a separate worker agent. |
| [`threads`](#s-threads) | Parallelising a queue of issues or PRs in Codex safely. |
| [`vibeguard`](#s-vibeguard) | Keeping AI-assisted work scoped and honest without heavy tooling. |

<a id="s-agentsmd-optimize"></a>
### agentsmd-optimize

[agentsmd-optimize.zip](agentsmd-optimize.zip) · entry: `spellbook-main/skills/agentsmd-optimize/SKILL.md`

- **What it does:** Audits and tidies AI coding-agent instructions — AGENTS.md, CLAUDE.md, skills and agent definitions. Finds conflicting rules, causes of excessive approval pauses, over-broad skill triggers, duplicate guidance and broken references. Read-only unless you authorize edits.
- **How to use:** Ask "audit my AGENTS.md / CLAUDE.md", "why does the agent keep stopping to ask?", or "clean up my skill triggers". Say explicitly if you want the fixes applied.
- **Best suited for:** An instruction set that has grown messy or contradictory over time.

<a id="s-agentsmd-scaffold"></a>
### agentsmd-scaffold

[agentsmd-scaffold.zip](agentsmd-scaffold.zip) · entry: `spellbook-main/skills/agentsmd-scaffold/SKILL.md`

- **What it does:** Generates or updates repository-specific AGENTS.md files from real repo evidence — a root file plus scoped per-directory files, with validation commands, generated-file boundaries and a short onboarding router.
- **How to use:** Inside a repo, ask "create AGENTS.md for this repo" or "split AGENTS.md by directory". It produces a plan first and writes files only when you ask it to apply them. For a health check only, use `repo-agent-context-audit` instead.
- **Best suited for:** Onboarding a repository for Codex / Claude Code agents.

<a id="s-claude-code-reverse"></a>
### claude-code-reverse

[claude-code-reverse.zip](claude-code-reverse.zip) · entry: `spellbook-main/skills/claude-code-reverse/SKILL.md`

- **What it does:** Read-only static reverse engineering of local executables you own or are authorised to inspect — Claude Code and other CLIs, Mach-O, ELF, PE, Wasm or packaged apps: file identity, strings, symbols, dependencies, sections, and version-to-version comparisons. Never runs the target and refuses cracking, licence or billing bypass.
- **How to use:** Ask explicitly, e.g. "reverse-engineer where this CLI gets this UI string" or "compare these two Claude Code builds". Uses the bundled `extract.sh`, caching by SHA-256.
- **Best suited for:** Verifying how a local tool behaves internally or what changed between versions.

<a id="s-codex"></a>
### codex

[codex.zip](codex.zip) · entry: `spellbook-main/skills/codex/SKILL.md`

- **What it does:** Runs OpenAI Codex CLI (`codex exec`, `codex resume`) from Claude Code for analysis, refactoring or automated edits, with safe prompt passing, the smallest needed sandbox (read-only vs workspace-write), a batch cost gate and follow-up handling.
- **How to use:** Say "run this with Codex" or "ask Codex to refactor X". It checks `codex --version` first and uses only flags your installed CLI supports.
- **Best suited for:** Delegating a coding task to Codex from inside Claude Code.

<a id="s-codex-agent"></a>
### codex-agent

[codex-agent.zip](codex-agent.zip) · entry: `spellbook-main/skills/codex-agent/SKILL.md`

- **What it does:** Lets Claude Code call OpenAI's Codex CLI for second-opinion reviews, cross-verification after Claude implements changes, debugging analysis and alternative implementations. Codex reviews read-only; Claude applies fixes only when you ask.
- **How to use:** Requires Codex CLI installed and authenticated (`npm i -g @openai/codex` or Homebrew). Ask "get a Codex review of this diff / file / project" or "have Codex double-check this".
- **Best suited for:** Cross-model code review inside Claude Code.

<a id="s-codex-fluent"></a>
### codex-fluent

[codex-fluent.zip](codex-fluent.zip) · entry: `spellbook-main/skills/codex-fluent/SKILL.md`

- **What it does:** Keeps Codex fast and light after months of heavy use: diagnoses session bloat, creates mandatory handoffs for valuable work, archives (never deletes) old sessions with clear restore paths, and verifies the result.
- **How to use:** Say "Codex feels slow / bloated" or "clean up my Codex sessions". Starts with a report; optionally sets a recurring reminder.
- **Best suited for:** Ongoing Codex session hygiene.

<a id="s-codex-log-guard"></a>
### codex-log-guard

[codex-log-guard.zip](codex-log-guard.zip) · entry: `spellbook-main/skills/codex-log-guard/SKILL.md`

- **What it does:** Diagnoses excessive writes to Codex's local SQLite diagnostic log (`logs_2.sqlite`, its WAL file) that can wear SSDs. Read-only by default; can install and verify a `block_log_inserts` guard, and clean up only with backups and an explicit request.
- **How to use:** Mention `logs_2.sqlite`, SSD/TBW wear, or ask to protect, clean up, verify or restore Codex logging. Modes: diagnose_only (default), protect, cleanup, restore.
- **Best suited for:** Stopping Codex from silently hammering your disk.

<a id="s-codex-retrospective"></a>
### codex-retrospective

[codex-retrospective.zip](codex-retrospective.zip) · entry: `spellbook-main/skills/codex-retrospective/SKILL.md`

- **What it does:** A self-improvement loop for Codex: reviews its own recent history (last N days or a set period), finds recurring friction and failures, and proposes minimal, high-signal updates to AGENTS.md plus tiny reusable skills — applied only after you approve.
- **How to use:** Ask "run a Codex retrospective on the last 7 days". Pairs with `codex-fluent`.
- **Best suited for:** Making Codex gradually fit your style and workflows.

<a id="s-flowguard"></a>
### flowguard

[flowguard.zip](flowguard.zip) · entry: `spellbook-main/skills/flowguard/SKILL.md`

- **What it does:** A single lifecycle entry point that guards long, ambiguous or stateful agent work from drift: routes the task, verifies current repo/runtime state instead of trusting summaries, runs bounded execution loops with explicit stop conditions, applies verification and review gates, and leaves a resumable handoff. Coordinates other skills rather than replacing them.
- **How to use:** Trigger for multi-step tasks, autonomous loops, repo changes, PR readiness checks, compaction handoffs, resuming from earlier context or cost checkpoints ("continue the task from yesterday's handoff").
- **Best suited for:** Long agent sessions that span many files, tools, sessions or agents.

<a id="s-meta-timing"></a>
### meta-timing

[meta-timing.zip](meta-timing.zip) · entry: `内层包/meta-timing-migration-v2.0.0/meta-timing/SKILL.md`

- **What it does:** A meta-level "when to act" framework: decides when to interrupt, surface quietly, remind, act autonomously, wait, batch or escalate. Separates WHAT (explicit content gate) from WHEN (deterministic timing policy: hard no-push windows + exact allowed windows), adapts per person, and outputs a standard "timing decision contract".
- **How to use:** Invoke when designing notifications, reminders, proactive agent behaviour or interruption policies ("when should we push this?", "通知策略"). Declares dependencies on `agent-harness-loop` and `scr-judgment`, which are not in this repo.
- **Best suited for:** Designing notification and proactive-agent timing that doesn't annoy people.

<a id="s-multi-model-orchestrator"></a>
### multi-model-orchestrator

[multi-model-orchestrator.zip](multi-model-orchestrator.zip) · entry: `spellbook-main/skills/multi-model-orchestrator/SKILL.md`

- **What it does:** Lightweight coordination of complex work across multiple AI agents (Claude models, Codex or others) using a single handoff document as the source of truth: decompose → execute in parallel → synthesise feedback, with full traceability. Includes templates for Claude Code and Codex.
- **How to use:** Ask to "plan this across agents" or "set up a handoff doc for this project"; follow the Quick Start in the SKILL.md.
- **Best suited for:** Multi-agent projects that need a shared plan and audit trail.

<a id="s-overengineering-brake"></a>
### overengineering-brake

[overengineering-brake.zip](overengineering-brake.zip) · entry: `overengineering-brake/skills/overengineering-brake/SKILL.md`

- **What it does:** Keeps agent work complete but proportionate: turns your request into a bounded task contract, treats answer/review/monitor as read-only, lets later tighter instructions override broader ones, and cuts speculative extras, repeated validation, unneeded dependencies, hashes, backups, reports and sub-agents — without blocking necessary work.
- **How to use:** Install as an always-available guard; it applies to ordinary tasks, skill creation, maintenance, migrations, audits and multi-stage work. Entry is `overengineering-brake/skills/overengineering-brake/SKILL.md`.
- **Best suited for:** Stopping agents from gold-plating simple requests.

<a id="s-persona-team"></a>
### persona-team

[persona-team.zip](persona-team.zip) · entry: `persona-team/SKILL.md`

- **What it does:** Gives a multi-agent team (Hermes profiles) role-based personalities: one persona card per role (five work dimensions, duties, no-go zones) compiled into that profile's SOUL.md, role-to-personality matching (MBTI accepted as input), a kanban collaboration protocol and probes to test whether a persona holds. Default six roles: orchestrator, researcher, ideator, executor, reviewer, arbiter.
- **How to use:** Say "set up an agent team", "what personality should my reviewer bot have?", "give me an INTJ auditor", or "this bot doesn't act like itself". Persona cards live in `~/.hermes/personas/`; needs terminal access.
- **Best suited for:** Hermes users building role-specialised multi-agent teams.

<a id="s-recap"></a>
### recap

[recap.zip](recap.zip) · entry: `spellbook-main/skills/recap/SKILL.md`

- **What it does:** Reviews your last N days of Claude Code use from the raw session files (not your memory of it): groups sessions by theme, maps them onto a personal "operating system" coverage table, and outputs patterns, risks and add/remove suggestions for your workflow. Optional cross-machine aggregation.
- **How to use:** Run `/recap` or say "what have I been doing in Claude lately?". `scripts/extract_sessions.py --days 7` for a weekly view; `--json` for structured output.
- **Best suited for:** Weekly reflection on how you actually use your coding agent.

<a id="s-repo-agent-context-audit"></a>
### repo-agent-context-audit

[repo-agent-context-audit.zip](repo-agent-context-audit.zip) · entry: `spellbook-main/skills/repo-agent-context-audit/SKILL.md`

- **What it does:** Read-only audit and scoring of a repository's agent-readable context: AGENTS.md, CLAUDE.md, WARP.md, CONTRIBUTING.md, `.agents/skills`, and `specs/PRODUCT.md` / `TECH.md`. Recommends the smallest useful change toward a three-layer standard (short routing file, task skills, specs).
- **How to use:** Ask "review / score our agent instructions" or "standardise agent context across repos". To generate AGENTS.md files, it hands off to `agentsmd-scaffold`.
- **Best suited for:** Checking whether a repo is easy for coding agents to work in.

<a id="s-review-agent-harness"></a>
### review-agent-harness

[review-agent-harness.zip](review-agent-harness.zip) · entry: `spellbook-main/skills/review-agent-harness/SKILL.md`

- **What it does:** Reviews whether a repo's coding-agent harness — rules, skills, hooks, memory, validation and recovery loops — can reliably take work from intent through controlled execution, verification, delivery and learning. Three isolated evidence passes, reconciled findings; modes: static (default), episode (with authorised session logs) and longitudinal (compare against a ledger).
- **How to use:** Ask "is this repo agent-ready?", "why do agents keep failing here?" or "did the harness fix help?". Not for code-only or AGENTS.md-only audits.
- **Best suited for:** Diagnosing systemic agent failures in a repository.

<a id="s-review-gate"></a>
### review-gate

[review-gate.zip](review-gate.zip) · entry: `spellbook-main/skills/review-gate/SKILL.md`

- **What it does:** Last-mile safety checkpoint before an agent-produced diff is committed, pushed, opened as a PR, merged or applied to your files: produces a concise review pack with risks and verification and blocks landing until a human explicitly approves (or approves with required fixes).
- **How to use:** Trigger with "review gate", "approve before landing", "diff first then land", or let it run before commit/push/PR steps. Template in `assets/review-pack-template.md`.
- **Best suited for:** Keeping a human in the loop for agent-made changes.

<a id="s-sol-luna-router"></a>
### sol-luna-router

[sol-luna-router.zip](sol-luna-router.zip) · entry: `spellbook-main/skills/sol-luna-router/SKILL.md`

- **What it does:** Routes substantial coding or repo-review work through a two-stage setup: "Sol" (the current agent) as commander and verifier, and a separate "Luna Max" CLI worker that does one bounded implementation or investigation, via a bundled runner, followed by Sol's review-and-correction loop. Can also inspect router config and efficiency read-only.
- **How to use:** Only when you explicitly ask Sol to direct Luna or ask for this router; small tasks stay in the main agent. Requires the Luna CLI and the bundled scripts.
- **Best suited for:** Auditable delegate-and-verify coding with a separate worker agent.

<a id="s-threads"></a>
### threads

[threads.zip](threads.zip) · entry: `spellbook-main/skills/threads/SKILL.md`

- **What it does:** Codex-native orchestration: turns a broad request or a GitHub issue/PR queue into controlled parallel sub-threads with explicit lanes, file ownership, worktrees, dependency-aware dispatch, verification budgets, review and merge gates, a run log and a closure audit. Falls back to a prompt pack when native sub-agents aren't available.
- **How to use:** Only when you explicitly ask, e.g. `$threads`, "spin up a few Codex sub-agents" / "开几个子 agent", or "work through this issue queue in parallel". Codex runtime only.
- **Best suited for:** Parallelising a queue of issues or PRs in Codex safely.

<a id="s-vibeguard"></a>
### vibeguard

[vibeguard.zip](vibeguard.zip) · entry: `spellbook-main/skills/vibeguard/SKILL.md`

- **What it does:** Lightweight anti-hallucination guardrails for three moments: a task-contract checklist before implementation, an evidence-based scoring matrix to prioritise review findings, and a weekly regression retrospective template. Does not install hooks or run scripts.
- **How to use:** Ask for "guardrails", "a task contract", "risk-score these findings" or "a regression retrospective".
- **Best suited for:** Keeping AI-assisted work scoped and honest without heavy tooling.

<a id="cat-skills"></a>
## Building & managing skills

Creating, auditing, repairing, archiving and measuring skills — useful for maintaining this repo itself.

| Skill | Best suited for |
|---|---|
| [`capability-distill`](#s-capability-distill) | Preserving hard-won decision rules from a strong model or session before they're lost. |
| [`self-evolution`](#s-self-evolution) | Repairing an underperforming or bloated skill without losing what works. |
| [`skill-archive-manager`](#s-skill-archive-manager) | Keeping a large personal skill library (like this repo) versioned and auditable. |
| [`skill-audit`](#s-skill-audit) | Deciding what skills to build and how they fit together. |
| [`skill-creator`](#s-skill-creator) | Building a skill properly, with tests and measurable improvement. |
| [`skill-ecosystem-doctor`](#s-skill-ecosystem-doctor) | Untangling the same skills installed in several agents and scopes. |
| [`skill-lifeguard`](#s-skill-lifeguard) | High-value workflow skills that must behave consistently. |
| [`skill-recaster`](#s-skill-recaster) | Converting prompts and SOPs into clean skills. |
| [`skill-reforge-foundry`](#s-skill-reforge-foundry) | Capturing a workflow you just did so you never have to correct the agent the same way again. |
| [`skill-usage-stats`](#s-skill-usage-stats) | Finding dead weight in your skill library. |

<a id="s-capability-distill"></a>
### capability-distill

[capability-distill.zip](capability-distill.zip) · entry: `spellbook-main/skills/capability-distill/SKILL.md`

- **What it does:** Extracts non-obvious judgment rules ("why choose option A over a reasonable B") from an approved strong-model interview or a real task transcript and packages them as an auditable "judgment packet" — the input that `skill-audit` and `skill-creator` then turn into a skill.
- **How to use:** Say "distil this model's judgment", "capture the key decisions from this task", or "the model window is closing, keep its judgment for this scenario". It only reads material you approve. Not for writing a SKILL.md directly or for generic best practices.
- **Best suited for:** Preserving hard-won decision rules from a strong model or session before they're lost.

<a id="s-self-evolution"></a>
### self-evolution

[self-evolution.zip](self-evolution.zip) · entry: `self-evolution/SKILL.md`

- **What it does:** "Self Evolution" — audits, diagnoses, improves, simplifies, rebuilds, cleans and validates agent skills (SKILL.md packages): locks the original intent, scans the whole package, diagnoses root causes, chooses a local patch, structural repair or full rebuild, validates behaviour before claiming improvement, and prepares clean external releases.
- **How to use:** Point it at a skill and say "audit this skill", "why are its outputs weak?", "simplify it" or "make it safe to share".
- **Best suited for:** Repairing an underperforming or bloated skill without losing what works.

<a id="s-skill-archive-manager"></a>
### skill-archive-manager

[skill-archive-manager.zip](skill-archive-manager.zip) · entry: `archive-center-suite/skill-archive-manager/SKILL.md`

- **What it does:** Governance hub for your user-level skill collection: discovers skills, registers them in an archive centre, manages versions and release status, keeps indexes and hashes, audits integrity, resolves conflicts, tracks issues to closure, refreshes a management page and packages the whole centre for migration to another machine. Five-stage pipeline: collect → verify → conflict → refresh → migrate.
- **How to use:** Say "archive / register these skills", "audit the skill archive", "resolve this version conflict", "refresh the management page" or "build a migration pack". Install with `install.py`. It ships in `archive-center-suite/` and relies on that suite's internal tooling.
- **Best suited for:** Keeping a large personal skill library (like this repo) versioned and auditable.

<a id="s-skill-audit"></a>
### skill-audit

[skill-audit.zip](skill-audit.zip) · entry: `spellbook-main/skills/skill-audit/SKILL.md`

- **What it does:** Strategy-level skill design and review based on Anthropic's "Lessons from building Claude Code: How we use skills" (June 2026): decides whether a workflow deserves a skill, classifies it, drafts a skill brief, designs progressive disclosure and operational details, plans library structure, distribution and usage measurement, then hands off to `skill-creator`.
- **How to use:** Ask "should this be a skill?", "review this skill", "plan our skill library" or "help me write a better trigger description".
- **Best suited for:** Deciding what skills to build and how they fit together.

<a id="s-skill-creator"></a>
### skill-creator

[skill-creator.zip](skill-creator.zip) · entry: `spellbook-main/skills/skill-creator/SKILL.md`

- **What it does:** Creates new skills and iteratively improves existing ones: captures intent, interviews, writes the SKILL.md, runs test prompts with and without the skill, grades and aggregates results in an eval viewer, iterates, supports blind comparisons and optimises the description for triggering accuracy.
- **How to use:** Say "create a skill for X", "improve this skill", "run evals on my skill" or "optimise the skill description". Install `requirements.txt` for the eval scripts.
- **Best suited for:** Building a skill properly, with tests and measurable improvement.

<a id="s-skill-ecosystem-doctor"></a>
### skill-ecosystem-doctor

[skill-ecosystem-doctor.zip](skill-ecosystem-doctor.zip) · entry: `spellbook-main/skills/skill-ecosystem-doctor/SKILL.md`

- **What it does:** Audits and safely repairs cross-runtime skill governance: which copy is canonical, divergent or duplicate projections between tools, exposure scopes and budgets, lifecycle drift, quarantine and retirement. Deterministic audit → classified findings → repair plan → approved repairs only → cross-runtime verification. Never runs unattended.
- **How to use:** Ask explicitly for cross-runtime or cross-scope skill governance ("my skills differ between Claude Code and Codex", "which copy is the source of truth?"). For usage stats use `skill-usage-stats`.
- **Best suited for:** Untangling the same skills installed in several agents and scopes.

<a id="s-skill-lifeguard"></a>
### skill-lifeguard

[skill-lifeguard.zip](skill-lifeguard.zip) · entry: `spellbook-main/skills/skill-lifeguard/SKILL.md`

- **What it does:** Makes brittle or drifting skills reliable by adding a Reliable Skill Contract: explicit negative examples, verification checkpoints, machine-checkable done conditions, replay or smoke hooks and drift signals — and turns failure logs into skill patches.
- **How to use:** Say "this skill keeps failing", "make this skill reliable" or "turn this failure log into a skill patch". A contract template is in `assets/`.
- **Best suited for:** High-value workflow skills that must behave consistently.

<a id="s-skill-recaster"></a>
### skill-recaster

[skill-recaster.zip](skill-recaster.zip) · entry: `skill-recaster-v1.0.0/SKILL.md`

- **What it does:** Recasts repeated tasks, old prompts, SOPs or messy skills into well-bounded, installable, maintainable agent skills: task contract → decision map (should/shouldn't trigger, conflicts, stop conditions) → behaviour path → just-enough file structure → scenario stress tests (normal, missing, ambiguous, neighbouring, conflicting, pressure) with an honest maturity label.
- **How to use:** Say "turn this prompt / SOP into a skill", "fix my SKILL.md" or "design the trigger boundary". Entry is detected automatically: from scratch, recast an old draft, or repair an existing skill.
- **Best suited for:** Converting prompts and SOPs into clean skills.

<a id="s-skill-reforge-foundry"></a>
### skill-reforge-foundry

[skill-reforge-foundry.zip](skill-reforge-foundry.zip) · entry: `skill-reforge-foundry-v5.1.0/SKILL.md` · `skill-reforge-foundry/SKILL.md`

- **What it does:** Builds, rebuilds, tests and packages reusable agent skills from a goal, rough prompt, SOP, existing skill, failure report — or the experience you just demonstrated in a conversation ("turn this chat into a skill"). Beginner-friendly seven-step flow, can create a small family of skills, writes realistic test cases and produces a release ZIP. The zip contains v5.1.0 (English, builder-focused) and a newer Chinese-first edition focused on extracting skills from conversations.
- **How to use:** Say "把刚才的经验做成 skill", "turn this chat into a skill", "build / upgrade / patch a skill", or give an old skill or failure report.
- **Best suited for:** Capturing a workflow you just did so you never have to correct the agent the same way again.

<a id="s-skill-usage-stats"></a>
### skill-usage-stats

[skill-usage-stats.zip](skill-usage-stats.zip) · entry: `spellbook-main/skills/skill-usage-stats/SKILL.md`

- **What it does:** Two read-only scanners: `agent_health.py` checks locally verifiable Claude Code and Codex configuration health, and `skill_usage_report.py` reports skill invocation evidence and low-use candidates (including enabled plugins). Reports in Chinese or English.
- **How to use:** Ask for "agent health check", "skill usage ranking" or "which skills do I never use?". For governance and repairs use `skill-ecosystem-doctor`.
- **Best suited for:** Finding dead weight in your skill library.

<a id="cat-ai-infra"></a>
## Local models, GPUs & API gateways

Running local models, checking GPU servers and metering API access.

| Skill | Best suited for |
|---|---|
| [`cliproxy-newapi-stack`](#s-cliproxy-newapi-stack) | Adding billing and per-user tokens to a self-hosted CLIProxyAPI deployment. |
| [`gemma4-local-deploy`](#s-gemma4-local-deploy) | Running a local Gemma 4 model server on a Mac. |
| [`gpu-use`](#s-gpu-use) | Quick "who is using which GPU?" checks on shared servers. |

<a id="s-cliproxy-newapi-stack"></a>
### cliproxy-newapi-stack

[cliproxy-newapi-stack.zip](cliproxy-newapi-stack.zip) · entry: `spellbook-main/skills/cliproxy-newapi-stack/SKILL.md`

- **What it does:** Deploys a NewAPI (`calciumion/new-api`) billing, rate-limit and multi-user token layer in front of an already-verified CLIProxyAPI upstream, turning Codex/Claude/Gemini/Qwen subscription accounts into a metered OpenAI-compatible API. Covers Docker deploy, container-to-host bridging (172.17.0.1), model pricing ratios, quota fixes, hot-loading OAuth credentials and dual-path verification.
- **How to use:** Give the SSH target (e.g. `root@1.2.3.4`) and ports. Triggers on phrases like "add NewAPI to my existing cliproxy" or "NewAPI prices are wrong". It does not install bare CLIProxyAPI, and it asks before installing containers or touching production quotas.
- **Best suited for:** Adding billing and per-user tokens to a self-hosted CLIProxyAPI deployment.

<a id="s-gemma4-local-deploy"></a>
### gemma4-local-deploy

[gemma4-local-deploy.zip](gemma4-local-deploy.zip) · entry: `spellbook-main/skills/gemma4-local-deploy/SKILL.md`

- **What it does:** Deploys Gemma 4 12B locally on a Mac / Apple Silicon: installs or upgrades llama.cpp, downloads a GGUF quant, serves an OpenAI-compatible API with `llama-server` (or via Ollama), runs it in tmux bound to 127.0.0.1, and verifies health, chat, resource use and common failures. Profiles: default Q4_K_M, 64K/128K long context, QAT Q4_0 @ 256K, side-by-side comparison demo.
- **How to use:** Say "deploy Gemma 4 locally", optionally with quant, port and background preference. Defaults: `ggml-org/gemma-4-12B-it-GGUF`, Q4_K_M, `http://127.0.0.1:8080`, 32K context.
- **Best suited for:** Running a local Gemma 4 model server on a Mac.

<a id="s-gpu-use"></a>
### gpu-use

[gpu-use.zip](gpu-use.zip) · entry: `spellbook-main/skills/gpu-use/SKILL.md`

- **What it does:** Checks GPU usage on a remote server over SSH: per-card memory and utilisation, running processes and which Docker container owns each one, multi-instance servers inside a single container, and free capacity, with a status label per card.
- **How to use:** Run with `user@host -p port`, or with no argument to use the default server — note the SKILL.md ships with the author's own server hard-coded, so edit that line before use. Say "check GPU usage" / "显存占用".
- **Best suited for:** Quick "who is using which GPU?" checks on shared servers.

<a id="cat-network"></a>
## Network & proxy troubleshooting

Clash / mihomo, IP quality, reconnects, network tuning and remote desktop.

| Skill | Best suited for |
|---|---|
| [`clash-doctor`](#s-clash-doctor) | Fixing and managing Clash Verge proxy setups, especially routing for AI tools. |
| [`clash-routes`](#s-clash-routes) | Quickly answering "which proxy is this app actually using?". |
| [`ip-check`](#s-ip-check) | Vetting a proxy or VPS IP before using it for AI services. |
| [`network-reconnect-repair`](#s-network-reconnect-repair) | "Keeps reconnecting" problems, especially with AI tools behind proxies. |
| [`optimize-network`](#s-optimize-network) | Evidence-based network tuning on a Mac without breaking your proxy setup. |
| [`rustdesk-doctor`](#s-rustdesk-doctor) | RustDesk issues on machines running Clash Verge. |

<a id="s-clash-doctor"></a>
### clash-doctor

[clash-doctor.zip](clash-doctor.zip) · entry: `spellbook-main/skills/clash-doctor/SKILL.md`

- **What it does:** Diagnostics and profile management for Clash Verge / mihomo: proxy failures, routing AI tools, local hub topology, multi-machine alignment, TUN bypass, cloning or switching subscriptions, and configs that didn't take effect after sync. Diagnose and align are read-only; writes need confirmation.
- **How to use:** Arguments include `status`, `profiles`, `hub`, `align`, `roles`, `switch-check <name>`, `clone <src> <dst>`, `setup-ai <name>`, `switch <name>`, `bypass <IP>`. For per-process routes use `clash-routes`; for exit-IP quality use `ip-check`.
- **Best suited for:** Fixing and managing Clash Verge proxy setups, especially routing for AI tools.

<a id="s-clash-routes"></a>
### clash-routes

[clash-routes.zip](clash-routes.zip) · entry: `spellbook-main/skills/clash-routes/SKILL.md`

- **What it does:** Read-only viewer that shows which mihomo proxy chain each local process is using right now (rule → policy group → real exit) — e.g. whether Claude, Codex, Gemini, ChatGPT or the browser goes through the intended proxy.
- **How to use:** Run with an optional process name (defaults to all active connections). Reads the Clash Verge controller without printing secrets. Profile changes belong to `clash-doctor`.
- **Best suited for:** Quickly answering "which proxy is this app actually using?".

<a id="s-ip-check"></a>
### ip-check

[ip-check.zip](ip-check.zip) · entry: `spellbook-main/skills/ip-check/SKILL.md`

- **What it does:** Checks the quality of an IP or residential/datacentre proxy node: registry and geo-database consistency, ASN/org, reputation and blacklists, residential authenticity, BGP announcements, service unlock for Grok/Claude/ChatGPT and latency triangulation — to catch IPs that are physically in one country but listed in another (causing region locks). Read-only.
- **How to use:** Say "check this IP" or give SOCKS5 proxy credentials; it runs `ipcheck.py` and returns a scorecard. Switching nodes is left to `clash-doctor`.
- **Best suited for:** Vetting a proxy or VPS IP before using it for AI services.

<a id="s-network-reconnect-repair"></a>
### network-reconnect-repair

[network-reconnect-repair.zip](network-reconnect-repair.zip) · entry: `network-reconnect-repair/SKILL.md`

- **What it does:** Diagnoses and repairs repeated reconnects, intermittent drops, DNS failures, broken streaming or app-specific connectivity on Windows, macOS and Linux — including Codex network errors. Locates the actual break (link, app, long-lived stream, VPN/TUN switching, resolver) and applies the smallest fix instead of a generic reset.
- **How to use:** Describe the affected app and device, OS, connection type, VPN/proxy state and when it started; it checks what it can directly and asks only for the missing essentials.
- **Best suited for:** "Keeps reconnecting" problems, especially with AI tools behind proxies.

<a id="s-optimize-network"></a>
### optimize-network

[optimize-network.zip](optimize-network.zip) · entry: `spellbook-main/skills/optimize-network/SKILL.md`

- **What it does:** Safely diagnoses and improves local network speed, latency, jitter, DNS, Wi-Fi/Ethernet, macOS network services and bufferbloat: read-only baseline first, then small reversible experiments with before/after verification. Explicitly protects Clash Verge, Mihomo, Shadowrocket, Tailscale, V2Ray, Surge and corporate VPNs.
- **How to use:** Arguments: `diagnose`, `optimize`, `report` plus an optional target domain. Or say "make my network faster", "why is Wi-Fi slow?", "Codex keeps lagging".
- **Best suited for:** Evidence-based network tuning on a Mac without breaking your proxy setup.

<a id="s-rustdesk-doctor"></a>
### rustdesk-doctor

[rustdesk-doctor.zip](rustdesk-doctor.zip) · entry: `spellbook-main/skills/rustdesk-doctor/SKILL.md`

- **What it does:** Diagnoses RustDesk connection problems — can't connect, no ID shown, registration fails — by checking the client process, config and logs, Clash/Mihomo interference (fake-IP DNS, TUN routing), network reachability, the self-hosted server (over SSH if possible) and the local-IP detection bug.
- **How to use:** Run with your self-hosted server IP as an argument (optional) and say "RustDesk won't connect". It follows the steps in order and gives a combined diagnosis.
- **Best suited for:** RustDesk issues on machines running Clash Verge.

<a id="cat-system"></a>
## Computer & editor maintenance

Disk cleanup, slow-machine diagnosis and editor performance.

| Skill | Best suited for |
|---|---|
| [`disk-cleaner`](#s-disk-cleaner) | Reclaiming space from `node_modules`, `target`, caches and old installers on a dev machine. |
| [`storage-gc-guardian`](#s-storage-gc-guardian) | Safe, reversible cleanup when you are low on space. |
| [`system-doctor`](#s-system-doctor) | Quickly finding what is bogging down your Mac. |
| [`vscode-doctor`](#s-vscode-doctor) | Finding the real cause of editor slowness. |

<a id="s-disk-cleaner"></a>
### disk-cleaner

[disk-cleaner.zip](disk-cleaner.zip) · entry: `spellbook-main/skills/disk-cleaner/SKILL.md`

- **What it does:** Scans disk usage and finds safely deletable caches, build outputs and installers, then frees space interactively from a numbered menu (high value / medium / reference-only) and verifies the result. Discovers real project roots instead of assuming folder names.
- **How to use:** Run with an optional path (defaults to the home directory), e.g. "clean up my disk" or `disk-cleaner ~/code`. It only deletes what you pick.
- **Best suited for:** Reclaiming space from `node_modules`, `target`, caches and old installers on a dev machine.

<a id="s-storage-gc-guardian"></a>
### storage-gc-guardian

[storage-gc-guardian.zip](storage-gc-guardian.zip) · entry: `storage-gc-guardian/SKILL.md`

- **What it does:** Transactional disk cleanup: audits stale temp files, rebuildable package caches and diagnostic residue, builds an evidence-bound plan, moves items to a reversible quarantine and deletes permanently only on explicit commit. Treats unknown data as not-garbage and never touches projects, Downloads, personal media, app data or Codex state by inference. Stdlib Python engine.
- **How to use:** Say "free up disk space" or "clean caches". It shows the plan first; restore is possible until you commit.
- **Best suited for:** Safe, reversible cleanup when you are low on space.

<a id="s-system-doctor"></a>
### system-doctor

[system-doctor.zip](system-doctor.zip) · entry: `spellbook-main/skills/system-doctor/SKILL.md`

- **What it does:** Diagnoses a slow computer: load and uptime, memory pressure, swap, CPU and memory top-20, per-app grouping (e.g. all Chrome renderers together), zombie processes and anomalies, then a structured report with recommendations and optional interactive actions.
- **How to use:** Say "my computer is slow", "what's using my CPU / memory?". No arguments. Commands target macOS.
- **Best suited for:** Quickly finding what is bogging down your Mac.

<a id="s-vscode-doctor"></a>
### vscode-doctor

[vscode-doctor.zip](vscode-doctor.zip) · entry: `spellbook-main/skills/vscode-doctor/SKILL.md`

- **What it does:** Evidence-first diagnosis of slow or freezing VS Code-compatible editors (VS Code, Cursor and others): typing lag, UI freezes, extension-host stalls, file-watcher noise, high CPU/RSS, or using the editor as a file browser over huge folders. No hard-coded paths, extension blocklists or assumed root causes; ranks by fresh evidence and verifies before/after.
- **How to use:** Say "VS Code / Cursor is lagging" with an optional workspace root. Starts in a simple read-only mode.
- **Best suited for:** Finding the real cause of editor slowness.

<a id="cat-productivity"></a>
## Productivity, knowledge & reports

Knowledge libraries, chat digests, weekly reports and small business systems.

| Skill | Best suited for |
|---|---|
| [`feishu-rent-billing`](#s-feishu-rent-billing) | Small landlords running utility and rent splitting in Feishu. |
| [`library-steward`](#s-library-steward) | Turning a folder of reference material into a searchable, versioned library. |
| [`wechat-group-daily-digest`](#s-wechat-group-daily-digest) | Catching up on busy WeChat groups. |
| [`weekly`](#s-weekly) | Auto-drafting a weekly work report from commits and agent sessions. |

<a id="s-feishu-rent-billing"></a>
### feishu-rent-billing

[feishu-rent-billing.zip](feishu-rent-billing.zip) · entry: `feishu-rent-billing/SKILL.md` · `feishu-rent-billing/deployment/chg-001/backup/local/SKILL.md`

- **What it does:** A rent-billing system in Feishu Bitable for a two-floor rental house: meter readings (main meter + upper meter, lower = main − upper), leases, shared costs, billing batches and line items; handles mid-month move-in/out pro-rating, vacancy costs borne by the landlord, "provisional 0" vs "confirmed 0" shared costs, duplicate-charge prevention and plain-text bill reports. Includes an offline calculator to reconcile and a locked rule set (R1–R12).
- **How to use:** Three modes: build (set up tables, fields, formulas, forms, workflows), calculate/report (give readings and occupancy, get the bill), troubleshoot (find why Feishu's numbers differ). Use the root `feishu-rent-billing/SKILL.md`; the copy under `deployment/chg-001/backup/` is an older backup. Not for multi-unit or commercial property, taxes or contracts.
- **Best suited for:** Small landlords running utility and rent splitting in Feishu.

<a id="s-library-steward"></a>
### library-steward

[library-steward.zip](library-steward.zip) · entry: `library-steward/SKILL.md`

- **What it does:** Connects to and manages a local knowledge base, document library, style library, asset library or photo collection: surveys it, agrees on usage with you, then handles search, precise location (line or page numbers), pulling whole groups out for use, ingesting new items, source registration, snapshots, rollback and integrity checks. One stdlib Python script with SQLite full-text search (works for Chinese).
- **How to use:** Point it at a library folder (`--root` or `STEWARD_ROOT`) and say "find …", "which page is …", "add this to the library", "snapshot / roll back". Optional `pip install pypdf opencc-python-reimplemented` adds PDF text and Traditional/Simplified search.
- **Best suited for:** Turning a folder of reference material into a searchable, versioned library.

<a id="s-wechat-group-daily-digest"></a>
### wechat-group-daily-digest

[wechat-group-daily-digest.zip](wechat-group-daily-digest.zip) · entry: `wechat-group-daily-digest/SKILL.md`

- **What it does:** "Moon Rabbit catch-up" — turns WeChat group chats you are authorised to read into a verifiable AI daily digest: read-only, evidence pack first, then summary, and only then advances the "last read" marker so you can continue from last time. Privacy modes keep nicknames or replace them with Member A/B/C.
- **How to use:** Input options: a JSON/JSONL export (`--input`), an authorised Windows offline snapshot (`--snapshot`), or a Mac's local WeChat via the separately installed `yichen-wechat-local-vault` tool. Run `doctor` first, then `prepare`. Say "爬楼", "群聊日报" or "从上次继续".
- **Best suited for:** Catching up on busy WeChat groups.

<a id="s-weekly"></a>
### weekly

[weekly.zip](weekly.zip) · entry: `spellbook-main/skills/weekly.SKILL.md`

- **What it does:** Generates a weekly report for a specified date range by combining Git commits, Claude Code sessions, Codex sessions and optional local memory notes, categorised into refactors, features, fixes, research and other work. Note: it is hard-wired to one project ("om-generator" front-end and back-end repos).
- **How to use:** Run with a range such as `2-1到2-7` (defaults to this Monday → today). Edit the repo names and paths in `weekly.SKILL.md` to use it for your own projects.
- **Best suited for:** Auto-drafting a weekly work report from commits and agent sessions.

<a id="cat-learning"></a>
## Learning & tutoring

Structured courses and one-on-one tutoring.

| Skill | Best suited for |
|---|---|
| [`ai-visual-generation-foundation-course`](#s-ai-visual-generation-foundation-course) | Complete beginners who want real skills rather than "magic words". |
| [`feynman-learning-coach`](#s-feynman-learning-coach) | Actually learning a topic or document, not just skimming answers. |

<a id="s-ai-visual-generation-foundation-course"></a>
### ai-visual-generation-foundation-course

[ai-visual-generation-foundation-course.zip](ai-visual-generation-foundation-course.zip) · entry: `ai-image-foundation-course-skill-v1.0.0/SKILL.md`

- **What it does:** A structured beginner course in AI image generation (levels L0 visual recognition → L4 project delivery). Teaches observe → control → generate → diagnose → fix, one new concept at a time, with lessons, exercises, homework and grading. Cross-model.
- **How to use:** Ask "teach me AI image generation from zero", "next lesson", "grade my homework image", or choose a mode: beginner (default), teacher, diagnosis, crash course, homework review. Course map and workbook are in the package.
- **Best suited for:** Complete beginners who want real skills rather than "magic words".

<a id="s-feynman-learning-coach"></a>
### feynman-learning-coach

[feynman-learning-coach.zip](feynman-learning-coach.zip) · entry: `feynman-learning-coach/SKILL.md`

- **What it does:** One-on-one Feynman-method tutor: builds a personal plan from your goal, level, daily time and deadline, then loops explain → you explain it back → probing questions → patch gaps → apply → spaced review. A "learning relay card" lets you resume across sessions.
- **How to use:** Say "I want to learn Python, zero background, 30 min a day", "help me understand chapter 3 of this handout", "quiz me on compound interest", or "continue" (paste back your relay card). Not for doing homework or exams for you.
- **Best suited for:** Actually learning a topic or document, not just skimming answers.

<a id="cat-lifestyle"></a>
## Home, travel & lifestyle

Interior design, trip planning and divination tools.

| Skill | Best suited for |
|---|---|
| [`home-design-director`](#s-home-design-director) | Home renovation planning, layout exploration and style switching. |
| [`trip-planner`](#s-trip-planner) | Practical, ready-to-follow trip plans. |
| [`xuanshu-agent`](#s-xuanshu-agent) | Accurate, tool-computed divination and astrology charts and reports. |

<a id="s-home-design-director"></a>
### home-design-director

[home-design-director.zip](home-design-director.zip) · entry: `home-design-director/SKILL.md`

- **What it does:** Beginner-friendly interior design: turns floor plans, room photos and plain-language needs into a geometry-grounded Room Model, 2–3 layout directions, room-by-room design decisions and geometry-locked visual briefs (styles may decorate, but never move walls, doors or windows). Unknown dimensions stay unknown.
- **How to use:** Start by uploading a floor plan or developer's layout screenshot (dimensions help); then answer at most three key questions at a time. Without a plan it can still give concept advice, not build dimensions.
- **Best suited for:** Home renovation planning, layout exploration and style switching.

<a id="s-trip-planner"></a>
### trip-planner

[trip-planner.zip](trip-planner.zip) · entry: `spellbook-main/skills/trip-planner/SKILL.md`

- **What it does:** Detailed travel itineraries: trip overview, day-by-day morning/afternoon/evening plans with themes, addresses, hours, booking links, durations, travel times, prep-tonight notes and a quick-reference section (booked activities, offline downloads, local spots), with realistic pacing.
- **How to use:** Give destination, dates, travellers, interests, budget and pace; ask for an itinerary.
- **Best suited for:** Practical, ready-to-follow trip plans.

<a id="s-xuanshu-agent"></a>
### xuanshu-agent

[xuanshu-agent.zip](xuanshu-agent.zip) · entry: `xuanshu-skill-2.0.0/.agents/skills/xuanshu-agent/SKILL.md` · `xuanshu-skill-2.0.0/skills/xuanshu-agent/SKILL.md`

- **What it does:** Agent guide for Xuanshu (玄枢), a local metaphysics engine with 110 techniques: Western astrology (natal, returns, progressions, primary directions, horary, electional, rectification, AstroCartoGraphy), BaZi, Zi Wei Dou Shu, Da Liu Ren, Qi Men Dun Jia, Tai Yi, Liu Yao, Mei Hua, tarot, geomancy, almanac and more. Core rule: never hand-calculate — every chart comes from the Xuanshu MCP tools or CLI, after clarifying birth time, place, timezone and similar settings. The zip contains the full xuanshu-skill 2.0.0 repo (AGPL-3.0).
- **How to use:** Install the local server (Python 3.12 + `uv` + offline runtime) and register it as an MCP server, e.g. `uv run --directory <repo>/xuanshu-skill xuanshu-skill client config --format codex` (see the repo README). Then ask "排盘", "起卦", "read my natal chart". Beginners start with `xuanshu_beginner_guide` → `xuanshu_full_reading`.
- **Best suited for:** Accurate, tool-computed divination and astrology charts and reports.
