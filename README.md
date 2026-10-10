# PR. 2 – Derivable Judgement
## Inferential Statistics and Hypothesis Testing

### 📌 Project Overview

**Derivable Judgement** is a Python-based data analysis project focused on **Inferential Statistics and Hypothesis Testing**. This project combines theoretical statistical concepts with practical analysis using a diabetes-related dataset.

The notebook explores statistical relationships between variables such as age, Body Mass Index (BMI), smoking status, and diabetes status. It applies various statistical tests to compare groups, evaluate hypotheses, estimate confidence intervals, and analyze correlations between numerical variables.

The project is implemented in Jupyter Notebook using Python and its scientific computing libraries.

### 🎯 Objectives

- Understand the fundamentals of inferential statistics.
- Learn the concepts and steps involved in hypothesis testing.
- Calculate confidence intervals, critical values, and p-values.
- Apply Z-tests, T-tests, Chi-square tests, and ANOVA.
- Analyze covariance and correlation between numerical variables.
- Compare BMI across smoking-status groups.
- Investigate age differences between diabetes and non-diabetes groups.
- Visualize relationships between age and BMI.
- Export the analyzed dataset to a CSV file.

### 📚 Concepts Covered

**1. Inferential Statistics**

Using sample data to draw conclusions about a larger population, estimate parameters, and test statistical assumptions.

**2. Hypothesis Testing**

A statistical method used to evaluate claims about a population using:

- Null Hypothesis (H₀)
- Alternative Hypothesis (H₁)
- Significance Level (α)
- Test Statistic
- P-value
- Statistical Conclusion

**3. Confidence Intervals and Critical Values**

A confidence interval provides a range of plausible values for a population parameter. Critical values help determine the threshold for rejecting the null hypothesis.

**4. P-value and Significance Level**

The p-value indicates how unusual the observed result, or a more extreme result, would be under the null hypothesis.

This project commonly uses a significance level of **α = 0.05**.

- If p-value < 0.05, reject the null hypothesis.
- If p-value ≥ 0.05, fail to reject the null hypothesis.

**5. Type I and Type II Errors**

- **Type I Error:** Rejecting a null hypothesis that is actually true (false positive).
- **Type II Error:** Failing to reject a null hypothesis that is actually false (false negative).

**6. Statistical Tests**

- **Z-test:** Tests means or proportions when the relevant normal-based assumptions are satisfied.
- **T-test:** Compares means, particularly when the population standard deviation is unknown.
- **Chi-square Test:** Examines associations between categorical variables or differences between observed and expected frequencies.
- **One-way ANOVA:** Compares the means of three or more independent groups.

**7. Covariance**

Measures how two numerical variables vary together. Positive covariance indicates movement in the same direction, while negative covariance indicates movement in opposite directions.

**8. Correlation**

Measures the strength and direction of a linear relationship between two numerical variables. The correlation coefficient ranges from -1 to +1.

### 🔬 Practical Analysis

The Jupyter Notebook performs the following statistical analyses:

| Analysis | Description |
|---|---|
| Age vs. Diabetes | Uses Welch's independent-samples T-test to compare the mean ages of diabetes and non-diabetes groups. |
| Confidence Interval | Calculates the mean age, standard error, critical T-value, margin of error, and 95% confidence interval. |
| BMI vs. Smoking Status | Compares the mean BMI of smokers and non-smokers using an independent-samples T-test. |
| BMI Z-test | Compares the sample mean BMI against a reference mean of 25, assuming a population standard deviation of 4. |
| Chi-square Test | Examines the association between smoking status and diabetes status. |
| One-way ANOVA | Compares mean BMI across smoking-status groups. |
| Covariance and Correlation | Calculates covariance and correlation matrices for age and BMI. |
| Data Visualization | Creates a scatter plot showing the relationship between age and BMI. |
| CSV Export | Saves the dataset as `derivable_judgement_dataset.csv`. |

### 🛠️ Technologies and Libraries

- **Python** – Programming language
- **Jupyter Notebook** – Interactive development environment
- **NumPy** – Numerical computations
- **Pandas** – Data manipulation and analysis
- **SciPy** – Statistical tests and probability distributions
- **Matplotlib** – Data visualization

### 📂 Project Structure

```text
PR-2-Derivable-Judgement/
│
├── PR. 2 Derivable Judgement.ipynb
├── Derivable Judgement.csv
├── derivable_judgement_dataset.csv
├── README.md
└── requirements.txt
```

