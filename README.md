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

## 2.3 Versiyon Kontrol Sistemleri

**Versiyon Kontrol Sistemleri (VCS)**, yazılım geliştirme sürecinde kodun farklı sürümlerini kaydetmek, yönetmek ve zaman içinde izlemek için kullanılan araçlardır. Bu sistemler, geliştiricilerin üzerinde çalıştıkları kodu paylaşmalarına, yaptığı değişiklikleri takip etmelerine ve gerektiğinde önceki sürümlere dönmelerine olanak tanır. Birden çok kişinin aynı proje üzerinde çalıştığı ortamlarda, versiyon kontrol sistemleri çakışmaları (conflicts) ve hataları yönetmeyi de büyük ölçüde kolaylaştırır.

### 2.3.1 Merkezi (Centralized) ve Dağıtık (Distributed) Versiyon Kontrol Sistemleri

1. **Merkezi Versiyon Kontrol Sistemleri (Centralized VCS)**
   - Tek bir **merkezi sunucu** (repository) vardır ve tüm geliştiriciler kodu bu sunucudan çeker (checkout) veya bu sunucuya yükler (commit).
   - **Subversion (SVN)** veya **Team Foundation Version Control (TFVC)** gibi sistemler merkezi bir yapıya sahiptir.
   - **Avantajlar**:
     - Kurulum ve yönetim çoğu zaman basittir.
     - Güvenlik politikaları merkezi şekilde yönetilebilir.
   - **Dezavantajlar**:
     - Bağlantı sorunları yaşandığında geliştiriciler depo (repo) erişiminden mahrum kalır.
     - Tarihçe yönetimi ve dallanma (branch) işlemleri genellikle daha kısıtlıdır.

2. **Dağıtık Versiyon Kontrol Sistemleri (Distributed VCS)**
   - Her geliştiricinin bilgisayarında projenin tam bir kopyası (tüm geçmişiyle birlikte) bulunur.
   - **Git** ve **Mercurial** bu kategorinin en yaygın örnekleridir.
   - **Avantajlar**:
     - Çevrimdışı çalışmak mümkündür; ana sunucuya bağlanmadan da commit, branch, merge işlemleri yapılabilir.
     - Performans yükü merkezi bir noktada değil, kullanıcılar arasında dağıtılmıştır.
   - **Dezavantajlar**:
     - Öğrenme eğrisi merkezi sistemlere göre biraz daha fazla olabilir.
     - Yönetim ve güvenlik politikaları doğru kurgulanmadığında dağıtık yapı karmaşıklaşabilir.

---

### 2.3.2 Git

**Git**, günümüzde en yaygın kullanılan dağıtık versiyon kontrol sistemidir. **Linus Torvalds** tarafından Linux çekirdeği geliştirme sürecini yönetmek amacıyla oluşturulmuştur. Git’in popüler olmasının nedeni; **hızlı**, **esnek** ve **kolay dallanma/birleştirme** (branch & merge) kabiliyetidir. Ayrıca GitHub, GitLab veya Bitbucket gibi platformlar, Git tabanlı projeler için işbirliği, proje yönetimi ve sürekli entegrasyon özellikleri sunarak ekiplere kapsamlı bir ekosistem yaratır.

Git’in bazı **temel kavramları** şunlardır:

- **Commit**: Değişikliklerin fotoğrafı (snapshot) alınarak kaydedilmesi.
- **Branch**: Paralel geliştirme amacıyla kodun bağımsız bir kopyasını oluşturma.
- **Merge**: Farklı branch’lerde yapılan değişikliklerin birleştirilmesi.
- **Pull Request** veya **Merge Request**: Diğer ekip üyelerinden kod incelemesi ve onay alma.

---

### 2.3.3 Team Foundation Version Control (TFVC)

**Team Foundation Version Control (TFVC)**, Microsoft’un **Azure DevOps** ya da eski adıyla **TFS (Team Foundation Server)** platformu içerisindeki **merkezi** bir versiyon kontrol sistemidir. Aşağıdaki özelliklerle öne çıkar:

- **Merkezi Depo**: Tüm kod, tek bir sunucu veya koleksiyon içinde saklanır. Geliştiriciler dosyaları “check out” ve “check in” konseptleriyle yönetir.
- **Büyük Kod Tabanları**: Özellikle kurumsal ortamlarda kullanılan devasa kod tabanlarını yönetmek için tasarlanmıştır.
- **Sürüm Yönetimi**: Check-in işlemlerinde “şelale” (waterfall) tarzı projelerde daha alışılmış bir mantıkla çalışır.
- **Bağlı Çalışma**: Çoğu işlem, sunucuyla etkileşim halinde yapılır (örneğin, kodu check out etmeden düzenleyememe gibi).

