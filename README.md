# Fuzyy-logic
Projemde netlik derecesi ve uzaklık mesafesi değerlerinin alınarak kişinin göz sağlık durumunun belirlenmesinin sağlanmasını amaçlayarak projemi oluşturdum. 

Örnek Uygulama :  
 

Projemde giriş değeri olarak netlik derecesi ve uzaklık mesafesini kullandım. Çıkış değeri olarak ise göz sağlığı değerimi kullandım. Projemde kullandığım durulama fonksiyonum ise Mean of Maximum (En Büyük Üyelik Dereceli Elemanın Orta Noktası). Yani çıkarım sonucu elde ettiğim en büyük üyelik derecesine sahip noktaların aritmetik ortalaması yani orta noktasının alınması. Bunu kullanmamın sebebi ise sonucun daha kesin,sağlıklı bir şekilde belirlenmesidir. 

 

Problemin Girdi-Tanım Bilgisi : 

Projemde giriş değerleri olarak  kullanıcının giriş yaptığı netlik derecesi ve uzaklık mesafesini kullanmaktayım. 

#kullanıcı girişleri  

netlik_derecesi = input('Netlik derecesini 0 ile 7 değerleri arasında giriniz!!!!!!')  

uzaklık_mesafesi = input('uzaklık mesafesini 0 ile 4 değerleri arasında giriniz!!!!')  
Problemin Çıktı – Tanım Bilgisi  

Projem de girdi olarak aldığım uzaklık mesafesi ve netlik derecesi değerlerimi bulanık mantık işlemine tabi tutarak göz sağlık değerini oluşturmaktayım . 

print ("gozsaglıgı = " , durulama_islemi , " düzeyindedir")      

Bulanık Sistem Tasarımı : 

Projemde kullanıcıya girdirdiğimiz uzaklık mesafesi ve netlik derecesi değerlerinin bulanık mantık işleminden geçirerek ve belirlemiş olduğum kuralların katkısıyla oluşan sonuca göre göz sağlık değerinin bulanık mantık çıkarımlarına göre belirlenmesi 

 

Giriş ve Çıkış Değerleri Tanımlanması : 

Projemde kullandığım giriş ve çıkış değerlerimin aralıkları şöyledir. 

Girdi değerlerim: 

NDY = fuzz.trimf(netlikderecesi, [0 ,0, 2])  

NDO = fuzz.trimf(netlikderecesi, [0, 2, 5])  

NDD = fuzz.trimf(netlikderecesi, [5, 7, 7]) 

2.girdi değerim: 

UMY = fuzz.trimf(uzaklıkmesafesi, [0, 0, 2])  

UMO = fuzz.trimf(uzaklıkmesafesi, [0,2,4])  

UMD = fuzz.trimf(uzaklıkmesafesi, [2,4,4]) 

Cıktı değerim: 

GSCD = fuzz.trimf(gozsaglıgı, [0, 0, 20])  

GSD = fuzz.trimf(gozsaglıgı, [20, 30, 50])  

GSO = fuzz.trimf(gozsaglıgı, [40, 55, 70])  

GSY = fuzz.trimf(gozsaglıgı, [60, 70, 80])  

GSCY = fuzz.trimf(gozsaglıgı, [70, 100, 100])    
