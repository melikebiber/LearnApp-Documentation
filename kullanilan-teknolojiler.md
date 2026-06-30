# Kullanılan Teknolojiler

LearnEng uygulaması geliştirilirken frontend, backend ve veritabanı katmanları birbirinden ayrılmıştır. Bu sayede uygulama daha düzenli, yönetilebilir ve geliştirilebilir bir yapıya sahip olmuştur.

## Frontend Teknolojileri

Frontend tarafında **Angular** kullanılmıştır. Angular, bileşen tabanlı yapısı sayesinde uygulama sayfalarının daha düzenli şekilde geliştirilmesini sağlamıştır.

Kullanılan frontend teknolojileri:

- Angular
- TypeScript
- HTML
- CSS
- Angular Routing
- Angular Standalone Components
- HTTP Client

Angular tarafında her özellik ayrı component yapısı ile geliştirilmiştir. Örneğin kelime pratiği, quiz, reading practice, listening practice, profil ve ilerleme sayfaları ayrı bileşenler olarak hazırlanmıştır.

## Backend Teknolojileri

Backend tarafında **Node.js** ve **Express.js** kullanılmıştır. Backend, frontend ile veritabanı arasındaki iletişimi sağlamaktadır.

Kullanılan backend teknolojileri:

- Node.js
- Express.js
- PostgreSQL bağlantısı için `pg` paketi
- CORS
- bcryptjs

Backend üzerinde kullanıcı kayıt ve giriş işlemleri, kelime verileri, quiz sonuçları, favori kelimeler, öğrenilen kelimeler ve ilerleme takip sistemi için API endpointleri oluşturulmuştur.

## Veritabanı Teknolojisi

Veritabanı olarak **PostgreSQL** kullanılmıştır. PostgreSQL üzerinde kullanıcı bilgileri, kelimeler, grammar konuları, reading ve listening içerikleri, quiz sonuçları ve kullanıcı ilerleme verileri saklanmaktadır.

Veritabanı tabloları ilişkisel şekilde tasarlanmıştır. Kullanıcıya özel veriler `user_id` alanı üzerinden kullanıcı tablosu ile ilişkilendirilmiştir.

## Kullanılan Geliştirme Araçları

Projede kullanılan geliştirme araçları şunlardır:

- Visual Studio Code
- PostgreSQL / pgAdmin
- GitHub
- GitBook
- Node Package Manager
- Tarayıcı geliştirici araçları

## Genel Teknoloji Yapısı

Uygulama genel olarak üç temel katmandan oluşmaktadır:

1. **Frontend:** Kullanıcı arayüzü ve sayfa işlemleri
2. **Backend:** API işlemleri ve sunucu tarafı mantığı
3. **Veritabanı:** Kullanıcı ve içerik verilerinin saklanması

Bu yapı sayesinde uygulama modüler, geliştirilebilir ve sürdürülebilir hale getirilmiştir.
