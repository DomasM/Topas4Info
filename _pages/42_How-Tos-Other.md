---
layout: page
title: Other How-Tos
permalink: /How-Tos/Other/
nolink: true
---



### <a name="Vid001"></a>Control device from smartphone/tablet via webpage
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid001">
    Copy address to this how-to
</button>
<video  controls="controls">
<source src="https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/WebpageControl.mp4" type="video/mp4" />
</video>

All computers, smartphones and tablets must be connected to the same local area network (LAN).


### <a name="Vid002"></a>Control the same device from multiple clients/computers
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002">
    Copy address to this how-to
</button>
<video  controls="controls">
<source src="https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/MultipleUserApps.mp4" type="video/mp4" />
</video>

All computers must be connected to the same local area network (LAN). Connection from another computer will require to confirm authentication, which is done be repeatedly puling and pushing devices interlock switch until authentication is complete.





### <a name="Vid003"></a>Use smooth wavelength scanner
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid003">
    Copy address to this how-to
</button>
<video  controls="controls">
<source src="https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/HowToUserSmoothScanner.mp4" type="video/mp4" />
</video>


### <a name="Vid004"></a>Enable Pharos laser control from WinTopas4
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid004">
    Copy address to this how-to
</button>

1. You should have PharosUserApp installed on the PC that is connected to the same local area network (LAN) as PC with Topas4Server application (might be the same PC too, of course)
2. [Download](https://lightconupdater.blob.core.windows.net/installers/EnablePharosUserAppRestAPI.bat)  and run the script **on the PC where PharosUserApp is installed**. Windows will try to prevent you from running this script with a message 'Windows protected your PC'. Click 'More info' and then 'Run anyway'. Grant Administrator rights. If PharosUserApp is running you will be asked to close it, do so.
3. You should see something like this in command line window:
```bat
C:\WINDOWS\system32>ipconfig /all   | find "Preferred"   | find "IPv4"   & pause
   IPv4 Address. . . . . . . . . . . : 192.168.8.191(Preferred)
Press any key to continue . . .
```
4. Find window of Topas4Server application you want to associate with Pharos. Press 'Stop', then F11.
5. In newly opened File Explorer window you will see file LaserControl.json, open it with notepad or more reasonable text editor of your choice.
6. Enter correct IP address. If you have PharosUserApp and Topas4Server on the same PC, just enter 127.0.0.1, otherwise enter value you saw in command line window (192.168.8.191 in this example). Now your file should look like this:
```json
{
  "Type": "PharosUserAppV2_9_Comp",
  "Address": "192.168.8.191"
}
```
7. Save changes to the file, click 'Start' in Topas4ServerApplication.
8. Now you can control Pharos from WinTopas4. To show laser controls, click on cog icon next to shutter button and turn on 'Show laser controls'.



