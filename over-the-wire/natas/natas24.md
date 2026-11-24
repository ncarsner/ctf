**Exploit (24 -> 25):** Convert `passwd` to an array with square brackets. `strcmp` returns literal `NULL` value, satisfying `!strcmp` gate.

**Flaw:** `strcmp()` misuse. Type handling bug. Comparison function never completes.

**Tooling:** Append `/index.php?passwd[]=<anything>` to url.
