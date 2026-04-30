# 🧠 Brain Tumor Detection & Classification System

Bu proje, Manyetik Rezonans Görüntüleme (MRI) verilerini kullanarak beyin tümörlerinin otomatik ve doğru bir şekilde analiz edilmesini sağlayan bir Derin Öğrenme (Deep Learning) sistemidir. Atatürk Üniversitesi Yazılım Mühendisliği bölümü "Örüntü Tanıma" dersi kapsamında geliştirilmiştir.

## 🎯 Projenin Amacı ve Aşamaları
1. **Tespit (Detection):** Bireyde beyin tümörü bulunup bulunmadığının ikili (binary) olarak tespiti.
2. **Sınıflandırma (Classification):** Tümör tespit edilirse türünün belirlenmesi (Glioma, Meningioma, Pituitary veya Sağlıklı).

## 📊 Veri Seti
Projeyi eğitmek için Kaggle üzerinde bulunan [Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset) kullanılmıştır. 
*(Not: Veri seti boyutu büyük olduğu için bu repoya eklenmemiştir, ilgili linkten indirilebilir.)*

## ⚙️ Kullanılan Yöntemler ve Mimari
Projeyi gerçekleştirirken aşağıdaki adımlar izlenmiştir:
* **Veri Ön İşleme:** Görüntüler 224x224 boyutuna getirilmiş, normalizasyon uygulanmış ve ezberlemeyi (overfitting) önlemek için veri artırma (Data Augmentation) teknikleri kullanılmıştır.
* **Özellik Çıkarımı (Feature Extraction):** Profesyonel özellik çıkarımı için önceden eğitilmiş **VGG16** mimarisi kullanılmıştır (Transfer Learning).
* **Derin Öğrenme (CNN):** VGG16 modelinin sonuna GlobalAveragePooling2D, Dense (256 nöron) ve Dropout katmanları eklenerek kendi çok sınıflı sinir ağımız kurulmuştur.

## 📈 Başarı Oranı (Değerlendirme Metrikleri)
Model, daha önce hiç görmediği test verileri üzerinde yaklaşık **%80 doğruluk (accuracy)** oranıyla çalışmaktadır. Sistem hem sağlıklı beyinleri yüksek güvenle ayırt edebilmekte hem de tümör türlerini başarıyla sınıflandırabilmektedir.

# 🧠 Brain Tumor Detection & Classification System

Bu proje, Manyetik Rezonans Görüntüleme (MRI) verilerini kullanarak beyin tümörlerinin otomatik ve doğru bir şekilde analiz edilmesini sağlayan bir Derin Öğrenme (Deep Learning) sistemidir. Atatürk Üniversitesi Yazılım Mühendisliği bölümü "Örüntü Tanıma" dersi kapsamında geliştirilmiştir.

## 🎯 Projenin Amacı ve Aşamaları
1. **Tespit (Detection):** Bireyde beyin tümörü bulunup bulunmadığının ikili (binary) olarak tespiti.
2. **Sınıflandırma (Classification):** Tümör tespit edilirse türünün belirlenmesi (Glioma, Meningioma, Pituitary veya Sağlıklı).

## 📊 Veri Seti
Projeyi eğitmek için Kaggle üzerinde bulunan [Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset) kullanılmıştır. 
*(Not: Veri seti boyutu büyük olduğu için bu repoya eklenmemiştir, ilgili linkten indirilebilir.)*

## ⚙️ Kullanılan Yöntemler ve Mimari
Projeyi gerçekleştirirken aşağıdaki adımlar izlenmiştir:
* **Veri Ön İşleme:** Görüntüler 224x224 boyutuna getirilmiş, normalizasyon uygulanmış ve ezberlemeyi (overfitting) önlemek için veri artırma (Data Augmentation) teknikleri kullanılmıştır.
* **Özellik Çıkarımı (Feature Extraction):** Profesyonel özellik çıkarımı için önceden eğitilmiş **VGG16** mimarisi kullanılmıştır (Transfer Learning).
* **Derin Öğrenme (CNN):** VGG16 modelinin sonuna GlobalAveragePooling2D, Dense (256 nöron) ve Dropout katmanları eklenerek kendi çok sınıflı sinir ağımız kurulmuştur.

## 📈 Başarı Oranı (Değerlendirme Metrikleri)
Model, daha önce hiç görmediği test verileri üzerinde yaklaşık **%80 doğruluk (accuracy)** oranıyla çalışmaktadır. Sistem hem sağlıklı beyinleri yüksek güvenle ayırt edebilmekte hem de tümör türlerini başarıyla sınıflandırabilmektedir.

## 🚀 Nasıl Kullanılır?
1. Repoyu bilgisayarınıza klonlayın veya indirin.
2. Gerekli kütüphaneleri yükleyin (`tensorflow`, `numpy`, `matplotlib`).
3. Eğitilmiş model dosyasını (.h5) boyutundan dolayı **[BURAYA TIKLAYARAK GOOGLE DRIVE ÜZERİNDEN İNDİREBİLİRSİNİZ](https://drive.google.com/file/d/1yrXZURdDF70q-S5VehGpK-6cMecbAGDf/view?usp=drive_link)** ve kod dosyasıyla aynı klasöre yerleştirin.
4. Python dosyasını çalıştırarak herhangi bir MRI görüntüsünü sisteme verip anında teşhis sonucunu alabilirsiniz.
