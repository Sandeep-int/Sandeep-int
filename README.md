<div align="center">
  <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&size=28&pause=1200&color=4A90D9&center=true&vCenter=true&width=700&lines=Hey%2C+I%27m+Sandeep" alt="Sandeep S" />
</div>

<br/>

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-Sandeep--int-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Sandeep-int)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Sandeep%20S-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sandeep-int/)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-Sandeep120205-FF9A00?style=for-the-badge&logo=huggingface&logoColor=white)](https://huggingface.co/Sandeep120205)

</div>

---

## About Me

## About Me

Security Engineer focused on LLM systems and adversarial ML.

I design attack surfaces — then close them. Every decision starts with: *how does this break, and how do I stop that.*

I build both sides of that question: **Agent Shield**, a production prompt injection firewall live on Azure since May 2026, and **Agent Strike**, the autonomous red-team system that attacks it — generating novel adversarial prompts, logging real false negatives, and feeding harder variants back into the loop.

Everything here is shipped and deployed. No tutorials. No demos.

---

## What I Specialise In

| Domain | What I Build |
|--------|-------------|
| **LLM Security** | Prompt injection detection, layered defense architecture, attack classification |
| **Adversarial ML / Red-Teaming** | Multi-agent attack generation (CrewAI), Garak-based vulnerability scanning, blindspot detection loops |
| **Secure API Design** | FastAPI, BLAKE2b auth, rate limiting, PII sanitization |
| **ML Infrastructure** | Transformer fine-tuning, ONNX deployment, model versioning, GPU training pipelines |
| **Cloud Engineering** | Azure App Service, Blob, Table, Monitor — production infra |
| **SOC / DevSecOps** | Grafana SIEM, GitHub Actions CI/CD, Bandit, SonarCloud |

---

## Flagship Project — Agent Shield

**Open source prompt injection firewall for production AI systems.**

**Built for:** AI teams, SaaS companies, and enterprises
shipping LLM-powered products who need input validation
before their first security incident — not after.

Intercepts malicious prompts before they reach your LLM. 5-layer detection pipeline. Self-improving via automated adversarial red-teaming. Live on Azure.

[![GitHub](https://img.shields.io/badge/GitHub-agent--shield-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Sandeep-int/agent-shield)
[![Live API](https://img.shields.io/badge/🔴%20Live-Azure-0078D4?style=for-the-badge&logoColor=white)](https://agent-shield-chbxh2hkhxgucgax.eastasia-01.azurewebsites.net)
[![PyPI](https://img.shields.io/badge/PyPI-agent--shield--int-3775A9?style=for-the-badge&logo=pypi&logoColor=white)](https://pypi.org/project/agent-shield-int/)
[![Demo](https://img.shields.io/badge/🤗%20Demo-HuggingFace-FF9A00?style=for-the-badge&logoColor=white)](https://huggingface.co/spaces/Sandeep120205/agent-shield)
[![CI](https://img.shields.io/github/actions/workflow/status/Sandeep-int/agent-shield/security-gate.yml?style=for-the-badge&logo=github&label=CI%20%7C%20156%20Tests&color=22c55e)](https://github.com/Sandeep-int/agent-shield/actions/workflows/security-gate.yml)

---

### The Moat

| Advantage | Why It Compounds |
|-----------|-----------------|
| **First-mover in open source LLM security** | No production-grade open source prompt injection firewall existed before this. |
| **Proprietary attack dataset** | Every blocked request adds to a dataset nobody can buy. Your traffic. Your attacks. |
| **Self-improving model** | Agent Strike attacks the system continuously. Misses become training data. Model retrains. |
| **100% true positive rate under red-team** | Tested against real adversarial attacks — not a benchmark dataset. |
| **$13/month infra** | First paying customer = profitable. Scales to B2/B3 as traffic grows. |
| **Open source distribution** | Stars → trust → integrations → word of mouth. Text layer is free on purpose. |
| **Multimodal roadmap** | Text + PDF are free and open source. URL, Image, and Video scanning are paid. |

---

### How It Works

Every prompt passes through 5 layers in sequence. One match = blocked.

| Layer | Model | Catches | Timeout |
|-------|-------|---------|---------|
| L1 | Vigil Signatures | Known jailbreaks, DAN, override patterns | N/A |
| L2 | DistilBERT ONNX | Semantic injection, adversarial phrasing | → BLOCK |
| L3 | mDeBERTa fp32 (HF Spaces) | Multilingual attacks, borderline cases | → ALLOW |
| L4 | Custom Rule Engine | Base64, ROT13, NATO, Atbash, Zalgo, Braille, Ecoji, homoglyphs, PII | N/A |
| L5 | Groq Llama3-70b | Social engineering, context-aware attacks | → ALLOW (advisory only) |

---

### Why 5 Layers — Key Decisions

**5 layers, not one model.**
One model has one blind spot. Layering catches what each individual layer misses.

**Fail-closed on owned infra. Fail-open on external.**
If our ML times out — BLOCK. If HuggingFace goes down — ALLOW. Users don't pay for third-party outages.

**Free text layer. Paid multimodal.**
Free = distribution and trust. Paid = PDF, Image, URL scanning. That's where revenue comes from.

**Model trains on its own attack traffic.**
No competitor can buy this dataset. It only exists because Agent Shield is live in production.

---

### Production Numbers

<div align="center">

| Metric | Value |
|--------|-------|
| Requests processed (live) | **265+** |
| Global block rate | **58.11%** |
| ML validation accuracy | **99.92%** |
| Agent Strike true positive rate | **100%** |
| Agent Strike false positive rate | **4%** |
| Tests passing | **156** |
| Bandit findings | **0 High · 0 Medium** |
| Avg detection latency | **~801ms** |
| Infra cost | **~$13/month on Azure** |

</div>

---

## Flagship Project — Agent Strike

**Autonomous LLM red-teaming framework. Built to break Agent Shield, on purpose.**

**Built for:** the same reason Agent Shield exists — you can't trust a detection
system's accuracy claims until something is actively trying to defeat it,
every day, with novel attacks no static benchmark ever covers.

Multi-agent system that generates new prompt injection attacks using an LLM, fires them at a live security API, and tracks every TP/FP/FN/TN outcome. False negatives don't get fixed manually — they get logged, mutated into harder variants, and re-tested automatically.

[![GitHub](https://img.shields.io/badge/GitHub-agent--strike-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Sandeep-int/agent-strike)
[![CrewAI](https://img.shields.io/badge/CrewAI-Multi--Agent-6E40C9?style=for-the-badge)](https://github.com/Sandeep-int/agent-strike)
[![Garak](https://img.shields.io/badge/Garak-9%20Attack%20Families-DC2626?style=for-the-badge)](https://github.com/Sandeep-int/agent-strike)

---

### The Moat

| Advantage | Why It Compounds |
|-----------|-----------------|
| **Attacks are LLM-generated, not static** | A hardcoded attack list goes stale. An agent that invents new ones doesn't. |
| **Closed feedback loop** | Every false negative becomes the next training input — no manual attack writing. |
| **Provider-independent** | Migrated off OpenRouter's routing layer to direct Groq inference after a provider-side block — no single point of failure on a third-party router. |
| **Honest measurement, not vanity metrics** | Reports real block rate under active adversarial pressure — including the misses. |
| **$2.50/month infra** | Groq free tier, Kaggle free GPU, Azure Table + Blob. Adversarial testing at near-zero cost. |

---

### How It Works

Generate novel attack (Groq + Qwen3-32B, reasoning_effort=none)

→ Fire at Agent Shield /v1/check

→ Log verdict (BLOCK/ALLOW) + latency → agent_results.csv

→ ALLOW verdict (false negative) → missed_samples.csv

→ blindspot_detector.py reads missed_samples.csv

→ Generates harder mutated variants of each miss

→ Re-fires mutated attacks → loop continues

10 attack categories: direct injection, persona hijack, roleplay escalation, token smuggling, multilingual switch, indirect/context injection, chain-of-thought hijack, fictional framing, base64 mid-sentence, authority impersonation.

---

### Production Numbers

<div align="center">

| Metric | Value |
|--------|-------|
| Total adversarial requests | **40,000+** |
| Blocked | **11,700+** |
| Adversarial block rate | **29.3%** |
| Attack families (Garak) | **9** |
| Avg attack latency | **~1,553ms** |
| Infra cost | **~$2.50/month** |

</div>

> **Why 29.3% and not 90%+:** this is adversarial traffic by design — every blocked attack here is one Agent Shield would have missed without Strike finding it first. Low block rate under active red-teaming surfaces real blind spots; it isn't a production accuracy number.

---

## Production Stack

> Only what I have actually shipped in production. No aspirational tools.

### Security & Detection

<div align="center">

![Python](https://img.shields.io/badge/Python%203.11-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=for-the-badge&logo=onnx&logoColor=white)
![DistilBERT](https://img.shields.io/badge/DistilBERT-FF9A00?style=for-the-badge&logo=huggingface&logoColor=white)
![mDeBERTa](https://img.shields.io/badge/mDeBERTa%20fp32-FF9A00?style=for-the-badge&logo=huggingface&logoColor=white)

</div>

### Cloud & Infrastructure

<div align="center">

![Azure App Service](https://img.shields.io/badge/Azure%20App%20Service-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Azure Blob](https://img.shields.io/badge/Azure%20Blob%20Storage-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Azure Table](https://img.shields.io/badge/Azure%20Table%20Storage-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Azure Monitor](https://img.shields.io/badge/Azure%20Monitor-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions%20CI%2FCD-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

</div>

### Monitoring & Code Quality

<div align="center">

![Grafana](https://img.shields.io/badge/Grafana%20SIEM-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Bandit](https://img.shields.io/badge/Bandit-0%20High%20Issues-22c55e?style=for-the-badge)
![SonarCloud](https://img.shields.io/badge/SonarCloud-Quality%20Gate%20✓-4E9BCD?style=for-the-badge&logo=sonarcloud&logoColor=white)
![CodeRabbit](https://img.shields.io/badge/CodeRabbit-AI%20Review-E05A2B?style=for-the-badge)
![pytest](https://img.shields.io/badge/pytest-156%20Tests%20Passing-22c55e?style=for-the-badge&logo=pytest&logoColor=white)

</div>

### ML Training & Fine-Tuning

<div align="center">

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Transformers](https://img.shields.io/badge/🤗%20Transformers-FF9A00?style=for-the-badge)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FF9A00?style=for-the-badge&logo=huggingface&logoColor=white)
![Kaggle](https://img.shields.io/badge/Kaggle%20T4x2-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)

</div>

### Agentic Systems & Red-Teaming

<div align="center">

![CrewAI](https://img.shields.io/badge/CrewAI-Multi--Agent-6E40C9?style=for-the-badge)
![Groq](https://img.shields.io/badge/Groq%20LPU-F55036?style=for-the-badge)
![Qwen3](https://img.shields.io/badge/Qwen3--32B-FF9A00?style=for-the-badge&logo=huggingface&logoColor=white)
![Garak](https://img.shields.io/badge/Garak-Vulnerability%20Scanning-DC2626?style=for-the-badge)
![LiteLLM](https://img.shields.io/badge/LiteLLM-1A1A2E?style=for-the-badge)

</div>

---

## Roadmap

| Input Type | Status |
|------------|--------|
| 📝 Text / Prompt injection | 🟢 Production · Open Source |
| 📄 PDF / Document scanning | 🟢 Open Source · Backlog |
| 🌐 URL / Webpage scan | 🔒 Paid · Backlog |
| 🖼️ Image OCR | 🔒 Paid · Backlog |
| 🎥 Video analysis | 🔒 Paid · Backlog |

| Agent Strike Pipeline | Status |
|------------------------|--------|
| Red Team Agent | 🟢 Live |
| Blindspot Detector | 🟢 Live |
| Blue Team Agent | 🟡 In Progress |
| Analyst Agent | 🔴 Planned |

---

## Activity

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Sandeep-int&show_icons=true&theme=transparent&title_color=4A90D9&icon_color=4A90D9&text_color=ffffff&bg_color=00000000&hide_border=true&rank_icon=github" height="160" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Sandeep-int&theme=transparent&ring=4A90D9&fire=4A90D9&currStreakLabel=4A90D9&sideLabels=4A90D9&hide_border=true" height="160" />
</div>

---

<div align="center">

**Open to:** Security Engineering · LLM Infrastructure · 
MLOps · DevSecOps · Founding Engineer roles

**For enterprise deployments, SLA, or custom integration:**
📩 sandeep.int.2005@gmail.com

**Agent Shield gets stronger every day. So do attackers. That's the point.**

</div>
