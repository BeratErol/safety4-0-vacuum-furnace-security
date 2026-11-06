# LAB 7 - PaketPro 3000: Yapay Zekâ ve Emniyet

**Çıktı:** AI Fail-Safe Decision, Evidence Pack EP 03 ve EP 15.

## Kavram ve araçlar

Prediction ≠ Safety. YZ tahmin üretir. İnsanı koruyan emniyet mimarisi YZ kararından bağımsız çalışmalıdır.

Fail-safe güvenli davranışı, fallback güvenli işleyişe dönüşü, human override insanın kararı geçersiz kılmasını, monitoring izlemeyi ifade eder. Confidence threshold, altında otomatik kararın kabul edilmediği güven eşiğidir.

## Senaryo ve iş akışı

YZ ile görsel paket kontrolü eklenmesi planlanmaktadır. Kamera → YZ modeli → OK / RED → Ret mekanizması → Hat hızı akışı değerlendirilir.

## Görev - Üç başarısızlıkta güvenli davranış

### 1. Model kusurlu parçaya OK verirse ne yapılır?

Kusurlu paket ikinci kontrol veya insan onayıyla ayrılır. Ret sonucu izlenir. Işık perdesi ve çene/bıçak durdurma zinciri YZ kararından bağımsız çalışır.

### 2. Kamera girdisi bozuk veya sahteyse ne yapılır?

Lens kirliliği ve görüntü kaybı izlenir, kaynak ve veri bütünlüğü kontrol edilir. Şüpheli paket insan kontrolüne ayrılır. Güvenli ayırma yapılamıyorsa hat durdurulur.

### 3. Modelin güven puanı düşerse ne yapılır?

Eşik, paket kusurlarını kapsayan doğrulama testleriyle belirlenir. Eşik altında otomatik OK verilmez. Paket insan kontrolüne ayrılır, ret arızasında hat güvenli durdurulur.

## Karar tablosu - AI Fail-Safe Decision

| Başarısızlık | Güvenli davranış ve kavram |
|---|---|
| Yanlış sınıflandırma | İkinci kontrol ve insan onayı (human override), bağımsız emniyet. |
| Girdi manipülasyonu | Kaynak/kalite izleme (monitoring), otomatik kabulü engelleme (fail-safe). |
| Düşük güven puanı | Testlerle belirlenen eşik (confidence threshold), insan incelemesi ve güvenli işleyiş (fallback). |

## Kaynaklar

- INSPECCO × KRIPTARIUM, PaketPro 3000 LAB Föyleri, LAB 7, PDF s. 8.
- Safety 4.0 Bootcamp Sunumu, PDF s. 24 ve 26.
- Kavramlar Sözlüğü, YZ Güvenliği, PDF s. 3.
