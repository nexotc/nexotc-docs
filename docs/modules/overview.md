# Overview

!!! note "What are Overview Modules?"
    Modules are the core components of NexOTC. Each one manages a specific part of the OTC process, from trade setup and execution to privacy, compliance and settlement.

## How It Works

NexOTC is built on a modular architecture that allows the platform to remain:

- **Flexible**: Easily adapt workflows and settings based on user type, whether individual or institutional;
- **Compliant**: Every module respects regulatory requirements and privacy standards by default;
- **Secure**: Smart contracts and privacy layers work together to isolate risk and enforce trade execution automatically.

## Architecture

<center>
  <img src="/assets/images/overview.png" alt="NexOTC Overview" width="800"/>
</center>

💡 Each module handles a function and can operate independently or as part of a complete trade flow.

## Primary Modules in NexOTC

| Module                            | Description                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| 1. Trustless OTC Escrow           | Smart contracts enforce OTC trades securely with support for time-based actions, asset swaps and flexible settlement options.  |
| 2. AI Matchmaking Agents          | Smart agents that connect counterparties based on trade preferences, behavior patterns and verified compliance.                |
| 3. Fee & Commission Structure     | Automatically routes fees to the platform, introducers and partners with full support for commission structure.                |
| 4. Multi-Layered Privacy          | Trade privately with zk-SNARK KYC / KYB, selective disclosure, proxy wallets and multi-sig support.                            |
| 5. Tranche & Milestone Settlement | Break large trades into secure tranches and optionally link them to milestones for added control and flexibility.              |
| 6. Asset & Token Support          | Supports major cryptocurrencies, ERC-20 tokens and future support for tokenized assets or commodities.                         |
| 7. OTC Trade Workflow             | A structured, modular flow covering the full OTC lifecycle, from trade setup to execution and post-trade compliance.           |
