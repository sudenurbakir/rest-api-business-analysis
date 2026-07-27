# UAT (User Acceptance Test)

## Amaç

Bu doküman, E-Ticaret Sipariş Yönetim Sistemi kapsamında geliştirilen API servislerinin iş gereksinimlerini karşıladığını doğrulamak amacıyla hazırlanan Kullanıcı Kabul Testi (User Acceptance Test - UAT) senaryolarını içermektedir.

UAT süreci, sistemin son kullanıcı beklentilerine ve iş kurallarına uygun şekilde çalıştığının doğrulanmasını hedefler.

---

# UAT Senaryoları

| UAT ID  | Senaryo                                                         | Beklenen Sonuç                                                        |
| ------- | --------------------------------------------------------------- | --------------------------------------------------------------------- |
| UAT-001 | Kullanıcı geçerli bilgilerle yeni bir sipariş oluşturur.        | Sipariş başarıyla oluşturulur ve kullanıcıya onay bilgisi gösterilir. |
| UAT-002 | Kullanıcı kendi siparişlerini görüntüler.                       | Kullanıcıya yalnızca kendisine ait siparişler listelenir.             |
| UAT-003 | Kullanıcı belirli bir siparişin detayını görüntüler.            | Seçilen siparişe ait bilgiler doğru şekilde görüntülenir.             |
| UAT-004 | Kullanıcı iptal edilebilir durumdaki bir siparişi iptal eder.   | Sipariş başarıyla iptal edilir ve güncel durum görüntülenir.          |
| UAT-005 | Kullanıcı bulunmayan bir siparişi görüntülemeye çalışır.        | Kullanıcıya uygun hata mesajı gösterilir.                             |
| UAT-006 | Kimliği doğrulanmamış kullanıcı API servisine erişmeye çalışır. | Erişim reddedilir ve yetkilendirme hatası döndürülür.                 |

---

# Kabul Kriterleri

Bir UAT senaryosu aşağıdaki koşullar sağlandığında başarılı kabul edilir.

* İş gereksinimleri eksiksiz karşılanmalıdır.
* İş kuralları doğru uygulanmalıdır.
* Kullanıcıya doğru ve tutarlı sonuç gösterilmelidir.
* Beklenen hata durumlarında uygun mesajlar sunulmalıdır.
* Sistem beklenen iş akışını desteklemelidir.

---

# UAT Sonucu

UAT sürecinin başarıyla tamamlanması, sistemin iş gereksinimlerini karşıladığını ve canlı kullanıma hazır olduğunu gösterir.
