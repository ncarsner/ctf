**Level goal:** The password for the next level is stored in a file called `--spaces in this filename--` located in the home directory.

**Exploit (2 -> 3):** Same as previous level. File name contains spaces, but reading within quoted identifiers produces requisite output.

**Flaw:** Arg parsing abuse.
