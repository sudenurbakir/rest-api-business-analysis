# Veri Sözlüğü

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi kapsamında kullanılan veri alanlarını tanımlamak ve bu alanların anlamlarını standart bir şekilde açıklamak amacıyla hazırlanmıştır.

---

# Veri Sözlüğü

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi kapsamında kullanılan veri alanlarını tanımlamak ve bu alanların anlamlarını standart bir şekilde açıklamak amacıyla hazırlanmıştır.

---

# Veri Sözlüğü

| Alan Adı | Veri Tipi | Kullanım | Zorunlu | Açıklama | Örnek |
|-----------|-----------|----------|---------|----------|--------|
| orderId | Integer | Response | Hayır | Sistem tarafından oluşturulan benzersiz sipariş kimlik numarası. | 25031 |
| customerId | Integer | Request | Evet | Siparişi oluşturan müşterinin benzersiz kimliği. | 10542 |
| productId | Integer | Request | Evet | Siparişe eklenen ürünün benzersiz kimliği. | 8841 |
| quantity | Integer | Request | Evet | Sipariş edilen ürün adedi. Minimum değer 1 olmalıdır. | 2 |
| unitPrice | Decimal | Request | Evet | Ürünün sipariş anındaki birim fiyatı. | 1200.00 |
| paymentMethod | String | Request | Evet | Sipariş için kullanılan ödeme yöntemi. | CREDIT_CARD |
| items | Array | Request | Evet | Siparişte bulunan ürünlerin listesidir. | Ürün listesi |
| status | String | Response | Hayır | Siparişin mevcut durumunu belirtir. | CREATED |
| message | String | Response | Hayır | İşlem sonucunu açıklayan bilgilendirme mesajıdır. | Sipariş başarıyla oluşturuldu. |
| timestamp | String (ISO 8601) | Response | Hayır | İşlemin gerçekleştiği tarih ve saat bilgisidir. | 2026-07-27T14:30:15Z |

---

# Veri Tipleri

| Veri Tipi | Açıklama |
|------------|----------|
| Integer | Tam sayı değerlerini temsil eder. |
| Decimal | Ondalıklı sayısal değerleri temsil eder. |
| String | Metinsel değerleri temsil eder. |
| Array | Birden fazla verinin listesini temsil eder. |

---

# Kullanım Açıklaması

| Kullanım | Açıklama |
|----------|----------|
| Request | İstemci tarafından API'ye gönderilen veri alanlarını ifade eder. |
| Response | API tarafından istemciye döndürülen veri alanlarını ifade eder. |

---

# Notlar

- Veri alanlarında camelCase isimlendirme standardı kullanılmıştır.
- Request alanları API isteği sırasında gönderilen bilgileri temsil eder.
- Response alanları API tarafından oluşturulan veya döndürülen bilgileri temsil eder.
- Zorunlu alanlar API isteğinde mutlaka bulunmalıdır.

# Veri Tipleri

| Veri Tipi | Açıklama                             |
| --------- | ------------------------------------ |
| Integer   | Tam sayı değeridir.                  |
| Decimal   | Ondalıklı sayısal değerdir.          |
| String    | Metinsel ifadeleri temsil eder.      |
| Array     | Birden fazla öğeden oluşan listedir. |

---

# Notlar

* Veri alanlarının isimlendirilmesinde **camelCase** standardı kullanılmıştır.
* Zorunlu alanlar API isteğinde mutlaka gönderilmelidir.
* Örnek değerler yalnızca dokümantasyon amacıyla verilmiştir.
