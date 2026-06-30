# İlerleme Takip Sistemi

LearnEng uygulamasında kullanıcıların öğrenme sürecini takip edebilmesi için çoklu veriye dayalı bir ilerleme sistemi geliştirilmiştir.

## Sistemin Amacı

İlerleme takip sisteminin amacı, kullanıcının yalnızca quiz başarısını değil, uygulama içindeki farklı öğrenme aktivitelerini de dikkate alarak daha gerçekçi bir seviye ilerlemesi hesaplamaktır.

İlk aşamada seviye ilerlemesi yalnızca quiz sonuçlarına göre düşünülmüştür. Ancak İngilizce öğrenme süreci yalnızca test çözmekten ibaret olmadığı için sistem geliştirilmiş ve farklı modüllerden gelen veriler ilerleme hesabına dahil edilmiştir.

## Kullanılan Veriler

Seviye ilerlemesi hesaplanırken aşağıdaki veriler dikkate alınır:

- Quiz doğru cevap sayısı
- Öğrenilen kelime sayısı
- Çalışılan grammar konu sayısı
- Tamamlanan Reading Practice sayısı
- Tamamlanan Listening Practice sayısı

Bu veriler sayesinde kullanıcıların uygulamadaki genel öğrenme davranışları daha kapsamlı şekilde değerlendirilir.

## İlerleme Hesaplama Mantığı

Genel seviye ilerlemesi beş farklı öğrenme alanının ağırlıklı ortalaması ile hesaplanır.

Kullanılan ağırlıklar:

```text
Quiz başarısı: %35
Öğrenilen kelime: %25
Grammar çalışması: %20
Reading Practice: %10
Listening Practice: %10
