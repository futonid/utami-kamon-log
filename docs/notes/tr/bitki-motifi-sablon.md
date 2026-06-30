## GIMP Bitki motifi şablonu
**Bağlam:** Özellikle, bitki motifi için, GIMP kullanarak şablon nasıl hazırlanmalı? **[19/06/26 / GIMP 3.2.0]**
### Problem

- **p1-şablon**    
Çalışma alanı ölçüsü seçilmeli ve genel sistemi belirlenmeli 
- **p2-maru-kararı**    
Maru içinde mi yoksa serbest mi olacağına karar verilmeli. 
- **p3-grid-yapısı**    
Özellikle bitki motifi için gridi ayarlamalı.

- **p4-motif-inşası**   
Bitki motifleri doğadan gelse de Kamon tasarımında yüksek düzeyde soyutlanmalı ve minimalist hale getirilmeli.
---

### Çözüm
#### p1-şablon:
- File > New: Width ve Height değerlerini `1200 px` olarak ayarla.
- Color Space kısmının Grayscale (Gri Tonlama) olarak ayarla. `Image` > `Mode` > `Grayscale`
- Altın Oran Hesabı: `1200 px / 1.618 ≈ 742 px.` Bu   "aktif" çalışma alanı.
- Margin (Kenar Boşluğu) Hesabı: `(1200 - 742) / 2 = 229 px`.
- Guides (Kılavuzlar): Image > Guides > New Guide (by Pixels) yolunu izleyerek hem dikey (Vertical) hem yatay (Horizontal) olarak 229 px ve 971 px (229+742) konumlarına kılavuz çizgileri ekleyin.
- **Kaynak:** [Analiz](/docs/notes/tr/analiz-sablonlar.md)
**Alternatif: Yüzde Bazlı Altın Oran (her tuval boyutu için geçerli)**
- Piksel hesaplamak yerine, GIMP'in yüzde tabanlı guide özelliği kullanılabilir; bu yöntem tuval boyutundan bağımsızdır çünkü φ (1.618) sabiti yüzdeye sabit şekilde yansır: **%19.1** ve **%80.9**.
- `Image > Guides > New Guide (by Percent)` yolunu izleyerek:
  - Orientation: Vertical, Position: `19.1` → ekle
  - Orientation: Vertical, Position: `80.9` → ekle
  - Orientation: Horizontal, Position: `19.1` → ekle
  - Orientation: Horizontal, Position: `80.9` → ekle
- Bu 4 guide, tuval boyutu ne olursa olsun (örn. 1080x400, 1200x1200 vb.) aynı oranda 4 kesişim noktası oluşturur; metin bloğu veya odak unsuru bu noktalardan birine hizalanabilir.
- Not: %19.1 + %80.9 = 100; iki çizgi tuvali "büyük parça – küçük parça" mantığıyla iki kez (19.1-80.9 ve 80.9-19.1) böler.

#### p2-maru-kararı:
- Dairesel çerçevede yapılacak.
- Kamon tasarımları genellikle merkezden dışa doğru denge kurar.
- Motif için ana aksı oluştur: `Image` > `Guides` > `New Guide (by Percent)` diyerek hem Horizontal hem Vertical olarak `%50` değerinde merkez kılavuzlarını yerleştir. 
- Daire çizimi için, Tool: `Ellipse Select Tool` (E), Tool Options: `Fixed Aspect Ratio (1:1)` seçeneğini işaretle. `Expand from center` kutucuğunu aktif et.
    - Uygulama: İmleci merkez kesişim noktasına koyun ve aktif alanınızın sınırlarına (742 px'lik kareye) değecek şekilde daireyi çizin. [Müller-Brockmann'ın](/docs/workbook/references/research.md#grid-system) sisteminde bu daire, dış kılavuzlarla matematiksel olarak tam çakışmalıdır


#### p3-grid-yapısı:
- 8x8 gibi daha az bölmeli bir ızgara, karmaşık detaylara boğulmadan temel formlara odaklanmayı kolaylaştırır 
- 742 px (aktif alan) / 8 birim = 92.75 px.
- `Edit` > `Preferences` > `Default Grid` veya o anki dosya için `Image` > `Configure Grid` menüsüne gidin.
- Izgarayı görmek için `View` > `Show Grid` ve çizgileri yakalamak için `View` > `Snap to Grid` seçeneklerini aktif et.


#### p4-motif-inşası
- Soyutlama: Bitkinin (yaprak, çiçek, sap) tüm gereksiz detaylarını at. Sadece temel formları bırak.
- Izgara Hizalama: Yaprakların uçlarını veya sapın birleşim noktalarını ızgara kesişimlerine tam olarak oturt.
- Simetri: Bir yaprağı çizdikten sonra `Layer` > `Transform` > `Flip Horizontally` kullanarak diğer tarafı rasyonel bir kesinlikle yansıt.




---    
### Sonuç

**[kamon-master-8Grid.xcf](/docs/workbook/templates/)**

**Not:**    
(Denge ve Negatif Alan)
[Müller-Brockmann'ın](/docs/workbook/references/research.md#grid-system) sisteminde boş (beyaz) alanlar, siyah formlar kadar aktif.

Monochrome Balance: Siyah bitki formlarının ızgara üzerinde kaç modül kapladığını say. Beyaz boşlukların bu formlarla bir "ritim" oluşturduğundan emin ol.

Legibility (Okunabilirlik): Çalışmaya %10-20 gibi küçük ölçeklerde bak; grid sayesinde Kamon'un karakterini koruyup korumadığını (uzaktan tanınabilirlik) test et.

---