**Exploit (18 -> 19):** Brute force PHPSESSID incrementally.

**Flaw:** Trusted client input: Session ID'd by cookie within a known range.

**Tooling:** shell script to iterate `PHPSESSID` values until valid creds received.
