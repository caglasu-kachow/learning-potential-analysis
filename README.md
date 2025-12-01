# Learning Potential & Distress Analysis — Final Report
Psychological Latent Structure + Predictive Modeling (PCA + Regression)  
Dataset: merge_all_factor_427.csv (427 participants, 98 variables)

## 🌍 Languages  
- 🇬🇧 English version below  
- 🇹🇷 Türkçe versiyon aşağıda  

---

# 🇬🇧 English Version

## 1. Project Overview
This project aims to uncover the underlying psychological structures behind multiple highly correlated mental health variables, and to model how a latent distress factor influences somatic symptom severity.
The workflow started with exploratory analysis and PCA experimentation, continued with measurement modeling and predictive regression analysis and ultimately evolved into a clean latent-variable-based approach to solve the multicollinearity problem.

## 2. Research Goal 
- Construct a latent learning potential score using PCA.
- Understand shared variance among stress, depression, cognitive-affective symptoms.
- Extract a latent distress factor (unidimensional) explaining most of the variance (EVR = 0.867).
- Model somatic symptoms using this latent factor (Linear Regression → R² = 0.71).
- Replace unstable multi-variable regression (due to multicollinearity) with a stable latent-variable model.

## 3. Dataset Description 
- Source: Nature 2023 psychological dataset (OSF replication)
- 427 participants
- ~98 variables
- Includes: stress, control, self-efficacy, depression, somatic symptoms, cognitive-affective symptoms
- Preprocessed dataset saved as: "merge_all_factor_427.csv", "final_learning_potential_dataset.csv"

## 4. Analysis Pipeline (Notebooks) 

| Notebook | Purpose |
|---------|---------|
| **01_data_exploration.ipynb** | Initial dataset exploration & variable inspection |
| **02_testing_pca.ipynb** | PCA experiments, sign-flipping, orientation stabilizing |
| **03_measurement_modeling.ipynb** | Reliability tests & regression-based construct validation |
| **04_baseline_prediction_modeling.ipynb** | Simple & multiple regression baselines |
| **05_prediction_modeling.ipynb** | Feature selection attempts, correlation checks |
| **06_full_predictive_model.ipynb** | OLS + VIF analysis → multicollinearity discovered |
| **07_latent_distress_modeling.ipynb** | PCA latent distress extraction + regression |
| **08_final_report.ipynb** | Final model, visualization, scientific summary |



## 5. Key Findings 
- Latent Distress Factor
  + PCA produced a strong single-factor structure     
  + Explained Variance Ratio (EVR) = 0.867
  + Loadings:
    stress (0.537)
    depression (0.597)
    cognitive-affect (0.595)
- Regression Result
  Somatic symptoms = β * Latent Distress
  + β = 0.569
  + Intercept ≈ 0
  + R² = 0.71

## 6. Repository Structure
learning-potential-analysis/
│
├── 01_data_exploration.ipynb
├── 02_testing_pca.ipynb
├── 03_measurement_modeling.ipynb
├── 04_baseline_prediction_modeling.ipynb
├── 05_prediction_modeling.ipynb
├── 06_full_predictive_model.ipynb
├── 07_latent_distress_modeling.ipynb
├── 08_final_report.ipynb
│
├── merge_all_factor_427.csv
├── final_learning_potential_dataset.csv
└── README.md

## 7. How to Run
Clone the repository and open the notebook:

jupyter notebook
Open notebooks in numerical order.

## 8. Final Notes 
This project demonstrates the limitations of classical regression under multicollinearity and shows how latent variable modeling can produce more stable, interpretable results in psychological datasets.


---

# 🇹🇷 Türkçe Versiyon

## 1. Proje Özeti 
Bu proje, yüksek korelasyonlu psikolojik değişkenlerin altında yatan gizli yapıları ortaya çıkarmayı ve elde edilen latent distress faktörünün somatik belirti şiddeti üzerindeki etkisini modellemeyi amaçlar.
Çalışma veri keşfinden başlayıp PCA denemeleri, ölçme modeli testleri ve regresyon analizlerinden geçerek en sonunda multikolinerlik sorununu çözen latent değişken temelli bir modele dönüşmüştür.


## 2. Araştırma Amacı 
- PCA ile bir learning potential skoru oluşturmak.
- Stres, depresyon ve bilişsel-duygusal belirtiler arasındaki ortak varyansı anlamak.
- Yüksek varyans açıklayan tek boyutlu bir latent distress faktörü elde etmek (EVR = 0.867).
- Somatik belirtileri bu latent faktörle modellemek (Doğrusal Regresyon → R² = 0.71).
- Multikolinerlik nedeniyle kararsız olan çoklu regresyon modelleri yerine daha stabil latent değişken yaklaşımı kullanmak.

## 3. Veri Seti Açıklaması 
- Kaynak: Nature 2023 psikoloji veri seti (OSF)
- 427 katılımcı
- ~98 değişken
- İçerik: stres, kontrol, öz-yeterlik, depresyon, somatik belirtiler, bilişsel-duygusal belirtiler
- İşlenmiş veri setleri: "merge_all_factor_427.csv", "final_learning_potential_dataset.csv"


## 4. Analiz Aşamaları 
| Notebook | Amaç |
|---------|---------|
| **01_data_exploration.ipynb** | Initial dataset exploration & variable inspection |
| **02_testing_pca.ipynb** | PCA experiments, sign-flipping, orientation stabilizing |
| **03_measurement_modeling.ipynb** | Reliability tests & regression-based construct validation |
| **04_baseline_prediction_modeling.ipynb** | Simple & multiple regression baselines |
| **05_prediction_modeling.ipynb** | Feature selection attempts, correlation checks |
| **06_full_predictive_model.ipynb** | OLS + VIF analysis → multicollinearity discovered |
| **07_latent_distress_modeling.ipynb** | PCA latent distress extraction + regression |
| **08_final_report.ipynb** | Final model, visualization, scientific summary |


## 5. Temel Bulgular 
- Latent Distress Faktörü
  + PCA tek boyutlu güçlü bir yapı ortaya çıkardı
  + Explained Variance Ratio (EVR) = 0.867
  + Yükler:
    stress (0.537)
    depression (0.597)
    cognitive-affect (0.595)
- Regresyon Sonucu
  Somatik belirtiler = β * Latent Distress
  + β = 0.569
  + Sabit ≈ 0
  + R² = 0.71


## 6. Depo Yapısı
 learning-potential-analysis/
│
├── 01_data_exploration.ipynb
├── 02_testing_pca.ipynb
├── 03_measurement_modeling.ipynb
├── 04_baseline_prediction_modeling.ipynb
├── 05_prediction_modeling.ipynb
├── 06_full_predictive_model.ipynb
├── 07_latent_distress_modeling.ipynb
├── 08_final_report.ipynb
│
├── merge_all_factor_427.csv
├── final_learning_potential_dataset.csv
└── README.md


## 7. Nasıl Çalıştırılır?
Repoyu klonlayın ve notebook'ları çalıştırın.

jupyter notebook
Notebooklar numara sırasıyla çalıştırılmalıdır.

## 8. Son Notlar
Bu proje, yüksek multikolinerlik altında klasik regresyonun sınırlamalarını ve latent değişken temelli yaklaşımların psikolojik veri analizinde nasıl daha stabil ve yorumlanabilir sonuçlar ürettiğini göstermektedir.

