**Level goal:** The password for the next level is stored in a file called `-` located in the home directory.

**Exploit (1 -> 2):** Although not immediately obvious, `-` is a readable file, and has bandit2 permissions.

**Flaw:** Arg/option injection via filename, and no access control.
