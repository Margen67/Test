### What is the difference between Xenia Canary and Xenia master?

Xenia Canary is a fork of Xenia with changes not present in master that may or may not fix games.
  * *[Full list of changes](https://github.com/xenia-canary/xenia-canary/projects/1)*
#
### What's the difference between canary_experimental, etc?
Most branches serve a specific purpose. For example, `canary_pr` only has changes with an open pull request on xenia master.
Branch              | Purpose
------              | -------
canary_experimental | Changes that don't have a PR open.
canary_pr           | Changes that have a PR open.
canary_base         | Base branch for above branches. (newest)
canary-new          | Newer than old-update.
canary-old-update   | Old, but newer branch. (has some features newer branches don't)
canary-old          | Old canary branch.
canary-linux        | TODO.
canary              | TODO.
clockfreq-test      | TODO.
fixups              | TODO.
import-libraries    | TODO.
new_dashboard_run   | Can run the dashboard. (outdated?)
qt-graphics-window  | TODO.
qt-settings-impl    | TODO.
canary-FFmpeg       | TODO.
qt-updated          | TODO.
stfs-headers-new    | TODO.
|                   |
~~master~~          |
~~gh-pages~~        |
~~systemlink~~      |
~~setthreaddesc~~   |
~~gen_tests~~       |
~~x64-cleanup~~     |
~~qt~~              |
~~texsplit~~        |
~~crash_dumps~~     |
~~vtx_cache~~       |
~~linux~~           |

#
### How do I install Title Update(s)?

  1. Identify Game Title ID. This can be identified by running the game in Xenia.
  <details><summary>Image (click to expand)</summary>

  ![](https://i.imgur.com/Vhz9sCC.png)</details>

  2. Locate your TU folder from your removable storage.
  <details><summary>Image (click to expand)</summary>

  ![](https://i.imgur.com/M4R1SyZ.png)</details>

  3. Copy your TU file from `$TitleUpdate\[TitleID]\000B0000` to `Documents\Xenia\[TitleID]\000B0000`
#
### How do I run the Xbox 360 dashboard?

See [[Dashboard#installation]].
