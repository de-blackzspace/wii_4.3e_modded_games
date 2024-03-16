NeoGamma is a modification of WiiGator's Gamma backup loader, see "old readme.txt"


FILEPATHS:

Ocarina codes: "NeoGamma/codes" or "codes" 
gameconfig.txt: "NeoGamma/gameconfig.txt" or "gameconfig.txt" or "codes/gameconfig.txt"
.dols: "NeoGamma" (either 4 or 6 digits of the disc id)
Patches(.wip files): "NeoGamma" (either 4 or 6 digits of the disc id)
Menu files(.wdm files): "NeoGamma" (either 3, 4 or 6 digits of the disc id)
Config file: (sd card only) "NeoGamma/NeoGamma.cfg"




PROBLEMS PLAYING A CERTAIN GAME?

Try the following options:
Hooktype: none
Ocarina: no
Alternative .dol: disc+
Boot language: Console Default (2nd test on import games: one language used in the game)
Force Video: Disc
Patch Video: no
VIDTV Patch: no
Patch Country Strings: no (3rd test on import games: yes)

If you play from sd or usb, insert a disc.

If the game does not work with this, the game is not compatible or an IOS Reloading game, or it's a cIOS, media or new unknown problem.

If you get either color issues or a green screen freeze(with video mode != Disc), try different combinations of Force Video, Patch Video and VIDTV. Note that this issue can't be fixed in lots of games.






PROBLEMS WITH OCARINA?

Try the different hooktypes.





PROBLEMS WITH USB LOADING?

*New possible fix*
Insert any usb device in the top port while the HDD is inserted in the bottom port.

- NeoGamma is not able to load games from usb with rev12(maybe rev11 does not work too) of Waninkoko's cIOS
- Make sure you are using the bottom usb port, the top one won't work for HDDs from cIOSrev12 on.
- Also if you have WiiConnect24 enabled, test what happens if you disable it.
- If you have an IDE HDD, try both master and slave jumper settings(experts only!, very low chance to change something)

Try starting the loader after the HDD was connected and powered
Try starting the loader, connect and power the HD, and then selecct mount WBFS
Try starting the loader, select mount WBFS, connect the HDD, and then power it
Try starting the loader, select mount WBFS, power the HDD, and then connect it
Try starting the loader, select mount WBFS, wait until tries left 20, connect the HDD, and then power it
Try starting the loader, select mount WBFS, wait until tries left 20, power the HDD, and then connect it

If all this does not help, get:
http://wiibrew.org/wiki/GeeXboX
start something from the HDD with it(requires 2 partitons, 1 wbfs and 1 other),
don't do anything to the HDD, do not unplug,
exit to HBC, start NeoGamma and try to connect.

If GeeXboX is the only way for you to get your HDD working, please get in contact with the people at irc://irc.freenode.org/cIOS or me

And if even this does not work, try to get 2 partitions on the HDD:
1. FAT32 or NTFS
2. WBFS

And then try again, maybe try the GeeXboX trick again.





OPTIONS:

Hook Type:
ONLY ENABLE IF YOU NEED IT! Required for debugging and Ocarina, the different option can differently reduce game compatibilty.

Ocarina:
ONLY ENABLE IF YOU NEED IT! You can select which IOS to use to load the code file from storage.(only, if at all, required for sdhc cards)

Alternative .dol:
ONLY ENABLE IF YOU NEED IT! "Disc" searches the disc for .dols and let's you select which one to load then. It should be ovious that only using a .dol different from the main.dol makes sense here. "Storage" load a .dol from sd or usb storage instead of loading the main.dol from disc. The .dol has to be in the folder 'NeoGamma' and the name has to be the first 6(or 4) characters of the disc id.

Boot Language:
Option which language to force. "Console Default" forces nothing, "Auto Force" forces english on NTSC-U games, and japanese on NTSC-J games. Forcing the language of the disc is required for some import games.

Force Video:
Option which video mode to use. "Disc" is the default and DOES NOT force anything and is THE option that works. "Wii" forces the video mode set in the Wii settings.

