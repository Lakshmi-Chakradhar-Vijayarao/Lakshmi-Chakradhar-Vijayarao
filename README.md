<img src="https://capsule-render.vercel.app/api?type=waving&color=0,050a14,0d2137,0e6655,1b4f72&height=240&section=header&text=Lakshmi%20Chakradhar%20Vijayarao&fontSize=42&fontColor=ffffff&fontAlignY=40&desc=Geometry-Based%20Governance%20of%20LLM%20Hallucination&descSize=17&descAlignY=62&animation=fadeIn" width="100%"/>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=22&pause=1200&color=1ABC9C&center=true&vCenter=true&width=800&height=45&lines=Prospective+PhD+Researcher+%E2%80%94+Reliable+AI+Systems;Geometry+is+the+language+of+failure+detection;5+Projects.+One+Arc.+Pre-registered+predictions.;Mechanism+%E2%86%92+Signal+%E2%86%92+Certificate+%E2%86%92+Dynamics+%E2%86%92+Governance;Negative+results+reported+alongside+positive+ones." alt="Typing SVG"/>
</p>

<p align="center">
  <a href="mailto:lakshmichakradhar.v@gmail.com">
    <img src="https://img.shields.io/badge/-lakshmichakradhar.v%40gmail.com-0d1b2a?style=for-the-badge&logo=gmail&logoColor=1abc9c"/>
  </a>
  &nbsp;
  <a href="https://linkedin.com/in/lakshmichakradharvijayarao">
    <img src="https://img.shields.io/badge/-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
  &nbsp;
  <a href="https://huggingface.co/Lakshmi-Chakradhar-Vijayarao">
    <img src="https://img.shields.io/badge/-HuggingFace-FFD21F?style=for-the-badge&logo=huggingface&logoColor=black"/>
  </a>
  &nbsp;
  <img src="https://img.shields.io/badge/-M.S.%20CS%20%C2%B7%20UT%20Dallas%202025-c0392b?style=for-the-badge&logo=academia&logoColor=white"/>
  &nbsp;
  <img src="https://komarev.com/ghpvc/?username=Lakshmi-Chakradhar-Vijayarao&style=for-the-badge&color=1abc9c&label=PROFILE+VIEWS"/>
</p>

<br/>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=soft&color=050a14&height=3" width="100%"/>
</div>

<br/>

<div align="center">

### ❝ Can we prove, from internal geometry alone, when a model is about to hallucinate — and govern it accordingly? ❞

</div>

<p align="center">
I study hallucination in large language models not as an alignment problem but as a <b>geometric one</b>.<br/>
Failures leave measurable signatures in representation space — my work traces those signatures<br/>
from their causal origin, through a mathematical certificate, through pipeline dynamics,<br/>
to a deployed adaptive routing system that acts on the signal in real time.
</p>

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=050a14&height=50&text=THE%205-PROJECT%20ARC&fontSize=22&fontColor=1abc9c&animation=fadeIn" width="100%"/>

<br/>

<div align="center">

<table>
<tr>
  <td align="center" width="19%">
    <img src="https://img.shields.io/badge/PROJECT%201-MECH--INT-1565c0?style=for-the-badge&logo=microscope&logoColor=white"/><br/>
    <b>Mechanism</b><br/>
    <sub>Where does the error originate?</sub><br/><br/>
    <kbd>GPT-2 Medium</kbd><br/>
    <kbd>534 samples</kbd>
  </td>
  <td align="center" width="4%"><b>→</b></td>
  <td align="center" width="19%">
    <img src="https://img.shields.io/badge/PROJECT%202-HaRP-6a1b9a?style=for-the-badge&logo=radar&logoColor=white"/><br/>
    <b>Signal</b><br/>
    <sub>Where does it become detectable?</sub><br/><br/>
    <kbd>Qwen 2.5 3B</kbd><br/>
    <kbd>TQA + HaluEval</kbd>
  </td>
  <td align="center" width="4%"><b>→</b></td>
  <td align="center" width="19%">
    <img src="https://img.shields.io/badge/PROJECT%203-GEOM--PROOF-1b5e20?style=for-the-badge&logo=math&logoColor=white"/><br/>
    <b>Certificate</b><br/>
    <sub>How do we certify the detection?</sub><br/><br/>
    <kbd>GPT-2 + Qwen</kbd><br/>
    <kbd>11 experiments</kbd>
  </td>
  <td align="center" width="4%"><b>→</b></td>
  <td align="center" width="19%">
    <img src="https://img.shields.io/badge/PROJECT%204-FAIL--CHAIN-b71c1c?style=for-the-badge&logo=link&logoColor=white"/><br/>
    <b>Dynamics</b><br/>
    <sub>How do errors propagate in pipelines?</sub><br/><br/>
    <kbd>Mistral + GPT</kbd><br/>
    <kbd>600 pipelines</kbd>
  </td>
  <td align="center" width="4%"><b>→</b></td>
  <td align="center" width="19%">
    <img src="https://img.shields.io/badge/PROJECT%205-GUARDIAN-00695c?style=for-the-badge&logo=shield&logoColor=white"/><br/>
    <b>Governance</b><br/>
    <sub>How do we act on the signal in real time?</sub><br/><br/>
    <kbd>Mistral 7B</kbd><br/>
    <kbd>TQA + HaluEval</kbd>
  </td>
