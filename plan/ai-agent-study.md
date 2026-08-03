# AI Agent 学习计划

> 基于 [深入理解 AI Agent：设计原理与工程实践](https://github.com/bojieli/ai-agent-book)
> 核心公式：**Agent = LLM + 上下文 + 工具**
> 优先级：⭐⭐⭐ 第一优先级

## 学习资源

| 资源 | 链接 |
| --- | --- |
| GitHub 仓库 | https://github.com/bojieli/ai-agent-book |
| 在线阅读 | https://bojieli/ai-agent-book/ |
| PDF 下载 | [中文 PDF](https://github.com/bojieli/ai-agent-book/releases/download/latest/AI-Agents-in-Depth-zh-CN.pdf) |
| 配套实验 | 95 个实验，Python 3.10+ |

---

## 学习路径

### 阶段一：基础入门（1-2 周）🟢

| 章节 | 主题 | 核心内容 | 实验数 |
| :--: | --- | --- | :--: |
| 第 1 章 | Agent 基础知识 | Agent = LLM + 上下文 + 工具；Harness 工程 | 4 |
| 第 2 章 | 上下文工程 | KV Cache、提示工程、Agent Skills、上下文压缩 | 9 |

**学习目标：**
- 理解 Agent 的核心架构和三要素
- 掌握上下文工程的基本概念
- 能够运行基础实验

**实践任务：**
- [ ] 克隆仓库，配置环境（uv sync --locked --extra ch1 --extra ch2）
- [ ] 运行第 1 章全部 4 个实验
- [ ] 运行第 2 章核心实验，理解上下文对 Agent 能力的影响
- [ ] 写学习笔记：Agent 架构理解

---

### 阶段二：进阶提升（2-3 周）🔵

| 章节 | 主题 | 核心内容 | 实验数 |
| :--: | --- | --- | :--: |
| 第 3 章 | 用户记忆和知识库 | 跨会话记忆、RAG、结构化索引、知识图谱 | 13 |
| 第 4 章 | 工具 | MCP 协议、感知/执行/协作三类工具、异步 Agent | 7 |

**学习目标：**
- 掌握 Agent 记忆机制和 RAG 架构
- 理解 MCP 协议和工具设计原则
- 能够设计和实现简单的 Agent 工具

**实践任务：**
- [ ] 运行第 3 章实验，重点理解 RAG 和记忆系统
- [ ] 运行第 4 章实验，理解 MCP 工具协议
- [ ] 实践：为 Agent 添加自定义工具
- [ ] 写学习笔记：记忆系统与工具设计

---

### 阶段三：高级实战（3-4 周）🟣

| 章节 | 主题 | 核心内容 | 实验数 |
| :--: | --- | --- | :--: |
| 第 5 章 | Coding Agent 与代码生成 | 生产级 Coding Agent 全景 | 12 |
| 第 6 章 | Agent 的评估 | 评估环境、指标、统计显著性 | 12 |

**学习目标：**
- 理解 Coding Agent 的完整实现
- 掌握 Agent 评估方法和指标
- 能够构建和评估自己的 Agent 系统

**实践任务：**
- [ ] 深入研究第 5 章 Coding Agent 实现
- [ ] 运行第 6 章评估实验，理解评估框架
- [ ] 实践：设计一个 Agent 评估方案
- [ ] 写学习笔记：Coding Agent 架构与评估方法

---

### 阶段四：专家进阶（4-6 周）🔴

| 章节 | 主题 | 核心内容 | 实验数 |
| :--: | --- | --- | :--: |
| 第 7 章 | 模型后训练 | SFT、RL、工具调用内化 | 16 |
| 第 8 章 | Agent 的持续进化 | 从轨迹信号更新知识、指令、程序与参数 | 9 |

**学习目标：**
- 理解模型训练三阶段：预训练/SFT/RL
- 掌握 Agent 自我进化的方法
- 能够进行模型微调和 Agent 优化

**实践任务：**
- [ ] 学习第 7 章，理解 SFT 和 RL 的应用场景
- [ ] 运行部分训练实验（注意硬件要求）
- [ ] 学习第 8 章，理解 Agent 持续进化机制
- [ ] 写学习笔记：模型训练与 Agent 进化

---

### 阶段五：应用拓展（2-3 周）🟠

| 章节 | 主题 | 核心内容 | 实验数 |
| :--: | --- | --- | :--: |
| 第 9 章 | 多模态与实时交互 | 语音 Agent、Computer Use、机器人 | 10 |
| 第 10 章 | 多 Agent 协作 | 协作框架、上下文共享/隔离、Agent 社会 | 8 |

**学习目标：**
- 了解多模态 Agent 的应用场景
- 掌握多 Agent 协作的设计模式
- 能够构建多 Agent 协作系统

**实践任务：**
- [ ] 运行第 9 章实验，体验多模态交互
- [ ] 运行第 10 章多 Agent 协作实验
- [ ] 综合项目：设计并实现一个多 Agent 协作应用
- [ ] 写学习笔记：多 Agent 协作设计模式

---

## 环境配置

```bash
# 克隆仓库
git clone https://github.com/bojieli/ai-agent-book.git
cd ai-agent-book

# 安装 uv（推荐）
# 参考：https://docs.astral.sh/uv/getting-started/installation/

# 按章节安装依赖
uv sync --locked --extra ch1  # 第 1 章
uv sync --locked --extra ch2  # 第 2 章
# ... 以此类推到 ch10

# 或一次性安装所有章节（不含本地训练栈）
uv sync --locked --extra all

# 配置 API Key
cp .env.example .env
# 编辑 .env 填入至少一个提供商的 Key
```

**推荐 API 平台：**
- Kimi（月之暗面）：https://platform.moonshot.cn/
- 智谱 GLM：https://open.bigmodel.cn/
- Siliconflow：https://siliconflow.cn/
- DeepSeek：https://platform.deepseek.com/

---

## 学习进度追踪

| 章节 | 状态 | 开始日期 | 完成日期 | 笔记链接 |
| :--: | :--: | :--: | :--: | :--: |
| 第 1 章 | ⬜ 未开始 | - | - | - |
| 第 2 章 | ⬜ 未开始 | - | - | - |
| 第 3 章 | ⬜ 未开始 | - | - | - |
| 第 4 章 | ⬜ 未开始 | - | - | - |
| 第 5 章 | ⬜ 未开始 | - | - | - |
| 第 6 章 | ⬜ 未开始 | - | - | - |
| 第 7 章 | ⬜ 未开始 | - | - | - |
| 第 8 章 | ⬜ 未开始 | - | - | - |
| 第 9 章 | ⬜ 未开始 | - | - | - |
| 第 10 章 | ⬜ 未开始 | - | - | - |

> 状态标记：⬜ 未开始 | 🔄 进行中 | ✅ 已完成

---

## 与现有笔记的关联

| 现有笔记 | 关联章节 | 说明 |
| --- | :--: | --- |
| [AI 开发使用技巧](../notes/AI开发使用技巧.md) | 第 1-2 章 | 基础概念补充 |
| [openclaw 使用心得](../ai/openclaw.md) | 第 5 章 | Coding Agent 实践对比 |
| [agentTeam 实战](../ai/agentTeam实战.md) | 第 10 章 | 多 Agent 协作实践 |
| [clawAgentTeam 开发](../ai/clawAgentTeam开发.md) | 第 10 章 | 多 Agent 开发经验 |

---

## 学习原则

1. **动手优先**：每个实验都要亲手跑一遍，不要只看代码
2. **循序渐进**：按章节顺序学习，不要跳级
3. **记录总结**：每章学完写学习笔记，记录核心概念和踩坑经验
4. **联系实践**：结合工作中的 Agent 项目理解书中内容
5. **定期复盘**：每周回顾学习进度，调整计划
