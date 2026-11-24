**Level goal:** The password for the next level is stored in the only human-readable file in the `inhere` directory. _Tip:_ if your terminal is messed up, try the `reset` command.

**Exploit (4 -> 5):** Multiple similarly named files. Triaging by file type with `file ./-file*` determines which, if any, contain readable content. `file07`, which is ASCII text, is the winner.

**Flaw:** More security by obscurity.