# LAB 1 — Şişeleme Hattı: Emniyet Mimarisi

**Çıktı:** Emniyet fonksiyon haritası (Safety Function Map).

Çalışma, derste kullanılan örnek şişeleme hattına aittir.

## 1. Tehlike nedir? İnsan neyden zarar görür?

Motorlar ve hareketli parçalar tehlike oluşturur. Çalışanın eli veya kolu bu parçalara sıkışırsa ezilme ya da kesilme gibi yaralanmalar meydana gelebilir.

## 2. Emniyet fonksiyonu hangisidir?

Acil durdurmaya basıldığında veya ışık perdesi ihlal edildiğinde tehlikeli hareketlerin güvenli biçimde durdurulması ve makinenin güvenli duruma getirilmesidir.

## 3. Emniyetle ilgili kontrol sistemi nerede?

Emniyetle ilgili kontrol sistemi, aşağıdaki emniyet yolundadır. Sensör veya acil durdurmadan gelen talep Safety PLC tarafından değerlendirilir; çıkışlar tehlikeli hareketin durdurulmasını sağlar.

| Yol | Fonksiyon haritası |
|---|---|
| Normal kontrol | Proses sensörü → Normal PLC → Aktüatör |
| Emniyet | Acil durdurma / Işık perdesi → Safety PLC → STO / Kontaktör → Güvenli durum |
| Dijital kesişim | IPC / bakım erişimi → Yetkili mühendislik bağlantısı → Emniyet yapılandırması |

STO, sürücünün tork üretmesini engelleyen emniyet işlevidir; tek başına bütün enerji kaynaklarının izolasyonu anlamına gelmez. Harita, föydeki örnek mimariyi gösterir.

## 4. Normal PLC ile Safety PLC farkı nedir?

Normal PLC üretim sürecini ve makinenin normal hareketlerini kontrol eder. Safety PLC ise insanı koruyan emniyet fonksiyonlarını yürütür. Korumanın güvenilirliği, sensörden son elemana kadar bütün emniyet yoluna bağlıdır.

## 5. PLr / SIL neden var? Bu fonksiyon için neden önemli?

Emniyet fonksiyonunun riskle orantılı bir güvenilirlik düzeyine sahip olması gerekir. PLr gerekli performans seviyesini, SIL ise emniyet bütünlük seviyesini ifade eder. Bu çalışmada sayısal seviye atanmamıştır.

## 6. Güvenli durum (safe state) nedir?

Bu örnekte, tehlikeli hareketlerin güvenli biçimde durdurulduğu ve insan için fiziksel risk oluşturmayacak duruma geçildiği haldir. Yeniden çalışma kontrollü olmalıdır.

## 7. Emniyet fonksiyonu hangi dijital bağımlılıklara sahip?

Safety PLC uygulaması, emniyet parametreleri, kullanılan yazılım ve bakım/güncelleme erişimleri bu fonksiyonu etkileyebilir. Yetkisiz değişiklik, beklenen durdurma davranışını bozabilir.

## 8. Siber müdahale hangi noktadan bu fonksiyonu bozar?

IPC veya bakım erişimi üzerinden emniyet yapılandırmasına ulaşılabiliyorsa dijital kesişim noktasında müdahale oluşabilir. Saldırgan gerekli erişimi elde edip Safety PLC parametrelerini değiştirirse emniyet fonksiyonu etkilenebilir. Bu, eğitim amaçlı olası bir senaryodur.

## Kaynaklar

- INSPECCO × KRIPTARIUM, Genel LAB Föyleri: PDF s. 2.
- Safety 4.0 Bootcamp Sunumu: PDF s. 4–8.
- Kavramlar Sözlüğü: LAB 1 terimleri, PDF s. 1.
