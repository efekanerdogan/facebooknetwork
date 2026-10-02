# 🦊 Facebook Network Genişletici

Facebook'ta **Önerilen Arkadaşlar**, grup üyeleri ve benzeri listelerdeki kişilere kontrollü şekilde arkadaşlık isteği gönderen, kurulum gerektirmeyen bir **Bookmarklet** (yer imi betiği) aracı.

**Canlı kurulum sayfası:** https://efekanerdogan.github.io/facebooknetwork/

---

## ✨ Özellikler (v2.0)

- **Buzlu cam panel:** Facebook'un koyu temasına uyumlu, yarı saydam arayüz. **Shadow DOM** kullandığı için Facebook'un stilleri panele karışmaz.
- **Sürüklenebilir ve hatırlayan:** Paneli istediğin köşeye taşı, küçült. Konum, limit ve hız ayarı bir sonraki açılışta hazır gelir.
- **Başlat · Duraklat · Durdur:** Çalışırken tam kontrol sende. Yer imine ikinci kez tıklamak paneli kapatır ve işlemi durdurur.
- **Canlı ilerleme:** İlerleme çubuğu, gönderilen sayısı, geçen süre ve eklenen kişilerin isimleri.
- **Hız profilleri:** Yavaş (4–9 sn), Normal (2,5–5 sn), Hızlı (1,5–3 sn) aralığında rastgele bekleme. Tek seferde en fazla **100** istek.
- **Otomatik güvenlik freni:** Facebook bir kısıtlama uyarısı gösterirse ya da tıklamalar üst üste 3 kez sonuçsuz kalırsa araç kendiliğinden durur.
- **Akıllı kaydırma:** Görünen kişiler bitince sayfayı kendi indirir; liste sonuna gelince sonsuz döngüye girmeden bitirir.
- **Türkçe + İngilizce arayüz desteği:** "Arkadaşı ekle" ve "Add friend" butonları algılanır.
- **Gizlilik:** Hiçbir sunucuya veri gönderilmez. Yalnızca limit, hız ve panel konumu tarayıcının yerel depolamasında tutulur.

---

## 🚀 Kurulum

1. [Kurulum sayfasını](https://efekanerdogan.github.io/facebooknetwork/) açın.
2. **🦊 FB Network Genişletici** butonunu fareyle tutup tarayıcınızın **Yer İmleri Çubuğuna** sürükleyin. (Çubuk görünmüyorsa `Ctrl + Shift + B`.)

**Alternatifler:**

- **Konsol:** Sayfadaki *Konsol kodunu kopyala* düğmesine basın, Facebook sekmesinde `F12` → *Console* → yapıştırın → `Enter`. Chrome yapıştırmayı engellerse önce `allow pasting` yazın.
- **Mobil / dokunmatik:** *Yer imi bağlantısını kopyala* düğmesiyle bağlantıyı kopyalayıp tarayıcıda yeni bir yer imi oluşturun ve adres alanına yapıştırın. Araç masaüstü Facebook arayüzü için tasarlanmıştır.

---

## 🎮 Kullanım

1. Facebook'a giriş yapın ve **Önerilen Arkadaşlar**, grup **Üyeler** sekmesi ya da "Arkadaşı ekle" butonları olan bir listeye gidin.
2. Yer imine tıklayın; panel açılır.
3. **Limit** ve **Hız** seçin (Yavaş/Normal önerilir) ve **▶ Başlat**'a basın.
4. İşlem bitene kadar sekmeyi açık tutun. Dilediğiniz an **⏸** ile duraklatın ya da **■** ile durdurun.

---

## 🛠️ Geliştirme

Proje tek dosyadan oluşur: [`index.html`](index.html).

- Kurulum sayfasının HTML/CSS'i ve canlı önizleme simülasyonu `index.html` içindedir.
- Bookmarklet'in **okunabilir kaynağı** `<script type="text/plain" id="bm-src">` bloğundadır. Sayfa yüklenirken satırları sıkıştırılıp `javascript:` bağlantısına çevrilir, yani elle minify etmeye gerek yoktur.
- Bu bloğa yazarken: satır içi `//` yorum kullanmayın, her ifadeyi `;` ile bitirin (satırlar boşlukla birleştirilir).
- Yerelde denemek için herhangi bir statik sunucu yeterlidir:
  ```bash
  npx serve .
  ```

Facebook arayüzü sık değişir. Araç çalışmayı bırakırsa `findButtons()` ve `nameOf()` fonksiyonlarındaki seçicileri güncellemek genellikle yeterlidir.

---

## ⚠️ Önemli Uyarılar

> [!WARNING]
> **Hesap güvenliği:** Facebook'un spam algoritmaları serttir. Otomatik istek göndermek platformun kullanım koşullarıyla çelişebilir ve hesabın kısıtlanmasına yol açabilir. Garanti verilemez.

> [!TIP]
> **Tavsiye edilen kullanım:** Günde 50–100 istek, "Yavaş" veya "Normal" hızda ve küçük paketler halinde.

> [!NOTE]
> **Sorumluluk:** Bu araç eğitim, araştırma ve iş akışını hızlandırma amacıyla paylaşılmıştır; Facebook ile bağlantısı yoktur. Kötüye kullanımdan ve politika ihlallerinden doğabilecek tüm sonuçlar kullanıcıya aittir.

---

## 👨‍💻 Geliştirici

**Efekan Erdoğan** · [efekanerdogan.com](https://efekanerdogan.com) · [MIT Lisansı](LICENSE)
