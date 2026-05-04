Embedded Systems / Computer Vision
Şerit Takip Sistemi
Otonom araçlar için gerçek zamanlı görüntü işleme tabanlı şerit tespiti ve uyarı sistemi. Raspberry Pi üzerinde çalışır.
Sistem, belirlenen piksel eşik değerine (500 px) göre şerit varlığını kontrol eder. Değer bu sınırın altına düşerse buzzer ile sesli uyarı verilir.
Platform
Raspberry Pi + Picamera2
Çözünürlük
320 × 240 px (RGB888)
Uyarı Çıkışı
GPIO 17 — Buzzer
Çıkış Tuşu
Q tuşu
Kullanılan teknolojiler
Python
OpenCV
NumPy
Picamera2
RPi.GPIO
Canny Edge Detection
Çalışma adımları
1
Kameradan anlık kare alınır
2
Görüntü gri tona çevrilir
3
Gaussian Blur ile gürültü azaltılır
4
Canny ile kenarlar tespit edilir
5
ROI maskesiyle yol bölgesi seçilir
6
Piksel yoğunluğu ölçülür
7
Eşik altında uyarı tetiklenir
Kurulum
# Standart ortam
pip install opencv-python numpy

# Raspberry Pi
sudo apt install python3-opencv
Çalıştırma
python gomulu2.py
Geliştirici: —
Real-time
Embedded
FPS monitored
