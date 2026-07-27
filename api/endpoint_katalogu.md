# API Endpoint Kataloğu

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi kapsamında sunulan REST API servislerini listelemek ve her servisin temel özelliklerini açıklamak amacıyla hazırlanmıştır.

---

# Endpoint Listesi

| Servis              | HTTP Method | Endpoint                   | Açıklama                                        |
| ------------------- | ----------- | -------------------------- | ----------------------------------------------- |
| Sipariş Oluştur     | POST        | `/api/v1/orders`           | Yeni bir sipariş oluşturur.                     |
| Siparişleri Listele | GET         | `/api/v1/orders`           | Kullanıcının siparişlerini listeler.            |
| Sipariş Detayı      | GET         | `/api/v1/orders/{orderId}` | Belirli bir siparişin detaylarını getirir.      |
| Sipariş İptal Et    | DELETE      | `/api/v1/orders/{orderId}` | İptal edilebilir durumdaki siparişi iptal eder. |

---

# Endpoint Açıklamaları

## 1. Sipariş Oluştur

* **HTTP Method:** `POST`
* **Endpoint:** `/api/v1/orders`

### Açıklama

Kullanıcının seçtiği ürünler ile yeni bir sipariş oluşturmasını sağlar.

---

## 2. Siparişleri Listele

* **HTTP Method:** `GET`
* **Endpoint:** `/api/v1/orders`

### Açıklama

Kimliği doğrulanmış kullanıcının tüm siparişlerini listeler.

---

## 3. Sipariş Detayı

* **HTTP Method:** `GET`
* **Endpoint:** `/api/v1/orders/{orderId}`

### Açıklama

Belirtilen sipariş numarasına ait detay bilgilerini döndürür.

---

## 4. Sipariş İptal Et

* **HTTP Method:** `DELETE`
* **Endpoint:** `/api/v1/orders/{orderId}`

### Açıklama

İptal koşullarını sağlayan siparişlerin iptal edilmesini sağlar.

---

# API Versiyonlama

Bu projede endpoint'ler versiyonlanabilir bir yapı ile tasarlanmıştır.

Örnek:

```text
/api/v1/orders
```

Bu yaklaşım sayesinde gelecekte yapılacak değişikliklerde yeni API sürümleri mevcut istemcileri etkilemeden yayınlanabilir.

---

# İsimlendirme Standartları

API endpoint'leri aşağıdaki kurallara uygun olarak tasarlanmıştır:

* URL yapılarında küçük harf kullanılır.
* Kaynak adları çoğul (plural) olarak yazılır.
* Endpoint isimlerinde fiil yerine kaynak adı kullanılır.
* HTTP methodu işlemin amacını belirler.
* URL yapıları okunabilir ve tutarlı olacak şekilde oluşturulur.
