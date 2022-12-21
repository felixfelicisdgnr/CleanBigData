# CleanBigData
Bu projede müşteri şikayetleri kayıtlarının tutulduğu bir veri seti içerisindeki benzer kayıtlar tespit edilmiş 
ve tespit edilen kayıtlar masaüstü uygulamasında gösterilmiştir. Multithreading kullanarak benzerlik arama süresini düşürmek amaçlanmaktadır.

Projenin Amacı
Veri seti içerisindeki arama işlem süresini multithreading kullanılarak azaltmak. Belirtilen sütun/sütunlar için her bir satırdaki kayıtların birbiriyle kelime bazlı karşılaştırılması ve aralarındaki benzerliğin tespit edilmesi. 
Uygulama içerisinde istenen özelliklere göre kayıtları filtrelemek ve kullanıcıya göstermek. 
Masaüstü uygulama geliştirme hakkında bilgi ve beceriye sahip olmamız hedeflenmektedir.

Verilerin Temizlenmesi
Bu projede bize verilen 1000000000 verilik kuralsız veri setindeki verilerimizi 
temizlemek için Python pandas kütüphanesini kullandık.

Bu veri seti; finansal ürünler ve hizmetler hakkında alınan
gerçek dünya şikayetlerini içermektedir.Veri seti, müşterilerin 

Kredi Raporları, Öğrenci Kredileri, Para Transferi vb. gibi 
finans sektöründeki birden fazla ürün ve hizmet hakkında 
yaptığı şikayetlerin farklı bilgilerini içermektedir.

● Veri seti aşağıdaki kurallara uygun olacak şekilde yeniden düzenlenmiştir.
○ Elde edilen tabloda 6 farklı sütun bulunmalıdır: Product (Ürün), Issue (Konu), 
Company (Şirket), State, Complaint ID, Zip Code.
○ Null değer içeren kayıtlar bulunmamaktadır.
○ Kayıtlardaki noktalama işaretleri kaldırılmıştır.
○ Kayıtlardaki stop word’ler kaldırılmıştır. 

4.3 Benzerlik Tespiti

Benzerlik tespti için

Geliştirilecek projede tüm kayıtlar arasındaki benzerlik ilişkisinin incelenmesi beklenmektedir. 

Bu nedenle her bir kaydın diğer bir kayıtla karşılaştırılması gerekmektedir. 
Karşılaştırmanın mümkün olduğunca hızlı olması için multithread kullanılmalıdır.
Benzerlik, kayıtların içerdikleri ortak kelime sayısına göre olmalıdır. Örneğin; ilk kayıt 5, ikinci kayıt 4 kelimeden 
oluşuyorsa ve ortak kelime sayısı 2 ise benzerlik oranı;
2 (𝑏𝑒𝑛𝑧𝑒𝑟 𝑘𝑒𝑙𝑖𝑚𝑒 𝑠𝑎𝑦𝚤𝑠𝚤)
5 (𝑢𝑧𝑢𝑛 𝑜𝑙𝑎𝑛 𝑘𝑎𝑦𝑑𝚤𝑛 𝑘𝑒𝑙𝑖𝑚𝑒 𝑠𝑎𝑦𝚤𝑠𝚤)
= %40′𝑡𝚤𝑟.
Şeklinde olacaktır.
Bu şekilde benzerlik oranını hesaplamış bulunmaktayız.

Projemizin arayüzü bu şekildedir.
![Ekran Görüntüsü (162)](https://user-images.githubusercontent.com/100204691/208923189-9b0fcab6-fd4e-410e-821c-a79292752675.png)





