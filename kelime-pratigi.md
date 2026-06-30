# Kelime Pratiği

Kelime Pratiği modülü, kullanıcıların seviyelerine uygun İngilizce kelimeleri öğrenmelerini sağlamak amacıyla geliştirilmiştir. Bu modülde kelimeler kart yapısında sunulur ve kullanıcı kelimeler üzerinde farklı işlemler yapabilir.

## Modülün Amacı

Kelime Pratiği modülünün amacı, kullanıcının İngilizce kelime bilgisini geliştirmesini sağlamaktır. Kullanıcılar seviyelerine uygun kelimeleri görür, Türkçe karşılıklarını inceleyebilir ve kelimelerin telaffuzlarını dinleyebilir.

## Temel Özellikler

Bu modülde bulunan temel özellikler şunlardır:

- Seviyeye uygun kelime gösterimi
- İngilizce kelime ve Türkçe karşılık görüntüleme
- Kelime telaffuzu dinleme
- Kelimeyi favorilere ekleme
- Kelimeyi öğrenildi olarak işaretleme
- Öğrenilen kelime bilgisini veritabanına kaydetme

## Kelime Kartı Yapısı

Kelime pratiği sayfasında kelimeler kartlar halinde gösterilir. Her kartta İngilizce kelime, Türkçe karşılık ve kelimeyle ilgili işlem butonları bulunur.

Kullanıcı bu kartlar üzerinden kelimeyi inceleyebilir, telaffuzunu dinleyebilir, favorilere ekleyebilir veya öğrendiğini işaretleyebilir.

## Telaffuz Özelliği

Kullanıcı kelimenin telaffuzunu dinleyebilir. Bu işlem tarayıcının seslendirme özelliği kullanılarak gerçekleştirilmiştir. İngilizce kelimeler sesli şekilde okunarak kullanıcının doğru telaffuz konusunda desteklenmesi amaçlanmıştır.

## Favori Kelime Sistemi

Kullanıcı önemli gördüğü veya tekrar çalışmak istediği kelimeleri favorilere ekleyebilir. Favori kelimeler kullanıcıya özel olarak veritabanında saklanır.

Bu sayede kullanıcı daha sonra favori kelimeler sayfasından bu kelimelere tekrar ulaşabilir.

## Öğrenilen Kelime Sistemi

Kullanıcı bir kelimeyi öğrendiğini düşündüğünde kelimeyi "Öğrendim" olarak işaretleyebilir. Bu bilgi `user_learned_words` tablosuna kaydedilir.

Öğrenilen kelime sayısı profil ve ilerleme sayfalarında gösterilir. Ayrıca seviye ilerleme hesabına da dahil edilir.

## İlerleme Sistemindeki Rolü

Kelime pratiği modülünde öğrenilen olarak işaretlenen kelimeler, kullanıcının genel seviye ilerlemesine katkı sağlar.

Seviye ilerleme sisteminde öğrenilen kelime sayısı belirli bir ağırlıkla değerlendirilir. Böylece kullanıcı yalnızca quiz çözerek değil, kelime öğrenerek de seviyesinde ilerleyebilir.

## Kullanıcıya Katkısı

Kelime Pratiği modülü, kullanıcının kelime bilgisini artırırken aynı zamanda aktif öğrenme davranışını da destekler. Kullanıcı yalnızca kelime görmekle kalmaz; kelimeyi dinler, favorilere ekler ve öğrendiğini işaretleyerek kendi gelişimini takip eder.
