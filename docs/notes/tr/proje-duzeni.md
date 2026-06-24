## Proje içi düzen
**Bağlam:** Çalışma ortamı hiyerarşisini nasıl kurmalıyım, [22/06/26 / GIMP 3.2.0]
### Problem
- **p1-modüler-yapı**
Bütün projeyi olabildiğince modüler bir yapı da inşa etmem gerekiyor, hem daha düzenli ve kontrollü olması için hem de GIMP'in teknik alt yapısı nedeniyle daha sürdürülebilir olması için.  

### Çözüm
#### p1-modüler-yapı
- GIMP içi klasörleme formatı:
    - `maru-one-example-mon` > Ana proje adı. [İsimlendirme](/docs/notes/tr/ilk-cizim.md#p4-nasıl-isimlendirilir) 
        - `parts` > Motifin tüm parçaları/layerları.
        - `base`  > Motifin işlendiği yüzey dosyaları.
            - `paper` > Motifin arka planı.
            - `maru`  > Motifi çevreleyen şekil yani çember.
            - `reflection` > Motifin aynı yansımasını alıp bu tarafa atmayı tercih ettim.
- `Path` isimleri ile `Layer` isimleri aynı olsun, çünkü ikisi farklı katmanlarda, birbirlerinden ayrı. Düzeni takip etmek açısından kolaylık sağlıyor.

---
### Sonuç

- **[kamon-master-8Grid.xcf](/docs/workbook/templates/)**     

---