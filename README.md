---
icon: bitcoin
cover: .gitbook/assets/image.jpg
coverY: 114.3157894736842
layout:
  width: default
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---
# Bold Bitcoin Wallet

> **Seedless, secure Bitcoin wallet using Threshold Signatures.**

No seeds, no hardware wallets, no dependencies. Pure and Resilient Bitcoin Security, powered by superior Threshold Signatures technology, for ultimate self-custody control.

---

## Table of Contents

- [Introduction](#introduction)
- [Key Features](#key-features)
- [Installation](#installation)
- [How It Works](#how-it-works)
- [Features](#features)
  - [Why Choose Bold Bitcoin Wallet?](#why-choose-bold-bitcoin-wallet)
  - [Nostr Integration - Connect from Anywhere](#-nostr-integration---connect-from-anywhere)
  - [Multi-Address Type Support](#-multi-address-type-support)
  - [Enhanced PSBT Signing](#-enhanced-psbt-signing)
  - [Privacy & Security Features](#-privacy--security-features)
  - [User Experience Features](#-user-experience-features)
  - [Reliability & Error Handling](#️-reliability--error-handling)
- [Security Model](#security-model)
  - [Privacy First](#privacy-first)
  - [User Responsibility](#user-responsibility)
  - [Self-Custody Grade](#self-custody-grade)
- [Recovery Guide](#recovery-guide)
- [Developer Guide](#developer-guide)
- [Community](#community)
- [Terms & Agreements](#terms--agreements)

---

## Introduction

Bold Bitcoin Wallet is an open-source, self-custodial Bitcoin wallet designed for maximum security and ease of use. Unlike traditional wallets, Bold eliminates the need for seed phrases or hardware wallets, leveraging threshold signature schemes (TSS) for robust security.

### What Makes Bold Different?

- **No Seed Phrases**: Traditional wallets require you to write down and secure a 12-24 word seed phrase. Bold uses Threshold Signatures, eliminating this single point of failure.
- **Multi-Device Security**: Your private key is split across 2-3 devices using cryptographic threshold signatures. No single device can access your funds alone.
- **Offline Capable**: Setup and signing can be done completely offline. No internet required for key generation or transaction signing.
- **100% Open Source**: Fully auditable and transparent codebase available on GitHub.

---

## Key Features

### 🔐 Security & Privacy
- ✅ **Seedless Setup** - No seed phrases to write down or lose. Uses Threshold Signature Scheme (TSS)
- 🔐 **Multi-Device Security** - Private key split across 2-3 devices. Choose Duo (2-of-2) or Trio (2-of-3) mode
- 🔒 **End-to-End Encryption** - All device communications encrypted with NIP-44
- 👁️ **Privacy Controls** - Hide/show balance, anonymous API access, no personal data collection

### 🌐 Connectivity
- 🌍 **Nostr Integration** - Connect devices from anywhere in the world via decentralized relays
- 📶 **Local WiFi/Hotspot** - Fast pairing option for nearby devices
- 🔄 **Resilient Connections** - Automatic relay failover, continues working if some relays fail
- 🚫 **Offline Capable** - No internet required for setup or signing transactions

### 💰 Bitcoin Features
- 💎 **All Address Types** - Legacy, SegWit Native, SegWit Compatible, and Taproot support
- 🎛 **PSBT Signing** - Sign transactions from Sparrow, Electrum, BlueWallet, and other wallets
- 📋 **Multi-Descriptor Support** - Generate output descriptors for all address types
- 🧾 **Flexible Mempool** - Support for Mempool.space (public or self-hosted)

### 🎨 User Experience
- 🚀 **Easy Setup** - Quick onboarding with intuitive device pairing
- 💼 **Clean Interface** - Wallet home with balance and transaction history
- 📱 **Smart Features** - Balance card with Max button, QR scanning, transaction details
- ⚙️ **Customizable** - Android icon changer, transport mode selector

### 📦 Open Source & Reliability
- 📦 **100% Open Source** - Fully auditable and transparent codebase
- 🔄 **Cross-Platform Recovery** - CLI tools for Windows, Linux, and macOS
- 🛡️ **Enhanced Reliability** - Transaction broadcast retry, session recovery
- 📱 **Multiple Platforms** - iOS, Android, F-Droid available

---

## Installation

### Download Bold Bitcoin Wallet

Install Bold Bitcoin Wallet on your mobile devices:

**iOS:**
[![Download on the App Store](https://tools.applemediaservices.com/api/badges/download-on-the-app-store/black/en-us?size=250x83&releaseDate=1699228800)](https://apps.apple.com/ae/app/bold-bitcoin-wallet/id6748949478)

**Android:**
- [Google Play Store](https://play.google.com/store/apps/details?id=com.boldwallet)
- [F-Droid](https://f-droid.org/packages/com.boldwallet) - FOSS version available
- [Zap Store](https://zapstore.dev/apps/naddr1qvzqqqr7pvpzq7xwd748yfjrsu5yuerm56fcn9tntmyv04w95etn0e23xrczvvraqq8xxmmd9e3x7mrywaskcmr9ws90nrd9)
- [Direct APK Download](https://github.com/BoldBitcoinWallet/BoldWallet/releases/latest)

> ⚠️ **Important:** If installing the APK directly, it is signed with the official BoldWallet keystore and is **not compatible** with the F-Droid version. Always install updates from **one source only** to avoid signature conflicts.

---

## How It Works

1. **Install on Two or Three Devices** – Set up the wallet on two separate devices (or three for 2-of-3 threshold).
2. **Setup or Restore** – Either create a new wallet or restore from key shares.
3. **Manage Your Bitcoin** – Securely send, receive, and hold Bitcoin.
4. **HODL with Peace of Mind** – Your private keys are never exposed or stored in a single place.

### Technical Overview

Bold Bitcoin Wallet uses **Threshold Signature Schemes (TSS)** to split your private key across multiple devices:

- **Duo Mode (2-of-2)**: Requires both devices to sign transactions - maximum security, both devices must be present
- **Trio Mode (2-of-3)**: Requires any 2 of 3 devices to sign transactions - more flexibility, can sign with any 2 devices
- **No Single Point of Failure**: No device alone can access your funds
- **Cryptographic Security**: Uses proven cryptographic protocols for key generation and signing

---

## Features

### Why Choose Bold Bitcoin Wallet?

Bold Bitcoin Wallet offers a unique combination of security, privacy, and convenience that sets it apart from traditional Bitcoin wallets:

- **Seedless Setup** – No seed phrases to write down, memorize, or lose. Backup keyshares via cloud, email, or messaging apps.
- **Multi-Device Security** – Choose Duo mode (2-of-2) for maximum security or Trio mode (2-of-3) for flexibility. No single device can access your funds.
- **Connect from Anywhere** – Use Nostr to pair devices globally, or use local WiFi for fast nearby pairing.
- **Self Custody** – All transactions happen locally between your devices, with no third-party involvement.
- **Open Source** – Fully auditable and transparent codebase available on GitHub.

### 🌐 Nostr Integration - Connect from Anywhere

Bold Wallet supports **Nostr** for decentralized device pairing and transaction signing. This is a major differentiator:

- **Works Globally** – Connect devices from anywhere in the world, not just on the same WiFi network
- **Decentralized Relays** – Uses Nostr relays for communication, no central server required
- **NIP-44 Encryption** – All Nostr communications use NIP-44 encryption for maximum security
- **Resilient Connections** – Automatically connects to multiple relays in parallel, continues working if some relays fail
- **Transport Mode Selector** – Choose between Local WiFi/Hotspot (fast for nearby devices) or Nostr (works from anywhere)

### 💰 Multi-Address Type Support

Bold supports all Bitcoin address types:

- **Legacy (P2PKH)** – Addresses starting with `1` (mainnet) or `m/n` (testnet)
- **SegWit Native (P2WPKH)** – Addresses starting with `bc1` (mainnet) or `tb1` (testnet) - **Default for new wallets** (lower fees)
- **SegWit Compatible (P2SH-P2WPKH)** – Addresses starting with `3` (mainnet) or `2` (testnet)
- **Taproot (P2TR)** – Addresses starting with `bc1p` (mainnet) or `tb1p` (testnet)

New wallets default to SegWit Native (BIP84) for better efficiency and lower transaction fees.

### 🎛 Enhanced PSBT Signing

Bold provides comprehensive PSBT (Partially Signed Bitcoin Transaction) support:

- **Dedicated PSBT Screen** – Easy-to-use interface with collapsible sections
- **Multi-Descriptor Support** – Generate and display output descriptors for all three address types (Legacy, SegWit Native, SegWit Compatible)
- **Copy/Share/QR Buttons** – Individual buttons for each descriptor type for easy sharing
- **Smart Signing** – Automatically filters and only signs inputs that belong to your wallet
- **Compatible Wallets** – Works with Sparrow, Electrum, BlueWallet, and other PSBT-compatible wallets

### 🔒 Privacy & Security Features

- **Hide/Show Balance** – Tap balance to toggle visibility, preference persists across sessions
- **No Personal Data Collection** – Privacy-first approach, no tracking
- **Anonymous API Access** – Public Bitcoin APIs accessed anonymously
- **NIP-44 Encryption** – All Nostr communications encrypted end-to-end
- **Local Processing** – All crypto actions occur locally and are encrypted

### 🎨 User Experience Features

- **Android Icon Changer** – Customize your app icon from wallet settings
- **Balance Card in Send Modal** – Prominent balance display with integrated "Max" button
- **Smart Balance Check** – Automatic balance refresh when clicking Send button
- **Improved Transaction Details** – Better address display, amount formatting, status indicators, direct links to blockchain explorers
- **Unified QR Scanner** – Platform-optimized QR scanning with progress indicators
- **QR Scan Shortcut** – Share transaction details (address, amount, fee) via QR code between devices for quick entry

### App Features

- **🔒 Secure Lock Screen** - Biometric and passcode protection
- **🚀 Easy Setup** - Quick onboarding with device pairing
- **💼 Wallet Home** - Clean interface showing balance and transaction history
- **📤 Send Bitcoin** - Create and sign transactions securely
- **📥 Receive Bitcoin** - Generate addresses with QR codes
- **🎛 PSBT Signing** - Import and sign PSBTs from Sparrow, Electrum, and other wallets
- **⚙️ Settings** - Customize network, API providers, Nostr relays, and wallet preferences
- **🔐 Multi-Device Pairing** - Connect devices via Nostr or local WiFi

### 🛡️ Reliability & Error Handling

- **Resilient Relay Connections** – Automatically connects to multiple Nostr relays in parallel, continues working if some fail
- **Transaction Broadcast Retry** – Automatic retries with exponential backoff for reliable transaction broadcasting
- **Enhanced Session Management** – Improved session recovery and error handling
- **Panic Recovery** – Comprehensive Go panic recovery coverage for stability

---

## Security Model

Bold Bitcoin Wallet implements a comprehensive security model designed for maximum protection and privacy.

### Privacy First

- No personal data collection.
- All crypto actions occur locally and are encrypted.
- Public Bitcoin APIs are accessed anonymously.

### User Responsibility

- Secure your devices against malware and threats.
- Keep backup shares safe and private.
- Understand that lost keys cannot be recovered.

### Self-Custody Grade

- Bold is open-source and available for public audit.
- Provided "as is"—no guarantees of error-free use.
- Developers are not liable for loss or unauthorized access.

### Threshold Signature Security

Bold uses **Threshold Signature Schemes (TSS)** which means:

- Your private key is **never** stored in one place
- Multiple devices must collaborate to sign transactions
- Even if one device is compromised, your funds remain secure
- No single point of failure

---

## Recovery Guide

If you need to recover or spend Bitcoin from your keyshares without using the mobile app, you can use the command-line recovery tools.

### When to Use Recovery Tools

These tools should **ONLY** be used when:
- The mobile app is permanently unavailable
- You need emergency access to funds
- You are prepared to move all funds to a new wallet immediately
- You understand and accept the security risks

> ⚠️ **CRITICAL SECURITY WARNING**: Using CLI recovery tools requires loading BOTH keyshares on the same computer, which creates a significant security risk. After using these tools, you MUST move ALL funds immediately to a new wallet and create new keyshares.

### Available Tools

1. **`bold-spend` binary** (Recommended) - Works on Windows, Linux, and macOS
2. **`spend-bitcoin.sh` script** - Unix/Linux/macOS only

### Quick Recovery Example

```bash
# Navigate to BBMTLib directory
cd BBMTLib

# Build the recovery binary
./build-bold-spend.sh

# Preview transaction (estimate fee)
./bin/bold-spend-darwin-arm64 \
  --to-address <recipient_address> \
  --amount-sats <amount> \
  --network testnet3 \
  --mempool-url https://mempool.space/testnet/api \
  --derivation-path "m/84'/1'/0'/0/0" \
  --address-type p2wpkh \
  --keyshare1 "KeyShare1.Dec19.2025.1257.share" \
  --keyshare2 "KeyShare2.Dec19.2025.1257.share" \
  --passphrase1 "your-passphrase-1" \
  --passphrase2 "your-passphrase-2" \
  --preview

# Send transaction (remove --preview and add --fee-sats)
./bin/bold-spend-darwin-arm64 \
  --to-address <recipient_address> \
  --amount-sats <amount> \
  --fee-sats <estimated_fee> \
  --network testnet3 \
  --mempool-url https://mempool.space/testnet/api \
  --derivation-path "m/84'/1'/0'/0/0" \
  --address-type p2wpkh \
  --keyshare1 "KeyShare1.Dec19.2025.1257.share" \
  --keyshare2 "KeyShare2.Dec19.2025.1257.share" \
  --passphrase1 "your-passphrase-1" \
  --passphrase2 "your-passphrase-2"
```

### Complete Recovery Documentation

For detailed recovery instructions, including:
- All address types (Legacy, SegWit Native, SegWit Compatible, Taproot)
- Platform-specific instructions (Windows, Linux, macOS)
- Troubleshooting common issues
- Complete workflow examples
- Security best practices

👉 **See the full [Recovery Guide](https://github.com/BoldBitcoinWallet/BoldWallet/blob/v2.1.2/BBMTLib/RECOVER.md)**

---

## Developer Guide

### Building from Source

BoldWallet is a React Native mobile app (Android/iOS) built using Node.js v20.18.1.

#### Android - Build It Yourself

**Via Auto Builder (Docker - Recommended)**

The easiest way to build the APK is using Docker:

```bash
# From project root
./docker/scripts/docker-apk-builder.sh

# With verbose output
./docker/scripts/docker-apk-builder.sh --verbose

# F-Droid build
./docker/scripts/docker-apk-builder.sh --fdroid

# Build from specific git reference
./docker/scripts/docker-apk-builder.sh --git=main --verbose
```

**Via Manual Build**

```bash
# Install dependencies
npm install

# To rebuild the android/app/libs/tss.aar:
# Check the BBMTLib/README.md, Android Section

# For Android APK build:
cd android
./release.sh
# APK generated under:
# ./android/app/build/outputs/apk/release/app-release.apk
```

#### iOS Build

iOS builds follow the standard React Native iOS guide. See the [React Native documentation](https://reactnative.dev/docs/environment-setup) for setup instructions.

### Docker Build System

The Docker build system provides a cross-platform solution for building the Android APK:

- **Cross-platform**: Works on macOS and Linux (Ubuntu/Debian tested)
- **Optimized**: Layer caching, BuildKit cache mounts, multi-stage builds
- **Fast**: First build ~30-60 minutes, subsequent builds ~5-10 minutes

For complete Docker build documentation, see [docker/README.md](https://github.com/BoldBitcoinWallet/BoldWallet/blob/main/docker/README.md).

---

## Community

Join and contribute to the Bold Bitcoin Wallet community:

- **Twitter (X)**: [@boldBTCWallet](https://x.com/boldBTCWallet)
- **Discord**: [Join our Discord](https://discord.gg/p4ectmVtJ2)
- **GitHub**: [BoldBitcoinWallet](https://github.com/BoldBitcoinWallet/)

### Contact Us

- **Email**: [info@boldbitcoinwallet.com](mailto:info@boldbitcoinwallet.com)
- **Discord**: [Join our Discord](https://discord.gg/8Qn5Xn42)

---

## Terms & Agreements

Please review the following before using Bold Bitcoin Wallet:

- [Terms of Service](https://github.com/BoldBitcoinWallet/Terms/blob/main/Terms%20Of%20Service.md)
- [Privacy Policy](https://github.com/BoldBitcoinWallet/Terms/blob/main/Privacy%20Policy.md)

By using Bold Bitcoin Wallet, you agree to:

- Use the app lawfully and responsibly.
- Accept the risks of managing Bitcoin independently.

---

## Travel with Confidence

With Bold Bitcoin Wallet, your private keys are not tied to any device or paper. Backup your key shares, uninstall the app, and restore anytime. Your Bitcoin, your control—secure, resilient, and incognito.

---

**Last Updated**: January 2025

