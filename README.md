## Setup 

Create an environment with dependencies specified in env.yml:
    
    conda env create -f env.yml

 Activate the new environment:
    
    conda activate aif
    
 Inside the new environment, instatll IPython kernel so we can use this environment in jupyter notebook: 
    
    python -m ipykernel install --user --name aif


 Homework 1 (only) is a Jupyter Notebook. With the above done you should be able to get underway by typing:

    jupyter lab --no-browser
    
 To make sure we are using the right environment, go to the toolbar of exploring_word_vectors.ipynb, click on Kernel -> Change kernel, you should see and select cs224n in the drop-down menu.

 To deactivate an active environment, use
    
    conda deactivate