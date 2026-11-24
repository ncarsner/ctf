**Level goal:** To gain access to the next level, you should use the `setuid` binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place `/etc/bandit_pass`, after you have used the `setuid` binary.

**Exploit (19 -> 20):** Try executing the binary. Further examine binary permissions. `cat` the `/etc` directory and get the payload.

**Flaw:** Privilege escalation on `setuid`.