##  🔹 🔸 BRAIN TUMOR DIAGNOSIS WITH ARTIFICIAL INTELLIGENCE 🔸 🔹

Beyin tümörleri, çocuklarda ve yetişkinlerde görülen agresif hastalıklar arasında kabul edilir. Merkezi Sinir Sistemi (MSS) tümörlerinin büyük çoğunluğunu oluştururlar ve tüm MSS tümörlerinin %85-90'ını teşkil ederler. Her yıl yaklaşık 11,700 kişiye beyin tümörü teşhisi konulmaktadır. Bu tür tümörlerle mücadele eden bireylerin 5 yıllık sağkalım oranı erkeklerde %34, kadınlarda ise %36 olarak belirlenmiştir. Hastaların sağkalım sürelerini artırmak için doğru tanı ve tedavi planlamaları kritik öneme sahiptir. Beyin tümörlerinin tespitinde en yaygın kullanılan yöntem Manyetik Rezonans Görüntüleme (MR) teknolojisidir. MR taramalarıyla elde edilen büyük miktarda görüntü verisi, uzman radyologlar tarafından analiz edilir. Beyin tümörlerinin karmaşıklığı göz önüne alındığında, manuel muayene yöntemleri hatalara açık olabilir.

Literatürde yapılan çalışmalar, Makine Öğrenimi (ML) ve Yapay Zeka (AI) tekniklerinin otomatik sınıflandırma için kullanılmasının, manuel sınıflandırmadan daha yüksek doğruluk sağladığını ortaya koymuştur. Bu nedenle, Evrişimli Sinir Ağları (CNN), Yapay Sinir Ağları (ANN) ve Makine Öğrenimi gibi Algoritmalar kullanılarak geliştirilen ve beyin tümörlerinin tespit ve sınıflandırılmasında kullanılan sistemler, tıp uzmanlarına büyük destek sağlayacaktır.

---

## VERİ SETİ
Toplamda 3060 adet beyin MRI görüntüsünden oluşan veri seti, Kaggle platformunda bulunan "[Br35H :: Brain Tumor Detection 2020](https://www.kaggle.com/datasets/ahmedhamada0/brain-tumor-detection?select=no)" adlı bir veri setidir. Görüntüler, "yes" (tumor), "no" (normal) ve "pred" olmak üzere üç farklı klasör altında düzenlenmiştir. Tumor sınıfı 1500 görüntü içerirken, normal sınıfı da 1500 görüntüden oluşmaktadır. "pred" klasöründe ise etiketsiz 60 görüntü bulunmaktadır. Bu çalışma kapsamında sadece "yes" ve "no" klasörlerindeki toplam 3000 görüntü kullanılmıştır.

---

Bu çalışmada, makine öğrenmesi yöntemlerinden altı farklı sınıflandırıcı, ayrıca yapay sinir ağı (ANN) ve evrişimli sinir ağı (CNN) kullanılarak bir dizi model eğitimi gerçekleştirilmiştir. 

Eğitilen modeller aşağıda listelenmiştir. 

🔰 **Makine öğrenmesi algoritmaları:**

    💠K-Nearest Neighbors
  
    💠Decision Tree
  
    💠Random Forest
  
    💠Support Vector Machine
  
    💠Gradient Boosting
  
    💠Logistic Regression
  
🔰 **Yapay Sinir Ağları(ANN)**

🔰 **Evrişimli Sinir Ağları (CNN)**

    💠Önerilen CNN Modeli
  
    💠ResNet50 Modeli


Her bir model için eğitim sürecinde k=5 kat çapraz doğrulama yöntemi uygulanmıştır.

Her eğitim sürecinin sonunda, modelin sınıflandırma performansını değerlendirmek için doğruluk (accuracy), hassasiyet (precision), duyarlılık (recall), F1 skoru, sınıflandırma raporu, karışıklık matrisi ve roc eğrisi gibi ölçütler elde edilmiştir. Elde edilen bu değerlendirme metrikleri, modellerin performansını karşılaştırmak ve en uygun modeli seçmek için kullanılmıştır.

---

## BULGULAR 📋


| Deep Learning Architectures | Training Accuracy | Validation Accuracy | Testing Accuracy | Precision | Recall | F1-score |
|----------------------------|-------------------|---------------------|------------------|-----------|--------|----------|
| K-Nearest Neighbors         | -                 | 86.99               | 90.33            | 91.68     | 90.333 | 90.25    |
| Decision Tree               | -                 | 84                  | 83               | 83.03     | 83     | 82.99    |
| Random Forest               | -                 | 95.14               | 94.33            | 93.38     | 94.33  | 94.33    |
| Support Vector Machine      | -                 | 94.74               | 94               | 94.03     | 94     | 93.99    |
| Gradient Boosting           | -                 | 94.37               | 93.66            | 93.66     | 93.66  | 93.66    |
| Logistic Regression         | -                 | 96.59               | 98               | 98        | 98     | 97.99    |
| Artificial Neural Network   | 85.75             | 81.70               | 81.66            | 81.66     | 81.66  | 81.6     |
| Proposed Model (CNN)        | 98.26             | 95.03               | 95.39            | 95.39     | 95.39  | 95.2     |
| ResNet50                    | 97.27             | 90.99               | 91.06            | 91.06     | 91.06  | 91       |



---
Projeye ait model dosyalarını (pkl ve hdf5 formatlarında) aşağıdaki bağlantıyı kullanarak indirebilirsiniz: [Google Drive Bağlantısı]([https://www.kaggle.com/datasets/ahmedhamada0/brain-tumor-detection?select=no](https://drive.google.com/drive/folders/1K2msh-PcmW79-1VLyRUarLUIpLdKa1k9?usp=drive_link))

