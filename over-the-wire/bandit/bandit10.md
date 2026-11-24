**Level goal:** The password for the next level is stored in the file `data.txt`, which contains base64 encoded data.

**Exploit (10 -> 11):** Verify file data type. Get `strings` from the file. Decode `base64` encoded string in the file.

**Flaw:** Encoding is not encryption.