</tr>
</table>

</div>

<br/>

---

<img src="https://capsule-render.vercel.app/api?type=rect&color=0a1628&height=50&text=%5B%20PROJECT%201%20%5D%20%20MECH-INT%20%E2%80%94%20Mechanistic%20Analysis%20of%20Hallucination&fontSize=16&fontColor=5b9bd5&animation=fadeIn&fontAlignY=62" width="100%"/>

<table>
<tr>
<td width="58%">

**Core finding:** Hallucination localizes causally to **Layers 8–9 (~33–38% depth)** in GPT-2 Medium via FFN over-retrieval — not attention pattern failure. Direct Logit Attribution (DLA) proves the wrong token is promoted by specific FFN components causally, not correlationally. A 12-stage interpretability pipeline over 534 manually curated samples.

<br/>

| Metric | Value |
|:-------|------:|
| Hallucination localization | **L8–9 · 33–38% depth** |
| Hidden-state probe AUROC | **0.604** vs 0.576 baseline |
| Representation sparsity | **87%** (100/768 active dims) |
| DLA causal attribution | FFN dominant, not attention |

</td>
<td width="42%" align="center">

<a href="https://github.com/Lakshmi-Chakradhar-Vijayarao/mech-int">
  <img src="https://img.shields.io/badge/GitHub-mech--int-1565c0?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<br/><br/>

<a href="https://mech-int.streamlit.app/">
  <img src="https://img.shields.io/badge/Research%20Brief-mech--int-1565c0?style=for-the-badge&logo=streamlit&logoColor=white"/>
</a>

<br/><br/>

<img src="https://img.shields.io/badge/Causal%20Depth-L8–9%20·%2033––38%25-1565c0?style=flat-square"/>
<br/>
<img src="https://img.shields.io/badge/AUROC-0.604-1565c0?style=flat-square"/>
<br/>
<img src="https://img.shields.io/badge/Method-FFN%20DLA%20Attribution-1565c0?style=flat-square"/>

</td>
</tr>
</table>

<br/>

---

<img src="https://capsule-render.vercel.app/api?type=rect&color=150a24&height=50&text=%5B%20PROJECT%202%20%5D%20%20HaRP%20%E2%80%94%20Hallucination-aware%20Representation%20Probing&fontSize=16&fontColor=b39ddb&animation=fadeIn&fontAlignY=62" width="100%"/>

<table>
<tr>
<td width="58%">

**Core finding:** The hallucination signal **crystallizes at L32 (89% depth)** in Qwen 2.5 3B, detectable at AUROC 0.775 OOD. Temperature scaling *degrades* hallucination calibration (ECE 0.071 → 0.395) — a counter-intuitive negative result reported transparently. 4-quadrant uncertainty decomposition: epistemic vs aleatoric × correct vs hallucinated.

<br/>

| Metric | Value |
|:-------|------:|
| In-domain probe AUROC | **0.758** (OOF-honest) |
| OOD AUROC (TQA → HaluEval) | **0.775** |
| ECE HaRP vs raw LLM | **0.039** vs 0.071 |
| Temperature scaling ECE | **0.395** — degraded ⚠ |
| Real-time latency | **23.9 ms** (<0.5% overhead) |

