# 🫀 CardioGuard: Kardiyovasküler Hastalık Tahmin ve Analiz Sistemi

Bu proje, yaklaşık 70.000 klinik kaydı analiz ederek bir bireyin kardiyovasküler hastalık riskini tahmin etmeyi amaçlayan kapsamlı bir veri bilimi çalışmasıdır. Sadece tahmin odaklı değil, aynı zamanda verinin istatistiksel doğasını anlamaya yönelik derinlemesine analizler içerir.

## 🚀 Proje Mimarisi
Proje, her biri belirli bir amaca hizmet eden 6 aşamalı bir "pipeline" yapısı üzerine kurulmuştur:

1.  **Veri Ön İşleme:** Gün bazlı yaş verisinin yıla çevrilmesi, BMI (Vücut Kitle Endeksi) hesaplama ve aykırı değerlerin (tansiyon verileri vb.) temizlenmesi.
2.  **Keşifsel Veri Analizi (EDA):** Özelliklerin hedef değişken (`cardio`) üzerindeki etkisinin görselleştirilmesi ve korelasyon analizi.
3.  **İstatistiksel Analiz:** Shapiro-Wilk, T-Test, Ki-Kare ve ANOVA testleri ile özelliklerin anlamlılığının bilimsel yöntemlerle kanıtlanması.
4.  **Model Eğitimi:** Logistic Regression, Random Forest, XGBoost, SVM, KNN ve Naive Bayes algoritmalarının karşılaştırılması.
5.  **Hiperparametre Optimizasyonu:** En iyi performans gösteren modelin (Gradient Boosting) GridSearch ve RandomSearch yöntemleriyle optimize edilmesi.
6.  **Sonuç ve Raporlama:** Karar matrisleri, ROC-AUC eğrileri ve hata analizi (False Positives/Negatives) ile model başarısının değerlendirilmesi.

## 📊 Öne Çıkan Bulgular
- **En Önemli Değişkenler:** Kan basıncı (ap_hi, ap_lo), yaş ve kolesterol seviyesinin hastalık riskiyle en güçlü korelasyona sahip olduğu saptanmıştır.
- **Model Başarısı:** Gradient Boosting modeli, hiperparametre optimizasyonu sonrası en yüksek F1-Score ve Accuracy değerlerine ulaşmıştır.
- **İstatistik:** Tansiyon değerlerinin hastalık üzerindeki etkisi p < 0.05 düzeyinde istatistiksel olarak anlamlı bulunmuştur.

## 🛠️ Kullanılan Teknolojiler
- **Programlama:** Python
- **Veri Analizi & Görselleştirme:** Pandas, NumPy, Matplotlib, Seaborn
- **İstatistik:** SciPy (Stats)
- **Makine Öğrenmesi:** Scikit-learn, XGBoost
- **Model Saklama:** Pickle
