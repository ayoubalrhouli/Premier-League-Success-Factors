# Premier League Success Factors

Data mining project analysing what drives match results in the **2018/2019 English Premier League** season: 380 matches, 66 variables.

The notebook (written in French) runs a full data mining pipeline:

- **Data cleaning and exploratory analysis**: univariate, bivariate and multivariate statistics, Cronbach reliability
- **Association rules (Apriori)**: patterns that co-occur with home wins and high-scoring matches
- **Logistic regression**: multinomial model predicting the match outcome (home win / draw / away win) and the factors behind it
- **K-Means clustering**: groups matches into profiles (K = 3), visualised with PCA

## Results

| Metric (logistic regression, 3 classes) | Value |
|---|---|
| Accuracy (20% test set, 76 matches) | 0.67 |
| Macro precision / recall / F1 | 0.58 / 0.58 / 0.56 |
| Cross-validated accuracy | 0.60 ± 0.04 |

The model uses match statistics (shots on target, possession, corners, cards), so it explains which factors are linked to a result rather than forecasting a match before kick-off.

## Tech Stack

Python · pandas · NumPy · SciPy · scikit-learn · mlxtend · Matplotlib · Seaborn

## Dataset

[England Premier League 2018 to 2019 Stats](https://www.kaggle.com/datasets/yusukefromjpn/england-premier-league-2018-to-2019-stats) on Kaggle (one row per match, 380 rows × 66 columns).

The data file is not included in this repository. Download it from the link above and save it as:

```
data/england-premier-league-matches-2018-to-2019-stats.csv
```

## Run it

```bash
git clone https://github.com/ayoubalrhouli/Premier-League-Success-Factors.git
cd Premier-League-Success-Factors
pip install -r requirements.txt
jupyter notebook Premier_League_Success_Factors.ipynb
```

## Project structure

```
├── Premier_League_Success_Factors.ipynb
├── data/                 # place the CSV here
├── requirements.txt
└── README.md
```
