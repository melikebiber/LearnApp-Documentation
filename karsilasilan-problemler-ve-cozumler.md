# Karşılaşılan Problemler ve Çözümler

LearnEng uygulamasının geliştirme sürecinde hem arayüz tasarımı hem de uygulama işleyişiyle ilgili çeşitli problemlerle karşılaşılmıştır. Bu problemler geliştirme sürecinin doğal bir parçası olarak değerlendirilmiş ve uygun çözümler uygulanmıştır.

## 1. Sayfalar Arası Yönlendirme Problemleri

Uygulama geliştirilirken bazı sayfalara geçişlerde yönlendirme sorunları yaşanmıştır. Özellikle modüller, quiz sayfası, kelime pratiği ve seviye bazlı sayfalar arasında geçişlerde route tanımlamalarının doğru yapılması gerekmiştir.

### Çözüm

Angular routing yapısı düzenlenmiş ve her sayfa için uygun path tanımlamaları yapılmıştır. Böylece kullanıcıların ana sayfadan ilgili modüllere sorunsuz şekilde geçiş yapması sağlanmıştır.

## 2. Component Yapısı ile İlgili Problemler

Uygulamada farklı öğrenme modülleri ayrı component yapılarıyla geliştirildiği için bazı dosya yolları ve import işlemlerinde hatalar oluşmuştur.

### Çözüm

Component dosyalarının bulunduğu klasörler kontrol edilmiş, gerekli import yolları düzenlenmiş ve sayfaların doğru component üzerinden çalışması sağlanmıştır.

## 3. Arayüz Düzeni Problemleri

İlk tasarım aşamasında bazı yazıların okunabilirliği ve ekran düzeni yeterince iyi görünmemiştir. Özellikle renk uyumu, yazı boyutu ve kart yapılarında düzenleme ihtiyacı oluşmuştur.

### Çözüm

CSS düzenlemeleri yapılarak yazıların daha okunabilir olması sağlanmıştır. Kart yapıları, butonlar, renk geçişleri ve boşluklar yeniden düzenlenerek daha modern ve kullanıcı dostu bir görünüm elde edilmiştir.

## 4. Seviye Bazlı İçerik Gösterimi

Uygulamada A1, A2, B1 ve B2 seviyelerine göre farklı içeriklerin gösterilmesi sırasında içeriklerin doğru seviyeye göre ayrılması gerekmiştir.

### Çözüm

Seviye bilgisi route üzerinden alınarak ilgili sayfalarda bu seviyeye göre içerik gösterimi sağlanmıştır. Böylece kullanıcı seçtiği seviyeye uygun alıştırmalara yönlendirilmiştir.

## 5. Quiz Sistemi Değerlendirme Problemleri

Quiz sisteminde kullanıcının verdiği cevapların doğru veya yanlış olarak değerlendirilmesi ve sonuca yansıtılması aşamasında mantıksal kontrollerin doğru yapılması gerekmiştir.

### Çözüm

Sorular, seçenekler ve doğru cevap bilgileri düzenli bir yapı içinde tanımlanmıştır. Kullanıcı cevabı ile doğru cevap karşılaştırılarak quiz sonucunun hesaplanması sağlanmıştır.

## 6. Favori Kelime Yapısı

Kullanıcının tekrar etmek istediği kelimeleri favorilere ekleyebilmesi için kelime verilerinin düzenli tutulması gerekmiştir.

### Çözüm

Favori kelime mantığı ayrı bir bölüm olarak ele alınmış ve kullanıcının öğrendiği veya önemli gördüğü kelimelere daha sonra ulaşabilmesi hedeflenmiştir.

## 7. İlerleme Takip Sistemi

Kullanıcının öğrenme sürecini takip edebilmesi için quiz sonuçları ve tamamlanan çalışmaların anlamlı şekilde gösterilmesi gerekmiştir.

### Çözüm

İlerleme takip sistemi, kullanıcının yaptığı çalışmaları ve quiz performansını temel alacak şekilde planlanmıştır. Böylece kullanıcı hangi seviyede ne kadar ilerlediğini görebilmektedir.

## Genel Değerlendirme

Karşılaşılan problemler, uygulamanın daha düzenli ve işlevsel hale gelmesini sağlamıştır. Geliştirme sürecinde yapılan düzenlemeler sonucunda LearnEng uygulamasının temel yapısı daha anlaşılır, kullanılabilir ve geliştirilebilir bir hale getirilmiştir.
