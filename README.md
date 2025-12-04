# Personal_Project_Transformer_Translator

## Goal

- Reproduction Transformer and applying it to translate English to French
- Check the performance between Attention Translator (in book) and Transformer Translator (self-made)

## Constraints

- GPU : 1 NVIDIA T4 (by using Colab)
- Storage limitation : 100MB (by using Colab)

## Duration

- 2025.04.10 ~ 2025.04.24 (During Military Services)

## Members

- Wonje Jang (Solo)

## Details

- Data & Data Preprocessing Method is in [here](https://wikidocs.net/216494).
- Adam optimizer was used (learning rate : 0.0003)
- After training, I checked the real context which is the output of model.
- I closely followed the model architecture in the paper.

## Results

<img width="450" height="399" alt="image" src="https://github.com/user-attachments/assets/4a218eca-4a49-473e-887a-442c7368b59f" />


- Comparing Attention Translator, Transformer Translator show better performance. (Hyper-Parameters except learning rate (0.001 → 0.0003) are all same.)
    - 
    
    |  | Best Valid Loss | Best Valid Accuracy |
    | --- | --- | --- |
    | Attention Translator | 1.4412 | 0.7268 |
    | Transformer Translator | 1.1299 | 0.7739 |

## What I Learned

1. Learn the exact transformer’s architecture
    - especially, Self-attention architecture, positioning encoding, Multi-head architecture, and so on
    - Reading paper and Realization to code is very different. In code, we should reflects on how to realize the content from paper to the code.
2. Data Preprocessing is also very important part.
    - There are a lot of parts to check.
        - Regular Expression may have huge impact on model’s performance.
        - Designating special tokens such as <PAD>, <EOS>, etc must be applied in loss function.
3. When defining the learning rate, both the dataset size and the model scale should be considered.
