# 📸 Yapay Zeka Destekli Görüntü Sınıflandırıcı

Bu proje, MTH Bulut Bilişim ve Yapay Zeka Teknolojileri dersi kapsamında geliştirilmiş, **kullanıcı dostu arayüz** üzerinden çalışan bir **görüntü sınıflandırma uygulamasıdır**. Proje, makine öğrenimi yöntemleriyle eğitilen bir modelin, kullanıcıdan alınan görselleri otomatik olarak sınıflandırmasını sağlar.

## 🎯 Proje Hedefi

Makine öğrenimi algoritmaları kullanarak görselleri sınıflandıran bir model geliştirmek ve bu modeli kullanıcıların etkileşimde bulunabileceği basit bir arayüzle sunmak.

## ⚙️ Kullanılan Teknolojiler

- Python
- TensorFlow
- Keras
- Google Colab
- Gradio (Web arayüzü için)

## 📁 Kullanılan Veri Seti

[CIFAR-10 Dataset](https://www.cs.toronto.edu/~kriz/cifar.html)  
Toplam 10 sınıf (uçak, kuş, kedi, köpek vb.) içeren, 32x32 boyutunda küçük görsellerden oluşan etiketli bir veri setidir.

## 🧠 Model Özeti

- **Model Türü:** Convolutional Neural Network (CNN)
- **Katmanlar:** Conv2D, MaxPooling2D, Dropout, Flatten, Dense
- **Aktivasyon Fonksiyonları:** ReLU ve Softmax
- **Optimizasyon:** Adam Optimizer
- **Kayıp Fonksiyonu:** Categorical Crossentropy
- **Değerlendirme Metrikleri:** Accuracy

## 🧪 Eğitim Sonuçları

- Eğitim Doğruluğu (Training Accuracy): `0.8190`
- Doğrulama Doğruluğu (Validation Accuracy): `0.8350`

## 📊 Model Performans Değerlendirmesi
Model, CIFAR-10 veri seti üzerinde eğitilmiş ve test edilmiştir. Aşağıda sınıf bazında precision, recall ve f1-score değerleri ile birlikte genel başarı metrikleri yer almaktadır:
| Sınıf      | Precision | Recall | F1-Score | Support |
| ---------- | --------- | ------ | -------- | ------- |
| Airplane   | 0.86      | 0.85   | 0.85     | 1000    |
| Automobile | 0.93      | 0.94   | 0.94     | 1000    |
| Bird       | 0.84      | 0.73   | 0.78     | 1000    |
| Cat        | 0.82      | 0.57   | 0.67     | 1000    |
| Deer       | 0.79      | 0.82   | 0.81     | 1000    |
| Dog        | 0.87      | 0.67   | 0.76     | 1000    |
| Frog       | 0.64      | 0.97   | 0.77     | 1000    |
| Horse      | 0.87      | 0.88   | 0.87     | 1000    |
| Ship       | 0.90      | 0.93   | 0.91     | 1000    |
| Truck      | 0.86      | 0.94   | 0.90     | 1000    |

Genel Değerlendirme:

Accuracy: 0.83

Macro Avg: Precision = 0.84, Recall = 0.83, F1-score = 0.83

Weighted Avg: Precision = 0.84, Recall = 0.83, F1-score = 0.83

Bu metrikler modelin genel olarak iyi bir performans sergilediğini göstermektedir. Özellikle "automobile", "ship" ve "truck" sınıflarında oldukça yüksek başarı gözlemlenmiştir. "Cat" ve "frog" sınıflarında bazı zorluklar yaşanmıştır, bu sınıflar için ek veri ile model geliştirilebilir.

## 🖼️ Arayüz Özellikleri (Gradio)

- Görüntü yükleme butonu
- Görsel önizlemesi
- Tahmin etme butonu
- Tahmin edilen sınıfın ekranda gösterimi

## 🚀 Nasıl Kullanılır?

Colab üzerinden çalıştırmak için:

1. [Google Colab Notebook'unu Aç](https://colab.research.google.com/github/busraksakalli7/Yapay-Zeka-Goruntu-Siniflandirma/blob/main/goruntu.siniflandirma.ipynb)
2. Gerekli kütüphaneleri yükle
3. Modeli eğit veya eğitimli modeli yükle
4. `gr.Interface` bloğunu çalıştırarak arayüzü başlat

## 🧩 Proje Dosya Yapısı

- `goruntu.siniflandirma.ipynb`: Tüm eğitim, test ve arayüz kodlarını içeren dosya.
- `README.md`: Proje dokümantasyonu.
- `demo.png`: Arayüz ekran görüntüsü.
- `demo.mp4`: Uygulamanın kullanım videosu.

## ✅ Fonksiyonel Özellikler

- ✅ Görsel yükleme
- ✅ Görsel ön işleme (yeniden boyutlandırma, normalize etme)
- ✅ Görsel sınıflandırma
- ✅ Arayüzde tahmin sonuçlarını gösterme

## 📌 Gereksinimler

Google Colab ortamında çalıştığı için ek yükleme gerekmez. Ancak yerel çalıştırma için:

```bash
pip install tensorflow gradio numpy matplotlib
