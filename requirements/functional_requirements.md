# Fonksiyonel Gereksinimler (Functional Requirements)

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi'nin yerine getirmesi gereken fonksiyonel gereksinimleri tanımlamak amacıyla hazırlanmıştır.

Fonksiyonel gereksinimler, sistemin kullanıcı isteklerine nasıl yanıt vereceğini ve hangi işlemleri gerçekleştireceğini açıklar.

---

# Fonksiyonel Gereksinimler

| ID     | Fonksiyonel Gereksinim                                                                            | Öncelik |
| ------ | ------------------------------------------------------------------------------------------------- | ------- |
| FR-001 | Sistem, yetkili kullanıcının yeni bir sipariş oluşturmasına izin vermelidir.                      | Yüksek  |
| FR-002 | Sistem, sipariş oluşturma isteğinde en az bir ürün bulunmasını zorunlu tutmalıdır.                | Yüksek  |
| FR-003 | Sistem, siparişe eklenen her ürün için adet bilgisini doğrulamalıdır.                             | Yüksek  |
| FR-004 | Sistem, sipariş oluşturulurken ürünlerin güncel stok durumunu kontrol etmelidir.                  | Yüksek  |
| FR-005 | Sistem, başarılı şekilde oluşturulan her sipariş için benzersiz bir sipariş numarası üretmelidir. | Yüksek  |
| FR-006 | Sistem, oluşturulan sipariş bilgilerini kullanıcıya döndürmelidir.                                | Yüksek  |
| FR-007 | Sistem, kullanıcının kendi siparişlerini listelemesine izin vermelidir.                           | Orta    |
| FR-008 | Sistem, kullanıcının belirli bir siparişin detaylarını görüntülemesine izin vermelidir.           | Orta    |
| FR-009 | Sistem, yalnızca iptal edilebilir durumdaki siparişlerin iptal edilmesine izin vermelidir.        | Yüksek  |
| FR-010 | Sistem, geçersiz isteklerde uygun hata mesajı döndürmelidir.                                      | Yüksek  |

---

# Beklenen Sistem Davranışı

Sistem;

* Kullanıcıdan gelen sipariş oluşturma isteğini doğrulamalıdır.
* Zorunlu alanların eksik olup olmadığını kontrol etmelidir.
* Sipariş içeriğini iş kurallarına göre değerlendirmelidir.
* Başarılı işlemlerde siparişi oluşturmalı ve kullanıcıya sonucu iletmelidir.
* Hatalı işlemlerde uygun hata mesajı döndürmelidir.
