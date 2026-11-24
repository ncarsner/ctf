**Exploit (21 -> 22):** Inject session key to HTML form on colocated url, reload to confirm request body, copy PHPSESSID to entry point url, reload as admin.

**Flaw:** No key whitelist. Cross-app session sharing. Lack of trust boundaries.

**Tooling:** DevTools, form manipulation, copied SESSID.
