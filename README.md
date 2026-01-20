# App_blockchain

Web application that combines a traditional frontend UI with Web3 authentication and social actions on the Solana blockchain.
The project demonstrates how wallet-based login, JWT authentication, and on-chain user relationships can work together in a modern dApp.

**Features:**

Frontend
- LinkedIn-style UI built with HTML, CSS, Bootstrap
- Responsive layout (navbar, feed, profile sidebar, posts)
- Font Awesome & SVG icons
- Static demo feed and profile components

Web3 Authentication
- Login using Phantom Wallet
- Message signing with a nonce
- Secure verification using tweetnacl
- JWT-based session handling

Backend (Node.js + Express)
- Nonce generation endpoint
- Signature verification
- JWT token issuance & validation
- REST API endpoints for:
- User registration
- Following users
- Static file hosting

Smart Contract (Solana Program – Rust)
- On-chain user accounts
- Add user instruction
- Follow user instruction
- Persistent user state using Borsh serialization
- Followers & followings stored on-chain



**Getting Started**
1. Prerequisites
- Node.js (v16+ recommended)
- Phantom Wallet browser extension
- Solana CLI (for smart contract development)
- Rust toolchain

2. Install Dependencies
npm install

Required packages:
- express
- jsonwebtoken
- tweetnacl
- bs58
- @solana/web3.js
- body-parser

3. Run the Server
node index.js

Server will start at:
http://localhost:3001



**Authentication Flow**
1. User clicks Login
2. Phantom Wallet connects
3. Backend generates a nonce
4. User signs message with wallet
5. Backend verifies signature
6. JWT token is issued
7. Token is validated
8. User is redirected to /success → home.html

