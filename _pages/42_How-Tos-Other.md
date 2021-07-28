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

<div class="row">

Jump to and copy:

  <button class="btn jump-to" onclick="goToSecond('BackupAndRestore',12)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid006?name=BackupAndRestore&time=12">
  Automatic Backup
  </button>

  <button class="btn jump-to" onclick="goToSecond('BackupAndRestore',76)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid006?name=BackupAndRestore&time=76">
  Zipped configuration
  </button>

</div>

<video controls controlsList="nodownload" class="video-js vjs-16-9" id="BackupAndRestore">
</video>


### <a name="Vid002"></a>Control multiple devices, manage devices
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002">
    Copy address to this how-to
</button>

<div class="row">

Jump to and copy:

  <button class="btn jump-to" onclick="goToSecond('DeviceManagement',8)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=DeviceManagement&time=8">
  Control windows
  </button>

  <button class="btn jump-to" onclick="goToSecond('DeviceManagement',30)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=DeviceManagement&time=30">
  Color / Nickname
  </button>

  <button class="btn jump-to" onclick="goToSecond('DeviceManagement',42)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=DeviceManagement&time=42">
  Multiple devices
  </button>

  <button class="btn jump-to" onclick="goToSecond('DeviceManagement',60)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=DeviceManagement&time=60">
  Mini view
  </button>

  <button class="btn jump-to" onclick="goToSecond('DeviceManagement',83)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=DeviceManagement&time=83">
  Demo device
  </button>

  <button class="btn jump-to" onclick="goToSecond('DeviceManagement',104)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=DeviceManagement&time=104">
  Launch from zipped config
  </button>

  <button class="btn jump-to" onclick="goToSecond('DeviceManagement',128)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=DeviceManagement&time=128">
  SelfHosts manager
  </button>
</div>

<video controls controlsList="nodownload" class="video-js vjs-16-9" id="DeviceManagement">
</video>



### <a name="Vid004"></a>Laser control from WinTopas4
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid004">
    Copy address to this how-to
</button>

<div class="row">
Jump to and copy:
  <button class="btn jump-to" onclick="goToSecond('LaserControl',14)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid004?name=LaserControl&time=14">
  Enable controls
  </button>

  <button class="btn jump-to" onclick="goToSecond('LaserControl',24)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid004?name=LaserControl&time=24">
  Overview
  </button>

  <button class="btn jump-to" onclick="goToSecond('LaserControl',75)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid004?name=LaserControl&time=75">
  Laser setup
  </button>

  <button class="btn jump-to" onclick="goToSecond('LaserControl',97)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid004?name=LaserControl&time=97">
  Assign laser preset
  </button>

  <button class="btn jump-to" onclick="goToSecond('LaserControl',122)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid004?name=LaserControl&time=122">
  Safe shutter switching
  </button>

</div>

<video controls controlsList="nodownload" class="video-js vjs-16-9" id="LaserControl">
</video>

 In case you want to add Pharos laser which is connected to another PC than Topas4Server is running
1. should have PharosUserApp installed on the PC that is connected to the same local area network (LAN)
2. [Download](https://lightconupdater.blob.core.windows.net/installers/EnablePharosUserAppRestAPI.bat)  and run the script **on the PC where PharosUserApp is installed**. Windows will try to prevent you from running this script with a message 'Windows protected your PC'. Click 'More info' and then 'Run anyway'. Grant Administrator rights. If PharosUserApp is running you will be asked to close it, do so.
3. Follow steps in video




### <a name="Vid005"></a>Add a new group to saved motors positions
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid005">
    Copy address to this how-to
</button>
<video controls controlsList="nodownload" class="video-js vjs-16-9" id="SavedMotorPositions">
</video>



<script>
var params = "?sv=2019-12-12&si=topas4infopage-sarunui&sr=c&sig=68DczjOkPucI%2BvzhV%2Btio15athKyrecmW9cuZadFHuI%3D";

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



if (location.hash != ""){
try {

if (findGetParameter("name") != "" && findGetParameter("time") != ""){
  goToSecond(findGetParameter("name"),findGetParameter("time"));
}

var myHash = window.location.hash.split("?")[0];
if (myHash != ""){
  scrollTo(myHash);
}
} catch {}
}


function scrollTo(hash) {
    location.hash =hash;
}

function findGetParameter(parameterName) {
    var result = "",
        tmp = [];

    window.location.hash
        .split("?")[1]
        .split("&")
        .forEach(function (item) {
          tmp = item.split("=");          
          if (tmp[0] === parameterName) result = decodeURIComponent(tmp[1]);
        });

    return result;
}

function goToSecond(name,time){
  videojs(name).currentTime(time);
}

</script>
