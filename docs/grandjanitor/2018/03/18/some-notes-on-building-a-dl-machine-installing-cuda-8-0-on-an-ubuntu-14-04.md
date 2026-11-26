---
title: "Some Notes on Building a DL-Machine (Installing CUDA 8.0 on an Ubuntu 14.04)"
date: 2018-03-18
categories: ["deep learning"]
---

# Some Notes on Building a DL-Machine (Installing CUDA 8.0 on an Ubuntu 14.04)

I mostly just follow this [link](https://blog.slavv.com/the-1700-great-deep-learning-box-assembly-setup-and-benchmarks-148c5ebe6415) by Slav Ivanov[. ](https://blog.slavv.com/the-1700-great-deep-learning-box-assembly-setup-and-benchmarks-148c5ebe6415)The build is for a friend, so nothing fancy. The only thing different is my friend got a Titan X instead of a 1080, and he requires Ubuntu 14.04.

As a rule of Linux installation, you can't always follow the instruction as if it is casted in stone. So what I did differently? So I did: 
1. ```
    sudo apt-get update
    ```
2. ```
    sudo apt-get --assume-yes install tmux build-essential gcc g++ make binutils
    sudo apt-get --assume-yes install software-properties-common
    sudo apt-get --assume-yes install git
    ```

    (Notice unlike Slavv, I didn't do an upgrade because upgrade seems to easily screw up CUDA 8.0 installation later on.)
3. So this is a major difference, Slavv suggested to install CUDA directly. No, no, no. What you should do is to make sure driver of your graphic card is installed first. And Ubuntu/Nvidia has good support on it. Following this [thread, ](https://askubuntu.com/questions/813629/ubuntu-14-04-trusty-on-nvidia-titan-x-pascal-cannot-install)I found that installing Titan require updating driving to `nvidia-367`. So I just did an `apt-get install nvidia-367`.
4. At this point if you reboot, you will notice that 14.04 recognize the display card. Usually what it means is the display is in the right resolution. (If the driver is not installed properly, then you will find a display with overlarged icons, etc.)
5. So now, you can test your setting, by typing nvidia-smi. Normally a screen would look like this [one](https://gist.github.com/allenday/57f5746e5126ce80c9f4d580da75549b). If you are running within a GUI, there should be at least one process running on the GPU.
6. Now all good, you now have the driver of the display card, now you can really follow Slavv's procedure : 

    ```
    wget [http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1404/x86_64/cuda-repo-ubuntu1404_8.0.61-1_amd64.deb](http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/cuda-repo-ubuntu1604_8.0.61-1_amd64.deb)
    sudo dpkg -i cuda-repo-ubuntu1404_8.0.61-1_amd64.deb
    sudo apt-get update
    sudo apt-get install cuda-toolkit-8.0
    ```
7. This is the point when I stopped. And I left it to my friend to install more software. Usually, installing display card driver and CUDA are the toughest steps in a Linux software build. So the rest should be quite smooth.

Arthur Chan

Acknowledgement: Thanks for the great post by Slav Ivanov!
