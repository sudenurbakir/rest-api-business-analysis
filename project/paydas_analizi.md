# Paydaş Analizi

## Amaç

Bu doküman, REST API İş Analizi projesinde yer alan paydaşları, projedeki rollerini ve projeye olan etki düzeylerini belirlemek amacıyla hazırlanmıştır.

Paydaşların doğru analiz edilmesi; gereksinim toplama, karar alma süreçleri ve proje iletişiminin etkin şekilde yürütülmesi açısından önemlidir.

---

# Paydaş Listesi

| Paydaş             | Rol                  | Projedeki Sorumluluğu                                             |
| ------------------ | -------------------- | ----------------------------------------------------------------- |
| Product Owner      | İş Birimi Temsilcisi | İş ihtiyaçlarını belirler ve gereksinimleri onaylar.              |
| Business Analyst   | Analiz               | İş gereksinimlerini analiz eder ve API dokümantasyonunu hazırlar. |
| Backend Developer  | Yazılım Geliştirme   | API servislerini geliştirir.                                      |
| Frontend Developer | Yazılım Geliştirme   | API servislerini kullanıcı arayüzüne entegre eder.                |
| QA (Test Uzmanı)   | Test                 | API servislerini test eder ve doğrular.                           |
| DevOps Engineer    | Operasyon            | API'nin dağıtım ve yayın süreçlerini yönetir.                     |

---

# Güç - İlgi Matrisi

| Paydaş             | Güç Düzeyi | İlgi Düzeyi | Yönetim Yaklaşımı                                                 |
| ------------------ | ---------- | ----------- | ----------------------------------------------------------------- |
| Product Owner      | Yüksek     | Yüksek      | Sürekli iletişim kurulmalıdır.                                    |
| Business Analyst   | Yüksek     | Yüksek      | Sürecin tamamında aktif rol alır.                                 |
| Backend Developer  | Orta       | Yüksek      | Teknik gereksinimler düzenli paylaşılmalıdır.                     |
| Frontend Developer | Orta       | Orta        | API değişiklikleri hakkında bilgilendirilmelidir.                 |
| QA                 | Orta       | Yüksek      | Gereksinimler ve test senaryoları birlikte gözden geçirilmelidir. |
| DevOps Engineer    | Düşük      | Orta        | Yayın planı ve teknik ihtiyaçlar paylaşılmalıdır.                 |

---

# İletişim Yaklaşımı

Proje boyunca paydaşlar arasında düzenli iletişim kurulması hedeflenmektedir.

* İş gereksinimleri Product Owner ile doğrulanacaktır.
* Teknik analizler geliştirici ekip ile paylaşılacaktır.
* Test senaryoları QA ekibi ile birlikte değerlendirilecektir.
* API değişiklikleri ilgili tüm paydaşlara duyurulacaktır.
