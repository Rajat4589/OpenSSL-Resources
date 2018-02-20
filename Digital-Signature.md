## Digital Signature

**To generate the digest of a file**

``openssl dgst -sha256 -out sign.sha256 input.txt``

**To generate the encrypted digest as signature using private key**

```
Method 1:
openssl dgst -sha256 -sign private.pem -out sign.sha256 input.txt
```

```
Method 2: 
openssl rsautl -sign -inkey private.pem -keyform PEM -in sign.sha256 > signature (sign.sha256 is the digest of input.txt)
```

**To convert signature to Base64 format**

``openssl base64 -in sign.sha256 -out signature``

**To convert signature to binary format**

``openssl base64 -d -in signature -out sign.sha256``

**To verify the signature**

```
Method 1: 
openssl dgst -sha256 -verify public.pem -signature sign.sha256 input.txt
```
```
Method 2: 
openssl rsautl -verify -inkey public.pem -keyform PEM -in signature input.txt
```