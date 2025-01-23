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

### 1.2 DevOps’un Tarihçesi
DevOps kavramının ortaya çıkışını daha iyi anlamak için, yazılım geliştirme ve operasyon dünyasında yaşanan dönüşümleri incelemek gerekir. 2000’li yılların başlarında, yazılım geliştirme süreçleri genellikle Waterfall veya “aşamalı teslim” yaklaşımlarıyla yürütülüyordu. Bu modellerde, analiz, tasarım, geliştirme, test ve dağıtım gibi aşamalar net sınırlarla birbirinden ayrılmıştı. Ancak internet kullanımının ve çevrimiçi servislerin hızla yaygınlaşmasıyla, şirketlerin yazılım dağıtım döngülerini kısaltmak ve daha hızlı yenilik sunmak ihtiyacı artmaya başladı.

DevOps’un temelleri, Agile felsefesinin yaygınlaşması ve Continuous Integration (CI) fikirlerinin filizlenmesiyle atıldı. Agile yöntemler, yazılım geliştirme ekiplerinin iteratif ve daha küçük parçalar halinde ürün geliştirmesine olanak sağladı. Ancak operasyon ekipleri hâlâ klasik yöntemlerle çalıştığında, geliştiricilerin yeni sürümleri hızlıca yayınlama isteği ile operasyonun kararlılık önceliği çatışmaya devam ediyordu. Bu noktada, 2000’li yılların ortalarında Continuous Delivery (CD) ve Continuous Deployment kavramları da konuşulmaya başlanarak, operasyon ekiplerinin de çevik yaklaşıma dahil edilmesi gerektiği fikri güçlendi.

DevOps teriminin doğuşu genellikle 2009 yılında düzenlenen bir konferansta (O’Reilly Velocity Conference) John Allspaw ve Paul Hammond tarafından yapılan “10 deploys per day” adlı sunuma dayanır. Bu sunum, Flickr platformunun günde on defa canlı ortama sürüm çıkabilmesini anlatıyor ve hem geliştirici hem de operasyon ekiplerinin aynı hedefe odaklanması gerektiğini vurguluyordu. Aynı yıl, Patrick Debois öncülüğünde Belçika’da ilk “DevOpsDays” etkinliği düzenlendi. Bu etkinlik, geliştirici ve operasyon topluluklarını bir araya getirerek DevOps kavramının hızla yayılmasına zemin hazırladı.

2010’lu yıllarda, büyük teknoloji şirketlerinin (Google, Amazon, Netflix vb.) kapsamlı otomasyon, bulut bilişim ve mikro servis yaklaşımlarıyla DevOps’u daha da ileri taşıması, konseptin dünyaya yayılmasında önemli rol oynadı. Geleneksel veri merkezlerinden bulut tabanlı (Cloud-native) ortamlara geçiş, DevOps’un sunduğu hızlı, sürekli ve otomasyon odaklı yaklaşımla mükemmel şekilde uyuşuyordu. Daha sonra Docker ve Kubernetes gibi container ve orkestrasyon teknolojilerinin yükselişi de DevOps hareketini iyice hızlandırdı. Bu araçlar, yazılım paketleme ve dağıtım işlerini kolaylaştırarak geliştirici ve operasyon ekiplerine büyük avantajlar sağladı.

Bugün DevOps, sadece bir araç seti veya teknik uygulama değil, aynı zamanda bir kültür olarak kabul ediliyor. Şirketlerin büyüklüğü veya sektöründen bağımsız olarak, DevOps yaklaşımı benimsenerek yazılımın tasarımdan canlı ortama kadar olan tüm aşamalarında iş birliği, otomasyon, hızlı geribildirim ve sürekli iyileştirme esas alınır. Bu evrim, “silo” mantığının yıkılması ve “ortak sorumluluk” anlayışının yerleşmesiyle mümkün olmuştur. DevOps’un tarihçesi, bu zihniyet dönüşümünün, teknolojik gelişmelerin ve rekabetin sürekli olarak organizasyonları daha hızlı ve çevik olmaya itmesinin bir yansıması olarak görülebilir.

