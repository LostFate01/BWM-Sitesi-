---
trigger: always_on
---

---
description: BMW Dealership üniversite projesi için sistem davranışları, veritabanı ve mimari kuralları.
---
# Proje Kuralları ve Kısıtlamaları (Rules)

Bu proje bir üniversite ödevidir. Statik bir BMW Bayi web sitesini (HTML/CSS/JS), RESTful API ve MySQL veritabanı kullanarak dinamik bir web uygulamasına dönüştürmelisin.

## 1. Veritabanı Kesin Kuralları
- **Zorunlu Tablolar:** Veritabanında kesinlikle şu 8 tablo bulunmalıdır: `seriler`, `modeller`, `donanim_paketleri`, `fiyat_listesi`, `iletisim_talepleri`, `geri_cagirmalar`, `kampanyalar`, `kullanicilar`.
- **Kalıcılık:** Tüm CRUD işlemleri doğrudan MySQL veritabanı üzerinde yapılmalıdır. Veri saklamak için yerel JSON dosyaları KULLANILAMAZ.
- **İlişkiler:** Tablolar arası Primary Key / Foreign Key ilişkileri (Örn: `seriler` ve `modeller` arasında 1-to-N) kesinlikle kurulmalıdır.

## 2. API İletişim Standartları
- Tüm backend endpoint'leri standart JSON formatında yanıt dönmelidir.
- Doğru HTTP Metotları kullanılmalıdır: `GET` (veri okuma), `POST` (veri oluşturma), `PUT/PATCH` (veri güncelleme), `DELETE` (veri silme).
- İşlem sonuçlarına göre uygun HTTP Statüs Kodları (200 OK, 201 Created, 400 Bad Request, 404 Not Found, 500 Internal Error) dönülmelidir.

## 3. Frontend Kuralları
- **Tasarımı Koruma:** Kullanıcının mevcut HTML ve CSS (Bootstrap) tasarımını BOZMA. Sadece veri entegrasyonu yap.
- **Dinamik Veri:** `fiyat-listesi.html` ve `modeller.html` gibi sayfalardaki statik (hardcoded) verileri kaldırıp, JS `fetch()` ile API'den gelen verilerle DOM üzerinden dinamik olarak render et.
- **Kullanıcı Geri Bildirimi:** İletişim veya kampanya formları gönderildiğinde başarılı/başarısız mesajlarını arayüzde göster.

## 4. Kod Kalitesi ve Akademik Sunum
- Kodlar temiz, modüler ve iyi yorumlanmış olmalıdır.
- **Öğrenci Savunması:** Bu bir üniversite projesi olduğu için, yazdığın karmaşık kodlarda veya mimari seçimlerde *neden* bu yöntemi seçtiğini kısaca açıkla (böylece öğrenci projeyi hocasına savunabilsin).
- Veritabanını hızlıca ayağa kaldırmak için projeye mutlaka bir `init.sql` script dosyası dahil et.

## 5. Admin Paneli Gereksinimi
- Projenin Update (Güncelleme) ve Delete (Silme) isterlerini karşılamak için temel bir `admin.html` arayüzü ve buna bağlı çalışan JS/API rotaları oluştur.