# RegPattern2Vec

## Introduction 



This repository contains the code and datasets for the manuscript "Predicting Protein and Pathway Associations for Understudied Dark Kinases using Pattern-constrained Knowledge Graph Embedding ".   


#### Included in this repository are the following: 

- DownloadLinkForData.txt file
  - file contains link for download 
  - Download contains KG, embeddings, uniprot2genename, and reactome2pathwayname files 
  
- 2 jupyter lab notebooks files
  - Notebook for measuring the accuracy (insert)
  - Notebook for prediction generation (insert)
  
- gp2v.yml file (name change?)
  - file can be used to create the environment 
  
- graphpattern2vec folders 
  - folder holds the objects/funtions of RegPattern2Vec

- Readme.md file
  - You're reading it right now
  
- model folder 
  - folder holds temporary files 


## Installing dependencies  

![python=3.10.8](https://img.shields.io/badge/Python-3.10.8-green)
Python == 3.10.8

From pip:

![jupyterlab=3.5.0](https://img.shields.io/pypi/v/jupyterlab?label=jupyterlab)
![numpy=1.23.5](https://img.shields.io/pypi/v/numpy?label=numpy)
![pandas=1.5.2](https://img.shields.io/pypi/v/pandas?label=pandas)
![matplotlib=3.6.2](https://img.shields.io/pypi/v/matplotlib?label=matplotlib)
![scikit-learn=1.1.3](https://img.shields.io/pypi/v/scikit-learn?label=scikit-learn)
![statsmodels=0.13.5](https://img.shields.io/badge/statsmodels-0.13.5-blue)
![tqdm=4.64.1](https://img.shields.io/badge/tqdm-4.64.1-blue)
![networkx==2.8.8](https://img.shields.io/pypi/v/networkx?label=networkx)

Todo update copy paste for badges

### optional envirorment 
![Anaconda](https://img.shields.io/badge/Anaconda-%2344A833.svg?style=for-the-badge&logo=anaconda&logoColor=white)


## Downloading this repository 
``` 
git clone https://github.com/gravelCompBio/GraphPattern2vec.git
 ``` 
 ``` 
cd GraphPatter2vec/  (name change?)
``` 
### ALSO DOWNLOAD THIS data/ FOLDER AND PUT IT IN THE RegPattern2Vec-main folder (unzip and make sure the name of the unziped folder is still "data")

https://outlookuga-my.sharepoint.com/:u:/g/personal/nmg60976_uga_edu/EatErUI0YUNMnDxxk-LOcnYBvG30lkW2weNIv2WuUfZVzw?e=Ig92AU
(Consider using figshare)



## Installing dependencies with conda ![Anaconda](https://img.shields.io/badge/Anaconda-%2344A833.svg?style=for-the-badge&logo=anaconda&logoColor=white)
the yml file is in RegPatter2Vec file and is named "gp2v.yml"  (Name change?)
``` 
conda env create -f gp2v.yml -n gp2v
``` 
``` 
conda activate gp2v
``` 

## Utilizing the Model 
### downloading needed file

1) Confirm prerequisite data has been downloaded (see download repostory section)
2) Navigate to GraphPattern2vec-main folder in the termimal and run jupyter lab  (Name Change?)

``` 
jupyter lab
``` 
#### once in the jupyter lab navigate to either 
#### ------ graphpattern2vec_process-multithread-Edited2022  (name change needed?)
- for measuring accuracy of the model (AUC-ROC) 

or
#### ------ graphpattern2vec_process-multithread-PREDICTION-Edited2022.ipynb  (Name change?)
- for generating perdictions  
- ROC in this file does not represent the overall accuracy 


# Before running the link prediction in either notebook generate your own embeddings  !!!!!!  PLEASE READ THIS SECTION !!!!!!

1) double check you downloaded all files of the Knowlege graph and embedding files from the "Downloading this repository " section

2) after you preform the random walk in sections of the code in either notebook, you can use the embbeding files we provided. If you wish to generate you own embedding you can preform metapath2vec off the random walk to re-generate new embbeding files. (see section below for metapath2vec instructrions)

3) If you happy with the existing emebbeding files you can run the link prediction sections of the code in either notebook

## Basic guide for running metapath2vec to generate new ebbedding files from your randomwalk file 

We use Change2vec++ to generate embeddings 
This is where the code is from  
#### https://github.com/Change2vec/change2vec/tree/master/metapath2vec/code_metapath2vec
We used These paramaters for change2vec
- Size 256
- Window 7
- Negitive 5
- MinCount 5
- Threads 32
- PlusPlus 1

Example code of how we put it in the terminal 

Todo update acutull example


``` 
./metapath2vec
``` 

see paper for a better explination 
#### Dong, Y., Chawla, N. V., & Swami, A. (2017, August). metapath2vec: Scalable representation learning for heterogeneous networks. In Proceedings of the 23rd ACM SIGKDD international conference on knowledge discovery and data mining (pp. 135-144).


## Other Info


------ TO DO fill out the rest of the documentaiton 

This section will describe utilizing the graphpattern2vec model and producing link-predictions with a knowledge graph  



To immediately use the model with the example data provided, Example code can be found in graphpattern2vec_process-multithread-Edited2022 notebook. The computational notebook can be viewed using JupyterLab which is included in our environment. You can run it using jupyter lab.   

Note if not using provided example embedding: 

All cells in the notebook should be run until the Link Prediction section. 

Embeddings used for predictions are generated from the output of graphpattern2vec (nodes collected through modified walk algorithm) which are then manually converted through metapath2vec- this step is done outside of the notebook  

Run the rest of the cells after the Link Prediction section, after inputting embedding file generated outside of notebook. 

 
