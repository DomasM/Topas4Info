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
var params = "?sv=2019-12-12&si=topas4infopage-sarunui&sr=c&sig=68DczjOkPucI%2BvzhV%2Btio15athKyrecmW9cuZadFHuI%3D";

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
