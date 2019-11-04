
# Classification analyses for ASD nback experiment

### Requirements:
- `python 3.6+`
  - `sklearn`
  - `matplotlib`
  - `numpy`
  - `scipy`
  - `pickle`
  - `tqdm`
  - `argparse`
  - `os`
  
To setup a conda environment with all of the required dependencies, install conda for python 3 and then do:  
`conda env create -f nback.yml`  
This environment can then be activated with  
`conda activate nback`  

### Classification analyses

We have pre-generated the data structures used in classification analyses. They were generated by running:  
` matlab setup_data.m `

1)
    - If you have access to SLURM-based cluster computing: 
        - clone this repository to your cluster and edit the header information in `run_slurm.sbatch` accordingly.
    - If you do not have access to a cluster: 
        - change line 9 of `classify_MAD.slurm` to `use_slurm=0`
2) ` . classify_MAD.slurm`

Alternatively, you can call the python script directly with a command line interface  
`python classify_MAD.py --help` to see options

If you followed instructions 1) and 2), run `python plot_results_table.py` to see a table of results