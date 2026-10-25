---
marp: true
size: 16:9
paginate: true
theme: default
header: 'Vibe Coding 知识库（讲义版）'
footer: 'E-Vibe Coding • AI 编程微课堂'
---

# Vibe Coding 知识库（讲义版）

AI 编程微课堂·Slides

讲师：________________  日期：________________

---

# 目录（Agenda）

1. AI 编程与 Vibe Coding
2. TRAE 安装与使用
3. Prompt Engineering
4. Git 版本控制
5. 实战：智能记事本
6. 进阶与避坑
7. 部署上线
8. 学习路径
9. 前后端分离（新增）
10. App 上架与小程序发布（新增）
11. AI 编程工具对比（新增）
12. Token 与费用（新增）
13. 开发阶梯：HTML → App（新增）
14. 更多选题方向（新增）
15. 课堂互动 Vibe Coding（新增）
16. AI 写一封信（新增）
17. 无 Git 账号的教学（新增）
18. 团队分工（新增）

---

# 1. AI 编程与 Vibe Coding（1/2）

- 发展历程：Copilot（2021）→ ChatGPT（2022）→ GPT-4（2023）→ AI IDE（2024）
- Karpathy（2025）：Vibe Coding 命名
- 定义：用自然语言描述，AI 生成与修改代码
- 你的角色：导演（提出需求、审查、取舍）

---

# 1. AI 编程与 Vibe Coding（2/2）

- 对比传统：语法→需求表达；自写→AI 写；自查→AI 修
- 学习门槛：分钟级入门
- 一句话：你说戏，AI 干活

---

# 2. TRAE 安装与使用（1/2）

- 字节出品，完全免费，中文友好
- 基于 VS Code，有 Agent + Chat 两种模式
- 安装：trae.ai 下载 → 安装 → 登录 → 打开项目文件夹

---

# 2. TRAE 安装与使用（2/2）

- 界面：文件侧栏 / 编辑器 / AI 面板 / 终端 / Git 面板
- Agent vs Chat：
  - Agent：AI 自动创建/修改文件、运行命令
  - Chat：仅问答，不改文件

---

# 3. Prompt Engineering（1/2）

- 好 Prompt：具体、带约束、带示例
- 技巧：
  1. 说“要什么”，少说“怎么做”
  2. 提供上下文和目标用户
  3. 一次一件事，迭代推进

---

# 3. Prompt Engineering（2/2）

- 模板：
```
我想做一个 [项目类型]
功能： [X,Y,Z]
技术： [单文件/LocalStorage/...]
设计： [风格/参考]
用户： [谁]
```
- 迭代：改外观 / 加功能 / 修问题 / 让 AI 解释代码

---

# 4. Git 版本控制（1/2）

- 价值：无限次撤销 + 完整历史 + 多人协作
- 概念：仓库 / 暂存 / 提交 / 分支 / 推送
- 口诀：add → commit → push

---

# 4. Git 版本控制（2/2）

- 常用：`git init`、`git add .`、`git commit -m`、`git status`、`git log --oneline`
- 回退：`git checkout -- .`、`git reset --hard HEAD~1`
- 在 TRAE：Git 面板一键完成；也可让 AI 代操作

---

# 5. 实战：智能记事本（1/2）

- 目标：单文件 HTML/CSS/JS
- 功能：添加/删除/搜索/本地持久化（LocalStorage）
- UI：深色主题 + 动效

---

# 5. 实战：智能记事本（2/2）

- 迭代 5 步：基础 → 删除+持久化 → 搜索 → 美化 → 进阶
- 每一步：测试 + `git commit`

---

# 6. 进阶与避坑（1/2）

- 先规划：问题/功能/优先级/草图（5 分钟省 30 分钟）
- 小步快跑：每次一个改动 + 测试 + 提交

---

# 6. 进阶与避坑（2/2）

- 四大翻车：
  - 越改越乱 → 及时 commit
  - AI 自说自话 → 明确“只做 X”
  - 不看代码 → 至少扫一眼或让 AI 解释
  - 一次说太多 → 拆小步

---

# 7. 部署上线（1/2）

- 静态站部署：
  - GitHub Pages（最简单）
  - Vercel / Netlify（CI/CD 自动部署）

---

# 7. 部署上线（2/2）

- GitHub Pages：Settings → Pages → Branch: main → Save → 等 1-2 分钟
- Vercel：GitHub 登录 → Import → Deploy → 之后 push 自动生效

---

# 8. 学习路径（1/2）

- 短期练手（1-2 周）：猜数字、番茄钟、记账、打卡、天气、Markdown 编辑器
- 中期方向（1-3 月）：前端框架、Python+AI、简易后端

---

# 8. 学习路径（2/2）

- 资源：MDN / freeCodeCamp / B 站 / GitHub / 掘金

---

# 9. 前后端分离（1/2）

- 定义：前端（界面）与后端（数据/业务）分离，通过 API 通信
- 优势：并行开发；一套后端服务多终端；技术自由；体验更好；维护性强
- 劣势：复杂度↑；SEO 需 SSR；首屏加载慢；学习曲线高

---

# 9. 前后端分离（2/2）

- 案例：校园二手平台
  - 传统：服务器拼接 HTML，难复用到 App/小程序
  - 分离：后端提供 `/api/products`，Web/小程序/App 共享同一套 API

---

# 10. 上架与小程序（1/3）

