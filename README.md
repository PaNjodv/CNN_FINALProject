# Where Does My CNN Make Its Mistakes? — MNIST Digit Classification & Error Analysis
 
## Overview
This is my first project that trains a convolutional neural network (CNN) to classify handwritten digits from the **MNIST** dataset, then investigates *where* and *why* it makes mistakes. Beyond raw accuracy, the goal is to understand the model's failure patterns using a confusion matrix, then test whether a controlled architectural change shifts those patterns.

## Dataset
- **MNIST** — 70,000 grayscale images (28x28) of handwritten digits (0–9).
 
**Scenario:** Systems like postal sorting machines and bank check readers rely on automated handwriting recognition. A misread digit isn't a harmless error — it can misroute mail or misdirect a payment. This project treats error analysis as seriously as accuracy.
 
**Central question:** Where does the CNN make its mistakes, and does one change to the model move them?

## Results
 
| Model | Accuracy | Most Confused Pair(s) |
|---|---|---|
| Baseline CNN | *fill in* | *fill in, e.g. 4 vs 9* |
| Modified CNN | *fill in* | *fill in* |
 
*Fill in the confusion matrix images or a short table once you've run the notebook.*

## Ethical Considerations
- **Handwriting variability:** The model's reliability may vary across different handwriting styles, ages, and cultural conventions in how digits are written — MNIST itself is not fully representative of real-world handwriting diversity.
- **Confident misreadings:** A model that is *confidently wrong* is more dangerous in an automated pipeline than one that flags uncertainty, since confident errors are less likely to be caught by a human reviewer. This is especially relevant for postal routing or financial transactions, where a misread digit has real downstream cost.
