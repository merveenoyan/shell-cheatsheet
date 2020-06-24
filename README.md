
![Shell Cheatsheet](https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/05df8cc2-4413-4a7c-93c7-dbf7991b18a7/ddzkgj0-fe2edca4-57ab-4dce-8899-ce94182a9160.png/v1/fill/w_1280,h_449,q_80,strp/shell_cheatsheet_by_markdownimgmn_ddzkgj0-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOiIsImlzcyI6InVybjphcHA6Iiwib2JqIjpbW3siaGVpZ2h0IjoiPD00NDkiLCJwYXRoIjoiXC9mXC8wNWRmOGNjMi00NDEzLTRhN2MtOTNjNy1kYmY3OTkxYjE4YTdcL2RkemtnajAtZmUyZWRjYTQtNTdhYi00ZGNlLTg4OTktY2U5NDE4MmE5MTYwLnBuZyIsIndpZHRoIjoiPD0xMjgwIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmltYWdlLm9wZXJhdGlvbnMiXX0.VYVfzUImBjcz2_b-_RRdfmOOdZju6u8gKFE-BOtQaD4)

Bu repo shell komutlarının türkçe açıklamalarını içerir. Ekleme için pull request'lere tamamiyle açıktır.

### Temel Komutlar

`whoami`: Bulunan oturumun sahibi olan kullanıcıyı yazdırır.

`su`: Başka bir kullanıcının yetkileri ile komut çalıştırmak için yeni bir shell ayağa kaldırır. (“Örnek: su root”) 

`pwd`: Neredeyiz? Şu an bulunduğunuz dizini yazdırır. (“print working directory”) 

`ls`: Bulunduğumuz dizinin içindeki dosyaları ve dizinleri listeler. (“listing”)

`cd dizin_adı`: Bulunduğunuz dizini değiştirmenize yarar. (“change directory”)

`man`: Argüman olarak verdiğiniz komutun manuelini, kılavuzunu açar. (Örnek: man touch)

`touch dosya_yolu`: Belirttiğiniz yoldaki dosyanın son değiştirilme tarihini günceller. Böyle bir dosya yoksa bu dosyayı oluşturur.

`cd ..` : Hiyerarşik olarak bulunduğunuz dizinden üst dizine çıkmanıza yarar. (Örnek: Çalışma dizininiz /home/ali iken çalışma dizininizi /home yapar)

`~` : Oturumun sahibi kullanıcı için home dizinini belirtir. (Tilde sembolü)

`cd ~/../.`: Çalışma dizininizi "home"'un üst dizinine ayarlar. Sondaki nokta bulunulan en son klasörün kendisini belirtir.

`cp klasör/dosya.csv backup/dosya.bck`: "klasör" dizinindeki "dosya.csv" dosyasını, "backup" dizinine "dosya.bck" dosya ismiyle kopyalar.

`cp dosya1.txt dosya2.txt backup`: Belirtilen iki dosyayı ("dosya1.txt" ve "dosya2.txt") aynı isimle "backup" dizinine kopyalar.

`dd`: Dosya kopyalama ve dönüştürme yapar.Örneğin `dd if=/dev/sda of=./disk.img` ile /dev/sda diskinin tamamının imajını .img dosyası olarak alabilirsiniz.

`mv`: Dosyaları taşımak ya da yeniden adlandırmak için kullanılan komut (move)

`mv dosya_adi.txt yeni_dosya_adi.txt`: dosya_adi.txt'yi yeni_dosya_adi.txt olarak taşıdık. Böylece adını değiştirmiş olduk.

`rm`: Dosyaları silmek için kullanılan komut. ("remove")

`rm dosya.txt backup/dosya-2.txt`: Belirtilen iki dosyayı da siler.

`mkdir dizin_ismi`: dizin_ismi adında yeni bir dizin oluşturur.

`mkdir -p gecersiz_dizin/hedef_dizin`: gecersiz_dizin'in varolmaması durumunda hedef_dizin ile birlikte onu da açar.

