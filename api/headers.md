# Headers

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi kapsamında API isteklerinde ve yanıtlarında kullanılan HTTP Header bilgilerini açıklamak amacıyla hazırlanmıştır.

---

# Request Headers

İstemciden sunucuya gönderilen API isteklerinde aşağıdaki header bilgileri kullanılmaktadır.

| Header        | Zorunlu | Açıklama                                               | Örnek                   |
| ------------- | ------- | ------------------------------------------------------ | ----------------------- |
| Authorization | Evet    | Kimlik doğrulama için Bearer Token bilgisi gönderilir. | `Bearer <Access_Token>` |
| Content-Type  | Evet    | İstek gövdesinin veri formatını belirtir.              | `application/json`      |
| Accept        | Hayır   | İstemcinin beklediği yanıt formatını belirtir.         | `application/json`      |

---

# Response Headers

Sunucu tarafından istemciye döndürülen yanıtlarda aşağıdaki header bilgileri kullanılabilir.

| Header         | Açıklama                                       | Örnek                           |
| -------------- | ---------------------------------------------- | ------------------------------- |
| Content-Type   | Döndürülen verinin formatını belirtir.         | `application/json`              |
| Date           | Yanıtın oluşturulduğu tarih ve saati belirtir. | `Mon, 27 Jul 2026 14:30:00 GMT` |
| Content-Length | Yanıt içeriğinin boyutunu belirtir.            | `512`                           |

---

# Header Kullanım İlkeleri

Bu proje kapsamında aşağıdaki kurallar benimsenmiştir.

* API istekleri JSON formatında gönderilmelidir.
* Kimlik doğrulaması gerektiren servislerde `Authorization` header'ı kullanılmalıdır.
* `Content-Type` değeri `application/json` olmalıdır.
* İstemci, yanıt formatı olarak `application/json` beklemelidir.

---

# Örnek Request Headers

```http
POST /api/v1/orders HTTP/1.1
Host: api.example.com
Authorization: Bearer <Access_Token>
Content-Type: application/json
Accept: application/json
```
