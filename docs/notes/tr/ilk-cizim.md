## İlk Çizim
**Bağlam:** Şablonum hazır, ancak çizim yapmaya nasıl başlayacağımı bilmiyorum, [22/06/26 / GIMP 3.2.0]
### Problem

- **p1-ilk-çizim-nereye**   
İlk çizimin dijitale mi yoksa kağıt üzerine mi yapılacak?
- **p2-ızgaraya-çizim**     
Izgara üzerine nasıl çizim yapılacak? 
- **p3-maru-ve-motif**  
Motif dairenin kenarlarına ne kadar yaklaşacak?
- **p4-nasıl-isimlendirilir**   
Bütün çizimi bitirdikten sonra ismini nasıl vermem gerekecek.

### Çözüm
#### p1-ilk-çizim-nereye
- [Müller-Brockmann'ın](/docs/workbook/references/resources.md#grid-system) tasarım sürecine kesinlikle küçük ölçekli eskizlerle kağıt üzerinde başlaması öneriliyor.
- Malzemelerim şu şekilde;
    - Tükenmez kalem, 
    - Kurşun kalem, 
    - Silgi, 
    - Kareli veya noktalı bir defter/kağıt.
    - Pergel
    - Cetvel

- Kağıdın toplam alanını cm cinsinden ölç.
- Kareli veya noktalı bir kağıda(bende noktalı var) 8x8 olacak şekilde ızgaranı çiz.
- Dijital ortam da ki gibi dilersen kılavuz hesabı yap ve çalışma alanını sınırla(tercihen)
- Örnek:
    - Tüm Alan   : 14cm
    - Aktif Alan : (14/1,618) ≈ 8,65
    - Marjinler  : 2,675 / 11,325 (sağ/yukarı,sol/aşağı)
    - Grid Ölçü  : 8,65 / 8 = 1,08125 ≈ 1,1 (kağıt üzerinde ben böyle kabul 
    ettim, hassas bir cetvelim olmadığı için).
    - [Steps](/docs/notes/tr/bitki-motifi-sablon.md/#p1-şablon:)
- **Kaynak:** [Bitki Motifi](/docs/notes/tr/bitki-motifi-sablon.md/#p1-şablon:)

#### p2-ızgaraya-çizim
- **Kağıt üzerinde:** 
    -   Çizim için ızgaranın parçalarını modül modül düşünüp ve kareleri sayarak çizdim. Bir kaç tekrar yaparak işin mantığı anlaşılıyor, detaya gerek yok.
- **Gimp üzerinde:** 
    - Kağıt üzerinde ki görseli referans görsel olarak proje dosyana dahil et(isteğe bağlı)
    - `Paths Tool` (Yollar Aracı) ile Çizim: `Paths Tool` (B) kullanılarak bitki motifinin düğüm noktaları (anchor points) ızgara çizgilerinin kesişim noktalarına (Snap to Grid) tam olarak oturt.
    - Her parçayı ayrı bir şekilde path et.
    - Motif rasyonel bir düzen için önce yarıya kadar çiz; ardından bu katmanı(yada hepsini bir) kopyalayıp çevir `Shift + F` (Flip Tool) ve simetri sağla.
    - **Hepsini bir seçerek yapmanın en temiz yolu:**
        - Tüm parçaları seç `Ctrl + A` > Yansıtmayacaklarını listeden çıkart `Ctrl + LeftClick` > `Shift + F` (Flip Tool) ve simetrisini al. 

        - Tam olarak bu yolu izlediğin de GIMP'i daha pürüzsüz kullanabildiğimi fark ettim, diğer türlü yansıtma işlemi sancılı gerçekleşiyor, ekstra ayarlamak zorunda kalabilirsin.

    ---
    - **Siyah-Beyaz Sınır Çizgileri**
    - Path ettiğin her parça için, yeni transparan bir katman oluştur
    - Seçtiğin path için şu yolu izle: `Select Path` > `Fill Path(Beyaz)` > `Shrink` > `Fill(Black)`. Bu sayede üstte olmasını istediğin motiflerin sınırları birbirlerine yapışmaz, **oyulmuş bir görüntü oluşur**.

#### p3-maru-ve-motif
- Bunun nasıl hesaplanması gerektiğine dair derin bir araştırma yapmadım, incelediğim çeşitli kamonların her biri farklı marulara sahip, çoğu zaman aynı kamon için farklı maru kalınlıkları tercih edilmiş. Bu nedenle göz zevkime göre yapmaya karar verdim.

- Maru dairesinin dışarı doğru taşmaması için daireyi bu şekilde ürettim:
    - Daire çizimi için, Tool: `Ellipse Select Tool` (E), Tool Options: `Fixed Aspect Ratio (1:1)` seçeneğini işaretle. `Expand from center` kutucuğunu aktif et.
    - Bucket Fill Tool( shift + B) ile siyaha boya
    - `Select` > `Shrink` > Tercihen `30-35px` > `OK` > `Alanı temizle` (Del)


#### p4-nasıl-isimlendirilir

- Google ve Claude ile araştırıp baktım, sanırım anladığım kadarıyla gerçekten de belirli bir standartta isimlendirme yapılmakta. 

- En yaygın kalıp: **"Maru ni ○○"** — yani bir motifin daire içine yerleştirilmesi .
    - maru (丸) = "çevreleyen daire" — bir çerçeve/sınır işlevi görür
    - ni (に) = "içinde" bağlacı
    - motif adı = aslında çizilen şey (yaprak, çiçek, hayvan, geometrik desen)
- **Sayı/tekrar bildiren ön ekler** motiften önce çoğunlukla kaç tane olduğunu belirten bir sayı sıfatı geliyormuş.
- + `[varsa çevreleyen şekil: maru]` + `Sayı/varyasyon` + `[Motif adı]`  + `(mon eki, formal kullanımda)`
 
[İlgili Makale](https://cocoro.faag.co.jp/en/what-is-a-japanese-family-crest-meaning-history-and-design/)

---
###  Notlar:
- Kağıt üzerinde çalışırken, eğer ölçülü çalışmak istiyorsan, kesinlikle hassas bir cetvelin olmalı, 1,1 gibi bir yuvarlama dahi oran orantıyı ciddi anlamda zedeledi. Görselleri incelersen, çizgilerin ne kadar eğrileştiğini ve karelerin tam olmadığını fark edeceksin, muhtemelen benim cetvel kullanma becerilerimin de tembel olmasının önemli bir payı var.

- GIMP bu iş için doğru araç olmayabilir, açık kaynak kodlu ve ücretsiz başka araçlarla çok daha rahat çalışılabilir, lakin GIMP ile devam edeceğim.



---