# 看看别人怎么做 · Research Solution Radar

一个面向研究生和研发人员的 Codex skill：**先确认你想解决什么，再查相关研究，最后给出带引用的做法或 idea。**

适合你已经在 Codex 中讨论项目，但还不确定该参考哪些工作、有哪些方向值得尝试的时候。

## 怎么用

安装后，在项目聊天里直接说：

> 帮我看看别人是怎么做的。

或者：

> 帮我看看有什么好的 idea。

它会先根据当前上下文确认需求。如果你还没想清楚，会提供两三个具体方向帮你选择；确认后再检索。默认介绍最相关的两三项，解释别人做了什么、能借鉴什么，并附原论文、官方文档或作者代码的链接。

需要明确调用时，可以说：

```text
使用 $research-solution-radar，帮我看看别人怎么解决当前问题。
```

## 安装

在提供 `skill-installer` 的 Codex 环境中，发送：

```text
请使用 skill-installer，从以下地址安装 research-solution-radar：
https://github.com/2950126474/research-solution-radar/tree/main/skills/research-solution-radar
```

也可以下载本仓库，将 `skills/research-solution-radar` 整个文件夹放入你的 Codex 用户技能目录：通常是 `~/.codex/skills/`，Windows 对应 `%USERPROFILE%\.codex\skills\`。如果设置了 `CODEX_HOME`，使用其下的 `skills/`。已有同名技能时，先比较或备份再更新。

安装后建议新开项目聊天测试。不要把整个仓库当成技能目录；技能入口是 [`skills/research-solution-radar/SKILL.md`](skills/research-solution-radar/SKILL.md)。

## 一次典型对话

以下为使用方式示例，不是检索结果或效果承诺。

**用户：** 帮我看看有什么好的 idea。

**AI：** 结合当前项目，你更想解决现有方法的不足，还是探索一个新课题方向？

**用户：** 想找能用现有数据尝试的研究问题。

**AI：** 检索相关工作后，说明已有方法、适用条件和候选想法，并把来源链接放在对应说法旁边。明确区分别人已验证的成果和仍需验证的建议。

## 需要什么

- 支持加载技能的 Codex 环境。
- 可用的联网检索能力；技能本身不附带搜索服务、API key 或论文数据库。
- 当前问题的基本上下文。它不会自动获得所有聊天或所有项目的内容。

不要求安装 Firecrawl、Obsidian 或其他特定第三方插件；使用运行环境已有的搜索工具即可。

## 边界与当前状态

- 这是按需使用的检索工作流，不是后台监控或定时推送软件。
- 自然语言触发取决于运行环境和模型；未触发时可明确调用技能。
- 尽量核对近期原始来源，但不保证穷尽最新成果，也不保证每条引用和推论正确。
- 论文 idea 是待验证建议，不等于已确认的新颖性或发表保证。
- 不因检索而自动运行实验、安装依赖或改动研究方案。
- 技能要求避免向外部查询上传私人数据，但它不是独立的数据隔离系统。

目前是早期公开试用版：技能结构通过校验，已在一个真实项目中观察到自然语言触发、需求确认及随后检索的流程；尚未完成跨领域的系统性评测。欢迎报告失败案例。

## 反馈与讨论

欢迎在 [Issues](https://github.com/2950126474/research-solution-radar/issues) 发起反馈或评论已有讨论，也欢迎提交 Pull Request。

最有帮助的反馈是：你问了什么、期望得到什么、实际发生什么。特别欢迎反馈误触发、反复确认、回答太长、引用不支持结论或建议脱离项目条件。请先移除私人数据、密钥、客户资料及未公开研究细节。

试用场景见 [pilot.md](skills/research-solution-radar/references/pilot.md)。

## English overview

A Chinese-first Codex skill for related-work discovery and research ideation. It clarifies the user's intent, searches relevant and recent primary sources, then offers concise, cited approaches or ideas grounded in the current project. It uses the host's search tools and does not require a specific provider. Natural-language invocation and research quality are not guaranteed; feedback is welcome through Issues.

## License

[MIT](LICENSE).