OpenWRT configuration
=====================

This is my OpenWRT configuration. At the moment, this works a Linksys WRT610N v1.0 router.

## Installation

First, run this command from your machine to set your private `fti/xxxxxxx` credentials (make sure to replace your own value):

```shell
$ ENCODED_FTI=$(echo -n 'fti/xxxxxxx' | xxd  -p)
```

Depending on which router you want to configure, run the following commands from your own machine making sure you point to the right file:

```shell
$ scp config.wrt1900acv2 root@192.168.1.1:/tmp/config \
    && ssh root@192.168.1.1 "cat /tmp/config | uci -m import network && uci commit" \
    && ssh root@192.168.1.1 "uci set network.wan.sendopts='0x4D:2b46535644534c5f6c697665626f782e496e7465726e65742e736f66746174686f6d652e4c697665626f7833 0x5a:0000000000000000000000$ENCODED_FTI' && uci commit"
```
