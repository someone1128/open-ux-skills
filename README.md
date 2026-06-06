# Open UX Skills

Product-agnostic UX skills for AI coding agents and product agents.

These skills help an agent review, improve, and govern interaction design without assuming a specific product, brand, industry, or UI pattern.

Default language: **English**. Chinese is supported when requested.

All skill names use the `hzy-ux-` prefix so they are easy to search, filter, and trigger.

## What this is

This repository contains reusable UX skills for:

- deciding whether a UI should be changed at all
- avoiding unnecessary redesign
- exploring better interaction models
- allocating complexity to the right users and moments
- designing states, feedback, guidance, and motion
- reviewing AI-assisted workflows
- improving value clarity and trust
- reviewing accessibility, mobile UX, information architecture, and microcopy
- creating bounded UX change proposals
- checking UX regressions after implementation

These skills are intentionally product-agnostic. Examples may mention AI image, AI video, AI music, AI writing, SaaS dashboards, editors, community feeds, and creator tools, but the skills must not assume any one product.

## Why this exists

AI agents are good at creating technically correct UI.

They are less reliable at deciding whether the interaction model is right, whether an interface should remain unchanged, or whether a proposed "optimization" adds more complexity than value. The universe did not need another animated dropdown with unresolved childhood issues, so here we are.

## Skill list

| Skill | Purpose |
|---|---|
| `hzy-ux-maturity-router` | Decide whether to keep, polish, optimize, prototype, or redesign. |
| `hzy-ux-stop-rule` | Prevent unnecessary redesign of familiar, working UI patterns. |
| `hzy-ux-interaction-model-explorer` | Explore better interaction models beyond the current UI. |
| `hzy-ux-flow-review` | Review the full user path from intent to outcome. |
| `hzy-ux-complexity-allocation` | Allocate complexity instead of blindly hiding it. |
| `hzy-ux-interaction-state-design` | Design appropriate UI states based on task risk and complexity. |
| `hzy-ux-interaction-polish-guidance` | Improve feedback, micro-interactions, helper text, and guidance. |
| `hzy-ux-motion-director` | Decide whether motion is needed and how strong it should be. |
| `hzy-ux-pattern-case-library` | Reference reusable UX patterns without mechanically applying them. |
| `hzy-ux-ai-assisted-workflow-review` | Review AI-assisted workflows beyond chat-only agents. |
| `hzy-ux-value-trust-review` | Improve pricing, quota, upgrade, payment, and trust UX without dark patterns. |
| `hzy-ux-change-proposal` | Convert UX findings into bounded implementation proposals. |
| `hzy-ux-regression-check` | Check whether a UX change solved the original problem without creating new ones. |
| `hzy-ux-accessibility-review` | Review accessibility, keyboard use, focus, contrast, screen reader support, and reduced motion. |
| `hzy-ux-mobile-responsive-review` | Review mobile interaction, touch targets, keyboard overlap, responsive layout, and small-screen behavior. |
| `hzy-ux-information-architecture-review` | Review navigation, grouping, naming, hierarchy, feature organization, and user mental models. |
| `hzy-ux-copy-microcopy-review` | Review button labels, helper text, empty states, errors, success messages, tooltips, and high-risk copy. |

## Recommended workflow

For mature products:

```txt
/hzy-ux-maturity-router
↓
/hzy-ux-stop-rule when the UI may already be good
↓
/hzy-ux-interaction-model-explorer if a new task model may unlock value
↓
specific review skill
↓
/hzy-ux-change-proposal
↓
implementation
↓
/hzy-ux-regression-check
```

For new or complex features:

```txt
/hzy-ux-interaction-model-explorer
↓
/hzy-ux-flow-review
↓
/hzy-ux-complexity-allocation
↓
/hzy-ux-interaction-state-design
↓
/hzy-ux-motion-director if animation is involved
↓
/hzy-ux-change-proposal
↓
/hzy-ux-regression-check
```

For UI quality review:

```txt
/hzy-ux-accessibility-review
/hzy-ux-mobile-responsive-review
/hzy-ux-copy-microcopy-review
/hzy-ux-regression-check
```

For product structure review:

```txt
/hzy-ux-information-architecture-review
/hzy-ux-flow-review
/hzy-ux-pattern-case-library
```

## Test cases

The `test-cases/` folder documents expected behavior for common UX review scenarios.

Use these cases to check whether an agent is applying the skills correctly:

```txt
test-cases/should-not-redesign-search.md
test-cases/should-hide-api-fields.md
test-cases/should-prototype-new-interaction-model.md
test-cases/should-avoid-dark-pattern-upgrade.md
```

The goal is not automated unit testing. The goal is to prevent predictable UX-agent failures:

- redesigning mature conventions without evidence
- directly exposing API fields to users
- replacing a working UI instead of prototyping a new model
- using pressure or dark patterns to increase conversion

## Motion and GSAP

This repo does not duplicate GSAP implementation guidance. Use `hzy-ux-motion-director` to decide *whether* motion is needed, what purpose it serves, and whether CSS or a dedicated animation system is appropriate.

For implementation, consider the official GSAP AI skills when advanced timelines, ScrollTrigger, React integration, plugins, or performance guidance are needed. The official `greensock/gsap-skills` repository describes itself as official AI skills for GSAP and documents installation via `npx skills add https://github.com/greensock/gsap-skills`. See the repository for current instructions.

## Installation

Copy the `skills/` folder into your agent's skills directory.

Example:

```bash
cp -R skills/* ~/.claude/skills/
```

Or copy selected skill folders into your project-level skill directory.

## Design principles

1. Diagnose before optimizing.
2. Do not assume redesign is needed.
3. Preserve mature conventions unless there is clear friction.
4. Examples are references, not prescriptions.
5. Basic operations should follow conventions.
6. Complex tasks can explore new interaction models.
7. Allocate complexity to the right user, moment, and surface.
8. Motion should clarify, not decorate confusion.
9. Conversion must not rely on pressure, hidden costs, or dark patterns.
10. Every meaningful UX change should solve a real user problem.
11. Accessibility and mobile behavior are not optional decoration.
12. Copy is part of interaction design, not the leftovers after UI work.

---

# 中文说明

这是一个**通用交互设计 Skills 仓库**，默认英文，支持中文。

所有 Skill 都使用 `hzy-ux-` 统一前缀，方便搜索和筛选。

它不绑定任何具体产品、品牌、域名或业务场景。案例可以来自 AI 图片、AI 视频、AI 音乐、AI 写作、SaaS、社区、编辑器、创作工具等，但不能把某一种产品形态当成默认答案。

## 核心目标

让 AI 不再机械地：

- 看到字段就生成表单
- 看到按钮就加动画
- 看到“优化交互”就强行重设计
- 看到案例就套模板
- 看到 AI 就默认聊天框
- 看到转化就乱加付费弹窗

而是先判断：

- 这个 UI 是否真的需要改？
- 用户真正要完成什么任务？
- 当前交互模型是否合适？
- 什么应该保持不变？
- 最小有效改动是什么？
- 是否需要探索新的交互模型？
- 上线后如何验证？

## 推荐使用方式

成熟产品先用：

```txt
/hzy-ux-maturity-router
```

不要一上来就重设计。人类已经做了够多无意义改版，别让 AI 也加入拆墙队。
