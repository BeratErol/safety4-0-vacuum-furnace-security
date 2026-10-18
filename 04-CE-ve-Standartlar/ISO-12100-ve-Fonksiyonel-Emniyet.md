# ISO 12100 ve Fonksiyonel Emniyet

## Analizin kapsamı

Fırının fiziksel tehlikeleri ve bunlara ulaşan siber senaryolar, risk azaltma ve emniyet kontrolü açısından birlikte değerlendirilmiştir. İnceleme, mevcut tehlike tablosu ile SF1 ve SF2 fonksiyonlarına dayanır.

## Standartların projedeki yeri

| Referans | Ele aldığı konu | Projedeki kullanım |
|---|---|---|
| ISO 12100:2010 | Makine tehlikelerinin belirlenmesi, risk değerlendirmesi ve risk azaltma yöntemi | T01–T05 tehlikeleri ve koruma ihtiyaçları |
| ISO 13849-1:2023 | Emniyetle ilgili kontrol sistemi bölümlerinin tasarım ve entegrasyonu | SF1/SF2 için gereken performans ve kontrol yapısının incelenmesi |
| IEC 62061:2021 ve değişiklikleri | Makine emniyet kontrol sistemlerinin tasarımı, entegrasyonu ve geçerlenmesi | SF1/SF2 güvenilirlik ve doğrulama kanıtlarının incelenmesi |

IEC 62061 için AMD1:2024 ve AMD2:2026 değişiklikleri de yayımlanmıştır. Hangi standardın ve sürümün kullanılacağı, sistem kapsamı ve ilgili mevzuatla birlikte değerlendirilir.

## Tehlike ile emniyet fonksiyonu arasındaki ilişki

| Tehlike | Analiz edilen koruma | İlgili siber risk |
|---|---|---|
| T01 — Sıcak yüke erişim | SF1: Güvenli sıcaklık koşulları doğrulanmadan erişimi engelleme | R01 — Operatör istasyonu |
| T01 — Aşırı ısınma | SF2: Isıtmayı sınırlandırma ve gerekli koruyucu işlevleri sürdürme | R02 — Olası uzak bakım |
| T02 — Tehlikeli basınçta erişim | SF1: Güvenli basınç doğrulaması ve erişim kilitlemesi | R03 — Yerel servis |
| T03–T05 — Azot, yük ve elektrik | Gaz/ortam kontrolü, güvenli taşıma ve bakım izolasyonunun değerlendirilmesi | Ayrı siber zincir kurulmadı |

SF1 ve SF2 proje kapsamında önerilen işlevlerdir. Gerçek emniyet donanımı ve yapılandırması için teknik kanıt gerekir.

## Risk azaltma yaklaşımı

- Tasarımdan kaynaklanan tehlikeleri azaltma imkânları incelenir.
- Kalan tehlikeler için uygun koruyucu işlevler değerlendirilir.
- Kullanım ve bakım bilgileriyle kalan riskler açıklanır.

Siber erişim önlemleri bu yapıyı destekler. Yalnızca parola veya VPN kullanılması, fiziksel emniyet fonksiyonunun güvenilirliğini tek başına göstermez.

## Fırına özgü kapsam

ISO 13577-1:2016, endüstriyel fırınların genel emniyet gereksinimlerini; IEC 60519-1:2020 ise endüstriyel elektrikli ısıtma sistemlerinin genel emniyetini ele alır. Fırının ısıtma yöntemi ve ekipman sınırlarıyla birlikte incelenmelidir. Bu referanslar, ISO 12100 risk analizini fırına özgü teknik gereksinimlerle tamamlar; tek başına uygunluk kanıtı oluşturmaz.

## Değerlendirme için gereken bilgiler

| Başlık | Gereken bilgi / kanıt |
|---|---|
| Risk koşulları | Amaçlanan kullanım, öngörülebilir yanlış kullanım, maruziyet ve kaçınma imkânı |
| Emniyet gereksinimleri | Güvenli eşikler, tepki süresi, güvenli durum ve yeniden başlatma koşulları |
| Kontrol yapısı | Sensör, mantık birimi, son eleman ve bunların devre bağlantıları |
| Güvenilirlik | Seçilen yönteme uygun bileşen ve hesap bilgileri |
| Geçerleme | Emniyet fonksiyonunun gereksinimleri sağladığını gösteren kayıtlar |
| Değişiklik yönetimi | Yazılım/parametre değişikliği ve sonrasında doğrulama kayıtları |

Mevcut bilgilerle PLr, erişilen PL veya SIL değeri hesaplanmamıştır. Test sıcaklığı ve basıncı, emniyet eşiği olarak kullanılmaz.

## Kaynaklar

- [ISO 13577-1:2016](https://www.iso.org/standard/68019.html).
- [IEC 60519-1:2020](https://webstore.iec.ch/en/publication/61886).
- [ISO 12100:2010](https://www.iso.org/standard/51528.html).
- [ISO 13849-1:2023](https://www.iso.org/standard/73481.html).
- [IEC 62061:2021](https://webstore.iec.ch/en/publication/59927), [AMD1:2024](https://webstore.iec.ch/en/publication/71331), [AMD2:2026](https://webstore.iec.ch/en/publication/92835).
- [Tehlike tablosu](../03-Risk-Analizleri/ISO-12100/Tehlike-Tablosu.md).
- [LAB 1 — Emniyet fonksiyonları](../02-LAB-Foyleri/03-Proje-Vakum-Firini/LAB-01-Emniyet-Mimarisi.md).

## Sonuç

Fonksiyonel emniyet değerlendirmesi, siber müdahalenin SF1 ve SF2 üzerindeki etkisini görünür kılar. Güvenilirlik seviyesi hakkında sonuç verebilmek için risk, devre ve geçerleme bilgileri tamamlanmalıdır.
