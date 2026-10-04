# Günlük Arpej

Telefonda günlük vokal çalışması için küçük bir web uygulaması.
Ton ve tempoyu seç, akoru dinle, arpeji söyle.

- 5 gam: majör, doğal minör, frijyan, melodik minör, harmonik minör
- 11 kalıp: arpejler, gamlar, uzun ses, siren
- Akor tam olarak seçilen tempoda çalar (2 / 4 / 8 vuruş), kalıp bir sonraki vuruşta girer
- Transpoze: çıkarak / inerek / çık-in, yarım veya tam ses adımlarla
- Çevrimdışı çalışır (service worker), ana ekrana eklenince tam ekran açılır

## iPhone'a kurmak

1. Safari'de yayınlanan adresi aç
2. Paylaş → **Ana Ekrana Ekle**
3. Ana ekrandaki ikondan aç — Safari çubuğu olmadan, tam ekran açılır

## Dosyalar

| Dosya | İşi |
|---|---|
| `index.html` | Uygulamanın tamamı (arayüz + Web Audio ses motoru) |
| `manifest.webmanifest` | Uygulama adı, ikonlar, tam ekran ayarı |
| `sw.js` | Çevrimdışı önbellek |
| `icon-*.png` | Ana ekran ve uygulama ikonları |
