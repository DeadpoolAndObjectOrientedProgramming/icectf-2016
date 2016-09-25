# IceCTF 2016 : RSA

**Category:** Cryptography
**Points:** 60
**Solves:** 417
**Description:**

DESCRIPTION

## Write-up

First we convert `N` and `d` to decimal by simply opening a python shell and copy/pasting the `0x..` value in. Python spits out the decimal value for us to use with [rsatool.py](https://github.com/ius/rsatool)

```
python rsatool.py -n 432... -d 367... -f PEM -o private.pem
```

giving us a private key. Now we just need to use they private key to decrypt the message. The following python script reads in the private RSA key and decrypts the message

```python
from Crypto.PublicKey import RSA 
from binascii import unhexlify

def long_to_bytes (val):
    width = val.bit_length()
    width += 8 - ((width % 8) or 8)
    fmt = '%%0%dx' % (width // 4)
    s = unhexlify(fmt % val)
    return s

c = 0x126c24e146ae36d203bef21fcd88fdeefff50375434f64052c5473ed2d5d2e7ac376707d76601840c6aa9af27df6845733b9e53982a8f8119c455c9c3d5df1488721194a8392b8a97ce6e783e4ca3b715918041465bb2132a1d22f5ae29dd2526093aa505fcb689d8df5780fa1748ea4d632caed82ca923758eb60c3947d2261c17f3a19d276c2054b6bf87dcd0c46acf79bff2947e1294a6131a7d8c786bed4a1c0b92a4dd457e54df577fb625ee394ea92b992a2c22e3603bf4568b53cceb451e5daca52c4e7bea7f20dd9075ccfd0af97f931c0703ba8d1a7e00bb010437bb4397ae802750875ae19297a7d8e1a0a367a2d6d9dd03a47d404b36d7defe8469

key = open('private.pem', 'r').read() 
rsakey = RSA.importKey(key)
print rsakey.decrypt(long_to_bytes(c))
```

giving us the flag

![flag](https://cloud.githubusercontent.com/assets/3537289/17644239/c8fd6920-6170-11e6-8373-e6057d6490bb.png)

See [#29](https://github.com/ikornaselur/project-firewater/issues/29)
