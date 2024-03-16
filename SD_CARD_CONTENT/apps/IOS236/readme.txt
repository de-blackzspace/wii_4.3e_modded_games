IOS236 Installer/Uninstaller v3.2

This application is a simplification of Trucha Bug Restorer.
It installs a patched IOS36 into the IOS236 slot.
It must be launched using the AHBPROT method, so will only
work with HBC 1.0.7 or higher. The meta.xml file is VERY important!

To install, simply copy the IOS236 directory and its contents
to your apps directory on your SD card or USB drive.  Thus,
you will have sd:/apps/IOS236/boot.dol as one of the files.

While this installation should be safe, it does install stuff
to your Wii's NAND. Do not use it if potential for power
outages occur as it could brick your system.  

Version history:

v3.2 (by PabloACZ):
- Deleted unnecessary code from the Makefile (some libraries, like libmodplay and libmad. Seriously, the app is not
  going to play music, :P), and changed the loaded program to wiiload.
- Compiled with differents rvl.ld and iospatch.c/h (now named RuntimeIOSPatch.c/h) files (both from R2-D2199's Trucha Bug
  Restorer AHBPROT MOD), and corrected some minor things on main.c (to try to prevent code dumps).

v3.1 (by PabloACZ):
- Deleted the jokes about piracy stuff, including the "steps" and the A/B/X/Y button prompt.
- Added more detailed output.
- Added an uninstallation and exit options at startup.

v3:
- Another change to avoid DSI errors.
- Changed buttons needed at Step 2.

v2:
- A few changes to avoid DSI errors.
- Changed version number of installed IOS236 to 65535.

v1:
- Initial release.

This application was based on Trucha Bug Restorer by WiiPower
and also used the iospatch code from FTPii
TBR was based on PatchMii by bushing, svpe and tona
and also contains code from:
Raven's Menu Loader Clone (IOS selection code)
Waninkoko's WAD Manager (WAD code)
AnyTitleDeleter (TITLE_UPPER and TITLE_LOWER)