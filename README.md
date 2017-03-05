
deb-aosp-nougat
===========

To initialize your local repository use a command like this:
````bash
repo init -u git://github.com/followmsi/manifests.git -b deb-aosp-nougat
````
Then to sync up:
````bash
repo sync
````
Finally to build:
````bash
. build/envsetup.sh
lunch                 -> (device number)
make -j8 otapackage
````
