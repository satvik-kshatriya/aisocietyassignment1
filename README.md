# CSET485 – AI and Society, Assignment 1

**Satvik Kshatriya · S24CSEU0479**
Dataset: Adult Census Income (last digit 9) · Random seed: **479** · Split: 70% train / 30% test

This repository holds the code behind the PDF report. Every number, table and figure in the report is produced by one notebook.

## Run it

```bash
pip install -r requirements.txt
jupyter notebook CSET485_A1_S24CSEU0479.ipynb   # Kernel -> Restart & Run All
```

or without opening Jupyter:

```bash
jupyter nbconvert --to notebook --execute --inplace CSET485_A1_S24CSEU0479.ipynb
```

It takes about one minute. The raw data is in `data/`. If a file is missing, the notebook downloads it from UCI.

## What is where

| Path | Content |
|---|---|
| `CSET485_A1_S24CSEU0479.ipynb` | Full analysis with explanations and saved outputs |
| `data/adult.data`, `data/adult.test` | Adult Census Income (UCI) |
| `data/census-income-kdd.zip` | Census-Income (KDD) from UCI, used only for the hidden-confound test in Part 2.2 |
| `results/results.json` | Every number quoted in the report |
| `results/figures/` | The six figures |
| `results/*.csv` | Tables: coefficients, subgroup models, omitted-variable test, fairness sweep, group thresholds, repair experiment, the 50 adversarial rows |

## Where each report section is computed

| Report section | Notebook section |
|---|---|
| Data Preprocessing | 1 |
| Part 1, Question 1 | 2 |
| Part 2.1, Question 2 | 3 |
| Part 2.2, Questions 3 and 4 | 4 (the residual audit is in 7) |
| Part 2.3, Question 5 | 5 |
| Part 2.4, Questions 6 to 8 | 6 and 7 |
| Part 4 | 7 |

Tested with Python 3.12, numpy 2.5.5, pandas 3.1.1, scipy 1.18.1, scikit-learn 1.9.1, statsmodels 0.15.0 and matplotlib 3.11.2.
