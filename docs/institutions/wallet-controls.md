# Multi-Sig & Proxy Wallets

!!! note "Institutional-Grade Asset Control"
    NexOTC supports **advanced wallet structures** designed for teams, funds, and institutions that require shared control, internal segregation, or added privacy in their OTC operations.

---

<h2>🔐 Multi-Signature Wallet Support</h2>

Multi-sig wallets ensure that **multiple signers must approve actions**—ideal for institutional governance or internal controls.

### Key Benefits
- **Team-Based Approvals** — Require 2-of-3, 3-of-5, or custom signature thresholds
- **Minimize Risk** — Prevent unauthorized access or transfers
- **Internal Policy Compliance** — Match internal treasury or fund control policies

### Use Cases
- DAO multisigs for treasury operations
- Fund managers requiring joint sign-off
- Legal/compliance dual-approval mechanisms

> ✅ NexOTC integrates with [Safe (formerly Gnosis Safe)](https://safe.global/) for secure, permissioned multi-sig functionality.

---

<h2>🕵️ Proxy Wallets (Optional)</h2>

Proxy wallets add a **layer of obfuscation** to increase privacy without breaking compliance.

### How It Works
- A one-time-use wallet is generated for the OTC deal
- The proxy receives/holds assets during escrow
- All routing is handled by smart contract logic
- Final destination wallet is known only to the system and party

### Benefits
- **Protect identity** from counterparties
- **Prevent wallet tracking** or reverse lookup
- **Support multiple OTC routes** per main wallet

> ⚠️ Proxy wallets are optional and fully compliant. They preserve privacy while enabling full ZK-KYC/AML checks and audit trails.

---

<h2>🧩 Use Both Together</h2>

Institutions can combine **multi-sig approval** with **proxy routing** to achieve the highest level of control and confidentiality in high-value OTC flows.