**TFVC**, merkezi yapı isteyen ya da kurumsal standartları doğrultusunda TFS/Azure DevOps Server’ın daha eski sürümlerini kullanan şirketlerde hâlâ tercih edilir. Ancak Microsoft, son yıllarda **Azure Repos** içerisindeki **Git** desteğini ön plana çıkarmış ve geliştiricilerin dağıtık VCS yaklaşımına geçişini desteklemiştir. Yeni projelerde Microsoft da Git kullanımını tavsiye etmektedir.

---

### 2.3.4 Versiyon Kontrol Sistemi Seçimi ve Öneriler

- **Kurum Kültürü ve Proje Boyutu**: Çok büyük, monolitik projeler veya eski kurumsal standartlar için TFVC veya SVN gibi merkezi sistemler halen tercih edilebilir. Modern ve çevik takımlar ise genellikle **Git**’in esnekliğinden yararlanır.
- **İş Akışı (Workflow)**: GitFlow, GitHub Flow veya Trunk-based development gibi stratejiler Git ekosistemiyle yaygındır. TFVC’de de dallanma ve birleştirme (branch/merge) yapılabilir ancak Git kadar esnek değildir.
- **Araç Desteği ve Ekosistem**: Git, GitHub/GitLab gibi platformlarla entegre çalışarak proje yönetimi, CI/CD, kod inceleme ve issue tracking gibi ihtiyaçlara bütüncül çözümler sunar. TFVC ise Azure Boards ve Pipelines ile entegredir.
- **Öğrenme Eğrisi**: Git komutları ve dallanma stratejileri ilk etapta karmaşık gelse de, geniş dokümantasyon ve topluluk desteği öğrenmeyi kolaylaştırır.

İster merkezi ister dağıtık bir yapı benimsensin, en önemli nokta **dallanma stratejilerinin net olması**, **kod inceleme** (code review) süreçlerinin düzenli yapılması ve **tüm ekibin versiyon kontrol kavramlarını benimsemesidir. Bu sayede, proje büyüse bile kod yönetimi düzenli ve sürdürülebilir kalır.

## 2.4 Infrastructure as Code (IaC)

**Infrastructure as Code (IaC)**, geleneksel yöntemlerde manuel adımlar veya grafik arayüzler üzerinden yapılan altyapı yapılandırma işlemlerini, **kod** (konfigürasyon dosyaları, betikler vb.) aracılığıyla tanımlama ve yönetme pratiğidir. Bu yaklaşımla, sunucuların kurulumu, ağ bileşenlerinin ayarlanması, veritabanı ve uygulama hizmetlerinin konfigürasyonu gibi altyapıya dair tüm adımlar **tekrar edilebilir**, **versiyonlanabilir** ve **otomasyon** dostu hale getirilir.

### 2.4.1 Neden IaC?

1. **Tekrarlanabilirlik ve Tutarlılık**  
   - Aynı altyapıyı tekrar tekrar oluşturmak istediğinizde, manuel işlem hatalarını ortadan kaldırarak **standart** ve **tutarlı** kurulumlar sağlanır.  
   - Farklı ortamlar (test, staging, prod) arasında oluşabilecek sürüm veya konfigürasyon uyuşmazlıkları azalır.

2. **Versiyon Kontrolü**  
   - Altyapı tanımları (kod dosyaları) bir versiyon kontrol sistemi (Git, TFVC vb.) içerisinde saklanabilir.  
   - Bu sayede, **hangi değişikliğin ne zaman, kim tarafından ve neden yapıldığı** net bir şekilde takip edilebilir.

3. **Sürekli Teslimat/Dağıtım (CI/CD) ile Entegrasyon**  
   - Altyapı kodunun da uygulama kodu gibi otomatik pipeline’lar içerisinde test edilmesi ve uygulanması mümkündür.  
   - Gerektiğinde hızlı bir şekilde yeni sunucular veya hizmetler devreye alınıp güncellenebilir.

---

### 2.4.2 Popüler IaC Araçları

- **Terraform**  
  - HashiCorp tarafından geliştirilen, **çoklu bulut** (AWS, Azure, GCP vb.) desteği olan ve **deklaratif** yaklaşımla altyapıyı tanımlayan bir araçtır.  
  - “.tf” uzantılı dosyalarla altyapı bileşenleri ve bağımlılıklar tariflenir; `terraform plan` ve `terraform apply` komutlarıyla değişiklik uygulanır.