Patch Video:
ONLY ENABLE IF YOU NEED IT! Patches the video mode(s) inside the main.dol to the video mode the game will be started with. This makes more import games playable with "correct" colors.

VIDTV Patch:
ONLY ENABLE IF YOU NEED IT! ??? Something video related.

Patch Country Strings:
ONLY ENABLE IF YOU NEED IT! Required for some import games, mostly people with japanese Wiis need this.

Storage device:
Defines which storage device is used for Ocarina, alternative .dol loading and .wip patches

Search patches:
Enables looking for .wip patch files in the NeoGamma folder on the selected storage device.

Gamecube Mode:
'MIOS' is the old behavior, it just starts the MIOS if a GC disc is inserted. 'internal' starts the included GC Backup Launcher from WiiGator(requires compatible cMIOS). 'external' starts an GC homebrew .dol from storage




WHICH cIOS TO USE:

Rev 19:
- allows using different IOS as base to fix games which require this
- Decrypted discs only work if IOS38 was used as base IOS. 1:1 discs should work fine
Seems to be the best cIOS so far(commendation #1)

Rev 18:
- allows using different IOS as base to fix games which require this
- sd/sdhc loading broken
- Can't play games with disc-in-the-drive-check games like Metroid Prime 3
- Decrypted discs only work if IOS38 was used as base IOS. 1:1 discs should work fine

Rev 17:
- contains BCA code
- Rebooter status unknown, may be broken, maybe not
- Same issues as with all other revisions: No instruments, no Monster Hunter Tri, possible online issues...
- DL minor bug, doesn't load the very last sector of DL discs, no reported problems because of this
Seems to be a good and stable cIOS(commendation #2)

Rev 16:
- Not compatbile with NeoGamma at all
- Same DL bug as rev14
- Maybe more issues, don't care

Rev 15:
- Not compatible with the disc channel(rebooter)
- Not compatible with NeoGamma

Rev 14:
- Not compatible with dual layer games, Super Smash Brothers Brawl DVD9 version is affected, DVD5 version works
- Some accessories don't work
- Maybe not compatible with some HDD enclosures that work on rev9/10 (issue with one of these would be: can't get HDD detected or can't start any games)
- Maybe not compatible with HDDs that spin down(only 1 report), but all other cIOS from Waninkoko are affected by this as well, issues are freezes in the middle of games
- Maybe muliplayer issues (strange reports, works for some people and for others it doesn't)
Heavily tested, no bigger issues other than the above reported(commendation #3)

Rev 13b:
- Plays most if not all games(but some accessories don't work)
- Improper 001 handling(main.dol patch)
- Improper 002 handling(main.dol patch)
- Improper patch to play games from usb without disc
- cIOS is not compatible with the disc channel.

Rev 13a:
- Plays most if not all games(but some accessories don't work)
- Improper 001 handling(main.dol patch)
- Improper patch to play games from usb without disc
- cIOS is not compatible with the disc channel.
Heavily tested, no bigger issues other than the above reported(commendation #4)

Rev 12:
- Totally broken 001 handling.
- Improper 002 handling(main.dol patch)
- Slower than the other usb cIOS.
- Improper patch to play games from usb without disc
- cIOS is not compatible with the disc channel.

Rev 11:
not tested! But it's the following is known:
-  1st cIOS that works on boot2v4/LU64+ Wiis
- Improper 001 handling(main.dol patch or totally broken one)
- Improper 002 handling(main.dol patch)
- cIOS is not compatible with the disc channel.

Rev 10:
- 1st cIOS with sd loading support.
- Improper 001 handling(main.dol patch)
- Improper 002 handling(main.dol patch)
- cIOS is not compatible with the disc channel.

Rev 9:
- 1st cIOS with usb loading support.
- Improper 001 handling(main.dol patch)
- Improper 002 handling(main.dol patch)
- cIOS is not compatible with the disc channel.

Rev 8:
- Improper 001 handling(main.dol patch)
- Improper 002 handling(main.dol patch)

Rev 7:
- No dual layer support, the 2nd layer is just not accessible. Most if not all other games should work from disc.
No usb loading and no DL, but works fine(commendation #5)

Rev 6:
- No dual layer support
- "an error occured" on half games.

Rev 5:
- No dual layer support
- only support for decrypted discs.

On top of all this there are differences in HDD and accessoire compatiblity between the different usb loading cIOS.







CHANGELOG:

R9 beta 43 - > R9 beta 44

- Gamecube loading(internal GC mode): Printing proper warnings about audio streams on screen
- Gamecube loading(internal GC mode): More plugin size optimisation
- Gamecube loading(internal GC mode): Plugin debugging: Added read audio debugging for retail discs, show filenames for read audio


R9 beta 42 - > R9 beta 43

- Added option to show/hide the rebooter
- Gamecube loading(internal GC mode): Added dirty fix to align bad audio streams
- Gamecube loading(internal GC mode): Added auto options for the backup plugin, patched MIOS and audio patches


R9 beta 41 - > R9 beta 42

- Gamecube loading(internal GC mode): Moved high plugin memory setup behind the apploader loop(increases compatiblity with high plugin(not patched MIOS or Action Replay + high plugin!)
- Gamecube loading(internal GC mode): Added warning when audio streams without 32KB alignment are found
- Gamecube loading(internal GC mode): Plugin debugging: Show filenames for dvd reads
- Gamecube loading(internal GC mode): Plugin debugging: Support for games with multiple .dols/.elfs on retail discs(only debugging related!)


R9 beta 40 - > R9 beta 41

- Gamecube loading(internal GC mode): More plugin size optimisations
- Gamecube loading(internal GC mode): Added some dvd read error debug messages


R9 beta 39 - > R9 beta 40

- Gamecube loading(internal GC mode): Added ability to select the 2nd disc from an actual 2nd disc
- Gamecube loading(internal GC mode): Checking the disc cover once, it seems this helps with disc switching in-game
- Gamecube loading(internal GC mode): Trying to revert memory setup when loading Action Replay(so it does not overwrite the backup plugin)


R9 beta 38 - > R9 beta 39

- Gamecube loading(internal GC mode): Changed the debug printf patterns to patterns received from Crediar, more stable + more output
- Gamecube loading(internal GC mode): Added option to play around with the Audio Status Request fix
- Gamecube loading(internal GC mode): Added patched MIOS boot method


R9 beta 37 - > R9 beta 38

- Gamecube loading(internal GC mode): More reloader optimisations, the fast reloader should work on everything now(there's a chance it breaks games that worked before with fast reloader, these should still work with forced reloader...)
- Gamecube loading(internal GC mode): Freeze with memory card in slot B should be fixed


R9 beta 36 - > R9 beta 37

- Gamecube loading(internal GC mode): Made the debug printf in the loader itself non blocking, should fix the current GC retail disc + Wiird issues


R9 beta 35 - > R9 beta 36

- Added basic cIOS rev20 identification
- Added IOS Reload block option(only cIOSrev20+, only discs)
- Gamecube loading(internal GC mode): Added proper dvd reset debugging


R9 beta 34 - > R9 beta 35

- Gamecube loading(internal GC mode): Fix for Wind Waker PAL freeze on mini map, might work in NTSC-U (extracted from MIOSv5, yes no c there)


R9 beta 33 - > R9 beta 34

- Only calling dvd inquiry once per NeoGamma boot(should fix init drive errors when using IOS61 for storage access[thanks to luminalace for reporting it], might also fix random inquiry errors)
- Updated the HBC icon with transparency


R9 beta 32 - > R9 beta 33

- Added Sneek's video patch for wii games, may work better than the old patches
- Gamecube loading(internal GC mode): Adding plugin debugging to the GUI, even for retail discs(requires usb gecko!)


R9 beta 31 - > R9 beta 32

- Gamecube loading(internal GC mode): Maybe fixed Action Replay support(changed suspicious jumptable nr)
- Gamecube loading(internal GC mode): More plugin size optimisation
- Gamecube loading(internal GC mode): Forced reloader is not saved anymore, it's only for testing(if a game requires it, NeoGamma will do it automatically once it is known)
- Gamecube loading(internal GC mode): Moved the memory setup before the apploader, might increase compatibility


R9 beta 30 - > R9 beta 31

- Better understandable drive warnings on read error
- Gamecube loading(internal GC mode): Dirty fix for Ikaruga(Thanks to Crediar for pointing to 0xCC006020 for Audio Status Requests)
- Gamecube loading(internal GC mode): Added lots of debug output(need to build debug version for this)


R9 beta 29 - > R9 beta 30

- Gamecube loading(internal GC mode): Fixed audio streaming on retail discs with the help of Crediar(Eternal Darkness, Starfox Adventures ...)
- Gamecube loading(internal GC mode): Added 4 new hooktypes thanks to Crediar(they all are for the same function, but different patterns)
- Gamecube loading(internal GC mode): Added possiblity to boot games with the high plugin for testing purposes(that it'S not saved is not a bug!)
- Gamecube loading(internal GC mode): Maybe fixed some serious memory setup issue(should be most noticeable when using the high plugin)


R9 beta 28 - > R9 beta 29

- Gamecube loading(internal GC mode): Fixed wrong time&date in GC games


R9 beta 27 - > R9 beta 28

- Gamecube loading(internal GC mode): Removed dvd_report_error_replacement to get more free memory
- Gamecube loading(internal GC mode): Calling the callback function directly for everything that does nothing


R9 beta 26 - > R9 beta 27

- Gamecube loading(internal GC mode): Next try to get rid of the random crashes


R9 beta 25 - > R9 beta 26

- Gamecube loading(internal GC mode): Added another sleep before video init in GC mode
- Gamecube loading(internal GC mode): Removed pad init in GC mode
- Gamecube loading(internal GC mode): Added option to set reloader to forced(fixes 007 Agent under Fire, automatically set to forced on it)


R9 beta 24 - > R9 beta 25

- Gamecube loading(internal GC mode): Added a sleep before booting BC, hopefully fixes these random crashes
- Gamecube loading(internal GC mode): Output which dvd function is used(just additional info)


R9 beta 23 - > R9 beta 24

- Gamecube loading(internal GC mode): Added Nicksasa's GC hooks again, they seem to work for a few games


R9 beta 22 - > R9 beta 23

- Gamecube loading(internal GC mode): Added warnings if dvd functions could or would not be patched


R9 beta 21 - > R9 beta 22

- Gamecube loading(internal GC mode): Using a png as background now
- Gamecube loading(internal GC mode): Removed sleep from beta 21, didn't help


R9 beta 20 - > R9 beta 21

- Using devkitPPC r21, libogc 1.8.3 and libfat 1.0.7 now
- Gamecube loading(internal GC mode): Added a sleep before video init(maybe helps with random crashes on startup)


R9 beta 19 - > R9 beta 20

- Gamecube loading(internal GC mode): Virtually disable Ocarina when no codes are found
- Gamecube loading(internal GC mode): Removed debugging only related dvd commands in the plugins
- Gamecube loading(internal GC mode): Added plugin memory protection on reloader(_tiny_ chance it fixes some multi .dol game problems)
- Gamecube loading(internal GC mode): Added report_error to low plugin(_tiny_ chance it fixes some audio problems)


R9 beta 18 - > R9 beta 19

- All unused options are now greyed out
- Allow .gct files with 4 and 6 digits of the disc id
- Auto Force language now only forces if the Wii's region is different from the game's region
- Added hidden feature for developers only, only talk in PM about it


R9 beta 17 - > R9 beta 18

- Gamecube loading(internal GC mode): Restored the possibilty to boot single game discs with Action Replay on a multi game disc
- Gamecube loading(internal GC mode): Speed optimisation for the reloader
- Gamecube loading(internal GC mode): Removed unused code


R9 beta 16 - > R9 beta 17

- Gamecube loading(internal GC mode): Dirty fix for Pokemon Box(proved to be not that bad)
- Gamecube loading(internal GC mode): Enabled reloader for games booted via Action Replay(but cheats won't work on mutli .dol games)


R9 beta 15 - > R9 beta 16

- Gamecube loading(internal GC mode): Finally added reloader support


R9 beta 14 - > R9 beta 15

- Gamecube loading(internal GC mode): Allow the drive to reset. The 2nd disc feature now works(again)


R9 beta 13 - > R9 beta 14

- Cosmetical changes to GUI and code
- Gamecube loading(internal GC mode): Calling ICInvalidateRange after DCFlushRange in the backup plugin, maybe increases stability, but results in slower reading


R9 beta 12 - > R9 beta 13

- Finally added saving of the gamecube options
- Gamecube loading(internal GC mode): Added Ocarina support (only retail discs)


R9 beta 11 - > R9 beta 12

- Added .wip files for Prince of Persia: The Forgotten Sands(not confirmed to work yet)
- Gamecube loading(internal GC mode): Switching to game video mode just before booting the game, fixes some video mode issues during the loading screen
- When using a .wip patch, it says "patch forced!" now if the old data from the .wip file did not match the data in memory


R9 beta 10 - > R9 beta 11

- Changed alt .dol code, seems bss wasn't cleared...
- Gamecube loading(internal GC mode): reverted video mode code from beta 10
- Gamecube loading(internal GC mode): Added proof of concept Wiird support for GC(only retail discs, only debugger, only VI hook)


R9 beta 9 - > R9 beta 10

- Gamecube loading(internal GC mode): Changed video mode code in the GC loading screen(doesn't change anything...)
- Gamecube loading(internal GC mode): Using drive command to enable audio streaming now(retail Eternal Darkness still not booting, while the backup still boots)


R9 beta 8 - > R9 beta 9

- Added identification of the used cIOS(rev13a+b, rev18 and rev19 only)
- Gamecube loading(internal GC mode): Disabled all debug printf and patching of debug printf in the main.dol 


R9 beta 7 - > R9 beta 8

- Gamecube loading(internal GC mode): Added video mode patches


R9 beta 6 - > R9 beta 7

- Rearranged the menu
- Gamecube loading(internal GC mode): Added PAL(auto) video mode, it's PAL480i for NTSC and PAL576i for PAL games
- Don't bug with the drive info when loading from usb


R9 beta 5 - > R9 beta 6

- Prevent that a stubbed IOS249 is loaded
- Added warning on dvd read error for drives that can't read DVD-Rs(needs to be improved)
- Hide usb/sd loading option when using an IOS


R9 beta 4 - > R9 beta 5

- Added code that allows to identify where a dvd read error occured


R9 beta 3 - > R9 beta 4

- Gamecube loading(internal GC mode): Partly fixed video mode code, forcing PAL60 works at least for some NTSC games now(but not PAL games!)


R9 beta 2 - > R9 beta 3

- Fixed alt .dol disc+ bug causing some .dols to be unloadable
- Added .wdm file for Rampage: Total Destrucion(by woodoste)
- Gamecube loading(internal GC mode): Hopefully fixed code dump when playing certain backups that are not multi game discs(bug found by Levente)


R9 beta 1 - > R9 beta 2

- Gamecube loading(internal GC mode): Added support for retail discs
- Gamecube loading(internal GC mode): Changed video mode code, only confirmed working video mode is NTSC480i, PAL480i is confirmed to NOT work at the moment, PAL576i seems to work, progressive unknown
- Gamecube loading: Clearing bss before loading .dol sections for homebrew .dols(only relevant when building a cMIOS)


R8 - > R9 beta 1

- Gamecube multi game disc selection moved to wii mode(compatible cMIOS + GC mode 'internal' only) see gamecube.txt for details
- Fixed controls(support 2nd, 3rd and 4th controller, shutdown always possible when waiting for button press)


R7 - > R8

- Changed to graphics from Empyr69er
- new Wiird / Ocarina engine (only partial gameconfig.txt support, but it's Brawl+ compatible) 
- Added alternative .dol loading from disc+(read .wdm file from storage to show option names that mean something and also allow parameters, Sam & Max episode selection)
- Added support to apply patches in form of .wip on the fly to the main.dol(discid.wip for main.dol, discid_dolname.wip for alterntive .dols from disc)
- Added WiiGator's GC Backup Launcher
- Added possibility to run GC homebrew if a GC disc is inserted

- Changed entrypoint to 0x80dfff00 (should change alternative .dol loading compatibility)
- Removed not game loading or rebooter related code
- Removed receiving commands from usb gecko
- Safe memory allocation (important for files loaded from nand)
- Compiled with newer libogc(see libogc.txt)
- Return to loader on exit only works for HBC now(libogc issue)
- added support for renamed ehci module in cIOS rev18
- Changed rebooter code, should also be preloader compatible now
- Changed rebooter code with hacks from preloader(skip disc updates, region free, force cIOS)
- Lots of changes to storage access code, this should allow to use IOS36 or IOS61 for all storage access(excluding the config)
- Changed most of the output


R8 RC6 - > R8 final:

- forced config reset


R8 RC5 - > R8 RC6:

- Fixed bug in .wdm file parsing code that caused the last parameter to be ignored if there isn't a newline at the end of the file
- Added some .wdm files
- Changed some config defaults


R8 RC4 - > R8 RC5:

- fixed code dump if no storage device was accessed, storage shutdown code dumps if storage was not inited


R8 RC3 - > R8 RC4:

- added support for renamed ehci module in cIOS rev18
- changed region free code on rebooter(taken from preloader)
- added paused start option for the debugger
- Lots of changes to storage access code, this should allow to use IOS36 or IOS61 for all storage access(excluding the config)
- Added alternative .dol loading from disc+(read .wdm file from storage to show option names that mean something and also allow parameters, Sam & Max episode selection)
- B button support in the menus


R8 RC2 - > R8 RC3:

- added missing options to the config file
- added possibility to turn preloader support for rebooter off
- changed some more output


R8 RC1 - > R8 RC2:

- eliminated compiler warnings
- changed code to force cIOS on rebooter(taken from preloader)
- added code to skip disc updates on 4.2 system menu on rebooter(taken from preloader)
- Added WiiGator's GC Backup Launcher
- Added possibility to run GC homebrew if a GC disc is inserted
- Changed output a bit


R8 beta 17 - > R8 RC1:

- updated cIOS warnings for cIOS rev17
- Hopefully fixed code dumps on exit if launched from a channel
- Added autoboot code(but disabled, no official version will have this enabled)


R8 beta 16 - > R8 beta 17:

- added .wip file for japanese New Super Mario Bros
- re-enabled manual 001 fix for alternative .dol loading from storage for cIOS rev < 14
- changed 002 code for IOS Version patched games again, works at least on not IOS Reloading 002 games that are patched


R8 beta 15 - > R8 beta 16:

- updated cIOS warnings
- included a gameconfig.txt for Brawl+ (if you get one together with the .gct file, use that one and not the one from NeoGamma)


R8 beta 14 - > R8 beta 15:

- Fixed code dump when poking values from gameconfig.txt


R8 beta 13 - > R8 beta 14:

- Changed Ocarina code a little more to match Gecko OS' code


R8 beta 12 - > R8 beta 13:

- Removed New Super Mario Bros patches
- Added support to apply patches in form of .wip on the fly to the main.dol
- Changed storage handling
- fixed another stupid bug in NeoGamma's Ocarina code


R8 beta 11 - > R8 beta 12:

- Repaired New Super Mario Bros patch for both PAL&NTSC, but still no discs


R8 beta 10 - > R8 beta 11:

- Patch updated to work with New Super Mario Bros NTSC too


R8 beta 9 - > R8 beta 10:

- not shutting down storage if Ocarina is enabled(Gecko OS does the same)


R8 beta 8 - > R8 beta 9:

- updated code handler to latest version


R8 beta 7 - > R8 beta 8:

- The code handler init should be in the proper place now ==> Brawl+ might actually work now


R8 beta 6 - > R8 beta 7:

- beta 6 had the wrong disc id for NSMB


R8 beta 5 - > R8 beta 6:

- Experimental patch for New Super Mario Bros added*

*Patch is said to be found by hqyhqyhqy, don't know if that's true 


R8 beta 4 - > R8 beta 5:

- gameconfig is searched on the same device as Ocarina now


R8 beta 3 - > R8 beta 4:

- Added partial gameconfig parsing code
- Next try to fix 002 on IOS Version patched games


R8 beta 2 - > R8 beta 3:

- fixed Ocarina
- expermental 002 fix that should work for IOS Version patched games
- warning if hook was not patched)


R8 beta 1 - > R8 beta 2:

- Rebooter should work on preloader
- Maybe fixed that Ocarina did not work at all
- Dirty Brawl+ compatiblity


R7 - > R8 beta 1:

- new Wiird / Ocarina engine
- Changed rebooter code
- Changed entrypoint to 0x80dfff00 (should change alternative .dol loading compatibility)
- Skip disc updates for PAL/US 3.2, 4.0 and 4.1
- Safe memory allocation (important for files loaded from nand)
- Removed not game loading or rebooter related code
- Removed receiving commands from usb gecko
- Changed to graphics from Empyr69er


R6 - > R7:

- Increased timeout to 30 seconds
- Cleaned up code for decrypted discs
- Hopefully 100% working gamecube disc detection now
- Cleaned up code for video modes, gamecube games are started with the selected video mode now
- Changed rebooter behaviour, hopefully works for all system menus WITHOUT preloader attached
- Removed 001 main.dol patching for alternative .dols
- Removed Anti 002 fix
- Removed dirty fix for Wii Sports Resort
- Added alternative .dol loading from usb storage
- Alternative .dol loading from storage now loads .dols with 6 and 4 characters
- Fixed error that prevented to load games after receiving an error in a previous loading attempt


R5 - > R6:

- Fixed bug in game selection
- Fixed no wpad error when no cIOS is installed
- Added timeout for dvd reading
- Clearing bss now for alternative .dols
- Added loading alternative .dols from disc 


R4 - > R5:

- Fixed a "Out of memory" error
- Fixed a "fst.bin error"
- Fixed alternative .dol loading when loading games from sd
- Dirty fix for Wii Sports Resort
- Accepting games with disc ids starting with 'D' as Wii games(Monter Hunter 3 demo for example)


R3 - > R4:

- Changed how the game entries are sorted
- Added IOS Reload when trying to mount a wbfs device (from 7th try on) to increase compatibility with enclosures and HDDs
- Changed sd and sdhc card handling, hopefully fixed the corruped config file bug with this
- Refuse to load a config with 1 or more option out of range
- Moved game selection to main menu
- Added option to load alternative .dol from sd card
- Applying main.dol patches only to main.dol now
- Added hooktype "none"
- Moved all file access on sd card to the folder "NeoGamma", loading Ocarina works from both NeoGamma/codes and codes.
- Added Anti 002 fix. This reverts the 002 main.dol patch. NOT TESTED! This also might do something else too.


Gamma - > NeoGamma R3:

- Ported to the new libogc
- Warning before memory card in slot 2 is accessed as usb gecko
- Auto Force Language option added, it forces english for games with region 'E'(NTSC-U) and japanese for games with region 'J'
- Moved memory stuff before the apploader. Now Red Steel and SSX should be working. (they still (try to) load their IOS themselves)
- Writes the Game ID Address(0x80000000) now into the memory at 0x80003184. Now Sam & Max and FarCry should be working. (they still (try to) load their IOS themselves)
- Save configuration to sd card
- Added Country String Patching (mostly helpful for japanese users with US and PAL games)
- Load Ocarina from SDHC and USB(when encountering problems, try the different strange options, using IOS61 is only compatible if NeoGamma was compiled with a libogc compatible with it like libogc SVN)
- Added option to patch video modes
- Added video modes that can be forced(MPAL) / Changed to use slightly different video modes
- Fake IOS Version in memory (this removes the 002 error)
- Changed to Graphics by: xabarasx
- Added SD/USB Loading


WiiPower