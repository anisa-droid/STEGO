# Stego: A Secure and Adaptive Image Steganography System

The idea:
- hide secret messages inside images
- encrypt the message before hiding it
- recover it later using a decryption key

Still improving it gradually. Current build is around the “May → June update” phase.

---

## Changelog for v1.051 

Fixed issues:

  - Windows 11 native file dialogs (PowerShell WinForms — reliable on all Win10/11 builds)
  - Key copy bug fixed (tk.Text widget, no null-char, no trailing newline)
  - Encryption/decryption runs in background thread — UI stays responsive

Added:

  - Drag-n-Drop feature for Encode/Decode page
  - Native OS notifications (Win32 MessageBox / notify-send / zenity / kdialog)
  - PBKDF2-HMAC-SHA256 key derivation (100,000 iterations) — token is 16-byte salt
  - True 2-LSB steganography — output image is *almost* same size as input
  - Share button: image → OS share sheet / bluetooth / email / file manager
  - Save-as-txt for the decryption key token

---
## Current Features

- AES-based encryption using Fernet
- Message embedding inside images
- GUI application using Tkinter
- Native file picker support
- Encode / Decode workflow
- Secret key generation
- Save encrypted image anywhere locally
- Cross-platform file dialog support (Linux/Windows/macOS)

---

## Tech Stack

- Python
- OpenCV (`cv2`)
- Tkinter
- Cryptography (Fernet)
- NumPy
- Pillow

---

## Project Status

Working prototype.

Main functionality works properly:
- encryption
- embedding
- extraction
- decryption

Still refining:
- embedding algorithm
- error handling
- optimization
- better steganography techniques

---

## Important Note

Current implementation is more focused on:
- learning
- functionality
- workflow

than perfect steganographic stealth.

---

## Installation

Clone the repo:

```bash
git clone https://github.com/anisa-droid/STEGO.git
```

Install dependencies:

```bash
pip install opencv-python cryptography numpy pillow
```

Run:

```bash
python stego_v1.051.py
```

---

## How it Works

### Encryption Flow

```text
Message
   ↓
Fernet Encryption
   ↓
Base64 Encoding
   ↓
Embedded into Image Pixels
   ↓
Encrypted Image Output
```

### Decryption Flow

```text
Encrypted Image
   ↓
Extract Embedded Data
   ↓
Base64 Decode
   ↓
Fernet Decryption
   ↓
Original Message
```

---

## Screenshots
### Homescreen
<img width="651" height="633" alt="image" src="https://github.com/user-attachments/assets/db8931d1-99d8-44c2-a243-9ea21d4eb6b1" />


### Encode Image - Screen
<img width="651" height="649" alt="image" src="https://github.com/user-attachments/assets/13c43868-6802-48ce-bb8b-ef4117eab594" />


### Decode Image - Screen
<img width="693" height="625" alt="image" src="https://github.com/user-attachments/assets/bd293602-50e0-4719-925b-111a83221ee0" />


---

## Future Plans

- Executable build
- Audio/Video input support
- Histogram
- Better Stealth and Detection Focused features

---
