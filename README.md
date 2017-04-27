# twrp_samsung_young23g
Device configuration for Samsung Galaxy young23g

OMNIROM IS RECOMMENDED

Setup your envinroment first
copy this configuration into /sourcedir/device/here

Than run comannd in terminal from your working dir

        . build/envsetup.sh
        lunch twrp_vivalto3gvn-userdebug
        make recoveryimage

Your build will start and you will find your recovery. img in
your working dir/out/target/product/young23g

To make it flashable via ODIN you have to make it recovery.tar.md5
Navigate with terminal where your recovey.img is.
For example cd android/out/target/product/young23g
where android is name of your working dir
and run comands:

        tar -H ustar -c recovery.img > recovery.tar
        md5sum -t recovery.tar >> recovery.tar
        mv recovery.tar recovery.tar.md5
        
An now you got recovery.tar.md5 ready to be flashed usin ODIN selected as PDA file

Happy building.