`rm -rf dizin_ismi`: dizin_ismi adlı dizini içindeki dosyaları ve altdizinleri de dahil ederek siler.

`pbcopy`: Argüman olarak verilen değeri panoya kopyalar.

`cat dosya_ismi`: Dosyanın içeriğini ekrana yazdırır.

`df`: Dosya sisteminizdeki disk alanı hakkında bilgi edinmenizi sağlar.

`du`: Disk kullanımını görmek ve hangi uygulamanın yada dosya alt sisteminin ne kadar yer kapladığını görmek için kullanılır.

`ps`: Sisteminizde hangi işlemlerin çalıştığını görmenizi sağlar.

`groups`: Verilen kullanıcının gruplarını listeler. Örneğin `groups root`

`wget`: HTTP, HTTPS veya FTP protokollerini kullanan bir adresteki dosyayı terminal üzerinden doğruca kendi makinemize indirmek için kullanılan komut.

`grep`: Dosyaların içinde düzenli ifadelerle (RegEx) arama yapmanızı sağlayan komut. Log incelerken vazgeçilmezimiz.

`watch`: Belirli aralıklarla bir komutun çıktısını çalıştırarak ekrana yazdırır.(watch -n1 ls -la )

## Veri Manipülasyonu

`less`: Büyük dosyalara bakmak için kullanılan bir komut. Dosyanın tamamını ekrana yazdırmaz, daha okunabilir ilerlenebilir hale getirir.

`less`’e birden fazla dosya ismi verirsek `:n`’le bir sonraki dosyaya, `:p`’yla bir önceki dosyaya gideriz, `:q`’la çıkarız.

`more`: `less`' in eskisi. Sadece aşağıya kaydırmaya izin verir.

`head`: Dosyanın ilk parçasını (standart 10 satır) yazdırır.

`tail`:  Head  komutunun tam tersi  olarak dosyanın son parçasını yazdırır. '-f' parametresi ile kullanıldığı zaman dosyaya anlık olarak yazılan içeriği ekrana basar.
 
### Komut Satırı Bayrakları:

`head -n 3 directory/dosya_ismi.csv`: Dosyadaki ilk üç satırı getiriyor (“number of lines”)

`ls -R`: Bütün klasörleri ve içindekileri gösterir

`man`: Yanına yazılan komut hakkında yardım eder (manual)

`cut`: csv dosyalarında sütunları seçer

