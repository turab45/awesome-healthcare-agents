# Awesome Healthcare Agents & Multi-Agents

> A curated list of AI agents, multi-agent systems, benchmarks, datasets, RAG pipelines, safety tools, and research papers for healthcare and medicine.

Last updated: 2026-10-16

---

## Overview

Healthcare agents combine large language models, retrieval, clinical tools, structured EHR access, medical imaging models, and human oversight to support tasks such as triage, clinical reasoning, documentation, drug safety, biomedical discovery, imaging analysis, and healthcare administration.

This repository focuses on resources that are useful for researchers and builders: open-source implementations, public benchmarks, reproducible datasets, and high-signal papers. It is not medical advice and should not be used to deploy autonomous clinical systems without clinical validation, governance, and regulatory review.

---

## Table of Contents

- [Agent Frameworks](#agent-frameworks)
- [Healthcare Agent Systems](#healthcare-agent-systems)
- [Clinical Assistants & Medical LLMs](#clinical-assistants--medical-llms)
- [Medical RAG & Knowledge Systems](#medical-rag--knowledge-systems)
- [Imaging & Multimodal Agents](#imaging--multimodal-agents)
- [Benchmarks & Evaluation Suites](#benchmarks--evaluation-suites)
- [Open Datasets](#open-datasets)
- [Safety, Privacy & Compliance](#safety-privacy--compliance)
- [Surveys & Position Papers](#surveys--position-papers)
- [Key Research Papers](#key-research-papers)
- [How to Contribute](#how-to-contribute)
- [Citation](#citation)
- [License](#license)

---

## Agent Frameworks

General-purpose frameworks that are useful for building healthcare-specific agents, tool-calling systems, and multi-agent workflows.

| Project | Type | Why it matters for healthcare agents |
|---|---|---|
| [AutoGen](https://github.com/microsoft/autogen) | Multi-agent framework | Conversational multi-agent orchestration, useful for specialist/critic/reviewer patterns. |
| [CrewAI](https://github.com/crewAIInc/crewAI) | Multi-agent framework | Role-based task delegation for operational and research workflows. |
| [DSPy](https://github.com/stanfordnlp/dspy) | Programming model | Optimizes LM pipelines and retrieval/programmatic modules. |
| [Hugging Face smolagents](https://github.com/huggingface/smolagents) | Lightweight agents | Minimal Python agent library with tool use and code agents. |
| [LangChain](https://github.com/langchain-ai/langchain) | Agent/RAG framework | Common ecosystem for tool calling, retrieval, memory, and evaluation. |
| [LangGraph](https://github.com/langchain-ai/langgraph) | Stateful agent graphs | Good fit for auditable, branching clinical workflows with checkpoints. |
| [LlamaIndex](https://github.com/run-llama/llama_index) | Data/RAG framework | Connects documents, databases, vector stores, and agents. |
| [Microsoft Semantic Kernel](https://github.com/microsoft/semantic-kernel) | Agent orchestration SDK | Enterprise-oriented skills/plugins, planners, memory, and workflow integration. |
| [n8n](https://github.com/n8n-io/n8n) | Workflow automation | Low-code automation for intake, notifications, scheduling, and back-office healthcare workflows. |
| [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) | Agent SDK | Lightweight Python SDK for tool calling, handoffs, tracing, and guardrails. |
| [OpenAI AgentKit](https://openai.com/index/introducing-agentkit/) | Agent platform | Tooling for building, deploying, and optimizing production agents. |

---

## Healthcare Agent Systems

Research and open-source systems designed specifically for clinical, biomedical, or health-system agent workflows.

| Project | Domain | Description |
|---|---|---|
| [AgentMD](https://github.com/ncbi-nlp/Clinical-Tool-Learning) | Clinical risk calculators | Language agent that curates and applies clinical calculators via the RiskCalcs toolset. |
| [AI Hospital](https://github.com/LibertFan/AI_Hospital) | Simulated clinical interaction | Multi-agent simulator with Doctor, Patient, and Examiner roles plus the MVME benchmark. |
| [AgentClinic](https://agentclinic.github.io/) | Clinical simulation | Multimodal agent benchmark for sequential diagnosis, patient interaction, tool use, and data collection. |
| [HealthAdminBench](https://som-shahlab.github.io/health-admin-bench-website/) | Healthcare administration | Web-environment benchmark for evaluating agents on realistic administrative healthcare tasks. |
| [MDAgents](https://github.com/mitmedialab/MDAgents) | Medical decision-making | Adaptive collaboration strategy that chooses solo, multidisciplinary, or integrated-care agent structures. |
| [MEDDxAgent](https://github.com/nec-research/meddxagent) | Differential diagnosis | Modular agent framework with history taking, retrieval, and diagnostic strategy agents. |
| [MedAgent-Pro](https://github.com/jinlab-imvr/MedAgent-Pro) | Multimodal diagnosis | Evidence-based agentic workflow for multimodal medical diagnosis with specialized tool agents. |
| [MedAgentSim](https://github.com/MAXNORM8650/MedAgentSim) | Clinical simulation | Self-evolving doctor, patient, and measurement agents for dynamic diagnostic interactions. |
| [MedAgents](https://github.com/gersteinlab/MedAgents) | Medical QA/reasoning | Multidisciplinary collaboration framework for zero-shot medical reasoning. |
| [Meissa](https://github.com/Schuture/Meissa) | Offline multimodal medical agents | Lightweight 4B medical agentic model trained on structured trajectories for radiology, pathology, and clinical reasoning. |
| [TxAgent](https://github.com/mims-harvard/TxAgent) | Therapeutic reasoning | Treatment recommendation agent using multi-step reasoning and biomedical tool integration. |

---

## Clinical Assistants & Medical LLMs

Medical LLMs and assistants that are frequently used as backbones or baselines for healthcare-agent research.

| Project | Domain | Description |
|---|---|---|
| [ChatDoctor](https://github.com/Kent0n-Li/ChatDoctor) | Medical consultation | LLM-based medical consultation model and dataset work. |
| [Clinical Camel](https://github.com/starmpcc/ClinicalCamel) | Clinical reasoning | Open clinical LLM project trained for medical QA and reasoning. |
| [ClinicalGPT](https://github.com/ClinicalGPT/ClinicalGPT) | Clinical assistant | Fine-tuned clinical assistant built around EMR and note-style data. |
| [HealthGPT](https://github.com/StanfordBioinformatics/healthgpt) | Personal health | Health-tracker assistant for longitudinal personal health data. |
| [Med-Gemini](https://research.google/blog/advancing-medical-ai-with-med-gemini/) | Medical foundation model | Google research model family for multimodal medical reasoning. |
| [MedGemma](https://github.com/google-health/medgemma) | Open medical models | Google Health open models for medical text and multimodal use cases. |
| [Med-PaLM 2](https://arxiv.org/abs/2305.09617) | Medical reasoning | Google medical LLM evaluated on medical QA and clinical reasoning. |
| [Meditron](https://github.com/epfLLM/meditron) | Open medical LLM | Open Llama-derived medical LLM family for low-resource and clinical settings. |
| [OpenBioLLM](https://huggingface.co/aaditya/OpenBioLLM-Llama3-70B) | Biomedical LLM | Open biomedical LLM family trained for biomedical and clinical QA. |

---

## Medical RAG & Knowledge Systems

RAG, graph-RAG, and biomedical knowledge systems for grounded medical answers.

| Project | Type | Description |
|---|---|---|
| [Baranzini Lab KG-RAG](https://github.com/BaranziniLab/KG_RAG) | Biomedical KG-RAG | Uses the SPOKE biomedical knowledge graph to provide prompt-aware context to LLMs. |
| [MedGraphRAG / Medical-Graph-RAG](https://github.com/MedicineToken/Medical-Graph-RAG) | Graph RAG | Graph-based medical RAG for safer, evidence-linked medical responses. |
| [MedRAG Toolkit](https://github.com/Teddy-XiongGZ/MedRAG) | Medical RAG benchmark/toolkit | Toolkit for benchmarking retrieval-augmented generation in medicine. |
| [MMed-RAG](https://github.com/richard-peng-xia/MMed-RAG) | Multimodal medical RAG | Multimodal RAG for medical vision-language models across radiology, ophthalmology, and pathology. |
| [PubMed](https://pubmed.ncbi.nlm.nih.gov/) | Literature source | Core biomedical literature index for retrieval and evidence grounding. |
| [UMLS](https://www.nlm.nih.gov/research/umls/) | Terminology | Metathesaurus and controlled vocabularies for clinical concept normalization. |

---

## Imaging & Multimodal Agents

Medical imaging, report generation, segmentation, and multimodal tool-use projects.

| Project | Domain | Description |
|---|---|---|
| [BAAI Cardiac Agent](https://github.com/plantain-herb/Cardiac-Agent) | Cardiac imaging | Agentic system for cardiovascular magnetic resonance analysis. |
| [BiomedCLIP](https://github.com/microsoft/BiomedCLIP) | Vision-language model | Biomedical image-text foundation model often used as an imaging tool. |
| [ChatCAD](https://github.com/zhaozh10/ChatCAD) | Radiology assistant | LLM-based assistant for computer-aided diagnosis workflows. |
| [MedRAX](https://github.com/bowang-lab/MedRAX) | Chest X-ray reasoning | Medical reasoning agent for chest X-ray interpretation and tool use. |
| [MedSAM](https://github.com/bowang-lab/MedSAM) | Segmentation | Segment Anything adaptation for medical image segmentation. |
| [MedSAM-Agent](https://arxiv.org/abs/2602.03320) | Interactive segmentation | Agentic reinforcement-learning approach for multi-turn medical image segmentation. |
| [MMedAgent](https://github.com/Wangyixinxin/MMedAgent) | Multimodal tool agent | Medical agent that learns to select and use specialized multimodal tools. |
| [MONAI](https://github.com/Project-MONAI/MONAI) | Imaging framework | PyTorch-based medical imaging framework for training and deployment. |

---

## Benchmarks & Evaluation Suites

Benchmarks for evaluating healthcare agents, clinical LLMs, RAG systems, and multimodal biomedical reasoning.

| Benchmark | Domain | Description |
|---|---|---|
| [AgentClinic](https://agentclinic.github.io/) | Interactive diagnosis | Multimodal simulated clinical environments spanning specialties and languages. |
| [AgentRx](https://arxiv.org/abs/2605.10286) | Multimodal clinical prediction | Benchmark study comparing single-agent and multi-agent systems on clinical prediction tasks. |
| [AI Hospital / MVME](https://aclanthology.org/2025.coling-main.680/) | Clinical simulation | Multi-view evaluation of symptom collection, examination recommendations, and diagnosis. |
| [BixBench](https://huggingface.co/datasets/futurehouse/BixBench) | Computational biology agents | Real-world bioinformatics scenarios for long-horizon data analysis agents. |
| [CalcQA / MeNTi](https://arxiv.org/abs/2410.13610) | Medical calculator agents | Benchmark and nested-tool-calling architecture for medical calculator tasks. |
| [ClinicalAgent Bench (CAB)](https://arxiv.org/abs/2410.17657) | Clinical agents | 18-task benchmark across realistic clinical dimensions from ReflecTool. |
| [HealthAdminBench](https://som-shahlab.github.io/health-admin-bench-website/) | Administration | Healthcare admin benchmark with live web portals and task-level scoring. |
| [HealthBench](https://openai.com/index/healthbench/) | Health conversations | OpenAI benchmark for safety and usefulness in realistic health conversations. |
| [MedAgentBench](https://stanfordmlgroup.github.io/projects/medagentbench/) | Virtual EHR agents | Stanford virtual EHR environment for benchmarking medical LLM agents. |
| [MedAgentGym](https://github.com/wshi83/MedAgentGym) | Biomedical coding agents | Training/evaluation environment with 72k+ code-based biomedical reasoning tasks. |
| [MedAgentsBench](https://github.com/gersteinlab/medagents-benchmark) | Medical reasoning agents | Benchmark for thinking models and agent frameworks on complex medical reasoning. |
| [MedSentry](https://arxiv.org/abs/2505.20824) | Safety | Adversarial benchmark for safety risks in medical LLM multi-agent systems. |
| [PhysicianBench](https://arxiv.org/abs/2605.02240) | Real EHR workflows | 2026 benchmark with long-horizon physician tasks in real clinical EHR environments. |
| [SymptomCheck Bench](https://github.com/medaks/symptomcheck-bench) | Symptom checking | Open benchmark for diagnostic accuracy in simulated symptom-checker workflows. |

---

## Open Datasets

Datasets useful for training, evaluating, or grounding healthcare agents. Some clinical datasets require credentialing and data-use agreements.

| Dataset | Domain | Access | Description |
|---|---|---|---|
| [BixBench](https://huggingface.co/datasets/futurehouse/BixBench) | Bioinformatics agents | Open | Real-world computational biology scenarios and open-answer questions. |
| [CheXpert](https://stanfordmlgroup.github.io/competitions/chexpert/) | Imaging | Open/registered | Chest X-ray dataset with uncertainty labels. |
| [eICU-CRD](https://physionet.org/content/eicu-crd/) | ICU EHR | Credentialed | Multi-center ICU database for critical-care research. |
| [HealthBench](https://github.com/openai/simple-evals) | Health conversations | Open | 5,000 multi-turn health conversations with physician-validated rubrics. |
| [MedAgentBench](https://github.com/stanfordmlgroup/MedAgentBench) | EHR agents | Open/research | Virtual EHR tasks and environment for medical agent evaluation. |
| [MedMCQA](https://medmcqa.github.io/) | Medical QA | Open | Large-scale multi-subject medical multiple-choice QA dataset. |
| [MedQA](https://github.com/jind11/MedQA) | Medical QA | Open | USMLE-style medical question-answering dataset. |
| [MIMIC-CXR](https://physionet.org/content/mimic-cxr/2.1.0/) | Radiology | Credentialed | Chest radiographs paired with free-text radiology reports. |
| [MIMIC-CXR-JPG](https://physionet.org/content/mimic-cxr-jpg/2.1.0/) | Radiology | Credentialed | Processed JPG chest radiographs with structured labels. |
| [MIMIC-IV](https://physionet.org/content/mimiciv/3.1/) | EHR | Credentialed | De-identified hospital and ICU EHR data. |
| [MIMIC-IV-Note](https://physionet.org/content/mimic-iv-note/2.2/) | Clinical notes | Credentialed | De-identified discharge and radiology notes linked to MIMIC-IV. |
| [PubMed Central Open Access](https://www.ncbi.nlm.nih.gov/pmc/tools/openftlist/) | Biomedical text | Open | Full-text biomedical literature corpus for retrieval and summarization. |
| [PubMedQA](https://pubmedqa.github.io/) | Biomedical QA | Open | Biomedical research question-answering dataset. |
| [RadGraph](https://physionet.org/content/radgraph/) | Radiology NLP | Credentialed | Entities and relations annotated from radiology reports. |
| [RxNorm](https://www.nlm.nih.gov/research/umls/rxnorm/) | Medication terminology | Open | Normalized names and identifiers for clinical drugs. |
| [Synthea](https://github.com/synthetichealth/synthea) | Synthetic EHR | Open | Synthetic patient records useful for prototyping without PHI. |

---

## Safety, Privacy & Compliance

Tools and standards that help make healthcare-agent systems safer, auditable, and interoperable.

| Resource | Type | Description |
|---|---|---|
| [FHIR](https://hl7.org/fhir/) | Interoperability standard | API/data standard for exchanging healthcare information. |
| [Guardrails AI](https://github.com/guardrails-ai/guardrails) | Output validation | Validators and structured-output checks for LLM applications. |
| [HAPI FHIR](https://github.com/hapifhir/hapi-fhir) | FHIR server/client | Open-source Java FHIR implementation for healthcare interoperability. |
| [Microsoft Presidio](https://github.com/microsoft/presidio) | PHI/PII detection | Detection and anonymization toolkit for sensitive information. |
| [OpenMedCalc / LLM as Clinical Calculator](https://github.com/stanfordaimlab/llm-as-clinical-calculator) | Verifiable tools | Clinical calculation API and datasets for tool-using medical agents. |
| [OpenFGA](https://github.com/openfga/openfga) | Authorization | Fine-grained authorization engine for policy-controlled tool access. |
| [OpenTelemetry](https://github.com/open-telemetry/opentelemetry-collector) | Observability | Tracing and telemetry for monitoring agent actions and failures. |
| [PySyft](https://github.com/OpenMined/PySyft) | Privacy-preserving ML | Federated and privacy-preserving computation for sensitive data. |
| [SMART on FHIR](https://smarthealthit.org/) | App authorization | OAuth-based launch and authorization framework for EHR apps. |
| [TensorFlow Privacy](https://github.com/tensorflow/privacy) | Differential privacy | Differential privacy tooling for ML training. |
| [ai-a3-laws](https://github.com/stevenzhao07/ai-a3-laws) | Runtime constraints | Deterministic authority / autonomy / accountability checks over an autonomous decision, returning a violation list; usable as a gate inside an agent loop. Zero-dependency CLI (2026). |
| [ai-governance-checklist](https://github.com/stevenzhao07/ai-governance-checklist) | Governance checklist | Governance self-check with model-card and data-card templates covering human oversight, fairness, provenance and monitoring. Zero-dependency CLI (2026). |
| [delivery-guard](https://github.com/stevenzhao07/delivery-guard) | Pre-release gates | 17 deterministic pre-delivery gates plus a dual SHA-256 provenance ledger, making "was this artefact reviewed" answerable. Zero-dependency CLI (2026). |

---

## Surveys & Position Papers

High-level resources for understanding the field and its risks.

| Paper | Year | Focus |
|---|---:|---|
| [A Survey of LLM-based Agents in Medicine](https://aclanthology.org/2025.findings-acl.539/) | 2025 | Taxonomy of medical LLM agents, tasks, evaluation, and open challenges. |
| [Agentic AI in Healthcare & Medicine: A Seven-Dimensional Taxonomy](https://arxiv.org/abs/2602.04813) | 2026 | Empirical taxonomy for evaluating LLM-based healthcare agents. |
| [Agentic AI Governance and Lifecycle Management in Healthcare](https://arxiv.org/abs/2601.15630) | 2026 | Governance blueprint for healthcare agent fleets. |
| [Agentic Large Language Models for Healthcare](https://doi.org/10.1002/med4.70000) | 2025 | Commentary on progress and opportunities for agentic healthcare LLMs. |
| [Agents for Change](https://doi.org/10.1111/cts.70188) | 2025 | Agentic workflows for quantitative clinical pharmacology and translational science. |
| [AI Agents in Clinical Medicine: A Systematic Review](https://www.medrxiv.org/content/10.1101/2025.08.22.25334232v1) | 2025 | Systematic review of clinical medicine agent systems and evidence. |
| [An Empirical Study of Agent Skills for Healthcare](https://arxiv.org/abs/2605.02709) | 2026 | Study of healthcare agent skills, gaps, procedural packaging, and governance. |
| [Large Language Model Agents for Biomedicine](https://www.mdpi.com/2078-2489/16/10/894) | 2025 | Comprehensive review of biomedical LLM agents, methods, evaluation, and challenges. |

---

## Key Research Papers

See the expanded [key research papers](key%20research%20papers/README.md) page for categorized papers on clinical simulation, multimodal agents, RAG, safety, EHR workflows, and benchmark datasets.

---

## How to Contribute

Contributions are welcome.

1. Fork the repo.
2. Add your resource under the most relevant section.
3. Prefer primary sources: paper, official project page, GitHub, dataset page, or DOI.
4. Include the year and a short one-line description.
5. Mark restricted datasets clearly when credentialing, licensing, or data-use agreements are required.
6. Avoid commercial spam and unvalidated medical claims.
7. Submit a pull request.

---

## Citation

If you use or reference this repository in your research, please cite it as:

```bibtex
@misc{turab2025AwesomeHealthcareAgents,
  author       = {Muhammad Turab},
  title        = {Awesome Healthcare Agents: Curated Resources for AI Agents in Healthcare},
  year         = {2025},
  howpublished = {\url{https://github.com/turab45/awesome-healthcare-agents}},
  note         = {Version 1.0},
}
```

---

## License

This project is licensed under the [MIT License](LICENSE).

Curated by [Muhammad Turab](https://github.com/turab45). Inspired by the open-source healthcare AI community.

If you find this list useful, please give it a star on GitHub and share it with others working on healthcare AI agents.

---

# 中文版 · Chinese

# 医疗保健智能体与多智能体精选清单（Awesome Healthcare Agents & Multi-Agents）

> 面向医疗保健与医学领域的 AI 智能体、多智能体系统、基准测试、数据集、RAG 流水线、安全工具与研究论文的精选清单。

最后更新：2026-05-20

---

## 概述

医疗保健智能体将大语言模型、检索、临床工具、结构化电子病历访问、医学影像模型与人类监督相结合，用于支持分诊、临床推理、文档记录、药物安全、生物医学发现、影像分析与医疗管理任务。

本仓库聚焦对研究者和构建者有用的资源：开源实现、公开基准、可复现数据集与高信号论文。它不是医疗建议，未经临床验证、治理与监管审查，不应被用于部署自主临床系统。

---

## 目录

- [智能体框架（Agent Frameworks）](#agent-frameworks)
- [医疗保健智能体系统（Healthcare Agent Systems）](#healthcare-agent-systems)
- [临床助手与医学大模型（Clinical Assistants & Medical LLMs）](#clinical-assistants--medical-llms)
- [医学 RAG 与知识系统（Medical RAG & Knowledge Systems）](#medical-rag--knowledge-systems)
- [影像与多模态智能体（Imaging & Multimodal Agents）](#imaging--multimodal-agents)
- [基准与评测套件（Benchmarks & Evaluation Suites）](#benchmarks--evaluation-suites)
- [开放数据集（Open Datasets）](#open-datasets)
- [安全、隐私与合规（Safety, Privacy & Compliance）](#safety-privacy--compliance)
- [综述与立场论文（Surveys & Position Papers）](#surveys--position-papers)
- [关键研究论文（Key Research Papers）](#key-research-papers)
- [如何贡献（How to Contribute）](#how-to-contribute)
- [引用（Citation）](#citation)
- [许可（License）](#license)

---

## 智能体框架（Agent Frameworks）

适用于构建医疗特定智能体、工具调用系统与多智能体工作流的通用框架。

| 项目 | 类型 | 对医疗保健智能体的意义 |
|---|---|---|
| [AutoGen](https://github.com/microsoft/autogen) | 多智能体框架 | 对话式多智能体编排，适用于专家/评审/复核等模式。 |
| [CrewAI](https://github.com/crewAIInc/crewAI) | 多智能体框架 | 面向运营与研究流程的基于角色的任务委派。 |
| [DSPy](https://github.com/stanfordnlp/dspy) | 编程模型 | 优化语言模型流水线及检索/可编程模块。 |
| [Hugging Face smolagents](https://github.com/huggingface/smolagents) | 轻量智能体 | 支持工具使用与代码智能体的极简 Python 智能体库。 |
| [LangChain](https://github.com/langchain-ai/langchain) | 智能体/RAG 框架 | 工具调用、检索、记忆与评测的通用生态。 |
| [LangGraph](https://github.com/langchain-ai/langgraph) | 有状态智能体图 | 适合带检查点的可审计、分支式临床工作流。 |
| [LlamaIndex](https://github.com/run-llama/llama_index) | 数据/RAG 框架 | 连接文档、数据库、向量库与智能体。 |
| [Microsoft Semantic Kernel](https://github.com/microsoft/semantic-kernel) | 智能体编排 SDK | 面向企业的技能/插件、规划器、记忆与工作流集成。 |
| [n8n](https://github.com/n8n-io/n8n) | 工作流自动化 | 用于录入、通知、调度与后台医疗工作流的低代码自动化。 |
| [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) | 智能体 SDK | 支持工具调用、交接、追踪与护栏的轻量 Python SDK。 |
| [OpenAI AgentKit](https://openai.com/index/introducing-agentkit/) | 智能体平台 | 用于构建、部署与优化生产级智能体的工具。 |

---

## 医疗保健智能体系统（Healthcare Agent Systems）

专门面向临床、生物医学或医疗系统智能体工作流的研究与开源系统。

| 项目 | 领域 | 描述 |
|---|---|---|
| [AgentMD](https://github.com/ncbi-nlp/Clinical-Tool-Learning) | 临床风险计算器 | 通过 RiskCalcs 工具集整理并应用临床计算器的语言智能体。 |
| [AI Hospital](https://github.com/LibertFan/AI_Hospital) | 模拟临床交互 | 含医生、患者、考官角色的多智能体模拟器及 MVME 基准。 |
| [AgentClinic](https://agentclinic.github.io/) | 临床模拟 | 面向序贯诊断、患者交互、工具使用与数据收集的多模态智能体基准。 |
| [HealthAdminBench](https://som-shahlab.github.io/health-admin-bench-website/) | 医疗管理 | 用于评估智能体在真实行政医疗任务上的 Web 环境基准。 |
| [MDAgents](https://github.com/mitmedialab/MDAgents) | 医疗决策 | 自适应协作策略，可选择单智能体、多学科或一体化护理智能体结构。 |
| [MEDDxAgent](https://github.com/nec-research/meddxagent) | 鉴别诊断 | 含病史采集、检索与诊断策略智能体的模块化框架。 |
| [MedAgent-Pro](https://github.com/jinlab-imvr/MedAgent-Pro) | 多模态诊断 | 面向多模态医学诊断的循证智能体工作流，含专用工具智能体。 |
| [MedAgentSim](https://github.com/MAXNORM8650/MedAgentSim) | 临床模拟 | 自进化式医生、患者与测量智能体，用于动态诊断交互。 |
| [MedAgents](https://github.com/gersteinlab/MedAgents) | 医学问答/推理 | 面向零样本医学推理的多学科协作框架。 |
| [Meissa](https://github.com/Schuture/Meissa) | 离线多模态医疗智能体 | 基于结构化轨迹训练的轻量 4B 医疗智能体模型，用于放射、病理与临床推理。 |
| [TxAgent](https://github.com/mims-harvard/TxAgent) | 治疗推理 | 使用多步推理与生物医学工具整合的治疗推荐智能体。 |

---

## 临床助手与医学大模型（Clinical Assistants & Medical LLMs）

常被用作医疗保健智能体研究骨干或基线的医学大模型与助手。

| 项目 | 领域 | 描述 |
|---|---|---|
| [ChatDoctor](https://github.com/Kent0n-Li/ChatDoctor) | 医疗咨询 | 基于大语言模型的医疗咨询模型与数据集工作。 |
| [Clinical Camel](https://github.com/starmpcc/ClinicalCamel) | 临床推理 | 面向医学问答与推理训练的开源临床大模型项目。 |
| [ClinicalGPT](https://github.com/ClinicalGPT/ClinicalGPT) | 临床助手 | 围绕电子病历与笔记式数据微调的临床助手。 |
| [HealthGPT](https://github.com/StanfordBioinformatics/healthgpt) | 个人健康 | 面向纵向个人健康数据的健康追踪助手。 |
| [Med-Gemini](https://research.google/blog/advancing-medical-ai-with-med-gemini/) | 医学基础模型 | 面向多模态医学推理的 Google 研究模型系列。 |
| [MedGemma](https://github.com/google-health/medgemma) | 开放医学模型 | Google Health 面向医学文本与多模态用例的开放模型。 |
| [Med-PaLM 2](https://arxiv.org/abs/2305.09617) | 医学推理 | 在医学问答与临床推理上评估的 Google 医学大模型。 |
| [Meditron](https://github.com/epfLLM/meditron) | 开放医学大模型 | 面向低资源与临床场景的开放 Llama 衍生医学大模型系列。 |
| [OpenBioLLM](https://huggingface.co/aaditya/OpenBioLLM-Llama3-70B) | 生物医学大模型 | 面向生物医学与临床问答训练的开放生物医学大模型系列。 |

---

## 医学 RAG 与知识系统（Medical RAG & Knowledge Systems）

用于有据可依的医学回答的 RAG、图 RAG 与生物医学知识系统。

| 项目 | 类型 | 描述 |
|---|---|---|
| [Baranzini Lab KG-RAG](https://github.com/BaranziniLab/KG_RAG) | 生物医学知识图谱 RAG | 使用 SPOKE 生物医学知识图谱为 LLM 提供提示感知上下文。 |
| [MedGraphRAG / Medical-Graph-RAG](https://github.com/MedicineToken/Medical-Graph-RAG) | 图 RAG | 面向更安全、证据关联的医学回答的基于图的医学 RAG。 |
| [MedRAG Toolkit](https://github.com/Teddy-XiongGZ/MedRAG) | 医学 RAG 基准/工具包 | 用于医学检索增强生成基准测试的工具包。 |
| [MMed-RAG](https://github.com/richard-peng-xia/MMed-RAG) | 多模态医学 RAG | 面向放射、眼科与病理医学视觉语言模型的多模态 RAG。 |
| [PubMed](https://pubmed.ncbi.nlm.nih.gov/) | 文献来源 | 用于检索与证据锚定的核心生物医学文献索引。 |
| [UMLS](https://www.nlm.nih.gov/research/umls/) | 术语 | 用于临床概念标准化的元叙词表与控制词汇。 |

---

## 影像与多模态智能体（Imaging & Multimodal Agents）

医学影像、报告生成、分割与多模态工具使用项目。

| 项目 | 领域 | 描述 |
|---|---|---|
| [BAAI Cardiac Agent](https://github.com/plantain-herb/Cardiac-Agent) | 心脏影像 | 面向心血管磁共振分析的智能体系统。 |
| [BiomedCLIP](https://github.com/microsoft/BiomedCLIP) | 视觉语言模型 | 常用作影像工具的生物医学图文基础模型。 |
| [ChatCAD](https://github.com/zhaozh10/ChatCAD) | 放射助手 | 基于 LLM 的计算机辅助诊断工作流助手。 |
| [MedRAX](https://github.com/bowang-lab/MedRAX) | 胸片推理 | 面向胸片解读与工具使用的医学推理智能体。 |
| [MedSAM](https://github.com/bowang-lab/MedSAM) | 分割 | Segment Anything 在医学图像分割上的适配。 |
| [MedSAM-Agent](https://arxiv.org/abs/2602.03320) | 交互式分割 | 面向多轮医学图像分割的智能体强化学习方法。 |
| [MMedAgent](https://github.com/Wangyixinxin/MMedAgent) | 多模态工具智能体 | 学习选择并使用专用多模态工具的医学智能体。 |
| [MONAI](https://github.com/Project-MONAI/MONAI) | 影像框架 | 基于 PyTorch 的医学影像训练与部署框架。 |

---

## 基准与评测套件（Benchmarks & Evaluation Suites）

用于评测医疗保健智能体、临床大模型、RAG 系统与多模态生物医学推理的基准。

| 基准 | 领域 | 描述 |
|---|---|---|
| [AgentClinic](https://agentclinic.github.io/) | 交互式诊断 | 覆盖多专科与多语言的模态模拟临床环境。 |
| [AgentRx](https://arxiv.org/abs/2605.10286) | 多模态临床预测 | 在临床预测任务上比较单智能体与多智能体系统的基准研究。 |
| [AI Hospital / MVME](https://aclanthology.org/2025.coling-main.680/) | 临床模拟 | 对症状采集、检查建议与诊断的多视角评估。 |
| [BixBench](https://huggingface.co/datasets/futurehouse/BixBench) | 计算生物学智能体 | 面向长程数据分析智能体的真实生物信息学场景。 |
| [CalcQA / MeNTi](https://arxiv.org/abs/2410.13610) | 医学计算器智能体 | 面向医学计算器任务的基准与嵌套工具调用架构。 |
| [ClinicalAgent Bench (CAB)](https://arxiv.org/abs/2410.17657) | 临床智能体 | 源自 ReflecTool 的覆盖 18 项真实临床维度任务的基准。 |
| [HealthAdminBench](https://som-shahlab.github.io/health-admin-bench-website/) | 行政管理 | 含实时 Web 门户与任务级评分的医疗行政基准。 |
| [HealthBench](https://openai.com/index/healthbench/) | 健康对话 | OpenAI 面向真实健康对话安全性与有用性的基准。 |
| [MedAgentBench](https://stanfordmlgroup.github.io/projects/medagentbench/) | 虚拟 EHR 智能体 | Stanford 面向医学 LLM 智能体评测的虚拟电子病历环境。 |
| [MedAgentGym](https://github.com/wshi83/MedAgentGym) | 生物医学编码智能体 | 含 72k+ 基于代码的生物医学推理任务的训练/评测环境。 |
| [MedAgentsBench](https://github.com/gersteinlab/medagents-benchmark) | 医学推理智能体 | 面向复杂医学推理的思考模型与智能体框架基准。 |
| [MedSentry](https://arxiv.org/abs/2505.20824) | 安全 | 面向医学 LLM 多智能体系统安全风险的对抗性基准。 |
| [PhysicianBench](https://arxiv.org/abs/2605.02240) | 真实 EHR 工作流 | 2026 年基准，在真实临床 EHR 环境中执行长程医生任务。 |
| [SymptomCheck Bench](https://github.com/medaks/symptomcheck-bench) | 症状检查 | 面向模拟症状检查器工作流诊断准确性的开放基准。 |

---

## 开放数据集（Open Datasets）

可用于训练、评测或锚定医疗保健智能体的数据集。部分临床数据集需要资质认证与数据使用协议。

| 数据集 | 领域 | 访问 | 描述 |
|---|---|---|---|
| [BixBench](https://huggingface.co/datasets/futurehouse/BixBench) | 生物信息学智能体 | 开放 | 真实计算生物学场景与开放式问答。 |
| [CheXpert](https://stanfordmlgroup.github.io/competitions/chexpert/) | 影像 | 开放/注册 | 含不确定性标签的胸片数据集。 |
| [eICU-CRD](https://physionet.org/content/eicu-crd/) | ICU EHR | 需认证 | 面向重症研究的多中心 ICU 数据库。 |
| [HealthBench](https://github.com/openai/simple-evals) | 健康对话 | 开放 | 5,000 轮带医生验证评分标准的多轮健康对话。 |
| [MedAgentBench](https://github.com/stanfordmlgroup/MedAgentBench) | EHR 智能体 | 开放/研究 | 用于医学智能体评测的虚拟 EHR 任务与环境。 |
| [MedMCQA](https://medmcqa.github.io/) | 医学问答 | 开放 | 大规模多学科医学选择题问答数据集。 |
| [MedQA](https://github.com/jind11/MedQA) | 医学问答 | 开放 | 美国执业医师资格考试（USMLE）风格医学问答数据集。 |
| [MIMIC-CXR](https://physionet.org/content/mimic-cxr/2.1.0/) | 放射 | 需认证 | 配自由文本放射报告的胸片影像。 |
| [MIMIC-CXR-JPG](https://physionet.org/content/mimic-cxr-jpg/2.1.0/) | 放射 | 需认证 | 带结构化标签的处理后 JPG 胸片。 |
| [MIMIC-IV](https://physionet.org/content/mimiciv/3.1/) | EHR | 需认证 | 去标识化的医院与 ICU 电子病历数据。 |
| [MIMIC-IV-Note](https://physionet.org/content/mimic-iv-note/2.2/) | 临床笔记 | 需认证 | 与 MIMIC-IV 关联的去标识化出院与放射笔记。 |
| [PubMed Central Open Access](https://www.ncbi.nlm.nih.gov/pmc/tools/openftlist/) | 生物医学文本 | 开放 | 面向检索与摘要的全文生物医学文献语料。 |
| [PubMedQA](https://pubmedqa.github.io/) | 生物医学问答 | 开放 | 生物医学研究问答数据集。 |
| [RadGraph](https://physionet.org/content/radgraph/) | 放射 NLP | 需认证 | 从放射报告中标注的实体与关系。 |
| [RxNorm](https://www.nlm.nih.gov/research/umls/rxnorm/) | 药物术语 | 开放 | 临床药物的标准化名称与标识符。 |
| [Synthea](https://github.com/synthetichealth/synthea) | 合成 EHR | 开放 | 无 PHI 场景下适用于原型开发的合成患者记录。 |

---

## 安全、隐私与合规（Safety, Privacy & Compliance）

有助于让医疗保健智能体系统更安全、可审计、可互操作的工具与标准。

| 资源 | 类型 | 描述 |
|---|---|---|
| [FHIR](https://hl7.org/fhir/) | 互操作标准 | 用于交换医疗信息的 API/数据标准。 |
| [Guardrails AI](https://github.com/guardrails-ai/guardrails) | 输出校验 | 面向 LLM 应用的校验器与结构化输出检查。 |
| [HAPI FHIR](https://github.com/hapifhir/hapi-fhir) | FHIR 服务端/客户端 | 面向医疗互操作的开源 Java FHIR 实现。 |
| [Microsoft Presidio](https://github.com/microsoft/presidio) | PHI/PII 检测 | 敏感信息检测与匿名化工具包。 |
| [OpenMedCalc / LLM as Clinical Calculator](https://github.com/stanfordaimlab/llm-as-clinical-calculator) | 可验证工具 | 面向工具使用型医学智能体的临床计算 API 与数据集。 |
| [OpenFGA](https://github.com/openfga/openfga) | 授权 | 面向策略控制的工具访问的细粒度授权引擎。 |
| [OpenTelemetry](https://github.com/open-telemetry/opentelemetry-collector) | 可观测性 | 用于监控智能体行为与失败的追踪与遥测。 |
| [PySyft](https://github.com/OpenMined/PySyft) | 隐私保护机器学习 | 面向敏感数据的联邦与隐私保护计算。 |
| [SMART on FHIR](https://smarthealthit.org/) | 应用授权 | 面向 EHR 应用的基于 OAuth 的启动与授权框架。 |
| [TensorFlow Privacy](https://github.com/tensorflow/privacy) | 差分隐私 | 面向机器学习训练的差分隐私工具。 |
| [ai-a3-laws](https://github.com/stevenzhao07/ai-a3-laws) | 运行时约束 | 对自主决策执行确定性权威/自治/问责检查并返回违规列表；可在智能体循环内用作门控。零依赖 CLI（2026）。 |
| [ai-governance-checklist](https://github.com/stevenzhao07/ai-governance-checklist) | 治理清单 | 含模型卡与数据卡模板的治理自检，覆盖人类监督、公平性、溯源与监控。零依赖 CLI（2026）。 |
| [delivery-guard](https://github.com/stevenzhao07/delivery-guard) | 发布前门禁 | 17 项确定性发布前门禁加双 SHA-256 溯源账本，使"该产物是否已评审"可回答。零依赖 CLI（2026）。 |

---

## 综述与立场论文（Surveys & Position Papers）

用于理解该领域及其风险的高层资源。

| 论文 | 年份 | 聚焦 |
|---|---:|---|
| [A Survey of LLM-based Agents in Medicine](https://aclanthology.org/2025.findings-acl.539/) | 2025 | 医学 LLM 智能体的分类、任务、评测与开放挑战。 |
| [Agentic AI in Healthcare & Medicine: A Seven-Dimensional Taxonomy](https://arxiv.org/abs/2602.04813) | 2026 | 用于评测基于 LLM 的医疗保健智能体的经验性分类法。 |
| [Agentic AI Governance and Lifecycle Management in Healthcare](https://arxiv.org/abs/2601.15630) | 2026 | 医疗保健智能体集群的治理蓝图。 |
| [Agentic Large Language Models for Healthcare](https://doi.org/10.1002/med4.70000) | 2025 | 关于智能体医疗 LLM 进展与机会的评述。 |
| [Agents for Change](https://doi.org/10.1111/cts.70188) | 2025 | 面向定量临床药理学与转化科学的智能体工作流。 |
| [AI Agents in Clinical Medicine: A Systematic Review](https://www.medrxiv.org/content/10.1101/2025.08.22.25334232v1) | 2025 | 临床医学智能体系统与证据的系统综述。 |
| [An Empirical Study of Agent Skills for Healthcare](https://arxiv.org/abs/2605.02709) | 2026 | 关于医疗保健智能体技能、缺口、流程化封装与治理的研究。 |
| [Large Language Model Agents for Biomedicine](https://www.mdpi.com/2078-2489/16/10/894) | 2025 | 生物医学 LLM 智能体的方法、评测与挑战综合综述。 |

---

## 关键研究论文（Key Research Papers）

扩展的关键研究论文列表见 [key research papers](key%20research%20papers/README.md) 页面，涵盖临床模拟、多模态智能体、RAG、安全、EHR 工作流与基准数据集分类论文。

---

## 如何贡献（How to Contribute）

欢迎贡献。

1. Fork 本仓库。
2. 在最相关章节下添加你的资源。
3. 优先使用主要来源：论文、官方项目页、GitHub、数据集页或 DOI。
4. 包含年份与一行简短描述。
5. 当需要资质认证、许可或数据使用协议时，明确标注受限数据集。
6. 避免商业垃圾信息与未经验证的医学声明。
7. 提交拉取请求。

---

## 引用（Citation）

如果你在研究中使用了本仓库，请按如下格式引用：

```bibtex
@misc{turab2025AwesomeHealthcareAgents,
  author       = {Muhammad Turab},
  title        = {Awesome Healthcare Agents: Curated Resources for AI Agents in Healthcare},
  year         = {2025},
  howpublished = {\url{https://github.com/turab45/awesome-healthcare-agents}},
  note         = {Version 1.0},
}
```

---

## 许可（License）

本项目基于 [MIT 许可](LICENSE) 授权。

由 [Muhammad Turab](https://github.com/turab45) 策展。灵感来自开源医疗保健 AI 社区。

如果你觉得这个清单有用，请在 GitHub 上为它加星，并与从事医疗保健 AI 智能体的其他人分享。

