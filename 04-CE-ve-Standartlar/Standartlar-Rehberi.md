# ISO ve IEC Standartları Rehberi

Bu rehber, projede başvurulan standartların amaçlarını ve VF-1D-A-696 analizleriyle ilişkilerini özetler. Türkçe başlıklar açıklama amacıyla verilmiştir; bağlantılar resmî yayın sayfalarına gider.

## Siber güvenlik

| Standart | Amaç ve projeyle ilişkisi | Resmî erişim |
|---|---|---|
| IEC 62443-3-2:2020 — Sistem tasarımında güvenlik risk değerlendirmesi | Endüstriyel kontrol sistemini bölge ve bağlantılara ayırarak riskleri ve hedef güvenlik seviyesini ele alır. LAB 2 mimarisi ile R01–R03 senaryolarının değerlendirilmesine temel sağlar. | [IEC](https://webstore.iec.ch/en/publication/30727) |
| IEC 62443-3-3:2013 — Sistem güvenlik gereksinimleri ve güvenlik seviyeleri | Kimlik doğrulama, yetki, bütünlük, veri akışı ve kullanılabilirlik gibi sistem kontrollerini ele alır. Emniyet parametrelerine yetkisiz erişim ve değişiklik riskleriyle ilişkilendirilir. | [IEC](https://webstore.iec.ch/en/publication/7033) |

İlgili belge: [IEC 62443 — Siber güvenlik incelemesi](IEC-62443-Siber-Guvenlik.md).

## Makine ve fonksiyonel emniyet

| Standart | Amaç ve projeyle ilişkisi | Resmî erişim |
|---|---|---|
| ISO 12100:2010 — Makine emniyeti, risk değerlendirmesi ve risk azaltma | Tehlikelerin belirlenmesi ve risk azaltma kararlarının düzenlenmesi için genel yöntem sağlar. T01–T05 tehlike tablosunda kullanılır. | [ISO](https://www.iso.org/standard/51528.html) |
| ISO 13849-1:2023 — Kontrol sistemlerinin emniyetle ilgili bölümleri | Emniyet işlevlerini gerçekleştiren kontrol bölümlerinin tasarım ve entegrasyonunu ele alır. SF1 güvenli erişim ve SF2 aşırı sıcaklık koruması için performans gereksinimlerinin değerlendirilmesiyle ilişkilidir. | [ISO](https://www.iso.org/standard/73481.html) |
| IEC 62061:2021 — Makine kontrol sistemlerinin fonksiyonel emniyeti | Emniyet kontrol sistemlerinin tasarımı, entegrasyonu ve geçerlenmesini ele alır. SF1/SF2 için güvenilirlik ve doğrulama kanıtlarının incelenmesine başvuru sağlar. AMD1:2024 ve AMD2:2026 değişiklikleri de dikkate alınır. | [IEC](https://webstore.iec.ch/en/publication/59927), [AMD1](https://webstore.iec.ch/en/publication/71331), [AMD2](https://webstore.iec.ch/en/publication/92835) |

İlgili belgeler: [ISO 12100 ve fonksiyonel emniyet](ISO-12100-ve-Fonksiyonel-Emniyet.md), [tehlike tablosu](../03-Risk-Analizleri/ISO-12100/Tehlike-Tablosu.md).

## Fırına özgü emniyet

| Standart | Amaç ve projeyle ilişkisi | Resmî erişim |
|---|---|---|
| ISO 13577-1:2016 — Endüstriyel fırınlar ve ilgili işlem ekipmanlarında genel emniyet | Fırının işletme, bakım ve öngörülebilir arıza koşullarındaki tehlikelerini ele alan genel çerçevedir. Fiziksel tehlike analizinin fırına özgü gereksinimlerle tamamlanmasına yardımcı olur. | [ISO](https://www.iso.org/standard/68019.html) |
| IEC 60519-1:2020 — Elektrikli ısıtma ve elektromanyetik işlem tesislerinde genel emniyet | Endüstriyel elektrikli ısıtma ekipmanlarının emniyetini ele alır. Isıtma yöntemi ve ekipman sınırları doğrultusunda elektrik ve sıcaklık tehlikeleri için incelenir. | [IEC](https://webstore.iec.ch/en/publication/61886) |

İlgili belge: [ISO 12100 ve fonksiyonel emniyet — Fırına özgü kapsam](ISO-12100-ve-Fonksiyonel-Emniyet.md#fırına-özgü-kapsam).

## Kullanım notu

Rehber, resmî kapsam açıklamalarına dayalı proje özetidir. Standartların tam metinleri yerine resmî erişim bağlantıları verilmiştir. ISO 13849-1 ve IEC 62061 değerlendirme yolları, sistemin kapsamına göre seçilir; tüm standartlar her bileşene birlikte uygulanmış sayılmaz. PL/SIL ile IEC 62443 güvenlik seviyesi farklı kavramlardır.

Standart referansı tek başına CE uygunluğunu göstermez. Mevzuat ve kanıt ilişkisi [CE incelemesinde](CE-Kanit-Incelemesi.md) açıklanmıştır.

## Sonuç

IEC 62443 siber erişim ve müdahale risklerini, ISO 12100 fiziksel tehlikeleri, fonksiyonel emniyet ve fırın standartları ise koruyucu işlevlerin teknik değerlendirmesini destekler. Projede bu çerçeveler, siber zafiyetlerin makine emniyetine etkisini birlikte incelemek için kullanılır.
