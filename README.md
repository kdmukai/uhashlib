# Hash functions for Bitcoin

Originally from https://github.com/diybitcoinhardware/f469-disco/tree/master/usermods/uhashlib

---

extends `hashlib` micropython module with `ripemd160` and `sha512` functions.

Also adds a single-line function for pbkdf2_hmac:

`pbkdf2_hmac(hash_name, password, salt, iterations, bytes_to_read)`

in Bitcoin to generate a seed:

`pbkdf2_hmac('sha512', mnemonic, 'mnemonic'+password, 2048, 64)`

## TODO:

- make API the same as in normal python
- make C-optimized `hmac` and `pbkdf2` versions with standard python API