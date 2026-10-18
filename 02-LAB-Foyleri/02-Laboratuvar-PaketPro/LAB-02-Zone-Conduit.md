# LAB 2 — PaketPro 3000: Zone / Conduit

**Çıktı:** Bölge ve bağlantı şeması (Zone / Conduit Diagram).

Föydeki varlıklar temel alınmış; bölgeleme ve erişim kararları öneri olarak hazırlanmıştır.

## Görev A — Varlıkları bölgelere ayırma

### 1. Hangi varlıklar aynı bölgede?

| Bölge | Varlıklar | Gerekçe |
|---|---|---|
| Üretim | Üretim PLC, HMI, motor sürücüleri | Paketleme işlemini ve makine hareketlerini yönetir. |
| Emniyet | Emniyet PLC’si | İnsan güvenliğiyle ilgili fonksiyonları yürütür. |
| Uzak erişim / DMZ | Uzak bakım modülü; önerilen jump server | Dış bakım bağlantısını kontrollü olarak sonlandırır. |
| Kablosuz erişim | Wi-Fi erişim noktası | Kablosuz bağlantıların üretim ağına doğrudan erişimini sınırlandırır. |
| Harici hizmet | Bulut telemetri | Makine dışındaki hizmete veri aktarımını temsil eder. |

İki kilitsiz USB, admin/admin servis hesabı, HMI’nin port 80 web arayüzü ve açıkta tutulan Wi-Fi parolası ayrı birer bölge değildir; ilgili varlıklara ait saldırı yüzeyleridir. Bulutun ayrı gösterilmesi, doğrudan erişim izni verildiği anlamına gelmez.

### 2. Açık uzak bakım modülü hangi bölgede olmalı? Orada kalabilir mi?

Uzak erişim / DMZ bölgesine yerleştirilebilir; ancak internete doğrudan açık ve kontrolsüz biçimde bırakılmamalıdır. Bağlantı yetkili, süreli ve kayıtlı olmalı; üretim ve emniyet bölgelerine geçiş sınırlandırılmalıdır.

### 3. Bölgeler arası geçişler nerede? Ne kontrol edilir?

| Geçiş (conduit) | Kontrol |
|---|---|
| İnternet → Uzak erişim / DMZ | VPN, MFA, kişisel hesap ve oturum kaydı. |
| Uzak erişim / DMZ → Üretim | İzin verilen hedef, protokol ve bakım işlemleri. |
| Üretim ↔ Emniyet | Yalnızca gerekli veri akışları; yetkisiz yapılandırma değişikliğinin engellenmesi. |
| Kablosuz erişim → Makine ağı | Kimlik doğrulama ve yalnızca gerekli hedeflere erişim. |
| Makine ağı → Bulut telemetri | Veri akışının amacı, yönü ve izinli hedefleri. |

Uzak bakımdan Safety PLC’ye doğrudan yapılandırma yolu önerilmez. USB kullanımı ve servis hesabı yetkileri ilgili cihazlarda ayrıca kontrol edilir.

## Görev B — Uzak erişim kararı

| Karar | Seçim ve nedeni |
|---|---|
| Aracı | Jump server: Makineye kontrollü bir ara nokta üzerinden erişilir. |
| Tünel | VPN: Bakım bağlantısı şifreli aktarılır. |
| Kimlik | MFA: Parolaya ek doğrulama istenir. |
| Hesap | Kişisel: İşlemler kullanıcıyla ilişkilendirilir. |
| Kayıt | Tam oturum kaydı: Bakım işlemleri incelenebilir. |
| Zamanlama | Varsayılan kapalı: Bağlantı yalnızca gerektiğinde süreli açılır. |

## Kaynaklar

- INSPECCO × KRIPTARIUM, PaketPro 3000 LAB Föyleri: PDF s. 3.
- Safety 4.0 Bootcamp Sunumu: PDF s. 9–14; PaketPro varlık örneği s. 12.
- Kavramlar Sözlüğü: zone, conduit ve uzak erişim terimleri.
