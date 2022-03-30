# Another Instagram Filter (AI-Filter)

## Hardware

 - Logitech HD Pro C920

 - JETSON NANO DEVELOPER KIT


## Setup 

Create an environment with dependencies specified in env.yml:
    
    conda env create -f env.yml

 Activate the new environment:
    
    conda activate aif

 Install Mediapipe

    pip install mediapipe
    
 Install the **aif** IPython kernel in order to use in jupyter lab : 
    
    python -m ipykernel install --user --name aif


 Deploy jupyter lab with no browser and open accessibility:

    jupyter lab --no-browser --ip="0.0.0.0"

 Follow the instructions to run jupyter lab on browser

 Make sure the the kernel is correct.

 To deactivate the environment, open the terminal and run:
    
    conda deactivate
 ### Note:
 To run on headless, open a jupyter compatible browser and type:
    
    <IP>:8888/lab?
## Author

Kai Chen