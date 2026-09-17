# 🌊 MintSea • Drops, Whale Alpha & Auto-Mint Suite 🐋

<div align="center">

[![Telegram Bot](https://img.shields.io/badge/Telegram-@MintSeaBot-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/MintSeaBot)
[![Platform](https://img.shields.io/badge/Platform-Cloudflare%20Workers-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)](https://workers.cloudflare.com/)
[![Runtime](https://img.shields.io/badge/Language-TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)

**Next-Generation Web3 Telegram Bot for NFT Drops, On-Chain Whitelist Verification & Whale Intelligence.**

[Launch Bot on Telegram](https://t.me/MintSeaBot) • [Report Issue](https://github.com/)

</div>

---

## ⚡ Overview

**MintSea** is an ultra-fast, serverless Telegram bot built on Cloudflare Workers edge infrastructure. Engineered specifically for NFT collectors, traders, and alpha hunters, it brings enterprise-grade drop intelligence directly to Telegram.

Simply paste an OpenSea drop link or collection slug, and MintSea instantly extracts on-chain SeaDrop parameters, validates your Merkle whitelist eligibility, displays tier schedules, and allows setting automated alerts and mint actions.

---

## ✨ Key Features

### 🎟️ Instant Whitelist (WL) Verification
- **On-Chain Merkle Proofs:** Queries SeaDrop smart contracts directly to verify if your connected or provided wallet is whitelisted.
- **Stage Classification:** Accurately identifies whether your wallet qualifies for **Guaranteed WL**, **VIP**, **Presale**, or **FCFS** phases.
- **Allocation & Mint Caps:** Displays max mintable items per wallet and mint price in ETH, POL, or native currencies.

### 👥 Bulk Multi-Wallet Checking
- Check **20+ wallets simultaneously** against any drop in a single command.
- Ideal for alpha callers, syndicates, and collectors managing multiple burner and vault addresses.
- Clear breakdown of which wallets are eligible and their respective allocations.

### 🐋 Whale Radar & Alpha Intelligence
- Real-time monitoring of top Web3 collectors and whale wallets.
- Instant alerts when whales mint, purchase, or interact with high-profile drops.
- Whale portfolio inspection directly through Telegram inline keyboards.

### ⏰ Mint Alarms & Countdown Timers
- Set custom alarms for upcoming drop stages (e.g., 10 mins before presale or public launch).
- Automated push notifications dispatched directly to your Telegram chat or group before the drop goes live.

### ⚡ Automated SeaDrop Minter
- Direct SeaDrop smart contract interaction engine.
- Scheduled minting and quick-mint wizard for high-demand, rapid sell-out drops.
- Gas management and non-blocking asynchronous execution on the edge.

### 🔗 Smart Auto-Link Detection & Group Support
- Paste any OpenSea drop URL (`https://opensea.io/collection/.../drop`) into PM or Telegram group chats.
- MintSea automatically detects the collection slug, contract address, and network chain, responding with a rich HTML intelligence card.

---

## 🚀 Telegram Commands

| Command | Description | Example |
| :--- | :--- | :--- |
| `/start` | Open interactive main menu and feature guide | `/start` |
| `/check <link> [0x...]` | Check whitelist eligibility for a drop | `/check collectr 0x123...456` |
| `/setwallet <0x...>` | Connect and save your default wallet address | `/setwallet 0x123...456` |
| `/mywallet` | View and manage connected main and burner wallets | `/mywallet` |
| `/bulk <link> <wallets...>` | Check multiple wallets simultaneously | `/bulk collectr 0x... 0x...` |
| `/drops` | Explore 24-hour trending drops on OpenSea | `/drops` |
| `/help` | Complete command list and usage documentation | `/help` |

> 💡 **Pro-Tip:** Once you set your default wallet with `/setwallet`, you don't need to type commands anymore — just **send any OpenSea link** and MintSea will do the rest!

---

## 📱 Sample Intelligence Card (Telegram Preview)

```text
🌊 MINTSEA • DROP INTEL 🐋
━━━━━━━━━━━━━━━━━━━━━━━━━━
📦 Collection : Collectr Genesis Pass
⛓️ Network    : Ethereum Mainnet
📄 Contract   : 0x7B9...42A1

🎟️ Whitelist Status:
✅ ELIGIBLE (Guaranteed WL)
• Max Allowed : 2 NFTs
• Price       : 0.025 ETH (~$85.50)
• Stage       : Allowlist Mint (Active Now 🔥)

⏰ Schedule:
🟢 Allowlist Sale : LIVE (Ends in 03h 42m)
⚪ Public Mint    : Starts Tomorrow at 18:00 UTC

[ ⚡ Quick Mint ]  [ ⏰ Set Alarm ]  [ 🐋 Whale Activity ]
```

---

## 🏗️ Architecture & Technology Stack

```
   ┌────────────────┐
   │ Telegram User  │
   └───────┬────────┘
           │ (Direct Links / Commands)
           ▼
   ┌──────────────────────────────────────────────────┐
   │ Cloudflare Workers (Global Edge Network)         │
   │ ──────────────────────────────────────────────── │
   │ • Grammy Framework (Webhook Routing)             │
   │ • Smart URL Parser & EVM Address Extractor       │
   │ • On-Chain SeaDrop Contract Reader (Viem)        │
   │ • Merkle Allowlist Verification Engine           │
   │ • KV / Edge State Management                     │
   └───────────────┬──────────────────┬───────────────┘
                   │                  │
        (On-Chain Read Queries)   (Metadata & Drop Feeds)
                   ▼                  ▼
      ┌──────────────────────┐   ┌────────────────────┐
      │ EVM RPC Providers    │   │ OpenSea API        │
      │ (ETH, Polygon, Base) │   │ & Public Endpoints │
      └──────────────────────┘   └────────────────────┘
```

- **Runtime:** Cloudflare Workers (Serverless V8 Edge Isolates)
- **Framework:** [Grammy](https://grammy.dev/) (Telegram Bot Framework)
- **Language:** TypeScript
- **Web3 / On-Chain:** Viem, SeaDrop ABI Protocols
- **Networks Supported:** Ethereum, Polygon, Arbitrum, Optimism, Base

---

## 🛡️ Security & Privacy

- **Read-Only Verification:** Default whitelist checks and drop monitoring only require public Ethereum addresses (`0x...`). 
- **Non-Custodial:** Never share private keys or seed phrases for standard checking.
- **Edge Security:** Powered by Cloudflare's DDoS protection and zero-trust infrastructure.

---

## 👨‍💻 Team & Credits

Designed and developed with ⚡ by **SaGaStack Team** (`lil x SG`).

Built for high-performance Web3 operations, alpha group integrations, and automated drop execution.

---

<div align="center">
  <sub>Built for the Web3 Community • 2026 MintSea</sub>
</div>
