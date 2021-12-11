**Step By Step Installation of FairMOT  on Linux Environment : Case Study- Google Colab**
<br/>

Requirements 
  - Nvidia GPU
  
1. Clone the FairMOT repo
    - git clone https://github.com/microsoft/FairMOT.git
2. Installing FFMpeg
    - sudo apt install ffmpeg
    - sudo apt-get -y install autoconf automake build-essential libass-dev libfreetype6-dev libgpac-dev \
      libsdl1.2-dev libtheora-dev libtool libva-dev libvdpau-dev libvorbis-dev libx11-dev \
      libxext-dev libxfixes-dev pkg-config texi2html zlib1g-dev
3. Install torch and torchvision Libraries for linux enviroments
    - pip install torch==1.4 torchvision==0.5
4. Moving to our cloned repository
    - cd FairMOT 
    - pip install -r requirements.txt
    - cd src/lib/models/networks/DCNv2
    - sh make.sh
5. Download Pretrained Model from google drive and save in FairMOT/src/lib/models
6. Move to Base directory
7. You can input a raw video and get the demo video by running src/demo.py and get the mp4 format of the demo video:
    - !python demo.py mot --load_model lib/models/all_dla34.pth
8. Results of this process can be found in 'FairMOT/results'  folder 
   Working Colab can be found [here](https://colab.research.google.com/drive/1j-UobIDfZBm5aW1TPi2t55WYxVpySab4?usp=sharing) 


    
