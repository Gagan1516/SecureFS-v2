# SecureFS-v2
# 🔐 SecureFS v2

### A Role-Based Encrypted File System with Blockchain-Anchored Audit Trails

SecureFS v2 is a browser-deployable encrypted file system designed for **multi-user, compliance-sensitive environments**. It addresses critical limitations in traditional encryption tools by integrating **cryptographic identity binding, role-based access control (RBAC), and tamper-evident audit logs**—all in a **zero-dependency HTML application**.

---

## 🚀 Features

* 🔒 **AES-256-GCM Encryption (AEAD)**

  * Ensures confidentiality + integrity in a single operation
  * Detects any tampering before decryption

* 🧑‍💼 **Identity-Bound Encryption**

  * Files are cryptographically tied to a specific user identity
  * Unauthorized users cannot decrypt—even with correct keys

* 🏢 **Six-Role RBAC Model**

  * Developer, Admin, Manager, User, Auditor, Read-Only
  * Enforces **principle of least privilege**

* 📜 **Blockchain-Based Audit Trail**

  * SHA-256 hash-linked logs
  * Fully tamper-evident and verifiable

* 🚨 **Sliding Window Intrusion Detection**

  * Detects brute-force attempts
  * Auto-lockout after repeated failed logins

* 🌐 **Browser-Only Deployment**

  * Runs as a **single HTML file**
  * No installation, no dependencies, no backend required

* 🔁 **Dual-Mode Operation**

  * Works offline (browser storage)
  * Optional Python backend for persistent storage

---

## 🧠 Architecture Overview

SecureFS v2 consists of the following core components:

1. **Encryption Layer**

   * AES-256-GCM with PBKDF2 key derivation
   * Two-level key hierarchy for enhanced security

2. **Identity Binding**

   * User identity embedded in AES-GCM AAD
   * Prevents cross-user decryption attacks

3. **Access Control (RBAC)**

   * Role-based permissions enforced both frontend and backend

4. **Audit Ledger**

   * Blockchain-style hash chaining of logs
   * Detects modification, deletion, or insertion attacks

5. **Intrusion Detection System**

   * Sliding-window login monitoring
   * Smart lockout mechanism

6. **Deployment Layer**

   * Web Crypto API (browser-native security)
   * Optional server fallback

---

## 📊 Why SecureFS v2?

| Feature                   | Traditional Tools | SecureFS v2 |
| ------------------------- | ----------------- | ----------- |
| Multi-user access control | ❌                 | ✅           |
| Tamper-proof audit logs   | ❌                 | ✅           |
| Identity-bound encryption | ❌                 | ✅           |
| Browser-based deployment  | ❌                 | ✅           |
| AEAD encryption           | ✅                 | ✅           |

---

## 🛠️ Technologies Used

* **Web Crypto API** (AES-GCM, PBKDF2, SHA-256)
* **JavaScript (Vanilla)**
* **HTML5**
* **Python (optional backend)**
* **SQLite (server mode)**

---

## ⚙️ How to Use

### 🔹 Browser Mode (Default)

1. Download the `.html` file
2. Open it in any modern browser
3. Start using SecureFS immediately

### 🔹 Server Mode (Optional)

1. Run the Python backend server
2. Open the frontend in browser
3. System auto-detects server and switches mode

---

## 🔐 Security Highlights

* No external libraries → **no supply-chain risk**
* Hardware-accelerated crypto via browser
* Per-file key isolation
* Tamper detection via blockchain logs
* Resistant to insider and application-layer attacks

---

## ⚠️ Limitations

* No plausible deniability (hidden volumes)
* Uses PBKDF2 (Argon2 planned for future)
* Blockchain is single-node (not distributed)
* No formal verification (future work)

---

## 🔮 Future Improvements

* Argon2-based key derivation
* Distributed blockchain audit system
* Formal RBAC verification (ProVerif)
* Enhanced UI/UX for enterprise adoption

---

## 📄 Author

**Gudabandi Gagan**
B.Tech CSE, Lovely Professional University

---

## ⭐ Acknowledgment

Inspired by research in:

* AES-GCM (NIST)
* RBAC (NIST Standard)
* Blockchain (Nakamoto)
* Web Crypto API (W3C)

---

---

