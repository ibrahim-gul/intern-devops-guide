# DevOps ve Azure DevOps Server Rehberi

## 1. Giriş ve Temel Kavramlar

### 1.1 DevOps Nedir?

DevOps, yazılım geliştirme (**Development**) ve operasyon (**Operations**) ekipleri arasındaki engelleri ortadan kaldırarak **hızlı, tutarlı ve yüksek kalitede** yazılım teslimatını amaçlayan bir kültür, metodoloji ve dizi uygulamadır. Klasik yaklaşımlarda, geliştirme ekipleri yeni özellikler eklemek için hızlı hareket ederken, operasyon ekipleri ise sistemin kararlılığını korumayı hedefler. Bu iki farklı öncelik, iletişim kopukluklarına ve uzun teslimat sürelerine neden olabilir. DevOps ise bu kopukluğun üstesinden gelmek için **sürekli entegrasyon, sürekli teslimat ve sürekli izleme** gibi prensipleri hayata geçirir.

Geleneksel “su yolu” (waterfall) veya hatta bazı “çevik” (agile) süreçlerde bile geliştirme ve operasyon ekipleri farklı zaman dilimlerinde, farklı önceliklerle çalıştıklarından yazılım döngüsünün son aşamalarında sorunlar ortaya çıkar. Örneğin, geliştiriciler kodlarını tamamlayıp testten geçirdikten sonra operasyon ekibine “şimdi yayınlayın” diyebilir; ancak operasyon ekibi, altyapı kısıtlamaları veya güvenlik politikaları nedeniyle süreçleri duraklatabilir. DevOps, bu engelleri en baştan kaldırmayı ve tüm paydaşların birlikte sorunsuz çalıştığı bir ortam oluşturmayı hedefler.

Aşağıda, DevOps’un sonsuz döngü (Infinity Loop) şeklindeki genel akışını betimleyen bir diyagram bağlantısı yer almaktadır. Bu diyagram, DevOps süreçlerinin döngüsel ve sürekli doğasını görselleştirir:

![image](https://github.com/user-attachments/assets/53d3d1ce-568c-44b4-b1bf-88a485d5abce)

Bu modelde, yazılımın yaşam döngüsü daima bir **geribildirim** (feedback) döngüsüne dayanır; kod herhangi bir aşamada geri bildirim aldığında, bir önceki adıma hızla dönülerek iyileştirme yapılabilir. “Planla, Kodla, Derle, Test Et, Yayınla, Dağıt, İşlet ve İzle” aşamaları sürekli olarak birbirini besler. Geliştiriciler yeni sürümler üzerinde çalışırken, operasyon ekipleri mevcut uygulamanın kararlı ve yüksek performansla çalışmasını sağlar. Hatalar veya değişiklik gereksinimleri ne kadar erken tespit edilirse, maliyet ve zaman kaybı o kadar düşük olur.

DevOps aynı zamanda bir **kültür** değişimidir. Ekiplerin sadece araçları değil, aynı zamanda iş birliği, iletişim, güven ve paylaşım odaklı bir zihniyeti benimsemesi gerekir. Örneğin, bir DevOps kültürüne sahip şirket, yazılımın olası arızalarını önceden tahmin etmek ve en kısa sürede çözüme kavuşturmak için tüm ekiplere izleme (monitoring) ve log bilgilerini şeffaf şekilde sunar. Bu sayede, herkes ortak hedef olan “kaliteli ve hızlı teslimat” doğrultusunda hareket eder.

Bir diğer önemli kavram ise “**Shift Left**” yaklaşımıdır. Geleneksel modellere göre, test ve güvenlik kontrolleri genellikle üretime yakın aşamalarda yapılır; bu da sorunların geç fark edilmesine yol açar. DevOps felsefesinde ise bu gibi test, güvenlik ve diğer kalite kontrolleri sürecin erken aşamalarında gerçekleştirilir (yani geliştirme tarafına doğru “kaydırılır”). Böylece, ortaya çıkabilecek sorunların erken çözümü sağlanır ve sürümün yayına hazır hale gelme süresi kısalır. Beklenmedik maliyetli hataların önüne geçmek de bu yaklaşım sayesinde kolaylaşır.

Son olarak, DevOps yalnızca bir **teknik uygulamalar seti** değildir; **ekip yapısı, organizasyonel iletişim ve sorumluluk paylaşımı** gibi insani ve kültürel unsurları da içerir. DevOps’u başarılı kılan, sadece otomasyon araçlarının doğru kullanılması değil, aynı zamanda ekiplerin vizyon, güven ve paylaşım ekseninde birleşmesidir. Bu kültür ve yöntemler benimsendiğinde, şirketler yazılım teslim sürelerini önemli ölçüde kısaltarak, yüksek kaliteli sürümleri hızlıca müşterilerine sunabilir ve bu süreçte oluşabilecek riskleri de asgariye indirebilir.

