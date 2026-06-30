# Sistem Mimarisi

LearnEng uygulaması frontend, backend ve veritabanı olmak üzere üç ana katmandan oluşmaktadır. Bu mimari yapı sayesinde kullanıcı arayüzü, sunucu işlemleri ve veri saklama süreçleri birbirinden ayrılmıştır.

## Genel Mimari Yapı

Uygulamanın genel çalışma yapısı aşağıdaki gibidir:

    Kullanıcı
       ↓
    Angular Frontend
       ↓
    Node.js / Express Backend
       ↓
    PostgreSQL Veritabanı

Kullanıcı, Angular ile geliştirilen arayüz üzerinden işlem yapar. Frontend tarafı, gerekli verileri backend API endpointlerine istek göndererek alır. Backend ise PostgreSQL veritabanı ile iletişim kurarak verileri işler ve frontend tarafına JSON formatında döndürür.

## Frontend Katmanı

Frontend katmanı kullanıcı ile doğrudan etkileşim kurulan bölümdür. Bu katmanda sayfalar ve modüller Angular component yapısıyla oluşturulmuştur.

Frontend tarafında bulunan temel sayfalar şunlardır:

- Ana sayfa
- Kullanıcı giriş sayfası
- Kullanıcı kayıt sayfası
- Seviye seçimi ve modlar sayfası
- Kelime pratiği sayfası
- Grammar sayfası
- Quiz sayfası
- Reading Practice sayfası
- Listening Practice sayfası
- Favoriler sayfası
- Profil sayfası
- İlerleme sayfası

Angular tarafında her sayfa ayrı bir component olarak geliştirilmiştir. Bu yapı sayesinde uygulamadaki bölümler daha düzenli hale getirilmiş ve yeni özelliklerin eklenmesi kolaylaştırılmıştır.

## Backend Katmanı

Backend katmanı Node.js ve Express.js ile geliştirilmiştir. Bu katman, frontend tarafından gönderilen istekleri alır, veritabanı işlemlerini gerçekleştirir ve sonucu frontend tarafına döndürür.

Backend üzerinde geliştirilen temel işlemler şunlardır:

- Kullanıcı kayıt işlemi
- Kullanıcı giriş işlemi
- Kelime verilerini getirme
- Grammar konularını getirme
- Quiz sorusu oluşturma
- Reading Practice verisi getirme
- Listening Practice verisi getirme
- Favori kelime ekleme ve silme
- Öğrenilen kelime ekleme ve silme
- Quiz sonucu kaydetme
- Reading sonucu kaydetme
- Listening sonucu kaydetme
- Grammar ilerlemesi kaydetme
- Kullanıcı profil özetini getirme
- Kullanıcı ilerleme özetini hesaplama

Backend, frontend ve veritabanı arasındaki iletişimi sağlayan ana katmandır. Frontend doğrudan veritabanına bağlanmaz. Tüm veri işlemleri backend üzerinden gerçekleştirilir.

## Veritabanı Katmanı

Veritabanı katmanında PostgreSQL kullanılmıştır. Uygulamadaki tüm kalıcı veriler PostgreSQL tablolarında saklanmaktadır.

Veritabanında saklanan temel veriler şunlardır:

- Kullanıcı bilgileri
- İngilizce kelimeler
- Grammar konu anlatımları
- Grammar alıştırmaları
- Quiz soruları
- Reading Practice metinleri
- Listening Practice metinleri
- Favori kelimeler
- Öğrenilen kelimeler
- Quiz sonuçları
- Grammar ilerleme kayıtları
- Reading sonuçları
- Listening sonuçları

Kullanıcıya özel veriler `user_id` alanı ile kullanıcı tablosuna bağlanmıştır. Böylece her kullanıcının öğrenme verileri ayrı şekilde saklanır.

## Veri Akışı

Uygulamadaki genel veri akışı şu şekildedir:

1. Kullanıcı Angular arayüzünde bir işlem yapar.
2. Frontend, ilgili backend API endpointine istek gönderir.
3. Backend isteği alır ve gerekli kontrolleri yapar.
4. Backend PostgreSQL veritabanı ile iletişime geçer.
5. Veriler alınır, kaydedilir veya güncellenir.
6. Backend sonucu JSON formatında frontend tarafına döndürür.
7. Frontend gelen veriyi kullanıcı arayüzünde gösterir.

Örneğin kullanıcı bir kelimeyi öğrenildi olarak işaretlediğinde, frontend bu bilgiyi backend tarafına gönderir. Backend ilgili kullanıcı ve kelime bilgisini `user_learned_words` tablosuna kaydeder. Daha sonra bu bilgi profil ve ilerleme sayfalarında kullanılabilir.

## Örnek İşlem Akışı

Kelime pratiği modülünde örnek bir işlem akışı şu şekildedir:

1. Kullanıcı seviye seçer.
2. Kelime pratiği modülüne girer.
3. Frontend backend tarafına seviyeye uygun kelime isteği gönderir.
4. Backend `words` tablosundan uygun kelimeleri getirir.
5. Kullanıcı kelimeyi favorilere ekleyebilir veya öğrenildi olarak işaretleyebilir.
6. Bu bilgiler kullanıcıya özel olarak veritabanına kaydedilir.
7. Kaydedilen veriler profil ve ilerleme sistemine yansıtılır.

## İlerleme Sistemi Akışı

İlerleme takip sistemi birden fazla tablodan gelen verileri birlikte değerlendirir.

İlerleme hesabında kullanılan veriler şunlardır:

- Quiz sonuçları
- Öğrenilen kelime sayısı
- Grammar çalışma kayıtları
- Reading Practice sonuçları
- Listening Practice sonuçları

Backend, bu verileri veritabanından çeker ve her seviye için genel ilerleme yüzdesini hesaplar. Hesaplanan değerler frontend tarafına gönderilir ve kullanıcı ilerleme sayfasında görüntüler.

## Mimari Yapının Avantajları

Bu mimari yapı sayesinde uygulama daha düzenli ve geliştirilebilir hale gelmiştir.

Mimari yapının sağladığı avantajlar şunlardır:

- Frontend ve backend birbirinden ayrılmıştır.
- Veritabanı işlemleri merkezi olarak yönetilir.
- Yeni modüller sisteme daha kolay eklenebilir.
- Kullanıcıya özel veriler düzenli şekilde saklanabilir.
- API yapısı sayesinde frontend ve backend iletişimi daha kontrollü olur.
- Uygulama daha sürdürülebilir bir yapıya sahip olur.

## Genel Değerlendirme

LearnEng uygulamasının sistem mimarisi, modern web uygulamalarında kullanılan katmanlı yapı temel alınarak hazırlanmıştır. Angular frontend kullanıcı arayüzünü oluştururken, Node.js ve Express.js backend işlemlerini yönetir. PostgreSQL ise uygulamadaki tüm verilerin saklandığı veritabanı katmanıdır.

Bu yapı sayesinde uygulama hem kullanıcı dostu bir arayüze hem de düzenli bir veri yönetim sistemine sahip olmuştur.
