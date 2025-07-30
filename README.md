# 📊 Telco Customer Churn Prediction
- [rapor.docx](https://github.com/user-attachments/files/21515669/rapor.docx)
Bu proje, bir telekomünikasyon şirketine ait müşteri verileri üzerinden müşteri kaybını (churn) tahmin etmek amacıyla veri analizi ve makine öğrenmesi modellerini kapsamaktadır.

---

## 🔍 Proje Amacı

Müşterilerin abonelik iptali (churn) davranışlarını öngörerek, işletmenin proaktif önlemler almasına katkı sağlamak. Bu sayede:

- Müşteri memnuniyetini artırmak
- Gelir kayıplarını azaltmak
- Sadakat programlarını kişiselleştirmek
- Hedef kitle odaklı kampanyalar geliştirmek

---

## 📂 Kullanılan Veri Seti

- **Kaynak:** IBM Sample Dataset – Telco Customer Churn
- **Toplam Gözlem:** 7043 müşteri
- **Hedef Değişken:** Churn (Yes / No)

---

## ⚙️ Kullanılan Kütüphaneler ve Teknolojiler

**Veri İşleme ve Görselleştirme:**
- pandas
- numpy
- matplotlib
- seaborn
- plotly
- missingno

**Ön İşleme:**
- LabelEncoder
- StandardScaler
- SMOTE

**Makine Öğrenmesi Algoritmaları:**
- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier
- AdaBoost Classifier
- Gradient Boosting Classifier
- Stacking Classifier
- Voting Classifier

**Değerlendirme Metrikleri:**
- accuracy_score
- precision_score
- recall_score
- f1_score
- roc_auc_score
- confusion_matrix
- classification_report

---

## 🔧 Uygulanan Adımlar

### 1️⃣ Veri Ön İşleme

- Eksik veriler dolduruldu (TotalCharges sütunu medyan ile).
- Aykırı değerler incelendi.
- Kategorik değişkenler one-hot encoding ile dönüştürüldü.
- Sayısal veriler StandardScaler ile normalize edildi.
- SMOTE uygulanarak dengesiz sınıf problemi giderildi.

### 2️⃣ Öz Nitelik Mühendisliği

- **AvgMonthlyCharge:** Ortalama aylık ödeme hesaplandı.
- **TenureGroup:** Abonelik süresi segmentlere ayrıldı.
- **TotalServices:** Kullanılan toplam hizmet sayısı hesaplandı.

### 3️⃣ Keşifsel Veri Analizi

- Churn oranı: %26.5
- Churn oranını etkileyen temel faktörler: Tenure, MonthlyCharges, TotalCharges, Contract Type, Payment Method
- Fiber Optic ve Electronic Check kullanıcılarında churn riski yüksek bulundu.
- Online Security ve TechSupport hizmetleri churn riskini azaltıcı etki göstermektedir.

### 4️⃣ Modelleme

| Model | Accuracy | Recall | ROC-AUC |
|---|---|---|---|
| Logistic Regression | 76% | 72% | 82.9% |
| Random Forest | 77% | 59% | 82.1% |
| Stacking | 74.17% | 74.33% | 83.15% |

### 5️⃣ Sonuç ve Öneriler

- Kısa sözleşmeli ve yüksek ödeme yapan müşteriler churn riski taşımaktadır.
- Online Security, TechSupport ve Device Protection hizmetleri müşteri bağlılığını artırmaktadır.
- Electronic Check ödemeleri riskli segmenttir.
- Uzun vadeli kontratlar churn riskini azaltmaktadır.
- Model çıktıları pazarlama ve müşteri ilişkileri yönetimi için erken uyarı sistemlerine entegre edilebilir.

---

## 🚀 İşletmeye Yönelik Öneriler

- **Erken Uyarı Sistemi:** Riskli müşteriler için kişiselleştirilmiş kampanyalar ve hizmet iyileştirmeleri geliştirilebilir.
- **Kontrat Uzatma:** Kısa vadeli sözleşmeleri uzun vadeli taahhütlere çevirmek churn oranını düşürecektir.
- **Hizmet Çeşitliliği:** OnlineSecurity, TechSupport ve DeviceProtection gibi hizmetler çapraz satış kampanyalarıyla artırılabilir.
- **Ödeme Alternatifleri:** Electronic Check kullanan müşteriler farklı ödeme yöntemlerine yönlendirilebilir.
- **Fiber Optic Geliştirmeleri:** Fiber kullanıcılarının kalite beklentileri daha iyi karşılanabilir.

---

## 📌 Notlar

- Proje Python dili ve Google Colab ortamında geliştirilmiştir.
- Tam makine öğrenmesi pipeline'ı uygulanmıştır.

---

## 👩‍💻 Proje Sahibi

**İrem Nur KAYA**  
Veri Bilimi ve Makine Öğrenmesi Çalışması  
Teslim Tarihi: 16.06.2025