- iOS：Apple 开发者（个人$99/年、企业$299/年）→ 证书/描述文件 → Xcode/TestFlight → 审核 1-3 天
- Android：Google Play（$25 一次性）+ 国内厂商商店需分别提交
- 鸿蒙：华为开发者联盟 + DevEco Studio（ArkTS）
- 微信小程序：注册 → 开发者工具 → 体验版 → 审核 1-7 天

---

# 10. 上架与小程序（2/3）

- 编译环境：
  - iOS：Xcode（仅 macOS）
  - Android：Android Studio（Win/Mac/Linux）
  - 鸿蒙：DevEco Studio（Win/Mac）
  - 小程序：微信开发者工具（云编译，门槛低）

---

# 10. 上架与小程序（3/3）

- 个人 vs 企业（小程序）：
  - 个人：类目受限，不支持电商/支付/直播/社交
  - 企业：认证后可开更多类目，支持微信支付

---

# 11. AI 工具对比（1/3）

- Claude Code：终端型 Agent，上下文大（~200K），强理解，昂贵/需翻墙
- Codex/ChatGPT：CLI/网页多形态，GPT-4o/o3 强，API 计费
- TRAE：本地免费中文 IDE，内置 Agent，教学友好

---

# 11. AI 工具对比（2/3）

| 对比 | TRAE | Claude Code | Codex CLI | Cursor |
| --- | --- | --- | --- | --- |
| 费用 | 免费 | 付费 | 付费 | 免费额度+付费 |
| 界面 | IDE | 终端 | 终端 | IDE |
| 国内 | 直连 | 需翻墙 | 需翻墙 | 需翻墙 |
| 上手 | 低 | 高 | 高 | 中 |

---

# 11. AI 工具对比（3/3）

- 共同限制：不是万能；会“幻觉”；上下文有限；结果存在波动
- 选择建议：
  - 学生/入门：TRAE
  - 进阶：Cursor
  - 专业：Claude Code / Codex

---

# 12. Token 与费用（1/3）

- Token：文本/代码的计量单位（输入+输出都计费）
- 上下文窗口：一次对话可容纳的最大 Token 数（超出会遗忘）

---

# 12. Token 与费用（2/3）

- 小项目费用（示例）：
  - 输入 ~10.5K / 输出 ~20K Token
  - GPT-4o ≈ $0.40；Claude Sonnet ≈ $0.11（参考价）

---

# 12. Token 与费用（3/3）

- 价格（2025 中）：
  - GPT-4o：$2.5 / $10 每百万（入/出）
  - GPT-4o-mini：$0.15 / $0.60
  - Sonnet 4：$3 / $15
  - Haiku：$0.25 / $1.25
  - DeepSeek V3：$0.27 / $1.10
- 建议：TRAE 免费 + ChatGPT/Claude 免费版问答

---

# 13. 开发阶梯：HTML → App（1/2）

- 为什么先做单机 HTML：零配置/立即见效/聚焦 AI 协作/调试简单

---

# 13. 开发阶梯：HTML → App（2/2）

- 五级：
  1) 单机 HTML
  2) 带 API 网页
  3) 微信小程序
  4) 前后端分离 Web 应用
  5) 跨平台 App（Flutter/React Native）

---

# 14. 更多选题方向（1/2）

- 生活工具：AA 记账、倒数日、随机点名、菜谱、排班表、财务看板
- 学习辅助：Markdown 笔记、番茄钟、单词卡、课程表、倒计时、错题本、GPA

---

# 14. 更多选题方向（2/2）

- 娱乐游戏：猜数字、RPS、成语接龙、2048、打字、贪吃蛇、五子棋、节拍
- 社交创意：表白墙、校园地图、心情日记、匿名投票、博客、活动报名
- 数据可视化：BMI+图表、天气趋势、GitHub 热力图、疫情看板、股票 K 线

---

# 15. 课堂互动 Vibe Coding（1/2）

- 工具：
  - TRAE（最佳教学）
  - bolt.new / v0（在线、震撼）
  - ChatGPT Canvas（易上手）

---

# 15. 课堂互动 Vibe Coding（2/2）

- 流程：开场 → 初始 Prompt → 轮流加需求（每人一句）→ 总结
- 适合项目：班级主页、在线简历、小游戏、仪表盘

---

# 16. AI 写一封信（新增）

- 用于课堂收尾/反思，营造“AI 的温度”
- Prompt：
```
以AI助手身份给本项目写一封信：回顾过程、评价成果、提出建议。
```

---

# 17. 无 Git 账号的教学（1/2）

- 只讲本地 Git：init / add / commit / log / checkout
- 远程由讲师演示；或课后注册 GitHub / 使用 Gitee

---

# 17. 无 Git 账号的教学（2/2）

- 概念讲解策略：
  - 撤销类比（改崩了 → 一键回到上个版本）
  - 文件夹类比（无限备份 vs 版本历史）
  - TRAE Git 面板（图形化直观）

---

# 18. 团队分工（1/2）

- 角色：PM / 前端 / 后端 / 测试 / 项目经理
- 关键变化：编码→表达与审查；每个人都是 AI 的“导演”

---

# 18. 团队分工（2/2）

- 工作流：需求定义 → 分工开发 → 联调 → 发布
- Git 分支：`feature/*` 各自开发，合并 main
- 原则：先约定再动手；频繁同步；接口先行；让 AI 处理重复劳动

---

# 附：更多细节

- 速查手册（Prompt / Git）、FAQ 等请见仓库：`knowledge-base.md`
- 本 Slides 使用 Marp Markdown，可一键导出 PPTX

---

# 谢谢！

Q&A
