# Error Responses

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi kapsamında API servisleri tarafından döndürülebilecek hata yanıtlarını ve hata mesajı formatını açıklamak amacıyla hazırlanmıştır.

---

# Error Response Nedir?

Error Response, istemciden gelen isteğin başarıyla işlenememesi durumunda API tarafından döndürülen standart hata yanıtıdır.

Standart bir hata yapısı kullanılması, istemci uygulamaların hataları daha kolay yorumlamasını ve yönetmesini sağlar.

---

# Standart Hata Yanıtı

```json
{
  "timestamp": "2026-07-27T14:30:15Z",
  "status": 400,
  "error": "Bad Request",
  "message": "Geçersiz istek verisi.",
  "path": "/api/v1/orders"
}
```

---

# Hata Alanları

| Alan      | Veri Tipi | Açıklama                                |
| --------- | --------- | --------------------------------------- |
| timestamp | String    | Hatanın oluştuğu tarih ve saat bilgisi. |
| status    | Integer   | HTTP durum kodu.                        |
| error     | String    | HTTP durum kodunun açıklaması.          |
| message   | String    | Hatanın açıklayıcı mesajı.              |
| path      | String    | Hatanın oluştuğu endpoint.              |

---

# Yaygın Hata Senaryoları

| HTTP Status Kodu          | Senaryo                        | Örnek Mesaj                                                      |
| ------------------------- | ------------------------------ | ---------------------------------------------------------------- |
| 400 Bad Request           | Eksik veya hatalı istek verisi | Geçersiz istek verisi.                                           |
| 401 Unauthorized          | Kimlik doğrulama başarısız     | Geçersiz veya eksik erişim belirteci.                            |
| 403 Forbidden             | Yetkisiz işlem                 | Bu işlem için yetkiniz bulunmamaktadır.                          |
| 404 Not Found             | Sipariş bulunamadı             | İstenen sipariş bulunamadı.                                      |
| 500 Internal Server Error | Beklenmeyen sistem hatası      | Beklenmeyen bir hata oluştu. Lütfen daha sonra tekrar deneyiniz. |

---

# Hata Yönetimi İlkeleri

Bu proje kapsamında aşağıdaki ilkeler benimsenmiştir.

* Hata mesajları kullanıcıya anlaşılır şekilde sunulmalıdır.
* Aynı hata türü için tutarlı yanıt yapısı kullanılmalıdır.
* Hata yanıtları ilgili HTTP durum kodu ile birlikte döndürülmelidir.
* Hata mesajları sistemin iç yapısı hakkında hassas bilgi içermemelidir.
* Tüm hata yanıtları JSON formatında döndürülmelidir.
