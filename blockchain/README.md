# ⛓️ CardAssist-AI — Blockchain Audit & Verification Layer

> **Solidity Smart Contracts & Immutable On-Chain Audit Logging.**

---

## 📋 Overview
The `blockchain` module guarantees trust, transparency, and immutability for CardAssist-AI. Critical actions executed by AI agents (such as card blocks, credit limit modifications, and fraud decisions) are hashed and recorded on EVM-compatible blockchains.

---

## 📂 Directory Structure

```
blockchain/
├── hardhat.config.js  # Hardhat development, compiler, and network configuration
├── package.json       # Node package dependencies for Hardhat & OpenZeppelin
├── contracts/         # Solidity smart contract source files (.sol)
├── scripts/           # Deployment and administrative maintenance scripts
├── test/              # Hardhat test suite for contract verification
├── abi/               # Exported JSON ABIs for backend & agent integration
└── ignition/          # Hardhat Ignition deployment modules
```

---

## 🛠️ Technology Stack
- **Smart Contract Language:** Solidity (`^0.8.20`)
- **Development Toolchain:** Hardhat
- **Libraries:** OpenZeppelin Contracts
- **Test Framework:** Hardhat Waffle / Chai / Viem / Ethers.js

---

## 🚀 Getting Started

### Installation
```bash
cd blockchain
npm install
```

### Compile Contracts
```bash
npx hardhat compile
```

### Run Smart Contract Unit Tests
```bash
npx hardhat test
```

### Deploy to Local Node / Network
```bash
npx hardhat node
npx hardhat run scripts/deploy.js --network localhost
```
