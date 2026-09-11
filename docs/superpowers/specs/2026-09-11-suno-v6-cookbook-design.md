# Suno v6 Cookbook 项目设计规格

日期：2026-09-11  
状态：已确认，待实施  
负责人：MJorgin + Codex

公开仓库：`MJorgin/suno-v6-cookbook`  
展示标题：`Awesome Suno v6 Cookbook`

## 1. 背景与机会

Suno 于 2026-09-09 正式发布 v6 系列模型。v6 不只是旧模型的质量升级，而是引入了新的模型分工和创作工作流：

- `v6`：面向 Pro / Premier 的旗舰模型，强调准确、稳定、精致和可控。
- `v6-wild`：面向探索，强调意外性、纹理感和更大胆的变化。
- `v6-mini`：面向所有用户的快速模型，适合草稿、低成本试唱和高频迭代。
- 自然语言局部编辑：只替换某一句歌词或某一个段落，同时保留其他部分。
- Mashup：从多个已有素材中抽取人声、鼓点、旋律或情绪并组合。
- 采样、拆轨和新建 beat：围绕音频片段完成 isolate、sample 和 rebuild。
- 多模态输入：从文本、音频、图片、视频和语音备忘录开始创作。

截至 2026-09-11，GitHub 上尚未出现成熟的 Suno v6 专项仓库。已有 Suno 技能主要停留在 V5 / V5.5，且大多存在以下问题：

- 只覆盖 Style Prompt 和歌词，不覆盖 v6 的局部编辑、mashup 和多模态输入；
- 以浏览器自动化或第三方 API 为卖点，带来账号、凭据和服务条款风险；
- 星标与验证不足，很多提示词没有来源、适用条件或失败记录；
- 大型插件过重，需要 Python、MCP、Playwright 或云端配置；
- 中文可唱性、中文曲风标签和跨语言发音支持不足。

机会窗口来自“新模型 + 新工作流 + 缺少可信资料”。项目应先成为最清楚、最安全、最容易复制的 Suno v6 知识库，再扩展成 Agent Skill 和案例社区。

## 2. 项目定位

最终仓库名：`suno-v6-cookbook`

GitHub 展示标题使用 `Awesome Suno v6 Cookbook`。仓库 slug 保留 `cookbook` 品牌，标题和 README 首屏保留 `awesome` 与 `suno v6` 搜索关键词。

英文一句话定位：

> A curated, evidence-labeled Suno v6 prompt, workflow, example, and agent-skill library.

中文一句话定位：

> 一个带证据分级、可直接复制使用的 Suno v6 提示词、工作流、案例库与 Agent Skill。

项目不是 Suno 官方项目，不以自动登录、自动扣费、绕过权限或调用私有 API 为目标。第一性原理是：

1. 用户把内容复制到 Suno，自己决定是否生成；
2. 所有规则都标明来源和可信等级；
3. 所有模板都能离线阅读和被 Agent 使用；
4. 不要求账号、API Key、浏览器插件或第三方付费服务；
5. 优先沉淀会随 v6 长期有效的工作流，而不是追逐短期玄学参数。

## 3. 目标用户

### 主要用户

- 第一次使用 Suno v6，但被 v6、v6-wild、v6-mini 选择困扰的创作者；
- 已有 V5 经验，想迁移到 v6 工作流的 Suno 用户；
- 需要写中文歌词、英文歌词或跨语言可唱文本的创作者；
- 想把语音备忘录、图片、视频或参考音频转成歌的人；
- 使用 Codex、Claude Code、Cursor、Gemini CLI 等 Agent 的提示词用户。

### 次要用户

- 音乐制作人和内容运营，需要批量探索曲风、hook 和短视频 BGM；
- 研究者或写作者，想记录 AI 音乐提示词的可复现实验；
- 开源社区贡献者，想补充曲风案例、语言案例或失败案例。

## 4. v0.1 范围

v0.1 只发布纯 Markdown 内容和纯文本 Agent Skill，不做网站、不执行脚本、不接第三方服务。

### 必须交付

1. 中英双语 README；
2. v6 官方新能力摘要；
3. `v6 / v6-wild / v6-mini` 模型路由表；
4. Suno v6 提示词结构说明；
5. 10 个 v6-native 工作流模板；
6. 12 个曲风或场景 Playbook；
7. 24 个原创虚构案例；
8. 中文歌词和跨语言发音指南；
9. 安全、版权和商标边界文档；
10. 贡献指南和案例提交流程；
11. 一个无脚本、无外联、无凭据要求的 `suno-v6-songwriter` Agent Skill。

