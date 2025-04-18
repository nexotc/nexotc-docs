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

The smart contract will:
- Deduct the 3% and 2% respectively from each party
- Send the commissions to the corresponding wallets
- Keep this logic private from the counterparty

```mermaid
flowchart TB
  subgraph Buyer
    A[Buyer]
    A --> A1[Wallet A (2%)]
    A --> A2[Wallet B (1%)]
  end

  subgraph Seller
    B[Seller]
    B --> B1[Wallet C (1.5%)]
    B --> B2[Wallet D (0.5%)]
  end

  A & B --> SC[Smart Contract Escrow]
  SC --> A1
  SC --> A2
  SC --> B1
  SC --> B2
