# Simulating SARS-CoV-2 Spread
## Interactive notebook
Use Binder to run our code online.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/nihcompmed/SIRD/master)

## If you'd like to keep a copy of this on your local machine:
### Linux with Singularity container:
Clone the repository
    USER$ git clone https://github.com/nihcompmed/SIRD
    USER$ cd SIRD

In SIRD/ (where the .simg files must be stored)
These commands are to be executed in command line
Use Singularity to pull and generate container which contains necessary enviornment to run the exmaple code

### Singularity: Build .simg file from Dockerhttps://hub.docker.com/repository/docker/evancresswell/sird
#### Docker Repository: https://hub.docker.com/repository/docker/evancresswell/sird
    user$ sudo singularity pull docker://evancresswell/sird:#TAG#
    user$ sudo singularity build sird.simg sird_#TAG#.sif 
### Running Example Notebook through Singularity Container
#### Once you have the '.simg' singularity image file you can run the jupyter notebook example through your new container:
    user$ singularity exec -B </path/to/SIRD/:/path/to/SIRD/> </path/to/SIRD>/sird.simg jupyter notebook SIRD_example.ipynb
####	 Click the resulting link in your command line and navigate to python notebook
####	 If you're using remote computing resources you will need to start ssh tunneling to display notebook
