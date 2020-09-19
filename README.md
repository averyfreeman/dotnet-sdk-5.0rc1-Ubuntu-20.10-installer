# dotnet-sdk-5.0rc1-Ubuntu-20.10-installer
Quick and dirty edit of the dotnet-sdk-5.0rc1 installer script for Ubuntu 20.10

Ubuntu 20.10 is released next month, but the dotnet-sdk 5.0rc1 preview installer wouldn't work on it because it's not officially released, so I figured out what was required to get it working and added it to the script

It downloads and installs libicu66 dependency, and changes dpkg permissions to prevent \_apt sandbox
