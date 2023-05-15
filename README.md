# Floyd-Warshall-algoritmas-rnek
Floyd-Warshall algoritması kullanılan bir örnek

Kod adımlarının açıklaması:

function1 , fonksiyonu bir diziyi ve boyutunu girdi olarak alır ve kabarcık sıralama algoritmasını kullanarak diziyi artan olacak şekilde sıralar.

function2 , fonksiyonu bir tamsayı dizisini girdi olarak alır ve dizinin maksimum altdizi toplamının ortalamasını hesaplar. Önce t ve current_sum değişkenlerini başlatır. 
Sonra dizi boyunca döngüler yapar ve a[i] ile current_sum toplamının 0'dan büyük olup olmadığını kontrol eder. 
Eğer öyleyse, dizzi boyutunu current_sum a ekler. Değilse, current_sum'u sıfırlar.Son olarak, maksimum alt dizi toplamlarının ortalamasını döndürür.

function3 , fonksiyonu girdi olarak tamsayılardan oluşan bir matrisi alır ve Floyd-Warshall algoritmasını kullanarak grafikteki her köşe çifti arasındaki en kısa yolu hesaplar.
function3 fonksiyonu g dizisini kullanarak d dizisini doldurur. Eğer i ve j eşitse, d[i][j]'yi sıfır olarak ayarlar. Eğer g[i][j] sıfır değilse, d[i][j]'yi g[i][j] olarak ayarlar. Aksi halde, d[i][j]'yi INF olarak ayarlar.
Daha sonra fonksiyon, Floyd-Warshall algoritmasını kullanarak en kısa yolları bulur. Bu algoritma her düğüm çifti için en kısa yolun uzunluğunu bulur. Algoritma her düğüm için diğer tüm düğümlere olan en kısa yolu bulmak için tekrarlanır.

main fonksiyonu rasgele tamsayılardan oluşan bir dizi oluşturur, function1'i kullanarak sıralar print1 ile yazdırır, function2'yi kullanarak maksimum altdizi toplamının ortalamasını hesaplar print2 ile bunu yazdırır, function3'ü kullanarak bir grafikteki her köşe çifti arasındaki en kısa yolu hesaplar ve print3 ile sonuçları yazdırır.
Ayrıca clock() fonksiyonunu kullanarak programı çalıştırmak için geçen süreyi de hesaplar ve bu süreyi konsola yazdırır.



Kodun çalışma zamanı analizi aşağıda verilmiştir

main fonksiyonu içerisinde

generate fonksiyonu:

Bu fonksiyon, dizinin elemanlarına rastgele değerler atar.
Boyutu size olan bir dizi üzerinde döngü yapar ve her döngü adımında bir atama işlemi gerçekleştirir.
Bu işlemlerin zaman karmaşıklığı O(size)dir.


function1 fonksiyonu:

Bu fonksiyon, diziyi küçükten büyüğe doğru sıralar.
Boyutu size olan bir dizi üzerinde iç içe iki for döngüsü kullanır.
Bu işlemlerin zaman karmaşıklığı iç içe iki for döngüsü kullanıldığı için O(size^2)dir.


function2 fonksiyonu:

Bu fonksiyon, dizideki en büyük toplamı hesaplar.
Boyutu size olan bir dizi üzerinde tek bir döngü kullanır.
Her döngü adımında bir karşılaştırma ve bir atama işlemi gerçekleştirir.
Bu işlemlerin zaman karmaşıklığı O(size)dir.


function3 fonksiyonu:

Bu fonksiyon, girdi olarak verilen grafın tüm düğümleri arasındaki en kısa mesafeleri hesaplar (Floyd-Warshall algoritması).
Boyutu size olan bir 2D matris üzerinde üç döngü kullanır.
İç içe döngüler, her bir düğüm çifti için en fazla size karşılaştırma ve atama işlemi yapar.
Bu işlemlerin zaman karmaşıklığı O(size^3)dir.


print1 fonksiyonu:

Bu fonksiyon, bir diziyi ekrana yazdırır.
Boyutu size olan bir dizi üzerinde bir döngü kullanır.
Her döngü adımında bir yazdırma işlemi gerçekleştirir.
Bu işlemlerin zaman karmaşıklığı O(size)dir.


print2 fonksiyonu:

Bu fonksiyon, bir 2D matrisi ekrana yazdırır.
Boyutu size olan bir 2D matris üzerinde iki döngü kullanır.
İç içe döngüler, her bir matris elemanı için bir yazdırma işlemi yapar.
Bu işlemlerin zaman karmaşıklığı O(size^2)dir.


print3 fonksiyonu:

Boyutu size olan bir 2D matris üzerinde iki döngü kullanır.
İç içe döngüler, her bir matris elemanı için bir karşılaştırma ve yazdırma işlemi yapar.
Bu işlemlerin zaman karmaşıklığı O(size^2)dir.


Tüm adımların zaman karmaşıklığı toplamı:

O(size) + O(size^2) + O(size) + O(size^3) + O(size) + O(size^2) + O(size^2)

Zaman karmaşıklığı hesaplanırken en yüksek dereceli terim önemlidir. Bu kod için karmaşıklığı en yüksek terim O(size^3) olduğundan kodun zaman karmaşıklığı da O(size^3) olur.
