# Post-Trade Compliance & Reporting

!!! info "Proof of Compliance Without Exposing Sensitive Data"
    After each OTC trade, NexOTC automatically generates compliance records using zero-knowledge proofs and selective disclosure so institutions can meet audit, regulatory or internal reporting needs while maintaining privacy.

## Zero-Knowledge Compliance Logs

Every trade includes a cryptographic ZK-SNARK proof confirming that:

- [x] KYC/KYB + AML were performed[^1]
- [x] Assets matched approved lists
- [x] Terms and conditions were digitally signed
- [x] All commissions were routed properly

> 🔐 These logs prove **compliance** without disclosing counterparties, asset size or wallet addresses.

## PDF Audit Reports (PDF, JSON)

Both Individuals and Institutions can request:

- Trade confirmations;
- Compliance summaries;
- Audit trails for internal, banking or legal use.

> ⚠️ These are generated only on request through the Dashboard.

## Verification Tools

Each trade can be independently verified using:

- On-chain smart contract verifier[^2]
- Institutional dashboard audit view  
- Internal hash ledger with secure timestamping[^3]

## Commission & Escrow Transparency

Post-trade logs include:

- Tranche/milestone execution timestamps
- Commission routing by wallet
- Role-based tagging for each participant in the trade (buyer, seller, introducer, platform)

[^1]: Proof that both parties were previously verified (KYC/KYB + AML) during onboarding and that verified identities were linked to the trade without revealing who they are.

[^2]: Anyone can verify the trade conditions were met on-chain (e.g. signatures collected, assets deposited, tranches settled) without revealing identities or amounts.

[^3]: NexOTC maintains a hash-logged internal record of all trades with timestamps. This serves as an auditable proof trail without exposing full details.