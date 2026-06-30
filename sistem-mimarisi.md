# Sistem Mimarisi

LearnEng uygulaması frontend, backend ve veritabanı olmak üzere üç ana katmandan oluşmaktadır. Bu mimari yapı sayesinde kullanıcı arayüzü, sunucu işlemleri ve veri saklama süreçleri birbirinden ayrılmıştır.

## Genel Mimari Yapı

Uygulamanın genel çalışma yapısı aşağıdaki gibidir:

```text
Kullanıcı
   ↓
Angular Frontend
   ↓
Node.js / Express Backend
   ↓
PostgreSQL Veritabanı
