# İş Gereksinimleri (Business Requirements)

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi için iş ihtiyaçlarını tanımlamak amacıyla hazırlanmıştır.

İş gereksinimleri, teknik çözümden bağımsız olarak sistemin işletmeye sağlayacağı değeri ve karşılaması gereken ihtiyaçları ifade eder.

---

| ID     | İş Gereksinimi                                                                       | Öncelik | İlgili Paydaş | Gerekçe                                                                                               |
| ------ | ------------------------------------------------------------------------------------ | ------- | ------------- | ----------------------------------------------------------------------------------------------------- |
| BR-001 | Müşteriler çevrim içi sipariş oluşturabilmelidir.                                    | Yüksek  | Product Owner | Sipariş oluşturma, satış sürecinin temel adımıdır.                                                    |
| BR-002 | Müşteriler oluşturdukları siparişleri görüntüleyebilmelidir.                         | Yüksek  | Product Owner | Kullanıcıların sipariş durumlarını takip edebilmesi gereklidir.                                       |
| BR-003 | Müşteriler uygun durumdaki siparişlerini iptal edebilmelidir.                        | Yüksek  | Product Owner | Kullanıcıya sipariş üzerinde kontrol ve esneklik sağlanmalıdır.                                       |
| BR-004 | Sistem yalnızca geçerli ürünler için sipariş oluşturulmasına izin vermelidir.        | Yüksek  | Product Owner | Hatalı veya geçersiz siparişlerin oluşması engellenmelidir.                                           |
| BR-005 | Sipariş oluşturma işlemleri güvenli şekilde gerçekleştirilmelidir.                   | Yüksek  | Product Owner | Yetkisiz erişim ve güvenlik riskleri önlenmelidir.                                                    |
| BR-006 | Kullanıcılara sipariş işlemlerinin sonucu açık ve anlaşılır şekilde gösterilmelidir. | Orta    | Product Owner | Kullanıcı deneyimini iyileştirmek ve işlem sonuçlarının doğru anlaşılmasını sağlamak amaçlanmaktadır. |

---

# İş Hedefleri

Bu gereksinimlerle aşağıdaki iş hedeflerinin desteklenmesi amaçlanmaktadır:

* Sipariş oluşturma sürecini dijital ortamda yönetmek.
* Sipariş yönetim süreçlerini standartlaştırmak.
* Hatalı sipariş oluşumunu azaltmak.
* Kullanıcı memnuniyetini artırmak.
* İş süreçlerinin izlenebilirliğini güçlendirmek.

---

# Başarı Kriterleri

Projenin başarılı kabul edilebilmesi için aşağıdaki hedeflerin karşılanması beklenmektedir:

* Müşteriler sipariş oluşturma işlemini başarılı şekilde tamamlayabilmelidir.
* Kullanıcılar sipariş bilgilerine erişebilmelidir.
* İş kurallarına uymayan sipariş talepleri reddedilmelidir.
* API servisleri tanımlanan iş gereksinimlerini karşılamalıdır.
