### Supervised ML (Data Processing) Folder

The repository contains a main Jupyter notebook called `Supervised_Machine_Learning_Notebook.ipynb` used for executing the three different supervised ML experiments. The notebook is in this folder. This folder also contains datasets for each ML experiment e.g. `experiment_1_randomised_data.csv`, these datasets consist of participants' preprocessed data that have been previously randomised. These datasets are used when an individual desires to reproduce the models and results from the report, this can be intiated when the argument `repeat = True` in any of the functions within `Supervised_Machine_Learning_Notebook.ipynb`; this was done because an actively randomised dataset may result in slightly differing results, compared to reusing the exact dataset used to create the results.
```
data_processing/                                  
├── Supervised_Machine_Learning_Notebook.ipynb      # supervised ML notebook
├── experiment_1_randomised_data.csv                # previously randomised dataset for experiment (1)
├── experiment_2_randomised_data.csv                # previously randomised dataset for experiment (2)
└── experiment_3_randomised_data.csv                # previously randomised dataset for experiment (3)   
```
