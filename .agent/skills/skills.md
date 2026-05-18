---
description: Python (Flask/FastAPI), MySQL, ve Vanilla JS için kullanılacak temel yetenekler ve kodlama pratikleri.
---
# Teknik Yetenekler (Skills)

Bu projeyi kodlarken aşağıdaki yeteneklerini en optimal seviyede kullanmalısın:

## 1. Python & API Framework Yetenekleri
- **Framework:** Flask veya FastAPI'de uzman seviyesinde kullanım.
- **Routing:** Dinamik parametreleri (`/api/modeller/<id>`) doğru işleme.
- **Serialization:** Veritabanından gelen verileri (SQL Row objelerini) JSON formatına güvenli bir şekilde dönüştürme.

## 2. MySQL & SQL Yetenekleri
- **Sorgular:** Raw SQL yazabilme veya ORM (Örn: SQLAlchemy) kullanarak güvenli veri çekme/ekleme.
- **Şema Yönetimi:** Tablo yapılarını tanımlama, `1-to-N` ilişkilerini (`modeller` tablosundaki `seri_id` gibi) eksiksiz yönetme.
- **Güvenlik:** SQL Injection saldırılarını önlemek için parametrik sorgular (Prepared Statements) kullanma.

## 3. Vanilla JavaScript (ES6+) Yetenekleri
- **Asenkron Programlama:** `fetch()`, `Promises` ve `async/await` yapılarına derinlemesine hakimiyet.
- **DOM Manipülasyonu:** `document.getElementById`, `innerHTML`, `createElement` gibi Vanilla JS metotlarıyla HTML elemanlarını dinamik olarak oluşturma.
- **Event Listeners:** Form gönderimlerini (Submit) dinleme ve sayfanın yenilenmesini (`e.preventDefault()`) engelleme.

## 4. Güvenlik ve Validasyon Yetenekleri
- **Payload Kontrolü:** Gelen JSON verilerindeki zorunlu alanları (Örn: İletişim formunda `isim` ve `mesaj`) backend tarafında doğrulama.
- **Hata Yönetimi (Error Handling):** Hatalı isteklerde uygulamayı çökertmek yerine, `try-catch` blokları kullanarak `{"error": "Açıklama"}` formatında temiz yanıtlar dönme.