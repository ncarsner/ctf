**Exploit (25 -> 26):** Calibrate directory hop count using `?lang=....//` until `/etc/passwd` reveals itself at root. Poison session log by sending PHP as User-Agent header. Confirm poisoned log view with `?lang=....//logs/natas25_<PHPSESSID>.log` path. Resend request, acquire password from PHP written to session log.

**Flaw:** Log poisoning, local file inclusion. Directory traversal and substring checks subverted by passing `....//` into request, defeating the `str_replace` filter, submitting script as User-Agent header to poison log.

**Tooling:** DevTools, User-Agent header mod and resend. Response body view.