### 1.3 DevOps Kültürü ve Takım İçi İletişim
DevOps’un yalnızca bir teknik yaklaşım değil aynı zamanda bir kültür olduğu sıklıkla vurgulanır. Bu kültür, geleneksel yazılım geliştirme ve operasyon ekiplerinin ayrı silolar halinde çalışmasından kaynaklanan iletişim ve iş birliği eksikliğini ortadan kaldırmayı amaçlar. DevOps kültüründe esas olan, paylaşım, açıklık ve sürekli geri bildirim anlayışıdır. Ekip üyeleri, proje sürecinin herhangi bir aşamasında yaşanan sorun veya ihtiyaç duyulan iyileştirmeler hakkında rahatça birbirleriyle iletişime geçer ve sorumlulukları ortaklaşa üstlenir.

DevOps kültürünün başarılı olabilmesi için, ekip içerisinde güven ve ortak hedef bilinci oluşturmak son derece önemlidir. Örneğin, geliştiriciler (Development) yeni özellikleri mümkün olduğunca hızlı teslim etmeye odaklanırken; operasyon ekibi (Operations) sistemin stabil, güvenli ve ölçeklenebilir olmasını sağlamaya çalışır. Geleneksel yaklaşımlarda, bu iki öncelik zaman zaman çelişebilir ve “sizin işiniz / bizim işimiz” ayrımına neden olur. DevOps kültüründe ise bu ayrımlar yıkılır; ekipler, yazılımın baştan sona tüm yaşam döngüsünden ortak sorumluluk duyar. Bu sayede “hatayı kim yaptı” yerine “nasıl çözeriz ve iyileştiririz” sorusu öne çıkar.

Takım içi iletişimi güçlendirmek adına, günlük stand-up toplantıları veya kısa geri bildirim döngüleri benimsenir. Ekip üyeleri, üzerinde çalıştıkları iş maddeleri, yaşadıkları engeller ve sonraki adımlar hakkında hızlı ve düzenli bilgi paylaşımında bulunur. Ayrıca, kod incelemeleri (code review), pull request süreçleri ve pair programming gibi uygulamalar da iletişimi artıran yöntemlerdir. Bu yöntemler sayesinde hem geliştiriciler birbirlerinden öğrenir hem de operasyon ekibi, geliştiricilerin hangi teknolojiler ve düzenlemeler üzerinde çalıştığını erken aşamada görüp buna göre önlemler veya iyileştirmeler planlayabilir.

Son olarak, DevOps kültürü organizasyon genelinde “açık kapı” (open door) bir yaklaşıma dayanır: Şeffaf araçlar, paylaşılan panolar (dashboard), merkezi log ve izleme (monitoring) sistemleri herkesin erişimine açıktır. Örneğin, bir hata ya da performans sorunu olduğunda, hem geliştiriciler hem de operasyon ekibi aynı log ekranlarını veya metrikleri inceleyerek sorunun kök nedenine hızla ulaşır. Bu şeffaflık, kurum içinde “biz ve onlar” yerine “hep birlikte” çalışma zihniyetini kuvvetlendirir. Bu şekilde, DevOps yalnızca bir “entegrasyon” veya “otomasyon” çabasından öte, tüm ekibin ortak sorumluluğu paylaştığı bir iş birliği modeline dönüşür.

### 1.4 DevOps’un Organizasyonel Faydaları
DevOps, bir yazılım geliştirme yöntemi olmasının ötesinde, organizasyonun tamamını etkileyen bir dönüşüm sunar. Doğru uygulandığında, sadece geliştirme ve operasyon ekipleri arasındaki iş birliğini artırmakla kalmaz, aynı zamanda iş süreçlerinden stratejik karar mekanizmalarına kadar pek çok alanı iyileştirir. Bu iyileştirmeler, kuruluşların yenilikçi olmak, pazara hızlı çıkmak ve müşteri memnuniyetini yüksek tutmak gibi hedeflerine ulaşmalarını kolaylaştırır.

