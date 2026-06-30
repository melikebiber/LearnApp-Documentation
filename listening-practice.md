# Listening Practice

Listening Practice modülü, kullanıcının İngilizce dinleme ve dinlediğini anlama becerisini geliştirmek amacıyla hazırlanmıştır.

## Modülün Amacı

Bu modülün amacı, kullanıcıya İngilizce kısa metinleri dinleterek metinle ilgili soruları cevaplamasını sağlamaktır. Kullanıcı metni ilk aşamada görmez, yalnızca dinler.

Bu yapı sayesinde kullanıcı gerçek bir dinleme pratiği yapar ve duyduğunu anlama becerisini geliştirir.

## Kullanım Akışı

Listening Practice modülünde kullanıcı önce **Dinle** butonuna basarak metni sesli olarak dinler. Metin ilk aşamada ekranda gösterilmez.

Ardından kullanıcıya İngilizce bir soru ve dört seçenek sunulur. Kullanıcı cevabını seçtikten sonra sistem cevabı kontrol eder.

Cevap verildikten sonra:

- Doğru veya yanlış bilgisi gösterilir.
- Doğru cevap gösterilir.
- Açıklama gösterilir.
- Dinlenen metnin yazılı hali açılır.
- Kullanıcı isterse metni tekrar dinleyebilir.

## İçerik Yapısı

Listening Practice içerikleri `listening_practices` tablosunda saklanır.

Bu tabloda aşağıdaki bilgiler yer alır:

- Seviye
- Başlık
- Dinleme metni
- Soru
- Seçenekler
- Doğru cevap
- Açıklama

## Seslendirme Sistemi

Metinler tarayıcının seslendirme özelliği kullanılarak İngilizce olarak okunur. Böylece ek bir ses dosyasına ihtiyaç duyulmadan dinleme pratiği sağlanır.

Bu özellik, kullanıcının İngilizce telaffuza aşina olmasına da katkı sağlar.

## Sonuç Kaydetme

Kullanıcı listening sorusunu cevapladığında sonuç `listening_results` tablosuna kaydedilir.

Kaydedilen bilgiler:

- Kullanıcı ID
- Seviye
- Listening ID
- Cevabın doğru olup olmadığı
- Oluşturulma tarihi

## İlerleme Sistemindeki Rolü

Listening Practice tamamlanma sayısı seviye ilerleme hesabına dahil edilir. Böylece kullanıcının dinleme çalışmaları da genel öğrenme ilerlemesine katkı sağlar.

## Kullanıcıya Katkısı

Listening Practice modülü, kullanıcının İngilizce duyduğunu anlama becerisini geliştirir. Metnin cevap verildikten sonra gösterilmesi, kullanıcının dinlediği metin ile yazılı metni karşılaştırmasını sağlar.

Bu sayede kullanıcı hem dinleme hem de okuma becerisini birlikte pekiştirir.
