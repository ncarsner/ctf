**Level goal:** The password for the next level is stored in a file `readme` in the homedirectory. Unfortunately, someone has modified `.bashrc` to log you out when you log in with SSH.

**Exploit (18 -> 19):** Login kicks out immediately, so interactivity must trigger the control. Appending a `cat` command returns the credentials.

**Flaw:** Shell init bypass.