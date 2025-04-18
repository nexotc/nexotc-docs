# Trustless OTC Escrow

!!! note "What is Trustless Escrow?"
    NexOTC’s escrow module ensures that both parties fulfill their obligations in a secure, smart contract-enforced environment — without any intermediaries or custodial risk.

<h2>💡 Why It Matters</h2>

Traditional OTC trades often rely on intermediaries (brokers, agents, or custodians) to hold funds and coordinate transfers. This introduces risk, delays, and high fees.

With NexOTC:

- Trades are executed **directly between parties**
- Funds are held and released via **smart contracts**
- **Zero counterparty risk** from the platform
- Everything is enforceable on-chain, automatically

<h2>⚙️ Core Features</h2>

!!! info "Smart Contract Logic"
    Trades are initiated and locked via smart contracts. Both parties must fulfill their end of the deal (signatures, deposits) before the escrow executes.

!!! info "Tranche-Based Execution"
    For large deals, escrow supports **phased execution** in tranches. Each tranche is released based on pre-defined conditions (signatures, milestones, time).

!!! info "Time-Based Settlement"
    Deadlines are built into every trade. If one party fails to act, funds are refunded or settled according to predefined fallback logic.

!!! info "Multi-Asset Support"
    Supports various asset types including:
    - Crypto (ETH, USDT, BTC via wrapped tokens)
    - ERC-20 tokens
    - Tokenized assets (future phase)

!!! info "Fee Routing Integration"
    Fees (platform, referral, introducers) are automatically routed from the escrow flow to designated wallets.

<h2>🔐 How Trust Is Removed</h2>

- ✅ **No custody** — NexOTC never holds assets.
- ✅ **Auditable** — Smart contracts are open and verifiable.
- ✅ **Immutable rules** — Once a trade is created, rules cannot be changed without both parties’ agreement.

<h2>📦 Example Workflow</h2>

1. Buyer and Seller agree on terms (off-chain or via AI Matchmaking)
2. A smart contract is deployed with:
   - Amount
   - Asset type
   - Deadline
   - Conditions
3. Both parties sign
4. Assets are deposited into the contract
5. On trigger conditions, the contract auto-settles
