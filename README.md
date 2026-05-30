# 📈 AI Stock Radar – Professional Research Dashboard

A **professional AI-powered stock ranking dashboard** designed for personal research and experimentation.

## Features

- ✅ **No API keys required** – Uses public web pages with local fallback data
- ✅ **Free deployment** – Designed for Streamlit Community Cloud
- ✅ **Intelligent scoring** – Momentum, volatility, and news sentiment analysis
- ✅ **Universe scanning** – Pre-configured watchlists (mega-cap, tech, defensive)
- ✅ **Interactive charts** – Plotly-powered price and moving average visualization
- ✅ **Win/Loss probability** – Confidence-weighted market outlook

## Getting Started

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/wseza24-code/ai-stock-radarseza.git
   cd ai-stock-radarseza
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the app**
   ```bash
   streamlit run app.py
   ```

### Deploy on Streamlit Cloud

1. Push this repository to GitHub
2. Go to [Streamlit Cloud](https://share.streamlit.io/)
3. Click "New app" and select this repository
4. Set the main file path to `app.py`
5. Click "Deploy"

## How It Works

### Scoring Algorithm

The dashboard calculates a **0–100 score** based on:

- **Momentum (55%)**: 1-month and 3-month price changes
- **Trend (35%)**: 20-day price movement direction
- **Volatility Penalty (-30%)**: Annualized volatility adjustment (higher risk = lower score)
- **News Bias (±4)**: Sentiment from public Yahoo Finance headlines

### Bias Labels

- **Bullish**: Score ≥ 70
- **Neutral**: 35 < Score < 70
- **Cautious**: Score ≤ 35

### Confidence Score

Reflects prediction reliability based on:
- Historical data length (120+ days = max confidence)
- Moving average slope stability
- Volatility consistency

## Data Sources

- **Prices**: Local fallback historical data for TSLA, AAPL, MSFT
- **News**: Public Yahoo Finance headlines (when accessible)
- **Fallback**: All tickers default to AAPL data if not available locally

## Disclaimer

⚠️ **This tool is for research and experimentation only.**

- **Does NOT provide financial advice**
- Scores are statistical models with no future guarantees
- All trading involves risk of loss
- Markets change; models decay
- Past performance ≠ future results

Use responsibly. Always do your own due diligence.

## License

MIT License – See LICENSE file for details

## Contributing

Contributions welcome! Feel free to submit issues or pull requests for improvements.

---

Built with ❤️ using [Streamlit](https://streamlit.io/) and [Plotly](https://plotly.com/)
