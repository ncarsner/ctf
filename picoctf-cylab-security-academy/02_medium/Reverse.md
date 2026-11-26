### Binary strings

- Use the `strings` command on the binary to see if the string used in the `strcmp` is visible.
- Get the binary using `wget`, and the flag is readily visible. Even more visible with a combo argument:

```bash
strings ret | grep academy
```