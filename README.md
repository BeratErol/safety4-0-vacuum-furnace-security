# Safety 4.0 — Vakum Fırını Siber Güvenlik ve Fonksiyonel Emniyet Analizi

**Sistem Teknik VF-1D-A-696 Vakum Sertleştirme Fırını**

Bu proje, Fırat Üniversitesi Yazılım Mühendisliği kapsamında yürütülen Safety 4.0 çalışmasıdır. Gerçek bir endüstriyel makine üzerinden siber güvenlik, fiziksel tehlikeler ve fonksiyonel emniyet arasındaki ilişki incelenmektedir.

| Alan | Bilgi |
|---|---|
| Hazırlayan | Berat Erol |
| Üniversite / Bölüm | Fırat Üniversitesi / Yazılım Mühendisliği |
| Üretici | Sistem Teknik Sanayi Fırınları A.Ş. |
| Makine | VF-1D-A-696 Vakum Sertleştirme Fırını |
| Yöntem | Kamuya açık kaynak araştırması ve eğitim amaçlı analiz |

## Projenin amacı

Makinenin çalışma sürecini ve belgelenmiş kontrol özelliklerini incelemek; olası siber müdahalelerin fiziksel sonuçlarını değerlendirmek ve gerekçeli risk azaltma önerileri geliştirmek amaçlanmaktadır.

Çalışma; makine tanıtımı, SWOT analizi, SMART hedefleri, Trello görev takibi, LAB uygulamaları, risk değerlendirmesi, standart ve CE incelemesi, Safety 4.0 hazırlık değerlendirmesi ve final raporunu kapsar.

## Makine ve belgelenmiş test bilgileri

VF-1D-A-696, vakum altında ısıl işlem ve gazla soğutma için kullanılan bir endüstriyel fırındır. Üreticinin NADCA test yayınlarında sıcaklık ve basınç verilerinin SCADA üzerinden izlendiği gösterilmektedir.

| Parametre | Yayımlanan test bilgisi |
|---|---|
| Test malzemesi | H13 / 1.2344 sıcak iş takım çeliği |
| Numune | 500 kg; 400 × 400 × 400 mm |
| Östenitleme sıcaklığı | 1030 °C |
| Soğutma gazı | Azot |
| Soğutma basıncı | 9. sayı makalesinde 8 bara |
| Fan devri | 2700 dev/dakika |
| İzleme | SCADA sıcaklık ve basınç kayıtları |

Kaynak: 9. sayı PDF s. 4 ve 6; NADCA posteri. Değerler test koşullarına aittir, makinenin çalışma sınırlarını belirtmez.

**Not:** Soğuma hızı yayınların bazı bölümlerinde farklı verilmiştir.

## Araştırma sınırları

- Yalnızca kamuya açık kaynaklar kullanılır; kurumlarla iletişim veya gerçek sistemlerde test yapılmaz.
- Doğrulanan bilgiler, varsayımlar ve öneriler ayrılır; diğer modellerin özellikleri fırına aktarılmaz.
- SCADA, uzaktan erişimin kanıtı değildir. Kontrol ve emniyet mimarisi belge olmadan kesinleştirilmez.
- Eksik belgeler uygunsuzluk kanıtı sayılmaz; çalışma resmi uygunluk değerlendirmesi değildir.
- Üçüncü taraf belgeleri paylaşım izni doğrulanmadan depoya yüklenmez.

## İncelenecek standartlar ve yaklaşımlar

ISO 12100, IEC 62443, ISO 13849-1, IEC 62061, ilgili CE gereksinimleri ve Safety 4.0 yaklaşımı incelenecektir. Güncel gereksinimler birincil kaynaklardan doğrulanacaktır.

## Planlanan depo yapısı

```text
README.md
01-Makine-Tanitimi/
02-LAB-Foyleri/
  01-Ders-Siseleme/
  02-Laboratuvar-PaketPro/
  03-Proje-Vakum-Firini/
03-Risk-Analizleri/
04-CE-ve-Standartlar/
05-SWOT-Analizi/
06-SMART-Hedefleri/
07-Trello/
08-Safety4-Hazirlik-Degerlendirmesi/
09-Final-Rapor/
```

## Kaynaklar

1. [Sistem Teknik — 9. sayı, NADCA testi teknik makalesi, arşiv PDF](https://web.archive.org/web/20240712231156id_/https://www.sistemteknik.com/ferrous/wp-content/uploads/2023/03/9-sistem-ic-1.pdf) — 44 sayfa; ilgili makale PDF s. 4–7 ve 9.
2. [Sistem Teknik — 10. sayı, tasarım standartlaştırma, arşiv PDF](https://web.archive.org/web/20240808052817id_/https://www.sistemteknik.com/ferrous/wp-content/uploads/2023/07/10-sistemteknik-internet.pdf) — 40 sayfa; ilgili makale PDF s. 4–5.
3. [Sistem Teknik — NADCA web makalesinin arşiv kaydı](https://web.archive.org/web/20241015124924/https://www.sistemteknik.com/ferrous/vf-1d-a-696-serisi-vakum-sertlestirme-firinlarinda-nadca-testi/).
4. [Alper Keleşoğlu — NADCA testi soğutma performansı ve enerji tüketimi konferans posteri](https://www.researchgate.net/publication/388276659_Cooling_Performance_and_Energy_Consumption_Analysis_of_NADCA_Test_on_VF-1D-A-696_Type_Vacuum_Furnace).
5. INSPECCO × KRIPTARIUM — Safety 4.0 Bootcamp sunumu, Kavramlar Sözlüğü ve LAB föyleri; ders materyalleri.

Erişim için arşiv bağlantıları kullanılmıştır. NADCA yayınları aynı teste dayanır; görselli HTML, bu kaynaklardan hazırlanan okuma kopyasıdır.
