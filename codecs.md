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
 
 RGB v.s. YUV
 
 http://www.sensoray.com/support/appnotes/frame_grabber_capture_modes.htm
 
|option   | value     | description1 | description2|
|-------------|-----------|----------|-------|
| -CRF      | 0-51    | 8-bit    | 0 is lossless, 51 is worst quality|
|          | 0-63    | 10-bit   |   |
| -tune     | film, animation, grain, stillinmage, fastdecode, zerolatency    |    |   |
| -profile:v  | baseline, main    | for old devies   |  usage of -profile:v is incompatible with lossless encoding. |
| -profile:v  | High profile    | modern devies   |  usage of -profile:v is incompatible with lossless encoding. |
         
