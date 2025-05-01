# 📈 Pairs Trading Strategy – Statistical Arbitrage

Quantitative Researcher | [Mustafa MAJJI](https://www.linkedin.com/in/mustafa-majji-3a59861a2/)

***

This project explores the implementation of a pairs trading strategy, a form of statistical arbitrage that aims to profit from relative mispricings between two historically correlated assets. While not truly zero-risk, the strategy is considered market-neutral and seeks to minimize directional exposure by taking offsetting positions in paired assets.

## 🔍 Strategy Overview
The core idea behind pairs trading is that if two assets are cointegrated—i.e., they have a stable long-term relationship—then temporary divergences in their prices can be exploited. When such a divergence occurs, the strategy assumes that prices will revert to their historical equilibrium. Therefore:

- You **short** the asset that has become overvalued.
- You **go long** on the asset that has become undervalued.
    
## 🧪 Project Workflow

**Step1: Data Acquisition**
- Import the list of all companies listed on the NASDAQ.

**Step2: Market Cap Classification**
- Group companies into:
     - **Large-cap**: Market cap > $10 billion.
     - **Mid-cap**: $2 billion < Market cap ≤ $10 billion.

**Step3: Liquidity Filter**
- Select the top 100 companies by average trading volume to ensure sufficient liquidity.

**Step4: Price Normalization**

- Normalize historical price series for comparability across assets.

**Step5: Distance Calculation**

- Compute Euclidean distances between normalized price series to find closely moving pairs within the same group (Large-cap or Mid-cap).

**Step6: Pair Selection**

- Select pairs with the smallest distances, indicating strong co-movement.

**Step7: Sector Consistency Filter**

- Retain only pairs from the same sector to increase the likelihood that both are influenced by similar macroeconomic or industry-specific factors.

**Step8: Cointegration Testing**

- Apply the **Johansen cointegration** test to validate long-term statistical relationships. Discard non-cointegrated pairs.

**Step9: Trading Signal Generation**

- Define entry and exit thresholds on the spread between the paired assets.

- Go long/short depending on whether the spread exceeds a set upper or lower limit.

 

## :mailbox_closed: Contact
For any information, feedback or questions, please [contact me][Mustafa-email]




[Mustafa-email]: mailto:majji1999@gmail.com
