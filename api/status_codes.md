# HTTP Status Kodları

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi kapsamında API servisleri tarafından döndürülen HTTP durum kodlarını ve kullanım amaçlarını açıklamak amacıyla hazırlanmıştır.

---

# HTTP Status Kodu Nedir?

HTTP durum kodları, istemci tarafından gönderilen isteğin sunucu tarafından nasıl sonuçlandığını gösteren standart yanıt kodlarıdır.

Her durum kodu, isteğin başarılı olup olmadığını veya neden başarısız olduğunu ifade eder.

---

# Kullanılan HTTP Status Kodları

| Status Kodu               | Durum          | Açıklama                                                    |
| ------------------------- | -------------- | ----------------------------------------------------------- |
| 200 OK                    | Başarılı       | İstek başarıyla işlenmiş ve istenen veri döndürülmüştür.    |
| 201 Created               | Oluşturuldu    | Yeni bir kaynak başarıyla oluşturulmuştur.                  |
| 400 Bad Request           | Geçersiz İstek | İstek formatı hatalı veya eksik bilgi içermektedir.         |
| 401 Unauthorized          | Yetkisiz       | Kimlik doğrulama bilgisi eksik veya geçersizdir.            |
| 403 Forbidden             | Yasak          | Kullanıcının ilgili kaynağa erişim yetkisi bulunmamaktadır. |
| 404 Not Found             | Bulunamadı     | İstenen kaynak sistemde bulunamamıştır.                     |
| 500 Internal Server Error | Sunucu Hatası  | Sunucu tarafında beklenmeyen bir hata oluşmuştur.           |

---

# Projede Kullanım Senaryoları

| HTTP Method | Endpoint                   | Başarılı Durum Kodu |
| ----------- | -------------------------- | ------------------- |
| POST        | `/api/v1/orders`           | 201 Created         |
| GET         | `/api/v1/orders`           | 200 OK              |
| GET         | `/api/v1/orders/{orderId}` | 200 OK              |
| DELETE      | `/api/v1/orders/{orderId}` | 200 OK              |

---

# Başarısız Durum Senaryoları

| Durum                                    | Döndürülen Status Kodu    |
| ---------------------------------------- | ------------------------- |
| Eksik veya hatalı istek verisi           | 400 Bad Request           |
| Geçersiz veya eksik Bearer Token         | 401 Unauthorized          |
| Yetkisiz bir kaynağa erişim denemesi     | 403 Forbidden             |
| Var olmayan bir siparişin görüntülenmesi | 404 Not Found             |
| Beklenmeyen sistem hatası                | 500 Internal Server Error |

---

# Genel İlkeler

Bu proje kapsamında aşağıdaki ilkeler benimsenmiştir.

* Başarılı işlemler uygun 2xx durum kodları ile sonuçlandırılır.
* İstemci kaynaklı hatalarda 4xx durum kodları kullanılır.
* Sunucu kaynaklı beklenmeyen hatalarda 5xx durum kodları kullanılır.
* Her durum kodu, işlemin sonucunu açık ve tutarlı şekilde yansıtmalıdır.
