# Request & Response

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi kapsamında kullanılan API istek (Request) ve yanıt (Response) yapılarının açıklanması amacıyla hazırlanmıştır.

---

# Request Nedir?

Request, istemcinin (Client) sunucuya (Server) gönderdiği istektir.

Bir API isteği; endpoint, HTTP methodu, header bilgileri ve gerektiğinde request body'den oluşur.

---

# Response Nedir?

Response, sunucunun istemciye gönderdiği yanıttır.

Yanıt içerisinde işlem sonucu, durum kodu (HTTP Status Code) ve gerekli veri yer alabilir.

---

# Sipariş Oluşturma İsteği

**HTTP Method**

```text
POST
```

**Endpoint**

```text
/api/v1/orders
```

### Request Body

```json
{
  "customerId": 10542,
  "items": [
    {
      "productId": 8841,
      "quantity": 1,
      "unitPrice": 1200.00
    }
  ],
  "paymentMethod": "CREDIT_CARD"
}
```

### Alan Açıklamaları

| Alan          | Veri Tipi | Zorunlu | Açıklama                               |
| ------------- | --------- | ------- | -------------------------------------- |
| customerId    | Integer   | Evet    | Siparişi oluşturan müşterinin kimliği. |
| items         | Array     | Evet    | Siparişe eklenecek ürünlerin listesi.  |
| productId     | Integer   | Evet    | Ürün kimliği.                          |
| quantity      | Integer   | Evet    | Sipariş adedi.                         |
| unitPrice     | Number    | Evet    | Ürünün birim fiyatı.                   |
| paymentMethod | String    | Evet    | Ödeme yöntemi.                         |

---

# Başarılı Response

```json
{
  "orderId": 25031,
  "status": "CREATED",
  "message": "Sipariş başarıyla oluşturuldu."
}
```

### Response Alanları

| Alan    | Veri Tipi | Açıklama                                    |
| ------- | --------- | ------------------------------------------- |
| orderId | Integer   | Oluşturulan siparişin benzersiz numarası.   |
| status  | String    | Siparişin güncel durumu.                    |
| message | String    | İşlem sonucu hakkında bilgilendirme mesajı. |

---

# Request ve Response İlkeleri

Bu proje kapsamında aşağıdaki prensipler benimsenmiştir.

* Tüm istek ve yanıtlar JSON formatında oluşturulur.
* Zorunlu alanlar eksiksiz gönderilmelidir.
* Başarılı işlemlerde anlamlı bir response döndürülmelidir.
* Response yapıları tutarlı ve okunabilir olmalıdır.
* Alan adlarında camelCase yazım standardı kullanılmalıdır.
