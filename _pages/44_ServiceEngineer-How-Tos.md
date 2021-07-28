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
var params = "?sv=2019-12-12&st=2021-07-28T06%3A17%3A46Z&se=2068-05-02T06%3A17%3A00Z&sr=c&sp=r&sig=XD7n6ZF%2BZcbXAiD5pd7dIVI7b0kxH28KFI6iGGZkV44%3D";

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
