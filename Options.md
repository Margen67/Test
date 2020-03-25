*[Xenia Master Options](https://github.com/xenia-project/xenia/wiki/Options)*

---
#### How to use:
* Go to `Documents\Xenia` and open `xenia-canary-config.toml` in a text editor like [Notepad++](https://notepad-plus-plus.org/download/).
    * If `portable.txt` is present it will be in the same directory as xenia.exe.
    * Per-game configs go in `config\TitleID.config.toml`.
* For launchers/frontends like [Bottlenose](https://github.com/quinton-ashley/bottlenose) you can use the `--config` launch parameter to specify what config to use.
    * To launch specific games, add the path to the game before the launch options. For example:
      ```cmd
      xenia-canary.exe path/to/game/default.xex --vsync=false
      ```
#
### Canary-exclusive options:
#### CPU:
##### Workaround for Unreal Engine 3 titles to run:
| `UE_Workaround` =             | `bool`
| -----------------             | ----- 
| On *(default)*                | `true`
| Off *(needed for some games)* | `false`

#### General:
##### FPS in titlebar:
| `fps_titlebar` = | `bool`
| ---------------- | ------
| On *(default)*   | `true`
| Off              | `false`

#### HID:
##### Maybe useful for debug games, disables keyboard->gamepad emulation, and forwards exact keyboard events to guest. Note that keybinds, eg. H to show FPS, will still be in effect:
| `keyboard_passthru` = | `bool`
| --------------------- | ------
| Off *(default)*       | `false`
| On                    | `true`
##### Sends keyup events when keys are released when using passthru. Some games like Saints Row 1 don't like seeing these, but the dashboard won't work properly without them:
| `keyboard_keyup` = | `bool`
| ------------------ | ------
| On *(default)*     | `true`
| Off                | `false`

#### Kernel:
##### Dashboard initial setup/OOBE:
| `xconfig_initial_setup` = | `bool`
| ------------------------- | ------
| Disabled *(default)*      | `false`
| Enabled                   | `true`

#### Profiles:
##### Signin state of (user_0-3):
| `user_#_state` =      | `#`
| ----------------      | :-:
| Signed out            | 0
| Signed in *(default)* | 1
| Signed in+Xbox Live   | 2
##### XUID of (user_0-3) [E0...]:
| `user_#_xuid` = | `#`
| --------------- | ---

#### UI:
##### Window height/width:
| `window_`  | `#`
| ---------  | ---
| `height` = | `720` *(default)*
| `width` =  | `1280` *(default)*

#### Video:
##### avpack (video mode):
| `avpack` =               | `#`
| --------                 | :-:
| HDMI *(default)*         | `8`
| TV PAL-60                | `7`
| VGA                      | `6`
| PAL-60 Composite/S-Video | `5`
| HDMI+A                   | `4`
| 480p Component(HD)       | `3`
| PAL-60 SCART             | `2`
|                          | ~~`1`~~
| PAL-60 Component(SD)     | `0`