İlk önemli fayda, daha hızlı teslimat ve kısa sürüm döngüleri elde etmektir. Geleneksel modellere kıyasla DevOps, otomasyon ve sürekli entegrasyon/delivery (CI/CD) prensiplerini benimseyerek kodun geliştirme, test ve dağıtım aşamalarında önemli zaman tasarrufu sağlar. Böylece işletmeler, yeni özelliklerini veya yamalarını daha hızlı biçimde canlı ortama çıkarabilir. Bu hız, aynı zamanda rakiplerin geride bırakılmasını ve sürekli olarak değer üretilmesini destekler.

İkinci olarak, DevOps’un getirdiği kalite artışı ve hata maliyetlerinin azalması, organizasyonun işleyişinde büyük rol oynar. Çevik (agile) ve sürekli test prensipleriyle bütünleşen DevOps kültürü, hataların erken aşamada tespit edilmesini sağlar. Otomatik testler, kod incelemeleri ve izleme araçları, hataların üretim ortamına ulaşmadan giderilmesine imkân tanır. Bu da müşteri memnuniyetini yükseltir ve arıza giderme maliyetlerini ciddi ölçüde azaltır.

Üçüncü bir fayda, ekipler arası iletişim ve iş birliği konusundaki gelişimdir. DevOps yaklaşımı sayesinde silolar yıkılarak geliştirme, test, operasyon ve güvenlik ekipleri aynı hedef etrafında birleşir. Ortak sorumluluk duygusu ve şeffaf bir çalışma ortamı, kurum içinde güveni artırır. Bu da daha sağlıklı, yenilikçi ve sürdürülebilir bir kurumsal kültürün oluşmasını destekler. İletişim aksaklıklarından kaynaklanan gecikmeler veya hatalar en aza iner.

Dördüncü olarak, DevOps’un maliyet avantajları da gözden kaçmamalıdır. Hızlı sürüm döngüleri ve otomasyon, tekrarlayan manuel işlemlerden doğan iş gücü ve zaman kaybını ortadan kaldırır. Böylece, insan kaynağı daha katma değerli işlere odaklanabilir. Ayrıca hataların üretimde ortaya çıkması durumunda ödenecek “hata bedeli” (rework, müşteri kaybı, itibar zararı vb.) önemli ölçüde düşer. Dolayısıyla DevOps, orta ve uzun vadede kuruma finansal fayda da sağlar.

Son olarak, DevOps’un müşteri odaklı doğası, organizasyonun rekabet gücünü artırır. Müşteri geri bildirimlerinin hızlıca alınması ve yeni özelliklerin veya düzeltmelerin süratle devreye alınması, işletmenin pazar dinamiklerine daha çevik tepki vermesini sağlar. Böylece müşteri beklentilerine en hızlı uyum sağlayan ve onları memnun etmeye devam eden şirketler, piyasa liderliği yolunda önemli bir avantaj elde ederler.

DevOps, bütün bu faydalarıyla birlikte bir şirketin sadece teknoloji ekibine değil, kurumsal stratejilerine de dokunan bir dönüşüm yaklaşımıdır. Şirketin hız, kalite, iletişim ve verimlilik eksenlerinde ilerlemesini desteklerken, aynı zamanda inovasyon ve müşteri memnuniyeti gibi kritik hedeflere de doğrudan katkı sunar. Bu yüzden, DevOps uygulamaları büyük veya küçük fark etmeksizin birçok organizasyon için stratejik bir gereklilik haline gelmiştir.

# 2. DevOps Temel Prensipleri

## 2.1 Continuous Integration (CI)
Continuous Integration (CI), yazılım geliştirme sürecinde geliştiricilerin yaptığı her kod değişikliğini sık sık (gün içinde birden fazla kez) ortak kod deposuna (repo) entegre etmesi ve bu değişikliğin otomatik olarak derlenip test edilmesi pratiğidir. Ana hedefi, kod birleşiminden kaynaklanan hataları erken aşamada tespit etmek ve ekibe hızlı geribildirim sağlayarak geliştirme sürecini akıcı ve hatasız hale getirmektir.

