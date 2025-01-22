# Wine Quality Prediction

This project demonstrates the use of machine learning to predict wine quality based on physicochemical properties using an **ElasticNet** regression model. The experiment tracks model parameters and performance metrics using **MLflow**.

## Dataset

The dataset used for this project is the [Wine Quality Data Set](http://archive.ics.uci.edu/ml/datasets/Wine+Quality) from the UCI Machine Learning Repository:

- P. Cortez, A. Cerdeira, F. Almeida, T. Matos and J. Reis.  
  *Modeling wine preferences by data mining from physicochemical properties*.  
  In Decision Support Systems, Elsevier, 47(4):547-553, 2009.

The dataset is hosted publicly [here](https://raw.githubusercontent.com/mlflow/mlflow/master/tests/datasets/winequality-red.csv).

## Prerequisites

- Python 3.7+
- Required Python packages:
  ```bash
  pip install pandas numpy scikit-learn mlflow
  ```

## How to Run

1. Clone this repository and navigate to the project directory.

2. Run the script to train the model:
   ```bash
   python <script_name.py> [alpha] [l1_ratio]
   ```
   Replace `<script_name.py>` with the script's name and optionally specify `alpha` and `l1_ratio` parameters for the ElasticNet model.

3. Example command with default values:
   ```bash
   python script_name.py
   ```

4. The output includes metrics like RMSE, MAE, and R² for the model's performance.

## MLflow Integration

The script uses MLflow to:
- Log model parameters (`alpha` and `l1_ratio`).
- Log model performance metrics (`rmse`, `mae`, `r2`).
- Save and optionally register the trained model.

## For dagshub
import dagshub
dagshub.init(repo_owner='ajuarjun528', repo_name='mlflow-sample', mlflow=True)


## Output

The following metrics are calculated:
- **RMSE**: Root Mean Squared Error.
- **MAE**: Mean Absolute Error.
- **R²**: R-squared score.

The trained model is saved and optionally registered in the MLflow Model Registry if an appropriate tracking URI is set.

## References

- [MLflow Documentation](https://mlflow.org/docs/latest/index.html)
- [UCI Wine Quality Dataset](http://archive.ics.uci.edu/ml/datasets/Wine+Quality)
