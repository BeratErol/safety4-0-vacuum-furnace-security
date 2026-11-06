# LAB 7 - VF-1D-A-696: Yapay Zekâ ve Emniyet

**Çıktı:** AI Fail-Safe Decision, Evidence Pack EP 03 ve EP 15.

## Kavram ve araçlar

Prediction ≠ Safety. YZ tahmin üretir. İnsanı koruyan emniyet mimarisi YZ kararından bağımsız çalışmalıdır.

Fail-safe güvenli davranışı, fallback güvenli işleyişe dönüşü, human override insanın kararı geçersiz kılmasını, monitoring izlemeyi ifade eder. Confidence threshold, altında otomatik kararın kabul edilmediği güven eşiğidir.

## Senaryo ve iş akışı

Önerilen senaryoda YZ, yükleme öncesi yük düzenini değerlendirir. Kamera → YZ modeli → OK / RED → Operatör onayı → Yükleme kararı akışı kullanılır. Kamera ve YZ bu proje senaryosunun varsayımlarıdır.

## Görev - Üç başarısızlıkta güvenli davranış

### 1. Model kusurlu parçaya OK verirse ne yapılır?

Uygunsuz yük düzenine OK verilirse ikinci kontrol ve operatör onayı istenir. YZ kararı SF1 güvenli erişim ve SF2 aşırı sıcaklık korumasını etkisizleştiremez.

### 2. Kamera girdisi bozuk veya sahteyse ne yapılır?

Görüntü kalitesi, güncelliği ve kaynak bütünlüğü kontrol edilir. Şüpheli görüntüde otomatik yük kabulü engellenir. Çalışan çevrimde SF1/SF2 ve gerekli koruyucu soğutma sürdürülür.

### 3. Modelin güven puanı düşerse ne yapılır?

Eşik, farklı yük düzenlerini kapsayan testler ve yanlış kabul riskiyle belirlenir. Altında yeni çevrim onayı bekletilir, yük insan kontrolüne alınır. Çalışan proses tanımlanmış güvenli işleyişte tutulur.

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

## Sonuç

YZ, yük kontrolünü destekler. Şüpheli kararlar insan incelemesine aktarılırken SF1/SF2 ve koruyucu soğutma işlevleri korunmalıdır.
