Getting the oxygen sources :

repo init -u git://github.com/napodan/android -b oxygen_4.3

You will got an error message :

fatal: manifest 'default.xml' not available

fatal: remote aosp not defined in .../.repo/manifests/default.xml


ln -s manifests/local_manifests .repo/

repo init -u git://github.com/napodan/android -b oxygen_4.3

(You must have no error)



repo sync


Building the oxygen rom :

. build/envsetup.sh

build

If you want to use mirror instead of server, replace :

ln -s .repo/manifests/local_manifests .repo/ by

cp -r .repo/manifests/local_manifests .repo/


and modify the file .repo/local_manifests/remote.xml

