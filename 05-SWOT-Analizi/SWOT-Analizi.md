# SWOT Analizi

## Kapsam

Bu analiz, VF-1D-A-696 üzerine yürütülen Safety 4.0 projesini değerlendirir. Üreticinin ticari durumuna veya makinenin sertifikasyonuna ilişkin bir değerlendirme değildir.

## Güçlü yönler (Strengths)

| Kod | Güçlü yön | Projeye katkısı |
|---|---|---|
| G1 | Belirli ve gerçek bir makine modelinin seçilmiş olması | Araştırma ve senaryoların somut bir sistem üzerinde kurulmasını sağlar. |
| G2 | Üreticinin test reçetesi, SCADA grafikleri ve deney sonuçlarının bulunması | Teknik tanıtımın belgelenmiş verilere dayanmasını sağlar. [K1, K4](../01-Makine-Tanitimi/Kaynaklar.md) |
| G3 | Isıtma, vakum ve gazla soğutma süreçlerinin birlikte incelenebilmesi | Kontrol sistemleri ile fiziksel sonuçlar arasındaki ilişkiyi ele almaya uygundur. [K1](../01-Makine-Tanitimi/Kaynaklar.md) |
| G4 | GitHub üzerinden sürüm kontrollü dokümantasyon yürütülmesi | Değişikliklerin izlenmesini ve çıktıların düzenli tutulmasını sağlar. |

## Zayıf yönler (Weaknesses)

| Kod | Zayıf yön | Projeye etkisi |
|---|---|---|
| Z1 | PLC modeli, ağ topolojisi ve emniyet devrelerinin doğrulanmamış olması | Mimari ve tehdit analizlerinin bazı bölümleri varsayımlara dayanır. |
| Z2 | Çalışmanın kamuya açık belgelerle sınırlı olması | Gerçek kurulumun davranışı ve önerilerin etkinliği sahada doğrulanamaz. |
| Z3 | Temel NADCA yayınlarının aynı test verilerine dayanması | Kaynak sayısı, bağımsız deney sayısını temsil etmez. |
| Z4 | Fırına özgü LAB, SMART ve görev takibi çıktılarının henüz tamamlanmamış olması | Bulguların ölçülebilir bir çalışma planına dönüştürülmesi gerekir. |

Teknik bilgi eksikleri [teknik özellikler belgesinde](../01-Makine-Tanitimi/Teknik-Ozellikler/Teknik-Ozellikler.md) belirtilmiştir.

## Fırsatlar (Opportunities)

| Kod | Fırsat | Nasıl değerlendirilebilir? |
|---|---|---|
| F1 | Bootcamp föyleri, sunumu ve örnek çalışmaların sağladığı yöntem | Şişeleme ve PaketPro çalışmalarındaki yöntemler fırına özgü cevaplara dönüştürülebilir. |
| F2 | ISO 12100 ve IEC 62443 gibi başvuru çerçeveleri | Fiziksel tehlikeler ile siber erişim yolları birlikte ve sistematik olarak incelenebilir. |
| F3 | Arşivlerde korunmuş teknik yayınlar | Eski site bağlantılarına bağlı kalmadan kaynakların izlenebilirliği korunabilir. |
| F4 | Haftalık LAB düzeni ve öğretim elemanı geri bildirimi | Belgeler aşamalı olarak geliştirilip önceki analizler gözden geçirilebilir. |

## Tehditler (Threats)

| Kod | Tehdit | Projeye etkisi |
|---|---|---|
| T1 | Harici kaynak bağlantılarının değişmesi veya erişilememesi | Kaynakların tekrar incelenmesini zorlaştırabilir. |
| T2 | Yayınlardaki farklı değerler ve modele özgü ayrıntıların sınırlı olması | Teknik yorumlarda belirsizliğe yol açabilir. |
| T3 | Üçüncü taraf belgelerinin paylaşım izinlerinin belirsiz olması | PDF ve görsellerin depoda paylaşılmasını sınırlayabilir. |
| T4 | Mevzuat ve standart gereksinimlerinin zaman içinde değişmesi | Güncel olmayan bilgiye dayalı değerlendirme yapılmasına neden olabilir. |

Bu tehditler projenin yürütülmesine ilişkindir. Makineye yönelik saldırı senaryoları LAB 3 ve risk analizlerinde ayrıca ele alınacaktır.

## SWOT’tan çıkan aksiyonlar

| İlişki | Aksiyon | Beklenen çıktı |
|---|---|---|
| G2 + F1 | Belgelenen teknik bilgilerle tüm LAB föylerini fırına uyarlamak | Makineye uyarlanmış LAB cevapları, şemalar ve değerlendirmeler |
| G4 + T1 | Kaynak künyelerini, ilgili sayfaları ve arşiv bağlantılarını sürüm kontrollü tutmak | İzlenebilir kaynak envanteri |
| Z1 + F1 | Her LAB’da doğrulanan bilgi, varsayım ve öneriyi ayırmak | Açık varsayım listesi ve kaynaklı cevaplar |
| Z4 + F4 | Hedefleri ölçüt ve takvime bağlayıp görev kartlarına dönüştürmek | SMART hedefleri ve Trello görevleri |
| Z3 + T2 | Aynı teste dayanan yayınları birlikte değerlendirmek ve farklı yazılan değerleri belirtmek | Kaynaklara uygun teknik yorum |
| G4 + T3 | Paylaşım izni netleşmeyen belgeler için bağlantı ve özgün özet kullanmak | Üçüncü taraf dosyaları içermeyen dokümantasyon |
| Z2 + T4 | Güncel birincil kaynakları inceleyip sonuçları eğitim çalışmasının sınırları içinde sunmak | Kaynaklı standart incelemesi ve sınırlılık notları |

## Kaynaklar

- [Makine tanıtımı](../01-Makine-Tanitimi/Makine-Tanitimi.md)
- [Teknik özellikler ve bilgi eksikleri](../01-Makine-Tanitimi/Teknik-Ozellikler/Teknik-Ozellikler.md)
- [Teknik yayın envanteri](../01-Makine-Tanitimi/Kaynaklar.md)
- Safety 4.0 Bootcamp sunumu, Kavramlar Sözlüğü ve LAB föyleri: çalışma yöntemi için kullanılan ders materyalleri.

SWOT maddeleri, bu kaynaklar ve projenin mevcut kapsamı üzerinden yapılan proje değerlendirmeleridir.
