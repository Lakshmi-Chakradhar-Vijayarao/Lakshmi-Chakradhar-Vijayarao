<h1 align="center">Lakshmi Chakradhar Vijayarao</h1>

<h3 align="center">
  Reliability-Focused AI Systems Researcher<br/>
  LLM Failure Detection &middot; Geometric Uncertainty &middot; Adaptive Governance
</h3>

<p align="center">
  <a href="mailto:lakshmichakradhar.v@gmail.com">lakshmichakradhar.v@gmail.com</a> &nbsp;|&nbsp;
  <a href="https://linkedin.com/in/lakshmichakradharvijayarao">LinkedIn</a> &nbsp;|&nbsp;
  <a href="https://github.com/Lakshmi-Chakradhar-Vijayarao">GitHub</a>
</p>

---

## About Me

I study **how failures emerge, propagate, and can be controlled in large language models**.

My work sits at the intersection of geometric representation analysis, statistical reliability theory,
and production-grade AI governance. I build systems that detect hallucinations before they cause
downstream harm -- not by wrapping a prompt or adding a retriever, but by reading the model's internal
geometry directly.

**M.S. Computer Science -- University of Texas at Dallas (May 2025)**

---

## Research Arc -- LLM Reliability (5-Project Series)

A ground-up empirical investigation into *why* LLMs fail and *how* those failures can be detected,
bounded, and governed.

```
MECH-INT  ->  HaRP  ->  GEOM-PROOF  ->  FAIL-CHAIN  ->  GUARDIAN
 cause         signal    certificate     dynamics        governance
```

---

### [GUARDIAN](https://github.com/Lakshmi-Chakradhar-Vijayarao/guardian) -- Reliability-Conditioned Adaptive Governance
**Project 5 of 5 &middot; Target: NeurIPS 2026 Trustworthy ML Workshop**

Post-generation routing system for Mistral 7B using **local Fisher J** computed over FAISS KNN (k=50)
neighborhoods. Three-zone adaptive policy: ACCEPT / REGENERATE / ABSTAIN.

| Metric | Value |
|---|---|
| In-domain AUROC (Mistral 7B, TruthfulQA) | **0.776** |
| Routing latency (CPU) | **~15ms** |
| Cascade override threshold | alpha > 0.95 -> ABSTAIN dominates REGENERATE |
| OOD false-accept reduction (HaluEval) | 0.0pp -- bottleneck: probe calibration |

Pre-registered predictions committed before any Mistral experiment. Negative results reported transparently.

---

### [FAIL-CHAIN](https://github.com/Lakshmi-Chakradhar-Vijayarao/fail-chain) -- Failure Propagation in Multi-Step Reasoning
**Project 4 of 5 &middot; Target: ICML 2026**

Models multi-step LLM failure as an **absorbing Markov chain**. Derives a policy-ordering theorem:
when cascade absorption exceeds 0.95, ABSTAIN strictly dominates REGENERATE in expected cost.

| Finding | Value |
|---|---|
| Empirical cascade coefficient (alpha) | **0.9947** |
| Expected recovery steps 1/(1-alpha) | **189** |
| Global Fisher J on OOD data (F-ratio) | **0.007** -- geometry collapses |
| Cascade AUROC (failure prediction) | **0.847** |

Five pre-registered predictions; 3 confirmed, 1 partially confirmed, 1 refuted -- all reported transparently.

---

### [GEOM-PROOF](https://github.com/Lakshmi-Chakradhar-Vijayarao/geom-proof) -- Geometric Certificate for Probe Reliability
**Project 3 of 5 &middot; Target: ICLR 2026**

Proves and validates the identity **J approx W2^2** (Fisher separability approx Wasserstein^2 distance)
in whitened representation space. Derives a conformal coverage guarantee from the certificate.

| Result | Value |
|---|---|
| Phi(sqrt(J)/2) bound error at optimal layer | **<= 1.5%** |
| SW2-AUROC Spearman r (vs Fisher r) | **0.821 vs 0.458** |
| Conformal coverage (in-distribution) | **0.997** at alpha* = 0.07 |
| R^2 fit (within-family scaling) | **0.9996** |

10 experiments across GPT-2, Qwen 2.5 (0.5B--7B), Mamba 130M.

---

### HaRP -- Hallucination-aware Representation Probing *(manuscript in preparation)*
**Project 2 of 5**

Systematic probe calibration study across GPT-2 Medium, Qwen 2.5 3B, and Mistral 7B. Identifies that
representation geometry crystallizes at ~89% depth in Qwen 2.5 3B.

| Metric | Value |
|---|---|
| Best probe AUROC | **0.775** |
| ECE improvement | 0.039 vs 0.072 baseline |
| OOD AUROC transfer gap | **0.225** (0.997 -> 0.775) |

---

### MECH-INT -- Mechanistic Interpretability of Hallucination *(manuscript in preparation)*
**Project 1 of 5**

Causal analysis of where hallucination decisions form in GPT-2 Medium using Direct Logit Attribution
and activation patching.

| Result | Value |
|---|---|
| Critical layer range | L8--L9 (33--38% depth, GPT-2 Medium) |
| Steering AUROC | **0.863** |
| Sparse feature coverage | top-3% of dims account for >60% of J variance |

---

## Tech Stack

### Languages & Frameworks
![Python](https://img.shields.io/badge/Python-%233776AB?style=for-the-badge&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-%23ED8B00?style=for-the-badge&logo=java&logoColor=white)
![C++](https://img.shields.io/badge/C++-%2300599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-%23F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Flask](https://img.shields.io/badge/Flask-%23000000?style=for-the-badge&logo=flask&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)

### AI & ML
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21F?style=for-the-badge&logo=huggingface&logoColor=black)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-%2313B1F4?style=for-the-badge&logo=langchain&logoColor=white)

### Cloud & DevOps
![AWS](https://img.shields.io/badge/AWS-%23FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-%234285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-%230db7ed?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-%23326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)

### Data & Research Tools
![Apache Spark](https://img.shields.io/badge/Spark-%23E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-%23017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-%2300B4D8?style=for-the-badge&logo=mlflow&logoColor=white)

**Research tools:** FAISS &middot; scipy &middot; scikit-learn &middot; numpy &middot; conformal prediction &middot; optimal transport

---

## Prior Systems Work

| Project | Description |
|---|---|
| **SafeRAG** | Atomic claim-level hallucination verification with ACCEPT/REJECT/REFUSE decisions |
| **MedRAG** | Clinical RAG with hybrid retrieval (dense + BM25) + post-generation verification; -34% hallucinations |
| **RL-Retriever** | PPO/DQN query rewriting agent for retrieval-aware optimization; +28% recall |
| **AlphaRoute** | RL-based trading engine; 18% slippage reduction |
| **AgroVision** | YOLO-based crop/weed detector; 90% mAP, 15% less herbicide |

---

## Intended Research Directions

- Mechanistic origins of failure in neural systems
- Geometric structure of reliability signals across model families
- Failure propagation in multi-step and agentic systems
- Conformal and distribution-free control under uncertainty
- AI governance and audit frameworks for deployed LLMs

---

*All empirical results pre-registered with git timestamps before experiments. Negative results reported alongside positive ones.*
