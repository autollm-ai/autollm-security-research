# AutoLLM Security Research

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
[![Disclosures](https://img.shields.io/badge/Disclosures-1-red.svg)]()
[![Research](https://img.shields.io/badge/autollm.ai%2Fresearch-active-purple.svg)](https://autollm.ai/research)

**Independent LLM attack research and responsible disclosure by [AutoLLM Security Research](https://autollm.ai).**

We study how large language models fail under adversarial conditions — and publish our findings openly so the industry can defend against them.

---

## Disclosed Attacks

| ID | Attack | Severity | Vector | Success Rate | Date | Full Disclosure |
|----|--------|----------|--------|:------------:|------|-----------------|
| SFE-001 | [Soft Follow-up Exfiltration](./attacks/SFE-001-soft-followup-exfiltration/) | 🔴 CRITICAL | Multi-turn conversation | 100% | Mar 19, 2026 | [autollm.ai/research/sfe](https://autollm.ai/research/sfe) |

> New disclosures are added as research is completed. Watch this repo to be notified.

---

## What This Repo Contains

Each attack disclosure lives in its own folder under `/attacks/` and follows a consistent structure:

```
attacks/
└── SFE-001-soft-followup-exfiltration/
    ├── README.md       ← Full technical disclosure
    ├── payload.txt     ← Canonical attack payload - not for all the attacks
    └── results.csv     ← Model × domain success rate data
```

**README.md** — The primary disclosure document. Contains the abstract, mechanism, four-step breakdown, canonical payload, results matrix, implications, defense analysis, distinction from prior work, and citation block. This is the document that should be cited.


---

## How to Read a Disclosure

Every disclosure follows the same section structure:

**Abstract** — What the attack is, why it works, and the one-line finding.

**Attack Mechanism** — The step-by-step breakdown of how the attack operates, including the psychological or architectural exploit it targets.

**Attack Payload** — The canonical payload used in testing. Copy-pasteable, reproducible, exact.

**Results Matrix** — Success rates across models and domains. Every cell is ≥20 independent trials with fresh conversation contexts.

**Implications** — What breaks in production. Written for specific deployment contexts — healthcare, fintech, edtech, enterprise — so operators can assess their own exposure.

**Defense** — What fails and why, followed by what actually works. Written to be actionable, not just descriptive.

**Distinction from Prior Work** — Where the attack sits relative to existing research. We cite the closest prior work and explain precisely what is new.

**Citation** — BibTeX and APA blocks, ready to copy.

---

## Responsible Disclosure Policy

We follow coordinated responsible disclosure principles:

1. Attack is identified and tested internally across target models and domains.
2. Disclosure email sent to affected providers before any public disclosure, responsibly, only with permission - where permission applies.
3. Public disclosure published at autollm.ai/research and this repository simultaneously.
4. Full academic paper submitted to arXiv following public disclosure.

We do not withhold findings for competitive advantage. We do not sell vulnerabilities. We publish because the industry cannot defend against attacks it does not know exist.

For private disclosure of a finding you believe affects AutoLLM products, contact **contact@autollm.ai**.

---

## Citation

If you use, reference, or build upon any finding in this repository, cite the specific attack disclosure. Each attack README contains its own BibTeX and APA citation block.

For the repository as a whole:

```bibtex
@misc{autollm2026research,
  author      = {AutoLLM Security Research},
  title       = {AutoLLM LLM Attack Disclosures},
  year        = {2026},
  publisher   = {GitHub},
  url         = {https://github.com/autollm-ai/autollm-security-research}
}
```

> **Usage requirement:** Any use of attack techniques, payload structures, or findings from this repository in research papers, security tools, CVE filings, blog posts, or conference presentations must include a citation to the specific disclosure. Commercial use requires explicit written permission. Contact **contact@autollm.ai**.

---

## License

This research is published under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/).

You may share and build upon this work for non-commercial purposes with attribution. Commercial use — including incorporating findings into paid security products or services — requires explicit written permission from AutoLLM.

Full license terms in [LICENSE](./LICENSE).

---

## About AutoLLM

AutoLLM builds LLM security and governance infrastructure for enterprises. Our products are informed directly by our research.

- **Chaos Probe** — LLM security auditor. Scans for known attack vectors including all attacks disclosed in this repository, plus 800+ additional vectors.
- **Warden LLM** — Runtime safety wrapper. Defends against attack classes discovered through our research program in production, 24/7, autonomously.

[autollm.ai](https://autollm.ai) · [autollm.ai/research](https://autollm.ai/research) · contact@autollm.ai
