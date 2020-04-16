### What is the difference between Xenia Canary and Xenia master?
Xenia Canary is a fork of Xenia with changes not present in master, such as the Unreal Engine workaround.

*[Full list of changes](https://github.com/xenia-canary/xenia-canary/projects/1)*

#
### How to install Title Update(s)
  1. Identify Game Title ID. This can be identified by running the game in Xenia.

<details><summary>Image (click to expand)</summary>

![](https://i.imgur.com/Vhz9sCC.png)
</details>

  2. Locate your TU folder from your removable storage.

<details><summary>Image (click to expand)</summary>

![](https://i.imgur.com/M4R1SyZ.png)
</details>

  3. Copy your TU file from `$TitleUpdate\[TitleID]\000B0000` to `Documents\Xenia\[TitleID]\000B0000`

#
### How to install the Xbox 360 dashboard
#### Prerequisites:
  * xextool
  * 7-Zip
  * Xbox 360 Dashboard 1888
  1. Extract the dashboard to the same directory as `xextool.exe`
  2. Open cmd and run the following:
  ```cmd
  xextool -d . xam.xex
  ```
  3. Add the `.xzp` file extension to `gamercrd`, `shrdres`, and `xam`
  4. Run `dash.xex`

#### TODO: Updating from 1888
  * **THIS REQUIRES 1888 AS A BASE!**
  * Xenia Canary can only run dashboards up to ~12625. Newer versions might not work.

<!--
Official dashboards | Info
------------------- | ----
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
-->
[Latest](https://www.xbox.com/system-update-usb) | [Source](https://beta.support.xbox.com/help/xbox-360/console/system-updates-info)
