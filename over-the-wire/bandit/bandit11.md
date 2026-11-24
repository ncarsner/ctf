**Level goal:** The password for the next level is stored in the file `data.txt`, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.

**Exploit (11 -> 12):** ROT13 cipher encoding exploit. Small file size, and file only contains strings. `rot13` doesn't exist. Rotate letters manually by 13 places.

```bash
cat encrypted_file.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

**Flaw:** Encoding, especially with a known cipher mechanism, is still not encryption.