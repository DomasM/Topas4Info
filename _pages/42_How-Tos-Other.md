---
layout: page
title: Other How-Tos
permalink: /How-Tos/Other/
nolink: true
---


### <a name="Vid006"></a>Device<->zip, automatic configuration changes history
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid006">
    Copy address to this how-to
</button>

<video controls class="video-js vjs-16-9" id="BackupAndRestore">
</video>


### <a name="Vid002"></a>Control multiple devices, manage devices
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002">
    Copy address to this how-to
</button>
<video controls class="video-js vjs-16-9" id="DeviceManagement">
</video>



### <a name="Vid004"></a>Laser control from WinTopas4
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid004">
    Copy address to this how-to
</button>
<video controls class="video-js vjs-16-9" id="LaserControl">
</video>

 In case you want to add Pharos laser which is connected to another PC than Topas4Server is running
1. should have PharosUserApp installed on the PC that is connected to the same local area network (LAN)
2. [Download](https://lightconupdater.blob.core.windows.net/installers/EnablePharosUserAppRestAPI.bat)  and run the script **on the PC where PharosUserApp is installed**. Windows will try to prevent you from running this script with a message 'Windows protected your PC'. Click 'More info' and then 'Run anyway'. Grant Administrator rights. If PharosUserApp is running you will be asked to close it, do so.
3. Follow steps in video




### <a name="Vid005"></a>Add a new group to saved motors positions
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid005">
    Copy address to this how-to
</button>
<video controls class="video-js vjs-16-9" id="SavedMotorPositions" data-setup="{}">
<source src="https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/HowToAddNewSavedMotorPositonsGroup.mp4?sv=2019-12-12&st=2021-05-25T08%3A06%3A21Z&se=2068-05-10T08%3A06%3A00Z&sr=c&sp=rl&sig=erdeW62Gl3KBJ%2Bn6vCwfcwqJKPo%2BHbA2yNnvlmKKzKY%3D" type="video/mp4" />
</video>



<script>
var params = "?sv=2019-12-12&st=2021-05-25T08%3A06%3A21Z&se=2068-05-10T08%3A06%3A00Z&sr=c&sp=rl&sig=erdeW62Gl3KBJ%2Bn6vCwfcwqJKPo%2BHbA2yNnvlmKKzKY%3D";

var links = [
    { Name: "BackupAndRestore", Link: "https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/BackupAndRestore.mp4"},
    { Name: "DeviceManagement", Link: "https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/DeviceManagement.mp4"},
    { Name: "LaserControl", Link: "https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/LaserControl.mp4"},
    { Name: "SavedMotorPositions", Link: "https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/HowToAddNewSavedMotorPositonsGroup.mp4"}
];


function InitializePlayer(link) {  
  videojs(link.Name).src({
    type: 'video/mp4',
    src: link.Link+params
  });
}

links.forEach(link => InitializePlayer(link));

</script>
