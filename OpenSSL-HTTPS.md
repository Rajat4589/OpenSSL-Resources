## Create a simple HTTPS server with OenSSL ``s_server``

**New private key with certificate**

``openssl req -x509 -newkey rsa:2048 -keyout key.pem -out cert.pem -days 365 -nodes``

**Starting OpenSSL s_server**

``openssl s_server -key key.pem -cert cert.pem -accept 44330 -www``                   (^c to kill server)

**Accessing s_server through browser**

``https://localhost:44330``

**Accessing s_server through s_client**

``openssl s_client -connect localhost:44330``                                         (^c to kill client)

## Useful Commands

**To list all openssl process with port number and PID**

``sudo netstat -nlp | grep openssl``

**To kill process**

``sudo kill -9 PID``

## References:

1. [Website](https://blog.jorisvisscher.com/2015/07/22/create-a-simple-https-server-with-openssl-s_server/)
