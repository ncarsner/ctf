**Level goal:** There are 2 files in the home directory. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new.

**Exploit (17 -> 18):** Review the directory files, and identify the `diff` between `passwords.old` and `passwords.new`.

**Flaw:** Change detection. Plaintext credentials.