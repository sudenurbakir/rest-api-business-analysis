# API Test Cases

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi kapsamında sunulan REST API servisleri için hazırlanan test senaryolarını içermektedir.

Amaç, API servislerinin fonksiyonel gereksinimlere ve iş kurallarına uygun şekilde çalıştığını doğrulamaktır.

---

# Test Senaryoları

| Test ID | Endpoint                   | HTTP Method | Senaryo                                                     | Beklenen Sonuç                                          |
| ------- | -------------------------- | ----------- | ----------------------------------------------------------- | ------------------------------------------------------- |
| TC-001  | `/api/v1/orders`           | POST        | Geçerli bilgiler ile yeni sipariş oluşturulur.              | **201 Created** döner ve sipariş başarıyla oluşturulur. |
| TC-002  | `/api/v1/orders`           | POST        | Zorunlu alanlardan biri eksik gönderilir.                   | **400 Bad Request** döner.                              |
| TC-003  | `/api/v1/orders`           | POST        | Geçersiz Bearer Token ile istek gönderilir.                 | **401 Unauthorized** döner.                             |
| TC-004  | `/api/v1/orders`           | GET         | Kullanıcının siparişleri listelenir.                        | **200 OK** döner ve sipariş listesi görüntülenir.       |
| TC-005  | `/api/v1/orders/{orderId}` | GET         | Geçerli sipariş numarası ile detay sorgulanır.              | **200 OK** döner ve sipariş bilgileri görüntülenir.     |
| TC-006  | `/api/v1/orders/{orderId}` | GET         | Sistemde bulunmayan sipariş numarası ile sorgulama yapılır. | **404 Not Found** döner.                                |
| TC-007  | `/api/v1/orders/{orderId}` | DELETE      | İptal edilebilir durumdaki sipariş iptal edilir.            | **200 OK** döner ve sipariş iptal edilir.               |
| TC-008  | `/api/v1/orders/{orderId}` | DELETE      | İptal edilemeyen bir sipariş iptal edilmeye çalışılır.      | **400 Bad Request** döner.                              |

---

# Test Kapsamı

Bu test senaryoları aşağıdaki kontrolleri kapsamaktadır:

* Başarılı işlem senaryoları
* Zorunlu alan kontrolleri
* Kimlik doğrulama kontrolleri
* Kaynak bulunamama senaryoları
* İş kurallarının doğrulanması
* Hata yönetimi kontrolleri
