<h1 align="center">Lakshmi Chakradhar Vijayarao</h1>

<h3 align="center">
  Prospective PhD Researcher &middot; Reliable and Verifiable AI Systems<br/>
  LLM Failure Detection &middot; Representation Geometry &middot; Adaptive Governance
</h3>

<p align="center">
  <a href="mailto:lakshmichakradhar.v@gmail.com">lakshmichakradhar.v@gmail.com</a> &nbsp;|&nbsp;
  <a href="https://linkedin.com/in/lakshmichakradharvijayarao">LinkedIn</a> &nbsp;|&nbsp;
  <a href="https://github.com/Lakshmi-Chakradhar-Vijayarao">GitHub</a>
</p>

---

## Research Focus

I study **how failures emerge, propagate, and can be controlled in neural models**.

My work examines how reliability signals are encoded within internal representations, how they evolve
across multi-step systems, and how geometric and statistical structure can be leveraged to detect and
govern model behaviour under distribution shift.

**M.S. Computer Science &mdash; University of Texas at Dallas (May 2025)**

Primary research themes: mechanistic origins of failure &middot; representation geometry as a reliability
substrate &middot; failure propagation in multi-step and agentic systems &middot; control and governance
under uncertainty

---

## Research Program &mdash; LLM Reliability (5-Project Series)

A structured, ground-up empirical investigation into *why* LLMs fail and *how* those failures can be
detected, bounded, and governed. All experiments pre-registered with git timestamps; negative results
reported alongside positive ones.

```
MECH-INT  ->  HaRP  ->  GEOM-PROOF  ->  FAIL-CHAIN  ->  GUARDIAN
 cause         signal    certificate     dynamics        governance
```

---

### [GUARDIAN](https://github.com/Lakshmi-Chakradhar-Vijayarao/guardian) &mdash; Adaptive Governance via Local Fisher Geometry
**Project 5 of 5**

Real-time reliability filter on Mistral 7B using **Local Fisher separability** (k=50 KNN neighborhoods)
for deployment-time routing: ACCEPT / REGENERATE / ABSTAIN.

| Metric | Value |
|---|---|
| Routing latency | **0.83 ms** (~0.14% overhead) |
| OOD queries in LOW reliability zone | **67.3%** vs 38.7% in-distribution |
| In-distribution false-accept rate | **0.0%** via adaptive thresholding |
| Generalization gap (in-dist -> OOD AUROC) | **0.804 -> 0.616** -- probe calibration as bottleneck |

*Demonstrates how geometric signals enable deployment-time control while revealing the limits of current
reliability mechanisms.*

---

### [FAIL-CHAIN](https://github.com/Lakshmi-Chakradhar-Vijayarao/fail-chain) &mdash; Failure Propagation in Multi-Step Systems
**Project 4 of 5**

Models failure propagation in 600 self-refinement pipelines as a **Markov process**, deriving a
policy-ordering result: at observed cascade rates, ABSTAIN dominates REGENERATE in expected cost.

| Finding | Value |
|---|---|
| Cascade failure rate across pipelines | **92.3%** |
| Empirical cascade coefficient | **P approx 0.9947** |
| Implied recovery horizon 1/(1-P) | **~189 steps** |
| Early-detection AUROC (before propagation) | **0.662** |
| Latent failures (missed by single-step eval) | **0.5%** of 8 failure modes |

*Shows that reliability is governed by system-level dynamics rather than isolated predictions, motivating
evaluation beyond single-step outputs.*

---

### [GEOM-PROOF](https://github.com/Lakshmi-Chakradhar-Vijayarao/geom-proof) &mdash; Geometric Characterisation of Reliability Signals
**Project 3 of 5**

Derives and empirically validates **J approx W2^2** (Fisher separability approx Wasserstein^2 in
whitened space), establishing a geometric foundation for reliability detection and connecting it to
conformal coverage guarantees.

