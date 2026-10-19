# LAB 4 - Şişeleme Hattı: Güvenli Uzak Erişim

**Çıktı:** Güvenli erişim mimarisi (Secure Architecture); Evidence Pack EP 02 ve EP 06 ile ilişkilidir.

Şişeleme hattında uzak erişim riskleri, erişim güvenliği ve emniyet bağımsızlığı açısından değerlendirilmiştir. Çalışma, mevcut erişim örneğini beş ilkeyle iyileştirir ve kontrol sistemi ele geçirilse bile korunması gereken emniyet gereksinimini tanımlar.

## Görev A - Mevcut erişim

Makineye doğrudan internet erişimi vardır; paylaşılan hesap kullanılır, MFA ve oturum kaydı bulunmaz, uzak erişim sürekli açıktır.

Bu, ders örneğindeki savunmasız erişim senaryosudur. Ortak hesap ve ikinci doğrulamanın olmaması yetkisiz erişimi kolaylaştırır. Kayıt bulunmadığında kimin bağlandığı ve hangi işlemleri yaptığı izlenemez.

## Görev A - Hedef erişim

Uzak kullanıcı → VPN ve MFA ile doğrulanan erişim → Jump server → İzin verilen bakım bağlantısı → Makine.

| İlke | Hedefteki karşılığı |
|---|---|
| Ara nokta (jump server) | Makineye doğrudan internet erişimi yerine kontrollü ara sunucu üzerinden bağlantı sağlanır. |
| Kişisel hesap | Her kullanıcı kendi hesabıyla bağlanır; işlemler ilgili kişiyle ilişkilendirilir. |
| MFA | Parolaya ek ikinci kimlik doğrulama faktörü kullanılır. |
| Varsayılan kapalı | Erişim yalnızca bakım gerektiğinde, onaylı ve süreli olarak açılır; iş bitince kapatılır. |
| Oturum kaydı | Kimin, ne zaman bağlandığı ve yaptığı işlemler kaydedilir. |

VPN, bağlantının şifreli taşınmasını destekler. Ara sunucudan yalnızca gerekli bakım hedeflerine ve işlemlerine erişim verilmelidir.

## Görev B - Emniyet fonksiyonu etkilenir mi?

Evet, emniyet sistemi yeterince bağımsız ve korumalı değilse etkilenebilir. Saldırgan, üretim PLC'si veya IPC üzerinden Safety PLC yapılandırmasına ulaşabiliyorsa acil durdurma işlevini bozabilir. Bu durumda şişeleme hattının tehlikeli hareketi durmayabilir ve çalışan yaralanabilir.

Bu nedenle erişimi zorlaştırmakla birlikte, üretim sistemindeki bir ihlalin emniyet fonksiyonunu bozmasını da önlemek gerekir.

## Görev B - Bağımsızlık gereksinimi

Emniyet fonksiyonu, üretim kontrol sistemi ve uzak erişim altyapısındaki arıza veya ele geçirilmeden etkilenmeden görevini yerine getirmelidir. Böyle bir durumda acil durdurma ve diğer koruyucu işlevler kullanılabilir kalmalı; hat gerektiğinde tanımlanan güvenli duruma geçebilmelidir.

Bu ifade bir gereksinimdir; belirli bir cihaz veya ürün seçimi değildir.

## Kaynaklar

- INSPECCO × KRIPTARIUM, Genel LAB Föyleri: LAB 4, PDF s. 5.
- Safety 4.0 Bootcamp Sunumu: LAB 4 görseli, PDF s. 20.
- Kavramlar Sözlüğü: Güvenli Erişim (LAB 4), PDF s. 2.
