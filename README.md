AutoKey-profile-switcher
========================

Script for switching "profiles" (folders) for AutoKey. It works by changing the autokey folder link to different one.  
It doesn't remove original autokey folder if it's not a link.  
Before changing anything, AutoKey is stopped and at the end run again.  
It works for my system - Linux Mint 17 and AutoKey 0.90.4, it may require some tinkering if you have different os.

Installing
---
1. Download aks.sh anywhere and create a link somwhere in your PATH e.g.

  ```
  ln -s /path/to/aks.sh /usr/local/bin/aks
  ```
2. Create new folder where you will keep your AutoKey "profiles" and put the path in the script as variable AK_SCRIPT_FOLDER
3. Change the variable AK_DEFAULT_FOLDER to your default autokey folder e.g. ~/.config/autokey
4. Move your default autokey folder to the AK_SCRIPT_FOLDER e.g:

  ```
  mv ~./config/autokey ~/path/default
  ```

Running AutoKey with new profile
---
It takes one parameter - the name of the folder/profile.  If you have "default" folder in your scripts path run:
```
aks default
```

Creating new profiles
---
Copy your default folder giving it another name and run aks to switch to it:
```
cp ~/path/default ~/path/profile1
aks profile1
```
Then edit the scripts in the AutoKey.
