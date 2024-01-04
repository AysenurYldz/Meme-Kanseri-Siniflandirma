# Meme Kanseri Sınıflandırma
Meme kanseri kadınlar arasında en yaygın meydana gelen kanser türüdür. 2020 yılında 2,3 milyona yakın yeni meme kanseri vakası bildirilmiştir. Bu tanı konulan her sekiz kanserden birinin meme kanseri olduğu anlamına gelir. 2020 yılı verilerine göre meme kanseri 685.000 ölüme neden olarak kanserler arasında en çok ölüme neden olan 5. Kanser olmuştur. Doğru ve erken teşhis kanser hastalıklarında hayatta kalma oranını arttırmada önemli rol oynamaktadır. Klinik pratikte mamografi, meme kanseri teşhisinde yaygın olarak kullan bir araçtır. Radyologların günlük olarak çok sayıda mamografi inceleyip bunları sınıflandırmaları zorlu bir süreçtir. Bu nedenle doktorlara kararlarında yardımcı olmak ve desteklemek için ikinci bir görüş sağlayabilen bilgisayar destekli teşhisin gerekli olduğu görülmektedir.
# CNN Modeli
## Görüntü Sınıflandırma Amaçlı Hazırlık:
Evrişimli katmanlar, farklı özellikleri tespit etmek ve yüksek seviyeli özelliklere dönüştürmek için kullanıldı.
## Katmanların İşlevleri:
MaxPooling katmanları, resmin boyutunu küçültürken önemli özellikleri korumaktadır.
ReLu aktivasyon fonksiyonu, ağın hızlı öğrenmesine ve daha az hesaplama gücü kullanmasına imkan sağlamaktadır.
## Mimari Yeniden Yapılandırma ve Sonuçlar:
Yapısal değişiklikler yapılarak istenilen sonuçlar elde edilmiştir.
# Efficient Net-B7 Modeli
## EfficientNet ve Ölçekleme Yaklaşımı:
Eşit ölçeklendirme katsayılarıyla derinlik, genişlik ve çözünürlük boyutlarını artıran bir evrişimli sinir ağı mimarisi.
## Transfer Öğrenimi ve Kullanılan Model:
EfficientNetB7 modeli, ImageNet veri kümesinde önceden eğitilmiş ve sınıflandırma görevinde kullanılmıştır.
## Modelin Yapısı ve Katmanları:
Model, EfficientNetB7'nin tüm katmanlarını içerir.
Flatten, BatchNormalization, Dense ve Dropout katmanları, sınıflandırma görevi için çıktıları şekillendirir.
## Geri Bildirimler ve Optimizasyon Yöntemleri:
Eğitimde EarlyStopping aşırı uyumu önlerken, ReduceLROnPlateau öğrenme oranını otomatik olarak düzenler.
# Resnet 50
## ResNet50 Modelinin Özellikleri:
50 katmanlı ResNet mimarisine dayanan bir CNN modelidir.
ImageNet veri seti üzerinde eğitilmiş ağırlıkları kullanarak önceden eğitilir.
## Yapılan Değişiklikler:
Son tam bağlı katman kaldırılıp yerine Flatten katmanı eklenir.
Sırasıyla Dropout, Flatten, BatchNormalization ve Dense katmanları kullanılır.
## Katmanların İşlevleri:
Dropout aşırı öğrenmeyi engeller.
Flatten, çıkışı düzleştirir ve ardından Dense katmanlara geçişi sağlar.
BatchNormalization hızlı öğrenmeyi destekler.
Dense katmanları çıkış üretir; ilk üç katmanda 256 nöron ve ReLU aktivasyon fonksiyonu bulunur.
# VGG-19
## Kullanılan Mimari ve Teknikler
VGG19 Modeli, görüntü sınıflandırma için 19 katmanlı bir CNN modelidir.
Evrişimli sinir ağı (CNN) mimarisi kullanılarak geliştirilmiştir.
Vgg-19 tam bağlı katmanlar ve özellik çıkarma için kullanılır. 
## Kullanılan Yöntem ve İşlem Adımları:
Transfer öğrenme ile sınıflandırma modeline uyarlanır.
224x224 boyutlu 3 kanallı görüntülerle çalışır.
## Katmanlar ve Sonuç:
Katmanlar özellik haritalarına dönüşüm için kullanılır, ardından Dropout ve Batch Normalization eklenir. Tam bağlı katmanlar sınıflandırma çıktısını hazırlar, son katman sigmoid aktivasyonunu kullanarak sınıflandırma yapar.
## Eğitim Süreci ve Ağırlıklar:
"Imagenet" veri kümesinde önceden eğitilmiş ağırlıklar kullanılır.
Önceden eğitilmiş katmanlar eğitim sürecinde dondurulur.
