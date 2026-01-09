# ds_Hemanth_Kumar_K
# Trader Performance vs Bitcoin Market Sentiment
## Project Overview

This project analyzes the relationship between Bitcoin market sentiment (Fear / Greed) and trader performance using historical trade data from the Hyperliquid exchange.

The goal is to uncover behavioral and performance patterns influenced by market sentiment and derive insights that can support data-driven trading strategies.

## Repository Structure
ds_<candidate_name>/
├── notebook_1.ipynb        # Main analysis notebook (Google Colab)
├── csv_files/              # Cleaned & intermediate datasets
│   └── *.csv
├── outputs/                # All plots and charts generated
│   └── *.png / *.jpg
├── ds_report.pdf           # Final summarized insights
└── README.md               # Project documentation

## Datasets Used
1️) Bitcoin Market Sentiment Dataset

Columns

Date

Classification (Fear / Greed)

Provides a daily view of overall Bitcoin market sentiment.

2️) Historical Trader Dataset (Hyperliquid)

Each row represents a single executed trade.

Key columns used:

Account

Coin

Execution Price

Size USD

Side

Direction

Closed PnL

Timestamp IST

System-level identifiers (transaction hash, order ID, trade ID) were excluded from analysis.

## Methodology Summary

Data Cleaning

Parsed timestamps using dayfirst=True to handle DD-MM-YYYY format

Removed invalid or zero-size trades

Filled missing PnL values

Feature Engineering

Aggregated trades at Account–Date level

Created metrics such as:

Daily PnL

Trade count

Average trade size

Win rate

PnL per trade

Sentiment Integration

Encoded sentiment:

Fear → 0

Greed → 1

Merged trader data with sentiment data by date

Exploratory Data Analysis

Compared trader performance and activity across sentiment regimes

All plots saved in the outputs/ directory

## Key Insights

Trader performance varies across Fear and Greed regimes

Higher trading activity does not always translate to higher profitability

Risk-adjusted metrics (PnL per trade) provide more reliable insights than raw PnL

Market sentiment influences both trading behavior and outcomes

Detailed insights are documented in ds_report.pdf.

## How to Run the Project

Open Google Colab

Upload the project folder

Open notebook_1.ipynb

Run cells sequentially (top to bottom)

All outputs will be automatically saved in:

csv_files/

outputs/

## Outputs

 Visualizations: Stored in outputs/

 Final Report: ds_report.pdf

 Cleaned Data: Stored in csv_files/

All plots can be downloaded as a single ZIP file from Colab.

## Tools & Libraries

Python

Pandas

NumPy

Matplotlib

Seaborn

Google Colab

## Author

Hemanth Kumar K
Data Science Internship Candidate

## Notes

All analysis is fully reproducible

No proprietary data or private credentials are included

Designed to emphasize clarity, insight, and real-world data handling
