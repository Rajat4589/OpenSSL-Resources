## OpenSSL Installation

### Procedure 1:

``1. sudo wget http://www.openssl.org/source/openssl-1.0.1g.tar.gz``

``2. sudo tar -xvzf openssl-1.0.1g.tar.gz``

``3. cd openssl-1.0.1g``

``4. sudo ./config --prefix=/usr/local/openssl --openssldir=/usr/local/openssl``

``5. sudo make depend``

``6. sudo make``

``7. sudo make install``

### Procedure 2:

``1. sudo apt-get install openssl``


## References:

1. https://geeksww.com/tutorials/libraries/openssl/installation/installing_openssl_on_ubuntu_linux.php
