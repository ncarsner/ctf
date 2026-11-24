**Exploit (13 -> 14):** Altered previous PHP payload satisfies `exif_imagetype` function. Subsequent payload passed through.

**Flaw:** Polyglot/magic bytes prepended to file bypassed the file type check.

**Tooling:** `GIF89a` prepended to PHP payload.

```bash
sed -i '1s/^/GIF89a\n/' <file.php>      # Linux / GNU
```
```bash
sed -i '' '1s/^/GIF89a\n/' <file.php>   # MacOS / BSD
```