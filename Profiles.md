# Profiles

Since 10th January 2020 the main canary branch now has support for Xbox 360 profiles - allowing Xenia to read from & write to the same profile files that an actual Xbox 360 console uses!

By default a XeniaUser0 profile will be generated for you, but if wanted you can easily make use of an existing profile instead, or create a profile by using a tool such as [Velocity](https://github.com/Gualdimar/Velocity/releases/tag/xex%2Biso-branch) or Horizon, etc.

### Using existing/created profiles

For this Xenia just needs to access the **E000xxxxxxxxxxx** file belonging to your profile.
Velocity/Horizon should create profiles in this format automatically, while extracting them from your Xbox 360 should be similar to extracting a HDD-installed game for use with Xenia.

Once you have the E000 file, just copy and paste it into the "**Content\FFFE07D1\00000001\\**" folder inside Xenia's user directory (**Documents\Xenia\\** by default).  
(If the folder doesn't exist, running the latest canary build should create it for you)

If there's already E000 files/folders inside this directory, you can either delete them all and replace them with your E0000 file (which should then sign you in to your profile automatically)

Or you can keep any existing profiles as-is, and just edit the config file to "sign-in" a user to this account.

Once Xenia has seen your newly-added profile for the first time, a new folder with the name "**[E000-filename].dir**" will be created - this is the folder where any changes made by Xenia will take place.  
Eg. achievements unlocked, profile settings changed, etc: all will be written into this ".dir" folder, leaving your original E0000 file untouched.  
This gives you an easy way to restore your profile in case Xenia breaks something - just delete the ".dir" folder, and next launch Xenia will recreate it from your original profile file!

### Signing-in users

Signing users into specific profiles can be done by editing the **xenia-canary-config.toml** config file, inside the [Profiles] section should be the following lines, for all 4 user slots:
```
user_X_state = 0
user_X_xuid = ''
```

To sign a user-slot into a profile, just set the state to either 1 (**signed-in offline**) or 2 (**online**), and then copy the E000 filename into the XUID field, eg:
```
user_1_state = 2
user_1_xuid = 'E000004D9328DFF3'
```

If the state is non-zero, but an XUID isn't set, Xenia will either try signing the user into an available non-signed-in profile, or if no profiles are available will generate a XeniaUser profile for the user.

### Using a Xenia profile on Xbox 360

Though this isn't recommended right now, it should be possible for profiles created/modified by Xenia to be used on a real Xbox360, you'll just need to find some way to package the ".dir" files into an STFS package that the Xbox can read.  
(Velocity/Horizon might allow doing this, maybe replacing the files of an existing profile would be easiest?)

Note that using a profile modified by Xenia on Xbox Live is highly discouraged - Xbox Live has a ton of protections against profile-modding, and Xenia doesn't make any attempt to overcome these - you've been warned!