

# Stablecoin Liquidity Rotation Dashboard

**A data‑driven look at where stablecoin capital is moving across Ethereum, Arbitrum, and Polygon.**


##  Project Overview

This project explores a simple but overlooked question in crypto: *"Where is liquidity actually staying?"**

Most dashboards track volume, but volume only tells you where activity happened—it doesn't tell you if that capital is sticking around or just passing through.

To answer the deeper question, I built a dashboard that analyzes **USDC and USDT transfers** over 7 days using:
- **Dune Analytics** (for raw on‑chain data)
- **Python (pandas, matplotlib, seaborn)** (for cleaning, analysis, and visualisation)
- **Power BI / Streamlit** (optional, for dashboarding)

The result is a clear, visual breakdown of:
- Which chain processes the most volume
- Which chain is actually accumulating capital (net flow)
- Which stablecoin dominates DeFi activity

## Key Findings

| Metric | Ethereum | Polygon | Arbitrum |
|--------|----------|---------|----------|
| **Total Volume (7d)** | ~$371B | ~$17B | ~$9B |
| **Net Flow (mint - burn)** | **-$507M** | **+$34.7M** | **-$232M** |
| **USDC Share** | 75.9% | 75.9% | 75.9% |

**The main takeaway**:
- **Ethereum** dominates by volume, but capital is leaving.
- **Polygon** has lower volume, but it was the only chain in this window where stablecoins actually accumulated.
- **Arbitrum** attracted activity, but liquidity didn’t stay.

**USDC** is the preferred stablecoin for DeFi, accounting for ~76% of all tracked volume.


##  Repository Structure
Stable-coin-Liquidity-Rotation/
├── stablecoin_flows.csv # Raw data exported from Dune

├── Stablecoin_Liquidity_Rotation.ipynb # Full analysis notebook

├── README.md # This file

└── requirements.txt # Python dependencies


##  How to Reproduce

1. **Clone the repository**
   ```bash
   git clone https://github.com/AkpanDaniel/Stable-coin-Liquidity-Rotation.git
   cd Stable-coin-Liquidity-Rotation

   pip install -r requirements.txt
   Run the notebook

Open Stablecoin_Liquidity_Rotation.ipynb in Jupyter or VS Code.

Run all cells to reproduce the analysis and visualisations.

##  Visuals
Chart	Description
Volume by Chain	Total stablecoin volume per chain (bar chart).
USDC vs USDT	Breakdown of stablecoin preference by chain (stacked bar).
Daily Heatmap	Volume trends over the 7 days (heatmap).
Volume vs. Net Flow: Bubble chart showing the relationship between activity and capital movement.
<img width="1495" height="602" alt="image" src="https://github.com/user-attachments/assets/0c688089-740f-407f-8f5f-43c2da587565" />
<img width="1015" height="513" alt="image" src="https://github.com/user-attachments/assets/14696b5e-652e-4307-9f85-a14d10513d3b" />


##  Why This Matters
For analysts, founders, and investors:

Volume is a lagging indicator. It shows what already happened.

Net flow is a leading indicator. It shows where capital is heading next.

Stablecoin preference matters. USDC and USDT serve different ecosystems.

This project is a reminder that the right question often matters more than the right answer.

##  Next Steps
I plan to expand this dashboard by:

Extending the time window to 30 days

Adding more chains (Solana, Base, Optimism)

Including DEX volume and bridge data for richer context

Automating the data pipeline with GitHub Actions

##  Contributing
Feedback, suggestions, and ideas for new metrics are welcome. Open an issue or reach out directly.

##   License
MIT License – feel free to use, adapt, and build on this work.

Built by Akpan Daniel
