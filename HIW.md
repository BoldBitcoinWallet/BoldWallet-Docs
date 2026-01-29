# How Bold Works  

**Bold protects your Bitcoin by splitting control across your own devices — with no seed phrase, no servers, and no company in the middle.**


---

## Think in “locks”, not keys 🔐

Most Bitcoin wallets give you **one secret**.

If that secret is:
- stolen → Bitcoin gone  
- lost → Bitcoin gone  

Bold works differently.

Instead of one secret, Bold creates a **lock that needs multiple devices to open**.

---

## Seedless by design — where your wallet really lives

Bold uses **Threshold Signature Schemes (TSS)**.

That means:
- no seed phrase
- no master private key
- no single point to steal or lose

Each device holds a **key share**.  
The full private key **never exists anywhere**, not even during signing.

```text
Traditional Wallet
------------------
[ Single Private Key ]
          |
        Spend


Bold Wallet (TSS)
-----------------
[ Device A ]   [ Device B ]   [ Device C ]
     |              |              |
     +---------- cooperate ----------+
                    |
                 Spend
```

On-chain, the result looks like a **normal single-signature Bitcoin transaction** — no multisig fingerprint, no privacy leak.

```text
❌ No Seed Phrase
❌ No Master Key
❌ No Reconstruction Point

[ Share A ] + [ Share B ] (+ [ Share C ])
        ↓
  Threshold Signature
        ↓
   Valid Bitcoin Tx
```


---

## Backups without compromise 🧠

Because Bold is **seedless**:
- each device holds its own key share
- each key share can be backed up **independently**
- backups can be stored in **different physical locations**

```text
Backups (Independent & Encrypted)
---------------------------------
[ Device A Backup ] → Location A (SD card)
[ Device B Backup ] → Location B (Signal App)
[ Device C Backup ] → Location C (cloud/inbox)

No single backup can restore the wallet
```

Stealing one device or one backup:
- cannot reconstruct the wallet
- cannot spend funds
- does not expose the full key

Security comes from **separation**, not secrecy.

---

## Choose how many devices protect you

### Option A — 2 devices (2-of-2)

- both devices are always required
- permanent loss of one device → funds are unrecoverable

```text
2-of-2 Setup
------------
[ Phone ] + [ Tablet ]
     |          |
     +---- sign ----+
           |
         Spend

Loss of one device = funds locked forever
```

**Pros**
- maximum control
- no recovery paths

**Cons**
- no forgiveness for loss

---

### Option B — 3 devices (2-of-3) ⭐ Recommended

- any two devices can approve
- one device can be lost or destroyed
- funds remain fully accessible

```text
2-of-3 Setup
------------
[ Phone ]     [ Tablet ]     [ Laptop ]
     |             |              |
     +----- any two cooperate ----+
                  |
                Spend

One device lost → wallet still usable
```

**Pros**
- no single point of failure
- no custodian
- real-world resilience

**Cons**
- extra device needed for the setup

---

## How devices communicate 🌍

Bold devices communicate **directly and bidirectionally**.

They use:
- **Nostr relays** (public or self-hosted)
- **NIP-44 end-to-end encryption**
- **multiple relays in parallel**

    (NIP-44 encrypted, bidirectional)

```text
Encrypted, Bidirectional Messaging
----------------------------------
          Relay 1
         ↗       ↘
[ Device A ]   Relay 2   [ Device B ]
         ↘       ↗
          Relay 3

• NIP-44 encrypted
• Multiple relays
• Relays = transport only
```

### Why this matters
- messages flow both ways
- no single relay can block signing
- relays never see keys or transactions
- you can run your **own private Nostr relay**

Relays are **transport only**, not trusted parties.

---

## Signing paths: online, local, and air-gapped

### Online signing
- devices coordinate over Nostr
- messages sent over multiple relays in parallel
- resilient across networks and borders

```text
Online Signing
--------------
[ Device A ] ⇄ Nostr ⇄ [ Device B ]
      |
  Threshold Signing
      |
   Final Tx
```

