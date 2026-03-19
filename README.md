# TRADX — AI Trading Copilot

> AI-powered trading assistant that analyzes charts, detects key levels and proposes trade setups using Claude AI + TradingView.

## Stack
- **Frontend:** HTML + Vanilla JS
- **Charts:** TradingView Embed Widget
- **AI Agent:** Claude Sonnet (Anthropic API)
- **Proxy:** Vercel Serverless Function
- **Deploy:** Vercel

## Setup

### 1. Clone
```bash
git clone https://github.com/samuelsrip/tradx.git
cd tradx
```

### 2. Deploy to Vercel
```bash
npm i -g vercel
vercel
```

### 3. Add environment variable in Vercel dashboard
```
ANTHROPIC_API_KEY=sk-ant-...
```

Settings → Environment Variables → Add `ANTHROPIC_API_KEY`

## Local dev
```bash
vercel dev
```
Then open `http://localhost:3000`

## Structure
```
tradx/
├── index.html          # Landing page
├── tradx-trading.html   # Trading app
├── api/
│   └── chat.js         # Serverless proxy → Anthropic API
├── vercel.json         # Vercel config
└── .gitignore
```

## Features
- TradingView real-time charts (BTC, ETH, SOL, BNB)
- AI agent chat powered by Claude
- Auto-detection of key levels (S/R, OBs, FVGs, liquidity)
- Trade setups with Entry / SL / TP / R:R
- Paper trading mode
- Decision logs

## License
MIT
