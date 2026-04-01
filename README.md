<a href="https://github.com/Lakshmi-Chakradhar-Vijayarao">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0,0d1b2a,1b4f72,0e6655&height=200&section=header&text=Lakshmi%20Chakradhar%20Vijayarao&fontSize=38&fontColor=ffffff&fontAlignY=38&desc=Geometry-Based%20Governance%20of%20LLM%20Hallucination&descSize=16&descAlignY=60&animation=fadeIn" width="100%"/>
</a>

<p align="center">
  <a href="https://readme-typing-svg.demolab.com">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&pause=1000&color=1ABC9C&center=true&vCenter=true&multiline=false&width=700&height=40&lines=Prospective+PhD+Researcher+%E2%80%94+Reliable+AI+Systems;LLM+Failure+Detection+via+Representation+Geometry;5-Project+Arc%3A+Mechanism+%E2%86%92+Certificate+%E2%86%92+Governance;All+predictions+pre-registered.+Negative+results+reported." alt="Typing SVG" />
  </a>
</p>

<p align="center">
  <a href="mailto:lakshmichakradhar.v@gmail.com">
    <img src="https://img.shields.io/badge/Email-lakshmichakradhar.v%40gmail.com-0d1b2a?style=flat-square&logo=gmail&logoColor=white"/>
  </a>
  &nbsp;
  <a href="https://linkedin.com/in/lakshmichakradharvijayarao">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/>
  </a>
  &nbsp;
  <a href="https://huggingface.co/Lakshmi-Chakradhar-Vijayarao">
    <img src="https://img.shields.io/badge/HuggingFace-Models%20%26%20Spaces-FFD21F?style=flat-square&logo=huggingface&logoColor=black"/>
  </a>
  &nbsp;
  <img src="https://img.shields.io/badge/M.S.%20CS-UT%20Dallas%202025-c0392b?style=flat-square&logo=google-scholar&logoColor=white"/>
  &nbsp;
  <img src="https://komarev.com/ghpvc/?username=Lakshmi-Chakradhar-Vijayarao&style=flat-square&color=1abc9c&label=Profile+Views"/>
</p>

---

## The Research Question

> *Can we prove, from internal geometry alone, when a model is about to hallucinate — and govern it accordingly?*

I study hallucination in large language models not as an alignment problem but as a **geometric one**: failures leave measurable signatures in representation space. My work traces those signatures from their causal origin inside feed-forward networks, through a mathematical certificate connecting geometry to detection guarantees, through failure propagation dynamics in multi-step pipelines, to a deployed adaptive routing system that acts on the signal in real time.

Five projects. One arc. Pre-registered predictions. Honest negative results.

---

## The 5-Project Arc

<div align="center">

```
  ┌─────────────┐      ┌──────────────┐      ┌───────────────┐      ┌─────────────────┐      ┌──────────────────┐
  │   MECH-INT  │─────▶│     HaRP     │─────▶│  GEOM-PROOF   │─────▶│   FAIL-CHAIN    │─────▶│    GUARDIAN      │
  │  [Project 1]│      │  [Project 2] │      │  [Project 3]  │      │  [Project 4]    │      │  [Project 5]     │
  │             │      │              │      │               │      │                 │      │                  │
  │  Mechanism  │      │    Signal    │      │  Certificate  │      │   Dynamics      │      │   Governance     │
  │             │      │              │      │               │      │                 │      │                  │
  │ Where does  │      │  Where does  │      │  How do we    │      │  How do errors  │      │  How do we act   │
  │ the error   │      │  it become   │      │  certify the  │      │  propagate in   │      │  on the signal   │
  │  originate? │      │ detectable?  │      │  detection?   │      │  pipelines?     │      │  in real-time?   │
  └─────────────┘      └──────────────┘      └───────────────┘      └─────────────────┘      └──────────────────┘
       GPT-2              Qwen 2.5 3B         GPT-2 + Qwen              Mistral + GPT          Mistral 7B Instruct
   534 samples           TQA + HaluEval         11 experiments          600 pipelines             TQA + HaluEval
```

</div>

---

## Project 1 — MECH-INT

**Mechanistic Analysis of Hallucination in Transformer Feed-Forward Networks**

<table>
<tr>
<td width="60%">

**Core finding:** Hallucination localizes causally to Layers 8–9 (~33–38% depth) in GPT-2 Medium via FFN over-retrieval — not attention pattern failure. Direct Logit Attribution (DLA) proves the wrong token is promoted by specific FFN components causally, not correlationally.

