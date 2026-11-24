**Exploit (15 -> 16):** Manually probe with `natas16" AND password LIKE BINARY "[char]%` until "This user exists" is returned.

**Flaw:** Blind SQL injection. Determinable with shell script, iterating through characters until username/password returns true value for 32 character password.

**Tooling:** shell script, boolean-blind `LIKE BINARY "{}%"` sweep
