# EduPrime TokenEDuPrime Backend

[![Node.js](https://img.shields.io/badge/Node.js-18.x-green)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-4.x-blue)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6.x-green)](https://www.mongodb.com/)
[![Hardhat](https://img.shields.io/badge/Hardhat-2.x-purple)](https://hardhat.org/)
[![Solidity](https://img.shields.io/badge/Solidity-^0.8.0-orange)](https://docs.soliditylang.org/)

EduPrime **TokenEDuPrime** is a Node.js/Express backend for a blockchain-powered e-learning platform.  
It integrates an **ERC‑20 token (EduToken)** via Hardhat/Ethers, manages users, courses, quizzes with MongoDB/Mongoose, and supports payments, authentication, and file uploads.

---

## 🔹 Highlights

- **Smart Contract Integration**  
  - ERC‑20 token: `contracts/EduToken.sol`  
  - Deploy via `scripts/deploy.js` and interact through `models/cont.js`.

- **REST API**  
  - Modular routes/controllers for auth, users, courses, domains, carts, quizzes in `routes/` & `controllers/`.

- **MongoDB Data Layer**  
  - Schemas in `models/`.

- **Authentication & Security**  
  - JWT auth, bcryptjs password hashing, route protection middleware in `middleware/`.

- **Payments & Notifications**  
  - Stripe payment flows (carts), optional Firebase Admin integration in AuthController.

- **File Uploads**  
  - Multer-based, served from `uploads/`.

- **Developer Tooling**  
  - Hardhat toolbox, environment-driven configuration (`.env`).

---

## 💻 Tech Stack

- **Backend:** Node.js, Express, Mongoose, JWT  
- **Blockchain:** Solidity, Hardhat, Ethers.js  
- **Payments/Services:** Stripe, Firebase Admin (optional)  
- **Utilities:** Multer, Morgan, Cors, Nodemailer  

---

## ⚡ Quick Start

```bash
# Install dependencies
npm install

# Compile smart contracts
npx hardhat compile

# Deploy contract (set PROVIDER_URL and PRIVATE_KEY first)
npx hardhat run scripts/deploy.js --network EDUPRIME

# Set CONTRACT_ADDRESS in .env after deployment

# Start the server
node server.js
