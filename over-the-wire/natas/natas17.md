**Exploit (17 -> 18):** Same as natas15, except `echo` responses do not exist. Evaluate with timing of responses.

**Flaw:** Time-based blind SQL injection. Inferred via sleep timing.

**Tooling:** shell script, measure with `curl -o /dev/null -w '%{time_total}'`