| Result | Value |
|---|---|
| AUROC approx Phi(sqrt(J)/2) bound error | **<= 1.5%** at optimal layer |
| Within-family scaling R^2 | **0.9996** |
| Conformal hallucination risk bound | **P <= 0.07** at ~52.9% coverage |
| SW2 vs Fisher Spearman r (non-Gaussianity) | **0.821 vs 0.458** |

*Provides a geometric foundation for reliability while explicitly identifying the limits of Gaussian
assumptions -- better captured by Sliced Wasserstein.*

---

### HaRP &mdash; Hallucination-aware Representation Probing *(manuscript in preparation)*
**Project 2 of 5**

Systematic probe calibration and deployment study across GPT-2 Medium, Qwen 2.5 3B, and Mistral 7B.
Reveals scale-dependent emergence of reliability signals in representation space.

| Metric | Value |
|---|---|
| Best probe AUROC (Qwen 2.5 3B) | **0.775** (+0.198 over entropy baseline) |
| ECE improvement | **0.039** vs 0.072 baseline |
| Real-time latency | **23.9 ms** (<0.5% overhead) |
| OOF AUROC after leakage correction | **0.771** (corrected +0.1906 leakage) |
| Scale emergence | ~0.50 AUROC (117M) -> 0.775 (3B) |

*Shows that reliability signals emerge geometrically in representation space and can be leveraged for
real-time control.*

---

### MECH-INT &mdash; Mechanistic Analysis of Failure in Transformer Models *(manuscript in preparation)*
**Project 1 of 5**

12-stage interpretability pipeline over 534 manually curated samples. Localises hallucination to specific
layers and identifies FFN over-retrieval as a consistent failure mechanism.

| Result | Value |
|---|---|
| Hallucination localisation | **Layers 8-9** (~33-38% depth, GPT-2 Medium) |
| Hidden-state probe AUROC vs output baseline | **0.604 vs 0.576** |
| Representation sparsity | **87%** (100/768 active dims) |
| Activation steering (alpha=40) | AUROC 0.490 -- directional, controllable signal |

*Establishes that reliability failures originate within identifiable internal mechanisms, motivating
representation-level detection and control.*

---

## 🛠️ Tech Stack

### 💻 Languages & Frameworks
![Python](https://img.shields.io/badge/Python-%233776AB?style=for-the-badge&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-%23ED8B00?style=for-the-badge&logo=java&logoColor=white)
![C++](https://img.shields.io/badge/C++-%2300599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-%23F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Flask](https://img.shields.io/badge/Flask-%23000000?style=for-the-badge&logo=flask&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)

### 🤖 AI & ML
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21F?style=for-the-badge&logo=huggingface&logoColor=black)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-%2313B1F4?style=for-the-badge&logo=langchain&logoColor=white)

### ☁️ Cloud & DevOps
![AWS](https://img.shields.io/badge/AWS-%23FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-%234285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-%230db7ed?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-%23326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)

### 📊 Data & Research Tools
![Apache Spark](https://img.shields.io/badge/Spark-%23E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-%23017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-%2300B4D8?style=for-the-badge&logo=mlflow&logoColor=white)

**Research:** FAISS &middot; scipy &middot; scikit-learn &middot; numpy &middot; conformal prediction &middot; optimal transport

---

## Prior Systems Work

| Project | Description |
|---|---|
| **SafeRAG** | Atomic claim-level hallucination verification with ACCEPT/REJECT/REFUSE decisions |
| **MedRAG** | Clinical RAG with hybrid retrieval (dense + BM25) + post-generation verification; -34% hallucinations |
| **RL-Retriever** | PPO/DQN query rewriting agent for retrieval-aware optimisation; +28% recall |
| **AlphaRoute** | RL-based trading engine; 18% slippage reduction |
| **AgroVision** | YOLO-based crop/weed detector; 90% mAP, 15% less herbicide |

---

*All experiments pre-registered with git timestamps before execution.
Negative results reported transparently alongside positive ones.*
