# HTTP Methodları

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi kapsamında kullanılan HTTP methodlarını ve kullanım amaçlarını açıklamak amacıyla hazırlanmıştır.

---

# HTTP Methodları

HTTP methodları, istemcinin sunucu üzerinde gerçekleştirmek istediği işlemi ifade eder. Bu projede REST mimarisine uygun olarak aşağıdaki methodlar kullanılmaktadır.

| HTTP Method | Kullanım Amacı                                              |
| ----------- | ----------------------------------------------------------- |
| GET         | Veri görüntüleme ve listeleme işlemlerinde kullanılır.      |
| POST        | Yeni bir kaynak oluşturmak için kullanılır.                 |
| DELETE      | Mevcut bir kaynağı silmek veya iptal etmek için kullanılır. |

---

# Projede Kullanılan HTTP Methodları

| HTTP Method | Endpoint                   | Açıklama                                        |
| ----------- | -------------------------- | ----------------------------------------------- |
| POST        | `/api/v1/orders`           | Yeni bir sipariş oluşturur.                     |
| GET         | `/api/v1/orders`           | Kullanıcının siparişlerini listeler.            |
| GET         | `/api/v1/orders/{orderId}` | Belirli bir siparişin detaylarını getirir.      |
| DELETE      | `/api/v1/orders/{orderId}` | İptal edilebilir durumdaki siparişi iptal eder. |

---

# HTTP Method Seçim Kriterleri

Bu projede HTTP methodları aşağıdaki prensiplere göre belirlenmiştir.

* Veri oluşturma işlemlerinde **POST** kullanılmıştır.
* Veri görüntüleme işlemlerinde **GET** kullanılmıştır.
* Sipariş iptal işlemi için **DELETE** kullanılmıştır.
* Her endpoint yalnızca tek bir işlevi yerine getirecek şekilde tasarlanmıştır.

---

# REST API Yaklaşımı

HTTP methodlarının doğru kullanımı;

* API'nin okunabilirliğini artırır.
* İstemci ve sunucu arasında tutarlı bir iletişim sağlar.
* REST standartlarına uygun bir API tasarımını destekler.
* API'nin bakımını ve geliştirilmesini kolaylaştırır.
