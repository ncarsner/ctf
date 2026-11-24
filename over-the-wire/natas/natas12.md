**Exploit (12 -> 13):** Hidden filename edited from `.jpg` to `.php`, uploaded `php` payload.

**Flaw:** File upload accepts and preserves the file extension blindly, client side manipulation provides the return path, which the server executes. No allowlist restrictions to image types only. No directory containment: allows client-side manipulation of file type (extension).

**Tooling:** DevTools, edit hidden filename to `php`, `curl` to execute the uploaded shell.
