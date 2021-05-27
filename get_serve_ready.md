## some links
- git repo:
  - [srt](https://github.com/Haivision/srt.git)<br>
  - [srt-live-server](https://github.com/Edward-Wu/srt-live-server.git)<br>
  - [ffmpeg](https://github.com/FFmpeg/FFmpeg.git)
- guides:
  - [build ffmpeg from source](https://trac.ffmpeg.org/wiki/CompilationGuide/Ubuntu)

### install open vmware tools
sudo apt update<br>
sudo apt install open-vm-tools-desktop

### install openssh server

  ```
  sudo apt update
  sudo apt install openssh-server
  ```
### install SRT
clone the repository from Github
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install tclsh pkg-config cmake libssl-dev build-essential
./configure
make
make install
```
### install ffmpeg (from source)
follow the instructions in this guaide : [complete guide](https://trac.ffmpeg.org/wiki/CompilationGuide/Ubuntu)<br>
1- get the dependences<br>
2- compile and install

   I follow the simple method:<br>
    
     sudo apt-get install nasm
     sudo apt-get install libx264-dev
    
# EXTRA DRAFT    
```
sudo apt-get install libssl-dev
cd ~/ffmpeg_sources
git clone --depth 1 https://github.com/Haivision/srt.git
mkdir srt/build
cd srt/build
cmake -DCMAKE_INSTALL_PREFIX="$HOME/ffmpeg_build" -DENABLE_C_DEPS=ON -DENABLE_SHARED=OFF -DENABLE_STATIC=ON ..
make
make install
```