### 暂不交付

- 不做可视化网站；
- 不做 npm / pip 包；
- 不做 Suno 账号登录或浏览器自动化；
- 不接 Suno 私有 API 或第三方中转 API；
- 不上传受版权保护音频、商业歌曲或用户私人素材；
- 不承诺生成效果，不提供付费代生成；
- 不伪造“数百个实测案例”。

## 5. 建议目录结构

```text
suno-v6-cookbook/
├── README.md
├── README.zh-CN.md
├── LICENSE
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── agents/
│   └── skills/
│       └── suno-v6-songwriter/
│           ├── SKILL.md
│           └── references/
│               ├── model-router.md
│               ├── prompt-patterns.md
│               ├── edit-and-mashup.md
│               ├── chinese-lyrics.md
│               └── quality-checklist.md
├── docs/
│   ├── what-is-new-in-v6.md
│   ├── model-router.md
│   ├── prompt-anatomy.md
│   ├── lyric-and-section-tags.md
│   ├── edit-and-mashup-workflows.md
│   ├── multimodal-inputs.md
│   ├── genre-playbook.md
│   ├── chinese-lyrics.md
│   ├── safety-and-copyright.md
│   └── case-schema.md
├── library/
│   ├── workflows/
│   ├── genres/
│   ├── examples/
│   └── failure-notes/
└── docs/superpowers/
    └── specs/
        └── 2026-09-11-suno-v6-design.md
```

`agents/skills/suno-v6-songwriter/` 是唯一正式 Skill 路径。详细解释放在 `docs/`，Skill 内只保留 Agent 在生成时必须加载的短参考。这样既符合开放 Agent Skill 的常见结构，也方便用户直接复制目录到本地 Skill 文件夹。

## 6. 内容架构

### 6.1 模型路由

模型选择按任务而不是按“新旧”判断：

| 任务 | 默认模型 | 备选模型 | 判断依据 |
|---|---|---|---|
| 明确曲风、明确歌词、要求稳定成品 | v6 | v6-mini | 追求一次性贴近目标 |
| 探索 hook、奇怪曲风、意外编曲 | v6-wild | v6 | 需要变化和灵感 |
| 快速试旋律、低成本改词 | v6-mini | v6 | 速度和额度优先 |
| 局部替换一句歌词 | v6 | v6-mini | 需要保持上下文一致 |
| 多素材 mashup | v6 | v6-wild | 需要理解多个来源及保留关系 |
| 音频采样、拆轨、围绕 riff 建 beat | v6 | v6-wild | 需要精确抽取和重组 |
| 图片 / 视频转音乐 | v6-wild | v6 | 先探索情绪，再用 v6 精修 |
| 中文流行情歌 | v6 | v6-mini | 发音、结构和情绪稳定性优先 |

### 6.2 提示词四层结构

所有案例统一拆成四层：

1. **Creative Intent**：创作目标、故事、情绪、使用场景；
2. **Music Direction**：曲风、年代、节奏、BPM、调式、乐器、制作质感；
3. **Vocal Direction**：人声年龄感、性别或音色、演唱方式、咬字、和声；
4. **Edit / Source Instruction**：参考素材、保留内容、替换内容、局部编辑和输出约束。

禁止把艺人名字作为直接模仿目标。若用户提到艺人，Skill 应将其转译为客观特征，例如年代、编曲、鼓组、空间感、唱法和情绪，不保留可识别的人名或歌曲名。

### 6.3 v6-native 工作流

v0.1 至少覆盖 10 个工作流：

1. 文本到完整歌曲；
2. 一句话情绪到歌曲；
3. 中文歌词可唱性优化；
4. 单句歌词替换；
5. 单段合唱改为福音合唱或其他演唱形式；
6. 从语音备忘录生成歌曲；
7. 从图片或视频生成氛围音乐；
8. 从音频中采样 riff 并新建 beat；
9. 隔离某个乐器或人声后重组；
10. 多首自有素材 mashup；
11. `v6-wild` 探索后回到 `v6` 精修；
12. 失败结果诊断与下一轮迭代。

### 6.4 案例格式

每个案例使用 Markdown 正文加 YAML Frontmatter。机器读结构化字段，人读完整解释。

```yaml
---
id: pop-zh-urban-rain-001
title: 中文都市雨夜情歌
language: zh-CN
genre: mandopop
workflow: text-to-song
model: v6
inputs: [text]
evidence_tier: official-informed
verified: false
created_at: 2026-09-11
updated_at: 2026-09-11
tags: [urban, ballad, rainy-night, female-vocal]
---
```

