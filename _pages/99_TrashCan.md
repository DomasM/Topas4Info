---
layout: page
title: Random
permalink: /Random/
nolink: true
---


### <a name="Vid007"></a>GPP quick demo
<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid001">
    Copy address to this how-to
</button>
<video   controls class="video-js vjs-16-9" id="GPPQuickDemo">
</video>


<script>
var params = "?sv=2019-12-12&st=2021-05-25T08%3A06%3A21Z&se=2068-05-10T08%3A06%3A00Z&sr=c&sp=rl&sig=erdeW62Gl3KBJ%2Bn6vCwfcwqJKPo%2BHbA2yNnvlmKKzKY%3D";

var links = [
    { Name: "CurrentDecreaseFactor", Link: "https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/GPPQuickDemo.mp4"},
];

function InitializePlayer(link) {  
  videojs(link.Name).src({
    type: 'video/mp4',
    src: link.Link+params
  });
}

links.forEach(link => InitializePlayer(link));

</script>
