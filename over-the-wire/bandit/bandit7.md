**Level goal:** The password for the next level is stored in the file `data.txt` next to the word millionth.

**Exploit (7 -> 8):** `data.txt` is a very large file that will flood `stdout`. Targeted search via `grep` locates the text efficiently.

```bash
grep millionth data.txt
```
