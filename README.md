# BI-LSTM-CRF-FC readme (steps to run the notebook code, result and references)

CS598  Final Project implementing the paper: 

1)**Fully‑connected LSTM–CRF on medical concept extraction**
**Jie Ji1, Bairui Chen, Hongcheng Jiang4**
Received: 14 December 2018 / Accepted: 12 February 2020 / Published online: 24 February 2020
© Springer-Verlag GmbH Germany, part of Springer Nature 202

2)There is no original repo provided by the above mentioned authors of the paper.

3)Dependencies: pytorch 1.9 , GLOVE300D6B (.txt), matlplotlib, conlleval(pip install conlleval), python 3.x

4)Data download instruction

i2b2010 dataset for medical concepts
Register for an account at https://portal.dbmi.hms.harvard.edu/ . The i2b2 NLP data sets previously released on i2b2.org are now hosted here on the DBMI Data Portal under their new name, n2c2 (National NLP Clinical Challenges):n2c2 NLP Research Data Sets: https://portal.dbmi.hms.harvard.edu/projects/n2c2-nlp/
2010 relation challenge datasets: download the concepts and txt 


5) Preprocessing code + command (if applicable)

Please run the notebook in jupyter/google colab: Transform_i2b2_CoNLL_data.ipynb
this notebook translates the concept and txt files data input into train,dev(validation) and test files(80/10/10) approx split ratio.

6) Training, Model and Test 

    a) Please run the jupyter notebook BIDIR_LSTM_CRF_FC.ipynb to train and test concepts and txt data for fully connected LSTM-CRF proposed by the original authors.
    
    b) Please run the jupyter notebook CS598BIDIR-LISTM-CRF-STACKED-Project.ipynb to train and test concepts and txt data for 4 layer stacked BIDIR-LSTM-CRF. 
    
    c) Please run the jupyter notebook BI-LISTM-CRF.ipynb to train and test concepts and txt data for BIDIR-LSTM-CRF.
    
    d) Please run the jupyter notebook UniLSTM-CRF.ipynb to train and test concepts and txt data for fully connected UNIDIR-LSTM-CRF.

7) Evaluation code + command 

Please run pip install conlleval (credit: https://github.com/kaniblu/conlleval) to get F1 scores, Precision, Recall, Accuracy scores. The last code cell in each notebook shows how to extract that info to an output file and get the best F1 score.


8) No Pretrained models used

9) Table of results 


![ScoresFinal](https://user-images.githubusercontent.com/6293859/167307471-7439a42d-ce43-45b1-b90c-94697da3eaf1.PNG)

Number 4 (Fully Connected LSTM-CRF) performed the best, but due to limited data availability I could not get the performance that the original authors achieved.

We run this notebook in google colab using GPU runtime

If you cannot use Google Colab, run a jupyter notebook and remove all the .cuda() function calls from the code to run code on a CPU. 

10) References:

LSTM-CRF code credits: https://github.com/huangxt39/LSTM-CRF-pytorch

Advanced: Making Dynamic Decisions and the Bi-LSTM CRF
https://pytorch.org/tutorials/beginner/nlp/advanced_tutorial.html


Preprocess Code credits: https://github.com/raghavchalapathy/Bidirectional-LSTM-CRF-for-Clinical-Concept-Extraction (theano)

