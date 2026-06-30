# Kullanıcı Kayıt ve Giriş Sistemi

LearnEng uygulamasında kullanıcıya özel öğrenme verilerinin saklanabilmesi için kayıt ve giriş sistemi geliştirilmiştir. Bu sistem sayesinde her kullanıcının favori kelimeleri, öğrendiği kelimeler, quiz sonuçları ve ilerleme bilgileri ayrı olarak tutulur.

## Kayıt Sistemi

Kullanıcı kayıt olurken aşağıdaki bilgileri girer:

- Kullanıcı adı
- E-posta adresi
- Şifre

Kayıt işlemi sırasında backend tarafında girilen bilgilerin boş olup olmadığı kontrol edilir. Ayrıca aynı e-posta adresi ile daha önce kayıt yapılmışsa kullanıcıya hata mesajı döndürülür.

## Şifre Güvenliği

Kullanıcı şifreleri veritabanına doğrudan metin olarak kaydedilmez. Şifreler backend tarafında `bcryptjs` kütüphanesi ile şifrelenerek saklanır.

Bu sayede veritabanında kullanıcı şifrelerinin açık şekilde tutulması engellenmiştir.

## Giriş Sistemi

Kullanıcı giriş yaparken e-posta adresi ve şifresini girer. Backend tarafında önce e-posta adresinin kayıtlı olup olmadığı kontrol edilir. Daha sonra kullanıcının girdiği şifre ile veritabanındaki şifrelenmiş şifre karşılaştırılır.

Şifre doğruysa giriş işlemi başarılı olur ve kullanıcı bilgileri frontend tarafına gönderilir.

## Kullanıcı Bilgisinin Saklanması

Giriş yapan kullanıcının bilgileri frontend tarafında `localStorage` içinde saklanır. Böylece kullanıcı uygulama içinde farklı sayfalara geçtiğinde kullanıcı bilgisi korunur.

Bu bilgi özellikle şu işlemlerde kullanılır:

- Favori kelime ekleme
- Öğrenilen kelime işaretleme
- Quiz sonucunu kaydetme
- Reading sonucunu kaydetme
- Listening sonucunu kaydetme
- Grammar ilerlemesini kaydetme
- Profil ve ilerleme bilgilerini getirme

## Kullanıcıya Özel Veri Yapısı

Uygulamada kullanıcıya ait tüm ilerleme ve öğrenme verileri `user_id` ile ilişkilendirilmiştir. Böylece farklı kullanıcılar aynı uygulamayı kullansa bile her kullanıcının verileri ayrı ayrı saklanır.

Örneğin bir kullanıcı A1 seviyesinde 10 kelime öğrenmişse bu bilgi sadece o kullanıcıya ait olur. Başka bir kullanıcı giriş yaptığında kendi öğrenme verilerini görür.

## Sistemin Önemi

Kullanıcı kayıt ve giriş sistemi, LearnEng uygulamasının kişiselleştirilmiş öğrenme deneyimi sunabilmesi için temel bir bileşendir. Bu sistem sayesinde uygulama yalnızca içerik gösteren bir platform olmaktan çıkarak kullanıcının gelişimini takip eden bir öğrenme uygulamasına dönüşmüştür.
