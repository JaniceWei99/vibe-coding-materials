# Vibe Coding 知识库 · Markdown 版

从零到一的 AI 编程完整指南（可直接编辑与版本管理）。本文件为 `knowledge-base.html` 的 Markdown 等价内容，结构与章节一致，并补充了新增加的第 9-18 章。

---

## 目录

- 第一章：AI 编程与 Vibe Coding
- 第二章：TRAE 安装与使用
- 第三章：Prompt Engineering
- 第四章：Git 版本控制
- 第五章：实战项目——智能记事本
- 第六章：进阶技巧与避坑指南
- 第七章：项目部署上线
- 第八章：课后学习路径
- 第九章：前后端分离（新增）
- 第十章：App 上架与小程序发布（新增）
- 第十一章：AI 编程工具对比（新增）
- 第十二章：Token 与费用（新增）
- 第十三章：开发阶梯：从 HTML 到 App（新增）
- 第十四章：更多选题方向（新增）
- 第十五章：课堂互动 Vibe Coding（新增）
- 第十六章：让 AI 给自己写一封信（新增）
- 第十七章：无 Git 账号的教学方案（新增）
- 第十八章：团队 Vibe Coding 分工（新增）
- 附录 A：Prompt 速查手册
- 附录 B：Git 命令速查表
- 附录 C：常见问题 FAQ

---

## 第一章：AI 编程与 Vibe Coding

### 1.1 AI 编程发展历程

| 时间 | 事件 | 意义 |
| --- | --- | --- |
| 2021-06 | GitHub Copilot 预览版 | 第一个规模化 AI 代码补全工具 |
| 2022-11 | ChatGPT 发布 | AI 走向大众，形成对话式编程 |
| 2023-03 | GPT-4 | 复杂代码与推理能力跃升 |
| 2024 | Cursor 爆火 | AI IDE 形态成熟 |
| 2025-02 | Karpathy 提出“Vibe Coding” | 自然语言编程的方法论定名 |

> 关键人物：Andrej Karpathy（前 OpenAI 联合创始人、前特斯拉 AI 总监）。

### 1.2 什么是 Vibe Coding

- 用自然语言描述需求，AI 负责生成与修改代码。
- 你负责提出需求、审查结果、做取舍与决策。

| 对比项 | 传统编程 | Vibe Coding |
| --- | --- | --- |
| 核心技能 | 语法、API | 需求描述、迭代指导 |
| 写代码的人 | 你 | AI（你审查） |
| Debug | 自查 | 告诉 AI 现象让其修复 |
| 学习周期 | 长 | 短 |

> 一句话：你是导演，AI 是编剧 + 程序员。

### 1.3 Copilot vs Agent 模式

| 特性 | Copilot（副驾驶） | Agent（智能体） |
| --- | --- | --- |
| 工作方式 | 你写，AI 补全 | 你说，AI 规划执行 |
| 能力范围 | 补全/建议 | 创建/修改文件、运行命令、修 Bug |
| 代表工具 | GitHub Copilot | TRAE、Cursor、Windsurf |

> 本课程采用 Agent 模式。

### 1.4 为什么学 Vibe Coding

- 10× 效率提升。
- 就业竞争力：会用 AI 编程逐渐成为基本功。
- 实现创意门槛更低。

---

## 第二章：TRAE 安装与使用

### 2.1 TRAE 是什么

| 特性 | 说明 |
| --- | --- |
| 价格 | 完全免费 |
| 出品 | 字节跳动（国内直连） |
| 语言 | 中文界面与对话 |
| 模型 | 内置，无需 API Key |
| 基础 | 基于 VS Code |
| 模式 | Agent + Chat |

> 对比：Cursor 流行但部分功能付费；TRAE 免费且本地体验佳，适合教学。

### 2.2 安装步骤

1) 从 trae.ai 下载并安装（Win/macOS）。
2) 登录字节账号（手机可注册）。
3) 在电脑新建项目文件夹并用 TRAE 打开。

### 2.3 界面介绍

