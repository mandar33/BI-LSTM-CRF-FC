# BI-LSTM-CRF-FC

CS598  Final Project implementing the paper: 

**Fully‑connected LSTM–CRF on medical concept extraction**
**Jie Ji1, Bairui Chen, Hongcheng Jiang4**
Received: 14 December 2018 / Accepted: 12 February 2020 / Published online: 24 February 2020
© Springer-Verlag GmbH Germany, part of Springer Nature 202

There is no original repo 

Dependencies: pytorch , GLOVE300D6B (.txt), matlplotlib, conlleval(pip install conlleval), python 3.x

Data download instruction
i2b2010 dataset for medical concepts
Register for an account at https://portal.dbmi.hms.harvard.edu/ 

The i2b2 NLP data sets previously released on i2b2.org are now hosted here on the DBMI Data Portal under their new name, n2c2 (National NLP Clinical Challenges):

n2c2 NLP Research Data Sets: https://portal.dbmi.hms.harvard.edu/projects/n2c2-nlp/

2010 relation challenge datasets: download the concepts and txt 


Preprocessing code + command (if applicable)
Please run the notebook in jupyter/google colab: Transform_i2b2_CoNLL_data.ipynb
this notebook translates the concept and txt files data input into train,dev(validation) and test files(80/10/10) approx split ratio.

1) Please run the jupyter notebook BIDIR_LSTM_CRF_FC.ipynb to train and test concepts and txt data for fully connected LSTM-CRF proposed by the original authors.
2) Please run the jupyter notebook CS598BIDIR-LISTM-CRF-STACKED-Project.ipynb to train and test concepts and txt data for 4 layer stacked BIDIR-LSTM-CRF 
3) Please run the jupyter notebook BI-LISTM-CRF.ipynb to train and test concepts and txt data for BIDIR-LSTM-CRF.
4) Please run the jupyter notebook UniLSTM-CRF.ipynb to train and test concepts and txt data for fully connected UNIDIR-LSTM-CRF.

Evaluation code + command 
Please run pip install conlleval (credit: https://github.com/kaniblu/conlleval) to get F1 scores, Precision, Recall, Accuracy scores. The last code cell in each notebook shows how to extract that info to an output file


No Pretrained models 

Table of results 
![ScoresFinal](https://user-images.githubusercontent.com/6293859/167307471-7439a42d-ce43-45b1-b90c-94697da3eaf1.PNG)


We run this notebook in google colab using GPU runtime

If you cannot use Google Colab, run a jupyter notebook and remove all the .cuda() function calls from the code to run code on a CPU. 

References:

LSTM-CRF code credits: https://github.com/huangxt39/LSTM-CRF-pytorch

Advanced: Making Dynamic Decisions and the Bi-LSTM CRF
https://pytorch.org/tutorials/beginner/nlp/advanced_tutorial.html


https://github.com/raghavchalapathy/Bidirectional-LSTM-CRF-for-Clinical-Concept-Extraction

