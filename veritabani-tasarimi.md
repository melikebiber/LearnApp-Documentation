# Veritabanı Tasarımı

LearnEng uygulamasında veritabanı olarak PostgreSQL kullanılmıştır. Veritabanı tasarımı, kullanıcıya özel verilerin saklanabilmesi ve uygulamadaki öğrenme aktivitelerinin takip edilebilmesi amacıyla ilişkisel bir yapıda hazırlanmıştır.

## Veritabanının Genel Amacı

Veritabanı aşağıdaki verileri saklamak için kullanılmaktadır:

- Kullanıcı bilgileri
- İngilizce kelimeler
- Grammar konu anlatımları
- Grammar alıştırmaları
- Quiz sonuçları
- Reading Practice içerikleri
- Listening Practice içerikleri
- Favori kelimeler
- Öğrenilen kelimeler
- Kullanıcı ilerleme kayıtları

## Temel Tablolar

Projede kullanılan temel tablolar şunlardır:

- `users`
- `words`
- `grammar_topics`
- `grammar_questions`
- `grammar_exercises`
- `reading_practices`
- `listening_practices`
- `user_favorite_words`
- `user_learned_words`
- `quiz_results`
- `grammar_progress`
- `reading_results`
- `listening_results`

## Users Tablosu

`users` tablosu kullanıcı kayıt bilgilerini saklamak için kullanılmıştır. Bu tabloda kullanıcı adı, e-posta adresi, şifre ve kayıt tarihi bilgileri tutulur.

Kullanıcı şifreleri doğrudan metin olarak saklanmaz. Backend tarafında `bcryptjs` kullanılarak şifrelenmiş şekilde veritabanına kaydedilir.

## Words Tablosu

`words` tablosu İngilizce kelime içeriklerini saklar. Her kelime bir seviyeye ve kategoriye sahiptir.

Bu tabloda yer alan temel alanlar:

- Seviye
- Kategori
- İngilizce kelime
- Türkçe karşılık

Kelime pratiği ve quiz sistemi bu tablodaki verilerden yararlanır.

## Grammar Tabloları

Grammar sistemi için üç farklı tablo kullanılmıştır:

- `grammar_topics`
- `grammar_questions`
- `grammar_exercises`

`grammar_topics` tablosu grammar konu anlatımlarını saklar.

`grammar_questions` tablosu quizlerde kullanılan grammar sorularını saklar.

`grammar_exercises` tablosu konu bazlı grammar alıştırmalarını saklar.

## Reading ve Listening Tabloları

Reading Practice modülü için `reading_practices` tablosu kullanılmıştır. Bu tabloda seviye, başlık, metin, anahtar kelimeler ve sorular yer almaktadır.

Listening Practice modülü için `listening_practices` tablosu kullanılmıştır. Bu tabloda dinleme metni, soru, seçenekler, doğru cevap ve açıklama bilgileri bulunmaktadır.

## Favori ve Öğrenilen Kelime Tabloları

Kullanıcıların favori kelimeleri `user_favorite_words` tablosunda saklanır.

Kullanıcının öğrendiğini işaretlediği kelimeler ise `user_learned_words` tablosunda saklanır.

Bu iki tabloda `user_id` ve `word_id` alanları kullanılarak kullanıcı ile kelime arasında ilişki kurulmuştur.

## Quiz Sonuçları Tablosu

`quiz_results` tablosu kullanıcının çözdüğü quiz sonuçlarını saklar. Bu tabloda seviye, quiz türü, toplam soru sayısı, doğru cevap sayısı ve başarı yüzdesi bilgileri yer alır.

Bu tablo, ilerleme takip sisteminin önemli bir parçasıdır.

## İlerleme Takip Tabloları

Kullanıcının farklı öğrenme aktivitelerini takip etmek için aşağıdaki tablolar kullanılmıştır:

- `grammar_progress`
- `reading_results`
- `listening_results`

`grammar_progress` tablosu kullanıcının çalıştığı grammar konularını tutar.

`reading_results` tablosu kullanıcının tamamladığı reading etkinliklerini kaydeder.

`listening_results` tablosu kullanıcının tamamladığı listening etkinliklerini kaydeder.

## İlişkisel Yapı

Kullanıcıya ait veriler `user_id` alanı ile `users` tablosuna bağlanmaktadır. Bu sayede her kullanıcının favori kelimeleri, öğrendiği kelimeler, quiz sonuçları ve ilerleme verileri kişiye özel olarak saklanır.

Bu yapı, uygulamanın çok kullanıcılı bir sisteme uygun şekilde çalışmasını sağlar.

## Genel Değerlendirme

Veritabanı tasarımı, uygulamanın kullanıcıya özel öğrenme takibi yapabilmesini sağlayacak şekilde hazırlanmıştır. Kullanıcıların öğrenme sürecinde oluşturduğu veriler ayrı tablolarda saklanarak hem düzenli hem de geliştirilebilir bir yapı elde edilmiştir.
