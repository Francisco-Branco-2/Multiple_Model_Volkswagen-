*Disclaimer: This model is for educational purposes only and uses hypothetical data.*
---
# Relative Valuation Model (Trading Multiples)

## 📊 Project Overview
This repository contains a **Comparable Company Analysis ("Comps")** model built in Microsoft Excel.

The objective of this model is to derive an implied valuation range for a target company (**Company A**) by analyzing the trading metrics of a specific peer group (**Companies B, C, D, and E**). It calculates key valuation multiples based on 2020 Actuals, and 2021/2022 Estimates.

## 📂 File Structure
The model is split into three primary logical sections:

* **General (Market Data & EV Bridge):**
    * Contains the "Market inputs": Share Prices, Shares Outstanding, and Tax Rate (30%).
    * Calculates **Equity Value** (Market Cap) and **Enterprise Value (EV)**.
    * **EV Bridge:** Bridges Equity Value to Enterprise Value by adding Net Debt, Minority Interest, and Preferred Equity, while subtracting Cash and Associates.
* **Financials (P&L Data):**
    * Raw financial data for the Target and Peers.
    * Metrics tracked: **Revenue, EBITDA, EBIT, and Net Income**.
    * Time horizons: 2020 (Actual), 2021 (Forecast), and 2022 (Forecast).
* **Adjustments (Normalization):**
    * Handles "Non-recurring items" to normalize earnings for a fair comparison.
    * Includes add-backs for: Restructuring costs, Litigation fees, Asset write-downs, and M&A expenses.

## ⚙️ Methodology & Logic

### 1. Enterprise Value Calculation
The model calculates the Enterprise Value for every peer using the standard formula:
$$\text{Enterprise Value} = \text{Market Cap} + \text{Debt} + \text{Minority Interest} + \text{Preferred Equity} - \text{Cash} - \text{Associates}$$

### 2. Normalization of Earnings
To ensure we are comparing "apples to apples," the model calculates **Adjusted EBITDA** and **Adjusted Net Income**.
* *Logic:* Reported Financials + One-off Expenses (from `Adjustments` tab) = Adjusted Financials.
* This prevents one-time events (like a lawsuit or factory closure) from distorting the valuation multiples.

### 3. Multiples Calculation
The model computes the following trading multiples for the Peer Group:
* **EV / Revenue** (2020A, 2021E, 2022E)
* **EV / EBITDA** (2020A, 2021E, 2022E)
* **EV / EBIT** (2020A, 2021E, 2022E)
* **P/E Ratio** (Price to Earnings)

### 4. Implied Valuation
Finally, the model applies the **Mean** and **Median** multiples of the Peer Group to Company A's financials to derive its implied share price and Enterprise Value.

## 🚀 How to Use
1.  **Update Market Data:** Update share prices in the `General` tab to reflect current market conditions.
2.  **Review Adjustments:** Check the `Adjustments` tab to ensure all non-recurring items are captured correctly (positive values add back to earnings).
3.  **Select Multiple:** Choose the most relevant multiple (e.g., EV/EBITDA for capital-intensive industries vs. P/E for mature banks) to view the implied valuation range.

## 🛠 Skills Applied
* Relative Valuation / Comparable Analysis.
* Financial Statement Normalization.
* Enterprise Value Bridge Construction.
* Market Data Analysis.

---
*Disclaimer: This model is for educational purposes only and uses hypothetical data.*
