**Exploit (11 -> 12):** Source code reveals decoding required to manipulate client-side cookie and resubmit to grant access. Decode cookie to raw bytes, XOR plaintext against ciphertext reveals the key.

**Flaw:** Known plaintext attack, XOR exploit, cookie tampering.

**Tooling:** shell script to decode cookie, recover and forge key
