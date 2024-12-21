# Plymouth theme - Lindbergh Loader Boot Image

This is a theme for plymouth which only displays Lindbergh Loader boot image

Any Plymouth theme that you use needs to be installed in /usr/share/plymouth/themes.

After you have the Plymouth theme installed into the directory, you will need to add the theme to the default.plymouth. To add the theme you add it like so:

sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/lindbergh/lindbergh.plymouth 100

Then you run the --config option so that you can choose the new Plymouth theme:

sudo update-alternatives --config default.plymouth

Now you should see the new theme and you can choose it:

After you have it chosen, you should now update your initramfs:

sudo update-initramfs -u

Reboot the system to see the new changes
