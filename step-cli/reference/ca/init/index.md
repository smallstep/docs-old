---
layout: auto-doc
title: step ca init
menu:
  docs:
    parent: step ca
---

## Name
**step ca init** -- initialize the CA PKI

## Usage

```raw
step ca init
[--root=<path>] [--key=<path>] [--pki] [--ssh] [--name=<name>]
[--dns=<dns>] [--address=<address>] [--provisioner=<name>]
[--provisioner-password-file=<path>] [--password-file=<path>]
[--with-ca-url=<url>] [--no-db]
```

## Description

**step ca init** command initializes a public key infrastructure (PKI) to be
 used by the Certificate Authority.

## Options


**--root**=`file`
The path of an existing PEM `file` to be used as the root certificate authority.

**--key**=`file`
The path of an existing key `file` of the root certificate authority.

**--pki**
Generate only the PKI without the CA configuration.

**--ssh**
Create keys to sign SSH certificates.

**--name**=`name`
The `name` of the new PKI.

**--dns**=`names`
The comma separated DNS `names` or IP addresses of the new CA.

**--address**=`address`
The `address` that the new CA will listen at.

**--provisioner**=`name`
The `name` of the first provisioner.

**--password-file**=`file`
The path to the `file` containing the password to encrypt the keys.

**--provisioner-password-file**=`file`
The path to the `file` containing the password to encrypt the provisioner key.

**--with-ca-url**=`URI`
`URI` of the Step Certificate Authority to write in defaults.json

**--ra**=`name`
The registration authority `name` to use. Currently only "CloudCAS" is supported.

**--issuer**=`name`
The registration authority issuer `name` to use.

If CloudCAS is used, this flag should be the resource name of the
intermediate certificate to use. This has the format
'projects/\*/locations/\*/certificateAuthorities/\*'.

**--credentials-file**=`file`
The registration authority credentials `file` to use.

If CloudCAS is used, this flag should be the path to a service account key.
It can also be set using the 'GOOGLE_APPLICATION_CREDENTIALS=path'
environment variable or the default service account in an instance in Google
Cloud.

**--no-db**
Generate a CA configuration without the DB stanza. No persistence layer.

