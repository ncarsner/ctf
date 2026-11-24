**Exploit (22 -> 23):** View sourcecode to id query parameter. Submit request with parameter, without following the `Location: /` redirect.

**Flaw:** PHP persists despite redirect, disclosing secret in body response.

**Tooling:** `curl -sS -u natas22:<pw> "<natas22>index.php?revelio" | grep -i password`. Eschew `-L` to avoid redirects.
