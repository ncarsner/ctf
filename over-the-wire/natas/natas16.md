**Exploit (16 -> 17):** Characters filter does not include `$` which allows manipulating of interior `grep` args to see what values are returned by the outer `grep`.

**Flaw:** Side channel exploit. Blind command injection. Blocklist gap.

**Tooling:** Observability performed with shell script + payload `<word>$(grep ^<guess> /etc/...)` to iterate through guesses.
