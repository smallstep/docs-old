---
layout: auto-doc
title: step fileserver
menu:
  docs:
    parent: step
---

## Name
**step fileserver** -- start an HTTP(S) server serving the contents of a path

## Usage

```raw
step fileserver <dir>
[--address=<address>] [--cert=<path>] [--key=<path>]
```

## Description

**step fileserver** command starts an HTTP(S) server serving the contents of a file
system.

This command is experimental and only intended for test purposes.

## Positional arguments

`dir`
The directory used as root for the HTTP file server.

## Options


**--address**=`address`
The TCP `address` to listen on (e.g. ":8443").

**--cert**=`path`
The `path` to the TLS certificate to use.

**--key**=`path`
The `path` to the key corresponding to the certificate.

## Examples

Start an HTTP file server on port 8080.
```shell
$ step fileserver --address :8080 /path/to/root
```

Start an HTTPS file server on 127.0.0.1:8443.
```shell
$ step ca certificate 127.0.0.1 localhost.crt localhost.key
...
$ step fileserver --address 127.0.0.1:8443 \
  --cert localhost.crt --key localhost.key /path/to/root
```

