### Not present in Xenia master:

#### CPU:
##### Workaround for Unreal Engine 3 titles to run, try disabling if other games have problems:
  * `UE_Workaround = true`

#
#### General:
##### FPS in titlebar:
  * `fps_titlebar = true`

#
#### HID:
##### When using passthru, sends keyup events when keys are released. Some games like SR1 don't like seeing these, but dash won't work properly without them:
  * `keyboard_keyup = true`
##### Maybe useful for debug games, disables keyboard->gamepad emulation and forwards exact keyboard events to game (note that Xenia keybinds, eg. H to show FPS, will still be in effect!):
  * `keyboard_passthru = false`

#
#### Kernel:
##### Enable the dashboard initial setup/OOBE:
  * `xconfig_initial_setup = false`

#
#### Profiles:
##### XUID/state (user_0-3):
  `* user_0_state = 1`
      * User 0 signin state (0/1/2)

  `* user_0_xuid = ''`
      * XUID of the profile to use for user 0 (E0...

#### UI:
  * `window_height = 720`
  * `window_width = 1280`

#
#### Video:
##### avpack (video mode):
  * `avpack = 8`