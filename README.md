﻿
![Shell Cheatsheet](https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/05df8cc2-4413-4a7c-93c7-dbf7991b18a7/ddzkgj0-fe2edca4-57ab-4dce-8899-ce94182a9160.png/v1/fill/w_1280,h_449,q_80,strp/shell_cheatsheet_by_markdownimgmn_ddzkgj0-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOiIsImlzcyI6InVybjphcHA6Iiwib2JqIjpbW3siaGVpZ2h0IjoiPD00NDkiLCJwYXRoIjoiXC9mXC8wNWRmOGNjMi00NDEzLTRhN2MtOTNjNy1kYmY3OTkxYjE4YTdcL2RkemtnajAtZmUyZWRjYTQtNTdhYi00ZGNlLTg4OTktY2U5NDE4MmE5MTYwLnBuZyIsIndpZHRoIjoiPD0xMjgwIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmltYWdlLm9wZXJhdGlvbnMiXX0.VYVfzUImBjcz2_b-_RRdfmOOdZju6u8gKFE-BOtQaD4)

✍️ Bu repo shell komutlarının türkçe açıklamalarını içerir. Ekleme için pull request'lere tamamiyle açıktır.

# Temel Komutlar

`whoami`: Bulunan oturumun sahibi olan kullanıcıyı yazdırır.

`pwd`: Neredeyiz? Şu an bulunduğunuz dizini yazdırır. (“print working directory”) 

`ls`: Bulunduğumuz dizinin içindeki dosyaları ve dizinleri listeler. (“listing”)

`cd dizin_adı`: Bulunduğunuz dizini değiştirmenize yarar. (“change directory”)

`man`: Argüman olarak verdiğiniz komutun manuelini, kılavuzunu açar.> (Örnek: man touch)

`touch dosya_yolu`: Belirttiğiniz yoldaki dosyanın son değiştirilme tarihini günceller. Böyle bir dosya yoksa bu dosyayı oluşturur.

`cd ..` : Hiyerarşik olarak bulunduğunuz dizinden üst dizine çıkmanıza yarar.> (Örnek: Çalışma dizininiz /home/ali iken çalışma dizininizi /home yapar)

`~` : Oturumun sahibi kullanıcı için home dizinini belirtir. (Tilde sembolü)

`cd ~/../.`: Çalışma dizininizi "home"'un üst dizinine ayarlar. Sondaki nokta bulunulan en son klasörün kendisini belirtir.

`cp klasör/dosya.csv backup/dosya.bck`: "klasör" dizinindeki "dosya.csv" dosyasını, "backup" dizinine "dosya.bck" dosya ismiyle kopyalar.

`cp dosya1.txt dosya2.txt backup`: Belirtilen iki dosyayı ("dosya1.txt" ve "dosya2.txt") aynı isimle "backup" dizinine kopyalar.

`mv`: Dosyaları taşımak ya da yeniden adlandırmak için kullanılan komuttur. (move)

`mv dosya_adi.txt yeni_dosya_adi.txt`: dosya_adi.txt'yi yeni_dosya_adi.txt olarak taşıdık. Böylece adını değiştirmiş olduk.

`rm`: Dosyaları silmek için kullanılan komut. ("remove")

`rm dosya.txt backup/dosya-2.txt`: Belirtilen iki dosyayı da siler.

`mkdir dizin_ismi`: dizin_ismi adında yeni bir dizin oluşturur.

`mkdir -p gecersiz_dizin/hedef_dizin`: gecersiz_dizin'in varolmaması durumunda hedef_dizin ile birlikte onu da açar.

`rm -rf dizin_ismi`: dizin_ismi adlı dizini içindeki dosyaları ve altdizinleri de dahil ederek siler.

`pbcopy`: Argüman olarak verilen değeri panoya kopyalar.

`cat dosya_ismi`: Dosyanın içeriğini ekrana yazdırır.

`df`: Dosya sisteminizdeki disk alanı hakkında bilgi edinmenizi sağlar.

`ps`: Sisteminizde hangi işlemlerin çalıştığını görmenizi sağlar.

