# LAB 1 — VF-1D-A-696: Emniyet Mimarisi

**Çıktı:** Önerilen emniyet fonksiyon haritası (Safety Function Map).

## Analizin kapsamı

Fırının sıcaklık, basınç ve erişim tehlikeleri değerlendirilerek güvenli erişim (SF1) ve aşırı sıcaklık koruması (SF2) için emniyet fonksiyon haritası hazırlanmıştır. Analizde NADCA testindeki proses bilgileri esas alınmıştır. [K1, PDF s. 4 ve 6](../../01-Makine-Tanitimi/Kaynaklar.md)

## 1. Tehlike nedir? İnsan neyden zarar görür?

Sıcak yük veya yüzeyle temas yanığa, basınç farkı varken kapağa erişim ciddi yaralanmaya yol açabilir. Azot kaçağı da kapalı veya yetersiz havalandırılan bir ortamda oksijen azalması tehlikesi oluşturabilir. Bunlar proses üzerinden belirlenen olası tehlikelerdir; makinede tespit edilmiş arızalar değildir.

## 2. Emniyet fonksiyonu hangisidir?

| Kod | Önerilen fonksiyon |
|---|---|
| SF1 — Güvenli erişim | Sıcaklık ve basınç koşulları güvenli olarak doğrulanmadan tehlikeli bölgeye erişimi engellemek. |
| SF2 — Aşırı sıcaklık koruması | Tehlikeli aşırı sıcaklıkta ısıtmayı sınırlandırmak; gerekli koruyucu soğutma işlevlerini sürdürmek. |

Güvenli eşikler ve tepki süreleri üretici tasarımı ve risk değerlendirmesiyle belirlenmelidir; deney değerleri emniyet eşiği değildir.

## 3. Emniyetle ilgili kontrol sistemi nerede?

| Yol | İşlevsel harita |
|---|---|
| Belgelenen proses | Sıcaklık / basınç ölçümü → Proses kontrolü ve SCADA → Isıtma / vakum / soğutma |
| Önerilen SF1 | Güvenilir sıcaklık ve basınç bilgisi → Bağımsız emniyet mantığı → Erişim izninin engellenmesi |
| Önerilen SF2 | Bağımsız aşırı sıcaklık algılama → Emniyet mantığı → Isıtma sınırlandırma ve koruyucu işlevler |
| Olası dijital kesişim | Yetkili mühendislik bağlantısı → Emniyet yapılandırması |

Harita belirli bir Safety PLC’nin varlığını göstermez. NADCA test termokuplları da bağımsız emniyet sensörleri olarak kabul edilmemiştir.

## 4. Normal PLC ile Safety PLC farkı nedir?

Normal kontrol; reçete, sıcaklık rampaları ve proses adımlarını yönetir. Emniyet kontrolü ise SF1 ve SF2 gibi insanı koruyan fonksiyonları güvenilir biçimde yürütmelidir. Bu fırında hangi kontrol cihazlarının kullanıldığı henüz bilinmemektedir.

## 5. PLr / SIL neden var? Bu fonksiyon için neden önemli?

Emniyet fonksiyonunun gereken güvenilirliği riskle ilişkilendirilir. PLr gerekli performans seviyesini, SIL emniyet bütünlük seviyesini ifade eder. Ayrıntılı risk verileri ve devre bilgileri olmadan bu fırına sayısal seviye atanmaz.

## 6. Güvenli durum (safe state) nedir?

İnsanın sıcaklık ve basınç kaynaklı tehlikelerden korunduğu, tehlikeli erişimin engellendiği ve prosesin kontrollü tutulduğu durumdur. Yalnızca bütün enerjiyi kesmek güvenli kabul edilmez; artık ısı ve basınç ile gerekli soğutma işlevleri değerlendirilmelidir.

## 7. Emniyet fonksiyonu hangi dijital bağımlılıklara sahip?

Varsa emniyet yazılımı, sıcaklık/basınç eşikleri, sensör doğrulama mantığı ve mühendislik erişimi bu fonksiyonları etkileyebilir. Gerçek parametreler ve bağlantılar bilinmediğinden bunlar incelenecek bağımlılıklardır.

## 8. Siber müdahale hangi noktadan bu fonksiyonu bozar?

Bir mühendislik hesabı veya kontrol istasyonu üzerinden eşik ve erişim izni mantığı değiştirilebiliyorsa SF1/SF2 etkilenebilir. Bunun fiziksel sonuca ulaşması için bağımsız korumaların da yetersiz veya etkilenmiş olması gerekir. Uzaktan erişim, modelde doğrulanmış bir özellik değildir.

## Kaynaklar

- [K1 ve K4 — NADCA test yayınları](../../01-Makine-Tanitimi/Kaynaklar.md).
- Genel LAB Föyleri, PDF s. 2; Bootcamp Sunumu, PDF s. 4–8; Kavramlar Sözlüğü, PDF s. 1.
- [HSE — The safe isolation of plant and equipment, HSG253](https://www.hse.gov.uk/pubns/priced/hsg253.pdf): artık enerji ve izolasyon için genel başvuru; modele özel belge değildir.
- [NIST SP 800-82 Rev. 3 — OT Security](https://csrc.nist.gov/pubs/sp/800/82/r3/final): siber güvenlik ve emniyet ilişkisi.

## Sonuç

Analizde güvenli erişim ve aşırı sıcaklık koruması temel emniyet fonksiyonları olarak ele alınmıştır. Bu fonksiyonların proses kontrolünden gelebilecek hatalı veya yetkisiz değişikliklere karşı korunması önceliklidir.
