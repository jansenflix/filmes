<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>Video Player</title>
<style>
.wide {
    width: 700px;
    height: 450px;
	margin:20px auto;
}

.wide video {
    width: 700px;
    height: 440px;
	background:rgb(11, 22, 1);
}
h1 {  font-family: Helvetica, Arial, sans-serif;  text-align: center; font-size:50px; margin-top:20px; color:#fff;
	  text-shadow: 2px 2px 0px rgba(255,255,255,.7), 5px 7px 0px rgba(0, 0, 0, 0.1); 
}
video::-webkit-media-controls-panel{
	background:rgba(0, 0, 0, 0.1)
	}
video::-webkit-media-controls-current-time-display{color:#fff}
video::-webkit-media-controls-time-remaining-display{color:#fff}
</style>
<script src="./script.js"></script>
<script>
$( document ).ready(function() {
var adManager = function () {
    var vid = document.getElementById("vid1564730217"),
        adSrc = "./entrada.mp4",
        src;

    var adEnded = function () {
        vid.removeEventListener("ended", adEnded, false);
        vid.src = src;
        vid.load();
        vid.play();
 $('<style>video::-webkit-media-controls-play-button{display:block}</style>').appendTo('head');        
$('<style>video::-webkit-media-controls-current-time-display{margin-left:0px}</style>').appendTo('head');
$('<style>video::-webkit-media-controls-mute-button{display:block}</style>').appendTo('head');
$('<style>video::-webkit-media-controls-volume-slider{display:block}</style>').appendTo('head');
$('<style>video::-webkit-media-controls-mute-button{display:block}</style>').appendTo('head');

$(window).keypress(function(e) {
  var video = document.getElementById("vid1564730217");
  if (e.which == 32) {
    if (video.paused == true)
      video.play();
    else
      video.pause();
  }
});
$('#vid1564730217').click(function(){this.paused?this.play():this.pause();});

    };
    return {
        init: function () {
            src = vid.src;
            vid.src = adSrc;
            vid.load();
            vid.addEventListener("ended", adEnded, false);
$('<style>video::-webkit-media-controls-play-button{display:none}</style>').appendTo('head')
$('<style>video::-webkit-media-controls-mute-button{display:none}</style>').appendTo('head');
$('<style>video::-webkit-media-controls-current-time-display{margin-left:20px}</style>').appendTo('head');
$('<style>video::-webkit-media-controls-volume-slider{display:none}</style>').appendTo('head');
$('<style>video::-webkit-media-controls-mute-button{display:none}</style>').appendTo('head');
	}};
   }().init();		
});
</script>
</head>

<body background="../background2.png">
<h1>JANSENFLIX</h1>
<div class="wide">
    <div class="content">
        <video id="vid1564730217" preload="none" autobuffer poster="https://www.fdcomunicacao.com.br/wp-content/uploads/2019/08/sony-homem-aranha.jpg" controls controlsList="nodownload"
        src="https://tinyurl.com/waw93ck" autoplay>
        
            <source src="https://commondatastorage.googleapis.com/gtv-videos-bucket/CastVideos/mp4/BigBuckBunny.mp4" type="video/mp4">
		</video>
    </div>
</div>
</body>
</html>
