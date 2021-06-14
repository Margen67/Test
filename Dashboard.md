Xenia Canary (and to some extent, master) can run the Xbox 360 dashboard.

### Installation

#### Automatic *(recommended)*

0. Prerequisites:
    * [7-Zip](https://www.7-zip.org)
1. [Right click this link](https://gist.githubusercontent.com/Margen67/ad7823f9e7427312c4a613d39cbdd562/raw/dashboard.ps1) and save it.
2. Right click the downloaded file and click `Run with PowerShell`.
3. Dashboard 1888 (Blades) will be saved to the `1888.FS` folder.
4. To run the dashboard in Xenia Canary, open `1888.FS\dash.xex`.

#### Manual

  0. Prerequisites:
      * [7-Zip](https://www.7-zip.org)
      * xextool
      * Xbox 360 Dashboard 1888 (see [dashboards list](FAQ#dashboards))
  1. Extract the dashboard to the same directory as `xextool.exe`
  2. Open Command Prompt (or PowerShell) and run the following:
      ```
      .\xextool -d . xam.xex
      ```
  3. Add the `.xzp` file extension to `gamercrd`, `shrdres`, and `xam`
  4. Run `dash.xex`

### Updating

* *Updating requires version 1888 as a base.*
* Only Dashboard versions up to ~13604 have been tested and proven to work. Versions newer than this might not work.
* Dashboards have varying levels of usability. None work perfectly, so far.
0. Prerequisites:
    * [7-Zip](https://www.7-zip.org)
    * A build of xenia which works with later dashboards.
      * [660559bd](https://github.com/xenia-canary/xenia-canary/releases/tag/tag-660559bd372e34f62979b43fc9bf23b81f236037)
    * An update file from [the list below](https://github.com/xenia-canary/xenia-canary/wiki/FAQ#dashboards)
    * wxPirs
    * Xbox 360 Dashboard 1888 (see [dashboards list](FAQ#dashboards))
    * xextool
1. Extract the 1888 archive and the update archive in the same folder using 7-Zip.
2. Extract your update files from `$SystemUpdate\su20076000_00000000` to your working directory using wxPirs.
    * You may delete the file when this process is complete.
3. Extract XZP files from xam.xex:
    1. If you have a file called `$flash_xam.xex`, delete `xam.xex` and rename `$flash_xam.xex` to `xam.xex`.
        * This will ensure that the right files are extracted.
        * You may optionally repeat this process for other `$flash_[name].xex` files as well.
    2. Move `xextool.exe` to your working directory (with the `.xex` files)
    3. Open Command Prompt (or PowerShell) and run the following command:
        ```
        .\xextool -d . xam.xex
        ```
        If these are successful, you should see messages like these in the console:
        ```
        Successfully dumped 6 resources to .
        ```
        You should also have several new files extracted from the xex inside the directory. Among these should be:
          * `audio`
          * `gamercrd`
          * `mplayer`
          * `shdres`
          * `xam`
    4. If the files that were extracted from `xam.xex` don't have the extension `.xzp` on the end, add it.
4. Extract any other PIRS files (no extension) from the `\$SystemUpdate\` folder to your working directory using wxPIRS. (They may or may not be needed)
    * You may delete the PIRS files afterward.
    * You should now have a folder containing at LEAST these files (Usually many more):
        * $flash_dash.xex
        * $flash_xam.xexp
        * dash.xex
        * gamercrd.xzp
        * mplayer.xzp
        * shdres.xzp
        * xam.xzp
        * xam.xex
5. Test:
    1. Launch `$flash_dash.xex` with the Xenia build you downloaded.
        * If you performed step 3.1 on `$flash_dash.xex` simply use `dash.xex` instead.

    Your Dashboard should launch successfully, and all sound effects should be working.

    If the dashboard doesn't launch, try this:
      1. Ensure you are using a compatible build of Xenia.
      2. Ensure your final file structure is correct.
      3. Launch `dash.xex` instead.
          * Unlikely this will work. Might open 1888 instead. This means you did not patch the file correctly.
      4. Attempt the optional steps above.

##### Dashboards:

Version | Source
------- | ------
[1888](http://download.digiex.net/Consoles/Xbox360/Dashboards/2.0.1888.0%20FS.rar) | [Source](https://digiex.net/threads/xbox-360-dashboard-update-2-0-1888-0-download.6730/)
[4552](https://web.archive.org/web/20070212052009/http://download.microsoft.com/download/d/1/8/d181ee58-de70-4484-936b-0e9161ccd6b2/HD_DVD_01-2007.zip) | [Source](https://web.archive.org/web/20070111154710/http://www.xbox.com:80/en-US/hardware/x/xbox360hddvdplayer/download.htm)
[5759](https://web.archive.org/web/20071012204343/http://download.microsoft.com/download/d/1/8/d181ee58-de70-4484-936b-0e9161ccd6b2/HD_DVD_05-2007.zip) | [Source](https://web.archive.org/web/20070116182005/http://www.xbox.com:80/en-US/hardware/x/xbox360hddvdplayer/download.htm)
[6683](https://web.archive.org/web/20130514173410/http://assets.xbox.com/en-us/hardware/hddvd/HD_DVD_12-2007.zip) | [Source](https://web.archive.org/web/20080210030627/http://www.xbox.com:80/en-US/hardware/x/xbox360hddvdplayer/download.htm)
[6909](https://web.archive.org/web/20090602054754/https://www.xbox.com/en-US/hardware/x/xbox360hddvdplayer/download.htm) | [Source](https://web.archive.org/web/20090602054754/https://www.xbox.com/en-US/hardware/x/xbox360hddvdplayer/download.htm)
[9199](https://web.archive.org/web/20101027072835/https://download.microsoft.com/download/1/d/8/1d8c09be-278e-41cd-98be-eb9188128227/$systemupdate9199.zip) | [Source](https://web.archive.org/web/20101027072835/https://support.xbox.com/en-us/pages/xbox-360/how-to/update-xbox-360/system-updates.aspx#copy)
[12625](https://web.archive.org/web/20110503185828/https://download.microsoft.com/download/4/B/5/4B502530-BC35-4477-B25A-AEFDCFB7F504/SystemUpdate_12625_USB.zip) | [Source](https://web.archive.org/web/20110123134623/http://support.xbox.com:80/en-US/pages/xbox-360/how-to/update-xbox-360/system-updates.aspx#copy)
[13146](https://web.archive.org/web/20111123140450/http://download.microsoft.com/download/C/B/4/CB4136B7-A0A4-4067-ABE6-D789DF16800F/SystemUpdate_13146_USB.zip) | [Source](https://web.archive.org/web/20110607190427/http://support.xbox.com:80/en-us/pages/xbox-360/how-to/update-xbox-360/system-updates.aspx)
[13599](https://web.archive.org/web/20110828104935/http://download.microsoft.com/download/2/A/C/2AC6BB6F-1A26-4784-BA64-09A96E70CD03/SystemUpdate_13599_USB.zip) | [Source](https://web.archive.org/web/20110712230853/http://support.xbox.com:80/en-us/pages/xbox-360/how-to/update-xbox-360/system-updates.aspx)
[13604](https://web.archive.org/web/20121004065307/http://download.microsoft.com/download/0/1/3/01350ECA-1B12-4920-8E47-80F9CC9F160F/SystemUpdate13604USB.zip) | [Source](https://web.archive.org/web/20111007193349/http://support.xbox.com:80/en-US/xbox-360/how-to/update-xbox-360/system-updates)
[14699](https://web.archive.org/web/20111221134944/http://download.microsoft.com/download/A/4/5/A45B1ADC-11E8-4771-AA5F-2D53A2A3B424/SystemUpdate_14699_USB.zip) | [Source](https://web.archive.org/web/20111213145648/http://support.xbox.com:80/en-US/xbox-360/system-updates/system-updates#0d1579fbc9ee4b7c82fa3373f91f2ce7)
[14719](https://web.archive.org/web/20140907083534/http://download.microsoft.com/download/4/F/D/4FD14C27-2301-4539-8454-AE71F6F1C4FF/SystemUpdate_14719_USB.zip) | [Source](https://web.archive.org/web/20120413170058/http://support.xbox.com/en-US/xbox-360/system-updates/system-updates-info#460401367e48446d9077f9738b00aad5)
[15574](https://web.archive.org/web/20120918032303/http://download.microsoft.com/download/C/0/D/C0D50A10-395F-4D1C-A5A4-3AF6917DCC77/SystemUpdate_15574_USB.zip) | [Source](https://web.archive.org/web/20120719034858/http://support.xbox.com/en-US/xbox-360/system-updates/system-updates-info#13e8c26081294f0e848aeb82eb5be9a4)
[16203](https://web.archive.org/web/20140514173813/http://download.microsoft.com/download/8/3/3/833C313F-C632-4270-8B25-26C214B54A2F/SystemUpdate_16203_USB.zip) | [Source](https://web.archive.org/web/20130621155111/http://support.xbox.com/en-US/xbox-360/system-updates/system-updates-info#470b4208b65444fea6dcee212513a015)
[16537](https://web.archive.org/web/20131103105805/http://download.microsoft.com/download/C/3/9/C39534C0-F579-4B74-8DDE-94CA3A298ABE/SystemUpdate_16537_USB.zip) | [Source](https://web.archive.org/web/20130923005905/http://support.xbox.com/en-US/xbox-360/system-updates/system-updates-info#df57c9267b2646ada66dc85a222eeb13)
[16547](https://web.archive.org/web/20140112120534/http://download.microsoft.com/download/6/8/9/68917704-C8D7-4EB0-AC87-8AAB41C4378E/SystemUpdate_16547_USB.zip) | [Source](https://web.archive.org/web/20131027130203/http://support.xbox.com/en-US/xbox-360/system-updates/system-updates-info#fc2cf1e65c1e40778fd4f7f72b4e58bc)
[Latest](https://www.xbox.com/system-update-usb) | [Source](https://beta.support.xbox.com/help/xbox-360/console/system-updates-info)
