# 🤖 ICML 2026 Agent-Related Papers

🌐 **Language:** English | [中文](./README.zh-CN.md)

> Unofficial reading list based on the ICML 2026 virtual site. It groups accepted posters whose titles explicitly mention agent / agentic / multi-agent / tool-use / computer-use / GUI/Web agent signals, and adds one-line navigation notes.

- 📌 **Source:** [ICML 2026 Papers](https://icml.cc/virtual/2026/papers.html)
- 📄 **Coverage:** 465 papers


## 🧭 Table Of Contents

- [✨ Highlights](#highlights)
- [🔎 Scope And Method](#scope-and-method)
- [🗂️ Taxonomy](#taxonomy)
- [📋 Full List](#full-list)
  - [📚 Benchmarks & Evaluation](#benchmarks-evaluation)
  - [🤝 Multi-Agent Systems & MARL](#multi-agent-systems-marl)
  - [🛠️ Tool Use, Training & RL](#tool-use-training-rl)
  - [🛡️ Safety, Security & Governance](#safety-security-governance)
  - [🧠 Theory, Behavior & Interpretability](#theory-behavior-interpretability)
  - [🔬 Scientific & Domain Agents](#scientific-domain-agents)
  - [💾 Memory, Context & Long-Horizon Tasks](#memory-context-long-horizon)
  - [💻 Coding, SWE & Theorem Proving](#coding-swe-theorem-proving)
  - [🖥️ GUI, Web & Computer-Use](#gui-web-computer-use)
  - [🎥 Multimodal, Embodied & Interactive Agents](#multimodal-embodied-interactive)
  - [🏗️ Planning, Architecture & Orchestration](#planning-architecture-orchestration)
  - [💬 Conversation & Assistant Interaction](#conversation-assistant-interaction)

<a id="highlights"></a>

## ✨ Highlights

- Agent research is moving from prompt engineering toward system engineering: training, environments, evaluation, safety, memory, and workflows now interact tightly.
- Benchmarks and diagnostics form the largest visible cluster, suggesting a strong push toward measurability and reproducibility.
- Multi-agent systems, agentic RL, tool-use RL, trajectory-SFT, self-evolution, and distillation define a clear trainable-agent thread.
- GUI/Web/computer-use, coding/SWE, scientific discovery, and domain workflows are the most visible application frontiers.
- Safety and reliability are a first-class research direction, spanning multi-turn attacks, tool poisoning, privacy leakage, runtime monitoring, refusals, and robustness.

<a id="scope-and-method"></a>

## 🔎 Scope And Method

A paper is included if its title explicitly contains agent-related signals, including but not limited to:
agent, agentic, multi-agent, tool-use, tool-calling, computer-use, GUI agent, web agent, and related interactive decision-making terms.

The taxonomy is semiautomatically curated for navigation. It is not an official ICML taxonomy. Some papers may fit multiple themes; each paper is assigned to one primary category for readability.

This list may miss agent-adjacent work whose titles do not expose these signals, and it may include classical MARL or social-simulation papers that are adjacent to modern LLM-agent research.


<a id="taxonomy"></a>

## 🗂️ Taxonomy

| Icon | Theme | Count | Focus |
|---|---|---:|---|
| 📚 | [Benchmarks & Evaluation](#benchmarks-evaluation) | 99 | Reproducible and diagnostic agent evaluations across long-horizon tasks, GUI/Web, coding, science, finance, healthcare, and other realistic settings. |
| 🤝 | [Multi-Agent Systems & MARL](#multi-agent-systems-marl) | 93 | LLM multi-agent debate, cooperation, protocol choice, social simulation, and MARL problems such as coordination, communication, and credit assignment. |
| 🛠️ | [Tool Use, Training & RL](#tool-use-training-rl) | 58 | The shift from prompt-based agents to trainable agents, including tool-use RL, agentic RL, GRPO, trajectory-SFT, self-evolution, and distillation. |
| 🛡️ | [Safety, Security & Governance](#safety-security-governance) | 51 | Multi-turn attacks, tool poisoning, environment corruptions, privacy leakage, refusal boundaries, red-teaming, runtime monitoring, and guardrails. |
| 🧠 | [Theory, Behavior & Interpretability](#theory-behavior-interpretability) | 39 | More conceptual agent questions: goal-directedness, empowerment, oversight, behavioral representations, calibration, interpretability, and reliability science. |
| 🔬 | [Scientific & Domain Agents](#scientific-domain-agents) | 30 | Agents for data science, finance, medicine, biosecurity, CAD/circuits/robotics, retrosynthesis, enterprise operations, and other domain workflows. |
| 💾 | [Memory, Context & Long-Horizon Tasks](#memory-context-long-horizon) | 29 | State management for long-horizon agents: trajectory compression, graph memory, context folding, lifelong conversation, and cross-session memory. |
| 💻 | [Coding, SWE & Theorem Proving](#coding-swe-theorem-proving) | 27 | Repository-level software tasks, CUDA/Triton/kernel generation, full-stack development, vulnerability discovery, coding environments, and theorem proving. |
| 🖥️ | [GUI, Web & Computer-Use](#gui-web-computer-use) | 13 | Web, desktop, mobile GUI, and computer-use agents, including environment synthesis, trajectory pretraining, action correction, robustness, and safety. |
| 🎥 | [Multimodal, Embodied & Interactive Agents](#multimodal-embodied-interactive) | 11 | Agentic reasoning connected to VLM/VLA, video, audio, navigation, spatial reasoning, active perception, and embodied manipulation. |
| 🏗️ | [Planning, Architecture & Orchestration](#planning-architecture-orchestration) | 11 | Agent workflows, sub-agent creation, topology evolution, protocol selection, planning/execution separation, and system orchestration. |
| 💬 | [Conversation & Assistant Interaction](#conversation-assistant-interaction) | 4 | Clarification, question asking, utility/cost tradeoffs, full-duplex voice, and task-oriented interaction policies for conversational agents. |

<a id="full-list"></a>

## 📋 Full List

Format: **paper title** — one-line navigation note. Each title links to the official ICML page.

<a id="benchmarks-evaluation"></a>
### 📚 1. Benchmarks & Evaluation (99)

Reproducible and diagnostic agent evaluations across long-horizon tasks, GUI/Web, coding, science, finance, healthcare, and other realistic settings.

- **[$\tau$-Knowledge: Evaluating Conversational Agents over Unstructured Knowledge](https://icml.cc/virtual/2026/poster/63427)** — Introduces **$\tau$-Knowledge** to evaluate "Conversational Agents" on "Unstructured Knowledge".
- **[$\tau$-Voice: Benchmarking Full-Duplex Voice Agents on Real-World Domains](https://icml.cc/virtual/2026/poster/66590)** — Introduces **$\tau$-Voice** to evaluate "Full-Duplex Voice Agents" on "Real-World Domains".
- **[$\tau^2$-Bench: Evaluating Conversational Agents in a Dual-Control Environment](https://icml.cc/virtual/2026/poster/64377)** — Introduces **$\tau^2$-Bench** to evaluate "Conversational Agents" in "Dual-Control Environment".
- **[A Behavioural and Representational Evaluation of Goal-Directedness in Language Model Agents](https://icml.cc/virtual/2026/poster/64314)** — Evaluates the "Goal-Directedness" of "Language Model Agents" from behavioral and representational perspectives.
- **[A Diagnostic Study of Multi-Agent LLMs for Real-World Debates](https://icml.cc/virtual/2026/poster/66089)** — Diagnoses the behavior of "Multi-Agent LLMs" in "Real-World Debates".
- **[ABC-Bench: An Agentic Bio-Capabilities Benchmark for Biosecurity](https://icml.cc/virtual/2026/poster/60590)** — Introduces **ABC-Bench**, a benchmark for "Biosecurity".
- **[AgentExpt: Automating AI Experiment Design with LLM-based Resource Retrieval Agent](https://icml.cc/virtual/2026/poster/62358)** — Introduces **AgentExpt** by incorporating "LLM-based Resource Retrieval Agent" into automate "AI Experiment Design".
- **[AgentHijack: Benchmarking Computer Use Agent Robustness to Common Environment Corruptions](https://icml.cc/virtual/2026/poster/66792)** — Introduces **AgentHijack** to evaluate "Computer Use Agent Robustness to Common Environment Corruptions".
- **[AgentLAB: Benchmarking LLM Agents against Long-Horizon Attacks](https://icml.cc/virtual/2026/poster/65640)** — Introduces **AgentLAB** to evaluate "LLM Agents" against "Long-Horizon Attacks".
- **[AgentNoiseBench: Benchmarking Robustness of Tool-Using LLM Agents Under Noisy Condition](https://icml.cc/virtual/2026/poster/64355)** — Introduces **AgentNoiseBench** to evaluate "Robustness of Tool-Using LLM Agents" under "Noisy Condition".
- **[AgentSelect: Benchmark for Narrative Query-to-Agent Recommendation](https://icml.cc/virtual/2026/poster/66362)** — Introduces **AgentSelect**, a benchmark for "Narrative Query-to-Agent Recommendation".
- **[AgentWebBench: Benchmarking Multi-Agent Coordination in Agentic Web](https://icml.cc/virtual/2026/poster/63068)** — Introduces **AgentWebBench** to evaluate "Multi-Agent Coordination" in "Agentic Web".
- **[AMA-Bench: Evaluating Long-Horizon Memory for Agentic Applications](https://icml.cc/virtual/2026/poster/65112)** — Introduces **AMA-Bench** to evaluate "Long-Horizon Memory" for "Agentic Applications".
- **[An Empirical Study of Memory Poisoning Defenses for LLM Agents](https://icml.cc/virtual/2026/poster/61006)** — Provides an empirical study of "Memory Poisoning Defenses" for "LLM Agents".
- **[ANCHOR: Automated Alignment Auditing for CLI Agents on Real-World Harm](https://icml.cc/virtual/2026/poster/63234)** — Introduces **ANCHOR** to examine study "Automated Alignment Auditing for CLI Agents" on "Real-World Harm".
- **[AOEB: Benchmarking Agent-Oriented Multimodal Embeddings](https://icml.cc/virtual/2026/poster/61847)** — Introduces **AOEB** to evaluate "Agent-Oriented Multimodal Embeddings".
- **[AppWorld-UL: Benchmarking Diverse Agent-User Interactions for Tool-Use](https://icml.cc/virtual/2026/poster/62856)** — Introduces **AppWorld-UL** to evaluate "Diverse Agent-User Interactions" for "Tool-Use".
- **[ArenaRL: Scaling RL for Open-Ended Agents via Tournament-based Relative Ranking](https://icml.cc/virtual/2026/poster/66670)** — Introduces **ArenaRL**, using "Tournament-based Relative Ranking" to scale "RL for Open-Ended Agents".
- **[ARLArena: Demystifying Policy Gradient Stability in Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/65909)** — Introduces **ARLArena** to examine study "Demystifying Policy Gradient Stability" in "Agentic Reinforcement Learning".
- **[AtelierEval: Agentic Evaluation of Humans & LLMs as Text-to-Image Prompters](https://icml.cc/virtual/2026/poster/64186)** — Introduces **AtelierEval** around "Agentic Evaluation of Humans & LLMs as Text-to-Image Prompters".
- **[Benchmarking Agent Memory in Interdependent Multi-Session Agentic Tasks](https://icml.cc/virtual/2026/poster/64842)** — Evaluates "Agent Memory" in "Interdependent Multi-Session Agentic Tasks".
- **[Beyond the Final Answer: Evaluating the Reasoning Trajectories of Tool-Augmented Agents](https://icml.cc/virtual/2026/poster/64255)** — Introduces **Beyond the Final Answer** to evaluate "Reasoning Trajectories of Tool-Augmented Agents".
- **[BioAgent Bench: An AI Agent Evaluation Suite for Bioinformatics](https://icml.cc/virtual/2026/poster/66549)** — Introduces **BioAgent Bench** for "Bioinformatics", focusing on "AI Agent Evaluation Suite".
- **[CaP-X: A Framework for Benchmarking and Improving Coding Agents for Robot Manipulation](https://icml.cc/virtual/2026/poster/66369)** — Introduces **CaP-X**, a framework for "Benchmarking and Improving Coding Agents for Robot Manipulation".
- **[CATArena: Evaluating Evolutionary Capabilities of Code Agents via Iterative Tournaments](https://icml.cc/virtual/2026/poster/65908)** — Introduces **CATArena** to evaluate "Evolutionary Capabilities of Code Agents via Iterative Tournaments".
- **[CausalGame: Benchmarking Causal Thinking of LLM Agents in Games](https://icml.cc/virtual/2026/poster/63530)** — Introduces **CausalGame** to evaluate "Causal Thinking of LLM Agents" in "Games".
- **[CentaurEval: Benchmarking Human-in-the-Loop Value in Agentic Coding](https://icml.cc/virtual/2026/poster/65136)** — Introduces **CentaurEval** to evaluate "Human-in-the-Loop Value" in "Agentic Coding".
- **[CLAM-Bench: Benchmarking LLM Agents for Library-Scale Cross-Architecture Migration](https://icml.cc/virtual/2026/poster/60997)** — Introduces **CLAM-Bench** to evaluate "LLM Agents" for "Library-Scale Cross-Architecture Migration".
- **[CoDA-Bench: Can Code Agents Handle Data-Intensive Tasks?](https://icml.cc/virtual/2026/poster/63815)** — Introduces **CoDA-Bench** around "Can Code Agents Handle Data-Intensive Tasks?".
- **[ComplexMCP: Evaluation of LLM Agents in Dynamic, Interdependent, and Large-Scale Tool Sandbox](https://icml.cc/virtual/2026/poster/66421)** — Introduces **ComplexMCP** to examine study "Evaluation of LLM Agents" in "Dynamic, Interdependent, and Large-Scale Tool Sandbox".
- **[CoopEval: Benchmarking Cooperation-Sustaining Mechanisms and LLM Agents in Social Dilemmas](https://icml.cc/virtual/2026/poster/66503)** — Introduces **CoopEval** to evaluate "Cooperation-Sustaining Mechanisms and LLM Agents" in "Social Dilemmas".
- **[Copyright-Bench: Agentic Evaluation of Copyright Law Compliance](https://icml.cc/virtual/2026/poster/66009)** — Introduces **Copyright-Bench** around "Agentic Evaluation of Copyright Law Compliance".
- **[CUARewardBench: Benchmark for Evaluating Reward Models on Computer-using Agent Trajectories](https://icml.cc/virtual/2026/poster/63367)** — Introduces **CUARewardBench**, a benchmark for "Evaluating Reward Models on Computer-using Agent Trajectories".
- **[CyberCycle: Scalable Real-World Benchmark for AI Agents' End-to-End Cybersecurity Capabilities](https://icml.cc/virtual/2026/poster/62134)** — Introduces **CyberCycle** for "AI Agents' End-to-End Cybersecurity Capabilities", focusing on "Scalable Real-World Benchmark".
- **[DeepImageSearch: Benchmarking Multimodal Agents for Context-Aware Image Retrieval in Visual Histories](https://icml.cc/virtual/2026/poster/61711)** — Introduces **DeepImageSearch** to evaluate "Multimodal Agents for Context-Aware Image Retrieval" in "Visual Histories".
- **[DEER: A Benchmark for Evaluating Deep Research Agents on Expert Report Generation](https://icml.cc/virtual/2026/poster/64961)** — Introduces **DEER**, a benchmark for "Evaluating Deep Research Agents on Expert Report Generation".
- **[DevEvol: Benchmarking LLM Agents on Continuous Software Evolution](https://icml.cc/virtual/2026/poster/65024)** — Introduces **DevEvol** to evaluate "LLM Agents" on "Continuous Software Evolution".
- **[DocOS: A Benchmark for Proactive Document-Guided Actions in GUI Agents](https://icml.cc/virtual/2026/poster/65725)** — Introduces **DocOS**, a benchmark for "Proactive Document-Guided Actions in GUI Agents".
- **[Does Reinforcement Fine-Tuning Improve Generalization of LLM Agents? An Empirical Study](https://icml.cc/virtual/2026/poster/65794)** — Frames "Does Reinforcement Fine-Tuning Improve Generalization of LLM Agents? An Empirical Study" as the key question and probes agent capabilities or failure modes.
- **[DRIFT-BENCH: Diagnosing CoopeRative Breakdowns in LLM Agents under Input Faults via Multi-Turn Interaction](https://icml.cc/virtual/2026/poster/60842)** — Introduces **DRIFT-BENCH** to diagnose "CoopeRative Breakdowns in LLM Agents" under "Input Faults via Multi-Turn Interaction".
- **[DSGym: A Standardized and Holistic Framework for Advancing Data Science Agents](https://icml.cc/virtual/2026/poster/66567)** — Introduces **DSGym** for "Advancing Data Science Agents", focusing on "Standardized and Holistic Framework".
- **[DV-World: Benchmarking Data Visualization Agents in Real-World Scenarios](https://icml.cc/virtual/2026/poster/61444)** — Introduces **DV-World** to evaluate "Data Visualization Agents" in "Real-World Scenarios".
- **[DynaSchedBench: Calibrated Dynamic Scheduling Benchmarks and Observability Paradox in LLM-based Scheduling Agents](https://icml.cc/virtual/2026/poster/60484)** — Introduces **DynaSchedBench** to examine study "Calibrated Dynamic Scheduling Benchmarks and Observability Paradox" in "LLM-based Scheduling Agents".
- **[EnterpriseOps-Gym: Environments and Evaluations for Stateful Agentic Planning and Tool Use in Enterprise Settings](https://icml.cc/virtual/2026/poster/64162)** — Introduces **EnterpriseOps-Gym** to examine study "Environments and Evaluations for Stateful Agentic Planning and Tool Use" in "Enterprise Settings".
- **[Evaluating Agentic Optimization on Large Codebases](https://icml.cc/virtual/2026/poster/63544)** — Evaluates "Agentic Optimization" on "Large Codebases".
- **[EVMbench: Evaluating AI Agents on Smart Contract Security](https://icml.cc/virtual/2026/poster/64768)** — Introduces **EVMbench** to evaluate "AI Agents" on "Smart Contract Security".
- **[EVOLVING ROLLOUTS: Harnessing Historical Experience for Web Agent Evolution in Reinforcement Learning](https://icml.cc/virtual/2026/poster/61544)** — Introduces **EVOLVING ROLLOUTS** to examine study "Harnessing Historical Experience for Web Agent Evolution" in "Reinforcement Learning".
- **[ExCyTIn-Bench: Evaluating LLM agents on Cyber Threat Investigation](https://icml.cc/virtual/2026/poster/66310)** — Introduces **ExCyTIn-Bench** to evaluate "LLM agents" on "Cyber Threat Investigation".
- **[FIRE-Bench: Evaluating Agents on the Rediscovery of Scientific Insights](https://icml.cc/virtual/2026/poster/61975)** — Introduces **FIRE-Bench** to evaluate "Agents" on "Rediscovery of Scientific Insights".
- **[Fix Before Search: Benchmarking Agentic Visual Query Pre-processing in Multimodal Retrieval-augmented Generation](https://icml.cc/virtual/2026/poster/62898)** — Introduces **Fix Before Search** to evaluate "Agentic Visual Query Pre-processing" in "Multimodal Retrieval-augmented Generation".
- **[GameDevBench: Evaluating Agentic Capabilities Through Game Development](https://icml.cc/virtual/2026/poster/64919)** — Introduces **GameDevBench** to evaluate "Agentic Capabilities Through Game Development".
- **[Harnessing Uncertainty: Entropy-Modulated Policy Gradients for Long-Horizon LLM Agents](https://icml.cc/virtual/2026/poster/63273)** — Introduces **Harnessing Uncertainty** for "Long-Horizon LLM Agents", focusing on "Entropy-Modulated Policy Gradients".
- **[How Far Can LLM Agents Reason with Tables? Benchmarking Multi-Turn Agentic Table Question Answering in the Wild](https://icml.cc/virtual/2026/poster/66187)** — Frames "How Far Can LLM Agents Reason with Tables? Benchmarking Multi-Turn Agentic Table Question Answering in the Wild" as the key question and probes agent capabilities or failure modes.
- **[HVR-Met: A Hypothesis-Verification-Replaning Agentic System for Extreme Weather Diagnosis](https://icml.cc/virtual/2026/poster/61110)** — Introduces **HVR-Met** for "Extreme Weather Diagnosis", focusing on "Hypothesis-Verification-Replanning Agentic System".
- **[Hybrid-Gym: Training Coding Agents to Generalize Across Tasks](https://icml.cc/virtual/2026/poster/66577)** — Introduces **Hybrid-Gym** around "Training Coding Agents to Generalize Across Tasks".
- **[Implicit Intelligence - Evaluating Agents on What Users Don’t Say](https://icml.cc/virtual/2026/poster/64912)** — Surveys/evaluates "Implicit Intelligence - Evaluating Agents" on "What Users Don’t Say".
- **[ImpText: A Benchmark and Tool-Augmented Framework for Implicit Text Reasoning](https://icml.cc/virtual/2026/poster/63174)** — Introduces **ImpText** for "Implicit Text Reasoning", focusing on "Benchmark and Tool-Augmented Framework".
- **[InteractComp: Evaluating Search Agents With Ambiguous Queries](https://icml.cc/virtual/2026/poster/65730)** — Introduces **InteractComp** to evaluate "Search Agents" with "Ambiguous Queries".
- **[Is Vibe Coding Safe? Benchmarking Vulnerability of Agent-Generated Code in Real-World Tasks](https://icml.cc/virtual/2026/poster/61427)** — Frames "Is Vibe Coding Safe? Benchmarking Vulnerability of Agent-Generated Code in Real-World Tasks" as the key question and probes agent capabilities or failure modes.
- **[It's a TRAP! Task-Redirecting Agent Persuasion Benchmark for Web Agents](https://icml.cc/virtual/2026/poster/63888)** — Surveys/evaluates "It's a TRAP! Task-Redirecting Agent Persuasion Benchmark" for "Web Agents".
- **[KernelCraft: Benchmarking for Agentic Close-to-Metal Kernel Generation on Emerging Hardware](https://icml.cc/virtual/2026/poster/65579)** — Introduces **KernelCraft** to evaluate "for Agentic Close-to-Metal Kernel Generation" on "Emerging Hardware".
- **[LitReview Arena: Evaluating Literature Review Agents with Battle-style Peer Review Platform](https://icml.cc/virtual/2026/poster/63625)** — Introduces **LitReview Arena** to evaluate "Literature Review Agents" with "Battle-style Peer Review Platform".
- **[LOCA-bench: Benchmarking Language Agents Under Controllable and Extreme Context Growth](https://icml.cc/virtual/2026/poster/64486)** — Introduces **LOCA-bench** to evaluate "Language Agents" under "Controllable and Extreme Context Growth".
- **[MAS-Orchestra: Understanding and Improving Multi-Agent Reasoning Through Holistic Orchestration and Controlled Benchmarks](https://icml.cc/virtual/2026/poster/66445)** — Introduces **MAS-Orchestra**, using "Holistic Orchestration and Controlled Benchmarks" to study "Understanding and Improving Multi-Agent Reasoning".
- **[MCP-Persona: Benchmarking LLM Agents on Personalized MCP Tools and Tasks](https://icml.cc/virtual/2026/poster/60873)** — Introduces **MCP-Persona** to evaluate "LLM Agents" on "Personalized MCP Tools and Tasks".
- **[MEAL: A Benchmark for Continual Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/64499)** — Introduces **MEAL**, a benchmark for "Continual Multi-Agent Reinforcement Learning".
- **[Memoria-Bench: A Comprehensive Benchmark for Evaluating Memory in Long-Horizon Autonomous Agents](https://icml.cc/virtual/2026/poster/64414)** — Introduces **Memoria-Bench**, a benchmark for "Evaluating Memory in Long-Horizon Autonomous Agents".
- **[Monitoring LLM-based Multi-Agent Systems Against Corruptions via Node Evaluation](https://icml.cc/virtual/2026/poster/63780)** — Surveys/evaluates "Monitoring LLM-based Multi-Agent Systems Against Corruptions", with "Node Evaluation" as the core mechanism.
- **[NL2Repo-Bench: Towards Long-Horizon Repository Generation Evaluation of Coding Agents](https://icml.cc/virtual/2026/poster/60772)** — Introduces **NL2Repo-Bench** around "Towards Long-Horizon Repository Generation Evaluation of Coding Agents".
- **[Off-Policy Evaluation with Strategic Agents via Local Disclosure](https://icml.cc/virtual/2026/poster/64971)** — Surveys/evaluates "Off-Policy Evaluation with Strategic Agents", with "Local Disclosure" as the core mechanism.
- **[Optimizing Agentic Reasoning with Retrieval via Synthetic Semantic Information Gain Reward](https://icml.cc/virtual/2026/poster/61838)** — Surveys/evaluates "Optimizing Agentic Reasoning with Retrieval", with "Synthetic Semantic Information Gain Reward" as the core mechanism.
- **[Persona2Web: Benchmarking Personalized Web Agents for Contextual Reasoning with User History](https://icml.cc/virtual/2026/poster/61367)** — Introduces **Persona2Web** to evaluate "Personalized Web Agents" for "Contextual Reasoning with User History".
- **[Position: Agent Evaluation Should Be Agentified for Openness, Standardization, and Reproducibility](https://icml.cc/virtual/2026/poster/67210)** — Introduces **Position** for "Openness, Standardization, and Reproducibility", focusing on "Agent Evaluation Should Be Agentified".
- **[PostTrainBench: Can LLM Agents Automate LLM Post-Training?](https://icml.cc/virtual/2026/poster/63667)** — Introduces **PostTrainBench** around "Can LLM Agents Automate LLM Post-Training?".
- **[PPT-Eval: A Benchmark for Computer-Use Agents on PowerPoint Tasks](https://icml.cc/virtual/2026/poster/65101)** — Introduces **PPT-Eval**, a benchmark for "Computer-Use Agents on PowerPoint Tasks".
- **[Protein Design with Agent Rosetta: A Case Study for Specialized Scientific Agents](https://icml.cc/virtual/2026/poster/64569)** — Introduces **Protein Design with Agent Rosetta** for "Specialized Scientific Agents", focusing on "Case Study".
- **[PSBench: Editing Image via GUI Agents in Photoshop](https://icml.cc/virtual/2026/poster/64381)** — Introduces **PSBench**, using "GUI Agents in Photoshop" to study "Editing Image".
- **[Recovering Policy-Induced Errors: Benchmarking and Trajectory Synthesis for Robust GUI Agents](https://icml.cc/virtual/2026/poster/62251)** — Introduces **Recovering Policy-Induced Errors** to evaluate "and Trajectory Synthesis" for "Robust GUI Agents".
- **[Reward Hacking Benchmark: Measuring Exploits in LLM Agents with Tool Use](https://icml.cc/virtual/2026/poster/63289)** — Introduces **Reward Hacking Benchmark** by incorporating "Tool Use" into study "Measuring Exploits in LLM Agents".
- **[Rule2DRC: Benchmarking LLM Agents for DRC Script Synthesis with Execution-Guided Test Generation](https://icml.cc/virtual/2026/poster/63031)** — Introduces **Rule2DRC** to evaluate "LLM Agents" for "DRC Script Synthesis with Execution-Guided Test Generation".
- **[SAGE-NAS: Synergizing LLM-Based Semantic Agent with Graph-Based Evaluator for Neural Architecture Search](https://icml.cc/virtual/2026/poster/62021)** — Introduces **SAGE-NAS** by incorporating "Graph-Based Evaluator for Neural Architecture Search" into study "Synergizing LLM-Based Semantic Agent".
- **[Salus: Strategic Diagnostic Testing for Complex Diagnosis via Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/64732)** — Introduces **Salus**, using "Multi-Agent Reinforcement Learning" to study "Strategic Diagnostic Testing for Complex Diagnosis".
- **[Scaling, Benchmarking, and Reasoning of Vision-Language Agents for Mobile GUI Navigation](https://icml.cc/virtual/2026/poster/63113)** — Surveys/evaluates "Scaling, Benchmarking, and Reasoning of Vision-Language Agents" for "Mobile GUI Navigation".
- **[SciAgentGym: Benchmarking Multi-Step Scientific Tool-Use in LLM Agents](https://icml.cc/virtual/2026/poster/66785)** — Introduces **SciAgentGym** to evaluate "Multi-Step Scientific Tool-Use" in "LLM Agents".
- **[SciNet: Evaluating AI Agents in Relation-Aware Scientific Literature Retrieval](https://icml.cc/virtual/2026/poster/66769)** — Introduces **SciNet** to evaluate "AI Agents" in "Relation-Aware Scientific Literature Retrieval".
- **[SWE-Bench Pro: Can AI Agents Solve Long-Horizon Software Engineering Tasks?](https://icml.cc/virtual/2026/poster/61047)** — Introduces **SWE-Bench Pro** around "Can AI Agents Solve Long-Horizon Software Engineering Tasks?".
- **[SWE-Compass: Towards Unified Evaluation of Agentic Coding Abilities for Large Language Models](https://icml.cc/virtual/2026/poster/64552)** — Introduces **SWE-Compass** for "Large Language Models", focusing on "Towards Unified Evaluation of Agentic Coding Abilities".
- **[Taming I2V models for Image HOI Editing: A Cognitive Benchmark and Agentic Self-Correcting Framework](https://icml.cc/virtual/2026/poster/63999)** — Introduces **Taming I2V models for Image HOI Editing** around "Cognitive Benchmark and Agentic Self-Correcting Framework".
- **[The Crowded Embedding Space: A Mean-Field Mechanism for Emergent Marginalization in Retrieval-Augmented Agents](https://icml.cc/virtual/2026/poster/64854)** — Introduces **The Crowded Embedding Space** to examine study "Mean-Field Mechanism for Emergent Marginalization" in "Retrieval-Augmented Agents".
- **[The Decrypto Benchmark for Multi-Agent Reasoning and Theory of Mind](https://icml.cc/virtual/2026/poster/62135)** — Surveys/evaluates "Decrypto Benchmark" for "Multi-Agent Reasoning and Theory of Mind".
- **[Toward More Reliable Agent Evaluation: A Component-Based Benchmark Auditing Pipeline](https://icml.cc/virtual/2026/poster/66603)** — Introduces **Toward More Reliable Agent Evaluation** around "Component-Based Benchmark Auditing Pipeline".
- **[Towards Professional-Grade Financial Agents: Benchmarking, Tooling, and Structured Reasoning](https://icml.cc/virtual/2026/poster/60732)** — Introduces **Towards Professional-Grade Financial Agents** around "Benchmarking, Tooling, and Structured Reasoning".
- **[TRIP-Bench: A Benchmark for Long-Horizon Interactive Agents in Real-World Scenarios](https://icml.cc/virtual/2026/poster/62985)** — Introduces **TRIP-Bench**, a benchmark for "Long-Horizon Interactive Agents in Real-World Scenarios".
- **[TritonGym: A Benchmark for Agentic LLM Workflows in Triton GPU Code Generation](https://icml.cc/virtual/2026/poster/65003)** — Introduces **TritonGym**, a benchmark for "Agentic LLM Workflows in Triton GPU Code Generation".
- **[UltraHorizon: Benchmarking LLM-Agent Capabilities in Ultra Long-Horizon Scenarios](https://icml.cc/virtual/2026/poster/61412)** — Introduces **UltraHorizon** to evaluate "LLM-Agent Capabilities" in "Ultra Long-Horizon Scenarios".
- **[Unsafer in Many Turns: Benchmarking and Defending Multi-Turn Safety Risks in Tool-Using Agents](https://icml.cc/virtual/2026/poster/62233)** — Introduces **Unsafer in Many Turns** to evaluate "and Defending Multi-Turn Safety Risks" in "Tool-Using Agents".
- **[VenusBench-Mobile: A Challenging and User-Centric Benchmark for Mobile GUI Agents with Capability Diagnostics](https://icml.cc/virtual/2026/poster/62831)** — Introduces **VenusBench-Mobile**, a benchmark for "Mobile GUI Agents with Capability Diagnostics".
- **[VeRO: An Evaluation Harness for Agents to Optimize Agents](https://icml.cc/virtual/2026/poster/60518)** — Introduces **VeRO** for "Agents to Optimize Agents", focusing on "Evaluation Harness".
- **[VisionWebDev: A Hierarchical Benchmark for Visual Website Development with Agent Verification](https://icml.cc/virtual/2026/poster/61957)** — Introduces **VisionWebDev**, a benchmark for "Visual Website Development with Agent Verification".

<a id="multi-agent-systems-marl"></a>
### 🤝 2. Multi-Agent Systems & MARL (93)

LLM multi-agent debate, cooperation, protocol choice, social simulation, and MARL problems such as coordination, communication, and credit assignment.

- **[$\texttt{Multi}^2$: Hierarchical Multi-Agent Decision-Making with LLM-Based Agents in Interactive Environments](https://icml.cc/virtual/2026/poster/65074)** — Introduces **$\texttt{Multi}^2$** by incorporating "LLM-Based Agents in Interactive Environments" into study "Hierarchical Multi-Agent Decision-Making".
- **[A Two-Tier Perspective on Inference-Time Parallelism in Multi-Agent LLM Systems](https://icml.cc/virtual/2026/poster/66552)** — Studies "Two-Tier Perspective on Inference-Time Parallelism" in "Multi-Agent LLM Systems".
- **[Agent Primitives: Reuseable Latent Building Blocks for Multi-Agent Systems](https://icml.cc/virtual/2026/poster/65501)** — Introduces **Agent Primitives** for "Multi-Agent Systems", focusing on "Reuseable Latent Building Blocks".
- **[AgentSteerTTS: A Multi-Agent Closed-Loop Framework for Composite-Instruction Text-to-Speech](https://icml.cc/virtual/2026/poster/62320)** — Introduces **AgentSteerTTS** for "Composite-Instruction Text-to-Speech", focusing on "Multi-Agent Closed-Loop Framework".
- **[AgentTailor: A Semantic-Aware LLM-Based Multi-Agent System with Actor-Critic Structure](https://icml.cc/virtual/2026/poster/60754)** — Introduces **AgentTailor** by incorporating "Actor-Critic Structure" into study "Semantic-Aware LLM-Based Multi-Agent System".
- **[ALSO: Adversarial Online Strategy Optimization for Social Agents](https://icml.cc/virtual/2026/poster/64379)** — Introduces **ALSO** for "Social Agents", focusing on "Adversarial Online Strategy Optimization".
- **[Automata-Conditioned Cooperative Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/63254)** — Studies "Automata-Conditioned Cooperative Multi-Agent Reinforcement Learning".
- **[AutoMS: Multi-Agent Evolutionary Search for Cross-Physics Inverse Microstructure Design](https://icml.cc/virtual/2026/poster/60501)** — Introduces **AutoMS** for "Cross-Physics Inverse Microstructure Design", focusing on "Multi-Agent Evolutionary Search".
- **[Betting on Equilibrium: Monitoring Strategic Behavior in Multi-Agent Systems](https://icml.cc/virtual/2026/poster/62338)** — Introduces **Betting on Equilibrium** to examine study "Monitoring Strategic Behavior" in "Multi-Agent Systems".
- **[Beyond Correctness: Distance-Based Social Dynamics of Multi-Agent Debate](https://icml.cc/virtual/2026/poster/61651)** — Introduces **Beyond Correctness** around "Distance-Based Social Dynamics of Multi-Agent Debate".
- **[CoPE: A Framework for Optimizing Coordination between Planning and Execution in LLM-based Agents](https://icml.cc/virtual/2026/poster/65839)** — Introduces **CoPE**, a framework for "Optimizing Coordination between Planning and Execution in LLM-based Agents".
- **[CORRECT: COndensed eRror RECognition via knowledge Transfer in multi-agent systems](https://icml.cc/virtual/2026/poster/63163)** — Introduces **CORRECT**, using "knowledge Transfer in multi-agent systems" to study "COndensed eRror RECognition".
- **[CyberJurors: A Multi-Agent Simulation Task for E-Commerce Disputes Verdict](https://icml.cc/virtual/2026/poster/61907)** — Introduces **CyberJurors** for "E-Commerce Disputes Verdict", focusing on "Multi-Agent Simulation Task".
- **[Decentralized and Disentangled Task–Role Representation Learning for Generalizable Offline Multi-Agent Meta Reinforcement Learning](https://icml.cc/virtual/2026/poster/61278)** — Studies "Decentralized and Disentangled Task–Role Representation Learning" for "Generalizable Offline Multi-Agent Meta Reinforcement Learning".
- **[DECOR: Learning to Decompose and Collaborate in Deep Search via Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/62745)** — Introduces **DECOR**, using "Multi-Agent Reinforcement Learning" to learn "to Decompose and Collaborate in Deep Search".
- **[Detecting Perspective Shifts in Multi-Agent Systems](https://icml.cc/virtual/2026/poster/61263)** — Studies "Detecting Perspective Shifts" in "Multi-Agent Systems".
- **[Diffusing to Coordinate: Efficient Online Multi-Agent Diffusion Policies](https://icml.cc/virtual/2026/poster/61146)** — Introduces **Diffusing to Coordinate** around "Efficient Online Multi-Agent Diffusion Policies".
- **[Distilling Task-Level Coordination Policies for Generalizable Multi-Agent Cooperation](https://icml.cc/virtual/2026/poster/66438)** — Studies "Distilling Task-Level Coordination Policies" for "Generalizable Multi-Agent Cooperation".
- **[DLM: Unified Decision Language Models for Offline Multi-Agent Sequential Decision Making](https://icml.cc/virtual/2026/poster/61365)** — Introduces **DLM** for "Offline Multi-Agent Sequential Decision Making", focusing on "Unified Decision Language Models".
- **[Dual Latent Memory for Visual Multi-agent System](https://icml.cc/virtual/2026/poster/63256)** — Studies "Dual Latent Memory" for "Visual Multi-agent System".
- **[E-mem: Multi-Agent Based Episodic Context Reconstruction for LLM Agent Memory](https://icml.cc/virtual/2026/poster/65274)** — Introduces **E-mem** for "LLM Agent Memory", focusing on "Multi-Agent Based Episodic Context Reconstruction".
- **[EduMirror: Modeling Educational Social Dynamics with Value-driven Multi-agent Simulation](https://icml.cc/virtual/2026/poster/65878)** — Introduces **EduMirror** by incorporating "Value-driven Multi-agent Simulation" into study "Modeling Educational Social Dynamics".
- **[Efficient Multi-Agent Reasoning via Confidence-Guided Adaptive Debate](https://icml.cc/virtual/2026/poster/60593)** — Studies "Efficient Multi-Agent Reasoning", with "Confidence-Guided Adaptive Debate" as the core mechanism.
- **[Emergence of Biased Consensus in Multi-Agent LLM Debates](https://icml.cc/virtual/2026/poster/66269)** — Studies "Emergence of Biased Consensus" in "Multi-Agent LLM Debates".
- **[Epistemic Gain, Aleatoric Cost: Uncertainty Decomposition in Multi-Agent Debate for Math Reasoning](https://icml.cc/virtual/2026/poster/65653)** — Introduces **Epistemic Gain, Aleatoric Cost** to examine study "Uncertainty Decomposition" in "Multi-Agent Debate for Math Reasoning".
- **[EvoCF: Multi-Agent Collaboration via Agentic Memory-Driven Evolutionary Counterfactual Planning](https://icml.cc/virtual/2026/poster/65198)** — Introduces **EvoCF**, using "Agentic Memory-Driven Evolutionary Counterfactual Planning" to study "Multi-Agent Collaboration".
- **[Evolutionary Generation of Multi-Agent Systems](https://icml.cc/virtual/2026/poster/62216)** — Studies "Evolutionary Generation of Multi-Agent Systems".
- **[Evolving Interpretable Constitutions for Multi-Agent Coordination](https://icml.cc/virtual/2026/poster/66529)** — Studies "Evolving Interpretable Constitutions" for "Multi-Agent Coordination".
- **[Factored Value Functions for Graph-Based Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/62462)** — Studies "Factored Value Functions" for "Graph-Based Multi-Agent Reinforcement Learning".
- **[Fault Tolerant Multi-Agent Learning with Adversarial Budget Constraints](https://icml.cc/virtual/2026/poster/61177)** — Studies "Fault Tolerant Multi-Agent Learning" and incorporates "Adversarial Budget Constraints".
- **[From Interaction Trajectories to Prompt Rules: Credit Assignment for Multi-Agent Prompt Optimization](https://icml.cc/virtual/2026/poster/61502)** — Introduces **From Interaction Trajectories to Prompt Rules** for "Multi-Agent Prompt Optimization", focusing on "Credit Assignment".
- **[Gecko: A Simulation Environment with Stateful Feedback for Refining Agent Tool Calls](https://icml.cc/virtual/2026/poster/65078)** — Introduces **Gecko** by incorporating "Stateful Feedback for Refining Agent Tool Calls" into study "Simulation Environment".
- **[Great Minds Think Alike: Contextual Tacit Communication for Decentralized LLM-Agent Cooperation](https://icml.cc/virtual/2026/poster/63854)** — Introduces **Great Minds Think Alike** for "Decentralized LLM-Agent Cooperation", focusing on "Contextual Tacit Communication".
- **[Group Cognition Learning: Making Everything Better Through Controlled Two-Stage Agents Collaboration](https://icml.cc/virtual/2026/poster/61162)** — Introduces **Group Cognition Learning**, using "Controlled Two-Stage Agents Collaboration" to study "Making Everything Better".
- **[HieraMAS: Optimizing Intra-Node LLM Mixtures and Inter-Node Topology for Multi-Agent Systems](https://icml.cc/virtual/2026/poster/61537)** — Introduces **HieraMAS** for "Multi-Agent Systems", focusing on "Optimizing Intra-Node LLM Mixtures and Inter-Node Topology".
- **[HiMAP-Travel: Hierarchical Multi-Agent Planning for Long-Horizon Constrained Travel](https://icml.cc/virtual/2026/poster/61536)** — Introduces **HiMAP-Travel** for "Long-Horizon Constrained Travel", focusing on "Hierarchical Multi-Agent Planning".
- **[HPS: Hyperspherical Parameter Sharing for Efficient Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/65604)** — Introduces **HPS** for "Efficient Multi-Agent Reinforcement Learning", focusing on "Hyperspherical Parameter Sharing".
- **[HyPOLE: Hyperproperty-Guided Multi-Agent Reinforcement Learning under Partial Observation](https://icml.cc/virtual/2026/poster/65345)** — Introduces **HyPOLE** to examine study "Hyperproperty-Guided Multi-Agent Reinforcement Learning" under "Partial Observation".
- **[IEC: When Information-Driven Exploration Meets Spectral Consensus via Primal–Dual Reward Regularization in Decentralized Multi-Agent RL](https://icml.cc/virtual/2026/poster/65199)** — Introduces **IEC**, using "Primal–Dual Reward Regularization in Decentralized Multi-Agent RL" to study "When Information-Driven Exploration Meets Spectral Consensus".
- **[Investigating Component Contributions in Multi-Agent ML Systems](https://icml.cc/virtual/2026/poster/65244)** — Studies "Investigating Component Contributions" in "Multi-Agent ML Systems".
- **[Judgment Operators: A Composition-Invariant Substrate for Multi-Agent Action Spaces](https://icml.cc/virtual/2026/poster/65952)** — Introduces **Judgment Operators** for "Multi-Agent Action Spaces", focusing on "Composition-Invariant Substrate".
- **[Latent Collaboration in Multi-Agent Systems](https://icml.cc/virtual/2026/poster/61180)** — Studies "Latent Collaboration" in "Multi-Agent Systems".
- **[Learning Decentralized LLM Collaboration with Multi-Agent Actor Critic](https://icml.cc/virtual/2026/poster/62068)** — Studies "Learning Decentralized LLM Collaboration" and incorporates "Multi-Agent Actor Critic".
- **[Learning Disentangled Multi-Agent World Model for Decentralized Control](https://icml.cc/virtual/2026/poster/61713)** — Studies "Learning Disentangled Multi-Agent World Model" for "Decentralized Control".
- **[Learning Multi-Agent Coordination via Sheaf-ADMM](https://icml.cc/virtual/2026/poster/62363)** — Studies "Learning Multi-Agent Coordination", with "Sheaf-ADMM" as the core mechanism.
- **[LLawCo: Learning Laws of Cooperation for Modeling Embodied Multi-Agent Behavior](https://icml.cc/virtual/2026/poster/64415)** — Introduces **LLawCo** for "Modeling Embodied Multi-Agent Behavior", focusing on "Learning Laws of Cooperation".
- **[LLM-Guided Communication for Cooperative Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/61721)** — Studies "LLM-Guided Communication" for "Cooperative Multi-Agent Reinforcement Learning".
- **[MAFE: Enabling Equitable Algorithm Design in Multi-Agent Multi-Stage Decision-Making Systems](https://icml.cc/virtual/2026/poster/60878)** — Introduces **MAFE** to examine study "Enabling Equitable Algorithm Design" in "Multi-Agent Multi-Stage Decision-Making Systems".
- **[MARS-SQL: A Multi-Agent Reinforcement Learning Framework For Text-To-SQL](https://icml.cc/virtual/2026/poster/65053)** — Introduces **MARS-SQL** for "Text-To-SQL", focusing on "Multi-Agent Reinforcement Learning Framework".
- **[MAS-Architect: Declarative Multi-Agent System Design via Separation of Concerns](https://icml.cc/virtual/2026/poster/63290)** — Introduces **MAS-Architect**, using "Separation of Concerns" to study "Declarative Multi-Agent System Design".
- **[MAS-ProVe: Understanding the Process Verification of Multi-Agent Systems](https://icml.cc/virtual/2026/poster/63666)** — Introduces **MAS-ProVe** around "Understanding the Process Verification of Multi-Agent Systems".
- **[MASPO: Joint Prompt Optimization for LLM-based Multi-Agent Systems](https://icml.cc/virtual/2026/poster/62219)** — Introduces **MASPO** for "LLM-based Multi-Agent Systems", focusing on "Joint Prompt Optimization".
- **[MASPOB: Bandit-Based Prompt Optimization for Multi-Agent Systems with Graph Neural Networks](https://icml.cc/virtual/2026/poster/65791)** — Introduces **MASPOB** by incorporating "Graph Neural Networks" into study "Bandit-Based Prompt Optimization for Multi-Agent Systems".
- **[MemIncept: Steering LLM Agents via Cooperative Stealthy Memory Injections](https://icml.cc/virtual/2026/poster/66667)** — Introduces **MemIncept**, using "Cooperative Stealthy Memory Injections" to study "Steering LLM Agents".
- **[MOC: Multi-Order Communication in LLM-based Multi-Agent Systems](https://icml.cc/virtual/2026/poster/60749)** — Introduces **MOC** to examine study "Multi-Order Communication" in "LLM-based Multi-Agent Systems".
- **[MonoScale: Scaling Multi-Agent System with Monotonic Improvement](https://icml.cc/virtual/2026/poster/62913)** — Introduces **MonoScale** by incorporating "Monotonic Improvement" into scale "Multi-Agent System".
- **[Mosaic: Runtime-Efficient Multi-Agent Embodied Planning](https://icml.cc/virtual/2026/poster/62291)** — Introduces **Mosaic** around "Runtime-Efficient Multi-Agent Embodied Planning".
- **[Multi-agent imitation learning with function approximation: linear Markov games and beyond](https://icml.cc/virtual/2026/poster/64113)** — Introduces **Multi-agent imitation learning with function approximation** around "linear Markov games and beyond".
- **[Multi-Agent Reinforcement Learning with Submodular Reward](https://icml.cc/virtual/2026/poster/61139)** — Studies "Multi-Agent Reinforcement Learning" and incorporates "Submodular Reward".
- **[Multi-Agent Teams Hold Experts Back](https://icml.cc/virtual/2026/poster/63358)** — Studies "Multi-Agent Teams Hold Experts Back".
- **[Navigating the Energy Landscape of Collaboration: Multi-Agent Communication Graph Generation via Score-Based Diffusion](https://icml.cc/virtual/2026/poster/61913)** — Introduces **Navigating the Energy Landscape of Collaboration**, using "Score-Based Diffusion" to study "Multi-Agent Communication Graph Generation".
- **[NonZero: Interaction-Guided Exploration for Multi-Agent Monte Carlo Tree Search](https://icml.cc/virtual/2026/poster/64800)** — Introduces **NonZero** for "Multi-Agent Monte Carlo Tree Search", focusing on "Interaction-Guided Exploration".
- **[Offline Multi-agent Continual Cooperation via Skill Partition and Reuse](https://icml.cc/virtual/2026/poster/66211)** — Studies "Offline Multi-agent Continual Cooperation", with "Skill Partition and Reuse" as the core mechanism.
- **[Offline Multi-Agent Reinforcement Learning via Sequential Score Decomposition](https://icml.cc/virtual/2026/poster/64191)** — Studies "Offline Multi-Agent Reinforcement Learning", with "Sequential Score Decomposition" as the core mechanism.
- **[OMAC: A Holistic Optimization Framework for LLM-Based Multi-Agent Collaboration](https://icml.cc/virtual/2026/poster/66164)** — Introduces **OMAC** for "LLM-Based Multi-Agent Collaboration", focusing on "Holistic Optimization Framework".
- **[OpenDeception: Learning Deception and Trust in Human–AI Interaction via Multi-Agent Simulation](https://icml.cc/virtual/2026/poster/64249)** — Introduces **OpenDeception**, using "Multi-Agent Simulation" to learn "Deception and Trust in Human–AI Interaction".
- **[Position: Multi-Agent Explainability Needs Contracts Before Methods](https://icml.cc/virtual/2026/poster/67110)** — Introduces **Position** around "Multi-Agent Explainability Needs Contracts Before Methods".
- **[Position: Multi-Agent Systems Should Prioritize Concurrency Control](https://icml.cc/virtual/2026/poster/67076)** — Introduces **Position** around "Multi-Agent Systems Should Prioritize Concurrency Control".
- **[PromptPilot: Game-Theoretic Multi-Agent Prompt Optimization for Segment Anything](https://icml.cc/virtual/2026/poster/65063)** — Introduces **PromptPilot** for "Segment Anything", focusing on "Game-Theoretic Multi-Agent Prompt Optimization".
- **[RADAR: Redundancy-Aware Diffusion for Multi-Agent Communication Structure Generation](https://icml.cc/virtual/2026/poster/65087)** — Introduces **RADAR** for "Multi-Agent Communication Structure Generation", focusing on "Redundancy-Aware Diffusion".
- **[Recognize Your Orchestrator: An Entropy Dynamics Perspective for LLM Multi-Agent Systems](https://icml.cc/virtual/2026/poster/63622)** — Introduces **Recognize Your Orchestrator** for "LLM Multi-Agent Systems", focusing on "Entropy Dynamics Perspective".
- **[Representational Similarity and Model Behavior in Multi-Agent Interaction](https://icml.cc/virtual/2026/poster/60905)** — Studies "Representational Similarity and Model Behavior" in "Multi-Agent Interaction".
- **[Role-Level Inductive Bias for Cross-Task Generalization in Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/61552)** — Studies "Role-Level Inductive Bias" for "Cross-Task Generalization in Multi-Agent Reinforcement Learning".
- **[ScaleSim: Serving Large-Scale Multi-Agent Simulation with Invocation Distance-Based Memory Management](https://icml.cc/virtual/2026/poster/62000)** — Introduces **ScaleSim** by incorporating "Invocation Distance-Based Memory Management" into study "Serving Large-Scale Multi-Agent Simulation".
- **[Scaling Multi-Agent Environment Co-Design with Diffusion Models](https://icml.cc/virtual/2026/poster/65949)** — Studies "Scaling Multi-Agent Environment Co-Design" and incorporates "Diffusion Models".
- **[Scaling up Multi-Turn Off-Policy RL and Multi-Agent Tree Search for LLM Step-Provers](https://icml.cc/virtual/2026/poster/65141)** — Studies "Scaling up Multi-Turn Off-Policy RL and Multi-Agent Tree Search" for "LLM Step-Provers".
- **[SceneSmith: Agentic Generation of Simulation-Ready Indoor Scenes](https://icml.cc/virtual/2026/poster/63465)** — Introduces **SceneSmith** around "Agentic Generation of Simulation-Ready Indoor Scenes".
- **[Sparks of Cooperative Reasoning: LLMs as Strategic Hanabi Agents](https://icml.cc/virtual/2026/poster/60843)** — Introduces **Sparks of Cooperative Reasoning** around "LLMs as Strategic Hanabi Agents".
- **[Sparse Topology-Aware Pairwise Scoring for Large-Scale Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/65907)** — Studies "Sparse Topology-Aware Pairwise Scoring" for "Large-Scale Multi-Agent Reinforcement Learning".
- **[Strat-Reasoner: Reinforcing Strategic Reasoning of LLMs in Multi-Agent Games](https://icml.cc/virtual/2026/poster/63649)** — Introduces **Strat-Reasoner** to examine study "Reinforcing Strategic Reasoning of LLMs" in "Multi-Agent Games".
- **[Systematic Failures in Collective Reasoning under Distributed Information in Multi-Agent LLMs](https://icml.cc/virtual/2026/poster/62206)** — Studies "Systematic Failures" in "Collective Reasoning under Distributed Information in Multi-Agent LLMs".
- **[TABX: A High-Throughput Sandbox Battle Simulator for Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/62035)** — Introduces **TABX** for "Multi-Agent Reinforcement Learning", focusing on "High-Throughput Sandbox Battle Simulator".
- **[TACTIC: Task-Aware Sparse Coordination Graphs for Multi-Task Multi-agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/66706)** — Introduces **TACTIC** for "Multi-Task Multi-agent Reinforcement Learning", focusing on "Task-Aware Sparse Coordination Graphs".
- **[Talk, Judge, Cooperate: Gossip-Driven Indirect Reciprocity in Self-Interested LLM Agents](https://icml.cc/virtual/2026/poster/62130)** — Introduces **Talk, Judge, Cooperate** to examine study "Gossip-Driven Indirect Reciprocity" in "Self-Interested LLM Agents".
- **[TeamTR: Trust-Region Fine-Tuning for Multi-Agent LLM Coordination](https://icml.cc/virtual/2026/poster/64955)** — Introduces **TeamTR** for "Multi-Agent LLM Coordination", focusing on "Trust-Region Fine-Tuning".
- **[The Value of Variance: Mitigating Debate Collapse in Multi-Agent Systems via Uncertainty-Driven Policy Optimization](https://icml.cc/virtual/2026/poster/65638)** — Introduces **The Value of Variance**, using "Uncertainty-Driven Policy Optimization" to study "Mitigating Debate Collapse in Multi-Agent Systems".
- **[Toward Culturally Aligned LLMs through Ontology-Guided Multi-Agent Reasoning](https://icml.cc/virtual/2026/poster/62316)** — Studies "Toward Culturally Aligned LLMs", with "Ontology-Guided Multi-Agent Reasoning" as the core mechanism.
- **[Towards Complete Multi-Agent Coordination Policy Learning via Denoising Maximum Entropy Optimization](https://icml.cc/virtual/2026/poster/64327)** — Studies "Towards Complete Multi-Agent Coordination Policy Learning", with "Denoising Maximum Entropy Optimization" as the core mechanism.
- **[Weaving in the Clouds: Achieving Synergistic Collaboration among LLM Agents via Federated Learning](https://icml.cc/virtual/2026/poster/66521)** — Introduces **Weaving in the Clouds**, using "Federated Learning" to study "Achieving Synergistic Collaboration among LLM Agents".
- **[What Preferences Can—and Cannot—Predict in Multi-Agent Online Learning](https://icml.cc/virtual/2026/poster/66240)** — Studies "What Preferences Can—and Cannot—Predict" in "Multi-Agent Online Learning".
- **[When LLMs Develop Languages: Symbolic Communication for Efficient Multi-Agent Reasoning](https://icml.cc/virtual/2026/poster/61557)** — Introduces **When LLMs Develop Languages** for "Efficient Multi-Agent Reasoning", focusing on "Symbolic Communication".
- **[When Planning Fails Despite Correct Execution: On Epistemic Calibration for LLM-Based Multi-Agent Systems](https://icml.cc/virtual/2026/poster/65821)** — Introduces **When Planning Fails Despite Correct Execution** for "LLM-Based Multi-Agent Systems", focusing on "On Epistemic Calibration".
- **[Which LLM Multi-Agent Protocol to Choose?](https://icml.cc/virtual/2026/poster/65129)** — Frames "Which LLM Multi-Agent Protocol to Choose?" as the key question and probes agent capabilities or failure modes.

<a id="tool-use-training-rl"></a>
### 🛠️ 3. Tool Use, Training & RL (58)

The shift from prompt-based agents to trainable agents, including tool-use RL, agentic RL, GRPO, trajectory-SFT, self-evolution, and distillation.

- **[Agent Learning via Early Experience](https://icml.cc/virtual/2026/poster/64488)** — Trains/optimizes "Agent Learning", with "Early Experience" as the core mechanism.
- **[Agent World Model: Infinity Synthetic Environments for Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/64306)** — Introduces **Agent World Model** for "Agentic Reinforcement Learning", focusing on "Infinity Synthetic Environments".
- **[Agent-Omit: Training Efficient LLM Agents for Adaptive Thought and Observation Omission via Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/63271)** — Introduces **Agent-Omit**, using "Agentic Reinforcement Learning" to train "Efficient LLM Agents for Adaptive Thought and Observation Omission".
- **[Agent0-VL: Exploring Self-Evolving Agent for Tool-Integrated Vision-Language Reasoning](https://icml.cc/virtual/2026/poster/63095)** — Introduces **Agent0-VL** for "Tool-Integrated Vision-Language Reasoning", focusing on "Exploring Self-Evolving Agent".
- **[Agentic Monte Carlo: Reinforcement Learning for Black-Box LLM Agents](https://icml.cc/virtual/2026/poster/62740)** — Introduces **Agentic Monte Carlo** for "Black-Box LLM Agents", focusing on "Reinforcement Learning".
- **[AuTAgent: A Reinforcement Learning Framework for Tool-Augmented Audio Reasoning](https://icml.cc/virtual/2026/poster/64128)** — Introduces **AuTAgent** for "Tool-Augmented Audio Reasoning", focusing on "Reinforcement Learning Framework".
- **[AutoTool: Dynamic Tool Selection and Integration for Agentic Reasoning](https://icml.cc/virtual/2026/poster/65574)** — Introduces **AutoTool** for "Agentic Reasoning", focusing on "Dynamic Tool Selection and Integration".
- **[Beyond Static Endpoints: Tool Programs as an Interface for Flexible Agentic Web Services](https://icml.cc/virtual/2026/poster/62527)** — Introduces **Beyond Static Endpoints** for "Flexible Agentic Web Services", focusing on "Tool Programs as an Interface".
- **[Bootstrapped Exploration with Causal Reasoning: A Training Paradigm for Adaptive Forecasting Agent](https://icml.cc/virtual/2026/poster/65944)** — Introduces **Bootstrapped Exploration with Causal Reasoning** for "Adaptive Forecasting Agent", focusing on "Training Paradigm".
- **[Can Agents Generalize to the Open World? Unveiling the Fragility of Static Training in Tool Use](https://icml.cc/virtual/2026/poster/65179)** — Frames "Can Agents Generalize to the Open World? Unveiling the Fragility of Static Training in Tool Use" as the key question and probes agent capabilities or failure modes.
- **[CRPO: Character-centric Group Relative Policy Optimization for Role-aware Reasoning in Role-playing Agents](https://icml.cc/virtual/2026/poster/62395)** — Introduces **CRPO** to examine study "Character-centric Group Relative Policy Optimization for Role-aware Reasoning" in "Role-playing Agents".
- **[D-CORE: Incentivizing Task Decomposition in Large Reasoning Models for Complex Tool Use](https://icml.cc/virtual/2026/poster/61056)** — Introduces **D-CORE** to examine study "Incentivizing Task Decomposition" in "Large Reasoning Models for Complex Tool Use".
- **[Data Agent: Learning to Select Data via End-to-End Dynamic Optimization](https://icml.cc/virtual/2026/poster/62583)** — Introduces **Data Agent**, using "End-to-End Dynamic Optimization" to learn "to Select Data".
- **[DIVE: Scaling Diversity in Agentic Task Synthesis for Generalizable Tool Use](https://icml.cc/virtual/2026/poster/66305)** — Introduces **DIVE** to examine scale "Diversity" in "Agentic Task Synthesis for Generalizable Tool Use".
- **[Diversity Over Frequency: Rethinking Tool Use in Visual Chain-of-Thought Agents](https://icml.cc/virtual/2026/poster/61111)** — Introduces **Diversity Over Frequency** to examine study "Rethinking Tool Use" in "Visual Chain-of-Thought Agents".
- **[Dynamic Optimizations of LLM Ensembles with Two-Stage Reinforcement Learning Agents](https://icml.cc/virtual/2026/poster/64593)** — Trains/optimizes "Dynamic Optimizations of LLM Ensembles" and incorporates "Two-Stage Reinforcement Learning Agents".
- **[EvoC2F: Compiling Tool Orchestration for Efficient and Evolvable LLM Agents](https://icml.cc/virtual/2026/poster/63166)** — Introduces **EvoC2F** for "Efficient and Evolvable LLM Agents", focusing on "Compiling Tool Orchestration".
- **[ExSkill: Continual Learning from Experience and Skills in Multimodal Agents](https://icml.cc/virtual/2026/poster/65729)** — Introduces **ExSkill** to examine study "Continual Learning from Experience and Skills" in "Multimodal Agents".
- **[FactGuard: Agentic Video Misinformation Detection via Reinforcement Learning](https://icml.cc/virtual/2026/poster/65720)** — Introduces **FactGuard**, using "Reinforcement Learning" to study "Agentic Video Misinformation Detection".
- **[Fourier Features Let Agents Learn High Precision Policies with Imitation Learning](https://icml.cc/virtual/2026/poster/60655)** — Trains/optimizes "Fourier Features Let Agents Learn High Precision Policies" and incorporates "Imitation Learning".
- **[From Interactions to Principles: Experience-Driven Self-Distillation for Evolving LLM Agents](https://icml.cc/virtual/2026/poster/65641)** — Introduces **From Interactions to Principles** for "Evolving LLM Agents", focusing on "Experience-Driven Self-Distillation".
- **[FT-Dojo: Towards Autonomous LLM Fine-Tuning with Language Agents](https://icml.cc/virtual/2026/poster/63475)** — Introduces **FT-Dojo** by incorporating "Language Agents" into move toward "Autonomous LLM Fine-Tuning".
- **[GLARE: Scalable Neuro-Symbolic Reward Shaping for LLM Agents via Group-Level Automata](https://icml.cc/virtual/2026/poster/66450)** — Introduces **GLARE**, using "Group-Level Automata" to study "Scalable Neuro-Symbolic Reward Shaping for LLM Agents".
- **[Goal-Conditioned Agents that Learn Everything All at Once](https://icml.cc/virtual/2026/poster/61317)** — Trains/optimizes "Goal-Conditioned Agents that Learn Everything All at Once".
- **[Graph-R1: Towards Agentic GraphRAG Framework via End-to-end Reinforcement Learning](https://icml.cc/virtual/2026/poster/63269)** — Introduces **Graph-R1**, using "End-to-end Reinforcement Learning" to move toward "Agentic GraphRAG Framework".
- **[GRPO-based Cluster Decision Agent for Unknown-$\boldsymbol{K}$ Multi-view Clustering](https://icml.cc/virtual/2026/poster/62944)** — Trains/optimizes "GRPO-based Cluster Decision Agent" for "Unknown-$\boldsymbol{K}$ Multi-view Clustering".
- **[HiPER: Hierarchical Plan–Execute RL for Multi-Turn LLM Agents](https://icml.cc/virtual/2026/poster/64058)** — Introduces **HiPER** for "Multi-Turn LLM Agents", focusing on "Hierarchical Plan–Execute RL".
- **[Imitation Learning for Multi-turn LM Agents via On-policy Expert Corrections](https://icml.cc/virtual/2026/poster/61984)** — Trains/optimizes "Imitation Learning for Multi-turn LM Agents", with "On-policy Expert Corrections" as the core mechanism.
- **[InfoPO: Information-Driven Policy Optimization for User-Centric Agents](https://icml.cc/virtual/2026/poster/64385)** — Introduces **InfoPO** for "User-Centric Agents", focusing on "Information-Driven Policy Optimization".
- **[IntentRL: Training Proactive User-intent Agents for Open-ended Deep Research via Reinforcement Learning](https://icml.cc/virtual/2026/poster/61305)** — Introduces **IntentRL**, using "Reinforcement Learning" to train "Proactive User-intent Agents for Open-ended Deep Research".
- **[Just-In-Time Reinforcement Learning: Continual Learning in LLM Agents Without Gradient Updates](https://icml.cc/virtual/2026/poster/61517)** — Introduces **Just-In-Time Reinforcement Learning** to examine study "Continual Learning" in "LLM Agents Without Gradient Updates".
- **[Large Language Model Agents Are Not Always Faithful Self-Evolvers](https://icml.cc/virtual/2026/poster/62034)** — Trains/optimizes "Large Language Model Agents Are Not Always Faithful Self-Evolvers".
- **[Learning Task-Sufficient World Models by Synergizing Agentic Exploration and Structured Modeling](https://icml.cc/virtual/2026/poster/64209)** — Trains/optimizes "Learning Task-Sufficient World Models", with "Synergizing Agentic Exploration and Structured Modeling" as the core mechanism.
- **[Learning to Explore: Scaling Agentic Reasoning via Exploration-Aware Policy Optimization](https://icml.cc/virtual/2026/poster/63287)** — Introduces **Learning to Explore**, using "Exploration-Aware Policy Optimization" to scale "Agentic Reasoning".
- **[LLM4Cov: Execution-Grounded Agent Learning for High-Coverage Hardware Verification](https://icml.cc/virtual/2026/poster/61436)** — Introduces **LLM4Cov** for "High-Coverage Hardware Verification", focusing on "Execution-Grounded Agent Learning".
- **[On Effectiveness and Efficiency of Agentic Tool-calling and RL Training](https://icml.cc/virtual/2026/poster/66433)** — Trains/optimizes "On Effectiveness and Efficiency of Agentic Tool-calling and RL Training".
- **[On Group Relative Policy Optimization Collapse in Agent Search: The Lazy Likelihood-Displacement](https://icml.cc/virtual/2026/poster/63945)** — Introduces **On Group Relative Policy Optimization Collapse in Agent Search** around "Lazy Likelihood-Displacement".
- **[Persistent Semantic Entities in Tool-Augmented LLM Systems](https://icml.cc/virtual/2026/poster/60521)** — Trains/optimizes "Persistent Semantic Entities" in "Tool-Augmented LLM Systems".
- **[Phase-Aware Mixture of Experts for Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/64382)** — Trains/optimizes "Phase-Aware Mixture of Experts" for "Agentic Reinforcement Learning".
- **[Post-Training LLMs as Better Decision-Making Agents: A Regret-Minimization Approach](https://icml.cc/virtual/2026/poster/62760)** — Introduces **Post-Training LLMs as Better Decision-Making Agents** around "Regret-Minimization Approach".
- **[PosterAgent: Agentic Poster Generation via Stage-Aware Reinforcement Learning](https://icml.cc/virtual/2026/poster/62650)** — Introduces **PosterAgent**, using "Stage-Aware Reinforcement Learning" to study "Agentic Poster Generation".
- **[Process Reward Agents for Steering Knowledge-Intensive Reasoning](https://icml.cc/virtual/2026/poster/66434)** — Trains/optimizes "Process Reward Agents" for "Steering Knowledge-Intensive Reasoning".
- **[PyVision-RL: Forging Open Agentic Vision Models via RL](https://icml.cc/virtual/2026/poster/65374)** — Introduces **PyVision-RL**, using "RL" to study "Forging Open Agentic Vision Models".
- **[Rationality Measurement and Theory for Reinforcement Learning Agents](https://icml.cc/virtual/2026/poster/64009)** — Trains/optimizes "Rationality Measurement and Theory" for "Reinforcement Learning Agents".
- **[ReSeek: A Self-Correcting Framework for Search Agents with Instructive Rewards](https://icml.cc/virtual/2026/poster/63905)** — Introduces **ReSeek** by incorporating "Instructive Rewards" into study "Self-Correcting Framework for Search Agents".
- **[ScaleEnv: Scaling Environment Synthesis from Scratch for Generalist Interactive Tool-Use Agent Training](https://icml.cc/virtual/2026/poster/66374)** — Introduces **ScaleEnv** for "Generalist Interactive Tool-Use Agent Training", focusing on "Scaling Environment Synthesis from Scratch".
- **[SEAgent: Self-Evolving Computer Use Agent with Autonomous Learning from Experience](https://icml.cc/virtual/2026/poster/65711)** — Introduces **SEAgent** by incorporating "Autonomous Learning from Experience" into study "Self-Evolving Computer Use Agent".
- **[Self-Evolving LLM Agents under Offline Data Support](https://icml.cc/virtual/2026/poster/62030)** — Trains/optimizes "Self-Evolving LLM Agents under Offline Data Support".
- **[Stratified GRPO: Handling Structural Heterogeneity in Reinforcement Learning of LLM Search Agents](https://icml.cc/virtual/2026/poster/63159)** — Introduces **Stratified GRPO** to examine study "Handling Structural Heterogeneity" in "Reinforcement Learning of LLM Search Agents".
- **[Student-Centered Distillation Narrows the Agentic Gap Between Small and Large LLMs](https://icml.cc/virtual/2026/poster/64717)** — Trains/optimizes "Student-Centered Distillation Narrows the Agentic Gap Between Small and Large LLMs".
- **[T$^2$PO: Uncertainty-Guided Exploration Control for Stable Multi-Turn Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/63090)** — Introduces **T$^2$PO** for "Stable Multi-Turn Agentic Reinforcement Learning", focusing on "Uncertainty-Guided Exploration Control".
- **[This State Looks Like That: Self-Interpretable Reinforcement Learning Agents using Prototype Soft Actor-Critic](https://icml.cc/virtual/2026/poster/62377)** — Introduces **This State Looks Like That**, using "Prototype Soft Actor-Critic" to study "Self-Interpretable Reinforcement Learning Agents".
- **[TodoEvolve: Learning to Architect Agent Planning Systems](https://icml.cc/virtual/2026/poster/64136)** — Introduces **TodoEvolve** around "Learning to Architect Agent Planning Systems".
- **[Towards Pareto-Optimal Tool-Integrated Agents with Pareto Ranking Policy Optimization](https://icml.cc/virtual/2026/poster/65819)** — Trains/optimizes "Towards Pareto-Optimal Tool-Integrated Agents" and incorporates "Pareto Ranking Policy Optimization".
- **[Training LLM Agents to Empower Humans](https://icml.cc/virtual/2026/poster/61627)** — Trains/optimizes "Training LLM Agents to Empower Humans".
- **[Understanding Reasoning Collapse in LLM Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/66821)** — Trains/optimizes "Understanding Reasoning Collapse" in "LLM Agent Reinforcement Learning".
- **[What Does Vision Tool-Use Reinforcement Learning Really Learn? Disentangling Tool-Induced and Intrinsic Effects for Crop-and-Zoom](https://icml.cc/virtual/2026/poster/62232)** — Frames "What Does Vision Tool-Use Reinforcement Learning Really Learn? Disentangling Tool-Induced and Intrinsic Effects for Crop-and-Zoom" as the key question and probes agent capabilities or failure modes.
- **[Words Towards Explainability: Caption Label-Free Learning via Dual Loop Agentic Time Series Captioning](https://icml.cc/virtual/2026/poster/64438)** — Introduces **Words Towards Explainability**, using "Dual Loop Agentic Time Series Captioning" to study "Caption Label-Free Learning".

<a id="safety-security-governance"></a>
### 🛡️ 4. Safety, Security & Governance (51)

Multi-turn attacks, tool poisoning, environment corruptions, privacy leakage, refusal boundaries, red-teaming, runtime monitoring, and guardrails.

- **[A New Framework for Cybersecurity Refusals in AI Agents](https://icml.cc/virtual/2026/poster/61093)** — Proposes a new framework for "Cybersecurity Refusals" in "AI Agents".
- **[AdvEvo-MARL: Shaping Internalized Safety through Adversarial Co-Evolution in Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/66275)** — Introduces **AdvEvo-MARL**, using "Adversarial Co-Evolution in Multi-Agent Reinforcement Learning" to study "Shaping Internalized Safety".
- **[AIR: Improving Agent Safety through Incident Response](https://icml.cc/virtual/2026/poster/62353)** — Introduces **AIR**, using "Incident Response" to improve "Agent Safety".
- **[Architecture Matters for Multi-Agent Security](https://icml.cc/virtual/2026/poster/64792)** — Studies how architectural choices affect "Multi-Agent Security".
- **[Are Your Agents Upward Deceivers?](https://icml.cc/virtual/2026/poster/62581)** — Frames "Are Your Agents Upward Deceivers?" as the key question and probes agent capabilities or failure modes.
- **[AutoRAS: Learning Robust Agentic Systems with Primitive Representations](https://icml.cc/virtual/2026/poster/66006)** — Introduces **AutoRAS** by incorporating "Primitive Representations" into learn "Robust Agentic Systems".
- **[BlueCodeAgent: A Blue Teaming Agent Powered by Automated Red Teaming for CodeGen AI](https://icml.cc/virtual/2026/poster/63820)** — Introduces **BlueCodeAgent**, using "Automated Red Teaming for CodeGen AI" to study "Blue Teaming Agent Powered".
- **[Causal Detection of Multi-Step LLM Agent Attacks](https://icml.cc/virtual/2026/poster/64714)** — Studies "Causal Detection of Multi-Step LLM Agent Attacks".
- **[Clarify Before You Draw: Proactive Agents for Robust Text-to-CAD Generation](https://icml.cc/virtual/2026/poster/66672)** — Introduces **Clarify Before You Draw** for "Robust Text-to-CAD Generation", focusing on "Proactive Agents".
- **[Co-RedTeam: Orchestrated Security Discovery and Exploitation with LLM Agents](https://icml.cc/virtual/2026/poster/60747)** — Introduces **Co-RedTeam** by incorporating "LLM Agents" into study "Orchestrated Security Discovery and Exploitation".
- **[Contextualized Privacy Defense for LLM Agents](https://icml.cc/virtual/2026/poster/62996)** — Studies "Contextualized Privacy Defense" for "LLM Agents".
- **[CVE-Factory: Scaling Expert-Level Agentic Tasks for Code Security Vulnerability](https://icml.cc/virtual/2026/poster/65622)** — Introduces **CVE-Factory** for "Code Security Vulnerability", focusing on "Scaling Expert-Level Agentic Tasks".
- **[EMBGUARD: Constructing Hazard-Aware Guardrails for Safe Planning in Embodied Agents](https://icml.cc/virtual/2026/poster/63023)** — Introduces **EMBGUARD** to examine study "Constructing Hazard-Aware Guardrails for Safe Planning" in "Embodied Agents".
- **[Functional Cache Grafting: Robust and Rapid Code-Policy Synthesis for Embodied Agents](https://icml.cc/virtual/2026/poster/62313)** — Introduces **Functional Cache Grafting** for "Embodied Agents", focusing on "Robust and Rapid Code-Policy Synthesis".
- **[Interaction-Breaking Adversarial Learning Framework for Robust Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/61001)** — Studies "Interaction-Breaking Adversarial Learning Framework" for "Robust Multi-Agent Reinforcement Learning".
- **[Learning When to Act or Refuse: Guarding Agentic Reasoning Models for Safe Multi-Step Tool Use](https://icml.cc/virtual/2026/poster/63878)** — Introduces **Learning When to Act or Refuse** for "Safe Multi-Step Tool Use", focusing on "Guarding Agentic Reasoning Models".
- **[MaMa: A Game-Theoretic Approach for Designing Safe Agentic Systems](https://icml.cc/virtual/2026/poster/64729)** — Introduces **MaMa** for "Designing Safe Agentic Systems", focusing on "Game-Theoretic Approach".
- **[MEMO: Memory-Augmented Model Context Optimization for Robust Multi-Turn Multi-Agent LLM Games](https://icml.cc/virtual/2026/poster/62950)** — Introduces **MEMO** for "Robust Multi-Turn Multi-Agent LLM Games", focusing on "Memory-Augmented Model Context Optimization".
- **[MINIM: Privacy-Aware Minimal View for Agents via Trusted Local Sanitization](https://icml.cc/virtual/2026/poster/61306)** — Introduces **MINIM**, using "Trusted Local Sanitization" to study "Privacy-Aware Minimal View for Agents".
- **[OrchJail: Jailbreaking Tool-Calling Text-to-Image Agents by Orchestration-Guided Fuzzing](https://icml.cc/virtual/2026/poster/63568)** — Introduces **OrchJail**, using "Orchestration-Guided Fuzzing" to study "Jailbreaking Tool-Calling Text-to-Image Agents".
- **[OTora: A Unified Red Teaming Framework for Reasoning-Level Denial-of-Service in LLM Agents](https://icml.cc/virtual/2026/poster/61771)** — Introduces **OTora** to examine study "Unified Red Teaming Framework for Reasoning-Level Denial-of-Service" in "LLM Agents".
- **[PolicyGuard: Towards Test-time and Step-level Backdoor Defense for Reinforcement Learning Agent](https://icml.cc/virtual/2026/poster/65628)** — Introduces **PolicyGuard** for "Reinforcement Learning Agent", focusing on "Towards Test-time and Step-level Backdoor Defense".
- **[Position: Agent Security Needs Redefinition through a Holistic Framework](https://icml.cc/virtual/2026/poster/67194)** — Introduces **Position**, using "Holistic Framework" to study "Agent Security Needs Redefinition".
- **[Position: Agentic Safety is an Epistemic Property, Not a Behavioral One](https://icml.cc/virtual/2026/poster/67237)** — Introduces **Position** around "Agentic Safety is an Epistemic Property, Not a Behavioral One".
- **[Position: Collusion Risks Among AI Reasoning Agents Justify Certification Requirements for Making Market Decisions](https://icml.cc/virtual/2026/poster/67141)** — Introduces **Position** for "Making Market Decisions", focusing on "Collusion Risks Among AI Reasoning Agents Justify Certification Requirements".
- **[Position: Safety Must Precede the Deployment of Open-Ended AI Agents](https://icml.cc/virtual/2026/poster/67207)** — Introduces **Position** around "Safety Must Precede the Deployment of Open-Ended AI Agents".
- **[Position: To Defend Against Cyber Attacks, We Must Teach AI Agents to Hack](https://icml.cc/virtual/2026/poster/67161)** — Introduces **Position** to examine study "To Defend" against "Cyber Attacks, We Must Teach AI Agents to Hack".
- **[Position: When AI Decides Who Gets an Organ: Multi-Agentic AI Systems in Transplant Medicine Risk Amplifying Disparities Without Targeted Explainability and Deployment Strategies](https://icml.cc/virtual/2026/poster/67102)** — Introduces **Position** to examine study "When AI Decides Who Gets an Organ: Multi-Agentic AI Systems" in "Transplant Medicine Risk Amplifying Disparities Without Targeted Explainability and Deployment Strategies".
- **[PrivAct: Internalizing Contextual Privacy Preservation via Multi-Agent Preference Training](https://icml.cc/virtual/2026/poster/65131)** — Introduces **PrivAct**, using "Multi-Agent Preference Training" to study "Internalizing Contextual Privacy Preservation".
- **[Privacy Risks of Agentic Inferential Capabilities in Data Linkage Attacks](https://icml.cc/virtual/2026/poster/64683)** — Studies "Privacy Risks of Agentic Inferential Capabilities" in "Data Linkage Attacks".
- **[Profiling the Irrational Agent: Cognitive Modeling of LLM Behaviors in Sequential Jailbreaks](https://icml.cc/virtual/2026/poster/64559)** — Introduces **Profiling the Irrational Agent** to examine study "Cognitive Modeling of LLM Behaviors" in "Sequential Jailbreaks".
- **[RedDebate: Safer Responses Through Multi-Agent Red Teaming Debates](https://icml.cc/virtual/2026/poster/66085)** — Introduces **RedDebate**, using "Multi-Agent Red Teaming Debates" to study "Safer Responses".
- **[Safe and Scalable Web Agent Learning via Recreated Websites](https://icml.cc/virtual/2026/poster/60744)** — Studies "Safe and Scalable Web Agent Learning", with "Recreated Websites" as the core mechanism.
- **[SafeHarbor: Defining Precise Decision Boundaries via Hierarchical Memory-Augmented Guardrail for LLM Agent Safety](https://icml.cc/virtual/2026/poster/64556)** — Introduces **SafeHarbor**, using "Hierarchical Memory-Augmented Guardrail for LLM Agent Safety" to study "Defining Precise Decision Boundaries".
- **[SafeSearch: Automated Red-Teaming of LLM-Based Search Agents](https://icml.cc/virtual/2026/poster/65893)** — Introduces **SafeSearch** around "Automated Red-Teaming of LLM-Based Search Agents".
- **[Secure Multi-agent Reinforcement Learning for Service Systems with Affinity and Byzantine Nodes: Stability Analysis and Protection Design](https://icml.cc/virtual/2026/poster/62838)** — Introduces **Secure Multi-agent Reinforcement Learning for Service Systems with Affinity and Byzantine Nodes** around "Stability Analysis and Protection Design".
- **[SkillTrojan: Backdoor Attacks on Skill-Based Agent Systems](https://icml.cc/virtual/2026/poster/65209)** — Introduces **SkillTrojan** to examine study "Backdoor Attacks" on "Skill-Based Agent Systems".
- **[SOPE: Situation-Aware and Statistically Indistinguishable Privacy Exfiltration for MCP-enabled Agents](https://icml.cc/virtual/2026/poster/64028)** — Introduces **SOPE** for "MCP-enabled Agents", focusing on "Situation-Aware and Statistically Indistinguishable Privacy Exfiltration".
- **[Speculative Safety Honeypot: Toward Proactive Defense Against Multi-turn Agent Attacks](https://icml.cc/virtual/2026/poster/65283)** — Introduces **Speculative Safety Honeypot** to examine move toward "Proactive Defense" against "Multi-turn Agent Attacks".
- **[Sponge Tool Attack: Stealthy Denial-of-Efficiency against Tool-Augmented Agentic Reasoning](https://icml.cc/virtual/2026/poster/62486)** — Introduces **Sponge Tool Attack** to examine study "Stealthy Denial-of-Efficiency" against "Tool-Augmented Agentic Reasoning".
- **[The Oversight Game: Learning to Cooperatively Balance an AI Agent's Safety and Autonomy](https://icml.cc/virtual/2026/poster/64439)** — Introduces **The Oversight Game** around "Learning to Cooperatively Balance an AI Agent's Safety and Autonomy".
- **[Think Twice Before You Act: Enhancing Agent Behavioral Safety with Thought Correction](https://icml.cc/virtual/2026/poster/60736)** — Introduces **Think Twice Before You Act** by incorporating "Thought Correction" into enhance "Agent Behavioral Safety".
- **[Think Twice Before You Act: Protecting LLM Agents Against Tool Description Poisoning via Isolated Planning](https://icml.cc/virtual/2026/poster/62116)** — Introduces **Think Twice Before You Act**, using "Isolated Planning" to protect "LLM Agents Against Tool Description Poisoning".
- **[TRACER: Trajectory Risk Aggregation for Critical Episodes in Agentic Reasoning](https://icml.cc/virtual/2026/poster/61608)** — Introduces **TRACER** to examine study "Trajectory Risk Aggregation for Critical Episodes" in "Agentic Reasoning".
- **[Training Language Model Agents to Find Vulnerabilities with CTF-Dojo](https://icml.cc/virtual/2026/poster/61783)** — Studies "Training Language Model Agents to Find Vulnerabilities" and incorporates "CTF-Dojo".
- **[VideoTemp-o3: Harmonizing Temporal Grounding and Video Understanding in Agentic Thinking-with-Videos](https://icml.cc/virtual/2026/poster/65425)** — Introduces **VideoTemp-o3** to examine study "Harmonizing Temporal Grounding and Video Understanding" in "Agentic Thinking-with-Videos".
- **[Vulnerable Agent Identification in Large-Scale Multi-Agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/64200)** — Studies "Vulnerable Agent Identification" in "Large-Scale Multi-Agent Reinforcement Learning".
- **[Watermarking LLM Agent Trajectories](https://icml.cc/virtual/2026/poster/62387)** — Studies "Watermarking LLM Agent Trajectories".
- **[When Agents Go Rogue: Activation-Based Detection of Malicious Behaviors in Multi-Agent Systems](https://icml.cc/virtual/2026/poster/65619)** — Introduces **When Agents Go Rogue** to examine study "Activation-Based Detection of Malicious Behaviors" in "Multi-Agent Systems".
- **[When Benign Inputs Lead to Severe Harms: Eliciting Unsafe Unintended Behaviors of Computer-Use Agents](https://icml.cc/virtual/2026/poster/64242)** — Introduces **When Benign Inputs Lead to Severe Harms** around "Eliciting Unsafe Unintended Behaviors of Computer-Use Agents".
- **[When Embedding-Based Defenses Fail: Rethinking Safety in LLM-Based Multi-Agent Systems](https://icml.cc/virtual/2026/poster/62170)** — Introduces **When Embedding-Based Defenses Fail** to examine study "Rethinking Safety" in "LLM-Based Multi-Agent Systems".

<a id="theory-behavior-interpretability"></a>
### 🧠 5. Theory, Behavior & Interpretability (39)

More conceptual agent questions: goal-directedness, empowerment, oversight, behavioral representations, calibration, interpretability, and reliability science.

- **[A World in Pieces: Structural Certification of General Agents](https://icml.cc/virtual/2026/poster/65633)** — Introduces **A World in Pieces** around "Structural Certification of General Agents".
- **[ABSINT-AI: Agentic Heap Abstractions for Abstract Interpretation](https://icml.cc/virtual/2026/poster/61550)** — Introduces **ABSINT-AI** for "Abstract Interpretation", focusing on "Agentic Heap Abstractions".
- **[Agentic Confidence Calibration](https://icml.cc/virtual/2026/poster/65705)** — Studies "Agentic Confidence Calibration".
- **[AgentVocab: Structure-Aware Vocabulary Adaptation for Efficient LLM Agents](https://icml.cc/virtual/2026/poster/61748)** — Introduces **AgentVocab** for "Efficient LLM Agents", focusing on "Structure-Aware Vocabulary Adaptation".
- **[Backjump-on-Graph: Empowering LLMs with Reinforced Retrospective Exploration for Agentic KG Reasoning](https://icml.cc/virtual/2026/poster/61995)** — Introduces **Backjump-on-Graph** by incorporating "Reinforced Retrospective Exploration for Agentic KG Reasoning" into study "Empowering LLMs".
- **[Can LLM Agents Stick to the Script? Modeling Commitment in Interactive Narratives](https://icml.cc/virtual/2026/poster/64786)** — Frames "Can LLM Agents Stick to the Script? Modeling Commitment in Interactive Narratives" as the key question and probes agent capabilities or failure modes.
- **[Characterizing Agents in Production](https://icml.cc/virtual/2026/poster/61834)** — Characterizes "Agents" in "Production".
- **[DeepHA: Scaling Action Chains Elicits Deep Hierarchical Agents](https://icml.cc/virtual/2026/poster/66241)** — Introduces **DeepHA** around "Scaling Action Chains Elicits Deep Hierarchical Agents".
- **[effGen: Enabling Small Language Models as Capable Autonomous Agents](https://icml.cc/virtual/2026/poster/63516)** — Introduces **effGen** around "Enabling Small Language Models as Capable Autonomous Agents".
- **[Estimating the Empowerment of Language Model Agents](https://icml.cc/virtual/2026/poster/61343)** — Studies "Estimating the Empowerment of Language Model Agents".
- **[FormAct: Agentic Source Editing for Rich-Format Document Generation](https://icml.cc/virtual/2026/poster/61769)** — Introduces **FormAct** for "Rich-Format Document Generation", focusing on "Agentic Source Editing".
- **[FormalJudge: A Neuro-Symbolic Paradigm for Agentic Oversight](https://icml.cc/virtual/2026/poster/61086)** — Introduces **FormalJudge** for "Agentic Oversight", focusing on "Neuro-Symbolic Paradigm".
- **[GRASP: Graph Reasoning via Agentic Solving and Probing of LLMs](https://icml.cc/virtual/2026/poster/61718)** — Introduces **GRASP**, using "Agentic Solving and Probing of LLMs" to study "Graph Reasoning".
- **[Guideline-Grounded Evidence Accumulation for High-Stakes Agent Verification](https://icml.cc/virtual/2026/poster/65243)** — Studies "Guideline-Grounded Evidence Accumulation" for "High-Stakes Agent Verification".
- **[Helpful to a Fault: Measuring Illicit Assistance in Multi-Turn, Multilingual LLM Agents](https://icml.cc/virtual/2026/poster/61155)** — Introduces **Helpful to a Fault** to examine study "Measuring Illicit Assistance" in "Multi-Turn, Multilingual LLM Agents".
- **[MarketSim: Simulating Stock Markets with Large-Scale Generative Agents](https://icml.cc/virtual/2026/poster/65297)** — Introduces **MarketSim** by incorporating "Large-Scale Generative Agents" into study "Simulating Stock Markets".
- **[MARS: Modular Agent with Reflective Search for Automated AI Research](https://icml.cc/virtual/2026/poster/61408)** — Introduces **MARS** by incorporating "Reflective Search for Automated AI Research" into study "Modular Agent".
- **[Numina-Lean-Agent: An Open and General Agentic Reasoning System for Formal Mathematics](https://icml.cc/virtual/2026/poster/66755)** — Introduces **Numina-Lean-Agent** for "Formal Mathematics", focusing on "Open and General Agentic Reasoning System".
- **[OpenHA: A Series of Open-Source Hierarchical Agentic Models in Minecraft](https://icml.cc/virtual/2026/poster/66679)** — Introduces **OpenHA** to examine study "Series of Open-Source Hierarchical Agentic Models" in "Minecraft".
- **[Opt-Miner: Empowering Information-Seeking Agent with Tree-Guided Data Synthesis for Optimization Modeling](https://icml.cc/virtual/2026/poster/65154)** — Introduces **Opt-Miner** by incorporating "Tree-Guided Data Synthesis for Optimization Modeling" into study "Empowering Information-Seeking Agent".
- **[PACE: Proactive Agent-Level Admission Control for Efficient Agentic Batch Inference](https://icml.cc/virtual/2026/poster/63743)** — Introduces **PACE** for "Efficient Agentic Batch Inference", focusing on "Proactive Agent-Level Admission Control".
- **[Position: Accountable Deployment of Agentic AI Demands Layered, System-Level Interpretability](https://icml.cc/virtual/2026/poster/67088)** — Introduces **Position** around "Accountable Deployment of Agentic AI Demands Layered, System-Level Interpretability".
- **[Position: Agentic AI Is a Foreseeable Pathway to AGI](https://icml.cc/virtual/2026/poster/67083)** — Introduces **Position** around "Agentic AI Is a Foreseeable Pathway to AGI".
- **[Position: Agentic AI systems should be making Bayes-consistent decisions](https://icml.cc/virtual/2026/poster/67041)** — Introduces **Position** around "Agentic AI systems should be making Bayes-consistent decisions".
- **[Position: Agentic Systems Should be General](https://icml.cc/virtual/2026/poster/67137)** — Introduces **Position** around "Agentic Systems Should be General".
- **[Position: Assistive Agents Need Accessibility Alignment](https://icml.cc/virtual/2026/poster/67129)** — Introduces **Position** around "Assistive Agents Need Accessibility Alignment".
- **[Position: Beyond Prediction: Toward Verifiable Physiological Waveform Reasoning with Foundation Models and Agentic LLMs](https://icml.cc/virtual/2026/poster/67119)** — Introduces **Position** by incorporating "Foundation Models and Agentic LLMs" into study "Beyond Prediction: Toward Verifiable Physiological Waveform Reasoning".
- **[Position: Collaborative Agentic AI Needs Interoperability Across Ecosystems](https://icml.cc/virtual/2026/poster/67223)** — Introduces **Position** around "Collaborative Agentic AI Needs Interoperability Across Ecosystems".
- **[Position: Digital Agents Require Unified Agent-Native Environments](https://icml.cc/virtual/2026/poster/67134)** — Introduces **Position** around "Digital Agents Require Unified Agent-Native Environments".
- **[Position: LLM Agents Are the Antidote to Walled Gardens](https://icml.cc/virtual/2026/poster/67081)** — Introduces **Position** around "LLM Agents Are the Antidote to Walled Gardens".
- **[Position: Preregister Experiments with AI Agents](https://icml.cc/virtual/2026/poster/67108)** — Introduces **Position** by incorporating "AI Agents" into study "Preregister Experiments".
- **[Position: World Models as an Intermediary between Agents and the Real World](https://icml.cc/virtual/2026/poster/67241)** — Introduces **Position** around "World Models as an Intermediary between Agents and the Real World".
- **[PragLocker: Protecting Agent Intellectual Property in Untrusted Deployments via Non-Portable Prompts](https://icml.cc/virtual/2026/poster/64248)** — Introduces **PragLocker**, using "Non-Portable Prompts" to protect "Agent Intellectual Property in Untrusted Deployments".
- **[Probabilistic Modeling of Latent Agentic Substructures in Deep Neural Networks](https://icml.cc/virtual/2026/poster/61223)** — Studies "Probabilistic Modeling of Latent Agentic Substructures" in "Deep Neural Networks".
- **[Pushing Forward Pareto Frontiers of Proactive Agents with Behavioral Agentic Optimization](https://icml.cc/virtual/2026/poster/61493)** — Studies "Pushing Forward Pareto Frontiers of Proactive Agents" and incorporates "Behavioral Agentic Optimization".
- **[Scaling Small Agents Through Strategy Auctions](https://icml.cc/virtual/2026/poster/62642)** — Studies "Scaling Small Agents", with "Strategy Auctions" as the core mechanism.
- **[Scaling the Scaling Logic: Agentic Meta-Synthesis of Logic Reasoning](https://icml.cc/virtual/2026/poster/66221)** — Introduces **Scaling the Scaling Logic** around "Agentic Meta-Synthesis of Logic Reasoning".
- **[Think Fast and Slow: Step-Level Cognitive Depth Adaptation for LLM Agents](https://icml.cc/virtual/2026/poster/63105)** — Introduces **Think Fast and Slow** for "LLM Agents", focusing on "Step-Level Cognitive Depth Adaptation".
- **[When AI Agents Compete for Jobs: Strategic Capabilities and Economic Dynamics of AI Labour Markets](https://icml.cc/virtual/2026/poster/66152)** — Introduces **When AI Agents Compete for Jobs** around "Strategic Capabilities and Economic Dynamics of AI Labour Markets".

<a id="scientific-domain-agents"></a>
### 🔬 6. Scientific & Domain Agents (30)

Agents for data science, finance, medicine, biosecurity, CAD/circuits/robotics, retrosynthesis, enterprise operations, and other domain workflows.

- **[Agentic Framework for Epidemiological Modeling](https://icml.cc/virtual/2026/poster/60990)** — Introduces for domain workflows "Agentic Framework" for "Epidemiological Modeling".
- **[AutoMat: Physics-Guided Agentic Reasoning for Solving Ill-Posed Inverse Microscopy Problems](https://icml.cc/virtual/2026/poster/63827)** — Introduces **AutoMat** for "Solving Ill-Posed Inverse Microscopy Problems", focusing on "Physics-Guided Agentic Reasoning".
- **[AutoSizer: Automatic Sizing of Analog and Mixed-Signal Circuits via Large Language Model (LLM) Agents](https://icml.cc/virtual/2026/poster/66562)** — Introduces **AutoSizer**, using "Large Language Model (LLM) Agents" to study "Automatic Sizing of Analog and Mixed-Signal Circuits".
- **[CocoRNA: Collective RNA Design with Cooperative Multi-agent Reinforcement Learning](https://icml.cc/virtual/2026/poster/65353)** — Introduces **CocoRNA** by incorporating "Cooperative Multi-agent Reinforcement Learning" into study "Collective RNA Design".
- **[Constitutional Black-Box Monitoring for Scheming in LLM Agents](https://icml.cc/virtual/2026/poster/65104)** — Introduces for domain workflows "Constitutional Black-Box Monitoring" for "Scheming in LLM Agents".
- **[Cycle-of-Science: Reliable Reasoning through Counterfactual Verification for Agent Decision Making](https://icml.cc/virtual/2026/poster/64408)** — Introduces **Cycle-of-Science**, using "Counterfactual Verification for Agent Decision Making" to study "Reliable Reasoning".
- **[Debate2Create: Robot Co-design via Multi-Agent LLM Debate](https://icml.cc/virtual/2026/poster/66635)** — Introduces **Debate2Create**, using "Multi-Agent LLM Debate" to study "Robot Co-design".
- **[DeepAnalyze: Agentic Large Language Models for Autonomous Data Science](https://icml.cc/virtual/2026/poster/61106)** — Introduces **DeepAnalyze** for "Autonomous Data Science", focusing on "Agentic Large Language Models".
- **[EngiAgent: Fully Connected Coordination of LLM Agents for Solving Open-ended Engineering Problems with Feasible Solutions](https://icml.cc/virtual/2026/poster/66645)** — Introduces **EngiAgent** by incorporating "Feasible Solutions" into study "Fully Connected Coordination of LLM Agents for Solving Open-ended Engineering Problems".
- **[From Conflict to Consensus: Boosting Medical Reasoning via Multi-Round Agentic RAG](https://icml.cc/virtual/2026/poster/63972)** — Introduces **From Conflict to Consensus**, using "Multi-Round Agentic RAG" to study "Boosting Medical Reasoning".
- **[LAGEA: Language Guided Embodied Agents for Robotic Manipulation](https://icml.cc/virtual/2026/poster/60801)** — Introduces **LAGEA** for "Robotic Manipulation", focusing on "Language Guided Embodied Agents".
- **[Learning Human-Robot Collaboration via Heterogeneous-Agent Lyapunov Policy Optimization](https://icml.cc/virtual/2026/poster/61049)** — Introduces for domain workflows "Learning Human-Robot Collaboration", with "Heterogeneous-Agent Lyapunov Policy Optimization" as the core mechanism.
- **[LiveFigure: Generating Editable Scientific Illustration with VLM Agents](https://icml.cc/virtual/2026/poster/62974)** — Introduces **LiveFigure** by incorporating "VLM Agents" into study "Generating Editable Scientific Illustration".
- **[Meta Context Engineering via Agentic Skill Evolution](https://icml.cc/virtual/2026/poster/64296)** — Introduces for domain workflows "Meta Context Engineering", with "Agentic Skill Evolution" as the core mechanism.
- **[ML-Agent: Reinforcing LLM Agents for Autonomous Machine Learning Engineering](https://icml.cc/virtual/2026/poster/62020)** — Introduces **ML-Agent** for "Autonomous Machine Learning Engineering", focusing on "Reinforcing LLM Agents".
- **[Ophiuchus: Incentivizing Tool-augmented ''Think with Images'' for Joint Medical Segmentation, Understanding and Reasoning](https://icml.cc/virtual/2026/poster/62829)** — Introduces **Ophiuchus** by incorporating "Images'' for Joint Medical Segmentation, Understanding and Reasoning" into study "Incentivizing Tool-augmented ''Think".
- **[PDAgent: An LLM-Driven Autonomous Agent Framework Towards *In Silico* Protein Design via Directed Mutation](https://icml.cc/virtual/2026/poster/63768)** — Introduces **PDAgent**, using "Directed Mutation" to study "LLM-Driven Autonomous Agent Framework Towards *In Silico* Protein Design".
- **[Position: Academic Conferences are Potentially Facing Denominator Gaming Caused by Fully Automated Scientific Agents](https://icml.cc/virtual/2026/poster/67236)** — Introduces **Position**, using "Fully Automated Scientific Agents" to study "Academic Conferences are Potentially Facing Denominator Gaming Caused".
- **[Position: Agent Should Invoke External Tools ONLY When Epistemically Necessary](https://icml.cc/virtual/2026/poster/67227)** — Introduces **Position** around "Agent Should Invoke External Tools ONLY When Epistemically Necessary".
- **[Position: The Age of AI Agents Demands A New Scientific Paradigm To Sustain Trustworthy Science](https://icml.cc/virtual/2026/poster/67156)** — Introduces **Position** around "Age of AI Agents Demands A New Scientific Paradigm To Sustain Trustworthy Science".
- **[Principled Zero-shot Ranking Agents with Tournament Graphs](https://icml.cc/virtual/2026/poster/62762)** — Introduces for domain workflows "Principled Zero-shot Ranking Agents" and incorporates "Tournament Graphs".
- **[Reinforcement Learning for Tool-Calling Agents in Fast Healthcare Interoperability Resources (FHIR)](https://icml.cc/virtual/2026/poster/65318)** — Introduces for domain workflows "Reinforcement Learning" for "Tool-Calling Agents in Fast Healthcare Interoperability Resources (FHIR)".
- **[RetrOrchestrator: A Multi-Step Retrosynthesis Agent Dynamically Orchestrating Single-Step Transition Models](https://icml.cc/virtual/2026/poster/61540)** — Introduces **RetrOrchestrator** around "Multi-Step Retrosynthesis Agent Dynamically Orchestrating Single-Step Transition Models".
- **[Small Agent Group is the Future of Digital Health](https://icml.cc/virtual/2026/poster/65768)** — Introduces for domain workflows "Small Agent Group is the Future of Digital Health".
- **[SPADA: A Verifiable Test-Driven Agent for Controllable Parametric CAD Assembly Generation](https://icml.cc/virtual/2026/poster/62308)** — Introduces **SPADA** for "Controllable Parametric CAD Assembly Generation", focusing on "Verifiable Test-Driven Agent".
- **[Textual Stochastic Gradient Descent: Discrete Optimization of External Memory for Reasoning Language Agents](https://icml.cc/virtual/2026/poster/60510)** — Introduces **Textual Stochastic Gradient Descent** for "Reasoning Language Agents", focusing on "Discrete Optimization of External Memory".
- **[Threat2Traffic: Multi-Agent Environment Synthesis for Malware Traffic Generation from Threat Intelligence](https://icml.cc/virtual/2026/poster/64510)** — Introduces **Threat2Traffic** for "Malware Traffic Generation from Threat Intelligence", focusing on "Multi-Agent Environment Synthesis".
- **[Toward Ultra-Long-Horizon Agentic Science: Cognitive Accumulation for Autonomous Machine Learning Engineering](https://icml.cc/virtual/2026/poster/66663)** — Introduces **Toward Ultra-Long-Horizon Agentic Science** for "Autonomous Machine Learning Engineering", focusing on "Cognitive Accumulation".
- **[Towards a Science of AI Agent Reliability](https://icml.cc/virtual/2026/poster/66364)** — Introduces for domain workflows "Towards a Science of AI Agent Reliability".
- **[Why Specialist Models Still Matter: A Heterogeneous Multi-Agent Paradigm for Medical Artificial Intelligence](https://icml.cc/virtual/2026/poster/60481)** — Introduces **Why Specialist Models Still Matter** for "Medical Artificial Intelligence", focusing on "Heterogeneous Multi-Agent Paradigm".

<a id="memory-context-long-horizon"></a>
### 💾 7. Memory, Context & Long-Horizon Tasks (29)

State management for long-horizon agents: trajectory compression, graph memory, context folding, lifelong conversation, and cross-session memory.

- **[$R^3$DAO: Reactive Recovery and Reconstruction for Long-horizon Data Agent Orchestration](https://icml.cc/virtual/2026/poster/64678)** — Introduces **$R^3$DAO** for "Long-horizon Data Agent Orchestration", focusing on "Reactive Recovery and Reconstruction".
- **[ACON: Optimizing Context Compression for Long-horizon LLM Agents](https://icml.cc/virtual/2026/poster/66270)** — Introduces **ACON** for "Long-horizon LLM Agents", focusing on "Optimizing Context Compression".
- **[AdaMEM: Test-Time Adaptive Memory for Language Agents](https://icml.cc/virtual/2026/poster/63989)** — Introduces **AdaMEM** for "Language Agents", focusing on "Test-Time Adaptive Memory".
- **[Beyond Trajectory-Level Attribution: Graph-Based Credit Assignment for Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/60543)** — Introduces **Beyond Trajectory-Level Attribution** for "Agentic Reinforcement Learning", focusing on "Graph-Based Credit Assignment".
- **[De-Linearizing Agent Traces: Bayesian Inference of Latent Partial Orders for Efficient Execution](https://icml.cc/virtual/2026/poster/63737)** — Introduces **De-Linearizing Agent Traces** for "Efficient Execution", focusing on "Bayesian Inference of Latent Partial Orders".
- **[Experience-Evolving Multi-Turn Tool-Use Agent with Hybrid Episodic–Procedural Memory](https://icml.cc/virtual/2026/poster/64271)** — Introduces "Experience-Evolving Multi-Turn Tool-Use Agent" and incorporates "Hybrid Episodic–Procedural Memory".
- **[ExpWeaver: LLM Agents Learn from Experience via Latent RAG](https://icml.cc/virtual/2026/poster/66387)** — Introduces **ExpWeaver**, using "Latent RAG" to study "LLM Agents Learn from Experience".
- **[From Outcomes to Actions: Leveraging Hindsight for Long-Horizon Language Agent Training](https://icml.cc/virtual/2026/poster/62250)** — Introduces **From Outcomes to Actions** for "Long-Horizon Language Agent Training", focusing on "Leveraging Hindsight".
- **[From Player to Master: Enhancing Test-Time Learning of LLM Agents via Reinforcement Learning over Memory](https://icml.cc/virtual/2026/poster/62463)** — Introduces **From Player to Master**, using "Reinforcement Learning over Memory" to enhance "Test-Time Learning of LLM Agents".
- **[JADE: Bridging the Strategic-Operational Gap in Dynamic Agentic RAG](https://icml.cc/virtual/2026/poster/64731)** — Introduces **JADE** to examine study "Bridging the Strategic-Operational Gap" in "Dynamic Agentic RAG".
- **[Learning Query-Aware Budget-Tier Routing for Runtime Agent Memory](https://icml.cc/virtual/2026/poster/66266)** — Introduces "Learning Query-Aware Budget-Tier Routing" for "Runtime Agent Memory".
- **[Learning to Share: Selective Memory for Efficient Parallel Agentic Systems](https://icml.cc/virtual/2026/poster/62890)** — Introduces **Learning to Share** for "Efficient Parallel Agentic Systems", focusing on "Selective Memory".
- **[Lifting Traces to Logic: Programmatic Skill Induction with Neuro-Symbolic Learning for Long-Horizon Agentic Tasks](https://icml.cc/virtual/2026/poster/65500)** — Introduces **Lifting Traces to Logic** by incorporating "Neuro-Symbolic Learning for Long-Horizon Agentic Tasks" into study "Programmatic Skill Induction".
- **[LRAgent: Efficient KV Cache Sharing for Multi-LoRA LLM Agents](https://icml.cc/virtual/2026/poster/61572)** — Introduces **LRAgent** for "Multi-LoRA LLM Agents", focusing on "Efficient KV Cache Sharing".
- **[Mem-T: Densifying Rewards for Long-Horizon Memory Agents](https://icml.cc/virtual/2026/poster/65925)** — Introduces **Mem-T** for "Long-Horizon Memory Agents", focusing on "Densifying Rewards".
- **[MemEvolve: Meta-Evolution of Agent Memory Systems](https://icml.cc/virtual/2026/poster/61379)** — Introduces **MemEvolve** around "Meta-Evolution of Agent Memory Systems".
- **[Memory is Reconstructed, Not Retrieved: Graph Memory for LLM Agents](https://icml.cc/virtual/2026/poster/60697)** — Introduces **Memory is Reconstructed, Not Retrieved** for "LLM Agents", focusing on "Graph Memory".
- **[Milestone-Guided Policy Learning for Long-Horizon Language Agents](https://icml.cc/virtual/2026/poster/65128)** — Introduces "Milestone-Guided Policy Learning" for "Long-Horizon Language Agents".
- **[ParamMem: Augmenting Language Agents with Parametric Reflective Memory](https://icml.cc/virtual/2026/poster/61133)** — Introduces **ParamMem** by incorporating "Parametric Reflective Memory" into study "Augmenting Language Agents".
- **[PlugMem: A Task-Agnostic Plugin Memory Module for LLM Agents](https://icml.cc/virtual/2026/poster/64446)** — Introduces **PlugMem** for "LLM Agents", focusing on "Task-Agnostic Plugin Memory Module".
- **[Position: Modular Memory is the Key to Continual Learning Agents](https://icml.cc/virtual/2026/poster/67101)** — Introduces **Position** around "Modular Memory is the Key to Continual Learning Agents".
- **[ProcMEM: Learning Reusable Procedural Memory from Experience via Non-Parametric PPO for LLM Agents](https://icml.cc/virtual/2026/poster/65830)** — Introduces **ProcMEM**, using "Non-Parametric PPO for LLM Agents" to learn "Reusable Procedural Memory from Experience".
- **[RE-TRAC: REcursive TRAjectory Compression for Deep Search Agents](https://icml.cc/virtual/2026/poster/60790)** — Introduces **RE-TRAC** for "Deep Search Agents", focusing on "REcursive TRAjectory Compression".
- **[RGMem: Renormalization Group–inspired Memory Evolution for Language Agents](https://icml.cc/virtual/2026/poster/65195)** — Introduces **RGMem** for "Language Agents", focusing on "Renormalization Group–inspired Memory Evolution".
- **[Scaling Long-Horizon Agent via Context Folding](https://icml.cc/virtual/2026/poster/61950)** — Introduces "Scaling Long-Horizon Agent", with "Context Folding" as the core mechanism.
- **[SimpleMem: Efficient Lifelong Memory for LLM Agents](https://icml.cc/virtual/2026/poster/61640)** — Introduces **SimpleMem** for "LLM Agents", focusing on "Efficient Lifelong Memory".
- **[Training-Free Hierarchical Working Memory for Small Language Model Agents](https://icml.cc/virtual/2026/poster/63532)** — Introduces "Training-Free Hierarchical Working Memory" for "Small Language Model Agents".
- **[Tvcache: A Tool-Value Cache for Post-Training LLM Agents](https://icml.cc/virtual/2026/poster/61148)** — Introduces **Tvcache** for "Post-Training LLM Agents", focusing on "Tool-Value Cache".
- **[What Do Agents Learn from Trajectory-SFT: Semantics or Interfaces?](https://icml.cc/virtual/2026/poster/61062)** — Introduces **What Do Agents Learn from Trajectory-SFT** around "Semantics or Interfaces?".

<a id="coding-swe-theorem-proving"></a>
### 💻 8. Coding, SWE & Theorem Proving (27)

Repository-level software tasks, CUDA/Triton/kernel generation, full-stack development, vulnerability discovery, coding environments, and theorem proving.

- **[A Minimal Agent for Automated Theorem Proving](https://icml.cc/virtual/2026/poster/64174)** — Introduces/evaluates "Minimal Agent" for "Automated Theorem Proving".
- **[ADEPT: RL-Aligned Agentic Decoding of Emotion via Evidence Probing Tools — From Consensus Learning to Ambiguity-Driven Emotion Reasoning](https://icml.cc/virtual/2026/poster/61830)** — Introduces **ADEPT**, using "Evidence Probing Tools — From Consensus Learning to Ambiguity-Driven Emotion Reasoning" to study "RL-Aligned Agentic Decoding of Emotion".
- **[AgentConductor: Topology Evolution for Multi-Agent Competition-Level Code Generation](https://icml.cc/virtual/2026/poster/66333)** — Introduces **AgentConductor** for "Multi-Agent Competition-Level Code Generation", focusing on "Topology Evolution".
- **[Agora: Toward Autonomous Bug Detection in Production-Level Consensus Protocols with LLM Agents](https://icml.cc/virtual/2026/poster/64937)** — Introduces **Agora** by incorporating "LLM Agents" into move toward "Autonomous Bug Detection in Production-Level Consensus Protocols".
- **[daVinci-Dev: Agent-native Mid-training for Software Engineering](https://icml.cc/virtual/2026/poster/63099)** — Introduces **daVinci-Dev** for "Software Engineering", focusing on "Agent-native Mid-training".
- **[DOCKSMITH: Scaling Reliable Coding Environments via an Agentic Docker Builder](https://icml.cc/virtual/2026/poster/61127)** — Introduces **DOCKSMITH**, using "Agentic Docker Builder" to scale "Reliable Coding Environments".
- **[EGG: An Expert-Guided Agent Framework for Kernel Generation](https://icml.cc/virtual/2026/poster/65929)** — Introduces **EGG**, a framework for "Kernel Generation".
- **[FullStack-Agent: Enhancing Agentic Full-Stack Web Coding via Development-Oriented Testing and Repository Back-Translation](https://icml.cc/virtual/2026/poster/60686)** — Introduces **FullStack-Agent**, using "Development-Oriented Testing and Repository Back-Translation" to enhance "Agentic Full-Stack Web Coding".
- **[How can we assess human-agent interactions? Case studies in software agent design](https://icml.cc/virtual/2026/poster/64319)** — Frames "How can we assess human-agent interactions? Case studies in software agent design" as the key question and probes agent capabilities or failure modes.
- **[Just Ask: Curious Code Agents Reveal System Prompts in Frontier LLMs](https://icml.cc/virtual/2026/poster/61428)** — Introduces **Just Ask** to examine study "Curious Code Agents Reveal System Prompts" in "Frontier LLMs".
- **[Large-Scale Terminal Agentic Trajectory Generation from Dockerized Environments](https://icml.cc/virtual/2026/poster/64240)** — Introduces/evaluates "Large-Scale Terminal Agentic Trajectory Generation from Dockerized Environments".
- **[MemDecoder: Enhancing Test-Time Compute for LLM Agents via Reinforced Memory Decoding](https://icml.cc/virtual/2026/poster/65523)** — Introduces **MemDecoder**, using "Reinforced Memory Decoding" to enhance "Test-Time Compute for LLM Agents".
- **[MulFCoder: Framework-conditioned Multi-agent for MLLM-based Multi-framework Front-end Code Generation](https://icml.cc/virtual/2026/poster/60693)** — Introduces **MulFCoder** for "MLLM-based Multi-framework Front-end Code Generation", focusing on "Framework-conditioned Multi-agent".
- **[NEMO: Execution-Aware Optimization Modeling via Autonomous Coding Agents](https://icml.cc/virtual/2026/poster/66684)** — Introduces **NEMO**, using "Autonomous Coding Agents" to study "Execution-Aware Optimization Modeling".
- **[One Tool Is Enough: Reinforcement Learning of LLM Agents for Repository-Level Code Navigation](https://icml.cc/virtual/2026/poster/63517)** — Introduces **One Tool Is Enough** for "Repository-Level Code Navigation", focusing on "Reinforcement Learning of LLM Agents".
- **[OpenSage: Self-programming Agent Generation Engine](https://icml.cc/virtual/2026/poster/66121)** — Introduces **OpenSage** around "Self-programming Agent Generation Engine".
- **[ParEVO: Synthesizing Code for Irregular Data: High-Performance Parallelism through Agentic Evolution](https://icml.cc/virtual/2026/poster/61756)** — Introduces **ParEVO**, using "Agentic Evolution" to study "Synthesizing Code for Irregular Data: High-Performance Parallelism".
- **[Scaling Agentic Verifier for Competitive Coding](https://icml.cc/virtual/2026/poster/65948)** — Introduces/evaluates "Scaling Agentic Verifier" for "Competitive Coding".
- **[SERA: Soft-Verified Efficient Repository Agents](https://icml.cc/virtual/2026/poster/65153)** — Introduces **SERA** around "Soft-Verified Efficient Repository Agents".
- **[StitchCUDA: An Automated Multi-Agents End-to-End GPU Programing Framework with Rubric-based Agentic Reinforcement Learning](https://icml.cc/virtual/2026/poster/64924)** — Introduces **StitchCUDA** by incorporating "Rubric-based Agentic Reinforcement Learning" into study "Automated Multi-Agents End-to-End GPU Programing Framework".
- **[Structurally Aligned Subtask-Level Memory for Software Engineering Agents](https://icml.cc/virtual/2026/poster/66605)** — Introduces/evaluates "Structurally Aligned Subtask-Level Memory" for "Software Engineering Agents".
- **[SWE-MiniSandbox: Container-Free Reinforcement Learning for Building Software Engineering Agents](https://icml.cc/virtual/2026/poster/61850)** — Introduces **SWE-MiniSandbox** for "Building Software Engineering Agents", focusing on "Container-Free Reinforcement Learning".
- **[ThunderAgent: A Fast, Simple, and Program-Aware Agentic Inference System](https://icml.cc/virtual/2026/poster/62040)** — Introduces **ThunderAgent** around "Fast, Simple, and Program-Aware Agentic Inference System".
- **[TOM-SWE: User Mental Modeling For Software Engineering Agents](https://icml.cc/virtual/2026/poster/65025)** — Introduces **TOM-SWE** for "Software Engineering Agents", focusing on "User Mental Modeling".
- **[Toward Training Superintelligent Software Agents through Self-Play SWE-RL](https://icml.cc/virtual/2026/poster/66747)** — Introduces/evaluates "Toward Training Superintelligent Software Agents", with "Self-Play SWE-RL" as the core mechanism.
- **[Towards Feedback-to-Plan Decisions for Self-Evolving LLM Agents in CUDA Kernel Generation](https://icml.cc/virtual/2026/poster/61256)** — Introduces/evaluates "Towards Feedback-to-Plan Decisions" for "Self-Evolving LLM Agents in CUDA Kernel Generation".
- **[Why Agentic Theorem Prover Works: A Statistical Provability Theory of Mathematical Reasoning Models](https://icml.cc/virtual/2026/poster/62379)** — Introduces **Why Agentic Theorem Prover Works** around "Statistical Provability Theory of Mathematical Reasoning Models".

<a id="gui-web-computer-use"></a>
### 🖥️ 9. GUI, Web & Computer-Use (13)

Web, desktop, mobile GUI, and computer-use agents, including environment synthesis, trajectory pretraining, action correction, robustness, and safety.

- **[Agent JIT Compilation for Latency-Optimizing Computer-Use Agent Planning and Scheduling](https://icml.cc/virtual/2026/poster/66062)** — Introduces/evaluates "Agent JIT Compilation" for "Latency-Optimizing Computer-Use Agent Planning and Scheduling".
- **[CAPTCHA Solving for Native GUI Agents: Automated Reasoning-Action Data Generation and Self-Corrective Training](https://icml.cc/virtual/2026/poster/65034)** — Introduces **CAPTCHA Solving for Native GUI Agents** around "Automated Reasoning-Action Data Generation and Self-Corrective Training".
- **[Continual GUI Agents](https://icml.cc/virtual/2026/poster/66053)** — Introduces/evaluates "Continual GUI Agents".
- **[Darwinian Memory: A Training-Free Self-Regulating Memory System for GUI Agent Evolution](https://icml.cc/virtual/2026/poster/61134)** — Introduces **Darwinian Memory** for "GUI Agent Evolution", focusing on "Training-Free Self-Regulating Memory System".
- **[Executable Agentic Memory for GUI Agent](https://icml.cc/virtual/2026/poster/65931)** — Introduces/evaluates "Executable Agentic Memory" for "GUI Agent".
- **[Faithful Mobile GUI Agents with Guided Advantage Estimator](https://icml.cc/virtual/2026/poster/63413)** — Introduces/evaluates "Faithful Mobile GUI Agents" and incorporates "Guided Advantage Estimator".
- **[Next-Gen CAPTCHAs: Leveraging the Cognitive Gap for Scalable and Diverse GUI-Agent Defense](https://icml.cc/virtual/2026/poster/60816)** — Introduces **Next-Gen CAPTCHAs** for "Scalable and Diverse GUI-Agent Defense", focusing on "Leveraging the Cognitive Gap".
- **[Position: Web Agents Should Use Typed Actions Instead of Click-Based Browsing](https://icml.cc/virtual/2026/poster/67155)** — Introduces **Position** around "Web Agents Should Use Typed Actions Instead of Click-Based Browsing".
- **[SE-GA: Memory-Augmented Self-Evolution for GUI Agents](https://icml.cc/virtual/2026/poster/65853)** — Introduces **SE-GA** for "GUI Agents", focusing on "Memory-Augmented Self-Evolution".
- **[Video2GUI: Synthesizing Large-Scale Interaction Trajectories for Generalized GUI Agent Pretraining](https://icml.cc/virtual/2026/poster/62028)** — Introduces **Video2GUI** for "Generalized GUI Agent Pretraining", focusing on "Synthesizing Large-Scale Interaction Trajectories".
- **[Weasel: Out-of-Domain Generalization for Web Agents via Importance-Diversity Data Selection](https://icml.cc/virtual/2026/poster/65342)** — Introduces **Weasel**, using "Importance-Diversity Data Selection" to study "Out-of-Domain Generalization for Web Agents".
- **[WebWorld: A Large-Scale World Model for Web Agent Training](https://icml.cc/virtual/2026/poster/65352)** — Introduces **WebWorld** for "Web Agent Training", focusing on "Large-Scale World Model".
- **[When Actions Go Off-Task: Detecting and Correcting Misaligned Actions in Computer-Use Agents](https://icml.cc/virtual/2026/poster/64196)** — Introduces **When Actions Go Off-Task** to examine detect and correct "Misaligned Actions" in "Computer-Use Agents".

<a id="multimodal-embodied-interactive"></a>
### 🎥 10. Multimodal, Embodied & Interactive Agents (11)

Agentic reasoning connected to VLM/VLA, video, audio, navigation, spatial reasoning, active perception, and embodied manipulation.

- **[Active Exploring like a Pigeon: Reinforcing Spatial Reasoning via Agentic Vision-Language Models](https://icml.cc/virtual/2026/poster/61450)** — Introduces **Active Exploring like a Pigeon**, using "Agentic Vision-Language Models" to study "Reinforcing Spatial Reasoning".
- **[DR-MMSearchAgent: Deepening Reasoning in Multimodal Search Agents](https://icml.cc/virtual/2026/poster/66547)** — Introduces **DR-MMSearchAgent** to examine study "Deepening Reasoning" in "Multimodal Search Agents".
- **[Failure is Feedback: History-Aware Backtracking for Agentic Traversal in Multimodal Graphs](https://icml.cc/virtual/2026/poster/60560)** — Introduces **Failure is Feedback** to examine study "History-Aware Backtracking for Agentic Traversal" in "Multimodal Graphs".
- **[Hierarchical Procedural Meta-Reasoning for Generalizable Multimodal Agents](https://icml.cc/virtual/2026/poster/60959)** — Studies "Hierarchical Procedural Meta-Reasoning" for "Generalizable Multimodal Agents".
- **[MM-DeepResearch: A Simple and Effective Multimodal Agentic Search Baseline](https://icml.cc/virtual/2026/poster/63393)** — Introduces **MM-DeepResearch** around "Simple and Effective Multimodal Agentic Search Baseline".
- **[See, Act, Adapt: Active Perception for Unsupervised Cross-Domain Visual Adaptation via Personalized VLM-Guided Agent](https://icml.cc/virtual/2026/poster/65692)** — Introduces **See, Act, Adapt**, using "Personalized VLM-Guided Agent" to study "Active Perception for Unsupervised Cross-Domain Visual Adaptation".
- **[SP-Mind: An Autonomous Reasoning Agent for Spatial Proteomics Analysis](https://icml.cc/virtual/2026/poster/63717)** — Introduces **SP-Mind** for "Spatial Proteomics Analysis", focusing on "Autonomous Reasoning Agent".
- **[Strategic Navigation or Stochastic Search? How Agents and Humans Reason Over Document Collections](https://icml.cc/virtual/2026/poster/62732)** — Frames "Strategic Navigation or Stochastic Search? How Agents and Humans Reason Over Document Collections" as the key question and probes agent capabilities or failure modes.
- **[Text Before Vision: Staged Knowledge Injection Matters for Agentic RLVR in Ultra-High-Resolution Remote Sensing Understanding](https://icml.cc/virtual/2026/poster/66614)** — Introduces **Text Before Vision** to examine study "Staged Knowledge Injection Matters for Agentic RLVR" in "Ultra-High-Resolution Remote Sensing Understanding".
- **[VIRUS: Injecting Persistent Cognitive Pathogens into Stateful Zero-Shot Object Navigation Agents](https://icml.cc/virtual/2026/poster/66293)** — Introduces **VIRUS** around "Injecting Persistent Cognitive Pathogens into Stateful Zero-Shot Object Navigation Agents".
- **[What You Think is What You See: Driving Exploration in VLM Agents via Visual-Linguistic Curiosity](https://icml.cc/virtual/2026/poster/60509)** — Introduces **What You Think is What You See**, using "Visual-Linguistic Curiosity" to study "Driving Exploration in VLM Agents".

<a id="planning-architecture-orchestration"></a>
### 🏗️ 11. Planning, Architecture & Orchestration (11)

Agent workflows, sub-agent creation, topology evolution, protocol selection, planning/execution separation, and system orchestration.

- **[Agentic Model Predictive Questioning Control in Visual Design](https://icml.cc/virtual/2026/poster/62292)** — Designs "Agentic Model Predictive Questioning Control" in "Visual Design".
- **[Agentic Proposing: Enhancing Large language Model Reasoning via Compositional Skill Synthesis](https://icml.cc/virtual/2026/poster/62973)** — Introduces **Agentic Proposing**, using "Compositional Skill Synthesis" to enhance "Large language Model Reasoning".
- **[AgentXRay: White-Boxing Agentic Systems via Workflow Reconstruction](https://icml.cc/virtual/2026/poster/65356)** — Introduces **AgentXRay**, using "Workflow Reconstruction" to study "White-Boxing Agentic Systems".
- **[AOrchestra: Automating Sub-Agent Creation for Agentic Orchestration](https://icml.cc/virtual/2026/poster/65930)** — Introduces **AOrchestra** for "Agentic Orchestration", focusing on "Automating Sub-Agent Creation".
- **[EvoMAS: Heuristics in the Loop—Evolving Smarter Agentic Workflows](https://icml.cc/virtual/2026/poster/62843)** — Introduces **EvoMAS** to examine study "Heuristics" in "Loop—Evolving Smarter Agentic Workflows".
- **[FlowMAP: Flow Matching for Generalizable Agent Planning](https://icml.cc/virtual/2026/poster/63407)** — Introduces **FlowMAP** for "Generalizable Agent Planning", focusing on "Flow Matching".
- **[GraphFlow: A Graph-Based Workflow Management for Efficient LLM-Agent Serving](https://icml.cc/virtual/2026/poster/66432)** — Introduces **GraphFlow** for "Efficient LLM-Agent Serving", focusing on "Graph-Based Workflow Management".
- **[Hermes: An Evidence-Driven Agentic Framework for Trustworthy and Explainable AI-Generated Video Detection](https://icml.cc/virtual/2026/poster/61817)** — Introduces **Hermes**, a framework for "Trustworthy and Explainable AI-Generated Video Detection".
- **[Probing the Knowledge Boundary: An Interactive Agentic Framework for Deep Knowledge Extraction](https://icml.cc/virtual/2026/poster/62443)** — Introduces **Probing the Knowledge Boundary**, a framework for "Deep Knowledge Extraction".
- **[VideoSEAL: Separating Planning from Answer Authority for Agentic Long Video Understanding](https://icml.cc/virtual/2026/poster/64001)** — Introduces **VideoSEAL** for "Agentic Long Video Understanding", focusing on "Separating Planning from Answer Authority".
- **[When Replanning Becomes the Bottleneck: Budgeted Replanning for Embodied Agents](https://icml.cc/virtual/2026/poster/63603)** — Introduces **When Replanning Becomes the Bottleneck** for "Embodied Agents", focusing on "Budgeted Replanning".

<a id="conversation-assistant-interaction"></a>
### 💬 12. Conversation & Assistant Interaction (4)

Clarification, question asking, utility/cost tradeoffs, full-duplex voice, and task-oriented interaction policies for conversational agents.

- **[Mitigating Conversational Inertia in Multi-Turn Agents](https://icml.cc/virtual/2026/poster/63848)** — Studies "Mitigating Conversational Inertia" in "Multi-Turn Agents".
- **[Reinforcing Real-world Service Agents: Balancing Utility and Cost in Task-oriented Dialogue](https://icml.cc/virtual/2026/poster/65380)** — Introduces **Reinforcing Real-world Service Agents** to examine study "Balancing Utility and Cost" in "Task-oriented Dialogue".
- **[Teaching Agents to Ask Effective Clarification Questions](https://icml.cc/virtual/2026/poster/63224)** — Studies "Teaching Agents to Ask Effective Clarification Questions".
- **[Uncertainty-Aware Clarification in LLM Agents with Information Gain](https://icml.cc/virtual/2026/poster/66065)** — Studies "Uncertainty-Aware Clarification in LLM Agents" and incorporates "Information Gain".

<a id="data-files"></a>
