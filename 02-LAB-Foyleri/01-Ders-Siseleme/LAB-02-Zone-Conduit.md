# LAB 2 — Şişeleme Hattı: Zone / Conduit

**Çıktı:** Bölge ve bağlantı şeması (Zone / Conduit Diagram).

Aşağıdaki gruplama, ders örneği için hazırlanmış bir tasarım önerisidir.

## Görev A — Varlıkları bölgelere ayırma

### 1. Hangi varlıklar aynı bölgede?

| Bölge | Varlıklar | Gerekçe |
|---|---|---|
| Üretim | PLC, HMI, robot kontrolörü | Üretim sürecini ve makinenin hareketlerini yönetir. |
| Emniyet | Safety PLC | İnsan güvenliğiyle ilgili fonksiyonları yürütür. |
| İzleme / Mühendislik | SCADA istemcisi, mühendislik istasyonu | İzleme ve bakım işlemleri için kullanılır. |
| Uzak erişim / DMZ | Uzak servis erişimi ve önerilen ara sunucu | Dış bağlantıların kontrollü olarak sonlandırılmasını sağlar. |
| Ofis | ERP / e-posta ağı | Ofis işlemleri üretim ve emniyet sistemlerinden ayrılır. |

Bu basitleştirilmiş gruplamada SCADA ve mühendislik istasyonu aynı bölgede gösterilmiştir; izleme ile değişiklik yapma yetkileri ayrıca sınırlandırılır.

### 2. Safety PLC hangi bölgede ve neden?

Safety PLC ayrı bir emniyet bölgesindedir. İnsan güvenliğini sağlayan görevleri nedeniyle erişimi daha sıkı kontrol edilmeli; üretim veya ofis ağındaki bir sorun emniyet yapılandırmasına serbest erişim sağlamamalıdır.

### 3. Bölgeler arası geçişler nerede? Ne kontrol edilir?

| Geçiş (conduit) | Kontrol |
|---|---|
| Uzak servis → Uzak erişim / DMZ | Kimlik doğrulama, süreli erişim ve oturum kaydı. |
| Uzak erişim / DMZ → İzleme / Mühendislik | Yalnızca yetkili kullanıcı ve hedeflere izin verilmesi. |
| İzleme / Mühendislik → Üretim | İzinli cihaz, protokol ve işlemlerin sınırlandırılması. |
| Yetkili mühendislik erişimi → Emniyet | Yapılandırma yetkisi, değişiklik onayı ve kayıt. |
| Ofis → OT sistemleri | Yalnızca gerekli veri akışlarına izin verilmesi. |

Her geçiş ayrı kontrol edilir; uzak servisten emniyet sistemine doğrudan erişim öngörülmez.

## Görev B — Uzak erişim kararı

| Karar | Seçim ve nedeni |
|---|---|
| Aracı | Jump server: Doğrudan makine bağlantısı yerine kontrollü bir ara nokta sağlar. |
| Tünel | VPN: İletişimin şifreli aktarılmasını sağlar. |
| Kimlik | MFA: Parolaya ek doğrulama ister. |
| Hesap | Kişisel: Kimin işlem yaptığı izlenebilir. |
| Kayıt | Tam oturum kaydı: Yapılan işlemler sonradan incelenebilir. |
| Zamanlama | Varsayılan kapalı: Uzak erişim yalnızca gerektiğinde süreli açılır. |

## Kaynaklar

- INSPECCO × KRIPTARIUM, Genel LAB Föyleri: PDF s. 3.
- Safety 4.0 Bootcamp Sunumu: PDF s. 9–14.
- Kavramlar Sözlüğü: zone, conduit ve uzak erişim terimleri.
