### 1. Review `keygenme-trial.py` to get trial username "BENNETT"
```python
username_trial = "BENNETT"
bUsername_trial = b"BENNETT"
```

### 2. Generate SHA256 hex digest of the byte string b"BENNETT"

### 3. Map the indices from the `check_key` function
- 4, 5, 3, 6, 2, 7, 1, 8

<details>

```python
def check_key(key, username_trial):

    global key_full_template_trial

    if len(key) != len(key_full_template_trial):
        return False
    else:
        # Check static base key part --v
        i = 0
        for c in key_part_static1_trial:
            if key[i] != c:
                return False

            i += 1

        # TODO : test performance on toolbox container
        # Check dynamic part --v
        if key[i] != hashlib.sha256(username_trial).hexdigest()[4]:
            return False
        else:
            i += 1

        if key[i] != hashlib.sha256(username_trial).hexdigest()[5]:
            return False
        else:
            i += 1

        if key[i] != hashlib.sha256(username_trial).hexdigest()[3]:
            return False
        else:
            i += 1

        if key[i] != hashlib.sha256(username_trial).hexdigest()[6]:
            return False
        else:
            i += 1

        if key[i] != hashlib.sha256(username_trial).hexdigest()[2]:
            return False
        else:
            i += 1

        if key[i] != hashlib.sha256(username_trial).hexdigest()[7]:
            return False
        else:
            i += 1

        if key[i] != hashlib.sha256(username_trial).hexdigest()[1]:
            return False
        else:
            i += 1

        if key[i] != hashlib.sha256(username_trial).hexdigest()[8]:
            return False

        return True
```
</details>

### 4. Decrypt with `keygenme.py` file

```python
import hashlib
username = b"BENNETT"
hash_val = hashlib.sha256(username).hexdigest()
print(f"Full Hash: {hash_val}")

# Build the dynamic part using the indices from the check_key function:
indices = [4, 5, 3, 6, 2, 7, 1, 8]
dynamic_part = "".join([hash_val[i] for i in indices])
print(f"Dynamic Part: {dynamic_part}")
```

### 5. Construct the key from the global static parts, adding dynamic component
```python
key_part_static1_trial = "picoCTF{1n_7h3_kk3y_of_"
key_part_dynamic1_trial = "xxxxxxxx"
key_part_static2_trial = "}"
```

### 6. Run `python keygenme-trial.py` and enter composite license key for Full version
