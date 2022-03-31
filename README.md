# Another Instagram Filter (AI-Filter)

## Description

## Hardware

 - Logitech HD Pro C920

 - JETSON NANO DEVELOPER KIT


## Install miniforge on JETSON NANO to run jupyter lab
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

## Setup Jupyter Lab

Create an environment with dependencies specified in env.yml:
    
    conda env create -f env.yml

 Activate the new environment:
    
    conda activate aif

    
 Install the **aif** IPython kernel in order to use in jupyter lab : 
    
    python -m ipykernel install --user --name aif


 Deploy jupyter lab with no browser and open accessibility:

    jupyter lab --no-browser --ip="0.0.0.0"

 Follow the instructions to run jupyter lab on browser

 Make sure the the kernel is `aif`.

 To deactivate the environment, open the terminal and run:
    
    conda deactivate
 ### Note:
 To run on headless, open a jupyter compatible browser and type:
    
    <IP>:8888/lab?
 
 Where `<IP>` is the IP address of the JETSON NANO.

 ## Usage


## Author

Kai Chen