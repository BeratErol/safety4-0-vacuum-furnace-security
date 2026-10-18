# VF-1D-A-696 — Tehlike Tablosu

## Analizin kapsamı

Fırının ısıl işlem, gazla soğutma, yükleme/boşaltma ve bakım aşamalarındaki olası fiziksel tehlikeler incelenmiştir. Proses bilgileri NADCA yayınlarına; koruma önerileri proje analizine dayanır.

ISO 12100, tehlike belirleme ve risk azaltma için yöntem çerçevesidir. Bu tabloda tehlikeler belirlenmiş; maruziyet sıklığı, kaçınma imkânı ve gerçek koruma bilgileri bulunmadığından sayısal emniyet riski hesabı yapılmamıştır.

## Tehlikeli durumlar

| Kod | Tehlikeli durum | Fiziksel sonuç / etkilenen kişi | Bilgi temeli |
|---|---|---|---|
| T01 | Sıcak yük veya yüzeye erişim; kontrolsüz aşırı ısınma | Operatör/bakım personelinde ağır yanık; aşırı ısınmada yangın olasılığı | K1: 1030 °C test sıcaklığı. Erişim ve yangın zinciri analiz koşuludur. |
| T02 | Güvenli basınç dengesi sağlanmadan kapağa erişim | Kapak çevresindeki kişide basınç ve mekanik etkiyle ağır yaralanma | K1: vakum ve 8 bara azotla soğutma. Kapak kontrol yapısı bilinmiyor. |
| T03 | Azot kaçağının yetersiz havalandırılan ortamda birikmesi | Yakındaki çalışanlarda oksijen yetersizliği / boğulma | K1: azot kullanımı. Kaçak ve ortam koşulları varsayım; HSE genel gaz tehlikesini açıklar. |
| T04 | Yükün taşınması sırasında düşme veya sıkışma | Operatör/taşıma personelinde ezilme ve sıkışma | K1: 500 kg numune. Gerçek taşıma sistemi ve yöntemi bilinmiyor. |
| T05 | Bakım sırasında tehlikeli elektrik enerjisine erişim | Bakım personelinde elektrik çarpması ve yanık | K1: rezistans ve elektrik tüketimi bilgisi. Pano ve izolasyon ayrıntıları bilinmiyor. |

Değerler belirli bir NADCA deneyine aittir; güvenli çalışma eşikleri olarak kullanılmaz.

## Koruma önerileri ve kanıt ihtiyacı

| Kod | İncelenecek koruma | Gereken kanıt |
|---|---|---|
| T01 | SF1 güvenli erişim, SF2 aşırı sıcaklık koruması ve gerekli soğutmanın korunması | Eşikler, sensörler, bağımsız koruma ve duruş/soğutma mantığı |
| T02 | Basınç durumunu güvenilir doğrulayan erişim kilitlemesi | Kilitleme mantığı, arıza davranışı ve basınç doğrulama kayıtları |
| T03 | Kaçak önleme, yeterli havalandırma; risk gerektiriyorsa oksijen izleme | Gaz tesisatı, havalandırma değerlendirmesi ve varsa alarm kayıtları |
| T04 | Yüke uygun taşıma sistemi ve güvenli yükleme alanı | Taşıma ekipmanı kapasitesi, yükleme düzeni ve bakım/kontrol kayıtları |
| T05 | Bakım için uygun enerji izolasyonu ve artık enerjinin değerlendirilmesi | Elektrik şeması, izolasyon düzeni ve bakım prosedürü |

SF1 ve SF2, [LAB 1’deki emniyet fonksiyonu önerileridir](../../02-LAB-Foyleri/03-Proje-Vakum-Firini/LAB-01-Emniyet-Mimarisi.md). Her koruma için tasarım, teknik koruyucu önlem ve kullanım bilgisi birlikte değerlendirilmelidir.

## Siber risklerle ilişki

- T01: R01 operatör istasyonu ve R02 olası uzak bakım senaryoları.
- T02: R03 yerel mühendislik senaryosu.
- T03–T05: Bu çalışmada ayrı siber saldırı zinciri kurulmamıştır; fiziksel tehlike tablosunda tutulur.

İlgili kayıtlar: [Siber risk kaydı](../Siber-Guvenlik/Risk-Kaydi.md).

## Kaynaklar

- [K1 ve K4 — NADCA test yayınları](../../01-Makine-Tanitimi/Kaynaklar.md): sıcaklık, basınç, gaz, yük ve enerji bilgileri.
- [ISO 12100:2010 — Resmi standart özeti](https://www.iso.org/standard/51528.html).
- [HSE — The safe isolation of plant and equipment, HSG253](https://www.hse.gov.uk/pubns/priced/hsg253.pdf): izolasyon ve artık enerji için genel başvuru.
- [HSE — Inerting](https://www.hse.gov.uk/comah/sragtech/techmeasinerting.htm): azot ve oksijen yetersizliği için genel başvuru.

## Sonuç

İnceleme, sıcaklık ve basınç kaynaklı erişim tehlikelerinin yanında azot, yük taşıma ve elektrik enerjisini de kapsamaktadır. Koruma önerilerinin değerlendirilmesi için gerçek emniyet devreleri ve işletme koşullarına ait kanıtlar gereklidir.
