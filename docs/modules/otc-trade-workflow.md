# OTC Trade Workflow

!!! info "End-to-end, Trustless Trade Lifecycle"
    Every OTC transaction on NexOTC follows a customizable workflow with compliance, privacy and escrow protection from negotiation to settlement.

## Overview of Workflow Phases

| Phase                          | Description                                                                                                                     |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| **1. Matchmaking / Invitation**| AI Agents identify the best counterparty based on trade preferences or use a private invite link.                               |
| **2. Terms Agreement**         | Discount, tranche settings, commission split, and settlement rules are finalized via user interface.                            |
| **3. KYC/AML Validation**      | Zero-knowledge identity checks confirm each party’s compliance, without revealing sensitive info.                               |
| **4. Escrow Deployment**       | A custom smart contract is deployed, locking in the asset types, deal size, tranches and timers.                                |
| **5. Signature Collection**    | Both parties sign to confirm terms. Multi-Sig support is available.                                                             |
| **6. Asset Transfer**          | Assets are exchanged securely via the escrow contract and routed to the right wallets (including proxy wallets if enabled).     |
| **7. Post-Trade Compliance**   | A zk-proof audit trail is generated for regulatory or internal reporting, with selective disclosure as needed.                  |

## OTC Trade Execution Flow

```mermaid
flowchart TD
  A[Create Trade Offer] --> B[Offer Published]
  B --> C[Counterparty Accepts / Counters & Balance Check]
  C --> D[Terms Finalized & Smart Contract Escrow Deployed]
  D --> E1[Optional: Multi-Sig Wallet Setup]
  D --> E2[Optional: Proxy Wallet Setup]

  E1 --> F1[Optional: Signature Collection]
  E2 --> F2[Optional: Asset Funding via Proxy Wallet]

  F1 --> G[Funds Deposited]
  F2 --> G

  G --> H[zk-Proof Compliance & Signature Check]
  H --> I[Final Asset Settlement]

style E1 stroke-width:2px,stroke-dasharray: 5 5;
style E2 stroke-width:2px,stroke-dasharray: 5 5;
style F1 stroke-width:2px,stroke-dasharray: 5 5;
style F2 stroke-width:2px,stroke-dasharray: 5 5;
```