
dragon-aosp-oreo
===========

To initialize your local repository use a command like this:
````bash
repo init -u https://android.googlesource.com/platform/manifest -b android-8.1.0_r10
````
Then you need to clone the local_manifest:
````bash
git clone https://github.com/followmsi/manifests.git
git checkout origin/dragon-aosp-oreo
````

Pls copy the "local_manifests" folder into your "./repo" folder inside your build tree.
Like below ...

````bash
~/root-of-your-build-tree/.repo$ ll
total 76
drwxrwxr-x  8 followmsi followmsi  4096 Feb 28 20:35 ./
drwxrwxr-x 31 followmsi followmsi  4096 Mar  1 09:21 ../
drwxrwxr-x  2 followmsi followmsi  4096 Mar  3 18:47 local_manifests/
drwxrwxr-x  3 followmsi followmsi  4096 Feb 28 20:33 manifests/
drwxrwxr-x 10 followmsi followmsi  4096 Feb 28 20:34 manifests.git/
lrwxrwxrwx  1 followmsi followmsi    21 Feb 28 20:33 manifest.xml -> manifests/default.xml
-rw-rw-r--  1 followmsi followmsi 11508 Feb 28 23:02 project.list
drwxrwxr-x 18 followmsi followmsi  4096 Feb 28 21:49 project-objects/
drwxrwxr-x 31 followmsi followmsi  4096 Feb 28 22:01 projects/
drwxrwxr-x  7 followmsi followmsi  4096 Feb 28 18:02 repo/
-rw-rw-r--  1 followmsi followmsi 29667 Feb 28 23:02 .repo_fetchtimes.json
````

Then to sync up:
````bash
repo sync
````
Finally to build:
````bash
. build/envsetup.sh
lunch aosp_dragon-userdebug
make -j8 otapackage
````
