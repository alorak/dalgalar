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

`nano.html` frekans ve malzemeye bağlı yüzey yansımasını ve zayıflamayı içerir.

- RF/mikrodalgada kırılma indisi kompleks dielektrik fonksiyonundan hesaplanır (`N=√ε`):
  Si için `ε=11.7+iσ/(ωε0)`, `σ=q(nμn+pμp)` (kütle-etki yasası + Caughey–Thomas mobilite,
  katkı tipi ve yoğunluğu seçilebilir), Cu için `ε=1+iσ/(ωε0)`, cam için `ε′≈4.6, tanδ≈3.7e-3`,
  su için Debye modeli (25 °C, τ=8.27 ps). Görünür ve 10 keV X-ışını değerleri ölçülmüş
  `n` ve 1/e güç uzunluğu `Lp`'den (`κ=λ/4πLp`) gelir; X-ışını zayıflaması NIST XCOM tabanlıdır.
- Yüzeyde Fresnel `rs, rp, ts, tp` hesaplanır. İçerideki dalganın normal bileşeni
  `kz=k0√(N²−sin²θ)` ile güç `I(z)=I0 exp(-z/L⊥)`, `L⊥=λ/(4π Im(kz/k0))` olarak azalır; bu
  ifade X-ışını total external reflection bölgesindeki evanescent alanı da süreksizlik olmadan verir.
- İç alan `|t|` ile çizilir, faz yüzeyde süreklidir (yansıyan `arg r`, iletilen `arg t`) ve dalga boyu
  fiziksel derinlik eksenine bağlıdır (çok sıksa n oranı korunarak seyreltilir).
- Yükler alanın enine yönünde salınır: serbest taşıyıcılar Drude (`ωτ` ile faz), bağlı elektronlar
  rezonans altı Lorentz, su dipolleri Debye gecikmesiyle (görünürde yönelim donar).

- `rssi.html` — RSSI, log-distance path loss, iki-yol fading ve zaman serisi simülasyonu
- `csi.html` — OFDM CSI kompleks kanal cevabı, alt taşıyıcı genlik/fazı ve gecikme profili simülasyonu
