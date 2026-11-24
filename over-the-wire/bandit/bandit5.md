**Level goal:** The password for the next level is stored in a file somewhere under the `inhere` directory and has all of the following properties:
- human-readable
- 1033 bytes in size
- not executable

**Exploit (5 -> 6):** Read `man find` and use recursive `find` looking for n-byte size, non-executable files, combining into one command. Reading `file2` within `maybehere07` subdirectory reveals the payload.

**Flaw:** File attribute/metadata crawl. This can be piped to the `cat` command to get the result directly from the validated `find` command.
