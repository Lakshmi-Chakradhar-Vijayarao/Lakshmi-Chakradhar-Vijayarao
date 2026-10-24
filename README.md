<img src="https://capsule-render.vercel.app/api?type=waving&color=0,050a14,0d2137,0e6655,1b4f72&height=220&section=header&text=Lakshmi%20Chakradhar%20Vijayarao&fontSize=42&fontColor=ffffff&fontAlignY=40&desc=Measurement%20Validity%20in%20LLM%20Reliability&descSize=17&descAlignY=62&animation=fadeIn" width="100%"/>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=20&pause=1400&color=1ABC9C&center=true&vCenter=true&width=820&height=45&lines=Prospective+PhD+researcher+%E2%80%94+reliable+and+verifiable+AI;Does+the+number+reflect+the+model+or+the+instrument%3F;Pre-registered.+Held-out.+Negative+results+reported." alt="Typing SVG"/>
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
</p>

## Research focus

I study when the evidence used to make claims about large language models can be trusted: whether a detector score, a label, a geometric certificate or an intervention result reflects the **model** or the **instrument** that measured it. I build the checks that tell the two apart, and use them to test what a model's internal states actually reveal about its own errors.

- Validity of evaluation evidence: data reuse, leakage, label quality and statistical testing
- What hidden states reveal about model errors, and what they do not
- When null and positive results in causal interpretability are informative
- Reliability of multi-step agents and associative memory systems

## Papers

| Paper | Status | Code |
|:--|:--|:--|
| **Data Reuse, Not Selection: A Code-Verified Audit of Optimism in Hidden-State Hallucination-Detection Pipelines**<br/><sub>Reusing evaluation data to configure a detector makes its confidence thresholds let through more errors than they promise: 0.85 extra unflagged errors per 100 answers across 25 independent samples. The cost comes from reusing data, not from selection.</sub> | Accepted, NeurIPS 2026 Workshop on Trustworthy AI Evaluation (poster). Extended version under review at TMLR. | [selection-leakage-calibration-audit](https://github.com/Lakshmi-Chakradhar-Vijayarao/selection-leakage-calibration-audit) |
| **AIG: Towards a Mechanistic Science of Retrieval Integrity in Associative Memory Systems**<br/><sub>Retrieval geometry in correlation-matrix memories degrades before output accuracy fails; a retrieval isolation score warns ahead of failure in 94.4% of 270 trials.</sub> | Presented, MeMo Workshop, University of Rome Tor Vergata, June 2026. Proceedings to appear in CEUR-WS. | [aig-associative-memory-governance](https://github.com/Lakshmi-Chakradhar-Vijayarao/aig-associative-memory-governance) |
| **Self-Refinement Failure in Multi-Step LLM Pipelines: A Re-audit with Measured Difficulty**<br/><sub>An apparent early-warning signal of agent self-correction failure was answer length under ROUGE-L labels and question difficulty under corrected ones (difficulty alone: AUROC 0.96–0.97 on NQ-open).</sub> | In revision | [agentic-failure-taxonomy](https://github.com/Lakshmi-Chakradhar-Vijayarao/agentic-failure-taxonomy) |
| **Uninterpretable Nulls in Interpretability Intervention Studies: A Closed-Book Case Study and a Validity Checklist**<br/><sub>"Patching changed nothing" is evidence only if the experiment could have detected a change. An eleven-item checklist makes that testable.</sub> | Manuscript | [ffn-mechanism-audit](https://github.com/Lakshmi-Chakradhar-Vijayarao/ffn-mechanism-audit) |
| **A Loose Ceiling, Not a Certificate: Auditing Fisher-Separability Bounds on Hallucination Detectability**<br/><sub>The training-free bound is never violated but over-predicts probe AUROC by 0.29–0.41; most of the gap is estimator bias.</sub> | Manuscript | [geom-proof](https://github.com/Lakshmi-Chakradhar-Vijayarao/geom-proof) |
| **Confident and Wrong: Detecting Confabulation from Hidden States Where Output Confidence Is Blind**<br/><sub>Among equally confident answers, a probe at a pre-fixed layer separates correct from confabulated answers (AUROC 0.854 vs 0.614 for entropy on Qwen2.5-1.5B).</sub> | In preparation | [detection-without-control](https://github.com/Lakshmi-Chakradhar-Vijayarao/detection-without-control) |
| **Committed Before Thinking: Reasoning Models Settle Their Answer Early**<br/><sub>Truncating at a hidden-state commitment point cut thinking tokens by 90% at an F1 cost of 0.012 (pre-registered, N = 500; one model, one task so far).</sub> | In preparation | [detection-without-control](https://github.com/Lakshmi-Chakradhar-Vijayarao/detection-without-control) |

## How I work

- Experiments are pre-registered with kill criteria, evaluated on held-out data, and tested against permutation nulls with multiple-testing correction.
- Every claim is tracked in a claims registry. When a held-out or controlled test fails, the claim is withdrawn and the record says so.
- Repositories from earlier phases carry a dated status note at the top pointing to the version that replaced them.

## Earlier projects (2025)

These were the starting point for the papers above. Several of their headline claims were later revised by those papers; each repository's README opens with a status note.

| Project | What it was | Where it led |
|:--|:--|:--|
| [mech-int](https://github.com/Lakshmi-Chakradhar-Vijayarao/mech-int) | Component-level analysis of hallucination in GPT-2 | Uninterpretable Nulls |
| [harp](https://github.com/Lakshmi-Chakradhar-Vijayarao/harp) | Hidden-state hallucination detector on Qwen2.5-3B | Data Reuse, Not Selection |
| [fail-chain](https://github.com/Lakshmi-Chakradhar-Vijayarao/fail-chain) | Failure propagation in self-refinement pipelines | Self-Refinement Failure re-audit |
| [guardian](https://github.com/Lakshmi-Chakradhar-Vijayarao/guardian) | Local-Fisher reliability filter on Mistral-7B | Data Reuse, Not Selection |

## Open-source software

**[Credence](https://github.com/Lakshmi-Chakradhar-Vijayarao/credence-ai)**: an MCP server that tracks unverified claims in AI coding sessions (rate limits, software versions, thresholds) and blocks file writes that depend on them until they are confirmed.

## Service

Reviewer, NeurIPS 2026 Workshop "Who Verifies the Agents? Toward Reliable Agent Development".
