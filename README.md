<!-- ============================================================ -->
<!--  HEADER — Terminal name + animated role                      -->
<!-- ============================================================ -->

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Roboto+Mono&weight=700&size=42&duration=1&pause=99999&color=00FF41&center=true&vCenter=true&width=700&height=80&lines=Sandeep+S" alt="Sandeep S" />

<img src="https://readme-typing-svg.demolab.com?font=Roboto+Mono&weight=400&size=20&duration=3500&pause=1200&color=00FF41&center=true&vCenter=true&width=700&height=50&lines=LLM+Security+Engineer;Adversarial+ML+Specialist;I+build+systems+that+defend+AI" alt="Roles" />

<br/>

<!-- Live status badges — animated hover via shields.io -->
<a href="https://agent-shield-chbxh2hkhxgucgax.eastasia-01.azurewebsites.net/health">
  <img src="https://img.shields.io/website?url=https%3A%2F%2Fagent-shield-chbxh2hkhxgucgax.eastasia-01.azurewebsites.net%2Fhealth&label=%F0%9F%9B%A1%EF%B8%8F%20Agent%20Shield%20API&style=for-the-badge&up_color=00FF41&down_color=FF3333&up_message=LIVE&down_message=DOWN&labelColor=0d1117" alt="API Status"/>
</a>
<a href="https://pypi.org/project/agent-shield-int/">
  <img src="https://img.shields.io/pypi/v/agent-shield-int?style=for-the-badge&logo=pypi&logoColor=white&label=PyPI&color=3775A9&labelColor=0d1117" alt="PyPI"/>
</a>
<a href="https://huggingface.co/Sandeep120205/agent-shield-distilbert">
  <img src="https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-Model-FFD21E?style=for-the-badge&labelColor=0d1117" alt="HuggingFace"/>
</a>
<a href="https://sonarcloud.io/project/overview?id=Sandeep-int_agent-shield">
  <img src="https://img.shields.io/badge/SonarCloud-Quality%20Gate%20%E2%9C%93-4E9BCD?style=for-the-badge&logo=sonarcloud&logoColor=white&labelColor=0d1117" alt="SonarCloud"/>
</a>

</div>

---

<!-- ============================================================ -->
<!--  ABOUT ME — Who, Specialized in, What I can build           -->
<!-- ============================================================ -->

## 👤 Who I Am

I'm a **Security Engineer** focused on LLM systems and adversarial machine learning.

I don't just write code — I **design attack surfaces, then close them**. Every decision I make starts with: *how does this break, and how do I stop that.*

**What I specialize in:**

| Area | What I do |
|------|-----------|
| 🔴 **LLM Threat Modeling** | Map how AI systems get compromised — injection, jailbreak, token smuggling |
| 🟡 **Adversarial ML** | Train models on attack data. Red-team my own systems. Measure detection gaps. |
| 🟢 **Secure AI Infrastructure** | Auth (BLAKE2b), rate limiting, PII sanitization, SIEM, CI/CD security gates |
| 🔵 **Detection Engineering** | Multi-layer pipelines: signatures → ML model → custom rules → LLM reasoning |

**What I can build for you:**
- Production prompt injection detection API — not a demo, not a prototype
- Adversarial red-team loop that attacks and hardens your LLM system automatically
- Security monitoring pipeline with Grafana SIEM + Azure Monitor alerts
- Custom threat detection rules tuned to your specific attack surface

---

<!-- ============================================================ -->
<!--  PROOF WALL — 5 numbers, no words needed                    -->
<!-- ============================================================ -->

## ⚡ Production Numbers

<div align="center">

| 🛡️ Live Requests | 🎯 Model Accuracy | 📊 Training Rows | 🔥 Detection Layers | 📦 PyPI |
|:---:|:---:|:---:|:---:|:---:|
| **703+** | **99.42%** | **291,471** | **4 layers** | **v1.0.3** |

</div>

---

<!-- ============================================================ -->
<!--  AGENT SHIELD — Featured Project                            -->
<!-- ============================================================ -->

## 🛡️ Agent Shield

> **Production LLM prompt injection detection API. 4 layers. Self-hardening. Live on Azure.**

**The detection pipeline — every prompt runs this gauntlet:**