- **Ansible**  
  - Red Hat tarafından geliştirilen, **agentless** (ajan gerektirmeyen) bir konfigürasyon yönetimi ve orkestrasyon aracıdır.  
  - YAML tabanlı **playbook** dosyalarıyla sunucuların yapılandırılması, paket kurulumu, servis konfigürasyonu gibi işlemler yapılır.

- **AWS CloudFormation**  
  - AWS özelinde çalışan bir IaC aracıdır. Yine **deklaratif** bir yaklaşımla JSON veya YAML formatında şablonlar oluşturularak, AWS kaynaklarının yönetimi otomatikleştirilir.

- **Azure Resource Manager (ARM) / Bicep**  
  - Microsoft Azure’un IaC çözümüdür. ARM şablonları JSON formatında yazılır.  
  - Yakın dönemde Bicep adı verilen, daha basit bir sözdizimi sunan dil ile ARM şablonlarına benzer işlevsellik elde edilebilir.

- **Puppet** ve **Chef**  
  - Daha geleneksel konfigürasyon yönetimi araçları olarak bilinen Puppet ve Chef, sunucuların sürekli olarak belirli bir durumda (state) kalmasını sağlar.

---

### 2.4.3 IaC Uygulama Yaklaşımları

1. **Deklaratif (Declarative)**  
   - “Ne” yapılması gerektiğini tanımlarsınız; araç “nasıl” yapılacağını kendisi belirler.  
   - Terraform, CloudFormation, ARM gibi araçlar bu yaklaşımı benimser.

2. **Emredici (Imperative)**  
   - Altyapının nasıl inşa edileceği adım adım tarif edilir.  
   - Ansible playbook’ları veya klasik betik (script) yöntemleri emredici tarza örnek gösterilebilir.

3. **Konfigürasyon Yönetimi**  
   - Ansible, Puppet, Chef gibi araçlar, sunucuların istenen konfigurasyonda kalmasını sağlar ve sapmalar (drift) oluştuğunda tekrar ayarlar.

---

### 2.4.4 IaC’nin Faydaları ve Karşılaşılan Zorluklar

#### Faydaları

- **Hızlı ve Otomatik Kurulum**: Yeni bir ortam kurmak, sadece birkaç komut veya pipeline tetiklemesiyle mümkün hale gelir.  
- **Risk Azaltma**: Elle yapılan yapılandırma hataları minimize edilir, hatalı adımlar süratle geri alınabilir.  
- **Ölçeklenebilirlik**: Dinamik bulut ortamlarında yatay/dikey ölçekleme işlemleri kodla yönetilerek, binlerce kaynağı yönetmek bile kolaylaşır.  
- **Maliyet Optimizasyonu**: Gereksiz kaynak kullanımı tespit edilip devre dışı bırakılabilir, altyapı kullanım raporları versiyon kontrol sisteminden izlenebilir.

#### Zorluklar

- **Öğrenme Eğrisi**: Terraform, Ansible veya CloudFormation gibi araçlar için zaman, eğitim ve deneyim gereklidir.  
- **Takımın Adaptasyonu**: Ekip, “altyapı yönetimi” zihniyetini manuel yöntemlerden kod tabanlı yaklaşıma dönüştürmekte zorlanabilir.  
- **İyileştirme Döngüsü**: Ufak bir değişikliğin bile öncelikle versiyon kontrol sistemine işlenmesi ve pipeline’ın çalıştırılması gerekebilir. Hız kazanmak için süreçlerin iyi planlanması şarttır.  
- **Güvenlik ve Erişim**: Altyapı kodu kritiktir; yanlış erişim yetkileri veya yanlış şifre yönetimi ciddi güvenlik sorunlarına yol açabilir.

---

### 2.4.5 IaC ve DevOps Entegrasyonu

- **CI/CD Pipeline**  
  - Kod (uygulama) ve altyapı değişiklikleri aynı veya ayrı pipeline’lar üzerinden otomasyonla uygulanabilir.  
  - Örnek: Terraform plan/apply aşamalarını, uygulama build & deploy aşamalarının sonuna eklemek.

- **Sürekli İzleme (Monitoring)**  
  - IaC ile kurulan altyapıya, otomatik izleme araçları (Prometheus, Grafana, Azure Monitor, AWS CloudWatch vb.) da entegre edilebilir.  
  - Her yeni oluşturulan kaynağa izleme agent’larının otomatik kurulması bir IaC betiğiyle sağlanabilir.

