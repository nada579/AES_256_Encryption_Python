# AES_256_Encryption_Python
📌 Encryption Project — Caesar Cipher + AES (GUI)



🔐 1) Caesar Cipher Program

✔ Description

A simple encryption program that uses the Caesar Cipher algorithm.
The user enters a text and a shift value, and the program performs:
	•	Encryption
	•	Decryption

The algorithm works by shifting each letter by a specific number of positions.

🧩 Features
	•	Supports both uppercase and lowercase letters
	•	Keeps numbers and symbols unchanged
	•	User chooses encryption or decryption
	•	Handles wrapping from Z → A

🧪 Example

Shift = 3
A → D
B → E

🔐 2) AES Encryption Program (GUI)

✔ Description

A Python GUI application built with Tkinter that performs:
	•	AES Encryption
	•	AES Decryption

It supports multiple AES modes:
	•	ECB
	•	CBC
	•	CFB
	•	OFB

Uses SHA-256 hashed password for key generation
and displays both ciphertext (Hex) and decrypted text.

🧩 Features
	•	Modern GUI design
	•	Multiple AES encryption modes
	•	Secure key generation using SHA-256
	•	Automatic padding/unpadding
	•	Easy input/output interface

🚀 Technologies Used
	•	Python
	•	Tkinter GUI
	•	PyCryptodome
	•	Hashlib
	•	ASCII operations

📂 Files Included
	•	caesar_cipher.py
	•	aes_gui.py
	•	README.md

📌 How to Run

Caesar Cipher

python caesar_cipher.py

AES GUI

python aes_gui.py

👩‍🏫 Project Goal

This project demonstrates the difference between:
	•	Simple encryption (Caesar Cipher)
	•	Strong modern encryption (AES)

and shows how GUI can be used to make encryption easier for users.

🎉 End of README.
