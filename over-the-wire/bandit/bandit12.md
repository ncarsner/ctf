**Level goal:** The password for the next level is stored in the file `data.txt`, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under `/tmp` in which you can work. Use `mkdir` with a hard to guess directory name. Or better, use the command `mktemp -d`. Then copy the datafile using `cp`, and rename it using `mv`.

**Exploit (12 -> 13):** Layered decompression. Check `data.txt` file type, create a tmp dir, `cp` `data.txt` into tmp dir, and examine the hexdump content. Reverse `data2.bin` to bytes and examine file type, then peel back the layers. The cycle is:
- gzip -> `.gz` + `gunzip`;
- bzip2 -> `.bz2` + `bunzip2`;
- tar -> `tar xf` then `ls`;
- Always `file` after

Labor intensive when doing by hand. The process can be more easily configured into a [shell script](https://github.com/ncarsner/offensivesecurity/blob/main/hexdump-unwrap.sh) with conditional variables for intelligent unwrapping.
