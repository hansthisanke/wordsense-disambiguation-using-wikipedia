<div align="center">
<h1 align="center">
<img src="https://icons.iconarchive.com/icons/custom-icon-design/flatastic-1/128/folder-icon.png" width="100" />
<br>WORDSENSE-DISAMBIGUATION-USING-WIKIPEDIA</h1>
<h3>Developed with the packages and tools below</h3>
<h3>Tensorflow, Keras, Numpy, Pandas, Matplotlib, Seaborn, Sklearn, Scipy</h3>
<p align="center">
<img src="https://img.shields.io/badge/TensorFlow-blue?style=flat&logo=tensorflow&logoSize=auto&labelColor=gray" alt="TensorFlow" />
<img src="https://img.shields.io/badge/Keras-blue?style=flat&logo=keras&logoSize=auto&labelColor=gray", alt="Keras"/>
<img src="https://img.shields.io/badge/Numpy-blue?style=flat&logo=numpy&logoSize=auto&labelColor=gray", alt="Numpy"/>
<img src="https://img.shields.io/badge/Pandas-blue?style=flat&logo=pandas&logoSize=auto&labelColor=gray", alt="Pandas"/>
<img src="https://img.shields.io/badge/Scikitlearn-blue?style=flat&logo=scikitlearn&logoSize=auto&labelColor=gray", alt="Sklearn"/>
<img src="https://img.shields.io/badge/Scipy-blue?style=flat&logo=scipy&logoSize=auto&labelColor=gray", alt="Scipy"/>
<img src="https://img.shields.io/badge/Wikipedia2Vec-blue?style=flat&logo=wikipedia&logoSize=auto&labelColor=gray", alt="Scipy"/>

</p>

<p align="center"> 
<img src="https://img.shields.io/github/license/hansthisanke/wordsense-disambiguation-using-wikipedia?style=for-the-badge&color=5D6D7E" alt="GitHub license" />
<img src="https://img.shields.io/github/last-commit/hansthisanke/wordsense-disambiguation-using-wikipedia?style=for-the-badge&color=5D6D7E" alt="git-last-commit" />
<img src="https://img.shields.io/github/commit-activity/m/hansthisanke/wordsense-disambiguation-using-wikipedia?style=for-the-badge&color=5D6D7E" alt="GitHub commit activity" />
<img src="https://img.shields.io/github/languages/top/hansthisanke/wordsense-disambiguation-using-wikipedia?style=for-the-badge&color=5D6D7E" alt="GitHub top language" />

</p>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=hansthisanke&repo=wordsense-disambiguation-using-wikipedia&layout=compact" alt="Top Languages" />
</div>




# DESCRIPTION
Implementing a novel scheme of word disambiguation using Python NLTK and Wikipedia

# TASK-3: COMPARISON BETWEEN UNIFIED WSD AND WIKI BASED APPROACH

## Overview
In this task, we compare the Unified Word Sense Disambiguation (WSD) approach with the Wiki-based approach for understanding word meanings in context. The comparison is performed using the semcor dataset obtained from the Training_corpora folder of the provided dataset.

## Dataset
The dataset used for this task is from the paper Word Sense Disambiguation: A Unified Evaluation Framework. To proceed with the task, you need to download (http://lcl.uniroma1.it/wsdeval/) the dataset and extract it.


Here is the folder structure of the dataset used for the Task-3:

```bash
├───Data_Validation
│   ├───lib
│   └───sample-dataset
├───Evaluation_Datasets
│   ├───ALL
│   ├───semeval2007
│   ├───semeval2013
│   ├───semeval2015
│   ├───senseval2
│   └───senseval3
├───Output_Systems_ALL
└───Training_Corpora
    ├───SemCor
    └───SemCor+OMSTI
```

## Task Workflow
The task was performed using the following steps:

### Select 10 Target Words
Choose 10 target words for disambiguation. These words will be the focus of comparison between the two approaches.

### Select Context Sentences
For each target word, select 3 context sentences from the XML file located in the sector_data folder inside the Training_corpora directory. These sentences will be used to disambiguate the target word's meaning.

### Identify Instance ID
For each selected context sentence, identify the instance ID of the target word. This instance ID represents a specific occurrence of the word in the context.

### Retrieve Sense Key
Using the instance ID, retrieve the sense key associated with the target word. The sense key is essential for finding the correct meaning of the word in WordNet.

### Obtain WordNet Definition
Use the sense key to retrieve the WordNet definition of the target word. WordNet provides a comprehensive and structured set of meanings (senses) for each word.

### Retrieve Wiki Definition
Using the target word and context sentence, retrieve the Wikipedia definition of the word. The Wiki-based approach leverages the vast knowledge in Wikipedia to capture the meaning of the word in the context of the sentence.

### Compare Definitions
Compare the WordNet definition and the Wikipedia definition for each target word. The comparison involves analyzing how closely the meanings from WordNet and Wikipedia align with the word's usage in the given context.

### Create a Histogram
Finally, based on the comparison, generate a histogram to visually represent the number of matches or differences between the WordNet and Wikipedia definitions across the target words.
## Histogram Comparison

Here is a visual comparison of the histograms:

<div style="display: flex; justify-content: space-between; gap: 20px;">
  <img src="./task_3_data/histogram.png" alt="Histogram 1" width="300" style="border: 2px solid #ddd; border-radius: 10px;">
  <img src="./task_3_data/histogram.png" alt="Histogram 2" width="300" style="border: 2px solid #ddd; border-radius: 10px;">
</div>

---



# TASK-6,7 and 8: Using Wikipedia2Vec for word pair similarity comparisons

## Overview
In this task,we use Wikipedia2Vec framework for similarity calculation, comparison word-pair correlation between standard embedding models across benchmark datasets. Development of a convex combination factor based vector embedding model for further comparison of performance enhancements.

## Dataset
The dataset used for this task are the benchmark datasets MC, RG and WS353. 


Here is the folder structure of the dataset used for the the tasks:

```bash
├───datasets
│   ├───mc.csv
│   ├───rg.csv
│   └───wordsim.csv
```

In additon to above the pre-trained vector embedding with 300 dimension need to be downloaded from https://wikipedia2vec.github.io/wikipedia2vec/pretrained/.

Also the required libraries and packages are listed in the requirements.txt file. By running this file can obtain the dependencies to run the script code_task6_onwards.ipynb

In the python notebook,
- The required pre-trained embeddings of word2vec, GloVe and FastText are installed with gensim packages.
- Wikipedia2Vec pre-trained embedding file need to be downloaded to the root folder in order to load in the script.