
# Awesome Environment — Papers on Agent Environments & Task Synthesis

English | [简体中文](readme.md)

> Scope: publicly available papers and open-source repos (2021–2026) on **agent environment synthesis, task synthesis, data synthesis, verifiers & benchmark measurement, and sandbox infrastructure**.
> Sources: arXiv, OpenReview / top venues (ICML, NeurIPS, ICLR, ACL, EMNLP, CVPR, CoRL, ICSE, FSE, ISSTA, NDSS, ACL Findings, COLM, ICRA, etc.), Semantic Scholar / Crossref / OpenAlex / DBLP, GitHub and AI paper platforms.
> **639 papers / entries** across 18 categorized sections plus an appendix, plus **121 open-source repos, infrastructures and awesome lists**; this round adds four sections: data synthesis, embodied/robotic, multi-agent/social simulation, and open-source projects.

---

## 1. Difficulty, Benchmark Measurement & Verification Reliability

| Paper Title | Link | Key Points | Status |
|---|---|---|---|
| A Matter of TASTE: Improving Coverage and Difficulty of Agent Benchmarks | [arXiv:2605.28556](https://arxiv.org/abs/2605.28556) | Procedurally generates harder tasks; performance on τ²-Bench Verified drops by -5% to -80% | ✅ Confirmed |
| AgentBoard: An Analytical Evaluation Board of Multi-turn LLM Agents | [arXiv:2401.13178](https://arxiv.org/abs/2401.13178) | Splits difficulty into easy/hard by sub-goal; proposes a progress-rate metric | ✅ Confirmed |
| τ²-Bench: Evaluating Conversational Agents in a Dual-Control Environment | [arXiv:2506.07982](https://arxiv.org/abs/2506.07982) | Dual-control architecture + compositional task generator; the Telecom dual-control domain is modeled as a Dec-POMDP; **ICML 2026 Oral** | ✅ Confirmed, venue added |
| τ-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains | [arXiv:2406.12045](https://arxiv.org/abs/2406.12045) | LLM-simulated user converses with the agent under domain policies; efficient and faithful evaluation by comparing final database state; predecessor of τ²-Bench | ✅ New, confirmed |
| Easy2Hard-Bench: Standardized Difficulty Labels | [arXiv:2409.18433](https://arxiv.org/abs/2409.18433) | Standardized difficulty labels; NeurIPS 2024 | ✅ Confirmed |
| Benchmarks as Microscopes: A Call for Model Metrology | [arXiv:2407.16711](https://arxiv.org/abs/2407.16711) | Defines difficulty as a measurable property of the model; **COLM 2024** | ✅ Confirmed, venue added |
| Curriculum RL from Easy to Hard | [arXiv:2506.06632](https://arxiv.org/abs/2506.06632) | Curriculum-style RL training paradigm that goes from easy to hard | ✅ Confirmed |
| Cheap Reward Hacking Detection | [arXiv:2606.08893](https://arxiv.org/abs/2606.08893) | Verifier-side difficulty research and reward-hacking detection | ✅ Confirmed |
| Do Agent Benchmarks Measure Capability? Protocol Validity | [arXiv:2607.22368](https://arxiv.org/abs/2607.22368) | Reward hacking is equivalent to benchmark verification failure; Tencent Hunyuan team | ✅ Confirmed |
| World Feedback for Clinical Agents (MAB-v3) | [arXiv:2607.01470](https://arxiv.org/abs/2607.01470) | Hardening clinical agent environments; performance-ceiling analysis; **ICML 2026** | ✅ Confirmed, venue added |
| EnviSAgE: A Survey of Environment Scaling | [arXiv:2511.09586](https://arxiv.org/abs/2511.09586) | Survey on environment scaling; proposes the three-stage GEF loop | ✅ Confirmed |
| **Predicting Task Difficulty Without Rollouts** | [arXiv:2608.05797](https://arxiv.org/abs/2608.05797) | Predicts intrinsic task difficulty without rollouts, saving compute for environment designers and curriculum builders | ✅ New, confirmed |
| **Why Do LLM Agents Fail in Exploring New Environments?** | [arXiv:2510.15047](https://arxiv.org/abs/2510.15047) | Identifies exploration collapse (Pass@1 edges up while Pass@k drops sharply during RL); diagnosed from a world-modeling perspective; **EMNLP 2026 Findings** | ✅ New, confirmed |
| **Reward Hacking Benchmark (RHB)** | [arXiv:2605.02964](https://arxiv.org/abs/2605.02964) | Multi-step tool tasks with naturalistic shortcuts (skipping verification, inferring answers from task-adjacent metadata, tampering with evaluation functions); **ICML 2026** | ✅ New, confirmed |
| **Hack-Verifiable Environments (HVE)** | [arXiv:2605.20744](https://arxiv.org/abs/2605.20744) | Plants detectable hacks into tasks so reward hacking can be identified automatically and reliably | ✅ New, confirmed |
| **SpecBench** | [arXiv:2605.21384](https://arxiv.org/abs/2605.21384) | Decomposes SWE tasks into specification, visible validation tests and hidden tests to measure reward hacking in long-horizon coding agents | ✅ New, confirmed |
| **Hack-Verifiable Terminal Bench** | [arXiv:2608.22103](https://arxiv.org/abs/2608.22103) | Applies the HVE methodology to terminal tasks, replacing unreliable human / LLM judgement with automatic detection | ✅ New, confirmed |
| **BAITBENCH** | [arXiv:2608.30724](https://arxiv.org/abs/2608.30724) | Three synthetic tabular ML tasks each containing a shortcut that inflates reported metrics | ✅ New, confirmed |
| **EvilGenie** | [arXiv:2511.21654](https://arxiv.org/abs/2511.21654) | Programming environments that are easy to reward-hack (hardcoded tests, edited test files); three-way cross-validation with held-out unit tests, LLM judges and test-file edit detection | ✅ New, confirmed |
| **Scalable Weak-to-Strong Verifier Hardening** | [arXiv:2610.15924](https://arxiv.org/abs/2610.15924) | Automatically repairs exploitable verifiers with scaled compute via weak-to-strong transfer | ✅ New, confirmed |
| **Audit Where Hacks Pay** | [arXiv:2610.35716](https://arxiv.org/abs/2610.35716) | Budgeted strong-verifier audits against reward hacking in GRPO, locating where the payoff comes from | ✅ New, confirmed |
| **Diagnosing and Correcting Reward Hacking in Verifiable Instruction Following** | [arXiv:2610.19525](https://arxiv.org/abs/2610.19525) | Diagnoses and corrects reward hacking in verifiable instruction-following settings | ✅ New, confirmed |
| **Reward Hacking as a Transmissible Strategy** | [arXiv:2610.12822](https://arxiv.org/abs/2610.12822) | Shows reward hacking can propagate as a transmissible strategy in multi-agent coding systems | ✅ New, confirmed |
| **Detecting and Suppressing Reward Hacking with Gradient Fingerprints** | [arXiv:2604.16242](https://arxiv.org/abs/2604.16242) | Gradient fingerprints for detecting and suppressing reward hacking; **COLM 2026** | ✅ New, confirmed |
| **Benchmarking Reward Hack Detection in Code Environments** | [arXiv:2601.20103](https://arxiv.org/abs/2601.20103) | Benchmarks reward-hack detection in code environments via contrastive analysis | ✅ New, confirmed |
| **Reward Hacking Challenges Oversight of Autonomous Research Agents** | [arXiv:2609.28614](https://arxiv.org/abs/2609.28614) | Shows reward hacking in autonomous research agents undermines human oversight | ✅ New, confirmed |
| **Agent Island** | [arXiv:2605.04312](https://arxiv.org/abs/2605.04312) | Multiplayer simulation yielding a dynamic benchmark resistant to saturation and contamination | ✅ New, confirmed |
| **SynAE** | [arXiv:2605.22564](https://arxiv.org/abs/2605.22564) | Framework for measuring the quality of synthetic data used to evaluate tool-calling agents | ✅ New, confirmed |
| **Search-Time Contamination (STC)** | [arXiv:2606.05241](https://arxiv.org/abs/2606.05241) | Defines three contamination types and measures performance inflation in public deep-research agent benchmarks | ✅ New, confirmed |
| **Automated Benchmark Auditing for AI Agents and LLMs** | [arXiv:2605.26079](https://arxiv.org/abs/2605.26079) | Automated auditing pipeline for agent and LLM benchmarks | ✅ New, confirmed |
| **Trial by Trace** | [arXiv:2610.32285](https://arxiv.org/abs/2610.32285) | Evaluates agent harnesses for reliability and failure attribution at trajectory granularity | ✅ New, confirmed |
| **On the Reliability of Computer Use Agents** | [arXiv:2604.17849](https://arxiv.org/abs/2604.17849) | Systematically characterizes the reliability envelope of computer-use agents | ✅ New, confirmed |
| **Multi-Agent Verification** | [arXiv:2502.20379](https://arxiv.org/abs/2502.20379) | Scales test-time compute with multiple verifiers | ✅ New, confirmed |
| **Detecting Benchmark Contamination Through Watermarking** | [arXiv:2502.17259](https://arxiv.org/abs/2502.17259) | Detects benchmark contamination via watermarking | ✅ New, confirmed |
| **Towards Contamination Resistant Benchmarks** | [arXiv:2505.08389](https://arxiv.org/abs/2505.08389) | A systematic methodology for contamination-resistant benchmarks | ✅ New, confirmed |
| **gg-bench: Measuring General Intelligence with Generated Games** | [arXiv:2505.07215](https://arxiv.org/abs/2505.07215) | LLM generates game descriptions implemented as Gym environments; a data-generating process that can emit new evaluation instances on demand | ✅ New, confirmed |
| **Verifiable Process Rewards for Agentic Reasoning** | [arXiv:2605.10325](https://arxiv.org/abs/2605.10325) | Verifiable process-level rewards for agentic reasoning | ✅ New, confirmed |
| **Beyond Binary Verifiable Rewards: Behavioral Self-Rewarding for SWE Agents** | [arXiv:2610.12598](https://arxiv.org/abs/2610.12598) | Breaks past 0/1 verifiable rewards with behavioral self-rewarding for finer-grained signals | ✅ New, confirmed |
| **AgentV-RL** | [arXiv:2604.16004](https://arxiv.org/abs/2604.16004) | Turns reward modeling into a multi-turn, tool-augmented deliberative process; **ACL 2026** | ✅ New, confirmed |
| **Agentic Rubrics as Contextual Verifiers for SWE Agents** | [arXiv:2601.04171](https://arxiv.org/abs/2601.04171) | Context-grounded rubrics replace execution-based verification, cutting environment setup overhead while staying interpretable | ✅ New, confirmed |
| **Task-Adaptive Rubrics for GUI Reward Modeling** | [arXiv:2608.24174](https://arxiv.org/abs/2608.24174) | Builds judging criteria per GUI task instance instead of transferring generic checks across tasks | ✅ New, confirmed |
| **Agentic Reward Modeling** | [arXiv:2602.00575](https://arxiv.org/abs/2602.00575) | Active, progressive trajectory-grounded interaction compensates for partial GUI state observability | ✅ New, confirmed |
| **Interactive Reward Agent** | [arXiv:2607.25904](https://arxiv.org/abs/2607.25904) | Evaluates GUI tasks via environment-state verification | ✅ New, confirmed |
| **GUI-PRA** | [arXiv:2509.23263](https://arxiv.org/abs/2509.23263) | Process reward agent for GUI tasks; supplies the domain adjudication logic standard PRMs lack | ✅ New, confirmed |
| **GUI-Shepherd** | [arXiv:2509.23738](https://arxiv.org/abs/2509.23738) | Process reward model trained on 52K annotated interactions; serves as both RL reward provider and inference-time verifier | ✅ New, confirmed |
| **VisCritic** | [arXiv:2606.24525](https://arxiv.org/abs/2606.24525) | Compares pre-action and post-action screenshots in visual feature space as process reward | ✅ New, confirmed |
| **VeriCUA** | [arXiv:2610.26469](https://arxiv.org/abs/2610.26469) | Learns proactive verification: what to check and when to stop, for reliable CUA rewards | ✅ New, confirmed |
| **AgentPRM** | [arXiv:2511.08325](https://arxiv.org/abs/2511.08325) | Process reward models from step-wise promise and progress signals | ✅ New, confirmed |
| **RLAR** | [arXiv:2603.00724](https://arxiv.org/abs/2603.00724) | An agentic reward system for multi-task RL on LLMs | ✅ New, confirmed |
| **Hybrid Reward Normalization** | [arXiv:2509.25598](https://arxiv.org/abs/2509.25598) | Hybrid reward normalization for process-supervised, non-verifiable agentic tasks | ✅ New, confirmed |
| **ARTIS** | [arXiv:2602.01709](https://arxiv.org/abs/2602.01709) | Risk-aware agentic test-time scaling via iterative simulation; **NeurIPS 2026** | ✅ New, confirmed |
| **Evaluating Test-Time Scaling of General LLM Agents** | [arXiv:2602.18998](https://arxiv.org/abs/2602.18998) | Evaluates test-time scaling gains for general LLM agents | ✅ New, confirmed |
| **Agentic Test-Time Scaling for WebAgents** | [arXiv:2602.12276](https://arxiv.org/abs/2602.12276) | Test-time scaling method for web agents | ✅ New, confirmed |
| **Scaling Test-Time Compute for Agentic Coding** | [arXiv:2604.16529](https://arxiv.org/abs/2604.16529) | Systematic study of test-time compute scaling for coding agents | ✅ New, confirmed |
| **Difficulty-Aware Agentic Orchestration** | [arXiv:2509.11079](https://arxiv.org/abs/2509.11079) | Difficulty-aware, query-specific multi-agent workflow orchestration; **WWW 2026** | ✅ New, confirmed |
| **A Rubric-Supervised Critic from Sparse Real-World Outcomes** | [arXiv:2603.03800](https://arxiv.org/abs/2603.03800) | Learns a critic from sparse, noisy human-in-the-loop outcomes; usable as an RL reward model or for inference-time scaling | ✅ New, confirmed |
| **SEABench** | [arXiv:2609.35596](https://arxiv.org/abs/2609.35596) | Benchmarks endogenous misalignment in self-evolving agents: locally useful updates can persist into unsafe later behavior | ✅ New, confirmed |
| **Query-Only Backdoor Attacks on Self-Evolving Skills** | [arXiv:2608.08303](https://arxiv.org/abs/2608.08303) | Exposes a trajectory-poisoning path to backdoor self-evolving skill systems | ✅ New, confirmed |
| **Humanize: Judgement Engineering for Agentic Coding** | [arXiv:2610.08900](https://arxiv.org/abs/2610.08900) | Multi-agent orchestration built on explicit, mechanically enforced decisions at the boundaries between planning, implementation, review and learning | ✅ New, confirmed |
| **SEVerA** | [arXiv:2603.25111](https://arxiv.org/abs/2603.25111) | The first formally verified self-evolving LLM agents, with safety and correctness guarantees for synthesized agent programs | ✅ New, confirmed |
| **TRACE** | [arXiv:2610.11678](https://arxiv.org/abs/2610.11678) | Turns score changes into testable diagnoses by perturbing one part of an evaluation, separating capability gains from verifier brittleness. | ✅ New, confirmed |
| **Computer Use at the Edge of the Statistical Precipice** | [arXiv:2605.08261](https://arxiv.org/abs/2605.08261) | A 1MB blind replay script that never looks at the screen beats frontier models on prominent CUA benchmarks, exposing a measurement flaw. | ✅ New, confirmed |
| **Executable-Contract Audit** | [arXiv:2609.37315](https://arxiv.org/abs/2609.37315) | Audits whether simulated tools in agent benchmarks actually honour their advertised interface contracts, a defect that persists across reruns. | ✅ New, confirmed |
| **EnvOS** | [arXiv:2610.40246](https://arxiv.org/abs/2610.40246) | Audits CUAs when software changes mid-task, attributing failures to the agent, an unapplied change, or the grader. | ✅ New, confirmed |
| **OpenReward** | [arXiv:2510.24636](https://arxiv.org/abs/2510.24636) | Learns reward models for long-form agentic tasks via RL, addressing grounding needs beyond internal model knowledge. | ✅ New, confirmed |
| **Autorubric** | [arXiv:2603.00077](https://arxiv.org/abs/2603.00077) | Unifying rubric-based evaluation framework handling position bias, stochastic inconsistency, criterion conflation and forced judgments under uncertainty. | ✅ New, confirmed |
| **PADMÉ** | [arXiv:2609.36086](https://arxiv.org/abs/2609.36086) | Preference-alignment data synthesis for meta-evaluating LM agent evaluators against human judgement. | ✅ New, confirmed |

---

## 2. Environment Synthesis

| Paper/Framework | Key Contribution | Date/Venue | Link | Status |
|---|---|---|---|---|
| **Agent-World** | 1978 environments / 19,822 tools; tool dependency graphs + executable Python solution-based task synthesis; multi-environment closed-loop RL with GRPO; self-evolving arena | 2026-04, Renmin University & ByteDance Seed | [arXiv:2604.18292](https://arxiv.org/abs/2604.18292) | ✅ Confirmed |
| **EnvScaler** | 191 environments / ~7K scenarios; SkelBuilder + ScenGenerator; after SFT, BFCL-MT +8.67 and ACEBench-Agent +11.57 | 2026-01, **ACL 2026 Findings** | [arXiv:2601.05808](https://arxiv.org/abs/2601.05808) | ✅ Confirmed |
| **Agent-World Model (AWM)** | Code-driven + database-backed fully synthetic environment pipeline; 1000 envs / 10000 tasks / 35 tools | 2026-02, **ICML 2026** | [arXiv:2602.10090](https://arxiv.org/abs/2602.10090) | ✅ Confirmed |
| **InfiniteWeb** | Scalable automatic synthesis of Web environments; unified specification + test-driven development, aimed at GUI Agent training | 2026-01, PKU/NJU/MSR Asia | [arXiv:2601.04126](https://arxiv.org/abs/2601.04126) | ✅ Confirmed |
| **ToolVerse** | ~400 MCP servers / ~4,500 tools; tool dependency graphs + Dynamic Unlocking; long-horizon TIR; BFCL-v3 35.00→37.50%, τ²-Bench 27.33→32.37% | 2026-07 | [arXiv:2607.15660](https://arxiv.org/abs/2607.15660) | ✅ Confirmed |
| **SPADE** | Self-play: an environment designer generates Gym-style executable environments ↔ a reasoning Agent solves them; BFCL v4 multi-turn +5.3, ACEBench-Agent +5.7 | 2026-08 | [arXiv:2608.19197](https://arxiv.org/abs/2608.19197) | ✅ Confirmed |
| **CuES** | Curiosity-driven, environment-grounded task synthesis; compatible with AppWorld/BFCL/WebShop, no human seeds required | 2025-12 | [arXiv:2512.01311](https://arxiv.org/abs/2512.01311) | ✅ Confirmed |
| **EnvFactory** | Executable environment synthesis; topology-aware graph-guided robust RL and trajectory generation | 2026-05, HKUST (Guangzhou) LARK et al. | [arXiv:2605.18703](https://arxiv.org/abs/2605.18703) | ✅ Confirmed |
| **Qwen-AgentWorld** | A language world model that simulates general-purpose Agent environments; 35B-A3B / 397B-A17B | 2026-06, Qwen | [arXiv:2606.24597](https://arxiv.org/abs/2606.24597) | ✅ Confirmed |
| **ScaleEnv** | Builds fully interactive environments and verifiable tasks from scratch; tool dependency graph expansion + executable action verification; substantial gains on multi-turn tool-use benchmarks such as τ²-Bench | 2026, **ICML 2026**, with Meituan | [arXiv:2602.06820](https://arxiv.org/abs/2602.06820) | ✅ Confirmed |
| **GenEnv** | Difficulty alignment; co-evolution of Agent and environment simulator, generating tasks at the capability boundary | 2025 | [arXiv:2512.19682](https://arxiv.org/abs/2512.19682) | ✅ Confirmed |
| **C-World** | Builds Agent environments on demand; 5,571 tools / 204 apps; a task distribution engine synthesizes constrained long-horizon workflows; transition functions inject realistic failures; Spearman=0.883 between World Engine and real execution | 2026, **ACL 2026 Long** | [arXiv:2601.06328](https://arxiv.org/abs/2601.06328) | ✅ Confirmed |
| **ClawEnvKit** | Natural-language specification → on-demand generation of claw-like Agent environments; Auto-ClawEval contains 1,040 environments / 24 categories; 13,800× cheaper than manual construction; harness engineering improves over bare ReAct by up to 15.7 points | 2026-04 | [arXiv:2604.18543](https://arxiv.org/abs/2604.18543) | ✅ Confirmed |
| **AgentMercury** | Synthesizes executable environments from high-level business scenarios; 4,783 environments / 14 industries / 50 countries; Qwen3.5-4B on EnterpriseOps-GYM goes 12.3→15.7; after fine-tuning, world-authoring success rate 3.3%→83.3% | 2026-08 | [arXiv:2608.20634](https://arxiv.org/abs/2608.20634) | ✅ Confirmed |
| **Repo2RLEnv** | Converts GitHub repositories / PRs / commit history into executable RL environments; emits Harbor-format task packages (instruction + environment + reference solution + verifier); ships 6 native pipelines + Tasksmith + 14 research recipes; supports pushing to the HuggingFace Hub | — | [GitHub](https://github.com/huggingface/Repo2RLEnv) · [Docs](https://huggingface.github.io/Repo2RLEnv/) | ✅ Confirmed |
| **AutoForge** | End-to-end automated synthesis of simulated environments with high-difficulty but easily verifiable tasks; environment-level RL algorithm mitigates simulated-user instability and environment heterogeneity | 2025-12 | [arXiv:2512.22857](https://arxiv.org/abs/2512.22857) | ✅ New, confirmed |
| **EnvCraft** | Synthesizes executable environments for Claw-like agents; breaks past the "tool-calling endpoint only" limitation of prior synthetic environments | 2026-09 | [arXiv:2609.05576](https://arxiv.org/abs/2609.05576) | ✅ New, confirmed |
| **AgentScaler (Towards General Agentic Intelligence via Environment Scaling)** | Alibaba Tongyi; argues function-calling breadth is tied to environment diversity; automatically constructs simulated function-calling environments | 2025-09 | [arXiv:2509.13311](https://arxiv.org/abs/2509.13311) | ✅ New, confirmed |
| **SynthAPI (Scaling Laws for Tool-Use Agents)** | Explicitly controls environment diversity along the tools, tasks and database axes; 458,752 tasks across 84 environments yield a reproducible scaling law | 2026-10 | [arXiv:2610.37648](https://arxiv.org/abs/2610.37648) | ✅ New, confirmed |
| **WorkForge (Scaling Verifiable Environments for Long-horizon Work Agents)** | Scalable synthesis framework bridging hand-crafted environment overhead and the loss of workspace realism and grounded verifiability | 2026-10 | [arXiv:2610.04906](https://arxiv.org/abs/2610.04906) | ✅ New, confirmed |
| **Learning Design Taste through Verifiable Synthetic Environments** | A small code model learns UI design taste via agentic RL in verifiable synthetic environments; layered verification (hard gates, render metrics, rubric judges, relative preference, blinded expert panel) | 2026-11 | [arXiv:2611.20612](https://arxiv.org/abs/2611.20612) | ✅ New, confirmed |
| **EnvOpt** | Introduces optimization over stationary environments as a third direction alongside parameter tuning and harness optimization | 2026-11 | [arXiv:2611.07372](https://arxiv.org/abs/2611.07372) | ✅ New, confirmed |
| **AgentFactory** | Automated design and optimization of agentic systems; explicitly models the role of model capability in the topology | 2026-09 | [arXiv:2609.01045](https://arxiv.org/abs/2609.01045) | ✅ New, confirmed |
| **Agent²** | Agent-Generates-Agent dual-agent framework; turns natural-language task descriptions plus environment code into executable RL solutions | 2025-09 | [arXiv:2509.13368](https://arxiv.org/abs/2509.13368) | ✅ New, confirmed |
| **CodeMidas** | Agentic pipeline turning implemented functionality in existing codebases into executable RL environments, using source code as the only task-specific signal | 2026-09 | [arXiv:2609.22068](https://arxiv.org/abs/2609.22068) | ✅ New, confirmed |
| **FrogNano** | A 4B coding agent post-trained purely by RL on ~1,500 SWE environments with synthetic tasks calibrated to the learnability frontier of the current checkpoint | 2026-09 | [arXiv:2609.07925](https://arxiv.org/abs/2609.07925) | ✅ New, confirmed |
| **PhantomEnvironments** | Synthetic environments generated entirely by rules (no LLM, zero marginal cost) train capable search agents, avoiding hallucination and contamination | 2026-09 | [arXiv:2609.40221](https://arxiv.org/abs/2609.40221) | ✅ New, confirmed |
| **ProgramGym** | Scalable training environments for long-horizon program reproduction agents that must discover requirements and decide the system design | 2026-10 | [arXiv:2610.13395](https://arxiv.org/abs/2610.13395) | ✅ New, confirmed |
| **POSEIDON** | Automated pipeline extracting diverse, verifiable training environments from scientific code repositories; nearly 10× more environments than a prior approach at the same repository budget | 2026-10 | [arXiv:2610.32448](https://arxiv.org/abs/2610.32448) | ✅ New, confirmed |
| **From Repositories to Training Environments** | An environment evolution loop that goes past build-and-validate, using timely proxy signals to improve training value for recursive self-improvement | 2026-11 | [arXiv:2611.21152](https://arxiv.org/abs/2611.21152) | ✅ New, confirmed |
| **Libra (Training the Environment)** | Introduces mutable hierarchical Markdown catalogs into the repository and optimizes them with an LLM-driven loop to train information localization | 2026-05 | [arXiv:2607.00016](https://arxiv.org/abs/2607.00016) | ✅ New, confirmed |
| **WebUniverse** | Constructs verifiable tasks with verified development trajectories for agentic web development from open-source repositories and real web pages | 2026-10 | [arXiv:2610.33149](https://arxiv.org/abs/2610.33149) | ✅ New, confirmed |
| **VeriEnv (Safe and Scalable Web Agent Learning via Recreated Websites)** | Automatically clones real websites into fully executable, verifiable synthetic environments with controlled internal access via a Python SDK | 2026-03 | [arXiv:2603.10505](https://arxiv.org/abs/2603.10505) | ✅ New, confirmed |
| **SynthTools** | A fully LLM-based pipeline spanning environment generation, simulation, validation and task construction for tool-use environments | 2025-11 | [arXiv:2511.09572](https://arxiv.org/abs/2511.09572) | ✅ New, confirmed |
| **Agent-Environment Alignment via Automated Interface Generation** | Automatically generates interfaces to align the agent's internal expectations with real environment state transitions | 2025-05 | [arXiv:2505.21055](https://arxiv.org/abs/2505.21055) | ✅ New, confirmed |
| **Simia (Simulating Environments with Reasoning Models)** | Shows LLMs can simulate realistic environment feedback without real testbed data or APIs; Simia-SFT + Simia-RL | 2025-11 | [arXiv:2511.01824](https://arxiv.org/abs/2511.01824) | ✅ New, confirmed |
| **RLVE (Adaptive Verifiable Environments)** | Each verifiable environment dynamically adapts its difficulty distribution to the policy model's capabilities | 2025-11, **ICML 2026** | [arXiv:2511.07317](https://arxiv.org/abs/2511.07317) | ✅ New, confirmed |
| **AutoEnv** | Automated, controllable and heterogeneous environment collection for measuring cross-environment agent learning | 2025-11 | [arXiv:2511.19304](https://arxiv.org/abs/2511.19304) | ✅ New, confirmed |
| **Dyna-Mind** | Argues agents need vicarious trial and error; learns to simulate from experience to improve long-horizon interaction | 2025-10 | [arXiv:2510.09577](https://arxiv.org/abs/2510.09577) | ✅ New, confirmed |
| **UI-Simulator** | Generates structured UI states and transitions plus guided rollouts and trajectory filtering to synthesize UI training data at scale | 2025-10 | [arXiv:2510.14969](https://arxiv.org/abs/2510.14969) | ✅ New, confirmed |
| **ReCreate** | Automatic creation and evolution of domain agents driven by real-world interaction experience | 2026-01 | [arXiv:2601.11100](https://arxiv.org/abs/2601.11100) | ✅ New, confirmed |
| **Youtu-Agent** | Modular framework for automated agent generation and continuous evolution, with hybrid policy optimization | 2025-12 | [arXiv:2512.24615](https://arxiv.org/abs/2512.24615) | ✅ New, confirmed |
| **From Language Models to World-Acting Systems** | Separates model competence, system integration, persistence and safe authority, surveying agentic AI across digital, social, virtual and physical environments | 2026-09 | [arXiv:2609.04894](https://arxiv.org/abs/2609.04894) | ✅ New, confirmed |
| **MCP-Universe RL** | RL framework for MCP tool-use agents: environment isolation for hundreds of concurrent trajectories plus rollout scheduling that keeps the GPU busy | 2026-08 | [arXiv:2608.22167](https://arxiv.org/abs/2608.22167) | ✅ New, confirmed |
| **Gecko** | A simulation environment with stateful feedback for refining agent tool calls without real-world side effects | 2026-02 | [arXiv:2602.19218](https://arxiv.org/abs/2602.19218) | ✅ New, confirmed |
| **LLM-in-Sandbox** | Virtualizes the computer as a code sandbox with only basic functionalities, showing a minimal setting already elicits general agentic intelligence | 2026-01 | [arXiv:2601.16206](https://arxiv.org/abs/2601.16206) | ✅ New, confirmed |
| **World of SWECraft** | The Software World framework simulates multi-agent coworking in realistic software ecosystems, with a pipeline creating environments of real, interacting projects | 2026-10 | [arXiv:2610.24061](https://arxiv.org/abs/2610.24061) | ✅ New, confirmed |
| **CompoWorld** | Compositional environment scaling: expands the task space by connecting information and actions across multiple services | 2026-09 | [arXiv:2609.33665](https://arxiv.org/abs/2609.33665) | ✅ New, confirmed |
| **SciDisco** | Scalable process-supervised environments over real scientific data for turn-level agentic RL | 2026-07 | [arXiv:2607.28990](https://arxiv.org/abs/2607.28990) | ✅ New, confirmed |
| **DeepSearch-World** | A deterministic, verifiable environment plus a self-distillation framework for training deep search agents | 2026-07 | [arXiv:2607.07820](https://arxiv.org/abs/2607.07820) | ✅ New, confirmed |
| **EE-MCP** | Self-evolving MCP-GUI agents via automated environment generation and experience learning | 2026-04 | [arXiv:2604.09815](https://arxiv.org/abs/2604.09815) | ✅ New, confirmed |
| **ReSyn** | Autonomously scales synthetic environments for reasoning models, moving beyond a few hand-crafted procedural verifiers | 2026-02 | [arXiv:2602.20117](https://arxiv.org/abs/2602.20117) | ✅ New, confirmed |
| **ASTRA** | Automated synthesis of agentic trajectories and reinforcement arenas without manual intervention | 2026-01 | [arXiv:2601.21558](https://arxiv.org/abs/2601.21558) | ✅ New, confirmed |
| **AgentGym (Evolving LLM Agents across Diverse Environments)** | Lets LLM agents evolve and self-improve across diverse environments instead of imitating expert trajectories | 2024-06 | [arXiv:2406.04151](https://arxiv.org/abs/2406.04151) | ✅ New, confirmed |
| **SkillGym** | Crawls internet agent skills, keeps only offline-reproducible ones; a builder-reviewer pipeline makes difficulty-controlled tasks with reference solutions and executable verifiers (6.8K envs, 19K verified trajectories for SFT). | 2026-09 | [arXiv:2609.37539](https://arxiv.org/abs/2609.37539) | ✅ New, confirmed |
| **Skill2Env** | Capability-oriented synthesis that turns skills into reusable difficulty patterns and task blueprints (objectives, challenges, environment facts, information boundaries, acceptance criteria) driving joint task+environment construction. | 2026-09 | [arXiv:2609.33772](https://arxiv.org/abs/2609.33772) | ✅ New, confirmed |
| **SimWorld Studio** | UE5-based open platform whose SimCoder coding agent writes and executes engine-level code to build physically grounded 3D embodied environments with verifiable tasks, self-evolving from execution feedback. | 2026-05 | [arXiv:2605.09423](https://arxiv.org/abs/2605.09423) | ✅ New, confirmed |
| **Envs-FORGE** | Converts verifier rewards into per-seed synthesis actions; scores six projection/direction edits around a target frontier and solves a MILP per seed, rewriting instruction, fixtures, oracle, tests and Docker together. | 2026-08 | [arXiv:2608.14312](https://arxiv.org/abs/2608.14312) | ✅ New, confirmed |
| **Learning to Build the Environment** | Reframes zero-data reasoning RL from a data-generation loop to an environment-construction loop, where the model writes reusable executable environments and relies on stable solve-verify asymmetry. | 2026-05 | [arXiv:2605.14392](https://arxiv.org/abs/2605.14392) | ✅ New, confirmed |
| **RecreationWorld** | Five-platform recreation benchmark: given a running reference, the hybrid CUA must discover behaviour, implement it, and visually verify, interleaving GUI exploration and CLI coding with verifiable levels. | 2026-09 | [arXiv:2609.22000](https://arxiv.org/abs/2609.22000) | ✅ New, confirmed |
| **VERA** | Scales resumable, rubric-verified environments built from initial trajectories (agent-written rubrics and executable checks), enabling agents to co-evolve on dozens-of-steps tasks instead of outcome-only scoring. | 2026-10 | [arXiv:2610.05923](https://arxiv.org/abs/2610.05923) | ✅ New, confirmed |
| **AutoGym** | Blueprint-first generation of agent gyms (task + executable environment + verifier), avoiding cosmetic difficulty and post-hoc LLM judging of single-pass synthesis. | 2026-09 | [arXiv:2609.22592](https://arxiv.org/abs/2609.22592) | ✅ New, confirmed |
| **AutoEnvScaling** | Treats environment design as a terminal task: a proposer agent builds new RL environments from the solver's rollouts, and the solver's new rollouts steer the next round — an automated data flywheel. | 2026-10 | [arXiv:2610.14163](https://arxiv.org/abs/2610.14163) | ✅ New, confirmed |
| **Recursive Environment Scaling (RES)** | Raises benchmark difficulty while holding objectives fixed by recursively rewriting information access, resource relations and execution dependencies, with execution-grounded checks and inherited edits (294 tasks, 3 benchmarks). | 2026-10 | [arXiv:2610.16397](https://arxiv.org/abs/2610.16397) | ✅ New, confirmed |
| **MetaExp** | Verifiable cross-task environment scaling that trains experience learning as a transferable capability rather than fitting an external experience scaffold on one task distribution. | 2026-10 | [arXiv:2610.21492](https://arxiv.org/abs/2610.21492) | ✅ New, confirmed |
| **Nex-N1** | Unified ecosystem that scales interactive environments along complexity, diversity and realism to supply high-quality interaction signals for agentic policy learning. | 2025-12 | [arXiv:2512.04987](https://arxiv.org/abs/2512.04987) | ✅ New, confirmed |
| **Scalable Environments Drive Generalizable Agents** | Position paper: generalization needs environment scaling — expanding the distribution of executable rule-sets, not just more trajectories or tasks inside fixed benchmarks. | 2026-05 | [arXiv:2605.18181](https://arxiv.org/abs/2605.18181) | ✅ New, confirmed |
| **TRUSTEE (Democratizing Tool Learning with Fully Simulated Environments)** | Trains tool-calling agents in environments fully simulated by open-source LMs as small as 8B (task, user, tool simulation and trajectory evaluation), removing annotation and proprietary-model dependence. | 2026-04 | [arXiv:2604.17739](https://arxiv.org/abs/2604.17739) | ✅ New, confirmed |
| **Simulate to Generalize** | Decouples data synthesis from environment construction by using LLMs as digital world models: from domain names alone it synthesizes APIs and state-changing trajectories. | 2026-07 | [arXiv:2607.16900](https://arxiv.org/abs/2607.16900) | ✅ New, confirmed |
| **EnvSimBench** | Benchmark for the fidelity of LLM-simulated environments, targeting hallucinations, logical inconsistency and silent state drift that corrupt reward signals. | 2026-05 | [arXiv:2605.07247](https://arxiv.org/abs/2605.07247) | ✅ New, confirmed |
| **CoDE (Environment Generation for Compositional RL)** | Early (2022) environment generation: a Generator agent builds compositional task sequences matched to the agent's skill level, forming an automatic curriculum for zero-shot compositional RL. | 2022-01 | [arXiv:2201.08896](https://arxiv.org/abs/2201.08896) | ✅ New, confirmed |
| **Synthetic Environments & Reward Networks** | 2022 precursor: neural Synthetic Environments and Reward Networks act as proxy environments trained by bi-level optimization; agents trained only on the proxy solve the real environment. | 2022-02 | [arXiv:2202.02790](https://arxiv.org/abs/2202.02790) | ✅ New, confirmed |
| **Dyna-bAbI** | 2021 work adding fine-grained controllable dynamic task generation to bAbI, turning a static synthetic benchmark into a tunable one. | 2021-11 | [arXiv:2112.00086](https://arxiv.org/abs/2112.00086) | ✅ New, confirmed |
| **SPHINX** | Procedural synthetic environment for visual perception and reasoning: 25 verifiable task types built from motifs, tiles, charts and geometric primitives; GPT-5 reaches only 51.1%. | 2025-11 | [arXiv:2511.20814](https://arxiv.org/abs/2511.20814) | ✅ New, confirmed |
| **LogicEnvGen** | Task-logic driven generation of logically diverse simulated environments for embodied AI, prioritizing test-view diversity over visual realism. | 2026-01 | [arXiv:2601.13556](https://arxiv.org/abs/2601.13556) | ✅ New, confirmed |
| **CrossEnv** | Synthesizes verifiable cross-environment tasks with an entity-tool graph, so that actions in one service depend on information obtained in another. | 2026-11 | [arXiv:2611.22777](https://arxiv.org/abs/2611.22777) | ✅ New, confirmed |
| **Interactive Structured Environment Scaling** | Shows upstream pre-filtering in structured/retrieval environments causes a measurement confound, and proposes interactive structured environment scaling to remove it. | 2026-11 | [arXiv:2611.19871](https://arxiv.org/abs/2611.19871) | ✅ New, confirmed |
| **EnvLunch** | Turns the environment into free supervision: samples valid action trajectories, executes them, and trains the agent to recover an equivalent trajectory from the final observation alone. | 2026-10 | [arXiv:2610.33817](https://arxiv.org/abs/2610.33817) | ✅ New, confirmed |
| **AgentPolicyForge / PolicyGym** | Builds policy benchmarks from executable environments (10 policy families, 698 synthetic + 254 held-out scenarios) and iteratively trains guards; violations all use permitted tools, forcing argument/resource/context checks. | 2026-10 | [arXiv:2610.28989](https://arxiv.org/abs/2610.28989) | ✅ New, confirmed |

---

## 3. Experience / Interaction Synthesis

| Paper/Framework | Key Contribution | Date/Venue | Link | Status |
|---|---|---|---|---|
| **Tool-R0** | Generator–solver self-play co-evolution; bootstraps tool calling with zero training data | 2026-02, UIUC | [arXiv:2602.21320](https://arxiv.org/abs/2602.21320) | ✅ Confirmed |
| **DreamGym** | Reasoning-based experience model synthesizes diverse experience; low-cost online RL, sim-to-real | 2025-11, **ICLR 2026**, Meta/University of Chicago/Berkeley | [arXiv:2511.03773](https://arxiv.org/abs/2511.03773) | ✅ Confirmed |
| **Grounded Interaction Synthesis (GAIS)** | Simulates long-horizon human–assistant interaction trajectories grounded in real environments, including adversarial constraints; two-stage grounding mechanism | 2026-06, **ACM SIGKDD 2026** | [arXiv:2606.02001](https://arxiv.org/abs/2606.02001) | ✅ Confirmed |
| **TOUCAN** | 1.5M trajectories / ~500 real MCP environments; currently the largest public tool-Agent dataset; after fine-tuning, BFCL V3 surpasses larger closed-source models and advances the MCP-Universe Bench Pareto frontier | 2025-10 | [arXiv:2510.01179](https://arxiv.org/abs/2510.01179) | ✅ Confirmed |
| **Mock Worlds, Real Skills** | The SYNTHAGENT framework: LLM user simulator + mock tool system + rubric rewards; significant gains on 14 datasets | 2026, **ACL 2026 Long** | [arXiv:2601.22511](https://arxiv.org/abs/2601.22511) | ✅ Confirmed |
| **AgentTrek** | Three-stage scalable synthesis pipeline: harvest and filter tutorial texts, guiding replay, trajectory generation; **ICLR 2025 Spotlight** | 2024-12 | [arXiv:2412.09605](https://arxiv.org/abs/2412.09605) | ✅ New, confirmed |
| **Execution-First Synthetic Tool-Use Trace Generation** | Execution-first synthesis generates valid tool sequences and executable workflows first, then derives queries, avoiding invalid calls from query-first synthesis | 2026-07 | [arXiv:2607.29175](https://arxiv.org/abs/2607.29175) | ✅ New, confirmed |
| **Self-Play SWE-RL (SSR)** | Self-play drives software agent training while minimizing dependence on human knowledge and hand-curated environments; **ICML 2026** | 2025-12 | [arXiv:2512.18552](https://arxiv.org/abs/2512.18552) | ✅ New, confirmed |
| **Live-SWE-agent** | Examines whether SWE agents can self-evolve on the fly without bespoke pipeline design | 2025-11 | [arXiv:2511.13646](https://arxiv.org/abs/2511.13646) | ✅ New, confirmed |
| **SWE-RM** | Execution-free reward-model feedback provides finer-grained signals than sparse unit-test outcomes | 2025-12 | [arXiv:2512.21919](https://arxiv.org/abs/2512.21919) | ✅ New, confirmed |
| **SWE-Synth** | Repository-level synthesis of realistic, verifiable, process-aware bug-fix datasets | 2025-04 | [arXiv:2504.14757](https://arxiv.org/abs/2504.14757) | ✅ New, confirmed |
| **SWE-Flow** | Infers incremental development steps from unit tests (TDD-grounded synthesis) via a Runtime Dependency Graph; **ICML 2025** | 2025-06 | [arXiv:2506.09003](https://arxiv.org/abs/2506.09003) | ✅ New, confirmed |
| **BugPilot** | SWE agents add a feature and inadvertently break tests, yielding realistic hard bugs without deliberate perturbation | 2025-10 | [arXiv:2510.19898](https://arxiv.org/abs/2510.19898) | ✅ New, confirmed |
| **SWE-Mirror** | Mirrors issues across repositories, reusing existing Gym environments while tapping the real GitHub issue pool | 2025-09 | [arXiv:2509.08724](https://arxiv.org/abs/2509.08724) | ✅ New, confirmed |
| **ScaleSWE (Immersion in the GitHub Universe)** | Sandboxed multi-agent workflow with dedicated environment-setup, test-creation and problem-description agents, producing high-quality SWE data at scale | 2026-02 | [arXiv:2602.09892](https://arxiv.org/abs/2602.09892) | ✅ New, confirmed |
| **daVinci-Agency** | Reconceptualizes long-horizon agent data synthesis around authentic long-dependency structures and cross-stage evolutionary dynamics | 2026-02 | [arXiv:2602.02619](https://arxiv.org/abs/2602.02619) | ✅ New, confirmed |
| **Training Versatile Coding Agents in Synthetic Environments** | Trains diverse coding agents from scratch in synthetic environments beyond issue-resolution tasks | 2025-12 | [arXiv:2512.12216](https://arxiv.org/abs/2512.12216) | ✅ New, confirmed |
| **Agent Learning via Early Experience** | Lets agents learn from their own early experience, sidestepping non-verifiable environments and costly long-horizon rollouts; **ICML 2026** | 2025-10 | [arXiv:2510.08558](https://arxiv.org/abs/2510.08558) | ✅ New, confirmed |
| **Skill Self-Play** | Uses agent skills as a middle ground to reconcile task diversity with verification reliability | 2026-07 | [arXiv:2607.22529](https://arxiv.org/abs/2607.22529) | ✅ New, confirmed |
| **Multi-Agent Evolve** | Self-play co-evolution that removes the dependence on human-curated datasets and verifiable rewards | 2025-10 | [arXiv:2510.23595](https://arxiv.org/abs/2510.23595) | ✅ New, confirmed |
| **π-Play** | Multi-agent self-play via privileged self-distillation without external data | 2026-04 | [arXiv:2604.14054](https://arxiv.org/abs/2604.14054) | ✅ New, confirmed |
| **Explorer-Zero** | Self-play that jointly generates tasks and fine-grained verifiable rewards through environment interaction | 2026-10 | [arXiv:2610.19868](https://arxiv.org/abs/2610.19868) | ✅ New, confirmed |
| **OMAR (One Model, All Roles)** | A single model role-plays every participant in multi-turn multi-agent self-play RL for social intelligence | 2026-02 | [arXiv:2602.03109](https://arxiv.org/abs/2602.03109) | ✅ New, confirmed |
| **From RLVR to RLSVR** | Task transformation induces self-verifiable rewards for open-ended self-improvement; **COLM 2026** | 2026-07 | [arXiv:2607.23802](https://arxiv.org/abs/2607.23802) | ✅ New, confirmed |
| **Go-Browse** | Frames data collection as graph search for efficient structured exploration of web environments | 2025-06 | [arXiv:2506.03533](https://arxiv.org/abs/2506.03533) | ✅ New, confirmed |
| **MCP-Flow** | Automated web-agent-driven pipeline for large-scale MCP server discovery, data synthesis and training; **ACL 2026 Main** | 2025-10 | [arXiv:2510.24284](https://arxiv.org/abs/2510.24284) | ✅ New, confirmed |
| **Hybrid-Gym** | Decomposes trajectories into fine-grained components, extracts transferable skills and designs auxiliary training tasks for cross-task generalization | 2026-02 | [arXiv:2602.16819](https://arxiv.org/abs/2602.16819) | ✅ New, confirmed |
| **Test-Time Adaptation via Environment Interaction** | Distinguishes and separately corrects syntactic (observation format) and semantic (state transition) misunderstandings at test time | 2025-11 | [arXiv:2511.04847](https://arxiv.org/abs/2511.04847) | ✅ New, confirmed |
| **Navalia** | Cowork Agent framework combining verifiable task synthesis with long-horizon post-training for financial analysis | 2026-10 | [arXiv:2610.26887](https://arxiv.org/abs/2610.26887) | ✅ New, confirmed |
| **EAU (Environment-Agent-User Co-evolution)** | Brings the user simulator and environment into the training loop, evolving them jointly to remove instability and verifier defects | 2026-10 | [arXiv:2610.16523](https://arxiv.org/abs/2610.16523) | ✅ New, confirmed |
| **MIMESIS** | Learns user simulators that are themselves training environments: realistic users that also give agents useful learning signal | 2026-10 | [arXiv:2610.09484](https://arxiv.org/abs/2610.09484) | ✅ New, confirmed |
| **Digital Red Queen** | A self-play algorithm embracing open-ended Red Queen dynamics, continually adapting to an evolving opponent | 2026-01 | [arXiv:2601.03335](https://arxiv.org/abs/2601.03335) | ✅ New, confirmed |
| **FAMA** | Failure-aware meta-agentic framework for smaller open-source LLMs facing cascading decision failures in interactive tool-use environments; **ACL 2026 Findings** | 2026-04 | [arXiv:2604.25135](https://arxiv.org/abs/2604.25135) | ✅ New, confirmed |
| **GPT-Red** | Automated red-teaming agent trained via self-play against a population of simultaneously trained defenders | 2026-07 | [arXiv:2607.26115](https://arxiv.org/abs/2607.26115) | ✅ New, confirmed |
| **StableToolBench-MirrorAPI** | Models tool environments as mirrors of 7,000+ real-world APIs, solving reproducibility of proprietary tool evaluation | 2025-03 | [arXiv:2503.20527](https://arxiv.org/abs/2503.20527) | ✅ New, confirmed |
| **Inducing Programmatic Skills for Agentic Tasks** | Induces and synthesizes reusable programmatic skills for agentic tasks | 2025-04 | [arXiv:2504.06821](https://arxiv.org/abs/2504.06821) | ✅ New, confirmed |
| **Environment-Grounded Automated Prompt Optimization** | LLM-driven evolutionary prompt optimization guided by environment returns, with a behavior analyzer attributing episode outcomes to specifications | 2026-06 | [arXiv:2606.17838](https://arxiv.org/abs/2606.17838) | ✅ New, confirmed |
| **Synthetic Data Generation & Multi-Step RL** | Synthetic data generation plus Step-Wise RL for multi-step reasoning and tool use | 2025-04 | [arXiv:2504.04736](https://arxiv.org/abs/2504.04736) | ✅ New, confirmed |
| **Darwin-Claw** | Environment-adaptive experience consolidation; selects and merges historical interactions instead of injecting raw trajectories indiscriminately | 2026-10 | [arXiv:2610.23574](https://arxiv.org/abs/2610.23574) | ✅ New, confirmed |
| **SynCo** | Data synthesis co-training for self-evolving LLMs, letting the synthesizer evolve alongside the agent | 2026-10 | [arXiv:2610.11345](https://arxiv.org/abs/2610.11345) | ✅ New, confirmed |
| **Self-Evolving Coding Agents** | Survey-style framing of post-deployment self-evolution for coding agents | 2026-08 | [arXiv:2608.03392](https://arxiv.org/abs/2608.03392) | ✅ New, confirmed |
| **Self-Evolving Software Agents** | A BDI-LLM architecture that autonomously evolves goals, reasoning and executable code beyond design-time requirements | 2026-04 | [arXiv:2604.27264](https://arxiv.org/abs/2604.27264) | ✅ New, confirmed |
| **Q-Evolve (in-distribution Optimization)** | A self-evolving framework that addresses long-horizon credit assignment with in-distribution optimization | 2026-06, **ICML 2026** | [arXiv:2606.07367](https://arxiv.org/abs/2606.07367) | ✅ New, confirmed |
| **From Self-Evolving Synthetic Data to Verifiable-Reward RL** | A post-training path from self-evolving synthetic data to verifiable-reward RL for multi-turn interactive tool-using agents | 2026-01 | [arXiv:2601.22607](https://arxiv.org/abs/2601.22607) | ✅ New, confirmed |
| **AgentFrontier** | ZPD-guided data synthesis that generates multidisciplinary tasks exactly at the frontier an LLM cannot solve alone but can master with guidance. | 2025-10 | [arXiv:2510.24695](https://arxiv.org/abs/2510.24695) | ✅ New, confirmed |
| **LoopTool** | Model-aware data evolution that closes the generate-train loop, adaptively targeting the model's weak spots and removing noisy labels instead of static two-stage synthesis. | 2025-11 | [arXiv:2511.09148](https://arxiv.org/abs/2511.09148) | ✅ New, confirmed |
| **FunReason-MT** | Data synthesis solution for real-world multi-turn tool use, replacing random environment sampling and role-play with a more controllable pipeline. | 2025-10 | [arXiv:2510.24645](https://arxiv.org/abs/2510.24645) | ✅ New, confirmed |
| **RAGShaper** | Automated data synthesis for agentic RAG that injects noise, retrieval failures and perturbations so agents learn planning and recovery under realistic retrieval conditions. | 2026-01 | [arXiv:2601.08699](https://arxiv.org/abs/2601.08699) | ✅ New, confirmed |
| **MATRIX (Multi-Agent Simulation)** | Multi-agent simulator generating diverse text scenarios that capture real human needs, used to synthesize post-training instruction data at scale. | 2024-10 | [arXiv:2410.14251](https://arxiv.org/abs/2410.14251) | ✅ New, confirmed |
| **Matrix (P2P Multi-Agent Data Synthesis)** | Peer-to-peer multi-agent synthetic data framework without a central orchestrator, avoiding scalability bottlenecks and domain hard-coding. | 2025-11 | [arXiv:2511.21686](https://arxiv.org/abs/2511.21686) | ✅ New, confirmed |
| **Multi-Agent Sampling** | Scales inference compute for data synthesis through tree-search-based multi-agent collaboration. | 2024-12 | [arXiv:2412.17061](https://arxiv.org/abs/2412.17061) | ✅ New, confirmed |
| **ProductResearch** | Trains e-commerce deep-research agents via multi-agent synthetic trajectory distillation. | 2026-02 | [arXiv:2602.23716](https://arxiv.org/abs/2602.23716) | ✅ New, confirmed |
| **ReAct** | Foundational think-act-observe loop interleaving reasoning with environment actions, the prototype of most tool-using agent trajectories. | 2022-10 | [arXiv:2210.03629](https://arxiv.org/abs/2210.03629) | ✅ New, confirmed |
| **Inner Monologue** | 闭环语言反馈的具身规划：把环境成功/失败反馈转成自然语言「内心独白」，据此在线修正计划 | 2022-07 | [arXiv:2207.05608](https://arxiv.org/abs/2207.05608) | ✅ New, confirmed |
| **Reflexion** | 语言化强化学习：把失败轨迹转成文字反思存入记忆，下次尝试据此改进，是「用环境反馈迭代」的经典范式 | 2023-03 | [arXiv:2303.11366](https://arxiv.org/abs/2303.11366) | ✅ New, confirmed |
| **Language Models as Zero-Shot Planners** | 提取可执行知识用于具身任务：把长程指令分解为可执行步骤序列，无需示范数据即可规划 | 2022-01 | [arXiv:2201.07207](https://arxiv.org/abs/2201.07207) | ✅ New, confirmed |

---

## 4. Web / GUI Environment Synthesis

| Paper/Framework | Key Contribution | Date/Venue | Link | Status |
|---|---|---|---|---|
| **WebArena-Infinity** | Multi-agent pipeline (coding + browser-use agents) generates verifiable Web environments from static artifacts; 10 environments / 1,260 tasks / 2,070 trajectories | 2026 | [GitHub](https://github.com/web-arena-x/webarena-infinity) | ✅ Confirmed |
| **ScaleWoB** | High-fidelity cross-platform GUI interaction environment synthesis; verifiable rewards, low resource overhead | 2026-05 | [arXiv:2605.25160](https://arxiv.org/abs/2605.25160) | ✅ Confirmed |
| **GUI-Genesis** | Reconstructs lightweight Web environments from real applications; verifiable rewards, GUI Agent post-training | 2026 | [arXiv:2602.14093](https://arxiv.org/abs/2602.14093) | ✅ Confirmed |
| **Weblica** | A reproducible, extensible interactive Web environment framework; aimed at visual Web Agent training | 2026-05 | [arXiv:2605.06761](https://arxiv.org/abs/2605.06761) | ✅ Confirmed |
| **ScaleCUA / VeriGen** | Verifiable task synthesis + efficient online RL to scale computer-use Agents | 2026-07 | [arXiv:2607.11185](https://arxiv.org/abs/2607.11185) | ✅ Confirmed |
| **FaraGen (Fara-7B)** | Generates multi-step Web task data from high-traffic websites | 2025-11, Microsoft | [arXiv:2511.19663](https://arxiv.org/abs/2511.19663) | ✅ Confirmed |
| **FaraGen1.5 (Fara-1.5)** | Three components — environment + solver + verifier — forming a scalable CUA data pipeline | 2026-06 | [arXiv:2606.20785](https://arxiv.org/abs/2606.20785) | ✅ Confirmed |
| **OS-Genesis** | Reverse task synthesis: explore first, then construct tasks, producing GUI Agent trajectories | 2024-12, **ACL 2025** | [arXiv:2412.19723](https://arxiv.org/abs/2412.19723) | ✅ Confirmed |
| **HATS** | Hardness-aware trajectory synthesis for GUI agents; adapted to AndroidWorld / WebArena | **CVPR 2026** | [arXiv:2603.12138](https://arxiv.org/abs/2603.12138) | ✅ Confirmed |
| **WebGym** | Largest open-source environment to date for training realistic visual web agents; nearly 300,000 tasks with rubric-based evaluation across real websites and difficulty levels | 2026-01 | [arXiv:2601.02439](https://arxiv.org/abs/2601.02439) | ✅ New, confirmed |
| **WEBSERV** | Full-stack, RL-ready web environment that avoids the resource cost of server-side Docker and the noisy observations of browser-side interfaces | 2025-10 | [arXiv:2510.16252](https://arxiv.org/abs/2510.16252) | ✅ New, confirmed |
| **WebHarbor** | 153 executable, dockerized website environments faithfully reconstructing visual interfaces, content and functional workflows of real sites | 2026-11 | [arXiv:2611.03634](https://arxiv.org/abs/2611.03634) | ✅ New, confirmed |
| **Training Needs Trustworthy Worlds** | Synthetic web environments that are executable, auditable and grounded in backend state, represented as structured scaffolds of pages, links and database records | 2026-08 | [arXiv:2608.21898](https://arxiv.org/abs/2608.21898) | ✅ New, confirmed |
| **Learning Simple Test-Time Environments** | Web agents can learn simple environment observations at test time, closing compositional generalization gaps | 2026-08 | [arXiv:2608.29305](https://arxiv.org/abs/2608.29305) | ✅ New, confirmed |
| **Build the web for agents, not agents for the web** | Argues for a fundamental mismatch between human-designed interfaces and LLM capabilities | 2025-06 | [arXiv:2506.10953](https://arxiv.org/abs/2506.10953) | ✅ New, confirmed |
| **Ego2Web** | A web agent benchmark grounded in egocentric videos, connecting physical perception with online execution; **CVPR 2026** | 2026-03 | [arXiv:2603.22529](https://arxiv.org/abs/2603.22529) | ✅ New, confirmed |
| **MAI-Gym** | An open all-in-one platform unifying GUI agent evaluation, data collection and online RL across mobile and computer environments | 2026-10 | [arXiv:2610.20939](https://arxiv.org/abs/2610.20939) | ✅ New, confirmed |
| **VEM (Value Environment Model)** | Environment-free RL that decouples value estimation from policy optimization to cut interaction cost and distribution shift | 2025-02 | [arXiv:2502.18906](https://arxiv.org/abs/2502.18906) | ✅ New, confirmed |
| **CUA-Universe** | A scalable, dynamic environment for hybrid GUI + CLI agents sharing application state | 2026-09 | [arXiv:2609.05374](https://arxiv.org/abs/2609.05374) | ✅ New, confirmed |
| **Recovering Policy-Induced Errors** | GUI-RobustEval with 1,216 executable cases measuring error recovery; Robustness-driven Trajectory Synthesis creates 800K high-quality trajectories; **ICML 2026 Spotlight** | 2026-05 | [arXiv:2605.29447](https://arxiv.org/abs/2605.29447) | ✅ New, confirmed |
| **SEE** | Two-stage structure-aware exploring and exploiting for long-horizon GUI trajectory synthesis, with high coverage of rare transitions; **ACM MM 2026 Oral** | 2026-07 | [arXiv:2607.18046](https://arxiv.org/abs/2607.18046) | ✅ New, confirmed |
| **GSAR** | Goal-State-Anchor rewards plus self-evolving data synthesis for mobile GUI agents; **EMNLP 2026 Main** | 2026-08 | [arXiv:2608.22847](https://arxiv.org/abs/2608.22847) | ✅ New, confirmed |
| **MobileGUI-RL** | Reinforcement learning for mobile GUI agents in an online environment, avoiding overfitting to UI templates | 2025-07 | [arXiv:2507.05720](https://arxiv.org/abs/2507.05720) | ✅ New, confirmed |
| **CRAFT-GUI** | Curriculum-reinforced training that explicitly models task difficulty variation for GUI agents | 2025-08 | [arXiv:2508.11360](https://arxiv.org/abs/2508.11360) | ✅ New, confirmed |
| **MobileWorld** | Agent-user interactive and MCP-augmented mobile agent benchmark, motivated by AndroidWorld saturation | 2025-12 | [arXiv:2512.19432](https://arxiv.org/abs/2512.19432) | ✅ New, confirmed |
| **OSWorld-MCP** | The first comprehensive and fair benchmark for computer-use agent tool invocation via MCP | 2025-10 | [arXiv:2510.24563](https://arxiv.org/abs/2510.24563) | ✅ New, confirmed |
| **GUI-CC** | Benchmarks contextual consistency of GUI world models as agent environments rather than isolated next-screen predictors; **EMNLP 2026 Findings** | 2026-09 | [arXiv:2609.00048](https://arxiv.org/abs/2609.00048) | ✅ New, confirmed |
| **Benchmarking and Improving GUI Agents in High-Dynamic Environments** | Benchmark and improvement methods for GUI agents in rapidly changing interfaces | 2026-04 | [arXiv:2604.25380](https://arxiv.org/abs/2604.25380) | ✅ New, confirmed |
| **WebChoreArena** | Evaluates web browsing agents on realistic, tedious and cognitively demanding tasks; **COLM 2026** | 2025-06 | [arXiv:2506.01952](https://arxiv.org/abs/2506.01952) | ✅ New, confirmed |
| **STAGE-Claw** | Automated state-based agent benchmarking for realistic scenarios | 2026-06 | [arXiv:2606.10394](https://arxiv.org/abs/2606.10394) | ✅ New, confirmed |
| **E-Bench** | Multi-step tool-use agents in real-world product scenarios | 2026-07 | [arXiv:2607.23722](https://arxiv.org/abs/2607.23722) | ✅ New, confirmed |
| **ViMo** | A generative visual GUI world model that predicts the next GUI observation for long-horizon planning | 2025-04 | [arXiv:2504.13936](https://arxiv.org/abs/2504.13936) | ✅ New, confirmed |
| **Code2World** | A GUI world model via renderable code generation, combining visual fidelity with structural controllability | 2026-02 | [arXiv:2602.09856](https://arxiv.org/abs/2602.09856) | ✅ New, confirmed; ID added (was search-only) |
| **Windows Agent Arena** | Evaluating multi-modal OS agents at scale on Windows | 2024-09 | [arXiv:2409.08264](https://arxiv.org/abs/2409.08264) | ✅ New, confirmed |
| **macOSWorld** | A multilingual interactive benchmark for GUI agents on macOS | 2025-06 | [arXiv:2506.04135](https://arxiv.org/abs/2506.04135) | ✅ New, confirmed |
| **MacArena** | Benchmarking computer use agents on an online macOS environment | 2026-06 | [arXiv:2606.06560](https://arxiv.org/abs/2606.06560) | ✅ New, confirmed |
| **MacAgentBench** | Benchmarking AI agents on real-world macOS desktops | 2026-06 | [arXiv:2606.22557](https://arxiv.org/abs/2606.22557) | ✅ New, confirmed |
| **OSUniverse** | Benchmark for multimodal GUI-navigation agents emphasizing usability, extensibility, test coverage and automatic validation | 2025-05 | [arXiv:2505.03570](https://arxiv.org/abs/2505.03570) | ✅ New, confirmed |
| **MMBench-GUI** | Hierarchical multi-platform evaluation framework for GUI agents | 2025-07 | [arXiv:2507.19478](https://arxiv.org/abs/2507.19478) | ✅ New, confirmed |
| **BEARCUBS** | A benchmark for computer-using web agents | 2025-03 | [arXiv:2503.07919](https://arxiv.org/abs/2503.07919) | ✅ New, confirmed |
| **VisualWebArena** | Evaluating multimodal agents on realistic visual web tasks; **ACL 2024** | 2024-01 | [arXiv:2401.13649](https://arxiv.org/abs/2401.13649) | ✅ New, confirmed |
| **AndroidWorld** | A dynamic benchmarking environment for autonomous agents with reproducible evaluation | 2024-05 | [arXiv:2405.14573](https://arxiv.org/abs/2405.14573) | ✅ New, confirmed |
| **WebFactory** | Fully automated closed-loop RL pipeline that compresses LLM latent knowledge into grounded web agents using reproducible synthetic sites instead of live-web or hand-crafted environments. | 2026-03 | [arXiv:2603.05044](https://arxiv.org/abs/2603.05044) | ✅ New, confirmed |
| **OpenMobile** | Open-source mobile-agent framework with task-instruction and trajectory synthesis, addressing the closed data recipes of frontier mobile agents. | 2026-04 | [arXiv:2604.15093](https://arxiv.org/abs/2604.15093) | ✅ New, confirmed |
| **OpenMobile-2** | Builds MobileGym++ (35 commercial-style apps with cross-app workflows, reset/verify controllable) plus emulator apps to span 110+ apps, with open training data and app-native tools. | 2026-10 | [arXiv:2610.14157](https://arxiv.org/abs/2610.14157) | ✅ New, confirmed |
| **SynWeaver** | Website-prior task/trajectory co-synthesis that first models a site's full functionality to avoid hallucinated tasks and improve coverage and efficiency. | 2026-08 | [arXiv:2608.12429](https://arxiv.org/abs/2608.12429) | ✅ New, confirmed |
| **WebSTAR** | Scalable CUA data synthesis with step-level filtering, since strong-CUA rollouts contain many incorrect or suboptimal steps that make naive imitation ineffective. | 2025-11 | [arXiv:2512.10962](https://arxiv.org/abs/2512.10962) | ✅ New, confirmed |
| **GUI-ReWalk** | Massive GUI trajectory generation via stochastic exploration plus intent-aware reasoning, balancing diversity with meaningful task coverage. | 2025-09 | [arXiv:2509.15738](https://arxiv.org/abs/2509.15738) | ✅ New, confirmed |
| **Explorer** | Scales exploration-driven web trajectory synthesis for multimodal web agents, addressing the lack of diverse trajectory-level data. | 2025-02 | [arXiv:2502.11357](https://arxiv.org/abs/2502.11357) | ✅ New, confirmed |
| **Imagine to Act** | High-fidelity GUI data synthesis with an image-editing world model that preserves pixel-level icons and layout details discarded by text or HTML-based models. | 2026-10 | [arXiv:2610.05861](https://arxiv.org/abs/2610.05861) | ✅ New, confirmed |
| **Echoverse** | Deep, evolving CUA environments: argues the bottleneck moved from environment count to behavioural depth, targeting real agent failure interactions, and reset/evolve capability. | 2026-07 | [arXiv:2607.28074](https://arxiv.org/abs/2607.28074) | ✅ New, confirmed |
| **PhoneWorld** | Trace-grounded framework turning real-app evidence into runnable, resettable, verifiable Android environments via a usage-weighted interaction skeleton. | 2026-05 | [arXiv:2605.29486](https://arxiv.org/abs/2605.29486) | ✅ New, confirmed |
| **WebAnything** | Fully automated reconstruction of source-grounded, reusable web environments from real URLs, avoiding per-site mirroring and generative drift. | 2026-10 | [arXiv:2610.37786](https://arxiv.org/abs/2610.37786) | ✅ New, confirmed |
| **UI-Mate** | Open-weight GUI agent combining an environment-grounded training stack with in-context demonstration learning to counter scarce, biased data and ambiguous instructions. | 2026-08 | [arXiv:2608.15930](https://arxiv.org/abs/2608.15930) | ✅ New, confirmed |
| **Agent-as-Annotators** | Structured trajectory synthesis by analogy to annotation roles (Task Designer, Annotator, Supervisor); 3,000 teacher trajectories across six web environments to fine-tune a 9B student. | 2026-04 | [arXiv:2604.07776](https://arxiv.org/abs/2604.07776) | ✅ New, confirmed |
| **WebShop** | Scalable real-web shopping environment with 1.18M products and crowdsourced instructions, an early standard for grounded web agents. | 2022-07 | [arXiv:2207.01206](https://arxiv.org/abs/2207.01206) | ✅ New, confirmed |
| **Mind2Web** | First generalist web-agent dataset spanning 137 real websites and 2,350 tasks for cross-domain generalization. | 2023-06 | [arXiv:2306.06070](https://arxiv.org/abs/2306.06070) | ✅ New, confirmed |
| **WebVoyager** | End-to-end multimodal web agent operating live websites with GPT-4V judging task success. | 2024-01 | [arXiv:2401.13919](https://arxiv.org/abs/2401.13919) | ✅ New, confirmed |

---

## 5. Terminal / Coding Environment Synthesis

| Paper/Framework | Key Contribution | Date/Venue | Link | Status |
|---|---|---|---|---|
| **Terminal-Bench 2.0** | 89 CLI tasks; each task has a unique environment + human-written solution + comprehensive tests; frontier models score <65% | 2026-01, **ICLR 2026** | [arXiv:2601.11868](https://arxiv.org/abs/2601.11868) | ✅ Confirmed |
| **CLI-Universe** | Verifiable task synthesis engine; 6K trajectories; Qwen3-32B scores 33.4% on TB2 | 2026-06, Nanjing University/StepFun/Shanghai AI Lab | [arXiv:2606.22883](https://arxiv.org/abs/2606.22883) | ✅ Confirmed |
| **SETA** | Dual pipelines SETA-Synth + SETA-Evol; SETA-Env contains 4,500+ environments; GRPO-trained Qwen3-8B reaches a 12% pass rate on TB 2.0 | 2026-07 | [arXiv:2607.10891](https://arxiv.org/abs/2607.10891) | ✅ Confirmed |
| **TerminalWorld** | Reverse-engineers real terminal dependencies to build executable sandboxes + environment synthesis | 2026-05, UCL/Nanjing University/Tencent | [arXiv:2605.22535](https://arxiv.org/abs/2605.22535) | ✅ Confirmed |
| **ResearchEnvBench** | Benchmark for research-code execution environment synthesis; dependency resolution, version alignment, distributed scenarios | 2026-03 | [arXiv:2603.06739](https://arxiv.org/abs/2603.06739) | ✅ Confirmed |
| **AI Scientist via Synthetic Task Scaling** | Synthesizes ML challenge tasks, compatible with SWE-Agent; topic sampling + dataset proposal + code generation | 2026-03 | [arXiv:2603.17216](https://arxiv.org/abs/2603.17216) | ✅ Confirmed |
| **SWE-Factory** | Automated factory for issue-resolution training data and evaluation benchmarks; SWE-Builder + exit-code scoring + fail2pass | 2025-06, **FSE 2026** | [arXiv:2506.10954](https://arxiv.org/abs/2506.10954) | ✅ Confirmed |
| **SWE-smith** | Generates SWE-gym from arbitrary Python repositories; 128 repos / 50K task instances; SWE-agent-LM-32B reaches 40.2% Pass@1 on SWE-bench Verified | **NeurIPS 2025 Spotlight** | [arXiv:2504.21798](https://arxiv.org/abs/2504.21798) | ✅ ID completed (was search-only) |
| **R2E-Gym / AgentGym** | Procedural environment generation + hybrid verifiers; 8.7K+ executable SWE tasks; open-sources SWE-Agent weights | **COLM 2025** | [arXiv:2504.07164](https://arxiv.org/abs/2504.07164) | ✅ ID completed (was search-only) |
| **SWE-World** | Docker-free framework; a learned surrogate model replaces physical execution; Qwen2.5-Coder-32B on SWE-bench Verified goes 6.2%→52.0% (SFT) / 55.0% (RL) / 68.2% (TTS) | 2026-02, Renmin University Gaoling & BOSS Zhipin | [arXiv:2602.03419](https://arxiv.org/abs/2602.03419) | ✅ Confirmed |
| **SWE-Universe** | Automatically builds verifiable SWE environments from GitHub PRs; 807,693 multilingual environments; Qwen3-Max-Thinking reaches 75.3% on SWE-Bench Verified | 2026-02, Alibaba Qwen & Zhejiang University | [arXiv:2602.02361](https://arxiv.org/abs/2602.02361) | ✅ Confirmed |
| **daVinci-Env** | Large-scale open SWE environment synthesis | 2026-03 | [arXiv:2603.13023](https://arxiv.org/abs/2603.13023) | ✅ Confirmed |
| **DockSmith** | Reliable coding environments at scale; automated construction of Dockerfiles and test scripts | 2026-02 | [arXiv:2602.00592](https://arxiv.org/abs/2602.00592) | ✅ Confirmed |
| **TerminalTraj** | Generates large-scale terminal Agent trajectories from Dockerized environments; 32K images / 50,733 verified trajectories; after training, Qwen2.5-Coder gains +20% on TB 1.0 and +10% on TB 2.0 | **ICML 2026** | [arXiv:2602.01244](https://arxiv.org/abs/2602.01244) | ✅ Confirmed |
| **Terminal-Universe** | Reverse-replays Agent trajectories into reusable terminal environments; 37.3k task-sufficient environments; fine-tuned Qwen3.5-27B gains +11.9 on TB 2.1 and +13.8 on EvoCode-Bench v2 MT@4 | 2026-09 | [arXiv:2609.04148](https://arxiv.org/abs/2609.04148) | ✅ Confirmed |
| **SWE-Gym** | The first environment for training real-world SWE agents; 2,438 real Python task instances with executable runtime, unit tests and natural-language task; up to +19% resolve rate on SWE-Bench Verified/Lite; **ICML 2025** | 2024-12 | [arXiv:2412.21139](https://arxiv.org/abs/2412.21139) | ✅ New, confirmed |
| **SWE-bench Goes Live!** | A continuously updated SWE benchmark that avoids frozen instances and manual construction | 2025-05 | [arXiv:2505.23419](https://arxiv.org/abs/2505.23419) | ✅ New, confirmed |
| **SWE-rebench** | Automated pipeline for task collection and decontaminated evaluation, continuously supplying real-world SWE training data | 2025-05 | [arXiv:2505.20411](https://arxiv.org/abs/2505.20411) | ✅ New, confirmed |
| **SWE-rebench V2** | Language-agnostic SWE task collection at scale across ecosystems; **ICML 2026** | 2026-02 | [arXiv:2602.23866](https://arxiv.org/abs/2602.23866) | ✅ New, confirmed |
| **SWE-Bench Pro Verified** | A reliable benchmark for software engineering agents | 2026-09 | [arXiv:2609.08149](https://arxiv.org/abs/2609.08149) | ✅ New, confirmed |
| **Reproducibility of Build Environments through Space and Time** | Systematic study of build-environment reproducibility across space and time; **ICSE 2026** | 2024-02 | [arXiv:2402.00424](https://arxiv.org/abs/2402.00424) | ✅ New, confirmed |
| **Repo2Run** | Automated building of executable environments for code repositories at scale | 2025-02 | [arXiv:2502.13681](https://arxiv.org/abs/2502.13681) | ✅ New, confirmed |
| **RepoST** | Sandbox testing isolates a target function and its dependencies, enabling scalable repository-level environment construction | 2025-03 | [arXiv:2503.07358](https://arxiv.org/abs/2503.07358) | ✅ New, confirmed |
| **EnvBench** | A benchmark for automated environment setup; **ICLR 2025 DL4Code Workshop** | 2025-03 | [arXiv:2503.14443](https://arxiv.org/abs/2503.14443) | ✅ New, confirmed |
| **HerAgent** | Rethinks automated environment deployment with a hierarchical test pyramid instead of weak success signals | 2026-02 | [arXiv:2602.07871](https://arxiv.org/abs/2602.07871) | ✅ New, confirmed |
| **Multi-Docker-Eval** | A benchmark on automatic environment building; 40 real repositories across 9 languages, measuring both executable-state success and efficiency | 2025-12 | [arXiv:2512.06915](https://arxiv.org/abs/2512.06915) | ✅ New, confirmed |
| **Enconda-bench** | Process-level trajectory evaluation diagnosing where environment configuration fails (planning, perception, execution) | 2025-10 | [arXiv:2510.25694](https://arxiv.org/abs/2510.25694) | ✅ New, confirmed |
| **SWE-MiniSandbox** | Container-free RL training of SWE agents, avoiding per-task image storage overhead and container privileges | 2026-02 | [arXiv:2602.11210](https://arxiv.org/abs/2602.11210) | ✅ New, confirmed |
| **Dockerless** | An environment-free agentic patch verifier that never executes the generated code | 2026-06 | [arXiv:2606.28436](https://arxiv.org/abs/2606.28436) | ✅ New, confirmed |
| **Agent-RLVR** | Training SWE agents via guidance and environment rewards to counter sparse reward landscapes | 2025-06 | [arXiv:2506.11425](https://arxiv.org/abs/2506.11425) | ✅ New, confirmed |
| **SWE-PRM (When Agents go Astray)** | Inference-time process reward model that course-corrects during execution to reduce redundant exploration and looping | 2025-09 | [arXiv:2509.02360](https://arxiv.org/abs/2509.02360) | ✅ New, confirmed |
| **Graph-Guided Repository Environment Construction** | Derives execution requirements fragmented across repository artifacts through graph-guided construction | 2026-09 | [arXiv:2609.33429](https://arxiv.org/abs/2609.33429) | ✅ New, confirmed |
| **Change2Task** | Undoing a merged PR on today's code recreates the same task inside a maintained revision, avoiding rebuilds at old revisions | 2026-07 | [arXiv:2607.28591](https://arxiv.org/abs/2607.28591) | ✅ New, confirmed |
| **For Coding Agents, the Repository Matters** | Exposes coordinated-attack risk from shared infrastructure (about 1,200 agents in a large internal evaluation joined an attack) | 2026-06 | [arXiv:2606.28235](https://arxiv.org/abs/2606.28235) | ✅ New, confirmed |
| **SWE-Search** | Monte Carlo tree search plus iterative refinement enables backtracking in software agents | 2024-10 | [arXiv:2410.20285](https://arxiv.org/abs/2410.20285) | ✅ New, confirmed |
| **SWT-Bench** | Code agents formalize user issues into test cases for validating real bug fixes | 2024-06 | [arXiv:2406.12952](https://arxiv.org/abs/2406.12952) | ✅ New, confirmed |
| **TDD-Bench Verified** | Can LLMs generate fail-to-pass tests before an issue is resolved | 2024-12 | [arXiv:2412.02883](https://arxiv.org/abs/2412.02883) | ✅ New, confirmed |
| **Otter** | Generating tests from issues to validate SWE patches before the patch exists | 2025-02 | [arXiv:2502.05368](https://arxiv.org/abs/2502.05368) | ✅ New, confirmed |
| **Issue2Test** | Generating reproducing test cases from issue reports to guide patch search and intent validation | 2025-03 | [arXiv:2503.16320](https://arxiv.org/abs/2503.16320) | ✅ New, confirmed |
| **Beyond pip install** | Evaluating LLM agents for the automated installation of Python projects | 2024-12 | [arXiv:2412.06294](https://arxiv.org/abs/2412.06294) | ✅ New, confirmed |
| **You Name It, I Run It** | An LLM agent to execute the test suites of arbitrary projects across languages and build systems; **ISSTA 2025** | 2024-12 | [arXiv:2412.10133](https://arxiv.org/abs/2412.10133) | ✅ New, confirmed |
| **debug-gym** | A lightweight text-based environment for interactive debugging where agents explore codebases for task-relevant information | 2025-03 | [arXiv:2503.21557](https://arxiv.org/abs/2503.21557) | ✅ New, confirmed |
| **UTBoost** | Rigorous evaluation of coding agents on SWE-Bench with augmented tests; **ACL 2025** | 2025-06 | [arXiv:2506.09289](https://arxiv.org/abs/2506.09289) | ✅ New, confirmed |
| **ProjectEval** | Automated evaluation of programming agents on project-level code generation | 2025-03 | [arXiv:2503.07010](https://arxiv.org/abs/2503.07010) | ✅ New, confirmed |
| **GitTaskBench** | 54 realistic tasks across 7 modalities and 7 domains for code agents leveraging large code repositories | 2025-08 | [arXiv:2508.18993](https://arxiv.org/abs/2508.18993) | ✅ New, confirmed |
| **MEnvAgent** | Multi-language environment construction with a Planning-Execution-Verification multi-agent architecture, scaling verifiable SWE task instances across languages. | 2026-01 | [arXiv:2601.22859](https://arxiv.org/abs/2601.22859) | ✅ New, confirmed |
| **TermiGen** | High-fidelity terminal environments plus robust trajectory synthesis that deliberately includes simple mistakes weaker models make, narrowing the instruction-tuning distribution gap. | 2026-02 | [arXiv:2602.07274](https://arxiv.org/abs/2602.07274) | ✅ New, confirmed |
| **LiteCoder-Terminal** | Zero-dependency synthesis pipeline that autonomously generates executable, verifiable long-horizon terminal tasks without scraping external repositories. | 2026-05 | [arXiv:2605.29559](https://arxiv.org/abs/2605.29559) | ✅ New, confirmed |
| **FACET** | Preserves source intent and executable state so the four task artifacts (instruction, initial environment, reference solution, verifier) share consistent assumptions. | 2026-08 | [arXiv:2608.18580](https://arxiv.org/abs/2608.18580) | ✅ New, confirmed |
| **RST (Recursive Synthetic Terminal Tasks)** | Recursive verified synthesis that extends reference solutions from seed tasks and realigns verifier and instruction, keeping long-horizon tasks consistent at scale. | 2026-08 | [arXiv:2608.05466](https://arxiv.org/abs/2608.05466) | ✅ New, confirmed |
| **Depth Measurement for Terminal Tasks** | Shows turn count reflects model habits rather than task demands and LLM difficulty labels poorly track pass rates; re-characterizes depth by the actual work a task requires. | 2026-11 | [arXiv:2611.01927](https://arxiv.org/abs/2611.01927) | ✅ New, confirmed |
| **Terminal-Task-Gen** | Lightweight terminal task generator supporting seed-based and skill-based construction, plus a systematic study of data-engineering and training strategies for terminal agents. | 2026-02 | [arXiv:2602.21193](https://arxiv.org/abs/2602.21193) | ✅ New, confirmed |
| **When Terminal-Agent Training Stalls** | Demystifies terminal task generation and verification failures: a runnable Docker image plus tests does not guarantee reward faithfulness, informativeness or attributability. | 2026-10 | [arXiv:2610.02405](https://arxiv.org/abs/2610.02405) | ✅ New, confirmed |
| **WorkBorne** | Discovers agentic tasks from real-world artifact transitions, bridging low-fidelity synthetic environments and shallow resource-as-static-input tasks. | 2026-10 | [arXiv:2610.14915](https://arxiv.org/abs/2610.14915) | ✅ New, confirmed |
| **SWE-Bench++** | Automatically generates repository-level coding tasks from live GitHub pull requests, covering bug fixes and feature requests across languages. | 2025-12 | [arXiv:2512.17419](https://arxiv.org/abs/2512.17419) | ✅ New, confirmed |
| **RepoForge** | End-to-end autonomous pipeline generating/evaluating/training SWE agents; 7,304 executable environments and RepoForge-8B-Agent at 17.4% on SWE-Bench-Verified. | 2025-08 | [arXiv:2508.01550](https://arxiv.org/abs/2508.01550) | ✅ New, confirmed |
| **daVinci-Dev** | Agent-native mid-training for software engineering on large-scale data mirroring authentic agentic workflows. | 2026-01 | [arXiv:2601.18418](https://arxiv.org/abs/2601.18418) | ✅ New, confirmed |
| **RAT (RunAnyThing)** | Fully automated environment configuration for arbitrary repositories, removing the manual Dockerfile/setup bottleneck without language restriction. | 2026-04 | [arXiv:2604.23190](https://arxiv.org/abs/2604.23190) | ✅ New, confirmed |
| **EnvAgent** | Agentic framework that synthesizes, builds and verifies repository execution environments from heterogeneous, incomplete requirements. | 2026-10 | [arXiv:2611.23258](https://arxiv.org/abs/2611.23258) | ✅ New, confirmed |
| **Counterfactual Rollout Replay (CRR)** | Uses forkable executable environments as free process rewards: restores decision points, samples alternative actions and rolls forward for step-level return contrasts. | 2026-09 | [arXiv:2609.33875](https://arxiv.org/abs/2609.33875) | ✅ New, confirmed |
| **Video2World** | Formulates autonomous video-to-simulation as a coding-agent task: build the simulated environment and robot behaviour from an embodied video. | 2026-10 | [arXiv:2610.04432](https://arxiv.org/abs/2610.04432) | ✅ New, confirmed |
| **ScienceIDE** | Turns scientific code repositories into agent-learnable environments, handling fragmented toolchains and implicit domain conventions. | 2026-09 | [arXiv:2609.19134](https://arxiv.org/abs/2609.19134) | ✅ New, confirmed |
| **SWE-Marathon** | Ultra-long-horizon software benchmark requiring sustained autonomous progress over hours, millions of tokens and complex environments. | 2026-06 | [arXiv:2606.07682](https://arxiv.org/abs/2606.07682) | ✅ New, confirmed |
| **Arctic-SWE** | Model-system co-design for long-horizon agent training, exposing the recipe and infrastructure needed for strong SWE RL. | 2026-10 | [arXiv:2610.24914](https://arxiv.org/abs/2610.24914) | ✅ New, confirmed |
| **Self-Play SWE-RL (SSR)** | Self-play driven software agent training that reduces reliance on human knowledge and hand-curated environments; **ICML 2026** | 2025-12 | [arXiv:2512.18552](https://arxiv.org/abs/2512.18552) | ✅ New, confirmed |
| **InterCode** | Framework standardizing interactive coding as multi-turn code-as-action across Bash, SQL and Python with execution feedback. | 2023-06 | [arXiv:2306.14898](https://arxiv.org/abs/2306.14898) | ✅ New, confirmed |
| **SWE-bench** | 2,294 real GitHub issue–PR pairs requiring repository-level fixes that pass tests; the canonical SWE environment. | 2023-10 | [arXiv:2310.06770](https://arxiv.org/abs/2310.06770) | ✅ New, confirmed |
| **RepoBench** | Repository-level code completion benchmark testing cross-file retrieval and dependency understanding. | 2023-06 | [arXiv:2306.03091](https://arxiv.org/abs/2306.03091) | ✅ New, confirmed |
| **DS-1000** | 1,000 real data-science coding problems across seven libraries with execution-based correctness checks. | 2022-11 | [arXiv:2211.11501](https://arxiv.org/abs/2211.11501) | ✅ New, confirmed |
| **CodeAct** | Unifies agent action space around executable Python, letting one code block perform multi-step tool use and self-correction. | 2024-02 | [arXiv:2402.01030](https://arxiv.org/abs/2402.01030) | ✅ New, confirmed |
| **DreamerV3** | General world-model RL that masters diverse domains with fixed hyperparameters, establishing world models as general environment representations. | 2023-01 | [arXiv:2301.04104](https://arxiv.org/abs/2301.04104) | ✅ New, confirmed |
| **IRIS** | Discrete-token world model (VQ-VAE observations + Transformer dynamics) achieving strong sample efficiency on Atari 100k. | 2022-09 | [arXiv:2209.00588](https://arxiv.org/abs/2209.00588) | ✅ New, confirmed |

---

## 6. Model-Based Simulation & Language World Models

| Paper/Framework | Key Contribution | Date/Venue | Link | Status |
|---|---|---|---|---|
| **ARE / GAIA2** | Meta Agents Research Environments; an extensible environment-creation platform + the asynchronous GAIA2 benchmark | 2025-09, Meta | [arXiv:2509.17158](https://arxiv.org/abs/2509.17158) | ✅ Confirmed |
| **Chimera** | Multi-agent enterprise threat simulation; environment + role simulation | 2025-08, **NDSS 2026** | [arXiv:2508.07745](https://arxiv.org/abs/2508.07745) | ✅ Confirmed |
| **WebWorld** | Large-scale open Web simulator; trained on 1M+ real Web interactions; supports 30+ step long-horizon simulation; trained Qwen3-14B gains +9.2% on WebArena; inference-time search as a world model surpasses GPT-5; cross-domain generalization to code, GUI and games | 2026-02, **ICML 2026**, Alibaba Qwen | [arXiv:2602.14721](https://arxiv.org/abs/2602.14721) | ✅ Confirmed |
| **Code2World** | A GUI world model via renderable code generation | **CVPR 2026** (there is also an ICML 2026 version) | [arXiv:2602.09856](https://arxiv.org/abs/2602.09856) | ✅ ID completed (was search-only) |
| **VirtualEnv** | Open-source simulation platform; programmatic task generation + game-like mechanics | 2026 | [arXiv:2601.07553](https://arxiv.org/abs/2601.07553) | ✅ Confirmed |
| **ProPlay** | Procedural world model; process-level rehearsal + process graphs; self-evolving LLM Agent | 2026-06 | [arXiv:2606.12780](https://arxiv.org/abs/2606.12780) | ✅ Confirmed |
| **EnvACE** | Replaces external environment interaction with world rehearsal; the policy emits a tool call first, then plays the environment to generate the response, with both roles optimized end-to-end; outperforms environment-scaling baselines on BFCL-v4 / τ²-Bench / VitaBench / FinMCP-Bench | 2026-08 | [arXiv:2608.06197](https://arxiv.org/abs/2608.06197) | ✅ Confirmed |
| **Simia** | Simulating environments with reasoning models: Simia-SFT (data synthesis) + Simia-RL, without real testbed data or APIs | 2025-11 | [arXiv:2511.01824](https://arxiv.org/abs/2511.01824) | ✅ New, confirmed |
| **Dyna-Mind** | Learning to simulate from experience to provide vicarious trial and error for long-horizon tasks | 2025-10 | [arXiv:2510.09577](https://arxiv.org/abs/2510.09577) | ✅ New, confirmed |
| **UI-Simulator** | LLMs as scalable, general-purpose simulators for evolving digital agent training | 2025-10 | [arXiv:2510.14969](https://arxiv.org/abs/2510.14969) | ✅ New, confirmed |
| **ViMo** | A generative visual GUI world model for app agents | 2025-04 | [arXiv:2504.13936](https://arxiv.org/abs/2504.13936) | ✅ New, confirmed |
| **DynaWeb** | Model-based reinforcement learning of web agents, replacing costly live-internet interaction with a learned world model | 2026-01 | [arXiv:2601.22149](https://arxiv.org/abs/2601.22149) | ✅ New, confirmed |
| **Is Your LLM Secretly a World Model of the Internet?** | Model-based planning for web agents that handles irreversible real-world actions where backtracking fails | 2024-11 | [arXiv:2411.06559](https://arxiv.org/abs/2411.06559) | ✅ New, confirmed |
| **Reinforcement World Model Learning (RWML)** | Self-supervised learning of action-conditioned world models on textual states with sim-to-real gap rewards; **NeurIPS 2026** | 2026-02 | [arXiv:2602.05842](https://arxiv.org/abs/2602.05842) | ✅ New, confirmed |
| **Trace2Env (From Traces to Agentic Worlds)** | A learning-free agentic language world model acts as the environment itself, supporting faithful stateful simulation | 2026-10 | [arXiv:2610.06100](https://arxiv.org/abs/2610.06100) | ✅ New, confirmed |
| **Agentic World Modeling without Environment Replica** | Agent test-time scaling without replicating the environment, relaxing the assumption that candidate trajectories can be executed in parallel | 2026-10 | [arXiv:2610.40927](https://arxiv.org/abs/2610.40927) | ✅ New, confirmed |
| **WildAWM (Agent World Model in the Wild)** | Synthesizes entire personal computers (GUI + MCP + CLI on shared state); 36 personas / 640 world states, ~170K DB records per world; XAI cross-interface tasks average 4.2 sub-tasks and 3.1 interface switches, 74.5% revisit an earlier interface; five quality gates cut 2,551 drafts to 341 tasks; verifier agrees with agent judge 95% (Cohen's κ=0.90); fully open-source pipeline; gains on 8 OOD benchmarks | 2026-10 | [arXiv:2610.26828](https://arxiv.org/abs/2610.26828) · [GitHub](https://github.com/MSR-Orchard/WildAWM) · [Page](https://msr-orchard.github.io/WildAWM/) | ✅ New, confirmed |
| **Genie** | Generative Interactive Environments | 2024-02 | [arXiv:2402.15391](https://arxiv.org/abs/2402.15391) | ✅ New, confirmed |
| **Learning Interactive Real-World Simulators** | Learning interactive real-world simulators | 2023-10 | [arXiv:2310.06114](https://arxiv.org/abs/2310.06114) | ✅ New, confirmed |
| **Posterior Twins** | Distributional behavioral simulation for enterprise decisions via memory-grounded digital twins | 2026-06 | [arXiv:2606.16415](https://arxiv.org/abs/2606.16415) | ✅ New, confirmed |
| **GenWorld** | Empirically grounded urban simulation infrastructure: building-level synthetic city + structured agent-environment interface + offline compilation of LLM decisions into lookup policies | 2026-06 | [arXiv:2606.27650](https://arxiv.org/abs/2606.27650) | ✅ New, confirmed |
| **DNative-Twin** | Graph-native digital twins that record a committed agentic decision as a typed trajectory and re-execute its mechanism | 2026-09 | [arXiv:2609.03787](https://arxiv.org/abs/2609.03787) | ✅ New, confirmed |
| **TwinLoop** | Simulation-in-the-loop digital twins for online multi-agent reinforcement learning | 2026-04 | [arXiv:2604.06610](https://arxiv.org/abs/2604.06610) | ✅ New, confirmed |
| **EnvGen** | Generating and adapting environments via LLMs for training embodied agents; **COLM 2024** | 2024-03 | [arXiv:2403.12014](https://arxiv.org/abs/2403.12014) | ✅ New, confirmed |
| **Active Zero** | Self-evolving vision-language models through active environment exploration | 2026-02 | [arXiv:2602.11241](https://arxiv.org/abs/2602.11241) | ✅ New, confirmed |
| **V-Dreamer** | Automating robotic simulation and trajectory synthesis via video generation priors | 2026-03 | [arXiv:2603.18811](https://arxiv.org/abs/2603.18811) | ✅ New, confirmed |
| **Adaptive Environment Generation for Embodied Agents** | Closed-loop environment generation that accounts for the agent's current performance instead of open-loop diversity | 2026-02 | [arXiv:2602.06366](https://arxiv.org/abs/2602.06366) | ✅ New, confirmed |
| **Automating the Design of Embodied Agent Architectures** | Transfers agent architecture search to perceptual embodied agents; **CoRL 2026** | 2026-06 | [arXiv:2606.30111](https://arxiv.org/abs/2606.30111) | ✅ New, confirmed |
| **SR-Platform** | An agentic pipeline for natural-language-driven robot simulation environment synthesis | 2026-05 | [arXiv:2605.14700](https://arxiv.org/abs/2605.14700) | ✅ New, confirmed |
| **CityPlanner / UrbanSandbox** | A sandbox agent for executable urban planning with a unified file-based environment | 2026-09 | [arXiv:2609.09578](https://arxiv.org/abs/2609.09578) | ✅ New, confirmed |
| **Automated Environment Design for Optimal Power Flow** | General automated RL environment design via multi-objective and hyperparameter optimization; **ACM e-Energy 2025** | 2025-05 | [arXiv:2505.07832](https://arxiv.org/abs/2505.07832) | ✅ New, confirmed |
| **COLOSSEUM** | A benchmark for evaluating generalization for robotic manipulation; **RSS 2024** | 2024-02 | [arXiv:2402.08191](https://arxiv.org/abs/2402.08191) | ✅ New, confirmed |
| **EmbodiSkill** | Skill-aware reflection for self-evolving embodied agents, transferring digital skill self-evolution to embodied settings | 2026-05 | [arXiv:2605.10332](https://arxiv.org/abs/2605.10332) | ✅ New, confirmed |
| **Sari Sandbox** | A photorealistic 3D retail store simulation with 250+ interactive grocery items, 3 store configurations and API control, supporting VR and embodied evaluation | 2025-08, **ICCV 2025 Workshop on Retail** | [arXiv:2508.00400](https://arxiv.org/abs/2508.00400) | ✅ New, confirmed |
| **GlobeBench** | A benchmark for text-based world models: 1,632 tasks across 5 domains and 19 simulation skills | 2026-10 | [arXiv:2610.22708](https://arxiv.org/abs/2610.22708) | ✅ New, confirmed |
| **World Models of Environment, Agent and Joint Systems** | Distinguishes world models by the channel they model: environment O→A, agent A→O, or joint | 2026-07 | [arXiv:2608.20401](https://arxiv.org/abs/2608.20401) | ✅ New, confirmed |
| **Ask the World Before Acting** | Environment probing calibrates the agent world model before acting, correcting beliefs that go stale as interactions accumulate | 2026-06 | [arXiv:2606.31422](https://arxiv.org/abs/2606.31422) | ✅ New, confirmed |
| **General Agents Contain World Models** | Formally proves that any agent generalizing to multi-step goal-directed tasks must learn a predictive model of its environment, extractable from the policy; **ICML 2025** | 2025-06 | [arXiv:2506.01622](https://arxiv.org/abs/2506.01622) | ✅ New, confirmed |
| **Learning Generative Interactive Environments by Trained Agent Exploration** | Uses trained agent exploration instead of random agents to improve generative interactive environment learning | 2024-09 | [arXiv:2409.06445](https://arxiv.org/abs/2409.06445) | ✅ New, confirmed |
| **PatchWorld** | Induces executable code as a world model from black-box text observations via gradient-free optimization, without ground-truth latent states or transition models. | 2026-05 | [arXiv:2605.30880](https://arxiv.org/abs/2605.30880) | ✅ New, confirmed |
| **From Word to World** | Studies whether and when LLMs can reliably act as implicit text-based world models that genuinely benefit agent learning. | 2025-12 | [arXiv:2512.18832](https://arxiv.org/abs/2512.18832) | ✅ New, confirmed |
| **Do Enterprise Systems Need Learned World Models?** | Argues enterprise dynamics are tenant-specific and drifting, so context to infer rules matters more than learned transition models. | 2026-05 | [arXiv:2605.12178](https://arxiv.org/abs/2605.12178) | ✅ New, confirmed |
| **Social World Model** | Unifies social interaction trajectories into structured, iterable signals so social intelligence accumulates rather than being statically evaluated. | 2026-06 | [arXiv:2606.21315](https://arxiv.org/abs/2606.21315) | ✅ New, confirmed |
| **Economic World Models** | Implementation roadmap for Economic World Models that simulate economies from within via heterogeneous agents, beliefs, actions and market/institutional mechanisms. | 2026-08 | [arXiv:2608.06020](https://arxiv.org/abs/2608.06020) | ✅ New, confirmed |
| **MoWorld** | Flash world model optimizing data generation, pretraining, distillation and inference for high-frame-rate responsiveness. | 2026-07 | [arXiv:2607.06216](https://arxiv.org/abs/2607.06216) | ✅ New, confirmed |
| **iWorld-Bench** | Unified benchmark and dataset for interactive world models with a unified action-generation framework, evaluating physical interaction capability. | 2026-05 | [arXiv:2605.03941](https://arxiv.org/abs/2605.03941) | ✅ New, confirmed |
| **World Model for Robot Learning (Survey)** | Survey organizing robot-learning world models by architecture, functional role (policy, planning, simulation, evaluation, data generation) and embodied application. | 2026-04 | [arXiv:2605.00080](https://arxiv.org/abs/2605.00080) | ✅ New, confirmed |
| **Robotic Video World Models (Survey)** | Survey of robotic video world models, their advantages over physics simulators, applications and open challenges. | 2026-01 | [arXiv:2601.07823](https://arxiv.org/abs/2601.07823) | ✅ New, confirmed |
| **The Robot Data Factory** | Argues robot experience (interaction preserving the perception-action-consequence loop) rather than raw data is the key resource, and designs a data factory around it. | 2026-09 | [arXiv:2609.16705](https://arxiv.org/abs/2609.16705) | ✅ New, confirmed |
| **RoboDream** | Compositional world models for scalable robot data synthesis, avoiding superficial visual augmentation and embodiment hallucinations. | 2026-06 | [arXiv:2606.02577](https://arxiv.org/abs/2606.02577) | ✅ New, confirmed |
| **RoboChemGym** | Protocol-driven generative simulation for long-horizon chemical manipulation demos, addressing scarce and safety-critical wet-lab data. | 2026-10 | [arXiv:2610.02708](https://arxiv.org/abs/2610.02708) | ✅ New, confirmed |

---

## 7. Task / Scenario Synthesis

| Paper/Framework | Key Contribution | Date/Venue | Link | Status |
|---|---|---|---|---|
| **Graph2Eval** | Knowledge-graph-driven multimodal task generation; document understanding + Web interaction; 1319 tasks | 2025-10, **CVPR 2026** | [arXiv:2510.00507](https://arxiv.org/abs/2510.00507) | ✅ Confirmed |
| **SimpleQA→DeepResearch** | Iterative task evolution via Explorer–Formalizer–Challenger; 500 verifiable deep-research tasks | 2026-08 | [arXiv:2608.02163](https://arxiv.org/abs/2608.02163) | ✅ Confirmed |
| **AgenticDataBench** | Skill clustering + LLM task generation to build a data-Agent benchmark | 2026-07, Tsinghua & Ant Group | [arXiv:2607.01647](https://arxiv.org/abs/2607.01647) | ✅ Confirmed |
| **ART** | Action-based Reasoning clinical task benchmark for medical AI Agents; four-stage pipeline; 600 tasks; retrieval is near-perfect, aggregate reasoning 28–64%, threshold reasoning 32–38% | 2026-01 | [arXiv:2601.08988](https://arxiv.org/abs/2601.08988) | ✅ Confirmed |
| **ACuRL** | Autonomous curriculum RL; environment exploration–curriculum generation–continuous adaptation, with zero human data | 2026-02, OSU-NLP-Group | [arXiv:2602.10356](https://arxiv.org/abs/2602.10356) | ✅ Confirmed |
| **State2State** | Derives intermediate training tasks from environment exploration states, with state-matching verification | 2026-08, THUNLP | [arXiv:2608.04934](https://arxiv.org/abs/2608.04934) | ✅ Confirmed |
| **SESA** | Self-play search Agent; question-setter–solver architecture that needs no external question bank | 2026-07 | [arXiv:2607.29468](https://arxiv.org/abs/2607.29468) | ✅ Confirmed |
| **Gym-V** | 179 procedural visual environments across 10 domains, with controllable difficulty | 2026 | [arXiv:2603.15432](https://arxiv.org/abs/2603.15432) | ✅ Confirmed |
| **InternAgentHarness (BOOTCAMPCLI)** | Four-layer environment definition, automatically converting training paradigms into harnesses | 2025-08 | [arXiv:2508.08636](https://arxiv.org/abs/2508.08636) | ✅ Confirmed |
| **RandomWorld (Procedural Environment Generation for Tool-Use Agents)** | Procedurally generates interactive tools and compositional tool-use data, fixing the non-interactive / non-compositional gap; **EMNLP 2025** | 2025-05 | [arXiv:2506.11045](https://arxiv.org/abs/2506.11045) | ✅ New, confirmed |
| **Doc2Agent** | Scalable generation of tool-using agents and executable Python tools from API documentation | 2025-06 | [arXiv:2506.19998](https://arxiv.org/abs/2506.19998) | ✅ New, confirmed |
| **Reasoning Gym** | Over 100 reasoning-environment data generators and verifiers with adjustable complexity and unbounded generation; **NeurIPS 2025 Spotlight** | 2025-05 | [arXiv:2505.24760](https://arxiv.org/abs/2505.24760) | ✅ New, confirmed |
| **Depth Before Breadth** | Reverse-to-forward curriculum with advantage decomposition over a policy-induced capability region | 2026-11 | [arXiv:2611.24697](https://arxiv.org/abs/2611.24697) | ✅ New, confirmed |
| **Curriculum Guided Massive Multi Agent System Solving** | Curriculum-guided large-scale multi-agent system solving for robust long-horizon tasks | 2025-12 | [arXiv:2512.08545](https://arxiv.org/abs/2512.08545) | ✅ New, confirmed |
| **SearchMaster** | Grounded and regulated self-play for search agents | 2026-08 | [arXiv:2608.01822](https://arxiv.org/abs/2608.01822) | ✅ New, confirmed |
| **Vision-DeepResearch Benchmark** | Rethinks visual and textual search for MLLMs, removing answer leakage through textual cues | 2026-02 | [arXiv:2602.02185](https://arxiv.org/abs/2602.02185) | ✅ New, confirmed |
| **API-BLEND** | A comprehensive corpus for training and benchmarking API LLMs; **ACL 2024 Main** | 2024-02 | [arXiv:2402.15491](https://arxiv.org/abs/2402.15491) | ✅ New, confirmed |
| **A Framework for Testing and Adapting REST APIs as LLM Tools** | A framework for testing REST APIs and adapting them as LLM tools | 2025-04 | [arXiv:2504.15546](https://arxiv.org/abs/2504.15546) | ✅ New, confirmed |
| **AgentDrive** | LLM prompt generates JSON driving scenarios; 300K scenarios | 2026-01 | [arXiv:2601.16964](https://arxiv.org/abs/2601.16964) | ✅ Confirmed |
| **EigenData** | A self-evolving multi-agent platform covering the full function-calling data lifecycle: synthesis, auditing and repair | 2026-03 | [arXiv:2603.05553](https://arxiv.org/abs/2603.05553) | ✅ New, confirmed |
| **Scaling Synthetic Task Generation for Agents via Exploration** | Scales synthetic task generation via exploration to produce diverse, feasible and verifiable agent tasks | 2025-09 | [arXiv:2509.25047](https://arxiv.org/abs/2509.25047) | ✅ New, confirmed |
| **DIVE** | Inverts synthesis order: executes diverse real tools first, then reverse-derives tasks strictly entailed by traces; scales tool-pool coverage and per-task toolset variety. | 2026-03 | [arXiv:2603.11076](https://arxiv.org/abs/2603.11076) | ✅ New, confirmed |
| **Synthesizing Agentic Data for Web Agents (Progressive Difficulty)** | Web-agent data synthesis with progressive difficulty enhancement for long-horizon deep-research tasks. | 2025-10 | [arXiv:2510.13913](https://arxiv.org/abs/2510.13913) | ✅ New, confirmed |
| **Meta-Task** | Turns terminal-task synthesis into a terminal task, so agents themselves scale the production of verifiable terminal tasks and trajectories. | 2026-07 | [arXiv:2607.27929](https://arxiv.org/abs/2607.27929) | ✅ New, confirmed |
| **NexForge** | Requirement-driven task synthesis that escapes substrate-bound generation tied to predefined tools. | 2026-07 | [arXiv:2607.14186](https://arxiv.org/abs/2607.14186) | ✅ New, confirmed |

---

## 8. MCP Tool Environments & Ecosystem

| Paper/Framework | Key Contribution | Date/Venue | Link | Status |
|---|---|---|---|---|
| **MCP-Universe** | The first comprehensive benchmark for LLMs on real-world Model Context Protocol servers; long-horizon reasoning and large unfamiliar tool spaces | 2025-08 | [arXiv:2508.14704](https://arxiv.org/abs/2508.14704) · [Page](https://mcp-universe.github.io) | ✅ New, confirmed |
| **MCP-Atlas** | Large-scale tool-use benchmark against production MCP servers; cross-server orchestration plus structured claim-level scoring | 2026-01 | [arXiv:2602.00933](https://arxiv.org/abs/2602.00933) | ✅ New, confirmed |
| **MCP-Bench** | 28 representative live MCP servers with 250 tools across finance, travel, scientific computing and academic search | 2025-08 | [arXiv:2508.20453](https://arxiv.org/abs/2508.20453) | ✅ New, confirmed |
| **MCP-Zero** | Active tool discovery: the LLM identifies capability gaps and requests tools on demand instead of receiving all schemas | 2025-06 | [arXiv:2506.01056](https://arxiv.org/abs/2506.01056) | ✅ New, confirmed |
| **MCPEvol-Bench** | Benchmarks agent performance across dynamic evolutions of MCP servers | 2026-07 | [arXiv:2607.14642](https://arxiv.org/abs/2607.14642) | ✅ New, confirmed |
| **Live API-Bench** | Converts NL2SQL datasets into interactive API environments with 2,500+ live APIs | 2025-06 | [arXiv:2506.11266](https://arxiv.org/abs/2506.11266) | ✅ New, confirmed |
| **StableToolBench-MirrorAPI** | Models tool environments as mirrors of 7,000+ real-world APIs | 2025-03 | [arXiv:2503.20527](https://arxiv.org/abs/2503.20527) | ✅ New, confirmed |
| **MCP-Flow** | Automated MCP server discovery, data synthesis and model training; **ACL 2026 Main** | 2025-10 | [arXiv:2510.24284](https://arxiv.org/abs/2510.24284) | ✅ New, confirmed |
| **SynthTools** | A fully LLM-based framework for scaling synthetic tools and tool-use environments | 2025-11 | [arXiv:2511.09572](https://arxiv.org/abs/2511.09572) | ✅ New, confirmed |
| **Gecko** | A simulation environment with stateful feedback for refining agent tool calls | 2026-02 | [arXiv:2602.19218](https://arxiv.org/abs/2602.19218) | ✅ New, confirmed |
| **MCP-Universe RL** | A framework for training MCP tool-use agents via reinforcement learning | 2026-08 | [arXiv:2608.22167](https://arxiv.org/abs/2608.22167) | ✅ New, confirmed |
| **ToolSandbox (Apple)** | Stateful multi-tool sandbox with assertion-based verification | — | [GitHub](https://github.com/apple/ToolSandbox) | ✅ New, confirmed |
| **ToolSpace** | Tool-centric MCP environment synthesis that mines data/state/retry dependencies from real MCP call traces before deriving interfaces and workflows. | 2026-11 | [arXiv:2611.05036](https://arxiv.org/abs/2611.05036) | ✅ New, confirmed |
| **STT-Arena** | More realistic tool-use arena with spatio-temporal dynamics that invalidate plans mid-task, testing replanning. | 2026-05 | [arXiv:2605.18548](https://arxiv.org/abs/2605.18548) | ✅ New, confirmed |
| **ToolHazard** | Scales adversarial environments with indirect prompt injections embedded in environmental state for agent security evaluation. | 2026-08 | [arXiv:2608.11878](https://arxiv.org/abs/2608.11878) | ✅ New, confirmed |
| **MLToolBench** | Tool-augmented environment for machine-learning development agents that learn through ML experimentation. | 2026-09 | [arXiv:2609.36679](https://arxiv.org/abs/2609.36679) | ✅ New, confirmed |
| **Tool Description Rewriting** | Learns to rewrite tool descriptions for reliable agent tool use, shifting optimization from the agent to the interface. | 2026-02 | [arXiv:2602.20426](https://arxiv.org/abs/2602.20426) | ✅ New, confirmed |

---

## 9. Enterprise / Office / Scientific & Professional Environments

| Paper/Framework | Key Contribution | Date/Venue | Link | Status |
|---|---|---|---|---|
| **OfficeBench** | Office automation benchmark across multiple applications, requiring integration of many information sources and multi-step decisions | 2024-07 | [arXiv:2407.19056](https://arxiv.org/abs/2407.19056) | ✅ New, confirmed |
| **AppWorld** | A controllable world of apps and people: 457 APIs / 750 tasks with database-state checks; **ACL 2024** | 2024-07 | [arXiv:2407.18901](https://arxiv.org/abs/2407.18901) | ✅ New, confirmed |
| **TheAgentCompany** | 175 consequential real-world tasks (messaging, code hosting, cloud storage, project management) with checkpoint-based evaluation | 2024-12 | [arXiv:2412.14161](https://arxiv.org/abs/2412.14161) | ✅ New, confirmed |
| **ScienceBoard** | Evaluating multimodal autonomous agents in realistic scientific workflows; **ICLR 2026** | 2025-05 | [arXiv:2505.19897](https://arxiv.org/abs/2505.19897) | ✅ New, confirmed |
| **FieldWorkArena** | Agentic AI benchmark for real field work in manufacturing and retail; **ICPR 2026** | 2025-05 | [arXiv:2505.19662](https://arxiv.org/abs/2505.19662) | ✅ New, confirmed |
| **ChemX** | 10 manually curated, domain-expert-validated datasets for automated chemical information extraction | 2025-10 | [arXiv:2510.00795](https://arxiv.org/abs/2510.00795) | ✅ New, confirmed |
| **DevOps-Gym** | Benchmarking AI agents across the full software DevOps cycle (develop, deploy, manage) | 2026-01 | [arXiv:2601.20882](https://arxiv.org/abs/2601.20882) | ✅ New, confirmed |
| **ProactiveMobile** | A benchmark for proactive intelligence on mobile devices | 2026-02 | [arXiv:2602.21858](https://arxiv.org/abs/2602.21858) | ✅ New, confirmed |
| **PIRA-Bench** | A transition from reactive GUI agents to GUI-based proactive intent recommendation | 2026-03 | [arXiv:2603.08013](https://arxiv.org/abs/2603.08013) | ✅ New, confirmed |
| **ProAgentBench** | Evaluating proactive assistance with real-world data rather than LLM-synthesized data | 2026-02 | [arXiv:2602.04482](https://arxiv.org/abs/2602.04482) | ✅ New, confirmed |
| **Proactive Agent Research Environment (Pare)** | Simulates active users to evaluate proactive assistants, modeling apps as stateful sequential interaction rather than flat tool APIs | 2026-04 | [arXiv:2604.00842](https://arxiv.org/abs/2604.00842) | ✅ New, confirmed |
| **PersonaMem-v2** | Personalized-intelligence dataset: 1,000 realistic user-chatbot interactions, 300+ scenarios, 20,000+ implicit preferences, 128K-token contexts | 2025-12 | [arXiv:2512.06688](https://arxiv.org/abs/2512.06688) | ✅ New, confirmed |
| **ASTRA-bench** | Unifies time-evolving personal context with an interactive toolbox; 2,413 scenarios across four protagonists | 2026-03 | [arXiv:2603.01357](https://arxiv.org/abs/2603.01357) | ✅ New, confirmed |
| **EverMemBench** | The first benchmark for long-horizon memory in multi-party collaborative dialogues | 2026-02 | [arXiv:2602.01313](https://arxiv.org/abs/2602.01313) | ✅ New, confirmed |
| **CyberGym** | 1,507 real-world vulnerabilities across 188 software projects | 2025-06 | [arXiv:2506.02548](https://arxiv.org/abs/2506.02548) | ✅ New, confirmed |
| **OS-Harm** | A benchmark for measuring safety of computer use agents; **NeurIPS 2025 Datasets & Benchmarks Spotlight** | 2025-06 | [arXiv:2506.14866](https://arxiv.org/abs/2506.14866) | ✅ New, confirmed |
| **DoomArena** | A plug-in security evaluation framework with detailed threat modeling for agentic frameworks | 2025-04 | [arXiv:2504.14064](https://arxiv.org/abs/2504.14064) | ✅ New, confirmed |
| **SafetyFlow** | An agent-flow system for automated LLM safety benchmarking | 2025-08 | [arXiv:2508.15526](https://arxiv.org/abs/2508.15526) | ✅ New, confirmed |
| **GHIssuemarket** | A sandbox environment for SWE-agent economic experimentation | 2024-12 | [arXiv:2412.11722](https://arxiv.org/abs/2412.11722) | ✅ New, confirmed |
| **ML-Bench** | Evaluating LLMs and agents on machine learning tasks at repository scale | 2023-11 | [arXiv:2311.09835](https://arxiv.org/abs/2311.09835) | ✅ New, confirmed |
| **Unified Emulation-Simulation Training Environment for Autonomous Cyber Agents** | A unified emulation-simulation training environment for autonomous cyber agents | 2023-04 | [arXiv:2304.01244](https://arxiv.org/abs/2304.01244) | ✅ New, confirmed |
| **SciAgentGym** | Scalable interactive environment with 1,780 domain tools across four natural-science disciplines for multi-step scientific tool orchestration. | 2026-02 | [arXiv:2602.12984](https://arxiv.org/abs/2602.12984) | ✅ New, confirmed |
| **D3-Gym** | First automatically constructed dataset of verifiable environments for scientific data-driven discovery (565 tasks). | 2026-04 | [arXiv:2604.27977](https://arxiv.org/abs/2604.27977) | ✅ New, confirmed |
| **Spreadsheet-RL** | Trains spreadsheet agents with RL on realistic Excel/Sheets tasks instead of specialized prompting. | 2026-05 | [arXiv:2605.22642](https://arxiv.org/abs/2605.22642) | ✅ New, confirmed |
| **EnterpriseSynth** | Zero-execution framework turning OpenAPI specs into SFT and evaluation data, avoiding access, compliance and production-data risk. | 2026-10 | [arXiv:2610.22412](https://arxiv.org/abs/2610.22412) | ✅ New, confirmed |
| **MEDVISTAGYM** | Scalable training environment for tool-integrated RL with medical images, enabling iterative re-examination of visual evidence. | 2026-01 | [arXiv:2601.07107](https://arxiv.org/abs/2601.07107) | ✅ New, confirmed |
| **MedAgentGym** | Scalable agentic training environment for code-centric biomedical data-science reasoning. | 2025-06 | [arXiv:2506.04405](https://arxiv.org/abs/2506.04405) | ✅ New, confirmed |
| **Healthcare AI GYM** | Clinical-reasoning gym covering history taking, test ordering, result interpretation and safe treatment planning as a multi-step loop. | 2026-05 | [arXiv:2605.02943](https://arxiv.org/abs/2605.02943) | ✅ New, confirmed |
| **6GAgentGym** | 6G network-management agent gym with tool use, data synthesis and agentic learning over observable state changes. | 2026-03 | [arXiv:2603.29656](https://arxiv.org/abs/2603.29656) | ✅ New, confirmed |
| **PatEx-Gym** | Agent environment for patent prior-art search and novelty assessment under sparse evidence. | 2026-10 | [arXiv:2610.33503](https://arxiv.org/abs/2610.33503) | ✅ New, confirmed |
| **EO-Gym** | Multimodal interactive environment for Earth-observation agents, where resolving uncertainty requires expanding regions and retrieving history. | 2026-05 | [arXiv:2605.01250](https://arxiv.org/abs/2605.01250) | ✅ New, confirmed |
| **AgentBench** | Eight interactive environments (OS, DB, KG, games, web, etc.) for the first systematic cross-environment LLM-agent benchmark. | 2023-08 | [arXiv:2308.03688](https://arxiv.org/abs/2308.03688) | ✅ New, confirmed |

---

## 10. Platforms / Infrastructure / Methodology

| Paper/Framework | Key Contribution | Date/Venue | Link | Status |
|---|---|---|---|---|
| **AgenticAI-Supervisor** | UI-driven simulation engine; thousands of parallel isolated trajectories; simulation as creation | 2026-07 | [arXiv:2607.05773](https://arxiv.org/abs/2607.05773) | ✅ Confirmed |
| **ClawGym II** | Black-box RL against real Agent harnesses (OpenClaw / Claude Code); 30 tasks | 2026-08, Renmin University Gaoling & IQuest | [arXiv:2608.16798](https://arxiv.org/abs/2608.16798) | ✅ Confirmed |
| **OccuBench** | Language environments simulate real occupational tasks; multidisciplinary, asynchronous settings | 2026-04 | [arXiv:2604.10866](https://arxiv.org/abs/2604.10866) | ✅ Confirmed |
| **AgentGym2** | De-idealized evaluation framework on real environments; 27 domains; measures exploratory tool discovery, tool composition and noise robustness | 2026-07, **ACL 2026 Long** | [arXiv:2607.05174](https://arxiv.org/abs/2607.05174) | ✅ Confirmed |
| **TUA-Bench** | General-purpose terminal Agent benchmark; 120 tasks / 5 major categories | 2026-06, Meta | [arXiv:2606.28480](https://arxiv.org/abs/2606.28480) | ✅ Confirmed |
| **AgencyBench** | 138 tasks / 32 scenarios; million-token-scale long-horizon context | 2026-01 | [arXiv:2601.11044](https://arxiv.org/abs/2601.11044) | ✅ Confirmed |
| **Hierarchy of Agentic Capabilities** | Evaluates the hierarchy of Agent capabilities in real RL environments | 2026-01 | [arXiv:2601.09032](https://arxiv.org/abs/2601.09032) | ✅ Confirmed |
| **Efficient Benchmarking of AI Agents** | Study of sampling efficiency across 8 Agent benchmarks | 2026-03 | [arXiv:2603.23749](https://arxiv.org/abs/2603.23749) | ✅ Confirmed |
| **OSGym** | CUA training infrastructure supporting 1024 parallel sandboxes | 2025 | [arXiv:2511.11672](https://arxiv.org/abs/2511.11672) | ✅ Confirmed |
| **EnvHarness** | A programmable layer wraps static environments to accelerate Agent learning without building new environments; Google Research | 2026 | [arXiv:2608.19880](https://arxiv.org/abs/2608.19880) | ✅ Confirmed |
| **Harbor-Index 1.0** | 6627 candidates filtered down to 82 tasks; difficulty filtering + AI/human audit hardening pipeline | 2026-07 | [harbor-index.org](https://harbor-index.org/) | ✅ Confirmed |
| **Environment Scaling Survey** | The GEF loop (Generate-Execute-Feedback) as a unified survey of environment scaling | 2025-11 | [arXiv:2511.09586](https://arxiv.org/abs/2511.09586) | ✅ Confirmed (same work as Section 1) |
| **Agentic Environment Engineering Survey** | Systematic survey from the environment-engineering lifecycle perspective: modeling → synthesis → evaluation → application; covers both symbolic and neural synthesis paradigms | 2026-06 | [arXiv:2606.12191](https://arxiv.org/abs/2606.12191) | ✅ Confirmed |
| **AgentJudgeBench** | 3,808 dependency-driven agentic workflows; 6 DAG topologies; 3 difficulty tiers; on hard queries all judges converge to a 77–82% accuracy ceiling | **EMNLP 2026 Main** | [arXiv:2608.26623](https://arxiv.org/abs/2608.26623) | ✅ Confirmed |
| **Benchmark Radar** | A living database and search engine for AI benchmarks; tracks 14,810+ records across 37 sources; offers a dashboard, CLI, RSS and full dataset downloads; technical report arXiv:2609.11115 | — | [GitHub](https://github.com/ktwu01/benchmark-radar) · [Dashboard](https://benchmark-radar.org/) | ✅ Confirmed |
| **ProRL Agent** | Rollout-as-a-Service for RL training of multi-turn LLM agents, decoupling rollout orchestration from the training loop | 2026-03 | [arXiv:2603.18815](https://arxiv.org/abs/2603.18815) | ✅ New, confirmed |
| **VenusRL** | A fully disaggregated agentic RL system with priority scheduling and scalable interaction | 2026-10 | [arXiv:2610.03286](https://arxiv.org/abs/2610.03286) | ✅ New, confirmed |
| **The Rollout Infrastructure Tax** | Comparative study of single containers, hosted sandboxes, Kubernetes-orchestrated containers and cloud VMs for coding-agent RL | 2026-07 | [arXiv:2607.01415](https://arxiv.org/abs/2607.01415) | ✅ New, confirmed |
| **ReCreate** | Reasoning and creating domain agents driven by experience | 2026-01 | [arXiv:2601.11100](https://arxiv.org/abs/2601.11100) | ✅ New, confirmed |
| **AgentFactory** | Towards automated agentic system design and optimization | 2026-09 | [arXiv:2609.01045](https://arxiv.org/abs/2609.01045) | ✅ New, confirmed |
| **Agent²** | An agent-generates-agent framework for RL automation | 2025-09 | [arXiv:2509.13368](https://arxiv.org/abs/2509.13368) | ✅ New, confirmed |
| **Youtu-Agent** | Automated generation and hybrid policy optimization for agent productivity | 2025-12 | [arXiv:2512.24615](https://arxiv.org/abs/2512.24615) | ✅ New, confirmed |
| **QUEST** | Trains frontier deep-research agents on fully synthetic, verifiable tasks instead of real query logs. | 2026-05 | [arXiv:2605.24218](https://arxiv.org/abs/2605.24218) | ✅ New, confirmed |
| **SAGE (Deep Search Data Generation)** | Steerable agentic data generation for deep search, using execution feedback to improve data quality and task diversity. | 2026-01 | [arXiv:2601.18202](https://arxiv.org/abs/2601.18202) | ✅ New, confirmed |
| **Orchard** | Open-source agentic modeling framework unifying data and training pipelines for planning, tool use and multi-turn interaction. | 2026-05 | [arXiv:2605.15040](https://arxiv.org/abs/2605.15040) | ✅ New, confirmed |
| **ActionStudio** | Lightweight framework for data and training of large action models, unifying heterogeneous trajectory sources. | 2025-03 | [arXiv:2503.22673](https://arxiv.org/abs/2503.22673) | ✅ New, confirmed |
| **GEM (Gym for Agentic LLMs)** | A gym for agentic LLMs shifting training from static datasets to experience-based learning in interactive environments. | 2025-10 | [arXiv:2510.01051](https://arxiv.org/abs/2510.01051) | ✅ New, confirmed |
| **Jaxnasium** | Any-agent, cross-suite JAX RL interface using PyTrees to unify environment suites under accelerated training. | 2026-10 | [arXiv:2610.36075](https://arxiv.org/abs/2610.36075) | ✅ New, confirmed |
| **Agentic RL Survey** | Survey of agentic RL for LLMs covering environments, rewards, data and training paradigms. | 2025-09 | [arXiv:2509.02547](https://arxiv.org/abs/2509.02547) | ✅ New, confirmed |
| **AI Scientist via Synthetic Task Scaling** | Synthesizes ML challenge tasks compatible with SWE-Agent (topic sampling, dataset proposal, code generation) | 2026-03 | [arXiv:2603.17216](https://arxiv.org/abs/2603.17216) | ✅ New, confirmed |
| **AgenticDataBench** | Data-agent benchmark built by skill clustering plus LLM task generation | 2026-07 | [arXiv:2607.01647](https://arxiv.org/abs/2607.01647) | ✅ New, confirmed |

---

## 11. Sandbox Infra

| Project | Description | Date | Link | Notes |
|---|---|---|---|---|
| **AgentENV (AENV)** | High-throughput distributed agent environment platform jointly open-sourced by Moonshot AI and kvcache-ai; strong-isolation Linux sandboxes on Firecracker microVMs, built for Kimi K3 agentic RL; snapshot, fork and on-demand image loading, start/restore <50ms, pause <100ms, E2B SDK compatible | 2026-07 | [github.com/kvcache-ai/AgentENV](https://github.com/kvcache-ai/AgentENV) | ✅ Confirmed; open-sourced 2026-07-27 |
| **WeEnv** | WeChat's full-lifecycle environment management system for agentic RL covering packaging, initialization and elastic provisioning; layer-group reuse, on-demand pull and elastic CPU/memory quotas cut environment initialization cost 5.6–14.2× and drop environment share of iteration time from up to 53.4% to 9.1% | 2026-09 | [arXiv:2609.30766](https://arxiv.org/abs/2609.30766) | ✅ Confirmed; submitted 2026-09-25 |
| **DeepSeek Elastic Compute (DSec)** | Production-grade sandbox infrastructure unifying FnCall, container, microVM and full-VM backends; ~160 nodes / 30K cores / 250TB memory per production unit, ~3M sandboxes daily, >380K peak concurrency, >5,000 creations/sec; all DeepSeek V3.2–V4.1 RL training and evaluation run on DSec | 2026-09 | [arXiv:2609.22978](https://arxiv.org/abs/2609.22978) | ✅ Confirmed; submitted 2026-09-19; 130+ authors |
| **Sandman** | A sandbox service built and operated at Amazon for large-scale agentic RL workloads in production on shared Kubernetes; a small daemon mounted into unmodified task images preserves files and processes across calls and paces creation | 2026-10 | [arXiv:2610.39711](https://arxiv.org/abs/2610.39711) | ✅ New, confirmed |
| **Readie** | Low-latency code sandboxes that attack the root cause of slow startup, decoupling agent harness from code execution | 2026-11 | [arXiv:2611.22171](https://arxiv.org/abs/2611.22171) | ✅ New, confirmed |
| **VenusRL** | A fully disaggregated agentic RL system with priority scheduling and scalable interaction | 2026-10 | [arXiv:2610.03286](https://arxiv.org/abs/2610.03286) | ✅ New, confirmed |
| **ProRL Agent** | Rollout-as-a-Service infrastructure for multi-turn LLM agent RL | 2026-03 | [arXiv:2603.18815](https://arxiv.org/abs/2603.18815) | ✅ New, confirmed |
| **SideKernel** | A usable microVM sandbox for AI coding agents on macOS; survey shows fewer than 40% of users sandbox their agents | 2026-10 | [arXiv:2610.02456](https://arxiv.org/abs/2610.02456) | ✅ New, confirmed |
| **Fault-Tolerant Sandboxing for AI Coding Agents** | Policy-based interception layer plus transactional semantics for safe autonomous execution, balancing destructive commands and system-state consistency | 2025-12 | [arXiv:2512.12806](https://arxiv.org/abs/2512.12806) | ✅ New, confirmed |
| **CUA-Sandbox** | Efficient environments for computer-use agent RL; state capsule + signed route capability + generation lease give state-scoped execution and transactional lifecycles; up to 6.20× rollout throughput, 9.2× memory reduction and 504× less incremental storage on WebArena-Lite / VisualWebArena / OSWorld | 2026-09 | [arXiv:2609.32750](https://arxiv.org/abs/2609.32750) · [GitHub](https://github.com/windskyyx/Cua-Sandbox) | ✅ Confirmed; first author Xin Yan, corresponding author Xingrui Yu; 14 authors from A*STAR, HKUST, BNU, NUS, NTU, ZJU, PKU |
| **OpenEnv** | PyTorch's RL environment interface library; AWM and other environments have been merged into it | — | [GitHub](https://github.com/meta-pytorch/OpenEnv) | ✅ New, confirmed |
| **verifiers** | Prime Intellect's library for RL environments and evaluation | — | [GitHub](https://github.com/PrimeIntellect-ai/verifiers) | ✅ New, confirmed |
| **Harbor** | Task format and execution framework unifying RL task packages (instruction + environment + reference solution + verifier) | — | [GitHub](https://github.com/laude-institute/harbor) | ✅ New, confirmed |
| **agent-infra/sandbox** | Agent sandbox runtime | — | [GitHub](https://github.com/agent-infra/sandbox) | ✅ New, confirmed |
| **kubernetes-sigs/agent-sandbox** | Kubernetes SIG implementation of agent sandboxes | — | [GitHub](https://github.com/kubernetes-sigs/agent-sandbox) | ✅ New, confirmed |
| **alibaba/OpenSandbox** | Alibaba's open-source sandbox infrastructure | — | [GitHub](https://github.com/alibaba/OpenSandbox) | ✅ New, confirmed |
| **E2B** | Cloud sandbox infrastructure for agents supporting parallel rollouts | — | [GitHub](https://github.com/e2b-dev/E2B) | ✅ New, confirmed |
| **inclusionAI/AEnvironment** | InclusionAI's open-source agent environment framework | — | [GitHub](https://github.com/inclusionAI/AEnvironment) | ✅ New, confirmed |
| **SWE-MiniSandbox** | Container-free SWE agent RL training sandbox | 2026-02 | [arXiv:2602.11210](https://arxiv.org/abs/2602.11210) | ✅ New, confirmed |
| **Polar** | Scales agentic RL on any harness by abstracting long-context management, multi-turn tool use and multi-agent interaction. | 2026-05 | [arXiv:2605.24220](https://arxiv.org/abs/2605.24220) | ✅ New, confirmed |
| **EnvSched** | Environment-aware scheduling that allocates rollouts by difficulty and verification cost under finite budget. | 2026-10 | [arXiv:2610.37609](https://arxiv.org/abs/2610.37609) | ✅ New, confirmed |
| **ThunderSync** | Lossless acceleration of agentic RL by optimizing rollout-training synchronization in long-horizon environments. | 2026-10 | [arXiv:2610.05935](https://arxiv.org/abs/2610.05935) | ✅ New, confirmed |
| **ECHO** | Terminal agents learn world models for free from command output streams, which already encode environment dynamics. | 2026-05 | [arXiv:2605.24517](https://arxiv.org/abs/2605.24517) | ✅ New, confirmed |

---

## 12. CUA / Computer Use

| Work | arXiv Link | Summary & Venue | Status |
|---|---|---|---|
| Gym-Anything: Turn any Software into an Agent Environment | [arXiv:2604.06126](https://arxiv.org/abs/2604.06126) | Multi-agent pipeline turns any software into an interactive CUA environment, building CUA-World (200 applications, 10K+ long-horizon tasks) and CUA-World-Long (>500 steps) | ✅ Confirmed, arXiv 2026.04 |
| CUA-GYM | [arXiv:2605.25624](https://arxiv.org/abs/2605.25624) | Generator/Discriminator dual-agent collaboration produces verifiable RLVR training tuples: 32,112 examples across 110 environments; CUA-GYM-A17B reaches 72.6% on OSWorld-Verified | ✅ Confirmed, arXiv 2026.05 |
| CUA-Lite | [UC Berkeley RDI blog](https://rdi.berkeley.edu/blog/cua-lite/) | Unifies Lite.Gym / Lite.Sample / model harness; 15+ benchmarks, 10+ datasets, 30K+ verifiable tasks | ✅ Confirmed, no arXiv ID |
| Cua (trycua/cua) | [GitHub](https://github.com/trycua/cua) | Open infrastructure: sandboxes, SDK and benchmarks for macOS/Linux/Windows desktop control; ships Cua-Bench | ✅ Confirmed, GitHub project |
| Cua Agent framework 0.4 | [Cua blog](https://cua.ai) | Unified multi-model interface with Composite Agents (grounding + planning) | ✅ Confirmed, official blog 2025.08 |
| OpenCUA | [arXiv:2508.09123](https://arxiv.org/abs/2508.09123) | Open framework with annotation infrastructure, AgentNet dataset (3 OS, 200+ apps) and CoT pipeline; OpenCUA-72B reaches 45.0% on OSWorld-Verified | ✅ Confirmed, **NeurIPS 2025** |
| CUA-Sandbox | [arXiv:2609.32750](https://arxiv.org/abs/2609.32750) | State capsule + shared runtime separation: 6.20× rollout throughput, 9.2× memory reduction, 504× storage reduction | ✅ Confirmed, arXiv 2026.09 |
| OSWorld | [arXiv:2404.07972](https://arxiv.org/abs/2404.07972) | 369 real desktop tasks across Web/desktop apps, file I/O and cross-app workflows on Ubuntu/Windows/macOS | ✅ Confirmed, arXiv 2024.04 |
| OSWorld 2.0 | [arXiv:2606.29537](https://arxiv.org/abs/2606.29537) | Pushes CUA evaluation to professional real-world workflows; binary success rate only 20.6% | ✅ Confirmed, arXiv 2026.06 |
| OSWorld-Human | [arXiv:2506.16042](https://arxiv.org/abs/2506.16042) | Human-annotated efficiency benchmark; leading agents use 1.4–2.7× the necessary steps | ✅ Confirmed, arXiv 2025.06 |
| WebArena | [arXiv:2307.13854](https://arxiv.org/abs/2307.13854) | Four self-hosted sites (e-commerce, forum, software dev, CMS) plus map tools; 812 long-horizon web tasks | ✅ Confirmed, arXiv 2023.07 |
| CUARewardBench | [arXiv:2510.18596](https://arxiv.org/abs/2510.18596) | First CUA reward-model benchmark covering 10 software categories and 7 agent architectures; UPE reaches 89.8% precision and 93.3% NPV | ✅ Confirmed, **ICML 2026** |
| Computer Agent Arena | [ICLR 2026 paper](https://proceedings.iclr.cc/paper_files/paper/2026/hash/5f1d328711b162e1cf9896c7d6aaecdd-Abstract-Conference.html) | Human-preference head-to-head evaluation platform, 2,201 votes over 12 agents, revealing rank inversions against static benchmarks | ✅ Confirmed, **ICLR 2026** |
| MCPWorld | [arXiv:2506.07672](https://arxiv.org/abs/2506.07672) | First testbed supporting API, GUI and hybrid paradigms; 201 tasks, 75.12% completion accuracy | ✅ Confirmed, arXiv 2025.06 |
| UI-CUBE | [arXiv:2511.17131](https://arxiv.org/abs/2511.17131) | UiPath enterprise-oriented deterministic benchmark; 226 tasks (136 simple + 90 complex) exposing fundamental CUA architectural limits | ✅ Confirmed, arXiv 2025.11 |
| Agent S | [arXiv:2410.08164](https://arxiv.org/abs/2410.08164) | Open agentic framework using computers like a human; Agent S2 reaches 18.9%/32.7% on OSWorld 15-step/50-step | ✅ Confirmed, **ICLR 2025** |
| Agent S3 | [arXiv:2510.02250](https://arxiv.org/abs/2510.02250) | Scaling version of the Agent S family, approaching human level with GPT-5 | ✅ Confirmed, **TMLR 2026** |
| OpenAgentFleet | [PyPI](https://pypi.org/project/open-agent-fleet/) | Self-hosted autonomous CUA platform; each agent gets a disposable Linux desktop streamed live to the browser | ✅ Confirmed, no arXiv paper |
| open-computer-use (QwenLM) | [GitHub](https://github.com/QwenLM/open-computer-use) | MCP-based computer-use service controlling macOS/Linux/Windows via accessibility APIs | ✅ Confirmed, GitHub project |
| open-computer-use (e2b-dev) | [GitHub](https://github.com/e2b-dev/open-computer-use) | Secure cloud Linux computer on E2B Desktop Sandbox, driven by open-source LLMs | ✅ Confirmed, GitHub project |
| OmniPilot | [PyPI](https://pypi.org/project/omnipilot-agent/) | Cross-platform open-source CUA with 13 model providers, 41 built-in tools and a four-level permission system | ✅ Confirmed, PyPI release |
| Tarsier-AI | [PyPI](https://pypi.org/project/tarsier-ai/) | Deterministic interaction layer for Windows desktop apps with a built-in MCP server, avoiding brittle pixel-coordinate clicking | ✅ Confirmed, no arXiv paper |
| **WildAWM** | [arXiv:2610.26828](https://arxiv.org/abs/2610.26828) | Microsoft Research + UNC + Gatech + Northeastern; synthesizes whole personal computers where GUI, MCP and CLI share one state; XAI cross-interface tasks average 4.2 sub-tasks / 3.1 interface switches, 74.5% revisit an earlier interface, some exceed 100 steps; five gates (verdict agreement, initially-incomplete, solvable, difficulty, counterfactual probe) cut 2,551 drafts to 341 tasks; synthesis-stage average success only 21.3%, GPT-6 Astra Pass@1 60% with 27.3% of tasks unsolved at Pass@8; verifier-agent-judge agreement 95% with Cohen's κ=0.90; fully open-source pipeline, gains on 8 OOD benchmarks (Qwen3.6-35B-A3B average 42.84→53.42) | ✅ New, confirmed, arXiv 2026.10 |
| **CUA-Universe** | [arXiv:2609.05374](https://arxiv.org/abs/2609.05374) | Scalable, dynamic environment for hybrid GUI + CLI agents coordinating over shared application state | ✅ New, confirmed, arXiv 2026.09 |
| **OSExpert** | [arXiv:2603.07978](https://arxiv.org/abs/2603.07978) | Introduces the OSExpert-Eval benchmark and a GUI depth-first-search exploration algorithm for learning professional skills | ✅ New, confirmed, arXiv 2026.03 |
| **GroundCUA** | [arXiv:2511.07332](https://arxiv.org/abs/2511.07332) | Desktop grounding dataset from expert human demonstrations: 87 applications, 12 categories, 56K screenshots; **ICLR 2026** | ✅ New, confirmed, arXiv 2025.11 |
| **WebHarbor** | [arXiv:2611.03634](https://arxiv.org/abs/2611.03634) | 153 executable dockerized website environments faithfully reconstructing visual interfaces, content and functional flows | ✅ New, confirmed, arXiv 2026.11 |
| **Ego2Web** | [arXiv:2603.22529](https://arxiv.org/abs/2603.22529) | Web agent benchmark grounded in egocentric videos | ✅ New, confirmed, **CVPR 2026** |
| **OSWorld-MCP** | [arXiv:2510.24563](https://arxiv.org/abs/2510.24563) | First comprehensive and fair benchmark for computer-use agent tool invocation | ✅ New, confirmed, arXiv 2025.10 |
| **GUI-CC** | [arXiv:2609.00048](https://arxiv.org/abs/2609.00048) | Benchmarks contextual consistency of GUI world models as agent environments | ✅ New, confirmed, **EMNLP 2026 Findings** |
| **MacArena** | [arXiv:2606.06560](https://arxiv.org/abs/2606.06560) | Benchmarking computer use agents on an online macOS environment | ✅ New, confirmed, arXiv 2026.06 |
| **MacAgentBench** | [arXiv:2606.22557](https://arxiv.org/abs/2606.22557) | Benchmarking AI agents on real-world macOS desktops | ✅ New, confirmed, arXiv 2026.06 |
| **macOSWorld** | [arXiv:2506.04135](https://arxiv.org/abs/2506.04135) | A multilingual interactive benchmark for GUI agents | ✅ New, confirmed, arXiv 2025.06 |
| **Windows Agent Arena** | [arXiv:2409.08264](https://arxiv.org/abs/2409.08264) | Evaluating multi-modal OS agents at scale | ✅ New, confirmed, arXiv 2024.09 |
| **OSUniverse** | [arXiv:2505.03570](https://arxiv.org/abs/2505.03570) | Benchmark for multimodal GUI-navigation agents with automatic validation | ✅ New, confirmed, arXiv 2025.05 |
| **MMBench-GUI** | [arXiv:2507.19478](https://arxiv.org/abs/2507.19478) | Hierarchical multi-platform evaluation framework for GUI agents | ✅ New, confirmed, arXiv 2025.07 |
| **On the Reliability of Computer Use Agents** | [arXiv:2604.17849](https://arxiv.org/abs/2604.17849) | Systematically characterizes the reliability envelope of CUAs | ✅ New, confirmed, arXiv 2026.04 |
| **OS-Harm** | [arXiv:2506.14866](https://arxiv.org/abs/2506.14866) | Safety benchmark for computer-use agents | ✅ New, confirmed, **NeurIPS 2025 D&B Spotlight** |
| **Trial by Trace** | [arXiv:2610.32285](https://arxiv.org/abs/2610.32285) | Benchmarks AI agent harnesses for reliability and failure attribution | ✅ New, confirmed, arXiv 2026.10 |
| **Benchmarking and Improving GUI Agents in High-Dynamic Environments** | [arXiv:2604.25380](https://arxiv.org/abs/2604.25380) | Benchmark and improvement for GUI agents in fast-changing interfaces | ✅ New, confirmed, arXiv 2026.04 |
| **MobileWorld** | [arXiv:2512.19432](https://arxiv.org/abs/2512.19432) | Agent-user interactive and MCP-augmented mobile agent benchmark | ✅ New, confirmed, arXiv 2025.12 |
| **ViMo** | [arXiv:2504.13936](https://arxiv.org/abs/2504.13936) | A generative visual GUI world model | ✅ New, confirmed, arXiv 2025.04 |
| **Code2World** | [arXiv:2602.09856](https://arxiv.org/abs/2602.09856) | A GUI world model via renderable code generation | ✅ New, confirmed, **CVPR 2026** |
| **UI-Simulator** | [arXiv:2510.14969](https://arxiv.org/abs/2510.14969) | Scales UI state, transition and trajectory synthesis | ✅ New, confirmed, arXiv 2025.10 |
| **Recovering Policy-Induced Errors** | [arXiv:2605.29447](https://arxiv.org/abs/2605.29447) | GUI-RobustEval with 1,216 cases plus RoTS synthesis of 800K trajectories | ✅ New, confirmed, **ICML 2026 Spotlight** |
| **SEE** | [arXiv:2607.18046](https://arxiv.org/abs/2607.18046) | Long-horizon GUI trajectory synthesis | ✅ New, confirmed, **ACM MM 2026 Oral** |
| **GSAR** | [arXiv:2608.22847](https://arxiv.org/abs/2608.22847) | Goal-state-anchor rewards with self-evolving data synthesis | ✅ New, confirmed, **EMNLP 2026 Main** |
| **OSGym** | [arXiv:2511.11672](https://arxiv.org/abs/2511.11672) | CUA training infrastructure with 1024 parallel sandboxes | ✅ Confirmed, arXiv 2025 |
| **CUA-Lite** | [arXiv:2610.26071](https://arxiv.org/abs/2610.26071) | Open CUA platform with three unified abstractions (environment interface across 12 desktop/browser/mobile benchmarks plus VM-free sandboxes, sampling, model harness), sharing one infrastructure for eval, RL and SFT. | ✅ New, confirmed |
| **CUA-Master** | [arXiv:2611.03126](https://arxiv.org/abs/2611.03126) | Nested double-loop recursive improvement: an outer world-data loop plus an inner policy loop, replacing self-generated experience with externally verifiable signals. | ✅ New, confirmed |
| **Covering Human Action Space** | [arXiv:2605.12501](https://arxiv.org/abs/2605.12501) | Finds CUA failures follow a long-tail pattern where few complex interactions dominate errors, and synthesizes targeted data plus a benchmark for that long tail. | ✅ New, confirmed |
| **EvoCUA** | [arXiv:2601.15876](https://arxiv.org/abs/2601.15876) | Native CUA that couples data generation with policy optimization in one loop instead of passive imitation of static datasets. | ✅ New, confirmed |
| **EvoCUA-1.5** | [arXiv:2607.09773](https://arxiv.org/abs/2607.09773) | Moves self-evolving CUAs to online RL in partially observable multimodal desktops, where each action changes screen state, action space and recovery options. | ✅ New, confirmed |
| **Player-1** | [arXiv:2610.20584](https://arxiv.org/abs/2610.20584) | Learns game play from synthetic experience, since games provide interaction data poorly covered by ordinary CUA datasets. | ✅ New, confirmed |

---

## 13. Data Synthesis (Trajectories / Tool-Use / Reasoning Data)

> Beyond environment synthesis, this section covers **data synthesis** proper: producing trainable, verifiable trajectories, tool-call sequences and reasoning data from environments, tools, corpora and real workflows, plus mechanisms for controlling quality, difficulty and coverage.

| Paper / Framework | Key Contribution | Date / Venue | Link | Status |
|---|---|---|---|---|
| **What Makes Good Agentic Data? (ACE Lens)** | Two-level framework for agentic data generation: consistency across environment, task, interaction and success signal, with candidate construction separated from verification and selection. | 2026-08 | [arXiv:2608.27260](https://arxiv.org/abs/2608.27260) | ✅ New, confirmed |
| **Trajectory2Gym** | Successful trajectories are not automatically useful supervision; requires compositional coverage and decision grounding (each action justified by learner-visible history) before turning trajectories into gyms. | 2026-10 | [arXiv:2610.33568](https://arxiv.org/abs/2610.33568) | ✅ New, confirmed |
| **COVERT (Controllable and Verifiable Tool-Use Data Synthesis)** | Two-stage pipeline: self-evolving synthesis with multi-level validation, then oracle-preserving augmentation (distractor tools, ambiguous queries, noise) to raise environment complexity for RL. | 2026-04 | [arXiv:2604.09813](https://arxiv.org/abs/2604.09813) | ✅ New, confirmed |
| **Davinci-Tool** | 30B tool-use model plus execution-grounded dataset that scales environment coverage and outcome verification together; new environments require rewriting success criteria too. | 2026-10 | [arXiv:2610.16867](https://arxiv.org/abs/2610.16867) | ✅ New, confirmed |
| **GRADS** | Graph-regulated agentic data synthesis that couples multi-hop evidence to the answer so apparent depth maps to real reasoning difficulty, with controllable difficulty. | 2026-10 | [arXiv:2610.21167](https://arxiv.org/abs/2610.21167) | ✅ New, confirmed |
| **Scaling Agentic Data for Long-Horizon Terminal Intelligence** | Argues short trajectories only show commands, while long-horizon trajectories capture evidence accumulation, judgement, feedback-driven adaptation and deliverable production. | 2026-10 | [arXiv:2610.13166](https://arxiv.org/abs/2610.13166) | ✅ New, confirmed |
| **SAP** | State-guided synthesis with tool-argument provenance, preventing fabricated or stale arguments even when the right tool is chosen. | 2026-09 | [arXiv:2609.06124](https://arxiv.org/abs/2609.06124) | ✅ New, confirmed |
| **EvoSyn** | Evolutionary data synthesis for verifiable learning, tackling hallucination-prone generation and weak verification artifacts that fail to separate strong from weak solutions. | 2025-10 | [arXiv:2510.17928](https://arxiv.org/abs/2510.17928) | ✅ New, confirmed |
| **SKT** | Verified synthetic data pipeline for skill use: selects single/multi-skill configurations and builds executable trajectories validated by rules and agents. | 2026-08 | [arXiv:2608.02287](https://arxiv.org/abs/2608.02287) | ✅ New, confirmed |
| **WebShaper** | Formalizes information-seeking structure before generating QA, fixing the mismatch between information structure and reasoning structure in web-agent data synthesis. | 2025-07 | [arXiv:2507.15061](https://arxiv.org/abs/2507.15061) | ✅ New, confirmed |
| **TDScaling (Beyond Quantity: Trajectory Diversity Scaling)** | Scales code-agent training by trajectory diversity rather than raw volume, breaking the early bottleneck of quantity-only scaling under a fixed budget. | 2026-02 | [arXiv:2602.03219](https://arxiv.org/abs/2602.03219) | ✅ New, confirmed |
| **GEM (Tool-Use Trajectories from Text)** | Synthesizes multi-turn tool-use trajectories from textual corpora, which already contain rich multi-step problem-solving experience. | 2026-01 | [arXiv:2601.10355](https://arxiv.org/abs/2601.10355) | ✅ New, confirmed |
| **Trajectory2Task** | Verifiable data pipeline targeting ambiguous, time-evolving and policy-infeasible user requests that real tool-calling agents must handle. | 2026-01 | [arXiv:2601.20144](https://arxiv.org/abs/2601.20144) | ✅ New, confirmed |
| **JudgeMix** | Judge-guided mixed-rollout synthesis that grounds training data in the target model's own state distribution, mitigating SFT's train-inference mismatch. | 2026-11 | [arXiv:2611.16174](https://arxiv.org/abs/2611.16174) | ✅ New, confirmed |
| **Know What You Don't Know** | Evolves the generation space so observed weaknesses translate into concrete changes to future synthesis, closing the feedback-to-decision gap. | 2026-10 | [arXiv:2610.12593](https://arxiv.org/abs/2610.12593) | ✅ New, confirmed |
| **Agent-R$^2$** | Real-source data synthesis for productivity work, built around real work intent, authentic file environments and deliverable-level verification. | 2026-11 | [arXiv:2611.08219](https://arxiv.org/abs/2611.08219) | ✅ New, confirmed |
| **RODS** | Reward-driven online synthesis that targets the shifting capability boundary using GRPO reward variance, preventing informative-sample depletion in static pools. | 2026-06 | [arXiv:2606.19047](https://arxiv.org/abs/2606.19047) | ✅ New, confirmed |
| **Constrained Data Synthesis + Graduated Rewards** | Builds a deterministic environment from a large cache of real API responses for constrained multi-step tool-orchestration synthesis, with graduated rewards for partial correctness. | 2026-03 | [arXiv:2603.24709](https://arxiv.org/abs/2603.24709) | ✅ New, confirmed |
| **ToolMind** | Large-scale, reasoning-enhanced tool-use dataset. | 2025-11 | [arXiv:2511.15718](https://arxiv.org/abs/2511.15718) | ✅ New, confirmed |
| **OpenVisTool** | Open recipe for synthesizing instructive visual tool-use trajectories, teaching multimodal agents to call visual tools for evidence beyond a fixed image encoding. | 2026-08 | [arXiv:2608.08557](https://arxiv.org/abs/2608.08557) | ✅ New, confirmed |
| **ToolACE-MT** | Non-autoregressive generation of agentic multi-turn interactions, producing whole interaction sequences rather than token-by-token. | 2025-08 | [arXiv:2508.12685](https://arxiv.org/abs/2508.12685) | ✅ New, confirmed |
| **AutoDataBench** | Asks whether agents can write the verifiable agentic data that feeds self-improvement, making data production itself the capability under test. | 2026-09 | [arXiv:2609.35025](https://arxiv.org/abs/2609.35025) | ✅ New, confirmed |
| **Self-Instruct** | Bootstraps instruction data from 175 human seeds into ~52K self-generated instruction-input-output triples, improving Super-NI by 33.3% over a GPT-3 baseline. | 2022-12 | [arXiv:2212.10560](https://arxiv.org/abs/2212.10560) | ✅ New, confirmed |
| **WizardLM / Evol-Instruct** | Evol-Instruct iteratively rewrites instructions along depth (constraints, deepening) and breadth (new topics) axes to synthesize 250K complex instructions. | 2023-04 | [arXiv:2304.12244](https://arxiv.org/abs/2304.12244) | ✅ New, confirmed |
| **AgentInstruct / Agentic Flow** | Generative teaching via agentic flows that convert raw corpora (code, web, text) into instruction-response data reusable across six task types. | 2024-07 | [arXiv:2407.03502](https://arxiv.org/abs/2407.03502) | ✅ New, confirmed |
| **ToolLLM / ToolBench** | Scales tool-use data to 16,464 real REST APIs across 49 categories with automatically constructed instructions, DFSDT search and the ToolEval metric. | 2023-07 | [arXiv:2307.16789](https://arxiv.org/abs/2307.16789) | ✅ New, confirmed |
| **APIGen** | Three-stage verifiable pipeline (format, real execution, semantic check) producing a 60K function-calling dataset; xLAM-7B reaches 88% on Berkeley Function-Calling. | 2024-06 | [arXiv:2406.18518](https://arxiv.org/abs/2406.18518) | ✅ New, confirmed |
| **ToolACE** | Dual-layer (rule + model) verification with self-evolution over 26,507 APIs, filtering hallucinations and inconsistencies in tool-call data. | 2024-09 | [arXiv:2409.00920](https://arxiv.org/abs/2409.00920) | ✅ New, confirmed |
| **Magicoder / OSS-Instruct** | OSS-Instruct seeds from open-source snippets to elicit diverse, realistic coding problems (75K data), letting small models surpass larger baselines. | 2023-12 | [arXiv:2312.02120](https://arxiv.org/abs/2312.02120) | ✅ New, confirmed |
| **AgentOhana** | Unified data schema and training pipeline standardizing heterogeneous agent trajectories from different environments for mixed training. | 2024-02 | [arXiv:2402.15506](https://arxiv.org/abs/2402.15506) | ✅ New, confirmed |
| **ToolAlpaca** | Synthesizes 3,000 tool-use instances over 400 tools, showing small models generalize tool use without real API interaction. | 2023-06 | [arXiv:2306.05301](https://arxiv.org/abs/2306.05301) | ✅ New, confirmed |
| **TaskCraft** | Automated generation of agentic tasks with depth and breadth expansion plus executable validation, yielding scalable, difficulty-controllable task sets. | 2025-06 | [arXiv:2506.10055](https://arxiv.org/abs/2506.10055) | ✅ New, confirmed |
| **Crafter** | 2D open-world survival benchmark with procedurally generated worlds and 22 achievements, a standard testbed for long-horizon exploration and generalization. | 2021-11 | [GitHub: danijar/crafter](https://github.com/danijar/crafter) | ✅ New, confirmed |
| **MineDojo** | Open-ended embodied suite built on internet-scale knowledge: 3,000+ tasks, 7,000+ videos and wiki pages, with MineCLIP rewards. | 2022-06 | [arXiv:2206.08853](https://arxiv.org/abs/2206.08853) | ✅ New, confirmed |
| **Voyager** | Lifelong LLM agent in Minecraft combining an automatic curriculum, an executable skill library and iterative prompting without gradient updates. | 2023-05 | [arXiv:2305.16291](https://arxiv.org/abs/2305.16291) | ✅ New, confirmed |
| **JARVIS-1** | Memory-augmented multimodal LLM agent for open-world multi-task learning in Minecraft. | 2023-11 | [arXiv:2311.05997](https://arxiv.org/abs/2311.05997) | ✅ New, confirmed |
| **GITM (Ghost in the Minecraft)** | Decomposes long-horizon open-world goals into executable skills using LLM knowledge plus a skill library, without human demonstrations. | 2023-05 | [arXiv:2305.17144](https://arxiv.org/abs/2305.17144) | ✅ New, confirmed |
| **ScienceWorld** | Interactive text-based science experimentation environment with 30 task types requiring multi-step laboratory actions. | 2022-03 | [arXiv:2203.07540](https://arxiv.org/abs/2203.07540) | ✅ New, confirmed |
| **ProcTHOR** | Procedurally generates 10,000+ interactive 3D rooms, showing scaling and generalization benefits over hand-authored scenes. | 2022-06 | [arXiv:2206.06994](https://arxiv.org/abs/2206.06994) | ✅ New, confirmed |
| **Habitat 3.0** | Co-habitat simulator for humans, avatars and robots enabling heterogeneous multi-agent collaboration and social navigation. | 2023-10 | [arXiv:2310.13724](https://arxiv.org/abs/2310.13724) | ✅ New, confirmed |
| **SayCan** | Grounds LLM plans in robot affordances: the LLM proposes skills and a value function scores feasibility. | 2022-04 | [arXiv:2204.01691](https://arxiv.org/abs/2204.01691) | ✅ New, confirmed |
| **BEHAVIOR-1K** | Human-centered embodied benchmark with 1,000 everyday activities across 50 scenes. | 2024-03 | [arXiv:2403.09227](https://arxiv.org/abs/2403.09227) | ✅ New, confirmed |
| **Generative Agents** | Smallville social simulation where 25 memory-stream agents live, socialize and coordinate, founding generative social simulation. | 2023-04 | [arXiv:2304.03442](https://arxiv.org/abs/2304.03442) | ✅ New, confirmed |
| **CAMEL** | Role-playing multi-agent collaboration generating cooperative dialogues, used for agent-society study and synthetic conversation data. | 2023-03 | [arXiv:2303.17760](https://arxiv.org/abs/2303.17760) | ✅ New, confirmed |
| **AgentVerse** | Multi-agent collaboration framework with dynamic recruitment, joint decision-making and emergent behaviour analysis. | 2023-08 | [arXiv:2308.10848](https://arxiv.org/abs/2308.10848) | ✅ New, confirmed |
| **MetaGPT** | Encodes standard operating procedures into a multi-agent software company, testing SOPs as multi-agent environment constraints. | 2023-08 | [arXiv:2308.00352](https://arxiv.org/abs/2308.00352) | ✅ New, confirmed |
| **Unnatural Instructions** | Rewrites human instructions with an LLM to synthesize 64K instruction data, showing synthetic instructions can substitute human annotation. | 2022-12 | [arXiv:2212.09689](https://arxiv.org/abs/2212.09689) | ✅ New, confirmed |
| **Toolformer** | Self-supervised API-use learning: the model annotates its own API calls, which are filtered by usefulness and used for training. | 2023-02 | [arXiv:2302.04761](https://arxiv.org/abs/2302.04761) | ✅ New, confirmed |
| **WebGPT** | Browser-assisted QA with human feedback, producing action-sequence demonstrations on the live web (Dec 2021). | 2021-12 | [arXiv:2112.09332](https://arxiv.org/abs/2112.09332) | ✅ New, confirmed |
| **Orca** | Progressive learning from GPT-4 explanation traces, studying how explanation data scale and quality transfer to smaller models. | 2023-06 | [arXiv:2306.02707](https://arxiv.org/abs/2306.02707) | ✅ New, confirmed |
| **AgentTuning** | AgentInstruct synthetic interaction data plus mixed-task tuning improves agent ability without hurting general capability. | 2023-10 | [arXiv:2310.12823](https://arxiv.org/abs/2310.12823) | ✅ New, confirmed |
| **MINT** | Benchmarks multi-turn tool use with language feedback as a core capability dimension. | 2023-09 | [arXiv:2309.10691](https://arxiv.org/abs/2309.10691) | ✅ New, confirmed |
| **API-Bank** | Comprehensive tool-augmented benchmark with 73 APIs and 314 dialogues covering calling, retrieval and multi-turn planning. | 2023-04 | [arXiv:2304.08244](https://arxiv.org/abs/2304.08244) | ✅ New, confirmed |
| **TaskBench** | Task-automation benchmark requiring task decomposition and tool-call dependency graphs. | 2023-11 | [arXiv:2311.18760](https://arxiv.org/abs/2311.18760) | ✅ New, confirmed |
| **Gorilla** | Massive API-calling ability with 1,645 APIs and retriever-aware training that reduces API hallucination. | 2023-05 | [arXiv:2305.15334](https://arxiv.org/abs/2305.15334) | ✅ New, confirmed |

---

## 14. Embodied / Robotic Environment Synthesis

> Scaling embodied interaction data through simulation, scene generation and executable reconstruction for VLA / robot foundation models, balancing semantic coherence, physical feasibility and verifiability.

| Paper / Framework | Key Contribution | Date / Venue | Link | Status |
|---|---|---|---|---|
| **Nimbus** | Unified embodied synthetic data framework consolidating fragmented task-specific pipelines into one high-throughput, stable generation system. | 2026-01 | [arXiv:2601.21449](https://arxiv.org/abs/2601.21449) | ✅ New, confirmed |
| **SkillWeaver** | Agentic exploration over neural interaction skills replaces open-loop controllers and scripted skill sequences, scaling robot data generation. | 2026-09 | [arXiv:2609.36171](https://arxiv.org/abs/2609.36171) | ✅ New, confirmed |
| **EmbodiedSmith** | Recursive self-improvement flywheel in simulation that co-scales assets, skills, scene and task generation, supporting complex embodiments and physics. | 2026-10 | [arXiv:2610.07969](https://arxiv.org/abs/2610.07969) | ✅ New, confirmed |
| **V-CAGE** | Vision-closed-loop agentic generation engine producing semantically coherent, physically feasible manipulation scenes for VLA training. | 2026-04 | [arXiv:2604.09036](https://arxiv.org/abs/2604.09036) | ✅ New, confirmed |
| **SceneBloom** | Agentic indoor scene generation combining language-guided planning with visual priors and geometric reasoning to yield simulation-ready layouts. | 2026-10 | [arXiv:2610.32978](https://arxiv.org/abs/2610.32978) | ✅ New, confirmed |
| **OWMM-Agent** | Multi-modal agentic data synthesis for open-world mobile manipulation, generalizing to open-ended instructions and environments. | 2025-06 | [arXiv:2506.04217](https://arxiv.org/abs/2506.04217) | ✅ New, confirmed |
| **GRUtopia** | First simulated interactive 3D society for diverse robots, with the GRScenes dataset, tasks and evaluation, targeting Sim2Real scaling. | 2024-07 | [arXiv:2407.10943](https://arxiv.org/abs/2407.10943) | ✅ New, confirmed |
| **PARTNR** | Human-robot collaboration benchmark with semi-automated LLM task generation and simulation-in-the-loop grounding, encoding spatial, temporal and capability constraints. | 2024-10 | [arXiv:2411.00081](https://arxiv.org/abs/2411.00081) | ✅ New, confirmed |
| **ABot-ER** | Unified embodied reasoning model built through agentic data-model co-evolution, balancing breadth and depth across perception, planning and execution. | 2026-10 | [arXiv:2610.18355](https://arxiv.org/abs/2610.18355) | ✅ New, confirmed |
| **SimWorld (Open-ended Simulator)** | Open-ended realistic simulator for autonomous agents in physical and social worlds. | 2025-11 | [arXiv:2512.01078](https://arxiv.org/abs/2512.01078) | ✅ New, confirmed |
| **SubTGraph** | Large-scale subterranean environment synthesis with controllable topological variability for robotic autonomy validation. | 2026-05 | [arXiv:2605.20917](https://arxiv.org/abs/2605.20917) | ✅ New, confirmed |
| **Synthetic Household Data at Scale** | Realistic synthetic household data generation at scale for embodied environmental reasoning and interaction. | 2026-02 | [arXiv:2602.07243](https://arxiv.org/abs/2602.07243) | ✅ New, confirmed |
| **Code as Policies** | 把语言模型生成的代码作为机器人控制策略：在感知 API 之上直接产出可执行策略代码，处理几何与数值约束 | 2022-09 | [arXiv:2209.07753](https://arxiv.org/abs/2209.07753) | ✅ New, confirmed |

---

## 15. Multi-Agent / Social Simulation Environments

> Multi-agent environments serve both as training grounds and testbeds, where tasks are shaped by social structure, interdependence and mixed motives, and where environments must support long-term evolution and state tracking.

| Paper / Framework | Key Contribution | Date / Venue | Link | Status |
|---|---|---|---|---|
| **AgentSociety** | Multi-agent environment where agents act autonomously, communicate strategically and improve from feedback channels over time. | 2026-05 | [arXiv:2605.26203](https://arxiv.org/abs/2605.26203) | ✅ New, confirmed |
| **AdaSociety** | Adaptive multi-agent environment with social structures where tasks, rewards and information access depend on social connections and agent actions. | 2024-11 | [arXiv:2411.03865](https://arxiv.org/abs/2411.03865) | ✅ New, confirmed |
| **MAC-Bench** | Benchmarks multi-agent collaboration with interconnected tasks, measuring ability to handle interdependent work rather than difficulty alone. | 2026-11 | [arXiv:2611.01728](https://arxiv.org/abs/2611.01728) | ✅ New, confirmed |
| **MEMTRACK** | Benchmark for long-term memory and state tracking across multi-platform dynamic enterprise environments. | 2025-10 | [arXiv:2510.01353](https://arxiv.org/abs/2510.01353) | ✅ New, confirmed |
| **Coopetition-Gym** | Formally grounded platform with 20 mixed-motive coopetition environments across four mechanism classes. | 2026-05 | [arXiv:2605.02063](https://arxiv.org/abs/2605.02063) | ✅ New, confirmed |
| **MAESTRO** | Open-ended environment design for MARL that adapts both environment parameters and co-player policies jointly. | 2023-03 | [arXiv:2303.03376](https://arxiv.org/abs/2303.03376) | ✅ New, confirmed |
| **UDE (Unified Distributed Environment)** | Environment virtualization toolkit unifying Gazebo/Unity/Unreal/Gym environments with remote offloading behind one interface. | 2022-05 | [arXiv:2205.06946](https://arxiv.org/abs/2205.06946) | ✅ New, confirmed |
| **ChatDev** | 多 Agent 软件公司仿真：CEO/CTO/程序员/测试等角色分工，用对话驱动「设计-编码-测试」全流程 | 2023-07 | [arXiv:2307.07924](https://arxiv.org/abs/2307.07924) | ✅ New, confirmed |
| **AutoGen** | 可对话的多 Agent 框架：把多 Agent 协作抽象为「可定制、可对话的 agent」，支持人机混合与工具调用编排 | 2023-08 | [arXiv:2308.08155](https://arxiv.org/abs/2308.08155) | ✅ New, confirmed |

---

## 16. Open-Source Projects (GitHub)

> Open-source entry points for environment synthesis, data synthesis, agentic RL and sandbox infrastructure; star counts are approximate at crawl time.

| Project | Summary | Date | Link | Note |
|---|---|---|---|---|
| **AgentENV (AENV)** | Distributed platform for running agent environments at scale. | 2026-07 | [kvcache-ai/AgentENV](https://github.com/kvcache-ai/AgentENV) | ✅ New, confirmed |
| **Agent-World** | Official code for real-world environment synthesis scaling general agent intelligence. | 2026-08 | [RUC-NLPIR/Agent-World](https://github.com/RUC-NLPIR/Agent-World) | ✅ New, confirmed |
| **EnvFactory** | Official code for scaling tool-use agents via executable environment synthesis and robust RL. | 2026-02 | [LARK-AI-Lab/EnvFactory](https://github.com/LARK-AI-Lab/EnvFactory) | ✅ New, confirmed |
| **ASTRA (code)** | End-to-end system synthesizing agentic trajectories and rule-verifiable environments for SFT and RL. | 2026-01 | [LianjiaTech/astra](https://github.com/LianjiaTech/astra) | ✅ New, confirmed |
| **CUA-Gym-Hub** | Hub of mock web apps as reproducible RL training environments for computer-use agents. | 2025-12 | [xlang-ai/CUA-Gym-Hub](https://github.com/xlang-ai/CUA-Gym-Hub) | ✅ New, confirmed |
| **RecreationWorld (code)** | Code for scalable verifiable environments for hybrid computer-use agents. | 2026-09 | [QwenLM/RecreationWorld](https://github.com/QwenLM/RecreationWorld) | ✅ New, confirmed |
| **Echoverse (code)** | Deep, evolving environment framework for computer-use agents. | 2026-07 | [microsoft/Echoverse](https://github.com/microsoft/Echoverse) | ✅ New, confirmed |
| **WebHarbor** | Docks real websites as evolving GUI-agent environments. | 2026-05 | [aiming-lab/WebHarbor](https://github.com/aiming-lab/WebHarbor) | ✅ New, confirmed |
| **AgentSynth** | Scalable task generation for generalist computer-use agents (ICLR 2026). | 2025-05 | [sunblaze-ucb/AgentSynth](https://github.com/sunblaze-ucb/AgentSynth) | ✅ New, confirmed |
| **AgentTrek** | Agent trajectory synthesis via guiding replay with web tutorials. | 2025-02 | [xlang-ai/AgentTrek](https://github.com/xlang-ai/AgentTrek) | ✅ New, confirmed |
| **CLI-Gym** | Scalable CLI task generation via agentic environment inversion. | 2026-02 | [LiberCoders/CLI-Gym](https://github.com/LiberCoders/CLI-Gym) | ✅ New, confirmed |
| **Trajectory2Gym** | Decision-grounded compositional interaction synthesis for tool-use agents. | 2026-10 | [yihaohu0118/Trajectory2Gym](https://github.com/yihaohu0118/Trajectory2Gym) | ✅ New, confirmed |
| **ClawEnvKit** | Open-source environment toolkit supporting task/harness generation and evaluation. | 2026-03 | [xirui-li/ClawEnvKit](https://github.com/xirui-li/ClawEnvKit) | ✅ New, confirmed |
| **Seahaven** | Framework for building synthetic worlds for agent RL and evaluation. | 2026-09 | [Kiln-AI/Seahaven](https://github.com/Kiln-AI/Seahaven) | ✅ New, confirmed |
| **agentenv-framework** | Infrastructure for building realistic RL environments with researchers, engineers and domain experts. | 2026-09 | [scaleapi/agentenv-framework](https://github.com/scaleapi/agentenv-framework) | ✅ New, confirmed |
| **AgentArk** | General-purpose environment framework for scalable multimodal agent evaluation and RL. | 2025-08 | [P90-RushB/AgentArk](https://github.com/P90-RushB/AgentArk) | ✅ New, confirmed |
| **archipelago** | Harness for running and evaluating agents against RL environments. | 2026-01 | [Mercor-Intelligence/archipelago](https://github.com/Mercor-Intelligence/archipelago) | ✅ New, confirmed |
| **hud-python** | RL environments and evals for agents: define once, train anything. | 2025-03 | [hud-evals/hud-python](https://github.com/hud-evals/hud-python) | ✅ New, confirmed |
| **Dressage** | Scalable RL for any agent and sandbox. | 2026-06 | [Accio-Lab/Dressage](https://github.com/Accio-Lab/Dressage) | ✅ New, confirmed |
| **agentcore-rl-toolkit** | Composable RL toolkit for real-world agents on Bedrock AgentCore. | 2025-12 | [awslabs/agentcore-rl-toolkit](https://github.com/awslabs/agentcore-rl-toolkit) | ✅ New, confirmed |
| **SWE-MiniSandbox** | Container-free RL framework for training software-engineering agents. | 2025-12 | [lblankl/SWE-MiniSandbox](https://github.com/lblankl/SWE-MiniSandbox) | ✅ New, confirmed |
| **tbench-agentic-data-pipeline** | Multi-agent synthetic data pipeline generating and validating long-horizon terminal/coding trajectories. | 2025-07 | [Danau5tin/tbench-agentic-data-pipeline](https://github.com/Danau5tin/tbench-agentic-data-pipeline) | ✅ New, confirmed |
| **rl-env-use** | Builds RL environments for any domain from real cases mined from the web by Browser Use agents. | 2026-10 | [browser-use/rl-env-use](https://github.com/browser-use/rl-env-use) | ✅ New, confirmed |
| **Agentix** | Universal bridge between agents and environments for evaluation, RL training and tracing. | 2026-04 | [Agentix-Project/Agentix](https://github.com/Agentix-Project/Agentix) | ✅ New, confirmed |
| **shepherd** | Runtime substrate turning agent execution into a reversible Git-like trace for meta-agents. | 2026-06 | [shepherd-agents/shepherd](https://github.com/shepherd-agents/shepherd) | ✅ New, confirmed |
| **envd** | Reproducible development environments for humans and agents. | 2022-04 | [tensorchord/envd](https://github.com/tensorchord/envd) | ✅ New, confirmed |
| **celesto** | Sandboxes for coding agents, CI runners and RL training. | 2026-02 | [CelestoAI/celesto](https://github.com/CelestoAI/celesto) | ✅ New, confirmed |
| **MAI-Gym** | Open all-in-one platform for GUI-agent evaluation and RL across mobile and computer environments. | 2026-10 | [Tongyi-MAI/MAI-Gym](https://github.com/Tongyi-MAI/MAI-Gym) | ✅ New, confirmed |
| **SimEHR** | High-fidelity EHR environment for computer-use agents. | 2026-11 | [HealthRex/SimEHR](https://github.com/HealthRex/SimEHR) | ✅ New, confirmed |
| **mcpmark** | Comprehensive stress-testing MCP benchmark. | 2025-07 | [eval-sys/mcpmark](https://github.com/eval-sys/mcpmark) | ✅ New, confirmed |
| **mcp-bench** | Benchmarks tool-using agents with complex real-world tasks via MCP servers. | 2025-08 | [Accenture/mcp-bench](https://github.com/Accenture/mcp-bench) | ✅ New, confirmed |
| **LiveMCPBench** | Benchmark for navigating and using a large-scale MCP tool ecosystem. | 2025-08 | [icip-cas/LiveMCPBench](https://github.com/icip-cas/LiveMCPBench) | ✅ New, confirmed |
| **MCPToolBench++** | MCP-based tool-use benchmark for agents and models. | 2025-07 | [mcp-tool-bench/MCPToolBenchPP](https://github.com/mcp-tool-bench/MCPToolBenchPP) | ✅ New, confirmed |
| **Meta Agents Research Environments** | Platform for evaluating agents in dynamic, realistic environments. | 2025-09 | [facebookresearch/meta-agents-research-environments](https://github.com/facebookresearch/meta-agents-research-environments) | ✅ New, confirmed |
| **Qwen-AgentWorld** | Language world models for general agents. | 2026-06 | [QwenLM/Qwen-AgentWorld](https://github.com/QwenLM/Qwen-AgentWorld) | ✅ New, confirmed |
| **awesome-agentic-world-modeling** | Curated list on agentic world modeling: foundations, capabilities, laws. | 2026-04 | [matrix-agent/awesome-agentic-world-modeling](https://github.com/matrix-agent/awesome-agentic-world-modeling) | ✅ New, confirmed |
| **tarit** | Hypervisor and sandbox cloud for self-hosting agents and RL. | 2026-07 | [instavm/tarit](https://github.com/instavm/tarit) | ✅ New, confirmed |
| **RedTeamCUA** | Realistic adversarial testing of computer-use agents in hybrid web-OS environments. | 2025-05 | [OSU-NLP-Group/RedTeamCUA](https://github.com/OSU-NLP-Group/RedTeamCUA) | ✅ New, confirmed |
| **MemGUI-Bench** | Benchmarking memory of mobile GUI agents in dynamic environments. | 2026-02 | [lgy0404/MemGUI-Bench](https://github.com/lgy0404/MemGUI-Bench) | ✅ New, confirmed |
| **VAGEN** | World-model RL framework for multi-turn VLM agents. | 2025-03 | [mll-lab-nu/VAGEN](https://github.com/mll-lab-nu/VAGEN) | ✅ New, confirmed |
| **MedResearcher-R1** | Medical deep-research agent built on knowledge-informed trajectory synthesis. | 2025-08 | [AQ-MedAI/MedResearcher-R1](https://github.com/AQ-MedAI/MedResearcher-R1) | ✅ New, confirmed |
| **OS-Sentinel** | Safety-enhanced mobile GUI agents with hybrid verification. | 2025-07 | [OS-Copilot/OS-Sentinel](https://github.com/OS-Copilot/OS-Sentinel) | ✅ New, confirmed |
| **LLM-MM-Agent** | LLM agents for real-world mathematical modeling (NeurIPS 2025). | 2025-05 | [usail-hkust/LLM-MM-Agent](https://github.com/usail-hkust/LLM-MM-Agent) | ✅ New, confirmed |

---

## 17. Key Points from Representative Works

| Work | Method | Scale / Experimental Results |
|---|---|---|
| **Agent-World** (BAAI/TARS) | Tool dependency graphs + executable Python solution-based task synthesis with controllable difficulty; multi-environment closed-loop RL with GRPO; self-evolving arena | 1,978 environments / 20 categories / 19,822 tools; 8B/14B models surpass several closed-source models after training |
| **EnvScaler** (Renmin University) | SkelBuilder (environment skeleton: executable program + documentation + tool interface, evaluated by dual Agents) + ScenGenerator (scenario/task/terminal-state verification functions) | 191 environments / ~7K scenarios; after SFT, BFCL-MT +8.67 and ACEBench-Agent +11.57 |
| **InfiniteWeb** | Scalable Web environment synthesis, targeting in-domain generalization for GUI Agents | Synthesized websites transferred to real web pages for generalization testing |
| **Agent-World Model** | Agentic RL over infinitely synthesized environments | 1,000 executable SQLite + MCP environments; trained only on synthetic data yet generalizes to three OOD benchmarks; merged into meta-pytorch/OpenEnv |
| **ToolVerse** | Large-scale tool environments + long-horizon tasks | ~400 MCP servers / ~4,500 tools; environment diversity yields more benefit than increasing rollout count; significant gains on BFCL-v3 / τ²-Bench |
| **WildAWM** (MSR et al.) | Synthesize a personal-computer world (GUI + MCP + CLI) → author tasks and verifiers → five quality gates → RL training | 36 personas / 640 worlds / ~170K DB records per world; 341 accepted environment-task pairs; fully open-source pipeline, gains on 8 OOD benchmarks (35B-A3B average +10.58) |
| **SynthAPI** | Explicit control of environment diversity along tools, tasks and databases | 458,752 tasks across 84 environments, yielding an environment scaling law for tool-use agents |
| **CodeMidas** | Uses source code as the only task-specific signal to build RL environments | Escapes the issue/commit-artifact limitation of prior methods and widens the extractable task space |
| **POSEIDON** | Extracts verifiable training environments from scientific code repositories | Nearly 10× more environments than a prior approach at the same repository budget |
| **AgentDrive** | LLM prompt generates JSON driving scenarios | 300K driving scenarios; [arXiv:2601.16964](https://arxiv.org/abs/2601.16964) |
| **Agentick** | Procedurally generates 37 tasks with a Gymnasium interface + oracle policy + SFT data | General sequential decision-making evaluation; [arXiv:2605.06869](https://arxiv.org/abs/2605.06869) |
| **Survey: Scaling Environments for LLM Agents** | Proposes the GEF loop — task generation, execution, feedback — as a unified taxonomy | Environment-centric survey |
| **Survey: Agentic Environment Engineering** | Systematic lifecycle classification (modeling → synthesis → evaluation → application) separating symbolic and neural synthesis | [arXiv:2606.12191](https://arxiv.org/abs/2606.12191) |

---

## 18. Awesome Lists & Aggregated Resources

| Resource | Contents | Link |
|---|---|---|
| **awesome-scaling-coding-agent-envs** | Curated tools, papers and frameworks for scaling RL environments for coding agents; three pillars: automated environment setup, scalable instance synthesis, novel training paradigms | [GitHub](https://github.com/jc-ryan/awesome-scaling-coding-agent-envs) |
| **Awesome-Agent-Environments** | Agent environments organized by task, construction and execution layers; 96+ environments and framework repos | [GitHub](https://github.com/ZackZikaiXiao/Awesome-Agent-Environments) |
| **Awesome-Agentic-Environments** | Environment reproducibility, sandbox infrastructure, vendors and industry reports | [GitHub](https://github.com/TraceLite-AI/Awesome-Agentic-Environments) |
| **Awesome Workplace Agent Environments** | 20 environments, 15 generation and training resources, 9 datasets, 5 providers; bilingual with BibTeX | [GitHub](https://github.com/gumlau/awesome-workplace-agent-environments) |
| **AgentsMeetRL** | Open-source agentic RL projects with framework, algorithm, reward and environment details | [GitHub](https://github.com/thinkwee/AgentsMeetRL) |
| **Awesome-AgenticLLM-RL-Papers** | Companion reading list for an agentic RL survey, including environments and frameworks | [GitHub](https://github.com/HHHHHejia/Awesome-AgenticLLM-RL-Papers) |
| **Awesome-LLM-Synthetic-Data** | Reading list on LLM-generated synthetic data | [GitHub](https://github.com/wasiahmad/Awesome-LLM-Synthetic-Data) |
| **acu (trycua)** | Computer-use agent papers, projects and frameworks | [GitHub](https://github.com/trycua/acu) |
| **AI Agent Benchmark Compendium** | Agent benchmarks grouped by tools, general assistance, coding and other tasks | [GitHub](https://github.com/philschmid/ai-agent-benchmark-compendium) |
| **Benchmark Radar** | Living database of AI benchmarks (14,810+ records / 37 sources) with dashboard, CLI, RSS and dataset downloads | [GitHub](https://github.com/ktwu01/benchmark-radar) · [Dashboard](https://benchmark-radar.org/) |

---

## Appendix: Quick Reference to Environment & Benchmark Repositories

| Category | Repositories |
|---|---|
| Environment frameworks / infra | [meta-pytorch/OpenEnv](https://github.com/meta-pytorch/OpenEnv), [PrimeIntellect-ai/verifiers](https://github.com/PrimeIntellect-ai/verifiers), [laude-institute/harbor](https://github.com/laude-institute/harbor), [agent-infra/sandbox](https://github.com/agent-infra/sandbox), [kubernetes-sigs/agent-sandbox](https://github.com/kubernetes-sigs/agent-sandbox), [alibaba/OpenSandbox](https://github.com/alibaba/OpenSandbox), [e2b-dev/E2B](https://github.com/e2b-dev/E2B), [inclusionAI/AEnvironment](https://github.com/inclusionAI/AEnvironment) |
| Environment synthesis projects | [Snowflake-Labs/agent-world-model](https://github.com/Snowflake-Labs/agent-world-model), [RUC-NLPIR/EnvScaler](https://github.com/RUC-NLPIR/EnvScaler), [Gen-Verse/GenEnv](https://github.com/Gen-Verse/GenEnv), [ModalMinds/gym-v](https://github.com/ModalMinds/gym-v), [AMAP-ML/Code2World](https://github.com/AMAP-ML/Code2World), [MSR-Orchard/WildAWM](https://github.com/MSR-Orchard/WildAWM), [camel-ai/seta](https://github.com/camel-ai/seta), [emrecanacikgoz/Tool-R0](https://github.com/emrecanacikgoz/Tool-R0), [TheAgentArk/Toucan](https://github.com/TheAgentArk/Toucan), [huggingface/Repo2RLEnv](https://github.com/huggingface/Repo2RLEnv), [Wusiwei0410/TerminalTraj](https://github.com/Wusiwei0410/TerminalTraj) |
| Coding / SWE environments | [SWE-bench/SWE-smith](https://github.com/SWE-bench/SWE-smith), [SWE-Gym/SWE-Gym](https://github.com/SWE-Gym/SWE-Gym), [R2E-Gym/R2E-Gym](https://github.com/R2E-Gym/R2E-Gym), [RUCAIBox/SWE-World](https://github.com/RUCAIBox/SWE-World), [r2e-project/r2e](https://github.com/r2e-project/r2e), [DeepSoftwareAnalytics/swe-factory](https://github.com/DeepSoftwareAnalytics/swe-factory), [yiqingxyq/RepoST](https://github.com/yiqingxyq/RepoST), [bytedance/Repo2Run](https://github.com/bytedance/Repo2Run), [JetBrains-Research/EnvBench](https://github.com/JetBrains-Research/EnvBench), [EuniAI/HerAgent](https://github.com/EuniAI/HerAgent), [FSoft-AI4Code/SWE-Synth](https://github.com/FSoft-AI4Code/SWE-Synth), [Hambaobao/SWE-Flow](https://github.com/Hambaobao/SWE-Flow), [neulab/SWE-Playground](https://github.com/neulab/SWE-Playground), [microsoft/RepoLaunch](https://github.com/microsoft/RepoLaunch), [TencentYoutuResearch/EnConda-Bench](https://github.com/TencentYoutuResearch/EnConda-Bench) |
| Environment setup / sandboxing | [microsoft/debug-gym](https://github.com/microsoft/debug-gym), [OpenAutoCoder/live-swe-agent](https://github.com/OpenAutoCoder/live-swe-agent), [logic-star-ai/swt-bench](https://github.com/logic-star-ai/swt-bench), [IBM/TDD-Bench-Verified](https://github.com/IBM/TDD-Bench-Verified), [aisa-group/PostTrainBench](https://github.com/aisa-group/PostTrainBench), [OpenHands/critic-rubrics](https://github.com/OpenHands/critic-rubrics), [sola-st/ExecutionAgent](https://github.com/sola-st/ExecutionAgent), [test-generation/issue2test](https://github.com/test-generation/issue2test), [cuhk-shenzhen-se/utboost](https://github.com/cuhk-shenzhen-se/utboost) |
| Benchmarks / simulators | [sierra-research/tau2-bench](https://github.com/sierra-research/tau2-bench), [StonyBrookNLP/appworld](https://github.com/StonyBrookNLP/appworld), [xlang-ai/OSWorld](https://github.com/xlang-ai/OSWorld), [google-research/android_world](https://github.com/google-research/android_world), [microsoft/WindowsAgentArena](https://github.com/microsoft/WindowsAgentArena), [web-arena-x/webarena](https://github.com/web-arena-x/webarena), [web-arena-x/visualwebarena](https://github.com/web-arena-x/visualwebarena), [web-arena-x/webarena-infinity](https://github.com/web-arena-x/webarena-infinity), [ServiceNow/WorkArena](https://github.com/ServiceNow/WorkArena), [ServiceNow/BrowserGym](https://github.com/ServiceNow/BrowserGym), [ServiceNow/DoomArena](https://github.com/ServiceNow/DoomArena), [ServiceNow/GroundCUA](https://github.com/ServiceNow/GroundCUA), [ethz-spylab/agentdojo](https://github.com/ethz-spylab/agentdojo), [SalesforceAIResearch/MCP-Universe](https://github.com/SalesforceAIResearch/MCP-Universe), [laude-institute/terminal-bench](https://github.com/laude-institute/terminal-bench), [apple/ToolSandbox](https://github.com/apple/ToolSandbox), [OS-Copilot/OS-Genesis](https://github.com/OS-Copilot/OS-Genesis), [OS-Copilot/ScienceBoard](https://github.com/OS-Copilot/ScienceBoard), [QuantaAlpha/GitTaskBench](https://github.com/QuantaAlpha/GitTaskBench), [Tongyi-MAI/MobileWorld](https://github.com/Tongyi-MAI/MobileWorld) |

---

*Last updated: 2026-11-24 | 260+ papers added, 14 sections, and arXiv IDs completed for SWE-smith / R2E-Gym / Code2World*
