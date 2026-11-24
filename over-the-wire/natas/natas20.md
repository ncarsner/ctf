**Exploit (20 -> 21):** Submit manipulated user input `<name>\nadmin 1`. Get PHPSESSID from cookie file, reload to escalate.

**Flaw:** Unsanitized user input poisons session file.

**Tooling:** `<name>\nadmin 1`, `curl`, `grep`
