Here's the **coreEscrow** README in the same style as the **GameItems** README:

---

# 🤝 **coreEscrow** Smart Contract

A simple smart contract to facilitate secure transactions between a buyer, seller, and an arbiter. The contract holds funds until both parties are satisfied with the transaction. Built using Solidity and Hardhat, deployable on Core Blockchain networks.

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Your-repository.git
cd escrow-core-sage
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the project root:

```env
PRIVATEKEY="YOUR_PRIVATE_KEY"
CORE_TEST2_SCAN_KEY="YOUR_CORE_TEST2_SCAN_KEY"
CORE_TEST1_SCAN_KEY="YOUR_CORE_TEST1_SCAN_KEY"
CORE_MAIN_SCAN_KEY="YOUR_CORE_MAIN_SCAN_KEY"
```

> ⚠️ **Important:** Never share your private key or commit the `.env` file to version control.

---

## 🛠 Hardhat Commands

### Compile Contracts

```bash
npx hardhat compile
```

### Run Tests

```bash
npx hardhat test
```

### Deploy Contract

Use a deployment script:

```bash
npx hardhat run scripts/deploy.js --network core_testnet2
```

---

## 🔍 Contract Verification

You can verify contracts using Core block explorers:

```bash
npx hardhat verify --network core_testnet2 <deployed_contract_address> <constructor_args_if_any>
```

API keys for verification must be included in `.env` as shown above.

---

### Contract Highlights

- **coreEscrow Logic:** Secure transaction between a buyer, seller, and an arbiter.
- **Key Functions:**
  - `fund()`: Allows the buyer to fund the escrow with ETH.
  - `releaseFunds()`: Allows the buyer or arbiter to release funds to the seller.
  - `refundBuyer()`: Allows the seller or arbiter to refund the buyer if needed.

---

