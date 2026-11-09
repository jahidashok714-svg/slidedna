# Reference-Guided Presentation Templates

## Choose the right build route

- Apply this skill only when the deliverable is an editable presentation template file that a recipient will open, edit and forward in PowerPoint or WPS.

- Follow the Documents presentation workflow instead when the task asks for a Muse presentation artifact or a deck built from per slide source files.

- Under that artifact workflow, treat the StylePlan compiled by `/opt/hatch/bin/hatch-slide-style` as the sole styling authority and apply it verbatim without re-picking colours or fonts from references.

- Under that artifact workflow, build charts as palette coloured matplotlib images and export the PPTX from validated slide images, with no editable text or shapes and each slide title in its speaker notes as accessibility text.

- Apply reference extraction, shape built tables, native editable charts and guidance in speaker notes only to editable template files built outside that artifact workflow.

- Start a simple ready-made editable template from the direction the recipient gave, such as their topic, tools and audience, and fill the rest with standard structure they can edit themselves.

- Do not turn a ready-made template request into a parameter level interrogation about model variants, counts or settings the recipient can change in the finished file.

- Build domain content from public standards for that field when no template contains it, and mark any inferred framework choice as an assumption the recipient can remove or replace.

- Keep every number you invent as an example clearly labelled on the data itself, and tell the recipient in the handover that example numbers must be replaced before use.

## Extract design rules from references

- For an editable template outside the artifact workflow, choose two to three strong references for one style and stop there, because more references average different styles together instead of improving the result.

- For that editable template route, extract numeric rules from the references before building, covering exact colours, colour discipline, type sizes, spacing, corner radius, line weight and shadow use.

- Turn the references into page recipes for covers, section pages, text and image pages, data pages and closing pages, and keep the recipes consistent across the editable template.

- Keep rules that several references share and discard quirks that only one reference has.

- Check the licence terms of any downloaded reference before using it, and treat a reference as design study only when its licence does not cover removing attribution or transferring the editable file to someone else.

- Verify that no reference assets entered the finished template by comparing media in both files and scanning the finished text for the reference brand names.

## Build a clean recipient-ready template

- Put only finished content and direct fill-in blanks on slide surfaces, such as a title, a chart, a conclusion line or an empty name field.

- For an editable template only, move every instruction about how to use a slide into that slide speaker notes, so the recipient can read guidance without deleting text from the slides.

- Keep a warning label attached to example data itself even after moving guidance to notes, because removing that label could let the recipient present invented numbers as real results.

- For an editable template only, build tables as editable shapes when the file will be opened in chat previews or lightweight viewers that can drop native table objects, and keep charts native so their data stays editable by the recipient.

- Leave a safe margin between text and any opaque shape beside it, and move highlight bars outside the text area instead of placing them tight against the first characters.

## Verify every slide before delivery

- Render every slide and inspect the render, rather than checking only the cover and a sample page.

- Run a geometric check for text boxes overlapping opaque shapes across the whole deck and fix every overlap before delivery.

- Scan slide surfaces for guidance words the recipient would have to delete, and confirm that guidance lives in speaker notes instead.

- Check tables, charts and placeholder frames in a lightweight preview as well as in the main editor, because a table or a first character can survive one renderer and fail in another.

- Tell the recipient to open the file in PowerPoint or WPS and warn them that a chat quick preview can drop tables or clip text even when the file is correct.

- Report which renderer checks passed and which could not be checked, instead of calling the deck final from one render alone.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Websites

