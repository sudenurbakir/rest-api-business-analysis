# İş Kuralları (Business Rules)

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi kapsamında sipariş oluşturma ve yönetme süreçlerinde uygulanacak iş kurallarını tanımlamak amacıyla hazırlanmıştır.

İş kuralları, sistemin kullanıcı taleplerini hangi koşullar altında kabul edeceğini veya reddedeceğini belirler.

---

# İş Kuralları

| ID        | İş Kuralı                                                                                           | Öncelik |
| --------- | --------------------------------------------------------------------------------------------------- | ------- |
| BRULE-001 | Bir sipariş en az bir ürün içermelidir.                                                             | Yüksek  |
| BRULE-002 | Siparişe eklenen her ürün için adet bilgisi 1 veya daha büyük olmalıdır.                            | Yüksek  |
| BRULE-003 | Stokta bulunmayan ürünler siparişe eklenemez.                                                       | Yüksek  |
| BRULE-004 | Sipariş yalnızca sistemde kayıtlı ürünlerden oluşturulabilir.                                       | Yüksek  |
| BRULE-005 | Sipariş oluşturma işlemi yalnızca kimliği doğrulanmış kullanıcılar tarafından gerçekleştirilebilir. | Yüksek  |
| BRULE-006 | Her sipariş benzersiz bir sipariş numarasına sahip olmalıdır.                                       | Yüksek  |
| BRULE-007 | Kullanıcı yalnızca kendisine ait siparişleri görüntüleyebilir.                                      | Yüksek  |
| BRULE-008 | Kullanıcı yalnızca iptal edilebilir durumdaki siparişleri iptal edebilir.                           | Yüksek  |
| BRULE-009 | İptal edilen bir sipariş tekrar aktif duruma getirilemez.                                           | Orta    |
| BRULE-010 | Başarılı sipariş oluşturma işlemi sonrasında kullanıcıya sipariş bilgileri döndürülmelidir.         | Orta    |

---

# Genel İlkeler

İş kuralları;

* İş süreçlerinin tutarlı şekilde yürütülmesini sağlar.
* Hatalı veya geçersiz işlemlerin önüne geçer.
* Geliştirme ve test ekipleri için ortak bir referans oluşturur.
* API servislerinin beklenen iş mantığına uygun çalışmasını destekler.