| 区域 | 位置 | 用途 |
| --- | --- | --- |
| 文件管理器 | 左侧 | 项目文件 |
| 代码编辑器 | 中央 | 编辑代码 |
| AI 面板 | 右侧 | 对话、指令 |
| 终端 | 底部 | 运行命令（Ctrl+`） |
| Git 面板 | 左侧图标 | 版本控制 |

### 2.4 Agent vs Chat

| 特性 | Agent 模式 | Chat 模式 |
| --- | --- | --- |
| 功能 | 自动改动代码/文件 | 仅回复，不改文件 |
| 适用 | 做项目、修 Bug | 学习、问答 |

### 2.5 第一个项目：个人介绍网页

示例 Prompt：

```text
帮我创建一个个人介绍网页，要求：
1. 单个HTML文件
2. 深色主题，现代简约风格
3. 包含：名字、照片占位符、自我介绍、兴趣爱好、联系方式
4. 有好看的动画效果
5. 响应式设计，手机也能看
```

---

## 第三章：Prompt Engineering

### 3.1 好 Prompt vs 坏 Prompt

| 坏 Prompt | 好 Prompt |
| --- | --- |
| “帮我做一个网站” | “单个 HTML，深色主题，待办功能，可添加/删除，数据保存在浏览器本地” |
| “代码有 Bug” | “点击添加后任务未显示，控制台无报错” |
| “优化一下” | “任务卡片加悬停效果；添加任务有淡入动画” |

> 原则：越具体越好。

### 3.2 五个核心技巧

1) 说清“要什么”，少说“怎么做”。
2) 给上下文与用户画像。
3) 一次一件事，逐步迭代。
4) 用例子和参考。
5) 不满意就迭代到满意。

### 3.3 万能 Prompt 模板

```text
我想做一个 [项目类型]，具体要求如下：
功能需求：
- [核心功能1]
- [核心功能2]
技术要求：
- [技术/存储/部署]
设计要求：
- [风格/参考]
用户： [谁会用]
```

### 3.4 迭代对话示例

- 修改外观：“整体深色，按钮用蓝紫渐变。”
- 添加功能：“给任务加截止日期，过期标红。”
- 修复问题：“添加后未清空输入框，新任务应置顶。”

---

## 第四章：Git 版本控制

### 4.1 为什么需要 Git

没有 Git：大量“备份_最终版_真的最终版.html”。
有 Git：一次提交一张快照，随时回退；多人协作。

### 4.2 核心概念

| 概念 | 类比 | 命令 |
| --- | --- | --- |
| 仓库 | 受管项目文件夹 | `git init` |
| 暂存 | 选要拍的快照 | `git add .` |
| 提交 | 拍快照 | `git commit -m "msg"` |
| 分支 | 平行宇宙 | `git checkout -b feat` |
| 推送 | 传云端 | `git push` |

### 4.3 常用命令速查

```bash
git init
git add .
git commit -m "msg"
git status
git log --oneline
git push origin main
git pull
git checkout -- .
git reset --hard HEAD~1
```

### 4.4 在 TRAE 中使用 Git

- Git 面板按钮即可完成 add/commit/push。
- 让 AI 执行 Git：“帮我把当前代码提交到 Git，备注写‘完成基础布局’”。

### 4.5 GitHub 远程仓库

1) 注册 GitHub，创建仓库。
2) 关联并推送：

```bash
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main
```

---

## 第五章：实战项目——智能记事本

- 目标：纯 HTML/CSS/JS（单文件）实现笔记增删查、持久化（LocalStorage）。
- 迭代 5 步：基础 → 删除+持久化 → 搜索 → 美化 → 进阶功能（标签/编辑/统计）。
- 每步完成后 `git commit`。

---

## 第六章：进阶技巧与避坑

- 先规划（问题/功能/优先级/草图）再动手。
- 小步快跑：每次一个改动 + 测试 + 提交。
- 四大翻车：越改越乱、AI 自说自话、不看代码、一次说太多。
- Debug：把错误信息直接给 AI；描述现象；必要时回滚。

---

## 第七章：项目部署上线

- 静态站点免费方案：GitHub Pages（最简单）、Vercel/Netlify（自动化更强）。
- GitHub Pages：仓库 Settings → Pages → 选择 main → Save → 等待 1-2 分钟。
- Vercel：GitHub 登录 → Import 项目 → Deploy → 之后每次 push 自动部署。

---

## 第八章：课后学习路径

### 8.1 短期练手（1-2 周）示例

| 难度 | 项目 | 核心 |
| --- | --- | --- |
| ⭐ | 猜数字 | 基础交互 |
| ⭐ | 番茄钟 | 计时/状态 |
| ⭐⭐ | 记账 | LocalStorage/统计 |
| ⭐⭐ | 打卡器 | 日期/持久化 |
| ⭐⭐⭐ | 天气查询 | API 请求 |
| ⭐⭐⭐ | Markdown 编辑器 | 文本解析/预览 |

### 8.2 中期方向（1-3 月）

- 前端基础 → 前端框架（React/Vue）
- Python + AI 入门
- 简单后端（Node/Flask）

### 8.3 推荐资源

| 类型 | 资源 | 说明 |
| --- | --- | --- |
| 文档 | MDN | Web 技术权威文档 |
| 课程 | freeCodeCamp | 免费课程（含中文） |
| 视频 | B 站 | 搜“AI 编程”“Vibe Coding” |
| 社区 | GitHub/掘金 | 实践/教程 |

---

## 第九章：前后端分离（新增）

### 9.1 定义

- 前端（界面/交互）与后端（业务/数据）分离，通过 API 通信。

### 9.2 优劣

- 优势：并行开发；一套后端服务多端；技术自由；体验更好；维护方便。
- 劣势：复杂度↑；SEO 需 SSR；首屏加载慢；学习曲线高。

### 9.3 案例对比：校园二手平台

- 传统：服务器拼接 HTML 返回整页，难复用到 App/小程序。
- 分离：后端提供 `/api/products` 等接口，前端（Web/小程序/App）公用同一套 API。

---

## 第十章：App 上架与小程序发布（新增）

### 10.1 上架流程要点

- iOS：Apple 开发者账号（个人$99/年，企业$299/年）→ 证书与描述文件 → Xcode/TestFlight → 审核 1-3 天。
- Android：Google Play（$25 一次性）或国内各厂商商店（分别注册和提交）。
- 鸿蒙：华为开发者联盟 + DevEco Studio（ArkTS）。
- 微信小程序：公众平台注册 → 微信开发者工具 → 体验版 → 审核 1-7 天。

### 10.2 编译环境

| 平台 | IDE | 编译 | 备注 |
| --- | --- | --- | --- |
| iOS | Xcode | 本地 | 需 macOS/Mac |
| Android | Android Studio | 本地 | Win/Mac/Linux |
| 鸿蒙 | DevEco Studio | 本地 | Win/Mac |
| 小程序 | 微信开发者工具 | 云编译 | 门槛低 |

### 10.3 个人 vs 企业（选摘）

- 小程序个人：类目受限、无法接微信支付/电商/直播/社交；企业认证后放宽限制。

---

## 第十一章：AI 编程工具对比（新增）

- Claude Code：终端型 Agent，理解大项目强，上下文大（200K），门槛/价格高。
- OpenAI Codex/ChatGPT：CLI/网页多形态，GPT-4o/o3 模型强，API 计费较贵。
- TRAE：本地免费中文 IDE，适合教学与入门，Agent 能力内置。

| 对比项 | TRAE | Claude Code | Codex CLI | Cursor |
| --- | --- | --- | --- | --- |
| 费用 | 免费 | 付费 | 付费 | 免费额度 + 付费 |
| 界面 | IDE | 终端 | 终端 | IDE |
| 国内可用 | 直连 | 需翻墙 | 需翻墙 | 需翻墙 |
| 上手 | 低 | 高 | 高 | 中 |

> 限制共性：不是万能；会幻觉；上下文有限；结果有波动。

---

## 第十二章：Token 与费用（新增）

### 12.1 Token 是什么

- 文字/代码被切分为 Token；输入与输出都会计费。

### 12.2 费用估算（示例）

- 小项目：总计 ~ 输入 10.5K / 输出 20K Token，GPT-4o 约 $0.40，Claude Sonnet 约 $0.11。

### 12.3 价格参考（2025 中）

| 模型 | 输入/$ 每百万 | 输出/$ 每百万 |
| --- | --- | --- |
| GPT-4o | 2.50 | 10.00 |
| GPT-4o-mini | 0.15 | 0.60 |
| Claude Sonnet 4 | 3.00 | 15.00 |
| Claude Haiku | 0.25 | 1.25 |
| DeepSeek V3 | 0.27 | 1.10 |

> 学生建议：TRAE（免费） + ChatGPT/Claude 免费版问答。

---

## 第十三章：开发阶梯——从 HTML 到 App（新增）

- 先做单机 HTML：零配置、立即见效、聚焦与 AI 协作。
- 五级阶梯：HTML → API 网页 → 小程序 → 全栈分离 → 跨平台 App。
- 每级推荐工具：TRAE/浏览器 → 微信开发者工具 → Node/Python → Flutter/原生工具链。

---

## 第十四章：更多选题方向（新增）

- 生活工具：AA 记账、倒数日、随机点名、菜谱推荐、排班表、财务看板。
- 学习辅助：Markdown 笔记、番茄钟、单词卡、课程表、倒计时、错题本、GPA。
- 娱乐游戏：猜数字、RPS、成语接龙、2048、打字测试、贪吃蛇、五子棋、节拍。
- 社交创意：表白墙、校园地图、心情日记、匿名投票、博客、活动报名。
- 数据可视化：BMI + 图表、天气图、GitHub 热力图、疫情/仪表盘、股票 K 线。

---

## 第十五章：课堂互动 Vibe Coding（新增）

- 推荐：TRAE（最佳演示）/bolt.new（在线、震撼）/ChatGPT Canvas（易上手）。
- 流程：开场 → 初始 Prompt → 轮流加需求（每人一句）→ 总结回顾。
- 选题：班级主页、在线简历、小游戏、仪表盘看板。

---

## 第十六章：让 AI 给自己写一封信（新增）

- 用于课堂收尾与反思，展示 AI 的“温度”。
- Prompt 模板：

```text
请以AI助手身份给本项目写一封信，回顾我们做了什么，对未来提出建议。
```

---

## 第十七章：无 Git 账号的教学方案（新增）

- 只讲本地 Git：init/add/commit/log/checkout → 能完整体验“快照 + 回退”。
- 远程操作由讲师演示；课后注册 GitHub 或使用 Gitee。
- 概念讲解策略：撤销类比、文件夹类比、TRAE Git 面板。

---

## 第十八章：团队 Vibe Coding 分工（新增）

- 角色：PM、前端、后端、测试/QA、项目经理。
- 工作流：需求定义 → 分工开发 → 联调整合 → 发布上线。
- Git 分支：`feature/*` 分工，完成后合并 main；先约定再动手，频繁同步。

---

## 附录 A：Prompt 速查手册

- 创建项目：

```text
帮我创建一个[项目类型]，单个HTML文件，[功能列表]，[设计风格]
```

- 让 AI 规划：

```text
我想做一个[项目]，请列出功能清单和开发步骤
```

- 修改外观/修复问题/重新实现等：聚焦现象 + 期望。

---

## 附录 B：Git 命令速查表

```bash
git init
git add .
git add <file>
git commit -m "..."
git status
git log --oneline

git remote add origin <URL>
git push origin main
git pull origin main

git checkout -- .
git reset HEAD <file>
git reset --hard HEAD~1
git branch
git checkout -b <branch>
git checkout <branch>
git merge <branch>

git config --global user.name "你的名字"
git config --global user.email "你的邮箱"
```

---

## 附录 C：常见问题 FAQ（选摘）

- AI 代码跑不动？用浏览器开发者工具查看 Console 报错，贴给 AI 定位。
- 结果与预期不符？用“我想要 XXX”的精确表述，参考 Prompt 模板。
- TRAE 打不开？检查系统要求，必要时重装。
- Git push 被拒？先 `git pull --rebase origin main` 再 push。
- LocalStorage 丢数据？与浏览器/域名绑定；生产应用用数据库。
- 做完怎么分享？用 GitHub Pages 或 Vercel 免费部署。
