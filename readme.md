# Language Modeling

In this project, I initially attempted to reduce perplexity on the WikiText2 dataset as much as possible using LSTM and simple regularizations, including weight decay and dropout incorporated into the LSTM.

The hyperparameters were determined empirically through multiple training iterations and observing the obtained results, aiming to find their optimal values.

In the second step, I tried to significantly reduce perplexity on the WikiText2 dataset by employing the techniques described in the research paper "Regularizing and Optimizing LSTM Language Models," known as AWD-LSTM (ASGD Weight-Dropped LSTM). Each regularization technique was implemented separately and then combined with the previous technique. The following list presents the implemented techniques:

1. Weight-Dropped LSTM
2. NTASGD optimizer
3. Combination of Weight Drop and NTASGD
4. Variational Dropout
5. Combination of Weight Drop, NTASGD, and Variational Dropout
6. Embedding Dropout
7. Combination of WD, NTASGD, VD, and ED
8. Weight Tying
9. Combination of WD, NTASGD, VD, ED, and WT

After going through all these steps, I attempted to select the best method and apply the best combination of techniques. The combination of the best techniques was determined based on experiments and multiple training iterations. Although not all techniques, including sentence length variation, were implemented in this project, I tried to incorporate most of the mentioned techniques from the research paper to improve the results.

#Dependencies:
* Python: 3.10.12
* torch: 2.0.1+cu118
* torchtext: 0.15.2+cpu
* numpy: 1.23.5
* pandas: 1.5.3
* tqdm: 4.66.1

