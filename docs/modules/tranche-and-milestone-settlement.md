# Tranche & Milestone Settlement

!!! info "End-to-end, Trustless Trade Lifecycle"
    Every OTC transaction on NexOTC follows a customizable workflow with compliance, privacy and escrow protection from negotiation to settlement.

---

<h2>Overview of Workflow Phases</h2>

| Phase                    | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **1. Matchmaking**       | AI Agents identify suitable counterparties based on trade preferences.     |
| **2. Terms Agreement**   | Discount, volume, tranche logic, and commission setup agreed via UI.       |
| **3. KYC/AML Validation**| ZK-powered checks validate identity & jurisdiction, without exposure.     |
| **4. Escrow Deployment** | Smart contract deployed with custom logic (assets, tranches, timers).      |
| **5. Signature Collection** | Both parties co-sign the final transaction and terms.                  |
| **6. Asset Transfer**    | Assets are exchanged via the smart contract and routed to final wallets.   |
| **7. Post-Trade Compliance** | ZK-proof + audit trail is generated for reporting.                  |

---

<h2>OTC Trade Execution Flow</h2>

```mermaid
flowchart TD
  A[Create Trade Offer] --> B[Offer Published]
  B --> C[Counterparty Accepts / Counters]
  C --> D[Terms Finalized & Smart Contract Escrow Deployed]
  D --> E1[Optional #1: Multi-Sig Wallet Setup]
  D --> E2[Optional #1: Proxy Wallet Creation]

  E1 --> F1[Optional #2: Signature Collection]
  E2 --> F2[Optional #2: Asset Deposits to Proxy Wallets]

  F1 --> G[Funds Deposited]
  F2 --> G

  G --> H[zk-Proof Compliance & Signature Check]
  H --> I[Final Asset Settlement]

style E1 stroke-width:2px,stroke-dasharray: 5 5;
style E2 stroke-width:2px,stroke-dasharray: 5 5;
style F1 stroke-width:2px,stroke-dasharray: 5 5;
style F2 stroke-width:2px,stroke-dasharray: 5 5;
```