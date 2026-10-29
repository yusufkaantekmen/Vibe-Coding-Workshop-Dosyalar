# PRD — Kart Not Defteri

> Ürün Gereksinim Dokümanı. Bu dosya uygulamanın **ne** olduğunu anlatır; **nasıl** kurulacağı `ai-agent-proje-kurulum-yonergesi.txt` dosyasındadır.

## 1. Ürün Özeti

Notları sosyal medya akışı gibi görsel kartlar halinde gösteren, görsel ve dosya eklenebilen, tamamen tarayıcıda çalışan kişisel bir not defteri. Hesap gerektirmez; veriler kullanıcının kendi tarayıcısında saklanır.

## 2. Problem ve Katma Değer

- **Problem:** Notlar, fotoğraflar ve dosyalar farklı uygulamalara dağılıyor; klasik not uygulamaları sıkıcı bir liste görünümünde.
- **Katma değer:** Notlarla ilgili görsel ve dosyalar tek kartta durur; akış görünümü göz gezdirmeyi kolaylaştırır. Kurulum ve hesap yok, açıp kullanılır.

## 3. Hedef Kullanıcı

Ders notlarını, fikirlerini ve ilgili görselleri tek yerde tutmak isteyen öğrenciler. Kişisel kullanım içindir; pazarlama hedefi yoktur.

## 4. Özellikler

### Öncelik 1 — Olmazsa olmaz
1. **Not oluşturma:** Başlık (zorunlu), metin içeriği (isteğe bağlı), kart rengi (6 hazır renkten biri).
2. **Dosya ekleme:** Bir nota birden fazla dosya eklenebilir. Görseller önizlenir; diğer dosyalar (PDF vb.) ad ve boyutuyla listelenir ve indirilebilir. Dosya başına sınır: 10 MB.
3. **Akış görünümü:** Notlar kart ızgarası halinde, en yeni üstte. Kartta görsel varsa ilk görsel kapak olur; yoksa kart renginde başlık ve metnin ilk satırları görünür.
4. **Not detayı:** Karta tıklayınca açılan pencerede notun tamamı, ekleri ve oluşturma/düzenleme tarihi görünür.
5. **Düzenleme ve silme:** Detay penceresinden not düzenlenir veya silinir (silmeden önce onay).
6. **Favori:** Kalp ikonuyla nota favori eklenir/çıkarılır.
7. **Arama:** Başlık ve içerikte anlık arama.
8. **Kalıcılık:** Sayfa yenilenince veya tarayıcı kapatılıp açılınca tüm notlar ve dosyalar yerinde durur.

### Öncelik 2 — Zaman kalırsa
9. **Etiketler:** Nota etiket eklenir; üstteki etiket çiplerine tıklayınca filtrelenir.
10. **Favoriler sekmesi:** Yalnızca favori notları gösteren görünüm.
11. **Yedekleme:** Tüm notları (dosyalarla birlikte) tek dosya olarak indirme ve geri yükleme.
12. **Karanlık mod:** Açık/karanlık tema geçişi; seçim hatırlanır.

## 5. Ekranlar ve Düzen

- **Üst çubuk:** Solda uygulama adı ("Notlarım"), ortada arama kutusu, sağda "+ Yeni not" butonu.
- **Akış:** Mobilde 2, tablette 3, masaüstünde 4 sütunlu kare kartlar. Kartların köşeleri yuvarlak, aralarında küçük boşluk.
- **Mobil alt menü:** Akış · Ara · (+) Yeni · Favoriler. Masaüstünde alt menü yerine üst çubuk kullanılır.
- **Not oluşturma/düzenleme:** Ortada açılan pencere (mobilde tam ekran). Alanlar: başlık, içerik, renk seçici, dosya ekleme alanı (sürükle-bırak + "Dosya seç"), etiketler.
- **Not detayı:** Görsel varsa üstte kaydırılabilir görsel alanı, altında başlık, içerik, ekler, tarih, kalp ve düzenle/sil butonları.
- **Boş durum:** İlk açılışta "Henüz not yok — ilk notunu ekle" mesajı ve büyük bir ekle butonu.
- **Bilgi notu:** Ayarlar veya alt kısımda "Notların yalnızca bu tarayıcıda saklanır" uyarısı.

**Görsel stil:** Popüler fotoğraf paylaşım uygulamalarını andıran sade, beyaz ağırlıklı, kart odaklı bir arayüz. Hiçbir markanın logosu, adı veya birebir tasarımı kullanılmayacak.

## 6. Veri Modeli

```
Note {
  id: string
  title: string
  content: string
  color: string
  tags: string[]
  isFavorite: boolean
  attachmentIds: string[]
  createdAt: ISO tarih
  updatedAt: ISO tarih
}

Attachment {
  id: string
  noteId: string
  name: string
  type: string        // MIME türü
  size: number        // bayt
  data: Blob
}
```

- Notlar ve dosyalar IndexedDB'de saklanır (dosyalar localStorage'a sığmaz).
- Tema tercihi localStorage'da saklanır.
- Not silinince ekleri de silinir.

## 7. Kapsam Dışı

- Kullanıcı hesabı, giriş, şifre
- Sunucu / backend / veritabanı sunucusu
- Cihazlar arası senkronizasyon
- Notları başka kullanıcılarla paylaşma
- Zengin metin editörü (kalın, başlık vb.) — içerik düz metindir
- Yapay zekâ özellikleri

## 8. Kabul Kriterleri

- [ ] Başlıksız not kaydedilemiyor; anlaşılır uyarı görünüyor.
- [ ] Görsel eklenen notun kartında görsel kapak olarak görünüyor.
- [ ] PDF eklenen notta dosya adı görünüyor ve indirilebiliyor.
- [ ] 10 MB'tan büyük dosya eklenmeye çalışılınca uyarı çıkıyor, uygulama çökmüyor.
- [ ] Sayfa yenilendiğinde notlar ve ekler kaybolmuyor.
- [ ] Silme onaydan sonra gerçekleşiyor; silinen notun ekleri de siliniyor.
- [ ] Arama yazarken sonuçlar anlık süzülüyor.
- [ ] 375 px genişlikteki telefonda yatay kaydırma yok, tüm butonlar tıklanabilir.
- [ ] `npm run lint` ve `npm run build` hatasız.
- [ ] Vercel'de yayınlanmış link telefonda açılıyor.

## 9. Başarı Ölçütü

Workshop sırasında site yayınlanıyor ve salondaki katılımcılar telefonlarından açıp kendi notlarını ekleyebiliyor.
