# Menderes düğüm yapbozu: dijital sürüm

İnce menderesler ve iki köprülü bağlar üzerine, tarayıcıda oynanan etkileşimli bir yapboz. Parçalar eksenin iki yanına dizilerek bir menderes kurulur. Kesişimlerdeki anahtar taşları, menderesin mi eksenin mi üstten geçeceğini belirler. Tek bir dokunuşla hangi düğümün ya da bağın kurulduğu görülür: bileşen sayısı, determinant, bağlanma sayısı, Jones polinomu ve Conway gösterimi.

> Makale künyesi: submitted to journal.

Bütün uygulama tek bir dosyadır: `index.html`.



## Nasıl oynanır

**Parçalar.** Küçük parça (B) iki komşu noktayı birleştiren yaydır. R<sub>r</sub> parçası 2r+2 noktayı kaplar; r çentiğine birer küçük parça oturur. Parçalar iki yoldan yerleştirilir:
- Kutudan tahtaya sürüklenir.
- Ya da önce kutudaki parçaya, sonra tahtada istenen yere dokunulur.

Yerleşmiş bir parçaya dokununca parça kalkar. Ardından tahtada başka bir yere dokununca oraya taşınır, kutuya dokununca kutuya döner. Tahtanın dışına sürüklenen parça da kutuya döner. Parça yalnız sığdığı yere oturur; büyük parçaların çentiklerine yalnız küçük parçalar girer.

**Taşlar.** Her kesişimde bir taş vardır. “Taşa dokununca” seçeneğine göre iki şey olur:
- **Çevir:** Alt/üst geçiş değişir; ya menderes ya eksen üstten geçer.
- **Düzleştir:** Kesişim iki yoldan düzleştirilir, sonra yeniden kesişime döner.

**Hazır düğmeler**

| Düğme | Ne yapar |
|---|---|
| Kur | Seçili ya da yazılı menderesi kurar |
| Rastgele menderes | Rastgele bir menderes kurar |
| Dağıt | Bütün parçaları kutuya geri koyar |
| Alterne | Tek numaralı kesişimlerde menderesi, çift numaralılarda ekseni üste alır |
| Hep menderes üstte | Bütün kesişimlerde menderesi üste alır |
| *n*. kesişimi düzleştir | Alterne ayarı kurar ve son kesişimi düzleştirir |
| Rastgele çevir | Taşları rastgele çevirir |
| Geri al | Son değişikliği geri alır |

**Takımlar**
- **16 kesişimli sabit takım** (menüde “Basılı takım”): 13 küçük parça, R1, R2 ve R4. Blok uzunlukları 1, 2 ve 4 olan altı menderes bu takımla kurulur.
- **Serbest:** Kesişim sayısı 4 ile 24 arasında seçilir ve parçalar sınırsızdır. Menderes bir ε kelimesiyle (örneğin `+--++++`) yazılır ya da ◀ ▶ düğmeleriyle bütün menderesler sırayla gezilir.

**“Hangi düğüm?”** Bu kart açıkken her değişiklikte güncellenir ve tahtadaki bileşenler ayrı renklerle gösterilir. Kurulum eksikse ya da yaylar tek bir eğri oluşturmuyorsa tahtanın altındaki durum satırı bunu söyler; ikinci durumda bağ yine hesaplanır.

**Bulmaca.** Sayfa bir hedef düğüm ya da bağ seçer. Doğru menderes ve taş ayarı bulununca hedef yeşile döner. “Çözümü göster” bir çözüm kurar.

Tarayıcı son durumu hatırlar.

## 3B, AR ve VR

**3B sekmesi**
- Görünüm parmakla ya da fareyle döndürülür, iki parmakla ya da tekerlekle yakınlaştırılır.
- Taşa dokununca çevrilir.
- Parçaya dokunup masada başka bir yere dokununca parça taşınır.
- Parça kutusu 3B'de de kullanılır.

**AR (Android, Chrome)**
- “Masada gör (AR)” düğmesine bas, telefonu masaya doğrult. Beyaz halka görününce ekrana dokun; yapboz gerçek boyutunda (24 mm nokta aralığı, yaklaşık 38 cm) masaya konur.
- Masadaki taşlara ve parçalara ekrandan dokunulur.
- Alttaki çubukta Alterne, Hangi düğüm?, Yeniden yerleştir ve Çık düğmeleri var.
- Telefonda Google Play Services for AR (ARCore) yüklü olmalı.

**VR (Meta Quest tarayıcısı)**
- Yapboz önündeki masanın üstünde durur.
- Denetleyici ışını bir taşa ya da parçaya tutulup tetiğe basılır; parça kutusu masanın ön tarafındadır.
- Havadaki panelde düğüm bilgisi ile Alterne, Hangi düğüm?, Çevir / Düzleştir, Rastgele menderes ve Çık düğmeleri bulunur.

claude.ai içinde açılan kopyada AR ve VR düğmeleri çalışmaz; oradaki çerçeve kamera ve XR izni vermez.

## Matematik

**İnce menderes.** Bir ε ∈ {+, −}<sup>n−1</sup> kelimesi, eksen üzerindeki 2n noktadan geçen bir menderesi belirler. Kelimedeki eşit işaretlerden oluşan r uzunluklu her blok, eksenin bir yanında bir R<sub>r</sub> yayına ve onun içindeki r küçük yaya karşılık gelir; işaret yayın hangi yanda olduğunu belirtir.

