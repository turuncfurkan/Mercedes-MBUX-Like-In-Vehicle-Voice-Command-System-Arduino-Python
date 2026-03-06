# MBUX Benzeri Sesli Komut Sistemi – Arduino & Python

## Proje Özeti

Bu proje, bilgisayar mikrofonu, Python ve Arduino kullanarak MBUX benzeri basit bir sesli komut sistemi geliştirmeyi amaçlar.

Sistem, kullanıcı **“Hey Mercedes”** veya **“Mercedes”** dediğinde aktif hale gelir ve sesli olarak geri dönüş yapar. Ardından verilen kısa sesli komutları algılayarak Arduino üzerinden fiziksel çıktılar üretir.

Sistem üzerinden şu işlemler gerçekleştirilebilir:

- RGB LED’in mavi, kırmızı veya yeşil renkte yanması
- Servo motorun çalıştırılması
- “Kapat” komutu ile LED ve servo motorun kapatılması
- Wake word sonrası kullanıcıya sesli geri bildirim verilmesi

Bu proje, sesli komut algılama, seri haberleşme ve Arduino kontrollü fiziksel çıktı üretimi açısından temel ama etkili bir gömülü sistem ve insan-makine arayüzü deneyimi sunar.

## Kullanılan Malzemeler

- Arduino Uno  
- SG90 Servo Motor  
- RGB LED  
- Dirençler (220Ω / 330Ω)  
- Jumper kablolar  
- Breadboard  
- Bilgisayar mikrofonu  

## Devre Bağlantıları

- **RGB LED**
  - Kırmızı kanal → D3
  - Yeşil kanal → D5
  - Mavi kanal → D6
  - Her renk hattında seri direnç kullanılır
  - Ortak bacak → LED tipine göre GND veya 5V

- **SG90 Servo Motor**
  - Kahverengi → GND
  - Kırmızı → 5V
  - Turuncu → D9

## Python Tarafı

Python tarafında sistem şu görevleri yerine getirir:

- Bilgisayar mikrofonundan sesi dinleme  
- “Hey Mercedes” / “Mercedes” uyandırma kelimesini algılama  
- Kullanıcıya sesli geri bildirim verme  
- Kısa sesli komutları algılama  
- Arduino’ya seri port üzerinden komut gönderme  

## Desteklenen Komutlar

- **Mercedes / Hey Mercedes** → Sistemi uyandırır  
- **Mavi** → RGB LED mavi yanar  
- **Kırmızı / Kirmizi** → RGB LED kırmızı yanar  
- **Yeşil / Yesil** → RGB LED yeşil yanar  
- **Motor** → Servo motor çalışır  
- **Kapat** → RGB LED ve servo motor kapanır  
- **Ambiyans** → Sesli geri bildirim verir  

## Kod Dosyaları

- `main_assistant.py` → Ana sistem akışı  
- `wake_word.py` → Wake word algılama  
- `command_listener.py` → Komut dinleme  
- `test_serial.py` → Seri haberleşme testi  
- `mbux_arduino.ino` → Arduino kontrol kodu  

## Öğrenim Kazanımları

- Python ile sesli komut sistemi geliştirme  
- Wake word mantığını uygulama  
- Bilgisayar ile Arduino arasında seri haberleşme kurma  
- RGB LED ve servo motor kontrolü  
- Sesli komutları fiziksel çıktıya dönüştürme  
- Projeyi GitHub üzerinde dokümante etme  
