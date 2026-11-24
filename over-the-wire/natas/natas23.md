**Exploit (23 -> 24):** Password requires two components: substring of 'iloveyou' and value > 10. Leading digits satisfy numeric check.

**Flaw:** Type juggling. Loose comparison casts the numeric string to its integer value.

**Tooling:** View page source, submit any number > 10 + `iloveyou` in userform, in that order.