`cut -f 2-5,8 -d , dosya.csv`: 2. ve 5. sütun arasındakileri seç. (flag'ler: -f (fields, sütunları belirtir), -d (delimiter, ayırıcı))

`sed`: Akış editörü. Dosyalar üzerinde bir çok işlem yapmaya yarar. Örneğin `sed -i 's/aaaa/bbbb/g' test.txt` ile text.txt içerisinde ki her aaaa dizisi bbbb haline getirilebilir.

`awk`: Metin dosyalarını işlemek için kullanılır. Örneğin `awk  -F';' '{print$1}' test.txt` ile test.txt içerisindeki  satırları ';' ayracına göre sütunlara ayırır ve ilk sütunları ekrana yazdırır  

`find`: Dizin araması yapar. `find / -name "temp*"` ile / dizininde ismi temp ile başlayan tüm dosyalar aranabilir.

`grep`: dosyada arama yapar

`grep kelime directory/dosya.csv`: "kelime"yi içeren satırları getirir

`grep -Hirn kelime directory`: belirtilen dizin altında "kelime"yi içeren satırları getirir

grep’in flag’leri:

-   `-c`: kelimenin bulunduğu satır sayısı döndürür
-   `-h`: birden fazla dosyada arama yapıyorsa dosya isimlerini döndürmez
-   `-i`: büyük/küçük harf farkını yok sayar ("kelime" ve "Kelime"yi arar)
-   `-l`: eşleşme bulunan dosya isimlerini getirir, eşleşmeleri getirmez
-   `-n`: eşleşen satırların satır sıralarını döndürür
-   `-v`: eşleşme bulunmayan satırları döndürür

`paste`: iki tabloyu tek tablo yapar

### Komutların çıktılarını nasıl saklıyoruz?

**örnek:** `head -n 5 directory/dosya.csv > dosya2.csv`: çıktı dosya2.csv’ye gider.

çıkardığımız dosyanın içeriklerine `cat dosya2.csv`’yle bakabiliriz.

**örnek:** `head -n 5 directory/dosya.csv >> dosya2.csv` : çıktı dosya2.csv'ye gider.

fakat buradaki farklılık, `>` yerine `>>` kullanmamız. 
eğer `>>` kullanırsak, yazdığımız veriler dosyaya eklenir, dosyada halihazırda bulunan veriler silinmez.

yine aynı şekilde çıkardığımız dosyanın içeriklerine `cat dosya2.csv`’yle bakabiliriz.

**örnek:** `head -n 5 directory/dosya.csv 2> dosya2.csv` : oluşan hata dosya2.csv'ye gider.

buradaki farklılık ise `>` yerine `2>` kullanmamız. 
eğer `2>` kullanırsak, kullandığımız komutta oluşan hata çıktılarını dosyaya yazmış oluruz. 

**örnek:** `head -n 5 directory/dosya.csv > dosya2.csv 2> err.txt` 

buradaki komutta hata oluşmazsa çıktı dosya2.csv'ye, hata oluşursa oluşan hata çıktısı err.txt'ye yazılır.

### pipe | operatörü:

pipe soldaki komutun çıktısını alıp sağa gönderiyor.

**örnek:** `head -n 5 directory/dosya.csv | tail -n 3`: beşinci satıra kadar aldı, sonra sondan üçüncüyü aldı (tail dosyanın sonundan alması gerektiğini belirtir)

**örnek:** `cut -d , -f 2 directory/dosyacsv | grep -v anahtar_kelime`:  `cut`’la dosya.csv’deki 2. kolonu seçti, `pipe`'la sağ tarafa `grep`’le "anahtar_kelime" kelimesinin geçmediği durumların aramasını yaptı

**örnek:** `cut -d , -f 1 directory/dosya.csv | grep -v Tarih | head -n 10`: dosya.csv verisinin ilk kolonunu seçtik, “Tarih” yazan header line’ı sildik ve ardından ilk on satırı aldık (`head` en baştaki satırları alması gerektiğini belirtir)

`wc`: kaç tane karakter, kelime, ya da satır varsa döndürür (“word count”)

## Jokerler

Komutlarda birden fazla dosya ismi verirsek birden fazla dosya üstüne çalışır. Bütün dosyaların hepsini tek tek yazmaktansa * operatörünü kullanırız 

    cut -d , -f 1 directory/*.csv

`cut -d , -f 1 directory/ka*.csv`: Klasörde kalem.csv ve kagit.csv isimli iki tane csv dosyası olsun, ikisini de seçmek için

`?` tek bir karakteri eşliyor, mesela `201?.txt` 2017.txt ve 2018.txt’yi eşliyor, ama 2017-01.txt’yi eşlemiyor.

`[…]`: köşeli parantezin içindeki bir karakteri eşler, mesela `201[78].txt` 2017.txt ya da 2018.txt’yi eşler.

`{…}`: `{*.txt, *.csv}` .txt ya da .csv’yle biten dosyaları eşler.

## Sıralama Yapmak
`sort` komutuyla yapılabilir.
`-n` flag’i: numerik olarak sıralar
`-r`: tersten sıralar
`-b`: boşlukları yok saymamızı sağlar
`-f`: büyük/küçük harfi yok saymamızı sağlar (folding)

**örnek:** `cut -d , -f 2 directory/dosya.csv | grep -v "anahtar_kelime" | sort -r`: aramayı tersten sıralar

`uniq`: çift yazılmış satırları siler

`cut -d , -f 2 directory/dosya.csv | grep -v "anahtar_kelime" | sort | uniq -c`: ikinci kolonu al, içinde anahtar_kelime geçmeyen çıktıları al, hepsini sırala, her eşleşme bir kez çıkacak şekilde göster ve kaç kez gözüktüğü yazsın

## Dosya İzinleri

bazen kullandığımız dosyalar üzerinde yeterli iznimiz olmayabilir, veya önemli dosyaların başkaları tarafından okunup yazılmasını istemeyebiliriz. böyle durumlarda dosya izinlerini kullanabiliriz.

`chmod` komutu ile yapılabilir

`chmod` sekizlik(octal) sayı sistemi kullanır, bu sistemde `read` izni 4, `write` izni 2, `execute` izni ise 1 sayısı ile gösterilir.

bir sistemde ise temel olarak 3 kullanıcı vardır, bunlar sırasıyla 
- `owner` dosyanın sahibi
- `group` bilgisayar üzerinde kayıtlı olan kullanıcılar
- `other` geri kalan herkes

**örnek:** `chmod 644 file.txt` :  bu komut sonrasında file.txt'yi dosyanın sahibi okuyabilir/yazabilir. bilgisayar üzerinde kayıtlı olan kullanıcılar ve geri kalan herkes bu dosyayı sadece okuyabilir. 

buradaki 6 sayısı dosya sahibinin iznini, 4 sayısı bilgisayar üzerinde kayıtlı olan kullanıcıların iznini ve diğer 4 sayısı ise geri kalan herkesin iznini temsil eder.

izinleri hesaplamak basittir. mesela dosya sahibine okuma ve yazma izni vermek için 4+2=6, okuma ve çalıştırma izni vermek için ise 4+1, yani 5 yazabiliriz. hiçbir izin vermek istemiyorsak 0 yazabiliriz. sıralama ise daima owner-group-other şeklindedir.

## Sistem Bilgisi

`who`: Oturum açmış kullanıcıları listeler.

`lsusb`: USB aygıtları listeler. USB ile takılan aygıtın tanınıp tanınmadığını anlamaya yarıyor.

`dmesg`: Sistem yeni bir donanım tespit ettiğini ya da bir donanımın bağlantısının kesildiğini farkettiğinde oluşturduğu mesajları görmemizi sağlar. Bu sayede bir donanımın bağlı olup olmadığını anlayabiliriz.

`lsblk`: Sistemde ki diskleri ve partitionları gösterir.

`lsb_release -a`: Mevcut GNU/Linux dağıtımı hakkında bilgi verir.(Debian tabanlılarda test ettim).

`uname -a`: Sistem ve çekirdek hakkında bilgi verir.

`free`: RAM kullanımı ve durumu ile ilgili bilgi verir.

`du ./`: Verilen dizin içinde bulunan dosyaları ve boyutlarını listeliyor.

`tree ./`: Verilen dizini ağaç yapısı şeklinde listeler. İşe yarar.

`history`: Kullanıcının komut geçmişini ortaya döker. Bu kayıtlar genelde home dizini altında eğer kullanılan shell bash ise home dizini altında .bash_history dosyasında tutulur.

`top`: Terminal içinde görev yöneticisi. Kardeşi `htop` daha renkli ve daha fazla özelliğe sahip ama indirmek gerekiyor.

`kill`: Processlere sinyal göndermeye yarar. Mesela kilitlenen bir işlem varsa örneğin Firefox, PID numarası tespit edildikten sonra `kill -9 PID_Numarası` yazılarak Firefox'a SIGKILL gönderilebilir. Bu da Firefox'u kapatacaktır.

## Ağ

`ip a` :  Sistemde varolan tüm interface bilgilerini numaralandırarak ekrana basar.

`ifconfig`: Ağ arayüzleri hakkında bilgi verir. Sistemde ki ağ kartlarının MAC ve IP adreslerini bulmakta yardımcı oluyor.

`ping`: Parametre olarak girilen adrese ICMP paketleri atar. Windows' dan farklı olarak GNU/Linux sürümünde eğer müdahale edilmez ise sonsuza kadar ping atmaya devam eder. Windows' da yanılmıyorsam 3 tane atıp kendini durduruyor.

`netstat -antup`: Kullanımda olan portları listeler. LISTEN olanlara dikkat edilmesi iyi olur.

`route`: Sistemdeki yönlendirme tablosunu listeleme ve yönetme işlemlerini yapar. Host üzerinde tanımlı olan  bir arayüz üzerinden belirtilmiş hedeflere static yönlendirme yapar.

`tcpdump`: Sisteme gelen network trafigini incelemeye yarar. 

**örnek:** `tcpdump -i eth0` : Belirtilen arayüzün dinlenmesini sağlar. Gelen network paketlerini ekrana yazdırır.

# Bash Söz Dizimi
 ## Değişkenler

 degisken=1 veya degisken="yazı" şeklinde değişken tanımlaması yapılır, boşlukla değişken tanımlanması halinde hata alırsınız.

 DEGISKEN=1 veya DEGISKEN="yazı" bu şekilde global değişken tanımlayabilirsiniz. Kodlarınızın herhangi bir yerine;
 ```bash
 export DEGISKEN
 ```
 yazdıktan sonra birbirini tetikleyen scriptler yazmanız halinde dosyalar arası değişkenlerinizi kullanabilirsiniz.

 ## Değişkenleri Yazdırmak
 ```bash
 ad="Ömer"
 echo $ad

 > Ömer
 ```
 ```bash
 echo ad
 > ad
 echo '$ad'
 > $ad
 ```
 ### Cümle İçinde Yazdırmak
 ```bash
 echo "Selam Benim Adım, $ad"
 ```
 ## Bilinmesi Gereken Bazı Değişkenler
 - $#: Komut dosyasına kaç komut satırı parametresi geçirildi.
 - $@: Komut satırı parametrelerine iletilen tüm komut satırı parametreleri.
 - $?: Çalıştırılacak son işlemin çıkış durumu.
 - $$: Geçerli komut dosyasının İşlem Kimliği (PID).
 - $USER: Betiği çalıştıran kullanıcının kullanıcı adı.
 - $HOSTNAME: Komut dosyasını çalıştıran bilgisayarın ana bilgisayar adı.
 - $SECONDS: Betiğin çalıştığı saniye sayısı.
 - $RANDOM: Rastgele bir sayı döndürür.
 - $LINENO: Komut dosyasının geçerli satır numarasını döndürür.
 - $PATH: PATH değişkeninde bir komut yazıldığı anda sistem tarafından aranacak olan patika listesi görüntülenir.

 ## Aritmetik İşlemler
 ```bash
 let "a=2+3" # +(toplama), -(çıkarma), *(çarpma), /(bölme)
 echo $a
 > 5
 ```
 ##

 ## Aritmetik Kıyaslamalar
 - -gt büyük 
 - -lt küçük
 - -ge büyük eşit
 - -le küçük eşit 
 - -eq eşit 
 - -ne eşit değil

 ```bash
 sayi=2
 [ $sayi -eq 3 ]
 echo $?
 > 0
 [ $sayi -lt 2 ]
 echo $?
 >1
 ```

 ## If Kullanımı
 ```bash
 #!/bin/bash
 sayi=3

 if [ $sayi -eq 3]; then  
 # == da kullanabilirsiniz.
   echo Sayı eşit
 else
   echo Sayı eşit değil
 fi

 > Sayı eşit
 ```

 ## While Kullanımı

 ```bash
 #!/bin/bash
 sayi=2
 while [ $sayi -lt 100 ]
    do
         deger=$((deger+2))
         echo $sayi
    done
 ```
 Yukarıda görmüş olduğunuz $() kullanımı terminalde dönen çıktı anlamına gelir. 
 Örneğin;
 ```bash
 $ pwd
 > /user/omerayyildiz/Desktop
 $ masaustuYolu=$(pwd)
 $ echo $masaustuYolu
 > /user/omerayyildiz/Desktop
 ```

 ## For-Do Kullanımı
 ```bash
 #!/bin/bash
 for agac in akasya mese visne
    do
        echo $agac
     done
 > akasya mese visne
 ```