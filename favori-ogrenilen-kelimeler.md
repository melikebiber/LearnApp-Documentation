# Favori ve Öğrenilen Kelimeler

LearnEng uygulamasında kullanıcıların kelimelerle daha kişisel şekilde çalışabilmesi için favori kelime ve öğrenilen kelime sistemleri geliştirilmiştir.

## Favori Kelimeler

Favori kelimeler sistemi, kullanıcının önemli gördüğü veya tekrar çalışmak istediği kelimeleri kaydetmesini sağlar.

Kullanıcı kelime pratiği sırasında bir kelimeyi favorilere ekleyebilir. Bu bilgi `user_favorite_words` tablosuna kaydedilir.

## Favori Kelimelerin Kullanım Amacı

Favori kelime sistemi sayesinde kullanıcı daha sonra tekrar etmek istediği kelimelere kolayca ulaşabilir.

Bu özellik özellikle zorlanılan veya önemli görülen kelimelerin tekrar edilmesi için faydalıdır.

## Öğrenilen Kelimeler

Öğrenilen kelime sistemi, kullanıcının öğrendiğini düşündüğü kelimeleri işaretlemesini sağlar.

Kullanıcı kelime kartında bulunan **Öğrendim** butonuna tıkladığında bu kelime kullanıcı için öğrenilmiş olarak kaydedilir.

## Öğrenilen Kelimelerin Kaydedilmesi

Öğrenilen kelimeler `user_learned_words` tablosunda saklanır. Bu tabloda kullanıcı ID ve kelime ID bilgileri bulunur.

Aynı kelime aynı kullanıcı için tekrar tekrar kaydedilmez. Böylece öğrenilen kelime sayısı doğru şekilde takip edilir.

## Profil ve İlerleme Sayfalarındaki Kullanımı

Öğrenilen kelime sayısı kullanıcının profil sayfasında gösterilir. Ayrıca ilerleme sayfasında seviye bazında öğrenilen kelime sayıları da görüntülenir.

Öğrenilen kelimeler seviye ilerleme hesabına dahil edilir. Bu sayede kullanıcı kelime öğrendikçe seviyesinde ilerleme sağlayabilir.

## Kullanıcıya Katkısı

Favori ve öğrenilen kelime sistemleri, kullanıcının öğrenme sürecini kişiselleştirir. Kullanıcı hem tekrar etmek istediği kelimeleri saklayabilir hem de öğrendiği kelimeleri takip edebilir.

Bu yapı, uygulamanın kullanıcıya özel bir öğrenme deneyimi sunmasını sağlar.
