# Another Instagram Filter (AI-Filter)
This Repository is part of the submission for the JETSON NANO AI SPECIALIST Certificate. 
A [demo](https://www.youtube.com/watch?v=9OX6vN9Tp54) of the project.
## Introduction
 Video processing technology has gained alot of attention in the recent years due to the pandemic and emplyees are forced to work remotely. Despite that the current narrative points towards an end of the pandemic, we predict that working remotely will remain as a standard for many company cultures that have adapted the environment. However, the most frequently used applications for real-time collaborative work such as; Microsoft Teams, Zoom and Slack, does not have handgesture based control for their features. In order to  enhance the user experience we have developed an application that controls, filters that mimics instrgram filters, by handgesture. 

 The program is developed and based on the Mediapipe library and has the follow landmarks of the hand: 
 ![](./imgs/hand_landmarks.png)

 Reference: **https://google.github.io/mediapipe/solutions/hands.html**

 We use miniforge to create anaconda environment on the Jetson Nano

## Hardware
 This project is developed with following hardware: 

 - [Logitech HD Pro C920](https://www.logitech.com/no-no/products/webcams/c920s-pro-hd-webcam.960-001252.html)

 - [JETSON NANO DEVELOPER KIT](https://developer.nvidia.com/embedded/jetson-nano-developer-kit)
 
 - Compatible mouse, display and keyboard (Optional) 
## Install miniforge on JETSON NANO to run jupyter lab
After completing the setup from [Jetson AI Fundamentals Course](https://developer.nvidia.com/embedded/learn/jetson-ai-certification-programs), on the Jetson Nano:
Update and upgrade
```bash
sudo apt update --yes
sudo apt upgrade --yes
```
Get miniforge for aarch64
```bash
   wget https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-aarch64.sh -O ~/miniforge.sh
   bash ~/miniforge.sh -b -p ~/miniforge
   rm ~/miniforge.sh
```
Update Path
```bash
echo "PATH=$PATH:$HOME/miniforge/bin" >> .bashrc
source .bashrc
```

# Usage
## Setup Jupyter Lab
 Clone the repository and change directory to AI_filter
 ```bash
 git clone git@github.com:kjchen93/AI_filter.git
 cd AI_filter
 ```
Create an environment with dependencies specified in env.yml:
    
    conda env create -f env.yml

 Activate the new environment:
    
    conda activate aif

    
 Install the **aif** IPython kernel in order to use in jupyter lab : 
    
    python -m ipykernel install --user --name aif


 Deploy jupyter lab with no browser and open accessibility:

    jupyter lab --no-browser --ip="0.0.0.0"

 Follow the instructions to run jupyter lab on browser. Make sure the the kernel is `aif`.

 Run the notebook. 

 To deactivate the environment, open the terminal and run:
    
    conda deactivate
 ### Note:
 To run on headless, open a jupyter compatible browser and type:
    
    <IP>:8888/lab?
 
 Where `<IP>` is the IP address of the JETSON NANO. 

 #### NB: openCV does not work yet in headless mode with this setup.

## Gestures
The program has 3 modes one without filter, one with a sketch filter and one with a negative filter. The user can use gestures to change between filters and tune the brightness or intensity of the filter. To activate the gestures, the palm of the users right hand must face towards the camera.

 - Tune intensity: 
   - Bring the fingertips towards the palm as if grabing a big dial until a green circle appears. 
   - While green circle is visible, turn clockwise to increase the intensity and counter-clockwise to decrease the intesity
 - Change Filter:
   - Bring the fingertips together towards the center of the palm in a sharp and decisive manner and quickly release from the position. The motion should be analogous to blinking human eye.

## Author

[Kai Chen](github.com/kjchen93)