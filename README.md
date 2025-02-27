# Thesis Datasets
In this repository the datasets that i used in my thesis are uploaded both before and after processing. The initial datasets are in the following tags:<br />
[Helios dataset](https://github.com/S-Lab-System-Group/HeliosData)<br />
[Philly dataset](https://github.com/msr-fiddle/philly-traces)<br />
[4G LTE dataset](https://cora.ucc.ie/handle/10468/6400)<br />

The processed datasets used in my thesis are included in this thesis repository except for philly. Because of its size philly dataset is in this google drive link: [Google Drive repository](https://drive.google.com/drive/folders/1VC8Z0mr91HRmZ8ygMXE8qA5Fh2XmFagi?dmr=1&ec=wgc-drive-globalnav-goto)


## Dataset Attribution
The Helios dataset is sourced from Sensetime and the dataset is available in [helios](https://github.com/S-Lab-System-Group/HeliosData) Github repository and is licensed under the [Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/). This dataset was presented in this paper: ["Characterization and prediction of deep learning workloads in large-scale GPU datacenters"](https://dl.acm.org/doi/10.1145/3458817.3476223)

The philly dataset is was done as part of Microsoft Research's Project Fiddle. The dataset was presented in this paper: ["Analysis of Large-Scale Multi-Tenant GPU Clusters for DNN Training Workloads"](https://arxiv.org/abs/1901.05758) in ATC’19 and is licensed under the [Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/) and is available in [philly](https://github.com/msr-fiddle/philly-traces) repository in Github. 

Last but not least the 4G LTE dataset that was used derived from this paper: [Beyond throughput: a 4G LTE dataset with channel and context metrics
](https://cora.ucc.ie/handle/10468/6400) under the licence [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). This dataset did not any changes and was used as it is. 

## Architecture of Github
The Helios file contains the processed data from helios dataset in a zip file. After downloading it you will see that the file is divided in 4 different GPU clusters (every GPU cluster data in one file). Each GPU cluster has information about different Virtual CLusters (VC). Each data available for every VC is available in respective csv files. 

The 4G dataset did not need any edit. See more information in this [link](https://www.kaggle.com/datasets/aeryss/lte-dataset) from Kaggle where the dataset is available 

Because the philly dataset is very big the philly dataset is available in this public [Google Drive repository](https://drive.google.com/drive/folders/1VC8Z0mr91HRmZ8ygMXE8qA5Fh2XmFagi?dmr=1&ec=wgc-drive-globalnav-goto). In the initial datasets we have a number of different files. We have a file named cluster_job_log, which contains information about each job. We divided every job's data the same way as helios, which means that we did a per VC division. Each VC has its respective csv file. We also have 3 different files that provide information about a per-minute record of each GPU's, CPU and memory utilization. Those files are merged into one and divided by machine. Now each file has all the information about the % utilization of GPUs, CPU and Memory, which means that each csv file corresponds to a machine with the same name. 
