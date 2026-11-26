### Living Off the Land

- Starting with the remedial `Printer Shares` level, `admin` was leftover as a default password, allowing list view of devices on the port for the address.
- On level 2, `admin` is still leftover as a default password, allowing view of shares and `secure-shares` on the network port.
- `content.txt` and `kafka.txt` have no significant content, but `notification.txt` identifies user `Joe`. Joe’s password is easily cracked with a brute force attack tool, producing the password to acquire the flag within the `secure-shares` subdirectory.
- Level 3 shows us a `script.sh` and `cron.log` file, which are running a health check every minute. Get the files and append a command to the script to `cat` the flag file’s content.
- Download again after it executed again (~1 minute), which provides the flag.

**Flaw:** Default passwords, lack of access control, and improper file execution permissions.