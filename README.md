# VMASK
Code for the paper "Learning Variational Word Masks to Improve the Interpretability of Neural Text Classifiers"

### Requirement:
- python == 3.7.3
- gensim == 3.4.0
- pytorch == 1.2.0
- numpy == 1.16.4

### Data:
Download the preprocessing [data with splits](https://drive.google.com/file/d/1n9wVSsPBjIu9Ni0GodF21nikgrSSKfWR/view?usp=sharing).

### Generate explanations:

We provide the example code of HEDGE interpreting the LSTM, CNN and BERT model on the IMDB dataset. We adopt the BERT-base model built by huggingface: https://github.com/huggingface/transformers.

In each folder, run the following command to generate explanations on the test data for a well-trained model.
```
python hedge_main_model_imdb.py --save /path/to/your/model
```
We save the start-end word indexes of text spans in a hierarchy into the "hedge_interpretation_index.txt" file.

To visualize the hierarchical explanation of a sentence, run
```
python hedge_main_model_imdb.py --save /path/to/your/model --visualize 1(the index of the sentence)
```

### Reference:
If you find this repository helpful, please cite our paper
