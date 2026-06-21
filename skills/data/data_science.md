# Data Science & Analytics | علوم البيانات والتحليل

## Arabic Description | وصف بالعربية
قواعد صارمة لعلوم البيانات والتحليل الإحصائي. تضمن هذه القواعد دقة النتائج، سهولة تكرار التجارب (Reproducibility)، ووضوح الرؤى المستخرجة من البيانات.

---

## Strict Rules | قواعد صارمة

### 1. Data Exploration (EDA)
- **Visual Analysis**: Always visualize distributions, correlations, and outliers before modeling.
- **Data Cleaning Documentation**: Document every step of data cleaning and preprocessing. Explain *why* certain data was removed or imputed.

### 2. Notebook Standards (Jupyter)
- **Cell Order**: Notebooks MUST run from top to bottom without errors.
- **Minimal Code in Notebooks**: Move complex logic, helper functions, and classes to external `.py` files.
- **Markdown Documentation**: Use Markdown cells to explain the narrative and findings of the analysis.

### 3. Statistical Rigor
- **Hypothesis Testing**: Clearly state null and alternative hypotheses before testing.
- **P-values**: Never rely solely on p-values. Report effect sizes and confidence intervals.
- **Sample Bias**: Always check for and document potential biases in the dataset.

### 4. Visualization Best Practices
- **Labeling**: Every chart MUST have a title, labeled axes (with units), and a legend if necessary.
- **Integrity**: Avoid misleading visualizations (e.g., non-zero y-axis for bar charts unless justified).

### 5. Reproducibility
- **Fixed Seeds**: Use fixed random seeds for all stochastic processes (splitting, modeling).
- **Environment Specs**: Provide a `requirements.txt` or `environment.yml` for the specific analysis environment.