A 12-stage interpretability pipeline over 534 manually curated samples.

| Metric | Value |
|--------|-------|
| Hallucination localization | **L8–9 (33–38% depth)** |
| Hidden-state probe AUROC | **0.604** (vs 0.576 baseline) |
| Representation sparsity | **87%** (100/768 active dims) |
| Steering signal (α=40) | AUROC 0.490 — directional |

</td>
<td width="40%" align="center">

<a href="https://github.com/Lakshmi-Chakradhar-Vijayarao/mech-int">
  <img src="https://img.shields.io/badge/GitHub-mech--int-1565c0?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<br/><br/>

<a href="https://lakshmi-chakradhar-vijayarao-mech-int-app-3enga8.streamlit.app/">
  <img src="https://img.shields.io/badge/Live%20Demo-Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white"/>
</a>

<br/><br/>

```
Error origin ≈ L8–9
        │
   ╔════╧════╗
   ║  FFN    ║
   ║ over-   ║
   ║retrieval║
   ╚═════════╝
```

</td>
</tr>
</table>

---

## Project 2 — HaRP

**Hallucination-aware Representation Probing**

<table>
<tr>
<td width="60%">

**Core finding:** The hallucination signal crystallizes at **L32 (89% depth)** in Qwen 2.5 3B, detectable with AUROC 0.775 OOD. Temperature scaling *degrades* hallucination calibration (ECE 0.071 → 0.395) — a counter-intuitive negative result reported transparently.

A 4-quadrant uncertainty decomposition: epistemic vs aleatoric × correct vs hallucinated.

| Metric | Value |
|--------|-------|
| In-domain probe AUROC | **0.758** (OOF-honest) |
| OOD AUROC (TQA → HaluEval) | **0.775** |
| ECE HaRP vs raw LLM | **0.039** vs 0.071 |
| Temperature scaling ECE | 0.395 — **worse** |
| Real-time latency | **23.9 ms** (<0.5% overhead) |

</td>
<td width="40%" align="center">

<a href="https://github.com/Lakshmi-Chakradhar-Vijayarao/harp">
  <img src="https://img.shields.io/badge/GitHub-harp-6a1b9a?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<br/><br/>

<a href="https://harpfind.streamlit.app/">
  <img src="https://img.shields.io/badge/Live%20Demo-Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white"/>
</a>

<br/><br/>

```
Signal peak at 89% depth:
0.50 ─────╮
          │       ╭──────
0.75 ─────┼───────╯  L32
          │  AUROC 0.775
          0%   89%  100%
```

</td>
</tr>
</table>

---

## Project 3 — GEOM-PROOF

**Geometric Certificates for Hallucination Detection**

<table>
<tr>
<td width="60%">

**Core finding:** Fisher separability J bounds probe AUROC via **Φ(√J/2)**, accurate within 2.7% max error across all layers and models. Conformal guarantee: P(hallucination) ≤ 0.07 at ~52.9% acceptance rate. SW2 > Fisher (Spearman 0.821 vs 0.458) because real distributions are non-Gaussian.

Scale curve: `AUROC = σ(8.62·log₁₀(params) − 69.10)`, R² = 0.9993.

| Result | Value |
|--------|-------|
| AUROC bound max error | **≤ 2.7%** (all layers + models) |
| Scale curve R² | **0.9993** |
| Conformal α* | **0.07** at 52.9% coverage |
| SW2 vs Fisher Spearman r | **0.821 vs 0.458** |
| Within-family R² | **0.9996** |

</td>
<td width="40%" align="center">

<a href="https://github.com/Lakshmi-Chakradhar-Vijayarao/geom-proof">
  <img src="https://img.shields.io/badge/GitHub-geom--proof-1b5e20?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<br/><br/>

<a href="https://geom-proof.streamlit.app/">
  <img src="https://img.shields.io/badge/Live%20Demo-Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white"/>
</a>

<br/><br/>

```
AUROC ≈ Φ(√J/2)
max error: 2.7%

Scale curve R²=0.9993
params → AUROC
117M  →  0.50
3B    →  0.775
7B    →  0.804
```

</td>
</tr>
</table>

---

## Project 4 — FAIL-CHAIN

**Failure Propagation Geometry in Multi-Step LLM Pipelines**

<table>
<tr>
<td width="60%">

