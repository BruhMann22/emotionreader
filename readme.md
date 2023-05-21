# Emotion Reader

My emotion reader is a camera that can be pointed or used by anyone to read emotions. My emotion reader could help people who can't read facial expressions and understand social situations and feelings more.

![neutral reading on the emotion reader] [Imgur](https://imgur.com/ReDJpoa)

## The Algorithm

First I had to create the camera, and identify it in my code [Imgur](https://imgur.com/vr2SYBz). Then I had to define my task and create my datasets [Imgur](https://imgur.com/kFnY0Vx). After that I needed to define which neural network I was using (ResNet18), and create widgets to display my image training popup. After that I took 24 images each of me being happy, sad, and neutral. Finally I had to code a release of the camera so that the emotion reader could be shut down [Imgur](https://imgur.com/7Kxhd7P).

## Running this project

1. Turn on the nano, go into putty, log in a nvidia, type:

  mkdir -p ~/nvdli-data
  
  echo "sudo docker run --runtime nvidia -it --rm --network host \
    --volume ~/nvdli-data:/nvdli-nano/data \
    --device /dev/video0 \
    nvcr.io/nvidia/dli/dli-nano-ai:v2.0.2-r32.7.1" > docker_dli_run.sh
    
    chmod +x docker_dli_run.sh
    
    ./docker_dli_run.sh
    
    Then enter nvidia as the password, copy the link given in the first row, and paste it into a new tab. Then type dlinano to log in to the Jupyter Lab website. Open the classification_interactive.ipynb, dataset.py, utils.py, and all the folders. Then run all cells except for the last one in the classification_interactive.ipynb, and then click on all the 3 different categories, set epoxy to 10 for each, and train. Then test it out!
2. All libraries are automatically downloaded in the code.

[Demonstration video, I had to do YouTube because StreamLabs made my computer glitch](https://www.youtube.com/watch?v=Vn3zC-feVJA)
