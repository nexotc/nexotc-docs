# Trustless OTC Escrow

!!! note "What is a Trustless Escrow?"
    In traditional deals, a middleman usually holds the money or assets until both sides complete the agreement but that means you have to trust the middleman. 

    NexOTC removes the need for any third party. Instead, a smart contract (a piece of code on the blockchain) holds the assets and only releases them when both sides meet the agreed terms.

## Why It Matters

Traditional OTC trades often rely on intermediaries (brokers, agents or custodians) to hold funds and coordinate transfers. This creates risk, adds delays and inflates fees.

With NexOTC's Escrow:

- Trades are executed **directly between counterparties**;
- Funds are locked and released via **smart contracts**;
- **Zero counterparty risk** from the platform;
- Fully **on-chain** and **autonomous**.

## Core Features

| Feature                       | Description                                                                                                                                 |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. Smart Contract Logic       | The entire trade is handled by a smart contract. Both sides must agree, sign and deposit their assets before the deal goes through.         |
| 2. Tranche-Based Execution    | Large deals can be split into smaller parts, called tranches. Each tranche is released only after certain conditions are met.               |
| 3. Time-Based Settlement      | Deadlines are built into every trade. If one party fails to act, funds are refunded or settled according to predefined fallback logic.      |
| 4. Multi-Asset Support        | Supports various asset types including ETH, USDT or wrapped BTC, ERC-20 tokens and future support for tokenized real-word assets.           |
| 5. Fee Routing Integration    | Automatically sends fees to the right counterparties, introducers and referral partners.                                                    |
| 6. Slippage Protection        | Escrow can be configured to cancel or pause execution if the market price moves beyond an agreed threshold.                                 |

## How Trust Is Removed

- ✅ **No Custody**: NexOTC never holds assets;
- ✅ **Auditable**: Smart contracts are open and verifiable;
- ✅ **Immutable Rules**: Once a trade is created, rules cannot be changed without both parties’ agreement;
- ✅ **Failsafe Logic**: Predefined fallbacks ensure no funds are stuck