正文固定包含：

- 目标；
- 适用模型；
- 输入素材；
- Style Prompt；
- Exclude Styles；
- 歌词与结构标签；
- 局部编辑指令；
- 预期结果；
- 已知失败模式；
- 下一轮迭代建议；
- 证据说明。

## 7. 证据分级

所有内容必须标注证据等级，不能把 V5 经验包装成 v6 官方事实。

| 等级 | 标识 | 含义 | 使用方式 |
|---|---|---|---|
| T0 | `official` | 来自 Suno 官方 v6 博客、发布说明或帮助文档 | 可作为确定规则 |
| T1 | `official-informed` | 由官方 v6 能力合理推导，并明确说明推导路径 | 可作为默认建议 |
| T2 | `community-tested` | 有社区或贡献者实测记录，包含输入、结果和日期 | 可收录，但保留失败可能 |
| T3 | `working-hypothesis` | 尚未实测的工作假设 | 只能作为实验模板 |
| T4 | `legacy-v5` | V5 / V5.5 经验，可能仍有效 | 必须提示 v6 待验证 |

当 Suno 更新与旧规则冲突时，高等级证据覆盖低等级证据，旧案例不删除，标记为 superseded。

## 8. Agent Skill 设计

Skill 名称：`suno-v6-songwriter`

### 触发场景

- 用户要求写 Suno v6 提示词；
- 用户要求写歌词、改歌词或翻译到可唱文本；
- 用户要求选择 v6、v6-wild、v6-mini；
- 用户要求生成局部编辑、mashup、采样、拆轨或多模态输入指令；
- 用户给出一个 Suno 失败结果并要求诊断下一轮提示词。

### 输出格式

默认输出：

1. 推荐模型及理由；
2. Style Prompt；
3. Exclude Styles；
4. Lyrics / Section Tags；
5. v6 Edit Instruction；
6. 可选的多模态输入描述；
7. 风险与版权提示；
8. 若第一次失败，下一轮三条修改建议。

### 安全边界

Skill 必须：

- 只输出可复制文本；
- 不要求 Suno 密码、Cookie、会话 Token 或 API Key；
- 不启动浏览器，不点击 suno.com，不替用户消耗额度；
- 不上传用户素材；
- 不生成绕过版权、商标或平台限制的指令；
- 不承诺生成某名艺人的真实声音；
- 遇到用户要求“克隆某歌手声音”时，改写为非侵权的客观音色描述。

## 9. 合规与版权策略

项目首页和贡献指南必须明确：

- 本项目是非官方社区项目，与 Suno 无隶属关系；
- Suno 是其权利人的商标或品牌标识，项目仅用于描述；
- 仓库只收录原创文本、用户有权使用的素材说明和公开官方资料摘要；
- 不收录商业歌曲完整歌词、盗版音频、扒带文件或未授权采样；
- 不提供艺人声音克隆、冒充、虚假代言或规避检测的教程；
- 用户对自己输入 Suno 的素材和生成结果负责；
- 侵权投诉通过 issue 或仓库邮箱处理，收到明确投诉后先下架再核验。

许可证建议：

- 文档、案例和提示词使用 CC-BY-4.0；
- 未来如果加入脚本或工具代码，再使用 MIT；
- v0.1 的纯 Markdown 仓库可先统一使用 CC-BY-4.0，保留未来并行加入 MIT `tools/` 目录的空间。

## 10. 与参考项目的差异

`awesome-gpt-image-2` 的可借鉴点是：视觉化首页、模板库、案例库、Agent Skill 和强 SEO。不能照抄它在模型刚更新时容易出现的问题。

本项目的差异：

- 首发先追求准确和可验证，不追求虚假的大数量；
- 每个案例都带证据等级、失败模式和迭代建议；
- 明确区分官方能力、推导规则、社区实测和旧版经验；
- Skill 无脚本、无依赖、无账号访问；
- 中文和英文同等重要，但英文 README 作为全球传播入口；
- 网站等案例数达到 50 个以上、结构稳定后再做。

## 11. 发布与增长

### 首发物料

- GitHub README：30 秒内说明是什么、为什么可信、如何复制第一条提示词；
- 一张 1280×720 的简单横幅，文案为 “Suno v6 Prompt & Workflow Library”；
- 一篇中文发布短文，强调 v6 新工作流和安全边界；
- 一篇英文发布短文，强调 evidence-labeled prompts 和 agent-ready skill；
- 3 张可转发卡片：模型路由、v6 工作流、提示词四层结构。

