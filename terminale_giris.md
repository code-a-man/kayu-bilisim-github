# Bash 101

Bu doküman, Bash terminalinde kullanılabilecek temel komutları ve kısa açıklamalarını içerir. Yeni başlayanlar için anlaşılır bir rehberdir.

---

## Temel Komutlar

### ls(*List*)  

  Bulunduğunuz dizindeki dosya ve klasörleri listeler.

### pwd(*Print Working Directory*)  

  Şu anda bulunduğunuz dizinin tam yolunu gösterir.

### cd(*Change Directory*)  

  Başka bir dizine geçiş yapmanızı sağlar. Örnek:  

- `cd desktop` → "desktop" adlı dizine geçer.

### .. , . , ~ , \*

- `..` → Bir üst dizine geçer.  
- `.` → Bulunduğunuz mevcut dizini ifade eder.  
- `~` → Kullanıcının ana dizinini ifade eder.  
- `*` → Dosya adı eşleştirme için joker karakterdir.

### clear

  Terminal ekranını temizler ve komut geçmişini yukarı kaydırır.

---

## Dosya ve Klasör İşlemleri

### mkdir(*Make Directory*)  

  Yeni bir klasör oluşturur. Örnek:  

- `mkdir denemeKlasoru` → "denemeKlasoru" adlı bir klasör oluşturur.

### touch

  Yeni bir dosya oluşturur. Örnek:  

- `touch deneme.txt` → "deneme.txt" adlı bir dosya oluşturur.

### cat(*Concatenate*)

  Dosya içeriğini terminalde görüntüler. Örnek:  

- `cat dosya.txt` → "dosya.txt" dosyasının içeriğini gösterir.

### rm(*Remove*)  

  Dosya veya klasörleri siler. Örnek:  

- `rm deneme.txt` → "deneme.txt" dosyasını siler.  
- `rm -rf denemeKlasoru` → "denemeKlasoru" adlı klasörü ve içindekileri siler.  Uyarı:*Yanlış kullanımda dosyalarınızı geri alamazsınız!*

### cp(*Copy*)  

Bir dosyayı veya klasörü kopyalar. Örnek:  

- `cp dosya.txt yeni_dosya.txt` → "dosya.txt" adlı dosyayı "yeni_dosya.txt" olarak kopyalar.

### mv(*Move/Rename*)  

Dosyaları taşır veya yeniden adlandırır. Örnek:  

- `mv dosya.txt yeni_dosya.txt` → "dosya.txt" dosyasını "yeni_dosya.txt" olarak yeniden adlandırır.  
- `mv dosya.txt /home/kullanici` → "dosya.txt" dosyasını belirtilen dizine taşır.

### find(*Search for Files*)  

Belirli bir dizinde dosya veya klasör arar.  
Örnekler:  

- `find . -name "dosya.txt"` → Bulunduğunuz dizinde "dosya.txt" dosyasını arar.  
- `find /home -type d -name "klasoradi"` → "/home" altında adı "klasoradi" olan dizinleri arar.  

### grep(*Search in Files*)  

Belirli bir metni dosyalar içinde arar.  
Örnekler:  

- `grep "anahtar kelime" dosya.txt` → "dosya.txt" içinde "anahtar kelime" geçen satırları gösterir.  
- `grep -r "anahtar kelime" /home` → "/home" dizini altındaki tüm dosyalarda "anahtar kelime"yi arar.  

### tar(*Archive Management*)  

Dosyaları sıkıştırmak veya sıkıştırılmış dosyaları açmak için kullanılır.  
Örnekler:  

- `tar -czvf arsiv.tar.gz dosya1 dosya2` → "dosya1" ve "dosya2"yi "arsiv.tar.gz" olarak sıkıştırır.  
- `tar -xzvf arsiv.tar.gz` → "arsiv.tar.gz" dosyasını çıkarır.  

### chmod(*Change Permissions*)  

Dosya veya klasör izinlerini değiştirir.  
Örnek:  

- `chmod 755 dosya.txt` → "dosya.txt" için kullanıcıya tam izin verir, diğer kullanıcılara sadece okuma ve çalıştırma izni sağlar.  

### chown(*Change Ownership*)  

Bir dosya veya klasörün sahipliğini değiştirir.  
Örnek:  

- `sudo chown kullanici:grup dosya.txt` → "dosya.txt" dosyasının sahipliğini belirtilen kullanıcı ve gruba verir.  

### nano` / `vim(*Text Editors*)  

Terminalde metin düzenlemek için kullanılan araçlardır.  

- `nano dosya.txt` → Basit bir metin düzenleyici.  
- `vim dosya.txt` → Daha gelişmiş ve güçlü bir düzenleyici (daha fazla öğrenme eğrisi gerektirir).  

---

## Sistem Güncelleme

### sudo apt update && sudo apt upgrade

  Sistemin mevcut yazılım paketlerini günceller.  

