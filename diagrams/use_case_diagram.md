# Use Case Diagram

## Amaç

Bu diyagram, E-Ticaret Sipariş Yönetim Sistemi kapsamında kullanıcıların API üzerinden gerçekleştirebileceği temel işlemleri göstermektedir.

---

```mermaid
flowchart LR

    User[Kullanıcı]

    UC1((Sipariş Oluştur))
    UC2((Siparişleri Listele))
    UC3((Sipariş Detayını Görüntüle))
    UC4((Siparişi İptal Et))

    User --> UC1
    User --> UC2
    User --> UC3
    User --> UC4
```

---

# Açıklama

Bu sistemde tek aktör **Kullanıcı** olarak ele alınmıştır.

Kullanıcı aşağıdaki işlemleri gerçekleştirebilir:

* Yeni sipariş oluşturabilir.
* Kendi siparişlerini listeleyebilir.
* Belirli bir siparişin detayını görüntüleyebilir.
* Uygun durumdaki siparişleri iptal edebilir.

Bu diyagram, sistemin kullanıcıya sunduğu temel işlevleri özetlemektedir.
