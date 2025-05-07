# Diyabet (Diabetes) Sınıflandırması

Bu proje, diyabet hastalığını sınıflandırmak için makine öğrenmesi algoritmalarını ve veri artırma (oversampling) tekniklerini kullanır. Veri analizi, eksik değer işlemleri, model karşılaştırmaları ve hiperparametre optimizasyonu adımlarını içerir.

## İçerik
- Veri Analizi ve Görselleştirme
- Eksik Değer İşlemleri
- Özellik Ölçeklendirme
- Veri Artırma (ADASYN, SMOTE, RandomOverSampler vb.)
- Model Karşılaştırması (Lojistik Regresyon, Random Forest, XGBoost, LightGBM)
- Hiperparametre Optimizasyonu
- Sonuçların Yorumlanması

## Veri Seti
Kullanılan veri seti [Pima Indians Diabetes Database](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database) olup, `diabetes.csv` dosyasında yer almaktadır.

| Sütun Adı                  | Açıklama                        |
|----------------------------|---------------------------------|
| Pregnancies                | Gebelik sayısı                  |
| Glucose                    | Glikoz düzeyi                   |
| BloodPressure              | Kan basıncı                     |
| SkinThickness              | Deri kalınlığı                  |
| Insulin                    | İnsülin seviyesi                |
| BMI                        | Vücut kitle indeksi             |
| DiabetesPedigreeFunction   | Soy ağacı fonksiyonu            |
| Age                        | Yaş                             |
| Outcome                    | Diyabet (1) / Sağlıklı (0)      |

## Kurulum

1. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn xgboost lightgbm
   ```
2. `diabetes.csv` dosyasını proje klasörüne ekleyin.
3. Python dosyasını çalıştırın:
   ```bash
   python diabetes_classification_optimized.py
   ```

## Kullanım
- Kod, veri setini okur, eksik değerleri işler, veri artırma uygular ve çeşitli modellerle sınıflandırma yapar.
- Sonuçlar ve önemli değişkenler ekrana yazdırılır ve grafikler olarak gösterilir.

## Modelleme Adımları
1. **Veri Yükleme ve Temizleme**: Eksik ve sıfır değerlerin analizi ve doldurulması.
2. **Veri Bölme**: Eğitim ve test setlerine ayırma.
3. **Ölçeklendirme**: Özelliklerin standartlaştırılması.
4. **Veri Artırma**: ADASYN veya başka bir oversampling yöntemi ile dengesiz veri problemi çözülür.
5. **Model Eğitimi ve Karşılaştırma**: Farklı algoritmalar ile eğitim ve test sonuçlarının karşılaştırılması.
6. **Hiperparametre Optimizasyonu**: GridSearchCV ile en iyi model parametrelerinin bulunması.
7. **Sonuçların Görselleştirilmesi**: ROC eğrisi ve önemli değişkenlerin grafikleri.

## Notlar
- Kodda ADASYN dışında SMOTE veya RandomOverSampler gibi yöntemler de kolayca kullanılabilir.
- Sonuçlar, veri setinin dengesizliğine ve seçilen modele göre değişiklik gösterebilir.

---

# Diabetes Classification (English)

This project uses machine learning algorithms and oversampling techniques to classify diabetes. It includes data analysis, missing value handling, model comparison, and hyperparameter optimization.

## Contents
- Data Analysis and Visualization
- Missing Value Handling
- Feature Scaling
- Oversampling (ADASYN, SMOTE, RandomOverSampler, etc.)
- Model Comparison (Logistic Regression, Random Forest, XGBoost, LightGBM)
- Hyperparameter Optimization
- Interpretation of Results

## Dataset
The dataset used is the [Pima Indians Diabetes Database](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database), provided as `diabetes.csv`.

| Column Name                | Description                     |
|---------------------------|---------------------------------|
| Pregnancies                | Number of pregnancies           |
| Glucose                    | Glucose level                   |
| BloodPressure              | Blood pressure                  |
| SkinThickness              | Skin thickness                  |
| Insulin                    | Insulin level                   |
| BMI                        | Body mass index                 |
| DiabetesPedigreeFunction   | Pedigree function               |
| Age                        | Age                             |
| Outcome                    | Diabetes (1) / Healthy (0)      |

## Installation

1. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn xgboost lightgbm
   ```
2. Place the `diabetes.csv` file in the project folder.
3. Run the Python script:
   ```bash
   python diabetes_classification_optimized.py
   ```

## Usage
- The code reads the dataset, handles missing values, applies oversampling, and performs classification with various models.
- Results and important features are printed and visualized.

## Modeling Steps
1. **Data Loading and Cleaning**: Analyze and fill missing/zero values.
2. **Data Splitting**: Split into training and test sets.
3. **Scaling**: Standardize features.
4. **Oversampling**: Solve class imbalance with ADASYN or another method.
5. **Model Training and Comparison**: Train and compare different algorithms.
6. **Hyperparameter Optimization**: Find best model parameters with GridSearchCV.
7. **Visualization**: Plot ROC curve and feature importances.

## Notes
- You can easily switch between ADASYN, SMOTE, or RandomOverSampler in the code.
- Results may vary depending on class imbalance and model selection.