**Core finding:** Self-refinement is a **nearly-absorbing Markov chain** (α = 0.9947). Recovery is mathematically impossible within 3 steps once failure occurs. Policy ordering theorem: ABSTAIN ≻ REGENERATE when α > 0.95. Context stripping *increases* amplified failures — a MODEL_BEHAVIOR_COLLAPSE mode.

Global Fisher J collapses completely (F-ratio = 0.007) at step 2 → local J (GUARDIAN) is the only viable solution.

| Finding | Value |
|---------|-------|
| CASCADE failure rate | **92.3%** (554/600 pipelines) |
| Cascade coefficient α | **0.9947** |
| Implied recovery horizon | **~189 steps** |
| Early-detection AUROC | **0.662** (pre-propagation) |
| F-ratio at step 2 | **0.007** — global J fails |

</td>
<td width="40%" align="center">

<a href="https://github.com/Lakshmi-Chakradhar-Vijayarao/fail-chain">
  <img src="https://img.shields.io/badge/GitHub-fail--chain-b71c1c?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<br/><br/>

<a href="https://fail-chain.streamlit.app/">
  <img src="https://img.shields.io/badge/Live%20Demo-Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white"/>
</a>

<br/><br/>

```
Markov cascade:
S1 wrong ──▶ S2 wrong
  α = 0.9947    │
                ▼
           S3 wrong
     P(recovery in 3) ≈ 0%
```

</td>
</tr>
</table>

---

## Project 5 — GUARDIAN

**Adaptive Reliability Governance via Local Fisher Separability**

<table>
<tr>
<td width="60%">

**Core finding:** Local Fisher J (FAISS k=50 KNN) enables real-time routing — ACCEPT / REGENERATE / ABSTAIN — on Mistral 7B at **0.77 ms per query** (0.14% overhead). Adaptive thresholds: false-accept rate 100% → 0% in-distribution via 3-zone reliability system.

Pre-registered P1 (70–90% depth peak): **CONFIRMED** at Layer 24 (75%). Pre-registered P2 (AUROC ≥ 0.75): **CONFIRMED** at 0.804.

| Metric | Value |
|--------|-------|
| CV probe AUROC | **0.804** |
| AUARC (reliable subset) | **0.783** |
| Routing latency | **0.77 ms** per query |
| OOD routing detection | **67.3%** in LOW zone |
| In-dist false-accept rate | **0.0%** (adaptive) |

</td>
<td width="40%" align="center">

<a href="https://github.com/Lakshmi-Chakradhar-Vijayarao/guardian">
  <img src="https://img.shields.io/badge/GitHub-guardian-00695c?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<br/><br/>

<a href="https://huggingface.co/spaces/Lakshmi-Chakradhar-Vijayarao/guardian-demo">
  <img src="https://img.shields.io/badge/Live%20Demo-HuggingFace-FFD21F?style=for-the-badge&logo=huggingface&logoColor=black"/>
</a>

<br/><br/>

```
Query → Local J (k=50)
   │
   ├─ HIGH  → ACCEPT
   ├─ MED   → REGENERATE
   └─ LOW   → ABSTAIN
    0.77 ms overhead
```

</td>
</tr>
</table>

---

## Key Numbers Across the Arc

<div align="center">

| Project | Model | Key Metric | Value | Significance |
|---------|-------|------------|-------|--------------|
| MECH-INT | GPT-2 Medium | Causal depth | **33–38%** | FFN over-retrieval layer |
| HaRP | Qwen 2.5 3B | OOD AUROC | **0.775** | +0.198 over entropy baseline |
| GEOM-PROOF | GPT-2 + Qwen | Bound max error | **≤ 2.7%** | Φ(√J/2) certificate |
| FAIL-CHAIN | Mistral + GPT | Cascade coeff α | **0.9947** | Nearly-absorbing chain |
| GUARDIAN | Mistral 7B | CV AUROC | **0.804** | P2 pre-registration confirmed |

</div>

---

## GitHub Stats

<div align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=Lakshmi-Chakradhar-Vijayarao&show_icons=true&theme=midnight-purple&include_all_commits=true&count_private=true&hide_border=true&bg_color=0d1117&title_color=1abc9c&icon_color=1abc9c&text_color=c9d1d9"/>
  &nbsp;
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Lakshmi-Chakradhar-Vijayarao&layout=compact&langs_count=8&theme=midnight-purple&hide_border=true&bg_color=0d1117&title_color=1abc9c&text_color=c9d1d9"/>
</div>

