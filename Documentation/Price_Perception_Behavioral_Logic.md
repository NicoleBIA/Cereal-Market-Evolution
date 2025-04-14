# Understanding Price Perception Difference (PPD) in Visuals Using Perceived vs Actual Price

**Definition:**  
Price Perception Difference (PPD) measures the average difference between what consumers believe a product *should* cost per ounce (Perceived $/oz) versus what it *actually* costs (Actual $/oz).

---

## Why It Matters

This is not just a simple numerical delta — it’s a **behavioral insight metric**. PPD reflects how aligned or misaligned consumers are in their value interpretation of a product’s price at the unit level.

- A **positive PPD** means the consumer *thought it would cost more* than it did — a potential trust or brand premium signal.
- A **negative PPD** means the consumer *thought it would cost less* — signaling possible sticker shock, dissatisfaction, or elasticity risk.

---

### How It’s Calculated

PPD is an **average of individual perception gaps** across all relevant purchase rows for a selected filter context (e.g., by Brand, Retailer, Promotion, or Timeframe).

Example:

| Consumer | Size (oz) | Perceived $/oz | Actual $/oz | PPD |
|----------|------------|----------------|-------------|-----|
| Amy      | 12.8       | 0.52           | 0.44        | 0.08 |
| James    | 11.9       | 0.47           | 0.45        | 0.02 |
| Michelle | 9.0        | 0.40           | 0.43        | -0.03 |
| Stacey   | 22.0       | 0.49           | 0.52        | -0.03 |
| Jose     | 14.5       | 0.41           | 0.45        | 0.04 |

Final **PPD for Group**:  
(0.08 + 0.02 + -0.03 + -0.03 + 0.04) / 5 = **0.016**

---

### Why Analysts Use It

PPD is especially useful when comparing **brand-level** or **promotion-level** pricing trends because it:

- Normalizes pricing behavior across varying package sizes
- Highlights consumer price expectation trends
- Indicates promotional strategy effectiveness
- Supports behavioral pricing analysis in regression or scatter plot visuals

---

### Analyst Tip

If you see a large **negative PPD**, ask:
- Did perceived value drop due to a weak brand?
- Was the promotion not clearly communicated?
- Did price changes outpace consumer expectation?

If you see a high **positive PPD**, ask:
- Is there brand trust or nostalgia bias at play?
- Are consumers mentally anchoring to old inflation levels?
- Is there hidden elasticity to leverage?

---
