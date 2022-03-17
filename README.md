<div align="center">

# Semantic Text Similarity (on quora dataset)

<img src='https://github.com/saumyagoyal95/Text-Similarity---Deep-Learning-Project/blob/aa529f1291718e2a39a355698db9774f09a2d050/QuoraDataset.png' width=300px> <br>
source : https://www.theverge.com/2012/9/11/3308440/quora-silicon-valley-topics-redesign-mainstream-q-and-a <br>

  
[About](#about) •
[Configuration Requirements](#configuration-requirements) •
[Description](#installation) •
  
</div>

## 📒 About <a name="about"></a>

This Mini-Project is done on Quora Question Pairs Similarity dataset. In this project, I dealt with the task of pairing up the duplicate questions from quora. 

Problem statement: 
- Identify which questions asked on Quora are duplicates of questions that have already been asked.
this could be useful to instantly provide answers to questions that have already been answered.
- Tasked with predicting whether a pair of questions are duplicates or not.
Note - Simalarity here referes to the Semantic similarity

## 👨‍💻 Configuration Requirements <a name="configuration-requirements"></a>

What is the required configuration for running this code
1. Jupyter Notebook
2. Glove Encoding 50 dimentional
3. Tensorboard for Visialization
4. Run requirements.txt for downloading the dependencies of the Notebook with the help of the following command
```python
pip install -r requirements.txt
```
## 🖥️ Description <a name="installation"></a>

Design Choice:
- GloVe Twitter Embedding with 50 dimentions were used
- Preprocssing steps used - Lammetization and stop_word removal - customized the choosen stop_words.
- Model Design: Two parallel LSTM layers were used for each question and further two fully connected Linear layers were used after concatinating the two - - LSTM layer tensors, finally a sigmoid layer was put forth for the classification
- Loss : Cross Entrophy Loss - classical data classification loss
- Optimizer: Adam
- Created Custome Trainer class for training, validation and test dataset
- Added Tensorboard for monitoring Training Loss, Training, Validation Accuracy and Hyper-params
- For Evaluation - n random samples can be picked and checked for Duplication

Obeservation:
- Model performs 77 percent(approx) accuracy on the Training Dataset (35k observation) and around 65 percent(approx) on the Validation dataset (10k)
- Model performs close to 65 percent(approx) on the Test Dataset(5k)
- Further Hyper-parameter tuning, more preprocessing steps and using higher dimention embedding might increase the accuracy of the model.
- In terms of Architecture, Bidirectional LSTM or Siamese Architecture could have been used.

Learnings:
I personally learned how to create a deep learning model from the absolute scratch, it was a nice mini-project to work up on. There is a lot of room for further learning.

Reference:
My work is inspired and referenced from : https://towardsdatascience.com/text-classification-with-pytorch-7111dae111a6 and
https://github.com/tanmay17061/pytorch-potpourri/blob/master/tutorial_scripts/unilstm.ipynb