- **Mikroservis & Konteyner Dünyası**  
  - Kubernetes gibi platformlarda, pod’lar, servisler, ingress konfigürasyonları YAML dosyalarıyla yönetildiği için aslında bir IaC yaklaşımı olarak görülebilir.  
  - DevOps ile el ele çalışan takımlar, Kubernetes manifestleri veya Helm chart’larıyla altyapı düzenlemelerini kod halinde saklar.

---

IaC, modern DevOps uygulamalarının **temel taşlarından** biridir. Uygulama kodunuza gösterdiğiniz özeni altyapınıza da göstererek, **tutarlı**, **izlenebilir** ve **yeniden üretilebilir** bir yapı oluşturabilirsiniz. Bu yaklaşım hem ekip verimliliğini hem de sistem güvenilirliğini artırır, ayrıca hızlı yeniliğe ve değişime daha kolay uyum sağlanmasına olanak tanır.

## 2.5 Monitoring ve Logging

**Monitoring (İzleme)** ve **Logging (Günlük Kayıtları Tutma)**, DevOps kültürünün temel bileşenlerindendir. Bu iki uygulama sayesinde, geliştirme ve operasyon ekipleri uygulamaların ve altyapının **performansını**, **sağlık durumunu** ve **hata** davranışlarını gerçek zamanlı veya geçmişe dönük olarak analiz edebilir. Sorunları erken tespit etmek ve çözmek için hayati önem taşırlar.

---

### 2.5.1 Monitoring (İzleme)

#### 1. Temel Kavramlar
- **Metrik (Metrics)**: CPU kullanımı, bellek kullanımı, yanıt süreleri, istek/saniye gibi niceliksel veriler.  
- **Alarmlar (Alerts)**: Ölçülen metrikler belirli eşikleri aştığında ya da belirli koşullar sağlandığında ekibe bildirim gönderen uyarılar.  
- **Dashboard / Panel**: Canlı veya tarihsel metriklerin görselleştirildiği, ekiplerin sistemi anlık olarak takip edebileceği bir arayüz.

#### 2. Monitoring Araçları
- **Prometheus** + **Grafana**:  
  - Prometheus, metrikleri toplayıp saklayan bir zaman serisi veritabanı sunar.  
  - Grafana, Prometheus’tan aldığı verileri pano (dashboard) olarak görselleştirir.  
- **Azure Monitor** / **Application Insights**:  
  - Microsoft Azure’un bulut tabanlı izleme platformu.  
  - Uygulamalardan gelen performans verilerini, hata kayıtlarını ve kullanıcı izlerini (telemetry) görselleştirme imkânı sunar.  
- **AWS CloudWatch**:  
  - AWS ortamındaki kaynakları izleyerek metrik ve log toplar, alarmlar oluşturur.  
- **Elastic Stack (ELK)**:  
  - Elasticsearch, Logstash, Kibana üçlüsüyle log analizi ve metrik yönetimi yapılabilir (ayrıca Beats ile de veri toplanabilir).

#### 3. Monitoring Stratejileri
- **Proaktif İzleme**: Sorun henüz büyük bir krize dönüşmeden tespit etmek için belirli eşiğe dayalı alarmlar kurmak (örneğin CPU %80’i aştığında bildirim).  
- **Real-time ve Tarihsel Analiz**: Hem gerçek zamanda uyarı alabilmek hem de tarihsel verilere bakarak trendler ve kök neden analizi (root cause analysis) yapmak.  
- **Distributed Tracing**: Mikroservis mimarilerinde, bir kullanıcı isteğinin sistem içinde izlediği yolu adım adım takip etmek (örn. Jaeger, Zipkin).

---

### 2.5.2 Logging (Günlük Kayıtları)

#### 1. Temel Kavramlar
- **Log Mesajı**: Uygulama veya sistem bileşenlerinin çalışma esnasında ürettiği metin tabanlı kayıtlar (ör. “INFO”, “WARN”, “ERROR”).  
- **Log Seviyeleri (Log Levels)**: Genellikle “Trace”, “Debug”, “Info”, “Warn”, “Error”, “Fatal” gibi seviyeler kullanılır.  
- **Log Formatı**: Logs genellikle metin dosyaları veya JSON formatında tutulur. JSON formatı, makine tarafından işlenmesi daha kolay olması sebebiyle sıkça tercih edilir.

