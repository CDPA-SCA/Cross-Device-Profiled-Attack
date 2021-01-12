# Cross-Device-Profiled-Attack
 
This repository contains Demos on how to reproduce the results presented in "Cross-Device Profiled Side-Channel Attack with Unsupervised Domain Adaptation."


Each dataset is composed of the following folders and script:

- ./Data: the datasets file (.npy format) used in the experiments. 
- ./models: contains the pre-trained model, fine-tuned model, etc.
- ...\_CDPA\_Demo.ipynb: the notebook file that contains both codes and outputs. This notebook demonstrates how to load a dataset, how to pre-process the data, how to fine-tune a network, how to evaluate the pre-trained and fine-tuned models, etc. 

The original sources for the publicly available datasets are:

- DPA contest-v4.2: [http://www.dpacontest.org/v4/42_traces.php](http://www.dpacontest.org/v4/42_traces.php)
- ASCAD: [https://github.com/ANSSI-FR/ASCAD](https://github.com/ANSSI-FR/ASCAD)
- AES\_HD: [https://github.com/AESHD/AES_HD_Dataset](https://github.com/AESHD/AES_HD_Dataset)
