# Bitcoin Market Sentiment & Trader Performance Analysis

Exploring the relationship between the Crypto Fear & Greed Index and Hyperliquid perpetual trader behavior across 2024.

---

## Files

| File | Description |
|------|-------------|
| `sentiment_analysis.ipynb` | Main Jupyter Notebook — full analysis with visualizations |
| `sentiment_report.docx` | Short report — insights, findings & strategy recommendations |
| `fear_greed_index.csv` | Input dataset — daily Fear & Greed Index (2018–2025) |
| `historical_data.csv` | Input dataset — Hyperliquid trade logs (90,199 trades, 2024) |

---

## Datasets

**Fear & Greed Index** — 2,644 daily rows, sourced from alternative.me  
Columns: `date`, `value` (0–100), `classification` (Extreme Fear → Extreme Greed)

**Hyperliquid Trader Data** — 90,199 trades across 16 wallet addresses  
Columns: `Account`, `Coin`, `Execution Price`, `Size USD`, `Side`, `Direction`, `Closed PnL`, `Fee`, `Timestamp IST`

---

## How to Run

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter

jupyter notebook sentiment_analysis.ipynb
```

No API keys or external dependencies required. Both CSV files must be in the same directory as the notebook.

---

## Key Findings

- **Extreme Greed** → highest mean PnL per trade ($221.85)
- **Fear** → highest win rate (91.8%) — consistent entries, consistent exits
- **Position sizes shrink at sentiment extremes** — traders self-regulate risk
- Sentiment vs. PnL difference is **statistically significant** (ANOVA p = 0.034)
- Total portfolio PnL across 16 traders: **$7,529,944** over 2024

---

## Notebook Structure

1. Setup & Imports
2. Data Loading & Inspection
3. Data Cleaning (dates, types, deduplication)
4. Merging Datasets
5. PnL Analysis by Sentiment
6. Trading Activity & Volume
7. Long vs. Short Positioning
8. Cumulative PnL vs. Fear & Greed (time-series)
9. Per-Account Heatmap
10. PnL Distribution (violin plots)
11. Top Coins by Sentiment
12. Statistical Tests (ANOVA + Kruskal-Wallis)
13. Summary Insights Table

---

*Tools: Python 3, pandas, matplotlib, seaborn, scipy*
