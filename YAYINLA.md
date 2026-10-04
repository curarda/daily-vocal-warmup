# GitHub Pages'e koyup iPhone'a kurmak

Bu klasör hazır bir git deposu. Kimlik, uzak adres ve dal zaten ayarlandı:

- kullanıcı: `curarda`
- commit e-postası: `211261331+curarda@users.noreply.github.com` (GitHub'ın gizli noreply adresi)
- uzak adres: `https://github.com/curarda/daily-vocal-warmup.git`
- dal: `main`

> **Neden noreply adresi:** GitHub hesabında "Keep my email addresses private" açık.
> Gerçek e-postanla commit atarsan push şu hatayla reddedilir:
> `GH007: Your push would publish a private email address.`
> Bu yüzden git'i baştan noreply adresine ayarladım, gerçek adresin hiçbir yere yazılmıyor.

## 1. GitHub'da boş depo aç

github.com → sağ üst `+` → **New repository**

- **Repository name:** `gunluk-arpej`
- **Public** (Pages ücretsiz hesapta sadece public depoda çalışır)
- README / .gitignore / lisans **ekleme** — hiçbirini işaretleme

## 2. Gönder

    cd ~/Downloads/gunluk-arpej-pwa
    git push -u origin main

Kullanıcı adı sorarsa `curarda`, **parola sorarsa parolanı değil token'ı** yapıştır:
github.com → Settings → Developer settings → Personal access tokens → Tokens (classic) →
Generate new token → `repo` yetkisini işaretle → çıkan `ghp_...` metnini parola alanına yapıştır.

> Terminalle uğraşmak istemezsen: yeni depo sayfasındaki **uploading an existing file**
> bağlantısına tıklayıp bu klasördeki 8 dosyayı sürükleyip bırak. (Bu yolda commit
> GitHub tarafında atıldığı için e-posta sorunu da hiç çıkmaz.)

## 3. Pages'i aç

Depo → **Settings** → sol menü **Pages** →
**Source:** Deploy from a branch · **Branch:** `main` · **klasör:** `/ (root)` → Save.

1–2 dakika sonra adres:

    https://curarda.github.io/daily-vocal-warmup/

## 4. iPhone'a ekle

1. Adresi **Safari'de** aç (Chrome'da ana ekrana ekleme düzgün çalışmaz)
2. Alttaki **Paylaş** → **Ana Ekrana Ekle**
3. İsim "Arpej" gelir → **Ekle**

Ana ekranda kendi ikonu olur, Safari çubuğu olmadan tam ekran açılır, internetsiz de çalışır.

## Sonradan değişiklik

    cd ~/Downloads/gunluk-arpej-pwa
    git add -A && git commit -m "değişiklik" && git push

Telefon eski sürümü önbellekte tutar. Yeni sürümü hemen almak için `sw.js` içindeki
`const CACHE = 'arpej-v1'` numarasını artır (`arpej-v2`), sonra push et.
