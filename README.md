# 🤖 Priced In

An autonomous AI-powered stock trading agent that executes trades on GitHub Actions, built with OpenAI's Agents framework.

<!-- auto start -->

## 💰 Portfolio value: $9,812.98** (-27.13% CAGR)

### 📊 Holdings

| Asset | Shares | Value |
|-------|--------|-------|
| Cash | - | $1283.23 |
| PFE | 100 | $2511.00 |
| PLTR | 5 | $905.10 |
| SQ | 20 | $1739.20 |
| WMT | 20 | $2017.00 |
| UNH | 5 | $1357.45 |

### 📈 Recent trades

- **August 15, 2025 at 1:31:06 PM**: BUY 5 UNH @ $271.49/share ($1357.45)
- **August 15, 2025 at 1:25:59 PM**: SELL 5 NVDA @ $182.02/share ($910.10)
- **August 13, 2025 at 1:31:38 PM**: BUY 20 WMT @ $103.62/share ($2072.40)
- **August 13, 2025 at 1:30:46 PM**: SELL 5 NVDA @ $183.16/share ($915.80)
- **August 11, 2025 at 1:33:10 PM**: SELL 7 NVDA @ $182.7/share ($1278.90)
- **August 11, 2025 at 1:32:58 PM**: SELL 1 AAPL @ $229.35/share ($229.35)
- **August 8, 2025 at 1:44:51 PM**: BUY 20 SQ @ $86.96/share ($1739.20)
- **August 7, 2025 at 1:38:25 PM**: BUY 5 PLTR @ $179.54/share ($897.70)
- **August 7, 2025 at 1:36:10 PM**: SELL 2 AMD @ $163.12/share ($326.24)
- **August 7, 2025 at 1:36:00 PM**: SELL 6 TMO @ $448.94/share ($2693.64)

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