### 发布渠道

按风险从低到高：

1. GitHub Topics：`suno`、`suno-v6`、`ai-music`、`prompt-engineering`、`agent-skill`；
2. 个人 X / 即刻 / 少数派或小红书；
3. Suno Discord 或相关社区，先阅读自推规则；
4. Reddit 的 r/Suno 等社区，避免硬广，以“我整理了 v6 工作流，求纠错”为姿态；
5. 向已有 Suno 工具项目或 awesome 列表提交 PR。

### 冷启动指标

发布后第一周关注：

- Star 数，但不只看 Star；
- 外部引用和 awesome list 收录；
- issue / PR 数量；
- 被纠正的规则数量；
- Skill 安装或复制反馈；
- 实际案例的复现反馈。

合理目标：首周 100–200 Star、5 个有效 issue、3 个社区案例；一个月达到 50 个以上案例后再评估网站。

## 12. 质量保证

v0.1 无代码依赖，仍执行内容质量检查：

- 每个案例必须有模型、工作流、证据等级和更新时间；
- 不出现“保证”“100% 复刻”“官方认证”等误导措辞；
- 所有官方事实必须能回到 Suno 官方博客、发布说明或帮助文档；
- V5 规则必须单独标记，不与 v6 规则混写；
- 每个提示词都要能被不懂音乐术语的人复制使用；
- 中文歌词必须检查断句、押韵、人称、数字和英文缩写的可唱性；
- Skill 不包含命令执行、网络请求、API Key、Cookie 或浏览器自动化；
- README 中的相对链接必须有效。

未来加入 CI 时再检查 Markdown frontmatter、死链、商标词和敏感凭据，但 v0.1 不引入安装依赖。

## 13. 风险与应对

| 风险 | 影响 | 应对 |
|---|---|---|
| v6 界面或能力快速变化 | 案例过期 | 证据分级、更新日期、过期标记 |
| V5 经验误导用户 | 可信度下降 | 单独标 T4，不默认套用 |
| 用户要求模仿艺人 | 版权 / 商标风险 | 转译客观特征，拒绝冒充 |
| 第三方 API 或自动工具搭便车 | 用户凭据风险 | 首页明确不授权、不推荐 |
| 案例数量不如大型仓库 | 初期看起来薄 | 宁可 24 个高质量案例，不做虚假数字 |
| 中文内容全球传播受限 | Star 增长慢 | 英文主入口，中文作为差异化内容 |
| 官方更新慢于社区实践 | 内容不完整 | 保留社区实测与失败记录通道 |

## 14. 实施阶段

### 阶段 A：规格确认

- 确认仓库名、许可证、语言策略和 v0.1 范围；
- 用户评审本设计；
- 设计获批后再写实施计划。

### 阶段 B：v0.1 内容骨架

- 初始化 README、贡献指南和许可证；
- 完成 v6 官方能力摘要、模型路由和提示词结构；
- 完成 10 个工作流模板；
- 完成 24 个案例的第一批。

### 阶段 C：Agent Skill

- 编写 `suno-v6-songwriter/SKILL.md`；
- 编写五个短参考文件；
- 用中文、英文和跨语言案例做手动验收；
- 检查无脚本、无外联、无凭据字段。

### 阶段 D：发布准备

- 完成双语 README 润色；
- 准备中英文发布帖；
- 检查商标、版权和非官方声明；
- 由用户决定 GitHub 账号和公开时间。

## 15. 验收标准

v0.1 满足以下条件才公开：

- README 能在 30 秒内解释项目价值；
- 至少 24 个原创案例，全部带证据等级；
- 至少 10 个 v6-native 工作流；
- Skill 可直接复制到 Codex / Claude 的技能目录；
- Skill 全文无网络请求、命令执行、账号或 API Key 要求；
- 安全和版权边界在首页可见；
- 所有 V5 遗留经验都明确标记；
- 没有未核实的“官方说法”；
- 用户确认 GitHub 仓库名、许可证和发布身份。

## 16. 已确认决策

1. 仓库名采用 `suno-v6-cookbook`；
2. 展示标题采用 `Awesome Suno v6 Cookbook`；
3. 以英文 README 为主入口、中文 README 为第二语言；
4. 文档和案例许可证采用 CC-BY-4.0；
5. v0.1 坚持纯 Markdown、无脚本和无第三方服务；
6. 公开账号使用个人 GitHub 账号 `MJorgin`。
