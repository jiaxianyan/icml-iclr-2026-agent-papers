# 🤖 ICML 2026 Agent 相关论文

🌐 **语言：** [English](./README.md) | 中文

> 非官方整理：基于 ICML 2026 官方 virtual site，对标题中显式包含 agent / agentic / multi-agent / tool-use / computer-use / GUI/Web agent 等信号的 poster 进行主题归类和一句话导读。

- 📌 **数据来源：** [ICML 2026 Papers](https://icml.cc/virtual/2026/papers.html)
- 📄 **覆盖范围：** 465 篇 papers


## 🧭 目录

- [✨ 主要观察](#highlights)
- [🔎 范围与方法](#scope-and-method)
- [🗂️ 主题分类](#taxonomy)
- [📋 完整清单](#full-list)
  - [📚 评测、基准与诊断](#benchmarks-evaluation)
  - [🤝 多智能体、社会模拟与 MARL](#multi-agent-systems-marl)
  - [🛠️ 工具使用、训练与 RL](#tool-use-training-rl)
  - [🛡️ 安全、鲁棒性与治理](#safety-security-governance)
  - [🧠 基础理论、行为分析与可解释性](#theory-behavior-interpretability)
  - [🔬 科学、行业与垂直领域 agent](#scientific-domain-agents)
  - [💾 记忆、上下文与长程任务](#memory-context-long-horizon)
  - [💻 代码、软件工程与定理证明](#coding-swe-theorem-proving)
  - [🖥️ GUI、Web 与 computer-use agent](#gui-web-computer-use)
  - [🎥 多模态、具身与交互](#multimodal-embodied-interactive)
  - [🏗️ 规划、架构与编排](#planning-architecture-orchestration)
  - [💬 对话、澄清与助理交互](#conversation-assistant-interaction)
- [📦 数据文件](#data-files)
- [⚠️ 免责声明](#disclaimer)

<a id="highlights"></a>

## ✨ 主要观察

- Agent 研究正在从 prompt 工程走向系统工程：训练、环境、评测、安全、记忆和工作流一起成为核心问题。
- 评测/基准是最密集的方向，说明社区正在补齐 agent 的可测量性、可复现性和诊断工具。
- 多智能体、agentic RL、tool-use RL、trajectory-SFT、自演化和蒸馏构成了“可训练 agent”的主线。
- GUI/Web/computer-use、coding/SWE、科学发现和行业工作流是最明显的落地方向。
- 安全与可靠性已经成为独立主线，覆盖多轮攻击、工具投毒、隐私外泄、运行时监控、拒答边界和鲁棒性。

<a id="scope-and-method"></a>

## 🔎 范围与方法

如果一篇论文的标题中明确包含 agent 相关信号，则会被纳入本列表，包括但不限于：
agent、agentic、multi-agent、tool-use、tool-calling、computer-use、GUI agent、web agent，以及其他与交互式决策相关的术语。

本分类体系是为了便于导航而进行的人工/半自动整理，并不是 ICML 官方分类。部分论文可能同时适用于多个主题；为提高可读性，每篇论文只分配到一个主要类别。

本列表可能会遗漏一些标题中没有显式体现这些信号的 agent 相关工作；同时，也可能包含一些与现代 LLM-agent 研究相邻的经典多智能体强化学习或社会模拟论文。

<a id="taxonomy"></a>

## 🗂️ 主题分类

| 图标 | 主题 | 数量 | 关注点 |
|---|---|---:|---|
| 📚 | [评测、基准与诊断 / Benchmarks & Evaluation](#benchmarks-evaluation) | 99 | 构建可复现、可诊断的 agent 评测环境，覆盖长程任务、GUI/Web、代码、科学、金融、医疗等真实场景。 |
| 🤝 | [多智能体、社会模拟与 MARL / Multi-Agent Systems & MARL](#multi-agent-systems-marl) | 93 | 研究 LLM 多智能体辩论、协作、协议选择，以及 MARL 中的协调、通信、信用分配和社会模拟。 |
| 🛠️ | [工具使用、训练与 RL / Tool Use, Training & RL](#tool-use-training-rl) | 58 | 从 prompt-based agent 转向可训练 agent，关注 tool-use RL、agentic RL、GRPO、trajectory-SFT、自演化和蒸馏。 |
| 🛡️ | [安全、鲁棒性与治理 / Safety, Security & Governance](#safety-security-governance) | 51 | 围绕多轮攻击、工具投毒、环境扰动、隐私外泄、拒答边界、红队、运行时检测和安全护栏展开。 |
| 🧠 | [基础理论、行为分析与可解释性 / Theory, Behavior & Interpretability](#theory-behavior-interpretability) | 39 | 讨论 goal-directedness、agent empowerment、oversight、行为表征、校准、可解释性和可靠性科学。 |
| 🔬 | [科学、行业与垂直领域 agent / Scientific & Domain Agents](#scientific-domain-agents) | 30 | 将 agent 落到数据科学、金融、医疗、生物安全、CAD/电路/机器人、回溯合成、企业运维等任务。 |
| 💾 | [记忆、上下文与长程任务 / Memory, Context & Long-Horizon Tasks](#memory-context-long-horizon) | 29 | 处理长程 agent 的状态管理瓶颈，包括轨迹压缩、图记忆、上下文折叠、长期会话和跨 session 记忆。 |
| 💻 | [代码、软件工程与定理证明 / Coding, SWE & Theorem Proving](#coding-swe-theorem-proving) | 27 | 面向 repo 级软件任务、CUDA/Triton/kernel、全栈开发、漏洞发现、容器环境和自动定理证明。 |
| 🖥️ | [GUI、Web 与 computer-use agent / GUI, Web & Computer-Use](#gui-web-computer-use) | 13 | 围绕网页、桌面、移动 GUI 和 computer-use，研究环境生成、轨迹预训练、动作纠错、鲁棒性和安全。 |
| 🎥 | [多模态、具身与交互 / Multimodal, Embodied & Interactive Agents](#multimodal-embodied-interactive) | 11 | 将 agentic reasoning 接入 VLM/VLA、视频、音频、导航、空间推理、主动感知和具身操作。 |
| 🏗️ | [规划、架构与编排 / Planning, Architecture & Orchestration](#planning-architecture-orchestration) | 11 | 关注 agent 工作流、子 agent 创建、拓扑演化、协议选择、规划/执行解耦和系统编排。 |
| 💬 | [对话、澄清与助理交互 / Conversation & Assistant Interaction](#conversation-assistant-interaction) | 4 | 研究对话 agent 的澄清提问、服务成本/效用平衡、全双工语音和任务型交互策略。 |

<a id="full-list"></a>

## 📋 完整清单

格式：**论文标题** — 一句话导读。每个标题链接到 ICML 官方详情页。

<a id="benchmarks-evaluation"></a>
### 📚 1. 评测、基准与诊断 / Benchmarks & Evaluation (99)

构建可复现、可诊断的 agent 评测环境，覆盖长程任务、GUI/Web、代码、科学、金融、医疗等真实场景。

- **[$\tau$-Knowledge: Evaluating Conversational Agents over Unstructured Knowledge](https://icml.cc/virtual/2026/poster/63427)** — 构建 **$\tau$-Knowledge**，用于评测“Conversational Agents”在“Unstructured Knowledge”上的表现。
- **[$\tau$-Voice: Benchmarking Full-Duplex Voice Agents on Real-World Domains](https://icml.cc/virtual/2026/poster/66590)** — 构建 **$\tau$-Voice**，用于评测“Full-Duplex Voice Agents”在“Real-World Domains”上的表现。
- **[$\tau^2$-Bench: Evaluating Conversational Agents in a Dual-Control Environment](https://icml.cc/virtual/2026/poster/64377)** — 构建 **$\tau^2$-Bench**，用于评测“Conversational Agents”在“Dual-Control Environment”中的表现。
- **[A Behavioural and Representational Evaluation of Goal-Directedness in Language Model Agents](https://icml.cc/virtual/2026/poster/64314)** — 从行为和表征两个层面评测“Language Model Agents”的“Goal-Directedness”。
- **[A Diagnostic Study of Multi-Agent LLMs for Real-World Debates](https://icml.cc/virtual/2026/poster/66089)** — 诊断“Multi-Agent LLMs”在“Real-World Debates”中的表现。
- **[ABC-Bench: An Agentic Bio-Capabilities Benchmark for Biosecurity](https://icml.cc/virtual/2026/poster/60590)** — 构建 **ABC-Bench**，作为“Biosecurity”的评测基准。
- **[AgentExpt: Automating AI Experiment Design with LLM-based Resource Retrieval Agent](https://icml.cc/virtual/2026/poster/62358)** — 提出 **AgentExpt**，将“LLM-based Resource Retrieval Agent”引入自动化“AI Experiment Design”。
- **[AgentHijack: Benchmarking Computer Use Agent Robustness to Common Environment Corruptions](https://icml.cc/virtual/2026/poster/66792)** — 构建 **AgentHijack**，用于评测“Computer Use Agent Robustness to Common Environment Corruptions”。
- **[AgentLAB: Benchmarking LLM Agents against Long-Horizon Attacks](https://icml.cc/virtual/2026/poster/65640)** — 构建 **AgentLAB**，用于评测“LLM Agents”面对“Long-Horizon Attacks”的表现。
- **[AgentNoiseBench: Benchmarking Robustness of Tool-Using LLM Agents Under Noisy Condition](https://icml.cc/virtual/2026/poster/64355)** — 构建 **AgentNoiseBench**，用于评测“Robustness of Tool-Using LLM Agents”在“Noisy Condition”下的表现。
- **[AgentSelect: Benchmark for Narrative Query-to-Agent Recommendation](https://icml.cc/virtual/2026/poster/66362)** — 构建 **AgentSelect**，作为“Narrative Query-to-Agent Recommendation”的评测基准。
- **[AgentWebBench: Benchmarking Multi-Agent Coordination in Agentic Web](https://icml.cc/virtual/2026/poster/63068)** — 构建 **AgentWebBench**，用于评测“Multi-Agent Coordination”在“Agentic Web”中的表现。
- **[AMA-Bench: Evaluating Long-Horizon Memory for Agentic Applications](https://icml.cc/virtual/2026/poster/65112)** — 构建 **AMA-Bench**，用于评测“Long-Horizon Memory”面向“Agentic Applications”的表现。
- **[An Empirical Study of Memory Poisoning Defenses for LLM Agents](https://icml.cc/virtual/2026/poster/61006)** — 实证研究“LLM Agents”中的“Memory Poisoning Defenses”。
- **[ANCHOR: Automated Alignment Auditing for CLI Agents on Real-World Harm](https://icml.cc/virtual/2026/poster/63234)** — 提出/整理 **ANCHOR**，考察“Automated Alignment Auditing for CLI Agents”在“Real-World Harm”上的表现。
- **[AOEB: Benchmarking Agent-Oriented Multimodal Embeddings](https://icml.cc/virtual/2026/poster/61847)** — 构建 **AOEB**，用于评测“Agent-Oriented Multimodal Embeddings”。
- **[AppWorld-UL: Benchmarking Diverse Agent-User Interactions for Tool-Use](https://icml.cc/virtual/2026/poster/62856)** — 构建 **AppWorld-UL**，用于评测“Diverse Agent-User Interactions”面向“Tool-Use”的表现。
- **[ArenaRL: Scaling RL for Open-Ended Agents via Tournament-based Relative Ranking](https://icml.cc/virtual/2026/poster/66670)** — 提出 **ArenaRL**，用“Tournament-based Relative Ranking”来扩展“RL for Open-Ended Agents”。
- **[ARLArena: Demystifying Policy Gradient Stability in Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/65909)** — 提出/整理 **ARLArena**，考察“Demystifying Policy Gradient Stability”在“Agentic Reinforcement Learning”中的表现。
- **[AtelierEval: Agentic Evaluation of Humans & LLMs as Text-to-Image Prompters](https://icml.cc/virtual/2026/poster/64186)** — 提出/整理 **AtelierEval**，关注“Agentic Evaluation of Humans & LLMs as Text-to-Image Prompters”。
- **[Benchmarking Agent Memory in Interdependent Multi-Session Agentic Tasks](https://icml.cc/virtual/2026/poster/64842)** — 评测“Agent Memory”在“Interdependent Multi-Session Agentic Tasks”中的表现。
- **[Beyond the Final Answer: Evaluating the Reasoning Trajectories of Tool-Augmented Agents](https://icml.cc/virtual/2026/poster/64255)** — 构建 **Beyond the Final Answer**，用于评测“Reasoning Trajectories of Tool-Augmented Agents”。
- **[BioAgent Bench: An AI Agent Evaluation Suite for Bioinformatics](https://icml.cc/virtual/2026/poster/66549)** — 提出/整理 **BioAgent Bench**，面向“Bioinformatics”研究“AI Agent Evaluation Suite”。
- **[CaP-X: A Framework for Benchmarking and Improving Coding Agents for Robot Manipulation](https://icml.cc/virtual/2026/poster/66369)** — 提出 **CaP-X**，作为“Benchmarking and Improving Coding Agents for Robot Manipulation”的框架。
- **[CATArena: Evaluating Evolutionary Capabilities of Code Agents via Iterative Tournaments](https://icml.cc/virtual/2026/poster/65908)** — 构建 **CATArena**，用于评测“Evolutionary Capabilities of Code Agents via Iterative Tournaments”。
- **[CausalGame: Benchmarking Causal Thinking of LLM Agents in Games](https://icml.cc/virtual/2026/poster/63530)** — 构建 **CausalGame**，用于评测“Causal Thinking of LLM Agents”在“Games”中的表现。
- **[CentaurEval: Benchmarking Human-in-the-Loop Value in Agentic Coding](https://icml.cc/virtual/2026/poster/65136)** — 构建 **CentaurEval**，用于评测“Human-in-the-Loop Value”在“Agentic Coding”中的表现。
- **[CLAM-Bench: Benchmarking LLM Agents for Library-Scale Cross-Architecture Migration](https://icml.cc/virtual/2026/poster/60997)** — 构建 **CLAM-Bench**，用于评测“LLM Agents”面向“Library-Scale Cross-Architecture Migration”的表现。
- **[CoDA-Bench: Can Code Agents Handle Data-Intensive Tasks?](https://icml.cc/virtual/2026/poster/63815)** — 提出/整理 **CoDA-Bench**，关注“Can Code Agents Handle Data-Intensive Tasks?”。
- **[ComplexMCP: Evaluation of LLM Agents in Dynamic, Interdependent, and Large-Scale Tool Sandbox](https://icml.cc/virtual/2026/poster/66421)** — 提出/整理 **ComplexMCP**，考察“Evaluation of LLM Agents”在“Dynamic, Interdependent, and Large-Scale Tool Sandbox”中的表现。
- **[CoopEval: Benchmarking Cooperation-Sustaining Mechanisms and LLM Agents in Social Dilemmas](https://icml.cc/virtual/2026/poster/66503)** — 构建 **CoopEval**，用于评测“Cooperation-Sustaining Mechanisms and LLM Agents”在“Social Dilemmas”中的表现。
- **[Copyright-Bench: Agentic Evaluation of Copyright Law Compliance](https://icml.cc/virtual/2026/poster/66009)** — 提出/整理 **Copyright-Bench**，关注“Agentic Evaluation of Copyright Law Compliance”。
- **[CUARewardBench: Benchmark for Evaluating Reward Models on Computer-using Agent Trajectories](https://icml.cc/virtual/2026/poster/63367)** — 构建 **CUARewardBench**，作为“Evaluating Reward Models on Computer-using Agent Trajectories”的评测基准。
- **[CyberCycle: Scalable Real-World Benchmark for AI Agents' End-to-End Cybersecurity Capabilities](https://icml.cc/virtual/2026/poster/62134)** — 提出/整理 **CyberCycle**，面向“AI Agents' End-to-End Cybersecurity Capabilities”研究“Scalable Real-World Benchmark”。
- **[DeepImageSearch: Benchmarking Multimodal Agents for Context-Aware Image Retrieval in Visual Histories](https://icml.cc/virtual/2026/poster/61711)** — 构建 **DeepImageSearch**，用于评测“Multimodal Agents for Context-Aware Image Retrieval”在“Visual Histories”中的表现。
- **[DEER: A Benchmark for Evaluating Deep Research Agents on Expert Report Generation](https://icml.cc/virtual/2026/poster/64961)** — 构建 **DEER**，作为“Evaluating Deep Research Agents on Expert Report Generation”的评测基准。
- **[DevEvol: Benchmarking LLM Agents on Continuous Software Evolution](https://icml.cc/virtual/2026/poster/65024)** — 构建 **DevEvol**，用于评测“LLM Agents”在“Continuous Software Evolution”上的表现。
- **[DocOS: A Benchmark for Proactive Document-Guided Actions in GUI Agents](https://icml.cc/virtual/2026/poster/65725)** — 构建 **DocOS**，作为“Proactive Document-Guided Actions in GUI Agents”的评测基准。
- **[Does Reinforcement Fine-Tuning Improve Generalization of LLM Agents? An Empirical Study](https://icml.cc/virtual/2026/poster/65794)** — 以“Does Reinforcement Fine-Tuning Improve Generalization of LLM Agents? An Empirical Study”为问题，考察 agent 的能力边界或失败模式。
- **[DRIFT-BENCH: Diagnosing CoopeRative Breakdowns in LLM Agents under Input Faults via Multi-Turn Interaction](https://icml.cc/virtual/2026/poster/60842)** — 构建 **DRIFT-BENCH**，用于诊断“CoopeRative Breakdowns in LLM Agents”在“Input Faults via Multi-Turn Interaction”下的表现。
- **[DSGym: A Standardized and Holistic Framework for Advancing Data Science Agents](https://icml.cc/virtual/2026/poster/66567)** — 提出/整理 **DSGym**，面向“Advancing Data Science Agents”研究“Standardized and Holistic Framework”。
- **[DV-World: Benchmarking Data Visualization Agents in Real-World Scenarios](https://icml.cc/virtual/2026/poster/61444)** — 构建 **DV-World**，用于评测“Data Visualization Agents”在“Real-World Scenarios”中的表现。
- **[DynaSchedBench: Calibrated Dynamic Scheduling Benchmarks and Observability Paradox in LLM-based Scheduling Agents](https://icml.cc/virtual/2026/poster/60484)** — 提出/整理 **DynaSchedBench**，考察“Calibrated Dynamic Scheduling Benchmarks and Observability Paradox”在“LLM-based Scheduling Agents”中的表现。
- **[EnterpriseOps-Gym: Environments and Evaluations for Stateful Agentic Planning and Tool Use in Enterprise Settings](https://icml.cc/virtual/2026/poster/64162)** — 提出/整理 **EnterpriseOps-Gym**，考察“Environments and Evaluations for Stateful Agentic Planning and Tool Use”在“Enterprise Settings”中的表现。
- **[Evaluating Agentic Optimization on Large Codebases](https://icml.cc/virtual/2026/poster/63544)** — 评测“Agentic Optimization”在“Large Codebases”上的表现。
- **[EVMbench: Evaluating AI Agents on Smart Contract Security](https://icml.cc/virtual/2026/poster/64768)** — 构建 **EVMbench**，用于评测“AI Agents”在“Smart Contract Security”上的表现。
- **[EVOLVING ROLLOUTS: Harnessing Historical Experience for Web Agent Evolution in Reinforcement Learning](https://icml.cc/virtual/2026/poster/61544)** — 提出/整理 **EVOLVING ROLLOUTS**，考察“Harnessing Historical Experience for Web Agent Evolution”在“Reinforcement Learning”中的表现。
- **[ExCyTIn-Bench: Evaluating LLM agents on Cyber Threat Investigation](https://icml.cc/virtual/2026/poster/66310)** — 构建 **ExCyTIn-Bench**，用于评测“LLM agents”在“Cyber Threat Investigation”上的表现。
- **[FIRE-Bench: Evaluating Agents on the Rediscovery of Scientific Insights](https://icml.cc/virtual/2026/poster/61975)** — 构建 **FIRE-Bench**，用于评测“Agents”在“Rediscovery of Scientific Insights”上的表现。
- **[Fix Before Search: Benchmarking Agentic Visual Query Pre-processing in Multimodal Retrieval-augmented Generation](https://icml.cc/virtual/2026/poster/62898)** — 构建 **Fix Before Search**，用于评测“Agentic Visual Query Pre-processing”在“Multimodal Retrieval-augmented Generation”中的表现。
- **[GameDevBench: Evaluating Agentic Capabilities Through Game Development](https://icml.cc/virtual/2026/poster/64919)** — 构建 **GameDevBench**，用于评测“Agentic Capabilities Through Game Development”。
- **[Harnessing Uncertainty: Entropy-Modulated Policy Gradients for Long-Horizon LLM Agents](https://icml.cc/virtual/2026/poster/63273)** — 提出/整理 **Harnessing Uncertainty**，面向“Long-Horizon LLM Agents”研究“Entropy-Modulated Policy Gradients”。
- **[How Far Can LLM Agents Reason with Tables? Benchmarking Multi-Turn Agentic Table Question Answering in the Wild](https://icml.cc/virtual/2026/poster/66187)** — 以“How Far Can LLM Agents Reason with Tables? Benchmarking Multi-Turn Agentic Table Question Answering in the Wild”为问题，考察 agent 的能力边界或失败模式。
- **[HVR-Met: A Hypothesis-Verification-Replaning Agentic System for Extreme Weather Diagnosis](https://icml.cc/virtual/2026/poster/61110)** — 提出/整理 **HVR-Met**，面向“Extreme Weather Diagnosis”研究“Hypothesis-Verification-Replanning Agentic System”。
- **[Hybrid-Gym: Training Coding Agents to Generalize Across Tasks](https://icml.cc/virtual/2026/poster/66577)** — 提出/整理 **Hybrid-Gym**，关注“Training Coding Agents to Generalize Across Tasks”。
- **[Implicit Intelligence - Evaluating Agents on What Users Don’t Say](https://icml.cc/virtual/2026/poster/64912)** — 整理/评测“Implicit Intelligence - Evaluating Agents”，场景是在“What Users Don’t Say”上。
- **[ImpText: A Benchmark and Tool-Augmented Framework for Implicit Text Reasoning](https://icml.cc/virtual/2026/poster/63174)** — 提出/整理 **ImpText**，面向“Implicit Text Reasoning”研究“Benchmark and Tool-Augmented Framework”。
- **[InteractComp: Evaluating Search Agents With Ambiguous Queries](https://icml.cc/virtual/2026/poster/65730)** — 构建 **InteractComp**，用于评测“Search Agents”结合“Ambiguous Queries”的表现。
- **[Is Vibe Coding Safe? Benchmarking Vulnerability of Agent-Generated Code in Real-World Tasks](https://icml.cc/virtual/2026/poster/61427)** — 以“Is Vibe Coding Safe? Benchmarking Vulnerability of Agent-Generated Code in Real-World Tasks”为问题，考察 agent 的能力边界或失败模式。
- **[It's a TRAP! Task-Redirecting Agent Persuasion Benchmark for Web Agents](https://icml.cc/virtual/2026/poster/63888)** — 整理/评测“It's a TRAP! Task-Redirecting Agent Persuasion Benchmark”，场景是面向“Web Agents”。
- **[KernelCraft: Benchmarking for Agentic Close-to-Metal Kernel Generation on Emerging Hardware](https://icml.cc/virtual/2026/poster/65579)** — 构建 **KernelCraft**，用于评测“for Agentic Close-to-Metal Kernel Generation”在“Emerging Hardware”上的表现。
- **[LitReview Arena: Evaluating Literature Review Agents with Battle-style Peer Review Platform](https://icml.cc/virtual/2026/poster/63625)** — 构建 **LitReview Arena**，用于评测“Literature Review Agents”结合“Battle-style Peer Review Platform”的表现。
- **[LOCA-bench: Benchmarking Language Agents Under Controllable and Extreme Context Growth](https://icml.cc/virtual/2026/poster/64486)** — 构建 **LOCA-bench**，用于评测“Language Agents”在“Controllable and Extreme Context Growth”下的表现。
- **[MAS-Orchestra: Understanding and Improving Multi-Agent Reasoning Through Holistic Orchestration and Controlled Benchmarks](https://icml.cc/virtual/2026/poster/66445)** — 提出 **MAS-Orchestra**，用“Holistic Orchestration and Controlled Benchmarks”来“Understanding and Improving Multi-Agent Reasoning”。
- **[MCP-Persona: Benchmarking LLM Agents on Personalized MCP Tools and Tasks](https://icml.cc/virtual/2026/poster/60873)** — 构建 **MCP-Persona**，用于评测“LLM Agents”在“Personalized MCP Tools and Tasks”上的表现。
- **[MEAL: A Benchmark for Continual Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/64499)** — 构建 **MEAL**，作为“Continual Multi-Agent Reinforcement Learning”的评测基准。
- **[Memoria-Bench: A Comprehensive Benchmark for Evaluating Memory in Long-Horizon Autonomous Agents](https://icml.cc/virtual/2026/poster/64414)** — 构建 **Memoria-Bench**，作为“Evaluating Memory in Long-Horizon Autonomous Agents”的评测基准。
- **[Monitoring LLM-based Multi-Agent Systems Against Corruptions via Node Evaluation](https://icml.cc/virtual/2026/poster/63780)** — 整理/评测“Monitoring LLM-based Multi-Agent Systems Against Corruptions”，核心机制是“Node Evaluation”。
- **[NL2Repo-Bench: Towards Long-Horizon Repository Generation Evaluation of Coding Agents](https://icml.cc/virtual/2026/poster/60772)** — 提出/整理 **NL2Repo-Bench**，关注“Towards Long-Horizon Repository Generation Evaluation of Coding Agents”。
- **[Off-Policy Evaluation with Strategic Agents via Local Disclosure](https://icml.cc/virtual/2026/poster/64971)** — 整理/评测“Off-Policy Evaluation with Strategic Agents”，核心机制是“Local Disclosure”。
- **[Optimizing Agentic Reasoning with Retrieval via Synthetic Semantic Information Gain Reward](https://icml.cc/virtual/2026/poster/61838)** — 整理/评测“Optimizing Agentic Reasoning with Retrieval”，核心机制是“Synthetic Semantic Information Gain Reward”。
- **[Persona2Web: Benchmarking Personalized Web Agents for Contextual Reasoning with User History](https://icml.cc/virtual/2026/poster/61367)** — 构建 **Persona2Web**，用于评测“Personalized Web Agents”面向“Contextual Reasoning with User History”的表现。
- **[Position: Agent Evaluation Should Be Agentified for Openness, Standardization, and Reproducibility](https://icml.cc/virtual/2026/poster/67210)** — 提出/整理 **Position**，面向“Openness, Standardization, and Reproducibility”研究“Agent Evaluation Should Be Agentified”。
- **[PostTrainBench: Can LLM Agents Automate LLM Post-Training?](https://icml.cc/virtual/2026/poster/63667)** — 提出/整理 **PostTrainBench**，关注“Can LLM Agents Automate LLM Post-Training?”。
- **[PPT-Eval: A Benchmark for Computer-Use Agents on PowerPoint Tasks](https://icml.cc/virtual/2026/poster/65101)** — 构建 **PPT-Eval**，作为“Computer-Use Agents on PowerPoint Tasks”的评测基准。
- **[Protein Design with Agent Rosetta: A Case Study for Specialized Scientific Agents](https://icml.cc/virtual/2026/poster/64569)** — 提出/整理 **Protein Design with Agent Rosetta**，面向“Specialized Scientific Agents”研究“Case Study”。
- **[PSBench: Editing Image via GUI Agents in Photoshop](https://icml.cc/virtual/2026/poster/64381)** — 提出 **PSBench**，用“GUI Agents in Photoshop”来“Editing Image”。
- **[Recovering Policy-Induced Errors: Benchmarking and Trajectory Synthesis for Robust GUI Agents](https://icml.cc/virtual/2026/poster/62251)** — 构建 **Recovering Policy-Induced Errors**，用于评测“and Trajectory Synthesis”面向“Robust GUI Agents”的表现。
- **[Reward Hacking Benchmark: Measuring Exploits in LLM Agents with Tool Use](https://icml.cc/virtual/2026/poster/63289)** — 提出 **Reward Hacking Benchmark**，将“Tool Use”引入“Measuring Exploits in LLM Agents”。
- **[Rule2DRC: Benchmarking LLM Agents for DRC Script Synthesis with Execution-Guided Test Generation](https://icml.cc/virtual/2026/poster/63031)** — 构建 **Rule2DRC**，用于评测“LLM Agents”面向“DRC Script Synthesis with Execution-Guided Test Generation”的表现。
- **[SAGE-NAS: Synergizing LLM-Based Semantic Agent with Graph-Based Evaluator for Neural Architecture Search](https://icml.cc/virtual/2026/poster/62021)** — 提出 **SAGE-NAS**，将“Graph-Based Evaluator for Neural Architecture Search”引入“Synergizing LLM-Based Semantic Agent”。
- **[Salus: Strategic Diagnostic Testing for Complex Diagnosis via Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/64732)** — 提出 **Salus**，用“Multi-Agent Reinforcement Learning”来“Strategic Diagnostic Testing for Complex Diagnosis”。
- **[Scaling, Benchmarking, and Reasoning of Vision-Language Agents for Mobile GUI Navigation](https://icml.cc/virtual/2026/poster/63113)** — 整理/评测“Scaling, Benchmarking, and Reasoning of Vision-Language Agents”，场景是面向“Mobile GUI Navigation”。
- **[SciAgentGym: Benchmarking Multi-Step Scientific Tool-Use in LLM Agents](https://icml.cc/virtual/2026/poster/66785)** — 构建 **SciAgentGym**，用于评测“Multi-Step Scientific Tool-Use”在“LLM Agents”中的表现。
- **[SciNet: Evaluating AI Agents in Relation-Aware Scientific Literature Retrieval](https://icml.cc/virtual/2026/poster/66769)** — 构建 **SciNet**，用于评测“AI Agents”在“Relation-Aware Scientific Literature Retrieval”中的表现。
- **[SWE-Bench Pro: Can AI Agents Solve Long-Horizon Software Engineering Tasks?](https://icml.cc/virtual/2026/poster/61047)** — 提出/整理 **SWE-Bench Pro**，关注“Can AI Agents Solve Long-Horizon Software Engineering Tasks?”。
- **[SWE-Compass: Towards Unified Evaluation of Agentic Coding Abilities for Large Language Models](https://icml.cc/virtual/2026/poster/64552)** — 提出/整理 **SWE-Compass**，面向“Large Language Models”研究迈向“Unified Evaluation of Agentic Coding Abilities”。
- **[Taming I2V models for Image HOI Editing: A Cognitive Benchmark and Agentic Self-Correcting Framework](https://icml.cc/virtual/2026/poster/63999)** — 提出/整理 **Taming I2V models for Image HOI Editing**，关注“Cognitive Benchmark and Agentic Self-Correcting Framework”。
- **[The Crowded Embedding Space: A Mean-Field Mechanism for Emergent Marginalization in Retrieval-Augmented Agents](https://icml.cc/virtual/2026/poster/64854)** — 提出/整理 **The Crowded Embedding Space**，考察“Mean-Field Mechanism for Emergent Marginalization”在“Retrieval-Augmented Agents”中的表现。
- **[The Decrypto Benchmark for Multi-Agent Reasoning and Theory of Mind](https://icml.cc/virtual/2026/poster/62135)** — 整理/评测“Decrypto Benchmark”，场景是面向“Multi-Agent Reasoning and Theory of Mind”。
- **[Toward More Reliable Agent Evaluation: A Component-Based Benchmark Auditing Pipeline](https://icml.cc/virtual/2026/poster/66603)** — 提出/整理 **Toward More Reliable Agent Evaluation**，关注“Component-Based Benchmark Auditing Pipeline”。
- **[Towards Professional-Grade Financial Agents: Benchmarking, Tooling, and Structured Reasoning](https://icml.cc/virtual/2026/poster/60732)** — 提出/整理 **Towards Professional-Grade Financial Agents**，关注“Benchmarking, Tooling, and Structured Reasoning”。
- **[TRIP-Bench: A Benchmark for Long-Horizon Interactive Agents in Real-World Scenarios](https://icml.cc/virtual/2026/poster/62985)** — 构建 **TRIP-Bench**，作为“Long-Horizon Interactive Agents in Real-World Scenarios”的评测基准。
- **[TritonGym: A Benchmark for Agentic LLM Workflows in Triton GPU Code Generation](https://icml.cc/virtual/2026/poster/65003)** — 构建 **TritonGym**，作为“Agentic LLM Workflows in Triton GPU Code Generation”的评测基准。
- **[UltraHorizon: Benchmarking LLM-Agent Capabilities in Ultra Long-Horizon Scenarios](https://icml.cc/virtual/2026/poster/61412)** — 构建 **UltraHorizon**，用于评测“LLM-Agent Capabilities”在“Ultra Long-Horizon Scenarios”中的表现。
- **[Unsafer in Many Turns: Benchmarking and Defending Multi-Turn Safety Risks in Tool-Using Agents](https://icml.cc/virtual/2026/poster/62233)** — 构建 **Unsafer in Many Turns**，用于评测“and Defending Multi-Turn Safety Risks”在“Tool-Using Agents”中的表现。
- **[VenusBench-Mobile: A Challenging and User-Centric Benchmark for Mobile GUI Agents with Capability Diagnostics](https://icml.cc/virtual/2026/poster/62831)** — 构建 **VenusBench-Mobile**，作为“Mobile GUI Agents with Capability Diagnostics”的评测基准。
- **[VeRO: An Evaluation Harness for Agents to Optimize Agents](https://icml.cc/virtual/2026/poster/60518)** — 提出/整理 **VeRO**，面向“Agents to Optimize Agents”研究“Evaluation Harness”。
- **[VisionWebDev: A Hierarchical Benchmark for Visual Website Development with Agent Verification](https://icml.cc/virtual/2026/poster/61957)** — 构建 **VisionWebDev**，作为“Visual Website Development with Agent Verification”的评测基准。

<a id="multi-agent-systems-marl"></a>
### 🤝 2. 多智能体、社会模拟与 MARL / Multi-Agent Systems & MARL (93)

研究 LLM 多智能体辩论、协作、协议选择，以及 MARL 中的协调、通信、信用分配和社会模拟。

- **[$\texttt{Multi}^2$: Hierarchical Multi-Agent Decision-Making with LLM-Based Agents in Interactive Environments](https://icml.cc/virtual/2026/poster/65074)** — 提出 **$\texttt{Multi}^2$**，将“LLM-Based Agents in Interactive Environments”引入“Hierarchical Multi-Agent Decision-Making”。
- **[A Two-Tier Perspective on Inference-Time Parallelism in Multi-Agent LLM Systems](https://icml.cc/virtual/2026/poster/66552)** — 研究“Two-Tier Perspective on Inference-Time Parallelism”，场景是在“Multi-Agent LLM Systems”中。
- **[Agent Primitives: Reuseable Latent Building Blocks for Multi-Agent Systems](https://icml.cc/virtual/2026/poster/65501)** — 提出/整理 **Agent Primitives**，面向“Multi-Agent Systems”研究“Reuseable Latent Building Blocks”。
- **[AgentSteerTTS: A Multi-Agent Closed-Loop Framework for Composite-Instruction Text-to-Speech](https://icml.cc/virtual/2026/poster/62320)** — 提出/整理 **AgentSteerTTS**，面向“Composite-Instruction Text-to-Speech”研究“Multi-Agent Closed-Loop Framework”。
- **[AgentTailor: A Semantic-Aware LLM-Based Multi-Agent System with Actor-Critic Structure](https://icml.cc/virtual/2026/poster/60754)** — 提出 **AgentTailor**，将“Actor-Critic Structure”引入“Semantic-Aware LLM-Based Multi-Agent System”。
- **[ALSO: Adversarial Online Strategy Optimization for Social Agents](https://icml.cc/virtual/2026/poster/64379)** — 提出/整理 **ALSO**，面向“Social Agents”研究“Adversarial Online Strategy Optimization”。
- **[Automata-Conditioned Cooperative Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/63254)** — 研究“Automata-Conditioned Cooperative Multi-Agent Reinforcement Learning”。
- **[AutoMS: Multi-Agent Evolutionary Search for Cross-Physics Inverse Microstructure Design](https://icml.cc/virtual/2026/poster/60501)** — 提出/整理 **AutoMS**，面向“Cross-Physics Inverse Microstructure Design”研究“Multi-Agent Evolutionary Search”。
- **[Betting on Equilibrium: Monitoring Strategic Behavior in Multi-Agent Systems](https://icml.cc/virtual/2026/poster/62338)** — 提出/整理 **Betting on Equilibrium**，考察“Monitoring Strategic Behavior”在“Multi-Agent Systems”中的表现。
- **[Beyond Correctness: Distance-Based Social Dynamics of Multi-Agent Debate](https://icml.cc/virtual/2026/poster/61651)** — 提出/整理 **Beyond Correctness**，关注“Distance-Based Social Dynamics of Multi-Agent Debate”。
- **[CoPE: A Framework for Optimizing Coordination between Planning and Execution in LLM-based Agents](https://icml.cc/virtual/2026/poster/65839)** — 提出 **CoPE**，作为“Optimizing Coordination between Planning and Execution in LLM-based Agents”的框架。
- **[CORRECT: COndensed eRror RECognition via knowledge Transfer in multi-agent systems](https://icml.cc/virtual/2026/poster/63163)** — 提出 **CORRECT**，用“knowledge Transfer in multi-agent systems”来“COndensed eRror RECognition”。
- **[CyberJurors: A Multi-Agent Simulation Task for E-Commerce Disputes Verdict](https://icml.cc/virtual/2026/poster/61907)** — 提出/整理 **CyberJurors**，面向“E-Commerce Disputes Verdict”研究“Multi-Agent Simulation Task”。
- **[Decentralized and Disentangled Task–Role Representation Learning for Generalizable Offline Multi-Agent Meta Reinforcement Learning](https://icml.cc/virtual/2026/poster/61278)** — 研究“Decentralized and Disentangled Task–Role Representation Learning”，场景是面向“Generalizable Offline Multi-Agent Meta Reinforcement Learning”。
- **[DECOR: Learning to Decompose and Collaborate in Deep Search via Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/62745)** — 提出 **DECOR**，用“Multi-Agent Reinforcement Learning”来学习“to Decompose and Collaborate in Deep Search”。
- **[Detecting Perspective Shifts in Multi-Agent Systems](https://icml.cc/virtual/2026/poster/61263)** — 研究“Detecting Perspective Shifts”，场景是在“Multi-Agent Systems”中。
- **[Diffusing to Coordinate: Efficient Online Multi-Agent Diffusion Policies](https://icml.cc/virtual/2026/poster/61146)** — 提出/整理 **Diffusing to Coordinate**，关注“Efficient Online Multi-Agent Diffusion Policies”。
- **[Distilling Task-Level Coordination Policies for Generalizable Multi-Agent Cooperation](https://icml.cc/virtual/2026/poster/66438)** — 研究“Distilling Task-Level Coordination Policies”，场景是面向“Generalizable Multi-Agent Cooperation”。
- **[DLM: Unified Decision Language Models for Offline Multi-Agent Sequential Decision Making](https://icml.cc/virtual/2026/poster/61365)** — 提出/整理 **DLM**，面向“Offline Multi-Agent Sequential Decision Making”研究“Unified Decision Language Models”。
- **[Dual Latent Memory for Visual Multi-agent System](https://icml.cc/virtual/2026/poster/63256)** — 研究“Dual Latent Memory”，场景是面向“Visual Multi-agent System”。
- **[E-mem: Multi-Agent Based Episodic Context Reconstruction for LLM Agent Memory](https://icml.cc/virtual/2026/poster/65274)** — 提出/整理 **E-mem**，面向“LLM Agent Memory”研究“Multi-Agent Based Episodic Context Reconstruction”。
- **[EduMirror: Modeling Educational Social Dynamics with Value-driven Multi-agent Simulation](https://icml.cc/virtual/2026/poster/65878)** — 提出 **EduMirror**，将“Value-driven Multi-agent Simulation”引入“Modeling Educational Social Dynamics”。
- **[Efficient Multi-Agent Reasoning via Confidence-Guided Adaptive Debate](https://icml.cc/virtual/2026/poster/60593)** — 研究“Efficient Multi-Agent Reasoning”，核心机制是“Confidence-Guided Adaptive Debate”。
- **[Emergence of Biased Consensus in Multi-Agent LLM Debates](https://icml.cc/virtual/2026/poster/66269)** — 研究“Emergence of Biased Consensus”，场景是在“Multi-Agent LLM Debates”中。
- **[Epistemic Gain, Aleatoric Cost: Uncertainty Decomposition in Multi-Agent Debate for Math Reasoning](https://icml.cc/virtual/2026/poster/65653)** — 提出/整理 **Epistemic Gain, Aleatoric Cost**，考察“Uncertainty Decomposition”在“Multi-Agent Debate for Math Reasoning”中的表现。
- **[EvoCF: Multi-Agent Collaboration via Agentic Memory-Driven Evolutionary Counterfactual Planning](https://icml.cc/virtual/2026/poster/65198)** — 提出 **EvoCF**，用“Agentic Memory-Driven Evolutionary Counterfactual Planning”来“Multi-Agent Collaboration”。
- **[Evolutionary Generation of Multi-Agent Systems](https://icml.cc/virtual/2026/poster/62216)** — 研究“Evolutionary Generation of Multi-Agent Systems”。
- **[Evolving Interpretable Constitutions for Multi-Agent Coordination](https://icml.cc/virtual/2026/poster/66529)** — 研究“Evolving Interpretable Constitutions”，场景是面向“Multi-Agent Coordination”。
- **[Factored Value Functions for Graph-Based Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/62462)** — 研究“Factored Value Functions”，场景是面向“Graph-Based Multi-Agent Reinforcement Learning”。
- **[Fault Tolerant Multi-Agent Learning with Adversarial Budget Constraints](https://icml.cc/virtual/2026/poster/61177)** — 研究“Fault Tolerant Multi-Agent Learning”，并引入“Adversarial Budget Constraints”。
- **[From Interaction Trajectories to Prompt Rules: Credit Assignment for Multi-Agent Prompt Optimization](https://icml.cc/virtual/2026/poster/61502)** — 提出/整理 **From Interaction Trajectories to Prompt Rules**，面向“Multi-Agent Prompt Optimization”研究“Credit Assignment”。
- **[Gecko: A Simulation Environment with Stateful Feedback for Refining Agent Tool Calls](https://icml.cc/virtual/2026/poster/65078)** — 提出 **Gecko**，将“Stateful Feedback for Refining Agent Tool Calls”引入“Simulation Environment”。
- **[Great Minds Think Alike: Contextual Tacit Communication for Decentralized LLM-Agent Cooperation](https://icml.cc/virtual/2026/poster/63854)** — 提出/整理 **Great Minds Think Alike**，面向“Decentralized LLM-Agent Cooperation”研究“Contextual Tacit Communication”。
- **[Group Cognition Learning: Making Everything Better Through Controlled Two-Stage Agents Collaboration](https://icml.cc/virtual/2026/poster/61162)** — 提出 **Group Cognition Learning**，用“Controlled Two-Stage Agents Collaboration”来“Making Everything Better”。
- **[HieraMAS: Optimizing Intra-Node LLM Mixtures and Inter-Node Topology for Multi-Agent Systems](https://icml.cc/virtual/2026/poster/61537)** — 提出/整理 **HieraMAS**，面向“Multi-Agent Systems”研究“Optimizing Intra-Node LLM Mixtures and Inter-Node Topology”。
- **[HiMAP-Travel: Hierarchical Multi-Agent Planning for Long-Horizon Constrained Travel](https://icml.cc/virtual/2026/poster/61536)** — 提出/整理 **HiMAP-Travel**，面向“Long-Horizon Constrained Travel”研究“Hierarchical Multi-Agent Planning”。
- **[HPS: Hyperspherical Parameter Sharing for Efficient Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/65604)** — 提出/整理 **HPS**，面向“Efficient Multi-Agent Reinforcement Learning”研究“Hyperspherical Parameter Sharing”。
- **[HyPOLE: Hyperproperty-Guided Multi-Agent Reinforcement Learning under Partial Observation](https://icml.cc/virtual/2026/poster/65345)** — 提出/整理 **HyPOLE**，考察“Hyperproperty-Guided Multi-Agent Reinforcement Learning”在“Partial Observation”下的表现。
- **[IEC: When Information-Driven Exploration Meets Spectral Consensus via Primal–Dual Reward Regularization in Decentralized Multi-Agent RL](https://icml.cc/virtual/2026/poster/65199)** — 提出 **IEC**，用“Primal–Dual Reward Regularization in Decentralized Multi-Agent RL”来“When Information-Driven Exploration Meets Spectral Consensus”。
- **[Investigating Component Contributions in Multi-Agent ML Systems](https://icml.cc/virtual/2026/poster/65244)** — 研究“Investigating Component Contributions”，场景是在“Multi-Agent ML Systems”中。
- **[Judgment Operators: A Composition-Invariant Substrate for Multi-Agent Action Spaces](https://icml.cc/virtual/2026/poster/65952)** — 提出/整理 **Judgment Operators**，面向“Multi-Agent Action Spaces”研究“Composition-Invariant Substrate”。
- **[Latent Collaboration in Multi-Agent Systems](https://icml.cc/virtual/2026/poster/61180)** — 研究“Latent Collaboration”，场景是在“Multi-Agent Systems”中。
- **[Learning Decentralized LLM Collaboration with Multi-Agent Actor Critic](https://icml.cc/virtual/2026/poster/62068)** — 研究“Learning Decentralized LLM Collaboration”，并引入“Multi-Agent Actor Critic”。
- **[Learning Disentangled Multi-Agent World Model for Decentralized Control](https://icml.cc/virtual/2026/poster/61713)** — 研究“Learning Disentangled Multi-Agent World Model”，场景是面向“Decentralized Control”。
- **[Learning Multi-Agent Coordination via Sheaf-ADMM](https://icml.cc/virtual/2026/poster/62363)** — 研究“Learning Multi-Agent Coordination”，核心机制是“Sheaf-ADMM”。
- **[LLawCo: Learning Laws of Cooperation for Modeling Embodied Multi-Agent Behavior](https://icml.cc/virtual/2026/poster/64415)** — 提出/整理 **LLawCo**，面向“Modeling Embodied Multi-Agent Behavior”研究学习“Laws of Cooperation”。
- **[LLM-Guided Communication for Cooperative Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/61721)** — 研究“LLM-Guided Communication”，场景是面向“Cooperative Multi-Agent Reinforcement Learning”。
- **[MAFE: Enabling Equitable Algorithm Design in Multi-Agent Multi-Stage Decision-Making Systems](https://icml.cc/virtual/2026/poster/60878)** — 提出/整理 **MAFE**，考察“Enabling Equitable Algorithm Design”在“Multi-Agent Multi-Stage Decision-Making Systems”中的表现。
- **[MARS-SQL: A Multi-Agent Reinforcement Learning Framework For Text-To-SQL](https://icml.cc/virtual/2026/poster/65053)** — 提出/整理 **MARS-SQL**，面向“Text-To-SQL”研究“Multi-Agent Reinforcement Learning Framework”。
- **[MAS-Architect: Declarative Multi-Agent System Design via Separation of Concerns](https://icml.cc/virtual/2026/poster/63290)** — 提出 **MAS-Architect**，用“Separation of Concerns”来“Declarative Multi-Agent System Design”。
- **[MAS-ProVe: Understanding the Process Verification of Multi-Agent Systems](https://icml.cc/virtual/2026/poster/63666)** — 提出/整理 **MAS-ProVe**，关注“Understanding the Process Verification of Multi-Agent Systems”。
- **[MASPO: Joint Prompt Optimization for LLM-based Multi-Agent Systems](https://icml.cc/virtual/2026/poster/62219)** — 提出/整理 **MASPO**，面向“LLM-based Multi-Agent Systems”研究“Joint Prompt Optimization”。
- **[MASPOB: Bandit-Based Prompt Optimization for Multi-Agent Systems with Graph Neural Networks](https://icml.cc/virtual/2026/poster/65791)** — 提出 **MASPOB**，将“Graph Neural Networks”引入“Bandit-Based Prompt Optimization for Multi-Agent Systems”。
- **[MemIncept: Steering LLM Agents via Cooperative Stealthy Memory Injections](https://icml.cc/virtual/2026/poster/66667)** — 提出 **MemIncept**，用“Cooperative Stealthy Memory Injections”来“Steering LLM Agents”。
- **[MOC: Multi-Order Communication in LLM-based Multi-Agent Systems](https://icml.cc/virtual/2026/poster/60749)** — 提出/整理 **MOC**，考察“Multi-Order Communication”在“LLM-based Multi-Agent Systems”中的表现。
- **[MonoScale: Scaling Multi-Agent System with Monotonic Improvement](https://icml.cc/virtual/2026/poster/62913)** — 提出 **MonoScale**，将“Monotonic Improvement”引入扩展“Multi-Agent System”。
- **[Mosaic: Runtime-Efficient Multi-Agent Embodied Planning](https://icml.cc/virtual/2026/poster/62291)** — 提出/整理 **Mosaic**，关注“Runtime-Efficient Multi-Agent Embodied Planning”。
- **[Multi-agent imitation learning with function approximation: linear Markov games and beyond](https://icml.cc/virtual/2026/poster/64113)** — 提出/整理 **Multi-agent imitation learning with function approximation**，关注“linear Markov games and beyond”。
- **[Multi-Agent Reinforcement Learning with Submodular Reward](https://icml.cc/virtual/2026/poster/61139)** — 研究“Multi-Agent Reinforcement Learning”，并引入“Submodular Reward”。
- **[Multi-Agent Teams Hold Experts Back](https://icml.cc/virtual/2026/poster/63358)** — 研究“Multi-Agent Teams Hold Experts Back”。
- **[Navigating the Energy Landscape of Collaboration: Multi-Agent Communication Graph Generation via Score-Based Diffusion](https://icml.cc/virtual/2026/poster/61913)** — 提出 **Navigating the Energy Landscape of Collaboration**，用“Score-Based Diffusion”来“Multi-Agent Communication Graph Generation”。
- **[NonZero: Interaction-Guided Exploration for Multi-Agent Monte Carlo Tree Search](https://icml.cc/virtual/2026/poster/64800)** — 提出/整理 **NonZero**，面向“Multi-Agent Monte Carlo Tree Search”研究“Interaction-Guided Exploration”。
- **[Offline Multi-agent Continual Cooperation via Skill Partition and Reuse](https://icml.cc/virtual/2026/poster/66211)** — 研究“Offline Multi-agent Continual Cooperation”，核心机制是“Skill Partition and Reuse”。
- **[Offline Multi-Agent Reinforcement Learning via Sequential Score Decomposition](https://icml.cc/virtual/2026/poster/64191)** — 研究“Offline Multi-Agent Reinforcement Learning”，核心机制是“Sequential Score Decomposition”。
- **[OMAC: A Holistic Optimization Framework for LLM-Based Multi-Agent Collaboration](https://icml.cc/virtual/2026/poster/66164)** — 提出/整理 **OMAC**，面向“LLM-Based Multi-Agent Collaboration”研究“Holistic Optimization Framework”。
- **[OpenDeception: Learning Deception and Trust in Human–AI Interaction via Multi-Agent Simulation](https://icml.cc/virtual/2026/poster/64249)** — 提出 **OpenDeception**，用“Multi-Agent Simulation”来学习“Deception and Trust in Human–AI Interaction”。
- **[Position: Multi-Agent Explainability Needs Contracts Before Methods](https://icml.cc/virtual/2026/poster/67110)** — 提出/整理 **Position**，关注“Multi-Agent Explainability Needs Contracts Before Methods”。
- **[Position: Multi-Agent Systems Should Prioritize Concurrency Control](https://icml.cc/virtual/2026/poster/67076)** — 提出/整理 **Position**，关注“Multi-Agent Systems Should Prioritize Concurrency Control”。
- **[PromptPilot: Game-Theoretic Multi-Agent Prompt Optimization for Segment Anything](https://icml.cc/virtual/2026/poster/65063)** — 提出/整理 **PromptPilot**，面向“Segment Anything”研究“Game-Theoretic Multi-Agent Prompt Optimization”。
- **[RADAR: Redundancy-Aware Diffusion for Multi-Agent Communication Structure Generation](https://icml.cc/virtual/2026/poster/65087)** — 提出/整理 **RADAR**，面向“Multi-Agent Communication Structure Generation”研究“Redundancy-Aware Diffusion”。
- **[Recognize Your Orchestrator: An Entropy Dynamics Perspective for LLM Multi-Agent Systems](https://icml.cc/virtual/2026/poster/63622)** — 提出/整理 **Recognize Your Orchestrator**，面向“LLM Multi-Agent Systems”研究“Entropy Dynamics Perspective”。
- **[Representational Similarity and Model Behavior in Multi-Agent Interaction](https://icml.cc/virtual/2026/poster/60905)** — 研究“Representational Similarity and Model Behavior”，场景是在“Multi-Agent Interaction”中。
- **[Role-Level Inductive Bias for Cross-Task Generalization in Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/61552)** — 研究“Role-Level Inductive Bias”，场景是面向“Cross-Task Generalization in Multi-Agent Reinforcement Learning”。
- **[ScaleSim: Serving Large-Scale Multi-Agent Simulation with Invocation Distance-Based Memory Management](https://icml.cc/virtual/2026/poster/62000)** — 提出 **ScaleSim**，将“Invocation Distance-Based Memory Management”引入“Serving Large-Scale Multi-Agent Simulation”。
- **[Scaling Multi-Agent Environment Co-Design with Diffusion Models](https://icml.cc/virtual/2026/poster/65949)** — 研究“Scaling Multi-Agent Environment Co-Design”，并引入“Diffusion Models”。
- **[Scaling up Multi-Turn Off-Policy RL and Multi-Agent Tree Search for LLM Step-Provers](https://icml.cc/virtual/2026/poster/65141)** — 研究“Scaling up Multi-Turn Off-Policy RL and Multi-Agent Tree Search”，场景是面向“LLM Step-Provers”。
- **[SceneSmith: Agentic Generation of Simulation-Ready Indoor Scenes](https://icml.cc/virtual/2026/poster/63465)** — 提出/整理 **SceneSmith**，关注“Agentic Generation of Simulation-Ready Indoor Scenes”。
- **[Sparks of Cooperative Reasoning: LLMs as Strategic Hanabi Agents](https://icml.cc/virtual/2026/poster/60843)** — 提出/整理 **Sparks of Cooperative Reasoning**，关注“LLMs as Strategic Hanabi Agents”。
- **[Sparse Topology-Aware Pairwise Scoring for Large-Scale Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/65907)** — 研究“Sparse Topology-Aware Pairwise Scoring”，场景是面向“Large-Scale Multi-Agent Reinforcement Learning”。
- **[Strat-Reasoner: Reinforcing Strategic Reasoning of LLMs in Multi-Agent Games](https://icml.cc/virtual/2026/poster/63649)** — 提出/整理 **Strat-Reasoner**，考察“Reinforcing Strategic Reasoning of LLMs”在“Multi-Agent Games”中的表现。
- **[Systematic Failures in Collective Reasoning under Distributed Information in Multi-Agent LLMs](https://icml.cc/virtual/2026/poster/62206)** — 研究“Systematic Failures”，场景是在“Collective Reasoning under Distributed Information in Multi-Agent LLMs”中。
- **[TABX: A High-Throughput Sandbox Battle Simulator for Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/62035)** — 提出/整理 **TABX**，面向“Multi-Agent Reinforcement Learning”研究“High-Throughput Sandbox Battle Simulator”。
- **[TACTIC: Task-Aware Sparse Coordination Graphs for Multi-Task Multi-agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/66706)** — 提出/整理 **TACTIC**，面向“Multi-Task Multi-agent Reinforcement Learning”研究“Task-Aware Sparse Coordination Graphs”。
- **[Talk, Judge, Cooperate: Gossip-Driven Indirect Reciprocity in Self-Interested LLM Agents](https://icml.cc/virtual/2026/poster/62130)** — 提出/整理 **Talk, Judge, Cooperate**，考察“Gossip-Driven Indirect Reciprocity”在“Self-Interested LLM Agents”中的表现。
- **[TeamTR: Trust-Region Fine-Tuning for Multi-Agent LLM Coordination](https://icml.cc/virtual/2026/poster/64955)** — 提出/整理 **TeamTR**，面向“Multi-Agent LLM Coordination”研究“Trust-Region Fine-Tuning”。
- **[The Value of Variance: Mitigating Debate Collapse in Multi-Agent Systems via Uncertainty-Driven Policy Optimization](https://icml.cc/virtual/2026/poster/65638)** — 提出 **The Value of Variance**，用“Uncertainty-Driven Policy Optimization”来“Mitigating Debate Collapse in Multi-Agent Systems”。
- **[Toward Culturally Aligned LLMs through Ontology-Guided Multi-Agent Reasoning](https://icml.cc/virtual/2026/poster/62316)** — 研究“Toward Culturally Aligned LLMs”，核心机制是“Ontology-Guided Multi-Agent Reasoning”。
- **[Towards Complete Multi-Agent Coordination Policy Learning via Denoising Maximum Entropy Optimization](https://icml.cc/virtual/2026/poster/64327)** — 研究“Towards Complete Multi-Agent Coordination Policy Learning”，核心机制是“Denoising Maximum Entropy Optimization”。
- **[Weaving in the Clouds: Achieving Synergistic Collaboration among LLM Agents via Federated Learning](https://icml.cc/virtual/2026/poster/66521)** — 提出 **Weaving in the Clouds**，用“Federated Learning”来“Achieving Synergistic Collaboration among LLM Agents”。
- **[What Preferences Can—and Cannot—Predict in Multi-Agent Online Learning](https://icml.cc/virtual/2026/poster/66240)** — 研究“What Preferences Can—and Cannot—Predict”，场景是在“Multi-Agent Online Learning”中。
- **[When LLMs Develop Languages: Symbolic Communication for Efficient Multi-Agent Reasoning](https://icml.cc/virtual/2026/poster/61557)** — 提出/整理 **When LLMs Develop Languages**，面向“Efficient Multi-Agent Reasoning”研究“Symbolic Communication”。
- **[When Planning Fails Despite Correct Execution: On Epistemic Calibration for LLM-Based Multi-Agent Systems](https://icml.cc/virtual/2026/poster/65821)** — 提出/整理 **When Planning Fails Despite Correct Execution**，面向“LLM-Based Multi-Agent Systems”研究“On Epistemic Calibration”。
- **[Which LLM Multi-Agent Protocol to Choose?](https://icml.cc/virtual/2026/poster/65129)** — 以“Which LLM Multi-Agent Protocol to Choose?”为问题，考察 agent 的能力边界或失败模式。

<a id="tool-use-training-rl"></a>
### 🛠️ 3. 工具使用、训练与 RL / Tool Use, Training & RL (58)

从 prompt-based agent 转向可训练 agent，关注 tool-use RL、agentic RL、GRPO、trajectory-SFT、自演化和蒸馏。

- **[Agent Learning via Early Experience](https://icml.cc/virtual/2026/poster/64488)** — 训练/优化“Agent Learning”，核心机制是“Early Experience”。
- **[Agent World Model: Infinity Synthetic Environments for Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/64306)** — 提出/整理 **Agent World Model**，面向“Agentic Reinforcement Learning”研究“Infinity Synthetic Environments”。
- **[Agent-Omit: Training Efficient LLM Agents for Adaptive Thought and Observation Omission via Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/63271)** — 提出 **Agent-Omit**，用“Agentic Reinforcement Learning”来训练“Efficient LLM Agents for Adaptive Thought and Observation Omission”。
- **[Agent0-VL: Exploring Self-Evolving Agent for Tool-Integrated Vision-Language Reasoning](https://icml.cc/virtual/2026/poster/63095)** — 提出/整理 **Agent0-VL**，面向“Tool-Integrated Vision-Language Reasoning”研究“Exploring Self-Evolving Agent”。
- **[Agentic Monte Carlo: Reinforcement Learning for Black-Box LLM Agents](https://icml.cc/virtual/2026/poster/62740)** — 提出/整理 **Agentic Monte Carlo**，面向“Black-Box LLM Agents”研究“Reinforcement Learning”。
- **[AuTAgent: A Reinforcement Learning Framework for Tool-Augmented Audio Reasoning](https://icml.cc/virtual/2026/poster/64128)** — 提出/整理 **AuTAgent**，面向“Tool-Augmented Audio Reasoning”研究“Reinforcement Learning Framework”。
- **[AutoTool: Dynamic Tool Selection and Integration for Agentic Reasoning](https://icml.cc/virtual/2026/poster/65574)** — 提出/整理 **AutoTool**，面向“Agentic Reasoning”研究“Dynamic Tool Selection and Integration”。
- **[Beyond Static Endpoints: Tool Programs as an Interface for Flexible Agentic Web Services](https://icml.cc/virtual/2026/poster/62527)** — 提出/整理 **Beyond Static Endpoints**，面向“Flexible Agentic Web Services”研究“Tool Programs as an Interface”。
- **[Bootstrapped Exploration with Causal Reasoning: A Training Paradigm for Adaptive Forecasting Agent](https://icml.cc/virtual/2026/poster/65944)** — 提出/整理 **Bootstrapped Exploration with Causal Reasoning**，面向“Adaptive Forecasting Agent”研究“Training Paradigm”。
- **[Can Agents Generalize to the Open World? Unveiling the Fragility of Static Training in Tool Use](https://icml.cc/virtual/2026/poster/65179)** — 以“Can Agents Generalize to the Open World? Unveiling the Fragility of Static Training in Tool Use”为问题，考察 agent 的能力边界或失败模式。
- **[CRPO: Character-centric Group Relative Policy Optimization for Role-aware Reasoning in Role-playing Agents](https://icml.cc/virtual/2026/poster/62395)** — 提出/整理 **CRPO**，考察“Character-centric Group Relative Policy Optimization for Role-aware Reasoning”在“Role-playing Agents”中的表现。
- **[D-CORE: Incentivizing Task Decomposition in Large Reasoning Models for Complex Tool Use](https://icml.cc/virtual/2026/poster/61056)** — 提出/整理 **D-CORE**，考察“Incentivizing Task Decomposition”在“Large Reasoning Models for Complex Tool Use”中的表现。
- **[Data Agent: Learning to Select Data via End-to-End Dynamic Optimization](https://icml.cc/virtual/2026/poster/62583)** — 提出 **Data Agent**，用“End-to-End Dynamic Optimization”来学习“to Select Data”。
- **[DIVE: Scaling Diversity in Agentic Task Synthesis for Generalizable Tool Use](https://icml.cc/virtual/2026/poster/66305)** — 提出/整理 **DIVE**，考察扩展“Diversity”在“Agentic Task Synthesis for Generalizable Tool Use”中的表现。
- **[Diversity Over Frequency: Rethinking Tool Use in Visual Chain-of-Thought Agents](https://icml.cc/virtual/2026/poster/61111)** — 提出/整理 **Diversity Over Frequency**，考察“Rethinking Tool Use”在“Visual Chain-of-Thought Agents”中的表现。
- **[Dynamic Optimizations of LLM Ensembles with Two-Stage Reinforcement Learning Agents](https://icml.cc/virtual/2026/poster/64593)** — 训练/优化“Dynamic Optimizations of LLM Ensembles”，并引入“Two-Stage Reinforcement Learning Agents”。
- **[EvoC2F: Compiling Tool Orchestration for Efficient and Evolvable LLM Agents](https://icml.cc/virtual/2026/poster/63166)** — 提出/整理 **EvoC2F**，面向“Efficient and Evolvable LLM Agents”研究“Compiling Tool Orchestration”。
- **[ExSkill: Continual Learning from Experience and Skills in Multimodal Agents](https://icml.cc/virtual/2026/poster/65729)** — 提出/整理 **ExSkill**，考察“Continual Learning from Experience and Skills”在“Multimodal Agents”中的表现。
- **[FactGuard: Agentic Video Misinformation Detection via Reinforcement Learning](https://icml.cc/virtual/2026/poster/65720)** — 提出 **FactGuard**，用“Reinforcement Learning”来“Agentic Video Misinformation Detection”。
- **[Fourier Features Let Agents Learn High Precision Policies with Imitation Learning](https://icml.cc/virtual/2026/poster/60655)** — 训练/优化“Fourier Features Let Agents Learn High Precision Policies”，并引入“Imitation Learning”。
- **[From Interactions to Principles: Experience-Driven Self-Distillation for Evolving LLM Agents](https://icml.cc/virtual/2026/poster/65641)** — 提出/整理 **From Interactions to Principles**，面向“Evolving LLM Agents”研究“Experience-Driven Self-Distillation”。
- **[FT-Dojo: Towards Autonomous LLM Fine-Tuning with Language Agents](https://icml.cc/virtual/2026/poster/63475)** — 提出 **FT-Dojo**，将“Language Agents”引入迈向“Autonomous LLM Fine-Tuning”。
- **[GLARE: Scalable Neuro-Symbolic Reward Shaping for LLM Agents via Group-Level Automata](https://icml.cc/virtual/2026/poster/66450)** — 提出 **GLARE**，用“Group-Level Automata”来“Scalable Neuro-Symbolic Reward Shaping for LLM Agents”。
- **[Goal-Conditioned Agents that Learn Everything All at Once](https://icml.cc/virtual/2026/poster/61317)** — 训练/优化“Goal-Conditioned Agents that Learn Everything All at Once”。
- **[Graph-R1: Towards Agentic GraphRAG Framework via End-to-end Reinforcement Learning](https://icml.cc/virtual/2026/poster/63269)** — 提出 **Graph-R1**，用“End-to-end Reinforcement Learning”来迈向“Agentic GraphRAG Framework”。
- **[GRPO-based Cluster Decision Agent for Unknown-$\boldsymbol{K}$ Multi-view Clustering](https://icml.cc/virtual/2026/poster/62944)** — 训练/优化“GRPO-based Cluster Decision Agent”，场景是面向“Unknown-$\boldsymbol{K}$ Multi-view Clustering”。
- **[HiPER: Hierarchical Plan–Execute RL for Multi-Turn LLM Agents](https://icml.cc/virtual/2026/poster/64058)** — 提出/整理 **HiPER**，面向“Multi-Turn LLM Agents”研究“Hierarchical Plan–Execute RL”。
- **[Imitation Learning for Multi-turn LM Agents via On-policy Expert Corrections](https://icml.cc/virtual/2026/poster/61984)** — 训练/优化“Imitation Learning for Multi-turn LM Agents”，核心机制是“On-policy Expert Corrections”。
- **[InfoPO: Information-Driven Policy Optimization for User-Centric Agents](https://icml.cc/virtual/2026/poster/64385)** — 提出/整理 **InfoPO**，面向“User-Centric Agents”研究“Information-Driven Policy Optimization”。
- **[IntentRL: Training Proactive User-intent Agents for Open-ended Deep Research via Reinforcement Learning](https://icml.cc/virtual/2026/poster/61305)** — 提出 **IntentRL**，用“Reinforcement Learning”来训练“Proactive User-intent Agents for Open-ended Deep Research”。
- **[Just-In-Time Reinforcement Learning: Continual Learning in LLM Agents Without Gradient Updates](https://icml.cc/virtual/2026/poster/61517)** — 提出/整理 **Just-In-Time Reinforcement Learning**，考察“Continual Learning”在“LLM Agents Without Gradient Updates”中的表现。
- **[Large Language Model Agents Are Not Always Faithful Self-Evolvers](https://icml.cc/virtual/2026/poster/62034)** — 训练/优化“Large Language Model Agents Are Not Always Faithful Self-Evolvers”。
- **[Learning Task-Sufficient World Models by Synergizing Agentic Exploration and Structured Modeling](https://icml.cc/virtual/2026/poster/64209)** — 训练/优化“Learning Task-Sufficient World Models”，核心机制是“Synergizing Agentic Exploration and Structured Modeling”。
- **[Learning to Explore: Scaling Agentic Reasoning via Exploration-Aware Policy Optimization](https://icml.cc/virtual/2026/poster/63287)** — 提出 **Learning to Explore**，用“Exploration-Aware Policy Optimization”来扩展“Agentic Reasoning”。
- **[LLM4Cov: Execution-Grounded Agent Learning for High-Coverage Hardware Verification](https://icml.cc/virtual/2026/poster/61436)** — 提出/整理 **LLM4Cov**，面向“High-Coverage Hardware Verification”研究“Execution-Grounded Agent Learning”。
- **[On Effectiveness and Efficiency of Agentic Tool-calling and RL Training](https://icml.cc/virtual/2026/poster/66433)** — 训练/优化“On Effectiveness and Efficiency of Agentic Tool-calling and RL Training”。
- **[On Group Relative Policy Optimization Collapse in Agent Search: The Lazy Likelihood-Displacement](https://icml.cc/virtual/2026/poster/63945)** — 提出/整理 **On Group Relative Policy Optimization Collapse in Agent Search**，关注“Lazy Likelihood-Displacement”。
- **[Persistent Semantic Entities in Tool-Augmented LLM Systems](https://icml.cc/virtual/2026/poster/60521)** — 训练/优化“Persistent Semantic Entities”，场景是在“Tool-Augmented LLM Systems”中。
- **[Phase-Aware Mixture of Experts for Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/64382)** — 训练/优化“Phase-Aware Mixture of Experts”，场景是面向“Agentic Reinforcement Learning”。
- **[Post-Training LLMs as Better Decision-Making Agents: A Regret-Minimization Approach](https://icml.cc/virtual/2026/poster/62760)** — 提出/整理 **Post-Training LLMs as Better Decision-Making Agents**，关注“Regret-Minimization Approach”。
- **[PosterAgent: Agentic Poster Generation via Stage-Aware Reinforcement Learning](https://icml.cc/virtual/2026/poster/62650)** — 提出 **PosterAgent**，用“Stage-Aware Reinforcement Learning”来“Agentic Poster Generation”。
- **[Process Reward Agents for Steering Knowledge-Intensive Reasoning](https://icml.cc/virtual/2026/poster/66434)** — 训练/优化“Process Reward Agents”，场景是面向“Steering Knowledge-Intensive Reasoning”。
- **[PyVision-RL: Forging Open Agentic Vision Models via RL](https://icml.cc/virtual/2026/poster/65374)** — 提出 **PyVision-RL**，用“RL”来“Forging Open Agentic Vision Models”。
- **[Rationality Measurement and Theory for Reinforcement Learning Agents](https://icml.cc/virtual/2026/poster/64009)** — 训练/优化“Rationality Measurement and Theory”，场景是面向“Reinforcement Learning Agents”。
- **[ReSeek: A Self-Correcting Framework for Search Agents with Instructive Rewards](https://icml.cc/virtual/2026/poster/63905)** — 提出 **ReSeek**，将“Instructive Rewards”引入“Self-Correcting Framework for Search Agents”。
- **[ScaleEnv: Scaling Environment Synthesis from Scratch for Generalist Interactive Tool-Use Agent Training](https://icml.cc/virtual/2026/poster/66374)** — 提出/整理 **ScaleEnv**，面向“Generalist Interactive Tool-Use Agent Training”研究扩展“Environment Synthesis from Scratch”。
- **[SEAgent: Self-Evolving Computer Use Agent with Autonomous Learning from Experience](https://icml.cc/virtual/2026/poster/65711)** — 提出 **SEAgent**，将“Autonomous Learning from Experience”引入“Self-Evolving Computer Use Agent”。
- **[Self-Evolving LLM Agents under Offline Data Support](https://icml.cc/virtual/2026/poster/62030)** — 训练/优化“Self-Evolving LLM Agents under Offline Data Support”。
- **[Stratified GRPO: Handling Structural Heterogeneity in Reinforcement Learning of LLM Search Agents](https://icml.cc/virtual/2026/poster/63159)** — 提出/整理 **Stratified GRPO**，考察“Handling Structural Heterogeneity”在“Reinforcement Learning of LLM Search Agents”中的表现。
- **[Student-Centered Distillation Narrows the Agentic Gap Between Small and Large LLMs](https://icml.cc/virtual/2026/poster/64717)** — 训练/优化“Student-Centered Distillation Narrows the Agentic Gap Between Small and Large LLMs”。
- **[T$^2$PO: Uncertainty-Guided Exploration Control for Stable Multi-Turn Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/63090)** — 提出/整理 **T$^2$PO**，面向“Stable Multi-Turn Agentic Reinforcement Learning”研究“Uncertainty-Guided Exploration Control”。
- **[This State Looks Like That: Self-Interpretable Reinforcement Learning Agents using Prototype Soft Actor-Critic](https://icml.cc/virtual/2026/poster/62377)** — 提出 **This State Looks Like That**，用“Prototype Soft Actor-Critic”来“Self-Interpretable Reinforcement Learning Agents”。
- **[TodoEvolve: Learning to Architect Agent Planning Systems](https://icml.cc/virtual/2026/poster/64136)** — 提出/整理 **TodoEvolve**，关注“Learning to Architect Agent Planning Systems”。
- **[Towards Pareto-Optimal Tool-Integrated Agents with Pareto Ranking Policy Optimization](https://icml.cc/virtual/2026/poster/65819)** — 训练/优化“Towards Pareto-Optimal Tool-Integrated Agents”，并引入“Pareto Ranking Policy Optimization”。
- **[Training LLM Agents to Empower Humans](https://icml.cc/virtual/2026/poster/61627)** — 训练/优化“Training LLM Agents to Empower Humans”。
- **[Understanding Reasoning Collapse in LLM Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/66821)** — 训练/优化“Understanding Reasoning Collapse”，场景是在“LLM Agent Reinforcement Learning”中。
- **[What Does Vision Tool-Use Reinforcement Learning Really Learn? Disentangling Tool-Induced and Intrinsic Effects for Crop-and-Zoom](https://icml.cc/virtual/2026/poster/62232)** — 以“What Does Vision Tool-Use Reinforcement Learning Really Learn? Disentangling Tool-Induced and Intrinsic Effects for Crop-and-Zoom”为问题，考察 agent 的能力边界或失败模式。
- **[Words Towards Explainability: Caption Label-Free Learning via Dual Loop Agentic Time Series Captioning](https://icml.cc/virtual/2026/poster/64438)** — 提出 **Words Towards Explainability**，用“Dual Loop Agentic Time Series Captioning”来“Caption Label-Free Learning”。

<a id="safety-security-governance"></a>
### 🛡️ 4. 安全、鲁棒性与治理 / Safety, Security & Governance (51)

围绕多轮攻击、工具投毒、环境扰动、隐私外泄、拒答边界、红队、运行时检测和安全护栏展开。

- **[A New Framework for Cybersecurity Refusals in AI Agents](https://icml.cc/virtual/2026/poster/61093)** — 提出一个面向“AI Agents”中“Cybersecurity Refusals”的新框架。
- **[AdvEvo-MARL: Shaping Internalized Safety through Adversarial Co-Evolution in Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/66275)** — 提出 **AdvEvo-MARL**，用“Adversarial Co-Evolution in Multi-Agent Reinforcement Learning”来“Shaping Internalized Safety”。
- **[AIR: Improving Agent Safety through Incident Response](https://icml.cc/virtual/2026/poster/62353)** — 提出 **AIR**，用“Incident Response”来改进“Agent Safety”。
- **[Architecture Matters for Multi-Agent Security](https://icml.cc/virtual/2026/poster/64792)** — 分析架构选择对“Multi-Agent Security”的影响。
- **[Are Your Agents Upward Deceivers?](https://icml.cc/virtual/2026/poster/62581)** — 以“Are Your Agents Upward Deceivers?”为问题，考察 agent 的能力边界或失败模式。
- **[AutoRAS: Learning Robust Agentic Systems with Primitive Representations](https://icml.cc/virtual/2026/poster/66006)** — 提出 **AutoRAS**，将“Primitive Representations”引入学习“Robust Agentic Systems”。
- **[BlueCodeAgent: A Blue Teaming Agent Powered by Automated Red Teaming for CodeGen AI](https://icml.cc/virtual/2026/poster/63820)** — 提出 **BlueCodeAgent**，用“Automated Red Teaming for CodeGen AI”来“Blue Teaming Agent Powered”。
- **[Causal Detection of Multi-Step LLM Agent Attacks](https://icml.cc/virtual/2026/poster/64714)** — 研究“Causal Detection of Multi-Step LLM Agent Attacks”。
- **[Clarify Before You Draw: Proactive Agents for Robust Text-to-CAD Generation](https://icml.cc/virtual/2026/poster/66672)** — 提出/整理 **Clarify Before You Draw**，面向“Robust Text-to-CAD Generation”研究“Proactive Agents”。
- **[Co-RedTeam: Orchestrated Security Discovery and Exploitation with LLM Agents](https://icml.cc/virtual/2026/poster/60747)** — 提出 **Co-RedTeam**，将“LLM Agents”引入“Orchestrated Security Discovery and Exploitation”。
- **[Contextualized Privacy Defense for LLM Agents](https://icml.cc/virtual/2026/poster/62996)** — 研究“Contextualized Privacy Defense”，场景是面向“LLM Agents”。
- **[CVE-Factory: Scaling Expert-Level Agentic Tasks for Code Security Vulnerability](https://icml.cc/virtual/2026/poster/65622)** — 提出/整理 **CVE-Factory**，面向“Code Security Vulnerability”研究扩展“Expert-Level Agentic Tasks”。
- **[EMBGUARD: Constructing Hazard-Aware Guardrails for Safe Planning in Embodied Agents](https://icml.cc/virtual/2026/poster/63023)** — 提出/整理 **EMBGUARD**，考察“Constructing Hazard-Aware Guardrails for Safe Planning”在“Embodied Agents”中的表现。
- **[Functional Cache Grafting: Robust and Rapid Code-Policy Synthesis for Embodied Agents](https://icml.cc/virtual/2026/poster/62313)** — 提出/整理 **Functional Cache Grafting**，面向“Embodied Agents”研究“Robust and Rapid Code-Policy Synthesis”。
- **[Interaction-Breaking Adversarial Learning Framework for Robust Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/61001)** — 研究“Interaction-Breaking Adversarial Learning Framework”，场景是面向“Robust Multi-Agent Reinforcement Learning”。
- **[Learning When to Act or Refuse: Guarding Agentic Reasoning Models for Safe Multi-Step Tool Use](https://icml.cc/virtual/2026/poster/63878)** — 提出/整理 **Learning When to Act or Refuse**，面向“Safe Multi-Step Tool Use”研究“Guarding Agentic Reasoning Models”。
- **[MaMa: A Game-Theoretic Approach for Designing Safe Agentic Systems](https://icml.cc/virtual/2026/poster/64729)** — 提出/整理 **MaMa**，面向“Designing Safe Agentic Systems”研究“Game-Theoretic Approach”。
- **[MEMO: Memory-Augmented Model Context Optimization for Robust Multi-Turn Multi-Agent LLM Games](https://icml.cc/virtual/2026/poster/62950)** — 提出/整理 **MEMO**，面向“Robust Multi-Turn Multi-Agent LLM Games”研究“Memory-Augmented Model Context Optimization”。
- **[MINIM: Privacy-Aware Minimal View for Agents via Trusted Local Sanitization](https://icml.cc/virtual/2026/poster/61306)** — 提出 **MINIM**，用“Trusted Local Sanitization”来“Privacy-Aware Minimal View for Agents”。
- **[OrchJail: Jailbreaking Tool-Calling Text-to-Image Agents by Orchestration-Guided Fuzzing](https://icml.cc/virtual/2026/poster/63568)** — 提出 **OrchJail**，用“Orchestration-Guided Fuzzing”来“Jailbreaking Tool-Calling Text-to-Image Agents”。
- **[OTora: A Unified Red Teaming Framework for Reasoning-Level Denial-of-Service in LLM Agents](https://icml.cc/virtual/2026/poster/61771)** — 提出/整理 **OTora**，考察“Unified Red Teaming Framework for Reasoning-Level Denial-of-Service”在“LLM Agents”中的表现。
- **[PolicyGuard: Towards Test-time and Step-level Backdoor Defense for Reinforcement Learning Agent](https://icml.cc/virtual/2026/poster/65628)** — 提出/整理 **PolicyGuard**，面向“Reinforcement Learning Agent”研究迈向“Test-time and Step-level Backdoor Defense”。
- **[Position: Agent Security Needs Redefinition through a Holistic Framework](https://icml.cc/virtual/2026/poster/67194)** — 提出 **Position**，用“Holistic Framework”来“Agent Security Needs Redefinition”。
- **[Position: Agentic Safety is an Epistemic Property, Not a Behavioral One](https://icml.cc/virtual/2026/poster/67237)** — 提出/整理 **Position**，关注“Agentic Safety is an Epistemic Property, Not a Behavioral One”。
- **[Position: Collusion Risks Among AI Reasoning Agents Justify Certification Requirements for Making Market Decisions](https://icml.cc/virtual/2026/poster/67141)** — 提出/整理 **Position**，面向“Making Market Decisions”研究“Collusion Risks Among AI Reasoning Agents Justify Certification Requirements”。
- **[Position: Safety Must Precede the Deployment of Open-Ended AI Agents](https://icml.cc/virtual/2026/poster/67207)** — 提出/整理 **Position**，关注“Safety Must Precede the Deployment of Open-Ended AI Agents”。
- **[Position: To Defend Against Cyber Attacks, We Must Teach AI Agents to Hack](https://icml.cc/virtual/2026/poster/67161)** — 提出/整理 **Position**，考察“To Defend”面对“Cyber Attacks, We Must Teach AI Agents to Hack”的表现。
- **[Position: When AI Decides Who Gets an Organ: Multi-Agentic AI Systems in Transplant Medicine Risk Amplifying Disparities Without Targeted Explainability and Deployment Strategies](https://icml.cc/virtual/2026/poster/67102)** — 提出/整理 **Position**，考察“When AI Decides Who Gets an Organ: Multi-Agentic AI Systems”在“Transplant Medicine Risk Amplifying Disparities Without Targeted Explainability and Deployment Strategies”中的表现。
- **[PrivAct: Internalizing Contextual Privacy Preservation via Multi-Agent Preference Training](https://icml.cc/virtual/2026/poster/65131)** — 提出 **PrivAct**，用“Multi-Agent Preference Training”来“Internalizing Contextual Privacy Preservation”。
- **[Privacy Risks of Agentic Inferential Capabilities in Data Linkage Attacks](https://icml.cc/virtual/2026/poster/64683)** — 研究“Privacy Risks of Agentic Inferential Capabilities”，场景是在“Data Linkage Attacks”中。
- **[Profiling the Irrational Agent: Cognitive Modeling of LLM Behaviors in Sequential Jailbreaks](https://icml.cc/virtual/2026/poster/64559)** — 提出/整理 **Profiling the Irrational Agent**，考察“Cognitive Modeling of LLM Behaviors”在“Sequential Jailbreaks”中的表现。
- **[RedDebate: Safer Responses Through Multi-Agent Red Teaming Debates](https://icml.cc/virtual/2026/poster/66085)** — 提出 **RedDebate**，用“Multi-Agent Red Teaming Debates”来“Safer Responses”。
- **[Safe and Scalable Web Agent Learning via Recreated Websites](https://icml.cc/virtual/2026/poster/60744)** — 研究“Safe and Scalable Web Agent Learning”，核心机制是“Recreated Websites”。
- **[SafeHarbor: Defining Precise Decision Boundaries via Hierarchical Memory-Augmented Guardrail for LLM Agent Safety](https://icml.cc/virtual/2026/poster/64556)** — 提出 **SafeHarbor**，用“Hierarchical Memory-Augmented Guardrail for LLM Agent Safety”来“Defining Precise Decision Boundaries”。
- **[SafeSearch: Automated Red-Teaming of LLM-Based Search Agents](https://icml.cc/virtual/2026/poster/65893)** — 提出/整理 **SafeSearch**，关注“Automated Red-Teaming of LLM-Based Search Agents”。
- **[Secure Multi-agent Reinforcement Learning for Service Systems with Affinity and Byzantine Nodes: Stability Analysis and Protection Design](https://icml.cc/virtual/2026/poster/62838)** — 提出/整理 **Secure Multi-agent Reinforcement Learning for Service Systems with Affinity and Byzantine Nodes**，关注“Stability Analysis and Protection Design”。
- **[SkillTrojan: Backdoor Attacks on Skill-Based Agent Systems](https://icml.cc/virtual/2026/poster/65209)** — 提出/整理 **SkillTrojan**，考察“Backdoor Attacks”在“Skill-Based Agent Systems”上的表现。
- **[SOPE: Situation-Aware and Statistically Indistinguishable Privacy Exfiltration for MCP-enabled Agents](https://icml.cc/virtual/2026/poster/64028)** — 提出/整理 **SOPE**，面向“MCP-enabled Agents”研究“Situation-Aware and Statistically Indistinguishable Privacy Exfiltration”。
- **[Speculative Safety Honeypot: Toward Proactive Defense Against Multi-turn Agent Attacks](https://icml.cc/virtual/2026/poster/65283)** — 提出/整理 **Speculative Safety Honeypot**，考察迈向“Proactive Defense”面对“Multi-turn Agent Attacks”的表现。
- **[Sponge Tool Attack: Stealthy Denial-of-Efficiency against Tool-Augmented Agentic Reasoning](https://icml.cc/virtual/2026/poster/62486)** — 提出/整理 **Sponge Tool Attack**，考察“Stealthy Denial-of-Efficiency”面对“Tool-Augmented Agentic Reasoning”的表现。
- **[The Oversight Game: Learning to Cooperatively Balance an AI Agent's Safety and Autonomy](https://icml.cc/virtual/2026/poster/64439)** — 提出/整理 **The Oversight Game**，关注“Learning to Cooperatively Balance an AI Agent's Safety and Autonomy”。
- **[Think Twice Before You Act: Enhancing Agent Behavioral Safety with Thought Correction](https://icml.cc/virtual/2026/poster/60736)** — 提出 **Think Twice Before You Act**，将“Thought Correction”引入增强“Agent Behavioral Safety”。
- **[Think Twice Before You Act: Protecting LLM Agents Against Tool Description Poisoning via Isolated Planning](https://icml.cc/virtual/2026/poster/62116)** — 提出 **Think Twice Before You Act**，用“Isolated Planning”来保护“LLM Agents Against Tool Description Poisoning”。
- **[TRACER: Trajectory Risk Aggregation for Critical Episodes in Agentic Reasoning](https://icml.cc/virtual/2026/poster/61608)** — 提出/整理 **TRACER**，考察“Trajectory Risk Aggregation for Critical Episodes”在“Agentic Reasoning”中的表现。
- **[Training Language Model Agents to Find Vulnerabilities with CTF-Dojo](https://icml.cc/virtual/2026/poster/61783)** — 研究“Training Language Model Agents to Find Vulnerabilities”，并引入“CTF-Dojo”。
- **[VideoTemp-o3: Harmonizing Temporal Grounding and Video Understanding in Agentic Thinking-with-Videos](https://icml.cc/virtual/2026/poster/65425)** — 提出/整理 **VideoTemp-o3**，考察“Harmonizing Temporal Grounding and Video Understanding”在“Agentic Thinking-with-Videos”中的表现。
- **[Vulnerable Agent Identification in Large-Scale Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/64200)** — 研究“Vulnerable Agent Identification”，场景是在“Large-Scale Multi-Agent Reinforcement Learning”中。
- **[Watermarking LLM Agent Trajectories](https://icml.cc/virtual/2026/poster/62387)** — 研究“Watermarking LLM Agent Trajectories”。
- **[When Agents Go Rogue: Activation-Based Detection of Malicious Behaviors in Multi-Agent Systems](https://icml.cc/virtual/2026/poster/65619)** — 提出/整理 **When Agents Go Rogue**，考察“Activation-Based Detection of Malicious Behaviors”在“Multi-Agent Systems”中的表现。
- **[When Benign Inputs Lead to Severe Harms: Eliciting Unsafe Unintended Behaviors of Computer-Use Agents](https://icml.cc/virtual/2026/poster/64242)** — 提出/整理 **When Benign Inputs Lead to Severe Harms**，关注“Eliciting Unsafe Unintended Behaviors of Computer-Use Agents”。
- **[When Embedding-Based Defenses Fail: Rethinking Safety in LLM-Based Multi-Agent Systems](https://icml.cc/virtual/2026/poster/62170)** — 提出/整理 **When Embedding-Based Defenses Fail**，考察“Rethinking Safety”在“LLM-Based Multi-Agent Systems”中的表现。

<a id="theory-behavior-interpretability"></a>
### 🧠 5. 基础理论、行为分析与可解释性 / Theory, Behavior & Interpretability (39)

讨论 goal-directedness、agent empowerment、oversight、行为表征、校准、可解释性和可靠性科学。

- **[A World in Pieces: Structural Certification of General Agents](https://icml.cc/virtual/2026/poster/65633)** — 提出/整理 **A World in Pieces**，关注“Structural Certification of General Agents”。
- **[ABSINT-AI: Agentic Heap Abstractions for Abstract Interpretation](https://icml.cc/virtual/2026/poster/61550)** — 提出/整理 **ABSINT-AI**，面向“Abstract Interpretation”研究“Agentic Heap Abstractions”。
- **[Agentic Confidence Calibration](https://icml.cc/virtual/2026/poster/65705)** — 研究“Agentic Confidence Calibration”。
- **[AgentVocab: Structure-Aware Vocabulary Adaptation for Efficient LLM Agents](https://icml.cc/virtual/2026/poster/61748)** — 提出/整理 **AgentVocab**，面向“Efficient LLM Agents”研究“Structure-Aware Vocabulary Adaptation”。
- **[Backjump-on-Graph: Empowering LLMs with Reinforced Retrospective Exploration for Agentic KG Reasoning](https://icml.cc/virtual/2026/poster/61995)** — 提出 **Backjump-on-Graph**，将“Reinforced Retrospective Exploration for Agentic KG Reasoning”引入“Empowering LLMs”。
- **[Can LLM Agents Stick to the Script? Modeling Commitment in Interactive Narratives](https://icml.cc/virtual/2026/poster/64786)** — 以“Can LLM Agents Stick to the Script? Modeling Commitment in Interactive Narratives”为问题，考察 agent 的能力边界或失败模式。
- **[Characterizing Agents in Production](https://icml.cc/virtual/2026/poster/61834)** — 刻画“Agents”在“Production”中的实际行为。
- **[DeepHA: Scaling Action Chains Elicits Deep Hierarchical Agents](https://icml.cc/virtual/2026/poster/66241)** — 提出/整理 **DeepHA**，关注“Scaling Action Chains Elicits Deep Hierarchical Agents”。
- **[effGen: Enabling Small Language Models as Capable Autonomous Agents](https://icml.cc/virtual/2026/poster/63516)** — 提出/整理 **effGen**，关注“Enabling Small Language Models as Capable Autonomous Agents”。
- **[Estimating the Empowerment of Language Model Agents](https://icml.cc/virtual/2026/poster/61343)** — 研究“Estimating the Empowerment of Language Model Agents”。
- **[FormAct: Agentic Source Editing for Rich-Format Document Generation](https://icml.cc/virtual/2026/poster/61769)** — 提出/整理 **FormAct**，面向“Rich-Format Document Generation”研究“Agentic Source Editing”。
- **[FormalJudge: A Neuro-Symbolic Paradigm for Agentic Oversight](https://icml.cc/virtual/2026/poster/61086)** — 提出/整理 **FormalJudge**，面向“Agentic Oversight”研究“Neuro-Symbolic Paradigm”。
- **[GRASP: Graph Reasoning via Agentic Solving and Probing of LLMs](https://icml.cc/virtual/2026/poster/61718)** — 提出 **GRASP**，用“Agentic Solving and Probing of LLMs”来“Graph Reasoning”。
- **[Guideline-Grounded Evidence Accumulation for High-Stakes Agent Verification](https://icml.cc/virtual/2026/poster/65243)** — 研究“Guideline-Grounded Evidence Accumulation”，场景是面向“High-Stakes Agent Verification”。
- **[Helpful to a Fault: Measuring Illicit Assistance in Multi-Turn, Multilingual LLM Agents](https://icml.cc/virtual/2026/poster/61155)** — 提出/整理 **Helpful to a Fault**，考察“Measuring Illicit Assistance”在“Multi-Turn, Multilingual LLM Agents”中的表现。
- **[MarketSim: Simulating Stock Markets with Large-Scale Generative Agents](https://icml.cc/virtual/2026/poster/65297)** — 提出 **MarketSim**，将“Large-Scale Generative Agents”引入“Simulating Stock Markets”。
- **[MARS: Modular Agent with Reflective Search for Automated AI Research](https://icml.cc/virtual/2026/poster/61408)** — 提出 **MARS**，将“Reflective Search for Automated AI Research”引入“Modular Agent”。
- **[Numina-Lean-Agent: An Open and General Agentic Reasoning System for Formal Mathematics](https://icml.cc/virtual/2026/poster/66755)** — 提出/整理 **Numina-Lean-Agent**，面向“Formal Mathematics”研究“Open and General Agentic Reasoning System”。
- **[OpenHA: A Series of Open-Source Hierarchical Agentic Models in Minecraft](https://icml.cc/virtual/2026/poster/66679)** — 提出/整理 **OpenHA**，考察“Series of Open-Source Hierarchical Agentic Models”在“Minecraft”中的表现。
- **[Opt-Miner: Empowering Information-Seeking Agent with Tree-Guided Data Synthesis for Optimization Modeling](https://icml.cc/virtual/2026/poster/65154)** — 提出 **Opt-Miner**，将“Tree-Guided Data Synthesis for Optimization Modeling”引入“Empowering Information-Seeking Agent”。
- **[PACE: Proactive Agent-Level Admission Control for Efficient Agentic Batch Inference](https://icml.cc/virtual/2026/poster/63743)** — 提出/整理 **PACE**，面向“Efficient Agentic Batch Inference”研究“Proactive Agent-Level Admission Control”。
- **[Position: Accountable Deployment of Agentic AI Demands Layered, System-Level Interpretability](https://icml.cc/virtual/2026/poster/67088)** — 提出/整理 **Position**，关注“Accountable Deployment of Agentic AI Demands Layered, System-Level Interpretability”。
- **[Position: Agentic AI Is a Foreseeable Pathway to AGI](https://icml.cc/virtual/2026/poster/67083)** — 提出/整理 **Position**，关注“Agentic AI Is a Foreseeable Pathway to AGI”。
- **[Position: Agentic AI systems should be making Bayes-consistent decisions](https://icml.cc/virtual/2026/poster/67041)** — 提出/整理 **Position**，关注“Agentic AI systems should be making Bayes-consistent decisions”。
- **[Position: Agentic Systems Should be General](https://icml.cc/virtual/2026/poster/67137)** — 提出/整理 **Position**，关注“Agentic Systems Should be General”。
- **[Position: Assistive Agents Need Accessibility Alignment](https://icml.cc/virtual/2026/poster/67129)** — 提出/整理 **Position**，关注“Assistive Agents Need Accessibility Alignment”。
- **[Position: Beyond Prediction: Toward Verifiable Physiological Waveform Reasoning with Foundation Models and Agentic LLMs](https://icml.cc/virtual/2026/poster/67119)** — 提出 **Position**，将“Foundation Models and Agentic LLMs”引入“Beyond Prediction: Toward Verifiable Physiological Waveform Reasoning”。
- **[Position: Collaborative Agentic AI Needs Interoperability Across Ecosystems](https://icml.cc/virtual/2026/poster/67223)** — 提出/整理 **Position**，关注“Collaborative Agentic AI Needs Interoperability Across Ecosystems”。
- **[Position: Digital Agents Require Unified Agent-Native Environments](https://icml.cc/virtual/2026/poster/67134)** — 提出/整理 **Position**，关注“Digital Agents Require Unified Agent-Native Environments”。
- **[Position: LLM Agents Are the Antidote to Walled Gardens](https://icml.cc/virtual/2026/poster/67081)** — 提出/整理 **Position**，关注“LLM Agents Are the Antidote to Walled Gardens”。
- **[Position: Preregister Experiments with AI Agents](https://icml.cc/virtual/2026/poster/67108)** — 提出 **Position**，将“AI Agents”引入“Preregister Experiments”。
- **[Position: World Models as an Intermediary between Agents and the Real World](https://icml.cc/virtual/2026/poster/67241)** — 提出/整理 **Position**，关注“World Models as an Intermediary between Agents and the Real World”。
- **[PragLocker: Protecting Agent Intellectual Property in Untrusted Deployments via Non-Portable Prompts](https://icml.cc/virtual/2026/poster/64248)** — 提出 **PragLocker**，用“Non-Portable Prompts”来保护“Agent Intellectual Property in Untrusted Deployments”。
- **[Probabilistic Modeling of Latent Agentic Substructures in Deep Neural Networks](https://icml.cc/virtual/2026/poster/61223)** — 研究“Probabilistic Modeling of Latent Agentic Substructures”，场景是在“Deep Neural Networks”中。
- **[Pushing Forward Pareto Frontiers of Proactive Agents with Behavioral Agentic Optimization](https://icml.cc/virtual/2026/poster/61493)** — 研究“Pushing Forward Pareto Frontiers of Proactive Agents”，并引入“Behavioral Agentic Optimization”。
- **[Scaling Small Agents Through Strategy Auctions](https://icml.cc/virtual/2026/poster/62642)** — 研究“Scaling Small Agents”，核心机制是“Strategy Auctions”。
- **[Scaling the Scaling Logic: Agentic Meta-Synthesis of Logic Reasoning](https://icml.cc/virtual/2026/poster/66221)** — 提出/整理 **Scaling the Scaling Logic**，关注“Agentic Meta-Synthesis of Logic Reasoning”。
- **[Think Fast and Slow: Step-Level Cognitive Depth Adaptation for LLM Agents](https://icml.cc/virtual/2026/poster/63105)** — 提出/整理 **Think Fast and Slow**，面向“LLM Agents”研究“Step-Level Cognitive Depth Adaptation”。
- **[When AI Agents Compete for Jobs: Strategic Capabilities and Economic Dynamics of AI Labour Markets](https://icml.cc/virtual/2026/poster/66152)** — 提出/整理 **When AI Agents Compete for Jobs**，关注“Strategic Capabilities and Economic Dynamics of AI Labour Markets”。

<a id="scientific-domain-agents"></a>
### 🔬 6. 科学、行业与垂直领域 agent / Scientific & Domain Agents (30)

将 agent 落到数据科学、金融、医疗、生物安全、CAD/电路/机器人、回溯合成、企业运维等任务。

- **[Agentic Framework for Epidemiological Modeling](https://icml.cc/virtual/2026/poster/60990)** — 面向垂直场景提出“Agentic Framework”，场景是面向“Epidemiological Modeling”。
- **[AutoMat: Physics-Guided Agentic Reasoning for Solving Ill-Posed Inverse Microscopy Problems](https://icml.cc/virtual/2026/poster/63827)** — 提出/整理 **AutoMat**，面向“Solving Ill-Posed Inverse Microscopy Problems”研究“Physics-Guided Agentic Reasoning”。
- **[AutoSizer: Automatic Sizing of Analog and Mixed-Signal Circuits via Large Language Model (LLM) Agents](https://icml.cc/virtual/2026/poster/66562)** — 提出 **AutoSizer**，用“Large Language Model (LLM) Agents”来“Automatic Sizing of Analog and Mixed-Signal Circuits”。
- **[CocoRNA: Collective RNA Design with Cooperative Multi-agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/65353)** — 提出 **CocoRNA**，将“Cooperative Multi-agent Reinforcement Learning”引入“Collective RNA Design”。
- **[Constitutional Black-Box Monitoring for Scheming in LLM Agents](https://icml.cc/virtual/2026/poster/65104)** — 面向垂直场景提出“Constitutional Black-Box Monitoring”，场景是面向“Scheming in LLM Agents”。
- **[Cycle-of-Science: Reliable Reasoning through Counterfactual Verification for Agent Decision Making](https://icml.cc/virtual/2026/poster/64408)** — 提出 **Cycle-of-Science**，用“Counterfactual Verification for Agent Decision Making”来“Reliable Reasoning”。
- **[Debate2Create: Robot Co-design via Multi-Agent LLM Debate](https://icml.cc/virtual/2026/poster/66635)** — 提出 **Debate2Create**，用“Multi-Agent LLM Debate”来“Robot Co-design”。
- **[DeepAnalyze: Agentic Large Language Models for Autonomous Data Science](https://icml.cc/virtual/2026/poster/61106)** — 提出/整理 **DeepAnalyze**，面向“Autonomous Data Science”研究“Agentic Large Language Models”。
- **[EngiAgent: Fully Connected Coordination of LLM Agents for Solving Open-ended Engineering Problems with Feasible Solutions](https://icml.cc/virtual/2026/poster/66645)** — 提出 **EngiAgent**，将“Feasible Solutions”引入“Fully Connected Coordination of LLM Agents for Solving Open-ended Engineering Problems”。
- **[From Conflict to Consensus: Boosting Medical Reasoning via Multi-Round Agentic RAG](https://icml.cc/virtual/2026/poster/63972)** — 提出 **From Conflict to Consensus**，用“Multi-Round Agentic RAG”来“Boosting Medical Reasoning”。
- **[LAGEA: Language Guided Embodied Agents for Robotic Manipulation](https://icml.cc/virtual/2026/poster/60801)** — 提出/整理 **LAGEA**，面向“Robotic Manipulation”研究“Language Guided Embodied Agents”。
- **[Learning Human-Robot Collaboration via Heterogeneous-Agent Lyapunov Policy Optimization](https://icml.cc/virtual/2026/poster/61049)** — 面向垂直场景提出“Learning Human-Robot Collaboration”，核心机制是“Heterogeneous-Agent Lyapunov Policy Optimization”。
- **[LiveFigure: Generating Editable Scientific Illustration with VLM Agents](https://icml.cc/virtual/2026/poster/62974)** — 提出 **LiveFigure**，将“VLM Agents”引入“Generating Editable Scientific Illustration”。
- **[Meta Context Engineering via Agentic Skill Evolution](https://icml.cc/virtual/2026/poster/64296)** — 面向垂直场景提出“Meta Context Engineering”，核心机制是“Agentic Skill Evolution”。
- **[ML-Agent: Reinforcing LLM Agents for Autonomous Machine Learning Engineering](https://icml.cc/virtual/2026/poster/62020)** — 提出/整理 **ML-Agent**，面向“Autonomous Machine Learning Engineering”研究“Reinforcing LLM Agents”。
- **[Ophiuchus: Incentivizing Tool-augmented ''Think with Images'' for Joint Medical Segmentation, Understanding and Reasoning](https://icml.cc/virtual/2026/poster/62829)** — 提出 **Ophiuchus**，将“Images'' for Joint Medical Segmentation, Understanding and Reasoning”引入“Incentivizing Tool-augmented ''Think”。
- **[PDAgent: An LLM-Driven Autonomous Agent Framework Towards *In Silico* Protein Design via Directed Mutation](https://icml.cc/virtual/2026/poster/63768)** — 提出 **PDAgent**，用“Directed Mutation”来“LLM-Driven Autonomous Agent Framework Towards *In Silico* Protein Design”。
- **[Position: Academic Conferences are Potentially Facing Denominator Gaming Caused by Fully Automated Scientific Agents](https://icml.cc/virtual/2026/poster/67236)** — 提出 **Position**，用“Fully Automated Scientific Agents”来“Academic Conferences are Potentially Facing Denominator Gaming Caused”。
- **[Position: Agent Should Invoke External Tools ONLY When Epistemically Necessary](https://icml.cc/virtual/2026/poster/67227)** — 提出/整理 **Position**，关注“Agent Should Invoke External Tools ONLY When Epistemically Necessary”。
- **[Position: The Age of AI Agents Demands A New Scientific Paradigm To Sustain Trustworthy Science](https://icml.cc/virtual/2026/poster/67156)** — 提出/整理 **Position**，关注“Age of AI Agents Demands A New Scientific Paradigm To Sustain Trustworthy Science”。
- **[Principled Zero-shot Ranking Agents with Tournament Graphs](https://icml.cc/virtual/2026/poster/62762)** — 面向垂直场景提出“Principled Zero-shot Ranking Agents”，并引入“Tournament Graphs”。
- **[Reinforcement Learning for Tool-Calling Agents in Fast Healthcare Interoperability Resources (FHIR)](https://icml.cc/virtual/2026/poster/65318)** — 面向垂直场景提出“Reinforcement Learning”，场景是面向“Tool-Calling Agents in Fast Healthcare Interoperability Resources (FHIR)”。
- **[RetrOrchestrator: A Multi-Step Retrosynthesis Agent Dynamically Orchestrating Single-Step Transition Models](https://icml.cc/virtual/2026/poster/61540)** — 提出/整理 **RetrOrchestrator**，关注“Multi-Step Retrosynthesis Agent Dynamically Orchestrating Single-Step Transition Models”。
- **[Small Agent Group is the Future of Digital Health](https://icml.cc/virtual/2026/poster/65768)** — 面向垂直场景提出“Small Agent Group is the Future of Digital Health”。
- **[SPADA: A Verifiable Test-Driven Agent for Controllable Parametric CAD Assembly Generation](https://icml.cc/virtual/2026/poster/62308)** — 提出/整理 **SPADA**，面向“Controllable Parametric CAD Assembly Generation”研究“Verifiable Test-Driven Agent”。
- **[Textual Stochastic Gradient Descent: Discrete Optimization of External Memory for Reasoning Language Agents](https://icml.cc/virtual/2026/poster/60510)** — 提出/整理 **Textual Stochastic Gradient Descent**，面向“Reasoning Language Agents”研究“Discrete Optimization of External Memory”。
- **[Threat2Traffic: Multi-Agent Environment Synthesis for Malware Traffic Generation from Threat Intelligence](https://icml.cc/virtual/2026/poster/64510)** — 提出/整理 **Threat2Traffic**，面向“Malware Traffic Generation from Threat Intelligence”研究“Multi-Agent Environment Synthesis”。
- **[Toward Ultra-Long-Horizon Agentic Science: Cognitive Accumulation for Autonomous Machine Learning Engineering](https://icml.cc/virtual/2026/poster/66663)** — 提出/整理 **Toward Ultra-Long-Horizon Agentic Science**，面向“Autonomous Machine Learning Engineering”研究“Cognitive Accumulation”。
- **[Towards a Science of AI Agent Reliability](https://icml.cc/virtual/2026/poster/66364)** — 面向垂直场景提出“Towards a Science of AI Agent Reliability”。
- **[Why Specialist Models Still Matter: A Heterogeneous Multi-Agent Paradigm for Medical Artificial Intelligence](https://icml.cc/virtual/2026/poster/60481)** — 提出/整理 **Why Specialist Models Still Matter**，面向“Medical Artificial Intelligence”研究“Heterogeneous Multi-Agent Paradigm”。

<a id="memory-context-long-horizon"></a>
### 💾 7. 记忆、上下文与长程任务 / Memory, Context & Long-Horizon Tasks (29)

处理长程 agent 的状态管理瓶颈，包括轨迹压缩、图记忆、上下文折叠、长期会话和跨 session 记忆。

- **[$R^3$DAO: Reactive Recovery and Reconstruction for Long-horizon Data Agent Orchestration](https://icml.cc/virtual/2026/poster/64678)** — 提出/整理 **$R^3$DAO**，面向“Long-horizon Data Agent Orchestration”研究“Reactive Recovery and Reconstruction”。
- **[ACON: Optimizing Context Compression for Long-horizon LLM Agents](https://icml.cc/virtual/2026/poster/66270)** — 提出/整理 **ACON**，面向“Long-horizon LLM Agents”研究“Optimizing Context Compression”。
- **[AdaMEM: Test-Time Adaptive Memory for Language Agents](https://icml.cc/virtual/2026/poster/63989)** — 提出/整理 **AdaMEM**，面向“Language Agents”研究“Test-Time Adaptive Memory”。
- **[Beyond Trajectory-Level Attribution: Graph-Based Credit Assignment for Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/60543)** — 提出/整理 **Beyond Trajectory-Level Attribution**，面向“Agentic Reinforcement Learning”研究“Graph-Based Credit Assignment”。
- **[De-Linearizing Agent Traces: Bayesian Inference of Latent Partial Orders for Efficient Execution](https://icml.cc/virtual/2026/poster/63737)** — 提出/整理 **De-Linearizing Agent Traces**，面向“Efficient Execution”研究“Bayesian Inference of Latent Partial Orders”。
- **[Experience-Evolving Multi-Turn Tool-Use Agent with Hybrid Episodic–Procedural Memory](https://icml.cc/virtual/2026/poster/64271)** — 提出“Experience-Evolving Multi-Turn Tool-Use Agent”，并引入“Hybrid Episodic–Procedural Memory”。
- **[ExpWeaver: LLM Agents Learn from Experience via Latent RAG](https://icml.cc/virtual/2026/poster/66387)** — 提出 **ExpWeaver**，用“Latent RAG”来“LLM Agents Learn from Experience”。
- **[From Outcomes to Actions: Leveraging Hindsight for Long-Horizon Language Agent Training](https://icml.cc/virtual/2026/poster/62250)** — 提出/整理 **From Outcomes to Actions**，面向“Long-Horizon Language Agent Training”研究“Leveraging Hindsight”。
- **[From Player to Master: Enhancing Test-Time Learning of LLM Agents via Reinforcement Learning over Memory](https://icml.cc/virtual/2026/poster/62463)** — 提出 **From Player to Master**，用“Reinforcement Learning over Memory”来增强“Test-Time Learning of LLM Agents”。
- **[JADE: Bridging the Strategic-Operational Gap in Dynamic Agentic RAG](https://icml.cc/virtual/2026/poster/64731)** — 提出/整理 **JADE**，考察“Bridging the Strategic-Operational Gap”在“Dynamic Agentic RAG”中的表现。
- **[Learning Query-Aware Budget-Tier Routing for Runtime Agent Memory](https://icml.cc/virtual/2026/poster/66266)** — 提出“Learning Query-Aware Budget-Tier Routing”，场景是面向“Runtime Agent Memory”。
- **[Learning to Share: Selective Memory for Efficient Parallel Agentic Systems](https://icml.cc/virtual/2026/poster/62890)** — 提出/整理 **Learning to Share**，面向“Efficient Parallel Agentic Systems”研究“Selective Memory”。
- **[Lifting Traces to Logic: Programmatic Skill Induction with Neuro-Symbolic Learning for Long-Horizon Agentic Tasks](https://icml.cc/virtual/2026/poster/65500)** — 提出 **Lifting Traces to Logic**，将“Neuro-Symbolic Learning for Long-Horizon Agentic Tasks”引入“Programmatic Skill Induction”。
- **[LRAgent: Efficient KV Cache Sharing for Multi-LoRA LLM Agents](https://icml.cc/virtual/2026/poster/61572)** — 提出/整理 **LRAgent**，面向“Multi-LoRA LLM Agents”研究“Efficient KV Cache Sharing”。
- **[Mem-T: Densifying Rewards for Long-Horizon Memory Agents](https://icml.cc/virtual/2026/poster/65925)** — 提出/整理 **Mem-T**，面向“Long-Horizon Memory Agents”研究“Densifying Rewards”。
- **[MemEvolve: Meta-Evolution of Agent Memory Systems](https://icml.cc/virtual/2026/poster/61379)** — 提出/整理 **MemEvolve**，关注“Meta-Evolution of Agent Memory Systems”。
- **[Memory is Reconstructed, Not Retrieved: Graph Memory for LLM Agents](https://icml.cc/virtual/2026/poster/60697)** — 提出/整理 **Memory is Reconstructed, Not Retrieved**，面向“LLM Agents”研究“Graph Memory”。
- **[Milestone-Guided Policy Learning for Long-Horizon Language Agents](https://icml.cc/virtual/2026/poster/65128)** — 提出“Milestone-Guided Policy Learning”，场景是面向“Long-Horizon Language Agents”。
- **[ParamMem: Augmenting Language Agents with Parametric Reflective Memory](https://icml.cc/virtual/2026/poster/61133)** — 提出 **ParamMem**，将“Parametric Reflective Memory”引入“Augmenting Language Agents”。
- **[PlugMem: A Task-Agnostic Plugin Memory Module for LLM Agents](https://icml.cc/virtual/2026/poster/64446)** — 提出/整理 **PlugMem**，面向“LLM Agents”研究“Task-Agnostic Plugin Memory Module”。
- **[Position: Modular Memory is the Key to Continual Learning Agents](https://icml.cc/virtual/2026/poster/67101)** — 提出/整理 **Position**，关注“Modular Memory is the Key to Continual Learning Agents”。
- **[ProcMEM: Learning Reusable Procedural Memory from Experience via Non-Parametric PPO for LLM Agents](https://icml.cc/virtual/2026/poster/65830)** — 提出 **ProcMEM**，用“Non-Parametric PPO for LLM Agents”来学习“Reusable Procedural Memory from Experience”。
- **[RE-TRAC: REcursive TRAjectory Compression for Deep Search Agents](https://icml.cc/virtual/2026/poster/60790)** — 提出/整理 **RE-TRAC**，面向“Deep Search Agents”研究“REcursive TRAjectory Compression”。
- **[RGMem: Renormalization Group–inspired Memory Evolution for Language Agents](https://icml.cc/virtual/2026/poster/65195)** — 提出/整理 **RGMem**，面向“Language Agents”研究“Renormalization Group–inspired Memory Evolution”。
- **[Scaling Long-Horizon Agent via Context Folding](https://icml.cc/virtual/2026/poster/61950)** — 提出“Scaling Long-Horizon Agent”，核心机制是“Context Folding”。
- **[SimpleMem: Efficient Lifelong Memory for LLM Agents](https://icml.cc/virtual/2026/poster/61640)** — 提出/整理 **SimpleMem**，面向“LLM Agents”研究“Efficient Lifelong Memory”。
- **[Training-Free Hierarchical Working Memory for Small Language Model Agents](https://icml.cc/virtual/2026/poster/63532)** — 提出“Training-Free Hierarchical Working Memory”，场景是面向“Small Language Model Agents”。
- **[Tvcache: A Tool-Value Cache for Post-Training LLM Agents](https://icml.cc/virtual/2026/poster/61148)** — 提出/整理 **Tvcache**，面向“Post-Training LLM Agents”研究“Tool-Value Cache”。
- **[What Do Agents Learn from Trajectory-SFT: Semantics or Interfaces?](https://icml.cc/virtual/2026/poster/61062)** — 提出/整理 **What Do Agents Learn from Trajectory-SFT**，关注“Semantics or Interfaces?”。

<a id="coding-swe-theorem-proving"></a>
### 💻 8. 代码、软件工程与定理证明 / Coding, SWE & Theorem Proving (27)

面向 repo 级软件任务、CUDA/Triton/kernel、全栈开发、漏洞发现、容器环境和自动定理证明。

- **[A Minimal Agent for Automated Theorem Proving](https://icml.cc/virtual/2026/poster/64174)** — 提出/评测“Minimal Agent”，场景是面向“Automated Theorem Proving”。
- **[ADEPT: RL-Aligned Agentic Decoding of Emotion via Evidence Probing Tools — From Consensus Learning to Ambiguity-Driven Emotion Reasoning](https://icml.cc/virtual/2026/poster/61830)** — 提出 **ADEPT**，用“Evidence Probing Tools — From Consensus Learning to Ambiguity-Driven Emotion Reasoning”来“RL-Aligned Agentic Decoding of Emotion”。
- **[AgentConductor: Topology Evolution for Multi-Agent Competition-Level Code Generation](https://icml.cc/virtual/2026/poster/66333)** — 提出/整理 **AgentConductor**，面向“Multi-Agent Competition-Level Code Generation”研究“Topology Evolution”。
- **[Agora: Toward Autonomous Bug Detection in Production-Level Consensus Protocols with LLM Agents](https://icml.cc/virtual/2026/poster/64937)** — 提出 **Agora**，将“LLM Agents”引入迈向“Autonomous Bug Detection in Production-Level Consensus Protocols”。
- **[daVinci-Dev: Agent-native Mid-training for Software Engineering](https://icml.cc/virtual/2026/poster/63099)** — 提出/整理 **daVinci-Dev**，面向“Software Engineering”研究“Agent-native Mid-training”。
- **[DOCKSMITH: Scaling Reliable Coding Environments via an Agentic Docker Builder](https://icml.cc/virtual/2026/poster/61127)** — 提出 **DOCKSMITH**，用“Agentic Docker Builder”来扩展“Reliable Coding Environments”。
- **[EGG: An Expert-Guided Agent Framework for Kernel Generation](https://icml.cc/virtual/2026/poster/65929)** — 提出 **EGG**，作为“Kernel Generation”的框架。
- **[FullStack-Agent: Enhancing Agentic Full-Stack Web Coding via Development-Oriented Testing and Repository Back-Translation](https://icml.cc/virtual/2026/poster/60686)** — 提出 **FullStack-Agent**，用“Development-Oriented Testing and Repository Back-Translation”来增强“Agentic Full-Stack Web Coding”。
- **[How can we assess human-agent interactions? Case studies in software agent design](https://icml.cc/virtual/2026/poster/64319)** — 以“How can we assess human-agent interactions? Case studies in software agent design”为问题，考察 agent 的能力边界或失败模式。
- **[Just Ask: Curious Code Agents Reveal System Prompts in Frontier LLMs](https://icml.cc/virtual/2026/poster/61428)** — 提出/整理 **Just Ask**，考察“Curious Code Agents Reveal System Prompts”在“Frontier LLMs”中的表现。
- **[Large-Scale Terminal Agentic Trajectory Generation from Dockerized Environments](https://icml.cc/virtual/2026/poster/64240)** — 提出/评测“Large-Scale Terminal Agentic Trajectory Generation from Dockerized Environments”。
- **[MemDecoder: Enhancing Test-Time Compute for LLM Agents via Reinforced Memory Decoding](https://icml.cc/virtual/2026/poster/65523)** — 提出 **MemDecoder**，用“Reinforced Memory Decoding”来增强“Test-Time Compute for LLM Agents”。
- **[MulFCoder: Framework-conditioned Multi-agent for MLLM-based Multi-framework Front-end Code Generation](https://icml.cc/virtual/2026/poster/60693)** — 提出/整理 **MulFCoder**，面向“MLLM-based Multi-framework Front-end Code Generation”研究“Framework-conditioned Multi-agent”。
- **[NEMO: Execution-Aware Optimization Modeling via Autonomous Coding Agents](https://icml.cc/virtual/2026/poster/66684)** — 提出 **NEMO**，用“Autonomous Coding Agents”来“Execution-Aware Optimization Modeling”。
- **[One Tool Is Enough: Reinforcement Learning of LLM Agents for Repository-Level Code Navigation](https://icml.cc/virtual/2026/poster/63517)** — 提出/整理 **One Tool Is Enough**，面向“Repository-Level Code Navigation”研究“Reinforcement Learning of LLM Agents”。
- **[OpenSage: Self-programming Agent Generation Engine](https://icml.cc/virtual/2026/poster/66121)** — 提出/整理 **OpenSage**，关注“Self-programming Agent Generation Engine”。
- **[ParEVO: Synthesizing Code for Irregular Data: High-Performance Parallelism through Agentic Evolution](https://icml.cc/virtual/2026/poster/61756)** — 提出 **ParEVO**，用“Agentic Evolution”来“Synthesizing Code for Irregular Data: High-Performance Parallelism”。
- **[Scaling Agentic Verifier for Competitive Coding](https://icml.cc/virtual/2026/poster/65948)** — 提出/评测“Scaling Agentic Verifier”，场景是面向“Competitive Coding”。
- **[SERA: Soft-Verified Efficient Repository Agents](https://icml.cc/virtual/2026/poster/65153)** — 提出/整理 **SERA**，关注“Soft-Verified Efficient Repository Agents”。
- **[StitchCUDA: An Automated Multi-Agents End-to-End GPU Programing Framework with Rubric-based Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/64924)** — 提出 **StitchCUDA**，将“Rubric-based Agentic Reinforcement Learning”引入“Automated Multi-Agents End-to-End GPU Programing Framework”。
- **[Structurally Aligned Subtask-Level Memory for Software Engineering Agents](https://icml.cc/virtual/2026/poster/66605)** — 提出/评测“Structurally Aligned Subtask-Level Memory”，场景是面向“Software Engineering Agents”。
- **[SWE-MiniSandbox: Container-Free Reinforcement Learning for Building Software Engineering Agents](https://icml.cc/virtual/2026/poster/61850)** — 提出/整理 **SWE-MiniSandbox**，面向“Building Software Engineering Agents”研究“Container-Free Reinforcement Learning”。
- **[ThunderAgent: A Fast, Simple, and Program-Aware Agentic Inference System](https://icml.cc/virtual/2026/poster/62040)** — 提出/整理 **ThunderAgent**，关注“Fast, Simple, and Program-Aware Agentic Inference System”。
- **[TOM-SWE: User Mental Modeling For Software Engineering Agents](https://icml.cc/virtual/2026/poster/65025)** — 提出/整理 **TOM-SWE**，面向“Software Engineering Agents”研究“User Mental Modeling”。
- **[Toward Training Superintelligent Software Agents through Self-Play SWE-RL](https://icml.cc/virtual/2026/poster/66747)** — 提出/评测“Toward Training Superintelligent Software Agents”，核心机制是“Self-Play SWE-RL”。
- **[Towards Feedback-to-Plan Decisions for Self-Evolving LLM Agents in CUDA Kernel Generation](https://icml.cc/virtual/2026/poster/61256)** — 提出/评测“Towards Feedback-to-Plan Decisions”，场景是面向“Self-Evolving LLM Agents in CUDA Kernel Generation”。
- **[Why Agentic Theorem Prover Works: A Statistical Provability Theory of Mathematical Reasoning Models](https://icml.cc/virtual/2026/poster/62379)** — 提出/整理 **Why Agentic Theorem Prover Works**，关注“Statistical Provability Theory of Mathematical Reasoning Models”。

<a id="gui-web-computer-use"></a>
### 🖥️ 9. GUI、Web 与 computer-use agent / GUI, Web & Computer-Use (13)

围绕网页、桌面、移动 GUI 和 computer-use，研究环境生成、轨迹预训练、动作纠错、鲁棒性和安全。

- **[Agent JIT Compilation for Latency-Optimizing Computer-Use Agent Planning and Scheduling](https://icml.cc/virtual/2026/poster/66062)** — 提出/评测“Agent JIT Compilation”，场景是面向“Latency-Optimizing Computer-Use Agent Planning and Scheduling”。
- **[CAPTCHA Solving for Native GUI Agents: Automated Reasoning-Action Data Generation and Self-Corrective Training](https://icml.cc/virtual/2026/poster/65034)** — 提出/整理 **CAPTCHA Solving for Native GUI Agents**，关注“Automated Reasoning-Action Data Generation and Self-Corrective Training”。
- **[Continual GUI Agents](https://icml.cc/virtual/2026/poster/66053)** — 提出/评测“Continual GUI Agents”。
- **[Darwinian Memory: A Training-Free Self-Regulating Memory System for GUI Agent Evolution](https://icml.cc/virtual/2026/poster/61134)** — 提出/整理 **Darwinian Memory**，面向“GUI Agent Evolution”研究“Training-Free Self-Regulating Memory System”。
- **[Executable Agentic Memory for GUI Agent](https://icml.cc/virtual/2026/poster/65931)** — 提出/评测“Executable Agentic Memory”，场景是面向“GUI Agent”。
- **[Faithful Mobile GUI Agents with Guided Advantage Estimator](https://icml.cc/virtual/2026/poster/63413)** — 提出/评测“Faithful Mobile GUI Agents”，并引入“Guided Advantage Estimator”。
- **[Next-Gen CAPTCHAs: Leveraging the Cognitive Gap for Scalable and Diverse GUI-Agent Defense](https://icml.cc/virtual/2026/poster/60816)** — 提出/整理 **Next-Gen CAPTCHAs**，面向“Scalable and Diverse GUI-Agent Defense”研究“Leveraging the Cognitive Gap”。
- **[Position: Web Agents Should Use Typed Actions Instead of Click-Based Browsing](https://icml.cc/virtual/2026/poster/67155)** — 提出/整理 **Position**，关注“Web Agents Should Use Typed Actions Instead of Click-Based Browsing”。
- **[SE-GA: Memory-Augmented Self-Evolution for GUI Agents](https://icml.cc/virtual/2026/poster/65853)** — 提出/整理 **SE-GA**，面向“GUI Agents”研究“Memory-Augmented Self-Evolution”。
- **[Video2GUI: Synthesizing Large-Scale Interaction Trajectories for Generalized GUI Agent Pretraining](https://icml.cc/virtual/2026/poster/62028)** — 提出/整理 **Video2GUI**，面向“Generalized GUI Agent Pretraining”研究“Synthesizing Large-Scale Interaction Trajectories”。
- **[Weasel: Out-of-Domain Generalization for Web Agents via Importance-Diversity Data Selection](https://icml.cc/virtual/2026/poster/65342)** — 提出 **Weasel**，用“Importance-Diversity Data Selection”来“Out-of-Domain Generalization for Web Agents”。
- **[WebWorld: A Large-Scale World Model for Web Agent Training](https://icml.cc/virtual/2026/poster/65352)** — 提出/整理 **WebWorld**，面向“Web Agent Training”研究“Large-Scale World Model”。
- **[When Actions Go Off-Task: Detecting and Correcting Misaligned Actions in Computer-Use Agents](https://icml.cc/virtual/2026/poster/64196)** — 提出/整理 **When Actions Go Off-Task**，考察检测并纠正“Misaligned Actions”在“Computer-Use Agents”中的表现。

<a id="multimodal-embodied-interactive"></a>
### 🎥 10. 多模态、具身与交互 / Multimodal, Embodied & Interactive Agents (11)

将 agentic reasoning 接入 VLM/VLA、视频、音频、导航、空间推理、主动感知和具身操作。

- **[Active Exploring like a Pigeon: Reinforcing Spatial Reasoning via Agentic Vision-Language Models](https://icml.cc/virtual/2026/poster/61450)** — 提出 **Active Exploring like a Pigeon**，用“Agentic Vision-Language Models”来“Reinforcing Spatial Reasoning”。
- **[DR-MMSearchAgent: Deepening Reasoning in Multimodal Search Agents](https://icml.cc/virtual/2026/poster/66547)** — 提出/整理 **DR-MMSearchAgent**，考察“Deepening Reasoning”在“Multimodal Search Agents”中的表现。
- **[Failure is Feedback: History-Aware Backtracking for Agentic Traversal in Multimodal Graphs](https://icml.cc/virtual/2026/poster/60560)** — 提出/整理 **Failure is Feedback**，考察“History-Aware Backtracking for Agentic Traversal”在“Multimodal Graphs”中的表现。
- **[Hierarchical Procedural Meta-Reasoning for Generalizable Multimodal Agents](https://icml.cc/virtual/2026/poster/60959)** — 研究“Hierarchical Procedural Meta-Reasoning”，场景是面向“Generalizable Multimodal Agents”。
- **[MM-DeepResearch: A Simple and Effective Multimodal Agentic Search Baseline](https://icml.cc/virtual/2026/poster/63393)** — 提出/整理 **MM-DeepResearch**，关注“Simple and Effective Multimodal Agentic Search Baseline”。
- **[See, Act, Adapt: Active Perception for Unsupervised Cross-Domain Visual Adaptation via Personalized VLM-Guided Agent](https://icml.cc/virtual/2026/poster/65692)** — 提出 **See, Act, Adapt**，用“Personalized VLM-Guided Agent”来“Active Perception for Unsupervised Cross-Domain Visual Adaptation”。
- **[SP-Mind: An Autonomous Reasoning Agent for Spatial Proteomics Analysis](https://icml.cc/virtual/2026/poster/63717)** — 提出/整理 **SP-Mind**，面向“Spatial Proteomics Analysis”研究“Autonomous Reasoning Agent”。
- **[Strategic Navigation or Stochastic Search? How Agents and Humans Reason Over Document Collections](https://icml.cc/virtual/2026/poster/62732)** — 以“Strategic Navigation or Stochastic Search? How Agents and Humans Reason Over Document Collections”为问题，考察 agent 的能力边界或失败模式。
- **[Text Before Vision: Staged Knowledge Injection Matters for Agentic RLVR in Ultra-High-Resolution Remote Sensing Understanding](https://icml.cc/virtual/2026/poster/66614)** — 提出/整理 **Text Before Vision**，考察“Staged Knowledge Injection Matters for Agentic RLVR”在“Ultra-High-Resolution Remote Sensing Understanding”中的表现。
- **[VIRUS: Injecting Persistent Cognitive Pathogens into Stateful Zero-Shot Object Navigation Agents](https://icml.cc/virtual/2026/poster/66293)** — 提出/整理 **VIRUS**，关注“Injecting Persistent Cognitive Pathogens into Stateful Zero-Shot Object Navigation Agents”。
- **[What You Think is What You See: Driving Exploration in VLM Agents via Visual-Linguistic Curiosity](https://icml.cc/virtual/2026/poster/60509)** — 提出 **What You Think is What You See**，用“Visual-Linguistic Curiosity”来“Driving Exploration in VLM Agents”。

<a id="planning-architecture-orchestration"></a>
### 🏗️ 11. 规划、架构与编排 / Planning, Architecture & Orchestration (11)

关注 agent 工作流、子 agent 创建、拓扑演化、协议选择、规划/执行解耦和系统编排。

- **[Agentic Model Predictive Questioning Control in Visual Design](https://icml.cc/virtual/2026/poster/62292)** — 设计“Agentic Model Predictive Questioning Control”，场景是在“Visual Design”中。
- **[Agentic Proposing: Enhancing Large language Model Reasoning via Compositional Skill Synthesis](https://icml.cc/virtual/2026/poster/62973)** — 提出 **Agentic Proposing**，用“Compositional Skill Synthesis”来增强“Large language Model Reasoning”。
- **[AgentXRay: White-Boxing Agentic Systems via Workflow Reconstruction](https://icml.cc/virtual/2026/poster/65356)** — 提出 **AgentXRay**，用“Workflow Reconstruction”来“White-Boxing Agentic Systems”。
- **[AOrchestra: Automating Sub-Agent Creation for Agentic Orchestration](https://icml.cc/virtual/2026/poster/65930)** — 提出/整理 **AOrchestra**，面向“Agentic Orchestration”研究自动化“Sub-Agent Creation”。
- **[EvoMAS: Heuristics in the Loop—Evolving Smarter Agentic Workflows](https://icml.cc/virtual/2026/poster/62843)** — 提出/整理 **EvoMAS**，考察“Heuristics”在“Loop—Evolving Smarter Agentic Workflows”中的表现。
- **[FlowMAP: Flow Matching for Generalizable Agent Planning](https://icml.cc/virtual/2026/poster/63407)** — 提出/整理 **FlowMAP**，面向“Generalizable Agent Planning”研究“Flow Matching”。
- **[GraphFlow: A Graph-Based Workflow Management for Efficient LLM-Agent Serving](https://icml.cc/virtual/2026/poster/66432)** — 提出/整理 **GraphFlow**，面向“Efficient LLM-Agent Serving”研究“Graph-Based Workflow Management”。
- **[Hermes: An Evidence-Driven Agentic Framework for Trustworthy and Explainable AI-Generated Video Detection](https://icml.cc/virtual/2026/poster/61817)** — 提出 **Hermes**，作为“Trustworthy and Explainable AI-Generated Video Detection”的框架。
- **[Probing the Knowledge Boundary: An Interactive Agentic Framework for Deep Knowledge Extraction](https://icml.cc/virtual/2026/poster/62443)** — 提出 **Probing the Knowledge Boundary**，作为“Deep Knowledge Extraction”的框架。
- **[VideoSEAL: Separating Planning from Answer Authority for Agentic Long Video Understanding](https://icml.cc/virtual/2026/poster/64001)** — 提出/整理 **VideoSEAL**，面向“Agentic Long Video Understanding”研究“Separating Planning from Answer Authority”。
- **[When Replanning Becomes the Bottleneck: Budgeted Replanning for Embodied Agents](https://icml.cc/virtual/2026/poster/63603)** — 提出/整理 **When Replanning Becomes the Bottleneck**，面向“Embodied Agents”研究“Budgeted Replanning”。

<a id="conversation-assistant-interaction"></a>
### 💬 12. 对话、澄清与助理交互 / Conversation & Assistant Interaction (4)

研究对话 agent 的澄清提问、服务成本/效用平衡、全双工语音和任务型交互策略。

- **[Mitigating Conversational Inertia in Multi-Turn Agents](https://icml.cc/virtual/2026/poster/63848)** — 研究“Mitigating Conversational Inertia”，场景是在“Multi-Turn Agents”中。
- **[Reinforcing Real-world Service Agents: Balancing Utility and Cost in Task-oriented Dialogue](https://icml.cc/virtual/2026/poster/65380)** — 提出/整理 **Reinforcing Real-world Service Agents**，考察“Balancing Utility and Cost”在“Task-oriented Dialogue”中的表现。
- **[Teaching Agents to Ask Effective Clarification Questions](https://icml.cc/virtual/2026/poster/63224)** — 研究“Teaching Agents to Ask Effective Clarification Questions”。
- **[Uncertainty-Aware Clarification in LLM Agents with Information Gain](https://icml.cc/virtual/2026/poster/66065)** — 研究“Uncertainty-Aware Clarification in LLM Agents”，并引入“Information Gain”。

<a id="data-files"></a>
