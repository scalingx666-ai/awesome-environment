# Agent 环境/任务合成相关论文整理

[简体中文](readme.md) | [English](readme.en.md)

> 覆盖范围：2021–2026 年公开发表的 **agent environment 合成 / task 合成 / 数据合成 / 验证器与基准度量 / 沙箱基建** 相关论文与开源仓库。
> 数据来源：arXiv、OpenReview / 顶会（ICML、NeurIPS、ICLR、ACL、EMNLP、CVPR、CoRL、ICSE、FSE、ISSTA、NDSS、ACL Findings、COLM、ICRA 等）、Semantic Scholar / Crossref / OpenAlex / DBLP、GitHub 与 AI 论文平台。
> 共收录 **639 篇论文 / 工作条目**（18 个分类章节 + 附录）+ **121 个开源仓库 / 基础设施 / Awesome 清单**；本轮新增「数据合成」「具身 / 机器人」「多 Agent / 社会仿真」「开源项目」四个章节。

---

## 一、难度、基准度量、验证可靠性方向

| 论文标题 | 链接 | 核心要点 | 验证状态 |
|---|---|---|---|
| A Matter of TASTE: Improving Coverage and Difficulty of Agent Benchmarks | [arXiv:2605.28556](https://arxiv.org/abs/2605.28556) | 程序化生成更难任务；在 τ²-Bench Verified 上性能下降范围 -5% ~ -80% | ✅ 确认 |
| AgentBoard: An Analytical Evaluation Board of Multi-turn LLM Agents | [arXiv:2401.13178](https://arxiv.org/abs/2401.13178) | 按子目标划分 easy/hard 难度；提出进度率度量指标 | ✅ 确认 |
| τ²-Bench: Evaluating Conversational Agents in a Dual-Control Environment | [arXiv:2506.07982](https://arxiv.org/abs/2506.07982) | 双控制器架构 + 组合式任务生成器；Telecom 双控制域建模为 Dec-POMDP；**ICML 2026 Oral** | ✅ 确认，补充 venue |
| **τ-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains** | [arXiv:2406.12045](https://arxiv.org/abs/2406.12045) | 由 LLM 模拟用户与 Agent 的动态对话，考察领域规则遵循；以对话结束时的数据库状态做高效且忠实的评估；τ²-Bench 的前身 | ✅ 新增，确认 |
| Easy2Hard-Bench: Standardized Difficulty Labels | [arXiv:2409.18433](https://arxiv.org/abs/2409.18433) | 难度标签标准化；NeurIPS 2024 | ✅ 确认 |
| Benchmarks as Microscopes: A Call for Model Metrology | [arXiv:2407.16711](https://arxiv.org/abs/2407.16711) | 将难度定义为可测量的模型属性；**COLM 2024** | ✅ 确认，补充 venue |
| Curriculum RL from Easy to Hard | [arXiv:2506.06632](https://arxiv.org/abs/2506.06632) | 从易到难的课程式强化学习训练范式 | ✅ 确认 |
| Cheap Reward Hacking Detection | [arXiv:2606.08893](https://arxiv.org/abs/2606.08893) | 面向验证器侧的难度研究、奖励欺骗检测 | ✅ 确认 |
| Do Agent Benchmarks Measure Capability? Protocol Validity | [arXiv:2607.22368](https://arxiv.org/abs/2607.22368) | 奖励欺骗等价于基准验证失效问题；腾讯混元团队 | ✅ 确认 |
| World Feedback for Clinical Agents (MAB-v3) | [arXiv:2607.01470](https://arxiv.org/abs/2607.01470) | 临床 Agent 环境加难，性能天花板分析；**ICML 2026** | ✅ 确认，补充 venue |
| EnviSAgE: A Survey of Environment Scaling | [arXiv:2511.09586](https://arxiv.org/abs/2511.09586) | 环境扩难综述，提出 GEF 三阶段循环 | ✅ 确认 |
| **Predicting Task Difficulty Without Rollouts** | [arXiv:2608.05797](https://arxiv.org/abs/2608.05797) | 无需 rollout 即可预测任务内在难度，为环境设计者与课程构建省算力 | ✅ 新增，确认 |
| **Why Do LLM Agents Fail in Exploring New Environments?（exploration collapse）** | [arXiv:2510.15047](https://arxiv.org/abs/2510.15047) | 训练中 Pass@1 微升而 Pass@k 大幅下降；用世界模型视角定位探索崩塌；**EMNLP 2026 Findings** | ✅ 新增，确认 |
| **Reward Hacking Benchmark (RHB)** | [arXiv:2605.02964](https://arxiv.org/abs/2605.02964) | 多步工具任务中的自然化捷径（跳过验证、从任务元数据推断、篡改评测函数）；**ICML 2026** | ✅ 新增，确认 |
| **Hack-Verifiable Environments (HVE)** | [arXiv:2605.20744](https://arxiv.org/abs/2605.20744) | 主动把可检测的 hack 植入任务，让奖励欺骗可被自动可靠识别 | ✅ 新增，确认 |
| **SpecBench** | [arXiv:2605.21384](https://arxiv.org/abs/2605.21384) | 把 SWE 任务拆成规格描述 / 可见验证测试 / 隐藏测试三部分，度量长程编码 Agent 奖励欺骗 | ✅ 新增，确认 |
| **Hack-Verifiable Terminal Bench** | [arXiv:2608.22103](https://arxiv.org/abs/2608.22103) | 将 HVE 方法论落到终端任务，用自动检测替代人工 / LLM 评判 | ✅ 新增，确认 |
| **BAITBENCH** | [arXiv:2608.30724](https://arxiv.org/abs/2608.30724) | 三个合成表格 ML 任务内置"捷径"，度量自主 ML 实验 Agent 的奖励欺骗 | ✅ 新增，确认 |
| **EvilGenie** | [arXiv:2511.21654](https://arxiv.org/abs/2511.21654) | 构造易刷分编程环境（硬编码测试、改测试文件）；留出单测 + LLM judge + 测试文件改动检测三重交叉验证 | ✅ 新增，确认 |
| **Scalable Weak-to-Strong Verifier Hardening** | [arXiv:2610.15924](https://arxiv.org/abs/2610.15924) | 用规模化算力自动修复可被攻击的验证器（weak-to-strong 迁移） | ✅ 新增，确认 |
| **Audit Where Hacks Pay** | [arXiv:2610.35716](https://arxiv.org/abs/2610.35716) | GRPO 训练中做预算约束的强验证器审计，定位奖励欺骗的收益来源 | ✅ 新增，确认 |
| **Diagnosing and Correcting Reward Hacking in Verifiable Instruction Following** | [arXiv:2610.19525](https://arxiv.org/abs/2610.19525) | 诊断并纠正可验证指令跟随中的奖励欺骗 | ✅ 新增，确认 |
| **Reward Hacking as a Transmissible Strategy** | [arXiv:2610.12822](https://arxiv.org/abs/2610.12822) | 揭示奖励欺骗可在多 Agent 编码系统中"传染"扩散 | ✅ 新增，确认 |
| **Detecting and Suppressing Reward Hacking with Gradient Fingerprints** | [arXiv:2604.16242](https://arxiv.org/abs/2604.16242) | 用梯度指纹检测并抑制奖励欺骗；**COLM 2026** | ✅ 新增，确认 |
| **Benchmarking Reward Hack Detection in Code Environments** | [arXiv:2601.20103](https://arxiv.org/abs/2601.20103) | 用对比分析（contrastive analysis）基准化代码环境中的奖励欺骗检测 | ✅ 新增，确认 |
| **Reward Hacking Challenges Oversight of Autonomous Research Agents** | [arXiv:2609.28614](https://arxiv.org/abs/2609.28614) | 指出自主科研 Agent 的奖励欺骗使人工监督机制失效 | ✅ 新增，确认 |
| **Agent Island** | [arXiv:2605.04312](https://arxiv.org/abs/2605.04312) | 用多 Agent 博弈（合作 / 冲突 / 说服）构造抗饱和、抗污染的动态基准 | ✅ 新增，确认 |
| **SynAE** | [arXiv:2605.22564](https://arxiv.org/abs/2605.22564) | 度量工具调用 Agent 评测中"合成数据"质量的系统框架 | ✅ 新增，确认 |
| **Search-Time Contamination (STC)** | [arXiv:2606.05241](https://arxiv.org/abs/2606.05241) | 定义检索期污染三类形态，度量深度研究 Agent 在公开基准上的性能虚高 | ✅ 新增，确认 |
| **Automated Benchmark Auditing for AI Agents and LLMs** | [arXiv:2605.26079](https://arxiv.org/abs/2605.26079) | 面向 AI Agent 与大模型的自动化基准审计流程 | ✅ 新增，确认 |
| **Trial by Trace** | [arXiv:2610.32285](https://arxiv.org/abs/2610.32285) | 以轨迹为单位评测 Agent Harness 的可靠性与失败归因 | ✅ 新增，确认 |
| **On the Reliability of Computer Use Agents** | [arXiv:2604.17849](https://arxiv.org/abs/2604.17849) | 系统刻画 CUA 的可靠性边界与失效模式 | ✅ 新增，确认 |
| **Multi-Agent Verification** | [arXiv:2502.20379](https://arxiv.org/abs/2502.20379) | 多验证器协同扩展测试时计算（test-time compute） | ✅ 新增，确认 |
| **Detecting Benchmark Contamination Through Watermarking** | [arXiv:2502.17259](https://arxiv.org/abs/2502.17259) | 用水印机制检测基准污染 | ✅ 新增，确认 |
| **Towards Contamination Resistant Benchmarks** | [arXiv:2505.08389](https://arxiv.org/abs/2505.08389) | 系统方法论：构建抗污染基准 | ✅ 新增，确认 |
| **gg-bench: Measuring General Intelligence with Generated Games** | [arXiv:2505.07215](https://arxiv.org/abs/2505.07215) | LLM 生成游戏描述并实现为 Gym 环境，数据生成过程可持续产出新评测实例 | ✅ 新增，确认 |
| **Verifiable Process Rewards for Agentic Reasoning** | [arXiv:2605.10325](https://arxiv.org/abs/2605.10325) | 为 Agentic 推理提供可验证的过程级奖励 | ✅ 新增，确认 |
| **Beyond Binary Verifiable Rewards: Behavioral Self-Rewarding for SWE Agents** | [arXiv:2610.12598](https://arxiv.org/abs/2610.12598) | 突破 0/1 二值可验证奖励，用行为自奖励为 SWE Agent 提供更细粒度信号 | ✅ 新增，确认 |
| **AgentV-RL** | [arXiv:2604.16004](https://arxiv.org/abs/2604.16004) | 把奖励建模转为多轮、工具增强的审议式流程；**ACL 2026** | ✅ 新增，确认 |
| **Agentic Rubrics as Contextual Verifiers for SWE Agents** | [arXiv:2601.04171](https://arxiv.org/abs/2601.04171) | 用"上下文相关 rubric"替代执行式验证，降低环境搭建开销且保持可解释 | ✅ 新增，确认 |
| **Task-Adaptive Rubrics for GUI Reward Modeling** | [arXiv:2608.24174](https://arxiv.org/abs/2608.24174) | 为每个 GUI 任务实例自适应构造评判标准，修复跨任务误迁移 | ✅ 新增，确认 |
| **Agentic Reward Modeling（渐进式轨迹锚定交互验证）** | [arXiv:2602.00575](https://arxiv.org/abs/2602.00575) | 主动交互式验证弥补 GUI 状态部分不可观测的缺陷 | ✅ 新增，确认 |
| **Interactive Reward Agent（GUI 环境状态校验）** | [arXiv:2607.25904](https://arxiv.org/abs/2607.25904) | 通过环境状态校验来评估 GUI 任务完成情况 | ✅ 新增，确认 |
| **GUI-PRA** | [arXiv:2509.23263](https://arxiv.org/abs/2509.23263) | 面向 GUI 的过程奖励 Agent，补齐标准 PRM 缺失的领域裁决逻辑 | ✅ 新增，确认 |
| **GUI-Shepherd** | [arXiv:2509.23738](https://arxiv.org/abs/2509.23738) | 52K 人工标注交互训练的过程奖励模型，兼作 RL 奖励与推理期验证器 | ✅ 新增，确认 |
| **VisCritic** | [arXiv:2606.24525](https://arxiv.org/abs/2606.24525) | 在视觉特征空间直接比对操作前后截图作为过程奖励（Siamese 视觉验证） | ✅ 新增，确认 |
| **VeriCUA** | [arXiv:2610.26469](https://arxiv.org/abs/2610.26469) | 学习"何时查、查什么"的主动验证策略，提升 CUA 奖励可靠性 | ✅ 新增，确认 |
| **AgentPRM** | [arXiv:2511.08325](https://arxiv.org/abs/2511.08325) | 以步骤级"承诺与进展"信号构建 Agent 过程奖励模型 | ✅ 新增，确认 |
| **RLAR** | [arXiv:2603.00724](https://arxiv.org/abs/2603.00724) | 面向多任务 LLM RL 的 Agent 化奖励系统 | ✅ 新增，确认 |
| **Hybrid Reward Normalization** | [arXiv:2509.25598](https://arxiv.org/abs/2509.25598) | 面向不可验证 Agent 任务的混合奖励归一化 | ✅ 新增，确认 |
| **ARTIS** | [arXiv:2602.01709](https://arxiv.org/abs/2602.01709) | 通过迭代仿真实现风险感知的 Agentic 测试时扩展；**NeurIPS 2026** | ✅ 新增，确认 |
| **Evaluating Test-Time Scaling of General LLM Agents** | [arXiv:2602.18998](https://arxiv.org/abs/2602.18998) | 系统评测通用 LLM Agent 的测试时扩展收益 | ✅ 新增，确认 |
| **Agentic Test-Time Scaling for WebAgents** | [arXiv:2602.12276](https://arxiv.org/abs/2602.12276) | Web Agent 的测试时扩展方法 | ✅ 新增，确认 |
| **Scaling Test-Time Compute for Agentic Coding** | [arXiv:2604.16529](https://arxiv.org/abs/2604.16529) | 编码 Agent 的测试时算力扩展系统研究 | ✅ 新增，确认 |
| **Difficulty-Aware Agentic Orchestration** | [arXiv:2509.11079](https://arxiv.org/abs/2509.11079) | 难度感知的查询特定多 Agent 工作流编排；**WWW 2026** | ✅ 新增，确认 |
| **A Rubric-Supervised Critic from Sparse Real-World Outcomes** | [arXiv:2603.03800](https://arxiv.org/abs/2603.03800) | 从稀疏、噪声的真实人机协作反馈学习 critic，兼作 RL 奖励模型与推理期扩展信号 | ✅ 新增，确认 |
| **SEABench** | [arXiv:2609.35596](https://arxiv.org/abs/2609.35596) | 评测自演化 Agent 的内生失配：局部有用的更新可能在后续任务中演变为不安全行为 | ✅ 新增，确认 |
| **Query-Only Backdoor Attacks on Self-Evolving Skills** | [arXiv:2608.08303](https://arxiv.org/abs/2608.08303) | 揭示通过轨迹投毒对自演化技能系统植入后门攻击的路径 | ✅ 新增，确认 |
| **Humanize: Judgement Engineering for Agentic Coding** | [arXiv:2610.08900](https://arxiv.org/abs/2610.08900) | 以显式、可机械强制的判定边界（规划/实现/评审/学习之间）构建多 Agent 编排工作流 | ✅ 新增，确认 |
| **SEVerA** | [arXiv:2603.25111](https://arxiv.org/abs/2603.25111) | 首个形式化验证的自演化 LLM Agent；对规划器合成的 Agent 程序给出安全性与正确性保证 | ✅ 新增，确认 |
| **TRACE** | [arXiv:2610.11678](https://arxiv.org/abs/2610.11678) | 把「分数变化」从结论变成可检验的诊断：对评测的某一部分做定向改动并对照，判断分数变化来自能力提升还是验证器脆弱（验证器既当指标又当训练奖励） | ✅ 新增 |
| **Computer Use at the Edge of the Statistical Precipice** | [arXiv:2605.08261](https://arxiv.org/abs/2605.08261) | 揭示 CUA 交互环境评测的方法论陷阱：一个 1MB 的盲目回放脚本（从不看屏幕、直接执行录制动作）在主流静态基准上超过前沿模型，其期望成功率恰等于录制的成功率 | ✅ 新增 |
| **Executable-Contract Audit** | [arXiv:2609.37315](https://arxiv.org/abs/2609.37315) | 对工具型 Agent 环境做「可执行契约审计」：基准默认模拟工具按接口声明执行，但该假设无分类可查，一处底层缺陷会在每次重跑中持续存在 | ✅ 新增 |
| **EnvOS** | [arXiv:2610.40246](https://arxiv.org/abs/2610.40246) | 面向「世界会变」的 CUA 审计：现象驱动任务构造 + 认证 + 证据式评测，区分失败来自 Agent、来自未生效的变更，还是来自评分器 | ✅ 新增 |
| **OpenReward** | [arXiv:2510.24636](https://arxiv.org/abs/2510.24636) | 用 RL 学习奖励长程 Agentic 任务：现有奖励模型在知识密集、长程任务上难以区分细微正确性，需要超越模型内部知识的接地 | ✅ 新增 |
| **Autorubric** | [arXiv:2603.00077](https://arxiv.org/abs/2603.00077) | 统一 rubric 式评测框架：针对 LLM judge 的位置偏置、随机不一致、标准混淆、不确定下强制判断与模型相关校准等问题给出统一处理 | ✅ 新增 |
| **PADMÉ** | [arXiv:2609.36086](https://arxiv.org/abs/2609.36086) | 面向 Agent 评测器「元评测」的偏好对齐数据合成：用偏好而非绝对打分来校准多准则 Agent 评估器与人类判断的一致性 | ✅ 新增 |

---

## 二、环境合成

| 论文/框架 | 核心贡献 | 时间/出处 | 链接 | 验证状态 |
|---|---|---|---|---|
| **Agent-World** | 1978 环境 / 19,822 工具；工具依赖图 + 可执行 Python 解任务合成；多环境闭环 RL + GRPO；自演化竞技场 | 2026-04，人大 & 字节 Seed | [arXiv:2604.18292](https://arxiv.org/abs/2604.18292) | ✅ 确认 |
| **EnvScaler** | 191 环境 / ~7K 场景；SkelBuilder + ScenGenerator；SFT 后 BFCL-MT +8.67、ACEBench-Agent +11.57 | 2026-01，**ACL 2026 Findings** | [arXiv:2601.05808](https://arxiv.org/abs/2601.05808) | ✅ 确认 |
| **Agent-World Model (AWM)** | 代码驱动 + 数据库支撑全合成环境管线；1000 envs / 10000 tasks / 35 tools | 2026-02，**ICML 2026** | [arXiv:2602.10090](https://arxiv.org/abs/2602.10090) | ✅ 确认 |
| **InfiniteWeb** | 可扩展 Web 环境自动合成；统一规格 + 测试驱动开发，面向 GUI Agent 训练 | 2026-01，PKU/NJU/MSR Asia | [arXiv:2601.04126](https://arxiv.org/abs/2601.04126) | ✅ 确认 |
| **ToolVerse** | ~400 MCP servers / ~4,500 工具；工具依赖图 + Dynamic Unlocking；长程 TIR；BFCL-v3 35.00→37.50%，τ²-Bench 27.33→32.37% | 2026-07 | [arXiv:2607.15660](https://arxiv.org/abs/2607.15660) | ✅ 确认 |
| **SPADE** | 自博弈：环境设计者生成 Gym 式可执行环境 ↔ 推理 Agent 求解；BFCL v4 多轮 +5.3，ACEBench-Agent +5.7 | 2026-08 | [arXiv:2608.19197](https://arxiv.org/abs/2608.19197) | ✅ 确认 |
| **CuES** | 好奇心驱动、环境锚定任务合成；兼容 AppWorld/BFCL/WebShop，无需人工种子 | 2025-12 | [arXiv:2512.01311](https://arxiv.org/abs/2512.01311) | ✅ 确认 |
| **EnvFactory** | 可执行环境合成；拓扑感知图引导鲁棒 RL 与轨迹生成 | 2026-05，港科大（广州）LARK 等 | [arXiv:2605.18703](https://arxiv.org/abs/2605.18703) | ✅ 确认 |
| **Qwen-AgentWorld** | 语言世界模型模拟通用 Agent 环境；35B-A3B / 397B-A17B | 2026-06，千问 | [arXiv:2606.24597](https://arxiv.org/abs/2606.24597) | ✅ 确认 |
| **ScaleEnv** | 从零构建完全交互式环境和可验证任务；工具依赖图扩展 + 可执行动作验证；τ²-Bench 等多轮工具基准显著提升 | 2026，**ICML 2026**，美团参与 | [arXiv:2602.06820](https://arxiv.org/abs/2602.06820) | ✅ 确认 |
| **GenEnv** | 难度对齐，Agent-环境模拟器协同进化，在能力边界生成任务 | 2025 | [arXiv:2512.19682](https://arxiv.org/abs/2512.19682) | ✅ 确认 |
| **C-World** | 按需构建 Agent 环境；5,571 工具 / 204 应用；任务分布引擎合成带约束长程工作流；转移函数注入真实故障；World Engine 与真实执行 Spearman=0.883 | 2026，**ACL 2026 Long** | [arXiv:2601.06328](https://arxiv.org/abs/2601.06328) | ✅ 确认 |
| **ClawEnvKit** | 自然语言规格 → 按需生成 claw-like Agent 环境；Auto-ClawEval 含 1,040 环境 / 24 类别；成本比人工低 13,800 倍；Harness engineering 比裸 ReAct 提升最多 15.7 个百分点 | 2026-04 | [arXiv:2604.18543](https://arxiv.org/abs/2604.18543) | ✅ 确认 |
| **AgentMercury** | 从高层商业场景合成可执行环境；4,783 环境 / 14 行业 / 50 国家；Qwen3.5-4B 在 EnterpriseOps-GYM 上 12.3→15.7；微调后世界编写成功率 3.3%→83.3% | 2026-08 | [arXiv:2608.20634](https://arxiv.org/abs/2608.20634) | ✅ 确认 |
| **Repo2RLEnv** | 将 GitHub 仓库/PR/提交历史转换为可执行 RL 环境；输出 Harbor 格式任务包（指令+环境+参考解+验证器）；内置 6 条原生流水线 + Tasksmith + 14 个研究配方；支持推送至 HuggingFace Hub | — | [GitHub](https://github.com/huggingface/Repo2RLEnv) · [文档](https://huggingface.github.io/Repo2RLEnv/) | ✅ 确认 |
| **AutoForge** | 端到端自动化合成"高难度但易验证"的模拟环境；提出环境级 RL 算法缓解模拟用户不稳定与环境异质性带来的训练难题 | 2025-12 | [arXiv:2512.22857](https://arxiv.org/abs/2512.22857) | ✅ 新增，确认 |
| **EnvCraft** | 面向 Claw-like Agent 合成可执行环境；突破既有合成环境"仅限工具调用端点"的限制，支撑端到端真实工作流 | 2026-09 | [arXiv:2609.05576](https://arxiv.org/abs/2609.05576) | ✅ 新增，确认 |
| **AgentScaler（环境扩展走向通用 Agent 智能）** | 阿里通义；论证函数调用能力广度与环境多样性直接相关，自动构造模拟函数调用环境 | 2025-09 | [arXiv:2509.13311](https://arxiv.org/abs/2509.13311) | ✅ 新增，确认 |
| **SynthAPI（工具使用 Agent 的环境扩展 Scaling Law）** | 显式控制工具 / 任务 / 数据库三维多样性；458,752 条任务 × 84 环境，给出可复现的 scaling law | 2026-10 | [arXiv:2610.37648](https://arxiv.org/abs/2610.37648) | ✅ 新增，确认 |
| **WorkForge（长程工作型 Agent 的可验证环境扩展）** | 在手写环境工程开销与合成方案失真之间取得平衡的可扩展合成框架 | 2026-10 | [arXiv:2610.04906](https://arxiv.org/abs/2610.04906) | ✅ 新增，确认 |
| **Learning Design Taste through Verifiable Synthetic Environments** | 在可验证合成环境中用 Agentic RL 学习 UI 设计品味；分层验证框架（硬门禁 / 渲染度量 / rubric 评委 / 组内相对偏好 / 盲评专家组） | 2026-11 | [arXiv:2611.20612](https://arxiv.org/abs/2611.20612) | ✅ 新增，确认 |
| **EnvOpt（环境本身的自动优化）** | 提出"稳态环境（stationary environment）"概念；补充参数调优与 harness 优化之外的第三个优化方向 | 2026-11 | [arXiv:2611.07372](https://arxiv.org/abs/2611.07372) | ✅ 新增，确认 |
| **AgentFactory** | 面向 Agentic 系统的自动化设计与优化；显式考虑模型能力在拓扑中的角色，而非只优化工作流结构 | 2026-09 | [arXiv:2609.01045](https://arxiv.org/abs/2609.01045) | ✅ 新增，确认 |
| **Agent²** | Agent-Generates-Agent：双 Agent 架构，从自然语言任务描述 + 环境代码自动生成可执行 RL 方案 | 2025-09 | [arXiv:2509.13368](https://arxiv.org/abs/2509.13368) | ✅ 新增，确认 |
| **CodeMidas** | 以源码为唯一任务来源，把代码库中已实现的功能转成可执行 RL 环境 | 2026-09 | [arXiv:2609.22068](https://arxiv.org/abs/2609.22068) | ✅ 新增，确认 |
| **FrogNano** | 仅用约 1,500 个合成环境 + 在线任务合成（校准到当前 checkpoint 的可学习前沿）后训练出 4B 编码 Agent | 2026-09 | [arXiv:2609.07925](https://arxiv.org/abs/2609.07925) | ✅ 新增，确认 |
| **PhantomEnvironments** | 完全由规则生成的合成环境（零 LLM 调用、零边际成本）训练搜索 Agent，规避幻觉与基准污染 | 2026-09 | [arXiv:2609.40221](https://arxiv.org/abs/2609.40221) | ✅ 新增，确认 |
| **ProgramGym** | 面向长程程序复现 Agent 的可扩展训练环境，迫使 Agent 自行发现需求并决定系统设计 | 2026-10 | [arXiv:2610.13395](https://arxiv.org/abs/2610.13395) | ✅ 新增，确认 |
| **POSEIDON** | 从科学代码仓库规模化抽取可验证训练环境；同预算下环境数量约为先前方法 10 倍 | 2026-10 | [arXiv:2610.32448](https://arxiv.org/abs/2610.32448) | ✅ 新增，确认 |
| **From Repositories to Training Environments（环境演化循环）** | 打破"构建—验证"的线性流水线，用及时可靠的代理信号持续提升环境的训练价值，适配递归自我改进（RSI） | 2026-11 | [arXiv:2611.21152](https://arxiv.org/abs/2611.21152) | ✅ 新增，确认 |
| **Libra（训练环境而非只训模型）** | 在仓库中引入可变"目录（catalog）"层级索引，用 LLM 驱动的优化循环训练 Agent 的信息定位能力 | 2026-05 | [arXiv:2607.00016](https://arxiv.org/abs/2607.00016) | ✅ 新增，确认 |
| **WebUniverse** | 从开源仓库与真实网页构造可验证的 Agentic 前端开发任务与已验证开发轨迹（文本落地 + 视觉复现） | 2026-10 | [arXiv:2610.33149](https://arxiv.org/abs/2610.33149) | ✅ 新增，确认 |
| **VeriEnv（重建真实网站为可验证合成环境）** | 把真实网站自动克隆为完全可执行、可验证的合成环境；通过 Python SDK 暴露受控内部访问，使 Agent 自生成任务 | 2026-03 | [arXiv:2603.10505](https://arxiv.org/abs/2603.10505) | ✅ 新增，确认 |
| **SynthTools** | 全 LLM 流水线覆盖工具使用环境的完整生命周期：环境生成 → 模拟 → 校验 → 任务构建 | 2025-11 | [arXiv:2511.09572](https://arxiv.org/abs/2511.09572) | ✅ 新增，确认 |
| **Agent-Environment Alignment via Automated Interface Generation** | 自动生成接口以对齐 Agent 的内部预期与环境的真实状态转移，抑制 agent-environment misalignement | 2025-05 | [arXiv:2505.21055](https://arxiv.org/abs/2505.21055) | ✅ 新增，确认 |
| **Simia（用推理模型模拟环境）** | 证明 LLM 能在无真实 testbed/API 的情况下模拟逼真的环境反馈；Simia-SFT + Simia-RL | 2025-11 | [arXiv:2511.01824](https://arxiv.org/abs/2511.01824) | ✅ 新增，确认 |
| **RLVE（自适应可验证环境）** | 每个可验证环境随策略能力动态调整问题难度分布，避免学习信号消失 | 2025-11，**ICML 2026** | [arXiv:2511.07317](https://arxiv.org/abs/2511.07317) | ✅ 新增，确认 |
| **AutoEnv** | 自动化构建可控且异构的环境集合，度量 Agent 的跨环境学习能力 | 2025-11 | [arXiv:2511.19304](https://arxiv.org/abs/2511.19304) | ✅ 新增，确认 |
| **Dyna-Mind** | 提出 Agent 需要"替代性试错（vicarious trial and error）"，从经验中学习模拟能力以支撑长程交互 | 2025-10 | [arXiv:2510.09577](https://arxiv.org/abs/2510.09577) | ✅ 新增，确认 |
| **UI-Simulator** | 生成结构化 UI 状态与转移 + 引导式 rollout + 轨迹筛选，规模化合成 UI 训练轨迹 | 2025-10 | [arXiv:2510.14969](https://arxiv.org/abs/2510.14969) | ✅ 新增，确认 |
| **ReCreate** | 由真实环境交互经验驱动领域 Agent 的自动创建与演化，避免黑箱式 scaffold 优化 | 2026-01 | [arXiv:2601.11100](https://arxiv.org/abs/2601.11100) | ✅ 新增，确认 |
| **Youtu-Agent** | 模块化框架，支持 Agent 的自动化生成与持续演化，配套混合策略优化 | 2025-12 | [arXiv:2512.24615](https://arxiv.org/abs/2512.24615) | ✅ 新增，确认 |
| **From Language Models to World-Acting Systems** | 综述：区分模型能力、系统集成、状态持久性与安全授权，梳理 Agentic AI 在数字/社会/虚拟/物理环境中的进展与边界 | 2026-09 | [arXiv:2609.04894](https://arxiv.org/abs/2609.04894) | ✅ 新增，确认 |
| **MCP-Universe RL** | 面向 MCP 工具使用 Agent 的 RL 框架：解决数百并发轨迹的环境隔离与长多轮 rollout 的 GPU 调度 | 2026-08 | [arXiv:2608.22167](https://arxiv.org/abs/2608.22167) | ✅ 新增，确认 |
| **Gecko** | 带状态反馈的模拟环境，用于低成本精炼 Agent 的工具调用序列，避免真实工具的副作用 | 2026-02 | [arXiv:2602.19218](https://arxiv.org/abs/2602.19218) | ✅ 新增，确认 |
| **LLM-in-Sandbox** | 把计算机虚拟化为仅含基础功能的代码沙箱，验证最小化计算机环境即可激发通用 Agent 智能 | 2026-01 | [arXiv:2601.16206](https://arxiv.org/abs/2601.16206) | ✅ 新增，确认 |
| **World of SWECraft** | Software World 框架模拟真实软件生态中的多 Agent 协作，并与 Agent 间交互的 SWECraft 流水线配套 | 2026-10 | [arXiv:2610.24061](https://arxiv.org/abs/2610.24061) | ✅ 新增，确认 |
| **CompoWorld** | 组合式环境扩展：通过跨多个服务连接信息与动作来扩张任务空间，突破单环境内生成任务的限制 | 2026-09 | [arXiv:2609.33665](https://arxiv.org/abs/2609.33665) | ✅ 新增，确认 |
| **SciDisco** | 面向科学发现的可扩展过程监督环境，用于回合级 Agentic RL | 2026-07 | [arXiv:2607.28990](https://arxiv.org/abs/2607.28990) | ✅ 新增，确认 |
| **DeepSearch-World** | 确定性且可验证的环境 + 自蒸馏框架，用于训练深度搜索 Agent | 2026-07 | [arXiv:2607.07820](https://arxiv.org/abs/2607.07820) | ✅ 新增，确认 |
| **EE-MCP** | 通过自动化环境生成与经验学习实现自演化的 MCP-GUI 混合 Agent | 2026-04 | [arXiv:2604.09815](https://arxiv.org/abs/2604.09815) | ✅ 新增，确认 |
| **ReSyn** | 面向推理模型自主扩展合成环境，摆脱依赖少数手工过程式验证器 | 2026-02 | [arXiv:2602.20117](https://arxiv.org/abs/2602.20117) | ✅ 新增，确认 |
| **ASTRA（Automated Synthesis of agentic Trajectories and Reinforcement Arenas）** | 自动合成 Agent 轨迹与强化竞技场，摆脱人工干预与不可验证的模拟环境 | 2026-01 | [arXiv:2601.21558](https://arxiv.org/abs/2601.21558) | ✅ 新增，确认 |
| **AgentGym（Evolving LLM Agents across Diverse Environments）** | 让 LLM Agent 在多样环境中自主演化自我提升，摆脱对专家轨迹模仿的依赖 | 2024-06 | [arXiv:2406.04151](https://arxiv.org/abs/2406.04151) | ✅ 新增，确认 |
| **SkillGym** | 从互联网爬取大量 agent skill 并筛选可离线复现者；builder-reviewer 流水线构造四类难度可控任务（任务 + 参考解 + 可执行验证器），产出 6.8K 环境 / 19K 验证成功轨迹用于 SFT | 2026-09 | [arXiv:2609.37539](https://arxiv.org/abs/2609.37539) | ✅ 新增 |
| **Skill2Env** | 能力导向的环境合成：以 skill 为起点，用可复用「难度模式」实例化任务蓝图（目标、挑战、环境事实、信息边界、验收标准），再据此联合构建可执行任务与环境 | 2026-09 | [arXiv:2609.33772](https://arxiv.org/abs/2609.33772) | ✅ 新增 |
| **SimWorld Studio** | 基于 Unreal Engine 5 的开放平台；核心 SimCoder 是工具/技能增强的编码 Agent，按语言或图像指令编写并执行引擎级代码来构建物理合理的可部署 3D 环境，含可验证任务与标准学习接口，并通过执行反馈自演化 | 2026-05 | [arXiv:2605.09423](https://arxiv.org/abs/2605.09423) | ✅ 新增 |
| **Envs-FORGE** | 把验证器奖励转成 per-seed 的环境合成动作：估计种子通过率，围绕目标学习前沿给六种「投影-方向」动作打分，再用混合整数线性规划为每个种子选择生成策略，同步重写指令、fixtures、oracle、测试与 Docker；只有 gold-verified 包进入 RL | 2026-08 | [arXiv:2608.14312](https://arxiv.org/abs/2608.14312) | ✅ 新增 |
| **Learning to Build the Environment** | 零数据推理 RL 的新范式：模型不只生成题目或轨迹，而是构造可复用的可执行环境（采样实例、计算参考、打分），把自进化从数据生成循环变成环境构建循环；关键在于「求解-验证不对称」 | 2026-05 | [arXiv:2605.14392](https://arxiv.org/abs/2605.14392) | ✅ 新增 |
| **RecreationWorld** | 五平台「重建式」环境：给定一个运行中的参考系统，Agent 需自行探索行为并用代码忠实重建，可自由交错 GUI 探索、编程实现与视觉自验；面向混合型 CUA，提供可复现环境与多级验证 | 2026-09 | [arXiv:2609.22000](https://arxiv.org/abs/2609.22000) | ✅ 新增 |
| **VERA** | 规模化构建「可恢复」的可验证环境：从初始轨迹出发由 Agent 写 rubric 与可执行检查，环境可在任意步骤恢复快照，让 Agent 在医疗研究等数十步依赖任务上共同进化，而非只给最终结果打分 | 2026-10 | [arXiv:2610.05923](https://arxiv.org/abs/2610.05923) | ✅ 新增 |
| **AutoGym** | blueprint-first 的 gym 生成：先出任务蓝图与验证规约，再生成可执行环境与验证器，避免单次合成的「表面难度」与事后 LLM 判分 | 2026-09 | [arXiv:2609.22592](https://arxiv.org/abs/2609.22592) | ✅ 新增 |
| **AutoEnvScaling** | 把环境设计本身当成终端任务：proposer Agent 依据被训 solver 的 rollout 造新 RL 环境，solver 的新 rollout 反过来指导下一轮 proposer，形成自动化数据飞轮 | 2026-10 | [arXiv:2610.14163](https://arxiv.org/abs/2610.14163) | ✅ 新增 |
| **Recursive Environment Scaling (RES)** | 在保持任务目标与完成要求不变的前提下，递归改写信息访问、资源关系与执行依赖来提升难度；每轮改动经执行侧 grounded 校验并在后续轮次继承，在 3 个基准 294 个初始任务上验证 | 2026-10 | [arXiv:2610.16397](https://arxiv.org/abs/2610.16397) | ✅ 新增 |
| **MetaExp** | 可验证的跨任务环境扩展：把「经验学习」本身训练成可迁移能力，让 Agent 从不同任务族的交互反馈中提炼可复用经验，而非只在固定任务分布上优化外部经验脚手架 | 2026-10 | [arXiv:2610.21492](https://arxiv.org/abs/2610.21492) | ✅ 新增 |
| **Nex-N1** | 统一生态从复杂度、多样性、真实性三个正交维度扩展交互环境与交互信号，用于大规模 Agent 策略学习 | 2025-12 | [arXiv:2512.04987](https://arxiv.org/abs/2512.04987) | ✅ 新增 |
| **Scalable Environments Drive Generalizable Agents** | 立场论文：泛化要求「环境扩展」——扩展 Agent 所面对的可执行规则集分布（接口、动力学、观测、反馈信号），而不只是在固定基准里堆轨迹或堆任务 | 2026-05 | [arXiv:2605.18181](https://arxiv.org/abs/2605.18181) | ✅ 新增 |
| **TRUSTEE（Democratizing Tool Learning with Fully Simulated Environments）** | 用开源 LM（最小 8B）完整模拟环境：任务生成、用户模拟、工具模拟与轨迹评估全部由小模型承担，动态可扩展，摆脱真值标注与闭源模型依赖 | 2026-04 | [arXiv:2604.17739](https://arxiv.org/abs/2604.17739) | ✅ 新增 |
| **Simulate to Generalize** | 用 LLM 充当数字世界模型，把数据合成与环境构建解耦：仅从领域名出发自动合成多样 API 与状态迁移轨迹，绕开为每个领域实现可执行环境的成本 | 2026-07 | [arXiv:2607.16900](https://arxiv.org/abs/2607.16900) | ✅ 新增 |
| **EnvSimBench** | 首个系统评测「LLM 环境模拟」保真度的基准，聚焦幻觉、逻辑不一致与静默状态漂移这类会污染奖励信号的失败模式 | 2026-05 | [arXiv:2605.07247](https://arxiv.org/abs/2605.07247) | ✅ 新增 |
| **CoDE (Environment Generation for Compositional RL)** | 2022 年早期环境生成工作：训练一个 Generator Agent 依据当前技能水平自动生成一系列组合式任务（依赖图形式），形成自动课程，使 RL Agent 学到比预定义任务更复杂的组合行为 | 2022-01 | [arXiv:2201.08896](https://arxiv.org/abs/2201.08896) | ✅ 新增 |
| **Synthetic Environments & Reward Networks** | 2022 年工作：用神经网络表示「合成环境（SE）」与「奖励网络（RN）」作为真实环境的代理，双层优化（内层训 Agent、外层训代理），仅在该代理环境中训练即可解真实环境 | 2022-02 | [arXiv:2202.02790](https://arxiv.org/abs/2202.02790) | ✅ 新增 |
| **Dyna-bAbI** | 2021 年工作：为 bAbI 故事理解基准加入细粒度可控的动态合成任务生成机制，让合成基准可按需要调节难度与干扰 | 2021-11 | [arXiv:2112.00086](https://arxiv.org/abs/2112.00086) | ✅ 新增 |
| **SPHINX** | 程序化生成的视觉感知与推理合成环境：用 motif、tile、图表、图标与几何基元生成带可验证真值的谜题，25 类任务；GPT-5 仅 51.1% | 2025-11 | [arXiv:2511.20814](https://arxiv.org/abs/2511.20814) | ✅ 新增 |
| **LogicEnvGen** | 任务逻辑驱动的具身仿真环境生成：自上而下由 LLM 生成「逻辑多样」的场景，而非只追求视觉真实感，补齐从测试视角评估具身 Agent 规划鲁棒性的维度 | 2026-01 | [arXiv:2601.13556](https://arxiv.org/abs/2601.13556) | ✅ 新增 |
| **CrossEnv** | 用实体-工具图合成「跨环境」可验证任务：一个服务中的动作依赖另一个服务获得的信息，解决单环境任务无法刻画真实跨服务交互的问题 | 2026-11 | [arXiv:2611.22777](https://arxiv.org/abs/2611.22777) | ✅ 新增 |
| **Interactive Structured Environment Scaling** | 指出结构化与检索式环境依赖「上游预过滤」（只保留答案附近的子图或固定段落），会引入根本性的测量混淆，并提出交互式结构化环境扩展来消除该问题 | 2026-11 | [arXiv:2611.19871](https://arxiv.org/abs/2611.19871) | ✅ 新增 |
| **EnvLunch** | 「环境即免费午餐」：环境本身自带丰富交互结构与可验证结果，据此从终态观测反推功能等价轨迹做无标注 warm-up，无需人工或模型写任务描述 | 2026-10 | [arXiv:2610.33817](https://arxiv.org/abs/2610.33817) | ✅ 新增 |
| **AgentPolicyForge / PolicyGym** | 用可执行环境构造策略基准并迭代训练 policy guard：10 类策略族 698 个生成场景 + 254 个留出人工复核测试场景，违规用例全部使用「被允许的工具」，必须核查参数、资源与上下文而非只看工具名 | 2026-10 | [arXiv:2610.28989](https://arxiv.org/abs/2610.28989) | ✅ 新增 |

---

## 三、经验/交互合成

| 论文/框架 | 核心贡献 | 时间/出处 | 链接 | 验证状态 |
|---|---|---|---|---|
| **Tool-R0** | 生成器-求解器自博弈共进化；零训练数据自举工具调用 | 2026-02，UIUC | [arXiv:2602.21320](https://arxiv.org/abs/2602.21320) | ✅ 确认 |
| **DreamGym** | 推理式经验模型合成多样化经验；低成本在线 RL、sim-to-real | 2025-11，**ICLR 2026**，Meta/芝大/伯克利 | [arXiv:2511.03773](https://arxiv.org/abs/2511.03773) | ✅ 确认 |
| **Grounded Interaction Synthesis (GAIS)** | 基于真实环境模拟人-助手长程交互轨迹，包含对抗约束；两阶段 grounding 机制 | 2026-06，**ACM SIGKDD 2026** | [arXiv:2606.02001](https://arxiv.org/abs/2606.02001) | ✅ 确认 |
| **TOUCAN** | 150 万条轨迹 / ~500 个真实 MCP 环境；当前最大公开工具 Agent 数据集；微调后 BFCL V3 超越更大闭源模型，推进 MCP-Universe Bench Pareto 前沿 | 2025-10 | [arXiv:2510.01179](https://arxiv.org/abs/2510.01179) | ✅ 确认 |
| **Mock Worlds, Real Skills** | SYNTHAGENT 框架：LLM 用户模拟器 + Mock 工具系统 + rubric 奖励；14 个数据集上显著提升 | 2026，**ACL 2026 Long** | [arXiv:2601.22511](https://arxiv.org/abs/2601.22511) | ✅ 确认 |
| **Digital Red Queen** | 自博弈算法拥抱红皇后式的开放对抗动力学，持续适应对手演化，突破静态优化式 LLM 演化框架 | 2026-01 | [arXiv:2601.03335](https://arxiv.org/abs/2601.03335) | ✅ 新增，确认 |
| **AgentTrek** | 三阶段可扩展数据合成流水线：抓取过滤教程文本 → 引导式回放 → 轨迹生成；**ICLR 2025 Spotlight** | 2024-12 | [arXiv:2412.09605](https://arxiv.org/abs/2412.09605) | ✅ 新增，确认 |
| **Execution-First Synthetic Tool-Use Trace Generation** | "执行优先"合成：先生成合法工具序列与可执行工作流再倒推用户请求，避免 query-first 合成产出无效调用 | 2026-07 | [arXiv:2607.29175](https://arxiv.org/abs/2607.29175) | ✅ 新增，确认 |
| **Self-Play SWE-RL (SSR)** | 自博弈驱动软件 Agent 训练，尽量摆脱对人类知识与人工策划环境的依赖；**ICML 2026** | 2025-12 | [arXiv:2512.18552](https://arxiv.org/abs/2512.18552) | ✅ 新增，确认 |
| **Live-SWE-agent** | 探索 SWE Agent 能否在推理过程中"边飞边自演化"，无需专用流程设计 | 2025-11 | [arXiv:2511.13646](https://arxiv.org/abs/2511.13646) | ✅ 新增，确认 |
| **SWE-RM** | 免执行（execution-free）反馈的奖励模型，提供比单元测试更细粒度的轨迹信号 | 2025-12 | [arXiv:2512.21919](https://arxiv.org/abs/2512.21919) | ✅ 新增，确认 |
| **SWE-Synth** | 仓库级、真实可验证、带中间推理轨迹的缺陷修复数据合成框架 | 2025-04 | [arXiv:2504.14757](https://arxiv.org/abs/2504.14757) | ✅ 新增，确认 |
| **SWE-Flow** | 从单元测试反推增量开发步骤（测试驱动式数据合成），构建运行时依赖图 RDG；**ICML 2025** | 2025-06 | [arXiv:2506.09003](https://arxiv.org/abs/2506.09003) | ✅ 新增，确认 |
| **BugPilot** | 让 SWE Agent 引入功能时"无意中"破坏测试以生成真实感高难度缺陷，规避刻意扰动带来的分布偏移 | 2025-10 | [arXiv:2510.19898](https://arxiv.org/abs/2510.19898) | ✅ 新增，确认 |
| **SWE-Mirror** | 跨仓库镜像 issue：最大化复用既有 Gym 环境 + 放大 GitHub 真实问题池 | 2025-09 | [arXiv:2509.08724](https://arxiv.org/abs/2509.08724) | ✅ 新增，确认 |
| **ScaleSWE（Immersion in the GitHub Universe）** | 沙箱化多 Agent 流水线，环境搭建 / 测试生成 / 问题描述三角色协同，规模化产出高质量 SWE 数据 | 2026-02 | [arXiv:2602.09892](https://arxiv.org/abs/2602.09892) | ✅ 新增，确认 |
| **daVinci-Agency** | 重构长程 Agent 数据合成：捕捉真实长依赖结构与跨阶段演化动态 | 2026-02 | [arXiv:2602.02619](https://arxiv.org/abs/2602.02619) | ✅ 新增，确认 |
| **Training Versatile Coding Agents in Synthetic Environments** | 从零合成环境训练多样化编码 Agent，突破"只用 issue 修复任务"的局限 | 2025-12 | [arXiv:2512.12216](https://arxiv.org/abs/2512.12216) | ✅ 新增，确认 |
| **Agent Learning via Early Experience** | 让 Agent 从自身早期经验中学习，绕开"无可验证奖励环境"与"长程 rollout 低效"两大障碍；**ICML 2026** | 2025-10 | [arXiv:2510.08558](https://arxiv.org/abs/2510.08558) | ✅ 新增，确认 |
| **Skill Self-Play** | 以"技能"为中间层，调和任务多样性与验证可靠性之间的根本矛盾 | 2026-07 | [arXiv:2607.22529](https://arxiv.org/abs/2607.22529) | ✅ 新增，确认 |
| **Multi-Agent Evolve** | 摆脱对人工标注与可验证奖励依赖的自博弈 co-evolution 框架 | 2025-10 | [arXiv:2510.23595](https://arxiv.org/abs/2510.23595) | ✅ 新增，确认 |
| **π-Play** | 多 Agent 自博弈 + 特权自蒸馏（privileged self-distillation），无需外部数据 | 2026-04 | [arXiv:2604.14054](https://arxiv.org/abs/2604.14054) | ✅ 新增，确认 |
| **Explorer-Zero** | 自博弈框架：学习式 proposer 联合生成任务与细粒度可验证奖励 | 2026-10 | [arXiv:2610.19868](https://arxiv.org/abs/2610.19868) | ✅ 新增，确认 |
| **OMAR（One Model, All Roles）** | 单模型同时扮演对话中所有角色，多轮多 Agent 自博弈 RL 学习社会智能 | 2026-02 | [arXiv:2602.03109](https://arxiv.org/abs/2602.03109) | ✅ 新增，确认 |
| **From RLVR to RLSVR** | 任务变换诱导自验证奖励，突破 RLVR 在开放式任务上的局限；**COLM 2026** | 2026-07 | [arXiv:2607.23802](https://arxiv.org/abs/2607.23802) | ✅ 新增，确认 |
| **Go-Browse** | 把数据收集建模为图搜索，实现 Web 环境结构化探索与信息复用 | 2025-06 | [arXiv:2506.03533](https://arxiv.org/abs/2506.03533) | ✅ 新增，确认 |
| **MCP-Flow** | Web Agent 驱动的自动化流水线：大规模 MCP server 发现 + 数据合成 + 训练；**ACL 2026 Main** | 2025-10 | [arXiv:2510.24284](https://arxiv.org/abs/2510.24284) | ✅ 新增，确认 |
| **Hybrid-Gym** | 拆解轨迹细粒度组件，抽取可迁移技能并设计辅助训练任务，让编码 Agent 跨任务泛化 | 2026-02 | [arXiv:2602.16819](https://arxiv.org/abs/2602.16819) | ✅ 新增，确认 |
| **Test-Time Adaptation for LLM Agents via Environment Interaction** | 测试时通过环境交互适配，区分并分别修正"观察格式"语法性误解与"状态转移"语义性误解 | 2025-11 | [arXiv:2511.04847](https://arxiv.org/abs/2511.04847) | ✅ 新增，确认 |
| **Navalia** | Cowork Agent 框架：可验证任务合成 + 长程后训练，面向金融分析等跨文档多步数值推理 | 2026-10 | [arXiv:2610.26887](https://arxiv.org/abs/2610.26887) | ✅ 新增，确认 |
| **EAU（环境-Agent-用户协同进化）** | 把用户模拟器与环境一并纳入训练闭环，共同演化以消除模拟用户的不稳定与验证器缺陷 | 2026-10 | [arXiv:2610.16523](https://arxiv.org/abs/2610.16523) | ✅ 新增，确认 |
| **MIMESIS** | 把"学习用户模拟器"本身作为训练环境：既像真实用户又对 Agent 有学习价值 | 2026-10 | [arXiv:2610.09484](https://arxiv.org/abs/2610.09484) | ✅ 新增，确认 |
| **StableToolBench-MirrorAPI** | 把工具环境建模为 7,000+ 真实 API 的"镜像"，解决工具 API 不可共享导致的评测不可复现 | 2025-03 | [arXiv:2503.20527](https://arxiv.org/abs/2503.20527) | ✅ 新增，确认 |
| **Inducing Programmatic Skills for Agentic Tasks** | 用程序化方式诱导并合成 Agent 任务所需的可复用技能 | 2025-04 | [arXiv:2504.06821](https://arxiv.org/abs/2504.06821) | ✅ 新增，确认 |
| **Environment-Grounded Automated Prompt Optimization for LLM Game Agents** | 用环境回报驱动 LLM 演化式 prompt 优化，并引入行为分析器把回合结果归因到具体规范 | 2026-06 | [arXiv:2606.17838](https://arxiv.org/abs/2606.17838) | ✅ 新增，确认 |
| **FAMA** | 失败感知的元 Agent 框架，针对小参数开源 LLM 在交互式工具环境中的决策级联失败；**ACL 2026 Findings** | 2026-04 | [arXiv:2604.25135](https://arxiv.org/abs/2604.25135) | ✅ 新增，确认 |
| **GPT-Red** | 自博弈规模化自动红队：攻击模型同时对抗一群并行训练的防御 Agent，用于评测并加固前沿模型 | 2026-07 | [arXiv:2607.26115](https://arxiv.org/abs/2607.26115) | ✅ 新增，确认 |
| **Synthetic Data Generation & Multi-Step RL for Reasoning & Tool Use** | 面向多步生成/推理/环境交互的合成数据 + Step-Wise RL 方法 | 2025-04 | [arXiv:2504.04736](https://arxiv.org/abs/2504.04736) | ✅ 新增，确认 |
| **Darwin-Claw** | 环境自适应的经验整合：按环境适配性筛选与合并历史交互，避免原始轨迹无差别注入记忆/技能 | 2026-10 | [arXiv:2610.23574](https://arxiv.org/abs/2610.23574) | ✅ 新增，确认 |
| **SynCo** | 数据合成与自演化 LLM 的多 Agent 协同训练：让合成器随 Agent 能力一同演化 | 2026-10 | [arXiv:2610.11345](https://arxiv.org/abs/2610.11345) | ✅ 新增，确认 |
| **Self-Evolving Coding Agents** | 系统梳理编码 Agent 部署后自演化的框架与挑战 | 2026-08 | [arXiv:2608.03392](https://arxiv.org/abs/2608.03392) | ✅ 新增，确认 |
| **Self-Evolving Software Agents** | BDI-LLM 架构：自主演化目标、推理与可执行代码，突破设计时固定的需求边界 | 2026-04 | [arXiv:2604.27264](https://arxiv.org/abs/2604.27264) | ✅ 新增，确认 |
| **Q-Evolve（in-distribution Optimization）** | 自演化框架解决长程信用分配：利用分布内优化处理延迟奖励 | 2026-06，**ICML 2026** | [arXiv:2606.07367](https://arxiv.org/abs/2606.07367) | ✅ 新增，确认 |
| **From Self-Evolving Synthetic Data to Verifiable-Reward RL** | 自演化合成数据到可验证奖励 RL 的后训练路径，面向多轮交互式工具使用 Agent | 2026-01 | [arXiv:2601.22607](https://arxiv.org/abs/2601.22607) | ✅ 新增，确认 |
| **AgentFrontier** | ZPD（最近发展区）引导的数据合成：把「模型无法独立完成、但给引导可掌握」的任务定义为能力前沿，自动流水线合成多学科数据，兼顾持续预训练与后训练 | 2025-10 | [arXiv:2510.24695](https://arxiv.org/abs/2510.24695) | ✅ 新增 |
| **LoopTool** | 闭合「数据生成-模型训练」环：模型感知的自进化数据框架，按当前模型弱点自适应生成数据并剔除噪声标签，替代静态两阶段流水线 | 2025-11 | [arXiv:2511.09148](https://arxiv.org/abs/2511.09148) | ✅ 新增 |
| **FunReason-MT** | 面向真实多轮工具调用的数据合成方案：针对随机环境采样与多 Agent 角色扮演在真实环境中质量不足的问题，用更可控的合成流程产出高质量多轮 function-calling 数据 | 2025-10 | [arXiv:2510.24645](https://arxiv.org/abs/2510.24645) | ✅ 新增 |
| **RAGShaper** | 自动化合成 Agentic RAG 训练数据：刻意注入噪声、检索失败与扰动，训练 Agent 在真实检索环境下规划、重试与纠错 | 2026-01 | [arXiv:2601.08699](https://arxiv.org/abs/2601.08699) | ✅ 新增 |
| **MATRIX (Multi-Agent Simulation)** | 多 Agent 模拟器自动生成多样化文本场景，覆盖广泛真实人类需求，用于合成高质量指令微调数据，规避隐私、稀缺与标注成本 | 2024-10 | [arXiv:2410.14251](https://arxiv.org/abs/2410.14251) | ✅ 新增 |
| **Matrix (P2P Multi-Agent Data Synthesis)** | 去中心化的点对点多 Agent 合成数据框架：多专长 Agent 协作产出更高质量、更多样、结构更丰富的合成数据，避免中心编排器的扩展瓶颈与领域硬编码 | 2025-11 | [arXiv:2511.21686](https://arxiv.org/abs/2511.21686) | ✅ 新增 |
| **Multi-Agent Sampling** | 用树搜索驱动的多 Agent 协作扩展推理算力来合成数据，研究「数据合成」侧的推理扩展律 | 2024-12 | [arXiv:2412.17061](https://arxiv.org/abs/2412.17061) | ✅ 新增 |
| **ProductResearch** | 用多 Agent 合成轨迹蒸馏训练电商 deep research Agent：多个专长 Agent 协作生成并筛选长程研究轨迹 | 2026-02 | [arXiv:2602.23716](https://arxiv.org/abs/2602.23716) | ✅ 新增 |
| **ReAct** | 推理与行动交替的范式奠基：「思考—行动—观测」循环让模型在环境中迭代决策，是后续几乎所有工具型 Agent 交互轨迹的原型 | 2022-10 | [arXiv:2210.03629](https://arxiv.org/abs/2210.03629) | ✅ 新增 |
| **Inner Monologue** | 闭环语言反馈的具身规划：把环境成功/失败反馈转成自然语言「内心独白」，据此在线修正计划 | 2022-07 | [arXiv:2207.05608](https://arxiv.org/abs/2207.05608) | ✅ 新增 |
| **Reflexion** | 语言化强化学习：把失败轨迹转成文字反思存入记忆，下次尝试据此改进，是「用环境反馈迭代」的经典范式 | 2023-03 | [arXiv:2303.11366](https://arxiv.org/abs/2303.11366) | ✅ 新增 |
| **Language Models as Zero-Shot Planners** | 提取可执行知识用于具身任务：把长程指令分解为可执行步骤序列，无需示范数据即可规划 | 2022-01 | [arXiv:2201.07207](https://arxiv.org/abs/2201.07207) | ✅ 新增 |

---

## 四、Web / GUI 环境合成

| 论文/框架 | 核心贡献 | 时间/出处 | 链接 | 验证状态 |
|---|---|---|---|---|
| **WebArena-Infinity** | 多 Agent 流水线（coding + browser-use agents）从静态 artifact 生成可验证 Web 环境；10 环境 / 1,260 任务 / 2,070 轨迹 | 2026 | [GitHub](https://github.com/web-arena-x/webarena-infinity) | ✅ 确认 |
| **ScaleWoB** | 高保真跨平台 GUI 交互环境合成；可验证奖励，低资源开销 | 2026-05 | [arXiv:2605.25160](https://arxiv.org/abs/2605.25160) | ✅ 确认 |
| **GUI-Genesis** | 从真实应用重建轻量 Web 环境；可验证奖励，GUI Agent 后训练 | 2026 | [arXiv:2602.14093](https://arxiv.org/abs/2602.14093) | ✅ 确认 |
| **Weblica** | 可复现可扩展交互式 Web 环境框架；面向视觉 Web Agent 训练 | 2026-05 | [arXiv:2605.06761](https://arxiv.org/abs/2605.06761) | ✅ 确认 |
| **ScaleCUA / VeriGen** | 可验证任务合成 + 高效在线 RL 扩展计算机使用 Agent | 2026-07 | [arXiv:2607.11185](https://arxiv.org/abs/2607.11185) | ✅ 确认 |
| **FaraGen (Fara-7B)** | 基于高频网站生成多步 Web 任务数据系统 | 2025-11，Microsoft | [arXiv:2511.19663](https://arxiv.org/abs/2511.19663) | ✅ 确认 |
| **FaraGen1.5 (Fara-1.5)** | 环境 + 求解器 + 验证器三组件，可扩展 CUA 数据管线 | 2026-06 | [arXiv:2606.20785](https://arxiv.org/abs/2606.20785) | ✅ 确认 |
| **OS-Genesis** | 反向任务合成：先探索再构造任务，产出 GUI Agent 轨迹 | 2024-12，**ACL 2025** | [arXiv:2412.19723](https://arxiv.org/abs/2412.19723) | ✅ 确认 |
| **HATS** | 难度感知轨迹合成；适配 AndroidWorld / WebArena | **CVPR 2026** | [arXiv:2603.12138](https://arxiv.org/abs/2603.12138) | ✅ 确认 |
| **WebGym** | 迄今最大的开源真实视觉 Web Agent 训练环境；近 30 万任务 + rubric 评测，覆盖真实网站与难度分层；用自身 rollout 做简单 RL 配方 | 2026-01 | [arXiv:2601.02439](https://arxiv.org/abs/2601.02439) | ✅ 新增，确认 |
| **WEBSERV** | 全栈 RL-ready Web 环境：解决服务端 Docker 资源过重与浏览器端观测噪声 / 动作不可靠两大痛点 | 2025-10 | [arXiv:2510.16252](https://arxiv.org/abs/2510.16252) | ✅ 新增，确认 |
| **WebHarbor** | 153 个可执行、docker 化的真实网站重建环境，保真还原视觉界面、内容与功能流程 | 2026-11 | [arXiv:2611.03634](https://arxiv.org/abs/2611.03634) | ✅ 新增，确认 |
| **Training Needs Trustworthy Worlds** | 构造可执行、可审计、以后端状态为锚的合成 Web 环境；每个生成网站被表示为页面/导航链接/数据库记录的结构化脚手架 | 2026-08 | [arXiv:2608.21898](https://arxiv.org/abs/2608.21898) | ✅ 新增，确认 |
| **Learning Simple Test-Time Environments for LLM Web Agents** | 提出 Agent 可在测试时学习简单环境观测，化解"多个简单环境的组合泛化"落差 | 2026-08 | [arXiv:2608.29305](https://arxiv.org/abs/2608.29305) | ✅ 新增，确认 |
| **Build the web for agents, not agents for the web** | 论证人机界面与 LLM 能力之间的根本错配，主张"为 Agent 而建 Web" | 2025-06 | [arXiv:2506.10953](https://arxiv.org/abs/2506.10953) | ✅ 新增，确认 |
| **Ego2Web** | 以第一视角视频为基准的 Web Agent 评测，衔接物理环境感知与线上执行；**CVPR 2026** | 2026-03 | [arXiv:2603.22529](https://arxiv.org/abs/2603.22529) | ✅ 新增，确认 |
| **MAI-Gym** | 开箱即用的 GUI Agent 一体化平台：统一评测、数据采集与跨移动端/计算机端的在线 RL 训练 | 2026-10 | [arXiv:2610.20939](https://arxiv.org/abs/2610.20939) | ✅ 新增，确认 |
| **VEM（Value Environment Model）** | 免环境 RL 框架：把价值估计与策略优化解耦，缓解交互成本与分布偏移 | 2025-02 | [arXiv:2502.18906](https://arxiv.org/abs/2502.18906) | ✅ 新增，确认 |
| **CUA-Universe** | 面向混合 GUI + CLI Agent 的可扩展动态环境，支持两种模态在同一应用状态上协同 | 2026-09 | [arXiv:2609.05374](https://arxiv.org/abs/2609.05374) | ✅ 新增，确认 |
| **Recovering Policy-Induced Errors (GUI-RobustEval + RoTS)** | 1,216 个可执行用例度量 GUI Agent 的错误恢复能力；Robustness-driven Trajectory Synthesis 产出 800K 高质量轨迹；**ICML 2026 Spotlight** | 2026-05 | [arXiv:2605.29447](https://arxiv.org/abs/2605.29447) | ✅ 新增，确认 |
| **SEE** | 结构感知"探索-利用"两阶段长程 GUI 轨迹合成，覆盖率高、可发现稀有状态转移；**ACM MM 2026 Oral** | 2026-07 | [arXiv:2607.18046](https://arxiv.org/abs/2607.18046) | ✅ 新增，确认 |
| **GSAR** | 目标状态锚定奖励（Goal-State-Anchor Reward）+ 自演化数据合成；**EMNLP 2026 Main** | 2026-08 | [arXiv:2608.22847](https://arxiv.org/abs/2608.22847) | ✅ 新增，确认 |
| **MobileGUI-RL** | 在在线环境中做 RL 训练移动 GUI Agent，克服离线轨迹的过拟合与模板依赖 | 2025-07 | [arXiv:2507.05720](https://arxiv.org/abs/2507.05720) | ✅ 新增，确认 |
| **CRAFT-GUI** | 课程强化（curriculum-reinforced）GUI 任务训练，显式建模任务难度差异 | 2025-08 | [arXiv:2508.11360](https://arxiv.org/abs/2508.11360) | ✅ 新增，确认 |
| **MobileWorld** | MCP 增强 + Agent-用户交互的移动 Agent 基准，针对 AndroidWorld 饱和与场景缺失 | 2025-12 | [arXiv:2512.19432](https://arxiv.org/abs/2512.19432) | ✅ 新增，确认 |
| **OSWorld-MCP** | 首个公平评估 CUA 工具调用（MCP）能力的基准，与纯 GUI 交互评测对齐 | 2025-10 | [arXiv:2510.24563](https://arxiv.org/abs/2510.24563) | ✅ 新增，确认 |
| **GUI-CC** | 评测 GUI 世界模型作为"多步 Agent 环境"（而非孤立 next-screen 预测器）的上下文一致性；**EMNLP 2026 Findings** | 2026-09 | [arXiv:2609.00048](https://arxiv.org/abs/2609.00048) | ✅ 新增，确认 |
| **Benchmarking and Improving GUI Agents in High-Dynamic Environments** | 面向高动态（快变化）界面的 GUI Agent 基准与改进方法 | 2026-04 | [arXiv:2604.25380](https://arxiv.org/abs/2604.25380) | ✅ 新增，确认 |
| **WebChoreArena** | 面向繁琐、认知负担高的真实 Web 任务评测；**COLM 2026** | 2025-06 | [arXiv:2506.01952](https://arxiv.org/abs/2506.01952) | ✅ 新增，确认 |
| **STAGE-Claw** | 状态化（state-based）的自动化 Agent 基准，面向真实场景 | 2026-06 | [arXiv:2606.10394](https://arxiv.org/abs/2606.10394) | ✅ 新增，确认 |
| **E-Bench** | 真实产品场景下的多步工具使用 Agent 基准 | 2026-07 | [arXiv:2607.23722](https://arxiv.org/abs/2607.23722) | ✅ 新增，确认 |
| **ViMo** | 生成式视觉 GUI 世界模型：预测下一 GUI 观测，提升长程规划 | 2025-04 | [arXiv:2504.13936](https://arxiv.org/abs/2504.13936) | ✅ 新增，确认 |
| **Code2World** | 通过可渲染代码生成模拟下一 UI 状态的 GUI 世界模型（代码生成路线，兼顾视觉保真与结构可控） | 2026-02 | [arXiv:2602.09856](https://arxiv.org/abs/2602.09856) | ✅ 新增，确认；原条目仅有 arXiv 搜索链接，已补全编号 |
| **Windows Agent Arena** | 规模化多模态 OS Agent 评测（Windows 环境） | 2024-09 | [arXiv:2409.08264](https://arxiv.org/abs/2409.08264) | ✅ 新增，确认 |
| **macOSWorld** | 多语言交互式 GUI Agent 基准（macOS） | 2025-06 | [arXiv:2506.04135](https://arxiv.org/abs/2506.04135) | ✅ 新增，确认 |
| **MacArena** | 在线 macOS 环境上的 CUA 评测 | 2026-06 | [arXiv:2606.06560](https://arxiv.org/abs/2606.06560) | ✅ 新增，确认 |
| **MacAgentBench** | 真实 macOS 桌面上的 AI Agent 基准 | 2026-06 | [arXiv:2606.22557](https://arxiv.org/abs/2606.22557) | ✅ 新增，确认 |
| **OSUniverse** | 多模态 GUI 导航基准，强调易用性、可扩展性、用例覆盖与自动验证 | 2025-05 | [arXiv:2505.03570](https://arxiv.org/abs/2505.03570) | ✅ 新增，确认 |
| **MMBench-GUI** | 分层多平台 GUI Agent 评测框架 | 2025-07 | [arXiv:2507.19478](https://arxiv.org/abs/2507.19478) | ✅ 新增，确认 |
| **BEARCUBS** | 计算机使用 Web Agent 基准 | 2025-03 | [arXiv:2503.07919](https://arxiv.org/abs/2503.07919) | ✅ 新增，确认 |
| **VisualWebArena** | 现实视觉 Web 任务上的多模态 Agent 评测；**ACL 2024** | 2024-01 | [arXiv:2401.13649](https://arxiv.org/abs/2401.13649) | ✅ 新增，确认 |
| **AndroidWorld** | 动态基准测试环境，支撑可复现的自主 Agent 评测 | 2024-05 | [arXiv:2405.14573](https://arxiv.org/abs/2405.14573) | ✅ 新增，确认 |
| **WebFactory** | 全自动闭环 RL 管线，把 LLM 的潜在知识「压缩」为接地 Web Agent 行为；不追求数据量，而是可复现的合成网站环境 + 闭环训练，摆脱不安全不可复现的实时网页交互与昂贵人工环境 | 2026-03 | [arXiv:2603.05044](https://arxiv.org/abs/2603.05044) | ✅ 新增 |
| **OpenMobile** | 开源移动 Agent 框架：任务指令合成 + 轨迹合成两条流水线，弥补领先移动 Agent 训练数据与配方不公开的缺口 | 2026-04 | [arXiv:2604.15093](https://arxiv.org/abs/2604.15093) | ✅ 新增 |
| **OpenMobile-2** | MobileGym++ 含 35 个功能丰富的商业风格应用（支持跨应用工作流、可重置与验证），加上 Android 模拟器新配置应用共 110+ 应用；配套开源大规模训练数据与 app-native 工具 | 2026-10 | [arXiv:2610.14157](https://arxiv.org/abs/2610.14157) | ✅ 新增 |
| **SynWeaver** | 以「网站先验」驱动的任务-轨迹协同合成：先建模网站完整功能面，再提任务，减少凭空想象的任务与轨迹效率低下问题，提升对未见网站的泛化 | 2026-08 | [arXiv:2608.12429](https://arxiv.org/abs/2608.12429) | ✅ 新增 |
| **WebSTAR** | 可扩展的 CUA 数据合成 + 步级过滤：强 CUA 的 rollout 噪声极大（错误/次优动作占比高），因此在步级筛选后再用于训练，替代昂贵人工示范 | 2025-11 | [arXiv:2512.10962](https://arxiv.org/abs/2512.10962) | ✅ 新增 |
| **GUI-ReWalk** | 随机探索 + 意图感知推理的大规模 GUI 轨迹生成：先做随机游走式探索，再据探索结果推理出有意图的任务，兼顾多样性与任务意义覆盖 | 2025-09 | [arXiv:2509.15738](https://arxiv.org/abs/2509.15738) | ✅ 新增 |
| **Explorer** | 探索驱动的 Web 轨迹合成扩展：通过在大规模网站中自主探索来扩展多模态 Web Agent 的轨迹级训练数据 | 2025-02 | [arXiv:2502.11357](https://arxiv.org/abs/2502.11357) | ✅ 新增 |
| **Imagine to Act** | 以「图像编辑世界模型」做高保真 GUI 数据合成：在像素级保留图标、布局等视觉细节（而非文本描述或 HTML 渲染），生成可扩展的视觉-动作轨迹 | 2026-10 | [arXiv:2610.05861](https://arxiv.org/abs/2610.05861) | ✅ 新增 |
| **Echoverse** | 深层、可演化的 CUA 训练环境：指出批量生成环境后瓶颈已从「数量」转向「每个环境内部有什么」，收益取决于行为深度、是否命中 Agent 真实失败点、以及可重置演化能力 | 2026-07 | [arXiv:2607.28074](https://arxiv.org/abs/2607.28074) | ✅ 新增 |
| **PhoneWorld** | 由真实 App 轨迹反推「可运行、可重置、可验证」的 Android 环境：从观测页面、状态转移与状态变更操作中归纳使用权重交互骨架 | 2026-05 | [arXiv:2605.29486](https://arxiv.org/abs/2605.29486) | ✅ 新增 |
| **WebAnything** | 从任意真实 URL 全自动重建「来源接地」的可复用 Web 环境：无需逐站工程化镜像，也不像纯生成式构建那样偏离真实网站 | 2026-10 | [arXiv:2610.37786](https://arxiv.org/abs/2610.37786) | ✅ 新增 |
| **UI-Mate** | 开放权重基础 GUI Agent：环境接地训练栈 + 上下文示范学习，用可扩展合成示范缓解训练数据稀缺、标注偏差与指令歧义 | 2026-08 | [arXiv:2608.15930](https://arxiv.org/abs/2608.15930) | ✅ 新增 |
| **Agent-as-Annotators** | 以「标注角色」类比组织合成轨迹生成：用 Task Designer / Annotator / Supervisor 三个模块化 LLM 组件替代人工标注角色；Gemini 3 Pro 作教师生成 3,000 条轨迹，纯 SFT 9B 学生 | 2026-04 | [arXiv:2604.07776](https://arxiv.org/abs/2604.07776) | ✅ 新增 |
| **WebShop** | 可扩展的真实 Web 交互环境：118 万真实商品、约 1.18M 条众包指令，带 grounded 语言理解与多步购买决策，是 Web Agent 环境的早期标杆 | 2022-07 | [arXiv:2207.01206](https://arxiv.org/abs/2207.01206) | ✅ 新增 |
| **Mind2Web** | 首个通用 Web Agent 数据集：跨 137 个真实网站、2,350 个任务，覆盖跨域泛化与跨站操作 | 2023-06 | [arXiv:2306.06070](https://arxiv.org/abs/2306.06070) | ✅ 新增 |
| **WebVoyager** | 端到端多模态 Web Agent：直接操作真实在线网站，用 GPT-4V 做任务成功判定，避免离线快照与真实网站的偏差 | 2024-01 | [arXiv:2401.13919](https://arxiv.org/abs/2401.13919) | ✅ 新增 |

---

## 五、终端 / 编码环境合成

| 论文/框架 | 核心贡献 | 时间/出处 | 链接 | 验证状态 |
|---|---|---|---|---|
| **Terminal-Bench 2.0** | 89 个 CLI 任务；每个任务含独特环境 + 人工解 + 综合测试；前沿模型得分 <65% | 2026-01，**ICLR 2026** | [arXiv:2601.11868](https://arxiv.org/abs/2601.11868) | ✅ 确认 |
| **CLI-Universe** | 可验证任务合成引擎；6K 轨迹；Qwen3-32B 在 TB2 得分 33.4% | 2026-06，南大/StepFun/上海 AI Lab | [arXiv:2606.22883](https://arxiv.org/abs/2606.22883) | ✅ 确认 |
| **SETA** | SETA-Synth + SETA-Evol 双流水线；SETA-Env 含 4,500+ 环境；GRPO 训练 Qwen3-8B 在 TB 2.0 达 12% pass rate | 2026-07 | [arXiv:2607.10891](https://arxiv.org/abs/2607.10891) | ✅ 确认 |
| **TerminalWorld** | 逆向真实终端依赖构建可执行沙箱 + 环境合成 | 2026-05，UCL/南大/腾讯 | [arXiv:2605.22535](https://arxiv.org/abs/2605.22535) | ✅ 确认 |
| **ResearchEnvBench** | 面向科研代码执行环境合成基准；依赖解析、版本对齐、分布式场景 | 2026-03 | [arXiv:2603.06739](https://arxiv.org/abs/2603.06739) | ✅ 确认 |
| **AI Scientist via Synthetic Task Scaling** | 合成 ML 挑战任务，兼容 SWE-Agent；主题采样 + 数据集提案 + 代码生成 | 2026-03 | [arXiv:2603.17216](https://arxiv.org/abs/2603.17216) | ✅ 确认 |
| **SWE-Factory** | 自动 issue-resolve 数据集工厂；SWE-Builder + exit-code 评分 + fail2pass | 2025-06，**FSE 2026** | [arXiv:2506.10954](https://arxiv.org/abs/2506.10954) | ✅ 确认 |
| **SWE-smith** | 任意 Python 仓库生成 SWE-gym；128 repos / 50K 任务实例；SWE-agent-LM-32B 在 SWE-bench Verified 达 40.2% Pass@1 | **NeurIPS 2025 Spotlight** | [arXiv:2504.21798](https://arxiv.org/abs/2504.21798) | ✅ 已补全编号（原为 arXiv 搜索链接） |
| **R2E-Gym / AgentGym** | 程序化环境生成 + 混合验证器；8.7K+ 可执行 SWE 任务；开源 SWE-Agent 权重 | **COLM 2025** | [arXiv:2504.07164](https://arxiv.org/abs/2504.07164) | ✅ 已补全编号（原为 arXiv 搜索链接） |
| **SWE-World** | 无 Docker 框架；学习式代理模型替代物理执行；SWE-bench Verified 上 Qwen2.5-Coder-32B 从 6.2%→52.0%（SFT）/ 55.0%（RL）/ 68.2%（TTS） | 2026-02，人大高瓴 & BOSS 直聘 | [arXiv:2602.03419](https://arxiv.org/abs/2602.03419) | ✅ 确认 |
| **SWE-Universe** | 从 GitHub PR 自动构建可验证 SWE 环境；807,693 个多语言环境；Qwen3-Max-Thinking 在 SWE-Bench Verified 达 75.3% | 2026-02，阿里 Qwen & 浙大 | [arXiv:2602.02361](https://arxiv.org/abs/2602.02361) | ✅ 确认 |
| **daVinci-Env** | 大规模开放 SWE 环境合成 | 2026-03 | [arXiv:2603.13023](https://arxiv.org/abs/2603.13023) | ✅ 确认 |
| **DockSmith** | 规模化可靠编码环境；Dockerfile、测试脚本自动化构建 | 2026-02 | [arXiv:2602.00592](https://arxiv.org/abs/2602.00592) | ✅ 确认 |
| **TerminalTraj** | 从 Docker 化环境生成大规模终端 Agent 轨迹；32K 镜像 / 50,733 条验证轨迹；Qwen2.5-Coder 训练后 TB 1.0 +20%，TB 2.0 +10% | **ICML 2026** | [arXiv:2602.01244](https://arxiv.org/abs/2602.01244) | ✅ 确认 |
| **Terminal-Universe** | 将 Agent 轨迹逆向回放为可复用终端环境；生成 37.3k 个任务充足环境；微调 Qwen3.5-27B 后 TB 2.1 +11.9 分，EvoCode-Bench v2 MT@4 +13.8 分 | 2026-09 | [arXiv:2609.04148](https://arxiv.org/abs/2609.04148) | ✅ 确认 |
| **SWE-Gym** | 首个真实 SWE Agent 训练环境；2,438 个真实 Python 任务实例（含可执行运行时 + 单元测试 + 自然语言任务）；SWE-Bench Verified/Lite 解决率最高 +19%；**ICML 2025** | 2024-12 | [arXiv:2412.21139](https://arxiv.org/abs/2412.21139) | ✅ 新增，确认 |
| **SWE-bench Goes Live!** | 持续更新的 SWE 基准，摆脱"发布即冻结"与纯手工构建实例的局限 | 2025-05 | [arXiv:2505.23419](https://arxiv.org/abs/2505.23419) | ✅ 新增，确认 |
| **SWE-rebench** | 自动化任务收集与去污染评测流水线，持续提供真实 SWE 场景训练数据 | 2025-05 | [arXiv:2505.20411](https://arxiv.org/abs/2505.20411) | ✅ 新增，确认 |
| **SWE-rebench V2** | 语言无关的 SWE 任务规模化收集，覆盖多语言生态；**ICML 2026** | 2026-02 | [arXiv:2602.23866](https://arxiv.org/abs/2602.23866) | ✅ 新增，确认 |
| **SWE-Bench Pro Verified** | 面向 SWE Agent 的可靠基准 | 2026-09 | [arXiv:2609.08149](https://arxiv.org/abs/2609.08149) | ✅ 新增，确认 |
| **Reproducibility of Build Environments through Space and Time** | 系统研究构建环境在空间与时间维度上的可复现性；**ICSE 2026** | 2024-02 | [arXiv:2402.00424](https://arxiv.org/abs/2402.00424) | ✅ 新增，确认 |
| **Repo2Run** | 自动化为代码仓库构建可执行环境，规模化提升可执行代码数据供给 | 2025-02 | [arXiv:2502.13681](https://arxiv.org/abs/2502.13681) | ✅ 新增，确认 |
| **RepoST** | 以沙箱测试隔离目标函数及依赖，降低外部依赖复杂度，实现仓库级环境可扩展构建 | 2025-03 | [arXiv:2503.07358](https://arxiv.org/abs/2503.07358) | ✅ 新增，确认 |
| **EnvBench** | 自动环境搭建（environment setup）基准；**ICLR 2025 DL4Code Workshop** | 2025-03 | [arXiv:2503.14443](https://arxiv.org/abs/2503.14443) | ✅ 新增，确认 |
| **HerAgent** | 用层次化测试金字塔重估环境部署成功，避免"依赖装上了即算成功"的弱信号 | 2026-02 | [arXiv:2602.07871](https://arxiv.org/abs/2602.07871) | ✅ 新增，确认 |
| **Multi-Docker-Eval** | 40 个真实仓库 / 9 种语言的自动环境构建基准，同时衡量可执行状态达成与效率 | 2025-12 | [arXiv:2512.06915](https://arxiv.org/abs/2512.06915) | ✅ 新增，确认 |
| **Enconda-bench（环境配置过程级评测）** | 过程级轨迹评估，定位环境配置在规划/感知/执行哪一环失败 | 2025-10 | [arXiv:2510.25694](https://arxiv.org/abs/2510.25694) | ✅ 新增，确认 |
| **SWE-MiniSandbox** | 免容器（container-free）RL 训练 SWE Agent，规避按任务构建镜像的存储与权限开销 | 2026-02 | [arXiv:2602.11210](https://arxiv.org/abs/2602.11210) | ✅ 新增，确认 |
| **Dockerless** | 免环境、不执行代码的补丁验证器，降低训练与评测的环境搭建成本 | 2026-06 | [arXiv:2606.28436](https://arxiv.org/abs/2606.28436) | ✅ 新增，确认 |
| **Agent-RLVR** | 通过指导 + 环境奖励训练 SWE Agent，缓解 Agentic 环境下奖励稀疏问题 | 2025-06 | [arXiv:2506.11425](https://arxiv.org/abs/2506.11425) | ✅ 新增，确认 |
| **SWE-PRM（When Agents go Astray）** | 推理期过程奖励模型，在执行过程中主动纠偏，减少冗余探索、循环与不终止问题 | 2025-09 | [arXiv:2509.02360](https://arxiv.org/abs/2509.02360) | ✅ 新增，确认 |
| **Graph-Guided Repository Environment Construction** | 图引导的仓库环境构建：从仓库各构件中碎片化的执行需求推导依赖关系 | 2026-09 | [arXiv:2609.33429](https://arxiv.org/abs/2609.33429) | ✅ 新增，确认 |
| **Change2Task** | 从仓库变更反推可执行任务与环境：在当前代码上撤销已合并 PR 的效果即可重建同一任务 | 2026-07 | [arXiv:2607.28591](https://arxiv.org/abs/2607.28591) | ✅ 新增，确认 |
| **For Coding Agents, the Repository Matters** | 揭示编码 Agent 共享基础设施带来的协同攻击风险（大规模评测中约 1,200 个 Agent 经共享包服务器串通攻击） | 2026-06 | [arXiv:2606.28235](https://arxiv.org/abs/2606.28235) | ✅ 新增，确认 |
| **SWE-Search** | 蒙特卡洛树搜索 + 迭代精化增强软件 Agent，支持回溯与多解探索 | 2024-10 | [arXiv:2410.20285](https://arxiv.org/abs/2410.20285) | ✅ 新增，确认 |
| **SWT-Bench** | 用 Code Agent 把用户 issue 形式化为测试用例以验证真实缺陷修复 | 2024-06 | [arXiv:2406.12952](https://arxiv.org/abs/2406.12952) | ✅ 新增，确认 |
| **TDD-Bench Verified** | 评测 LLM 能否在 issue 被修复之前生成 fail-to-pass 测试（TDD 场景） | 2024-12 | [arXiv:2412.02883](https://arxiv.org/abs/2412.02883) | ✅ 新增，确认 |
| **Otter** | 从 issue 生成测试以验证 SWE 补丁，支持 TDD 与补丁验证两类用例 | 2025-02 | [arXiv:2502.05368](https://arxiv.org/abs/2502.05368) | ✅ 新增，确认 |
| **Issue2Test** | 从 issue 报告自动生成可复现测试用例，指导补丁搜索与意图校验 | 2025-03 | [arXiv:2503.16320](https://arxiv.org/abs/2503.16320) | ✅ 新增，确认 |
| **Beyond pip install** | 评测 LLM Agent 自动安装 Python 项目（依赖解析与环境搭建）的能力 | 2024-12 | [arXiv:2412.06294](https://arxiv.org/abs/2412.06294) | ✅ 新增，确认 |
| **You Name It, I Run It** | 用 LLM Agent 执行任意项目的测试套件，跨越语言/构建系统/测试框架差异；**ISSTA 2025** | 2024-12 | [arXiv:2412.10133](https://arxiv.org/abs/2412.10133) | ✅ 新增，确认 |
| **debug-gym** | 轻量文本化交互式调试环境，让 Agent 主动探索代码库获取任务相关信息 | 2025-03 | [arXiv:2503.21557](https://arxiv.org/abs/2503.21557) | ✅ 新增，确认 |
| **UTBoost** | 用增强测试严格评估 SWE-Bench 上的编码 Agent，防止"过测试但未解决问题"；**ACL 2025** | 2025-06 | [arXiv:2506.09289](https://arxiv.org/abs/2506.09289) | ✅ 新增，确认 |
| **ProjectEval** | 项目级代码生成的编程 Agent 自动评测 | 2025-03 | [arXiv:2503.07010](https://arxiv.org/abs/2503.07010) | ✅ 新增，确认 |
| **GitTaskBench** | 评测代码 Agent 利用大型代码仓库解决真实任务的能力；54 个任务 / 7 种模态 / 7 个领域 | 2025-08 | [arXiv:2508.18993](https://arxiv.org/abs/2508.18993) | ✅ 新增，确认 |
| **MEnvAgent** | 多语言自动化环境构建：Planning-Execution-Verification 三角色多 Agent 架构，支持多语言可执行环境与可验证任务实例的规模化生成，缓解 SWE 可验证数据集稀缺 | 2026-01 | [arXiv:2601.22859](https://arxiv.org/abs/2601.22859) | ✅ 新增 |
| **TermiGen** | 高保真终端环境 + 稳健轨迹合成：既解决「仓库合成环境不够多样/可扩展、LLM 轨迹易幻觉」两个瓶颈，又刻意保留小模型常见的简单错误以缩小训练-推理分布差 | 2026-02 | [arXiv:2602.07274](https://arxiv.org/abs/2602.07274) | ✅ 新增 |
| **LiteCoder-Terminal** | 零依赖终端环境合成流水线（LiteCoder-Terminal-Gen）：不靠抓取外部仓库，自主生成可执行可验证终端任务，可控域多样性与能力缺口定向 | 2026-05 | [arXiv:2605.29559](https://arxiv.org/abs/2605.29559) | ✅ 新增 |
| **FACET** | 终端任务合成中保持「来源意图」与「可执行状态」一致：任务四件套（指令、初始化环境、参考解、可执行验证器）若假设不一致就会变成不可解或错评，FACET 从源头约束一致性 | 2026-08 | [arXiv:2608.18580](https://arxiv.org/abs/2608.18580) | ✅ 新增 |
| **RST (Recursive Synthetic Terminal Tasks)** | 递归可验证的长程终端任务合成：从已验证种子任务出发，扩展参考解、同步重定位验证器与指令，避免直接 LLM 生成造成四件套不一致 | 2026-08 | [arXiv:2608.05466](https://arxiv.org/abs/2608.05466) | ✅ 新增 |
| **Depth Measurement for Terminal Tasks** | 质疑现有长程终端基准的「深度」度量：轮数多反映模型习惯而非任务需求，LLM 生成的难度标签也几乎不反映真实通过率；提出以「工作量」重新刻画任务深度 | 2026-11 | [arXiv:2611.01927](https://arxiv.org/abs/2611.01927) | ✅ 新增 |
| **Terminal-Task-Gen** | 轻量级终端合成任务生成管线（种子式 + 技能式两种构建方式），并系统公开终端 Agent 的数据工程与训练策略分析 | 2026-02 | [arXiv:2602.21193](https://arxiv.org/abs/2602.21193) | ✅ 新增 |
| **When Terminal-Agent Training Stalls** | 拆解「可跑通 Docker 镜像 + 可执行测试」并不等于奖励可信：把生成与评测失败模式分解为不可解、不可验证、奖励不可归因等类别 | 2026-10 | [arXiv:2610.02405](https://arxiv.org/abs/2610.02405) | ✅ 新增 |
| **WorkBorne** | 从真实「产物状态迁移」中发现 Agentic 任务：既避免指令导向方法造出低保真环境，也避免资源导向方法把真实产物降级为静态输入而任务过于琐碎 | 2026-10 | [arXiv:2610.14915](https://arxiv.org/abs/2610.14915) | ✅ 新增 |
| **SWE-Bench++** | 从开源 GitHub 项目自动生成仓库级编码任务：采集真实 PR 覆盖 bug 修复与功能请求，跨多语言，替代人工策划的静态基准 | 2025-12 | [arXiv:2512.17419](https://arxiv.org/abs/2512.17419) | ✅ 新增 |
| **RepoForge** | 端到端自主 SWE 数据管线：生成、评测、训练一体化，产出 7,304 个可执行环境；RepoForge-8B-Agent 在 SWE-Bench-Verified 达 17.4%，为 ≤8B 非思考模型 SOTA | 2025-08 | [arXiv:2508.01550](https://arxiv.org/abs/2508.01550) | ✅ 新增 |
| **daVinci-Dev** | 面向 SWE 的「Agent 原生 mid-training」：在模拟真实 Agent 工作流的大规模数据上做中期训练，填补后训练之外的空白 | 2026-01 | [arXiv:2601.18418](https://arxiv.org/abs/2601.18418) | ✅ 新增 |
| **RAT (RunAnyThing)** | 全自动仓库环境配置：不依赖预定义产物、不限定语言，为任意真实仓库自动配置可执行环境，解除代码 Agent 的环境配置瓶颈 | 2026-04 | [arXiv:2604.23190](https://arxiv.org/abs/2604.23190) | ✅ 新增 |
| **EnvAgent** | 多 Agent 自动构建云端科研环境：仓库对操作系统、工具链、依赖与构建流程的要求常是异构且不完整的，EnvAgent 负责合成、构建并验证 | 2026-10 | [arXiv:2611.23258](https://arxiv.org/abs/2611.23258) | ✅ 新增 |
| **Counterfactual Rollout Replay (CRR)** | 把「可 fork 的执行环境」当作免费过程奖励：选取关键决策点、恢复状态、采样替代动作并前向 rollout，得到步级回报对比，缓解 SWE 的 outcome-only 信号稀疏 | 2026-09 | [arXiv:2609.33875](https://arxiv.org/abs/2609.33875) | ✅ 新增 |
| **Video2World** | 把「视频→可交互仿真」定义为软件工程任务：Agent 观看具身视频后构建对应仿真环境与机器人行为，评测编码 Agent 能否端到端自动化环境构建 | 2026-10 | [arXiv:2610.04432](https://arxiv.org/abs/2610.04432) | ✅ 新增 |
| **ScienceIDE** | 把科学代码库变成 Agent 可学习环境：碎片化工具链与隐式领域约定是主要障碍，ScienceIDE 将其改写为可执行、可验证的训练环境 | 2026-09 | [arXiv:2609.19134](https://arxiv.org/abs/2609.19134) | ✅ 新增 |
| **SWE-Marathon** | 超长程软件工作基准：要求 Agent 在数小时、百万 token、复杂环境条件下自主持续推进 | 2026-06 | [arXiv:2606.07682](https://arxiv.org/abs/2606.07682) | ✅ 新增 |
| **Arctic-SWE** | 长程 Agent 训练的模型-系统协同设计：公开强 RL 训练所需的配方与基础设施细节 | 2026-10 | [arXiv:2610.24914](https://arxiv.org/abs/2610.24914) | ✅ 新增 |
| **InterCode** | 「代码即动作」的交互式编码框架：Bash / SQL / Python 三类环境，每步执行后返回观测，把编码任务统一为多轮交互 | 2023-06 | [arXiv:2306.14898](https://arxiv.org/abs/2306.14898) | ✅ 新增 |
| **SWE-bench** | 真实 GitHub issue 解决基准：2,294 个 issue-PR 对，要求 agent 在仓库级环境中定位并修复缺陷并通过测试 | 2023-10 | [arXiv:2310.06770](https://arxiv.org/abs/2310.06770) | ✅ 新增 |
| **RepoBench** | 仓库级代码补全基准：要求跨文件检索与依赖理解，评测仓库上下文利用能力 | 2023-06 | [arXiv:2306.03091](https://arxiv.org/abs/2306.03091) | ✅ 新增 |
| **DS-1000** | 数据科学代码生成基准：1,000 个来自真实 StackOverflow 的问题，覆盖 7 个库，需在多解空间中做正确性判定 | 2022-11 | [arXiv:2211.11501](https://arxiv.org/abs/2211.11501) | ✅ 新增 |
| **CodeAct** | 把可执行 Python 作为统一动作空间：合并「代码动作」与「自然语言动作」，让 agent 用一段代码完成多步工具调用与自我纠错 | 2024-02 | [arXiv:2402.01030](https://arxiv.org/abs/2402.01030) | ✅ 新增 |
| **DreamerV3** | 通用世界模型 + RL：在 150+ 任务上用同一套超参掌握多领域控制，说明「世界模型」可作为跨域通用环境表征 | 2023-01 | [arXiv:2301.04104](https://arxiv.org/abs/2301.04104) | ✅ 新增 |
| **IRIS** | 离散 token 世界模型：用 VQ-VAE 编码观测、Transformer 建模动力学，在 Atari 100k 上以极少交互达到强样本效率 | 2022-09 | [arXiv:2209.00588](https://arxiv.org/abs/2209.00588) | ✅ 新增 |

---

## 六、模型基仿真与语言世界模型

| 论文/框架 | 核心贡献 | 时间/出处 | 链接 | 验证状态 |
|---|---|---|---|---|
| **ARE / GAIA2** | Meta Agents Research Environments；可扩展环境创建平台 + 异步基准 GAIA2 | 2025-09，Meta | [arXiv:2509.17158](https://arxiv.org/abs/2509.17158) | ✅ 确认 |
| **Chimera** | 多 Agent 企业威胁仿真；环境 + 角色模拟 | 2025-08，**NDSS 2026** | [arXiv:2508.07745](https://arxiv.org/abs/2508.07745) | ✅ 确认 |
| **WebWorld** | 大规模开放 Web 模拟器；1M+ 真实 Web 交互训练；支持 30+ 步长程模拟；Qwen3-14B 训练后 WebArena +9.2%；推理时搜索作为世界模型超越 GPT-5；跨域泛化到代码、GUI、游戏 | 2026-02，**ICML 2026**，阿里 Qwen | [arXiv:2602.14721](https://arxiv.org/abs/2602.14721) | ✅ 确认 |
| **Code2World** | GUI 世界模型；代码渲染预测下一 UI 状态 | **CVPR 2026**（另有 ICML 2026 版本） | [arXiv:2602.09856](https://arxiv.org/abs/2602.09856) | ✅ 已补全编号（原为 arXiv 搜索链接） |
| **VirtualEnv** | 开源模拟平台；程序化任务生成 + 游戏式机制 | 2026 | [arXiv:2601.07553](https://arxiv.org/abs/2601.07553) | ✅ 确认 |
| **ProPlay** | 程序化世界模型；过程级预演 + 过程图，自演化 LLM Agent | 2026-06 | [arXiv:2606.12780](https://arxiv.org/abs/2606.12780) | ✅ 确认 |
| **EnvACE** | 用"世界排练"替代外部环境交互；策略先发工具调用，再扮演环境生成响应，两角色端到端联合优化；BFCL-v4 / τ²-Bench / VitaBench / FinMCP-Bench 上优于环境扩展基线 | 2026-08 | [arXiv:2608.06197](https://arxiv.org/abs/2608.06197) | ✅ 确认 |
| **Simia** | 证明 LLM 可在无真实 testbed/API 情况下模拟逼真环境反馈；Simia-SFT（数据合成）+ Simia-RL | 2025-11 | [arXiv:2511.01824](https://arxiv.org/abs/2511.01824) | ✅ 新增，确认 |
| **Dyna-Mind** | "替代性试错"学习：从经验中习得模拟能力，补齐推理模型在长程交互任务上的短板 | 2025-10 | [arXiv:2510.09577](https://arxiv.org/abs/2510.09577) | ✅ 新增，确认 |
| **UI-Simulator** | 结构化 UI 状态与转移生成 + 引导式 rollout + 轨迹筛选，规模化合成 UI 训练数据 | 2025-10 | [arXiv:2510.14969](https://arxiv.org/abs/2510.14969) | ✅ 新增，确认 |
| **ViMo** | 生成式视觉 GUI 世界模型，预测下一 GUI 观测以支撑长程规划 | 2025-04 | [arXiv:2504.13936](https://arxiv.org/abs/2504.13936) | ✅ 新增，确认 |
| **DynaWeb** | 模型化 RL：为 Web Agent 学习世界模型，以模拟交互替代昂贵的真实互联网交互 | 2026-01 | [arXiv:2601.22149](https://arxiv.org/abs/2601.22149) | ✅ 新增，确认 |
| **Is Your LLM Secretly a World Model of the Internet?** | 面向 Web Agent 的模型化规划，处理真实 Web 中不可逆动作对回溯搜索的破坏 | 2024-11 | [arXiv:2411.06559](https://arxiv.org/abs/2411.06559) | ✅ 新增，确认 |
| **Reinforcement World Model Learning (RWML)** | 自监督学习动作条件世界模型，用 sim-to-real 差距奖励对齐模拟与真实下一状态；**NeurIPS 2026** | 2026-02 | [arXiv:2602.05842](https://arxiv.org/abs/2602.05842) | ✅ 新增，确认 |
| **Trace2Env（From Traces to Agentic Worlds）** | 学习自由（learning-free）的世界模型 Agent 直接充当环境，支持有状态仿真，替代难以复现的真实系统 | 2026-10 | [arXiv:2610.06100](https://arxiv.org/abs/2610.06100) | ✅ 新增，确认 |
| **Agentic World Modeling without Environment Replica** | 无环境副本情况下用 Agentic 世界建模做测试时扩展，突破并行轨迹必须真实执行的假设 | 2026-10 | [arXiv:2610.40927](https://arxiv.org/abs/2610.40927) | ✅ 新增，确认 |
| **WildAWM（Agent World Model in the Wild）** | 微软研究院等；合成整台"个人电脑"（GUI + MCP + CLI 三种接口）；36 个人物 / 640 个世界状态，平均 17 万条数据库记录；XAI 跨界面任务平均 4.2 子任务 / 3.1 次接口切换；五道质量关卡后 2,551 个草稿仅留 341 题；verifier 与 agent judge 一致率 95%、Cohen's κ=0.90；仅用开源模型训练，8 个 OOD 基准全面提升 | 2026-10 | [arXiv:2610.26828](https://arxiv.org/abs/2610.26828) · [GitHub](https://github.com/MSR-Orchard/WildAWM) · [主页](https://msr-orchard.github.io/WildAWM/) | ✅ 新增，确认 |
| **Genie** | 生成式交互环境（Generative Interactive Environments） | 2024-02 | [arXiv:2402.15391](https://arxiv.org/abs/2402.15391) | ✅ 新增，确认 |
| **Learning Interactive Real-World Simulators** | 交互式真实世界模拟器的学习方法 | 2023-10 | [arXiv:2310.06114](https://arxiv.org/abs/2310.06114) | ✅ 新增，确认 |
| **Posterior Twins** | 企业决策的数字孪生：用后验分布表示"在特定决策下人群的行为分布" | 2026-06 | [arXiv:2606.16415](https://arxiv.org/abs/2606.16415) | ✅ 新增，确认 |
| **GenWorld** | 城市尺度仿真基础设施：建筑级合成城市 + 结构化 Agent-环境接口 + 离线编译为查表策略以支撑大规模 rollout | 2026-06 | [arXiv:2606.27650](https://arxiv.org/abs/2606.27650) | ✅ 新增，确认 |
| **DNative-Twin** | 图原生数字孪生：把已提交的 Agent 决策记录为类型化轨迹并在声明条件下重放其决策机制 | 2026-09 | [arXiv:2609.03787](https://arxiv.org/abs/2609.03787) | ✅ 新增，确认 |
| **TwinLoop** | 仿真在环（simulation-in-the-loop）的数字孪生，支撑在线多 Agent RL | 2026-04 | [arXiv:2604.06610](https://arxiv.org/abs/2604.06610) | ✅ 新增，确认 |
| **EnvGen** | 用 LLM 生成并自适应调整训练环境，降低具身 Agent 的 LLM 调用成本；**COLM 2024** | 2024-03 | [arXiv:2403.12014](https://arxiv.org/abs/2403.12014) | ✅ 新增，确认 |
| **Active Zero** | 自博弈自演化 VLM：通过主动环境探索获取契合当前能力的视觉数据 | 2026-02 | [arXiv:2602.11241](https://arxiv.org/abs/2602.11241) | ✅ 新增，确认 |
| **V-Dreamer** | 从自然语言指令全自动生成开放式、可仿真、可执行的机器人操作环境与专家轨迹 | 2026-03 | [arXiv:2603.18811](https://arxiv.org/abs/2603.18811) | ✅ 新增，确认 |
| **Towards Adaptive Environment Generation for Training Embodied Agents** | 闭环自适应环境生成：把 Agent 当前表现纳入生成过程，避免"多样但无反馈"的低效 | 2026-02 | [arXiv:2602.06366](https://arxiv.org/abs/2602.06366) | ✅ 新增，确认 |
| **Automating the Design of Embodied Agent Architectures** | Agent 架构搜索（AAS）迁移到具身感知 Agent；**CoRL 2026** | 2026-06 | [arXiv:2606.30111](https://arxiv.org/abs/2606.30111) | ✅ 新增，确认 |
| **SR-Platform** | 自然语言驱动的机器人仿真环境合成 Agent 流水线 | 2026-05 | [arXiv:2605.14700](https://arxiv.org/abs/2605.14700) | ✅ 新增，确认 |
| **CityPlanner / UrbanSandbox** | 统一的文件式沙箱环境，用于可执行城市规划这一空间优化问题 | 2026-09 | [arXiv:2609.09578](https://arxiv.org/abs/2609.09578) | ✅ 新增，确认 |
| **Automated Environment Design for Optimal Power Flow** | 用多目标优化 + 超参数优化框架做通用自动化 RL 环境设计；**ACM e-Energy 2025** | 2025-05 | [arXiv:2505.07832](https://arxiv.org/abs/2505.07832) | ✅ 新增，确认 |
| **COLOSSEUM** | 机器人操作泛化评测基准；**RSS 2024** | 2024-02 | [arXiv:2402.08191](https://arxiv.org/abs/2402.08191) | ✅ 新增，确认 |
| **GlobeBench** | 文本世界模型基准：1,632 个任务 / 5 个领域 / 19 种仿真技能，用于规模化环境模拟 | 2026-10 | [arXiv:2610.22708](https://arxiv.org/abs/2610.22708) | ✅ 新增，确认 |
| **World Models of Environment, Agent and Joint Systems** | 按建模通道（环境通道 O→A、Agent 通道 A→O、联合通道）区分世界模型的三种情形 | 2026-07 | [arXiv:2608.20401](https://arxiv.org/abs/2608.20401) | ✅ 新增，确认 |
| **Ask the World Before Acting** | 环境探针机制：在行动前主动校准 Agent 的世界模型，修正交互累积导致的信念过时 | 2026-06 | [arXiv:2606.31422](https://arxiv.org/abs/2606.31422) | ✅ 新增，确认 |
| **General Agents Contain World Models** | 形式化证明：能泛化到多步目标导向任务的 Agent 必须学到环境的预测模型，且该模型可从策略中提取；**ICML 2025** | 2025-06 | [arXiv:2506.01622](https://arxiv.org/abs/2506.01622) | ✅ 新增，确认 |
| **Learning Generative Interactive Environments by Trained Agent Exploration** | 用受训 Agent 的探索替代随机智能体，提升生成式交互环境（Genie 类）的探索效率 | 2024-09 | [arXiv:2409.06445](https://arxiv.org/abs/2409.06445) | ✅ 新增，确认 |
| **EmbodiSkill** | 面向自演化具身 Agent 的技能感知反思，把数字环境中的技能自演化方法迁移到具身场景 | 2026-05 | [arXiv:2605.10332](https://arxiv.org/abs/2605.10332) | ✅ 新增，确认 |
| **Sari Sandbox** | 高保真照片级 3D 零售商店仿真：250+ 交互商品 / 3 种门店配置 / API 控制，支持 VR 与具身 Agent 评测 | 2025-08，**ICCV 2025 Workshop on Retail** | [arXiv:2508.00400](https://arxiv.org/abs/2508.00400) | ✅ 新增，确认 |
| **PatchWorld** | 黑盒环境下用「可执行代码」作为世界模型：只有观测文本、无真值潜状态与转移模型，仍通过无梯度优化把代码归纳为可执行世界模型，供预测与决策 | 2026-05 | [arXiv:2605.30880](https://arxiv.org/abs/2605.30880) | ✅ 新增 |
| **From Word to World** | 系统检验「LLM 能否作为隐式文本世界模型」：在何种条件下 LLM 世界模型能真正提升 Agent 学习效率，而非仅生成看似合理的文本 | 2025-12 | [arXiv:2512.18832](https://arxiv.org/abs/2512.18832) | ✅ 新增 |
| **Do Enterprise Systems Need Learned World Models?** | 企业系统的动力学由租户特定业务逻辑定义且随部署变化，历史转移上训练的世界模型在部署漂移下易脆；因此关键在「上下文」而非参数化学习 | 2026-05 | [arXiv:2605.12178](https://arxiv.org/abs/2605.12178) | ✅ 新增 |
| **Social World Model** | 面向终身社会智能的社会世界模型：把社会交互轨迹统一为结构化表示形成可迭代学习信号，使社会能力可累积而非只做静态评测 | 2026-06 | [arXiv:2606.21315](https://arxiv.org/abs/2606.21315) | ✅ 新增 |
| **Economic World Models** | 面向「智能体经济」的系统蓝图：以异质 Agent、其信念与行动、以及市场与制度机制为内核，构建可生成式推演经济体演化的经济世界模型（EWM） | 2026-08 | [arXiv:2608.06020](https://arxiv.org/abs/2608.06020) | ✅ 新增 |
| **MoWorld** | 强调世界模型的「实用性扩展」：不止参数能力，还要高帧率推理效率；端到端覆盖数据生成、预训练、蒸馏与高效推理 | 2026-07 | [arXiv:2607.06216](https://arxiv.org/abs/2607.06216) | ✅ 新增 |
| **iWorld-Bench** | 交互式世界模型的统一评测基准：提供大规模数据集与统一动作生成框架，系统评测物理交互能力 | 2026-05 | [arXiv:2605.03941](https://arxiv.org/abs/2605.03941) | ✅ 新增 |
| **World Model for Robot Learning (Survey)** | 机器人学习世界模型综述：从架构、功能角色（策略学习、规划、仿真、评测、数据生成）与具身应用三个维度统一碎片化文献 | 2026-04 | [arXiv:2605.00080](https://arxiv.org/abs/2605.00080) | ✅ 新增 |
| **Robotic Video World Models (Survey)** | 机器人视频世界模型综述：讨论其相对物理仿真器的优势、应用场景、挑战与未来方向 | 2026-01 | [arXiv:2601.07823](https://arxiv.org/abs/2601.07823) | ✅ 新增 |
| **The Robot Data Factory** | 提出 Physical AI 的核心科学资源不是「原始机器人数据」而是「机器人经验」——保留感知-动作-后果闭环的接地交互，并据此设计数据工厂 | 2026-09 | [arXiv:2609.16705](https://arxiv.org/abs/2609.16705) | ✅ 新增 |
| **RoboDream** | 组合式世界模型做机器人数据合成：克服现有视频扩散方法只做表观增强、或产生具身幻觉导致物理不可行动作的问题 | 2026-06 | [arXiv:2606.02577](https://arxiv.org/abs/2606.02577) | ✅ 新增 |
| **RoboChemGym** | 协议驱动的生成式化学操作仿真：面向湿实验长程操作，用协议约束生成可执行的长程化学操作演示，缓解真实数据稀缺与安全成本 | 2026-10 | [arXiv:2610.02708](https://arxiv.org/abs/2610.02708) | ✅ 新增 |

---

## 七、任务 / 场景合成

| 论文/框架 | 核心贡献 | 时间/出处 | 链接 | 验证状态 |
|---|---|---|---|---|
| **Graph2Eval** | 知识图谱驱动多模态任务生成；文档理解 + Web 交互；1319 任务 | 2025-10，**CVPR 2026** | [arXiv:2510.00507](https://arxiv.org/abs/2510.00507) | ✅ 确认 |
| **SimpleQA→DeepResearch** | Explorer–Formalizer–Challenger 迭代任务演化；500 个可验证深度研究任务 | 2026-08 | [arXiv:2608.02163](https://arxiv.org/abs/2608.02163) | ✅ 确认 |
| **AgenticDataBench** | 技能聚类 + LLM 任务生成构建数据 Agent 基准 | 2026-07，清华 & 蚂蚁 | [arXiv:2607.01647](https://arxiv.org/abs/2607.01647) | ✅ 确认 |
| **ART** | 医疗 AI Agent 的 Action-based Reasoning 临床任务基准；四阶段流水线；600 个任务；检索接近完美，聚合推理 28–64%，阈值推理 32–38% | 2026-01 | [arXiv:2601.08988](https://arxiv.org/abs/2601.08988) | ✅ 确认 |
| **ACuRL** | 自主课程 RL；环境探索-课程生成-持续适配，零人工数据 | 2026-02，OSU-NLP-Group | [arXiv:2602.10356](https://arxiv.org/abs/2602.10356) | ✅ 确认 |
| **State2State** | 从环境探索状态导出中间训练任务，状态匹配验证 | 2026-08，THUNLP | [arXiv:2608.04934](https://arxiv.org/abs/2608.04934) | ✅ 确认 |
| **SESA** | 自博弈搜索 Agent；出题者-求解者架构，不需要外部题库 | 2026-07 | [arXiv:2607.29468](https://arxiv.org/abs/2607.29468) | ✅ 确认 |
| **Gym-V** | 179 个程序化视觉环境、10 个领域，难度可控 | 2026 | [arXiv:2603.15432](https://arxiv.org/abs/2603.15432) | ✅ 确认 |
| **InternAgentHarness (BOOTCAMPCLI)** | 四层环境定义，自动转换训练范式 Harness | 2025-08 | [arXiv:2508.08636](https://arxiv.org/abs/2508.08636) | ✅ 确认 |
| **RandomWorld（Procedural Environment Generation for Tool-Use Agents）** | 程序化生成交互式工具与组合式工具使用数据，弥补既有合成数据"非交互/非组合"的缺陷；**EMNLP 2025** | 2025-05 | [arXiv:2506.11045](https://arxiv.org/abs/2506.11045) | ✅ 新增，确认 |
| **Doc2Agent** | 从 API 文档可扩展生成工具使用 Agent 与可执行 Python 工具 | 2025-06 | [arXiv:2506.19998](https://arxiv.org/abs/2506.19998) | ✅ 新增，确认 |
| **Reasoning Gym** | 100+ 推理环境数据生成器与验证器，复杂度可调、可无限生成；**NeurIPS 2025 Spotlight** | 2025-05 | [arXiv:2505.24760](https://arxiv.org/abs/2505.24760) | ✅ 新增，确认 |
| **Depth Before Breadth** | 逆向-正向课程 + 优势分解；定义"策略诱导能力域"，把长程信用分配问题转化为短程 | 2026-11 | [arXiv:2611.24697](https://arxiv.org/abs/2611.24697) | ✅ 新增，确认 |
| **Curriculum Guided Massive Multi Agent System Solving** | 课程引导的大规模多 Agent 系统求解，面向鲁棒长程任务 | 2025-12 | [arXiv:2512.08545](https://arxiv.org/abs/2512.08545) | ✅ 新增，确认 |
| **SearchMaster** | 有依据（grounded）且受控（regulated）的搜索 Agent 自博弈 | 2026-08 | [arXiv:2608.01822](https://arxiv.org/abs/2608.01822) | ✅ 新增，确认 |
| **Vision-DeepResearch Benchmark** | 重新审视多模态模型的视觉 + 文本联合检索，修复"视觉检索答案被文本线索泄漏"的问题 | 2026-02 | [arXiv:2602.02185](https://arxiv.org/abs/2602.02185) | ✅ 新增，确认 |
| **API-BLEND** | 用于训练与评测 API LLM 的综合语料库；**ACL 2024 Main** | 2024-02 | [arXiv:2402.15491](https://arxiv.org/abs/2402.15491) | ✅ 新增，确认 |
| **A Framework for Testing and Adapting REST APIs as LLM Tools** | 把 REST API 测试并适配为 LLM 工具的方法框架 | 2025-04 | [arXiv:2504.15546](https://arxiv.org/abs/2504.15546) | ✅ 新增，确认 |
| **AgentDrive** | 通过 LLM Prompt 生成 JSON 驾驶场景；30 万个驾驶场景 | 2026-01 | [arXiv:2601.16964](https://arxiv.org/abs/2601.16964) | ✅ 确认 |
| **EigenData** | 自演化多 Agent 平台，覆盖函数调用数据合成、审计与修复的全生命周期 | 2026-03 | [arXiv:2603.05553](https://arxiv.org/abs/2603.05553) | ✅ 新增，确认 |
| **Scaling Synthetic Task Generation for Agents via Exploration** | 通过探索式扩展合成任务生成，产出多样、可行且可验证的 Agent 任务 | 2025-09 | [arXiv:2509.25047](https://arxiv.org/abs/2509.25047) | ✅ 新增，确认 |
| **DIVE** | 「先执行、后反推」的多样性任务合成：先在真实工具上执行多样操作得到轨迹，再严格由轨迹反推任务，从构造上保证接地；沿工具池覆盖与单任务工具集多样性两个可控轴扩展 | 2026-03 | [arXiv:2603.11076](https://arxiv.org/abs/2603.11076) | ✅ 新增 |
| **Synthesizing Agentic Data for Web Agents (Progressive Difficulty)** | 渐进加难的 Web deep research 数据合成：由易到难逐级提升长程在线工具交互任务的难度 | 2025-10 | [arXiv:2510.13913](https://arxiv.org/abs/2510.13913) | ✅ 新增 |
| **Meta-Task** | 把「终端任务合成」本身变成终端任务：让 Agent 在终端里完成任务合成这一工作，从而规模化产出可验证终端任务与轨迹 | 2026-07 | [arXiv:2607.27929](https://arxiv.org/abs/2607.27929) | ✅ 新增 |
| **NexForge** | 需求驱动的任务合成，摆脱「substrate-bound」：不与预定义工具绑定，而以需求规格为起点生成可执行任务，扩展 Agent 训练数据 | 2026-07 | [arXiv:2607.14186](https://arxiv.org/abs/2607.14186) | ✅ 新增 |

---

## 八、MCP 工具环境与生态

| 论文/框架 | 核心贡献 | 时间/出处 | 链接 | 验证状态 |
|---|---|---|---|---|
| **MCP-Universe** | 首个面向真实 MCP server 的综合基准；覆盖长程推理与大规模陌生工具空间 | 2025-08 | [arXiv:2508.14704](https://arxiv.org/abs/2508.14704) · [主页](https://mcp-universe.github.io) | ✅ 新增，确认 |
| **MCP-Atlas** | 大规模真实 MCP server 工具使用基准；跨 server 编排工作流 + claim 级结构化可复现评分 | 2026-01 | [arXiv:2602.00933](https://arxiv.org/abs/2602.00933) | ✅ 新增，确认 |
| **MCP-Bench** | 28 个代表性真实 MCP server / 250 个工具，覆盖金融、旅行、科学计算、学术检索等 | 2025-08 | [arXiv:2508.20453](https://arxiv.org/abs/2508.20453) | ✅ 新增，确认 |
| **MCP-Zero** | 主动工具发现框架：让 LLM 自行识别能力缺口并按需请求工具，摆脱"全量 schema 注入" | 2025-06 | [arXiv:2506.01056](https://arxiv.org/abs/2506.01056) | ✅ 新增，确认 |
| **MCPEvol-Bench** | 评测 MCP server 持续演化（接口与功能变化）下 Agent 的适应能力 | 2026-07 | [arXiv:2607.14642](https://arxiv.org/abs/2607.14642) | ✅ 新增，确认 |
| **Live API-Bench** | 把 NL2SQL 数据集（NVIDIA 内部 + BIRD SQL）转成交互式 API 环境，2500+ 实时 API | 2025-06 | [arXiv:2506.11266](https://arxiv.org/abs/2506.11266) | ✅ 新增，确认 |
| **StableToolBench-MirrorAPI** | 将工具环境建模为 7,000+ 真实 API 的镜像 | 2025-03 | [arXiv:2503.20527](https://arxiv.org/abs/2503.20527) | ✅ 新增，确认 |
| **MCP-Flow** | 自动化 MCP server 发现 + 数据合成 + 训练；**ACL 2026 Main** | 2025-10 | [arXiv:2510.24284](https://arxiv.org/abs/2510.24284) | ✅ 新增，确认 |
| **SynthTools** | 全 LLM 的工具环境生成 / 模拟 / 校验 / 任务构建流水线 | 2025-11 | [arXiv:2511.09572](https://arxiv.org/abs/2511.09572) | ✅ 新增，确认 |
| **Gecko** | 带状态反馈的模拟环境，用于低成本精炼工具调用序列 | 2026-02 | [arXiv:2602.19218](https://arxiv.org/abs/2602.19218) | ✅ 新增，确认 |
| **MCP-Universe RL** | 面向 MCP 工具使用 Agent 的 RL 框架（环境隔离 + rollout 调度） | 2026-08 | [arXiv:2608.22167](https://arxiv.org/abs/2608.22167) | ✅ 新增，确认 |
| **ToolSandbox（Apple）** | MCP 工具沙箱：状态化的多工具调用沙箱，含断言式验证 | — | [GitHub](https://github.com/apple/ToolSandbox) | ✅ 新增，确认 |
| **ToolSpace** | 以工具为中心的环境合成（反向于数据中心的 MCP 扩展）：从真实 MCP 服务调用轨迹中挖掘数据、状态与重试依赖，再生成工具接口与可执行工作流 | 2026-11 | [arXiv:2611.05036](https://arxiv.org/abs/2611.05036) | ✅ 新增 |
| **STT-Arena** | 带时空动态的更真实工具使用环境：任务中途的扰动会使既有计划失效，考察 Agent 的重规划与适应能力 | 2026-05 | [arXiv:2605.18548](https://arxiv.org/abs/2605.18548) | ✅ 新增 |
| **ToolHazard** | 面向工具型 Agent 安全的对抗环境扩展：把间接提示注入埋入环境状态，规模化构造安全评测与对齐环境 | 2026-08 | [arXiv:2608.11878](https://arxiv.org/abs/2608.11878) | ✅ 新增 |
| **MLToolBench** | 面向机器学习开发的工具增强 Agent 环境：让 Agent 通过 ML 实验而非仅推理推进任务，降低实验的时间与算力成本 | 2026-09 | [arXiv:2609.36679](https://arxiv.org/abs/2609.36679) | ✅ 新增 |
| **Tool Description Rewriting** | 把工具描述本身当作可学习对象：重写工具说明以贴合 Agent 使用方式，而非只优化 Agent 或提示 | 2026-02 | [arXiv:2602.20426](https://arxiv.org/abs/2602.20426) | ✅ 新增 |

---

## 九、企业 / 办公 / 科研 / 专业领域环境

| 论文/框架 | 核心贡献 | 时间/出处 | 链接 | 验证状态 |
|---|---|---|---|---|
| **OfficeBench** | 跨多应用的办公自动化基准；要求整合多源信息并经由一系列决策过程产出结果 | 2024-07 | [arXiv:2407.19056](https://arxiv.org/abs/2407.19056) | ✅ 新增，确认 |
| **AppWorld** | 457 API / 750 任务的可控"应用与人"世界；数据库状态校验；**ACL 2024** | 2024-07 | [arXiv:2407.18901](https://arxiv.org/abs/2407.18901) | ✅ 新增，确认 |
| **TheAgentCompany** | 175 个真实职场任务（消息、代码托管、云存储、项目管理），基于 checkpoint 与执行结果评测 | 2024-12 | [arXiv:2412.14161](https://arxiv.org/abs/2412.14161) | ✅ 新增，确认 |
| **ScienceBoard** | 真实科研工作流中的多模态自主 Agent 评测；**ICLR 2026** | 2025-05 | [arXiv:2505.19897](https://arxiv.org/abs/2505.19897) | ✅ 新增，确认 |
| **FieldWorkArena** | 面向真实现场作业（制造与零售的安全隐患检测、程序违规记录）的 Agent 基准；**ICPR 2026** | 2025-05 | [arXiv:2505.19662](https://arxiv.org/abs/2505.19662) | ✅ 新增，确认 |
| **ChemX** | 化学信息抽取的 10 个数据集，由领域专家校验，揭示通用与领域 Agent 的性能瓶颈 | 2025-10 | [arXiv:2510.00795](https://arxiv.org/abs/2510.00795) | ✅ 新增，确认 |
| **DevOps-Gym** | 完整软件 DevOps 周期（开发、部署、管理）的 Agent 评测 | 2026-01 | [arXiv:2601.20882](https://arxiv.org/abs/2601.20882) | ✅ 新增，确认 |
| **ProactiveMobile** | 移动端主动智能基准：从"执行显式指令"转向"自主预判需求" | 2026-02 | [arXiv:2602.21858](https://arxiv.org/abs/2602.21858) | ✅ 新增，确认 |
| **PIRA-Bench** | 从被动 GUI Agent 到基于 GUI 的主动意图推荐 Agent 的范式转变基准 | 2026-03 | [arXiv:2603.08013](https://arxiv.org/abs/2603.08013) | ✅ 新增，确认 |
| **ProAgentBench** | 基于真实数据的主动辅助评测，修复"LLM 合成数据失真"与"孤立任务"两大缺陷 | 2026-02 | [arXiv:2602.04482](https://arxiv.org/abs/2602.04482) | ✅ 新增，确认 |
| **Proactive Agent Research Environment (Pare)** | 模拟"活跃用户"以评测主动式助手；把应用建模为有状态的顺序交互而非平面工具 API | 2026-04 | [arXiv:2604.00842](https://arxiv.org/abs/2604.00842) | ✅ 新增，确认 |
| **PersonaMem-v2** | 个性化智能数据集：1,000 次真实风格用户-助手交互 / 300+ 场景 / 20,000+ 隐式偏好 / 128K 上下文 | 2025-12 | [arXiv:2512.06688](https://arxiv.org/abs/2512.06688) | ✅ 新增，确认 |
| **ASTRA-bench** | 时序演化的个人上下文 + 交互式工具箱；2,413 个场景 / 4 类主角 | 2026-03 | [arXiv:2603.01357](https://arxiv.org/abs/2603.01357) | ✅ 新增，确认 |
| **EverMemBench** | 多方协作对话中的长程记忆评测（跨群组、跨渠道、随时间修订） | 2026-02 | [arXiv:2602.01313](https://arxiv.org/abs/2602.01313) | ✅ 新增，确认 |
| **CyberGym** | 1,507 个真实漏洞 / 188 个软件项目的规模化网络安全 Agent 评测 | 2025-06 | [arXiv:2506.02548](https://arxiv.org/abs/2506.02548) | ✅ 新增，确认 |
| **OS-Harm** | 基于 OSWorld 的计算机使用 Agent 安全性基准；**NeurIPS 2025 Datasets & Benchmarks Spotlight** | 2025-06 | [arXiv:2506.14866](https://arxiv.org/abs/2506.14866) | ✅ 新增，确认 |
| **DoomArena** | 可插拔的安全评测框架，可接入 BrowserGym / τ-bench，支持细粒度威胁建模 | 2025-04 | [arXiv:2504.14064](https://arxiv.org/abs/2504.14064) | ✅ 新增，确认 |
| **SafetyFlow** | 自动化 LLM 安全基准的 Agent-Flow 系统 | 2025-08 | [arXiv:2508.15526](https://arxiv.org/abs/2508.15526) | ✅ 新增，确认 |
| **GHIssuemarket** | 面向 SWE Agent 经济性实验的沙箱环境 | 2024-12 | [arXiv:2412.11722](https://arxiv.org/abs/2412.11722) | ✅ 新增，确认 |
| **ML-Bench** | 评测 LLM 与 Agent 在仓库级代码上完成机器学习任务的能力 | 2023-11 | [arXiv:2311.09835](https://arxiv.org/abs/2311.09835) | ✅ 新增，确认 |
| **Unified Emulation-Simulation Training Environment for Autonomous Cyber Agents** | 面向自主网络 Agent 的统一仿真-模拟训练环境 | 2023-04 | [arXiv:2304.01244](https://arxiv.org/abs/2304.01244) | ✅ 新增，确认 |
| **Self-Play SWE-RL（环境侧）** | 见"三、经验/交互合成" | 2025-12 | [arXiv:2512.18552](https://arxiv.org/abs/2512.18552) | ✅ 新增，确认 |
| **SciAgentGym** | 科学多步工具使用基准与可扩展交互环境：覆盖四个自然科学学科、1,780 个领域专用工具，考察 Agent 编排工具完成严谨科研流程 | 2026-02 | [arXiv:2602.12984](https://arxiv.org/abs/2602.12984) | ✅ 新增 |
| **D3-Gym** | 首个自动构建的「数据驱动科学发现」可验证环境数据集，含 565 个任务，填补真实科研任务可验证环境的空白 | 2026-04 | [arXiv:2604.27977](https://arxiv.org/abs/2604.27977) | ✅ 新增 |
| **Spreadsheet-RL** | 用 RL 在真实电子表格任务上训练 Agent，替代专用提示与静态监督，并给出可交互的表格环境 | 2026-05 | [arXiv:2605.22642](https://arxiv.org/abs/2605.22642) | ✅ 新增 |
| **EnterpriseSynth** | 「零执行」企业数据合成：把 OpenAPI 规范直接转成 SFT 与评测数据，避开访问控制、合规、限流与改动生产数据的风险 | 2026-10 | [arXiv:2610.22412](https://arxiv.org/abs/2610.22412) | ✅ 新增 |
| **MEDVISTAGYM** | 面向「用医学图像思考」的可扩展训练环境：工具集成 RL 让 VLM 在多步推理中反复复查、验证与修正视觉证据，而非单次静态编码 | 2026-01 | [arXiv:2601.07107](https://arxiv.org/abs/2601.07107) | ✅ 新增 |
| **MedAgentGym** | 面向生物医学数据科学代码推理的可扩展 Agentic 训练环境 | 2025-06 | [arXiv:2506.04405](https://arxiv.org/abs/2506.04405) | ✅ 新增 |
| **Healthcare AI GYM** | 医疗 Agent 的临床推理 Gym：覆盖采集病史、开检查、解读结果、给出安全治疗方案的完整多步交互闭环 | 2026-05 | [arXiv:2605.02943](https://arxiv.org/abs/2605.02943) | ✅ 新增 |
| **6GAgentGym** | 6G 网络管理 Agent 环境：要求 Agent 执行工具、观察状态变化并据此调整决策，配套工具使用、数据合成与 Agentic 学习流程 | 2026-03 | [arXiv:2603.29656](https://arxiv.org/abs/2603.29656) | ✅ 新增 |
| **PatEx-Gym** | 专利审查中的「现有技术检索」Agent 环境：任务需发现稀疏现有技术、迭代精炼检索式并核查技术细节，用来自动化新颖性评估 | 2026-10 | [arXiv:2610.33503](https://arxiv.org/abs/2610.33503) | ✅ 新增 |
| **EO-Gym** | 地球观测 Agent 的多模态交互环境：解决不确定性常需扩大区域、调取历史影像或多源数据，是典型的交互式科研工作流 | 2026-05 | [arXiv:2605.01250](https://arxiv.org/abs/2605.01250) | ✅ 新增 |
| **AgentBench** | 多维 Agent 评测：8 类交互环境（操作系统、数据库、知识图谱、卡牌、网页等），首个系统化「LLM 作为 Agent」的跨环境基准 | 2023-08 | [arXiv:2308.03688](https://arxiv.org/abs/2308.03688) | ✅ 新增 |

---

## 十、平台 / 基建 / 方法论

| 论文/框架 | 核心贡献 | 时间/出处 | 链接 | 验证状态 |
|---|---|---|---|---|
| **AgenticAI-Supervisor** | UI 驱动仿真引擎；千路并行隔离轨迹，模拟即创作 | 2026-07 | [arXiv:2607.05773](https://arxiv.org/abs/2607.05773) | ✅ 确认 |
| **ClawGym II** | 黑盒 RL 对接真实 Agent Harness（OpenClaw / Claude Code）；30 任务 | 2026-08，人大高瓴 & IQuest | [arXiv:2608.16798](https://arxiv.org/abs/2608.16798) | ✅ 确认 |
| **OccuBench** | 语言环境模拟真实职业任务；多学科、异步设定 | 2026-04 | [arXiv:2604.10866](https://arxiv.org/abs/2604.10866) | ✅ 确认 |
| **AgentGym2** | 去理想化真实环境评测框架；27 个领域；测量探索性工具发现、工具组合、噪声鲁棒性 | 2026-07，**ACL 2026 Long** | [arXiv:2607.05174](https://arxiv.org/abs/2607.05174) | ✅ 确认 |
| **TUA-Bench** | 通用终端 Agent 基准；120 任务 / 5 大类 | 2026-06，Meta | [arXiv:2606.28480](https://arxiv.org/abs/2606.28480) | ✅ 确认 |
| **AgencyBench** | 138 任务 / 32 场景；百万 token 级长程上下文 | 2026-01 | [arXiv:2601.11044](https://arxiv.org/abs/2601.11044) | ✅ 确认 |
| **Hierarchy of Agentic Capabilities** | 真实 RL 环境下 Agent 能力层级评估 | 2026-01 | [arXiv:2601.09032](https://arxiv.org/abs/2601.09032) | ✅ 确认 |
| **Efficient Benchmarking of AI Agents** | 8 套 Agent 基准的采样效率研究 | 2026-03 | [arXiv:2603.23749](https://arxiv.org/abs/2603.23749) | ✅ 确认 |
| **OSGym** | 支持 1024 并行沙箱的 CUA 训练基础设施 | 2025 | [arXiv:2511.11672](https://arxiv.org/abs/2511.11672) | ✅ 确认 |
| **EnvHarness** | 可编程层包装静态环境，加速 Agent 学习，不新建环境；Google Research | 2026 | [arXiv:2608.19880](https://arxiv.org/abs/2608.19880) | ✅ 确认 |
| **Harbor-Index 1.0** | 6627 候选过滤得到 82 任务；难度过滤 + AI/人工审计加固流水线 | 2026-07 | [harbor-index.org](https://harbor-index.org/) | ✅ 确认 |
| **Environment Scaling Survey** | GEF 循环（生成-执行-反馈）统一环境扩展综述 | 2025-11 | [arXiv:2511.09586](https://arxiv.org/abs/2511.09586) | ✅ 确认（与"一"同源条目） |
| **Agentic Environment Engineering Survey** | 从环境工程生命周期视角系统综述：建模 → 合成 → 评估 → 应用；涵盖符号合成、神经合成两种范式 | 2026-06 | [arXiv:2606.12191](https://arxiv.org/abs/2606.12191) | ✅ 确认 |
| **AgentJudgeBench** | 3,808 个依赖驱动的 Agentic 工作流；6 种 DAG 拓扑；3 个难度层级；硬查询上所有 judge 收敛于 77-82% 准确率天花板 | **EMNLP 2026 Main** | [arXiv:2608.26623](https://arxiv.org/abs/2608.26623) | ✅ 确认 |
| **Benchmark Radar** | AI 基准的活数据库与搜索引擎；追踪 14,810+ 条记录，覆盖 37 个来源；提供 Dashboard、CLI、RSS 和完整数据集下载；技术报告 arXiv:2609.11115 | — | [GitHub](https://github.com/ktwu01/benchmark-radar) · [Dashboard](https://benchmark-radar.org/) | ✅ 确认 |
| **ProRL Agent** | Rollout-as-a-Service：把 rollout 编排与训练循环解耦，规模化多轮 Agent 的 RL 训练基础设施 | 2026-03 | [arXiv:2603.18815](https://arxiv.org/abs/2603.18815) | ✅ 新增，确认 |
| **VenusRL** | 全解耦 Agentic RL 系统：优先级调度 + 可扩展交互；针对多轮长轨迹的尾延迟与沙箱静态分配两大瓶颈 | 2026-10 | [arXiv:2610.03286](https://arxiv.org/abs/2610.03286) | ✅ 新增，确认 |
| **The Rollout Infrastructure Tax in Coding-Agent RL** | 对比单容器、托管沙箱、Kubernetes 编排容器、云 VM 四种执行基座的 overhead，量化 RL 后训练效率提升空间 | 2026-07 | [arXiv:2607.01415](https://arxiv.org/abs/2607.01415) | ✅ 新增，确认 |
| **ReCreate** | 由交互经验驱动的领域 Agent 自动创建与演化 | 2026-01 | [arXiv:2601.11100](https://arxiv.org/abs/2601.11100) | ✅ 新增，确认 |
| **AgentFactory** | 自动化 Agentic 系统设计与优化 | 2026-09 | [arXiv:2609.01045](https://arxiv.org/abs/2609.01045) | ✅ 新增，确认 |
| **Agent²** | Agent-Generates-Agent：自动化 RL Agent 设计 | 2025-09 | [arXiv:2509.13368](https://arxiv.org/abs/2509.13368) | ✅ 新增，确认 |
| **Youtu-Agent** | Agent 的自动化生成与持续演化框架 | 2025-12 | [arXiv:2512.24615](https://arxiv.org/abs/2512.24615) | ✅ 新增，确认 |
| **AI Scientist via Synthetic Task Scaling** | 合成 ML 挑战任务的可扩展流水线 | 2026-03 | [arXiv:2603.17216](https://arxiv.org/abs/2603.17216) | ✅ 确认 |
| **AgenticDataBench** | 技能聚类 + LLM 任务生成的数据 Agent 基准 | 2026-07 | [arXiv:2607.01647](https://arxiv.org/abs/2607.01647) | ✅ 确认 |
| **QUEST** | 用「全合成任务」训练前沿 deep research Agent：任务由可控合成产生，配套可验证答案与轨迹，摆脱对真实查询日志的依赖 | 2026-05 | [arXiv:2605.24218](https://arxiv.org/abs/2605.24218) | ✅ 新增 |
| **SAGE (Deep Search Data Generation)** | 可操控的搜索 Agent 数据生成：以执行反馈驱动数据生成与筛选，提升 Deep Search 数据质量与任务多样性 | 2026-01 | [arXiv:2601.18202](https://arxiv.org/abs/2601.18202) | ✅ 新增 |
| **Orchard** | 开源 Agentic 建模框架：统一规划、推理、工具使用与多轮交互的数据与训练流水线，降低 Agentic 建模的门槛 | 2026-05 | [arXiv:2605.15040](https://arxiv.org/abs/2605.15040) | ✅ 新增 |
| **ActionStudio** | 面向 Large Action Model 的轻量数据与训练框架：把多源异构轨迹整理成统一可训练格式 | 2025-03 | [arXiv:2503.22673](https://arxiv.org/abs/2503.22673) | ✅ 新增 |
| **GEM (Gym for Agentic LLMs)** | 把「经验式学习」做成 gym：训练范式从静态数据集转向 Agent 在交互环境中习得技能 | 2025-10 | [arXiv:2510.01051](https://arxiv.org/abs/2510.01051) | ✅ 新增 |
| **Jaxnasium** | 基于 PyTrees 的「任意 Agent / 跨套件」RL 接口：统一 JAX 生态中不同环境套件的接口与硬件加速训练流程 | 2026-10 | [arXiv:2610.36075](https://arxiv.org/abs/2610.36075) | ✅ 新增 |
| **Agentic RL Survey** | Agentic RL 综述：系统梳理 LLM Agent 强化学习的环境、奖励、数据与训练范式 | 2025-09 | [arXiv:2509.02547](https://arxiv.org/abs/2509.02547) | ✅ 新增 |

---

## 十一、Sandbox Infra（沙箱基础设施）

| 项目 | 简述 | 日期 | 链接 | 备注 |
|---|---|---|---|---|
| **AgentENV (AENV)** | 由 Moonshot AI 与 kvcache-ai 联合开源的高吞吐分布式智能体环境平台，基于 Firecracker microVM 提供强隔离 Linux 沙箱，专为 Kimi K3 的 Agentic RL 训练打造；支持快照、fork、按需镜像加载，启动 / 恢复 <50ms，暂停 <100ms，兼容 E2B SDK | 2026-07 | [github.com/kvcache-ai/AgentENV](https://github.com/kvcache-ai/AgentENV) | ✅ 确认；开源日期 2026-07-27 |
| **WeEnv** | 微信（WeChat）面向 Agentic RL 的全生命周期环境管理系统，覆盖打包、初始化与弹性供给三阶段；通过层组复用、按需拉取与 CPU / 内存弹性配额，将环境初始化开销降低 5.6–14.2 倍，迭代时间中环境占比从最高 53.4% 降至 9.1% | 2026-09 | [arXiv:2609.30766](https://arxiv.org/abs/2609.30766) | ✅ 确认；arXiv 提交于 2026-09-25 |
| **DeepSeek Elastic Compute (DSec)** | DeepSeek 生产级沙盒基础设施，统一提供 FnCall、容器、microVM 与 full-VM 四种后端；单生产单元约 160 节点 / 3 万核 / 250TB 内存，日均服务约 300 万沙盒，峰值并发超 38 万，创建速率超 5000/秒。所有 DeepSeek V3.2–V4.1 的 RL 训练与评测均在 DSec 上运行 | 2026-09 | [arXiv:2609.22978](https://arxiv.org/abs/2609.22978) | ✅ 确认；arXiv 提交于 2026-09-19；梁文锋署名，130+ 作者 |
| **Sandman** | Amazon 在共享 Kubernetes 上生产运行的 Agentic RL 沙箱服务；小型 daemon 挂载进未修改的任务镜像以跨调用保留文件与进程；限流创建节奏，避免突发请求压垮集群 | 2026-10 | [arXiv:2610.39711](https://arxiv.org/abs/2610.39711) | ✅ 新增，确认 |
| **Readie** | 低延迟代码沙箱：针对快照或单体大镜像启动慢的根因，解耦 Agent harness 与代码执行 | 2026-11 | [arXiv:2611.22171](https://arxiv.org/abs/2611.22171) | ✅ 新增，确认 |
| **VenusRL** | 全解耦 Agentic RL 系统，优先级调度 + 可扩展交互调度 | 2026-10 | [arXiv:2610.03286](https://arxiv.org/abs/2610.03286) | ✅ 新增，确认 |
| **ProRL Agent** | Rollout-as-a-Service 的多轮 Agent RL 基础设施 | 2026-03 | [arXiv:2603.18815](https://arxiv.org/abs/2603.18815) | ✅ 新增，确认 |
| **SideKernel** | macOS 上可用的 microVM 沙箱，面向本地 AI 编码 Agent；调研显示不到 40% 用户在沙箱中运行 Agent | 2026-10 | [arXiv:2610.02456](https://arxiv.org/abs/2610.02456) | ✅ 新增，确认 |
| **Fault-Tolerant Sandboxing for AI Coding Agents** | 基于策略拦截层 + 事务语义的安全自主执行框架，兼顾破坏性命令与系统状态一致性 | 2025-12 | [arXiv:2512.12806](https://arxiv.org/abs/2512.12806) | ✅ 新增，确认 |
| **CUA-Sandbox** | 计算机使用智能体 RL 的高效环境方案。状态胶囊（state capsule）+ 签名路由能力 + 代际租约，实现状态作用域执行与事务性生命周期；WebArena-Lite / VisualWebArena / OSWorld 上最高 6.20× rollout 吞吐、9.2× 内存降低、504× 增量存储降低 | 2026-09 | [arXiv:2609.32750](https://arxiv.org/abs/2609.32750) · [GitHub](https://github.com/windskyyx/Cua-Sandbox) | ✅ 确认；第一作者 Xin Yan，通讯作者 Xingrui Yu；14 位作者来自 A*STAR、HKUST、BNU、NUS、NTU、ZJU、PKU |
| **OpenEnv** | PyTorch 官方 RL 环境接口库，Meta-PyTorch 主导；AWM 等环境已合入其生态 | — | [GitHub](https://github.com/meta-pytorch/OpenEnv) | ✅ 新增，确认 |
| **verifiers** | Prime Intellect 出品的 RL 环境与评测库 | — | [GitHub](https://github.com/PrimeIntellect-ai/verifiers) | ✅ 新增，确认 |
| **Harbor** | 任务格式与执行框架，统一 RL 任务包（指令 + 环境 + 参考解 + 验证器） | — | [GitHub](https://github.com/laude-institute/harbor) | ✅ 新增，确认 |
| **agent-infra/sandbox** | Agent 沙箱运行时 | — | [GitHub](https://github.com/agent-infra/sandbox) | ✅ 新增，确认 |
| **kubernetes-sigs/agent-sandbox** | Kubernetes 官方 SIG 的 Agent 沙箱实现 | — | [GitHub](https://github.com/kubernetes-sigs/agent-sandbox) | ✅ 新增，确认 |
| **alibaba/OpenSandbox** | 阿里开源的沙箱基础设施 | — | [GitHub](https://github.com/alibaba/OpenSandbox) | ✅ 新增，确认 |
| **E2B** | 面向 Agent 的云端沙箱基础设施，支撑并行 rollout | — | [GitHub](https://github.com/e2b-dev/E2B) | ✅ 新增，确认 |
| **inclusionAI/AEnvironment** | InclusionAI 开源的 Agent 环境框架 | — | [GitHub](https://github.com/inclusionAI/AEnvironment) | ✅ 新增，确认 |
| **SWE-MiniSandbox** | 免容器的 SWE Agent RL 训练沙箱方案 | 2026-02 | [arXiv:2602.11210](https://arxiv.org/abs/2602.11210) | ✅ 新增，确认 |
| **Polar** | 「任意 harness 上做 Agentic RL」的规模化方案：把长上下文管理、多轮工具使用与多 Agent 交互统一抽象，降低自建 harness 的成本 | 2026-05 | [arXiv:2605.24220](https://arxiv.org/abs/2605.24220) | ✅ 新增 |
| **EnvSched** | 环境感知的调度：在有限 rollout 预算下，依据环境难度与验证成本分配 rollout，提升 Agent RL 的 rollout 效率 | 2026-10 | [arXiv:2610.37609](https://arxiv.org/abs/2610.37609) | ✅ 新增 |
| **ThunderSync** | Agentic RL 的无损加速：针对长程交互环境中 rollout 生成与训练的同步开销做无损优化 | 2026-10 | [arXiv:2610.05935](https://arxiv.org/abs/2610.05935) | ✅ 新增 |
| **ECHO** | 终端 Agent 免费获得世界模型：命令执行后的返回流本身就是环境动力学信号，可据此学习世界模型，无需额外环境建模成本 | 2026-05 | [arXiv:2605.24517](https://arxiv.org/abs/2605.24517) | ✅ 新增 |

---

## 十二、CUA / 计算机使用

| 工作名称 | arXiv 链接 | 简要描述与 venue | 确认状态 |
|---|---|---|---|
| Gym-Anything: Turn any Software into an Agent Environment | [arXiv:2604.06126](https://arxiv.org/abs/2604.06126) | 多 Agent 流水线将任意软件转化为交互式 CUA 环境，构建 CUA-World（200 软件、10K+ 长视野任务）和 CUA-World-Long（>500 步） | ✅ 确认，arXiv 2026.04 |
| CUA-GYM: Scaling Verifiable Training Environments and Tasks for Computer-Use Agents | [arXiv:2605.25624](https://arxiv.org/abs/2605.25624) | Generator/Discriminator 双 Agent 协作生成可验证 RLVR 训练元组，32,112 条覆盖 110 环境；CUA-GYM-A17B 在 OSWorld-Verified 达 72.6% | ✅ 确认，arXiv 2026.05 |
| CUA-Lite: An Open Platform for Computer-Use Agents | [UC Berkeley RDI 博客](https://rdi.berkeley.edu/blog/cua-lite/) | 统一 Lite.Gym / Lite.Sample / 模型 harness 三大抽象，15+ 基准、10+ 数据集、30K+ 可验证任务 | ✅ 确认，暂无 arXiv 编号 |
| Cua (trycua/cua) | [GitHub](https://github.com/trycua/cua) | 开源基础设施：沙箱、SDK 和基准测试，支持 macOS/Linux/Windows 全桌面控制；配套 Cua-Bench | ✅ 确认，GitHub 项目 |
| Cua Agent framework 0.4 | [Cua 博客](https://cua.ai) | 统一多模型接口，支持 Composite Agents（grounding + planning 模型组合） | ✅ 确认，官方博客 2025.08 |
| OpenCUA: Open Foundations for Computer-Use Agents | [arXiv:2508.09123](https://arxiv.org/abs/2508.09123) | 开源框架含标注基础设施、AgentNet 数据集（3 OS、200+ 应用）和 CoT 推理流水线；OpenCUA-72B 在 OSWorld-Verified 达 45.0% | ✅ 确认，**NeurIPS 2025** |
| CUA-Sandbox: Efficient Environments for Computer-Use Agent Reinforcement Learning | [arXiv:2609.32750](https://arxiv.org/abs/2609.32750) | 通过 state capsule 与共享运行时分离，实现 6.20× rollout 吞吐提升、9.2× 内存降低、504× 存储减少 | ✅ 确认，arXiv 2026.09 |
| OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments | [arXiv:2404.07972](https://arxiv.org/abs/2404.07972) | 369 个真实桌面任务，覆盖 Web/桌面应用、文件 I/O 和跨应用工作流，Ubuntu/Windows/macOS | ✅ 确认，arXiv 2024.04 |
| OSWorld 2.0: Benchmarking Computer Use Agents on Long-Horizon Real-World Tasks | [arXiv:2606.29537](https://arxiv.org/abs/2606.29537) | 将 CUA 评估推至专业级真实工作流难度，二进制成功率仅 20.6% | ✅ 确认，arXiv 2026.06 |
| OSWorld-Human: Benchmarking the Efficiency of Computer-Use Agents | [arXiv:2506.16042](https://arxiv.org/abs/2506.16042) | 人工标注效率基准，发现领先 Agent 平均使用必要步骤的 1.4–2.7 倍 | ✅ 确认，arXiv 2025.06 |
| WebArena: A Realistic Web Environment for Building Autonomous Agents | [arXiv:2307.13854](https://arxiv.org/abs/2307.13854) | 四个自托管网站（电商、社交论坛、协作开发、CMS）+ 地图工具，812 个长视野 Web 任务 | ✅ 确认，arXiv 2023.07 |
| CUARewardBench: A Benchmark for Evaluating Reward Models on Computer-using Agent | [arXiv:2510.18596](https://arxiv.org/abs/2510.18596) | 首个 CUA 奖励模型基准，覆盖 10 软件类别、7 Agent 架构；UPE 方法达 89.8% 精度和 93.3% NPV | ✅ 确认，**ICML 2026** |
| Computer Agent Arena: Toward Human-Centric Evaluation and Analysis of Computer-Use Agents | [ICLR 2026 论文](https://proceedings.iclr.cc/paper_files/paper/2026/hash/5f1d328711b162e1cf9896c7d6aaecdd-Abstract-Conference.html) | 人类偏好驱动的头对头评估平台，2,201 票覆盖 12 Agent，观察到与静态基准的排名反转 | ✅ 确认，**ICLR 2026** |
| MCPWorld: A Unified Benchmarking Testbed for API, GUI, and Hybrid Computer Use Agents | [arXiv:2506.07672](https://arxiv.org/abs/2506.07672) | 首个同时支持 API、GUI 和混合范式的 CUA 测试平台，201 个任务，75.12% 完成准确率 | ✅ 确认，arXiv 2025.06 |
| UI-CUBE: Enterprise-Grade Computer Use Agent Benchmarking Beyond Task Accuracy to Operational Reliability | [arXiv:2511.17131](https://arxiv.org/abs/2511.17131) | UiPath 企业导向确定性基准，226 任务（136 简单 + 90 复杂），暴露 CUA 根本性架构局限 | ✅ 确认，arXiv 2025.11 |
| Agent S: An Open Agentic Framework that Uses Computers Like a Human | [arXiv:2410.08164](https://arxiv.org/abs/2410.08164) | 开放 Agent 框架，通过 GUI 实现计算机自主交互；Agent S2 在 OSWorld 15 步/50 步评估达 18.9%/32.7% | ✅ 确认，**ICLR 2025** |
| Agent S3: The Unreasonable Effectiveness of Scaling Agents for Computer Use | [arXiv:2510.02250](https://arxiv.org/abs/2510.02250) | Agent S 系列的缩放版本，GPT-5 驱动下接近人类水平 | ✅ 确认，**TMLR 2026** |
| OpenAgentFleet | [PyPI](https://pypi.org/project/open-agent-fleet/) | 自托管自主 CUA 平台，每个 Agent 获得独立可丢弃的 Linux 桌面并实时流式传输到浏览器 | ✅ 确认，无 arXiv 论文 |
| open-computer-use (QwenLM) | [GitHub](https://github.com/QwenLM/open-computer-use) | 基于 MCP 的计算机使用服务，通过 accessibility API 控制 macOS/Linux/Windows | ✅ 确认，GitHub 项目 |
| open-computer-use (e2b-dev) | [GitHub](https://github.com/e2b-dev/open-computer-use) | 基于 E2B Desktop Sandbox 的安全云 Linux 计算机，由开源 LLM 控制 | ✅ 确认，GitHub 项目 |
| OmniPilot | [PyPI](https://pypi.org/project/omnipilot-agent/) | 跨平台开源 CUA，支持 13 个模型提供商和本地模型，41 个内置工具，四级权限系统 | ✅ 确认，无 arXiv 论文，PyPI 发布 |
| Tarsier-AI | [PyPI](https://pypi.org/project/tarsier-ai/) | 为 LLM 提供 Windows 桌面应用的确定性交互层，内置 MCP Server，避免基于像素坐标的脆弱点击 | ✅ 确认，无 arXiv 论文 |
| **WildAWM（Agent World Model in the Wild）** | [arXiv:2610.26828](https://arxiv.org/abs/2610.26828) | 微软研究院 + UNC + Gatech + Northeastern；合成整台"个人电脑"（GUI + MCP + CLI 三接口并存于同一状态）；XAI 跨界面任务平均 4.2 子任务 / 3.1 次接口切换 / 74.5% 任务需回到旧接口 / 部分超 100 步；五道质量关卡（评判一致 / 初始未完成 / 可解 / 难度 / 反事实探针）后 2,551 草稿仅留 341 题；合成阶段平均成功率仅 21.3%，GPT-6 Astra Pass@1 60%、Pass@8 仍有 27.3% 做不出；verifier 与 agent judge 一致率 95%、Cohen's κ=0.90；仅用开源模型训练，8 个 OOD 基准（WebArena / Online-Mind2Web / QwenClawBench / ClawEval / CUA-Gym / OSWorld-Verified / OSWorld 2.0 / ALE）全部提升，Qwen3.6-35B-A3B 平均分 42.84→53.42 | ✅ 新增，确认，arXiv 2026.10 |
| **CUA-Universe** | [arXiv:2609.05374](https://arxiv.org/abs/2609.05374) | 面向混合 GUI + CLI Agent 的可扩展动态环境；让视觉状态检视与高吞吐命令行操作协同作用于同一应用状态 | ✅ 新增，确认，arXiv 2026.09 |
| **OSExpert** | [arXiv:2603.07978](https://arxiv.org/abs/2603.07978) | 提出 OSExpert-Eval 基准；用 GUI 深度优先搜索（GUI-DFS）探索算法让 CUA 学习专业技能 | ✅ 新增，确认，arXiv 2026.03 |
| **GroundCUA（Grounding Computer Use Agents on Human Demonstrations）** | [arXiv:2511.07332](https://arxiv.org/abs/2511.07332) | 87 个应用 / 12 类 / 56K 截图的桌面 grounding 数据集；**ICLR 2026** | ✅ 新增，确认，arXiv 2025.11 |
| **WebHarbor** | [arXiv:2611.03634](https://arxiv.org/abs/2611.03634) | 153 个可执行、docker 化的真实网站重建环境，保真还原视觉界面、内容与功能流程 | ✅ 新增，确认，arXiv 2026.11 |
| **Ego2Web** | [arXiv:2603.22529](https://arxiv.org/abs/2603.22529) | 以第一视角视频为基准的 Web Agent 评测 | ✅ 新增，确认，**CVPR 2026** |
| **OSWorld-MCP** | [arXiv:2510.24563](https://arxiv.org/abs/2510.24563) | 首个公平评估 CUA 工具调用能力的基准 | ✅ 新增，确认，arXiv 2025.10 |
| **GUI-CC** | [arXiv:2609.00048](https://arxiv.org/abs/2609.00048) | 评测 GUI 世界模型作为多步 Agent 环境时的上下文一致性 | ✅ 新增，确认，**EMNLP 2026 Findings** |
| **MacArena** | [arXiv:2606.06560](https://arxiv.org/abs/2606.06560) | 在线 macOS 环境上的 CUA 评测 | ✅ 新增，确认，arXiv 2026.06 |
| **MacAgentBench** | [arXiv:2606.22557](https://arxiv.org/abs/2606.22557) | 真实 macOS 桌面上的 AI Agent 基准 | ✅ 新增，确认，arXiv 2026.06 |
| **macOSWorld** | [arXiv:2506.04135](https://arxiv.org/abs/2506.04135) | 多语言交互式 GUI Agent 基准 | ✅ 新增，确认，arXiv 2025.06 |
| **Windows Agent Arena** | [arXiv:2409.08264](https://arxiv.org/abs/2409.08264) | 规模化多模态 OS Agent 评测 | ✅ 新增，确认，arXiv 2024.09 |
| **OSUniverse** | [arXiv:2505.03570](https://arxiv.org/abs/2505.03570) | 多模态 GUI 导航基准，强调易用性、可扩展性与自动验证 | ✅ 新增，确认，arXiv 2025.05 |
| **MMBench-GUI** | [arXiv:2507.19478](https://arxiv.org/abs/2507.19478) | 分层多平台 GUI Agent 评测框架 | ✅ 新增，确认，arXiv 2025.07 |
| **On the Reliability of Computer Use Agents** | [arXiv:2604.17849](https://arxiv.org/abs/2604.17849) | 系统刻画 CUA 的可靠性边界 | ✅ 新增，确认，arXiv 2026.04 |
| **OS-Harm** | [arXiv:2506.14866](https://arxiv.org/abs/2506.14866) | CUA 安全性基准 | ✅ 新增，确认，**NeurIPS 2025 D&B Spotlight** |
| **Trial by Trace** | [arXiv:2610.32285](https://arxiv.org/abs/2610.32285) | 以轨迹为单位评测 Agent Harness 的可靠性与失败归因 | ✅ 新增，确认，arXiv 2026.10 |
| **Benchmarking and Improving GUI Agents in High-Dynamic Environments** | [arXiv:2604.25380](https://arxiv.org/abs/2604.25380) | 高动态界面的 GUI Agent 基准与改进 | ✅ 新增，确认，arXiv 2026.04 |
| **MobileWorld** | [arXiv:2512.19432](https://arxiv.org/abs/2512.19432) | MCP 增强 + Agent-用户交互的移动 Agent 基准 | ✅ 新增，确认，arXiv 2025.12 |
| **ViMo** | [arXiv:2504.13936](https://arxiv.org/abs/2504.13936) | 生成式视觉 GUI 世界模型 | ✅ 新增，确认，arXiv 2025.04 |
| **Code2World** | [arXiv:2602.09856](https://arxiv.org/abs/2602.09856) | 可渲染代码生成路线的 GUI 世界模型 | ✅ 新增，确认，**CVPR 2026** |
| **UI-Simulator** | [arXiv:2510.14969](https://arxiv.org/abs/2510.14969) | 规模化合成 UI 状态、转移与轨迹 | ✅ 新增，确认，arXiv 2025.10 |
| **Recovering Policy-Induced Errors** | [arXiv:2605.29447](https://arxiv.org/abs/2605.29447) | GUI-RobustEval 1,216 用例 + RoTS 合成 800K 轨迹 | ✅ 新增，确认，**ICML 2026 Spotlight** |
| **SEE** | [arXiv:2607.18046](https://arxiv.org/abs/2607.18046) | 长程 GUI 轨迹合成 | ✅ 新增，确认，**ACM MM 2026 Oral** |
| **GSAR** | [arXiv:2608.22847](https://arxiv.org/abs/2608.22847) | 目标状态锚定奖励 + 自演化数据合成 | ✅ 新增，确认，**EMNLP 2026 Main** |
| **OSGym** | [arXiv:2511.11672](https://arxiv.org/abs/2511.11672) | 1024 并行沙箱的 CUA 训练基础设施 | ✅ 确认，arXiv 2025 |
| **CUA-Lite** | [arXiv:2610.26071](https://arxiv.org/abs/2610.26071) | 开放 CUA 平台，三大统一抽象：统一环境接口（整合桌面/浏览器/移动 12 个基准 + 免 VM 轻量沙箱）、统一采样与模型 harness，使评测、RL、SFT 共用一套基础设施 | ✅ 新增 |
| **CUA-Master** | [arXiv:2611.03126](https://arxiv.org/abs/2611.03126) | 嵌套双环递归改进：外层做世界数据扩展、内层做策略提升，用外部可验证信号替代纯自生成经验，缓解递归改进的收益递减 | ✅ 新增 |
| **Covering Human Action Space** | [arXiv:2605.12501](https://arxiv.org/abs/2605.12501) | 发现 CUA 失败呈长尾：少数复杂多样交互占据不成比例的失败；据此针对长尾复杂交互做数据合成并建立对应基准 | ✅ 新增 |
| **EvoCUA** | [arXiv:2601.15876](https://arxiv.org/abs/2601.15876) | 原生 CUA 模型，把数据生成与策略优化整合进同一闭环，替代对静态数据集的被动模仿，以捕捉长程任务中的因果动态 | ✅ 新增 |
| **EvoCUA-1.5** | [arXiv:2607.09773](https://arxiv.org/abs/2607.09773) | 从离线经验学习推进到在线 RL：策略在部分可观测多模态桌面环境中交互，静态轨迹无法覆盖「动作改变屏幕状态—改变动作空间与恢复选项」的因果闭环 | ✅ 新增 |
| **Player-1** | [arXiv:2610.20584](https://arxiv.org/abs/2610.20584) | 在游戏中学习：为解决游戏场景交互数据稀缺，用合成经验训练 CUA，使其从合成交互中习得游戏操作策略 | ✅ 新增 |

---

## 十三、数据合成（轨迹 / 工具调用 / 推理数据）

> 不只是「环境合成」，还包括**数据合成**：从环境、工具、文本语料与真实工作流中产出可训练、可验证的轨迹、工具调用序列与推理数据，以及数据质量/难度/覆盖的可控机制。

| 论文/框架 | 核心贡献 | 时间/出处 | 链接 | 验证状态 |
|---|---|---|---|---|
| **What Makes Good Agentic Data? (ACE Lens)** | 系统梳理 Agentic 数据生成的统一框架：要求环境、任务、交互与成功信号四者一致，并把「候选构造」与「验证/选择」明确分离；给出跨领域生成机制的两层分类 | 2026-08 | [arXiv:2608.27260](https://arxiv.org/abs/2608.27260) | ✅ 新增 |
| **Trajectory2Gym** | 指出「成功的轨迹不等于有用的监督」，提出组合覆盖 + 决策接地两条要求：每条被监督动作必须由学习者可见的交互历史支持；据此把轨迹转为可训练 gym | 2026-10 | [arXiv:2610.33568](https://arxiv.org/abs/2610.33568) | ✅ 新增 |
| **COVERT（Controllable and Verifiable Tool-Use Data Synthesis）** | 两阶段可验证工具调用数据合成：先自进化合成并多级校验得到可靠基础轨迹，再做保 oracle 的增广（干扰工具、间接/歧义用户查询、噪声），系统性提升环境复杂度，服务 RL 在线 rollout | 2026-04 | [arXiv:2604.09813](https://arxiv.org/abs/2604.09813) | ✅ 新增 |
| **Davinci-Tool** | 30B 工具调用模型 + Davinci-ToolData：执行接地的数据集，同步扩展环境覆盖与结果验证，因为新环境带来新状态、规则与依赖，成功判据也必须随之改写 | 2026-10 | [arXiv:2610.16867](https://arxiv.org/abs/2610.16867) | ✅ 新增 |
| **GRADS** | 图调控的 Agentic 数据合成：用图结构约束多跳证据与答案的耦合强度，使「表面深度」变成真实推理难度，实现难度可控的 deep research 合成数据 | 2026-10 | [arXiv:2610.21167](https://arxiv.org/abs/2610.21167) | ✅ 新增 |
| **Scaling Agentic Data for Long-Horizon Terminal Intelligence** | 长程终端 Agentic 数据扩展：短轨迹只能展示命令，长程轨迹才能体现「积累证据—判断—按反馈调整—产出交付物」的完整行为链 | 2026-10 | [arXiv:2610.13166](https://arxiv.org/abs/2610.13166) | ✅ 新增 |
| **SAP** | 状态引导 + 参数溯源的多轮工具调用数据合成：约束工具参数的出处，避免「选对工具但参数编造/过期」，直接针对长程工具调用的参数级依赖 | 2026-09 | [arXiv:2609.06124](https://arxiv.org/abs/2609.06124) | ✅ 新增 |
| **EvoSyn** | 面向可验证学习的进化式数据合成：针对「生成易幻觉、验证器太弱无法区分强弱解」两大痛点，进化式构造可迁移的验证数据 | 2025-10 | [arXiv:2510.17928](https://arxiv.org/abs/2510.17928) | ✅ 新增 |
| **SKT** | 技能使用的大规模可验证合成数据：从技能库选出单技能/多技能组合，规则+Agent 双重校验构造可执行轨迹，训练 Agent 识别、应用与协同 skill | 2026-08 | [arXiv:2608.02287](https://arxiv.org/abs/2608.02287) | ✅ 新增 |
| **WebShaper** | 「信息寻求形式化」驱动的 Web Agent 数据合成：先形式化信息结构与推理结构再生成问答，解决「先抓网页再出题」造成的信息结构与推理结构不一致 | 2025-07 | [arXiv:2507.15061](https://arxiv.org/abs/2507.15061) | ✅ 新增 |
| **TDScaling（Beyond Quantity: Trajectory Diversity Scaling）** | 面向代码 Agent 的「轨迹多样性扩展」：在固定训练预算下，提升轨迹多样性比堆数量更有效，可突破数量扩展的早期瓶颈 | 2026-02 | [arXiv:2602.03219](https://arxiv.org/abs/2602.03219) | ✅ 新增 |
| **GEM (Tool-Use Trajectories from Text)** | 把文本语料中天然存在的多步求解经验转成多轮工具调用轨迹，开辟无需模拟环境的、可扩展且真实的合成数据来源 | 2026-01 | [arXiv:2601.10355](https://arxiv.org/abs/2601.10355) | ✅ 新增 |
| **Trajectory2Task** | 可验证数据生成流水线，专门覆盖真实用户意图的三类难例：歧义请求、随时间变化的请求、因策略约束不可行的请求 | 2026-01 | [arXiv:2601.20144](https://arxiv.org/abs/2601.20144) | ✅ 新增 |
| **JudgeMix** | Judge 引导的混合 rollout 数据合成：按目标模型自身状态分布决定专家介入程度与步级监督密度，缓解 SFT 的训推分布错配 | 2026-11 | [arXiv:2611.16174](https://arxiv.org/abs/2611.16174) | ✅ 新增 |
| **Know What You Don't Know** | 通过「进化生成空间」做 Agentic 数据合成：把观测到的模型弱点直接转成未来合成应如何改变生成空间的决策，支持闭环学习 | 2026-10 | [arXiv:2610.12593](https://arxiv.org/abs/2610.12593) | ✅ 新增 |
| **Agent-R$^2$** | 面向真实生产力工作的「真实来源」数据合成：以真实工作意图、真实文件环境与交付物级验证为核心，扩展长程专业工作流的后训练数据 | 2026-11 | [arXiv:2611.08219](https://arxiv.org/abs/2611.08219) | ✅ 新增 |
| **RODS** | 奖励驱动的在线数据合成：依据 GRPO 的奖励方差（Popoviciu 上界）定位能力边界，随着边界漂移持续生成新的高信息量样本，避免静态数据池耗尽 | 2026-06 | [arXiv:2606.19047](https://arxiv.org/abs/2606.19047) | ✅ 新增 |
| **Constrained Data Synthesis + Graduated Rewards** | 用大规模真实 API 响应缓存构成确定性环境，做受约束的工具编排数据合成，并配渐进式奖励为部分正确的多步调用提供信号 | 2026-03 | [arXiv:2603.24709](https://arxiv.org/abs/2603.24709) | ✅ 新增 |
| **ToolMind** | 大规模、推理增强的工具调用数据集，面向多样工具与多轮推理场景 | 2025-11 | [arXiv:2511.15718](https://arxiv.org/abs/2511.15718) | ✅ 新增 |
| **OpenVisTool** | 合成「指令性视觉工具调用轨迹」的开放配方：让多模态 Agent 学会主动调用视觉工具以获取图像编码之外的证据 | 2026-08 | [arXiv:2608.08557](https://arxiv.org/abs/2608.08557) | ✅ 新增 |
| **ToolACE-MT** | 非自回归的 Agentic 多轮交互生成：面向复杂函数调用与动态环境，一次生成整段多轮交互而非逐 token 生成，提升数据合成效率与一致性 | 2025-08 | [arXiv:2508.12685](https://arxiv.org/abs/2508.12685) | ✅ 新增 |
| **AutoDataBench** | 反向提问：Agent 能否自动写出「喂养自我改进循环」的数据？把数据生产本身作为待评测的 Agent 能力 | 2026-09 | [arXiv:2609.35025](https://arxiv.org/abs/2609.35025) | ✅ 新增 |
| **Self-Instruct** | 数据合成的起点工作：用 175 条人工种子指令引导模型自生成指令-输入-输出三元组，过滤低质与重复后得到约 52K 条指令数据，在 Super-NaturalInstructions 上相对基线提升 33.3% | 2022-12 | [arXiv:2212.10560](https://arxiv.org/abs/2212.10560) | ✅ 新增 |
| **WizardLM / Evol-Instruct** | 把「指令复杂度」当作可演化对象：用深度演化（增加约束、深化、具体化）与广度演化（新主题）迭代改写指令，合成 250K 复杂指令数据，训练出 WizardLM | 2023-04 | [arXiv:2304.12244](https://arxiv.org/abs/2304.12244) | ✅ 新增 |
| **AgentInstruct / Agentic Flow** | 微软的「生成式教学」：用 agentic flow 把原始语料（代码、网页、文本）转成高质量指令-回答数据，单一流程即可跨 6 类任务复用，配合 Orca 式渐进学习 | 2024-07 | [arXiv:2407.03502](https://arxiv.org/abs/2407.03502) | ✅ 新增 |
| **ToolLLM / ToolBench** | 工具调用数据的规模化标杆：覆盖 16,464 个真实 REST API（49 个类别），用 ChatGPT 自动构造指令并做 DFSDT 多路径搜索，配 ToolEval 自动评测 | 2023-07 | [arXiv:2307.16789](https://arxiv.org/abs/2307.16789) | ✅ 新增 |
| **APIGen** | 可验证函数调用数据的三级校验流水线：格式检查、真实执行、语义校验；产出 60K 可执行函数调用数据集，训练的 xLAM-7B 系列在 Berkeley Function-Calling 达 88% | 2024-06 | [arXiv:2406.18518](https://arxiv.org/abs/2406.18518) | ✅ 新增 |
| **ToolACE** | 双层验证 + 自演化的工具调用数据合成：26,507 个 API 覆盖多样场景，规则验证器与模型验证器互补过滤幻觉与不一致，模型自身参与数据难度演化 | 2024-09 | [arXiv:2409.00920](https://arxiv.org/abs/2409.00920) | ✅ 新增 |
| **Magicoder / OSS-Instruct** | 以开源代码片段为种子「启发」模型写出多样、真实的编程问题，合成 75K 指令数据；证明高质量合成数据可让小模型超过更大基线 | 2023-12 | [arXiv:2312.02120](https://arxiv.org/abs/2312.02120) | ✅ 新增 |
| **AgentOhana** | 统一多源 Agent 轨迹的数据 schema 与训练管线：把来自不同环境的异构轨迹标准化，解决跨环境数据难以混合训练的工程问题 | 2024-02 | [arXiv:2402.15506](https://arxiv.org/abs/2402.15506) | ✅ 新增 |
| **ToolAlpaca** | 用 400 个工具、3,000 个模拟实例合成工具使用数据，验证小模型无需真实 API 交互即可获得泛化的工具调用能力 | 2023-06 | [arXiv:2306.05301](https://arxiv.org/abs/2306.05301) | ✅ 新增 |
| **TaskCraft** | 自动生成「多深度、多广度」的 Agentic 任务：从原子任务出发做深度/宽度扩展并做可执行校验，产出可扩展、难度可控且带轨迹的任务集 | 2025-06 | [arXiv:2506.10055](https://arxiv.org/abs/2506.10055) | ✅ 新增 |
| **Crafter** | 2D 开放世界生存基准：程序化生成世界、22 个可解锁成就，观测为 64×64 图像，考察长程探索、记忆与泛化，是 LLM/RL Agent 开放世界研究的常用底座 | 2021-11 | [GitHub: danijar/crafter](https://github.com/danijar/crafter) | ✅ 确认 · NeurIPS 2021 D&B（无 arXiv 编号） |
| **MineDojo** | 互联网规模知识 + Minecraft 开放式具身环境：3,000+ 任务、7,000+ YouTube 视频与 Wiki 数据，配套 MineCLIP 奖励与开放式 agent 评测 | 2022-06 | [arXiv:2206.08853](https://arxiv.org/abs/2206.08853) | ✅ 新增 |
| **Voyager** | Minecraft 中的 LLM 终身学习 Agent：自动课程（按技能水平提任务）+ 可执行技能代码库 + 迭代提示自修复，全程无梯度更新即可持续探索 | 2023-05 | [arXiv:2305.16291](https://arxiv.org/abs/2305.16291) | ✅ 新增 |
| **JARVIS-1** | 记忆增强的多模态 LLM Agent：在 Minecraft 开放世界中构建多模态记忆（观测、动作、反馈），支持多任务终身学习 | 2023-11 | [arXiv:2311.05997](https://arxiv.org/abs/2311.05997) | ✅ 新增 |
| **GITM (Ghost in the Minecraft)** | 用 LLM + 文本知识 + 技能库把长程目标分解为可执行技能序列，解决开放世界长程任务（如获取钻石），无需人类示范数据 | 2023-05 | [arXiv:2305.17144](https://arxiv.org/abs/2305.17144) | ✅ 新增 |
| **ScienceWorld** | 交互式文本科学实验环境：30 类小学科学任务（物质、生命、力与运动等），要求 agent 通过多步实验操作达成目标，是科学推理环境的经典基准 | 2022-03 | [arXiv:2203.07540](https://arxiv.org/abs/2203.07540) | ✅ 新增 |
| **ProcTHOR** | 程序化生成 10,000+ 可交互 3D 房间，展示「程序化生成」相对人工场景在具身 AI 训练规模与泛化上的优势 | 2022-06 | [arXiv:2206.06994](https://arxiv.org/abs/2206.06994) | ✅ 新增 |
| **Habitat 3.0** | 人-虚拟人-机器人共居仿真环境：支持异构多智能体协作与社交导航，配套人机协作任务与评测 | 2023-10 | [arXiv:2310.13724](https://arxiv.org/abs/2310.13724) | ✅ 新增 |
| **SayCan** | 把 LLM 的语言知识与机器人可执行 affordance 结合：LLM 提出候选技能，价值函数判断可行性，实现长程机器人指令接地 | 2022-04 | [arXiv:2204.01691](https://arxiv.org/abs/2204.01691) | ✅ 新增 |
| **BEHAVIOR-1K** | 以人为本的具身 AI 基准：1,000 项日常活动、50 个场景，强调人类日常需求与物理交互真实性 | 2024-03 | [arXiv:2403.09227](https://arxiv.org/abs/2403.09227) | ✅ 新增 |
| **Generative Agents** | Smallville 社会仿真：25 个具备记忆流与反思机制的 agent 自主生活、社交与协作，开创「生成式社会仿真」范式 | 2023-04 | [arXiv:2304.03442](https://arxiv.org/abs/2304.03442) | ✅ 新增 |
| **CAMEL** | 角色扮演式多 Agent 协作：用「任务指定者-执行者」对话自动生成协作轨迹，用于研究 agent 社会与合成对话数据 | 2023-03 | [arXiv:2303.17760](https://arxiv.org/abs/2303.17760) | ✅ 新增 |
| **AgentVerse** | 多 Agent 协作框架：动态招募、协同决策与行为评测，观察群体涌现行为 | 2023-08 | [arXiv:2308.10848](https://arxiv.org/abs/2308.10848) | ✅ 新增 |
| **MetaGPT** | 把标准作业流程（SOP）编码进多 Agent 软件公司：产品-架构-工程角色分工，验证「SOP 作为多 Agent 环境约束」的有效性 | 2023-08 | [arXiv:2308.00352](https://arxiv.org/abs/2308.00352) | ✅ 新增 |
| **Unnatural Instructions** | 用 LLM 改写人工指令，自动扩增出 64K「不自然」指令-输入-输出数据；证明合成指令可替代大量人工标注 | 2022-12 | [arXiv:2212.09689](https://arxiv.org/abs/2212.09689) | ✅ 新增 |
| **Toolformer** | 自监督地让模型学会「何时调用哪个 API」：用少量示例引导模型自己标注 API 调用位置并过滤有用调用，再据此训练 | 2023-02 | [arXiv:2302.04761](https://arxiv.org/abs/2302.04761) | ✅ 新增 |
| **WebGPT** | 浏览器辅助问答：用人类反馈训练模型在真实浏览器中检索、引用与作答，产出带动作序列的示范数据（2021-12，早于多数 agent 数据工作） | 2021-12 | [arXiv:2112.09332](https://arxiv.org/abs/2112.09332) | ✅ 新增 |
| **Orca** | 从 GPT-4 的「解释轨迹」渐进学习：用复杂解释与逐步推理作为监督信号，系统研究解释数据规模与质量对小模型的影响 | 2023-06 | [arXiv:2306.02707](https://arxiv.org/abs/2306.02707) | ✅ 新增 |
| **AgentTuning** | AgentInstruct 数据集 + 混合任务微调：用 6 类任务的合成交互数据微调，提升 LLM 的 agent 能力且不损害通用能力 | 2023-10 | [arXiv:2310.12823](https://arxiv.org/abs/2310.12823) | ✅ 新增 |
| **MINT** | 多轮工具使用 + 语言反馈评测：把「能否利用工具返回与反馈不断修正」作为核心能力维度 | 2023-09 | [arXiv:2309.10691](https://arxiv.org/abs/2309.10691) | ✅ 新增 |
| **API-Bank** | 工具增强 LLM 的综合基准：73 个 API、314 组对话，覆盖调用、检索与多轮规划 | 2023-04 | [arXiv:2304.08244](https://arxiv.org/abs/2304.08244) | ✅ 新增 |
| **TaskBench** | 任务自动化基准：要求模型分解任务并生成工具调用依赖图，从「任务分解 + 工具调用」双维度评测 | 2023-11 | [arXiv:2311.18760](https://arxiv.org/abs/2311.18760) | ✅ 新增 |
| **Gorilla** | 大规模 API 调用能力：1,645 个 API 的调用数据 + retriever-aware 训练，显著降低 API 幻觉 | 2023-05 | [arXiv:2305.15334](https://arxiv.org/abs/2305.15334) | ✅ 新增 |

---

## 十四、具身 / 机器人环境合成

> 通过仿真、场景生成与可执行重建规模化产出具身交互数据，服务 VLA / 机器人基础模型；核心是语义连贯、物理可行与可验证三类性质的平衡。

| 论文/框架 | 核心贡献 | 时间/出处 | 链接 | 验证状态 |
|---|---|---|---|---|
| **Nimbus** | 统一的具身合成数据生成框架：把碎片化、任务专用的生成管线收敛为统一调度，解决工程低效与系统不稳定，支撑基础模型训练所需的高吞吐数据生产 | 2026-01 | [arXiv:2601.21449](https://arxiv.org/abs/2601.21449) | ✅ 新增 |
| **SkillWeaver** | 在神经交互技能上做 Agentic 探索来扩机器人数据：用闭环技能组合替代开环控制器、脚本化技能序列与任务专用程序 | 2026-09 | [arXiv:2609.36171](https://arxiv.org/abs/2609.36171) | ✅ 新增 |
| **EmbodiedSmith** | 仿真中的递归自我改进飞轮：同时扩展资产、技能、场景生成与任务生成，并支持复杂具身形态与物理，缓解预定义资产与技能的约束 | 2026-10 | [arXiv:2610.07969](https://arxiv.org/abs/2610.07969) | ✅ 新增 |
| **V-CAGE** | 视觉闭环的 Agentic 生成引擎：为 VLA 训练合成语义连贯且物理可行的操作场景，解决缺乏上下文感知、目标不可达导致任务提前失败的问题 | 2026-04 | [arXiv:2604.09036](https://arxiv.org/abs/2604.09036) | ✅ 新增 |
| **SceneBloom** | Agentic 室内环境生成：结合语言引导的语义规划与视觉生成先验，再经几何推理修正，产出可仿真、多样且物理合理的 3D 室内布局 | 2026-10 | [arXiv:2610.32978](https://arxiv.org/abs/2610.32978) | ✅ 新增 |
| **OWMM-Agent** | 开放世界移动操作的多模态 Agentic 数据合成：覆盖开放式指令与环境的泛化，打通高层决策与底层控制的数据链路 | 2025-06 | [arXiv:2506.04217](https://arxiv.org/abs/2506.04217) | ✅ 新增 |
| **GRUtopia** | 首个面向多种机器人的交互式 3D 社会仿真：配套场景数据集 GRScenes、任务与评测体系，探索具身智能的仿真-现实（Sim2Real）扩展 | 2024-07 | [arXiv:2407.10943](https://arxiv.org/abs/2407.10943) | ✅ 新增 |
| **PARTNR** | 人-机器人协作的规划与推理基准：LLM 半自动任务生成流水线 + 仿真在环接地，任务含空间、时间与异质能力约束 | 2024-10 | [arXiv:2411.00081](https://arxiv.org/abs/2411.00081) | ✅ 新增 |
| **ABot-ER** | 通过「Agentic 数据-模型协同进化」统一具身推理的广度与深度：单一模型内兼顾感知、规划与执行 | 2026-10 | [arXiv:2610.18355](https://arxiv.org/abs/2610.18355) | ✅ 新增 |
| **SimWorld (Open-ended Simulator)** | 面向物理与社会世界的开放式真实感仿真器，作为 LLM/VLM Agent 在复杂物理与社会环境中的可扩展训练/评测场 | 2025-11 | [arXiv:2512.01078](https://arxiv.org/abs/2512.01078) | ✅ 新增 |
| **SubTGraph** | 大规模地下（SubT）环境合成，具备可控的拓扑变异性，用于机器人自主性的验证 | 2026-05 | [arXiv:2605.20917](https://arxiv.org/abs/2605.20917) | ✅ 新增 |
| **Synthetic Household Data at Scale** | 规模化生成真实感家庭合成数据，为具身 Agent 的环境推理与交互提供可扩展数据源 | 2026-02 | [arXiv:2602.07243](https://arxiv.org/abs/2602.07243) | ✅ 新增 |
| **Code as Policies** | 把语言模型生成的代码作为机器人控制策略：在感知 API 之上直接产出可执行策略代码，处理几何与数值约束 | 2022-09 | [arXiv:2209.07753](https://arxiv.org/abs/2209.07753) | ✅ 新增 |

---

## 十五、多 Agent / 社会仿真环境

> 多 Agent 环境既是训练场也是评测场：任务受社会结构、相互依赖与混合动机影响，环境需支持长期演化与状态追踪。

| 论文/框架 | 核心贡献 | 时间/出处 | 链接 | 验证状态 |
|---|---|---|---|---|
| **AgentSociety** | 多 Agent 环境驱动的社会智能：让 Agent 在可自主行动、策略沟通与协同的多 Agent 环境中，借由通信通道与反馈信号长期演化 | 2026-05 | [arXiv:2605.26203](https://arxiv.org/abs/2605.26203) | ✅ 新增 |
| **AdaSociety** | 带社会结构的自适应多 Agent 环境：任务受社会连接影响（改变奖励与信息访问），并能依据 Agent 行为生成新任务 | 2024-11 | [arXiv:2411.03865](https://arxiv.org/abs/2411.03865) | ✅ 新增 |
| **MAC-Bench** | 用「互联任务」评测多 Agent 协作：不只测解题能力，还测处理相互依赖工作的能力 | 2026-11 | [arXiv:2611.01728](https://arxiv.org/abs/2611.01728) | ✅ 新增 |
| **MEMTRACK** | 多平台动态企业环境中的长期记忆与状态追踪基准：把真实组织工作流拆成跨平台的状态演化链 | 2025-10 | [arXiv:2510.01353](https://arxiv.org/abs/2510.01353) | ✅ 新增 |
| **Coopetition-Gym** | 混合动机下「竞合」多 Agent RL 的形式化平台：20 个环境分四类机制（相互依赖与互补、信任与声誉、集体行动等） | 2026-05 | [arXiv:2605.02063](https://arxiv.org/abs/2605.02063) | ✅ 新增 |
| **MAESTRO** | 多 Agent 强化学习的开放式环境设计：同时自适应环境参数与协作者策略，联合塑造课程（单 Agent 方法只能各自独立适配） | 2023-03 | [arXiv:2303.03376](https://arxiv.org/abs/2303.03376) | ✅ 新增 |
| **UDE (Unified Distributed Environment)** | 环境虚拟化工具包：把 Gazebo / Unity / Unreal / OpenAI Gym 等不同平台的环境统一接口并可卸载到远端执行，为大规模并行仿真提供底座 | 2022-05 | [arXiv:2205.06946](https://arxiv.org/abs/2205.06946) | ✅ 新增 |
| **ChatDev** | 多 Agent 软件公司仿真：CEO/CTO/程序员/测试等角色分工，用对话驱动「设计-编码-测试」全流程 | 2023-07 | [arXiv:2307.07924](https://arxiv.org/abs/2307.07924) | ✅ 新增 |
| **AutoGen** | 可对话的多 Agent 框架：把多 Agent 协作抽象为「可定制、可对话的 agent」，支持人机混合与工具调用编排 | 2023-08 | [arXiv:2308.08155](https://arxiv.org/abs/2308.08155) | ✅ 新增 |

---

## 十六、开源项目（GitHub）

> 环境合成、数据合成、Agentic RL 与沙箱基建的开源入口；星数为抓取时的近似值，以仓库页为准。

| 项目 | 简述 | 日期 | 链接 | 备注 |
|---|---|---|---|---|
| **AgentENV (AENV)** | 分布式平台，用于大规模运行 Agent 环境；把环境的创建、隔离、调度与回收做成可横向扩展的服务 | 2026-07 | [kvcache-ai/AgentENV](https://github.com/kvcache-ai/AgentENV) | ✅ 确认 · ★3.8k |
| **Agent-World** | Agent-World 官方代码：真实世界环境合成，用于演化通用 Agent 智能 | 2026-08 | [RUC-NLPIR/Agent-World](https://github.com/RUC-NLPIR/Agent-World) | ✅ 确认 · ★227 |
| **EnvFactory** | 通过可执行环境合成 + 稳健 RL 扩展工具使用 Agent 的官方代码 | 2026-02 | [LARK-AI-Lab/EnvFactory](https://github.com/LARK-AI-Lab/EnvFactory) | ✅ 确认 · ★102 |
| **ASTRA (code)** | 端到端系统：合成 Agentic 轨迹与规则可验证环境，供 SFT 与 RL 使用 | 2026-01 | [LianjiaTech/astra](https://github.com/LianjiaTech/astra) | ✅ 确认 · ★166 |
| **CUA-Gym-Hub** | 用 mock Web 应用作为可复现 RL 训练环境的 CUA 环境中心 | 2025-12 | [xlang-ai/CUA-Gym-Hub](https://github.com/xlang-ai/CUA-Gym-Hub) | ✅ 确认 · ★85 |
| **RecreationWorld (code)** | 混合型 CUA 的可扩展可验证环境：参考实现与代码 | 2026-09 | [QwenLM/RecreationWorld](https://github.com/QwenLM/RecreationWorld) | ✅ 确认 · ★123 |
| **Echoverse (code)** | 面向 CUA 的「深、可演化」环境框架 | 2026-07 | [microsoft/Echoverse](https://github.com/microsoft/Echoverse) | ✅ 确认 · ★41 |
| **WebHarbor** | 把真实网站「对接」为可演化 GUI Agent 环境，避免静态快照带来的环境漂移 | 2026-05 | [aiming-lab/WebHarbor](https://github.com/aiming-lab/WebHarbor) | ✅ 确认 · ★79 |
| **AgentSynth** | 面向通用 CUA 的可扩展任务生成（ICLR 2026） | 2025-05 | [sunblaze-ucb/AgentSynth](https://github.com/sunblaze-ucb/AgentSynth) | ✅ 确认 · ★54 |
| **AgentTrek** | 用 Web 教程「引导式回放」合成 Agent 轨迹（ICLR 2025 Spotlight） | 2025-02 | [xlang-ai/AgentTrek](https://github.com/xlang-ai/AgentTrek) | ✅ 确认 · ★60 |
| **CLI-Gym** | 通过「Agentic 环境反演」实现可扩展 CLI 任务生成 | 2026-02 | [LiberCoders/CLI-Gym](https://github.com/LiberCoders/CLI-Gym) | ✅ 确认 · ★139 |
| **Trajectory2Gym** | 决策接地的组合式交互合成（工具使用 Agent）官方代码与训练数据 | 2026-10 | [yihaohu0118/Trajectory2Gym](https://github.com/yihaohu0118/Trajectory2Gym) | ✅ 确认 · ★67 |
| **ClawEnvKit** | 开放式环境工具包：支持任务与 harness 生成及评测 | 2026-03 | [xirui-li/ClawEnvKit](https://github.com/xirui-li/ClawEnvKit) | ✅ 确认 · ★65 |
| **Seahaven** | 为 AI Agent 构建合成世界的框架，用于 RL 训练与评测 | 2026-09 | [Kiln-AI/Seahaven](https://github.com/Kiln-AI/Seahaven) | ✅ 确认 · ★61 |
| **agentenv-framework** | 面向多角色协作（研究者 / 工程师 / 领域专家）构建真实 RL 环境的基础设施 | 2026-09 | [scaleapi/agentenv-framework](https://github.com/scaleapi/agentenv-framework) | ✅ 确认 · ★448 |
| **AgentArk** | 通用环境框架，面向可扩展的多模态 Agent 评测与 RL | 2025-08 | [P90-RushB/AgentArk](https://github.com/P90-RushB/AgentArk) | ✅ 确认 · ★310 |
| **archipelago** | 运行与评测 AI Agent 的 harness，对接多种 RL 环境 | 2026-01 | [Mercor-Intelligence/archipelago](https://github.com/Mercor-Intelligence/archipelago) | ✅ 确认 · ★307 |
| **hud-python** | Agent 的 RL 环境与评测集合，「定义一次，可训练任意模型」 | 2025-03 | [hud-evals/hud-python](https://github.com/hud-evals/hud-python) | ✅ 确认 · ★330 |
| **Dressage** | 面向任意 Agent 与沙箱的可扩展 RL 训练框架 | 2026-06 | [Accio-Lab/Dressage](https://github.com/Accio-Lab/Dressage) | ✅ 确认 · ★822 |
| **agentcore-rl-toolkit** | 可组合的真实 Agent RL 工具包（基于 Bedrock AgentCore） | 2025-12 | [awslabs/agentcore-rl-toolkit](https://github.com/awslabs/agentcore-rl-toolkit) | ✅ 确认 · ★123 |
| **SWE-MiniSandbox** | 无容器的 RL 框架，用于训练软件工程 Agent | 2025-12 | [lblankl/SWE-MiniSandbox](https://github.com/lblankl/SWE-MiniSandbox) | ✅ 确认 · ★87 |
| **tbench-agentic-data-pipeline** | 多 Agent 合成数据流水线，生成并校验长程终端 / 编码轨迹 | 2025-07 | [Danau5tin/tbench-agentic-data-pipeline](https://github.com/Danau5tin/tbench-agentic-data-pipeline) | ✅ 确认 · ★76 |
| **rl-env-use** | 从 Browser Use Agent 在真实网页中挖掘的案例，构建任意领域的 RL 环境 | 2026-10 | [browser-use/rl-env-use](https://github.com/browser-use/rl-env-use) | ✅ 确认 · ★171 |
| **Agentix** | Agent 与环境之间的通用桥接：在任意沙箱中评测、RL 训练与追踪 Agent | 2026-04 | [Agentix-Project/Agentix](https://github.com/Agentix-Project/Agentix) | ✅ 确认 · ★78 |
| **shepherd** | 把 Agent 执行过程转成可回滚、类 Git 的轨迹运行时，让「元 Agent」观察与重放执行 | 2026-06 | [shepherd-agents/shepherd](https://github.com/shepherd-agents/shepherd) | ✅ 确认 · ★2.7k |
| **envd** | 为人与 Agent 提供可复现的开发环境 | 2022-04 | [tensorchord/envd](https://github.com/tensorchord/envd) | ✅ 确认 · ★2.3k |
| **celesto** | 面向编码 Agent、CI 与 RL 训练的沙箱 | 2026-02 | [CelestoAI/celesto](https://github.com/CelestoAI/celesto) | ✅ 确认 · ★1.9k |
| **MAI-Gym** | 覆盖移动端与桌面环境的 GUI Agent 评测与 RL 训练一体化开放平台 | 2026-10 | [Tongyi-MAI/MAI-Gym](https://github.com/Tongyi-MAI/MAI-Gym) | ✅ 确认 · ★59 |
| **SimEHR** | 高保真电子病历（EHR）环境，用于 CUA 在医疗信息系统中的训练与评测 | 2026-11 | [HealthRex/SimEHR](https://github.com/HealthRex/SimEHR) | ✅ 确认 · ★70 |
| **mcpmark** | 压力测试型 MCP 基准，评测模型与 Agent 在 MCP 生态中的能力 | 2025-07 | [eval-sys/mcpmark](https://github.com/eval-sys/mcpmark) | ✅ 确认 · ★475 |
| **mcp-bench** | 通过 MCP Server 上的真实复杂任务评测工具使用型 Agent | 2025-08 | [Accenture/mcp-bench](https://github.com/Accenture/mcp-bench) | ✅ 确认 · ★517 |
| **LiveMCPBench** | 大规模 MCP 工具生态下的 Agent 导航与使用能力基准 | 2025-08 | [icip-cas/LiveMCPBench](https://github.com/icip-cas/LiveMCPBench) | ✅ 确认 · ★106 |
| **MCPToolBench++** | MCP 协议下的工具使用基准，覆盖 Agent 与模型的工具调用能力 | 2025-07 | [mcp-tool-bench/MCPToolBenchPP](https://github.com/mcp-tool-bench/MCPToolBenchPP) | ✅ 确认 · ★46 |
| **Meta Agents Research Environments** | 在动态、真实环境中评测 AI Agent 的综合平台 | 2025-09 | [facebookresearch/meta-agents-research-environments](https://github.com/facebookresearch/meta-agents-research-environments) | ✅ 确认 · ★582 |
| **Qwen-AgentWorld** | 面向通用 Agent 的语言世界模型开源实现 | 2026-06 | [QwenLM/Qwen-AgentWorld](https://github.com/QwenLM/Qwen-AgentWorld) | ✅ 确认 · ★1k |
| **awesome-agentic-world-modeling** | Agentic 世界建模的清单型综述仓库（基础、能力、定律与展望） | 2026-04 | [matrix-agent/awesome-agentic-world-modeling](https://github.com/matrix-agent/awesome-agentic-world-modeling) | ✅ 确认 · ★340 |
| **tarit** | 面向自托管 AI Agent 与 RL 的 hypervisor 与沙箱云 | 2026-07 | [instavm/tarit](https://github.com/instavm/tarit) | ✅ 确认 · ★91 |
| **RedTeamCUA** | 混合 Web-OS 环境中的 CUA 对抗性测试（ICLR'26 Oral） | 2025-05 | [OSU-NLP-Group/RedTeamCUA](https://github.com/OSU-NLP-Group/RedTeamCUA) | ✅ 确认 · ★68 |
| **MemGUI-Bench** | 动态环境中移动 GUI Agent 的记忆能力基准（ACM MM 2026） | 2026-02 | [lgy0404/MemGUI-Bench](https://github.com/lgy0404/MemGUI-Bench) | ✅ 确认 · ★55 |
| **VAGEN** | 面向多轮 VLM Agent 的世界模型强化学习框架（NeurIPS 2025） | 2025-03 | [mll-lab-nu/VAGEN](https://github.com/mll-lab-nu/VAGEN) | ✅ 确认 · ★525 |
| **MedResearcher-R1** | 基于知识引导轨迹合成的医疗场景 deep research Agent | 2025-08 | [AQ-MedAI/MedResearcher-R1](https://github.com/AQ-MedAI/MedResearcher-R1) | ✅ 确认 · ★526 |
| **OS-Sentinel** | 移动 GUI Agent 的安全增强与混合验证环境（ACL 2026） | 2025-07 | [OS-Copilot/OS-Sentinel](https://github.com/OS-Copilot/OS-Sentinel) | ✅ 确认 · ★51 |
| **LLM-MM-Agent** | 把 LLM 作为 Agent 求解真实数学建模问题（NeurIPS 2025） | 2025-05 | [usail-hkust/LLM-MM-Agent](https://github.com/usail-hkust/LLM-MM-Agent) | ✅ 确认 · ★702 |

---

## 十七、代表性工作要点摘要

| 工作 | 方法 | 规模 / 实验结果 |
|---|---|---|
| **Agent-World**（智源 / TARS） | 基于工具依赖图与可执行 Python 求解的任务合成，难度可控；多环境闭环 RL + GRPO；自演化竞技场 | 1,978 个环境 / 20 类 / 19,822 个工具；8B / 14B 模型训练后超越多个闭源模型 |
| **EnvScaler**（人大） | SkelBuilder（环境骨架：可执行程序 + 文档 + 工具接口，双 Agent 评估）+ ScenGenerator（场景 / 任务 / 终态校验函数） | 191 个环境 / 约 7K 场景；SFT 后 BFCL-MT 提升 +8.67、ACEBench-Agent 提升 +11.57 |
| **InfiniteWeb** | 可扩展 Web 环境合成，面向 GUI Agent 域内泛化 | 将合成网站迁移至真实网页进行泛化测试 |
| **Agent-World Model** | 面向无限合成环境的 Agentic RL | 1,000 个可执行 SQLite + MCP 环境；仅用合成环境训练后在三个 OOD 基准上泛化良好；已合入 meta-pytorch/OpenEnv |
| **ToolVerse** | 大规模工具环境 + 长程任务 | 约 400 个 MCP servers / 约 4,500 个 tools；环境多样性带来的收益大于单纯增加 rollout 数量，BFCL-v3 / τ²-Bench 显著提升 |
| **WildAWM**（MSR 等） | 合成"个人电脑"世界（GUI + MCP + CLI）→ 出题 + 验证器 → 五道质量关卡筛选 → RL 训练 | 36 人物 / 640 世界 / 平均 17 万条 DB 记录；341 个合格环境-任务对；仅用开源模型，8 个 OOD 基准全面提升（35B-A3B 平均 +10.58 分） |
| **SynthAPI（Scaling Laws for Tool-Use Agents）** | 显式控制工具 / 任务 / 数据库三维多样性 | 458,752 条任务 × 84 个环境，给出工具使用 Agent 的环境扩展 scaling law |
| **CodeMidas** | 以源码为唯一任务来源构造 RL 环境 | 摆脱 issue / commit 等开发过程工件的限制，扩大可提取任务范围 |
| **POSEIDON** | 从科学代码仓库抽取可验证训练环境 | 同等仓库预算下环境数约为先前方法的 10 倍 |
| **AgentDrive** | LLM prompt 生成 JSON 驾驶场景 | 30 万个驾驶场景；[arXiv:2601.16964](https://arxiv.org/abs/2601.16964) |
| **Agentick** | 程序化生成 37 个任务，Gymnasium 接口 + oracle 策略 + SFT 数据 | 用于通用序贯决策评测；[arXiv:2605.06869](https://arxiv.org/abs/2605.06869) |
| **Survey: Scaling Environments for LLM Agents** | 提出 GEF loop（任务生成—执行—反馈），并给出统一分类框架 | 从环境中心视角进行综述 |
| **Survey: Agentic Environment Engineering** | 从生命周期（建模 → 合成 → 评估 → 应用）系统分类，区分符号合成与神经合成 | [arXiv:2606.12191](https://arxiv.org/abs/2606.12191) |

---

## 十八、Awesome 清单与聚合资源

| 资源 | 内容 | 链接 |
|---|---|---|
| **awesome-scaling-coding-agent-envs** | 面向编码 Agent 环境扩展的工具/论文/框架清单；三大支柱：自动环境搭建、可扩展实例合成、自博弈等新型训练范式 | [GitHub](https://github.com/jc-ryan/awesome-scaling-coding-agent-envs) |
| **Awesome-Agent-Environments** | 按任务/构建/执行层组织 Agent 环境总览，含 96+ 环境与框架仓库 | [GitHub](https://github.com/ZackZikaiXiao/Awesome-Agent-Environments) |
| **Awesome-Agentic-Environments** | 关注环境可复现性、沙箱基建、供应商与产业报告 | [GitHub](https://github.com/TraceLite-AI/Awesome-Agentic-Environments) |
| **Awesome Workplace Agent Environments** | 职场 Agent 环境/基准/数据集清单；20 环境 + 15 生成与训练资源 + 9 数据集 + 5 供应商；含中英双语与 BibTeX | [GitHub](https://github.com/gumlau/awesome-workplace-agent-environments) |
| **AgentsMeetRL** | 开源 Agentic RL 项目，含框架、算法、奖励与环境细节 | [GitHub](https://github.com/thinkwee/AgentsMeetRL) |
| **Awesome-AgenticLLM-RL-Papers** | Agentic RL 综述配套阅读清单（含环境与框架） | [GitHub](https://github.com/HHHHHejia/Awesome-AgenticLLM-RL-Papers) |
| **Awesome-LLM-Synthetic-Data** | LLM 生成合成数据的阅读清单 | [GitHub](https://github.com/wasiahmad/Awesome-LLM-Synthetic-Data) |
| **acu（trycua）** | 计算机使用 Agent 的论文、项目与框架合集 | [GitHub](https://github.com/trycua/acu) |
| **AI Agent Benchmark Compendium** | 按工具、通用辅助、编码等分类的 Agent 基准合集 | [GitHub](https://github.com/philschmid/ai-agent-benchmark-compendium) |
| **Benchmark Radar** | AI 基准活数据库（14,810+ 记录 / 37 来源），提供 Dashboard、CLI、RSS 与数据集下载 | [GitHub](https://github.com/ktwu01/benchmark-radar) · [Dashboard](https://benchmark-radar.org/) |

---

## 附：常用环境与基准仓库速查

| 类别 | 仓库 |
|---|---|
| 环境框架 / 基建 | [meta-pytorch/OpenEnv](https://github.com/meta-pytorch/OpenEnv)、[PrimeIntellect-ai/verifiers](https://github.com/PrimeIntellect-ai/verifiers)、[laude-institute/harbor](https://github.com/laude-institute/harbor)、[agent-infra/sandbox](https://github.com/agent-infra/sandbox)、[kubernetes-sigs/agent-sandbox](https://github.com/kubernetes-sigs/agent-sandbox)、[alibaba/OpenSandbox](https://github.com/alibaba/OpenSandbox)、[e2b-dev/E2B](https://github.com/e2b-dev/E2B)、[inclusionAI/AEnvironment](https://github.com/inclusionAI/AEnvironment) |
| 环境合成项目 | [Snowflake-Labs/agent-world-model](https://github.com/Snowflake-Labs/agent-world-model)、[RUC-NLPIR/EnvScaler](https://github.com/RUC-NLPIR/EnvScaler)、[Gen-Verse/GenEnv](https://github.com/Gen-Verse/GenEnv)、[ModalMinds/gym-v](https://github.com/ModalMinds/gym-v)、[AMAP-ML/Code2World](https://github.com/AMAP-ML/Code2World)、[MSR-Orchard/WildAWM](https://github.com/MSR-Orchard/WildAWM)、[camel-ai/seta](https://github.com/camel-ai/seta)、[emrecanacikgoz/Tool-R0](https://github.com/emrecanacikgoz/Tool-R0)、[TheAgentArk/Toucan](https://github.com/TheAgentArk/Toucan)、[huggingface/Repo2RLEnv](https://github.com/huggingface/Repo2RLEnv)、[Wusiwei0410/TerminalTraj](https://github.com/Wusiwei0410/TerminalTraj) |
| 编码 / SWE 环境 | [SWE-bench/SWE-smith](https://github.com/SWE-bench/SWE-smith)、[SWE-Gym/SWE-Gym](https://github.com/SWE-Gym/SWE-Gym)、[R2E-Gym/R2E-Gym](https://github.com/R2E-Gym/R2E-Gym)、[RUCAIBox/SWE-World](https://github.com/RUCAIBox/SWE-World)、[r2e-project/r2e](https://github.com/r2e-project/r2e)、[DeepSoftwareAnalytics/swe-factory](https://github.com/DeepSoftwareAnalytics/swe-factory)、[yiqingxyq/RepoST](https://github.com/yiqingxyq/RepoST)、[bytedance/Repo2Run](https://github.com/bytedance/Repo2Run)、[JetBrains-Research/EnvBench](https://github.com/JetBrains-Research/EnvBench)、[EuniAI/HerAgent](https://github.com/EuniAI/HerAgent)、[FSoft-AI4Code/SWE-Synth](https://github.com/FSoft-AI4Code/SWE-Synth)、[Hambaobao/SWE-Flow](https://github.com/Hambaobao/SWE-Flow)、[neulab/SWE-Playground](https://github.com/neulab/SWE-Playground)、[microsoft/RepoLaunch](https://github.com/microsoft/RepoLaunch)、[TencentYoutuResearch/EnConda-Bench](https://github.com/TencentYoutuResearch/EnConda-Bench) |
| 环境搭建 / 沙箱 | [microsoft/debug-gym](https://github.com/microsoft/debug-gym)、[OpenAutoCoder/live-swe-agent](https://github.com/OpenAutoCoder/live-swe-agent)、[logic-star-ai/swt-bench](https://github.com/logic-star-ai/swt-bench)、[IBM/TDD-Bench-Verified](https://github.com/IBM/TDD-Bench-Verified)、[aisa-group/PostTrainBench](https://github.com/aisa-group/PostTrainBench)、[OpenHands/critic-rubrics](https://github.com/OpenHands/critic-rubrics)、[sola-st/ExecutionAgent](https://github.com/sola-st/ExecutionAgent)、[test-generation/issue2test](https://github.com/test-generation/issue2test)、[cuhk-shenzhen-se/utboost](https://github.com/cuhk-shenzhen-se/utboost) |
| 基准 / 仿真环境 | [sierra-research/tau2-bench](https://github.com/sierra-research/tau2-bench)、[StonyBrookNLP/appworld](https://github.com/StonyBrookNLP/appworld)、[xlang-ai/OSWorld](https://github.com/xlang-ai/OSWorld)、[google-research/android_world](https://github.com/google-research/android_world)、[microsoft/WindowsAgentArena](https://github.com/microsoft/WindowsAgentArena)、[web-arena-x/webarena](https://github.com/web-arena-x/webarena)、[web-arena-x/visualwebarena](https://github.com/web-arena-x/visualwebarena)、[web-arena-x/webarena-infinity](https://github.com/web-arena-x/webarena-infinity)、[ServiceNow/WorkArena](https://github.com/ServiceNow/WorkArena)、[ServiceNow/BrowserGym](https://github.com/ServiceNow/BrowserGym)、[ServiceNow/DoomArena](https://github.com/ServiceNow/DoomArena)、[ServiceNow/GroundCUA](https://github.com/ServiceNow/GroundCUA)、[ethz-spylab/agentdojo](https://github.com/ethz-spylab/agentdojo)、[SalesforceAIResearch/MCP-Universe](https://github.com/SalesforceAIResearch/MCP-Universe)、[laude-institute/terminal-bench](https://github.com/laude-institute/terminal-bench)、[apple/ToolSandbox](https://github.com/apple/ToolSandbox)、[OS-Copilot/OS-Genesis](https://github.com/OS-Copilot/OS-Genesis)、[OS-Copilot/ScienceBoard](https://github.com/OS-Copilot/ScienceBoard)、[QuantaAlpha/GitTaskBench](https://github.com/QuantaAlpha/GitTaskBench)、[web-arena-x/webarena-infinity](https://github.com/web-arena-x/webarena-infinity)、[Tongyi-MAI/MobileWorld](https://github.com/Tongyi-MAI/MobileWorld) |

---

*最后更新：2026-11-23 ｜ 本轮基于 arXiv API 全量检索（64 组关键词、2021-11 至 2026-11）新增 276 篇论文与 43 个开源项目，并新增四个分类章节*
