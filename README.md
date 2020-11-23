# Clean_Data_Sets_for_Molecular_Classification
A collection of 15 clean benchmark data sets for binary classification tasks on molecules (represented as SMILES strings). Most of these data sets are canonically used in publications in the area of molecular machine learning to validate methods and compare the performance of computational classification methods.

Each folder corresponds to one data set and contains the following items:

- A readme file or a scientific paper which describes the nature of the data set and its context and source.
- A .csv file in which one can find a SMILES representation for each molecule and a binary target variable (0 or 1) to distinguish positives from negatives.
- Depending on the context, some additional information and data.

The file "overview.csv" gives some basic information about the chosen data sets: 

- Seven data sets have been taken from MoleculeNet.ai. 
- Two data sets (hERG inhibition and inhibition of SARS-CoV-2 induced cytotoxicity) have been constructed by the author by extracting data from the ChEMBL database.
- Two data sets have been taken from papers which introduced specific benchmark data sets.
- Two data sets (MUTAG and PTC) have been added since they have been used canonically in the field for years.
- One data set relates to drugs which have been shown experimentally to extend the life span of C. elegans according to a 2017 paper (contained).
- One data set relates to inhibition of SARS-CoV-2 main protease and was constructed by the author from data published by the Diamond Light Source.

Finally, a Jupyter lab notebook called "data_pipeline" with Python code is contained which provides computational pipelines to automatically load the data sets and bring them into a useful form for machine learning. This notebook encompasses methods for each data set 

- to import the data set into a pandas dataframe,
- to check for and remove invalid SMILES (there is none in most data sets),
- to check for missing values (there is none in most data sets)
- to balance both classes in the data set if it is desired,
- to get some basic statistics on the data set,
- to construct a binary target variable y in the form of a 1d numpy array which contains 0s and 1s, and
- to construct a predictor variable x in the form of a 1d numpy array which contains SMILES strings.

The data processing functions in the notebook rely on basic functions within the Python packages numpy, pandas, matplotlib, math, sys, io and RDkit. To get a nice structuring of the notebook, it is recommended to use a Jupyer lab extension for collapsible headings.
