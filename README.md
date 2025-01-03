# Compression Support for TLSv1.3
> [!WARNING]
> This is only a PoC for whether it is possible to add compression support into
> TLSv1.3. Use this at your own risk only if you understand the security
> implication of compression in TLS. See [CRIME -
> Wikipedia](https://en.wikipedia.org/wiki/CRIME) for example.

## Usage
1. Clone OpenSSL
```sh
$ git clone https://github.com/openssl/openssl.git
$ cd openssl
```

2. Apply the patch
```sh
$ git apply ../openssl-tlsv1.3-compression.patch
```

3. Build OpenSSL with compression support
```sh
$ ./config enable-zlib
$ make -j
```
