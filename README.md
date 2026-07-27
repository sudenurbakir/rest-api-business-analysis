# REST API Analizi ve İstemci-Sunucu Sözleşmesi (API Contract)

> **E-Ticaret Sipariş Yönetimi Servisi için İş Analisti API Spesifikasyonu**

---

## Proje Amacı ve İş Problemi

Modern yazılım mimarilerinde ön yüz (Frontend) ve arka yüz (Backend) sistemleri **REST API** servisleri aracılığıyla haberleşir. İş analizinde API dokümantasyonunun eksik veya belirsiz olması; eksik parametre gönderimine, hatalı veri tiplerine ve sistemler arası entegrasyon kilitlenmelerine yol açar.

Bu proje; bir İş Analisti olarak bir e-ticaret platformundaki **"Sipariş Oluşturma (Create Order)"** API servisinin gereksinimlerini, veri tiplerini, doğrulama (validation) kurallarını ve yanıt durum kodlarını tanımlamak amacıyla hazırlanmıştır.

---

## API Servis Özeti

* **Servis Adı:** Sipariş Oluşturma Servisi
* **HTTP Yöntemi:** `POST`
* **Uç Nokta (Endpoint):** `/api/v1/orders`
* **İçerik Tipi (Content-Type):** `application/json`
* **Yetkilendirme (Auth):** `Bearer Token`

---

## İstek (Request) Parametreleri ve İş Kuralları

| Parametre | Veri Tipi | Zorunlu mu? | Açıklama ve Doğrulama Kuralı |
| :--- | :--- | :--- | :--- |
| `customerId` | `integer` | Evet | Siparişi veren müşterinin benzersiz ID'si. Pozitif tam sayı olmalı. |
| `items` | `array` | Evet | Sepetteki ürünlerin listesi. En az 1 ürün içermelidir. |
| `items[].productId` | `integer` | Evet | Satın alınan ürünün ID'si. |
| `items[].quantity` | `integer` | Evet | Ürün adedi. Minimum `1` olmalıdır. |
| `items[].unitPrice` | `number` | Evet | Ürünün birim fiyatı. Ondalıklı sayı (Örn: `1200.00`). |
| `paymentMethod` | `string` | Evet | Ödeme yöntemi. Alabileceği değerler: `CREDIT_CARD`, `BANK_TRANSFER`. |
| `shippingAddress` | `object` | Evet | Teslimat adresi detayları. |

---

## Yanıt (Response) Durum Kodları ve Senaryolar

| HTTP Kodu | Durum Metni | Senaryo Açıklaması |
| :--- | :--- | :--- |
| **`201 Created`** | Başarılı | Sipariş veritabanında başarıyla oluşturuldu ve stok düşüldü. |
| **`400 Bad Request`** | Geçersiz İstek | Eksik parametre (Örn: `items` dizisinin boş gelmesi) veya geçersiz veri tipi. |
| **`422 Unprocessable`** | İş Kuralı İhlali | Stok yetersizliği veya geçersiz ödeme yöntemi. |
| **`500 Internal Error`** | Sunucu Hatası | Arka planda ödeme ağ geçidi ile iletişim kopması. |

---

## Örnek İstek Gövdesi (JSON Payload)

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
  "paymentMethod": "CREDIT_CARD",
  "shippingAddress": {
    "city": "İstanbul",
    "district": "Kadıköy",
    "addressLine": "Atatürk Cad. No:12 D:4"
  }
}
