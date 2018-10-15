OpenWRT configuration
=====================

This is my OpenWRT configuration. At the moment, this works a Linksys WRT1900ac v2.0 and a Linksys WRT610N v1.0 router.

## Dependencies

This script needs [nagromc/openwrt-configuration-for-livebox](https://github.com/nagromc/openwrt-configuration-for-livebox) to work. First, to checkout this dependency, run

```shell-session
$ git submodule update --init --recursive
```

## Installation

First, run this command from your machine to set your private `fti/xxxxxxx` credentials (make sure to replace your own value):

```shell
$ export CLEARTEXT_FTI=fti/xxxxxxx
```

Depending on which router you want to configure (`wrt1900acv2` or `wrt610n`), run the following command from your own machine:

```shell
$ ./install wrt1900acv2
```

## References

The Internet connection part is based on this thread: [Remplacement de la Livebox par un routeur Openwrt 18+ (DHCP V4/V6 + TV)](https://lafibre.info/remplacer-livebox/remplacement-de-la-livebox-par-un-routeur-openwrt-18-dhcp-v4v6-tv/).
