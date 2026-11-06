# LAB 7 - Şişeleme Hattı: Yapay Zekâ ve Emniyet

**Çıktı:** AI Fail-Safe Decision, Evidence Pack EP 03 ve EP 15.

## Kavram ve araçlar

Prediction ≠ Safety. YZ tahmin üretir. İnsanı koruyan emniyet mimarisi YZ kararından bağımsız çalışmalıdır.

Fail-safe güvenli davranışı, fallback güvenli işleyişe dönüşü, human override insanın kararı geçersiz kılmasını, monitoring izlemeyi ifade eder. Confidence threshold, altında otomatik kararın kabul edilmediği güven eşiğidir.

## Senaryo ve iş akışı

Föydeki akış Kamera → YZ modeli → OK / RED → Parametre → Robot şeklindedir. Şişeleme hattındaki görsel ürün kontrolü üzerinden değerlendirilmiştir.

## Görev - Üç başarısızlıkta güvenli davranış

### 1. Model kusurlu parçaya OK verirse ne yapılır?

Kusurlu ürün ikinci kontrol veya insan onayıyla ayrılır. YZ’nin OK kararı robotun bağımsız emniyet koşullarını aşamaz.

### 2. Kamera girdisi bozuk veya sahteyse ne yapılır?

Görüntü kalitesi, güncelliği ve veri kaynağı kontrol edilir. Şüpheli görüntüde otomatik kabul engellenir, ürün insan incelemesine ayrılır.

### 3. Modelin güven puanı düşerse ne yapılır?

Eşik, doğrulama verileri ve yanlış kabul riskiyle belirlenir. Eşik altında ürün insan kontrolüne ayrılır. Güvenli ayırma mümkün değilse hat kontrollü durdurulur.

## Karar tablosu - AI Fail-Safe Decision

| Başarısızlık | Güvenli davranış ve kavram |
|---|---|
| Yanlış sınıflandırma | İkinci kontrol ve insan onayı (human override), bağımsız emniyet. |
| Girdi manipülasyonu | Kaynak/kalite izleme (monitoring), otomatik kabulü engelleme (fail-safe). |
| Düşük güven puanı | Testlerle belirlenen eşik (confidence threshold), insan incelemesi ve güvenli işleyiş (fallback). |

## Kaynaklar

- INSPECCO × KRIPTARIUM, Genel LAB Föyleri, LAB 7, PDF s. 8.
- Safety 4.0 Bootcamp Sunumu, PDF s. 24 ve 26.
- Kavramlar Sözlüğü, YZ Güvenliği, PDF s. 3.
