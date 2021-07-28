---
layout: page
title: Calibration How-Tos
permalink: /How-Tos/Calibration/
nolink: true
---


### <a name="Vid010"></a>Calibration overview
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid010">
    Copy address to this how-to
</button>

<div class="row">
Jump to and copy:
  <button class="btn jump-to" onclick="goToSecond('CalibrationOverview',18)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid010?name=CalibrationOverview&time=18">
  Access level
  </button>

  <button class="btn jump-to" onclick="goToSecond('CalibrationOverview',39)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid010?name=CalibrationOverview&time=39">
  Calibration windows
  </button>
</div>

<video  controlsList="nodownload" controls class="video-js vjs-16-9" id="CalibrationOverview">
</video>



### <a name="Vid001"></a>Calibration tuning
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid001">
    Copy address to this how-to
</button>

<div class="row">
Jump to and copy:
  <button class="btn jump-to" onclick="goToSecond('CalibrationTuning',16)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid001?name=CalibrationTuning&time=16">
  Tuning and keyboard shortcuts
  </button>

  <button class="btn jump-to" onclick="goToSecond('CalibrationTuning',112)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid001?name=CalibrationTuning&time=112">
  Curve offset
  </button>
</div>

<video controls controlsList="nodownload" class="video-js vjs-16-9" id="CalibrationTuning">
</video>


### <a name="Vid002"></a>Modify calibration, correct wavelengths to match actual output
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002">
    Copy address to this how-to
</button>

<div class="row">
Jump to and copy:
  <button class="btn jump-to" onclick="goToSecond('CalibrationModifications',15)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=CalibrationModifications&time=15">
  Wavelength correction
  </button>

  <button class="btn jump-to" onclick="goToSecond('CalibrationModifications',58)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=CalibrationModifications&time=58">
  Respacing the points
  </button>

  <button class="btn jump-to" onclick="goToSecond('CalibrationModifications',82)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=CalibrationModifications&time=82">
  Extending range
  </button>

  <button class="btn jump-to" onclick="goToSecond('CalibrationModifications',130)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=CalibrationModifications&time=130">
  Change pump wl and regenerate idler
  </button>
</div>


<video controls controlsList="nodownload" class="video-js vjs-16-9" id="CalibrationModifications">
</video>



### <a name="Vid005"></a>Named motor positions
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid005">
    Copy address to this how-to
</button>

<div class="row">
Jump to and copy:
  <button class="btn jump-to" onclick="goToSecond('NamedMotorPositions',18)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid005?name=NamedMotorPositions&time=18">
  Modify named positions
  </button>

  <button class="btn jump-to" onclick="goToSecond('NamedMotorPositions',60)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid005?name=NamedMotorPositions&time=60">
  Assign to calibration
  </button>

  <button class="btn jump-to" onclick="goToSecond('NamedMotorPositions',100)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid005?name=NamedMotorPositions&time=100">
  Separation configuration
  </button>
</div>


<video controls controlsList="nodownload" class="video-js vjs-16-9" id="NamedMotorPositions">
</video>



<script>
var params = "?sv=2019-12-12&st=2021-07-28T06%3A17%3A46Z&se=2068-05-02T06%3A17%3A00Z&sr=c&sp=r&sig=XD7n6ZF%2BZcbXAiD5pd7dIVI7b0kxH28KFI6iGGZkV44%3D";

var links = [
    { Name: "CalibrationOverview", Link: "https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/CalibrationOverview.mp4"},
    { Name: "CalibrationTuning", Link: "https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/CalibrationTuning.mp4"},  
    { Name: "CalibrationModifications", Link: "https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/CalibrationModifications.mp4"},   
    { Name: "NamedMotorPositions", Link: "https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/NamedMotorPositions.mp4"},
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
