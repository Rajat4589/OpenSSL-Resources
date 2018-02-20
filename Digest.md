## Digest

**MD5 digest**

```
Method 1:
openssl dgst -md5 input.txt
```
```
Method 2: 
md5sum input.txt
```

**SHA1 digest**

```
Method 1: 
openssl dgst -sha1 filename
```

```
Method 2: 
sha1sum input.txt
```

**SHA256 digest**

``openssl dgst -sha256 filename``

**To generate and sign a digest** (it means encrypting digest using private key)

``openssl dgst -sha256 -sign private.pem -out input.sha1 input.txt``

**To verify signed digest** (it means decrypting digest using public key)

``openssl dgst -sha256 -verify pubkey.pem -signature input.sha1 input.txt``