# Multi-Layered Privacy

!!! note "Customizable Privacy"
    NexOTC offers dynamic privacy options across every phase of the OTC trade. From wallet routing to disclosure settings, users maintain full control over what is shared and with whom.

<h2>What is Multi-Layered Privacy?</h2>

At NexOTC, privacy isn’t a toggle — it’s a stack. We offer **graduated privacy levels** to match both the **user’s preferences** and **regulatory needs**:

| Level     | Features                                                                 | Ideal For                           |
|-----------|--------------------------------------------------------------------------|-------------------------------------|
| **Low**   | zk-KYC, AML Check                                                        | Standard KYC users                  |
| **Medium**| Selective Disclosure                                                     | Professionals, brokers              |
| **High**  | Proxy Routing, Multi-Sig                                                 | Funds, DAOs, Family Offices         |

<h2>Key Privacy Components</h2>

=== "zk-KYC & AML Verification"

    Your identity and compliance status are securely verified without exposing any sensitive personal or institutional data.
    ```mermaid
    flowchart TD
      A[Wallet Connect] --> B[Submit KYC/KYB Info]
      B --> C[zk-SNARK Proof Generated]
      C --> D{AML Check Required?}
      D -- Yes --> E{Compliant or Flagged?}
      E -- Compliant --> F[✅ DID Issued]
      E -- Flagged --> G[🚫 Manual Review / Trade Blocked]
      D -- No --> F
      F --> H[🔗 KYC/AML Proof Linked to OTC Profile]

    style D stroke-width:2px,stroke-dasharray: 5 5;
    style E stroke-width:2px,stroke-dasharray: 5 5;
    ```

=== "Multi-Sig Wallet Setup"

    Multi-signature wallets provide shared control and added protection, making them a reliable choice for individuals, teams and institutions.
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

=== "Proxy Wallet Setup & Routing"

    Trades are routed through one-time-use wallets to prevent address tracking, especially useful for counterparties requiring confidentiality.
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

<h2>Compliance First</h2>

All privacy settings are **auditable** using zk-Proofs and built with regulators in mind. Users must still complete mandatory KYC/KYB — but can decide **what's visible to counterparties**.