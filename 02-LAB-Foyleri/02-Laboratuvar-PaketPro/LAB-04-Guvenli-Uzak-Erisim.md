# LAB 4 - PaketPro 3000: Güvenli Uzak Erişim

**Çıktı:** Güvenli erişim mimarisi (Secure Architecture).

## Görev A - Mevcut erişim

İnternet → Doğrudan erişime açık uzak bakım modülü → PLC/HMI.

Uzak bakım modülünün doğrudan internete açık olması, yetkisiz erişim ve makine kontrolüne müdahale riski oluşturur.

## Görev A - Hedef erişim (5 ilke)

1. **Jump server:** Uzak erişim doğrudan değil, güvenli bir ara sunucu üzerinden sağlanmalıdır.
2. **VPN:** Bağlantılar şifreli VPN üzerinden gerçekleştirilmelidir.
3. **MFA:** Kişisel kullanıcı hesapları ve çok faktörlü kimlik doğrulama kullanılmalıdır.
4. **Oturum kaydı:** Bütün uzaktan erişim işlemleri kaydedilmelidir.
5. **Varsayılan kapalı:** Uzak erişim yalnızca ihtiyaç halinde, belirli süreyle açılmalıdır.

## Görev B - Functional Safety Köprüsü

### 1. Saldırgan tüm önlemlere rağmen içeri girerse emniyet fonksiyonu etkilenir mi? Neden?

Emniyet fonksiyonu, normal kontrol sisteminden bağımsız tasarlanmışsa etkilenmemelidir. Ancak saldırgan Safety PLC'ye veya emniyet parametrelerine müdahale edebiliyorsa ışık perdesi ve durdurma fonksiyonları tehlikeye girebilir.

### 2. Işık perdesi zincirinin uzak bakım yolundan etkilenmemesi için gereksinimi yazın (çözümü değil).

Uzak bakım erişimi, ışık perdesi → Safety PLC → STO/kontaktör emniyet zincirinin çalışmasını değiştirememeli, devre dışı bırakamamalı veya geciktirememelidir. Yetkisiz erişim gerçekleşse bile emniyet fonksiyonu bağımsız ve güvenilir şekilde çalışmaya devam etmelidir.

## Kaynaklar

- INSPECCO × KRIPTARIUM, PaketPro 3000 LAB Föyleri: LAB 4, PDF s. 5.
- Safety 4.0 Bootcamp Sunumu: LAB 4, PDF s. 20.
- Kavramlar Sözlüğü: Güvenli Erişim (LAB 4), PDF s. 2.
