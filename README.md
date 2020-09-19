# dotnet-sdk-5.0rc1-Ubuntu-20.10-installer
Quick and dirty edit of the dotnet-sdk-5.0rc1 installer script for Ubuntu 20.10

Ubuntu 20.10 is released next month, but the dotnet-sdk 5.0rc1 preview installer wouldn't work on it because it's not officially released, so I figured out what was required to get it working and added it to the script

It downloads and installs libicu66 dependency, and changes dpkg permissions to prevent \_apt sandbox

Note:  The values are hardcoded, not os-dependent variables, so it's not suitable for other distros

### Instructions:

```
$ mkdir empty-directory && cd empty-directory 

$ wget https://raw.githubusercontent.com/averyfreeman/dotnet-sdk-5.0rc1-Ubuntu-20.10-installer/261df27fd670c052788874785ca197e7d4b0decb/install-dotnet-preview-groovy.sh

$ chmod + x install-dotnet-preview-groovy.sh

$ sudo su

# ./install-dotnet-preview-groovy.sh

# exit

$ dotnet --info
```

Original instructions located here:  https://github.com/dotnet/core/blob/master/release-notes/5.0/preview/5.0.0-rc.1-install-instructions.md
