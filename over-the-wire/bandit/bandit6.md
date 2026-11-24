**Level goal:** The password for the next level is stored somewhere on the server and has all of the following properties:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

**Exploit (6 -> 7):** Search by ownership through file system, since there is nothing in the home directory. `cd /` and searching returns multiple ```Permissions denied``` or ```No such file or directory``` except one line. Suppress noise by redirecting `stderr`.
```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

**Flaw:** No access control.