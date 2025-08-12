# Netrum Lite Node – Quick Setup Guide
![Netrum Lite Node Guide Header](https://github.com/izmerGhub/Netrum-Lite-Node-Guide-by-Izmer/blob/main/asset/lightnode%20guide%20orange.png)

**Netrum Lite Node CLI** is a lightweight tool to join the [Netrum](https://netrum.io) decentralized compute network — create/import wallets, register your node, sync, mine, and claim rewards from your terminal.

---

## 📋 Prerequisites

**Minimum Requirements**
| Component | Minimum | Recommended |
|-----------|---------|-------------|
| CPU       | 2 Cores | 2+ Cores    |
| RAM       | 4 GB    | 6 GB+       |
| Disk      | 50 GB SSD | 100 GB SSD |
| Network   | 10 Mbps up/down | Stable high-speed |

**Software Requirements**
- Ubuntu 20.04/22.04 (Linux VPS or local machine)
- Node.js **v20** (required)
- `npm` (bundled with Node.js)

---

## ⚡ Installation

### 1. Clone Repository

**➡ VPS**
```bash
git clone https://github.com/NetrumLabs/netrum-lite-node.git
cd netrum-lite-node
```

**➡ Local PC (WSL)**
> ⚠ Install inside your **Linux home directory (`~`)**, not `/mnt/c/` or any Windows path — avoids permission & speed issues.
```bash
cd ~
git clone https://github.com/NetrumLabs/netrum-lite-node.git
cd netrum-lite-node
```

---

### 2. Install Dependencies
```bash
sudo apt update && sudo apt install -y curl bc jq speedtest-cli nodejs npm
```

---

### 3. (If Needed) Install Node.js v20
```bash
node -v    # check version
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install -y nodejs
```

---

### 4. Install Project Dependencies
```bash
npm install
```

---

### 5. Link CLI Globally
```bash
npm link
```

---

### 6. Test CLI
```bash
netrum
```
You should see:
```
Netrum CLI  Version v2.0.0
Light-weight node & wallet toolkit for the Netrum network.
```

---

## 🚀 Step-by-Step Usage

> ⚠️ Always **back up your private keys** before starting.

### 1️⃣ Import Wallet (EVM-Compatible)
```bash
netrum-import-wallet
```
💡 *Paste your existing private key.*  
If new wallet:  
```bash
netrum-new-wallet
```

---

### 2️⃣ Check Base Name
```bash
netrum-check-basename
```
💡 Example output:
```
✅ Your Base name: mynode.base
```
If unregistered → set one up via Base Name Service.

---

### 3️⃣ Check Node ID
```bash
netrum-node-id
```
💡 Shows your current node identity on the Netrum network.

### 4️⃣ Sign Node ID
```bash
netrum-node-sign
```
💡 Signs a message to verify ownership.

### 5️⃣ Register Node
```bash
netrum-node-register
```
💡 Registers on-chain & backend.
Gas needed: 0.0002–0.0005 BASE.

### 6️⃣ Sync Node
```bash
netrum-sync
```
📜 Logs:
```bash
netrum-sync-log
```
💡 Maintains uptime & heartbeat signals.

### 7️⃣ Start Mining
```bash
netrum-mining
```
📜 Logs:
```bash
netrum-mining-log
```
💡 Earns NPT based on uptime.

---

## 💰 Token Claim & Balance

### 8️⃣ Claim Rewards
```bash
netrum-claim
```
💡 Claim after ~24h mining.
Gas: 0.00002–0.00003 BASE.
```
---

### 9️⃣ Check Wallet & Balance
```bash
netrum-wallet
```
💡 Shows NPT balance & wallet address.
```

---

## 🔑 Wallet Management
```bash
netrum-wallet-key
netrum-wallet-remove
```

---

## 📞 Support
Join the **[Official Netrum Discord](https://discord.gg/PJmDWb9C74)** for help.

---

## ⚡ Quick Commands Cheat Sheet

| Step | Command | Purpose |
|------|---------|---------|
| 1 | `netrum-import-wallet` / `netrum-new-wallet` | Import or create wallet |
| 2 | `netrum-check-basename` | Check Base domain name |
| 3 | `netrum-node-id` | Show Node ID |
| 4 | `netrum-node-sign` | Sign Node ID |
| 5 | `netrum-node-register` | Register node on-chain |
| 6 | `netrum-sync` | Start syncing |
| – | `netrum-sync-log` | View sync logs |
| 7 | `netrum-mining` | Start mining |
| – | `netrum-mining-log` | View mining logs |
| 8 | `netrum-claim` | Claim rewards |
| 9 | `netrum-wallet` | Check wallet & balance |
