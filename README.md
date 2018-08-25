OpenWRT configuration
=====================

This is my OpenWRT configuration. At the moment, this works a Linksys WRT1900ac v2.0 and a Linksys WRT610N v1.0 router.

## Installation

First, run this command from your machine to set your private `fti/xxxxxxx` credentials (make sure to replace your own value):

```shell
$ export CLEARTEXT_FTI=fti/xxxxxxx
```

Depending on which router you want to configure (`wrt1900acv2` or `wrt610n`), run the following command from your own machine:

```shell
$ ./install -r wrt1900acv2
```
