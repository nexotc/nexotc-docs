# Referral & Introducer Setup

!!! note "Earn While You Introduce OTC Deals"
    NexOTC allows brokers, introducers, and referrers to earn commission **without holding user funds** or being exposed to the counterparties.

---

<h2>🧩 How It Works</h2>

Each OTC deal includes a parameterized section where either party (buyer or seller) can:

- Add up to **3 introducer wallet addresses**
- Define a custom **commission percentage** per wallet  
  _(max 5% per introducer, enforced by the contract)_
- Ensure routing is **automatically handled** by the smart contract during trade execution

> 💸 The fee routing is private — each side only sees **their own introducers and terms**.

---

<h2>🧾 Trustless Payment Logic</h2>

All commissions are:
- Routed by the **escrow smart contract**
- Delivered instantly after milestone/trade confirmation
- Enforced on-chain — no delays or manual handling

---

<h2>🔐 Privacy & Separation</h2>

- Referrer wallets never gain access to trade details
- Parties can add referral logic **without disclosing trade size, counterparty, or asset type**
- Helps protect deal flow while still enabling incentives

---

<h2>📚 Introducer Use Cases</h2>

- Broker-dealer firms bringing clients
- Family offices introducing verified counterparties
- DAO members earning by connecting counterparties
- OTC specialists helping off-market trade execution

---

<h2>🛠️ Setup Guide</h2>

To enable this feature:
1. During OTC Deal Setup, click **“Add Introducers”**
2. Add wallet address + % allocation (up to 3 total)
3. Preview commission logic before executing the trade

🧠 Advanced: Introducer wallets can be updated before signature collection closes. After that, fees are locked and final.

---

<h2>✅ Summary</h2>

The NexOTC commission model is:
- Fully automated and smart-contract enforced
- Invisible to the counterparty
- Ideal for trusted brokers, traders, and dealmakers

Want to become a verified Introducer or Referral Partner?  
[Reach out to the team](../links/support.md).