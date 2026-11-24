**Exploit (10 -> 11):** A defined character array is prohibited with a regex (`preg`) function, but `.*` appends to `grep`, allowing a query against password directory.

**Flaw:** Command injection vulnerability, just limited characters.

**Tooling:** `.*` to read `/etc/`
