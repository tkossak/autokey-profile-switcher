AutoKey-profile-switcher
========================

Script for switching "profiles" (folders) for AutoKey.  
It doesn't remove original autokey folder if it's not a link.  
It takes one parameter - the name of the folder.  
Before changing AutoKey is stopped and then restarted.  

Installing
---
Download aks.sh anywhere and create a link somwhere in your path:
```
ln -s /path/to/aks.sh /usr/local/bin/aks
```

Running
---
If you have "default" folder in your scripts path:
```
aks default
```

