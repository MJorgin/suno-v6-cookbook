# GitHub 发布包

本页用于准备公开仓库 `MJorgin/suno-v6-cookbook`。所有设置都可以手动完成，不需要自动化或账号授权。

## 仓库字段

| 字段 | 建议内容 |
|---|---|
| 仓库名 | `suno-v6-cookbook` |
| 简介 | `A bilingual, evidence-labeled Suno v6 cookbook for prompts, local edits, multimodal workflows, and rights-safe original music.` |
| Website | v0.1 先留空；以后有文档站再填写 |
| Social preview | 上传 [`../assets/social-card.png`](../assets/social-card.png)，尺寸 1280×640 |
| Wiki | 关闭 |
| Projects | 关闭 |
| Issues | 开启 |
| Discussions | 维护精力足够后开启；首发前可以先关闭 |

## Topics

建议使用这些 Topics：

```text
suno
suno-v6
ai-music
music-generation
prompt-engineering
awesome-list
multimodal
agents
agent-skills
songwriting
chinese
mandopop
markdown
creative-ai
```

## 首发设置顺序

1. 推送仓库后确认 README 首屏卡片正常显示。
2. 上传 1280×640 Social Preview。
3. 保持非官方声明在首屏可见位置。
4. 创建置顶 issue：`What Suno v6 workflow should we document next?`
5. 首次公开推送后创建轻量文档 Release：`v0.1.0`。
6. README 顶部保留中英双入口，方便中文和海外用户分流。

## Release 标题

```text
v0.1.0 — Bilingual Suno v6 Cookbook
```

## Release 文案

```markdown
## Awesome Suno v6 Cookbook v0.1.0

- 12 个工作流：创作、局部改词、多模态输入、采样、隔离、mashup、中文可唱性和失败诊断
- 12 个曲风提示词 Playbook
- 24 个原创、可复制案例
- 6 个高频失败笔记
- 1 个无依赖、纯 Markdown 的 Agent 写歌 Skill
- 英文和中文双入口
- 使用证据标签区分官方能力和仍需试听验证的实践假设
- 为素材类工作流提供权利与安全边界

这是独立社区项目，不是 Suno 官方资源。
```

## 英文发布帖

详见 [English Launch Kit](./launch-kit.md#english-launch-posts)。

## 中文发布帖

### 即刻

```text
给 Suno v6 做了一个开源 Cookbook。

里面有 12 个工作流、12 个曲风 Playbook、24 个原创可复制案例、6 个失败修复笔记，还有一个无依赖的 Suno v6 写歌 Skill。

重点不是堆提示词，而是把 v6 / v6-wild / v6-mini 怎么选、局部改词、人声备忘录、图片/视频转音乐、采样隔离、自有素材 mashup、中文可唱性和失败诊断讲清楚。每个案例都标了证据等级，也明确了素材权利边界。

英文主入口 + 中文入口：MJorgin/suno-v6-cookbook
```

### 小红书

标题：

```text
Suno v6 不会写提示词？我整理了一套开源菜谱
```

正文：

```text
最近 Suno v6 更新后，模型、素材输入和局部编辑方式都变多了。

我整理了一个开源 Cookbook：

1. v6 / v6-wild / v6-mini 怎么选
2. 12 个从灵感到改歌的工作流
3. 12 个曲风提示词 Playbook
4. 24 个原创可复制案例
5. 6 个常见翻车修复笔记
6. 一个纯 Markdown、无依赖的写歌 Skill
7. 中文、粤语、双语歌词可唱性建议

里面也特别强调：只用自己拥有或已获授权的素材，不做未授权采样，不冒充真实歌手。

适合想认真玩 AI 音乐、又不想靠玄学抽卡的人。
```

### 微信群 / 朋友圈

```text
我做了一个 Suno v6 开源 Cookbook：工作流、曲风 Playbook、原创案例、失败修复和写歌 Skill 都配齐了。中英双语，带证据标签，也写清了素材版权边界。仓库：MJorgin/suno-v6-cookbook。
```

## 发布节奏

| 时间 | 动作 |
|---|---|
| 第 0 天 | 发布仓库、上传社交卡片、设置 Topics、创建 `v0.1.0` Release |
| 第 0 天 | 发即刻/朋友圈中文短帖，以及英文 X/Threads 帖子 |
| 第 1 天 | 以创作者身份发 HN/Reddit，重点征求工作流反馈 |
| 第 2–3 天 | 回复 issue，把真实翻车案例沉淀成新的失败笔记 |
| 第 1 周 | 补 1 个 `community-tested` 案例，记录模型、日期、提示词和结果 |
| 第 2 周 | 发后续内容：“Suno v6 最常见的 5 类提示词翻车与修复” |

## 传播重点

这个项目的差异点不是“又一个提示词列表”，而是模型路由、局部编辑、多模态素材、中文可唱性、证据标签、版权边界和无服务/无凭据 Agent Skill 的组合。