*Note: The input dataset and exported CSV are shown as expected project files. Include them in your repository only when available and permitted to share.*

### 📊 Dataset Requirements

The notebook requires a CSV dataset containing the following columns:

| Column | Description | Expected Data |
|---|---|---|
| `age` | Age of the individual | Numerical |
| `bmi` | Body Mass Index | Numerical |
| `diabetes` | Diabetes status | Boolean (`True` / `False`) |
| `smoking_status` | Smoking category | Categorical, such as `Smoker` and `Non-Smoker` |

**Important:** The notebook currently uses Boolean filtering for the `diabetes` column. If your dataset contains values such as `Yes` and `No`, convert them to Boolean values or update the filtering logic before running the notebook.

### ⚙️ Installation

**Step 1: Install Python**

Install Python from the official website:

https://www.python.org/downloads/

**Step 2: Install the required libraries**

Run the following command in your terminal:

```bash
pip install numpy pandas scipy matplotlib jupyter
```

**Step 3: Download or clone the repository**

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

Navigate to the project folder:

```bash
cd PR-2-Derivable-Judgement
```

### ▶️ How to Run the Notebook

1. Place the Jupyter Notebook and required CSV dataset in the project folder.
2. Open a terminal in that folder.
3. Start Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Open `PR. 2 Derivable Judgement.ipynb`.
5. Update the dataset path in the CSV-loading cell.

   Example:

   ```python
   import pandas as pd

   DF = pd.read_csv("Derivable Judgement.csv")
   ```

6. Verify the dataset column names, data types, and missing values.
7. Run all notebook cells from top to bottom.
8. Review the statistical results, confidence interval, matrices, and scatter plot.
9. Confirm that `derivable_judgement_dataset.csv` is generated in the current working directory.

### 📈 Expected Outputs

After successfully running the notebook, you should obtain:

- A preview of the dataset.
- T-test statistics and p-values.
- A 95% confidence interval for mean age.
- A Z-statistic and p-value for the BMI reference comparison.
- A contingency table and Chi-square test results.
- ANOVA F-statistic and p-value.
- Covariance and correlation matrices for age and BMI.
- A scatter plot titled **Correlation between Age and BMI**.
- An exported CSV file named `derivable_judgement_dataset.csv`.

*Note: Exact numerical results depend on the dataset and its contents.*

### 🧠 Interpreting the Results

The notebook uses a significance level of 0.05 to support statistical decisions.

- **p-value < 0.05:** Reject the null hypothesis.
- **p-value ≥ 0.05:** Fail to reject the null hypothesis.

A statistically significant result suggests evidence against the null hypothesis under the assumptions of the test. However, a p-value does not measure the practical importance of a result.

Similarly, statistical association does not establish causation. Results should be interpreted alongside the test assumptions, sample size, effect sizes, and data quality.

### ⚠️ Important Notes and Limitations

- The original dataset path is specific to a Windows computer. A relative path is recommended for portability.
- The diabetes column must be compatible with the notebook's Boolean filtering expressions.
- The BMI Z-test uses a reference mean of 25 and a population standard deviation of 4. These assumptions should be verified before interpreting the result.
- The ANOVA implementation compares BMI across smoking-status groups. Its written explanation should match this actual analysis.
- The T-tests compare group means and do not establish that smoking causes diabetes.
- The Chi-square test evaluates association, not causation.
- Statistical tests should be checked for their relevant assumptions before conclusions are drawn.
- The output CSV is saved in the notebook's current working directory.
- The dataset is not included automatically; provide the required CSV separately if sharing is permitted.

### 🚀 Future Improvements

- Replace machine-specific file paths with relative paths.
- Add a `requirements.txt` file for dependency management.
- Add data validation and missing-value handling.
- Validate column names, data types, and category values.
- Clearly define H₀ and H₁ for every hypothesis test.
- Add test-specific interpretations and conclusions.
- Check statistical assumptions and report effect sizes.
- Improve visualizations with labels, legends, and informative titles.
- Add a sample dataset or data-source documentation when permitted.

### 👨‍💻 Author

**Nitin Singh**

Student | Artificial Intelligence and Machine Learning (AIML)

**Project:** PR. 2 – Derivable Judgement  
**Domain:** Inferential Statistics and Hypothesis Testing  
**Tools:** Python, Jupyter Notebook, NumPy, Pandas, SciPy, Matplotlib

---

### 📄 License

This project is intended for educational and learning purposes. Add a suitable open-source license if you intend to distribute the project publicly.
