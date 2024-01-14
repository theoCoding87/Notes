lampp yt mvc
when ready: do it in a docker container and make the index.php available in browser, while having php only installed in docker container.

then go to laradock.

------------------------------

Docker MongoDB 
sudo docker start <containername>
sudo docker exe -it <containername> bash

Ubuntu live does not start Firefox Instance
  Live mode breaks apparmor
  How it effects the usage:
  User is not allowed to start Firefox on Ubuntu Live with persistent Storage.

  Workaround: 
  create folder: 
  sudo mkdir /lib/systemd/system/apparmor.service.d

  open file and insert following two lines:
  sudo gedit /lib/systemd/system/apparmor.service.d/30_live_mode.conf

[Unit]
ConditionPathExists=

  (ignore failure-messages)
  Save and Reboot.



Windows Start-Script-Path:
C:\Users\user\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup\script.bat
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


iFuse
Dateizugriff auf iPhone, von Linux

Mount
~$ idevicepair pair
~$ ifuse <mountingpoint>

Unmount: 
~$ fusermount -u <mountingpoint>

  
  youtube-dl
pip install git+https://github.com/ytdl-org/youtube-dl.git@master#egg=youtube_dl --force-reinstall

Wallpaper Background Color #15908E

Docker Engine on new Mint installation
""""""""""""""""""""""""""""""""""""""
console apt-get update says:
E: The repository 'https://download.docker.com/linux/ubuntu vanessa Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
-> solution: change "vanessa" to "jammy" in file /etc/apt/sources.list.d/docker.list
