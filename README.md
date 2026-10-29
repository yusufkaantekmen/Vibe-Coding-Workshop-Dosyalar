# Vibe Coding Workshop — Dosyalar

**İTÜ ACM · 3 Kasım 2026 · Med A**

Yapay zekâ ile bir fikri, kod bilmeden de çalışan ve yayında olan bir web sitesine dönüştürmek için ihtiyacın olan her şey burada. İki dosyayı bir klasöre koyup bir AI kodlama ajanına tek cümlelik bir komut veriyorsun, gerisini ajan yapıyor.

---

## 📁 Bu depoda neler var?

| Dosya | Ne işe yarar? |
|---|---|
| `ai-agent-proje-kurulum-yonergesi.txt` | AI ajanına projeyi **nasıl** kuracağını anlatan kurallar: teknik yığın, klasör yapısı, güvenlik, seninle nasıl konuşacağı. Her projede aynı kalır, değiştirmene gerek yok. |
| `ornek-PRD-sablonu.md` | Fikrini anlatacağın **doldurulabilir şablon**. Her bölümde açıklama ve örnek var. |
| `not-defteri-proje-PRD.md` | Workshop'ta canlı geliştirdiğimiz not defteri uygulamasının **doldurulmuş PRD'si**. Şablonu doldururken örnek olarak bak. |
| `sunum-PRD.md` | Workshop sunumunun planı: bölümler, slayt içerikleri, süreler ve konuşma notları. |
| `not-defteri-uygulama/` | Workshop'ta yapılan uygulamanın kodları *(workshop sonrası eklenecek)*. |

---

## 🚀 Hızlı başlangıç

### 1. Bir kodlama ajanı seç
Sohbet penceresi değil, **dosya oluşturabilen ve komut çalıştırabilen** bir ajan gerekiyor:
Claude Code, Codex, GitHub Copilot (ajan modu), Gemini CLI vb.

### 2. Gerekenleri kur
- [Node.js](https://nodejs.org) (LTS sürümü)
- [Git](https://git-scm.com)
- Yayınlamak için ücretsiz [GitHub](https://github.com) ve [Vercel](https://vercel.com) hesabı

> Eksik bir şey varsa sorun değil: ajan kontrol edip ne yapman gerektiğini adım adım anlatır.

### 3. Proje klasörünü hazırla
1. Boş bir klasör oluştur (ör. `benim-projem`).
2. İçine `ai-agent-proje-kurulum-yonergesi.txt` ve `ornek-PRD-sablonu.md` dosyalarını koy.
3. Şablonun adını **`PRD.md`** yap.

### 4. PRD'yi doldur
`PRD.md` içindeki `[...]` yerlerini kendi fikrine göre doldur. Emin olmadığın yere *"Bilmiyorum, sen karar ver"* yazabilirsin.

### 5. Ajana tek komut ver
Ajanı bu klasörde başlat ve şunu yaz:

```
ai-agent-proje-kurulum-yonergesi.txt dosyasındaki kurallara uyarak PRD.md'deki uygulamayı geliştir.
```

Ajan planını anlatır, projeyi kurar, test eder ve bitince sana tarayıcıda hangi adresi açacağını söyler.

### 6. Yayınla
Ajana *"Vercel'de yayınlayalım"* de. GitHub'a yükleme ve Vercel'e bağlama adımlarını tek tek anlatır.

---

## 🧩 İki dosya nasıl birlikte çalışıyor?

```
PRD.md                 →  NE yapılacak   (projeye özel: fikir, özellikler, ekranlar)
kurulum yönergesi      →  NASIL yapılacak (her projede aynı: teknik kurallar)
                ↓
         AI kodlama ajanı
                ↓
   Çalışan, düzenli, yayınlanabilir web sitesi
```

Sadece *"bana not uygulaması yap"* demek, AI'ın boşlukları tahminle doldurmasına ve dağınık bir sonuca ("AI slop") yol açar. PRD ve yönerge bu boşlukları baştan kapatır.

---

## ⚙️ Yönerge neleri garanti ediyor?

- **En basit çözüm önce:** Varsayılan olarak uygulama tamamen tarayıcıda çalışır ve Vercel'de ücretsiz yayınlanır.
  - Hesap/giriş ya da kullanıcılar arası paylaşım gerekiyorsa **Supabase** eklenir.
  - Gizli API anahtarı gibi sunucu işleri gerekiyorsa **Render** eklenir.
  - Ajan bunları eklemeden önce nedenini anlatır ve onayını alır.
- **Teknik yığın:** React, Vite, Tailwind CSS, ESLint, Vercel.
- **Düzenli kod:** İşlevine göre ayrılmış klasörler, küçük dosyalar.
- **Sade anlatım:** Kod bilmeyen birine anlatır gibi Türkçe açıklama, yapman gerekenler için adım adım talimat.
- **Güvenlik:** API anahtarları koda yazılmaz; Supabase'de satır bazlı erişim kuralları (RLS) zorunludur.
- **Teslimden önce kontrol:** Lint ve build hatasız geçmeden "bitti" denmez.

---

## 💡 İpuçları

- **Önce plan, sonra kod.** Ajana önce ne yapacağını anlattır.
- **Küçük adımlarla ilerle.** Büyük projelerde her şeyi tek komutta isteme.
- **Her adımda test et.** Hata çıkarsa hata mesajını olduğu gibi ajana ver.
- **Git ile kaydet.** Çalışan her hali kaydet ki bir şey bozulunca geri dönebil.
- **"Kapsam dışı" bölümünü boş bırakma.** AI'ın gereksiz özellik eklemesini en iyi bu engeller.

---

## 📒 Örnek: Not defteri uygulaması

Workshop'ta canlı geliştirdiğimiz uygulama:

- Notları kart akışı halinde gösterir
- Notlara görsel ve dosya eklenebilir
- Veriler tarayıcıda saklanır, hesap gerekmez

Kodlar workshop sonrası `not-defteri-uygulama/` klasörüne eklenecek. Bilgisayarında çalıştırmak için:

```bash
cd not-defteri-uygulama
npm install
npm run dev
```

---

## 🤝 İletişim

Daha kapsamlı uygulamalar geliştirmek istersen ya da sorun olursa ulaşabilirsin:

- **LinkedIn:** [Yusuf Kaan Tekmen](https://www.linkedin.com/in/yusufkaantekmen/)
- **İTÜ ACM DevTeam** WhatsApp grubu: duyurular ve yaklaşan **Vibe Coding Hackathon** için takipte kal.

Teknik detayları merak edenler için İTÜ ACM'in mentörlük ve bootcamp etkinliklerine göz at.
