**Exploit (4 -> 5):** `curl` the `natas4` site using `natas5` as the Referer.

**Flaw:** Access control is dependent on the client-side header, which can be synthesized.

**Tooling:** `curl -s -u natas4:<pw> -H "Referer: <natas5>" <natas4>`
