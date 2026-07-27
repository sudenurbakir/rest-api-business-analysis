# Authentication

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi API servislerine erişim sırasında kullanılacak kimlik doğrulama (Authentication) yöntemini açıklamak amacıyla hazırlanmıştır.

---

# Authentication Yöntemi

Bu projede API servislerine erişim için **Bearer Token** tabanlı kimlik doğrulama yöntemi kullanılmaktadır.

Kimliği doğrulanmamış kullanıcıların korunan API servislerine erişmesine izin verilmez.

---

# Authorization Header

Kimlik doğrulama bilgisi, her isteğin HTTP Header bölümünde gönderilmelidir.

| Header        | Değer                 |
| ------------- | --------------------- |
| Authorization | Bearer <Access_Token> |

### Örnek

```http
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

---

# Kimlik Doğrulama Süreci

API'ye erişim süreci aşağıdaki adımlardan oluşur:

1. Kullanıcı sisteme giriş yapar.
2. Kimlik doğrulama işlemi başarılı olursa kullanıcıya bir Access Token üretilir.
3. İstemci uygulama bu token'ı saklar.
4. Korunan API servislerine yapılan her istekte Access Token, Authorization header'ı ile gönderilir.
5. Sunucu token'ı doğrular ve isteği işler.

---

# Authentication Gerektiren Servisler

Aşağıdaki servisler kimlik doğrulaması gerektirir.

| HTTP Method | Endpoint                   |
| ----------- | -------------------------- |
| POST        | `/api/v1/orders`           |
| GET         | `/api/v1/orders`           |
| GET         | `/api/v1/orders/{orderId}` |
| DELETE      | `/api/v1/orders/{orderId}` |

---

# Başarısız Kimlik Doğrulama

Aşağıdaki durumlarda istek reddedilir:

* Authorization header'ı bulunmuyorsa
* Bearer Token geçersizse
* Bearer Token süresi dolmuşsa
* Bearer Token doğrulanamıyorsa

Bu durumlarda API aşağıdaki HTTP durum kodunu döndürür:

```text
401 Unauthorized
```

---

# Güvenlik İlkeleri

Bu proje kapsamında aşağıdaki güvenlik ilkeleri benimsenmiştir:

* API istekleri HTTPS üzerinden gerçekleştirilmelidir.
* Access Token istemci tarafından güvenli şekilde saklanmalıdır.
* Token üçüncü kişilerle paylaşılmamalıdır.
* Her istek bağımsız olarak doğrulanmalıdır.

```

---



Burada sadece GET, POST, PUT, PATCH ve DELETE'nin tanımını vermeyeceğiz. Aynı zamanda **neden bu projede belirli endpoint'lerde bu metodların tercih edildiğini** de açıklayacağız. Bu, bir İş Analistinin API tasarım kararlarını dokümante etmesi açısından oldukça değerli bir bölüm olacak.
```
