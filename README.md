=============
 MemcardRex:
=============

 Author: Shendo
 Version: 1.9
 Updated: 2014-XX-XX (YYYY-MM-DD)

===============
 Requirements:
===============

 .NET Framework 2.0.
 Windows® Vista™ or 7 for the glass status bar.

===================
 About MemcardRex:
===================

 MemcardRex is a PS1 Memory Card explorer/editor.

 The following Memory Card formats are supported:

    * ePSXe/PSEmu Pro Memory Card(*.mcr)
    * DexDrive Memory Card(*.gme)
    * pSX/AdriPSX Memory Card(*.bin)
    * Bleem! Memory Card(*.mcd)
    * VGS Memory Card(*.mem, *.vgs)
    * PSXGame Edit Memory Card(*.mc)
    * DataDeck Memory Card(*.ddf)
    * WinPSM Memory Card(*.ps)
    * Smart Link Memory Card(*.psm)
    * MCExplorer(*.mci)
    * PSP virtual Memory Card(*.VMP) (opening only)
    * PS3 virtual Memory Card(*.VM1)

 The following single save formats are supported:

    * PSXGame Edit single save(*.mcs)
    * XP, AR, GS, Caetla single save(*.psx)
    * Memory Juggler(*.ps1)
    * Smart Link(*.mcb)
    * Datel(*.mcx;*.pda)
    * RAW single saves
    * PS3 virtual saves (*.psv) (importing only)

 Reading and writing data to real Memory Cards is supported via DexDrive.

==========
 License:
==========

 This software is licensed under GPL 3.0 licence.

===========
 DexDrive:
===========

 As of version 1.6 MemcardRex has a suport for InterAct DexDrive.
 Both reading and writing data from/to PS1 Memory Cards is supported.

 As you may or may not know DexDrive is a very quirky device and sometimes it just refuses to work.
 Even the first party software (DexPlorer) has problems with it (failed detection of a device).
 If you encounter problems, unplug power from DexDrive, unplug it from COM port and connect it all again.

 It is recommended that a power cord is connected to a DexDrive, otherwise some cards won't be detected.
 Communication was tested on Windows 7 x64 on a real COM port and with a Prolific and FTDI based USB adapters.

 To select a COM port DexDrive is connected to go to "Options"->"Preferences".

==============
 MemCARDuino:
==============

 MemCARDuino is an open source Memory Card communication software for various Arduino boards.
 It acts as a simple interface for Memory Card communication similar to commercial DexDrive device.

 More information can be found in the "Hardware" directory of MemcardRex package.

 Support for MemCARDuino was added in MemcardRex version 1.8.

==============
 PS1CardLink:
==============

 PS1CardLink is a software for the actual PlayStation and PSOne consoles.
 It requires an official or home made TTL serial cable for communication with PC.
 
 It acts as a firmware which allows you to turn a console into a Memory Card reader.
 More information can be found in the "Hardware" directory of MemcardRex package.

 Support for PS1CardLink was added in MemcardRex version 1.8.

============
 ChangeLog:
============

 Version 1.8:
--------------
* Fixed a crash if "File->Quit" was selected after reading Memory Card from DexDrive.
* Added "Restore window position at startup" option.
* Added "Format card" option under "Hardware" menu per Carmax91's suggestion.
* Added support for MemCARDuino, an Arduino based Memory Card reader with open source firmware.
	- Check out "Hardware" directory included with MemcardRex.
* Added support for PS1CardLink, a PS1 software which acts as a Memory Card reader.
	- Check out "Hardware" directory included with MemcardRex.
* Extended support for Action Replay saves. Non standard saves can be imported now (codelist, e00-exe, etc...).
* Bundled "BCLoader 0.1" plugin, a loader for Black Chocobo FF7 save editor.

 Version 1.7:
--------------
* DTR line is now used in DexDrive communication.
* Adjusted timing for DexDrive communication.
	 - Memory Cards that were not readable should work now.