#### 2. Log Yönetimi Araçları
- **Elasticsearch, Logstash, Kibana (ELK)**:  
  - **Logstash** ile çok sayıda kaynaktan toplanan loglar filtrelenir ve **Elasticsearch** veritabanına aktarılır.  
  - **Kibana** ile loglar görselleştirilebilir ve analiz edilebilir.  
- **Fluentd / Fluent Bit**:  
  - Hafif ve yüksek performanslı log toplama araçlarıdır.  
  - Genellikle konteyner ekosistemlerinde (Docker, Kubernetes) yaygınlaşmıştır.  
- **Splunk**:  
  - Kurumsal düzeyde log yönetimi ve analiz platformu.  
  - Büyük veri setlerinde arama ve korelasyon yetenekleri oldukça güçlüdür.

#### 3. Logging Stratejileri
- **Merkezi (Centralized) Log Yönetimi**: Tüm uygulama ve sunucuların loglarını tek bir merkezde toplamak, analiz etmek ve uzun süre saklamak.  
- **Log Standardizasyonu**: Tüm hizmetlerde tutarlı log formatı, alan isimlendirmesi (JSON) ve timestamp düzeni kullanmak, aramayı ve analizi kolaylaştırır.  
- **Arşivleme ve Rotasyon**: Log dosyalarının büyümesi, disk alanı sorunlarına yol açabilir. Rotasyon planı ve arşivleme stratejisi belirlemek gerekir.  
- **Güvenlik ve Erişim Kontrolü**: Loglarda gizli bilgiler (şifre, kredi kartı numarası vb.) depolanmaması veya maskeleme (masking) yapılması önemlidir.

---

### 2.5.3 Monitoring ve Logging Entegrasyonu

- **Kök Neden Analizi (Root Cause Analysis)**  
  - Izleme panolarında anormallik tespit edildiğinde, log kayıtlarının detayları incelenerek sorunun kaynağına hızla ulaşılabilir.  
- **Otomatik Bildirim ve Olay Yönetimi**  
  - Metrik veya log seviyesi uyarı kriterleri karşılandığında, Slack, e-posta, SMS veya diğer kanallarla olay yönetimi (incident management) başlatılabilir.  
- **Performans ve Kullanıcı Deneyimi**  
  - Uygulama performansıyla ilgili metrikler (işlem süresi, yanıt süresi, throughput) ve log incelemeleriyle kullanıcı deneyimini gerçek zamanlı iyileştirmek mümkündür.  
- **Sürekli İyileştirme (Continuous Improvement)**  
  - Monitoring ve logging verileri, sistemde tekrarlayan sorunları veya darboğazları (bottleneck) tespit etmeyi kolaylaştırır.  
  - Elde edilen bulgular yeni sprint veya geliştirme döngülerine yansıtılarak kalite artışı sağlanır.

---

### 2.5.4 Önerilen En İyi Uygulamalar

1. **Log ve Metrik Ayrımı**  
   - Uygulama loglarının yanı sıra sistem metriklerini ve olayları da (events) ayrı olarak toplayıp ilişkilendirin.  
2. **Her Şeyi Merkeze Toplayın**  
   - Dağınık log dosyaları veya metrik kaynakları sorun tespitini zorlaştırır; merkezi bir log ve izleme çözümü kullanın.  
3. **Log Formatını Standardize Edin**  
   - İster JSON ister metin (plain text) tercih edin, tüm servislerin benzer bir yapıda log üretmesi sorgulamayı hızlandırır.  
4. **Doğru Alarm Eşikleri Tanımlayın**  
   - Çok fazla alarm “alarm yorgunluğuna” yol açabilir. İyi tasarlanmış alarmlar kritik hataları ve performans anormalliklerini doğru şekilde yansıtır.  
5. **Gerçek Zamanlı ve Geçmişe Dönük Analiz**  
   - Anlık gözlem kadar tarihsel trend analizi de önemlidir. Hangi metriklerin uzun vadede nasıl değiştiğini izlemek, kapasite planlamasına yardımcı olur.

---

Monitoring ve Logging, DevOps’un “**kullandığın şeyi izle**” ve “**hatalardan ders al**” prensiplerini hayata geçiren temel yöntemlerdir. Sağlam bir izleme ve log yönetimi altyapısı, sorunların erken tespitini ve hızlı çözümünü sağlayarak hem geliştirme hem de operasyon ekiplerinin verimliliğini artırır, kesintileri ve müşteri memnuniyetsizliğini azaltır.

