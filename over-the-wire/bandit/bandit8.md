**Level goal:** The password for the next level is stored in the file `data.txt` and is the only line of text that occurs only once.

**Exploit (8 -> 9):** Frequency analysis/dedup content by piping a series of commands to identify the unique string that appears in the file.

```bash
sort data.txt | uniq -u
```
