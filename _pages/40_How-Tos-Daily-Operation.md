---
layout: page
title: Daily Operation How-Tos
permalink: /How-Tos/Daily-Operation/
nolink: true
video: true
---


### <a name="Vid001"></a>Topas4 Introduction


<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid001">
      Copy address to this how-to
</button>


<video class="video-js vjs-16-9 vjs-default-skin"  id="Introduction" data-setup='{}'>
</video>


### <a name="Vid002"></a>Select interaction(s) to use and create interaction groups

<button class="btn" data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002">
    Copy address to this how-to
</button>

<div class="row">
 Jump to and copy:
  <button class="btn jump-to" onclick="goToSecond('UsingInteractions',15)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=UsingInteractions&time=15">
  Selecting single
  </button>

  <button class="btn jump-to" onclick="goToSecond('UsingInteractions',34)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=UsingInteractions&time=34">
  Selecting multiple
  </button>

  <button class="btn jump-to" onclick="goToSecond('UsingInteractions',47)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=UsingInteractions&time=47">
  Priorities
  </button>

  <button class="btn jump-to" onclick="goToSecond('UsingInteractions',68)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=UsingInteractions&time=68">
  Grouping
  </button>

  <button class="btn jump-to" onclick="goToSecond('UsingInteractions',85)"
  data-clipboard-text="{{site.fullUrl}}{{page.url}}#Vid002?name=UsingInteractions&time=85">
  Message window
  </button>
</div>


<video  controls controlsList="nodownload" class="video-js vjs-16-9" id="UsingInteractions">
</video>



<script>
var params = "?sv=2019-12-12&st=2021-11-30T13%3A29%3A50Z&se=2047-10-01T12%3A29%3A00Z&sr=c&sp=rl&sig=PXP8Z5IQdevNxwEe8TtsY4jibnf5%2FyetP5sjyxYo8Y4%3D";

var links = [
    { Name: "Introduction", Link: "https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/Introduction.mp4"},
    { Name: "UsingInteractions", Link: "https://lightconupdater.blob.core.windows.net/topas4infopage/Videos/UsingInteractions.mp4"}
];


function InitializePlayer(link) {

var myVid =   videojs(link.Name);
myVid.src({
    type: 'video/mp4',
    src: link.Link+params
  });

myVid.controls("true");
myVid.preload("auto");
}



links.forEach(link => InitializePlayer(link));

var noDownload = function() {
    var videoElem = document.getElementsByTagName("video");
    for (x in videoElem) {
  	    if (isNaN(x) == true) {
            continue;
        }        
  	    videoElem[x].setAttribute("controlsList", "nodownload");
    }
}
noDownload();

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
