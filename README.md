# Akbank_Derinogrenme_Boostcamp
Bu proje, farklı balık türlerini görüntüleri üzerinden sınıflandırmak için derin öğrenme yöntemleri kullanmaktadır.
## Balık Sınıflandırma Projesi
Bu proje, farklı balık türlerini görüntüleri üzerinden sınıflandırmak için derin öğrenme yöntemleri kullanmaktadır. TensorFlow kütüphanesi ile inşa edilen model, çeşitli balık görüntüleri üzerinde eğitilmiş olup, görüntü işleme ve veri ön işleme teknikleri ile desteklenmiştir.

## Proje İçeriği
### 1. Kurulum
Projeyi çalıştırmadan önce, gerekli bağımlılıkların yüklenmesi gerekmektedir. Aşağıdaki adımları izleyerek ortamınızı hazırlayabilirsiniz:

Gereksinimler
tensorflow==2.16.1
numpy
pandas
opencv-python
matplotlib
seaborn
scikit-learn
h5py
keras
### 2. Veri Seti
Proje, balık türlerini içeren bir görüntü veri seti üzerinde çalışmaktadır. Veri seti, her bir balık türünü temsil eden çeşitli görüntülerden oluşmaktadır. Görüntüler, eğitim ve test seti olarak ikiye ayrılmıştır.
Eğitim Seti: Modelin öğrenmesi için kullanılan görüntüler.
Test Seti: Modelin doğruluğunu ölçmek için kullanılan görüntüler.

### 3. Veri Ön İşleme
Görüntü verileri, modelin eğitilmesi için çeşitli adımlardan geçirilmiştir:

Yeniden Boyutlandırma: Tüm görüntüler belirli bir boyuta (örneğin 224x224 piksel) yeniden boyutlandırılır.
Normalizasyon: Görüntülerin piksel değerleri 0 ile 1 arasında normalize edilir.
Augmentation: Eğitim sırasında modeli daha dayanıklı hale getirmek için veri artırma teknikleri (döndürme, kırpma, yatay-dikey çevirme) uygulanır.
### 4. Model
Projenin ana bileşeni olan model, bir derin öğrenme modelidir ve TensorFlow ile geliştirilmiştir. Aşağıdaki yapıya sahiptir:

Giriş Katmanı (Input Layer): 224x224x3 boyutunda bir görüntü alır.
Convolutional Katmanlar (Conv Layers): Görüntüdeki özellikleri öğrenir.
MaxPooling Katmanları: Özellik haritalarını küçültür.
Dense Katmanlar: Tam bağlantılı katmanlar modelin sınıflandırma yapmasını sağlar.
Dropout: Overfitting'i önlemek için bazı nöronlar eğitim sırasında rastgele kapatılır.
Softmax Çıkış Katmanı: Sonuçta balık türlerinin olasılıklarını hesaplar.
### 5. Eğitim (Training)
Model, veri seti üzerinde eğitim adımlarından geçirilir. Eğitim sırasında:

Kayıp Fonksiyonu (Loss Function): Kategorik çapraz entropi kullanılır.
Optimizasyon Algoritması (Optimizer): Adam optimizer kullanılır.
Değerlendirme Metrikleri (Metrics): Modelin doğruluğunu ölçmek için doğruluk (accuracy) metriği kullanılır.

### 6. Değerlendirme ve Sonuçlar
Eğitim tamamlandıktan sonra model test verileri üzerinde değerlendirilir. Aşağıdaki metrikler hesaplanır:

Doğruluk (Accuracy): Modelin sınıflandırma doğruluğunu ölçer.
Kayıp (Loss): Eğitim ve doğrulama kayıpları incelenir.
Sonuçları görselleştirmek için matplotlib kullanılarak grafikler oluşturulur
### 7. Model Kaydetme
Model eğitildikten sonra .h5 formatında kaydedilir ve ileride tekrar kullanılabilir.

### 9. GPU Kullanımı
Model, GPU'yu destekleyecek şekilde yapılandırılmıştır. Eğer bir GPU kullanıyorsanız, TensorFlow otomatik olarak GPU'yu kullanacaktır. Aksi takdirde CPU ile çalışacaktır.
### Lisans
Bu proje MIT Lisansı altında lisanslanmıştır. 

## Kaggle link
https://www.kaggle.com/code/feyzaavc/fish-classification

