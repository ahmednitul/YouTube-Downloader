Project: YouTube Downloader
Author: John Eckman
URL: https://github.com/jeckman/YouTube-Downloader
License: GPL v2 or Later

PHP Scripts to download videos from YouTube.  

NOTE: YouTube Downloader does not work with videos using a cipher signature. 

See https://github.com/jeckman/YouTube-Downloader/issues/9

You can manually visit a web form (the index.php file), enter a YouTube
video id, and get in return a list of links showing the various formats in which
that video can be downloaded. You can simply choose "save link as" or the 
equivalent to download the file. 

Second, you can directly target the getvideo.php script, passing in a videoID and
preferred format, and you will get redirected to the file itself. 

http://example.com/yt/getvideo.mp4?videoid=GkvvH8pBoTg&format=ipad

Potential formats:
 * best = just give me the largest file / best quality
 * free = give the largest version including WebM, lower priority to FLV
 * ipad = ignore WebM and FLV, look for best MP4 file
 
171         webm      audio only  DASH audio  115k , audio@128k (44100Hz), 2.59MiB (worst)
140         m4a       audio only  DASH audio  129k , audio@128k (44100Hz), 3.02MiB
141         m4a       audio only  DASH audio  255k , audio@256k (44100Hz), 5.99MiB
160         mp4       256x144     DASH video  111k , 12fps, video only, 2.56MiB
247         webm      1280x720    DASH video 1807k , 1fps, video only, 23.48MiB
136         mp4       1280x720    DASH video 2236k , 24fps, video only, 27.73MiB
248         webm      1920x1080   DASH video 3993k , 1fps, video only, 42.04MiB
137         mp4       1920x1080   DASH video 4141k , 24fps, video only, 60.28MiB
43          webm      640x360
18          mp4       640x360
22          mp4       1280x720    (best)
140         m4a       audio only  DASH audio , audio@128k (worst)
160         mp4       144p        DASH video , video only
133         mp4       240p        DASH video , video only
134         mp4       360p        DASH video , video only
135         mp4       480p        DASH video , video only
136         mp4       720p        DASH video , video only
17          3gp       176x144     
36          3gp       320x240     
5           flv       400x240     
43          webm      640x360     
18          mp4       640x360     
22          mp4       1280x720    (best)

You can also pass in a specific format number, if you know it. 

Note this approach, because it redirects you to the file itself, currently bypasses the
proxy option, so if your browser/server setup requires the proxy to work these will fail. 
  
Enjoy!

John
