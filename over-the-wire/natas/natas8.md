**Exploit (8 -> 9):** Source code contains the functions which creates the encodedSecret, which is also in the source code.

**Flaw:** Encoding is not encryption. Encoded answer and answer key coexist client-side.

**Tooling:** `echo <secret> | xxd -r -p | rev | base64 -d`
