# Requirements

- A PC with a CUDA-capable GPU
- Ubuntu 22.04
- Python environment with Python 3.11 installed - in this case, Conda was used.
- Fast internet connection and about 7GB of disk space - after all packages were installed, the environment took up 6.5GB, according to Nautilus

# Setup

1. clone the AEROBALDE repository (https://github.com/jonasricker/aeroblade/)
2.Create a conda environment with Python 3.11 and activate it: `conda create -n aero-3.11 python=3.11` then `conda activate aero-3.11`
3. Open the `requirements.txt` file and remove the version of the package called `packaging`: `packaging=0.29` -> `packaging`
4. run `pip install -r requirements.txt`
5. Wait until installation is complete

# Running

1. To run a prediction, remove or rename a folder called `aeroblade_output`, then run the command `python scripts/run_aeroblade.py --files-or-dirs path/to/your/folder`
2. The results will be output to the newly created folder `aeroblade_output`, the file `distances.csv` will contain the distances to the images after being put through respective model's autoencoders.