</td>
<td width="42%" align="center">

<a href="https://github.com/Lakshmi-Chakradhar-Vijayarao/harp">
  <img src="https://img.shields.io/badge/GitHub-harp-6a1b9a?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<br/><br/>

<a href="https://harpfind.streamlit.app/">
  <img src="https://img.shields.io/badge/Research%20Brief-harp-6a1b9a?style=for-the-badge&logo=streamlit&logoColor=white"/>
</a>

<br/><br/>

<img src="https://img.shields.io/badge/Signal%20Peak-L32%20·%2089%25%20Depth-6a1b9a?style=flat-square"/>
<br/>
<img src="https://img.shields.io/badge/OOD%20AUROC-0.775-6a1b9a?style=flat-square"/>
<br/>
<img src="https://img.shields.io/badge/Temp%20Scaling-HARMFUL%20⚠-b71c1c?style=flat-square"/>

</td>
</tr>
</table>

<br/>

---

<img src="https://capsule-render.vercel.app/api?type=rect&color=091a0e&height=50&text=%5B%20PROJECT%203%20%5D%20%20GEOM-PROOF%20%E2%80%94%20Geometric%20Certificates%20for%20Detection&fontSize=16&fontColor=81c784&animation=fadeIn&fontAlignY=62" width="100%"/>

<table>
<tr>
<td width="58%">

**Core finding:** Fisher separability J bounds probe AUROC via **Φ(√J/2)**, accurate within 2.7% max error across all layers and models. Conformal guarantee: P(hallucination) ≤ 0.07 at ~52.9% acceptance. SW2 > Fisher (Spearman 0.821 vs 0.458) — real distributions are non-Gaussian.

Scale curve: `AUROC = σ(8.62 · log₁₀(params) − 69.10)` &nbsp; R² = 0.9993.

<br/>

| Result | Value |
|:-------|------:|
| AUROC bound max error | **≤ 2.7%** across all layers + models |
| Scale curve R² | **0.9993** |
| Conformal α* | **0.07** at 52.9% acceptance |
| SW2 vs Fisher Spearman r | **0.821 vs 0.458** |
| Scale range validated | 117M → 3B → 7B |

</td>
<td width="42%" align="center">

<a href="https://github.com/Lakshmi-Chakradhar-Vijayarao/geom-proof">
  <img src="https://img.shields.io/badge/GitHub-geom--proof-1b5e20?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<br/><br/>

<a href="https://geom-proof.streamlit.app/">
  <img src="https://img.shields.io/badge/Research%20Brief-geom--proof-1b5e20?style=for-the-badge&logo=streamlit&logoColor=white"/>
</a>

<br/><br/>

<img src="https://img.shields.io/badge/Certificate-AUROC%20≈%20Φ(√J%2F2)-1b5e20?style=flat-square"/>
<br/>
<img src="https://img.shields.io/badge/Max%20Error-≤%202.7%25-1b5e20?style=flat-square"/>
<br/>
<img src="https://img.shields.io/badge/Scale%20R²-0.9993-1b5e20?style=flat-square"/>

</td>
</tr>
</table>

<br/>

---

<img src="https://capsule-render.vercel.app/api?type=rect&color=1a0505&height=50&text=%5B%20PROJECT%204%20%5D%20%20FAIL-CHAIN%20%E2%80%94%20Failure%20Propagation%20in%20Multi-Step%20Pipelines&fontSize=16&fontColor=ef9a9a&animation=fadeIn&fontAlignY=62" width="100%"/>

<table>
<tr>
<td width="58%">

**Core finding:** Self-refinement is a **nearly-absorbing Markov chain** (α = 0.9947). Recovery within 3 steps is mathematically impossible. Policy ordering theorem: **ABSTAIN ≻ REGENERATE** when α > 0.95. Context stripping *increases* amplified failures (MODEL_BEHAVIOR_COLLAPSE). Global Fisher J collapses at step 2 (F-ratio = 0.007) — local J is the only viable path.

<br/>

| Finding | Value |
|:--------|------:|
| CASCADE failure rate | **92.3%** (554 / 600 pipelines) |
| Cascade absorption α | **0.9947** |
| Recovery horizon 1/(1−α) | **~189 steps** |
| Early-detection AUROC | **0.662** (pre-propagation) |
| F-ratio at step 2 | **0.007** — global J fails |

