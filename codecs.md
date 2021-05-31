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
