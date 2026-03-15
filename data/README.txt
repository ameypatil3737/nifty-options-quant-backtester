

# Data Folder

This folder contains **sample data required to understand the structure of the dataset used by the strategy**.

Due to GitHub file size limitations, the **complete dataset is not included in this repository**.

## Sample File Included

`NIFTY_OPTIONS_SAMPLE.parquet`

This is a **small sample extracted from the full dataset** and is provided only for:

* Understanding the **data schema**
* Testing the **code structure**
* Running quick examples

This file **cannot be used for full backtesting**.

---

# How to Download Full Dataset

Step 1 — Download the raw data from Kaggle

Dataset link:

[https://www.kaggle.com/datasets/senthilkumarvaithi/historical-nifty-options-2024-all-expiries](https://www.kaggle.com/datasets/senthilkumarvaithi/historical-nifty-options-2024-all-expiries)

Download the dataset and extract it locally.

---

Step 2 — Generate consolidated parquet file

Run the notebook:

```
FNO 2024 Nifty50 Data Consolidator.ipynb
```

This notebook processes all expiries and creates a **single consolidated dataset** required for the strategy.

The notebook will generate:

```
NIFTY_OPTIONS_2024_CONSOLIDATED.parquet
```

---

Step 3 — Place the file in the data folder

Move the generated file into this folder:

```
data/NIFTY_OPTIONS_2024_CONSOLIDATED.parquet
```

---

# Final Folder Structure

```
project_root
│
├── data
│   ├── README.md
│   ├── NIFTY_OPTIONS_SAMPLE.parquet
│   └── NIFTY_OPTIONS_2024_CONSOLIDATED.parquet   (generated from Kaggle data)
│
├── FNO 2024 Nifty50 Data Consolidator.ipynb
├── main_strategy.py
└── README.md
```

---

# Important Note

The consolidated dataset is approximately **900MB**, which exceeds GitHub’s recommended file size limits.

Therefore only a **sample dataset is provided in this repository**.
