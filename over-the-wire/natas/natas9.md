**Exploit (9 -> 10):** Input key _(search parameter)_ is dropped unquoted into a shell. `; cat` terminates `grep` and returns the whole 50k-word dictionary.

**Flaw:** Command injection vulnerability. A fork bomb or similar exploit could be catastrophic if processed from raw user input.

**Tooling:** `;` and `cat` to read `/etc/`
