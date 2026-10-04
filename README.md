# dalgalar

Teknoloji bağımsız, etkileşimli fizik eğitim sayfaları.

## İçerik

- Dalga nasıl oluşur?
- 1B, 2B ve 3B dalga yayılımı ve dalga cepheleri
- Dalga enerjisi, güç ve şiddet; genlik/frekans/uzaklık ilişkileri
- Diyapazon ve anten için sayısal enerji → güç → şiddet örnekleri
- Mekanik dalgalar ve kaynakları
- Diyapazon
- Sesin gaz, sıvı ve katıda yayılması
- Elektromanyetik dalgaların oluşumu ve kaynakları
- Elektromanyetik spektrum
- Antenlerin çalışma mantığı
- EM dalgaların boşluk, hava, su ve katılardaki yayılımı
- Mekanik / elektromanyetik dalga karşılaştırması
- Etkileşimli mini test

## Sayfalar

- `index.html` — ana eğitim sayfası
- `2d.html` — iki koherent kaynağın 2B girişim, bileşke genlik ve göreli şiddet simülasyonu
- `3d.html` — iki koherent küresel kaynağın 3B hacim girişim simülasyonu
- `yuzey.html` — RF, mikrodalga, görünür ve X-ışını için makroskopik yüzey/kalınlık/yansıma simülasyonu
- `mikro.html` — farklı malzeme ve frekanslarda kolektif alan, yansıma, yeniden yayım ve sönümü mikro ölçekte gösteren simülasyon
- `nano.html` — silisyum ağırlıklı elektron/hol, bağlı elektron polarizasyonu, iç EM alan ve bant geçişlerini nano ölçekte gösteren simülasyon
- `txrx.html` — 3B TX/RX anten bağlantısı, çubuk/dipol omni + patch + yönlü desenler, çift TX coherent/incoherent girişim, Friis link bütçesi ve RX analiz simülasyonu

Tüm sayfalar vanilla HTML/CSS/JavaScript ile çalışır ve harici kütüphane gerektirmez.


## Nano fizik modeli

`nano.html` frekans ve malzemeye bağlı zayıflamayı içerir. Görünümde güç/şiddet için
`I(z)=I0 exp(-z/Lp)`, klasik alan genliği için `E(z)=E0 exp(-z/(2Lp))` kullanılır.
10 keV X-ışını modu klasik sinüzoidal alan yerine azalan foton akısı ve etkileşim olayları
olarak gösterilir. 10 keV X-ışını zayıflama değerleri NIST XCOM tabanlıdır; diğer
presetler öğretici temsilî değerler olarak arayüzde etiketlenir.


- `rssi.html` — RSSI, log-distance path loss, iki-yol fading ve zaman serisi simülasyonu
- `csi.html` — OFDM CSI kompleks kanal cevabı, alt taşıyıcı genlik/fazı ve gecikme profili simülasyonu
