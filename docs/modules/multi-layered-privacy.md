# Multi-Layered Privacy

!!! note "Customizable Privacy, Built for Trust"
    Privacy isn’t one-size-fits-all. NexOTC gives every user full control over what they share and when, without compromising on compliance or security.

## What is Multi-Layered Privacy?

At NexOTC, privacy isn’t just “on” or “off.” It’s a flexible system with multiple layers that adjust to your needs whether you're an individual, a fund or an institution.

| Level     | Features                                                                 | Ideal For                           |
|-----------|--------------------------------------------------------------------------|-------------------------------------|
| **Low**   | zk-KYC, AML Check                                                        | Standard KYC Users                  |
| **Medium**| Selective Disclosure (Share Only What's Needed)                          | Professionals, Brokers              |
| **High**  | Proxy Routing, Multi-Sig Wallets                                         | Funds, DAOs, Family Offices         |

## Key Privacy Tools

=== "zk-KYC & AML Verification"

    Your identity and compliance status are verified using zero-knowledge proofs which means you can prove you're verified **without revealing personal details**.
    ```mermaid
    flowchart TD
      A[Wallet Connect] --> B[Submit KYC/KYB Info]
      B --> C[zk-SNARK Proof Generated]
      C --> D{AML Check Required?}
      D -- Yes --> E{Compliant or Flagged?}
      E -- Compliant --> F[✅ DID Issued]
      E -- Flagged --> G[🚫 Manual Review]
      D -- No --> F
      F --> H[🔗 KYC/AML Proof Linked to OTC User Profile]

    style D stroke-width:2px,stroke-dasharray: 5 5;
    style E stroke-width:2px,stroke-dasharray: 5 5;
    ```

=== "Multi-Sig Wallets"

    Multi-signature wallets require approvals from multiple parties before a trade goes through. Perfect for teams, DAOs or anyone who needs shared control over funds.
    ```mermaid
    flowchart TD
      A[Define Signers & Threshold] --> B[Deploy Multi-Sig Wallet]
      B --> C[Link Multi-Sig Wallet to OTC Profile]
      C --> D[Sign OTC Trade Proposal]
      D --> E{Threshold Met?}
      E -- Yes --> F[✅ Trade Authorized]
      E -- No --> G[🔒 Waiting for More Signers]

    style E stroke-width:2px,stroke-dasharray: 5 5;
    ```

=== "Proxy Wallet for Private Routing"

    Trades can be routed through temporary one-time wallets. This protects your main wallet address from being tracked, especially useful in sensitive deals.
    ```mermaid
    flowchart TD
      A[Generate Proxy Wallet] --> B[Link Proxy Wallet to Main Profile]
      B --> C[Fund Proxy Wallet]
      C --> D{Ready to Trade?}
      D -- Yes --> E[🔀 Assets Routed via Proxy Wallet]
      E --> F[✅ OTC Trade Executed]
      D -- No --> G[⏳ Wait or Cancel Setup]

    style D stroke-width:2px,stroke-dasharray: 5 5;
    ```
