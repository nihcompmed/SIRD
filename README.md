
# Generate Singularity Container to Run Code

### In SIRD/ (where the .simg files must be stored)

## Singularity: Build .simg file from Docker
'''	$ sudo singularity pull docker://evancresswell/sird:#TAG#
'''	$ sudo singularity build sird.simg sird_#TAG#.sif 
## Running Example Notebook through Singularity Container ---#
'''	$ singularity exec -B </path/to/SIRD/:/path/to/SIRD/> </path/to/SIRD>/sird.simg jupyter notebook SIRD_example.ipynb
###	 CLICK RESULTING LINK AND NAVIGATE TO EXAMPLE
###	 If you're using remote computing resources you will need to start ssh tunneling to display notebook
