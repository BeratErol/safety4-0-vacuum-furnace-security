# LAB 6 - PaketPro 3000: CRA Olay Simülasyonu

**Çıktı:** Olay müdahale akışı (Incident Workflow), Evidence Pack EP 13 - Incident Response.

## Senaryo ve kavram

Saat 10:15’te servis hesabına gece 03:00’te tanınmayan bir konumdan girildiği fark edilir. PLC yapılandırması değişmiş olabilir. Işık perdesi parametreleri henüz doğrulanmamıştır ve makine çalışmaktadır. Müdahaleyi vardiya sorumlusu başlatır.

**Kavram:** Güvenlik ihlali veya ihlal şüphesi bir olaydır. Önce emniyet sağlanır, ardından zaman damgalı kanıtlar korunur. Gereksiz sıfırlama veya yeniden başlatma geçici kayıtları silebilir.

## Görev - Zaman çizgisi

### 1. İlk 15 dakika (10:15-10:30)

OT/BT, bakım ve emniyet ekiplerini ararım. (1) Çalışanları çene ve bıçak bölgesinden uzaklaştırıp makineyi güvenli duruma alırım. (2) Şüpheli uzak oturumu keserim. (3) 03:00 girişini ve 10:15 tespitini olay kaydına işlerim.

### 2. İlk 2 saat - Egzoz, emniyet, kanıt ve hesap

Bakım, egzozun çalışmasını ve varsa akış alarmını yerinde kontrol eder. Emniyet ekibi ışık perdesi ayarlarını onaylı yedekle karşılaştırır, ışık perdesi ihlalinde tehlikeli hareketin durduğunu kontrollü koşullarda doğrular. OT/BT şüpheli servis hesabını kapatır, oturumları sonlandırır ve PLC yapılandırması ile erişim kayıtlarını korur.

### 3. İlk 24 saat - Erken uyarı

03:00 giriş ve 10:15 tespit zamanı, etkilenen ürün ve biliniyorsa sürümü, yetkisiz erişimin özeti, olası etkiler ve ilk önlemler hazırlanır. Bildirim gerekiyorsa üreticiye gecikmeden iletilir.

### 4. İlk 72 saat - Ayrıntılı bildirim

Sunumdaki görev dağılımına göre OT ve BT incelemeyi yürütür, bakım ve emniyet ekiplerinin görüşü alınır. Yönetim müdahaleden nihai olarak sorumludur. Üretici, gerekiyorsa bilinen kök nedeni, etkiyi ve alınan önlemleri bildirir. Kesinleşmeyen bulguları ayrıca belirtir.

### 5. Föydeki 14. gün - Son rapor için kanıtlar

PLC değişiklik kayıtları, olay anındaki yapılandırma ve onaylı yedek, HMI alarmları, servis hesabı ve uzak erişim kayıtları, ışık perdesi ve egzoz kontrol kayıtları ile vardiya kayıtları korunur. Kopyaların kim tarafından ve ne zaman alındığı kaydedilir.

## CRA süre notu

14. gün föyün son rapor adımıdır. CRA kapsamında aktif olarak istismar edilen bir zafiyette 14 günlük süre, düzeltici veya azaltıcı önlemin kullanılabilir olmasından başlar. Bildirime tabi ciddi olayda son rapor, 72 saatlik bildirimin sunulmasından itibaren bir ay içinde verilir.

## Kaynaklar

- INSPECCO × KRIPTARIUM, PaketPro 3000 LAB Föyleri, LAB 6, PDF s. 7.
- Safety 4.0 Bootcamp Sunumu, PDF s. 23 ve 28-29.
- Kavramlar Sözlüğü, Olay ve Mevzuat, PDF s. 3.
- Avrupa Komisyonu, CRA bildirim yükümlülükleri. digital-strategy.ec.europa.eu/en/policies/cra-reporting
