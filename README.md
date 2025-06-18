# SolMate CLI 🪙

A beginner-friendly CLI wallet on the Solana blockchain that teaches you how to generate keypairs, receive SOL airdrops, send transactions, and trace them using block explorers.

---

## 🚀 Features

- 🔐 Generate Solana wallet (keypair) using CLI
- 🌐 Configure Devnet for safe testing
- 🪂 Airdrop SOL tokens to your wallet
- 💸 Send transactions to another wallet
- 🔎 Track transactions using Solana Explorer / Solscan
- 📜 Read logs, fees, and signature confirmations
- 🧠 Learn-by-doing: ideal for Web3 beginners

---

## 📦 Prerequisites

- macOS/Linux/WSL terminal
- [Solana CLI](https://docs.solana.com/cli/install-solana-cli-tools)

Install Solana CLI:  
- figure out yourself for your own OS.

---

## 🛠️ How I Built It — Step-by-Step Walkthrough

This is a guide for anyone looking to learn by doing.

### ✅ Step 1: Install Solana CLI and check

```bash
solana --version
````

---

### 🔐 Step 2: Generate a Wallet Keypair

```bash
solana-keygen new --outfile ~/my-solana-wallet.json
solana-keygen pubkey ~/my-solana-wallet.json
```

---

### 🌐 Step 3: Configure Devnet

```bash
solana config set --url https://api.devnet.solana.com
solana config get
```

---

### 📬 Step 4: Get Your Wallet Address

```bash
solana address
```

---

### 💸 Step 5: Airdrop SOL to Wallet

```bash
solana airdrop 1
solana balance
```

---

### 👥 Step 6: Create a Second Wallet for Testing Transfers

```bash
solana-keygen new --outfile ~/receiver-wallet.json
solana-keygen pubkey ~/receiver-wallet.json
```

---

### 🔁 Step 7: Send SOL (0.1) to the Second Wallet

```bash
solana transfer \
  $(solana-keygen pubkey ~/receiver-wallet.json) \
  0.1 \
  --from ~/.config/solana/id.json \
  --allow-unfunded-recipient \
  --fee-payer ~/.config/solana/id.json \
  --no-wait
```

---

### 🔎 Step 8: Confirm the Transaction

```bash
solana confirm <TRANSACTION_SIGNATURE>
```

---

### 🌐 Step 9: View on Block Explorer

Paste your transaction signature into:

* [Solana Explorer](https://explorer.solana.com/?cluster=devnet)
* [Solscan](https://solscan.io/?cluster=devnet)

Or directly use:

```
https://explorer.solana.com/tx/<SIGNATURE>?cluster=devnet
```

Explore:

* Sender/Receiver
* Instructions
* Logs
* Fees
* Confirmation status

---

## 📸 Screenshots of my own terminal
<img width="606" alt="Screenshot 2025-06-19 at 1 41 35 AM" src="https://github.com/user-attachments/assets/672b9504-4caf-4287-b38d-c90a472427ef" />
<img width="605" alt="Screenshot 2025-06-19 at 1 42 14 AM" src="https://github.com/user-attachments/assets/d8fab964-2e0f-42c8-aaba-cd2d6477c934" />
<img width="604" alt="Screenshot 2025-06-19 at 1 44 03 AM" src="https://github.com/user-attachments/assets/a73345d9-7be6-4af3-8158-f69f205e3c29" />
<img width="604" alt="Screenshot 2025-06-19 at 1 47 57 AM" src="https://github.com/user-attachments/assets/6b8b80f9-7deb-4172-a854-a71eeaeab00a" />

---

## 📘 License

Free to use ♥️

---

## 🙌 Credits

Built during my personal Web3 journey.
Inspired by Solana docs, CLI tooling, and curiosity.