```
  ┌──────────────────────────────────────────────────┐
  │  INCOMING PROMPT                                  │
  └──────────────────────┬───────────────────────────┘
                         │
                         ▼
  ┌──────────────────────────────────────────────────┐
  │  L1 — Vigil Signature Scanner          ~8ms      │
  │  Regex pattern match. Known jailbreaks.           │
  │  Catches: DAN, "ignore instructions", roleplay    │
  └──────────────────────┬───────────────────────────┘
                    PASS │
                         ▼
  ┌──────────────────────────────────────────────────┐
  │  L2 — DistilBERT ONNX Classifier      ~514ms     │
  │  Trained on 291,471 rows. Val acc 99.42%.         │
  │  10s timeout → auto BLOCK if inference hangs      │
  └──────────────────────┬───────────────────────────┘
                    PASS │
                         ▼
  ┌──────────────────────────────────────────────────┐
  │  L3 — Custom Rule Engine               ~2ms      │
  │  Base64 (10 depth), ROT13, homoglyphs,            │
  │  URL encoding, PII detection, toxic words         │
  └──────────────────────┬───────────────────────────┘
                    PASS │
                         ▼
  ┌──────────────────────────────────────────────────┐
  │  L4 — Groq Llama3 Reasoning           ~200ms     │
  │  Deep semantic analysis. Fire-and-forget.         │
  │  Advisory layer — flags social engineering        │
  └──────────────────────┬───────────────────────────┘
                    PASS │
                         ▼
  ┌──────────────────────────────────────────────────┐
  │  ✅ ALLOW — sanitize_prompt() → Azure Table log  │
  └──────────────────────────────────────────────────┘
```

**What makes Agent Shield different:**

| Capability | Agent Shield | Other tools |
|------------|:---:|:---:|
| 4-layer detection pipeline | ✅ | ❌ Most are 1 layer |
| Self-hardening via red-team loop | ✅ | ❌ Static rules only |
| Base64 / ROT13 / homoglyph decode | ✅ | ❌ |
| PII sanitization before logging | ✅ | ❌ |
| BLAKE2b API key hashing | ✅ | ❌ |
| Custom-trained model (291K rows) | ✅ | ❌ Generic pretrained |
| Live production on Azure | ✅ | ❌ Demo / local only |
| Grafana SIEM dashboard | ✅ | ❌ |
| CI/CD security gate (Bandit + pytest) | ✅ | ❌ |

