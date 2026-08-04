# diabetes-prediction-svm
Ein Machine-Learning-Projekt zur Klassifikation, ob eine Person anhand medizinischer Messwerte an Diabetes erkrankt ist. Implementiert mit scikit-learn in Python.

Datensatz

Pima Indians Diabetes Database (Kaggle / UCI Machine Learning Repository) — 768 Patientinnen, 8 medizinische Merkmale (u. a. Glukosewert, Blutdruck, BMI, Alter) sowie die Zielvariable Outcome (0 = kein Diabetes, 1 = Diabetes).

Vorgehen
Explorative Datenanalyse — Struktur, Datentypen, Duplikate
Behandlung fehlender Werte — mehrere Merkmale enthalten medizinisch unplausible Nullwerte (z. B. Blutdruck = 0), die als fehlend erkannt und per Median-Imputation (gruppiert nach Outcome) ersetzt wurden
Standardisierung der Merkmale mit StandardScaler
Train/Test-Split (80/20, stratifiziert)
Modelltraining — SVM mit linearem Kernel
Evaluation — Accuracy, Confusion Matrix, Classification Report
Ergebnisse
Metrik	Wert
Accuracy (Training)	78,5 %
Accuracy (Test)	75,3 %
Precision (Diabetic)	0,69
Recall (Diabetic)	0,54
F1-Score (Diabetic)	0,60

Da die Klassen unbalanciert sind (500 vs. 268 Fälle), ist neben der Accuracy besonders der Recall für die Klasse "Diabetic" relevant.

Tech Stack
Python 3
pandas, numpy
scikit-learn
Jupyter Notebook
Der Datensatz (data/diabetes.csv) kann von Kaggle heruntergeladen und im Ordner data/ abgelegt werden.

Mögliche Erweiterungen
Hyperparameter-Tuning mit GridSearchCV
Cross-Validation statt einzelnem Train/Test-Split
Vergleich mit weiteren Modellen (Random Forest, Logistic Regression)
Feature-Importance-Analyse
Autor

Eseosa Idemudia
