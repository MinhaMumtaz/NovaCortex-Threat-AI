![Language](https://img.shields.io/badge/C%20%7C%20Python-Security-blue)
![Crypto](https://img.shields.io/badge/Crypto-AES--GCM-green)
![Status](https://img.shields.io/badge/Status-Active_Development-orange)

  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQsYH5Rcw229NWwDt_Ni6E4CINx6QpWtP3ZXA&s" alt="Ubuntu" width="60" height="60"/>
  <img src="https://www.serversaustralia.com.au/assets/articles/featured_images/vmware-765x460-1.jpg" alt="VMware" width="100" height="90"/>


---

# 🔐 VaultX & VaultX-Kernel  
## Dual-Layer Secure File Encryption Framework

---

## 📑 Table of Contents

1. Project Overview  
2. VaultX – High-Level File Encryption  
3. VaultX-Kernel – Low-Level Cryptography  
4. Core Methodology  
5. Benchmark & Performance  
6. Comparison: VaultX vs VaultX-Kernel  
7. Installation & Setup  
8. Usage  
9. File & Password Management  
10. Technologies Used  
11. Project Significance & Canonical Relevance  

---

## 📌 Project Overview

**VaultX & VaultX-Kernel** is a dual-layer file encryption framework designed to explore both **high-level user-friendly encryption** and **low-level system cryptography**.

- **VaultX:** High-level, Python-based, GUI-driven encryption system  
- **VaultX-Kernel:** Low-level, C-based, CLI-driven system using OpenSSL EVP APIs  

The project demonstrates secure encryption, key derivation, memory management, performance benchmarking, and password management, covering both **application-level** and **system-level cryptography**.

---

## VaultX – High-Level File Encryption

**Small Description:** Python GUI-based file encryption system  

VaultX is a high-level Python encryption framework that provides a **user-friendly interface** for securely encrypting and decrypting files. It abstracts cryptographic complexity while ensuring strong protection using modern algorithms.

### Key Features

- AES-GCM encryption for secure data
- Argon2 key derivation for strong password protection
- Graphical User Interface (Tkinter) for file selection
- Automatic password storage in `passwords.txt`
- Separate directories for encrypted and decrypted files

### Functionality

1. User selects a file via GUI  
2. Generates random salt and nonce  
3. Derives 256-bit key using Argon2  
4. Encrypts file using AES-GCM  
5. Saves encrypted output in `encrypted_files/`  
6. Stores password with filename in `passwords.txt`  
7. Decryption reverses the process using stored or user-provided password  

VaultX focuses on **ease of use**, **high-level abstraction**, and **secure file management**, making it suitable for application-level encryption tasks.

---

## VaultX-Kernel – Low-Level Cryptography

**Small Description:** C-based system cryptography with OpenSSL  

VaultX-Kernel is a low-level C encryption framework that provides **system-level control** over cryptography using OpenSSL EVP APIs. It emphasizes manual memory management, buffer handling, and high-performance encryption.

### Key Features

- AES-256-GCM encryption via OpenSSL EVP APIs
- PBKDF2-HMAC-SHA256 key derivation
- Manual buffer allocation for plaintext, ciphertext, nonce, and salt
- Command-line interface (CLI) for precise control
- Structured output: `salt + nonce + ciphertext + GCM tag`
- Optimized for performance and system-level precision

### Functionality

1. Load file into manually allocated memory buffers  
2. Generate salt and nonce using OpenSSL RNG  
3. Derive key using PBKDF2-HMAC-SHA256  
4. Encrypt/decrypt using EVP API  
5. Save output maintaining data integrity and confidentiality  

VaultX-Kernel is ideal for **system-level cryptography**, **performance optimization**, and **low-level Linux security experimentation**.

---

## Core Methodology

| Layer | Steps |
|-----|------|
| **VaultX (High-Level)** | Generate salt & nonce → Argon2 key derivation → AES-GCM encryption → Save file + password |
| **VaultX-Kernel (Low-Level)** | Allocate buffers → Generate salt & nonce (OpenSSL) → PBKDF2-HMAC key derivation → AES-GCM encryption via EVP → Save structured output |

Both layers ensure **confidentiality**, **integrity**, and **secure key management**, while demonstrating different levels of abstraction and performance focus.

---

## 📊 Benchmark & Performance

**Environment:** 1 MB test file  

| System | Encrypt Time | Decrypt Time |
|------|-------------|-------------|
| VaultX (Python GUI) | 0.1572 s | 0.1233 s |
| VaultX-Kernel (C EVP) | 0.0378 s | 0.0391 s |

### 🔍 Observations

- VaultX-Kernel is approximately **4× faster** than VaultX  
- Demonstrates **system-level efficiency vs application-level convenience**  
- Confirms performance awareness and disciplined measurement  

---

## 🔎 Comparison: VaultX vs VaultX-Kernel

| Feature | VaultX | VaultX-Kernel |
|------|------|--------------|
| Language | Python | C |
| Crypto Libraries | cryptography, Argon2 | OpenSSL EVP |
| Key Derivation | Argon2 | PBKDF2-HMAC-SHA256 |
| Abstraction | High-level | Low-level |
| Memory Handling | Python-managed | Manual buffer allocation |
| Interface | GUI (Tkinter) | CLI |
| Password Logging | Automatic | Manual |
| Performance | Moderate | Optimized |
| Use Case | Application-level encryption | System-level cryptography & learning kernel crypto |

### Summary

- VaultX emphasizes **usability and abstraction**
- VaultX-Kernel emphasizes **speed, memory control, and system-level mastery**
- Together, they illustrate cryptography across abstraction layers

---

## 📂 File & Password Management

- **Encrypted files:** `encrypted_files/`
- **Decrypted files:** `decrypted_files/`
- **Passwords:** `passwords.txt` (`filename : password`)
- Ensures **organized storage**, **recoverability**, and **secure access**

---

## 🧰 Technologies Used

- **Python:** `cryptography`, Argon2, Tkinter
- **C / OpenSSL:** EVP APIs, PBKDF2-HMAC-SHA256
- **Platform:** Ubuntu (VMware)
- **Benchmarking:** Python `time` & C `clock_gettime(CLOCK_MONOTONIC)`

source venv/bin/activate
pip install cryptography argon2-cffi