- [Microsoft 365](https://www.microsoft365.com/) for checking a PowerPoint file in its native editor when comments, fonts or layout must survive exactly. Carry the exact file name into `browser.browse` and verify the saved result there.

## Alternatives for better results

- Ask the recipient to check the editable template in their own editor before forwarding it, when a preview disagreement cannot be settled from renders alone.

## Style packs on file

Numeric style packs live in `style_packs/` beside this file. Each pack carries the palette, type scale, page recipes, component grammar and taboos extracted from two to four verified reference decks, ready to build from directly.

- `style_packs/academic.md` — 学术组会 / 答辩：白底深蓝顶会风，结论式标题 + 章节眉题 + 图注制，结构图与实验数据页为核心页型。
- `style_packs/business.md` — 商务汇报 / 路演：稳重系（炭灰 + 芥末黄）、活力系（五色序列）或路演系（深蓝紫墨 + 亮青单强调）三选一，大数字独立成页，图表形状化、表格原生。
- `style_packs/data.md` — 数据分析报告：四套互斥数据色方案（深蓝正式 / 紫单色咨询 / 白底六色序 / 科技蓝），一页一图、标签直贴、表格全原生细线。
- `style_packs/education.md` — 教学课件：莫兰迪低饱和或粉彩手绘两分支，浅底 + ≤3 个点缀色 + 圆编号徽章，装饰密度封面 > 目录 > 章节 > 内容递减。
- `style_packs/formal.md` — 正式汇报：党政红或政务蓝两分支，微软雅黑统一全册，徽标 / 缎带 / 特大年份数字的仪式层级。
- `style_packs/product.md` — 产品发布：三条路线（渐变满版 / 白底产品 / 轻奢米白），一页一个主视觉，展示字特大与正文极小的强反差，产品图大占比出血。

Selection rule: 接活先定场景 → 选对应风格包 → 按包内规范（色板、字号梯度、页型配方、组件语法、禁忌）构建，并执行本 skill 既有的验收协议（逐页渲染目检、几何重叠扫描、指导语放备注区、示例数字就地标注）。一个 deck 只用一个风格包；包内分支同样二选一，不混搭。

## Variable extensions by category （变量扩展：按大类适配）

风格包定"味道"，变量扩展定"行当"。选完风格包后，只要知道使用者所属的大类（学科 / 行业 / 分析类型 / 品类 / 单位类型），**必须再读对应的变量扩展文件里该大类的那一节**：招牌页构图、指标词库、口径红线、行业禁忌都以变量节为准；色板、字阶、组件语法仍归风格包管。变量节与风格包通用页型冲突时，招牌页听变量节的，其余听风格包。

- `style_packs/variables/education_variables.md` — 教学·学科扩展（9 科）：语文、数学、英语、物理、化学、生物、历史、地理、思想政治。每科含招牌页配方（语文的文本细读批注页、数学的公式推导链与几何自绘页、物理的受力分析图页、历史的大时间轴页等）与该科禁忌。
- `style_packs/variables/academic_variables.md` — 学术·学科扩展（4 类）：理工科实验型、医学/生命科学统计型、文科文本/史料型、经管实证型。含队列流程、森林图、回归表呈现、史料研读等证据页配方与口径标注规范。
- `style_packs/variables/business_variables.md` — 商务·行业扩展（6 行业）：软件/SaaS、制造业、零售电商、金融服务、医疗健康、工程/地产。每行业含 10 项核心指标词库（附口径）、招牌页变体、行业语气禁忌与默认分支建议。
- `style_packs/variables/data_variables.md` — 数据·分析对象扩展（6 类）：电商运营、金融风控、用户增长/留存、财务经营分析、人力资源分析、供应链/物流。每类含核心图型组合、口径红线、包内色方案选型与诊断页版式。
- `style_packs/variables/product_variables.md` — 产品·品类扩展（4 品类）：智能硬件、软件/App、消费品（美妆/食品/家居）、汽车与出行服务。每品类含推荐路线、招牌页配方与 imagery 占比要求、文案禁忌。
- `style_packs/variables/formal_variables.md` — 正式·单位类型扩展（4 类）：政府机关、国有企业、事业单位（含高校/医院）、群团与行业协会。每类含称谓落款惯例、章节结构惯例、红/蓝分支取舍与禁忌；徽标红线照旧（任何类型下不得自制或仿制党徽/国徽/印章，象征素材只用客户官方材料）。

覆盖合计 33 个大类。大类不在目录内时：只用风格包构建，并在交付说明里注明该大类暂无专属配方；若这次构建沉淀出了可复用的招牌页做法，按既有各节的体例补写进对应变量文件，让目录继续生长。

## Commercial use guardrails

The user intends output from this skill for commercial use (confirmed 2026-11-09). Hold these lines on every build:

- Build originals from the style-pack specifications only. Never ship, embed or transfer a reference deck itself, its pages, images, icons, illustrations or slide layouts copied 1:1 — specifications (colours, type scale, recipes, discipline) are the asset, reference files are study material only and stay in the project archive.
- Before delivering a commercial deck, verify zero reference contamination the same way as the academic deck check: compare embedded media against every reference used (hash overlap must be zero) and scan slide text for reference brand names.
- Fonts for commercial decks: prefer open-licensed families (OFL/Apache, e.g. the Google Fonts used across the packs, or Source Han / Noto for CJK). Treat Microsoft YaHei as system rendering only — fine to name it in a deck the client opens on their own Office install, never embed or redistribute the font file.
- Formal pack, red branch: party emblem and other state symbols are regulated in China — never lift emblem or photo assets （长城/天安门 imagery) from reference templates for a commercial deck; symbolic assets must come from the client's own official materials.
- Reference provenance to remember when a pack is chosen for a paid job: the formal pack's parameters were measured from decks licensed for study use only, and the SlidesMania-derived parameters carry a no-redistribution rule for the templates themselves — both are satisfied by building fresh decks from the abstracted specifications, and both forbid shipping anything derived from the reference files directly.
