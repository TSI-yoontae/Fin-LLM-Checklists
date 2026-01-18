<div align="center">

# Position: Financial LLM Evaluation Requires Explicit Bias Consideration

<p align="center">
<strong>Large Language Models are increasingly integrated into financial workflows, yet their evaluation remains vulnerable to domain-specific biases.</strong>
</p>

[Read the Paper](#) | [Use the Checklist] 

</div>

## 📌 Abstract

We argue that current evaluation practices for Financial LLMs are insufficient. They often fail to account for domain-specific biases that distort performance assessments and compromise downstream decision-making. We identify five recurring sources of bias ("The Five Sins") and propose a Structural Validity Framework to address them.

This repository hosts the Interactive Evaluation-Guidance Checklist, a tool designed to help researchers and practitioners diagnose these biases and design fairer, more reliable financial systems.

---

## 🛑 The "Five Sins" of Financial LLM Evaluation

Our paper identifies five critical pitfalls that inflate performance metrics and hide risks.

| Bias | Definition | The Risk |
| :--- | :--- | :--- |
| **1. Look-Ahead Bias** | Information unavailable at decision time $t$ leaks into the model. | Predicting the past using future knowledge ("Time Travel"). |
| **2. Survivorship Bias** | Excluding entities that failed or were delisted. | Ignoring downside risk by only evaluating "winners." |
| **3. Narrative Bias** | Generating coherent stories unsupported by evidence. | Creating an "Illusion of Understanding" that masks complexity. |
| **4. Objective Bias** | Rewarding confident guessing over abstention. | Hallucinating certainty instead of admitting ignorance. |
| **5. Cost Bias** | Ignoring fees, slippage, and inference latency. | Strategies that look profitable but lose money in production. |

---

## 🛠️ Interactive Checklist Tool

We provide a web-based implementation of our Structural Validity Framework. You do not need to install any local code. This tool allows authors and reviewers to audit financial LLM systems against the criteria defined in our paper.

### [👉 Click Here to Open the Checklist](Will be updated because of anonymous)

**How to use:**

1.  **Access the Tool:** Navigate to the link above.
2.  **Self-Assessment:** Review your system against the 5 structural pillars.
3.  **Export:** Generate a PDF report to attach to your paper or documentation.

---

## 📋 The Structural Validity Framework

The checklist enforces minimum requirements for a result to be considered "deployable alpha" rather than a theoretical artifact.

* **Temporal Sanitation:** Enforce strict non-anticipativity. Verify knowledge cutoffs and ensure RAG retrieval only accesses documents available at time $t$.
* **Dynamic Universe Construction:** Include delisted and bankrupt firms. Sample from the universe as it existed at time $t$, not the current universe.
* **Epistemic Calibration:** Reward abstention ("I don't know"). The action space must include a "No Trade" option to prevent confident hallucinations.
* **Rationale Robustness:** Ground rationales in verifiable evidence. Pass entity substitution tests to prove reasoning is not merely memorization.
* **Realistic Implementation:** Report Net Utility. Deduct transaction costs and account for price slippage caused by LLM inference latency ($\Delta_{gen}$).

---

## 🖊️ Citation

If you use this framework or the checklist tool in your research, please cite our paper:

```bibtex
Todo
