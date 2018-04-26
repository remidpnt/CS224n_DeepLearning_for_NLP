# Assignments CS224n: Natural Language Processing with Deep Learning


These files are my solution for the CS224n course from Stanford University 2017.
http://web.stanford.edu/class/cs224n/


### General overview

These assignments are related to neural networks application for Natural language processing.

  * First assignment code: As an introduction, we will implement some basic functions to run a neural network. We will then use theses functions to produce some GloVe vector to encode some words to vectors using their context in a corpus.

### Installation to run these python programs

I used python 2.7 to run these files, with Anaconda.
Please note that if you have a gpu, you should install tensorflow-gpu to save time (especially for assignment 2). Make sure you have downloaded the dataset before you run the files.

cd /path/to/assignmentX/

pip install -r requirements.txt


### Assignment 3, if you use Windows
In these case, you will need python 3. Please:

replace line 105 from `data_util.py` to:
```python
with open(os.path.join(path, "features.pkl"), "wb") as f:
```
(Just add a `b` to avoid) _"write() argument must be str not bytes"_ error
Also replace line 113 by:
```python
with open(os.path.join(path, "features.pkl"), "rb") as f:
```
You will also need to replace:
`tf.nn.rnn_cell.RNNCell`
to
`tf.contrib.rnn.core_rnn_cell.RNNCell`
in files `q2_gru_cell.py` and `q2_rnn_cell.py`.
