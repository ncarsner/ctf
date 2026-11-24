**Exploit (14 -> 15):** Quoted identifier + logical true satisfied password requirement. Additional text following comment marker is ignored.

**Flaw:** SQL injection. User input is incorporated into non-parameterized query, allowing query logic to be rewritten.

**Tooling:** `" or 1=1 --`
