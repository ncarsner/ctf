### Nano permissions

- The `flag.txt` file is visible in the directory, but permissions are limited to the root user.
- `sudo -l` displays default permissions for current users, which includes nano within `/etc/sudoers`.
- Nano can read another file, and with `sudo` permissions within this context, the content of `flag.txt` can now be read within nano, producing the flag.

_Note: This is quintessential Broken Access Control, a persistent OWASP Top 10 vulnerability._