**Bağ ve düğüm.** Eksenin iki ucu, dışarıdan dolaşan bir yayla birleşmiş sayılır; bu yay yeni kesişim eklemez. Taşları çevirmek bileşen sayısını değiştirmez; düzleştirme olmadan sonuç her zaman iki bileşenli bir bağdır (menderes ve eksen). Bütün kesişimlerde menderes üstteyse iki halka birbirinden ayrılır. Bir kesişimin düzleştirilmesi iki bileşeni birleştirir ve tek bileşenli bir düğüm verir.

| ε | Alterne bağ | Son kesişim düzleştirilince | Taş öbür yüzüyle |
|---|---|---|---|
| +−−++++ | C(3,4,9), det 120 | C(3,4,8), det 107 | 7₃ = C(3,4), det 13 |
| +−−−−++ | C(3,8,5), det 128 | C(3,8,4), det 103 | C(3,8), det 25 |
| ++−++++ | C(5,2,9), det 104 | C(5,2,8), det 93 | 7₂ = C(5,2), det 11 |

## Hesap yöntemi

- **Kauffman parantezi:** Diyagram eksen boyunca soldan sağa taranır. Her adımda açık uçların eşleşmeleri ve bunlara ait Laurent polinomları tutulur. İnce menderesler dar olduğundan bu tarama 32 kesişime kadar anında biter.
- **Jones polinomu:** V(t) = (−A³)<sup>−w</sup>⟨D⟩, burada A = t<sup>−1/4</sup> ve w kıvrım sayısıdır. Determinant |V(−1)|'dir.
- **Bağlanma sayısı:** Bileşenler arası kesişimlerin işaretlerinin toplamının yarısıdır.
- **Ad ve Conway gösterimi:** Bir iki köprülü bağ, determinantı p'ye ve parantezinin genişliği 4c'ye eşit olan C(a₁, …, a<sub>k</sub>) ile aranır; burada a₁ + … + a<sub>k</sub> = c'dir. Adayların parantezi rasyonel yumak hesabıyla bulunur ve diyagramın parantezi ile birim çarpanına ve ayna görüntüsüne kadar karşılaştırılır. Eşleşme yoksa iki iki-köprülü parçanın bağlantılı toplamı ve “düğüm ⊔ çember” biçimindeki ayrık bağ denenir.
- **Düğüm adları:** 7 kesişime kadarki adlar, Rolfsen tablosundaki Conway gösterimlerinden alınmıştır.

Eşleştirme Jones polinomu düzeyindedir: iki bağın Jones polinomları ve determinantları aynıysa aynı ad verilir. Ayna görüntüsü ayırt edilmez.

## Doğrulama

- Jones polinomları, yapının bağımsız bir Python uygulamasıyla 5 menderes ve 125 rastgele taş ayarında karşılaştırıldı; hepsi birebir tuttu.
- Basılı takımla kurulan menderesler için daha önce elle bulunan sonuçlar aynen çıkıyor: C(3,4,9), C(3,8,5), C(3,4,8), C(3,8,4).
- 16 kesişimde 3000 rastgele ayar denendi; iki bileşene kadar olanların hepsi tanındı. Bunlar iki köprülü bağ, iki iki-köprülünün toplamı ya da ayrık bağ çıktı. Bu bir ispat değil, Jones polinomu düzeyinde bir gözlem.
- Arayüz masaüstü ve telefon boyutunda, fare ve dokunmayla sınandı. AR ve VR gerçek cihazda henüz sınanmadı.

## Kaynaklar

- J. H. Conway, *An enumeration of knots and links, and some of their algebraic properties*, Computational Problems in Abstract Algebra (J. Leech, ed.), Pergamon, 1970, 329–358.
- P. Di Francesco, O. Golinelli, E. Guitter, *Meanders and the Temperley–Lieb algebra*, Comm. Math. Phys. 186 (1997), 1–59.
- V. F. R. Jones, *A polynomial invariant for knots via von Neumann algebras*, Bull. Amer. Math. Soc. 12 (1985), 103–111.
- L. H. Kauffman, *State models and the Jones polynomial*, Topology 26 (1987), 395–407.
- L. H. Kauffman, S. Lambropoulou, *On the classification of rational knots*, L'Enseignement Math. 49 (2003), 357–410.
- S. K. Lando, A. K. Zvonkin, *Plane and projective meanders*, Theoret. Comput. Sci. 117 (1993), 227–241.
- W. B. R. Lickorish, *An Introduction to Knot Theory*, Graduate Texts in Mathematics 175, Springer, 1997.
- D. Rolfsen, *Knots and Links*, Publish or Perish, 1976.
- H. Schubert, *Knoten mit zwei Brücken*, Math. Z. 65 (1956), 133–170.

## Kullanılan yazılımlar

- three.js r147 (MIT lisansı), jsDelivr üzerinden: 3B görünüm, AR ve VR (WebXR).
- Yazı tipleri: Sora ve Inter (Google Fonts).
- Hesap ve 2B çizim: kütüphanesiz JavaScript ve SVG.

Tasarım ve kod Claude (Anthropic) ile birlikte hazırlandı.
# meanderpuzzle
