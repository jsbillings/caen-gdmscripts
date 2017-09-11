# caen-gdmscripts
Scripts aimed to handle multiple display delegration both pre and post login in RHEL 7

Due to a gdm issue in RHEL that results in warped login backgrounds on multiple displays and to correct default monitor arrangement, these scripts aim to detect the connected displays and disable the secondary monitor until a login is achieved at which point the PreSession script will reinitilize all displays according to established standards. 

This script's modifications WILL be overwritten by any custom monitors.xml file.

The benefit of this implementation is that it allows us to set the primary display system-wide rather than just for login, thus allowing us to customize this configuration to set other dual+ monitor stations, projectors, crestrons, etc. to use the desired display configuration. 

This also frees up the Nvidia-tearing fix from having to specify specific ports allowing it to work on all configurations out of the box.