* Added import icon feature in the icon editor.
	- 16x16 pixel icons with no more than 16 colors are supported.
* Added a complete set of new interface icons.
	- Silk icon set 1.3 by Mark James.
* Added a "Compare with temp buffer" option.
* Added Del shortcut for "Remove save" option.
* Message box is now slightly larger for easier readability.
* Save prompt now defaults to "Yes" instead of "No".
* Menu options are now dynamic and items are enabled/disabled related to the currently selected save.
* Bundled "CTREdit 0.1" plugin, a Crash Team Racing save editor.

 Version 1.6:
--------------
* Added Ctrl-C and Ctrl-V shortcuts for "Copy" and "Paste save from temp buffer" options respectively.
* Added support for *.VM1 Memory Cards.
* Added support for InterAct DexDrive.
	- Thanks to Frédéric Brière for information.
* Icon size for save properties window can now be selected
	- Inspired by the Kubusleonidas' Memory Card editor.
* Simplified plugin interface (for programmer) but just as powerfull.
* Application settings are now stored in the XML file format.
* GUI is now more consistent with the general usage guidelines.
* Updated "SpyroEdit" plugin to version 0.3.
* Bundled "MGSEdit 0.1" plugin, a Metal Gear Solid save editor.

 Version 1.5:
--------------
* Fixed errors which caused crash in the following situations:
	- Formating a slot and saving card in .gme format.
	- Opening a card containing corrupted slots.
	- Attempt of an edit operation with no save selected.
* Fixed issue which caused significant delay when preferences dialog was opened for the first time.
* Fixed issue which locked a file even if it failed to open.
* Added second color picker to icon editor which is controlled by right mouse button.
* Added "All files (*.*)" option in the "Open Memory Card" dialog.
* Added warning message when editing a save with plugin.
	- This message can be turned off in the preferences dialog.
* Added "Close All" option under the "File" menu.
* If the card could not be opened a more descriptive message is now shown.
* If the save region is unknown hex data will be shown instead in certain dialogs (Datel saves).
* Saves with ASCII encoding (opposite to default Shift-JIS) will now display correct title (Datel saves).
* Product codes can now be less then 10 character long but only if there is no identifier.
* Plugin specs updated. Refer to the sample interface code for changes.
* Updated "SpyroEdit" plugin to version 0.2.

 Version 1.4:
--------------
* Fixed error with discarding returned data from plugin.
* Fixed error with plugin menu showing plugins even if there is no card opened.
* Rearanged plugin window to fit more information in less space.
* Bundled "SpyroEdit 0.1 beta" plugin, a very simple save editor for Spyro the Dragon.


 Version 1.3:
--------------
* Added temp buffer save information on the toolbar.
* Added plugin system which allows other developers to make save editors for MemcardRex.
	- sample code for the plugin interface can be found on www.shendo.xtemu.com.


 Version 1.2:
--------------
* Fixed issue where PSV file containing PS2 save could be imported as PS1 save.
* Fixed crash when zero byte file was imported as a single save.
* Glass status bar can now be toggled on/off from the preferences dialog.
* Only one instance of the same file can now be opened.


 Version 1.1:
--------------
* Fixed error with status bar not being updated after saving a card.
* Added prompt when "format slot(s)" operation is initiated.
* Added glass status bar (available on Windows® Vista™ and 7).
* Added multiple file selection in "Open Memory Card" dialog.
* Tabs can now be closed by pressing the middle mouse button.
* If the backup directory is missing it will now be created when the cards are being backed up.
* If the initial "Untitled" card has not been edited it will be removed when the existing card is opened.
* Extension left on the raw files will now be ommited upon saving.
* Changed settings format to ".ini".


 Version 1.0:
--------------
  Note: This version of MemcardRex was written from the scratch.

