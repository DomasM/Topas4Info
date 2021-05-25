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
<video  controls class="video-js vjs-16-9" id="CalibrationOverview">
</video>



### <a name="Vid001"></a>Calibration tuning
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid001">
    Copy address to this how-to
</button>
<video controls class="video-js vjs-16-9" id="CalibrationTuning">
</video>


### <a name="Vid002"></a>Modify calibration, correct wavelengths to match actual output
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002">
    Copy address to this how-to
</button>
<video controls class="video-js vjs-16-9" id="CalibrationModifications">
</video>



### <a name="Vid005"></a>Named motor positions
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid005">
    Copy address to this how-to
</button>
<video controls class="video-js vjs-16-9" id="NamedMotorPositions">
</video>



<script>
var params = "?sv=2019-12-12&st=2021-05-25T08%3A06%3A21Z&se=2068-05-10T08%3A06%3A00Z&sr=c&sp=rl&sig=erdeW62Gl3KBJ%2Bn6vCwfcwqJKPo%2BHbA2yNnvlmKKzKY%3D";

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

</script>
