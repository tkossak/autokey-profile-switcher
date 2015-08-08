AutoKey-profile-switcher
========================

Script for switching "profiles" (=folders) for [AutoKey](https://code.google.com/p/autokey/). It works by changing the autokey folder (link) to required profile.

Installing
---
1. Make sure you have [AutoKey](https://code.google.com/p/autokey/) installed.
1. Clone git repository and create link to `aks` somewhere in your $PATH for example:

  ```ln -s /usr/local/bin/aks /FULL/PATH/TO/aks ```
  
1. run:

  ```aks --install```
  
  It will create new profile from current AutoKey folder and create link to it.

Using
---
* list all options

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
* create new profile:

  ```aks -c new_profile_name```

* switch AutoKey to new profile:

  ```aks new_profile_name```

  Now you can modify your scripts in AutoKey and they will be saved to your "new_profile_name".