### Local signing
- devices connect over **local Wi-Fi / hotspot**
- no internet required
- ideal for nearby devices

```text
Local Network Signing
---------------------
[ Device A ] ⇄ Local Wi-Fi / Hotspot ⇄ [ Device B ]
      |
  Threshold Signing
      |
   Final Tx

• No internet
• Same security model
• Same TSS guarantees
```

---

### Air-gapped capability - signing (PSBT via QR)

Air-gap applies to **PSBT workflows**, not device coordination.

1. Transaction created in a watch-only wallet
2. PSBT shown as **animated QR**
3. Bold scans and signs offline
4. Signed PSBT returned via QR

```text
Air-Gapped Flow
---------------
[ Watch-Only Wallet ]
        |
     PSBT (QR)
        ↓
[ Bold Signer ]  ← offline
        |
 Signed PSBT (QR)
        ↓
[ Broadcaster ]
```

Signing still happens using:
- local device cooperation
- no internet
- no servers

---

## Seeing your balance — no company backend

Bold does **not** run wallet infrastructure.

You choose how blockchain data is fetched:
- public `mempool.space`
- your **self-hosted mempool**
- a mempool connected to your **Bitcoin node**

```text
Balance & UTXO Sources
---------------------
[ Bold Wallet ]
      |
      +── Public mempool.space
      +── Self-hosted mempool
      +── Private mempool → Bitcoin Node

Switch anytime. No dependency.
```

If a service disappears:
- switch endpoints
- wallet keeps working
- funds remain safe

---

## Signer-only mode (advanced users)

Bold can act as a **pure TSS signer**.

- wallet exported as **watch-only** using output descriptors
- PSBT created in Sparrow, Electrum, or BlueWallet
- Bold signs — nothing else

```text
Advanced Setup
--------------
[ Sparrow / Electrum ]
      |
   Create PSBT
      |
[ Bold TSS Signer ]
      |
   Signed PSBT
      |
 Broadcast Anywhere
```

This enables:
- cold storage
- audits
- infrastructure separation

---

## What Bold deliberately avoids 🚫

Bold does **not**:
- generate seed phrases
- store master keys
- hold recovery secrets
- run signing servers
- depend on one relay
- rely on unverifiable hardware

## If Bold vanishes tomorrow, nothing breaks.
> **Bold is software — not a service.**
- ✅ **Your wallet still works**  
  There are no Bold-operated servers, accounts, or backend dependencies.

- ✅ **Your Bitcoin remains yours**  
  Funds are controlled exclusively by your devices using threshold signatures (TSS).

- ✅ **Fully open-source**  
  The entire Bold codebase is public, auditable, and verifiable on GitHub.

- ✅ **Decentralized app distribution**  
  The Bold APK is not tied to a single store and is available via:
  - GitHub Releases  
  - F-Droid  
  - OpenAPK  
  - ZapStore  
  - Community mirrors and more others

- ✅ **No app store or vendor lock-in**  
  You don’t need Google Play, Apple services, or Bold infrastructure to install or run the wallet.

- ✅ **Alternative recovery path**  
  A CLI binaries are provided, enabling advanced users to:
  - Restore device key shares  
  - Reconstruct signing capability  
  - Create and sign transactions without the mobile app UI

> **If Bold disappears tomorrow, nothing breaks.**

This is **anti-fragile self-custody** by design:

- No backend that can be shut down  
- No company key that can be revoked  
- No permission that can be taken away  

Bold doesn’t ask for your trust —  
**it removes itself from the trust model entirely.** 🧠🛡️

---


## The honest truth

Bold gives you **real sovereignty**, not convenience theater.

- 2-of-2 → absolute control, zero forgiveness  
- 2-of-3 → resilience without trust  

No magic recovery.  
No hidden safety net.

Only:
- your devices
- math
- open-source code.

---

## Final mental model 🧠

Bold says:  
> **Your full sovereignty - no one else**

**Bold isn’t an upgrade — it’s the exit!**

