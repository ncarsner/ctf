**Exploit (3 -> 4):** Public advisory file `robots.txt` contains an unprotected path that leads to a `users.txt` file with the password.

**Flaw:** Security through obscurity. PAF requests omission from crawlers, but does not enforce the mechanism.

**Tooling:** browser, read `robots.txt`, open `/s3cr3t/users.txt`.
