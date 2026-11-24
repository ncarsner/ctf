**Level goal:** The password for the next level is stored in a file called `readme` located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

**Exploit (0 -> 1):** The password for bandit1 is stored in a world-readable file named `readme` in bandit0's home directory. `cat` it and read the contents.

**Flaw:** No access control.