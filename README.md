# Secure Image Steganography 

The idea:
- hide secret messages inside images
- encrypt the message before hiding it
- recover it later using a decryption key

Still improving it gradually. Current build is around the “April → May update” phase.

---

## Changelog for v1.04 

Fixed issues:

  - Windows 11 native file dialogs (PowerShell WinForms — reliable on all Win10/11 builds)
  - Key copy bug fixed (tk.Text widget, no null-char, no trailing newline)
  - Encryption/decryption runs in background thread — UI stays responsive
  - All lambda-in-loop closure bugs fixed
Added:

  - Native OS notifications (Win32 MessageBox / notify-send / zenity / kdialog)
  - PBKDF2-HMAC-SHA256 key derivation (100,000 iterations) — token is 16-byte salt
  - True 2-LSB steganography — output image is *almost* same size as input
  - Share button: image → OS share sheet / bluetooth / email / file manager
  - Share + Save-as-txt for the decryption key token

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
- UI cleanup
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
git clone https://github.com/anisa-droid/Secure-Image-Steganography-Project.git
```

Install dependencies:

```bash
pip install opencv-python cryptography numpy pillow
```

Run:

```bash
python stego_gui_may_update_1.04.py
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

(Will be adding real soon)

---

## Future Plans

- Better image capacity handling
- Executable build
- Drag & drop support
- More secure key management

---
