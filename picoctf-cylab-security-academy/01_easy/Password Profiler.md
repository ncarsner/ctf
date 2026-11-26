### Three files:
- `userinfo.txt`
    - contains personal details about the user
- `hash.txt`
    - contains the SHA-1 hash of the user’s password; and
- `check_password.py`
    - a Python script that reads from `hash.txt` and
`passwords.txt` - a text file containing a lengthy list of potential passwords.

### Download `cupp.py` and `cupp.cfg` files from a Github repo using `wget`
- `cupp.py` generates several thousand potential passwords based on user details provided in the `userinfo.txt` file.
- The `cupp.py` file must be run in interactive mode so user details can be entered when asked by the script
- Rename the rendered file to `passwords.txt` for the
`check_password.py` script to work and produce the flag.