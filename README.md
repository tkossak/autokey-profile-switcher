AutoKey-profile-switcher
========================

[![GuardRails badge](https://badges.production.guardrails.io/tkossak/autokey-profile-switcher.svg)](https://www.guardrails.io)

Script for switching "profiles" (=folders) for [AutoKey](https://code.google.com/p/autokey/). It works by changing the autokey folder (link) to required profile.

Installing
---
1. Make sure you have [AutoKey](https://code.google.com/p/autokey/) installed.
2. Clone git repository and create link to `aks` somewhere in your $PATH for example:

  ```ln -s /FULL/PATH/TO/aks /usr/local/bin/aks```
  
3. run:

  ```aks --install```
  
  It will create new profile from current AutoKey folder and create link to it.

Using
---
* create new profile:

  ```aks -c mplayer```

* switch to new profile:
  
  ```aks mplayer```

  You can modify your scripts in AutoKey now and they will be saved to your new profile "mplayer".

* list all profiles

  ```aks -l```
  
* get help and all options

  ```aks -h```
  
  Result:

  ```
  aks - change AutoKey profiles
  Usage:
    aks [OPTIONS] [PROFILE_NAME]

  OPTIONS:
    -h | --help : print this help
    --install   : install AKS (create profile from current AutoKey folder, replace it with link)
    -l          : list available profiles
    -c <NAME>   : create new profile from default one
    -r <NAME>   : remove profile
    -k          : kill AutoKey process
    -p          : print profiles directory path
  ```
