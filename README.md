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

Mount:
idevice pair
ifuse <mountingpoint>

Unmount:
fisermount -u <mountingpoint>
