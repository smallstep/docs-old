---
layout: auto-doc
title: step crypto key public
menu:
  docs:
    parent: step crypto key
---

## Name
**step crypto key public** -- print the public key from a private key

## Usage

```raw
step crypto key public <key-file> [--out=<path>]
```

## Description

**step crypto key public** prints or writes in a PEM format
the public key corresponding to the given `key-file`.

## Positional arguments

`key-file`
Path to a private key.

## Options


**--out**=`value`
Path to write the public key.

**-f**, **--force**
Force the overwrite of files without asking.

## Examples

Print the corresponding public key:
```shell
$ step crypto key public priv.pem
```

Write the corresponding public key to a file:
```shell
$ step crypto key public --out pub.pem key.pem
```

