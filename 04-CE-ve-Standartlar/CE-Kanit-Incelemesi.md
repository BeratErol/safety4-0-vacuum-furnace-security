# CE — Mevzuat ve Kanıt İncelemesi

## Analizin kapsamı

Fırının Türkiye’de piyasaya arzı ve AB pazarına sunulması için ilgili mevzuat, siber güvenlikle ilişkili emniyet gereksinimleri ve uygunluk kanıtları değerlendirilmiştir.

## Mevzuat çerçevesi

| Düzenleme | İncelemedeki yeri |
|---|---|
| Türkiye — Makina Emniyeti Yönetmeliği (2006/42/AT) | Geçiş dönemindeki makine çerçevesi; yeni yönetmeliğin Md. 51 ve geçici Md. 1 hükümleriyle birlikte değerlendirilir |
| Türkiye — Makine Emniyeti Yönetmeliği (2023/1230/AB) | 16 Ekim 2026 tarihli, 33402 sayılı Resmî Gazete’de yayımlandı. Md. 52’de sayılan hükümler yayımda, diğer hükümler 20 Ocak 2027’de yürürlüğe girer |
| AB — 2006/42/EC ve (AB) 2023/1230 | AB pazarında direktiften tüzüğe genel geçiş tarihi 20 Ocak 2027’dir |

Türkiye’de ulusal yönetmelik, AB pazarında ilgili AB düzenlemesi esas alınır. Yönetmelik adındaki AT/AB ifadeleri resmî adlandırmadır; Türkiye kapsamını dışlamaz. Uygulanacak hükümler, piyasaya arz/hizmete sunma tarihi ve varsa önemli değişiklik koşullarıyla belirlenir.

## Siber güvenlikle ilişki

AB Tüzüğü 2023/1230 Ek III 1.1.9, emniyetle ilgili yazılım/verinin bozulmaya karşı korunmasını ve müdahale/değişiklik kanıtlarını ele alır. Ek III 1.2.1 ise kontrol sistemlerinin tehlikeli durum oluşturmayacak güvenilirliğini, kötü niyetli müdahaleler dahil değerlendirir.

| Proje riski | İlgili inceleme | Beklenen kanıt |
|---|---|---|
| R01 — Operatör istasyonu | Emniyet parametrelerine yetkisiz müdahalenin engellenmesi | Yetki ve değişiklik kayıtları |
| R02 — Olası uzak bakım | Bağlı/uzak cihazların tehlikeli duruma yol açmaması | Erişim sınırları ve koruma doğrulaması |
| R03 — Yerel servis | Emniyet yazılımı ve yapılandırma değişikliklerinin korunması | Sürüm, bütünlük ve geçerleme kayıtları |

Türkiye’deki yeni yönetmelik de Ek-3 1.1.9 ve 1.2.1 hükümlerine atıf yapar. Eşleştirme, yeni çerçeveye yönelik proje değerlendirmesidir.

## Kanıt tablosu

| Belge / kayıt | Mevcut durum | İncelemedeki önemi |
|---|---|---|
| Modele ve ilgili makineye ait uygunluk beyanı | Erişilmedi | Ürün kimliği ve beyan edilen mevzuat/standartlar |
| Makine kimliği ve piyasaya arz bilgisi | Model biliniyor; ilgili makine/arz bilgisi yok | Hangi ürün ve mevzuatın inceleneceği |
| Üretici risk değerlendirmesi | Erişilmedi | Tehlikeler ve risk azaltma kararları |
| Teknik dosya ve devre şemaları | Erişilmedi | Kontrol ve emniyet tasarımının kanıtı |
| Kullanım/bakım talimatları | Erişilmedi | Güvenli kullanım, sınırlar ve kalan riskler |
| Emniyet fonksiyonlarının geçerleme kayıtları | Erişilmedi | SF1/SF2 karşılığı korumaların davranışı |
| Siber erişim ve değişiklik kayıtları | Erişilmedi | Yetkisiz müdahale ve yapılandırma korunması |
| NADCA test yayını | Mevcut | Deney performansını destekler; CE uygunluk beyanı yerine geçmez |

Erişilemeyen belgeler, üreticide bulunmadığı veya makinenin uygunsuz olduğu şeklinde yorumlanmaz.

## Diğer kapsam kontrolleri

Türkiye’de Elektromanyetik Uyumluluk Yönetmeliği (2014/30/AB) ve Basınçlı Ekipmanlar Yönetmeliği (2014/68/AB); AB pazarında karşılık gelen EMC/PED düzenlemeleri, ürün ve ekipman sınıflandırmasına göre ayrıca incelenir. NADCA deneyindeki 8 bara değeri; izin verilen azami basınç, hacim, sınıflandırma ve istisnalar bilinmeden tek başına PED kararı verdirmez.

IEC/ISO standardının kullanılması tek başına CE uygunluğunu göstermez. Uyumlaştırılmış standardın uygunluk varsayımı, ilgili mevzuatın kapsanan gereksinimleri ve resmî yayımlanan referansıyla sınırlıdır.

## Kaynaklar

- [Resmî Gazete — Makine Emniyeti Yönetmeliği (2023/1230/AB), Md. 21, 51, 52 ve geçici Md. 1](https://www.resmigazete.gov.tr/eskiler/2026/10/20261016-12.htm).
- [Ticaret Bakanlığı — Makinalar ve 2006/42/AT çerçevesi](https://urunkurallari.ticaret.gov.tr/tr/sektorel-rehber/makinalar).
- [Ticaret Bakanlığı — Elektromanyetik uyumluluk](https://urunkurallari.ticaret.gov.tr/tr/sektorel-rehber/elektrikli-materyaller).
- [Türk Loydu — Basınçlı Ekipmanlar Yönetmeliği kapsamı](https://www.turkloydu.org/hizmetlerimiz/endustri/belgelendirme/urun-belgelendirme/basincli-ekipmanlarin-belgelendirmesi/).

- [Avrupa Komisyonu — Machinery ve geçiş çerçevesi](https://single-market-economy.ec.europa.eu/sectors/mechanical-engineering/machinery_en).
- [2006/42/EC — Md. 5; Ek II ve Ek VII](https://eur-lex.europa.eu/eli/dir/2006/42/oj/eng).
- [2023/1230 — Güncel derlenmiş metin; Md. 54, Ek III 1.1.9 ve 1.2.1](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:02023R1230-20260727).
- [Siber risk kaydı](../03-Risk-Analizleri/Siber-Guvenlik/Risk-Kaydi.md).

## Sonuç

İnceleme, CE açısından teknik dosya, risk değerlendirmesi ve emniyet kanıtlarının önemini ortaya koymaktadır. Siber güvenlik odağı, emniyet yazılımı ve parametrelerinin korunmasıdır; mevcut kamuya açık bilgilerle modele uygunluk kararı verilmemiştir.
