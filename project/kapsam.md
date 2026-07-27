# Proje Kapsamı

## Amaç

Bu doküman, REST API İş Analizi projesinin kapsamını tanımlamak amacıyla hazırlanmıştır. Proje kapsamında yer alan süreçler, kapsam dışındaki konular, varsayımlar ve kısıtlar bu dokümanda belirtilmektedir.

---

# Kapsam Dahilindeki Süreçler

Bu proje aşağıdaki REST API servislerinin analiz ve dokümantasyon çalışmalarını kapsamaktadır:

* Sipariş oluşturma
* Sipariş listeleme
* Sipariş detayını görüntüleme
* Sipariş iptal etme

Her servis için aşağıdaki analiz çıktıları hazırlanacaktır:

* İş gereksinimleri
* Fonksiyonel gereksinimler
* İş kuralları
* API endpoint tanımları
* Request ve Response yapıları
* HTTP durum kodları
* Hata senaryoları
* OpenAPI (Swagger) dokümantasyonu
* API test senaryoları

---

# Kapsam Dışındaki Konular

Aşağıdaki konular bu projenin kapsamı dışındadır:

* Backend uygulamasının geliştirilmesi
* Frontend kullanıcı arayüzünün geliştirilmesi
* Veritabanının fiziksel olarak oluşturulması
* Gerçek ödeme sistemleri ile entegrasyon
* Kargo ve lojistik entegrasyonları
* Canlı ortama dağıtım (Deployment)

---

# Varsayımlar

Bu proje hazırlanırken aşağıdaki varsayımlar esas alınmıştır:

* Kullanıcı sisteme giriş yapmış ve kimliği doğrulanmıştır.
* Ürün bilgileri sistemde kayıtlıdır.
* Siparişe eklenecek ürünlerin stok bilgileri günceldir.
* API servisleri REST mimarisine uygun olarak geliştirilecektir.

---

# Kısıtlar

Proje aşağıdaki kısıtlar çerçevesinde hazırlanmıştır:

* Çalışma yalnızca örnek bir e-ticaret sipariş yönetimi senaryosunu kapsamaktadır.
* Dokümantasyon eğitim ve portfolyo amacıyla hazırlanmıştır.
* API örnekleri gerçek bir kurumun sistemini temsil etmemektedir.
