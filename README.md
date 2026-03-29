# 💰 ET Money Mentor — AI-Powered Personal Finance Coach

> **ET AI Hackathon 2026** · Problem Statement 9: AI Money Mentor  
> Built with Claude AI (Anthropic) + Vanilla HTML/CSS/JS

[![Live Demo](https://img.shields.io/badge/Live%20Demo-View%20App-C9A84C?style=for-the-badge)](./ai-money-mentor.html)
[![Problem Statement](https://img.shields.io/badge/PS%209-AI%20Money%20Mentor-1E3A5F?style=for-the-badge)](https://economictimes.com)
[![Powered by Claude](https://img.shields.io/badge/Powered%20by-Claude%20AI-orange?style=for-the-badge)](https://anthropic.com)

---

## 🎯 The Problem

| Stat | Reality |
|------|---------|
| **95%** of Indians | Have no financial plan |
| **₹25,000+/year** | Cost of a qualified advisor |
| **14 Crore+** | Demat accounts in India |
| **₹46,800** | Average annual tax savings missed |

India's retail investors are flying blind — reacting to tips, missing tax savings, staying underinsured, and managing portfolios on gut feel. ET Money Mentor fixes this.

---

## 🚀 Solution — 3 AI-Powered Modules

### 1. 💰 Money Health Score
A 5-minute onboarding flow scoring your financial wellness across **6 dimensions**:
- Emergency Fund preparedness
- Investment Rate (% of income invested)
- Debt Health (debt-to-income ratio)
- Insurance Coverage adequacy
- Tax Efficiency (80C, NPS, HRA utilisation)
- Retirement Readiness

**Output:** 0–100 composite score + personalised 3-action plan + SIP allocation table

### 2. 🔥 FIRE Path Planner
Financial Independence, Retire Early — your personalised roadmap:
- Calculates exact **FIRE corpus** using 4% Safe Withdrawal Rate
- Computes **monthly SIP required** using future value of annuity
- Generates **year-by-year milestone timeline**
- Models scenarios: step-up SIP, delayed retirement

### 3. 🤖 AI Advisor Chat
Conversational AI financial advisor powered by **Claude Sonnet (Anthropic)**:
- Deep Indian finance knowledge: 80C, NPS, ELSS, SEBI, HRA
- Multi-turn conversation with session memory
- Never recommends specific stocks (SEBI compliant)
- Quick questions: prepay vs invest, old vs new tax regime, SIP recommendations

---

## 🏗 Architecture

```
User Input
    │
    ▼
┌─────────────────────────────────────────────┐
│           Orchestrator Agent                │
│  (routing, session state, error recovery)   │
└────────┬────────────────┬───────────────────┘
         │                │
    ┌────▼────┐      ┌────▼────────┐      ┌──────────────┐
    │Scoring  │      │FIRE Planning│      │LLM Chat Agent│
    │ Agent   │      │   Agent     │      │(Claude Sonnet│
    └────┬────┘      └────┬────────┘      └──────┬───────┘
         │                │                      │
         └────────┬───────┴──────────────────────┘
                  │
         ┌────────▼────────┐
         │ Compliance Guard │
         │ (SEBI filters)  │
         └────────┬────────┘
                  │
         ┌────────▼────────┐
         │   UI Renderer   │
         └─────────────────┘
```

**5 Specialised Agents:**
- **Orchestrator** — routes queries, manages state, handles errors
- **Scoring Agent** — rule-based 6-dimension financial wellness engine
- **FIRE Planning Agent** — deterministic corpus & SIP calculator
- **LLM Chat Agent** — Claude Sonnet with Indian finance system prompt
- **Compliance Guard** — SEBI rule filters + risk disclaimers

---

## ⚡ Quick Start

### Option 1 — Open Directly (No Setup Required)
```bash
# Just open the HTML file in any browser
open ai-money-mentor.html
```

### Option 2 — Local Server
```bash
# Python (recommended)
python3 -m http.server 8080
# Then open: http://localhost:8080/ai-money-mentor.html

# OR Node.js
npx serve .
```

### Option 3 — Deploy to GitHub Pages
```bash
git clone https://github.com/YOUR_USERNAME/et-money-mentor
cd et-money-mentor
# Enable GitHub Pages in repo settings → Source: main branch
```

---

## 🔑 API Key Setup (for AI Chat)

The AI Advisor Chat uses the Anthropic Claude API. To enable it:

1. Get a free API key at [console.anthropic.com](https://console.anthropic.com)
2. The app calls `https://api.anthropic.com/v1/messages` directly from the browser
3. For production: proxy API calls through a backend to protect your key

> **Note:** The Money Health Score and FIRE Planner work **fully offline** — no API key needed. Only the AI Chat requires the Anthropic API.

---

## 📊 Impact Model

Assuming **5 lakh active users** in Year 1:

| Impact Area | Calculation | Value |
|-------------|-------------|-------|
| Advisor cost saved | ₹25K/yr × 5L users | ₹1,250 Cr/yr |
| Better SIP returns | +10% returns × ₹10K SIP × 20 yrs | ₹8.5L per user |
| Tax savings unlocked | ₹46,800 avg × 5L users | ₹2,340 Cr/yr |
| ET premium upgrades | 15% conversion lift | +₹180 Cr ARR |

**Total societal value: ₹3,770+ Cr/year**

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Vanilla HTML5, CSS3, JavaScript (ES6+) |
| AI/LLM | Anthropic Claude Sonnet (`claude-sonnet-4-20250514`) |
| Scoring Engine | Pure JavaScript (deterministic, no LLM) |
| FIRE Calculator | JavaScript financial formulas (FV of annuity, 4% SWR) |
| Compliance | Rule-based JS filter (SEBI keyword blocklist) |
| Hosting | Static HTML — deploys anywhere, no server needed |
| Fonts | Google Fonts (Playfair Display + DM Sans) |

---

## 📁 File Structure

```
et-money-mentor/
├── ai-money-mentor.html        # Main application (single file)
├── pitch-video-script.html     # 3-minute video script
├── architecture_document.docx  # Agent architecture document
├── impact_model.md             # Quantified business impact
└── README.md                   # This file
```

---

## 🗺 Roadmap

- [ ] **Phase 2:** CAMS/KFintech PDF upload → MF Portfolio X-Ray
- [ ] **Phase 2:** Form 16 upload → automated Tax Wizard
- [ ] **Phase 3:** Hindi/Tamil/Telugu voice interface
- [ ] **Phase 3:** WhatsApp bot integration
- [ ] **Phase 4:** Couple's joint financial planning module
- [ ] **Phase 4:** Life event triggers (bonus, marriage, new baby)

---

## 👥 Team

Built by MBA students for the **ET AI Hackathon 2026**  
Avataar.ai (Hiring Partner) · Unstop (Hackathon Partner)

---

## ⚠️ Disclaimer

ET Money Mentor is an AI-powered educational tool. It does not constitute SEBI-registered investment advice. Always consult a qualified financial advisor for major financial decisions. Past performance of financial instruments does not guarantee future returns.

---

*Built with ❤️ for India's 14 crore+ investors*

