# GraphPattern2vec

## Introduction 

 

This repository contains the code and datasets for the manuscript "".   

Included in this repository are the following: 

Example Knowledge Graph  

Example Embedding file 


## Installing dependencies  

![Python 3.10.8](https://img.shields.io/badge/Python-3.10.8-green)
Python == 3.10.8

From pip:

![PyPIwoop](https://img.shields.io/pypi/v/jupyterlab?label=matplotlib)
![PyPI](https://img.shields.io/pypi/v/numpy?label=numpy)
![PyPI](https://img.shields.io/pypi/v/pandas?label=pandas)
![PyPI](https://img.shields.io/pypi/v/matplotlib?label=matplotlib)
![PyPI](https://img.shields.io/pypi/v/scikit-learn?label=scikit-learn)
![PyPI](https://img.shields.io/pypi/v/tqdm?label=tqdm)
![PyPI](https://img.shields.io/pypi/v/statsmodels?label=tqdm)
![PyPI](https://img.shields.io/pypi/v/networkx?label=networkx)

### optional envirorment 
![Anaconda](https://img.shields.io/badge/Anaconda-%2344A833.svg?style=for-the-badge&logo=anaconda&logoColor=white)


## Downloading this repository 
``` 
git clone https://github.com/..... 
 ``` 
 ``` 
cd GraphPatter2Vec 
``` 



## Installing dependencies with conda ![Anaconda](https://img.shields.io/badge/Anaconda-%2344A833.svg?style=for-the-badge&logo=anaconda&logoColor=white)
the yml file is in GraphPatter2Vec file and is named "gp2v.yml"
``` 
conda env create -f gp2v.yml -n gp2v
``` 
``` 
conda activate gp2v
``` 

## Utilizing Model 

``` 
jupyter lab
``` 
#### once in the jupyter lab navigate to either 
#### ------ graphpattern2vec_process-multithread-Edited2022  
- for measureing an accurate ROC 

or
#### ------ graphpattern2vec_process-multithread-PREDICTION-Edited2022.ipynb
- for generating perdiction 
- ROC in this file does not represeint the overall accuracy 


# Before running the link prediction in either notebook generate your own embeddings  !!!!!!  PLEASE READ THIS SECTION !!!!!!



This section will describe utilizing the graphpattern2vec model and producing link-predictions with a knowledge graph  



To immediately use the model with the example data provided, Example code can be found in graphpattern2vec_process-multithread-Edited2022 notebook. The computational notebook can be viewed using JupyterLab which is included in our environment. You can run it using jupyter lab.   

Note if not using provided example embedding: 

All cells in the notebook should be run until the Link Prediction section. 

Embeddings used for predictions are generated from the output of graphpattern2vec (nodes collected through modified walk algorithm) which are then manually converted through metapath2vec- this step is done outside of the notebook  

Run the rest of the cells after the Link Prediction section, after inputting embedding file generated outside of notebook. 

 
