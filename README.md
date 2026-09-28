# cybersecurity-week-3-project
Task 1
# Encrypted PDF Password Cracking & Network Configuration (Kali Linux)

## 📌 Project Overview
This repository documents **Week 3 - Task 2** of my Cybersecurity Internship. The objective of this lab is to perform password extraction and cracking on an encrypted PDF file (`My Locked PDF1.pdf`) using native Kali Linux tools while maintaining proper network connectivity over a static VirtualBox NAT network.

---

## 🛠️ Tools & Technologies
* **Operating System:** Kali Linux (VirtualBox VM)
* **Networking:** VirtualBox NAT Network (`10.0.0.0/24`), Static IPv4 (`10.0.0.2`)
* **Utilities:** `pdf2john`, `john` (John the Ripper), `gzip`
* **Text Editors/CLI Tools:** `nano`, `ip route`, `NetworkManager`

---

## 🚀 Step-by-Step Implementation

### 1. Network Interface & Static IP Configuration
* Configured VirtualBox network adapter to **NAT Network** (`NatNetwork1`).
* Assigned static IP `10.0.0.2` and configured default gateway and DNS settings:
  ```bash
  sudo ip route add default via 10.0.0.1 dev eth0
  echo "nameserver 8.8.8.8" | sudo tee /etc/resolv.conf


<img width="1920" height="922" alt="Screenshot_2026-09-28_05_13_30" src="https://github.com/user-attachments/assets/85267a0b-3665-4638-9d43-d9a41a3a47f9" />
<img width="1920" height="922" alt="Screenshot_2026-09-28_05_05_12" src="https://github.com/user-attachments/assets/be354ddd-5c02-4b06-af27-1f76869b56d3" />
<img width="1917" height="912" alt="Screenshot_2026-09-28_02-35-15" src="https://github.com/user-attachments/assets/7e848f31-da9f-4dc5-91a0-a1edec5430e5" />
Task two
# Password Cracking with Networkwalks Tools 🛡️

This repository contains the documentation, step-by-step walkthrough, and proof-of-concept (PoC) screenshots for **Week 3 - Project Module 2** of the Cybersecurity Internship program.

## 📌 Project Overview
The primary objective of this lab is to demonstrate how stored hashes in encrypted files (such as PDFs) can be extracted and cracked using dictionary-based recovery techniques. 

### 🎯 Key Objectives:
* Extract John/Hashcat-compatible hash signatures (`$pdf$`) from locked PDF files.
* Perform a dictionary-based attack on the extracted hash to recover the plaintext password.
* Gain hands-on understanding of encryption vs. hashing mechanisms.

---

## 🛠️ Tools & Technologies Used
* **Target File:** `My Locked PDF1.pdf`
* **Hash Extraction:** [Networkwalks Hash Calculator](https://networkwalks.com/hash-calculator/)
* **Hash Cracking:** [Networkwalks Password Cracker](https://networkwalks.com/password-cracker/)
* **PDF Reader:** Adobe Acrobat Reader DC / Web Browser

---

## 🚀 Execution Steps & Screenshots

### Step 1: File Preparation & Hash Extraction
1. Loaded `My Locked PDF1.pdf` into the **Networkwalks Hash Calculator**.
2. The tool successfully parsed the encrypted file and extracted the Hashcat/John-compatible `$pdf$` hash format.



### Step 2: Running the Password Cracker
1. Copied the complete `$pdf$` hash signature.
2. Pasted the string into the **Networkwalks Password Cracker**.
3. Initiated the dictionary attack using built-in wordlists.



### Step 3: Password Cracked & Flag Captured
1. The tool matched the target hash digest with the plaintext entry: **`password1`**.
2. Used the recovered password to unlock `My Locked PDF1.pdf`.
3. Verified document access and captured **Flag 1**.

<img width="1920" height="922" alt="Screenshot_2026-09-28_05_41_28" src="https://github.com/user-attachments/assets/aab39176-3df3-40ed-ac82-6ff3ff774414" />


<img width="1920" height="922" alt="Screenshot_2026-09-28_05_37_36" src="https://github.com/user-attachments/assets/af8077fe-0ac2-47db-9a3f-ea123ee1bced" />
<img width="1920" height="922" alt="Screenshot_2026-09-28_05_35_45" src="https://github.com/user-attachments/assets/eda3413d-0e41-4fcc-8b15-4c9f0c343f44" />
<img width="1920" height="922" alt="Screenshot_2026-09-28_05_48_20" src="https://github.com/user-attachments/assets/03ffcb46-7894-4c28-94a0-4c3bee871708" />
<img width="1920" height="922" alt="Screenshot_2026-09-28_05_46_37" src="https://github.com/user-attachments/assets/815c3ca0-8fbe-4e63-b5e7-465b85a3c591" />


