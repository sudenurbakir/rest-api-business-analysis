# REST API Genel Bakış

## Amaç

Bu doküman, proje kapsamında kullanılacak REST API yaklaşımını açıklamak ve API tasarımında benimsenen temel prensipleri tanımlamak amacıyla hazırlanmıştır.

---

# REST API Nedir?

REST (Representational State Transfer), istemci (Client) ile sunucu (Server) arasında veri alışverişi yapılmasını sağlayan yaygın bir web servis mimarisidir.

Bu projede, e-ticaret sipariş yönetim süreçleri REST mimarisi esas alınarak tasarlanmıştır.

---

# REST API'nin Temel Özellikleri

* İstemci ve sunucu birbirinden bağımsız çalışır.
* İletişim HTTP protokolü üzerinden gerçekleştirilir.
* Veri alışverişinde JSON formatı kullanılır.
* Her istek bağımsızdır (Stateless).
* Kaynaklar (Resources) URL yapıları ile temsil edilir.

---

# Projede Kullanılan Temel Kavramlar

| Kavram   | Açıklama                                                       |
| -------- | -------------------------------------------------------------- |
| Client   | API'ye istek gönderen uygulama veya kullanıcı.                 |
| Server   | İstekleri işleyen ve yanıt döndüren sistem.                    |
| Resource | API üzerinden erişilen veri veya iş nesnesi (örneğin Sipariş). |
| Endpoint | Belirli bir kaynağa erişim sağlayan URL.                       |
| Request  | İstemcinin sunucuya gönderdiği istek.                          |
| Response | Sunucunun istemciye gönderdiği yanıt.                          |
| JSON     | API'de kullanılan veri alışverişi formatı.                     |

---

# REST API Tasarım Prensipleri

Bu proje kapsamında aşağıdaki REST API tasarım prensipleri benimsenmiştir.

* Endpoint isimlendirmelerinde isim (noun) kullanılır.
* URL yapıları küçük harflerle oluşturulur.
* Kaynak isimleri çoğul (plural) olarak kullanılır.
* HTTP metodları işlem amacına uygun seçilir.
* Her endpoint tek bir sorumluluğa sahip olacak şekilde tasarlanır.
* Başarılı ve hatalı işlemler için uygun HTTP durum kodları kullanılır.
* Tüm veri alışverişi JSON formatında gerçekleştirilir.

---

# Bu Projede REST API'nin Kullanım Amacı

REST API yapısı sayesinde;

* Sipariş oluşturma
* Sipariş listeleme
* Sipariş detayını görüntüleme
* Sipariş iptal etme

işlemleri standart ve tutarlı bir yapı ile gerçekleştirilecektir.

Bu yaklaşım, istemci uygulamalar ile sunucu arasında güvenilir ve sürdürülebilir bir iletişim kurulmasını desteklemektedir.
