# GitHub Pages'e koyup iPhone'a kurmak

Bu klasör hazır bir git deposu — ilk commit atıldı. Yapman gereken tek şey
GitHub'da boş bir depo açıp buradakini göndermek.

## 1. GitHub'da boş depo aç

github.com → sağ üst `+` → **New repository**

- **Repository name:** `gunluk-arpej`
- **Public** (GitHub Pages ücretsiz hesapta sadece public depoda çalışır)
- "Add a README" **işaretleme** — burada zaten var

## 2. Gönder

Aşağıdaki komutta `KULLANICI_ADIN` yerine kendi GitHub kullanıcı adını yaz:

    cd ~/Downloads/gunluk-arpej-pwa
    git remote add origin https://github.com/KULLANICI_ADIN/gunluk-arpej.git
    git branch -M main
    git push -u origin main

Şifre sorarsa: GitHub artık parola kabul etmiyor, **personal access token** istiyor.
github.com → Settings → Developer settings → Personal access tokens → Tokens (classic) →
Generate new token → `repo` yetkisi → çıkan uzun metni parola alanına yapıştır.

> Terminalle uğraşmak istemezsen: depo sayfasında **uploading an existing file**
> bağlantısına tıklayıp bu klasördeki 8 dosyayı sürükleyip bırakman da yeter.

## 3. Pages'i aç

Depo → **Settings** → sol menüde **Pages** →
**Source: Deploy from a branch**, **Branch: main**, **klasör: / (root)** → Save.

1–2 dakika sonra adres hazır olur:

    https://KULLANICI_ADIN.github.io/gunluk-arpej/

## 4. iPhone'a ekle

1. Bu adresi **Safari'de** aç (Chrome'da ana ekrana ekleme düzgün çalışmaz)
2. Alttaki **Paylaş** düğmesi → **Ana Ekrana Ekle**
3. İsmi "Arpej" gelir, **Ekle**

Artık ana ekranda kendi ikonu var; Safari çubuğu olmadan tam ekran açılıyor ve
uçak modunda / internetsiz de çalışıyor.

## Sonradan değişiklik yaparsan

    cd ~/Downloads/gunluk-arpej-pwa
    git add -A && git commit -m "değişiklik" && git push

Telefon eski sürümü önbellekte tutabilir. Yeni sürümü hemen almak için
`sw.js` içindeki `const CACHE = 'arpej-v1'` satırındaki numarayı artır (`arpej-v2`),
sonra push et.

---

**Not:** git commit'i `Arda / curaarda@gmail.com` adına atıldı. Değiştirmek istersen:

    cd ~/Downloads/gunluk-arpej-pwa
    git config user.name "Adın"
    git config user.email "mail@adresin"
    git commit --amend --reset-author --no-edit