Aşağıdaki adımlar, tipik bir CI sürecini özetler:

1. Geliştirici Kodu Yazıp Versiyon Kontrolüne Gönderir (Commit & Push)
  * Geliştirici, lokal ortamında yaptığı değişiklikleri (kod, konfigürasyon, vb.) versiyon kontrol sistemine (Git, SVN vb.) aktarır.
  * CI anlayışında, bu işlemin küçük ve sık commit’lerle yapılması önerilir.

2. Otomatik Build (Derleme) Süreci Tetiklenir
  * Versiyon kontrol deposuna kod gönderildiği anda, CI sunucusu (örneğin Azure DevOps, Jenkins, GitLab CI vb.) bir “build” işi başlatır.
  * Bu aşamada kod, projenin gerektirdiği derleme süreci (örneğin .NET, Java, Node.js vb.) üzerinden geçer.

3. Otomatik Testler Çalışır
  * Derleme başarılı olursa, unit test, integration test gibi test setleri otomatik olarak devreye girer.
  * Test süreci de tam otomasyonla yürütüldüğü için, ekibe gecikme olmadan anlık geribildirim verilir.

4. Sonuç ve Raporlama
  * Build veya test aşamalarından herhangi birinde hata oluşursa, CI aracı bunu ekibe bildirim (e-posta, Slack, Teams vb.) yoluyla duyurur.
  * Hatalar, detaylı loglar ve raporlarla birlikte paylaşılır, böylece geliştiriciler hızlıca müdahale edebilir.

5. Sürekli ve Küçük Adımlarla Entegrasyon
  * CI felsefesinde, tüm ekip üyeleri kodu sık sık tek bir ana dal (main/trunk) üzerinde birleştirdiği için büyük çaplı çakışmalar (merge conflict) minimuma iner.
  * Kodu küçük parçalara bölerek ve her parçayı test ederek ilerlemek, hata çözme maliyetini önemli ölçüde azaltır.

**CI’nin Önemli Noktaları**
  * Erken Uyarı Sistemi: Geliştiriciler kodun bozulduğunu (örneğin, bir testin başarısız olduğunu) çok kısa sürede öğrenir.
  * Daha Kısa Sürüm Döngüleri: Sürekli test edilmiş ve entegre edilmiş kod, dağıtıma (release) daha hazır hale gelir.
  * Ekip İşbirliği: Ortak bir kod deposu ve sürekli otomasyon, geliştiriciler arasındaki iş birliğini ve kod kalitesini artırır.
  * Kod Kalitesi ve Standartlar: CI sürecinde kod analiz araçları, statik kod analizleri (örneğin SonarQube) de entegre edilerek standartlar korunabilir.

Bu sayede, Continuous Integration uygulayan ekipler yazılım geliştirme hızlarını artırırken kaliteden ödün vermez ve uzun vadede teknik borcun (technical debt) büyümesini engeller. Özellikle Continuous Delivery (CD) ve Continuous Deployment süreçlerinin temeli de CI ile atılır; çünkü düzenli olarak entegre ve test edilen kod, sonraki dağıtım aşamalarına güvenle ilerleyebilir.

## 2.2 Continuous Delivery (CD) & Continuous Deployment
Continuous Delivery (CD) ve Continuous Deployment, Continuous Integration (CI) sürecinin bir sonraki aşamaları olarak görülebilir. Her iki yaklaşım da kodun, üretim veya son kullanıcının erişimine açık ortama (production) sürekli ve güvenle taşınmasını amaçlar. Ancak aralarında önemli bir fark bulunur:

1. Continuous Delivery (CD):
  * Kodun her zaman canlı ortama (production) çıkmaya hazır halde olmasını hedefler.
  * Yeni bir sürümü manuel onay veya belirli süreçlerden (örneğin QA aşaması, güvenlik testleri, kullanıcı kabul testleri) geçirdikten sonra üretime alır.
  * Ekipler, her an “Deploy” düğmesine basarak veya kısa bir onay akışıyla birlikte yeni sürümü yayına alabilecek güvene sahip olur.

2. Continuous Deployment:
  * Burada, başarılı bir build ve test aşamasından geçen her sürüm otomatik olarak canlı ortama aktarılır.
  * Üretime geçiş için manuel onay gerekmez; süreç tamamen otomatiktir.
  * Bu yaklaşım, yüksek düzeyde otomasyon, izleme (monitoring), hata yönetimi ve geri dönüş (rollback) mekanizmaları gerektirir.

**Continuous Delivery (CD) Süreci Nasıl İşler?**

1. CI Süreciyle Entegre
  * CD, başarılı tamamlanmış bir CI sürecinin çıktısını alarak başlar. Build ve test aşamalarını sorunsuz geçen paket veya imaj, CD aşamasında kullanılmaya hazırdır.

2. Paketleme ve Ortam Hazırlığı
  * Uygulama, dağıtıma uygun bir formata (örneğin Docker imajı, zip paketi, NuGet paketi, npm paketi vb.) getirilir.
  * CD pipeline’ı, uygulamayı test, staging veya canary gibi farklı ortamlara dağıtmak üzere konfigüre edilir.

3. Ek Testler ve Onay Mekanizmaları
  * CD aşamasında, integration test, yük ve performans testleri, güvenlik taramaları veya kullanıcı kabul testleri (UAT) yapılabilir.
  * Kurumun politikalarına göre bu aşamada bir manuel onay (approval) adımı eklenebilir. Bu, ekiplere canlı ortama geçmeden önce ek doğrulama imkanı sağlar.

4. Üretim (Production) Dağıtımı
  * Gerekli onaylar verildikten sonra, pipeline uygulamayı üretim ortamına yayına alır (deploy).
  * Deployment sonrası bir doğrulama aşamasıyla birlikte, uygulamanın sorunsuz çalıştığı onaylanır.

**Continuous Deployment Süreciyle Farklar**

1. Manuel Onay Yok
  * Continuous Deployment’da, başarıyla testi geçen her sürüm canlıya otomatik olarak çıkar.
  * Büyük ölçekli, yüksek hacimli uygulamalarda (örneğin e-ticaret siteleri, SaaS platformları) sıklıkla uygulanır.

2. Otomatik Rollback
  * Çok hızlı sürüm çıkıldığından, uygulamada oluşabilecek sorunlara karşı otomatik geri dönüş (rollback) ve ileri seviye izleme sistemleri bulunmalıdır.

3. Hız ve Sürekli Güncelleme
  * Her değişiklik anında son kullanıcılara ulaşabilir. Bu durum, rekabetçi ortamlarda büyük avantaj sağlarken, aynı zamanda yönetim ve kontrol mekanizmalarını daha karmaşık hale getirir.

**CD ve Kurumsal Düzeyde Katma Değer**
  * Daha Kısa “Lead Time”: Kod yazıldığı andan canlı ortama geçene kadar geçen süre minimum düzeye iner.
  * Düşük Risk: Her sürüm, küçük ve test edilmiş parçalardan oluştuğu için hata riski azalır.
  * Sürekli Gelişim: Hızlı geribildirim döngüleri, müşteri ihtiyaçlarına anında yanıt verme olanağı sunar.
  * İş Birliği: Geliştirme, test ve operasyon ekipleri aynı pipeline üzerinden sorumluluk paylaşır, bu da iletişimi ve iş birliğini güçlendirir.

Continuous Delivery ve Continuous Deployment prensiplerini doğru şekilde kurgulayan organizasyonlar, yenilik ve kalite açısından rakiplerinden önde olmanın yanı sıra, beklenmeyen hatalara daha hızlı tepki verme ve bunları en az maliyetle çözme yeteneğini de kazanmış olurlar.