</td>
<td width="42%" align="center">

<a href="https://github.com/Lakshmi-Chakradhar-Vijayarao/fail-chain">
  <img src="https://img.shields.io/badge/GitHub-fail--chain-b71c1c?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<br/><br/>

<a href="https://failchain.streamlit.app/">
  <img src="https://img.shields.io/badge/Research%20Brief-fail--chain-b71c1c?style=for-the-badge&logo=streamlit&logoColor=white"/>
</a>

<br/><br/>

<img src="https://img.shields.io/badge/Cascade%20Rate-92.3%25-b71c1c?style=flat-square"/>
<br/>
<img src="https://img.shields.io/badge/Absorption%20α-0.9947-b71c1c?style=flat-square"/>
<br/>
<img src="https://img.shields.io/badge/Policy-ABSTAIN%20≻%20REGEN-b71c1c?style=flat-square"/>

</td>
</tr>
</table>

<br/>

---

<img src="https://capsule-render.vercel.app/api?type=rect&color=041310&height=50&text=%5B%20PROJECT%205%20%5D%20%20GUARDIAN%20%E2%80%94%20Adaptive%20Governance%20via%20Local%20Fisher%20Geometry&fontSize=16&fontColor=4db6ac&animation=fadeIn&fontAlignY=62" width="100%"/>

<table>
<tr>
<td width="58%">

**Core finding:** Local Fisher J (FAISS k=50 KNN) enables real-time routing — **ACCEPT / REGENERATE / ABSTAIN** — on Mistral 7B at 0.77 ms per query (0.14% overhead). Three reliability zones with adaptive threshold pairs derived from conformal coverage. Pre-registered predictions confirmed: Layer 24 at 75% depth (P1 ✓), AUROC 0.804 (P2 ✓).

<br/>

| Metric | Value |
|:-------|------:|
| CV probe AUROC | **0.804** |
| AUARC (reliable subset) | **0.783** |
| Routing latency | **0.77 ms** per query |
| OOD in LOW reliability zone | **67.3%** vs 38.7% in-dist |
| In-dist false-accept rate | **0.0%** (adaptive thresholds) |

</td>
<td width="42%" align="center">

<a href="https://github.com/Lakshmi-Chakradhar-Vijayarao/guardian">
  <img src="https://img.shields.io/badge/GitHub-guardian-00695c?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<br/><br/>

<a href="https://guardiian.streamlit.app/">
  <img src="https://img.shields.io/badge/Research%20Brief-guardian-00695c?style=for-the-badge&logo=streamlit&logoColor=white"/>
</a>

<br/><br/>

<img src="https://img.shields.io/badge/AUROC-0.804-00695c?style=flat-square"/>
<br/>
<img src="https://img.shields.io/badge/Latency-0.77%20ms-00695c?style=flat-square"/>
<br/>
<img src="https://img.shields.io/badge/P1%20%26%20P2-✓%20CONFIRMED-00695c?style=flat-square"/>

</td>
</tr>
</table>

<br/>

---

<img src="https://capsule-render.vercel.app/api?type=rect&color=050a14&height=50&text=KEY%20NUMBERS%20ACROSS%20THE%20ARC&fontSize=20&fontColor=1abc9c&animation=fadeIn" width="100%"/>

<br/>

<div align="center">

| | Project | Model | Key Finding | Key Number | Significance |
|:-:|:--------|:------|:------------|:----------:|:-------------|
| 🔵 | **MECH-INT** | GPT-2 Medium | Causal hallucination depth | **33–38%** | FFN over-retrieval at L8–9 |
| 🟣 | **HaRP** | Qwen 2.5 3B | OOD AUROC | **0.775** | +0.198 over entropy baseline |
| 🟢 | **GEOM-PROOF** | GPT-2 + Qwen | AUROC bound max error | **≤ 2.7%** | Φ(√J/2) geometric certificate |
| 🔴 | **FAIL-CHAIN** | Mistral + GPT | Cascade absorption | **α = 0.9947** | Nearly-absorbing Markov chain |
| 🩵 | **GUARDIAN** | Mistral 7B Instruct | CV AUROC | **0.804** | P2 pre-registration confirmed |

