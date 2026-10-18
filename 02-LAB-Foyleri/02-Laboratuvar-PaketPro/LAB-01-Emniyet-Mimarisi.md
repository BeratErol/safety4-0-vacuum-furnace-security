# LAB 1 — PaketPro 3000: Emniyet Mimarisi

**Çıktı:** Emniyet fonksiyon haritası (Safety Function Map).

Çalışma, laboratuvarda kullanılan örnek paketleme makinesine aittir.

## 1. Tehlike nedir? İnsan neyden zarar görür?

Sıcak yapıştırma çenesi ve film kesme bıçağı el ve parmaklar için tehlikelidir. Çalışan bu bölgeye girerse yanma, kesilme veya sıkışma nedeniyle yaralanabilir.

## 2. Emniyet fonksiyonu hangisidir?

Işık perdesi ihlal edildiğinde veya koruyucu kapak açıldığında tehlikeli çene ve bıçak hareketinin güvenli biçimde durdurulmasıdır. Koruyucu koşullar sağlanmadan yeniden hareket engellenmelidir.

## 3. Emniyetle ilgili kontrol sistemi nerede?

| Yol | Fonksiyon haritası |
|---|---|
| Normal kontrol | Proses sensörü → Üretim PLC → Çene ve bıçak hareketi |
| Emniyet | Işık perdesi / Kapak kilidi → Safety PLC → STO / Kontaktör → Güvenli durum |
| Dijital kesişim | Uzak bakım veya servis bağlantısı → Erişilebilen emniyet yapılandırması |

Emniyet sistemi, algılayıcıdan tehlikeli hareketi durduran son elemana kadar olan yoldur. STO tork üretimini engeller; sıcak çenenin soğuduğu veya tüm enerjilerin izole edildiği anlamına gelmez.

## 4. Normal PLC ile Safety PLC farkı nedir?

Normal PLC paketleme sürecini ve çene-bıçak hareketlerini yönetir. Safety PLC, ışık perdesi ve kapak kilidi gibi korumalardan gelen bilgiyi değerlendirerek emniyet fonksiyonunu yürütür. Güvenilirlik, bütün emniyet yolunun tasarımına bağlıdır.

## 5. PLr / SIL neden var? Bu fonksiyon için neden önemli?

Emniyet fonksiyonunun riskle orantılı güvenilirliğini tanımlamak için kullanılır. PLr gerekli performans seviyesini, SIL emniyet bütünlük seviyesini ifade eder. Çene ve bıçak ciddi yaralanmaya yol açabileceğinden korumanın güvenilir olması önemlidir. Bu çalışmada sayısal seviye atanmamıştır.

## 6. Güvenli durum (safe state) nedir?

Tehlikeli çene ve bıçak hareketi durdurulur, beklenmedik yeniden çalışma engellenir. Çenenin artık sıcaklığı tehlike oluşturmaya devam edebileceğinden yalnızca hareketin durması bakım veya elle müdahale için yeterli kabul edilmez.

## 7. Emniyet fonksiyonu hangi dijital bağımlılıklara sahip?

Safety PLC uygulaması, tepki süreleri ve diğer emniyet parametreleri ile bakım/güncelleme erişimleri fonksiyonu etkileyebilir. Yetkisiz değişiklik, koruyucunun beklenen zamanda durdurma yapmasını bozabilir.

## 8. Siber müdahale hangi noktadan bu fonksiyonu bozar?

Föydeki internete açık uzak bakım modülünden emniyet yapılandırmasına erişilebiliyorsa saldırgan dijital kesişim noktasını kullanabilir. Safety PLC parametreleri değiştirildiğinde ışık perdesi veya kapak kilidinin durdurma davranışı etkilenebilir. Emniyet sistemine bu yoldan erişim, senaryoda ayrıca varsayılmalıdır.

## Kaynaklar

- INSPECCO × KRIPTARIUM, PaketPro 3000 LAB Föyleri: PDF s. 2.
- Safety 4.0 Bootcamp Sunumu: PDF s. 4–8.
- Kavramlar Sözlüğü: LAB 1 terimleri, PDF s. 1.
