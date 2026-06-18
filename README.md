# 🎯 First Line — AI Cold Call Opener Builder

**The hardest part of a cold call is the first sentence.**

Paste a prospect's LinkedIn profile, add context, and get 3 ready-to-use cold call openers — each with the psychological reasoning behind it. Built by [Alex Roggero](https://www.linkedin.com/in/alexroggero/) and the [Crono](https://www.crono.one) team.

<p align="center">
  <a href="https://first-line-app.netlify.app">
    <img src="https://img.shields.io/badge/Try_it_live-00C7B7?style=for-the-badge&logo=netlify&logoColor=white" alt="Try it live">
  </a>
  <a href="https://ko-fi.com/firstline">
    <img src="https://img.shields.io/badge/Buy_us_a_coffee-FF5E5B?style=for-the-badge&logo=ko-fi&logoColor=white" alt="Ko-fi">
  </a>
</p>

---

## What it does

1. **Choose your language** — EN, IT, ES, FR, DE
2. **Paste the prospect's LinkedIn URL** → AI researches name, role, company, triggers, background in ~10 seconds
3. **Paste your company URL** → AI reads your site and fills in what you sell
4. **Adjust context** — persona, trigger, industry, company size, country, call type
5. **Click "Build my openers"** → get 3 complete, verbatim-ready openers with:
   - The technique used (name-drop, trigger-based, permission-based...)
   - A detailed explanation of *why* it works psychologically
   - One-click copy to clipboard

---

## Why this exists

Every SDR knows they should personalize their opener. Nobody gives them a fast, structured way to do it before each call. First Line does it in under a minute.

Built for SDRs who hate *"Hi, how are you today?"*

---

## Features

| Feature | Details |
|---|---|
| 🔍 **LinkedIn Research** | Auto-fills persona, company, industry, country, triggers |
| 🌐 **Website Reader** | Paste your company URL → auto-fills what you sell |
| 🌍 **5 Languages** | EN, IT, ES, FR, DE — full UI + AI output |
| 🎭 **Seniority-Aware Greetings** | C-level gets "Buongiorno Rossi", SDR gets "Ciao Marco" |
| 🧠 **3 Ready-to-Use Openers** | Complete, verbatim-ready with technique label |
| 📖 **Why It Works** | 4-6 sentence psychological breakdown per opener |
| 📋 **One-Click Copy** | Copy any opener directly to clipboard |
| 📖 **Cold Calling Playbook** | 8 collapsible principles from Gong, Cognism, Crono |

---

## Opener Techniques

Each build generates 3 openers using different techniques:

- **Name-drop / Referral** — "I was talking to someone from your [team] and they mentioned you'd be the right person"
- **Trigger-based** — references a specific recent event (funding, hiring, launch, leadership change)
- **Permission-based** — "I know this is out of the blue, can I get 30 seconds?"
- **Problem hypothesis** — leads with a quantified pain
- **Pattern interrupt** — breaks the "sales call" frame

---

## Architecture

```
┌─────────────────────────────────────────────┐
│              first-line.html                 │
│              (single file)                   │
├─────────────────────────────────────────────┤
│  UI Layer           │  AI Layer             │
│  ──────────         │  ──────────           │
│  Vanilla HTML/CSS/JS│  Claude Sonnet 4.6    │
│  5-language i18n    │  (opener generation)  │
│  Responsive mobile  │  Claude Haiku 4.5     │
│                     │  + Web Search         │
│                     │  (LinkedIn + website) │
└─────────────────────────────────────────────┘
```

**Zero backend. Zero frameworks. Zero build step.** One HTML file.

---

## Getting Started

### 1. Get an Anthropic API key
Sign up at [console.anthropic.com](https://console.anthropic.com)

### 2. Add your key
Open `first-line.html`, find line ~506:
```js
const API_KEY='PASTE_YOUR_KEY_HERE';
```
Replace with your `sk-ant-...` key.

### 3. Deploy
Drag and drop onto [app.netlify.com/drop](https://app.netlify.com/drop). Done.

### 4. Set a spending limit
[console.anthropic.com](https://console.anthropic.com) → Settings → Limits → set a monthly cap.

---

## Cost

| Action | Model | Est. cost |
|---|---|---|
| LinkedIn Research | Haiku 4.5 + Web Search | ~$0.01 |
| Website Reader | Haiku 4.5 + Web Search | ~$0.005 |
| Opener Generation | Sonnet 4.6 | ~$0.015 |

~$0.03 per full session.

---

## Contributing

PRs welcome:
- [ ] More languages (PT, JA, KO, ZH, AR, NL...)
- [ ] Leaderboard
- [ ] Email collection + PDF export
- [ ] CRM integrations
- [ ] Dark mode

---

## License

MIT — use it, fork it, make it yours.

---

## Credits

Built by **[Alex Roggero](https://www.linkedin.com/in/alexroggero/)** — Co-founder of [Crono](https://www.crono.one), Europe's leading execution layer for B2B sales teams.

---

<p align="center">
  <strong>because 'Hi, how are you today?' is not a strategy</strong><br><br>
  <a href="https://first-line-app.netlify.app">Try First Line →</a>
</p>
