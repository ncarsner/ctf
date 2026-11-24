**Level goal:** The password for the next level is stored in the file `data.txt` in one of the few human-readable strings, preceded by several `=` characters.

**Exploit (9 -> 10):** Printable string extraction. Simple `grep` command informs that this file contains content more that just text. Verify file type, determine `strings` in the file, and then `grep` against those strings.

```bash
strings data.txt | grep '^='
```