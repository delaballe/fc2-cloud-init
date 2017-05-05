fcu-cloud-init
==============


This is a fork of Canonical cloud-init that can be found at :

  - https://git.launchpad.net/cloud-init

it has been patched to work out of the box in the Outscale® Cloud Platform.

[![Ubuntu Cloud-Init Technology](https://github.com/delaballe/fcu-cloud-init/raw/master/img/video.png)](https://www.youtube.com/watch?v=-zL3BdbKyGY)

## Install

```bash
git clone https://github.com/delaballe/fcu-cloud-init
cd fc2-cloud-init
python setup.py install --init-system systemd
```

or the line bellow in your project's pip requirement.txt

```
-e git+https://github.com/delaballe/fcu-cloud-init.git
```

and then run

```
pip install -r requirement.txt
``` 

## Test


```bash
rm -rf /var/lib/cloud/instance && rm -rf /var/lib/cloud/instances/* && rm -rf /var/lib/cloud/sem/*
cloud-init init && cloud-init modules --mode config && cloud-init modules --mode final
```
