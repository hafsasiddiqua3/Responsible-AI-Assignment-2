# Responsible & Explainable AI — Assignment 2
Auditing a BERT-based Content Moderation Classifier

## Environment
- Python 3.12
- GPU: NVIDIA T4 (Kaggle free tier)
- Training: ~30 min per DistilBERT fine-tune

## Dataset
Jigsaw Unintended Bias in Toxicity Classification (train.csv only).
Not committed to repo — download from:
https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification

## Reproduction
1. Download `train.csv` from the Kaggle competition above
2. `pip install -r requirements.txt`
3. Update dataset paths in Part 1's notebook
4. Run notebooks in order: part1 → part2 → part3 → part4 → part5

## Files
- `part1.ipynb` — baseline DistilBERT fine-tuning
- `part2.ipynb` — bias audit (high-black vs reference cohorts)
- `part3.ipynb` — adversarial attacks (evasion, poisoning)
- `part4.ipynb` — mitigation (reweighing, threshold opt, oversampling)
- `part5.ipynb` — guardrail pipeline demo
- `pipeline.py` — ModerationPipeline class

## Key results
- Baseline EOD: 0.183 (under-flags high-black cohort)
- Best mitigation: Threshold Optimization (EOD → 0.025, F1 cost 0.003)
- Attack 1 (evasion) ASR: 99.4%
- Pipeline auto-action F1: [fill in from your Cell 5 output]
