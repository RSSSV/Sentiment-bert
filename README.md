# Sentiment analysis by BERT in PyTorch
BERT is state-of-the-art natural language processing model from Google. Using its latent space, it can be repurpossed for various NLP tasks, such as sentiment analysis.

This simple wrapper based on [Transformers](https://github.com/huggingface/transformers) (for managing BERT model) and PyTorch achieves 92% accuracy on guessing positivity / negativity on IMDB reviews.

# How to use

## Prepare data

First, you need to prepare IMDB data which are publicly available. Format used here is one review per line, with first 12500 lines being positive, followed by 12500 negative lines.

## Train weights

Training with default parameters can be performed simply by.

`python script.py --train`

Optionally, you can change output dir for weights or input dir for dataset.

## Evaluate weights

You can find out how great simply by running

`python script.py --evaluate`

Of course, you need to train your data first or get them from my drive.

## Predict text

`python script.py --predict "It was truly amazing experience."`

or

`python script.py --predict "It was so terrible and disgusting as coffee topped with ketchup."`
