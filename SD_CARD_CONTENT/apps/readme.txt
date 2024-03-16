[MMM] Multi-Mod-Manager


[MMM] is a multi-purpose all-in-one tool for the Wii.  Many useful functions are neatly integrated into
a easy-to-use menu to enable and better support homebrew.  Like a handy 'Swiss knife', it saves users
from the hassle of dealing with separate different tools.  And it does it without sacrificing any features
or functionality.  


Main Features:

* APP Manager to easily launch homebrew from SD card
* WAD Manager with faster batch operations and safety measures
* IOS Manager to check/install/delete/patch/dop IOS or custom IOS
* Manage Priiloader Hacks and switch to it or Wii System Menu
* Install Wii System Menu v4.x from Nintendo servers
* Install Wii Channels from Nintendo servers
* Install & Patch IOS36 to enable homebrew (express 1-click TBR)
* Remove stub IOS or unused Korean IOS
* Display boot2 version and information
* Display Wii system settings and more...
* Reload to any IOS via a easy-to-use selection menu
* Configurable by editing "sd:/mmmconfig.txt" file
* Real-time on-screen status and detail reports on all operations
* Clear and easy-to-understand user interface to a powerful tool
* Stable, compact and loadable from HBC, bannerbomb or as a channel

There is more to [MMM], so just give it a try to better understand what it can do to help you.  
If you have ideas for future feature enhancements or any bug reports, do let me know. 
And as with all tools, please keep the children away and use it yourself appropriately.


  Homepage at  http://mmm4wii.posterous.com
  Support at  http://gbatemp.net/index.php?showtopic=208281


I'm currently seeking donations to support MMM's development - it will help to offset the cost of getting a Wii capable of boot2 bootmii and SSBB, Lego Indiana Jones etc.

I'll greatly appreciate if you can help by sending your donations via Paypal to wiiwu2@yahoo.com

Thank you.


(WiiWu - Sep 20, 2010)



[Changelog for v13.4 - Sep 20, 2010]

Install & Patch IOS36:
- upgraded to support Nintendo's Sep7 IOS updates
- installs patched IOS36 as IOS36 & IOS236
- IOS36-64-v3608.wad used as base IOS

IOS Manager
- updated IOS information database to Sep7

Others
- added new on-the-fly patches to active IOS via AHBPROT mode (if available)

*Important Note*
If your Wii has a non-working internet connection setup, a bug in Homebrew Channel 1.07 & 1.08 will crash any homebrew apps (including MMM) within seconds after launch.  This affects apps launched in AHBPROT mode.

To disable AHBPROT mode, delete the "no_ios_reload" line from meta.xml file in MMM apps folder.


------------------------------------

[Changelog for v13.3 - Sep 13, 2010]

Install & Patch IOS36:
- updated to support System Menu 4.3

IOS Manager
- updated IOS information database

System Menu
- support online install of System Menu 4.3


[Changelog for v13.2 - May 13, 2010]

Wii System Info:
- added feature to extract and show Wii's Parental Controls PIN and Secret answer

IOS Manager + Install & Patch IOS36:
- added IOS patch to remove version restriction when installing IOS (fixes Error -1035)
- upgraded patching engine

WAD Manager:
- added autoloading of a installed IOS if it matches the one in AutoLoadIOS config option


[Changelog for v13.1 - May 5, 2010]

WAD Manager:
- 25% faster WAD installation
- support new cIOSx_v19 & Hermes_v5; fixed all "Error -1029"
- natural sorting of file listing (IOS4 before IOS10)
- upgraded batch selection interface
- new feature to mark a sub-folder and install all its wads with (+) button
- added safety features to protect Wii critical system components and IOS

IOS Manager:
- improved custom IOS install option
- cleanup screen interface

Priiloader:
- added switch to System Menu via priiloader v0.4 and later
- upgraded System Menu's Hacks editor

Stub removal:
- separate categories of stubs
- added removal of unused Korean IOS

System Menu/Channels:
- added safety checks and warnings
  
Others:
- mmmconfig.txt; copy to SD root to configure IOS autoload, storage device, startup path
- enabled support for USB storage devices on port 0
- fixed display support for component connected TV
- and other mostly underlying rewrite and fixes



