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

- [Tool Learing with Large Language Models: A Survey](https://arxiv.org/abs/2405.17935) `2024/05`

- [What Are Tools Anyway? A Survey from the Language Model Perspective](https://arxiv.org/pdf/2403.15452) `2024/03`

- [Augmented language models: a survey](https://arxiv.org/abs/2302.07842)

- [Tool Learning with Foundation Models](https://arxiv.org/abs/2304.08354) `2023/04`

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


- [API-Bank: A Comprehensive Benchmark for Tool-Augmented LLMs](https://aclanthology.org/2023.emnlp-main.187.pdf) :fire::fire::fire: important work, also for dialogues

- [Toolformer: Language Models Can Teach Themselves to Use Tools](https://arxiv.org/abs/2302.04761)

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



### 2.3 Environments

- [MINT: Evaluating llms in multi-turn interaction with tools and language feedback](https://arxiv.org/abs/2309.10691.pdf)

- [Metatool benchmark for large language models: Deciding whether to use tools and which to use](https://arxiv.org/abs/2310.03128.pdf)


## Tool Learning based on LLMs


### Tool-oriented Learning



### Tool-augmented Learning


### Learning of Tool Learning

- [GPT4Tools: Teaching Large Language Model to Use Tools via Self-instruction](https://arxiv.org/pdf/2305.18752.pdf)


## Application of Tool Learning


### Tool Creation Selection and Utilization

- [CRUXEval: A Benchmark for Code Reasoning Understanding and Execution](https://arxiv.org/abs/2401.03065.pdf)

- [Toolrerank: Adaptive and hierarchy-aware reranking for tool retrieval](https://aclanthology.org/2024.lrec-main.1413/)

- [Craft: Customizing llms by creating and retrieving from specialized toolsets](https://arxiv.org/pdf/2309.17428.pdf)

- [CREATOR: Tool Creation for Disentangling Abstract and Concrete Reasoning of Large Language Models](https://aclanthology.org/2023.findings-emnlp.462/)



### Tool Learning in Embodied Environment

- [A Solution-based LLM API-using Methodology for Academic Information Seeking]

- [Voyager: An Open-Ended Embodied Agent with Large Language Models](https://arxiv.org/abs/2305.16291.pdf) `2023.05`

- [SCIENCEWORLD: Is your Agent Smarter than a 5th Grader?](https://arxiv.org/abs/2203.07540.pdf)    `22.03` `Interactive Env` 

- [ALFWorld: Aligning Text and Embodied Environments for Interactive Learning](https://arxiv.org/abs/2010.03768.pdf) `2020.10`

- [VirtualHome: Simulating Household Activities via Programs](https://arxiv.org/pdf/1806.07011.pdf)


- [On the tool manipulation capability of open-source large language models]


## Advanced Topic and Future Directions
<details open>
<summary>defnition and scope of tools</summary>

- [0 Multi-modal and Multi-agent Tool Learning](#0-multi-modal-and-multi-agent-tool-learning)
- [1 Safe, Trustworthy and Personalized Tool Learning](#1-safe-trustworthy-and-personalized-tool-learning)
- [2 Emerging Trends and Future Opportunities](#2-emerging-trends-and-future-opportunities)


### Multi-modal and Multi-agent Tool Learning

- [Scaling Large-Language-Model-based Multi-Agent Collaboration](https://arxiv.org/pdf/2406.07155.pdf) `multi-agent`

- [Mobile-Agent-v2: Mobile Device Operation Assistant with Effective Navigation via Multi-Agent Collaboration](https://arxiv.org/pdf/2406.01014.pdf)

- [MOBILE-AGENT: AUTONOMOUS MULTI-MODAL MOBILE DEVICE AGENT WITH VISUAL PERCEPTION](https://arxiv.org/pdf/2401.16158.pdf) `multi-modal`

- [WEBARENA: A REALISTIC WEB ENVIRONMENT FOR BUILDING AUTONOMOUS AGENTS](https://arxiv.org/abs/2307.13854.pdf) `multi-modal`



### Safe, Trustworthy and Personalized Tool Learning

- [Watch Out for Your Agents! Investigating Backdoor Threats to LLM-Based Agent](https://arxiv.org/pdf/2402.11208.pdf)


### Emerging Trends and Future Opportunities

- [Knowledge Conflicts for LLMs: A Survey](https://arxiv.org/abs/2403.08319.pdf)

- [Metacognitive Retrieval-Augmented Large Language Models](https://arxiv.org/pdf/2402.11626.pdf) tools conflicts


</details>



```
@article{tools_meet_llm,
    author    = { Hongru Wang, Yujia Qin, Yankai Lin, Jeff Z. Pan and Kam-fai Wong},
    title     = { SIGIR 2024 Tutorial: Empowering Large Language Models: Tool Learning for Real-World Interaction},
    journal   = { SIGIR 2024 },
    year      = { 2024 },
}
```