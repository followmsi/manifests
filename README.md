LineageOS Ultra Legacy
===========

Getting started
---------------

To get started with Android/LineageOS, you'll need to get familiar with [Source Control Tools](https://source.android.com/setup/develop).

To initialize your local repository using the LineageOS trees, use a command like this:
```
repo init -u https://github.com/followmsi/manifests.git -b flo-deb-lineage-19.1 --git-lfs
```
Then to sync up:
```
repo sync --force-sync
```
Please see the [LineageOS Wiki](https://wiki.lineageos.org/) for building instructions, by device.


Build
--------

```
source build/envsetup.sh

brunch flo
```

