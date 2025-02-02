# TOPSIS Method for Selecting the Best Pretrained Model for Dialogue Generation

## Overview
This project implements the TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution) method to evaluate and rank pretrained models for dialogue generation based on multiple performance criteria.

## 1. Models and Evaluation Criteria
The following pretrained models are evaluated:
- DialoGPT
- BlenderBot
- ChatGPT-Turbo
- Mistral
- Gemini Nano

The criteria for evaluation include:
- **BLEU Score** (Higher is better)
- **Diversity Score** (Higher is better)
- **Latency (ms)** (Lower is better)
- **Parameter Size (GB)** (Lower is better)

### Decision Matrix
| Model         | BLEU Score | Diversity Score | Latency (ms) | Parameter Size (GB) |
|--------------|------------|----------------|--------------|------------------|
| DialoGPT     | 30         | 0.75           | 120          | 6.5              |
| BlenderBot   | 35         | 0.78           | 150          | 8.0              |
| ChatGPT-Turbo| 40         | 0.80           | 100          | 12.0             |
| Mistral      | 38         | 0.77           | 110          | 10.5             |
| Gemini Nano  | 36         | 0.79           | 130          | 7.8              |

## 2. Implementation Steps
The TOPSIS method is applied using the following steps:
1. Normalization of the decision matrix.
2. Weighted normalization of the decision matrix.
3. Calculation of ideal best and worst solutions.
4. Distance computation from the ideal solutions.
5. Calculation of TOPSIS scores for each model.
6. Ranking of models based on the scores.

## 3. Code Execution
The implementation is provided in the Jupyter Notebook: `102217161_Topsis_TextGeneration.ipynb`.

## 4. Results
### Final Rankings:
| Rank | Model          | TOPSIS Score |
|------|--------------|--------------|
| 1    | ChatGPT-Turbo | 0.5621       |
| 2    | Mistral       | 0.5302       |
| 3    | Gemini Nano   | 0.4985       |
| 4    | BlenderBot    | 0.4653       |
| 5    | DialoGPT      | 0.4398       |

### TOPSIS Output:
A bar chart is generated to visualize the rankings.

## 5. Usage
1. Clone this repository.
2. Run `102217161_Topsis_TextGeneration.ipynb` in Jupyter Notebook.
3. Modify the dataset to evaluate different models.

## 6. Conclusion
Using the TOPSIS method, we effectively ranked pretrained models for dialogue generation based on multiple criteria, providing a systematic approach for model selection.

### Results
**Final Rankings:**
![img.png](img.png)

**TOPSIS Output:**
![img_1.png](img_1.png)
