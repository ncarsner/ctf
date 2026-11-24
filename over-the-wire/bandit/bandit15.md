**Level goal:** The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

**Exploit (15 -> 16):** TLS-wrapped network service. The underlying weakness from before remains, although the tooling is different. Connecting within the client.

**Flaw:** Plaintext network credentials.