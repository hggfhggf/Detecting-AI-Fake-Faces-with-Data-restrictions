# AI Fake Face Detection

Solution to an interesting task from the **Artificial Intelligence Implementation Show Winter Contest**.

The problem is framed as hunting “ghosts,” which in practice means detecting AI-generated fake faces. The main restriction is that the training set contains only real human faces, while the test set contains a mix of real and fake faces. The goal is to build a classifier without using any external data.

## Approach

My first approach identified 201 test images that differed the most from the real training images based on the standard deviation of image color channels. I treated these images as likely fake and trained a simple classifier, achieving about **0.75 F1-score**.

After further data analysis, I noticed that fake faces often looked overly smooth and visually mixed. Based on this observation, I generated synthetic fake examples by merging pairs of random real images.

Then I extracted embeddings using **ResNet18** and trained a simple **scikit-learn Logistic Regression** classifier on this generated data. This approach achieved about **0.92 F1-score**.

## Repository Contents

This repository contains:

- `data/train` — real human face images used for training
- `data/test` — mixed real and fake face images used for testing
- Jupyter Notebook solution written in Python

## Result

Best solution: **0.92 F1-score**

## Problem

Problem link:  
https://judge.nitro-ai.org/competitions/aiis/aiis-winter-contest/2

## Credits

Special thanks to **Morariu Tudor** (@morariutudor) and **Alexandru Ionut Tone** (@tonealexandru236) for designing this problem.
