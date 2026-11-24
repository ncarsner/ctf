### 1. Download four (4) files
- dictionary.txt _(65k 4-digit hexadecimal combinations)_
- level5.flag.txt.enc
- level5.hash.bin
- level5.py

### 2. Create `solve.py` for brute force password crack
```python
import hashlib

# 1. Load target hash
with open('level5.hash.bin', 'rb') as f:
    target_hash = f.read()

# 2. Iterate and check
with open('dictionary.txt', 'r') as f:
    for line in f:
        password = line.strip()
        # Compute MD5 and compare directly against the binary hash
        if hashlib.md5(password.encode()).digest() == target_hash:
            print(f"Password found: {password}")
            break
```

### 3. Execute `python solve.py`
