---
layout: auto-doc
title: step ssh inspect
menu:
  docs:
    parent: step ssh
---

## Name
**step ssh inspect** -- print the contents of an ssh certificate

## Usage

```raw
step ssh inspect <crt-file>
```

## Description

**step ssh inspect** command prints ssh certificate details in human readable
format.

## Positional arguments

`crt-file`
The path to an ssh certificate.

## Examples

Prints the contents of id_ecdsa-cert.pub:
```shell
$ step ssh inspect id_ecdsa-cert.pub
```
