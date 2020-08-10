<p align="center">
	<sub>Imperial College London<br>Dyson School of Design Engineering</sub>
</p>
<h1 align="center">
Detecting Social Anxiety in Young People Using Physiological Data Collected From Wearables
</h1>


## 1. Overview

This project investigates whether social anxiety can be detected in young people using physiological data recorded from a wearable and Machine Learning (ML) techniques. This repository contains the full dataset and code needed to recreate the classification models and reproduce the results within the report; as well as this the notebooks contain functions that enable further experimentation.

#### 1.1. Nature of the dataset

The dataset consists of Heart Rate (HR) data, Skin Temperature (ST) data and Electrodermal Activity (EDA) data, which is labelled in various ways depending on the classification context. The physiological data was recorded by a multi-sensor wristband wearable called E4 Empatica.

This data was collected during twelve experiments involving young people who have been identified as subclinically socially anxious based on their scores from the self-reported version of the Liebowitz Social Anxiety Scale (LSAS-SR). The data was collected during an impromptu speech task used to invoke a social anxiety response (invoking both anticipation and reactive social anxiety). The task initiated with a relaxation period (invoking a baseline response) followed by task announcement and preparation period (invoking anticipation anxiety), this was then followed by performing the impromptu speech task (invoking reactive anxiety).

#### 1.2. Description of the ML experiments

Various classification algorithms such as Support Vector Machine (SVM), Random Forest, Decision Tree and K-Nearest Neighbours (KNN) were used to train models for three different ML experiments. Furthermore, the following experiments were carried out using datasets with all modalities combined, as well as datasets with only singular modalities.

__Experiment (1)__ investigates whether models can be trained to classify baseline and socially anxious states.

__Experiment (2)__ investigates whether models can be trained to differentiate between baseline, anticipation anxiety and reactive anxiety states.

__Experiment (3)__ investigates whether models can be trained to differentiate between social anxiety experienced by individuals with differing levels of social anxiety.

__Results & Evaluation__ The models were then evaluated using 10-fold cross validation as a performance index. Confusion matrices were also used to examine the classification accuracies per class.

_Note:_ In order to reproduce the results in the report, please set the argument `repeat = True` in the functions within the `Supervised_Machine_Learning_Notebook.ipynb`.


## 2. Repository structure

#### 2.1. Data Preprocessing Folder

The repository contains Jupyter notebooks used to preprocess each participant's data in the `data_preprocessing` folder, within this folder there is a folder for each participant; each participant folder contains csv files of raw data and a notebook that preprocesses the data, called `Data_Preprocessing.ipynb`. Each participant folder also contains datasets for each experiment e.g `experiment_1.csv` that consist of previously preprocessed data so that the main notebook `Supervised_Machine_Learning_Notebook.ipynb` can execute without running each participant's preprocessing notebook.

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

#### 2.2. Supervised ML (Data Processing) Folder

The repository contains a main Jupyter notebook called `Supervised_Machine_Learning_Notebook.ipynb` used for executing the three different supervised ML experiments. The notebook is in the `data_processing` folder. The folder also contains datasets for each ML experiment e.g. `experiment_1_randomised_data.csv`, these datasets consist of participants' preprocessed data that have been previously randomised. These datasets are used when an individual desires to reproduce the models and results from the report, this can be intiated when the argument `repeat = True` in any of the functions within `Supervised_Machine_Learning_Notebook.ipynb`; this was done because an actively randomised dataset may result in slightly differing results, compared to reusing the exact dataset used to create the results.
```
data_processing/                                  
├── Supervised_Machine_Learning_Notebook.ipynb      # supervised ML notebook
├── experiment_1_randomised_data.csv                # previously randomised dataset for experiment (1)
├── experiment_2_randomised_data.csv                # previously randomised dataset for experiment (2)
└── experiment_3_randomised_data.csv                # previously randomised dataset for experiment (3)   
```

## 3. Instructions

You can view the notebooks with their outputs in this Github without running the notebooks. However, if you would like to run the notebooks firsthand, you must first download a zip file of this repository, then you must download [Anaconda Navigator](https://docs.anaconda.com/anaconda/install/). Following the download, you must launch Anaconda Navigator and click 'Jupyter Notebook'. Once Jupyter Notebook is launched, navigate to where the extracted zip folder is and open a notebook of your choice. You must then download each dependency (see below). After downloading the dependencies you should be able to run any of the notebooks.

#### Dependencies: 
The notebooks utilise NumPy, Matplotlib, Seaborn, Scikit-learn and Pandas dependencies. To download the dependencies you must write the following commands in a code block in a Jupyter notebook and run the code block (this only needs to take place once). _Note:_ Matplotlib version 3.1.0 was installed as there is a bug in the latest version that affects the rendering of seaborn plots

```
 pip install numpy
 pip install matplotlib==3.1.0
 pip install seaborn
 pip install scikit-learn
 pip install pandas
```
## 4. References

This project was powered by:

- [Scikit Learn](https://scikit-learn.org/stable/)
- [Matplotlib](https://matplotlib.org/)
- [Pandas](https://pandas.pydata.org/)
- [NumPy](https://numpy.org/)
- [Seaborn](https://seaborn.pydata.org/)

## 5. Quick Links 

<p align="left">
	<a href="https://github.com/rs2416/Predicting_Social_Anxiety/blob/master/data_processing/Supervised_Machine_Learning_Notebook.ipynb">Supervised ML notebook</a>
</p>
<p align="left">
	<a href="https://github.com/rs2416/Predicting_Social_Anxiety/blob/master/data_preprocessing/1/Data_Preprocessing_Notebook.ipynb" target="_blank">An example of a preprocessing notebook</a>
</p>

