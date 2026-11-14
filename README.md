# Twins Mobilya İş Takip

Twins Mobilya için mobil uyumlu iş takip uygulaması (tek sayfa, kurulum gerektirmez).

Sayfalar: Giriş, Ayarlar, Yapılacak İş Listesi, Gün Sonu (PDF), Kullanılan Malzeme Listesi (Ay Sonu PDF).

## GitHub Pages ile yayınlama

1. GitHub'da yeni bir repo oluştur (örn. `twins-is-takip`).
2. Bu klasördeki tüm dosyaları repoya yükle (`index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `README.md`). Dosyalar kök dizinde olmalı.
3. Repo → **Settings → Pages** → Source: **Deploy from a branch** → Branch: **main** / **(root)** → Save.
4. Birkaç dakika sonra adres hazır olur: `https://KULLANICI-ADIN.github.io/twins-is-takip/`

## Telefona uygulama gibi kurma

- **Android (Chrome):** adresi aç → ⋮ menüsü → **Uygulamayı yükle / Ana ekrana ekle**.
- **iPhone (Safari):** adresi aç → Paylaş → **Ana Ekrana Ekle**.

## Önemli notlar

- Veriler (müşteriler, görevler, malzemeler) şu an **sadece o telefonun/tarayıcının içinde** saklanır. Farklı telefonlar birbirinin verisini görmez. Tarayıcı verisi silinirse kayıtlar da silinir.
- Ortak veri için sonraki adımda bir veritabanı (örn. Firebase / Supabase) bağlanmalıdır.
- Giriş ekranında şu an her kullanıcı adı kabul edilir; izinli kullanıcı listesi sonradan eklenecek.
- Güncelleme yaparken `sw.js` içindeki `CACHE` adındaki sürüm numarasını (`v1` → `v2`) artır, telefonlar yeni sürümü alsın.
