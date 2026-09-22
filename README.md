# Awesome Healthcare Agents & Multi-Agents

> A curated list of AI agents, multi-agent systems, benchmarks, datasets, RAG pipelines, safety tools, and research papers for healthcare and medicine.

Last updated: 2026-05-20

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
| [Allowly Receipt Format](https://github.com/Allowly-AI/allowly-receipt-format) | Decision audit | Open receipt format and offline verifiers for signed policy decisions; verification authenticates recorded bytes, not source truth, execution, approval identity, or completeness. |
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
