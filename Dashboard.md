Certain builds of Xenia Canary can run the Xbox 360 dashboard.

Dashboards have varying levels of usability. None work perfectly.

Versions newer than ~13604 might not work.

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
  1. Extract the dashboard to the same directory as `xextool.exe`.
  2. Open Command Prompt (or PowerShell) and run the following:
      ```
      .\xextool -d . xam.xex
      ```
  3. Add the `.xzp` file extension to `gamercrd`, `shrdres`, and `xam`.
  4. Run `dash.xex`.

### Updating

0. Prerequisites:
    * **Completed installation**
    * A version of Xenia Canary that works with newer dashboards: ([660559bd](https://github.com/xenia-canary/xenia-canary/releases/download/tag-660559bd372e34f62979b43fc9bf23b81f236037/xenia-canary.zip))
      * It's recommended to run older builds with `portable.txt`. See [Options#how-to-use](https://github.com/xenia-project/xenia/wiki/Options#how-to-use)
      * To disable the annoying update message set `check_update` to `false`.
    * wxPirs
    * 1888> dashboard from the list below
1. Extract the downloaded dashboard.
2. Open `su20076000_00000000` in wxPirs. (might be in $systemupdate)
3. Extract all files into the same directory as the 1888 dashboard.

To run the new dashboard open `$flash_dash.xex` in Xenia Canary.

<!--0. Prerequisites:
    * [7-Zip](https://www.7-zip.org)
    * A build of xenia which works with later dashboards.
      * [660559bd](https://github.com/xenia-canary/xenia-canary/releases/download/tag-660559bd372e34f62979b43fc9bf23b81f236037/xenia-canary.zip)
    * An update file from [the list below](https://github.com/xenia-canary/xenia-canary/wiki/FAQ#dashboards)
    * wxPirs
    * Xbox 360 Dashboard 1888 (see [dashboards list](FAQ#dashboards))
    * xextool
1. Extract the 1888 archive and the update archive in the same folder using 7-Zip.
2. Extract your update files from `$SystemUpdate\su20076000_00000000` to your working directory using wxPirs.
    * You may delete the file when this process is complete.
    *  If you have a file called `$flash_xam.xex`, delete `xam.xex` and rename `$flash_xam.xex` to `xam.xex`.
      * This will ensure that the right files are extracted.
      * You may optionally repeat this process for other `$flash_[name].xex` files as well.
3. Move `xextool.exe` to your working directory (with the `.xex` files)
4. Open Command Prompt (or PowerShell) and run the following command:
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
5. If the files that were extracted from `xam.xex` don't have the extension `.xzp` on the end, add it.
6. Extract any other PIRS files (no extension) from the `\$SystemUpdate\` folder to your working directory using wxPIRS. (They may or may not be needed)
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
7. Test:
    1. Launch `$flash_dash.xex` with the Xenia build you downloaded.
        * If you performed step 3.1 on `$flash_dash.xex` simply use `dash.xex` instead.

    Your Dashboard should launch successfully, and all sound effects should be working.-->

##### Dashboards:
<!--
https://web.archive.org/web/20070615000000*/http://www.xbox.com/en-US/support/systemuse/xbox360/console/systemupdates.htm
https://web.archive.org/web/20081217003323/http://www.xbox.com/en-US/support/systemupdates/default.htm
https://web.archive.org/web/20070901000000*/http://www.xbox.com/en-US/support/systemuse/xbox360/console/softwareupdatesredirect.htm
https://web.archive.org/web/*/http://assets.xbox.com/*
https://web.archive.org/web/*/http://download.microsoft.com/*
-->

Version | Source
------- | ------
[1888](http://download.digiex.net/Consoles/Xbox360/Dashboards/2.0.1888.0%20FS.rar) | [Source](https://digiex.net/threads/xbox-360-dashboard-update-2-0-1888-0-download.6730/)
[4548](https://web.archive.org/web/20070103133631/http://download.microsoft.com/download/d/1/8/d181ee58-de70-4484-936b-0e9161ccd6b2/SystemUpdate_11-2006.zip) | 
[4552](https://web.archive.org/web/20070212052009/http://download.microsoft.com/download/d/1/8/d181ee58-de70-4484-936b-0e9161ccd6b2/HD_DVD_01-2007.zip) | [Source](https://web.archive.org/web/20070111154710/http://www.xbox.com:80/en-US/hardware/x/xbox360hddvdplayer/download.htm)
[5759](https://web.archive.org/web/20071012204343/http://download.microsoft.com/download/d/1/8/d181ee58-de70-4484-936b-0e9161ccd6b2/HD_DVD_05-2007.zip) | [Source](https://web.archive.org/web/20070116182005/http://www.xbox.com:80/en-US/hardware/x/xbox360hddvdplayer/download.htm)
[6683](https://web.archive.org/web/20130514173410/http://assets.xbox.com/en-us/hardware/hddvd/HD_DVD_12-2007.zip) | [Source](https://web.archive.org/web/20080210030627/http://www.xbox.com:80/en-US/hardware/x/xbox360hddvdplayer/download.htm)
[6690](https://web.archive.org/web/20090602054754/http://assets.xbox.com/en-us/hardware/hddvd/$Systemupdate_Fall07.zip) | [Source](https://web.archive.org/web/20090602054754/https://www.xbox.com/en-US/hardware/x/xbox360hddvdplayer/download.htm)
[7357](https://web.archive.org/web/20110430070604/http://download.microsoft.com/download/D/1/8/D181EE58-DE70-4484-936B-0E9161CCD6B2/$SystemUpdate_Fall08.zip) | 
[7363](https://web.archive.org/web/20120915104740/http://download.microsoft.com/download/D/1/8/D181EE58-DE70-4484-936B-0E9161CCD6B2/$SystemUpdate_Fall08_7363.zip) | 
[7371](https://web.archive.org/web/20110328234121/http://download.microsoft.com/download/D/1/8/D181EE58-DE70-4484-936B-0E9161CCD6B2/$SystemUpdate_Fall08_7371.zip) | 
[8955](https://web.archive.org/web/20101225052105/http://download.microsoft.com/download/D/1/8/D181EE58-DE70-4484-936B-0E9161CCD6B2/$SystemUpdate_Fall09_8955.zip) | 
[9199](https://web.archive.org/web/20101027072835/https://download.microsoft.com/download/1/d/8/1d8c09be-278e-41cd-98be-eb9188128227/$systemupdate9199.zip) | [Source](https://web.archive.org/web/20101027072835/https://support.xbox.com/en-us/pages/xbox-360/how-to/update-xbox-360/system-updates.aspx#copy)
[12611](https://web.archive.org/web/20110113044414/http://download.microsoft.com/download/1/4/6/146DC573-E0D9-4357-9D85-5A7DEC443050/systemupdate.zip) |
[12625](https://web.archive.org/web/20110503185828/https://download.microsoft.com/download/4/B/5/4B502530-BC35-4477-B25A-AEFDCFB7F504/SystemUpdate_12625_USB.zip) | [Source](https://web.archive.org/web/20110123134623/http://support.xbox.com:80/en-US/pages/xbox-360/how-to/update-xbox-360/system-updates.aspx#copy)
[13146](https://web.archive.org/web/20111123140450/http://download.microsoft.com/download/C/B/4/CB4136B7-A0A4-4067-ABE6-D789DF16800F/SystemUpdate_13146_USB.zip) | [Source](https://web.archive.org/web/20110607190427/http://support.xbox.com:80/en-us/pages/xbox-360/how-to/update-xbox-360/system-updates.aspx)
[13599](https://web.archive.org/web/20110828104935/http://download.microsoft.com/download/2/A/C/2AC6BB6F-1A26-4784-BA64-09A96E70CD03/SystemUpdate_13599_USB.zip) | [Source](https://web.archive.org/web/20110712230853/http://support.xbox.com:80/en-us/pages/xbox-360/how-to/update-xbox-360/system-updates.aspx)
[13604](https://web.archive.org/web/20121004065307/http://download.microsoft.com/download/0/1/3/01350ECA-1B12-4920-8E47-80F9CC9F160F/SystemUpdate13604USB.zip) | [Source](https://web.archive.org/web/20111007193349/http://support.xbox.com:80/en-US/xbox-360/how-to/update-xbox-360/system-updates)
[14699](https://web.archive.org/web/20111221134944/http://download.microsoft.com/download/A/4/5/A45B1ADC-11E8-4771-AA5F-2D53A2A3B424/SystemUpdate_14699_USB.zip) | [Source](https://web.archive.org/web/20111213145648/http://support.xbox.com:80/en-US/xbox-360/system-updates/system-updates#0d1579fbc9ee4b7c82fa3373f91f2ce7)
[14717](https://web.archive.org/web/20121004064821/http://download.microsoft.com/download/5/2/C/52C2BB5E-6A58-44FB-BC05-ECF6BC7240C0/SystemUpdate_14717_USB.zip) | 
[14719](https://web.archive.org/web/20140907083534/http://download.microsoft.com/download/4/F/D/4FD14C27-2301-4539-8454-AE71F6F1C4FF/SystemUpdate_14719_USB.zip) | [Source](https://web.archive.org/web/20120413170058/http://support.xbox.com/en-US/xbox-360/system-updates/system-updates-info#460401367e48446d9077f9738b00aad5)
[15574](https://web.archive.org/web/20120918032303/http://download.microsoft.com/download/C/0/D/C0D50A10-395F-4D1C-A5A4-3AF6917DCC77/SystemUpdate_15574_USB.zip) | [Source](https://web.archive.org/web/20120719034858/http://support.xbox.com/en-US/xbox-360/system-updates/system-updates-info#13e8c26081294f0e848aeb82eb5be9a4)
[16197](https://web.archive.org/web/20140907083414/http://download.microsoft.com/download/E/D/9/ED98782C-C47B-4D1A-9F5F-BDE300AE375F/SystemUpdate_16197_USB.zip) | 
[16202](https://web.archive.org/web/20130329110918/http://download.microsoft.com/download/E/D/9/ED98782C-C47B-4D1A-9F5F-BDE300AE375F/SystemUpdate_16202_USB.zip) | 
[16203](https://web.archive.org/web/20140514173813/http://download.microsoft.com/download/8/3/3/833C313F-C632-4270-8B25-26C214B54A2F/SystemUpdate_16203_USB.zip) | [Source](https://web.archive.org/web/20130621155111/http://support.xbox.com/en-US/xbox-360/system-updates/system-updates-info#470b4208b65444fea6dcee212513a015)
[16537](https://web.archive.org/web/20131103105805/http://download.microsoft.com/download/C/3/9/C39534C0-F579-4B74-8DDE-94CA3A298ABE/SystemUpdate_16537_USB.zip) | [Source](https://web.archive.org/web/20130923005905/http://support.xbox.com/en-US/xbox-360/system-updates/system-updates-info#df57c9267b2646ada66dc85a222eeb13)
[16547](https://web.archive.org/web/20140112120534/http://download.microsoft.com/download/6/8/9/68917704-C8D7-4EB0-AC87-8AAB41C4378E/SystemUpdate_16547_USB.zip) | [Source](https://web.archive.org/web/20131027130203/http://support.xbox.com/en-US/xbox-360/system-updates/system-updates-info#fc2cf1e65c1e40778fd4f7f72b4e58bc)
[16747](https://web.archive.org/web/20140407072239/http://download.microsoft.com/download/6/8/9/68917704-C8D7-4EB0-AC87-8AAB41C4378E/SystemUpdate_16747_USB.zip) | 
[16756](https://web.archive.org/web/20140808063226/http://download.microsoft.com/download/B/6/9/B6917DAC-C3F2-43EE-97DC-2E19D259F4B8/SystemUpdate_16756_USB.zip) |
[16767](https://web.archive.org/web/20140907074806/http://download.microsoft.com/download/D/3/8/D38FA512-BEC6-407C-8B4D-BCE0920D3238/SystemUpdate_16767_USB.zip) | 
[17148](https://web.archive.org/web/20150724204500/http://download.microsoft.com/download/1/E/F/1EFFD3E4-15D3-463A-A534-5A909202CE88/SystemUpdate_17148_USB.zip) | 
[17150](https://web.archive.org/web/20141213014405/http://download.microsoft.com/download/6/C/4/6C41DBB4-2670-4EFE-8347-0CE303643BE9/SystemUpdate_17150_USB.zip) | 
[17349](https://web.archive.org/web/20150509085531/http://download.microsoft.com/download/6/1/5/6152F995-A2B7-4DF7-8DE3-3DAC8E22CFC2/SystemUpdate_17349_USB.zip) | 
[17489](https://web.archive.org/web/20210614090203/http://download.microsoft.com/download/6/8/F/68FB5F1D-E0AB-4B0C-9457-DC8378ED80CA/SystemUpdate_17489_USB.zip) |
[17502](https://web.archive.org/web/20160819074608/http://download.microsoft.com/download/3/E/B/3EBDD477-ADB7-4171-A294-AD427D169DF9/SystemUpdate_17502_USB.zip) | 
[17511](https://web.archive.org/web/20170412134713/http://download.microsoft.com/download/D/E/F/DEF05D37-65B5-4EB4-8E1C-EC9B8AB21A32/SystemUpdate_17511_USB.zip) | 
[17526](https://web.archive.org/web/20180921203638/http://download.microsoft.com/download/F/F/4/FF41F147-CE31-4665-A71B-83F00C0940B8/SystemUpdate_17526_USB.zip) | 
[17544](https://web.archive.org/web/20191029205342/https://download.microsoft.com/download/2/e/4/2e457a41-d7d5-4403-888e-07d9a3a914aa/SystemUpdate_17544_USB.zip) | 
[17559](https://web.archive.org/web/20191119231337/https://download.microsoft.com/download/b/5/b/b5b2e1bc-a5c7-4e78-9518-e1c59ff738d0/SystemUpdate_17559_USB.zip) | 
[Latest](https://www.xbox.com/system-update-usb) | [Source](https://beta.support.xbox.com/help/xbox-360/console/system-updates-info)
