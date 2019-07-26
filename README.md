A working version of the kaggle_RSNA_Pneumonia_Detection - the 2nd place winner in the kaggle RSNA Pneumonia Detection Challenge
https://www.kaggle.com/c/rsna-pneumonia-detection-challenge 
Detailed solution according to the original author:
https://www.kaggle.com/c/rsna-pneumonia-detection-challenge/discussion/70427#latest-497399

required folder structure for the project to work:

    $(curr_dir)
    |__models
    |__output
    |__checkpoints # checkpoints saved after every epoch to this folder
    |__submissions  # kaggle rsna submission files saved here
    |__data
      |__test_dicoms # test data goes here
      |__train_dicoms # train data goes here
      |__detailed_class_invo.csv
      |__trainn_labels.csv
    |__pytorch_retinanet

REQUIREMENTS to run the code correctly:

Code runs in on a GCP ubuntu instance.

    $ uname -a
    Linux instance-4 4.15.0-1036-gcp #38-Ubuntu SMP Mon Jun 24 13:49:05 UTC 2019 x86_64 x86_64 x86_64 GNU/Linux
 
    $ lsb_release -a
    Distributor ID:	Ubuntu
    Description:	Ubuntu 18.04.2 LTS
    Release:	18.04
    Codename:	bionic

CUDA is installed on the instance.

    $ nvcc --version
    nvcc: NVIDIA (R) Cuda compiler driver
    Copyright (c) 2005-2017 NVIDIA Corporation
    Built on Fri_Nov__3_21:07:56_CDT_2017
    Cuda compilation tools, release 9.1, V9.1.85

the code runs in a conda env, a clone of the env could be made using:

    $ conda env create -f environment.yml
