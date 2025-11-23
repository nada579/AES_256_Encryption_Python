# AES_256_Encryption_Python
📌 Encryption Project — Caesar Cipher + AES (GUI)

## Description
This project contains Python implementations of *Caesar Cipher* and *AES encryption, including a **GUI for AES encryption/decryption* with multiple modes (ECB, CBC, CFB, OFB). It's a learning project to demonstrate classic and modern encryption techniques.

---

## 1️⃣ Caesar Cipher

*File:* caesar_cipher.py

*Description:*  
A simple substitution cipher where each letter in the plaintext is shifted by a fixed number of positions.

*Functions:*
- caesar_encrypt(text, shift) – Encrypts text by shifting letters forward.  
- caesar_decrypt(text, shift) – Decrypts text by shifting letters backward.  

*Usage Example:*
```python
# Encrypt
encrypted_text = caesar_encrypt("HELLO", 3)
print(encrypted_text)  # Output: KHOOR

# Decrypt
decrypted_text = caesar_decrypt(encrypted_text, 3)
print(decrypted_text)  # Output: HELLO

2️⃣ AES-128 Implementation (From Scratch)

File: aes_128.py

Description:
A full AES-128 implementation from scratch, including:
	•	Key Expansion
	•	SubBytes & ShiftRows
	•	MixColumns & AddRoundKey
	•	PKCS7 Padding

Functions:
	•	aes_encrypt_block(block, keys) – Encrypts a 16-byte block.
	•	aes_decrypt_block(block, keys) – Decrypts a 16-byte block.
	•	pad(data) / unpad(data) – For block alignment.
	•	key_expansion(key) – Expands a 16-byte key into 11 round keys.

Usage Example:

msg = "HELLO WORLD"
msg_bytes = pad(msg.encode())
key = b"\x2b\x7e\x15\x16\x28\xae\xd2\xa6\xab\xf7\x15\x88\x09\xcf\x4f\x3c"
keys = key_expansion(list(key))

# Encrypt
cipher_blocks = [aes_encrypt_block(msg_bytes[i:i+16], keys) for i in range(0, len(msg_bytes), 16)]
ciphertext = b"".join(cipher_blocks)

# Decrypt
plain_blocks = [aes_decrypt_block(ciphertext[i:i+16], keys) for i in range(0, len(ciphertext), 16)]
plaintext = unpad(b"".join(plain_blocks))
print(plaintext.decode())  # Output: HELLO WORLD

3️⃣ AES GUI (Tkinter + PyCryptodome)

File: aes_gui.py

Description:
A GUI for AES encryption/decryption supporting multiple modes: ECB, CBC, CFB, OFB. Uses SHA-256 hashed password as key and PKCS7 padding.

How it works:
	1.	User enters a message and a password.
	2.	Click on a mode button (e.g., ECB, CBC, CFB, OFB).
	3.	GUI displays encrypted text in hex and decrypted text.

Dependencies:

pip install pycryptodome

Usage:

python aes_gui.py

	•	Enter your message and password.
	•	Select the encryption mode to get the encrypted and decrypted outputs.

Notes
	•	Caesar Cipher is for educational purposes; AES provides secure encryption.
	•	The AES-from-scratch implementation is a learning tool; for production use, prefer PyCryptodome.

---
