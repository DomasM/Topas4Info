---
layout: page
title: How-Tos for Service Engineer
permalink: /How-Tos/Service-Engineer/
nolink: true
---


### <a name="Vid001"></a>Set current decrease factor for motor (or other advanced properties)
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid001">
    Copy address to this how-to
</button>
<video  controls class="video-js vjs-16-9" id="CurrentDecreaseFactor">
</video>


<script>
var params = "?sv=2020-08-04&st=2021-11-30T13%3A29%3A50Z&se=2047-10-01T12%3A29%3A00Z&sr=c&sp=rl&sig=PXP8Z5IQdevNxwEe8TtsY4jibnf5%2FyetP5sjyxYo8Y4%3D";

var links = [
    { Name: "CurrentDecreaseFactor", Link: "https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/HowToSetCurrentDecreaseFactor.mp4"},
];

function InitializePlayer(link) {  
  videojs(link.Name).src({
    type: 'video/mp4',
    src: link.Link+params
  });
}

links.forEach(link => InitializePlayer(link));

</script>
