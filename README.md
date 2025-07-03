# **Task-7: Support Vector Machines (SVM)**

### **Dataset**

* **File:** `breast-cancer.csv`
* **Location:** Local upload
* **Target Variable:** `diagnosis`
  * `M` = Malignant
  * `B` = Benign

### **Tools & Libraries**

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

### **Steps Performed**

1. **Loaded the dataset**
   * Removed the `id` column.
   * Used `head()` and `info()` to explore the structure.
2. **Preprocessed the data**
   * Encoded `diagnosis` using **Label Encoding** (M = 1, B = 0).
   * Selected two features (`radius_mean`, `texture_mean`) for 2D visualization.
   * Standardized features using **StandardScaler**.
3. **Split into Train-Test sets**
   * Used **80% training**, **20% testing** with `train_test_split()`.
4. **Trained SVM Models**
   * Built **SVM with Linear Kernel** using `SVC(kernel='linear')`.
   * Built **SVM with RBF Kernel** using `SVC(kernel='rbf')`.
5. **Hyperparameter Tuning**
   * Applied **GridSearchCV** to optimize `C` and `gamma` for RBF kernel.
6. **Evaluated Model Performance**
   * Measured:
     * **Accuracy**
     * **Confusion Matrix**
     * **Classification Report** (Precision, Recall, F1-score)
7. **Visualized Decision Boundary**
   * Plotted decision regions using `radius_mean` and `texture_mean` features.
   * Used `plot_decision_regions()` for clear boundary illustration.

### **Output**

* **Evaluation Metrics:**
  * Accuracy and confusion matrix for both linear and RBF models.
  * Best parameters from GridSearchCV.
* **Decision Boundary Plot:**
  * Visualized classification boundary using 2D feature space.
* **Conclusion:**
  * SVM with RBF kernel performed well on non-linear patterns.
  * Standardization and hyperparameter tuning improved performance.
