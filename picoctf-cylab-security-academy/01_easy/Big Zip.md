### 1. Download zip file
```bash
wget "https://artifacts.picoctf.net/c/505/big-zip-files.zip"
```

### 2. Unzip file
```bash
unzip big-zip-files.zip
```

### 3. Search recursively from `pwd`, exit at first match
```bash
grep -r -m 1 "<flag_prefix>" .
```

Prefix was _"pico"_, now is _"academy"_
