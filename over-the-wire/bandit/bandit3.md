**Level goal:** The password for the next level is stored in a hidden file in the `inhere` directory.

**Exploit (3 -> 4):** `cd` into `inhere` folder. Although the filename appears to require directory traversal, the elipses are literal characters that are part of the file name. Viewing the entire file name reveals the material. Permissions that are readable by owner and group.

**Flaw:** Security via obscurity. Simple `grep` tools and lack of access control only hinder discovery; they do not prevent it. Intermediate, advanced, and malicious users can easily traverse directories for sensitive info if _'hiding the loot'_ is the only security measure in play.
