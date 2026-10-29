# PRD — [Uygulamanın Adı]

> 📌 **Nasıl kullanılır?**
> 1. Bu dosyanın adını `PRD.md` yap ve `ai-agent-proje-kurulum-yonergesi.txt` ile aynı klasöre koy.
> 2. Köşeli parantezli `[...]` yerleri kendi fikrine göre doldur. Açıklama kutularını (› ile başlayan satırlar) silebilirsin; silmesen de olur.
> 3. Emin olmadığın bir yere **"Bilmiyorum, sen karar ver"** yazabilirsin. AI makul bir seçim yapar ve sonunda sana söyler.
> 4. Kodlama ajanına şunu yaz:
>    *"ai-agent-proje-kurulum-yonergesi.txt dosyasındaki kurallara uyarak PRD.md'deki uygulamayı geliştir."*
>
> 💡 **Altın kural:** Ne kadar net yazarsan sonuç o kadar iyi olur. "Güzel bir site" yerine "Ana sayfada en yeni 10 tarif kart olarak görünsün" yaz.

---

## 1. Ürün Özeti

> 💡 Uygulaman ne yapıyor? 1–2 cümle. Birine asansörde anlatır gibi yaz.
> *Örnek: "Öğrencilerin kampüsteki boş çalışma alanlarını görüp yer ayırabildiği bir web sitesi."*

[Buraya yaz]

## 2. Problem ve Katma Değer

> 💡 **Problem:** Hangi sorunu çözüyorsun? Şu an insanlar bu işi nasıl yapıyor, neyi zor?
> **Katma değer:** Seninki neden daha iyi? Daha hızlı mı, daha basit mi, daha eğlenceli mi?
> *Örnek: "Problem: Kütüphanede yer bulmak için kat kat dolaşmak gerekiyor. Katma değer: Boş yerleri tek ekranda, anlık görmek."*

- **Problem:** [Buraya yaz]
- **Katma değer:** [Buraya yaz]

## 3. Hedef Kullanıcı

> 💡 Bu uygulamayı kim kullanacak? Sadece sen mi, arkadaşların mı, herkes mi?
> Kullanıcıyı ne kadar net tarif edersen tasarım o kadar ona uygun olur.
> *Örnek: "Sınav döneminde çalışacak yer arayan İTÜ öğrencileri. Çoğunlukla telefondan girecekler."*

[Buraya yaz]

**Bu ürünü:** [Kendim kullanacağım / Arkadaşlarımla kullanacağım / Herkese açacağım]

## 4. Özellikler

> 💡 Uygulama neler yapabilmeli? Her maddeyi **kullanıcının yapabildiği bir eylem** olarak yaz.
> - ❌ "Arama özelliği"
> - ✅ "Kullanıcı tarif adına göre arama yapabilir, sonuçlar yazarken anlık güncellenir."
>
> Özellikleri ikiye ayır: **olmazsa olmaz** olanlar ilk sürümde mutlaka olmalı; **zaman kalırsa** olanlar sonraya bırakılabilir. İlk projen için olmazsa olmazları 3–7 madde arasında tut.

### Olmazsa olmaz
1. [Kullanıcı ... yapabilir]
2. [Kullanıcı ... yapabilir]
3. [Kullanıcı ... yapabilir]

### Zaman kalırsa
1. [...]
2. [...]

## 5. Ekranlar ve Görünüm

> 💡 Hangi sayfalar/ekranlar olacak ve her birinde ne görünecek? Kâğıda kabaca çizip buraya kelimelerle anlatmak çok işe yarar.
> *Örnek:*
> - *Ana sayfa: Üstte arama kutusu, altında kart halinde tarifler.*
> - *Tarif detayı: Büyük fotoğraf, malzeme listesi, adım adım yapılış.*

**Ekranlar:**
- [Ekran adı]: [Bu ekranda ne var?]
- [Ekran adı]: [Bu ekranda ne var?]

> 💡 Tarzını tarif et: renkler, his (sade, eğlenceli, ciddi), örnek aldığın uygulamalar. Bir uygulamaya "benzesin" diyebilirsin; AI genel düzeni alır ama logosunu ve birebir tasarımını kopyalamaz.
> *Örnek: "Sade ve ferah, beyaz arka plan, yeşil vurgu rengi. Pinterest'teki gibi kart düzeni."*

**Görsel tarz:** [Buraya yaz]

**Öncelikli cihaz:** [Telefon / Bilgisayar / İkisi de]

**Arayüz dili:** [Türkçe / İngilizce]

## 6. Veriler ve Hesaplar

> 💡 Bu bölüm, uygulamanın ne kadar karmaşık kurulacağını belirler. Teknik bilgi gerekmez, sadece soruları cevapla. AI buna göre en basit çözümü seçer.

- **Uygulama hangi bilgileri saklayacak?** [Örn: tarif adı, malzemeler, fotoğraf]
- **Kullanıcıların hesap açıp giriş yapması gerekiyor mu?** [Evet / Hayır]
- **Bir kullanıcının eklediğini başkaları da görmeli mi?** [Evet / Hayır]
- **Aynı kişi verisini farklı cihazlardan (telefon + bilgisayar) görmeli mi?** [Evet / Hayır]
- **Uygulama dışarıdan bir servis kullanacak mı?** [Örn: hava durumu, yapay zekâ, harita / Hayır]

> 💡 Hepsine "Hayır" dediysen uygulama tamamen tarayıcıda çalışır ve kurulumu en basit hali olur. İlk proje için önerilen budur.

## 7. Kapsam Dışı

> 💡 Uygulamanın **yapmayacağı** şeyler. En çok unutulan ama en çok işe yarayan bölüm: AI'ın gereksiz özellik eklemesini engeller.
> *Örnek: "Ödeme sistemi yok. Mesajlaşma yok. Yönetici paneli yok."*

- [...]
- [...]

## 8. Kabul Kriterleri

> 💡 "Uygulama bitti" demek için neyi denemen gerekir? Her maddeyi **test edilebilir** bir cümle olarak yaz. AI işi bitirince bunları tek tek kontrol eder.
> - ❌ "Hızlı çalışsın"
> - ✅ "Sayfa yenilenince eklenen tarifler kaybolmuyor."

- [ ] [...]
- [ ] [...]
- [ ] [...]
- [ ] Telefonda düzgün görünüyor, yatay kaydırma yok.

## 9. Başarı Ölçütü

> 💡 Bu proje ne olursa başarılı sayılır? Kendin için yapıyorsan "her gün kullanıyorum" bile yeterli.
> *Örnek: "İlk hafta 20 arkadaşım kullanmaya başlarsa."*

[Buraya yaz]

## 10. Ekstra Notlar (isteğe bağlı)

> 💡 Yukarıya sığmayan her şey: ilham aldığın siteler, özel istekler, aklına takılan sorular.

[Buraya yaz]
