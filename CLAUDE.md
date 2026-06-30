# Alina Silvera — Website

## Proje Özeti
Tek sayfalık statik HTML/CSS sitesi. Backend yok, framework yok. Tüm stiller `index.html` içindeki `<style>` bloğunda.

## Dosyalar

| Dosya | Açıklama |
|---|---|
| `index.html` | Tüm HTML, CSS ve JS tek dosyada |
| `*.jpeg` | Ürün ve bölüm görselleri |

## Deploy
- **GitHub:** `https://github.com/HayyyJ/alina-silvera`
- **Vercel:** GitHub'a push edilince otomatik deploy olur
- Değişiklik sonrası tarayıcıda **Ctrl+Shift+R** ile hard refresh gerekebilir

## Tasarım Kararları

### Tipografi
- **Nav logo:** `Clicker Script` cursive, 66px, gümüş renk (`--silver`), `nav-height: 100px`
- **Section başlıkları (h1, h2):** `Cormorant Garamond` italic bold, `clamp(38px, 4.5vw, 58px)`
- **Eyebrow etiketleri** (JOURNAL, THE BRAND vb.): Raleway, 17px, bold 700, `--text-soft` rengi
- **Nav linkleri** (HOME, ABOUT vb.): Raleway, 15px, bold 700
- **Footer linkleri:** 15px; footer başlıkları (Navigate/Shop/Connect): 21px

### Renkler (CSS değişkenleri)
```
--navy:        #0D1B2A   (koyu lacivert — nav, dark section arka planı)
--cream:       #FDFAF7   (açık krem — sayfa arka planı)
--blush:       #F7EAED   (açık pembe — women & statement section)
--silver:      #C4B5AF   (gümüş — nav logo, accent)
--text-soft:   #8E8480   (soluk gri — eyebrow etiketleri)
```

### Görseller
Her section'daki görseller `object-fit: contain !important` ile tam görünür.
Global CSS'deki `img { object-fit: cover }` kuralını ezmek için `!important` kullanılıyor.

Resim wrapper örneği:
```html
<div style="max-width:400px; margin:0 auto 100px;">
    <div style="overflow:hidden;">
        <img src="..." style="width:100%; height:auto !important; object-fit:contain !important; display:block;">
    </div>
</div>
```

### Bölümler (sırayla)
1. `#hero` — Nature, carried with grace / This is me.jpeg
2. `#statement` — Women do not simply wear beauty / Elegant Saphire 2.jpeg
3. `#about` — Born from a desire / Round Handmade.jpeg
4. `#nature` — There is a quiet language in nature / Pink Beauty.jpeg
5. `#women` — Women as the Great Transformers / Quiet Drop (2).jpeg
6. `#collection` — Ürün kartları
7. `#journal` — Blog yazıları
8. `#cta` — Find your piece
9. `#footer` — Linkler ve sosyal medya

## Değişiklik Yaparken
- Sadece `index.html` düzenle
- Değişiklik sonrası: `git add index.html && git commit -m "..." && git push origin main`
- Vercel otomatik deploy eder (~1-2 dk)
