# MENA-Scraper
# MENA Equity Data Scraper & Volatility Pipeline

## Overview
An automated Python-based data pipeline designed to systematically scrape, clean, and format historical price data for emerging market equities in the Middle East and North Africa (MENA) region. 

This tool is built to handle the inherent noise and missing data points common in emerging market exchanges, structuring the output into clean, econometric-ready CSV matrices.

## Core Features
* **Automated Data Extraction:** Integrates with the `yfinance` API to pull high-fidelity daily closing prices.
* **Data Cleansing (NaN Handling):** Systematically identifies and drops missing values or halted trading days to maintain matrix integrity.
* **Statistical Volatility Engine:** Calculates localized risk metrics, including 20-day rolling moving averages and annualized 20-day rolling standard deviation (volatility).
* **Target Assets:** Currently configured for the Egyptian Exchange (EGX), targeting heavyweight equities like Commercial International Bank (`COMI.CA`) and the VanEck Egypt Index ETF (`EGPT`).

## Tech Stack
* **Language:** Python 3
* **Libraries:** `pandas`, `numpy`, `yfinance`

## Usage
Run the pipeline directly from the terminal. The script will output cleaned, statistically formatted CSV datasets to the local directory.
```bash
python mena_scraper.py
