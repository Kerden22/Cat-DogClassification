# Kedi & Köpek Görüntü Sınıflandırma

Bu projede, PyTorch kullanılarak **Kedi** ve **Köpek** görüntülerinin sınıflandırılması için iki farklı model (Yapay Sinir Ağı - ANN ve Evrişimli Sinir Ağı - CNN) geliştirilmiştir. Projede, verilerin önişlemesinden model eğitimine, değerlendirmeye ve tek bir görüntü üzerinde tahmine kadar tüm adımlar detaylı olarak yer almaktadır.

https://www.kaggle.com/datasets/anthonytherrien/dog-vs-cat veriyi indirdikten sonra data_path değişkenini güncelleyin.

## İçerik

- **Veri Yükleme & Önişleme:**  
  Görüntüler, gri tonlamaya çevrilip, 128x128 boyutuna yeniden boyutlandırılıyor, tensor formatına dönüştürülüyor ve normalize ediliyor.

- **ANN Modeli:**  
  Basit bir tam bağlı sinir ağı (ANN) kullanılarak sınıflandırma gerçekleştiriliyor.

- **CNN Modeli:**  
  4 adet evrişim (convolution) katmanı ve fully-connected katmanlardan oluşan derin öğrenme mimarisi ile sınıflandırma yapılıyor. Katmanları artırabilirsiniz.

- **Model Eğitimi & Değerlendirme:**  
  Hem ANN hem de CNN modelleri, eğitim ve test veri setleri kullanılarak eğitilip değerlendiriliyor. Ek olarak, sklearn kütüphanesi ile detaylı sınıflandırma raporu ve doğruluk oranı hesaplanıyor.

- **Tek Görüntü Üzerinde Deneme:**  
  Belirtilen bir test görüntüsü üzerinde tahmin yapılarak, modelin gerçek zamanlı performansı gözlemlenebiliyor. 

## Gereksinimler

- Python 3.x
- [PyTorch](https://pytorch.org/)
- [torchvision](https://pytorch.org/vision/stable/index.html)
- [scikit-learn](https://scikit-learn.org/stable/)
- [Pillow](https://python-pillow.org/)
- [matplotlib](https://matplotlib.org/)
- [OpenCV](https://opencv.org/) (isteğe bağlı)

## Notlar

-   **Veri Organizasyonu:**  
    Veri seti, her sınıf için ayrı klasörler içeren `ImageFolder` formatında organize edilmelidir.
    
-   **Kendi Veriniz:**  
    Kendi verilerinizi kullanırken `data_path` değişkenini uygun şekilde güncellemeyi unutmayın.
    
-   **Model Eğitimi:**  
    Eğitim süresi ve epoch sayısı, veri setine ve sistem kaynaklarına göre ayarlanabilir.
