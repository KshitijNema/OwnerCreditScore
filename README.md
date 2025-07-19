# Wallet Credit Scoring on Aave V2

This project assigns a credit score (0–1000) to wallets interacting with the Aave V2 protocol using transaction-level DeFi data.

## Method Overview

Wallets are evaluated based on:

- Repayment Ratio: Amount repaid versus borrowed
- Liquidation Rate: Fraction of transactions that are liquidations
- Total Deposits (USD): Total value deposited
- Net Contribution: Deposit + Repay - Borrow - Redeem
- Activity Duration: Number of days between first and last transaction

## Scoring Formula

```python
score_raw = (
    400 * repay_ratio +
    200 * (1 - liq_rate) +
    0.5 * log1p(total_deposit_usd) +
    0.3 * log1p(net_contribution) +
    0.2 * log1p(activity_days)
)
