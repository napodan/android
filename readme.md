Known issues :
- FC in Browser with some web site (bug in the last webkit)
- Contacts unusuable (you need 3rd party to manage contacts)

Don't use this branch : I rebase it very very...very often

Getting the oxygen sources :

repo init -u git://github.com/napodan/android -b oxygen_1007

You will got an error message :

fatal: manifest 'default.xml' not available

fatal: remote aosp not defined in .../.repo/manifests/default.xml


ln -s manifests/local_manifests .repo/

repo init -u git://github.com/napodan/android -b oxygen_1007

(You must have no error)



repo sync


Building the oxygen rom :

. build/envsetup.sh

build

If you want to use mirror instead of server, replace :

ln -s .repo/manifests/local_manifests .repo/ by

cp -r .repo/manifests/local_manifests .repo/


and modify the file .repo/local_manifests/remote.xml

