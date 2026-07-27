# Fonksiyonel Olmayan Gereksinimler (Non-Functional Requirements)

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi'nin performans, güvenlik, kullanılabilirlik ve güvenilirlik gibi fonksiyonel olmayan gereksinimlerini tanımlamak amacıyla hazırlanmıştır.

---

# Fonksiyonel Olmayan Gereksinimler

| ID      | Gereksinim Kategorisi | Gereksinim                                                                                           | Öncelik |
| ------- | --------------------- | ---------------------------------------------------------------------------------------------------- | ------- |
| NFR-001 | Performans            | Sipariş oluşturma isteği normal sistem yükü altında en fazla 2 saniye içerisinde sonuçlanmalıdır.    | Yüksek  |
| NFR-002 | Güvenlik              | API servislerine yalnızca kimliği doğrulanmış kullanıcılar erişebilmelidir.                          | Yüksek  |
| NFR-003 | Güvenlik              | Tüm API istekleri HTTPS protokolü üzerinden gerçekleştirilmelidir.                                   | Yüksek  |
| NFR-004 | Kullanılabilirlik     | API servisleri standart JSON formatında yanıt döndürmelidir.                                         | Orta    |
| NFR-005 | Güvenilirlik          | Beklenmeyen sistem hatalarında kullanıcıya anlamlı hata mesajları gösterilmelidir.                   | Yüksek  |
| NFR-006 | Kullanılabilirlik     | API dokümantasyonu geliştirici ekip tarafından erişilebilir olmalıdır.                               | Orta    |
| NFR-007 | Ölçeklenebilirlik     | API tasarımı gelecekte yeni sipariş işlemlerinin eklenmesini destekleyecek şekilde oluşturulmalıdır. | Orta    |
| NFR-008 | Bakım Kolaylığı       | Endpoint isimlendirmeleri REST standartlarına uygun ve tutarlı olmalıdır.                            | Orta    |

---

# Genel İlkeler

Fonksiyonel olmayan gereksinimler, sistemin kalite standartlarını belirler. Bu gereksinimlerin amacı;

* Güvenli bir API altyapısı oluşturmak,
* Performans beklentilerini karşılamak,
* Tutarlı ve sürdürülebilir bir API tasarımı sağlamak,
* Geliştirme ve bakım süreçlerini kolaylaştırmaktır.
