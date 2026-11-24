**Exploit (7 -> 8):** Appended the subdirectory in the comment to the page target, revealing the password.

**Flaw:** Unsanitized user input, local file inclusion, no allowlist protocols. Path traversal attack target.

**Tooling:** `curl` target url appended with `?page=/etc/natas_webpass/natas8`.
