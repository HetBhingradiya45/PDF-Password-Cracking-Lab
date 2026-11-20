# 🔐 Password Cracking Lab — README

**📅 Week 3 | Project Modules 1 & 2**
**🎓 Cybersecurity & Ethical Hacking Project Tasks**

---

## 📋 Overview

This README walks you through **two different methods** to crack the password of a locked PDF file (`My Locked PDF1.pdf`):

| Module | Tool Used | Installation Needed? |
|--------|-----------|----------------------|
| 🛠️ **Module 1** | John the Ripper (JTR) + Johnny GUI | ✅ Yes |
| 🌐 **Module 2** | Networkwalks Online Tools | ❌ No (runs in browser) |

---

## 🛠️ Module 1: Password Cracking with JTR (John the Ripper)

### 1️⃣ Download John the Ripper
📥 Official site: https://www.openwall.com/john/

🔗 Alternate links:
- https://distro.ibiblio.org/openwall/projects/john/1.9.0/
- 💾 Google Drive mirror: https://drive.google.com/drive/u/1/folders/1aHtgOh7U9mQhkN8VHU7ctTyaDg5KbuJx

### 2️⃣ Download Johnny (GUI for JTR)
📥 https://openwall.info/wiki/john/johnny

💾 Google Drive mirror: https://drive.google.com/drive/u/1/folders/1aHtgOh7U9mQhkN8VHU7ctTyaDg5KbuJx

### 3️⃣ Extract Both ZIP Files
📂 Extract John the Ripper and Johnny zips on your PC (e.g., Downloads folder).

> ⚠️ **Heads up:** Antivirus/Windows Defender may quarantine or delete `john.exe` / `johnnyInstaller.exe` since these look like "hacking tools" to it. If the exe goes missing, add the folder to antivirus exclusions, or temporarily turn off real-time protection before extracting. 🛡️

### 4️⃣ Install & Open Johnny
▶️ Run `johnnyInstaller.exe`, finish the install, then open Johnny.

### 5️⃣ Point Johnny to John.exe
⚙️ Click **Settings** → **Browse** → select `john.exe` from the `run` folder
📁 (e.g., `john-1.9.0-jumbo-1-win64\run\john.exe`)

### 6️⃣ Extract the PDF Hash
🌐 https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php

📤 Upload `My Locked PDF1.pdf` → Click **Upload** → get hash starting with `$pdf$...`

### 7️⃣ Save the Hash
📝 Copy the hash → paste in **Notepad** → save as `hash1.txt`

> ⚠️ Make sure no stray characters (like `b'`) are at the start — hash must begin exactly with `$pdf$`.

### 8️⃣ Load Hash into Johnny
📂 Click **Open password file** → select `hash1.txt` → Open

### 9️⃣ Start the Attack
🚀 Click **Start new attack** — JTR will try passwords until it finds a match ⏳

### 🔟 Get Your Password!
✅ Once cracked, password shows in the **Password** column (e.g., `password1`) 🎉

### 🔑 Open the PDF
📄 Open `My Locked PDF1.pdf` → enter cracked password → unlocked! 🔓

---

## 🌐 Module 2: Password Cracking with Networkwalks Tools

✨ No installation needed — everything runs right in your browser!

### 1️⃣ Get the Locked PDF
📥 https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/

### 2️⃣ Open the Hash Calculator
🌐 https://networkwalks.com/hash-calculator/

### 3️⃣ Upload the PDF
📑 Select the **PDF** tab → choose/drop `My Locked PDF1.pdf`
🔒 (parsed locally, nothing uploaded to any server — safe! ✅)
→ get hash starting with `$pdf$...`

### 4️⃣ Copy the Hash
📋 Click **Copy** → grab the *complete* hash starting from `$pdf$`

### 5️⃣ Open the Password Cracker
🌐 https://networkwalks.com/password-cracker/

### 6️⃣ Paste & Crack
📥 Paste hash into **PDF HASH ($PDF$...)** box
📋 Keep **Built-in List (100 passwords)** selected (or upload your own `.txt` wordlist)
🚀 Click **START CRACKING**

### 7️⃣ Wait for the Magic ✨
⏳ Tool tries passwords from the list → when matched:
🎉 **"PASSWORD CRACKED SUCCESSFULLY"** + actual password shown (e.g., `password1`)

### 8️⃣ Unlock the PDF
🔑 Open `My Locked PDF1.pdf` → enter cracked password → 🔓 Done!

---

## 💡 Key Concepts

| Concept | Meaning |
|---------|---------|
| 🔄 **Encryption** | Two-way — encrypted data can be decrypted with the right key |
| 🔒 **Hashing** | One-way — scrambles text into a unique digest; cracking tools guess & compare hashes |
| ⚡ **Weak passwords** | Can be cracked in seconds/minutes (e.g., `password1`) |
| 🛡️ **Strong passwords** | Long + mixed characters can take years to crack |

---

## ⚠️ Good Practice Reminder
This lab is for **learning & authorized testing only**. Always get proper permission before testing password security on any file or system that isn't your own. 🙏

---

*📚 Lab Source: Networkwalks Training Academy — www.networkwalks.com*
