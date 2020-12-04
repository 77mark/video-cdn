## 视频床-jsdeliver
- https://cdn.jsdelivr.net/gh/Ysnsn/video-cdn/001.m3u8
- https://cdn.jsdelivr.net/gh/lete114/CDN2/video/4.m3u8

````
ffmpeg.exe -y -i 002.mp4 -vcodec copy -acodec copy -vbsf h264_mp4toannexb 002.ts
ffmpeg -i 002.ts -c copy -map 0 -f segment -segment_list 002.m3u8 -segment_time 4 002%03d.ts
````

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
