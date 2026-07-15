# Vergi Takvimim

Türkiye'deki mali müşavirler, muhasebeciler ve işletmeler için tamamen tarayıcıda çalışan, kurulabilir vergi takip PWA'sı.

## Çalıştırma

Bu proje statiktir: `index.html` dosyasını bir yerel sunucuyla açın. PWA ve çevrimdışı özellikleri için HTTPS ya da `localhost` gerekir.

## GitHub Pages'e yayınlama

1. Dosyaları bir GitHub deposunun köküne yükleyin.
2. **Settings → Pages** ekranında **Deploy from a branch** seçin.
3. `main` dalı ve `/ (root)` klasörünü seçerek kaydedin.
4. Yayınlanan adresi açın; mobil tarayıcıdan ana ekrana ekleyebilirsiniz.

## Otomatik veri kontrolü

`.github/workflows/update-tax-calendar.yml`, her gece Türkiye saatiyle 02:00'de çalışır. GİB öncelikli, TÜRMOB ikincil kaynaktır. Resmî sayfanın yapısı değişebileceğinden `scripts/update-gib.js` içindeki eşleştirici üretime alınmadan önce gözden geçirilmelidir. Otomasyon yalnızca değişiklik oluşursa JSON verilerini commitleyecektir.

## Klasörler

- `data/`: Uygulamanın okuduğu takvim ve güncelleme verileri
- `scripts/`: Sunucuda değil GitHub Actions üzerinde çalışan veri araçları
- `icons/`: PWA simgeleri

## Gizlilik

Firma profili, tamamlanan işlemler ve favoriler yalnızca cihazın LocalStorage alanında saklanır; uygulama bunları bir sunucuya göndermez.

## Lisans

MIT