- `sudo apt update` → Paket listesini günceller.  
- `sudo apt upgrade` → Paketlerin en son sürümlerini yükler.  

---

## Eğlenceli Komutlar

### cowsay -f tux "Hello Linux"

  Terminal ekranında bir penguenin "Hello Linux" yazısını konuşuyormuş gibi göstermesini sağlar. Eğlenceli bir görsel komuttur.

---

## Ek Linux Komutları

### echo

Ekrana bir mesaj veya metin yazdırır. Örnek:  

- `echo "Merhaba Linux"` → Terminalde "Merhaba Linux" yazar.

### whoami

Hangi kullanıcı olarak oturum açtığınızı gösterir.

### date

Sistemin tarih ve saatini görüntüler.

### man(*Manual*)  

Komutlar için detaylı açıklamaları içeren kılavuzu açar. Örnek:  

- `man ls` → "ls" komutunun ne işe yaradığını, tüm seçeneklerini ve kullanım detaylarını gösterir.

### history

Daha önce çalıştırdığınız komutların bir listesini gösterir.
Örnekler:

- `history` → Tüm komut geçmişini gösterir.
- `history 10` → Son 10 komutu gösterir.
- `history | grep "aranan"` → Daha önce çalıştırdığınız komutlar arasında "aranan" kelimesini arar. (Burada "|" işareti, komutları birbirine bağlar.)

### wget(*Web Get*)

Bir web sitesinden dosya indirmenizi sağlayan bir komuttur. Özellikle dosya indirme işlemlerinde kullanılır.  
Örnek:

- `wget https://linux101.local/banner-main.webp` → "banner-main.webp" adlı dosyayı belirtilen URL'den indirir.  
Not:Bazı sitelerde indirme işlemi için internet erişim izni gerekebilir.

### convert(*ImageMagick*)

Görselleri farklı formatlara dönüştürmek veya boyutlandırmak için kullanılan bir komuttur.  
Örnekler:

- `convert dosya.png dosya.jpg` → "dosya.png" görselini "dosya.jpg" olarak dönüştürür.
- `convert -resize 50% orijinal.jpg yeni.jpg` → Görselin boyutunu %50 küçültüp "yeni.jpg" olarak kaydeder.  
Not:Bu komut, sistemde *ImageMagick* yüklü olduğunda çalışır.

## Alias Oluşturma

Bash terminalinde sık kullandığınız komutlar için kısayol oluşturabilirsiniz.

### alias

  Sık kullanılan bir komut için kısayol oluşturur. Aynı zamanda tek başına kullanıldığında tanımlı kısayolları listeler.
  Örnekler:

- `alias ll='ls -alF'` → "ll" komutunu "ls -alF" komutunun kısayolu olarak tanımlar.
- `alias c='clear'` → "c" komutunu "clear" komutunun kısayolu olarak tanımlar.
- `alias update='sudo apt update && sudo apt upgrade -y'` → "update" komutunu "sudo apt update && sudo apt upgrade" komutlarının kısayolu olarak tanımlar.

Kalıcı alias tanımlamak için `~/.bashrc` dosyasına tanımlamalar ekleyebilirsiniz.

## Sistem İzleme ve Yönetim Araçları

### htop

Sistemin donanım ve işlem kaynaklarını gerçek zamanlı olarak izlemek için kullanılan bir araçtır. *htop*, *top* komutunun daha kullanıcı dostu ve görselli bir alternatifidir.

- `htop` → CPU, RAM, işlemler gibi sistem bilgilerini detaylı ve renkli bir arayüzde gösterir.  
Not:Bu komutu çalıştırmadan önce `sudo apt install htop` ile kurulum yapmanız gerekebilir.

### btop(*Better Top*)

*htop* komutunun daha modern ve detaylı bir sürümüdür. Sistem kaynaklarını grafiksel bir şekilde izlemek için kullanılır.

- `btop` → İşlemci, bellek, disk, ağ kullanımı ve işlemleri görselli bir arayüzde gösterir.  
Not:*btop* modern sistemlerde tercih edilen bir alternatiftir ve kurulumu için `sudo apt install btop` komutunu kullanabilirsiniz.

Dokümanınız oldukça kapsamlı olmuş, fakat Linux dünyasında temel seviyede sık kullanılan bazı komutlar eksik olabilir. İşte eklemeyi düşünebileceğiniz birkaç komut:  

### ps(*Process Status*)  

Çalışan işlemleri listeler.  
Örnek:  

- `ps aux` → Tüm çalışan işlemleri gösterir.  
- `ps -u kullanici` → Belirtilen kullanıcının işlemlerini listeler.  

### kill ve killall(*Terminate Processes*)  

Çalışan bir işlemi sonlandırır.  
Örnekler:  

- `kill PID` → Belirli bir işlem kimliği (PID) ile işlemi sonlandırır.  
- `kill -9 PID` → İşlemi zorla sonlandırır.
- `killall isim` → Belirli bir isme sahip tüm işlemleri sonlandırır.  