<div align="center">
  <img src="https://streak-stats.demolab.com?user=Lakshmi-Chakradhar-Vijayarao&theme=dark&hide_border=true&background=0d1117&ring=1abc9c&fire=1abc9c&currStreakLabel=1abc9c" alt="GitHub Streak"/>
</div>

<br/>

<div align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=Lakshmi-Chakradhar-Vijayarao&theme=darkhub&no-frame=true&no-bg=true&row=1&column=7&margin-w=10" alt="GitHub Trophies"/>
</div>

---

## Tech Stack

<details>
<summary><b>Languages & Frameworks</b></summary>
<br/>

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)

</details>

<details>
<summary><b>AI & ML Research</b></summary>
<br/>

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21F?style=for-the-badge&logo=huggingface&logoColor=black)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-13B1F4?style=for-the-badge&logo=langchain&logoColor=white)

**Research-specific:** FAISS · conformal prediction · optimal transport · mechanistic interpretability · Fisher separability · Sliced Wasserstein · UMAP · activation patching

</details>

<details>
<summary><b>Cloud, Data & DevOps</b></summary>
<br/>

![AWS](https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-0db7ed?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-00B4D8?style=for-the-badge&logo=mlflow&logoColor=white)

</details>

---

## Prior Systems Work

<details>
<summary><b>Applied AI & Systems Projects</b></summary>
<br/>

| Project | Domain | Method | Result |
|---------|--------|--------|--------|
| [**SafeRAG**](https://github.com/Lakshmi-Chakradhar-Vijayarao/SafeRAG) | RAG Safety | Atomic claim-level hallucination verification (ACCEPT / REJECT / REFUSE) | 3-tier decision system |
| [**MedRAG**](https://github.com/Lakshmi-Chakradhar-Vijayarao/MedRAG) | Clinical AI | Hybrid retrieval (dense + BM25) + post-generation verification | −34% hallucinations |
| [**RL-Retriever**](https://github.com/Lakshmi-Chakradhar-Vijayarao/rl-retriever) | Retrieval | PPO/DQN query rewriting agent | +28% recall |
| [**FinAgentX**](https://github.com/Lakshmi-Chakradhar-Vijayarao/finagentx) | Finance | Multi-agent system with LLM-driven portfolio decisions | Live trading sim |
| [**AlphaRoute**](https://github.com/Lakshmi-Chakradhar-Vijayarao/AlphaRoute_V2.0) | Trading | RL-based order routing engine | −18% slippage |
| [**AgroVision**](https://github.com/Lakshmi-Chakradhar-Vijayarao/AgroVision) | AgriTech | YOLO-based crop/weed detection | 90% mAP, −15% herbicide |
| [**neural-to-text-xai**](https://github.com/Lakshmi-Chakradhar-Vijayarao/neural-to-text-xai) | XAI | Neural network behavior → natural language explanations | Interpretability pipeline |
| [**x-orch-6G**](https://github.com/Lakshmi-Chakradhar-Vijayarao/x-orch-6g) | Networking | RL-based network orchestration for 6G xApp | Policy optimization |

</details>

---

## Contribution Activity

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Lakshmi-Chakradhar-Vijayarao&bg_color=0d1117&color=1abc9c&line=1abc9c&point=ffffff&area=true&hide_border=true" alt="Contribution Graph" width="100%"/>
</div>

<br/>

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Lakshmi-Chakradhar-Vijayarao/Lakshmi-Chakradhar-Vijayarao/output/github-contribution-grid-snake-dark.svg"/>
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Lakshmi-Chakradhar-Vijayarao/Lakshmi-Chakradhar-Vijayarao/output/github-contribution-grid-snake.svg"/>
    <img alt="GitHub contribution snake" src="https://raw.githubusercontent.com/Lakshmi-Chakradhar-Vijayarao/Lakshmi-Chakradhar-Vijayarao/output/github-contribution-grid-snake-dark.svg"/>
  </picture>
</div>

---

<div align="center">

**M.S. Computer Science · University of Texas at Dallas · May 2025**<br/>
Dallas, TX &nbsp;·&nbsp; lakshmichakradhar.v@gmail.com<br/><br/>

*All experiments pre-registered with git timestamps before execution.*<br/>
*Negative results reported alongside positive ones.*

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0,0e6655,1b4f72,0d1b2a&height=100&section=footer" width="100%"/>
