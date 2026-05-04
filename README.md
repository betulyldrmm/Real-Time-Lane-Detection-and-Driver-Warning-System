# 🚗 Şerit Takip Sistemi (Lane Detection for Autonomous Vehicle)

## 📌 Proje Hakkında

Bu projede, otonom araçlar için gerçek zamanlı çalışan bir şerit takip sistemi geliştirilmiştir. Sistem, kamera görüntülerini işleyerek yol üzerindeki şeritleri tespit eder ve aracın şeritten çıkma durumunu algılayarak kullanıcıyı uyarır.

## 🎯 Amaç

* Gerçek zamanlı görüntü işleme ile şerit tespiti yapmak
* Şerit dışına çıkıldığında uyarı sistemi geliştirmek
* Gömülü sistemler üzerinde (Raspberry Pi) çalışabilen bir çözüm üretmek

## 🛠️ Kullanılan Teknolojiler

* Python
* OpenCV
* NumPy
* Raspberry Pi
* Picamera2
* RPi.GPIO

## ⚙️ Sistem Çalışma Mantığı

1. Kamera üzerinden anlık görüntü alınır
2. Görüntü gri tona çevrilir
3. Gürültüyü azaltmak için Gaussian Blur uygulanır
4. Canny Edge Detection ile kenarlar tespit edilir
5. İlgi alanı (ROI) belirlenerek sadece yol kısmı analiz edilir
6. Şerit piksel yoğunluğu hesaplanır
7. Eğer şerit tespiti zayıfsa:

   * Ekranda uyarı verilir
   * Buzzer ile sesli uyarı yapılır

## 🔊 Uyarı Sistemi

Şerit kaybı durumunda GPIO üzerinden bağlı buzzer aktif edilerek kullanıcıya sesli geri bildirim sağlanır.

## 📷 Çalışma Prensibi

Sistem, belirlenen piksel eşik değerine göre şerit varlığını kontrol eder. Eğer bu değer belirlenen sınırın altına düşerse araç şeritten çıkmış olarak kabul edilir.

## 🚀 Kurulum

```bash
pip install opencv-python numpy
```

Raspberry Pi üzerinde:

```bash
sudo apt install python3-opencv
```

## ▶️ Çalıştırma

```bash
python gomulu2.py
```

## 📌 Notlar

* Proje gerçek zamanlı çalışacak şekilde optimize edilmiştir
* FPS değeri ekranda gösterilmektedir
* Çıkmak için 'Q' tuşuna basabilirsiniz

## 👨‍💻 Geliştirici

[Adını buraya yaz]
