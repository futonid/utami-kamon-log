## Şablonlar nasıl olmalı
**Bağlam:** Şablonların nasıl olması gerektiğine dair genel analiz, **[19/06/26]**

### Problemler
- **p1-şablon-ölçü**    
    Şablonların ölçüleri hakkında net bir bilgim yok.
    

- **p2-grid-yapısı**   
    Şablonların sahip olması gereken düzen hakkında net bir bilgim yok.

---
### Çözümler
#### p1-şablon-ölçü:
- Logo ölçüleri için araştırma yaptım. 
- Ölçeklendirilebilir şablon boyutu: **1200 x 1200 px**
- **Kaynak:** [Logo](/docs/workbook/references/research.md#logo)


#### p2-grid-yapısı:
- Dijital ortam da Kamon tasarımı için araştırma yaptım.
- Tasarım probleminin gereksinimlerine göre grid sistemi oluşturulacak.
- Kamonlar sıklıkla daire (maru) formunu temel alır ve simetriye dayanır.
- Motif seçilmeli ve motife uygun çalışılmalı
- Maru içinde mi yoksa serbest mi olacağına karar verilmeli.
- **Kaynak:** [Kamon](/docs/workbook/references/research.md#kamon)
---
### Sonuç
#### Grid Hesabı
- Görselin yerleşeceği toplam alan, altın oranla bölmek
- 1200/1,618 ≈ 741 piksellik bir merkezi kare oluşturarak tasarıma nefes alacak bir çerçeve sağlar.
- Sayfa kenarlarından Margin(boşluk) bırakılmalı.
- Izgara Modülleri kullanılabilir
- Küçük Birimler: Izgara sistemi, iki boyutlu bir düzlemi daha küçük hücrelere ayırır. Bu hücrelere "alan" veya "modül" denir
- Yapı Taşları: Tasarladığınız bitki motifinin parçalarını (yaprak, sap vb.) bu modüllerin içine veya birkaç modülü birleştirerek oluşturduğunuz alanlara yerleştirirsiniz
- Hesaplama Örneği: 1200 piksellik alanınızdan kenar boşluklarını (örneğin her yandan 100 piksel) çıkardınız; elinizde 1000 piksellik net alan kaldı. Eğer 8 sütunlu bir ızgara istiyorsanız, 1000 / 8 = 125 piksellik kare modüller elde edersiniz
- **Kaynak:** [Grid System](/docs/workbook/references/research.md#grid-system)

**Not:** Kaynakların analizinde NotebookLM'den faydalandım.

---