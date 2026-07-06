# Isparta – Manavgat Yemekli Bot Turu — Landing Page

Tek dosyalık statik site. Kayıtlar **WhatsApp'a** düşer: kullanıcı formu doldurup gönderince
tüm bilgileri hazır bir WhatsApp mesajı olarak size iletir. Online ödeme yoktur.

## 🚀 Yayına Alma
Hiçbir kurulum gerekmez. `index.html` dosyasını herhangi bir yere koyabilirsiniz:
- **Netlify / Vercel:** klasörü sürükle-bırak → anında yayında (ücretsiz).
- **GitHub Pages:** repoya yükleyin, Pages'i açın.
- **Kendi hosting'iniz:** `index.html`'i `public_html` içine atın.

## ⚙️ Düzenlenmesi Gerekenler
`index.html` içinde en alttaki `<script>` bloğunda **CONFIG** kısmını açın:

```js
const CONFIG = {
  whatsappNumber: "905XXXXXXXXX", // ← KENDİ WhatsApp numaranız (ülke kodu + no, + ve boşluk yok)
  price: "2450",                  // ← Fiyat
  tourDate: "2026-07-19 07:00",   // ← Tur tarihi (geri sayım buna göre çalışır)
  totalSeats: 50,                 // ← Toplam kontenjan
  seatsLeft: 12,                  // ← Kalan koltuk (hero'daki "Son X koltuk kaldı")
};
```

> **WhatsApp numarası örneği:** `0532 123 45 67` → `905321234567`

## 📸 Gerçek Fotoğraf Ekleme (Galeri)
Galeri şu an renkli ikon kutuları. Gerçek fotoğraf koymak için `index.html` içinde
`<!-- Gerçek fotoğraf eklemek için ... -->` yorumunu bulun ve ilgili `.gcard` içindeki
`<div class="ph">...</div>` yerine `<img src="fotograf.jpg" alt="Eşsiz Doğa">` yazın.
Fotoğrafları `index.html` ile aynı klasöre atın.

## ✅ İçindekiler
- Güçlü hero (fiyat kartı + geri sayım + "son X koltuk")
- Tur detayları (ikonlu)
- Saat saat program akışı
- Galeri (Eşsiz Doğa / Lezzetli Yemek / Side)
- Kayıt formu → WhatsApp'a hazır mesaj + başarı bildirimi
- Katılımcı yorumları
- Sıkça Sorulan Sorular
- Sabit WhatsApp butonu + mobil alt bar (tam mobil uyumlu)

## 🔧 Sonradan Eklenebilir
İleride kayıtları bir panelde/veritabanında toplamak isterseniz (Supabase + admin paneli),
Google Sheets entegrasyonu veya otomatik e-posta bildirimi eklenebilir.
