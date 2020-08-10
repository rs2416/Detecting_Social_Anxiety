### Data Preprocessing Folder

The repository contains Jupyter notebooks used to preprocess each participant's data in this folder, within this folder there is a folder for each participant; each participant folder contains csv files of raw data and a notebook that preprocesses the data, called `Data_Preprocessing.ipynb`. Each participant folder also contains datasets for each experiment e.g `experiment_1.csv` that consist of previously preprocessed data so that the main notebook `Supervised_Machine_Learning_Notebook.ipynb` can execute without running each participant's preprocessing notebook.

```
data_preprocessing/
├── 1/                                  # folder for participant 1
│   ├── Data_Preprocessing.ipynb        # preprocessing notebook
│   ├── experiment_1.csv                # previously outputted preprocessed dataset for experiment (1)
│   ├── experiment_2.csv                # previously outputted preprocessed dataset for experiment (2)
│   ├── experiment_3.csv                # previously outputted preprocessed dataset for experiment (3)
│   ├── HR.csv                          # HR dataset for participant 1
│   ├── EDA.csv                         # EDA dataset for participant 1
│   └── ST.csv                          # ST dataset for participant 1
│
├── 2/ ...                              # folder for participant 2
```
