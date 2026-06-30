# Quiz Sistemi

Quiz Sistemi, kullanıcının kelime ve grammar bilgisini ölçmek amacıyla geliştirilmiştir. Kullanıcı seçtiği seviyeye göre quiz soruları çözer ve sonuçları veritabanına kaydedilir.

## Modülün Amacı

Quiz sisteminin amacı, kullanıcının öğrendiği bilgileri test etmesini sağlamaktır. Quizler sayesinde kullanıcı kendi seviyesindeki kelime ve dil bilgisi bilgisini ölçebilir.

## Quiz Yapısı

Quiz soruları seviyeye göre oluşturulur. Kullanıcıya soru ve dört seçenek sunulur. Kullanıcı bir seçenek işaretlediğinde cevap kontrol edilir ve doğru cevap bilgisi gösterilir.

Quiz sistemi, kullanıcıya anlık geri bildirim vererek öğrenme sürecini destekler.

## Karma Quiz

Uygulamada karma quiz yapısı kullanılmıştır. Bu yapı sayesinde quizlerde hem kelime hem de grammar soruları yer alabilir.

Bu yaklaşım kullanıcının yalnızca tek bir alanda değil, farklı İngilizce becerilerinde kendini test etmesini sağlar.

## Sonuç Kaydetme

Kullanıcı quiz tamamladığında sonuç backend üzerinden `quiz_results` tablosuna kaydedilir.

Kaydedilen bilgiler şunlardır:

- Kullanıcı ID
- Seviye
- Quiz türü
- Toplam soru sayısı
- Doğru cevap sayısı
- Başarı yüzdesi
- Oluşturulma tarihi

## İlerleme Sistemindeki Rolü

Quiz sonuçları seviye ilerleme sisteminde önemli bir rol oynar. Kullanıcının doğru cevap sayısı, genel seviye ilerlemesinin hesaplanmasında kullanılır.

LearnEng uygulamasında quiz başarısı genel seviye ilerlemesine belirli bir ağırlıkla katkı sağlar. Ancak seviye ilerlemesi yalnızca quiz sonucuna bağlı değildir. Kelime, grammar, reading ve listening çalışmaları da ilerleme hesabına dahil edilir.

## Kullanıcıya Katkısı

Quiz sistemi kullanıcının öğrendiği bilgileri test etmesini sağlar. Kullanıcı eksik olduğu alanları fark edebilir ve tekrar çalışması gereken konulara yönelebilir.

Bu modül, öğrenilen bilgilerin ölçülmesi ve kullanıcının gelişiminin takip edilmesi açısından önemli bir bölümdür.
