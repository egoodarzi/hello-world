## H.264
two **rate control** modes:

  1- Constant Rate Factor (CRF)<br>
  2- Two-Pass ABR

# A- Constant Rate Factor **CRF**:  

to keep the best quality and care less about the file size

  - **single** pass
  - adjust **quantizer** for each frame
  - **not** recommneded for **streaming**
  - CRF ranges 0-51 (8-bit) or 0-63 (10-bit), **0 is lossless, 51 is worst quality** and 23 is default (17-18 is visually lossless)
  - **range is exponential**, increase by +6 resaults in roughly half bitrate.
  - **Choose the highest CRF value** that still provides an acceptable quality.
 
 to configure:
 
 1- choose a **CRF** value<br>
 2- Choose a
 
     - **preset**
     - **tune**
     - **profile**
     
 # B- Two-Pass
 Use this rate control mode if you are targeting a specific output file size, and if output quality from frame to frame is of less importance.
 
 ```

 ```
 
 |option   | value     | description1 | description2|
|-------------|-----------|----------|-------|
| -CRF      | 0-51    | 8-bit    | 0 is lossless, 51 is worst quality|
|          | 0-63    | 10-bit   |   |
| -tune     | film, animation, grain, stillinmage, fastdecode, zerolatency    |    |   |
| -profile:v  | baseline, main    | for old devies   |  usage of -profile:v is incompatible with lossless encoding. |
| -profile:v  | High profile    | modern devies   |  usage of -profile:v is incompatible with lossless encoding. |
         
         
         
 
 RGB v.s. YUV
 
 http://www.sensoray.com/support/appnotes/frame_grabber_capture_modes.htm
 
 https://www.youtube.com/watch?v=SjN_vCDi6_I
 
srt make install
```
Install the project...
-- Install configuration: "Release"
-- Installing: /usr/local/lib/libsrt.so.1.4.3
-- Installing: /usr/local/lib/libsrt.so.1.4
-- Installing: /usr/local/lib/libsrt.so
-- Installing: /usr/local/lib/libsrt.a
-- Installing: /usr/local/include/srt/version.h
-- Installing: /usr/local/include/srt/srt.h
-- Installing: /usr/local/include/srt/logging_api.h
-- Installing: /usr/local/include/srt/access_control.h
-- Installing: /usr/local/include/srt/platform_sys.h
-- Installing: /usr/local/include/srt/udt.h
-- Installing: /usr/local/lib/pkgconfig/haisrt.pc
-- Installing: /usr/local/lib/pkgconfig/srt.pc
-- Installing: /usr/local/bin/srt-live-transmit
-- Up-to-date: /usr/local/bin/srt-live-transmit
-- Installing: /usr/local/bin/srt-file-transmit
-- Up-to-date: /usr/local/bin/srt-file-transmit
-- Installing: /usr/local/bin/srt-tunnel
-- Up-to-date: /usr/local/bin/srt-tunnel
-- Installing: /usr/local/bin/srt-ffplay
```

```
Install the project...
-- Install configuration: "Release"
-- Installing: /root/ffmpeg_build/lib/libsrt.a
-- Installing: /root/ffmpeg_build/include/srt/version.h
-- Installing: /root/ffmpeg_build/include/srt/srt.h
-- Installing: /root/ffmpeg_build/include/srt/logging_api.h
-- Installing: /root/ffmpeg_build/include/srt/access_control.h
-- Installing: /root/ffmpeg_build/include/srt/platform_sys.h
-- Installing: /root/ffmpeg_build/include/srt/udt.h
-- Installing: /root/ffmpeg_build/lib/pkgconfig/haisrt.pc
-- Installing: /root/ffmpeg_build/lib/pkgconfig/srt.pc
-- Installing: /root/ffmpeg_build/bin/srt-live-transmit
-- Up-to-date: /root/ffmpeg_build/bin/srt-live-transmit
-- Installing: /root/ffmpeg_build/bin/srt-file-transmit
-- Up-to-date: /root/ffmpeg_build/bin/srt-file-transmit
-- Installing: /root/ffmpeg_build/bin/srt-tunnel
-- Up-to-date: /root/ffmpeg_build/bin/srt-tunnel
-- Installing: /root/ffmpeg_build/bin/srt-ffplay
```