`wget`: HTTP, HTTPS veya FTP protokollerini kullanan bir adresteki dosyayı terminal üzerinden doğruca kendi makinemize indirmek için kullanılan komut.

`grep`: Dosyaların içinde düzenli ifadelerle (RegEx) arama yapmanızı sağlayan komut. Log incelerken vazgeçilmezimiz.

# Veri Manipülasyonu

`less`: Büyük dosyalara bakmak için kullanılan bir komut. Dosyanın tamamını ekrana yazdırmaz, daha okunabilir ilerlenebilir hale getirir.

`less`’e birden fazla dosya ismi verirsek `:n`’le bir sonraki dosyaya, `:p`’yla bir önceki dosyaya gideriz, `:q`’la çıkarız.

`head`: Dosyanın ilk parçasını (standart 10 satır) yazdırır.

# Komut Satırı Bayrakları

`head -n 3 directory/dosya_ismi.csv`: Dosyadaki ilk üç satırı getirir. (“number of lines”)

`ls -R`: Bütün klasörleri ve içindekileri gösterir.

`man`: Yanına yazılan komut hakkında yardım eder. (manual)

`cut`: csv dosyalarında sütunları seçer.

`cut -f 2-5,8 -d , dosya.csv`: 2. ve 5. sütun arasındakileri seçer. (flag'ler: -f (fields, sütunları belirtir), -d (delimiter, ayırıcı))

`grep`: Dosyada arama yapar.

`grep kelime directory/dosya.csv`: "kelime"yi içeren satırları getirir.

`grep -Hirn kelime directory`: Belirtilen dizin altında "kelime"yi içeren satırları getirir.

## Grep komutunun flag’leri:

-   `-c`: Kelimenin bulunduğu satır sayısı döndürür.
-   `-h`: Birden fazla dosyada arama yapıyorsa dosya isimlerini döndürmez.
-   `-i`: Büyük/küçük harf farkını yok sayar. ("kelime" ve "Kelime"yi arar.)
-   `-l`: Eşleşme bulunan dosya isimlerini getirir, eşleşmeleri getirmez.
-   `-n`: Eşleşen satırların satır sıralarını döndürür.
-   `-v`: Eşleşme bulunmayan satırları döndürür.

`paste`: İki tabloyu tek tablo yapar.

# Komutların Çıktılarını Nasıl Saklarız?

>**Örnek:** `head -n 5 directory/dosya.csv > dosya2.csv`: çıktı dosya2.csv’ye gider.

Çıkardığımız dosyanın içeriklerine `cat dosya2.csv`’yle bakabiliriz.

>**Örnek:** `head -n 5 directory/dosya.csv >> dosya2.csv` : çıktı dosya2.csv'ye gider.

Fakat buradaki farklılık, `>` yerine `>>` kullanmamız. 
eğer `>>` kullanırsak, yazdığımız veriler dosyaya eklenir, dosyada halihazırda bulunan veriler silinmez.

Yine aynı şekilde çıkardığımız dosyanın içeriklerine `cat dosya2.csv`’yle bakabiliriz.

>**Örnek:** `head -n 5 directory/dosya.csv 2> dosya2.csv` : oluşan hata dosya2.csv'ye gider.

Buradaki farklılık ise `>` yerine `2>` kullanmamız. 
eğer `2>` kullanırsak, kullandığımız komutta oluşan hata çıktılarını dosyaya yazmış oluruz. 

>**Örnek:** `head -n 5 directory/dosya.csv > dosya2.csv 2> err.txt` 

Buradaki komutta hata oluşmazsa çıktı dosya2.csv'ye, hata oluşursa oluşan hata çıktısı err.txt'ye yazılır.

# pipe | operatörü:

## pipe soldaki komutun çıktısını alıp sağa gönderir.

>**Örnek:** `head -n 5 directory/dosya.csv | tail -n 3`: beşinci satıra kadar aldı, sonra sondan üçüncüyü aldı (tail dosyanın sonundan alması gerektiğini belirtir)

>**Örnek:** `cut -d , -f 2 directory/dosyacsv | grep -v anahtar_kelime`:  `cut`’la dosya.csv’deki 2. kolonu seçti, `pipe`'la sağ tarafa `grep`’le "anahtar_kelime" kelimesinin geçmediği durumların aramasını yaptı.

>**Örnek:** `cut -d , -f 1 directory/dosya.csv | grep -v Tarih | head -n 10`: dosya.csv verisinin ilk kolonunu seçtik, “Tarih” yazan header line’ı sildik ve ardından ilk on satırı aldık. (`head` en baştaki satırları alması gerektiğini belirtir)

`wc`: kaç tane karakter, kelime, ya da satır varsa döndürür (“word count”)

# Jokerler

Komutlarda birden fazla dosya ismi verirsek birden fazla dosya üstüne çalışır. Bütün dosyaların hepsini tek tek yazmaktansa * operatörünü kullanırız 

    cut -d , -f 1 directory/*.csv

`cut -d , -f 1 directory/ka*.csv`: Klasörde kalem.csv ve kagit.csv isimli iki tane csv dosyası olsun, ikisini de seçmek için kullanırız.

`?`: Tek bir karakteri eşliyor, mesela `201?.txt` 2017.txt ve 2018.txt’yi eşliyor, ama 2017-01.txt’yi eşlemiyor.

`[…]`: Köşeli parantezin içindeki bir karakteri eşler, mesela `201[78].txt` 2017.txt ya da 2018.txt’yi eşler.

`{…}`: `{*.txt, *.csv}` .txt ya da .csv’yle biten dosyaları eşler.

# Sıralama Yapmak
- `sort` komutuyla yapılabilir.
- `-n` flag’i: numerik olarak sıralar
- `-r`: tersten sıralar
- `-b`: boşlukları yok saymamızı sağlar
- `-f`: büyük/küçük harfi yok saymamızı sağlar (folding)

>**Örnek:** `cut -d , -f 2 directory/dosya.csv | grep -v "anahtar_kelime" | sort -r`: aramayı tersten sıralar.

`uniq`: Çift yazılmış satırları siler.

`cut -d , -f 2 directory/dosya.csv | grep -v "anahtar_kelime" | sort | uniq -c`: İkinci kolonu al, içinde anahtar_kelime geçmeyen çıktıları al, hepsini sırala, her eşleşme bir kez çıkacak şekilde göster ve kaç kez gözüktüğü yazsın.

# Dosya İzinleri

Bazen kullandığımız dosyalar üzerinde yeterli iznimiz olmayabilir, veya önemli dosyaların başkaları tarafından okunup yazılmasını istemeyebiliriz. böyle durumlarda dosya izinlerini kullanabiliriz.

`chmod` komutu ile yapılabilir.

`chmod` sekizlik(octal) sayı sistemi kullanır, bu sistemde `read` izni 4, `write` izni 2, `execute` izni ise 1 sayısı ile gösterilir.

Bir sistemde ise temel olarak 3 kullanıcı vardır, bunlar sırasıyla:
- `owner` dosyanın sahibi
- `group` bilgisayar üzerinde kayıtlı olan kullanıcılar
- `other` geri kalan herkes

>**Örnek:** `chmod 644 file.txt` :  bu komut sonrasında file.txt'yi dosyanın sahibi okuyabilir/yazabilir. bilgisayar üzerinde kayıtlı olan kullanıcılar ve geri kalan herkes bu dosyayı sadece okuyabilir. 

Buradaki 6 sayısı dosya sahibinin iznini, 4 sayısı bilgisayar üzerinde kayıtlı olan kullanıcıların iznini ve diğer 4 sayısı ise geri kalan herkesin iznini temsil eder.

İzinleri hesaplamak basittir. mesela dosya sahibine okuma ve yazma izni vermek için 4+2=6, okuma ve çalıştırma izni vermek için ise 4+1, yani 5 yazabiliriz. hiçbir izin vermek istemiyorsak 0 yazabiliriz. sıralama ise daima owner-group-other şeklindedir.