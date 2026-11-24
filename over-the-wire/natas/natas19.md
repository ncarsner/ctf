**Exploit (19 -> 20):** Decode PHPSESSID cookie, learn its format, then brute force loop.

**Flaw:** Encoding as encryption. PHPSESSID hex decodes to <n>-<username>. Appears encrypted, but is merely obfuscated.

**Tooling:** `curl`, `xxd -r -p`, shell script to decode and iterate.