[![GitHub](https://img.shields.io/badge/GitHub-agent--shield-181717?style=for-the-badge&logo=github&labelColor=0d1117)](https://github.com/Sandeep-int/agent-shield)
[![Live API](https://img.shields.io/badge/Live%20API-Azure-0078D4?style=for-the-badge&logo=microsoftazure&labelColor=0d1117)](https://agent-shield-chbxh2hkhxgucgax.eastasia-01.azurewebsites.net/health)
[![HF Space](https://img.shields.io/badge/UI-HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black&labelColor=0d1117)](https://huggingface.co/spaces/Sandeep120205/agent-shield)
[![Grafana](https://img.shields.io/badge/SIEM-Grafana-F46800?style=for-the-badge&logo=grafana&labelColor=0d1117)](https://sandeepint.grafana.net/d/agent-shield-siem/agent-shield)
[![PyPI](https://img.shields.io/badge/PyPI-agent--shield--int-3775A9?style=for-the-badge&logo=pypi&logoColor=white&labelColor=0d1117)](https://pypi.org/project/agent-shield-int/)

---

<!-- ============================================================ -->
<!--  AGENT STRIKE — Red Team Project                            -->
<!-- ============================================================ -->

## ⚔️ Agent Strike

> **Adversarial red-team agent. Attacks Agent Shield daily. Missed attacks become training data. The loop runs forever.**

```
  Agent Strike wakes (2AM daily via Azure Function)
          │
          ▼
  Generates hard attacks using Garak + Groq Llama3
          │
          ▼
  Fires attacks at Agent Shield /v1/check (internal key)
          │
          ├── BLOCKED → logged as True Positive ✅
          │
          └── ALLOWED → logged as False Negative ⚠️
                  │
                  ▼
          miss rate > 5% → triggers Kaggle retraining
                  │
                  ▼
          new ONNX model → Azure Blob → App Service restart
                  │
                  ▼
          Agent Shield stronger → Agent Strike generates harder attacks
                  │
                  ▼
                  ∞  (self-improving loop)
```

**Current results:** `FP 4%` | `FN 4%` | `96% detection rate`

[![GitHub](https://img.shields.io/badge/GitHub-agent--strike-FF4444?style=for-the-badge&logo=github&labelColor=0d1117)](https://github.com/Sandeep-int/agent-strike)

---

<!-- ============================================================ -->
<!--  PRODUCTION STACK — only what's shipped                     -->
<!-- ============================================================ -->

## 🛠️ Production Stack

> Only what I've actually shipped to production. No aspirational tools.

**Security & ML**

![Python](https://img.shields.io/badge/Python_3.11-3776AB?style=flat-square&logo=python&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX_Runtime-005CED?style=flat-square&logo=onnx&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Groq](https://img.shields.io/badge/Groq_Llama3-F55036?style=flat-square&logoColor=white)

**Cloud & Infrastructure**

![Azure App Service](https://img.shields.io/badge/Azure_App_Service-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Azure Blob](https://img.shields.io/badge/Azure_Blob_Storage-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Azure Table](https://img.shields.io/badge/Azure_Table_Storage-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Gunicorn](https://img.shields.io/badge/Gunicorn-499848?style=flat-square&logo=gunicorn&logoColor=white)

**Monitoring & Security**

![Grafana](https://img.shields.io/badge/Grafana_SIEM-F46800?style=flat-square&logo=grafana&logoColor=white)
![Azure Monitor](https://img.shields.io/badge/Azure_Monitor-4_Alert_Rules-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Bandit](https://img.shields.io/badge/Bandit-0_High_Issues-00C853?style=flat-square&logo=python&logoColor=white)
![SonarCloud](https://img.shields.io/badge/SonarCloud-Quality_Gate_%E2%9C%93-F3702A?style=flat-square&logo=sonarcloud&logoColor=white)
![CodeRabbit](https://img.shields.io/badge/CodeRabbit-AI_Review-FF6B35?style=flat-square&logoColor=white)

---

<!-- ============================================================ -->
<!--  GITHUB STATS                                                -->
<!-- ============================================================ -->

## 📊 GitHub Stats

<div align="center">

<img height="170em" src="https://github-readme-stats.vercel.app/api?username=Sandeep-int&show_icons=true&theme=chartreuse-dark&include_all_commits=true&count_private=true&hide_border=true&bg_color=0d1117&title_color=00FF41&icon_color=00FF41&text_color=c9d1d9&ring_color=00FF41"/>

<img height="170em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sandeep-int&layout=compact&theme=chartreuse-dark&hide_border=true&bg_color=0d1117&title_color=00FF41&text_color=c9d1d9"/>

</div>

<div align="center">

<img src="https://streak-stats.demolab.com/?user=Sandeep-int&theme=dark&hide_border=true&background=0d1117&stroke=00FF41&ring=00FF41&fire=FF4444&currStreakLabel=00FF41&sideLabels=00FF41&dates=888888" />

</div>

---

<!-- ============================================================ -->
<!--  CONTRIBUTION SNAKE                                          -->
<!-- ============================================================ -->

## 🐍 Contribution Activity

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Sandeep-int/Sandeep-int/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Sandeep-int/Sandeep-int/output/github-contribution-grid-snake.svg">
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/Sandeep-int/Sandeep-int/output/github-contribution-grid-snake-dark.svg">
</picture>

</div>

---

<!-- ============================================================ -->
<!--  CONNECT                                                     -->
<!-- ============================================================ -->

## 📡 Connect

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Sandeep_S-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0d1117)](www.linkedin.com/in/sandeep-int)
[![Email](https://img.shields.io/badge/Gmail-sandeep.int.2005-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0d1117)](mailto:sandeep.int.2005@gmail.com)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-Sandeep120205-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black&labelColor=0d1117)](https://huggingface.co/Sandeep120205)
[![PyPI](https://img.shields.io/badge/PyPI-agent--shield--int-3775A9?style=for-the-badge&logo=pypi&logoColor=white&labelColor=0d1117)](https://pypi.org/project/agent-shield-int/)

<br/>

```
Currently building  →  mDeBERTa L2.5 on HF Spaces (multilingual attack detection)
Open to             →  Security Engineer · AI Red Team · MLSec · LLM Security roles
```

</div>

---

<div align="center">
<sub><code>Built in production. Not a demo. Not a portfolio toy.</code></sub>
</div>
