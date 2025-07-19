
---

### `analysis.md`

```markdown
# Wallet Credit Score Analysis


### Binned Score Ranges:

| Score Range | Wallet Count |
|-------------|--------------|
| 0–100       | High         |
| 100–200     | Very High    |
| 200–300     | Moderate     |
| 900–1000    | Very Few     |

## Observations

### Low-Scoring Wallets (0–200)

- Low or no repayment activity
- Frequently involved in liquidation events
- Minimal total deposits
- Negative or low net contribution
- Low active duration

### High-Scoring Wallets (700–1000)

- High repayment ratios
- Zero or very low liquidation rates
- Consistent deposits
- Positive net contribution
- Long active durations across the dataset

## Insights

- The majority of wallets cluster in the low score bins, suggesting either one-off or poor-quality interactions with Aave V2
- Very few wallets demonstrate good borrowing discipline and consistent activity, and they are rewarded with high scores
- Repayment behavior and avoidance of liquidation are strong signals of wallet reliability