download from google drive in linux command line

https://medium.com/@acpanjan/download-google-drive-files-using-wget-3c2c025a8b99

ball track

https://medium.com/@gonzacor/ball-tracking-and-detection-in-sports-with-new-yolov5-9f30f5252cf2

https://web.wpi.edu/Pubs/E-project/Available/E-project-042519-133951/unrestricted/MacLeod_Palermo_Panicci_MQP_2019.pdf

https://pdf.sciencedirectassets.com/280203/1-s2.0-S1877050916X0021X/1-s2.0-S1877050916319299/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjED8aCXVzLWVhc3QtMSJGMEQCIBzS3OA6qOh3CZl9djnWwdjlhiSJCRffgwXEV5apVXNmAiBE%2B7aV8xwvlJtylc%2FlKLOtBX0aYQX0heWlPw0CClnf5iqDBAjo%2F%2F%2F%2F%2F%2F%2F%2F%2F%2F8BEAQaDDA1OTAwMzU0Njg2NSIMtFHlL4bEzY9VPebRKtcDEnoQrJ7rYDDVxy200nIqpfvky474%2FTHEcKSLUoTZUHH79OJs94a2Vb1PdGzDttlp5eDNA7vq92cy8BDlsdi8ltFAK9CHljwCxsep7UDApUqTQ8e8xIdJ%2BQ4Z%2FE%2BwrQVEI7PbSVX5BTIuwix6a%2B3Tg9bTP563zOPx84KXfR%2FN9eeVR5HKl27m0hQqKXQf0sS7R%2FdscPk6wnDeo5kq0BqZlA%2F96%2BA%2B1PNRE1nsEjcrzKrEZR5XGkN7UvmHzuz0J7paZRwT1%2FQpm4yJsM8%2FqLuCIeDun2NkLjSU3DNmejmPW%2BHq9L%2BPLL8vPNbUslMFOxEDTxdsHIymOAXOV4k9MPTC6hk7UF%2BzExuhXtw22N7TS%2Bdhbomw0xaO1LpYQ2mv%2FBMggV7YlPnwD%2B4hE%2B%2BlpW7pEg9ahk%2Bms6srbdUbkd2BomBAoxizJ8uhbRnQ5GhLmOapE0176krD5V8Q9zeZqa92hDF62OO5zS7n6s47OMagcekKO43hAOXf8QS8tiHWj84H5T6XjjylZ%2FfgjILCJVXUgi6QNxO9IwlZsC07VJv%2FOsWTHpTCOoxkXBKMJz8dGlAFxpOeIjtiRTVgipQ7KV9j5U%2Fg0aJA60f8BkkZLImxWwaHTlx%2FSn7lMJH04YUGOqYBsuR%2FM%2Bg87bd4zkGlw83HooJ%2FO0OodS4rx5d9MTphZREp5dm2rcP%2BM%2F%2B83%2BIjCYRXQqxAjgIhxYOLLk8ZoaWDb8a6wtz3L6CtOMV23Z%2BOoDM8UCa5IUwp6QbsSACasplFTfb1jrD%2B0PSDarJ8d6LGEVaBjj9r8MbO0Bw%2BhxS3nw%2FVdIJPQb4IcfLrvlRFG8gdy4SO5TNfExvb0jkYkhEKbu4HQ0tiig%3D%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20210603T081809Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTY7V66AALA%2F20210603%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=4872569f3585ad78fe57aab0018d6e8464fbe04e650f1cf47040b4ad907e411f&hash=5930e9c8519ccb1374045bf65cf77ce0c025aeb421efd380ae06f092432743bc&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S1877050916319299&tid=spdf-107fc2df-e6b8-4f54-b5a8-9ea07ab55887&sid=6fef38296ff9294154385fe309283837b866gxrqb&type=client

https://www.researchgate.net/publication/314449012_Application_of_Computer_Vision_in_Cricket_Foot_Overstep_No-ball_Detection

https://www.ijcsi.org/papers/7-3-2-30-35.pdf

https://www.fireblazeaischool.in/blogs/ball-tracking-system-for-cricket/

https://ieeexplore.ieee.org/document/7873086

https://peerj.com/preprints/3402.pdf

