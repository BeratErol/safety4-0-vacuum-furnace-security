# LAB 3 — Şişeleme Hattı: Tehdit ve Risk

**Çıktı:** Risk kaydı (Risk Register).

Senaryolar eğitim amaçlıdır. Erişim koşulları aşağıda belirtilen varsayımlara dayanır.

## Değerlendirme yöntemi

Her senaryo beş parçadır: Kim → Giriş kapısı → Eylem → Zincir → Fiziksel sonuç.

| Ölçüt | Anlamı |
|---|---|
| L | Saldırı yolunun istismar edilebilirliği / olasılığı. |
| S | Fiziksel sonucun şiddeti. |
| E | Saldırı yolunun dışa açıklığı; çalışanın fiziksel maruziyeti değildir. |

Her ölçüt 1–3 aralığında puanlanır. Skor = L × S × E. Kritik: 18–27; yüksek: 9–17; orta: 4–8; düşük: 1–3. S=3 olan senaryolar düşük skorda da ayrıca öne alınır.

## Senaryo 1 — Uzak servis erişimi

Fırsatçı dış saldırgan → Uzak servis erişimi → PLC ayarlarını değiştirir → Makine beklenmedik şekilde çalışır → Koruma yetersizse çalışan sıkışarak ciddi şekilde yaralanabilir.

**Varsayım:** Uzak servis internete açık, erişim koruması yetersiz ve üretim parametrelerini değiştirmeye izin veriyor.

**Puan:** L=3, S=3, E=3 → 27 (Kritik).

L yüksek çünkü varsayılan erişim koşulları istismarı kolaylaştırıyor. S yüksek çünkü ciddi yaralanma mümkün. E yüksek çünkü giriş yolu internete açık.

## Senaryo 2 — HMI üzerinden yetkisiz değişiklik

Yetkisini aşan çalışan → HMI paneli → Üretim hızını değiştirir → Şişeler sıkışır → Sıkışmaya müdahale eden çalışan elinden yaralanabilir.

**Varsayım:** HMI’ye fabrika içinden erişilebiliyor, yetki kısıtları yetersiz ve müdahale sırasında koruma yeterli değil.

**Puan:** L=2, S=2, E=2 → 8 (Orta).

Yetkisiz değişiklik belirli koşullara bağlıdır; örnekte hafif, geri dönüşlü yaralanma ve kısıtlı ağ erişimi varsayılmıştır.

## Senaryo 3 — Safety PLC parametrelerine müdahale

Tedarik zinciri saldırganı → Mühendislik istasyonu → Safety PLC parametrelerini değiştirir → Acil durdurma fonksiyonu bozulur → Makine durmayarak çalışanın ciddi şekilde yaralanmasına neden olabilir.

**Varsayım:** Emniyet yapılandırmasına yalnızca makine başında fiziksel erişimle ulaşılabilir; saldırganın bu erişimi ve yetkili mühendislik bağlantısını kötüye kullanması gerekir.

**Puan:** L=1, S=3, E=1 → 3 (Düşük; S=3 nedeniyle ayrıca öncelikli).

L ve E erişim koşulları nedeniyle düşük, fiziksel sonucun ağırlığı nedeniyle S yüksektir. Bu puanlar erişim varsayımları değişirse yeniden değerlendirilir.

## Risk tablosu

| Senaryo | L | S | E | Skor | Öncelik |
|---|---|---|---|---|---|
| 1 — Uzak servis | 3 | 3 | 3 | 27 | Kritik |
| 2 — HMI | 2 | 2 | 2 | 8 | Orta |
| 3 — Safety PLC | 1 | 3 | 1 | 3 | Düşük; S=3 özel işaretli |

## 1. En yüksek öncelikli senaryo hangisi ve neden?

Uzak servis senaryosu en yüksek skora sahiptir. Varsayılan açık erişim üzerinden PLC ayarlarının değiştirilmesi ciddi fiziksel yaralanmaya yol açabilir.

## 2. S=3 olup skoru düşük kalan senaryo var mı?

Evet, Safety PLC senaryosu. Risk tablosunda S3 bayrağıyla ayrıca işaretlenir; öncelikli incelemeye alınır ve önlem ya da yazılı kabul kararı olmadan kapatılmaz.

## Kaynaklar

- INSPECCO × KRIPTARIUM, Genel LAB Föyleri: PDF s. 4.
- Safety 4.0 Bootcamp Sunumu: PDF s. 15–18.
- Kavramlar Sözlüğü: Tehdit ve Risk, PDF s. 2.
- Fatih Özkaynak, Threat & Risk Lab + Safety 4.0 Risk Matrix (LAB3.pdf): PDF s. 11, 23–29 ve 35–37.
