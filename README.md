# 🤖 Priced In

An autonomous AI-powered stock trading agent that executes trades on GitHub Actions, built with OpenAI's Agents framework.

<!-- auto start -->

## 💰 Portfolio value: $9,851.43** (-34.79% CAGR)

### 📊 Holdings

| Asset | Shares | Value |
|-------|--------|-------|
| Cash | - | $995.95 |
| TMO | 6 | $2798.52 |
| NVDA | 17 | $3030.42 |
| AMD | 2 | $348.62 |
| AAPL | 1 | $202.92 |
| PFE | 100 | $2475.00 |

### 📈 Recent trades

- **August 6, 2025 at 1:41:07 PM**: BUY 100 PFE @ $24.75/share ($2475.00)
- **August 6, 2025 at 1:38:44 PM**: SELL 3 NOW @ $905.12/share ($2715.36)
- **August 6, 2025 at 1:38:32 PM**: SELL 1 AMZN @ $213.75/share ($213.75)
- **August 6, 2025 at 1:38:17 PM**: SELL 1 ALNY @ $418.91/share ($418.91)
- **July 30, 2025 at 1:36:41 PM**: BUY 1 AMZN @ $231.01/share ($231.01)
- **July 30, 2025 at 1:36:18 PM**: BUY 1 AAPL @ $211.27/share ($211.27)
- **July 29, 2025 at 3:16:31 PM**: SELL 2 AMD @ $179.69/share ($359.38)
- **July 28, 2025 at 7:24:21 PM**: BUY 4 AMD @ $172.68/share ($690.72)
- **July 25, 2025 at 3:24:11 PM**: BUY 1 ALNY @ $326.64/share ($326.64)
- **July 24, 2025 at 7:01:52 PM**: BUY 17 NVDA @ $173.355/share ($2947.03)

<!-- auto end -->

- [🧠 Logs](./agent.log)
- [🧑‍💻 System prompt](./system-prompt.md)
- [📁 Source code](./agent.ts)

## 🛠️ Installation

1. Clone the repository:

```bash
git clone https://github.com/AnandChowdhary/priced-in.git
cd priced-in
```

2. Install dependencies:

```bash
npm install
```

3. Set up your OpenAI API key:

```bash
export OPENAI_API_KEY="your-api-key-here"
```

## 🏃‍♂️ Running the agent

The agent's portfolio is stored in `portfolio.json`:

```json
{
  "cash": 95.44,
  "holdings": {
    "AAPL": 4,
    "CLNE": 56
  },
  "history": [
    {
      "date": "2025-06-21T12:43:07.141Z",
      "type": "buy",
      "ticker": "AAPL",
      "shares": 4,
      "price": 201.5,
      "total": 806
    }
  ]
}
```

- **cash**: Available cash balance for trading
- **holdings**: Current stock positions (ticker: number of shares)
- **history**: Complete record of all trades

### Local execution

Run the trading agent manually:

```bash
npm start
```

This will execute one trading session where the agent will:

1. Check the current portfolio
2. Analyze market conditions
3. Make trading decisions
4. Update the portfolio

### Automated execution via GitHub Actions

The agent is configured to run automatically every hour via GitHub Actions. To enable this:

1. Fork this repository
2. Go to Settings → Secrets and variables → Actions
3. Add a new repository secret named `OPENAI_API_KEY` with your OpenAI API key
4. Optionally add a new repository variable named `MODEL` and set it to e.g., `o3` (default is o3 if not set).
5. The agent runs at 9am, 11am, 1pm, and 3pm EDT.

You can also trigger a manual run from the Actions tab in your GitHub repository.

## ⚠️ Disclaimer

This is an experimental AI trading agent for educational purposes. Real trading involves significant risk. Never invest money you cannot afford to lose.

## 📄 License

[MIT](./LICENSE) © [Anand Chowdhary](https://anandchowdhary.com)
