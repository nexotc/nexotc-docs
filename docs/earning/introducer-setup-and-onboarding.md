# Introducer Setup & Onboarding

!!! note "Earn Commissions on OTC Deals"
    Introducers are wallets added to a specific OTC trade by a counterparty. Their commission is automatically routed when the trade is executed.

## What is an Introducer?

An introducer is someone who:

- Connects buyers and sellers off-chain;
- Represents a counterparty in the deal;
- Is eligible to receive a % of the trade.

> ⚠️ Introducers are attached **per trade**, not at the platform level.

## How to Add Introducers

During the OTC deal setup process:

1. Navigate to the **Deal Parameters** section;
2. Choose "Add Introducers" under the commission settings;
3. Input up to 3 wallet addresses per counterparty;
4. Assign a commission % for each wallet (max 5% per counterparty);
5. Review and confirm introducer wallets and commission splits before the deal is signed.

> ⚠️ Introducer wallets are screened for compliance to prevent payouts from being sent to restricted or sanctioned addresses.

💡 _View the full commission routing logic in the [Commission Routing Logic Diagram](../modules/fees-and-commission-structure.md#commission-routing-logic)_.

## Privacy Benefits

- [x] Introducer wallets never gain access to trade details;
- [x] Counterparties can add commission logic without disclosing trade size, counterparty or asset type;
- [x] Helps protect deal flow while still enabling incentives.
