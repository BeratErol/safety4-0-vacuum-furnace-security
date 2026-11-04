# LAB 6 - Şişeleme Hattı: CRA Olay Simülasyonu

**Çıktı:** Olay müdahale akışı (Incident Workflow), Evidence Pack EP 13 - Incident Response.

## Senaryo ve kavram

Saat 10:15’te servis hesabında yetkisiz erişim tespit edilir. PLC yapılandırması değişmiş olabilir ve hat çalışmaktadır. Müdahaleyi vardiya sorumlusu başlatır.

**Kavram:** Güvenlik ihlali veya ihlal şüphesi bir olaydır. Önce emniyet sağlanır, ardından zaman damgalı kanıtlar korunur. Gereksiz sıfırlama veya yeniden başlatma geçici kayıtları silebilir.

## Görev - Zaman çizgisi

### 1. İlk 15 dakika (10:15-10:30)

OT/BT, bakım ve emniyet ekiplerini ararım. (1) Çalışanları tehlikeli bölgeden uzaklaştırıp hattı prosedüre göre güvenli duruma alırım. (2) Şüpheli uzak erişimi sınırlarım. (3) Tespit saatini, hesabı ve ilk kararları kaydederim.

### 2. İlk 2 saat - Emniyet, kanıt ve hesap

Bakım ve emniyet ekipleri acil durdurma ve koruyucu kilitleri doğrular. Emniyet teyit edilmeden hat başlatılmaz. OT/BT şüpheli servis hesabını kapatır, oturumlarını sonlandırır ve PLC yapılandırması ile erişim kayıtlarını korur.

### 3. İlk 24 saat - Erken uyarı

Tespit zamanı, etkilenen ürün ve biliniyorsa sürümü, yetkisiz erişimin özeti, olası etkiler ve ilk önlemler hazırlanır. Bildirim gerekiyorsa üreticiye gecikmeden iletilir.

### 4. İlk 72 saat - Ayrıntılı bildirim

Sunumdaki görev dağılımına göre OT ve BT incelemeyi yürütür, bakım ve emniyet ekiplerinin görüşü alınır. Yönetim müdahaleden nihai olarak sorumludur. Üretici, gerekiyorsa bilinen kök nedeni, etkiyi ve alınan önlemleri bildirir. Kesinleşmeyen bulguları ayrıca belirtir.

### 5. Föydeki 14. gün - Son rapor için kanıtlar

PLC değişiklik kayıtları, olay anındaki yapılandırma ve onaylı yedek, HMI alarmları, servis hesabı ve uzak erişim kayıtları, emniyet testleri ve vardiya kayıtları korunur. Kopyaların kim tarafından ve ne zaman alındığı kaydedilir.

## CRA süre notu

14. gün föyün son rapor adımıdır. CRA kapsamında aktif olarak istismar edilen bir zafiyette 14 günlük süre, düzeltici veya azaltıcı önlemin kullanılabilir olmasından başlar. Bildirime tabi ciddi olayda son rapor, 72 saatlik bildirimin sunulmasından itibaren bir ay içinde verilir.

## Kaynaklar

- INSPECCO × KRIPTARIUM, Genel LAB Föyleri, LAB 6, PDF s. 7.
- Safety 4.0 Bootcamp Sunumu, PDF s. 23 ve 28-29.
- Kavramlar Sözlüğü, Olay ve Mevzuat, PDF s. 3.
- Avrupa Komisyonu, CRA bildirim yükümlülükleri. digital-strategy.ec.europa.eu/en/policies/cra-reporting
