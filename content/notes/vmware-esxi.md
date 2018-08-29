---
title: vmware esxi
---

# sata pass through

```
export DRIVE=/vmfs/devices/disks/naa.50014ee2b687de02
export SERIAL=unknown

vmkfstools -z $DRIVE /vmfs/volumes/5b86eeca-c8414b34-e1db-74867ade692a/nas/nas-disk-$SERIAL.vmdk
```
