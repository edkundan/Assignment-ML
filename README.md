

```markdown
# Freight Rate Prediction - Spotter ML Assessment

This repository contains the model and workflow for the Spotter Machine Learning Engineer assessment. The objective is to predict freight rates for December 2025 using a time-series validated historical dataset.

## Project Structure
* `Assignment.ipynb`: The primary Jupyter Notebook containing data preprocessing, time-series feature engineering, model training (HistGradientBoostingRegressor), and inference.
* `score.py`: The official evaluation script used to validate the output format and generate the final predictions chart.
* `requirements.txt`: Python package dependencies.
* Data files: `train-test.csv`, `validation.csv`, `december-chart-inputs.csv`, and `validation-predictions-template.csv` are required in the root directory to execute the pipeline.

## Execution Instructions

### Option 1: Running via Google Colab (Recommended)
1. Open Google Colab and upload `Assignment.ipynb`.
2. Open the file explorer on the left sidebar and upload `score.py`, `requirements.txt`, and the four CSV data files into the default session storage.
3. Execute the cells sequentially. The first cell will install the necessary dependencies (`!pip install -r requirements.txt`).
4. The main code cell will train the model, handle data anomalies, and output the two required prediction files: `validation_predictions.csv` and the updated `december-chart-inputs.csv`.
5. The final cell runs the official scorer:
   ```bash
   !python score.py --predictions validation_predictions.csv --december-predictions december-chart-inputs.csv

```

6. Download `validation_predictions.csv` and the generated chart from the newly created `scorer_results/` folder.

### Option 2: Running Locally

1. Clone this repository and open the project folder in your terminal.
2. Install the required dependencies:
```bash
pip install -r requirements.txt

```


3. Run all cells in `Assignment.ipynb` using Jupyter Notebook or your preferred IDE (e.g., VS Code).
4. Open your terminal in the exact same directory and validate the generated outputs:
```bash
python score.py --predictions validation_predictions.csv --december-predictions december-chart-inputs.csv

```


5. Retrieve the output visualization from the `scorer_results/` directory.

---

**Author:** Kundan Kumar

**Contact:** Exchandanlife2001gmail.com

```

```
