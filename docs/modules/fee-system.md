# Fee & Commission Structure

!!! note "Transparent Fees. Flexible Commissions. Fully Automated Routing."
    NexOTC was designed to streamline high-value trades, including how fees and commissions are handled — from platform fees to introducer payouts, all embedded directly into the smart contract workflow.

<h2>💰 Platform Fee Model</h2>

Our fee system is **tiered by deal size**, offering fair pricing across a wide range of OTC trades:

| Deal Size (USD)         | Platform Fee       |
|-------------------------|--------------------|
| $25K – $500K            | 0.30%              |
| $500K – $5M             | 0.20%              |
| $5M – $50M              | 0.10%              |
| $50M+                   | Custom / VIP       |

- Fees are deducted directly via the escrow smart contract
- Both parties are notified of fee structure prior to execution
- Volume-based discounts available for institutional desks

<h2>🔁 Workflow Integration</h2>

| Step | Logic                                                                  |
|------|------------------------------------------------------------------------|
| Deal Created   | Fee and commission preferences are attached to the proposal |
| Smart Contract | Deducts fees + splits commissions upon execution            |
| Post-Trade     | zk-Proof can include fee/commission trail for compliance    |

<h2>🔐 Privacy by Design</h2>

- Introducer wallets are **not shown to counterparties**
- Percentages are **not visible** to the other side
- Compliance audit shows only total values, with opt-in disclosure


<h2>🧾 Commission Routing Logic</h2>

NexOTC supports **flexible and private commission routing**, ideal for trades involving introducers, brokers, or facilitators on either side.

Each party (buyer and seller) can:

- Define up to **3 introducer wallet addresses**
- Assign a custom percentage per wallet (total must not exceed 5%)
- Have these fees routed **automatically** by the escrow smart contract

!!! example "Example: Buyer & Seller Introducers"

Let’s say a $10M trade is executed with the following configuration:

- **Buyer Side**
    - Wallet A (2%)
    - Wallet B (1%)

- **Seller Side**
    - Wallet C (1.5%)
    - Wallet D (0.5%)

The smart contract automatically handles commission routing by:
- Deducting 3% from the buyer side and 2% from the seller side, based on their introducer settings  
- Distributing the respective fees to the designated introducer wallets  
- Keeping each party’s commission structure fully private from the counterparty  

The diagram below illustrates how NexOTC routes commissions in a trustless and privacy-preserving manner using smart contract automation.

<p align="center">
  <img src="/assets/images/Diagram_CommissionRouting.png" alt="Commission Routing Diagram" style="max-width: 512px; width: 100%; height: auto;"/>
</p>
