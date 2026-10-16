# AES Communication System

Secure message communication using the Advanced Encryption Standard (AES) — a symmetric encryption algorithm widely used across the globe for securing sensitive data.

## Author

**Rajgopal Pandilwar**

## Based On Original Work By
## What is AES?

The Advanced Encryption Standard (AES) is a symmetric-key block cipher adopted by the U.S. government and now used worldwide. It supports key sizes of 128, 192, and 256 bits.

- **Block size:** 128 bits
- **Key sizes:** 128, 192, or 256 bits
- **Rounds:** 10, 12, or 14 (depending on key size)

## Project Structure

This project implements AES encryption and decryption for secure communication between parties.

## Dependencies

```bash
pip install pycryptodome
```

## Usage

```python
from Crypto.Cipher import AES
from Crypto.Random import get_random_bytes

key = get_random_bytes(16)  # 128-bit key
cipher = AES.new(key, AES.MODE_EAX)
nonce = cipher.nonce
ciphertext, tag = cipher.encrypt_and_digest(b"Secret message")
```
