
![Shell Cheatsheet](https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/05df8cc2-4413-4a7c-93c7-dbf7991b18a7/ddzkgj0-fe2edca4-57ab-4dce-8899-ce94182a9160.png/v1/fill/w_1280,h_449,q_80,strp/shell_cheatsheet_by_markdownimgmn_ddzkgj0-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOiIsImlzcyI6InVybjphcHA6Iiwib2JqIjpbW3siaGVpZ2h0IjoiPD00NDkiLCJwYXRoIjoiXC9mXC8wNWRmOGNjMi00NDEzLTRhN2MtOTNjNy1kYmY3OTkxYjE4YTdcL2RkemtnajAtZmUyZWRjYTQtNTdhYi00ZGNlLTg4OTktY2U5NDE4MmE5MTYwLnBuZyIsIndpZHRoIjoiPD0xMjgwIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmltYWdlLm9wZXJhdGlvbnMiXX0.VYVfzUImBjcz2_b-_RRdfmOOdZju6u8gKFE-BOtQaD4)

Bu repo shell komutlarının türkçe açıklamalarını içerir. Ekleme için pull request'lere tamamiyle açıktır.

### Temel Komutlar

`pwd`: Neredeyiz? Şu an bulunduğumuz directory’i döndürür. (“print working directory”) 

`ls`: Bulunduğumuz directory’nin içindeki dosyaları ve klasörleri listeler (“listing”)

`cd directory_adı`: başka bir directory’e gitmek (“change directory”)

`touch dosya_adı`: Bulunduğumuz directory'de yeni dosya açar, uzantısını da belirtebiliriz

`cd ..` : Şu anda olduğumuz directory’nin bulunduğu klasöre gitmek için

`~` : home directory

`cd ~/../.`: 'home,' 'bir üst klasör', 'burası'

`cp klasör/dosya.csv backup/dosya.bck`: backup directory’sinde dosya.csv’nin kopyasını oluşturup ismini duplicate.txt yapar

`cp dosya1.txt dosya2.txt backup`: iki tane dosyayı backup’ta kopyalar

`mv`: dosyaları taşımak için (move)

`mv dosya_adi.txt yeni_dosya_adi.txt`: mv aynı şekilde dosyaların ve directory’lerin ismini değiştirmek için de kullanılır

`rm`: dosyaları silmek için (remove)

`rm dosya.txt backup/dosya-2.txt`: Directory’de ismi verilen iki dosyayı siler

`mkdir directory_ismi`: Yeni boş directory açar

`rm -rf directory_ismi`: Directory'i siler

`pbcopy`: sağına yazılanı clipboard'a kopyalar

## Data Manipulation

`less`: daha büyük dosyalara bakmak için kullanılır

`less`’e birden fazla dosya ismi verirsek `:n`’le bir sonraki dosyaya, `:p`’yla bir önceki dosyaya gideriz, `:q`’la çıkarız.

`head`: dosyanın başına bakmak için

### command line flags:

`head -n 3 directory/dosya_ismi.csv`: Dosyadaki ilk üç satırı getiriyor (“number of lines”)

`ls -R`: Bütün klasörleri ve içindekileri gösterir

`man`: Yanına yazılan command hakkında yardım eder (manual)

`cut`: csv dosyalarında kolonları seçer

`cut -f 2-5,8 -d , dosya.csv`: 2. ve 5. kolon arasındakileri seç. (flag'ler: -f (fields, kolonları belirtir), -d (delimiter, ayırıcı))

`grep`: dosyada arama yapar

`grep kelime directory/dosya.csv`: "kelime"yi içeren satırları getirir

grep’in flag’leri:

-   `-c`: kelimenin bulunduğu satır sayısı döndürür
-   `-h`: birden fazla dosyada arama yapıyorsa dosya isimlerini döndürmez
-   `-i`: büyük/küçük harf farkını yok sayar ("kelime" ve "Kelime"yi arar)
-   `-l`: eşleşme bulunan dosya isimlerini getirir, eşleşmeleri getirmez
-   `-n`: eşleşen satırların satır sıralarını döndürür
-   `-v`: eşleşme bulunmayan satırları döndürür

`paste`: iki tabloyu tek tablo yapar

### Command’lerin çıktılarını nasıl saklıyoruz?

`head -n 5 directory/dosya.csv > dosya2.csv`: çıktı dosya2.csv’ye gider.

çıkardığımız dosyanın içeriklerine `cat dosya2.csv`’yle bakabiliriz.

### pipe | operatörü:

pipe soldaki komutun çıktısını alıp sağa gönderiyor.

**örnek:** `head -n 5 directory/dosya.csv | tail -n 3`: beşinci satıra kadar aldı, sonra sondan üçüncüyü aldı (tail dosyanın sonundan alması gerektiğini belirtir)

**örnek:** `cut -d , -f 2 directory/dosyacsv | grep -v anahtar_kelime`:  `cut`’la dosya.csv’deki 2. kolonu seçti, `pipe`'la sağ tarafa `grep`’le "anahtar_kelime" kelimesinin geçmediği durumların aramasını yaptı

**örnek:** `cut -d , -f 1 directory/dosya.csv | grep -v Tarih | head -n 10`: dosya.csv verisinin ilk kolonunu seçtik, “Tarih” yazan header line’ı sildik ve ardından ilk on satırı aldık (`head` en baştaki satırları alması gerektiğini belirtir)

`wc`: kaç tane karakter, kelime, ya da satır varsa döndürür (“word count”)

## Wildcards

Komutlarda birden fazla dosya ismi verirsek birden fazla dosya üstüne çalışır. Bütün dosyaların hepsini tek tek yazmaktansa * operatörünü kullanırız 

    cut -d , -f 1 directory/*.csv

`cut -d , -f 1 directory/ka*.csv`: Klasörde kalem.csv ve kagit.csv isimli iki tane csv dosyası olsun, ikisini de seçmek için

`?` tek bir karakteri eşliyor, mesela `201?.txt` 2017.txt ve 2018.txt’yi eşliyor, ama 2017-01.txt’yi eşlemiyor.

`[…]`: köşeli parantezin içindeki bir karakteri eşler, mesela `201[78].txt` 2017.txt ya da 2018.txt’yi eşler.

`{…}`: `{*.txt, *.csv}` .txt ya da .csv’yle biten dosyaları eşler.

## sıralama yapmak
`sort` komutuyla yapılabilir.
`-n` flag’i: numerik olarak sıralar
`-r`: tersten sıralar
`-b`: boşlukları yok saymamızı sağlar
`-f`: büyük/küçük harfi yok saymamızı sağlar (folding)

**örnek:** `cut -d , -f 2 directory/dosya.csv | grep -v "anahtar_kelime" | sort -r`: aramayı tersten sıralar

`uniq`: çift yazılmış satırları siler

`cut -d , -f 2 directory/dosya.csv | grep -v "anahtar_kelime" | sort | uniq -c`: ikinci kolonu al, içinde anahtar_kelime geçmeyen çıktıları al, hepsini sırala, her eşleşme bir kez çıkacak şekilde göster ve kaç kez gözüktüğü yazsın

> Written with [StackEdit](https://stackedit.io/).
