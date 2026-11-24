**Exploit (2 -> 3):** Found `users.txt` file in the `files/` subdirectory, which is visible in the page source.

**Flaw:** Leaving sensitive file(s) in an auto-indexed `files/` path.

**Tooling:** browser, open the `files/` directory listing, read `users.txt`.
