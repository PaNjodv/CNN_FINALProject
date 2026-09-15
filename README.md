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
| Baseline CNN | *98.7* | *{1,7} and {9,7}* |
| Modified CNN | *98.9* | *{9,4} and {9,7}* |


ORIGINAL
<img width="427" height="455" alt="image" src="https://github.com/user-attachments/assets/69640209-be32-4579-af88-2e4ab900e6ee" />
MODIFIED
<img width="427" height="455" alt="image" src="https://github.com/user-attachments/assets/9913b78f-1d9b-43db-87e4-703c83b5b77a" />


## Ethical Considerations
- **Handwriting variability:** The model's reliability may vary across different handwriting styles, ages, and cultural conventions in how digits are written — MNIST itself is not fully representative of real-world handwriting diversity.
- **Confident misreadings:** A model that is *confidently wrong* is more dangerous in an automated pipeline than one that flags uncertainty, since confident errors are less likely to be caught by a human reviewer. This is especially relevant for postal routing or financial transactions, where a misread digit has real downstream cost.
