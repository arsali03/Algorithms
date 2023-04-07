---Horspool Algoritması---

-Horspool algoritması, bir metin (text) içindeki belirli bir deseni (pattern) aramak için kullanılan bir string arama algoritmasıdır.
Bu algortima genellikle dosya okuma, metin işleme ve veritabanı arama gibi uygulamalarda kullanılmaktadır.Bu algoritma 
çalışırken ilk önce metin ve aranacak desen belirlenir. Daha sonra desen içindeki her karakter için, bir kaydırma tablosu 
(shift table) oluşturulur. Bu tablo desen içindeki karakterlerin metin içinde görüldüğü durumlarda ne kadar kaydırılacağını 
bulmak için kullanılacaktır. Metin içindeki desen aranırken desenin son karakterinden başlanılır. Eğer son karakter eşlenirse
bir önceki karakterin eşlenip eşlenmediğine bakılır ve bu böyle devam eder. Eğer son karakterde eşlenme olmazsa karakterin
desende bulunup bulunmadığına bakılır; bulunuyorsa shift tableda verilen değer kadar ileri kaydırılır, bulunmuyorsa desenin
karakter uzunluğu kadar ileri kaydırılır ve bu işlem desenin metin içinde bulunmasına kadar devam eder. Bu algoritma Boyer-Moore 
algoritmasına fazlasıyla benzemesine rağmen farklı bir algoritmadır. Kaydırma tablosu, karşılaştırma sırası, performans gibi 
farklılıkları vardır. Horspool algoritması, Boyer-Moore algoritması ile birlikte en hızlı string arama algoritmalarından biri olmasına 
rağmen, bazı durumlarda diğer algoritmalar daha hızlı olabilir.


---Ford-Fulkerson Algoritması---

Ford-fulkerson algoritması, en yaygın kullanılan akış ağı problemlerinden biri olan  maksimum akış (max-flow) problemini çözmek için kullanılan bir algoritmadır. Max-flow problemi bir ağ üzerinde kaynaktan (source), hedefe (sink) doğru ağdaki maksimum akışı sağlamak için kullanılan yolların belirlenmesi gereklidir. Algoritmanın amacı azami miktarda akışı sağlayabilmektir.

Algoritma aram işlemi sırasında derin öncelikli arama (depth first search,DFS) kullanıyorsa buna ford-fulkerson algoritması denir.

Bu yöntemde, bir artırıcı yol bulmak için kaynaktan hedefe doğru DFS kullanılır. DFS sırasında, kaynaktan hedefe giden bir yol bulunana kadar ilerlenir. Bu yolun üzerindeki en küçük kapasiteli kenarın kapasitesi, artırıcı kapasite olarak belirlenir ve bu kapasite kadar akış artırılır.

DFS tabanlı Ford-Fulkerson algoritması, BFS tabanlı algoritmadan daha hızlı olabilir ancak BFS tabanlı algoritma daha güvenilirdir ve daha geniş bir uygulama yelpazesine sahiptir.

---Çalışma Zamanı Analizi---

1. Graf yapısının matris boyutuna n x n diyelim.
2. Başlangıçta max-flow değeri sıfırdır.
3. Algoritma DPS kullanarak artan yol bulur ve bu yolları kullanarak max-flowu arttırır.
4. Max-flow değerindeki artış en az 1 olacağından algoritmanın en fazla n kere tekrar etmesi gerekir.
5. DPS için en kötü durum O(n^2) dır.



