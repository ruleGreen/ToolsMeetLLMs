# Empowering LLMs: Tool Learning with Real-World Interactions

This is the official repo for SIGIR 2024 tutorial: Empowering LLMs: Tool Learning with Real-World Interactions. More details can be found in https://rulegreen.github.io/services/tools-meet-llm/

We record the recent progress of tool learning based on LLMs. We list works following the structure of tutorail, and will constantly update it, welcome to raise a issue to add new works!!

## Table of Contents

<details open>
<summary>table of contents</summary>

- [0 Survey](#0-survey)
- [1 Defnition and Scope of Tools](#1-definition-and-scope-of-tools)
  - [1.1 Cognitive Tools](#11-cognitive-tools)
  - [1.2 Physical Tools](#12-physical-tools)
- [2 Components and Architecture of Tool Learning](#2-components-and-architecture-of-tool-learning)
  - [2.1 Tool Set](#21-tool-set)
  - [2.2 Controller/Planner](#22-controller)
  - [2.3 Environments](#23-environment)
  - [2.4 Perceiver](#24-perceiver)
- [3 Tool Learning based on LLMs](#3-tool-learning-based-on-llms)
  - [3.1 Tool-oriented Learning](#31-tool-oriented-learning)
  - [3.2 Tool-augmented Learning](#32-tool-augmented-learning)
  - [3.3 Learning of Tool Learning](#33-learning-of-tool-learning)
- [4 Application of Tool Learning](#4-application-of-tool-learning)
  - [4.1 Tool Creation, Selection and Utilization](#41-tool-creation-selection-and-utilization)
  - [4.2 Tool Learning in IR](#42-tool-learning-in-ir)
  - [4.3 Tool Learning in Embodied Env](#43-tool-learning-in-embodied-env)
- [5 Advanced Topics and Future Directions](#5-advanced-topics-and-future-directions)
  - [5.1 Multi-modal and Multi-agent Tool Learning](#51-multi-modal-and-multi-agent-tool-learning)
  - [5.2 Safe, Trsutworthy and Personalized Tool Learning](#52-safe-trustworthy-and-personalized-tool-learning)
  - [5.3 Emerging Trends and Future Opportunities](#53-emerging-trends-and-future-opportunities)

</details>

## 0 Survey

- [Tool Learning with Large Language Models: A Survey](https://arxiv.org/abs/2405.17935) `2024/05`

- [What Are Tools Anyway? A Survey from the Language Model Perspective](https://arxiv.org/pdf/2403.15452) `2024/03`

- [Augmented language models: a survey](https://arxiv.org/abs/2302.07842)

- [Tool Learning with Foundation Models](https://arxiv.org/abs/2304.08354) `2023/04`

- [Interactive Natural Language Processing](https://arxiv.org/pdf/2305.13246)

- [A Survey on Large Language Model based Autonomous Agents](https://arxiv.org/pdf/2308.11432)

- [The Rise and Potential of Large Language Model Based Agents: A Survey](https://arxiv.org/pdf/2309.07864)
- [If LLM Is the Wizard, Then Code Is the Wand: A Survey on How Code Empowers Large Language Models to Serve as Intelligent Agents](https://arxiv.org/pdf/2401.00812)

- [Agent AI: Surveying the Horizons of Multimodal Interaction](https://arxiv.org/pdf/2401.03568)

- [Personal LLM Agents: Insights and Survey about the Capability, Efficiency and Security](https://arxiv.org/pdf/2401.05459)

## 1 Defnition and Scope of Tools

<details open>
<summary>defnition and scope of tools</summary>

- [0 Cognitive Tools](#0-cognitive-tools)
- [1 Physical Tools](#1-physical-tools)

</details>

### 1.1 Cognitive Tools

<details open>
<summary>relevant cognitive tools</summary>


- [TPE: Towards Better Compositional Reasoning over Conceptual Tools with Multi-persona Collaboration](https://arxiv.org/abs/2309.16090.pdf) :fire::fire::fire:

- [Large Language Models as Source Planner for Personalized Knowledge-grounded Dialogues](https://aclanthology.org/2023.findings-emnlp.641/) :fire::fire::fire:

- [StrategyLLM: Large Language Models as Strategy Generators, Executors, Optimizers, and Evaluators for Problem Solving](https://arxiv.org/pdf/2311.08803.pdf)

- [Meta Reasoning for Large Language Models](https://arxiv.org/pdf/2406.11698v1)

- [Meta-Reasoning: Monitoring and Control of Thinking and Reasoning](https://pdf.sciencedirectassets.com/271877/1-s2.0-S1364661316X00095/1-s2.0-S1364661317301055/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEIT%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJHMEUCIQDLJD9QHT4cwiLvZdyEmv0YHEKVMPc8cv198ayZ43%2B2GAIgf9u4NXgQJnNFXrxS%2FSE%2BsX2p%2BpnUVILjW48I%2BknQ7tgqswUILRAFGgwwNTkwMDM1NDY4NjUiDIl%2FeKcmRxSAy3DU5SqQBZyegI5NiRxKBioMP59P9NBWEG%2Ffzag5tHuyJO4xY5BM7duXcxRf6C9t7BDnMC12LYtTvj0ZxCXhZUpEpnw3hi7COD%2Bc1j4Nc8huxpfmUCBjhq9QQrJptHaK7PSr%2BzZ9lLp5VkzNdohI3b1d%2BKO9j1KBNRDSE0NIFzWLNAEn5AokCNVxLy%2BlNroV8cuDj90f1MPfudb2%2BA5jnE6VGzKBTrOR%2Fc1JQZuCABZgvujxQ81AqokvlLaIhSA1H5UTaF%2BjmJALkTr52ODOj%2FcxSqdLw%2BbdHicOTjCIxlDgMm9BDdhRNsH13RBgcoFpZfqBWOaayA3p01L1wjsuZje7oGzWsWDB6H8jk3mMvY%2BlgTNE5pqZyigcsOibyypwFD8KBJMHRiYvx88GhcH90H%2Btn7XvLUzPfY3midZA79Z5BYNcsjyRmQ2FmkVrigeXXgJ8DRDmjomyZQe4F4GjVMPLp5yOyUi5AJRhNAnvtg5ijfReDonqDXe%2FF8pgSykLizVwf%2BhRwi8rC13yP0d2wm%2F6bT%2F8uLFIGutyzoe7xgX4Ml7pQg2RJhWaLQMXRooCHtHPA6KR9hAo8DYoWzFbIF1Jv6CaHCm2wnCG4CW86RgtUPcdGRAKi4BtI0RtejMNL3mbmmthSyjB0KOtS%2FgFsy1qGx%2BoV%2FNyq%2BNOs7HvEMr3bs%2Fp4CvojucUqvUv6bh4JiYd1y3FiAhXfnVY5wCEZMgdtbv6UvlCIRVzDqsLO2ABvGr%2Fded26WGOg54xHGUXfkwmiLZ1SReOMXehtVSL5Tk0Bpl%2BmcYd8WhxwGACl84T4unio4MmppBBO4cTiVPqHc5XzazPzWShM%2F8FtGXkHPqOkjHLS6XDuYkxmf%2BVcsdxOzWtVxtBMOqEy7MGOrEBO7RAs1QufMTHrz93W2asJsZqOUVttsNSlHpHilKwqVWML7c%2F%2F6INDauo9qEaK%2BHEoFO5qE%2FgYJBlqiPLq61tSG08Bs%2BnuiagQorWXBE%2Fn3pIew9eLJ4w0ehapVmfuySG7dQ1XdJL9frc8Ma0kU9pcon1Y9maVN1YD8T%2FeuEQpzPBW3NSO2%2FhJLINeGI3lf%2BYE9nFttqAx99P3gcUBMNDBgrUNN3dvvoS6bIndWIuc90e&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20240619T122257Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYSPAYTPRF%2F20240619%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=22ffc90b4d00d5a79d1bf1266b0e67fe03aa3ce7d3e663b2d186b91f23bf8da0&hash=a18b2a25b071c242e7931e03c9120639a858e842907c64b4e5f5a64731eb860d&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S1364661317301055&tid=spdf-d8aaa253-1764-4563-9064-d1a68a0dfa56&sid=babac21183ae03428f6b2bd22294cead2623gxrqb&type=client&tsoh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&ua=0100565752535003010a&rr=89637ccdaa28075d&cc=gb) :fire::fire::fire::fire::fire: personally like this

</details>

### 1.2 Physical Tools

<details open>
<summary>relevant physical tools</summary>

- [API-Bank: A Comprehensive Benchmark for Tool-Augmented LLMs](https://aclanthology.org/2023.emnlp-main.187.pdf) 🔥🔥🔥 important work, also for dialogues

- [Toolformer: Language Models Can Teach Themselves to Use Tools](https://arxiv.org/abs/2302.04761)

- [TravelPlanner: A Benchmark for Real-World Planning with Language Agents](https://arxiv.org/pdf/2402.01622)

- [ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs](https://arxiv.org/abs/2307.16789.pdf)

</details>

## 2 Components and Architecture of Tool Learning

### 2.1 Tool Set

see above

### 2.2 Controller

- [Chameleon: Plug-and-Play Compositional Reasoning with Large Language Models](https://arxiv.org/abs/2304.09842.pdf)

- [ToolAlpaca: Generalized Tool Learning for Language Models with 3000 Simulated Cases](https://arxiv.org/pdf/2306.05301) multi-modal

- [ReWOO: Decoupling Reasoning from Observations for Efficient Augmented Language Models](https://arxiv.org/pdf/2305.18323)

- [ART: Automatic multi-step reasoning and tool-use for large language models](https://arxiv.org/pdf/2303.09014)

- [Toolformer: Language Models Can Teach Themselves to Use Tools](https://arxiv.org/pdf/2302.04761.pdf)

- [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629.pdf)

- [Self-Refine: Iterative Refinement with Self-Feedback](https://arxiv.org/pdf/2303.17651)

- [Teaching Large Language Models to Self-Debug](https://arxiv.org/pdf/2304.05128)

- [WizardLM: Empowering Large Language Models to Follow Complex Instructions](https://arxiv.org/pdf/2304.12244)

- [FrugalGPT: How to Use Large Language Models While Reducing Cost and Improving Performance](https://arxiv.org/pdf/2305.05176)

- [Tree of Thoughts: Deliberate Problem Solving with Large Language Models](https://arxiv.org/pdf/2305.10601)

- [Knowledge-enhanced Agents for Interactive Text Games](https://arxiv.org/pdf/2305.05091)

- [SwiftSage: A Generative Agent with Fast and Slow Thinking for Complex Interactive Tasks](https://arxiv.org/pdf/2305.17390)

- [AdaPlanner: Adaptive Planning from Feedback with Language Models](https://arxiv.org/pdf/2305.16653)

- [Plan-and-Solve Prompting: Improving Zero-Shot Chain-of-Thought Reasoning by Large Language Models](https://arxiv.org/pdf/2305.04091)

- [Enabling Intelligent Interactions between an Agent and an LLM: A Reinforcement Learning Approach](https://arxiv.org/pdf/2306.03604)

- [User Behavior Simulation with Large Language Model based Agents](https://arxiv.org/pdf/2306.02552)

- [Towards A Unified Agent with Foundation Models](https://arxiv.org/pdf/2307.09668)

- [A Real-World WebAgent with Planning, Long Context Understanding, and Program Synthesis]()

- [PanGu-Coder2: Boosting Large Language Models for Code with Ranking Feedback](https://arxiv.org/abs/2307.14936)

- [Retroformer: Retrospective Large Language Agents with Policy Gradient Optimization](https://arxiv.org/pdf/2308.02151)

- [SelfCheck: Using LLMs to Zero-Shot Check Their Own Step-by-Step Reasoning](https://arxiv.org/pdf/2308.00436)

- [ExpeL: LLM Agents Are Experiential Learners](https://arxiv.org/pdf/2308.10144)

- [ReST meets ReAct: Self-Improvement for Multi-Step Reasoning LLM Agent](https://arxiv.org/abs/2312.10003)

- [Self-Contrast: Better Reflection Through Inconsistent Solving Perspectives](https://arxiv.org/abs/2401.02009)

- [Agent-Pro: Learning to Evolve via Policy-Level Reflection and Optimization](https://arxiv.org/pdf/2402.17574)

- [AutoAct: Automatic Agent Learning from Scratch for QA via Self-Planning](https://arxiv.org/abs/2401.05268)

- [SOTOPIA-π: Interactive Learning of Socially Intelligent Language Agents](https://arxiv.org/pdf/2403.08715)

- [AutoGuide: Automated Generation and Selection ofState-Aware Guidelines for Large Language Model Agents](https://arxiv.org/pdf/2403.08978)

### 2.3 Environments / Benchmarks

- [ToolEyes: Fine-Grained Evaluation for Tool Learning Capabilities of Large Language Models in Real-world Scenarios](https://arxiv.org/abs/2401.00741.pdf)

- [CToolEval: A Chinese Benchmark for LLM-Powered Agent Evaluation in Real-World API Interactions] chinese benchmark

- [TOOLTALK: EVALUATING TOOL USAGE IN A CONVERSATIONAL SETTING](https://arxiv.org/abs/2311.10775.pdf)

- [MINT: Evaluating llms in multi-turn interaction with tools and language feedback](https://arxiv.org/abs/2309.10691.pdf)

- [Metatool benchmark for large language models: Deciding whether to use tools and which to use](https://arxiv.org/abs/2310.03128.pdf)

### 2.4 Perceiver

- [Self-Contrast: Better Reflection Through Inconsistent Solving Perspectives](https://arxiv.org/pdf/2401.02009.pdf)

- [Agent-Pro: Learning to Evolve via Policy-Level Reflection and Optimization](https://arxiv.org/abs/2402.17574.pdf)

- [CRITIC: LARGE LANGUAGE MODELS CAN SELFCORRECT WITH TOOL-INTERACTIVE CRITIQUING](https://arxiv.org/pdf/2305.11738) first to use external feedback from tools to critic/refine outputs of LLMs? [[code](https://github.com/microsoft/ProphetNet/tree/master/CRITIC)]

- [Reflexion: Language Agents with Verbal Reinforcement Learning](https://arxiv.org/abs/2303.11366)

- [Chat with the Environment: Interactive Multimodal Perception Using Large Language Models](https://arxiv.org/pdf/2303.08268)


## 3 Tool Learning based on LLMs

### 3.1 Tool-oriented Learning

* [A Real-World WebAgent with Planning, Long Context Understanding, and Program Synthesis](https://arxiv.org/pdf/2307.12856)

### 3.2 Tool-augmented Learning

* [JARVIS-1: Open-World Multi-task Agents with Memory-Augmented Multimodal Language Models](https://arxiv.org/pdf/2311.05997)

* [Chain of Code: Reasoning with a Language Model-Augmented Code Emulator](https://arxiv.org/pdf/2312.04474)

* [KnowAgent: Knowledge-Augmented Planning for LLM-Based Agents](https://arxiv.org/pdf/2403.03101)

* [ChatCoT: Tool-Augmented Chain-of-Thought Reasoning on Chat-based Large Language Models](https://arxiv.org/abs/2305.14323)

### 3.3 Learning of Tool Learning

- [GPT4Tools: Teaching Large Language Model to Use Tools via Self-instruction](https://arxiv.org/pdf/2305.18752.pdf)

- [Making Language Models Better Tool Learners with Execution Feedback](https://arxiv.org/abs/2305.13068)

## 4 Application of Tool Learning

### 4.1 Tool Creation Selection and Utilization

#### Tool Creation

- [LARGE LANGUAGE MODELS AS TOOL MAKERS](https://arxiv.org/abs/2305.17126.pdf)

- [Craft: Customizing llms by creating and retrieving from specialized toolsets](https://arxiv.org/pdf/2309.17428.pdf)

- [CREATOR: Tool Creation for Disentangling Abstract and Concrete Reasoning of Large Language Models](https://aclanthology.org/2023.findings-emnlp.462/)

#### Tool Selection and Utilization

- [EASYTOOL: ENHANCING LLM-BASED AGENTS WITH CONCISE TOOL INSTRUCTION](https://openreview.net/pdf?id=3TuG3S68bb) optimizate tool documentation

- [TOOLVERIFIER: Generalization to New Tools via Self-Verification](https://arxiv.org/pdf/2402.14158) finetune a model to select tool based on desc, and propose questions to self-refine decisions

- [TPTU-v2: Boosting Task Planning and Tool Usage of Large Language Model-based Agents in Real-world Systems](https://openreview.net/pdf?id=8rfeWF4ZNt) `ICLR2024`

- [CRUXEval: A Benchmark for Code Reasoning Understanding and Execution](https://arxiv.org/abs/2401.03065.pdf)

- [Toolrerank: Adaptive and hierarchy-aware reranking for tool retrieval](https://aclanthology.org/2024.lrec-main.1413/)

- [Empowering Large Language Model Agents through Action Learning](https://arxiv.org/abs/2402.15809)


### 4.2 Tool Learning in IR

- [UniMS-RAG: A Unified Multi-source Retrieval-Augmented Generation for Personalized Dialogue Systems](https://arxiv.org/abs/2401.13256.pdf) :fire::fire::fire:

- [Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection](https://arxiv.org/abs/2310.11511.pdf) :fire::fire::fire::fire::fire:

- [UniRetriever: Multi-task Candidates Selection for Various Context-Adaptive Conversational Retrieval](https://arxiv.org/abs/2402.16261.pdf)

- [Active Retrieval Augmented Generation](https://aclanthology.org/2023.emnlp-main.495/) `EMNLP 2023` :fire::fire::fire: interesting and useful -> may can be used in dialogues

- [I^3 Retriever: Incorporating Implicit Interaction in Pre-trained Language Models for Passage Retrieval](https://arxiv.org/abs/2306.02371)

- [Learning Retrieval Augmentation for Personalized Dialogue Generation](https://aclanthology.org/2023.emnlp-main.154.pdf) `EMNLP 2023`

- [PK-ICR: Persona-Knowledge Interactive Multi-Context Retrieval for Grounded Dialogue](https://aclanthology.org/2023.emnlp-main.1020.pdf) `EMNLP 2023`

- [Interleaving Retrieval with Chain-of-Thought Reasoning for Knowledge-Intensive Multi-Step Questions](https://aclanthology.org/2023.acl-long.557.pdf) `ACL 2023`

- [Self-Knowledge Guided Retrieval Augmentation for Large Language Models](https://aclanthology.org/2023.findings-emnlp.691/) `EMNLP 2023`


### 4.3 Tool Learning in Embodied Environment

- [A Solution-based LLM API-using Methodology for Academic Information Seeking](https://arxiv.org/abs/2405.15165)

- [Voyager: An Open-Ended Embodied Agent with Large Language Models](https://arxiv.org/abs/2305.16291.pdf) `2023.05`

- [SCIENCEWORLD: Is your Agent Smarter than a 5th Grader?](https://arxiv.org/abs/2203.07540.pdf)    `22.03` `Interactive Env`

- [ALFWorld: Aligning Text and Embodied Environments for Interactive Learning](https://arxiv.org/abs/2010.03768.pdf) `2020.10`

- [VirtualHome: Simulating Household Activities via Programs](https://arxiv.org/pdf/1806.07011.pdf)

- [On the tool manipulation capability of open-source large language models](https://arxiv.org/abs/2305.16504.pdf)

- [Code as Policies: Language Model Programs for Embodied Control](https://arxiv.org/pdf/2209.07753)

- [Plan4MC: Skill Reinforcement Learning and Planning for Open-World Minecraft Tasks](https://arxiv.org/pdf/2303.16563)

- [Plan, Eliminate, and Track -- Language Models are Good Teachers for Embodied Agents](https://arxiv.org/pdf/2305.02412)

- [Language Models Meet World Models: Embodied Experiences Enhance Language Models](https://arxiv.org/pdf/2305.10626)

- [Ghost in the Minecraft: Generally Capable Agents for Open-World Environments via Large Language Models with Text-based Knowledge and Memory](https://arxiv.org/pdf/2305.17144)

- [Reasoning with Language Model is Planning with World Model](https://arxiv.org/pdf/2305.14992)

- [An Embodied Generalist Agent in 3D World](https://arxiv.org/pdf/2311.12871)


### 4.4 Tool Learning for All

- [FACTOOL: Factuality Detection in Generative AI A Tool Augmented Framework for Multi-Task and Multi-Domain Scenarios](https://arxiv.org/abs/2307.13528.pdf) [[code](https://github.com/GAIR-NLP/factool)]

## 5 Advanced Topic and Future Directions

<details open>
<summary>defnition and scope of tools</summary>

- [0 Multi-modal and Multi-agent Tool Learning](#0-multi-modal-and-multi-agent-tool-learning)
- [1 Safe, Trustworthy and Personalized Tool Learning](#1-safe-trustworthy-and-personalized-tool-learning)
- [2 Emerging Trends and Future Opportunities](#2-emerging-trends-and-future-opportunities)

### 5.1 Multi-modal and Multi-agent Tool Learning

- [Scaling Large-Language-Model-based Multi-Agent Collaboration](https://arxiv.org/pdf/2406.07155.pdf) `multi-agent`

- [Mobile-Agent-v2: Mobile Device Operation Assistant with Effective Navigation via Multi-Agent Collaboration](https://arxiv.org/pdf/2406.01014.pdf)

- [MOBILE-AGENT: AUTONOMOUS MULTI-MODAL MOBILE DEVICE AGENT WITH VISUAL PERCEPTION](https://arxiv.org/pdf/2401.16158.pdf) `multi-modal`

- [WEBARENA: A REALISTIC WEB ENVIRONMENT FOR BUILDING AUTONOMOUS AGENTS](https://arxiv.org/abs/2307.13854.pdf) `multi-modal`



### 5.2 Safe, Trustworthy and Personalized Tool Learning

- [ToolSword: Unveiling Safety Issues of Large Language Models in Tool Learning Across Three Stages](https://arxiv.org/abs/2402.10753.pdf) `ACL 2024`


- [Watch Out for Your Agents! Investigating Backdoor Threats to LLM-Based Agent](https://arxiv.org/pdf/2402.11208.pdf)


### 5.3 Emerging Trends and Future Opportunities

- [Self-DC: When to retrieve and When to generate? Self Divide-and-Conquer for Compositional Unknown Questions](https://arxiv.org/abs/2402.13514.pdf) :fire::fire:

- [Knowledge Conflicts for LLMs: A Survey](https://arxiv.org/abs/2403.08319.pdf)

- [Metacognitive Retrieval-Augmented Large Language Models](https://arxiv.org/pdf/2402.11626.pdf) tools conflicts

- [TORA: A TOOL-INTEGRATED REASONING AGENT FOR MATHEMATICAL PROBLEM SOLVING](https://arxiv.org/pdf/2309.17452) :fire::fire::fire: [code]

</details>

```
@inproceedings{toolmeetllm,
        author = {Wang, Hongru and Qin, Yujia and Lin, Yankai and Pan, Jeff Z. and Wong, Kam-Fai},
        title = {Empowering Large Language Models: Tool Learning for Real-World Interaction},
        year = {2024},
        isbn = {9798400704314},
        publisher = {Association for Computing Machinery},
        address = {New York, NY, USA},
        url = {https://doi.org/10.1145/3626772.3661381},
        doi = {10.1145/3626772.3661381},
        abstract = {Since the advent of large language models (LLMs), the field of tool learning has remained very active in solving various tasks in practice, including but not limited to information retrieval. This half-day tutorial provides basic concepts of this field and an overview of recent advancements with several applications. In specific, we start with some foundational components and architecture of tool learning (i.e., cognitive tool and physical tool), and then we categorize existing studies in this field into tool-augmented learning and tool-oriented learning, and introduce various learning methods to empower LLMs this kind of capability. Furthermore, we provide several cases about when, what, and how to use tools in different applications. We end with some open challenges and several potential research directions for future studies. We believe this tutorial is suited for both researchers at different stages (introductory, intermediate, and advanced) and industry practitioners who are interested in LLMs and tool learning.},
        booktitle = {Proceedings of the 47th International ACM SIGIR Conference on Research and Development in Information Retrieval},
        pages = {2983–2986},
        numpages = {4},
        keywords = {language agents, large language models, tool learning},
        location = {Washington DC, USA},
        series = {SIGIR '24}
}
```