</div>

<br/>

---

<img src="https://capsule-render.vercel.app/api?type=rect&color=050a14&height=50&text=TECH%20STACK&fontSize=20&fontColor=1abc9c&animation=fadeIn" width="100%"/>

<br/>

<div align="center">
  <img src="https://skillicons.dev/icons?i=python,pytorch,tensorflow,sklearn,fastapi,flask,streamlit,r&theme=dark&perline=8"/>
  <br/><br/>
  <img src="https://skillicons.dev/icons?i=aws,gcp,docker,kubernetes,github,git,linux,vscode&theme=dark&perline=8"/>
</div>

<br/>

<div align="center">

**Research-specific:**&nbsp;
<img src="https://img.shields.io/badge/FAISS-KNN%20Search-1565c0?style=flat-square"/>
<img src="https://img.shields.io/badge/Conformal%20Prediction-Coverage%20Bounds-1b5e20?style=flat-square"/>
<img src="https://img.shields.io/badge/Optimal%20Transport-Wasserstein-6a1b9a?style=flat-square"/>
<img src="https://img.shields.io/badge/Mechanistic%20Interp-DLA%20%2F%20Activation%20Patching-b71c1c?style=flat-square"/>
<img src="https://img.shields.io/badge/Fisher%20Separability-Local%20%26%20Global-00695c?style=flat-square"/>
<img src="https://img.shields.io/badge/Markov%20Chains-Cascade%20Modeling-e65100?style=flat-square"/>

</div>

<br/>

---

<img src="https://capsule-render.vercel.app/api?type=rect&color=050a14&height=50&text=PRIOR%20SYSTEMS%20WORK&fontSize=20&fontColor=1abc9c&animation=fadeIn" width="100%"/>

<br/>

<details>
<summary><b>&nbsp; Applied AI & Systems Projects — click to expand</b></summary>
<br/>

<div align="center">

| Project | Domain | Core Method | Result |
|:--------|:-------|:------------|-------:|
| [**SafeRAG**](https://github.com/Lakshmi-Chakradhar-Vijayarao/SafeRAG) | RAG Safety | Atomic claim-level verification (ACCEPT / REJECT / REFUSE) | 3-tier decision system |
| [**MedRAG**](https://github.com/Lakshmi-Chakradhar-Vijayarao/MedRAG) | Clinical AI | Hybrid retrieval (dense + BM25) + post-generation verification | −34% hallucinations |
| [**RL-Retriever**](https://github.com/Lakshmi-Chakradhar-Vijayarao/rl-retriever) | Retrieval | PPO/DQN query rewriting agent for retrieval-aware optimization | +28% recall |
| [**FinAgentX**](https://github.com/Lakshmi-Chakradhar-Vijayarao/finagentx) | Finance | Multi-agent LLM system with portfolio decision loop | Live trading sim |
| [**AlphaRoute**](https://github.com/Lakshmi-Chakradhar-Vijayarao/AlphaRoute_V2.0) | Trading | RL-based order routing engine | −18% slippage |
| [**AgroVision**](https://github.com/Lakshmi-Chakradhar-Vijayarao/AgroVision) | AgriTech | YOLO-based crop/weed detector | 90% mAP · −15% herbicide |
| [**neural-to-text-xai**](https://github.com/Lakshmi-Chakradhar-Vijayarao/neural-to-text-xai) | XAI | Neural behavior → natural language explanations | Interpretability pipeline |
| [**x-orch-6G**](https://github.com/Lakshmi-Chakradhar-Vijayarao/x-orch-6g) | Networking | RL-based xApp orchestration for 6G networks | Policy optimization |

</div>
</details>

<br/>

---

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=14&pause=2000&color=1ABC9C&center=true&vCenter=true&width=700&height=30&lines=All+experiments+pre-registered+with+git+timestamps+before+execution.+Negative+results+reported." alt="Footer typing"/>

<br/>

**M.S. Computer Science &nbsp;·&nbsp; University of Texas at Dallas &nbsp;·&nbsp; May 2025**<br/>
Dallas, TX &nbsp;·&nbsp; lakshmichakradhar.v@gmail.com

</div>

<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0,0e6655,1b4f72,050a14&height=120&section=footer" width="100%"/>