* Multiple files can now be opened simultaneously.
* Name of the Memory Card is now displayed on the tab.
* Location of the Memory Card is now shown in the status bar.
* Save title can be shown in either ASCII or UTF-16 representation of the original Shift-JIS title.
	- This means that if you have a save with innacurate title
	  switching to UTF-16 should yield better results.
* Custom font can now be selected for the save list in the preferences dialog.
	- Recommended font: Microsoft Sans Serif.
* Settings are now stored in "Settings.cfg" file.


 Version 0.9:
---------------
* Fixed a small issue with invisible coordinates in icon editor.
* Region column now replaced with country flags.
* Added "backup memory cards" option which can be toggled on/off from the preferences dialog.
	- Upon opening cards will be saved to a backup directory under the same filename.
	- Warning: Files over 512KB won't be backed up.


 Version 0.8:
---------------
* VMP format is supported once again (opening only) since some people were asking for it.
* PS3 virtual save format (*.psv) is now supported (importing only).
* RAW single save format is now supported (both importing and exporting).
* On startup first slot of both memorycards is now selected.
		- This will prevent errors with the save import function if user has not
		  selected the slot to import to.


 Version 0.7:
---------------
* Fixed error with the "format slot(s)" function (some data was not deleted after formatting).
* Fixed error with the "Paste from temp buffer" function
	- sometimes occupied slots were detected as free so pasted saves could overwrite existing ones.
* Added flipping and rotation options to icon editor.
* Added support for additional image formats when exporting the icon.
* Added support for XPlorer, Action Replay, GameShark, Caetla, Smart Link and Datel single saves.


 Version 0.6:
---------------
* Memory Card open function rewritten, files should load a lot faster now.
* Fixed a small error when editing icon of the save on Memory Card 2.
* Old DexDrive cards (with missing slots) and the ones with corrupted header are now supported.
* Requirements have been dropped down to .NET Framework 2.0.
* Right click menu added per Hard core Rikki's suggestion.
* Added save cards prompt upon closing if memorycards have been edited.
* Added occupied slots indicator in save information dialog.


 Version 0.5 rev 2:
--------------------
* Fixed a major bug in the card formatting function.
* Fixed error with import save function for Memory Card 2.
* Fixed error with the grid line settings for Memory Card 2.
* Added command line support per RedawgTS's suggestion.
	- That means you can now associate memcards with MemcardRex to open them.


 Version 0.5:
---------------
* Fixed error with the Shift-JIS to ASCII conversion where 'b' character would come out as "bb".
* Added icon editor per TheCloudOfSmoke's suggestion.
* Added preferences dialog where user can change settings.
* Added support for Memory Juggler single saves.


 Version 0.4:
---------------
  Note: This version of MemcardRex was written from the scratch.

* Added comments support for dexdrive memory cards.
* Added toolstrip information.
* Added support for simultaneous editing of 2 memory cards.
* Added support for dragging-and-dropping of memory card files.
* Saves can now be copied to the temp buffer and pasted to the selected card and slot.
* Double click on the selected item now shows a save information.
* Product code, Identifier and Region now shown in the list instead on the toolbar.
* Editing operations are now save based instead of the slot based like in older versions.
* Dropped support for .vmp cards until proper header reconstruction is possible.


 Version 0.3b:
---------------
* New GUI.
* Added export/import single save function.


 Version 0.2b:
---------------
* Fixed a small issue with the list refresh function.


 Version 0.1b:
---------------
* Initial release.


==========
 Credits:
==========

 Beta testers:
--------------
 Gamesoul Master.
 Xtreme2damax.
 Carmax91.

 Thanks to:
------------
 @ruantec.
 Cobalt.
 TheCloudOfSmoke.
 RedawgTS.
 Hard core Rikki.
 RainMotorsports.
 Zieg.
 Bobbi.
 OuTman.
 Kevstah2004.
 Kubusleonidas.
 Frédéric Brière.
 Mark James.
 Cor'e.
