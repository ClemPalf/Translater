# Translater

Notebook to create from scratch your own translator!
We will be using the Tensorflow functional API in order to build and train this complex RNN model. 

## Overview

<p align="center">
  <img src="https://github.com/ClemPalf/Translater/blob/371730adf0da0206fdaaa97d3f2fcecc31305308/Images/neural_translation_model.png"/>
</p>

<p align="center">
  <img src="https://github.com/ClemPalf/Translater/blob/371730adf0da0206fdaaa97d3f2fcecc31305308/Images/neural_translation_model_key.png"/>
</p>

The above schematic represents the architecture of the model. 
1)	The input text goes through a 128-dimensional embedding layer (directly imported from TensorHub). 
2)	The embedding layer output is then fed to an encoder, of which will keep only the last hidden and cell state. 
3)	Those hidden and cell state are then used as the decoder initial state. 
4)	A start token is passed in as the first input, which is embedded using another embedding layer (which we will train ourselves this time). 
5)	The decoder RNN then makes a prediction for the next word, which is then passed in as the following input, and this process is repeated until a special ```<end>``` token is emitted from the decoder. 

## Instructions

The first step will be to download the data. 
Download your training data according to which pair of language you want to build your model upon: http://www.manythings.org/anki/.

In the 2nd coding cell, enter the name of your freshly download text file. In this example the file is named 'deu.txt'.
```  
with open('deu.txt', 'r', encoding='utf8') as f: 
``` 

Run all the notebook till the 3rd to last cell.
Now, all you need to do is enter the sentence you want to translate...
```  
Sentence_to_translate = "Hello I am Tom!" 
```
... and run the two cells below! Done!
  

The model creation and training are explained throughout the notebook.

  
