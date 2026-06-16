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

Security Engineer focused on LLM systems and adversarial ML.

I design attack surfaces — then close them. Every decision starts with: *how does this break, and how do I stop that.*

Currently building **Agent Shield** — an open source prompt injection firewall running live on Azure under real production traffic since May 2026.

Everything here is shipped and deployed. No tutorials. No demos.

---

## What I Specialise In

| Domain | What I Build |
|--------|-------------|
| **LLM Security** | Prompt injection detection, adversarial red-teaming, attack classification |
| **ML Infrastructure** | ONNX deployment, model fine-tuning, self-improving retraining loops |
| **Cloud Engineering** | Azure App Service, Blob, Table, Monitor — production infra |
| **Secure API Design** | FastAPI, BLAKE2b auth, rate limiting, PII sanitization |
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
[![CI](https://img.shields.io/github/actions/workflow/status/Sandeep-int/agent-shield/security-gate.yml?style=for-the-badge&logo=github&label=CI%20%7C%20146%20Tests&color=22c55e)](https://github.com/Sandeep-int/agent-shield/actions/workflows/security-gate.yml)

---

### The Moat 

| Advantage | Why It Compounds |
|-----------|-----------------|
| **First-mover in open source LLM security** | No production-grade open source prompt injection firewall existed before this. |
| **Proprietary attack dataset** | Every blocked request adds to a dataset nobody can buy. Your traffic. Your attacks. |
| **Self-improving model** | Agent Strike attacks nightly. Misses become training data. Model retrains automatically. |
| **96% detection under red-team** | Tested against real adversarial attacks — not a benchmark dataset. |
| **$13/month infra** | First paying customer = profitable. Scales to B2/B3 as traffic grows. |
| **Open source distribution** | Stars → trust → integrations → word of mouth. Text layer is free on purpose. |
| **Multimodal roadmap** | Text + PDF are free and open source. URL, Image, and Video scanning are paid.|

---

### How It Works

Every prompt passes through 5 layers in sequence. One match = blocked.

| Layer | Model | Catches | Timeout |
|-------|-------|---------|---------|
| L1 | Vigil Signatures | Known jailbreaks, DAN, override patterns | N/A |
| L2 | DistilBERT ONNX | Semantic injection, adversarial phrasing | → BLOCK |
| L3 | mDeBERTa fp32 (HF Spaces) | Multilingual attacks, borderline cases | → ALLOW |
| L4 | Custom Rule Engine (458 rules) | Base64, ROT13, homoglyphs, PII, 14 encoding schemes | N/A |
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
| Requests processed (live) | **703+** |
| Global block rate | **67%** |
| ML validation accuracy | **99.42%** |
| Training dataset | **291,471 rows** |
| Agent Strike true positive rate | **96%** |
| Agent Strike false positive rate | **4%** |
| Tests passing | **146** |
| Bandit findings | **0 High · 0 Medium** |
| Avg detection latency | **~741ms** |
| Infra cost | **~$13/month on Azure** |

</div>

---

### Agent Strike — Self-Improving Red-Team Loop

Automated adversarial agent that attacks Agent Shield nightly. Missed attacks become training data. Model retrains. Loop repeats.

```
Wake up 2AM (Azure Function)
  → Generate multilingual attacks (Garak + Groq Llama3)
  → Fire at /v1/check (internal key · no rate limit)
  → Log BLOCK / ALLOW + latency → Azure Table
  → Missed attacks → Azure Blob dataset
  → Miss rate > 5% → Kaggle T4x2 retraining
  → New mDeBERTa ONNX → Azure Blob → App Service restart
  → Loop forever
```

**Cost: ~$2.50/month.** Groq free · Kaggle free · Azure Table + Blob.

---

## Production Stack

> Only what I have actually shipped in production. No aspirational tools.

### Security & ML

<div align="center">

![Python](https://img.shields.io/badge/Python%203.11-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX%20Runtime-005CED?style=for-the-badge&logo=onnx&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FF9A00?style=for-the-badge&logo=huggingface&logoColor=white)
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

### Monitoring & Security

<div align="center">

![Grafana](https://img.shields.io/badge/Grafana%20SIEM-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Bandit](https://img.shields.io/badge/Bandit-0%20High%20Issues-22c55e?style=for-the-badge)
![SonarCloud](https://img.shields.io/badge/SonarCloud-Quality%20Gate%20✓-4E9BCD?style=for-the-badge&logo=sonarcloud&logoColor=white)
![CodeRabbit](https://img.shields.io/badge/CodeRabbit-AI%20Review-E05A2B?style=for-the-badge)
![pytest](https://img.shields.io/badge/pytest-146%20Tests%20Passing-22c55e?style=for-the-badge&logo=pytest&logoColor=white)

</div>

### ML & Training

<div align="center">

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Transformers](https://img.shields.io/badge/🤗%20Transformers-FF9A00?style=for-the-badge)
![Kaggle](https://img.shields.io/badge/Kaggle%20T4x2-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)
![Groq](https://img.shields.io/badge/Groq%20Llama3%2070b-F55036?style=for-the-badge)

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
