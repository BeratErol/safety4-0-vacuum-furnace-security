# LAB 6 - VF-1D-A-696: CRA Olay Simülasyonu

**Çıktı:** Olay müdahale akışı (Incident Workflow), Evidence Pack EP 13 - Incident Response.

## Senaryo ve kavram

LAB 4’teki koşullu uzak bakım senaryosunda saat 10:15’te bir servis hesabında yetkisiz erişim saptanır. Fırın çalışırken kontrol yapılandırmasının değiştirilmiş olabileceği değerlendirilir. Uzak bağlantı ve servis hesabı bu simülasyonun varsayımlarıdır. Müdahaleyi vardiya sorumlusu başlatır.

**Kavram:** Güvenlik ihlali veya ihlal şüphesi bir olaydır. Önce emniyet sağlanır, ardından zaman damgalı kanıtlar korunur. Gereksiz sıfırlama veya yeniden başlatma geçici kayıtları silebilir.

## Görev - Zaman çizgisi

### 1. İlk 15 dakika (10:15-10:30)

OT/BT, bakım ve emniyet ekiplerini ararım. (1) Kapak çevresini boşaltıp prosesi prosedüre göre güvenli duruma alırım. (2) Gerekli soğutmayı aksatmadan şüpheli bakım erişimini sınırlarım. (3) Olay saatini, hesabı ve ilk kararları kaydederim.

### 2. İlk 2 saat - Emniyet, kanıt ve hesap

Bakım ve emniyet ekipleri, güvenli sıcaklık ve basınç doğrulanmadan erişimin engellendiğini (SF1) ve aşırı sıcaklıkta ısıtmanın sınırlandırılıp gerekli soğutmanın korunduğunu (SF2) kontrollü koşullarda doğrular. OT/BT şüpheli servis hesabını kapatır ve yapılandırma, SCADA ve erişim kayıtlarını korur.

### 3. İlk 24 saat - Erken uyarı

Tespit zamanı, etkilenen ürün ve biliniyorsa sürümü, yetkisiz erişimin özeti, olası etkiler ve ilk önlemler hazırlanır. Bildirim gerekiyorsa üreticiye gecikmeden iletilir.

### 4. İlk 72 saat - Ayrıntılı bildirim

OT/BT, bakım oturumunu ve yapılandırma farklarını inceleyerek giriş yolunu araştırır. Bakım ve emniyet ekipleri değişikliğin SF1/SF2 üzerindeki etkisini değerlendirir. Yönetim müdahaleyi takip eder. Bildirim gerekiyorsa üretici bilinen bulguları ve önlemleri iletir.

### 5. Föydeki 14. gün - Son rapor için kanıtlar

Servis hesabı ve bakım oturumları, SCADA alarm ve proses geçmişi, olay anındaki yapılandırma ve onaylı yedek, SF1/SF2 geçerleme ve vardiya kayıtları korunur. Kanıt kopyalarının kaynağı, alınma saati ve sorumlusu kaydedilir.

## CRA süre notu

14. gün föyün son rapor adımıdır. CRA kapsamında aktif olarak istismar edilen bir zafiyette 14 günlük süre, düzeltici veya azaltıcı önlemin kullanılabilir olmasından başlar. Bildirime tabi ciddi olayda son rapor, 72 saatlik bildirimin sunulmasından itibaren bir ay içinde verilir.

## Kaynaklar

- INSPECCO × KRIPTARIUM, Genel LAB Föyleri, LAB 6, PDF s. 7.
- Safety 4.0 Bootcamp Sunumu, PDF s. 23 ve 28-29.
- Kavramlar Sözlüğü, Olay ve Mevzuat, PDF s. 3.
- Avrupa Komisyonu, CRA bildirim yükümlülükleri. digital-strategy.ec.europa.eu/en/policies/cra-reporting

## Sonuç

Yeniden devreye alma kararı, güvenli erişim ve aşırı sıcaklık korumasının doğrulanmasına dayanır.
