# 🌐 Netrum Node Installation Guide & Project Overview

## 📌 About Netrum

**Netrum** is an **AI-powered Web3 developer platform** designed to simplify blockchain development, enhance security, and accelerate deployment through intelligent automation.  
It aims to lower the technical barrier for developers and provide a seamless integration layer for blockchain applications.

🔗 Official website: [netrumlabs.com](https://www.netrumlabs.com/)

---

## 💻 Hardware & Network Requirements

To run the **Netrum Lite Node** smoothly, make sure your system meets the following minimum requirements:

### 🔧 Hardware Requirements
| Component   | Minimum | Recommended |
|-------------|----------|--------------|
| **CPU**     | 2 Cores  | 2+ Cores     |
| **RAM**     | 4 GB     | 6 GB+        |
| **Disk**    | 50 GB SSD| 100 GB SSD   |

⚡ *SSD storage is highly recommended for faster performance and node stability.*

### 🌐 Network Requirements
| Type       | Minimum Speed |
|------------|----------------|
| **Download** | 10 Mbps       |
| **Upload**   | 10 Mbps       |

A stable and fast internet connection is crucial for uptime, sync, mining tasks, and daily reward claims.

---

## 🚀 Key Features
- 🤖 **AI-Assisted Development** – auto-generates secure smart contracts, optimizes gas usage, and simplifies development.
- 🔗 **Multi-Chain Support** – unified API/SDK interface to interact with multiple blockchains.
- 💳 **Crypto Payment Gateway** – instant settlement, automated reconciliation, and programmable payment flows.
- ⚡ **Web3 Gateway** – CLI and SDKs (e.g., JavaScript SDK) for seamless integration.
- 🛡️ **Infrastructure AI Co-Pilot** – assists with frontend scaffolding, security analysis, and automated testing.
- 🌍 **Community Node Network** – decentralized, community-operated nodes ensuring reliability, security, and tokenized incentives.

---

## 🏗️ Four Pillars of Netrum
1. **Crypto Payment Gateway**  
2. **Web3 Gateway (API & SDK)**  
3. **Infrastructure AI Co-Pilot**  
4. **Community-Operated Node Network**  

---

## 🔧 Netrum Lite Node – Setup Guide (Ubuntu/Linux)

Follow these steps to install and run the **Netrum Lite Node CLI** on Ubuntu/Linux:

### 1. Clone the Repository
```bash
git clone https://github.com/NetrumLabs/netrum-lite-node.git
```

### 2. Navigate to Project Directory
```bash
cd netrum-lite-node
```

### 3. Install Required Dependencies
```bash
sudo apt update && sudo apt install -y curl bc jq speedtest-cli nodejs npm
```

### 4. (Recommended) Install Node.js v20
Check your current Node.js version:
```bash
node -v
```
If not **v20.x.x**, install it:
```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install -y nodejs
```

### 5. Install Project Dependencies
```bash
npm install
```

### 6. Link the CLI Globally
```bash
npm link
```

### 7. Test the CLI
```bash
netrum
```
You should see the Netrum Lite Node CLI interface:
```
  Netrum CLI  Version v2.0.0
  Light-weight node & wallet toolkit for the Netrum network.

  Available Commands:
  netrum-update          Cli Update
  netrum-system          System status & logs
  netrum-new-wallet      Create / new a wallet
  netrum-import-wallet   Create / import a wallet
  netrum-wallet          Create / inspect a wallet
  netrum-wallet-key      Export private key
  netrum-wallet-remove   Delete wallet files
  netrum-check-basename  Check basename conflicts
  netrum-node-id         Show current Node ID
  netrum-node-id-remove  Clear Node ID
  netrum-node-sign       Sign a message with node key
  netrum-node-register   Register node on-chain
  netrum-sync            Sync blockchain data
  netrum-sync-log        Node sync logs
  netrum-mining          Start mining
  netrum-mining-log      Node mining logs
  netrum-claim           Claim rewards
```
Run `netrum <command> --help` for command-specific options.

---

## ⚡ Post-Domain Registration Workflow
After registering your domain https://www.base.org/names, run the following sequence:

```bash
netrum-new-wallet

![Netrum Lite Node Screenshot](https://github.com/robotek8/netrum-node-guide/blob/main/images/1.png?raw=true)


netrum-check-basename
netrum-node-id
netrum-node-sign
netrum-node-register
netrum-sync
```

Wait until you see the message:
```
Mining token saved
```

Then start mining:
```bash
netrum-mining
```

To check mining status:
```bash
netrum-mining-log
```

---

## 📚 Resources
- [Official Website](https://www.netrumlabs.com/)
- [Whitepaper (v1.1, Aug 2025)](https://www.netrumlabs.com/Netrum-Official-Whitepaper.pdf)
- [GitHub Repository](https://github.com/NetrumLabs/netrum-lite-node)

---

## 🤝 Contributing
Want to contribute? Fork the repository, make changes, and submit a Pull Request.  
For community support, join discussions and help others set up their nodes!

---

## 📜 License
This project follows the license provided in the official repository.

---

✨ **Netrum makes Web3 development human-centric, secure, and efficient.**
