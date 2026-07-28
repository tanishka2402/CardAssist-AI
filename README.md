# ⛓️ CardAssist-AI — Blockchain Development Branch (`blockchain`)

> **Domain Branch for EVM Smart Contracts, Hardhat Deployment Scripts, Contract ABIs, and On-Chain Audit Verification.**

---

## 📌 Branch Focus: Blockchain Subsystem

This branch (`blockchain`) is dedicated to building, compiling, testing, and deploying Solidity smart contracts for CardAssist-AI. Developers working on this branch focus on audit logging contracts (`AuditLogger.sol`), Hardhat testing, verification registries, and client ABI generation.

---

## 📂 Blockchain Subsystem Map (`blockchain/`)

```
blockchain/
├── hardhat.config.js  # Hardhat development environment & compiler configuration
├── package.json       # Node package dependencies for Hardhat & OpenZeppelin
├── contracts/         # Solidity smart contract source files (.sol)
├── scripts/           # Deployment and administrative management scripts
├── test/              # Hardhat test suite for smart contract verification
├── abi/               # Exported JSON ABIs for backend & agent integration
└── ignition/          # Hardhat Ignition deployment modules
```

---

## 🚀 Quick Start for Blockchain Developers

1. **Navigate to the blockchain directory:**
   ```bash
   cd blockchain
   ```
2. **Install Hardhat & contract dependencies:**
   ```bash
   npm install
   ```
3. **Compile Solidity smart contracts:**
   ```bash
   npx hardhat compile
   ```
4. **Run Smart Contract Unit Tests:**
   ```bash
   npx hardhat test
   ```

5. **Detailed Blockchain Architecture Documentation:**
   See [blockchain/README.md](file:///c:/Users/svija/Downloads/CardAssist-AI/blockchain/README.md) for full contract and deployment details.

---

## 🌿 Git Workflow Rules for `blockchain`
- Always pull the latest changes from `develop` before editing smart contracts:
  ```bash
  git pull origin develop
  ```
- Push contract updates to `blockchain` and open a Pull Request to merge into `develop`.
