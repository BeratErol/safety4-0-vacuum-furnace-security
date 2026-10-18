# LAB 3 — PaketPro 3000: Tehdit ve Risk

**Çıktı:** Risk kaydı (Risk Register).

Föydeki PaketPro örneği esas alınmıştır. Senaryoya eklenen erişim koşulları ve fiziksel sonuçlar varsayım olarak belirtilmiştir.

## Değerlendirme yöntemi

Her senaryo beş parçadır: Kim → Giriş kapısı → Eylem → Zincir → Fiziksel sonuç.

| Ölçüt | Anlamı |
|---|---|
| L | Saldırı yolunun istismar edilebilirliği / olasılığı. |
| S | Fiziksel sonucun şiddeti. |
| E | Saldırı yolunun dışa açıklığı; çalışanın fiziksel maruziyeti değildir. |

Her ölçüt 1–3 aralığında puanlanır. Skor = L × S × E. Kritik: 18–27; yüksek: 9–17; orta: 4–8; düşük: 1–3. S=3 olan senaryolar ayrıca işaretlenir.

## Senaryo 1 — Uzak bakım üzerinden PLC’ye müdahale

Fırsatçı dış saldırgan → İnternete açık uzak bakım modülü → Üretim PLC ayarlarını değiştirir → Paketleme makinesi beklenmedik şekilde çalışır → Emniyet koruması yetersizse çalışan çene veya bıçakta ciddi şekilde yaralanabilir.

**Varsayım:** Zayıf servis hesabıyla PLC ayarlarına ulaşılabiliyor ve senaryodaki koruma, tehlikeli hareketi önleyemiyor.

**Puan:** L=3, S=3, E=3 → 27 (Kritik).

L=3: Varsayılan veya zayıf hesap erişimi kolaylaştırır. S=3: Çene ve bıçak ağır yaralanmaya yol açabilir. E=3: Uzak bakım modülü internete doğrudan açıktır.

## Senaryo 2 — HMI üzerinden üretim hızının değiştirilmesi

Yetkisini aşan çalışan → HMI web arayüzü → Üretim hızını değiştirir → Ambalaj sıkışır → Sıkışan ambalaja müdahale eden çalışan elinden hafif şekilde yaralanabilir.

**Varsayım:** HMI fabrika ağından erişilebilir ve yetki sınırları yetersizdir. Çene ve bıçak emniyetle durmuştur; bu senaryonun fiziksel sonucu ambalaj malzemesinin neden olduğu hafif, geri dönüşlü kesidir.

**Puan:** L=2, S=2, E=2 → 8 (Orta).

L=2: Yetkisiz değişiklik için kullanıcı erişimi gerekir. S=2: Hafif, geri dönüşlü yaralanma varsayılmıştır. E=2: HMI’ye fabrika ağından erişilir. Sıcak çene veya hareketli bıçakla temas mümkünse S yeniden değerlendirilir.

## Senaryo 3 — Servis bilgisayarından emniyet parametresi değişikliği

Tedarik zinciri saldırganı → Servis bilgisayarı → Safety PLC parametrelerini değiştirir → Işık perdesinin durdurma fonksiyonu bozulur → Çene veya bıçak durmayarak çalışanın ciddi şekilde yaralanmasına neden olabilir.

**Varsayım:** Emniyet yapılandırmasına yalnızca makine başında fiziksel bağlantıyla ulaşılır. Servis bilgisayarının ele geçirilmesi ve yapılandırma kontrollerinin aşılması gerekir; uzak bakım modülü bu değişiklik yoluna doğrudan erişemez.

**Puan:** L=1, S=3, E=1 → 3 (Düşük; S3 bayraklı).

L=1: Birden çok kontrolün aşılması gerekir. S=3: Çene veya bıçak ağır yaralanma oluşturabilir. E=1: Yapılandırma için fiziksel erişim gerekir. Bu varsayımlar geçerli değilse L ve E yeniden puanlanır.

## Risk tablosu

| Senaryo | L | S | E | Skor | Öncelik |
|---|---|---|---|---|---|
| 1 — Uzak bakım | 3 | 3 | 3 | 27 | Kritik |
| 2 — HMI | 2 | 2 | 2 | 8 | Orta |
| 3 — Safety PLC | 1 | 3 | 1 | 3 | Düşük; S3 bayraklı |

## 1. En yüksek öncelikli senaryo hangisi ve neden?

Uzak bakım senaryosu en yüksek skora sahiptir. İnternete açık giriş ve zayıf erişim kontrolü, senaryodaki emniyet yetersizliğiyle birlikte ciddi yaralanmaya yol açabilir.

## 2. S=3 olup skoru düşük kalan senaryo var mı?

Evet, Safety PLC senaryosu. S3 bayrağıyla ayrıca gösterilir; önlem veya yazılı kabul kararı olmadan kapatılmaz.

## Kaynaklar

- INSPECCO × KRIPTARIUM, PaketPro 3000 LAB Föyleri: PDF s. 4.
- Safety 4.0 Bootcamp Sunumu: PDF s. 12 ve 15–18.
- Kavramlar Sözlüğü: Tehdit ve Risk, PDF s. 2.
- Fatih Özkaynak, Threat & Risk Lab + Safety 4.0 Risk Matrix (LAB3.pdf): PDF s. 11, 23–29 ve 35–37.
