# 📸 Yapay Zeka Destekli Görüntü Sınıflandırıcı

Bu proje, PEAKUP Bulut Bilişim ve Yapay Zeka Teknolojileri dersi kapsamında geliştirilmiş, **kullanıcı dostu arayüz** üzerinden çalışan bir **görüntü sınıflandırma uygulamasıdır**. Proje, makine öğrenimi yöntemleriyle eğitilen bir modelin, kullanıcıdan alınan görselleri otomatik olarak sınıflandırmasını sağlar.

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

- Eğitim Doğruluğu (Training Accuracy): `%{{eğitim doğruluğu}}`
- Doğrulama Doğruluğu (Validation Accuracy): `%{{doğrulama doğruluğu}}`
> Not: Bu değerleri kod çıktısına göre manuel ekleyebilirsin.

## 🖼️ Arayüz Özellikleri (Gradio)

- Görüntü yükleme butonu
- Görsel önizlemesi
- Tahmin etme butonu
- Tahmin edilen sınıfın ekranda gösterimi

## 🚀 Nasıl Kullanılır?

Colab üzerinden çalıştırmak için:

1. [Google Colab Notebook'unu Aç](#)
2. Gerekli kütüphaneleri yükle
3. Modeli eğit veya eğitimli modeli yükle
4. `gr.Interface` bloğunu çalıştırarak arayüzü başlat

## 🧩 Proje Dosya Yapısı

- `goruntu.siniflandirma.ipynb`: Tüm eğitim, test ve arayüz kodlarını içeren Jupyter Notebook.
- `model.h5`: Eğitilen modelin kaydedilmiş hali (eğer ayrı sunuluyorsa).
- `README.md`: Proje dokümantasyonu.
- `demo.png`: Arayüz ekran görüntüsü (gerekiyorsa).
- `demo.mp4`: Uygulamanın kullanım videosu (isteğe bağlı).

## ✅ Fonksiyonel Özellikler

- ✅ Görsel yükleme
- ✅ Görsel ön işleme (yeniden boyutlandırma, normalize etme)
- ✅ Görsel sınıflandırma
- ✅ Arayüzde tahmin sonuçlarını gösterme

## 📌 Gereksinimler

Google Colab ortamında çalıştığı için ek yükleme gerekmez. Ancak yerel çalıştırma için:

```bash
pip install tensorflow gradio numpy matplotlib
