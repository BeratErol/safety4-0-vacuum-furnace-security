# LAB 2 — VF-1D-A-696: Zone / Conduit

**Çıktı:** Önerilen bölge ve bağlantı şeması (Zone / Conduit Diagram).

SCADA, proses kontrolü, emniyet ve bakım işlevleri bölgelere ayrılmış; bölgeler arasındaki veri akışları ve erişim kontrolleri değerlendirilmiştir. [Teknik bilgi temeli](../../01-Makine-Tanitimi/Teknik-Ozellikler/Teknik-Ozellikler.md)

## Görev A — Varlıkları bölgelere ayırma

### 1. Hangi varlıklar aynı bölgede?

| Bölge | Varlık / işlev | Bilgi durumu |
|---|---|---|
| Proses kontrol | Sıcaklık ve basınç ölçümü; ısıtma, vakum ve fan kontrolü | İşlevler belgelenmiş; cihaz ve bağlantı ayrıntıları bilinmiyor. |
| İzleme / Operasyon | SCADA ve operatör kontrol işlevi | SCADA belgelenmiş; ayrı HMI donanımı doğrulanmadı. |
| Emniyet | LAB 1’de önerilen SF1/SF2 algılama ve kontrol işlevleri | Öneri; gerçek emniyet donanımı doğrulanmadı. |
| Mühendislik | Yetkili bakım / yapılandırma istasyonu | Analiz varsayımı. |
| Uzak erişim / DMZ | Koşullu uzak bakım ve ara sunucu | Yalnızca uzaktan bakım varsa önerilir. |

Ofis ağıyla bağlantı da doğrulanmamıştır; böyle bir bağlantı gerekiyorsa ayrı bir sınırda değerlendirilir.

### 2. Safety PLC hangi bölgeye konulmalı ve neden?

Safety PLC veya başka bir emniyet denetleyicisi varsa emniyet bölgesinde değerlendirilmelidir. Amaç, proses veya SCADA erişiminin emniyet yapılandırmasına serbest geçiş sağlamamasıdır. Bu öneri, fırında Safety PLC bulunduğu anlamına gelmez.

### 3. Bölgeler arası geçişler nerede? Ne kontrol edilir?

| Önerilen geçiş (conduit) | Kontrol |
|---|---|
| SCADA / Operasyon ↔ Proses | İzinli ölçüm, komut ve reçete akışları; kullanıcı yetkileri. |
| Mühendislik → Proses | Yetkili değişiklik, hedef cihaz sınırı ve işlem kaydı. |
| Mühendislik → Emniyet | Ayrı yetki ve onay; emniyet yapılandırmasına kısıtlı erişim. |
| Uzak bakım → DMZ → Yetkili bakım hedefi | Bağlantı varsa MFA, VPN, kişisel hesap ve süreli izin. |
| Emniyet → İzleme | Gerektiğinde durum bilgisi; izleme hesabıyla emniyet parametresi yazılamaması. |

Bunlar izin verilmesi değerlendirilen akışlardır; mevcut kablolama veya ağ tespiti değildir. Uzak bakımın emniyet bölgesine doğrudan yazma erişimi öngörülmez.

## Görev B — Uzak erişim kararı

Modele özel uzaktan erişim doğrulanmamıştır. Aşağıdaki seçimler, böyle bir erişim kurulacaksa geçerlidir.

| Karar | Seçim ve nedeni |
|---|---|
| Aracı | Jump server: Yetkili bakım hedeflerine kontrollü geçiş sağlar. |
| Tünel | VPN: Bakım trafiğini şifreler. |
| Kimlik | MFA: Hesabın ele geçirilmesine karşı ek doğrulama sağlar. |
| Hesap | Kişisel: İşlemleri kullanıcıyla ilişkilendirir. |
| Kayıt | Oturum kaydı: Yapılan bakım işlemlerini izlenebilir kılar. |
| Zamanlama | Varsayılan kapalı: Erişim gerektiğinde onaylı ve süreli açılır. |

## Kaynaklar

- [K1 ve K4 — SCADA ve proses bilgileri](../../01-Makine-Tanitimi/Kaynaklar.md).
- Genel LAB Föyleri, PDF s. 3; Bootcamp Sunumu, PDF s. 9–14.
- [IEC — IEC 62443 genel çerçevesi](https://syc-se.iec.ch/deliveries/cybersecurity-guidelines/security-standards-and-best-practices/iec-62443/).
- [NIST SP 800-82 Rev. 3 — OT Security](https://csrc.nist.gov/pubs/sp/800/82/r3/final).

## Sonuç

Bölgeleme analizi, proses ve emniyet işlevlerine erişimin ayrı kontrol edilmesini öne çıkarmaktadır. Bakım bağlantıları yetkili hedeflerle sınırlandırılmalı ve gerektiğinde süreli açılmalıdır.
