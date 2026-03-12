# starter code

# CS4375 Assignment - Neural Networks for Sentiment Analysis

## Overview
This project implements two neural network models (FFNN and RNN) to predict Yelp review star ratings (1-5). The main task was completing the `forward()` function in both models.

## Setup
```bash
conda create -n cs4375 python=3.8
conda activate cs4375
pip install torch numpy tqdm
```

## Running the Models

**FFNN**
```bash
python ffnn.py --hidden_dim 64 --epochs 5 --train_data training.json --val_data validation.json
```

**RNN**
```bash
python rnn.py --hidden_dim 64 --epochs 5 --train_data training.json --val_data validation.json
```

## Results

| Model | Hidden Dim | Epochs | Best Val Accuracy |
|-------|------------|--------|------------------|
| FFNN  | 64         | 5      | 59.8%            |
| FFNN  | 128        | 10     | 61.6%            |
| RNN   | 64         | 6      | 55.9%            |

## Files
- `ffnn.py` - Feedforward Neural Network implementation
- `rnn.py` - Recurrent Neural Network implementation
- `training.json` - Training data
- `validation.json` - Validation data
- `word_embedding.pkl` - Pretrained word embeddings (required for RNN)
