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

---------------------------------------------------------------------------------------------------------------

```bash
netrum-new-wallet

After entering the command, you will see something like the following:

rasalghul@rasalghul-System-Product-Name:~/netrum-lite-node$ netrum-new-wallet
✅ New Wallet Created:
Address:  0xA6c548C5729F229836d7B973388
Private Key:  0x7f4bf80c7a1e7eb7b418db62da79 
?? Saved to /home/rasalghul/netrum-lite-node/data/wallet/key.txt
?? Also saved to /home/rasalghul/netrum-lite-node/src/wallet/key.txt

Import your private key into an EVM wallet and fund it with $5.
👉 “You will have your own address and private key.”

----------------------------------------------------------------------------------------------------------------

Go to [base.org/names](https://www.base.org/names)

and register your unique domain, paying for it with the wallet you just created. After registration, run the following command:

netrum-check-basename

After entering the command, you will see something like the following:

rasalghul@rasalghul-System-Product-Name:~/netrum-lite-node$ netrum-check-basename
?? Checking .base name for: 0xA6c548C5729F229836d7B9733888D4c901F9708C
✅  .base name found: netrum-node.base.eth
??  Saved domain name to: /home/rasalghul/netrum-lite-node/src/identity/node-id/basename.txt

----------------------------------------------------------------------------------------------------------------

netrum-node-id

You will see this:

rasalghul@rasalghul-System-Product-Name:~/netrum-lite-node$ netrum-node-id
✅  Generated Node ID: netrum.lite.netrum-node.base.eth
??  Saved locally: /home/rasalghul/netrum-lite-node/src/identity/node-id/id.txt
??  Also saved to global path: /home/rasalghul/netrum-lite-node/data/node-id/id.txt

-----------------------------------------------------------------------------------------------------------------

netrum-node-sign

You will see:

rasalghul@rasalghul-System-Product-Name:~/netrum-lite-node$ netrum-node-sign
Looking for wallet key at: /home/rasalghul/netrum-lite-node/src/wallet/key.txt
Looking for node ID at: /home/rasalghul/netrum-lite-node/src/identity/node-id/id.txt

?? Signing Details:

-----------------------------------------------------------------------------------------------------------------
Node ID:      netrum.lite.netrum-node.base.eth
Signer Addr:  0xA6c548C5729F229836d7B9733888D4c901F9708C
Timestamp:    1755862446
Message Hash: 0x0fe6c527d27c7407807d9d4394306374273486e3f7d467ab45e59c0d98e55283
Signature:    0xb07bb0dac9be3f2d4060407c8827fcb5549da5fd34c23d3b1f1c5bb18268ea440de25b3813d1d66347920a88570941c851c4c2037bfcf333aafe12e554aa68d71c

------------------------------------------------------------------------------------------------------------------

netrum-node-register

As a result of running this command, you should see the following message at the end. If you see it, it means the node registration was successful:

⏳ Registration Response Data:

┌──────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                                                                                      │
│   🆔 Node ID: netrum.lite.netrum-node.base.eth                                                       │
│   🟠 Wallet: 0xA6c548C5729F229836d7B9733888D4c901F9708C                                              │
│   ✍️ Signature: 0xb07bb0dac9be3f2d4060407c8827fcb5549da5fd34c23d3b1f1c5bb18268ea440de25b3813d1d663   │
│   47920a88570941c851c4c2037bfcf333aafe12e554aa68d71c                                                 │
│   🔗 TX Hash: 0xa32d740e592b278aa824b0b5514dec3c330891cedf094207690e9e1947eeb006                     │
│                                                                                                      │
└──────────────────────────────────────────────────────────────────────────────────────────────────────┘


✅ Registration Completed Successfully!

------------------------------------------------------------------------------------------------------------------

netrum-sync

Yoy will see:

✅   Netrum Node Sync service installed.

Check status:
  sudo systemctl status netrum-node.service

Live logs:
  netrum-sync-log

------------------------------------------------------------------------------------------------------------------

netrum-sync-log

You will see:

[INFO] Mining token saved

After this, run command:

netrum-mining




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
