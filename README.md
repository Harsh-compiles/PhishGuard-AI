# 🛡️ PhishGuard AI — Email Threat Analyzer

An AI-powered phishing email detector that doesn't just classify emails as safe or dangerous — it **explains exactly why**, highlighting the specific phrases, links, and patterns that triggered the alert. Built as part of a cybersecurity AI portfolio.

---

## 🔍 What It Does

Most phishing detectors are black boxes. PhishGuard AI works like an AI security analyst — it reads the email, makes a verdict, and shows its reasoning in plain English.

- **Classifies** emails as `PHISHING`, `SUSPICIOUS`, or `SAFE`
- **Risk scores** every email from 0–100
- **Highlights** the exact phrases and URLs that are suspicious (color-coded by severity)
- **Flags** specific threat indicators: urgency language, credential harvesting, impersonation, spoofed domains, suspicious TLDs
- **Tracks** scan history across your session
- **Explains** every decision — no black box

---

## 🚀 Live Demo

👉 [**Try it live →**](https://harsh-compiles.github.io/PhishGuard-AI/)

---

## 📸 Features

| Feature | Description |
|---|---|
| 🔴 Phishing Detection | NLP-based classification with confidence score |
| 🔦 Phrase Highlighting | Color-coded overlay on suspicious text spans |
| 🚩 Threat Flags | Per-indicator breakdown (urgency, impersonation, URLs) |
| 📋 Scan History | Session log of all analyzed emails |
| ⚡ Sample Emails | Built-in phishing and safe samples to demo instantly |

---

## 🧠 How It Works

```
Email Input
    ↓
Feature Extraction (URLs, headers, body text, sender analysis)
    ↓
NLP Classification Engine (DistilBERT-style analysis via Claude AI)
    ↓
SHAP-style Explainability → which spans drove the verdict
    ↓
Verdict + Risk Score + Highlighted Email + Threat Flags
```

The AI analyzes:
- **Sender patterns** — domain spoofing, lookalike addresses (paypa1.com vs paypal.com)
- **Urgency language** — "act now", "account suspended", "24 hours"
- **Credential requests** — SSN, credit card, password asks
- **Suspicious URLs** — newly registered domains, foreign TLDs, redirect chains
- **Impersonation signals** — brand names mismatched with sender domain

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| AI Engine | Claude AI (claude-sonnet-4) via Anthropic API |
| NLP Approach | Zero-shot classification + explainability extraction |
| Frontend | Vanilla HTML/CSS/JavaScript |
| Deployment | GitHub Pages (static, no backend needed) |
| Dataset Reference | PhishTank, CEAS corpus, Enron email dataset |

---

## 📂 Project Structure

```
phishguard-ai/
├── index.html       # Full app — UI + AI logic in one file
└── README.md
```

---

## ⚙️ Run Locally

No install needed. Just open `index.html` in your browser.

```bash
git clone https://github.com/yourusername/phishguard-ai
cd phishguard-ai
open index.html
```

---

## 🎯 Why I Built This

Phishing is the #1 entry point for enterprise breaches, yet most consumer tools just say "suspicious" with no explanation. I wanted to build something that works like a real analyst — one that a non-technical person could actually understand and act on.

This project demonstrates:
- Applied NLP for security classification
- Explainable AI (XAI) — surfacing model reasoning to the user
- Real-world threat indicator analysis (OWASP-aligned)
- Clean, deployable frontend with no dependencies

---

## 📊 Example Output

```
Verdict:     PHISHING
Risk Score:  94 / 100
Confidence:  97%

Flags:
  🔴 HIGH   · Urgency Language — "act now or account will be closed"
  🔴 HIGH   · Credential Harvesting — requests SSN and credit card
  🔴 HIGH   · Spoofed Domain — paypa1-verify.com ≠ paypal.com
  🟡 MED    · Foreign TLD — .ru domain linked in body
  🟡 MED    · Sender/Brand Mismatch — claims to be PayPal
```

---

## 👤 Author

**Harshith Pankaja Mahendra**  
CS Student @ University of New Brunswick  
[LinkedIn](https://www.linkedin.com/in/harshith-mahendra-b61aa02a1)

---

> Part of a two-project AI Cybersecurity Portfolio — see also [NetWatch AI](https://github.com/yourusername/netwatch-ai)
