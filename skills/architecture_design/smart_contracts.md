# Blockchain & Smart Contract Engineering | هندسة البلوكشين والعقود الذكية

## Arabic Description | وصف بالعربية
قواعد صارمة لتطوير العقود الذكية وتطبيقات الويب 3 (Web3) تضمن الأمان المطلق، الكفاءة في استهلاك الغاز (Gas)، واللامركزية.

---

## Strict Rules | قواعد صارمة

### 1. Smart Contract Security
- **Auditing**: Every contract MUST be audited by a third party before deployment to mainnet.
- **Reentrancy Protection**: Use `ReentrancyGuard` or the checks-effects-interactions pattern for all external calls.
- **Integer Overflow**: Use Solidity 0.8.x or `SafeMath` to prevent arithmetic overflows/underflows.

### 2. Gas Optimization
- **Efficient Storage**: Minimize on-chain storage. Use `external` functions where appropriate.
- **Batching**: Use batching for multiple operations to save gas for users.

### 3. Decentralization & Trust
- **No Backdoors**: Avoid administrative functions that can rug-pull or freeze user funds without community consensus.
- **Transparency**: All contract code MUST be verified on block explorers (e.g., Etherscan).

### 4. Web3 Integration
- **Wallet Connection**: Handle wallet disconnections and network changes gracefully in the frontend.
- **Provider Management**: Use robust providers (Infura, Alchemy) with fallback mechanisms.

### 5. Testing & Simulation
- **Fork Testing**: Test contracts against a local fork of the mainnet to simulate real conditions.
- **Fuzzing**: Use tools like `Echidna` or `Foundry` for property-based testing and fuzzing.
