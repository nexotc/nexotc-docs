# Overview

!!! note "What are Overview Modules?"
    Modules are the core building blocks of NexOTC. Each one handles a specific aspect of the OTC lifecycle, from trade initiation to compliance and final settlement.

## How It Works

At the heart of NexOTC lies a modular architecture. This allows the platform to remain:

- **Flexible** — plug-and-play different workflows or settings depending on the user profile (e.g. retail vs institutional);
- **Compliant** — every module is aware of privacy and legal contexts;
- **Secure** — smart contracts and privacy layers isolate risk and enforce trade rules automatically.

## Architecture

<center>
  <img src="/assets/images/overview.png" alt="NexOTC Overview" width="800"/>
</center>

💡 Each module is designed to perform a specialized task and can work independently or as part of a larger flow.

## Primary Modules in NexOTC

| Module                            | Description                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| 1. Trustless OTC Escrow           | Smart contracts enforce OTC trades securely with support for time-based actions, asset swaps and flexible settlement options.  |
| 2. AI Matchmaking Agents          | Smart agents that connect traders based on preferences, patterns and verified compliance.                                      |
| 3. Fee & Commission Structure     | Routes fees to the platform, introducers and partners, with full support for tiered trade sizes and commission logic.          |
| 4. Multi-Layered Privacy          | Trade privately with zk-SNARK KYC / KYB, selective disclosure, proxy wallets and multi-sig support.                            |
| 5. Tranche & Milestone Settlement | Settle large trades in secure tranches and optionally link them to milestones for added control and flexibility.               |
| 6. Asset & Token Support          | Supports major cryptocurrencies, ERC-20s and future tokenized assets or commodities.                                           |
| 7. OTC Trade Workflow             | A structured journey from trade creation to settlement, optimized for high-value P2P deals.                                    |
