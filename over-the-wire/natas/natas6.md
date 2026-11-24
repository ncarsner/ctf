**Exploit (6 -> 7):** Secret string is compared to content in `/includes/secret.inc` which is raw text leaked by the source code.

**Flaw:** Exposed source in PHP.

**Tooling:** `curl`, `POST` secret.inc
