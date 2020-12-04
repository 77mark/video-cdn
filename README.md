## 视频床-jsdeliver
- https://cdn.jsdelivr.net/gh/Ysnsn/video-cdn/001.m3u8
- https://cdn.jsdelivr.net/gh/lete114/CDN2/video/4.m3u8
````
<script src="https://cdn.jsdelivr.net/npm/hls.js"></script>
<video id="video" preload muted loop autoplay style="height: 100%;width: 100%;object-fit: cover;">
</video>
<script>
  var video = document.getElementById('video');
  var videoSrc = 'https://cdn.jsdelivr.net/gh/Ysnsn/video-cdn/001.m3u8';
  if (Hls.isSupported()) {
    var hls = new Hls();
    hls.loadSource(videoSrc);
    hls.attachMedia(video);
    hls.on(Hls.Events.MANIFEST_PARSED, function() {
      video.play();
    });
  }
</script>
````
<script src="https://cdn.jsdelivr.net/npm/hls.js"></script>
<video id="video" preload muted loop autoplay style="height: 100%;width: 100%;object-fit: cover;">
</video>
<script>
  var video = document.getElementById('video');
  var videoSrc = 'https://cdn.jsdelivr.net/gh/Ysnsn/video-cdn/001.m3u8';
  if (Hls.isSupported()) {
    var hls = new Hls();
    hls.loadSource(videoSrc);
    hls.attachMedia(video);
    hls.on(Hls.Events.MANIFEST_PARSED, function() {
      video.play();
    });
  }
</script>