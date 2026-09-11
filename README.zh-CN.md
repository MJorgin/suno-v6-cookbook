# Awesome Suno v6 Cookbook

面向 Suno v6 的社区提示词菜谱：覆盖新歌创作、局部改词、多模态输入、采样/隔离、自有素材 mashup、中文可唱性与失败诊断。

[English](./README.md) · [贡献指南](./CONTRIBUTING.md) · [安全与版权](./docs/safety-and-copyright.md) · [CC-BY-4.0](./LICENSE)

> **非官方项目。** 本仓库是独立社区资料，不隶属于 Suno，也未获得 Suno 官方背书或认证。

> **安全边界：** 只使用你拥有或已获许可的文字、音频、图片、视频、人声录音和分轨。不要上传商业发行作品、盗版媒体、未授权采样，或要求冒充真实人物。

## 快速开始

1. 先用[模型路由表](./docs/model-router.md)选择 `v6`、`v6-wild` 或 `v6-mini`。
2. 从[编辑与 Mashup 工作流索引](./docs/edit-and-mashup-workflows.md)挑一个菜谱。
3. 从[曲风 Playbook](./docs/genre-playbook.md)选择乐器、人声和制作描述。
4. 直接参考[原创案例库](./library/examples/)里的可复制模板。
5. 生成失败时，用[失败笔记](./library/failure-notes/)定位原因。
6. 可安装纯 Markdown Agent Skill：[`suno-v6-songwriter`](./agents/skills/suno-v6-songwriter/SKILL.md)。

## v6 新能力

先读 [v6 新能力说明](./docs/what-is-new-in-v6.md)。官方事实来源是 Suno 公告：<https://suno.com/blog/introducing-v6>。

v6 的重点包括：

- 三个模型入口：`v6`、`v6-wild`、`v6-mini`；
- 用自然语言替换单句歌词或局部段落；
- 基于人声备忘录和音频素材继续创作；
- 采样、隔离乐器/人声，并围绕片段重建；
- 组合多个自有来源；
- 文本、音频、图片、视频等多模态输入。

不同套餐、地区和界面能力可能变化，请以 Suno 当前产品为准。

## 常见入口

| 我想…… | 从这里开始 |
|---|---|
| 不知道选哪个模型 | [模型路由表](./docs/model-router.md) |
| 写第一个高质量提示词 | [提示词结构](./docs/prompt-anatomy.md) |
| 改一句词或一个段落 | [编辑与 Mashup 工作流](./docs/edit-and-mashup-workflows.md) |
| 把人声备忘录做成歌 | [Voice Memo to Song](./library/workflows/06-voice-memo-to-song.md) |
| 用自己的 riff 建 beat | [Sample Riff to Beat](./library/workflows/08-sample-riff-to-beat.md) |
| 安全组合自有素材 | [Owned-Source Mashup](./library/workflows/10-owned-source-mashup.md) |
| 改善中文/双语可唱性 | [中文歌词指南](./docs/chinese-lyrics.md) |
| 修复跑偏的生成 | [Failure Diagnosis](./library/workflows/12-failure-diagnosis.md) |

## 内容库

- [12 个工作流](./docs/edit-and-mashup-workflows.md)：创作、改词、采样、隔离、mashup、中文与修复。
- [12 个曲风 Playbook](./docs/genre-playbook.md)：身份、乐器、人声、节奏制作、避坑和迷你模板。
- [24 个原创案例](./library/examples/)：带证据元数据，可复制后改写。
- [6 个失败笔记](./library/failure-notes/)：症状、原因、保守修复和探索性修复。
- [Agent Skill](./agents/skills/suno-v6-songwriter/SKILL.md)：纯 Markdown，无依赖、不联网、不处理账号信息。

## 证据等级

| 标签 | 含义 |
|---|---|
| `official` | 官方来源直接说明 |
| `official-informed` | 基于官方能力推导的实用提示词 |
| `community-tested` | 有可复现实验记录的社区测试 |
| `working-hypothesis` | 尚未验证、需要试听的实践假设 |
| `legacy-v5` | V5/V5.5 旧经验，可能需要在 v6 重测 |

案例元数据格式见 [Case Schema](./docs/case-schema.md)。

## 仓库原则

- v0.1 只做 Markdown：无包管理、无运行依赖、无 API 客户端、无浏览器自动化、不上传媒体。
- 明确区分官方事实和仍需试听验证的提示词经验。
- 所有案例保持原创，避免商业歌词和指定真实歌手模仿。
- 所有素材工作流先确认权利和使用范围。
- 英文 README 是全球入口，中文 README 服务中文创作者。

## 参与贡献

欢迎 issue 和 pull request。新增内容前请先阅读 [CONTRIBUTING.md](./CONTRIBUTING.md)。

## 许可

文本内容采用 [CC-BY-4.0](./LICENSE)。相关商标归其权利人所有。
