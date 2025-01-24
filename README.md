# DevOps Rehberi

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

## 2.6 DevOps Araç Ekosistemi

DevOps kültürü, yalnızca bir metodoloji ya da organizasyon yapısı değil, aynı zamanda **geniş bir araç ekosistemini** de kapsar. Bu araçlar, yazılımın planlama aşamasından, geliştirme, test, dağıtım ve izleme süreçlerine kadar pek çok adımda ekiplerin işini kolaylaştırır. Doğru araç seçimi, verimliliği artırırken, hataları ve gecikmeleri azaltır.

---

### 2.6.1 Sürekli Entegrasyon ve Teslim (CI/CD) Araçları

- **Jenkins**  
  - Açık kaynak, Java tabanlı popüler bir CI/CD sunucusudur.  
  - Büyük bir eklenti (plugin) ekosistemine sahiptir ve hemen her programlama diline entegre olabilir.

- **GitLab CI/CD**  
  - GitLab’ın entegre CI/CD özelliği; Git deposuyla sıkı entegrasyona sahiptir.  
  - Pipeline konfigürasyonu `.gitlab-ci.yml` dosyasıyla yapılır.

- **GitHub Actions**  
  - GitHub platformu üzerinde çalışan, YAML tabanlı bir CI/CD altyapısıdır.  
  - Geniş bir “action marketplace” sunarak farklı otomasyon senaryolarına olanak tanır.

- **Azure Pipelines**  
  - Azure DevOps ekosisteminin bir parçası olarak hem bulutta (Azure DevOps Services) hem de şirket içi (Azure DevOps Server) kullanılabilir.  
  - .NET, Java, Node.js gibi birçok teknolojiyle entegre olabilir ve YAML veya klasik (UI) modunu destekler.

---

### 2.6.2 Konteynerleştirme ve Orkestrasyon Araçları

- **Docker**  
  - Uygulama ve bağımlılıklarını konteyner adı verilen standart birimlerde paketler.  
  - Geliştirme ve üretim ortamları arasında **tutarlılık** sağlar, “Works on my machine” sorunlarını büyük ölçüde azaltır.

- **Kubernetes (K8s)**  
  - Google tarafından geliştirilen, konteynerleri orkestre etmek ve yönetmek için yaygın kullanılan bir platform.  
  - Otomatik ölçeklendirme, yük dengeleme, hata iyileştirme gibi özellikler sunar.

- **Docker Compose**  
  - Birden çok konteynerin (örneğin, uygulama + veritabanı) aynı anda yönetilmesi için hafif bir araç.  
  - Geliştirme ve test aşamalarında sıkça tercih edilir.

---

### 2.6.3 İzleme ve Log Analizi Araçları

- **Prometheus** ve **Grafana**  
  - Prometheus, metrik toplama ve saklama için zaman serisi veritabanı sunar.  
  - Grafana, görsel panolar (dashboard) oluşturmaya yarar ve alarmlar da tanımlanabilir.

- **Elastic Stack (ELK)**  
  - **Elasticsearch** (veri dizini), **Logstash** (veri işleme) ve **Kibana** (görselleştirme) üçlüsünü içerir.  
  - Log analizi ve arama konusunda oldukça yaygındır.

- **Splunk**  
  - Büyük ölçekte log ve veri analizi yapar.  
  - Arama, korelasyon ve görselleştirme olanakları sunar.

---

### 2.6.4 Altyapı Otomasyonu ve Provisioning Araçları

- **Terraform**  
  - Çoklu bulut (AWS, Azure, GCP) ve on-prem altyapıları kodla yönetmek için kullanılır.  
  - Deklaratif yaklaşımı sayesinde, istenen hedef durumu (desired state) tanımlayıp `terraform apply` ile altyapıyı oluşturur veya günceller.

- **Ansible**  
  - Agentless (ajan gerektirmeyen) bir konfigürasyon yönetimi ve provisioning aracıdır.  
  - Basit YAML dosyaları (`playbook`) aracılığıyla sunucuların konfigürasyonunu tanımlamayı sağlar.

- **Chef / Puppet**  
  - Sunucu konfigürasyonu ve yönetimi için kullanılan diğer popüler araçlar.  
  - Büyük kurumsal ortamlarda uzun zamandır tercih edilen çözümlerdir.

---

### 2.6.5 Kod Deposu ve Proje Yönetimi Araçları

- **GitHub**  
  - Dünyanın en popüler Git barındırma (hosting) platformu.  
  - Açık kaynak ve topluluk projeleri için sıkça kullanılır; GitHub Actions gibi yerleşik CI/CD özellikleri vardır.

- **GitLab**  
  - Kendine ait Git deposu barındırma hizmeti ve entegre CI/CD, issue takibi, container registry gibi özellikler sunar.  
  - Açık kaynak sürümü veya bulut tabanlı sürümü vardır.

- **Bitbucket**  
  - Atlassian ekosisteminin bir parçası; Jira, Confluence gibi araçlarla entegre çalışır.  
  - Küçük takımlar ve kurumsal kullanıcılar tarafından tercih edilir.

- **Azure Repos**  
  - Azure DevOps ekosisteminin parçası olarak Git veya TFVC (Team Foundation Version Control) desteği sunar.  
  - Azure Boards, Pipelines, Artifacts gibi diğer modüllerle entegredir.

---

### 2.6.6 İş Birliği ve İletişim Araçları

- **Slack** / **Microsoft Teams**  
  - Ekip içi anlık iletişim ve kanal bazlı iş birliği sağlar.  
  - CI/CD platformlarından gelen bildirimleri entegre etmek mümkündür.

- **Jira**  
  - Yazılım geliştirme süreçlerinde iş akışı, backlog yönetimi, sprint planlama gibi konularda yaygın kullanılan bir araç.  
  - Confluence ile dokümantasyon, Bamboo ile CI/CD gibi Atlassian ailesi ürünleriyle entegre olabilir.

- **Trello**  
  - Kolay kanban panoları ve görev yönetimi sağlayan hafif bir araç.  
  - Küçük takımlar veya hızlı proje takibi için uygundur.

---

### 2.6.7 Doğru Araç Seçimi

DevOps ekosisteminde her kategori için farklı seçenekler mevcuttur ve **her bir aracın güçlü/zayıf yönleri** bulunur. Doğru aracı seçerken göz önünde bulundurmanız gereken faktörler:

- **Ekip Becerileri ve Deneyimi**: Ekip hangi dili, hangi araçları daha iyi biliyor?  
- **Proje ve Altyapı Ölçeği**: Küçük ölçekli bir uygulama mı, yoksa mikroservis mimarisiyle çalışan bir devasa sistem mi?  
- **Entegrasyon İhtiyaçları**: Mevcut sistemlerle, bulut sağlayıcılarla, güvenlik duvarlarıyla veya veritabanlarıyla uyumluluk önemli.  
- **Lisans ve Bütçe**: Bazı araçlar açık kaynak ve ücretsizken, bazıları kurumsal lisans modelleriyle gelir.

Seçilen araçlar, **DevOps** prensiplerini destekleyerek otomasyon, sürekli geri bildirim ve iş birliğini kolaylaştırmalıdır. Ekip büyüdükçe veya proje gereksinimleri değiştikçe, araç seti de gözden geçirilebilir ve uyarlanabilir. DevOps kültürü, “doğru araç” olmadan tam verimli çalışamayacağı gibi, araçlar da **iş birliği, iletişim** ve **sorumluluk paylaşımı** prensiplerine dayalı bir kültür olmadan tek başına yeterli değildir.

# 3. Azure DevOps Server’a Giriş

## 3.1 Azure Boards

**Azure Boards**, projelerinizi planlamak, izlemek ve yönetmek için kullanabileceğiniz bir **iş takibi (work tracking)** platformudur. Yazılım geliştirme sürecini düzenli ve şeffaf hale getirmek için **Scrum**, **Kanban** veya **karma** yaklaşımlarına uygun araçlar sunar. Ekipler, **backlog** oluşturabilir, **iş öğelerini** (User Story, Bug, Task vb.) takip edebilir ve **sprint** planlamaları yapabilir. Ayrıca proje yönetimi süreçlerinin merkezinde yer alarak, geliştirme ve operasyon ekiplerinin birbirleriyle etkin bir şekilde koordinasyon kurmasını sağlar.

> **Resmi Dokümantasyon**:  
> [Azure Boards Hakkında Daha Fazla Bilgi Edinin](https://learn.microsoft.com/tr-tr/azure/devops/boards/)

---

### 3.1.1 Temel Özellikler

1. **Work Items (İş Öğeleri)**  
   - **User Story**, **Bug**, **Epic**, **Feature**, **Issue** gibi iş öğeleri; projenin gereksinimlerini ve yapılacak işleri tanımlamak için kullanılır.  
   - Her iş öğesi, bir başlık (title), açıklama (description), tahmini efor ve sorumlu (assignee) gibi alanları barındırır.

2. **Backlog ve Sprint Yönetimi**  
   - Yazılım geliştirme sürecinde, ekiplerin plan yapması ve iş öğelerini önceliklendirmesi için **backlog** kullanılır.  
   - **Sprint** süreçlerinde, backlog’daki öğelerden seçilen işler belirli bir zaman aralığında tamamlanmaya çalışılır.

3. **Board (Tablo) ve Kanban**  
   - Ekipler, **board** ekranı üzerinden iş öğelerini sürükle-bırak mantığıyla yönetebilir.  
   - Kanban sütunları (To Do, In Progress, Done vb.) veya Scrum görev panosu aracılığıyla, işlerin hangi aşamada olduğunu kolayca takip edebilir.

4. **Query ve Filtreler**  
   - İş öğeleri üzerinde detaylı sorgular (query) oluşturabilir, belirli kriterlere uyan öğeleri listeleyip filtreleyebilirsiniz.  
   - Ekibin ihtiyaçlarına göre özel listeler oluşturarak, iş yükü dağılımını ve öncelikli görevleri görebilirsiniz.

5. **Dashboard ve Raporlama**  
   - Azure Boards verilerini kullanarak **burndown chart**, **cumulative flow diagram** gibi çeşitli raporlar ve panolar oluşturabilirsiniz.  
   - Bu sayede sprint ilerlemesi, ekip performansı veya hata trendleri hakkında görsel ve güncel bilgiler elde edersiniz.

---

### 3.1.2 Process Templates (Süreç Şablonları)

Azure Boards’ta varsayılan olarak **Basic**, **Agile**, **Scrum** ve **CMMI** adlı dört temel süreç şablonu bulunur. Her şablon, iş öğesi tiplerini ve alanlarını yönetmek için farklı bir yapı ve terminoloji sunar:

1. **Basic**  
   - En sade yaklaşımdır. Yeni başlayan ekipler ya da az sayıda iş öğesi kullanan takımlar için uygundur.  
   - **Issue**, **Task**, **Epic** gibi temel iş öğesi tipleri vardır.

2. **Agile**  
   - Kullanıcı hikayesi (User Story), Görev (Task), Hata (Bug), Epic vb. gibi öğeler içerir.  
   - Çevik prensipleri uygulayan ekiplerin sıklıkla tercih ettiği süreç şablonu.

3. **Scrum**  
   - **Product Backlog Item (PBI)**, **Task**, **Bug**, **Sprint**, **Epic** gibi öğeler barındırır.  
   - Sprint temelli iş yönetimi yapan takımlar için uygundur.

4. **CMMI (Capability Maturity Model Integration)**  
   - Daha kurumsal ve süreç odaklı, fazlaca onay/durum akışına ihtiyaç duyan ekipler için tasarlanmıştır.  
   - Değişiklik isteme (Change Request), Gereksinim (Requirement), Görev (Task) gibi ek iş öğesi tipleri bulunur.

Bu süreç şablonları, projenizin **metodolojisi**, **kurumsal standartlar** ve **ekip yaklaşımı** doğrultusunda seçilir. Ayrıca süreç şablonlarında kendi özel iş öğesi tiplerini ekleyerek veya alanları özelleştirerek, şirket gereksinimlerinize uyarlayabilirsiniz.

---

### 3.1.3 Epic -> Feature -> PBI -> Task Hiyerarşisi

**Azure Boards**, iş öğelerini üstten alta bir hiyerarşiyle yönetmeye olanak tanır. Özellikle **Scrum** veya **Agile** şablonlarında şu yapı çok sık görülür:

1. **Epic**  
   - Geniş kapsamlı bir iş veya işlevdir. Örneğin, “Mobil Uygulama Arayüzünün Yenilenmesi” bir Epic olabilir.  
   - Genellikle birkaç sprint veya proje aşamasını kapsayacak kadar büyük iş paketlerini ifade eder.

2. **Feature**  
   - Epic’i destekleyen alt özellikler veya modüller. Örneğin, “Yeni Login Ekranı”, “Profil Düzenleme Modülü” gibi parçalar Epic’in daha somut kısımlarıdır.  
   - Bir Epic birden fazla Feature içerebilir.

3. **Product Backlog Item (PBI) veya User Story**  
   - Scrum sürecinde, Feature’ların gerçekleştirilmesi için gereken kullanıcı senaryoları veya gereksinim parçaları.  
   - Örneğin, “Kullanıcı adı ve şifre ile giriş yapabilme” bir PBI olabilir.  
   - Genelde bir sprint içinde tamamlanabilecek büyüklükte olur.

4. **Task**  
   - Bir User Story veya PBI’nin gerçekleştirilmesi için gerekli teknik/operasyonel adımlardır.  
   - “Veritabanı Şeması Oluşturma”, “Arayüz Tasarımı”, “API Endpoint Yazma” gibi spesifik işleri ifade eder.  
   - Genellikle birkaç saatlik veya en fazla 1-2 günlük süreyle kapatılacak kadar küçük parçalara ayrılır.

#### Örnek Senaryo

- **Epic**: “Mobil Bankacılık Uygulamasının Yeniden Tasarımı”  
  - Yüksek seviyede; 2 aylık bir süreyi kapsayabilir. İçinde birçok modül veya ekran yenilemesi barındırır.

  - **Feature 1**: “Giriş ve Kayıt İşlemleri”  
    - **PBI 1.1**: “Kullanıcı yeni bir hesap oluşturabilmeli”  
      - **Task 1.1.1**: Veritabanı tablolarının düzenlenmesi  
      - **Task 1.1.2**: API endpoint’lerinin yazılması  
      - **Task 1.1.3**: Mobil arayüz tasarımı  
    - **PBI 1.2**: “Mevcut kullanıcı, kullanıcı adı ve şifre ile giriş yapabilmeli”  
      - **Task 1.2.1**: Oturum açma doğrulama (authentication) servisi  
      - **Task 1.2.2**: Hata mesajlarının lokalizasyonu  
      - **Task 1.2.3**: Test senaryolarının yazılması

  - **Feature 2**: “Anasayfa ve Profil Ekranı”  
    - **PBI 2.1**: “Kullanıcı, anasayfada hesap bakiyelerini görüntüleyebilmeli”  
    - **PBI 2.2**: “Kullanıcı, profil bilgilerini güncelleyebilmeli”  
    - (Devam eden benzer PBIs / Task’lar…)

Bu yapı, hem üst seviye iş yönetimini (Epic/Feature) hem de günlük çalışma detaylarını (PBI/Task) organize etmenizi sağlar. Her seviyedeki öğeler birbirine “parent-child” ilişkisiyle bağlanır. Böylece hangi büyük resim (Epic) altında hangi küçük iş öğeleri (Task) yürütüldüğü açıkça görülür.

---

### 3.1.4 Avantajları

- **Planlama Kolaylığı**: Büyük işleri (Epic) daha küçük, yönetilebilir parçalara (Feature, PBI, Task) ayırarak sprint planlaması yapmak daha sağlıklıdır.  
- **İzlenebilirlik**: Task seviyesinde kim ne yapıyor, hangi işi ne kadar tamamladı gibi soruların cevabı tek bir yapı içinde görülebilir.  
- **Şeffaf İletişim**: Yöneticiler ve iş birimi sahipleri, hangi Epic veya Feature’ın ne aşamada olduğunu backlog panosu üzerinden takip edebilir.  
- **Önceliklendirme**: Epic’ler veya Feature’lar arasında öncelik sıralaması yapabilir, ek kaynak gerektiğinde veya bir işi beklemeye aldığınızda kolayca yönetebilirsiniz.

---

### 3.1.5 İpuçları ve En İyi Uygulamalar

- **Düzgün Boyutlandırma**: Epic ve Feature’lar mümkün olduğunca proje aşamalarını yansıtacak şekilde tanımlanmalı; PBI’lar bir sprint içinde bitirilebilecek kadar küçük tutulmalıdır.  
- **Düzenli Refinement/Grooming**: Backlog öğelerinin düzenli aralıklarla gözden geçirilmesi (Refinement) ve güncellenmesi, sprint planlamalarının daha pürüzsüz geçmesini sağlar.  
- **Net Tanım ve Kabul Kriterleri**: Her PBI veya User Story, “Done” (Tamamlanmış) sayılabilmesi için net kabul kriterleri (Acceptance Criteria) içermeli.  
- **Bağımlılıklar**: Farklı Feature veya PBI’lar arasındaki bağımlılıkları görünür kılmak, ekipler arası koordinasyonu kolaylaştırır.  
- **Sürükle-Bırak veya Kısayollar**: Azure Boards’daki arayüz, iş öğelerini hızlıca sürükle-bırak yöntemiyle hiyerarşik olarak bağlamanıza olanak verir (örneğin, bir Task’ı ilgili PBI altına taşıma).

---

Azure Boards’taki **Process Templates** ve **Epic -> Feature -> PBI -> Task** hiyerarşisi, projelerinizi üst düzeyden en ince detaya kadar **tek bir yönetim modelinde** takip etmenizi sağlar. Bu sayede organizasyon genelinde **izlenebilirlik** artar, **planlama** ve **raporlama** süreçleri kolaylaşır. Özelleştirilebilir iş akışları ve raporlama kabiliyeti ile Azure Boards, çeşitli metodolojileri benimsemiş takımlar için oldukça esnek ve güçlü bir çözüm sunar.

## 3.2 Azure Repos

**Azure Repos**, yazılım geliştirme projeleriniz için **Git** veya **Team Foundation Version Control (TFVC)** tabanlı depo (repository) yönetimi sunan bir platformdur. Bu sayede kodunuzu versiyonlayabilir, dallar (branches) arasında geçiş yapabilir, pull request (PR) süreçlerini yönetebilir ve ekip içi kod incelemesi (code review) gerçekleştirebilirsiniz. 

Azure Repos; *Azure DevOps* ekosisteminin bir modülü olarak, **Azure Boards**, **Pipelines**, **Artifacts** gibi diğer bileşenlerle **entegre** bir şekilde çalışır. Böylelikle hem sürüm kontrolü hem de CI/CD iş akışlarını tek bir platform üzerinden yönetmek mümkün hale gelir.

---

### 3.2.1 Başlangıç: Proje Oluşturma ve Repo Seçimi

1. **Yeni Proje Oluşturma**  
   - Azure DevOps ana sayfasında “**New Project**” butonu ile yeni bir proje oluşturabilirsiniz.  
   - Proje oluşturulurken, **Repo türü** (Git veya TFVC) seçilir. *Önerilen*: Modern ve dağıtık yapısı nedeniyle **Git** kullanımı daha yaygındır.

2. **Var Olan Projelerde Repo Ekleme**  
   - Mevcut bir proje içinde **Repos** sekmesine giderek yeni bir repo oluşturabilirsiniz.  
   - “**Initialize Repository**” adımı ile boş bir depo açabilir veya bir .gitignore, README.md vb. ekleyerek başlatabilirsiniz.

---

### 3.2.2 Azure Repos Menülerinin Detaylı İncelemesi

Azure Repos’a girdiğinizde, sol menüde yer alan çeşitli sekmelerle karşılaşırsınız. Her sekme farklı bir işlevi yerine getirir:

1. **Files (Dosyalar)**  
   - Depodaki tüm klasör ve dosya yapısını gösterir.  
   - Üst kısımda dallar (branches) arasında geçiş yapma seçeneği bulunur.  
   - Dosya içeriklerini direkt olarak tarayıcıda görüntüleyebilir ve küçük değişiklikler için (örneğin README.md düzenlemeleri) tarayıcı üzerinden “**Edit**” diyerek commit yapabilirsiniz.  

2. **Commits**  
   - Seçili dal (branch) üzerindeki son commit’leri, commit mesajlarını, hangi dosyaların değiştiğini ve commit tarihlerini gösterir.  
   - Her commit için detay sayfası mevcut olup, ek olarak **diff** görüntüleme yapılabilir.  
   - Commit’leri kronolojik sırayla görebilir, commit ID’si üzerinden geçmişteki sürümlere göz atabilirsiniz.

3. **Branches (Dallar)**  
   - Projeye ait tüm dalları (branches) ve varsa *tags* (etiketler) listeleyen bölümdür.  
   - Yeni bir dal oluşturabilir, dal silme işlemi yapabilir veya dalları birleştirmek (merge) için *Pull Request* oluşturabilirsiniz.  
   - Her dalın son commit mesajı, commit tarihi ve dal üzerinde kimlerin çalıştığı gibi bilgileri görebilirsiniz.

4. **Pull Requests (PR)**  
   - Kod değişikliklerinin incelendiği, onaylandığı ve dalların birleştirildiği (merge) ana alandır.  
   - Yeni bir PR oluştururken hedef dal (target branch) ve kaynak dal (source branch) seçilir, açıklama (description) yazılır ve *reviewer* eklenir.  
   - Pull Request sayfasında dosya değişikliklerini satır satır (diff) inceleyebilir, yorum (comment) bırakabilir ve onay (approve) veya reddetme (reject) gibi aksiyonlarda bulunabilirsiniz.  
   - **Policies** (ilke) tanımlayarak, örneğin “En az 2 kişinin onayı olmadan merge yapılamaz” gibi kurallar koyabilirsiniz.

5. **Tags (Etiketler)**  
   - Projede belirli commit noktalarını işaretlemek için kullanılan etiketleri (tags) listeler.  
   - Örneğin, bir sürüm (version) yayınladığınızda “v1.0” veya “release-2025-01” gibi bir tag ekleyebilirsiniz.  
   - Bu etiketler, belirli commit’lere hızlıca dönme ve sürümleri takip etme açısından faydalıdır.

6. **Compare**  
   - İki dal veya iki commit arasında farkları (diff) karşılaştırmanızı sağlar.  
   - Geliştiriciler, birleşme (merge) yapmadan önce “compare” özelliği ile hangi dosyalarda ne gibi değişikliklerin olduğunu inceleyebilir.

7. **Branch Policies (Dallar için Politikalar)**  
   - *Branches* menüsünden belirli bir dal (genellikle `main` veya `master`) için koruma (policy) tanımlayabilirsiniz.  
   - Zorunlu çekme istekleri (pull request requirement), zorunlu kod inceleme onayı (reviewers), zorunlu geçmiş başarıyla tamamlanmış build (CI), gibi kurallar eklenebilir.  
   - Böylece ana dalın kalitesi korunur ve ekibin kod review süreciyle tutarlı kalması sağlanır.

8. **Wiki veya Code Search (Opsiyonel Ek Menüler)**  
   - Azure DevOps içerisindeki “Wiki” modülü ile depo içindeki dokümantasyon veya proje belgeleri tutulabilir.  
   - “Code Search” ise depo içindeki kod aramaları için kullanışlı bir özelliktir. (Genellikle ayrı bir extension şeklinde eklenir.)

---

### 3.2.3 Git İş Akışı ile Azure Repos Kullanımı

1. **Repo Klonlama**  
   - Geliştiriciler, **Clone** butonuna tıklayarak URL’yi kopyalar ve `git clone <url>` komutuyla yerel makinede projeyi indirir.  
   - Visual Studio veya VS Code gibi IDE’ler üzerinden de doğrudan klon işlemi yapılabilir.

2. **Branch Oluşturma**  
   - Yeni bir özelliğe veya hata düzeltmesine başlarken, `git checkout -b feature/new-login-page` gibi bir isimle dal oluşturulur.  
   - Azure DevOps’taki *Branches* sekmesiyle dallarınızı görebilir ve yönetebilirsiniz.

3. **Commit & Push**  
   - Yerelde yapılan değişiklikler commit edilerek uzak (remote) depoya push edilir.  
   - Azure Repos, “**Commits**” sekmesinde bu değişiklikleri kayıt altına alır; kim ne zaman, hangi mesajla commit yapmış görünür.

4. **Pull Request Açma**  
   - İş tamamlandığında, “Pull Requests” menüsünden yeni bir PR oluşturulur.  
   - Kaynak dal (ör. `feature/new-login-page`) ve hedef dal (ör. `develop` veya `main`) seçilir.  
   - Ekipten 1 veya 2 kişi “Reviewer” olarak eklenir, gerekirse ek açıklamalar yapılır.

5. **Kod İncelemesi ve Onay**  
   - İnceleme yapan kişiler, diff ekranında satır satır değişiklikleri inceleyip yorum yazar.  
   - Müsait olmayan alanlar veya hatalı görülen noktalar “**Request changes**” seçeneğiyle gönderilir.

6. **Merge (Birleştirme)**  
   - Tüm incelemeler onaylandıktan ve varsa tüm *pipeline/build* kontrolleri (CI) başarılı olduktan sonra PR merge edilir.  
   - Otomatik kapatılma, squash merge veya rebase gibi seçenekler proje tercihinize göre kullanılabilir.

---

### 3.2.4 Sık Karşılaşılan Senaryolar

- **Conflict Çözme**  
  - İki farklı geliştirici aynı satırda değişiklik yaptığında, “merge conflict” ortaya çıkabilir.  
  - Conflict, yerel ortamda veya Azure DevOps web arayüzü üzerinden çözülebilir (yine de genellikle yerelde çözüm daha verimlidir).

- **Kod İnceleme Zorunluluğu**  
  - Branch policy olarak “Pull request review” kuralı konulduğunda, ana dala direkt push engellenir.  
  - Tüm değişikliklerin PR üzerinden geçmesi hem kod kalitesini hem de iş birliğini artırır.

- **Release Branch Stratejisi**  
  - Ekipler “GitFlow”, “GitHub Flow” veya “Trunk-based development” gibi dal stratejilerini Azure Repos üzerinde uygular.  
  - Major, minor ve patch sürümlerine göre branch yapısı tanımlanabilir.

---

### 3.2.5 En İyi Uygulamalar

1. **Anlamlı Commit Mesajları**  
   - “Fix bug” gibi belirsiz mesajlar yerine, “Fix null reference bug in login controller” gibi net tanımlar kullanmak ekip iletişimini güçlendirir.

2. **Kısa Ömürlü Branch’ler**  
   - Branch’leri uzun süre açık tutmak conflict riskini artırır. Mümkün olduğunca kısa feature dalı, sık merge işlemi idealdir.

3. **Düzenli Pull Request İncelemeleri**  
   - Kod incelemeleri (code review) sadece hataları yakalamakla kalmaz, ekip içinde bilgi paylaşımını da artırır.  
   - PR’ların küçük ve odaklı olması incelemeyi kolaylaştırır.

4. **Pipeline Entegrasyonu**  
   - Her PR açıldığında otomatik build/test çalıştırarak hataları erken tespit edin. (Azure Pipelines ile entegre edilebilir.)  

5. **Branch Policy**  
   - Ana dalın güvenliği için, en az bir onay (approval) ve başarılı build koşulu gibi politikalar eklenmesi tavsiye edilir.

---

Azure Repos, **DevOps** yaklaşımını benimseyen ekipler için **güçlü** ve **esnek** bir kod yönetim ortamı sunar. Hem küçük ekipler hem de büyük kurumsal projeler, Azure Repos’un dallanma stratejileri, pull request mekanizmaları ve zengin entegrasyon özellikleri sayesinde kodlarını düzenli ve güvende tutabilir. Bu sayede, geliştirme süreçleri daha şeffaf, izlenebilir ve iş birliğine dayalı hale gelir.

## 3.3 Azure Pipelines

**Azure Pipelines**, yazılım projelerinizi **sürekli entegrasyon (CI)** ve **sürekli teslim (CD)** süreçleriyle otomatik hale getirmenizi sağlayan bir araçtır. Kod değişiklikleriniz depo (Azure Repos, GitHub, vb.) üzerine gönderildiğinde veya belirli tetikleyiciler gerçekleştiğinde, **derleme**, **test**, **yayınlama** ve **dağıtım** (deployment) gibi aşamaları **pipeline** adını verdiğimiz iş akışları sayesinde otomatik olarak çalıştırabilirsiniz. Bu sayede yazılımlarınızı **daha hızlı**, **daha güvenilir** ve **daha tutarlı** şekilde üretim veya test ortamlarına taşımanız mümkün olur.

> **Resmi Dokümantasyon**:  
> [Azure Pipelines Hakkında Daha Fazla Bilgi Edinin](https://learn.microsoft.com/tr-tr/azure/devops/pipelines)

---

### 3.3.1 Pipeline Türleri: YAML ve Klasik (Classic)

Azure Pipelines, iki farklı yöntemle pipeline tanımlamaya izin verir:

1. **YAML Tabanlı Pipelines**  
   - Pipeline tanımınızı bir `.yml` dosyası içinde saklarsınız. Bu dosya, **versiyon kontrol** altında olduğundan, pipeline değişiklikleri de tıpkı kod gibi sürümlenir.  
   - Geliştiriciler, pipeline’ı doğrudan kod deposunda düzenleyebilir, dallara ayırarak (branch) farklı denemeler yapabilir.  
   - DevOps felsefesine uygun olarak, **pipeline-as-code** yaklaşımını destekler.

2. **Klasik (Classic) Pipelines**  
   - Azure DevOps’un grafik arayüzü (UI) üzerinden adım adım oluşturulur.  
   - Sürükle-bırak mantığıyla **derleme (build)** ve **yayınlama (release)** adımlarını tanımlayabilirsiniz.  
   - Özellikle **Release Pipelines** (ortam yönetimi, onay mekanizmaları vb.) tarafında klasik arayüz hâlâ yaygın şekilde kullanılır.

> **Not**: Microsoft, gelecekte YAML yaklaşımını daha fazla teşvik ederken, mevcut klasik pipeline’ları da desteklemeye devam ediyor. Ekip ve proje ihtiyaçlarınıza göre tercih yapabilirsiniz.

---

### 3.3.2 Ana Menüler ve Özellikler

Azure Pipelines sekmesine girdiğinizde, sol menüde veya üst kısımda bazı alt bölümler görürsünüz:

1. **Pipelines**  
   - Mevcut tüm **CI** (build) pipeline’larını listeler.  
   - Yeni bir pipeline oluşturabilir, varolanları düzenleyebilir, tetikleyebilir veya sonuçlarını inceleyebilirsiniz.

2. **Releases**  
   - Klasik “**Release Pipelines**” yönetimini yapar.  
   - Ortam (environment) tanımları, aşamalar (stages), onaylar (approvals) ve dağıtım (deploy) geçmişine buradan erişebilirsiniz.

3. **Environments (YAML tabanlı)**  
   - Çok aşamalı (multi-stage) YAML pipeline’larda **staging**, **production** gibi ortamları yönetmek için kullanılır.  
   - Manuel onaylar veya denetimler (gates) ekleyerek, belirli bir aşamadan diğerine geçişte kontrol sağlanabilir.

4. **Library**  
   - Değişken grupları (variable groups), güvenli dosyalar (secure files) veya sertifikalar gibi ortak öğelerin saklandığı alandır.  
   - Pipeline’larda tekrar tekrar kullanmak istediğiniz gizli değerleri (ör. API anahtarları) burada yönetebilirsiniz.

5. **Task Grupları (UI)**  
   - Sık kullanılan bir dizi pipeline adımını (ör. test, derleme, dağıtım) tek bir grup olarak tanımlayarak başka projelerde de yeniden kullanabilirsiniz.

---

### 3.3.3 Sürekli Entegrasyon (CI) Pipeline Süreci

Aşağıda, tipik bir **CI Pipeline** akışının adımları yer alır:

1. **Tetikleyici (Trigger)**  
   - Kod deposuna (Azure Repos, GitHub vb.) bir commit geldiğinde veya planlanmış bir zamanlama (cron) devreye girdiğinde pipeline tetiklenir.

2. **Kaynak Kod Alımı (Checkout)**  
   - Pipeline, build ajanına (agent) kodu klonlar veya indirir.

3. **Bağımlılıkları Yükleme**  
   - .NET, Node.js, Java gibi projelerde gerekli paketler (NuGet, npm, Maven vb.) indirilir.

4. **Derleme (Build)**  
   - Kod, proje türüne göre derlenir. (Örneğin, `dotnet build --configuration Release`)

5. **Test**  
   - Unit test, integration test veya UI test aşamaları otomatik olarak çalışır.  
   - Başarısız olan testler pipeline’ın başarısız olmasına yol açar.

6. **Sonuç ve Artefact Yayınlama**  
   - Testler geçildiyse, derlenen çıktı (ör. DLL’ler, paketler, Docker imajı vb.) bir artefact deposuna veya kayıt deposuna (registry) yüklenebilir.  
   - Bu artefact’lar, **Continuous Delivery** veya **Release** aşamalarında kullanılmak üzere saklanır.

7. **Bildirim**  
   - Pipeline sonuçları (başarılı/başarısız) ekibe e-posta, Teams, Slack vb. kanallar üzerinden iletilebilir.

---

### 3.3.4 Sürekli Teslim/Dağıtım (CD) ve Release Pipelines

**Continuous Delivery (CD)** aşamasında, başarılı bir build sonrası elde edilen artefact veya imajlar, farklı ortamlara (test, staging, production) otomatik ya da yarı otomatik (manuel onayla) olarak dağıtılır.

1. **Ortamlar ve Aşamalar (Stages)**  
   - “Dev”, “Test/QA”, “Stage” ve “Prod” gibi farklı aşamalar tanımlanır.  
   - Her aşamada farklı görevler (tasks) veya onay mekanizmaları olabilir.

2. **Görevler (Tasks)**  
   - IIS Web App Deploy, Azure App Service Deploy, Docker Push, Kubernetes rollout vb. görevler mevcuttur.  
   - Bu görevler, uygulamanın ilgili hedef ortama veya platforma gönderilmesini (deploy) sağlar.

3. **Onay Mekanizmaları (Approvals)**  
   - Ortam geçişlerinde ekip yöneticisi, ürün sahibi veya güvenlik ekibinin manuel onay vermesi gerekebilir.  
   - CD pipeline, onay verilene kadar bekler.

4. **Dağıtım Stratejileri**  
   - **Blue-Green**: İki farklı üretim ortamı (blue ve green) arasında trafiği yönlendirerek kesintisiz geçiş sağlanır.  
   - **Canary**: Yeni sürüm, kullanıcıların sadece küçük bir kısmına yönlendirilir, sorunsuz çalıştığı onaylanınca tam dağıtım yapılır.  
   - **Rolling**: Dağıtım, parça parça gerçekleştirilir ve eski versiyon kademeli olarak kapatılır.

5. **Geri Dönüş (Rollback)**  
   - Dağıtımdan sonra sorun çıkarsa, bir önceki başarılı sürüme dönmek (rollback) mümkündür.  
   - Bu işlem için pipeline içinde geri dönüş adımları veya anlık yedekler (snapshot) kullanılabilir.

---

### 3.3.5 En İyi Uygulamalar

1. **Küçük ve Sık Değişiklikler**  
   - Büyük, kapsamlı değişiklikler yerine küçük parça halinde sürümler yapmak, hataları daha çabuk yakalamayı kolaylaştırır.

2. **Pipeline-as-Code**  
   - Mümkün olduğunca **YAML** yaklaşımını kullanarak, pipeline’ınızı **versiyon kontrolü** altında tutun.  
   - Değişikliklerin kim tarafından ve ne amaçla yapıldığı şeffaf bir şekilde izlenebilir.

3. **Test Otomasyonu**  
   - Bir pipeline’da farklı test türleri (birim, entegrasyon, performans, güvenlik) otomatik olarak çalıştırılarak daha yüksek kod kalitesi elde edilir.

4. **Aşamalı Dağıtım**  
   - Tüm kullanıcıları riske atmak yerine, önce test/staging ortamında veya küçük bir kullanıcı grubunda deneme yapmak idealdir.

5. **Gizli Bilgileri Güvenli Saklama**  
   - API anahtarları, parolalar gibi hassas bilgiler “Library > Variable Groups” içinde **secret** olarak tutulmalı ve pipeline’da asla düz metin olarak yer almamalı.

6. **Gözlemleme ve Geri Bildirim Döngüsü**  
   - Dağıtım sonrası izleme (monitoring) araçlarından gelen alarmlar, log analizleri pipeline sonuçlarına dahil edilmeli.  
   - Sorunlar erken tespit edildiğinde hızlıca yeni bir sürüm (hotfix) pipeline’la yayınlanabilir.

---

**Azure Pipelines**, DevOps ekosisteminde otomasyon ve sürekli iyileştirme felsefesinin **omurgasını** oluşturur. Ekipler, sık sık kod değişikliği yapabilir, her değişikliği derleyip test ederek sürüm kalitesini artırabilir ve hızlıca üretim ortamına taşıyabilir. Bu, yazılım projelerinin **hız, güvenilirlik ve müşteri memnuniyeti** açısından büyük avantajlar elde etmesini sağlar.

## 3.4 Azure Artifacts

**Azure Artifacts**, yazılım projelerinizde kullandığınız paketleri (NuGet, npm, Maven, Python vb.) **merkezi bir konumda** barındırma ve yönetme imkânı sunar. Şirket içi (on-prem) veya bulut tabanlı projelerde, bağımlılık paketlerinizi dış ortamlardan izole edebilir, özelleştirilmiş paket depoları (feed) oluşturabilir ve kurumsal güvenlik politikalarına uygun şekilde dağıtabilirsiniz. Aynı zamanda **proxy** (aracı) görevi görerek, geliştiricilerin makinelerinden direkt olarak harici paket kaynaklarına (npmjs.org, nuget.org, pypi.org vb.) bağlanma ihtiyacını ortadan kaldırabilir.

> **Resmi Dokümantasyon**:  
> [Azure Artifacts Hakkında Daha Fazla Bilgi Edinin](https://learn.microsoft.com/tr-tr/azure/devops/artifacts)

---

### 3.4.1 Temel Özellikler

1. **Paket Depolama (Feeds)**  
   - Takım veya organizasyon genelinde kullanılacak **NuGet**, **npm**, **Maven**, **Python** paketlerini özel depolarda saklayabilirsiniz.  
   - Her feed, sadece belirli geliştiricilerin veya projelerin erişimine açık olacak şekilde konfigüre edilebilir.

2. **Proxy (Upstream Kaynaklar)**  
   - Kurumsal ortamlarda, geliştiricilerin **doğrudan** internet üzerindeki paket kayıtlarına (registry) erişmeleri güvenlik veya ağ politikaları gereği engellenebilir.  
   - Azure Artifacts, **proxy** olarak çalışıp ihtiyaç duyulan paketleri harici kaynaktan (örn. npmjs, nuget.org) indirerek kendi içinde önbellekler.  
   - Geliştiriciler ise **organizasyon içi** bir URL üzerinden paketlere erişir. Böylece hem güvenlik hem de merkezî yönetim sağlanır.

3. **Sürüm ve Bağımlılık Yönetimi**  
   - Versiyon çakışmalarını önlemek için paketleri belirli sürüm kurallarıyla yayınlayabilir, silme (deprecate) veya liste dışı bırakma (unlist) işlemleri yapabilirsiniz.  
   - Pipeline’larda kullanılan paketlerin tam olarak hangi sürümlerinin nerede tüketildiğini görebilir, bağımlılık zincirlerini analiz edebilirsiniz.

4. **Paket Paylaşımı**  
   - Birden fazla projede kullanılan ortak kütüphaneleri (shared libraries) tek bir feed üzerinde tutarak tekrar kullanılabilir hale getirebilirsiniz.  
   - Böylece hem kod tekrarını (duplicate) azaltır hem de güncellemeleri tek noktadan yönetirsiniz.

---

### 3.4.2 Nasıl Çalışır? (Proxy / Upstream Senaryosu)

#### 1. Upstream Kaynak Tanımlama
- Azure DevOps’taki **Artifacts** > **Feeds** bölümüne girip, oluşturacağınız feed için “**Upstream Sources**” sekmesinden harici kayıtları (örneğin npmjs.org veya nuget.org) ekleyebilirsiniz.  
- Bu sayede, feed içinde bulunmayan bir paket talep edildiğinde, Azure Artifacts **harici kaynağa** gidip paketi alır ve yerel depoda önbelleğe alır.

#### 2. Geliştirici Makinesinden Erişim
- Geliştirici tarafında, `npm install` veya `nuget restore` gibi komutlar çalıştığında, adres olarak **Azure Artifacts feed URL** kullanılır.  
- Paket yerel depoda (cache) yoksa, Azure Artifacts upstream kaynağa bağlanıp paketi alır ve geliştiriciye iletir.

#### 3. Kurumsal Güvenlik ve Ağ Politikası
- Geliştiricilerin direkt internet çıkışı yapması engellenmiş olsa bile, Azure DevOps servis hesabı (veya on-prem Azure DevOps Server) izinli bir ağ segmentinde konumlandırılabilir.  
- Böylece tüm paket trafiği **tek bir çıkış noktası** üzerinden yönetilir, loglanır ve kontrol altında tutulur.

---

### 3.4.3 Azure Artifacts Menüsü ve Özellikleri

1. **Feeds**  
   - Organizasyonunuzdaki tüm feed’lerin (ör. `MyTeamFeed`, `GlobalSharedPackages`) listelendiği bölümdür.  
   - Yeni feed oluşturmak veya mevcut feed’leri düzenlemek buradan yapılır.

2. **Feed Ayarları**  
   - Erişim seviyeleri (kimler görüntüleyebilir, kimler paket yükleyebilir?)  
   - Otomatik paket silme stratejileri (retention policies)  
   - Upstream kaynaklar (proxy yapılandırmaları)

3. **Package Management**  
   - Her feed’in içinde paketleri görebilirsiniz (NuGet paketleri, npm modülleri, PyPI paketleri vb.).  
   - Bir paketin hangi sürümleri mevcut, hangi meta verilere sahip (description, license, last updated) gibi bilgileri inceleyebilirsiniz.  
   - Paketleri tek tıkla silme, sürüm yükseltme veya indirme işlemleri mümkündür.

4. **Connect to Feed**  
   - Farklı paket yöneticileriyle (npm, NuGet, Maven, pip) feed’e bağlanmak için gereken konfigürasyon yönergelerini içeren kısım.  
   - Örneğin, `.npmrc` veya `nuget.config` dosyasına eklemeniz gereken URL ve kimlik doğrulama bilgilerini burada bulursunuz.

5. **Usage** (Kullanım)  
   - Bazı durumlarda, feed içindeki paketlerin hangi projelerde veya pipeline’larda kullanıldığını görebilir, kullanım metrikleri çıkarabilirsiniz (özellikle kurumsal paketlerin versiyon yönetiminde faydalıdır).

---

### 3.4.4 Tipik Kullanım Senaryoları

1. **Ortak Kütüphanelerin Paylaşımı**  
   - Büyük bir organizasyonda, farklı takımların ortak kullandığı .NET kütüphanelerini (NuGet) tek bir feed üzerinden yönetebilirsiniz.  
   - Güncellemeleri veya hata düzeltmelerini yapınca, paketi Azure Artifacts’e yayınlarsınız; tüm ekipler otomatik olarak yeni sürümü kullanabilir (ya da geçmeyi tercih edebilir).

2. **Kurumsal Proxy / Hava Geçirmez Ağ (Air-Gapped Network) Senaryosu**  
   - Sıkı güvenlik duvarı kuralları nedeniyle, geliştiricilerin npm veya nuget.org’a doğrudan erişimi yoktur.  
   - Azure Artifacts, **upstream** olarak konfigüre edilerek harici paketlerin indirilmesi ve önbelleklenmesi için kullanılır.

3. **Pipeline ve Sürüm Yönetimi**  
   - Azure Pipelines, build aşamasında ihtiyaç duyduğu tüm bağımlılık paketlerini Azure Artifacts üzerinden çekebilir.  
   - Özel bir paketi (.NET, npm modülü vb.) başka projelere dağıtmak istediğinizde, build sonucunda o paketi de Azure Artifacts’e yükleyebilirsiniz.

4. **Kontrollü Paket Akışı**  
   - Paketlerin (örneğin belirli sürümdeki npm veya NuGet paketlerinin) zararlı veya hatalı olduğu tespit edildiğinde, feed üzerinden kaldırabilir veya erişimi kısıtlayabilirsiniz.  
   - Bu denetim sayesinde, olası güvenlik açıklarını kapatmak veya hatalı paketlerin kullanımını engellemek kolaylaşır.

---

### 3.4.5 En İyi Uygulamalar

1. **Versiyon Politikasını Belirleme**  
   - SemVer (Semantic Versioning) gibi endüstri standartlarını takip etmek, paket güncellemelerinin öngörülebilirliğini artırır.

2. **Bağımlılık Yönetimi**  
   - Aynı paketin farklı sürümlerine duyulan ihtiyacın farkında olun; hangi projelerin hangi sürümü kullandığını dokümante edin veya Azure Artifacts üzerinden izleyin.  
   - Gerektiğinde eski sürümlere geri dönmek için (rollback) paketlerinizi kaldırmak yerine “deprecated” ilan edebilir veya “unlist” yapabilirsiniz.

3. **Upstream Kaynak Sınırlamaları**  
   - Her harici kaynağı (npmjs, nuget.org vb.) eklemek yerine, sadece ihtiyaç duyulanları ekleyerek saldırı yüzeyini daraltın.  
   - Şirket politikasına uygunluk (lisans, güvenlik vb.) açısından sadece onaylı kaynaklar eklenmeli.

4. **Kimlik Doğrulama ve Erişim Kontrolü**  
   - Feed’lere erişecek kullanıcı ve servis hesapları, Azure DevOps üzerinden uygun izinlerle (Contributor, Reader, vb.) atanmalı.  
   - Hassas iç paketlerin yanlışlıkla herkesin kullanımına açılmasını engellemek için gizlilik (private feed) ayarlarına dikkat edin.

5. **Pipeline Entegrasyonu**  
   - Yapılan her build’de üretilen paketleri Azure Artifacts’e otomatik yüklemek, sürüm takibini basitleştirir.  
   - Varsayılan olarak feed’i pipeline’da tanımlayarak geliştiricilerin manuel ayar yapma yükünü azaltabilirsiniz.

---

**Azure Artifacts**, paket yönetimini **merkezi**, **güvenli** ve **izlenebilir** bir yapıya kavuşturur. Gerek kurumsal güvenlik gerekse yeniden kullanılabilirlik açısından avantaj sağlayan bu modül, **DevOps** felsefesinin “otomasyon” ve “iş birliği” prensiplerini paket yönetimi tarafında destekler. Özellikle güvenlik kısıtları olan şirketlerde, **proxy** özelliği aracılığıyla harici paket kaynaklarına **kontrollü** erişim sağlamak ve geliştiricilerin işini kolaylaştırmak için sıkça tercih edilir.

## 3.5 Azure Test Plans

**Azure Test Plans**, yazılım projeleriniz için kapsamlı **test yönetimi** çözümleri sunan bir hizmettir. Manuel testler, keşif testleri ve otomatik testler gibi farklı test türlerini planlamak, yürütmek ve izlemek için kullanılır. Azure Test Plans, kalite güvencesi süreçlerini sistematik hale getirerek, hataların erken tespit edilmesini ve çözülmesini sağlar. Bu sayede, yazılımın **yüksek kalitede** ve **güvenilir** olarak teslim edilmesine katkıda bulunur.

> **Resmi Dokümantasyon**:  
> [Azure Test Plans Hakkında Daha Fazla Bilgi Edinin](https://learn.microsoft.com/tr-tr/azure/devops/test/overview)

---

### 3.5.1 Temel Kavramlar

Azure Test Plans, test süreçlerinizi organize etmek ve yönetmek için aşağıdaki temel bileşenleri kullanır:

1. **Test Plan (Test Planı)**
   - Projenizdeki tüm test aktivitelerini kapsayan yüksek seviyeli bir plandır.
   - Test planları, farklı sürümler, özellikler veya sprint’ler için ayrı ayrı oluşturulabilir.
   - Her test planı, belirli bir hedefi veya kapsamı temsil eder ve ilgili test suite’leri içerir.

2. **Test Suite (Test Takımı)**
   - Test planı içinde organize edilen testlerin gruplandırıldığı bölümdür.
   - Farklı test türlerine veya işlevsel alanlara göre ayrılabilir.
   - Üç ana test suite türü vardır:
     - **Static Test Suite**: Belirli test case’lerinin manuel olarak eklenip çıkarıldığı sabit bir test grubudur.
     - **Requirement-based Test Suite**: Belirli bir gereksinime (user story, epic) bağlı test case’lerini otomatik olarak toplar.
     - **Query-based Test Suite**: Belirli bir sorguya (query) göre dinamik olarak test case’lerini toplar.

3. **Test Case (Test Durumu)**
   - Belirli bir işlevin veya gereksinimin doğrulanmasını sağlayan ayrıntılı adımlardır.
   - Her test case, **girdi**, **beklenen çıktı** ve **adımlar** gibi bilgileri içerir.
   - Test case’leri, manuel testler için ayrılır veya otomatik test senaryolarına entegre edilebilir.

4. **Test Run (Test Çalıştırması)**
   - Test case’lerinin belirli bir zaman diliminde veya sprint içerisinde yürütüldüğü oturumdur.
   - Test run’lar, testlerin durumu (başarılı, başarısız, atlanmış) hakkında bilgi sağlar.
   - Hatalar veya eksiklikler olduğunda, ilgili test case’ler üzerinden geri bildirim sağlanır.

---

### 3.5.2 Test Plan -> Test Suite -> Test Case Hiyerarşisi

Azure Test Plans içerisinde, test aktiviteleri **hiyerarşik** bir yapı ile organize edilir. Bu yapı, testlerin sistematik bir şekilde yönetilmesini ve izlenmesini sağlar.

#### 1. Test Planı (Test Plan)
   - **Tanım**: Projenizin genel test stratejisini ve kapsamını belirleyen üst seviye plandır.
   - **Örnek**: "Sprint 1 Test Planı" veya "Release 1.0 Test Planı"
   - **İçerik**: Birden fazla test suite’i barındırır.

#### 2. Test Takımı (Test Suite)
   - **Tanım**: Test planı içinde belirli bir alana veya işlevselliğe odaklanan testlerin toplandığı gruptur.
   - **Örnek**:
     - "Kullanıcı Girişi Test Takımı"
     - "Ödeme İşlemleri Test Takımı"
   - **İçerik**: Birden fazla test case’i içerir.

#### 3. Test Durumu (Test Case)
   - **Tanım**: Belirli bir işlevin veya gereksinimin doğrulanmasını sağlayan ayrıntılı adımlardır.
   - **Örnek**:
     - **Başlık**: "Kullanıcı adı ve şifre ile giriş yapabilme"
     - **Açıklama**: "Geçerli kullanıcı adı ve şifre ile giriş yapıldığında, kullanıcı ana sayfaya yönlendirilmelidir."
     - **Adımlar**:
       1. Giriş sayfasını açın.
       2. Kullanıcı adı alanına geçerli bir kullanıcı adı girin.
       3. Şifre alanına geçerli bir şifre girin.
       4. "Giriş Yap" butonuna tıklayın.
     - **Beklenen Sonuç**: Kullanıcı, ana sayfaya yönlendirilir ve başarı mesajı görüntülenir.

#### Hiyerarşi Örneği

Aşağıda, bir test planı içindeki hiyerarşik yapının nasıl olabileceğine dair bir örnek verilmiştir:

- **Test Planı**: "Sprint 1 Test Planı"
  - **Test Takımı**: "Kullanıcı Girişi Test Takımı"
    - **Test Durumu 1**: "Geçerli kullanıcı adı ve şifre ile giriş yapabilme"
      - **Adımlar ve Beklenen Sonuçlar**
    - **Test Durumu 2**: "Geçersiz şifre ile giriş yapılamaması"
      - **Adımlar ve Beklenen Sonuçlar**
  - **Test Takımı**: "Ödeme İşlemleri Test Takımı"
    - **Test Durumu 3**: "Kredi kartı ile ödeme yapabilme"
      - **Adımlar ve Beklenen Sonuçlar**
    - **Test Durumu 4**: "Geçersiz kredi kartı bilgileri ile ödeme yapılamaması"
      - **Adımlar ve Beklenen Sonuçlar**

Bu yapı sayesinde, her bir test case’in hangi test takımına ve test planına ait olduğu net bir şekilde görülebilir. Ayrıca, belirli bir işlevselliğin test edilip edilmediği kolayca kontrol edilebilir.

---

### 3.5.3 Test Run'lar

**Test Run**, belirli bir zaman diliminde veya sprint içerisinde gerçekleştirilen testlerin toplandığı oturumdur. Test run’lar, test planındaki test case’lerinin yürütülmesini ve sonuçların kaydedilmesini sağlar. Bu sayede, testlerin ne kadarının başarılı, ne kadarının başarısız olduğu, hangi hataların ortaya çıktığı ve hangi iyileştirmelerin gerektiği hakkında bilgi sahibi olunur.

#### Test Run Oluşturma

1. **Yeni Test Run Başlatma**
   - Azure Test Plans ana sayfasında, ilgili **Test Planı** seçilir.
   - Sağ üst köşedeki “**Run Tests**” butonuna tıklanarak yeni bir test run başlatılır.

2. **Test Case’leri Seçme**
   - Yürütülecek test case’leri seçin veya tüm test case’lerini dahil edin.
   - Filtreler kullanarak belirli koşullara uyan test case’lerini seçebilirsiniz.

3. **Ortam ve Ayarlar**
   - Test run’un hangi ortamda (test, staging, production) yürütüleceği belirlenir.
   - Gerekli ayarlar (örneğin, özel test ortamları veya cihazlar) yapılır.

4. **Test Run’u Başlatma**
   - Seçilen test case’leri için test run başlatılır.
   - Her bir test case, manuel olarak veya otomatik olarak yürütülür.

#### Test Run Sonuçları

- **Durumlar**: Her bir test case’in durumu “Passed”, “Failed”, “Blocked” veya “Not Executed” gibi kategorilere ayrılır.
- **Hatalar ve Notlar**: Başarısız olan test case’leri için hata detayları ve geliştirici notları eklenebilir.
- **Raporlama**: Test run sonuçları, **raporlar** ve **grafikler** aracılığıyla analiz edilebilir. Bu sayede, hangi alanlarda iyileştirme gerektiği belirlenir.

#### Test Run Yönetimi

- **Tekrarlama (Rerun)**: Başarısız olan test case’leri yeniden çalıştırabilirsiniz.
- **İptal Etme (Abort)**: Gerekirse, devam eden bir test run’u iptal edebilirsiniz.
- **Tarihçe**: Önceki test run’ların sonuçlarını inceleyerek, zaman içindeki gelişmeleri ve trendleri takip edebilirsiniz.

---

### 3.5.4 Örnek Bir Test Planı Süreci

Aşağıda, **Epic -> Feature -> PBI -> Test Plan -> Test Suite -> Test Case** hiyerarşisi içinde bir test planının nasıl oluşturulabileceğine dair bir örnek senaryo verilmiştir:

#### 1. Epic ve Feature Oluşturma

- **Epic**: "Kullanıcı Yönetimi Modülü"
  - **Feature 1**: "Kullanıcı Kaydı"
    - **PBI 1.1**: "Yeni kullanıcı kayıt olabilmeli"
      - **Test Planı**: "Kullanıcı Kaydı Test Planı"
        - **Test Takımı**: "Kullanıcı Kaydı Test Suite"
          - **Test Case 1**: "Geçerli bilgilerle kayıt olma"
          - **Test Case 2**: "Eksik bilgilerle kayıt olmama"
    - **PBI 1.2**: "Kullanıcı doğrulama e-postası alabilmeli"
      - **Test Planı**: "Kullanıcı Doğrulama Test Planı"
        - **Test Takımı**: "Doğrulama E-postası Test Suite"
          - **Test Case 3**: "Doğrulama e-postasının gönderilmesi"
          - **Test Case 4**: "Doğrulama bağlantısının çalışması"

#### 2. Test Planı ve Test Suite Oluşturma

- **Test Planı**: "Kullanıcı Kaydı Test Planı"
  - **Test Suite**: "Kullanıcı Kaydı Test Suite"
    - **Test Case 1**: "Geçerli bilgilerle kayıt olma"
      - **Adımlar**:
        1. Kayıt sayfasını açın.
        2. Geçerli kullanıcı bilgilerini girin.
        3. "Kayıt Ol" butonuna tıklayın.
      - **Beklenen Sonuç**: Kullanıcı başarıyla kayıt olur ve giriş sayfasına yönlendirilir.
    - **Test Case 2**: "Eksik bilgilerle kayıt olmama"
      - **Adımlar**:
        1. Kayıt sayfasını açın.
        2. Bazı zorunlu alanları boş bırakın.
        3. "Kayıt Ol" butonuna tıklayın.
      - **Beklenen Sonuç**: Kullanıcıya eksik alanlarla ilgili hata mesajları gösterilir.

#### 3. Test Run Yürütme

- **Test Run**: "Sprint 1 Test Run"
  - **Test Planı**: "Kullanıcı Kaydı Test Planı"
    - **Test Case 1**: "Geçerli bilgilerle kayıt olma" - **Passed**
    - **Test Case 2**: "Eksik bilgilerle kayıt olmama" - **Failed**
      - **Hata Detayı**: "Kayıt olma işlemi sırasında eksik alan uyarısı gösterilmiyor."
      - **Not**: "Frontend validasyonunda eksiklik var, düzeltme gereklidir."

Bu örnek senaryo, bir Epic altında nasıl test planlarının, test suite’lerinin ve test case’lerinin organize edilebileceğini göstermektedir. Her bir adım, kalite güvencesi süreçlerinin nasıl yapılandırılabileceği ve izlenebileceği konusunda net bir yol haritası sunar.

---

### 3.5.5 En İyi Uygulamalar

1. **Test Hiyerarşisini Net Belirleyin**
   - Epic, Feature, PBI ve Test Plan gibi hiyerarşik yapıları belirlerken, her seviyenin amacını ve kapsamını netleştirin. Bu, test süreçlerinin daha düzenli ve yönetilebilir olmasını sağlar.

2. **Detaylı ve Net Test Case’ler Oluşturun**
   - Her test case’in adımları ve beklenen sonuçları açık ve net olmalıdır. Bu, testlerin tekrarlanabilirliğini ve doğruluğunu artırır.

3. **Düzenli Test Run’lar Yapın**
   - Test run’ları düzenli aralıklarla (örneğin, her sprint sonunda) gerçekleştirerek, yazılımın kalitesini sürekli olarak değerlendirin ve iyileştirin.

4. **Otomatik Testlerle Entegrasyonu Sağlayın**
   - Mümkün olduğunca, manuel testlerin yanında otomatik testleri de kullanarak test süreçlerini hızlandırın ve hata payını azaltın.

5. **Geri Bildirim Döngülerini Hızlandırın**
   - Test sonuçlarını hızlıca ekibe ileterek, hataların hızlıca düzeltilmesini sağlayın. Bu, geliştirme sürecinin verimliliğini artırır.

6. **Test Verilerini Yönetim Altına Alın**
   - Testler için kullanılan verilerin doğru ve güncel olduğundan emin olun. Test ortamlarında gerçekçi ve çeşitli veri setleri kullanmak, testlerin etkinliğini artırır.

7. **İzlenebilirlik Sağlayın**
   - Her test case’in hangi gereksinime veya kullanıcı hikayesine karşılık geldiğini izleyebilmek için ilişkilendirme yapın. Bu, gereksinimlerin karşılanıp karşılanmadığını değerlendirmeyi kolaylaştırır.

8. **Düzenli Backlog Refinement ve Grooming Yapın**
   - Test planlarınızı ve test case’lerinizi düzenli olarak gözden geçirerek güncelleyin. Yeni gereksinimler ortaya çıktıkça test planlarınıza eklemeler yapın.

---

Azure Test Plans, **DevOps** süreçlerinin **kalite güvencesi** kısmını güçlü bir şekilde destekler. Test planlama, yürütme ve izleme aşamalarında sağladığı kapsamlı özelliklerle, yazılım geliştirme sürecinde kaliteyi en üst düzeye çıkarmak için vazgeçilmez bir araçtır. Ekipler, Azure Test Plans’ı etkin kullanarak daha **iyi test stratejileri** geliştirebilir, hataları erken aşamalarda tespit edip düzelterek müşteri memnuniyetini artırabilir ve yazılım teslim süreçlerini **daha güvenilir** hale getirebilirler.

## 3.6 Azure DevOps Server ve Azure DevOps Services Farkları

**Azure DevOps Server** ve **Azure DevOps Services**, Microsoft’un sunduğu iki farklı DevOps çözümüdür. Her ikisi de yazılım geliştirme süreçlerini yönetmek, işbirliğini artırmak ve CI/CD (Continuous Integration/Continuous Deployment) süreçlerini otomatikleştirmek için kapsamlı araçlar sağlar. Ancak, bu iki hizmet arasında çeşitli farklar bulunmaktadır. Bu bölümde, Azure DevOps Server ile Azure DevOps Services arasındaki temel farkları detaylı bir şekilde inceleyeceğiz.

> **Resmi Dokümantasyon**:
> - [Azure DevOps Server](https://learn.microsoft.com/tr-tr/azure/devops/server/?view=azure-devops)
> - [Azure DevOps Services](https://learn.microsoft.com/tr-tr/azure/devops/?view=azure-devops)

---

### 3.6.1 Temel Tanımlar

1. **Azure DevOps Server**
   - **Tanım**: Önceden **Team Foundation Server (TFS)** olarak bilinen, şirket içi (on-premises) kurulumlar için tasarlanmış bir DevOps platformudur.
   - **Kullanım Alanı**: Güvenlik, uyumluluk veya veri yönetimi gibi nedenlerle bulut çözümlerini tercih etmeyen kurumsal şirketler tarafından kullanılır.

2. **Azure DevOps Services**
   - **Tanım**: Microsoft’un bulut tabanlı DevOps çözümüdür. Tamamen bulutta barındırılır ve internet üzerinden erişilir.
   - **Kullanım Alanı**: Esneklik, ölçeklenebilirlik ve hızlı kurulum gerektiren projeler için idealdir. Küçük ve orta ölçekli işletmelerden büyük kurumsal yapılar kadar geniş bir kullanıcı kitlesine hitap eder.

---

### 3.6.2 Dağıtım Modeli

| **Özellik**                     | **Azure DevOps Server**                                    | **Azure DevOps Services**                            |
|---------------------------------|------------------------------------------------------------|------------------------------------------------------|
| **Dağıtım**                     | Şirket içi (on-premises) sunucular üzerinde kurulur.        | Microsoft’un bulut altyapısı üzerinde barındırılır.   |
| **Bakım ve Güncellemeler**      | Kullanıcı tarafından yönetilir ve güncellenir.               | Microsoft tarafından otomatik olarak güncellenir.     |
| **Erişim**                      | Şirket içi ağlar veya VPN üzerinden erişim sağlanır.        | İnternet üzerinden her yerden erişilebilir.          |

---

### 3.6.3 Özellikler ve Entegrasyon

1. **Özellik Seti**
   - **Azure DevOps Server** ve **Azure DevOps Services**, temelde aynı temel özelliklere sahiptir: Boards, Repos, Pipelines, Test Plans ve Artifacts. Ancak, bazı ileri düzey özellikler ve entegrasyon seçenekleri sadece Azure DevOps Services’te bulunabilir.
   - **Bulut Özellikleri**: Azure DevOps Services, bulut tabanlı avantajlarından dolayı, yapay zeka destekli araçlar, daha hızlı entegrasyon güncellemeleri ve gelişmiş güvenlik özellikleri sunar.

2. **Entegrasyonlar**
   - **Azure DevOps Server**: Kurumsal iç sistemlerle (örneğin Active Directory) daha derin entegrasyon imkânı sağlar.
   - **Azure DevOps Services**: Diğer bulut hizmetleri ve üçüncü parti uygulamalarla daha geniş entegrasyon seçenekleri sunar. Örneğin, GitHub, Slack, Jira gibi popüler araçlarla kolay entegrasyon sağlanır.

---

### 3.6.4 Maliyet ve Lisanslama

1. **Azure DevOps Server**
   - **Lisanslama**: Sunucu tabanlı lisanslama modeli kullanır. Kullanıcı başına lisans gerektirir ve genellikle büyük kuruluşlar için maliyetli olabilir.
   - **Maliyet**: Kurulum ve bakım maliyetleri, donanım gereksinimleri ve lisans ücretleri dikkate alınmalıdır.
   - **Avantaj**: Büyük ölçekli ve karmaşık projeler için özelleştirilebilirlik sunar.

2. **Azure DevOps Services**
   - **Lisanslama**: Abonelik tabanlı fiyatlandırma modeli kullanır. Kullanıcı başına aylık veya yıllık ücretlendirme yapılır.
   - **Maliyet**: Başlangıçta düşük maliyetli olabilir ve kullanım arttıkça esnek bir şekilde ölçeklenebilir.
   - **Avantaj**: Küçük ve orta ölçekli işletmeler için uygun maliyetli çözümler sunar.

---

### 3.6.5 Güvenlik ve Uyum

1. **Azure DevOps Server**
   - **Veri Kontrolü**: Tüm veriler şirketin kendi altyapısında tutulduğu için, veri kontrolü ve gizliliği üzerinde tam hakimiyet sağlar.
   - **Uyum**: Özellikle GDPR, HIPAA gibi sıkı veri koruma standartlarına uyum sağlamak isteyen kurumlar için uygundur.

2. **Azure DevOps Services**
   - **Güvenlik**: Microsoft’un sağladığı bulut güvenlik önlemleri ve sürekli güncellenen güvenlik yamaları sayesinde yüksek güvenlik sunar.
   - **Uyum**: Microsoft, Azure DevOps Services’in birçok uluslararası uyum sertifikasına sahip olmasını sağlar, bu da global ölçekte uyum gereksinimleri olan şirketler için idealdir.

---

### 3.6.6 Performans ve Ölçeklenebilirlik

1. **Azure DevOps Server**
   - **Performans**: Şirketin kendi donanım kaynaklarına bağlıdır. Büyük projeler ve yüksek kullanım durumları için yeterli donanım yatırımı yapılması gerekebilir.
   - **Ölçeklenebilirlik**: Donanım kapasitesine bağlı olarak ölçeklendirilir. Daha fazla kaynak eklemek manuel bir süreç gerektirebilir.

2. **Azure DevOps Services**
   - **Performans**: Microsoft’un bulut altyapısı sayesinde yüksek performans ve düşük gecikme süreleri sunar.
   - **Ölçeklenebilirlik**: Otomatik olarak ölçeklenebilir, bu sayede talep arttıkça hizmetin performansı düşmez.

---

### 3.6.7 Yedekleme ve Felaket Kurtarma

1. **Azure DevOps Server**
   - **Yedekleme**: Şirketin kendi yedekleme stratejisini uygulaması gerekir. Yedeklemeler düzenli olarak yapılmalı ve güvenli bir şekilde saklanmalıdır.
   - **Felaket Kurtarma**: Şirketin kendi felaket kurtarma planını oluşturması ve uygulaması gerekir.

2. **Azure DevOps Services**
   - **Yedekleme**: Microsoft tarafından otomatik olarak yedeklenir ve veri kurtarma süreçleri yönetilir.
   - **Felaket Kurtarma**: Yüksek düzeyde felaket kurtarma desteği sunar; veri kaybı riski minimuma indirilmiştir.

---

### 3.6.8 Kullanım Senaryoları

1. **Azure DevOps Server**
   - **Güvenlik Gereksinimi Yüksek Kurumlar**: Verilerin kendi altyapısında saklanması gereken büyük finansal kurumlar, devlet daireleri ve sağlık kuruluşları.
   - **Özelleştirme İhtiyacı Olan Projeler**: Mevcut sistemlerle derin entegrasyon ve özel geliştirmeler gerektiren projeler.

2. **Azure DevOps Services**
   - **Hızlı Başlangıç Gerektiren Projeler**: Hızlı kurulum ve ölçeklenebilirlik isteyen start-up’lar ve küçük işletmeler.
   - **Dağıtık Takımlar**: Farklı coğrafi konumlarda çalışan ekipler için idealdir, çünkü internet üzerinden her yerden erişim sağlar.
   - **Esnek ve Dinamik Projeler**: Sürekli değişen gereksinimlere hızlıca uyum sağlaması gereken projeler.

---

### 3.6.9 Özet ve Seçim Kriterleri

| **Özellik**                  | **Azure DevOps Server**                                    | **Azure DevOps Services**                            |
|------------------------------|------------------------------------------------------------|------------------------------------------------------|
| **Dağıtım Modeli**           | On-premises                                                | Bulut (Cloud)                                        |
| **Bakım ve Güncellemeler**   | Kullanıcı tarafından yönetilir                              | Microsoft tarafından otomatik olarak yönetilir       |
| **Maliyet**                  | Yüksek başlangıç maliyeti, lisans ve donanım gerektirir    | Esnek abonelik modeli, düşük başlangıç maliyeti      |
| **Ölçeklenebilirlik**        | Donanım kaynaklarına bağlı olarak manuel ölçeklenir        | Otomatik ve esnek ölçeklenebilir                      |
| **Güvenlik ve Uyum**         | Tam veri kontrolü, yüksek uyum gereksinimleri için ideal   | Gelişmiş bulut güvenliği, geniş uyum sertifikaları    |
| **Entegrasyonlar**           | Kurumsal iç sistemlerle derin entegrasyon                  | Geniş bulut ve üçüncü parti entegrasyon seçenekleri    |
| **Yedekleme ve Kurtarma**   | Kullanıcı sorumluluğunda                                    |


## 4. Proje Tanıtımı

Bu bölümde, geliştirilecek olan **Basit Ürün Yönetimi Platformu** projesini detaylı bir şekilde tanıtacağız. Proje, temel ürün yönetimi işlevlerini gerçekleştiren, kullanıcı dostu bir arayüze sahip ve modern teknolojilerle inşa edilmiş bir uygulamadır. Aşağıda, projenin genel yapısı, kullanılan teknolojiler, mimarisi ve sunduğu özellikler hakkında bilgi bulabilirsiniz.

---

### 4.1 Proje Genel Görünümü

**Basit Ürün Yönetimi Platformu**, kullanıcıların ürünleri listeleyebildiği, yeni ürünler ekleyebildiği, mevcut ürünleri düzenleyip silebildiği bir web uygulamasıdır. Bu platform, küçük ve orta ölçekli işletmelerin veya bireysel kullanıcıların ürün envanterlerini kolayca yönetmelerine olanak tanır. Proje, başlangıç aşamasında temel CRUD (Create, Read, Update, Delete) işlemlerini desteklerken, ilerleyen aşamalarda **authentication** ve **authorization** özellikleri ile güvenlik katmanı eklenmesi planlanmaktadır.

---

### 4.2 Kullanılan Teknolojiler

Proje, modern ve popüler teknolojiler kullanılarak geliştirilmiştir. Bu teknolojiler, uygulamanın performansını, ölçeklenebilirliğini ve bakımını kolaylaştırmayı amaçlamaktadır.

- **Backend: ASP.NET Core Web API (.NET 8)**
  - Yüksek performanslı, platformlar arası çalışabilen bir framework.
  - RESTful API’ler geliştirmek için ideal.
  
- **Frontend: Angular**
  - Google tarafından desteklenen, güçlü bir frontend framework’ü.
  - Tek sayfa uygulamaları (SPA) geliştirmek için kullanılır.
  
- **Veritabanı: SQL Server**
  - Güçlü ve güvenilir bir ilişkisel veritabanı yönetim sistemi.
  
- **ORM: Entity Framework Core**
  - .NET uygulamaları için nesne-ilişkisel eşleme (ORM) aracı.
  - Veritabanı işlemlerini kolaylaştırır ve kod ile veritabanı arasındaki bağı azaltır.
  
- **Diğer Teknolojiler:**
  - **Visual Studio 2022**: Geliştirme ortamı.
  - **Postman**: API test araçları.
  - **Git**: Versiyon kontrol sistemi.
  - **Azure DevOps**: CI/CD süreçleri ve proje yönetimi.

---

### 4.3 Mimari

Proje, **MVC (Model-View-Controller)** tasarım desenine dayalı olarak, katmanlı bir mimari ile inşa edilmiştir. Bu mimari, uygulamanın farklı bileşenlerinin birbirinden bağımsız olarak geliştirilmesini ve bakımını kolaylaştırır.

#### 4.3.1 Backend (ASP.NET Core Web API)

- **Controllers**: API uç noktalarını tanımlar ve istemciden gelen istekleri işler.
- **Services**: İş mantığını içerir ve veri işleme görevlerini üstlenir.
- **Repositories**: Veritabanı ile etkileşim kurar, CRUD işlemlerini gerçekleştirir.
- **Models**: Veritabanı varlıklarını ve veri transfer objelerini (DTO) tanımlar.

#### 4.3.2 Frontend (Angular)

- **Components**: Kullanıcı arayüzünün parçalarını oluşturur.
- **Services**: API ile iletişimi sağlar, veri işlemlerini yönetir.
- **Modules**: Uygulamanın farklı bölümlerini organize eder.
- **Routing**: Uygulama içinde sayfalar arası geçişleri yönetir.

#### 4.3.3 Veritabanı (SQL Server)

- **Tables**: Ürün bilgilerini saklamak için tablolar oluşturulur.
- **Relationships**: Tablolar arasında ilişkiler tanımlanır.
- **Stored Procedures**: Veri işlemlerini optimize etmek için kullanılır.

---

### 4.4 Özellikler

Proje, kullanıcıların ürün yönetimi süreçlerini etkili bir şekilde gerçekleştirebilmeleri için çeşitli özellikler sunmaktadır.

#### 4.4.1 Ürün Listeleme

- **Açıklama**: Kullanıcılar, mevcut tüm ürünleri listeleyebilir.
- **Özellikler**:
  - Ürün adı, açıklaması, fiyatı ve stok durumu gibi bilgiler görüntülenir.
  - Arama ve filtreleme seçenekleri ile ürünler kolayca bulunabilir.

#### 4.4.2 Yeni Ürün Ekleme

- **Açıklama**: Kullanıcılar, yeni ürünler ekleyebilir.
- **Özellikler**:
  - Ürün adı, açıklaması, fiyatı, kategorisi ve stok miktarı gibi alanlar doldurulur.
  - Form doğrulama ile eksik veya hatalı bilgilerin girilmesi engellenir.

#### 4.4.3 Ürün Düzenleme

- **Açıklama**: Kullanıcılar, mevcut ürünlerin bilgilerini güncelleyebilir.
- **Özellikler**:
  - Mevcut ürün bilgileri önceden doldurulur ve kullanıcı tarafından güncellenebilir.
  - Değişiklikler kaydedildiğinde, veritabanında güncelleme yapılır.

#### 4.4.4 Ürün Silme

- **Açıklama**: Kullanıcılar, artık ihtiyaç duymadıkları ürünleri silebilir.
- **Özellikler**:
  - Ürün silme işlemi onaylanmadan gerçekleştirilmez.
  - Silinen ürünler veritabanından kaldırılır ve listeden çıkarılır.

---

### 4.5 Gelecek Aşamalar ve Geliştirmeler

Projenin ilk aşamasında temel ürün yönetimi işlevleri geliştirildikten sonra, ilerleyen dönemlerde aşağıdaki ek özellikler ve geliştirmeler planlanmaktadır:

- **Authentication/Authorization**: Kullanıcıların kimlik doğrulama ve yetkilendirme süreçlerinin eklenmesi.
- **Rol Tabanlı Erişim Kontrolü**: Farklı kullanıcı rolleri için erişim izinlerinin tanımlanması.
- **Gelişmiş Raporlama**: Ürün satışları, stok durumu gibi alanlarda detaylı raporlar oluşturulması.
- **Entegrasyonlar**: Diğer sistemlerle (örneğin, ödeme sistemleri, CRM) entegrasyonların sağlanması.
- **Responsive Tasarım**: Uygulamanın mobil cihazlarda da sorunsuz çalışacak şekilde optimize edilmesi.
- **Performans Optimizasyonları**: Uygulamanın performansını artırmak için optimizasyon çalışmaları yapılması.

---

**Basit Ürün Yönetimi Platformu** projesi, modern yazılım geliştirme metodolojileri ve DevOps prensipleri doğrultusunda tasarlanmış, esnek ve ölçeklenebilir bir yapıya sahiptir. Bu proje üzerinden gerçekleştirilecek laboratuvar çalışmaları ile DevOps araçlarının ve süreçlerinin pratikte nasıl kullanılacağını öğrenmek mümkün olacaktır.

---

## 5. Azure DevOps Lab'ları

Bu bölümde, **Basit Ürün Yönetimi Platformu** projesini Azure DevOps üzerinde adım adım kurarak, DevOps süreçlerini pratikte nasıl uygulayacağınızı öğreneceksiniz. Her laboratuvar çalışması, projeyi oluşturma, yapılandırma ve geliştirme sürecinin farklı aşamalarını kapsayacak şekilde tasarlanmıştır.

### 5.1 Lab-1: Azure DevOps'ta Yeni Bir Team Project Oluşturma

Bu laboratuvar çalışmasında, **Azure DevOps** üzerinde yeni bir takım projesi oluşturacağız. Projemizin adı `ProductManagement` olacak ve süreç şablonu olarak **Scrum** kullanılacaktır. Aşağıdaki adımları takip ederek projenizi başarıyla oluşturabilirsiniz.

#### 5.1.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Azure DevOps Hesabı**: [Azure DevOps](https://dev.azure.com/) üzerinde bir hesabınız olmalı.
- **Giriş Bilgileri**: Azure DevOps hesabınıza giriş yapabileceğiniz kullanıcı adı ve şifreniz olmalı.
- **İnternet Bağlantısı**: Azure DevOps web arayüzüne erişmek için stabil bir internet bağlantısı gereklidir.

#### 5.1.2 Adım 1: Azure DevOps'a Giriş Yapma

1. **Azure DevOps Web Sitesine Gidin**
   - Tarayıcınızda [Azure DevOps](https://dev.azure.com/) web sitesini açın.

2. **Giriş Yapın**
   - Sağ üst köşede bulunan **"Sign in"** butonuna tıklayın.
   - Microsoft hesabınızla giriş yapın. Eğer bir hesabınız yoksa, **"Create one!"** seçeneğiyle yeni bir hesap oluşturabilirsiniz.

#### 5.1.3 Adım 2: Yeni Bir Team Project Oluşturma

1. **Azure DevOps Ana Sayfasına Erişim**
   - Giriş yaptıktan sonra, Azure DevOps ana sayfasına yönlendirileceksiniz. Burada mevcut projelerinizi görebilir veya yeni bir proje oluşturabilirsiniz.

2. **Yeni Proje Oluşturma**
   - **"New Project"** butonuna tıklayın. Bu buton genellikle ana sayfanın sağ üst köşesinde bulunur.

3. **Proje Detaylarını Girin**
   - Açılan formda aşağıdaki bilgileri doldurun:
     - **Project Name (Proje Adı)**: `ProductManagement`
     - **Description (Açıklama)**: *(Opsiyonel)* `Basit Ürün Yönetimi Platformu projesi için Scrum süreç şablonu kullanılarak oluşturulan takım projesi.`
     - **Visibility (Görünürlük)**:
       - **Private**: Sadece davet edilen üyeler projeyi görebilir ve erişebilir.
       - **Public**: Herkes projeyi görebilir. *(Güvenlik ve gizlilik gereksinimlerinize bağlı olarak seçin.)*
     - **Advanced (Gelişmiş)**:
       - **Version Control (Versiyon Kontrolü)**: `Git` seçili olduğundan emin olun.
       - **Work Item Process (İş Öğesi Süreci)**: `Scrum` şablonunu seçin.

4. **Proje Oluşturma**
   - Tüm bilgileri doldurduktan sonra, **"Create"** butonuna tıklayarak projeyi oluşturun.

#### 5.1.4 Adım 3: Proje Ayarlarını Kontrol Etme

1. **Proje Ana Sayfasına Gidin**
   - Proje oluşturulduktan sonra, otomatik olarak oluşturduğunuz `ProductManagement` projesinin ana sayfasına yönlendirileceksiniz.

2. **Process Şablonunun Doğrulanması**
   - Sol menüden **"Project settings"** (Proje Ayarları) seçeneğine tıklayın.
   - **"Overview"** altında, **"Process"** bölümünü kontrol edin. Süreç şablonunun **Scrum** olarak ayarlandığından emin olun.


#### 5.1.5 Adım 4: Projeyi Tanıma ve Giriş

1. **Boards, Repos, Pipelines, Test Plans, Artifacts Sekmelerini İnceleme**
   - Proje ana sayfasında, sol tarafta yer alan sekmelerden **Boards**, **Repos**, **Pipelines**, **Test Plans** ve **Artifacts** gibi DevOps araçlarına erişebilirsiniz.

2. **Boards Sekmesine Göz Atma**
   - **Boards** sekmesi altında, iş öğeleri (Work Items), backlog, sprintler ve panolar (boards) gibi proje yönetimi araçlarını bulabilirsiniz.
   - Scrum süreç şablonunu kullandığınız için, burada **Epics**, **Features**, **Product Backlog Items (PBI)** ve **Tasks** gibi iş öğelerini yönetebileceksiniz.

3. **Repos Sekmesine Göz Atma**
   - **Repos** sekmesi, projenizin Git depolarını yönetmenize olanak tanır.
   - Başlangıçta boş bir depo oluşturduğunuz için, burada README dosyanızı görüntüleyebilir veya yeni branch'ler oluşturabilirsiniz.

4. **Pipelines Sekmesine Göz Atma**
   - **Pipelines** sekmesi, CI/CD süreçlerinizi oluşturup yönetebileceğiniz alandır.
   - Henüz pipeline oluşturmadığınız için bu bölümde "No pipelines found" mesajı görebilirsiniz.

5. **Test Plans ve Artifacts Sekmelerini İnceleme**
   - **Test Plans** sekmesi, manuel ve otomatik test süreçlerinizi yönetmenizi sağlar.
   - **Artifacts** sekmesi, projelerinizde kullanacağınız paketleri (NuGet, npm, Maven vb.) yönetmenize olanak tanır.

### 5.1.6 Lab-1'in Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak, Azure DevOps üzerinde `ProductManagement` adlı yeni bir takım projesi oluşturmuş oldunuz. Projeyi Scrum süreç şablonu ile yapılandırdınız ve temel DevOps araçlarına göz attınız. Bir sonraki laboratuvar çalışmasında, backlog öğelerini tanımlamaya, sprint planlaması yapmaya ve Git reposu oluşturma adımlarına geçeceğiz.

---

## 5.2 Lab-2: Epic, Feature, PBI ve Task'ları Ayrı Ayrı Oluşturma

Bu laboratuvar çalışmasında, **ProductManagement** projesi için **Epic**, **Feature**, **Product Backlog Item (PBI)** ve **Task** öğelerini ayrı ayrı oluşturacağız. Bu adımlar, Scrum metodolojisi kapsamında iş öğelerini hiyerarşik olarak organize etmenizi sağlayacak ve proje yönetimini kolaylaştıracaktır. Ayrıca, her bir temel işlev (listeleme, ekleme, düzenleme, silme) için ayrı iş öğeleri oluşturarak daha detaylı bir yapı kuracağız.

### 5.2.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Lab-1'in Tamamlanması**: Azure DevOps üzerinde `ProductManagement` adlı takım projesini başarıyla oluşturmuş olun.
- **Giriş Bilgileri**: Azure DevOps hesabınıza erişim sağlayabilecek kullanıcı adı ve şifreniz olmalı.
- **İnternet Bağlantısı**: Azure DevOps web arayüzüne erişmek için stabil bir internet bağlantısı gereklidir.

### 5.2.2 Adım 1: Boards'a Erişim ve Backlog Görünümüne Geçiş

1. **Azure DevOps'a Giriş Yapın**
   - [Azure DevOps](https://dev.azure.com/) hesabınıza giriş yapın ve `ProductManagement` projesini seçin.

2. **Boards Sekmesine Gidin**
   - Sol taraftaki menüden **"Boards"** sekmesine tıklayın.

3. **Backlog Görünümünü Açın**
   - **Boards** menüsünden **"Backlogs"** seçeneğine tıklayın. Bu sayede projenizin backlog'unu görebilir ve yönetebilirsiniz.

### 5.2.3 Adım 2: Epic Oluşturma

**Epic**, büyük ve geniş kapsamlı iş öğelerini temsil eder. Projenizin ana hedeflerini veya önemli işlevlerini kapsar.

1. **Yeni Epic Ekleyin**
   - Backlog listesinin üst kısmında bulunan **"New Work Item"** butonuna tıklayın ve **"Epic"** seçeneğini seçin.

2. **Epic Detaylarını Girin**
   - **Title (Başlık)**: `Ürün Yönetimi Modülü`
   - **Description (Açıklama)**: `Ürünlerin listelenmesi, eklenmesi, düzenlenmesi ve silinmesi işlevlerini içeren modül.`
   - **Save** butonuna tıklayarak Epic'i oluşturun.

### 5.2.4 Adım 3: Feature Oluşturma

**Feature**, bir Epic'in altında yer alan ve belirli bir işlevselliği temsil eden daha küçük iş öğeleridir.

1. **Yeni Feature Ekleyin**
   - Oluşturduğunuz **Epic**'e tıklayın.
   - **"Add"** butonuna tıklayarak yeni bir **Feature** ekleyin.

2. **Feature Detaylarını Girin**
   - **Title (Başlık)**: `Ürün İşlemleri`
   - **Description (Açıklama)**: `Ürünlerin listelenmesi, eklenmesi, düzenlenmesi ve silinmesi işlevlerini kapsayan özellikler.`
   - **Save** butonuna tıklayarak Feature'ı oluşturun.

### 5.2.5 Adım 4: Product Backlog Item (PBI) Oluşturma

**Product Backlog Item (PBI)**, kullanıcı hikayelerini veya ürün gereksinimlerini temsil eden iş öğeleridir. Her PBI, belirli bir işlevin veya özelliğin geliştirilmesini sağlar. Bu adımda, her temel işlev için ayrı PBI'lar oluşturacağız.

#### 1. **Ürün Listeleme PBI'si Oluşturma**

1. **Yeni PBI Ekleyin**
   - Oluşturduğunuz **Feature**'ın altında, **"Add"** butonuna tıklayarak yeni bir **PBI** ekleyin.

2. **PBI Detaylarını Girin**
   - **Title (Başlık)**: `Ürünleri Listelenebilir Hale Getirme`
   - **Description (Açıklama)**: `Veritabanından ürün verilerini çekip arayüzde listelemek için gerekli API ve frontend bileşenlerini oluşturmak.`
   - **Acceptance Criteria (Kabul Kriterleri)**:
     - Ürün listesi, ürün adı, açıklaması, fiyatı ve stok durumunu içermelidir.
     - Arayüzde sayfalama ve arama özellikleri bulunmalıdır.
   - **Save** butonuna tıklayarak PBI'yi oluşturun.

#### 2. **Ürün Ekleme PBI'si Oluşturma**

1. **Yeni PBI Ekleyin**
   - **Feature** altında **"Add"** butonuna tıklayarak yeni bir **PBI** ekleyin.

2. **PBI Detaylarını Girin**
   - **Title (Başlık)**: `Yeni Ürün Eklenebilir Hale Getirme`
   - **Description (Açıklama)**: `Kullanıcıların yeni ürünler ekleyebilmesi için gerekli API ve frontend bileşenlerini oluşturmak.`
   - **Acceptance Criteria (Kabul Kriterleri)**:
     - Ürün ekleme formu, ürün adı, açıklaması, fiyatı ve stok miktarı gibi alanları içermelidir.
     - Form doğrulama ile eksik veya hatalı bilgilerin girilmesi engellenmelidir.
   - **Save** butonuna tıklayarak PBI'yi oluşturun.

#### 3. **Ürün Düzenleme PBI'si Oluşturma**

1. **Yeni PBI Ekleyin**
   - **Feature** altında **"Add"** butonuna tıklayarak yeni bir **PBI** ekleyin.

2. **PBI Detaylarını Girin**
   - **Title (Başlık)**: `Ürün Düzenlenebilir Hale Getirme`
   - **Description (Açıklama)**: `Kullanıcıların mevcut ürünlerin bilgilerini güncelleyebilmesi için gerekli API ve frontend bileşenlerini oluşturmak.`
   - **Acceptance Criteria (Kabul Kriterleri)**:
     - Mevcut ürün bilgileri önceden doldurulmuş şekilde gösterilmelidir.
     - Kullanıcılar, bilgileri güncelleyip kaydedebilmelidir.
   - **Save** butonuna tıklayarak PBI'yi oluşturun.

#### 4. **Ürün Silme PBI'si Oluşturma**

1. **Yeni PBI Ekleyin**
   - **Feature** altında **"Add"** butonuna tıklayarak yeni bir **PBI** ekleyin.

2. **PBI Detaylarını Girin**
   - **Title (Başlık)**: `Ürün Silinebilir Hale Getirme`
   - **Description (Açıklama)**: `Kullanıcıların mevcut ürünleri silebilmesi için gerekli API ve frontend bileşenlerini oluşturmak.`
   - **Acceptance Criteria (Kabul Kriterleri)**:
     - Ürün silme işlemi onaylanmadan gerçekleştirilmemelidir.
     - Silinen ürünler veritabanından kaldırılmalı ve listeden çıkarılmalıdır.
   - **Save** butonuna tıklayarak PBI'yi oluşturun.

### 5.2.6 Adım 5: Task Oluşturma

Her bir **PBI** için gerekli olan **Task**'ları oluşturacağız. Bu adımda, her temel işlevin gerçekleştirilmesi için spesifik görevler tanımlayacağız.

#### 1. **Ürünleri Listelenebilir Hale Getirme için Task'lar**

##### a. Backend API Oluşturma

1. **Yeni Task Ekleyin**
   - `Ürünleri Listelenebilir Hale Getirme` PBI'sine tıklayın.
   - **"Add"** butonuna tıklayarak yeni bir **Task** ekleyin.

2. **Task Detaylarını Girin**
   - **Title (Başlık)**: `Backend API Oluşturma`
   - **Description (Açıklama)**: `ASP.NET Core Web API kullanarak ürünleri listeleyen endpoint oluşturmak.`
   - **Save** butonuna tıklayarak Task'ı oluşturun.

##### b. Frontend Ürün Listesi Oluşturma

1. **Yeni Task Ekleyin**
   - Aynı **PBI** altında **"Add"** butonuna tıklayarak yeni bir **Task** ekleyin.

2. **Task Detaylarını Girin**
   - **Title (Başlık)**: `Frontend Ürün Listesi Oluşturma`
   - **Description (Açıklama)**: `Angular kullanarak ürünlerin listelendiği bileşeni oluşturmak.`
   - **Save** butonuna tıklayarak Task'ı oluşturun.

##### c. Veritabanı Tablolarını Oluşturma

1. **Yeni Task Ekleyin**
   - Aynı **PBI** altında **"Add"** butonuna tıklayarak yeni bir **Task** ekleyin.

2. **Task Detaylarını Girin**
   - **Title (Başlık)**: `Veritabanı Tablolarını Oluşturma`
   - **Description (Açıklama)**: `SQL Server üzerinde gerekli tabloları ve ilişkileri tanımlamak.`
   - **Save** butonuna tıklayarak Task'ı oluşturun.

#### 2. **Yeni Ürün Eklenebilir Hale Getirme için Task'lar**

##### a. Backend API Oluşturma

1. **Yeni Task Ekleyin**
   - `Yeni Ürün Eklenebilir Hale Getirme` PBI'sine tıklayın.
   - **"Add"** butonuna tıklayarak yeni bir **Task** ekleyin.

2. **Task Detaylarını Girin**
   - **Title (Başlık)**: `Backend API Oluşturma`
   - **Description (Açıklama)**: `ASP.NET Core Web API kullanarak yeni ürün ekleme endpoint'i oluşturmak.`
   - **Save** butonuna tıklayarak Task'ı oluşturun.

##### b. Frontend Ürün Ekleme Formu Oluşturma

1. **Yeni Task Ekleyin**
   - Aynı **PBI** altında **"Add"** butonuna tıklayarak yeni bir **Task** ekleyin.

2. **Task Detaylarını Girin**
   - **Title (Başlık)**: `Frontend Ürün Ekleme Formu Oluşturma`
   - **Description (Açıklama)**: `Angular kullanarak yeni ürün eklemek için form bileşenini oluşturmak.`
   - **Save** butonuna tıklayarak Task'ı oluşturun.

##### c. Form Doğrulama Eklemek

1. **Yeni Task Ekleyin**
   - Aynı **PBI** altında **"Add"** butonuna tıklayarak yeni bir **Task** ekleyin.

2. **Task Detaylarını Girin**
   - **Title (Başlık)**: `Form Doğrulama Eklemek`
   - **Description (Açıklama)**: `Ürün ekleme formunda gerekli alanlar için doğrulama kuralları eklemek.`
   - **Save** butonuna tıklayarak Task'ı oluşturun.

#### 3. **Ürün Düzenlenebilir Hale Getirme için Task'lar**

##### a. Backend API Oluşturma

1. **Yeni Task Ekleyin**
   - `Ürün Düzenlenebilir Hale Getirme` PBI'sine tıklayın.
   - **"Add"** butonuna tıklayarak yeni bir **Task** ekleyin.

2. **Task Detaylarını Girin**
   - **Title (Başlık)**: `Backend API Oluşturma`
   - **Description (Açıklama)**: `ASP.NET Core Web API kullanarak ürün düzenleme endpoint'i oluşturmak.`
   - **Save** butonuna tıklayarak Task'ı oluşturun.

##### b. Frontend Ürün Düzenleme Formu Oluşturma

1. **Yeni Task Ekleyin**
   - Aynı **PBI** altında **"Add"** butonuna tıklayarak yeni bir **Task** ekleyin.

2. **Task Detaylarını Girin**
   - **Title (Başlık)**: `Frontend Ürün Düzenleme Formu Oluşturma`
   - **Description (Açıklama)**: `Angular kullanarak mevcut ürün bilgilerini düzenlemek için form bileşenini oluşturmak.`
   - **Save** butonuna tıklayarak Task'ı oluşturun.

##### c. Form Doğrulama ve Güncelleme İşlemleri

1. **Yeni Task Ekleyin**
   - Aynı **PBI** altında **"Add"** butonuna tıklayarak yeni bir **Task** ekleyin.

2. **Task Detaylarını Girin**
   - **Title (Başlık)**: `Form Doğrulama ve Güncelleme İşlemleri`
   - **Description (Açıklama)**: `Ürün düzenleme formunda gerekli alanlar için doğrulama kuralları eklemek ve güncelleme işlemlerini gerçekleştirmek.`
   - **Save** butonuna tıklayarak Task'ı oluşturun.

#### 4. **Ürün Silinebilir Hale Getirme için Task'lar**

##### a. Backend API Oluşturma

1. **Yeni Task Ekleyin**
   - `Ürün Silinebilir Hale Getirme` PBI'sine tıklayın.
   - **"Add"** butonuna tıklayarak yeni bir **Task** ekleyin.

2. **Task Detaylarını Girin**
   - **Title (Başlık)**: `Backend API Oluşturma`
   - **Description (Açıklama)**: `ASP.NET Core Web API kullanarak ürün silme endpoint'i oluşturmak.`
   - **Save** butonuna tıklayarak Task'ı oluşturun.

##### b. Frontend Ürün Silme İşlevi Oluşturma

1. **Yeni Task Ekleyin**
   - Aynı **PBI** altında **"Add"** butonuna tıklayarak yeni bir **Task** ekleyin.

2. **Task Detaylarını Girin**
   - **Title (Başlık)**: `Frontend Ürün Silme İşlevi Oluşturma`
   - **Description (Açıklama)**: `Angular kullanarak ürünleri silmek için gerekli bileşen ve işlevleri oluşturmak.`
   - **Save** butonuna tıklayarak Task'ı oluşturun.

##### c. Silme İşlemi Onayı Eklemek

1. **Yeni Task Ekleyin**
   - Aynı **PBI** altında **"Add"** butonuna tıklayarak yeni bir **Task** ekleyin.

2. **Task Detaylarını Girin**
   - **Title (Başlık)**: `Silme İşlemi Onayı Eklemek`
   - **Description (Açıklama)**: `Kullanıcıların yanlışlıkla silme yapmasını önlemek için onay diyaloğu eklemek.`
   - **Save** butonuna tıklayarak Task'ı oluşturun.

### 5.2.7 Adım 6: Backlog Hiyerarşisini İnceleme

Oluşturduğunuz **Epic**, **Feature**, **PBI** ve **Task**'ların hiyerarşik yapısını kontrol ederek, iş öğelerinin doğru bir şekilde organize edildiğinden emin olun.

1. **Backlog'da Hiyerarşi Kontrolü**
   - **Boards > Backlogs** sekmesinde, sol tarafta oluşturduğunuz **Epic**'i genişleterek altındaki **Feature**, **PBI** ve **Task**'ları görüntüleyin.

2. **Gerekirse Düzenleme Yapın**
   - Yanlış yerleştirilmiş iş öğelerini sürükle-bırak yöntemiyle doğru konuma taşıyabilirsiniz.
   - **PBI**'lere veya **Feature**'lara ek açıklamalar ekleyerek iş öğelerini daha ayrıntılı hale getirebilirsiniz.

### 5.2.8 Örnek Hiyerarşi

Aşağıda, oluşturduğunuz **Epic** altında nasıl bir hiyerarşi oluşturduğunuza dair bir örnek verilmiştir:

- **Epic**: `Ürün Yönetimi Modülü`
  - **Feature**: `Ürün İşlemleri`
    - **PBI**: `Ürünleri Listelenebilir Hale Getirme`
      - **Task**: `Backend API Oluşturma`
      - **Task**: `Frontend Ürün Listesi Oluşturma`
      - **Task**: `Veritabanı Tablolarını Oluşturma`
    - **PBI**: `Yeni Ürün Eklenebilir Hale Getirme`
      - **Task**: `Backend API Oluşturma`
      - **Task**: `Frontend Ürün Ekleme Formu Oluşturma`
      - **Task**: `Form Doğrulama Eklemek`
    - **PBI**: `Ürün Düzenlenebilir Hale Getirme`
      - **Task**: `Backend API Oluşturma`
      - **Task**: `Frontend Ürün Düzenleme Formu Oluşturma`
      - **Task**: `Form Doğrulama ve Güncelleme İşlemleri`
    - **PBI**: `Ürün Silinebilir Hale Getirme`
      - **Task**: `Backend API Oluşturma`
      - **Task**: `Frontend Ürün Silme İşlevi Oluşturma`
      - **Task**: `Silme İşlemi Onayı Eklemek`

### 5.2.9 Lab-2'nin Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak, `ProductManagement` projesi için **Epic**, **Feature**, **PBI** ve **Task** iş öğelerini başarıyla ayrı ayrı oluşturmuş oldunuz. Her temel işlev için ayrı PBI'lar ve bunlara bağlı Task'lar oluşturarak, projenizin iş akışını daha detaylı ve yönetilebilir hale getirdiniz. Bir sonraki laboratuvar çalışmasında, sprint oluşturma ve iş öğelerini sprint'e atama adımlarını gerçekleştireceğiz.

---

## 5.3 Lab-3: Yeni Bir Sprint Oluşturma ve Task'ları İlgili Sprint'e Atama

Bu laboratuvar çalışmasında, **ProductManagement** projesi için yeni bir sprint oluşturacak ve oluşturduğunuz **Task**'ları bu sprint'e atayacaksınız. Bu adımlar, Scrum metodolojisi kapsamında sprint planlamasını gerçekleştirmenizi ve iş öğelerinin sprint'e dahil edilmesini sağlayacaktır.

### 5.3.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Lab-1'in Tamamlanması**: Azure DevOps üzerinde `ProductManagement` adlı takım projesini başarıyla oluşturmuş olun.
- **Lab-2'nin Tamamlanması**: Epic, Feature, PBI ve Task'ları başarıyla oluşturmuş olun.
- **Giriş Bilgileri**: Azure DevOps hesabınıza erişim sağlayabilecek kullanıcı adı ve şifreniz olmalı.
- **İnternet Bağlantısı**: Azure DevOps web arayüzüne erişmek için stabil bir internet bağlantısı gereklidir.

### 5.3.2 Adım 1: Boards Sekmesine Giriş ve Sprint Görünümüne Geçiş

1. **Azure DevOps'a Giriş Yapın**
   - [Azure DevOps](https://dev.azure.com/) hesabınıza giriş yapın ve `ProductManagement` projesini seçin.

2. **Boards Sekmesine Gidin**
   - Sol taraftaki menüden **"Boards"** sekmesine tıklayın.

3. **Sprints Görünümüne Geçiş Yapın**
   - **Boards** menüsünden **"Sprints"** seçeneğine tıklayın. Bu sayede mevcut sprint'lerinizi görebilir ve yeni sprint'ler oluşturabilirsiniz.

### 5.3.3 Adım 2: Yeni Bir Sprint Oluşturma

1. **Yeni Sprint Ekleme**
   - **Sprints** sayfasında, sağ üst köşede bulunan **"New Sprint"** butonuna tıklayın.

2. **Sprint Detaylarını Girin**
   - **Sprint Name (Sprint Adı)**: `Sprint 1`
   - **Start Date (Başlangıç Tarihi)**: Projenizin zaman çizelgesine uygun bir başlangıç tarihi belirleyin.
   - **End Date (Bitiş Tarihi)**: Sprint süresini belirleyin (genellikle 2-4 hafta arası).
   - **Add Sprint** butonuna tıklayarak sprint'i oluşturun.

3. **Sprint'in Doğrulanması**
   - Oluşturduğunuz `Sprint 1`'in **Sprints** listesindeki yerini kontrol edin ve doğru tarihlerle oluşturulduğundan emin olun.

### 5.3.4 Adım 3: Task'ları Sprint'e Atama

1. **Backlogs Sekmesine Geri Dönün**
   - Sol menüden **"Boards"** sekmesine, ardından **"Backlogs"** seçeneğine tıklayın.

2. **Sprint 1'e Geçiş Yapın**
   - Backlog görünümünde, sağ üst köşede bulunan **"Iteration Path"** dropdown menüsünden `Sprint 1`'i seçin. Bu, backlog öğelerinizin sadece `Sprint 1` için filtrelenmesini sağlar.

3. **Task'ları Sprint'e Sürükleyip Bırakma**
   - Oluşturduğunuz **Task**'ları sprint'e atamak için aşağıdaki adımları izleyin:
     - Backlog listesinde yer alan **Task**'ları bulun.
     - Her bir **Task**'ı seçin ve sürükleyip `Sprint 1` kutusuna bırakın.
     - Alternatif olarak, **Task**'ın üzerine gelip açılan detay panelinde **"Iteration Path"** alanını `Sprint 1` olarak değiştirin.

4. **Atanan Task'ları Doğrulama**
   - `Sprint 1`'e atadığınız tüm **Task**'ların doğru şekilde eklendiğinden emin olmak için **Sprints** sekmesine geri dönün.
   - **Sprint 1**'i seçin ve atanmış **Task**'ların listelendiğini doğrulayın.

### 5.3.5 Adım 4: Sprint'in Durumunu İzleme

1. **Sprint Board'u İnceleme**
   - **Sprints** sekmesinde, `Sprint 1`'i seçin.
   - **Sprint Board** üzerinde, **Task**'ların durumlarını (To Do, In Progress, Done) takip edebilirsiniz.
   - **Task**'ların ilerleme durumlarına göre board üzerinde sürükle-bırak yöntemiyle taşınmasını sağlayın.

2. **Burndown Chart Görüntüleme**
   - **Sprints** sekmesinde, `Sprint 1`'i seçtikten sonra, sağ üst köşede bulunan **"Burndown"** sekmesine tıklayın.
   - Burndown chart, sprint süresince tamamlanan iş miktarını görsel olarak takip etmenizi sağlar.

### 5.3.6 Adım 5: Sprint Planlaması ve Takip

1. **Sprint Hedeflerini Belirleme**
   - `Sprint 1` için belirlediğiniz **Feature**, **PBI** ve **Task**'ları gözden geçirerek sprint hedeflerinizi netleştirin.
   - Hangi **Task**'ların öncelikli olduğunu ve sprint süresince tamamlanması gerekenleri belirleyin.

2. **Daily Stand-up Toplantıları**
   - Sprint süresince günlük kısa toplantılar düzenleyerek ekip üyelerinin ilerlemelerini, karşılaştıkları engelleri ve günlük hedeflerini paylaşmalarını sağlayın.
   - **Sprint Board** üzerindeki **Task**'ların güncel durumlarını takip edin ve gerektiğinde yeniden önceliklendirme yapın.

3. **Sprint İncelemesi ve Retrospektif**
   - Sprint sonunda, tamamlanan işlerin gözden geçirilmesi için bir sprint inceleme toplantısı düzenleyin.
   - Sprint sürecinde nelerin iyi gittiğini, nelerin geliştirilmesi gerektiğini belirlemek için retrospektif toplantısı yapın.

### 5.3.7 Lab-3'ün Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak, `ProductManagement` projesi için yeni bir sprint oluşturmuş ve mevcut **Task**'ları bu sprint'e başarıyla atamış oldunuz. Sprint planlaması ve takip süreçlerini uygulayarak, proje yönetimini daha düzenli ve verimli hale getirdiniz. Bir sonraki laboratuvar çalışmasında, backend ve frontend için Git reposu oluşturma adımlarını gerçekleştireceğiz.

---

## 5.4 Lab-4: Backend ve UI İçin Git Repolarını Oluşturma

Bu laboratuvar çalışmasında, **ProductManagement** projesi için **Backend** ve **UI** olmak üzere iki ayrı Git repoları oluşturacağız. Bu adımlar, projenizin backend ve frontend bileşenlerini bağımsız olarak yönetmenizi ve sürüm kontrolünü etkin bir şekilde gerçekleştirmenizi sağlayacaktır.

### 5.4.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Lab-1'in Tamamlanması**: Azure DevOps üzerinde `ProductManagement` adlı takım projesini başarıyla oluşturmuş olun.
- **Lab-2'nin Tamamlanması**: Epic, Feature, PBI ve Task'ları başarıyla oluşturmuş olun.
- **Lab-3'ün Tamamlanması**: Sprint oluşturmuş ve Task'ları sprint'e atamış olun.
- **Giriş Bilgileri**: Azure DevOps hesabınıza erişim sağlayabilecek kullanıcı adı ve şifreniz olmalı.
- **İnternet Bağlantısı**: Azure DevOps web arayüzüne erişmek için stabil bir internet bağlantısı gereklidir.

### 5.4.2 Adım 1: Repos Sekmesine Erişim

1. **Azure DevOps'a Giriş Yapın**
   - [Azure DevOps](https://dev.azure.com/) hesabınıza giriş yapın ve `ProductManagement` projesini seçin.

2. **Repos Sekmesine Gidin**
   - Sol taraftaki menüden **"Repos"** sekmesine tıklayın. Bu sekme, projelerinizin Git repolarını yönetmenize olanak tanır.

### 5.4.3 Adım 2: Backend Reposu Oluşturma

1. **Yeni Repository Oluşturma**
   - **Repos** sekmesinde, sağ üst köşede bulunan **"New repository"** butonuna tıklayın.

2. **Repository Detaylarını Girin**
   - **Repository Name (Depo Adı)**: `Backend`
   - **Add a README**: `Initialize with a README` seçeneğini işaretleyin. Bu, depo oluşturulduğunda bir README dosyası ile başlatılmasını sağlar.
   - **Create** butonuna tıklayarak **Backend** reposunu oluşturun.

3. **Backend Reposunun Doğrulanması**
   - Oluşturulan **Backend** reposunun ana sayfasına yönlendirileceksiniz. Burada README dosyasını görüntüleyebilir ve depo hakkında bilgi edinebilirsiniz.

### 5.4.4 Adım 3: UI Reposu Oluşturma

1. **Yeni Repository Oluşturma**
   - **Repos** sekmesinde, tekrar sağ üst köşede bulunan **"New repository"** butonuna tıklayın.

2. **Repository Detaylarını Girin**
   - **Repository Name (Depo Adı)**: `UI`
   - **Add a README**: `Initialize with a README` seçeneğini işaretleyin.
   - **Create** butonuna tıklayarak **UI** reposunu oluşturun.

3. **UI Reposunun Doğrulanması**
   - Oluşturulan **UI** reposunun ana sayfasına yönlendirileceksiniz. Burada README dosyasını görüntüleyebilir ve depo hakkında bilgi edinebilirsiniz.

### 5.4.5 Adım 4: Repoların Doğrulanması

1. **Backend Reposunu Kontrol Etme**
   - Azure DevOps üzerindeki **Backend** reposuna geri dönün.
   - `README.md` dosyasının doğru şekilde oluşturulduğunu ve depo hakkında gerekli bilgilerin bulunduğunu doğrulayın.

2. **UI Reposunu Kontrol Etme**
   - Azure DevOps üzerindeki **UI** reposuna geri dönün.
   - `README.md` dosyasının doğru şekilde oluşturulduğunu ve depo hakkında gerekli bilgilerin bulunduğunu doğrulayın.

### 5.4.6 Lab-4'ün Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak, `ProductManagement` projesi için **Backend** ve **UI** olmak üzere iki ayrı Git repolarını Azure DevOps üzerinde başarıyla oluşturmuş oldunuz. Bu repolar, projenizin backend ve frontend bileşenlerini bağımsız olarak yönetmenizi ve sürüm kontrolünü etkin bir şekilde gerçekleştirmenizi sağlayacaktır. Bir sonraki laboratuvar çalışmasında, backend reposunu klonlayarak projenizin temel yapısını oluşturma adımlarını gerçekleştireceğiz.

---

## 5.5 Lab-5: Backend İçin Git Repounu Visual Studio Kullanarak Klonlama, Yeni Bir Branch Açma ve Proje Yapısını Oluşturma

Bu laboratuvar çalışmasında, **ProductManagement** projesinin **Backend** reposunu Visual Studio kullanarak lokal makinenize klonlayacak, ana (main) branch'ten yeni bir branch oluşturacak ve temel proje yapısını kuracaksınız. Ardından, yaptığınız değişiklikleri commit ve push ederek bir Pull Request (PR) oluşturacak ve bu PR'ı main branch'e merge edeceksiniz. Bu adımlar, projenizin sürüm kontrolünü etkin bir şekilde yönetmenizi ve iş akışınızı düzenli tutmanızı sağlayacaktır.

### 5.5.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Lab-1'in Tamamlanması**: Azure DevOps üzerinde `ProductManagement` adlı takım projesini başarıyla oluşturmuş olun.
- **Lab-2'nin Tamamlanması**: Epic, Feature, PBI ve Task'ları başarıyla oluşturmuş olun.
- **Lab-3'ün Tamamlanması**: Sprint oluşturmuş ve Task'ları sprint'e atamış olun.
- **Lab-4'ün Tamamlanması**: Backend ve UI için Git repolarını başarıyla oluşturmuş olun.
- **Visual Studio 2022**: [Download](https://visualstudio.microsoft.com/downloads/)
- **.NET 8 SDK**: [Download](https://dotnet.microsoft.com/download/dotnet/8.0)
- **Git Extension for Visual Studio**: Visual Studio 2022 ile birlikte gelir, ancak güncel olduğundan emin olun.
- **Azure DevOps'a Erişim**: Azure DevOps hesabınıza erişim sağlayabilecek kullanıcı adı ve şifreniz olmalı.
- **İnternet Bağlantısı**: Azure DevOps web arayüzüne ve Git'e erişmek için stabil bir internet bağlantısı gereklidir.

### 5.5.2 Adım 1: Backend Reposunu Visual Studio ile Klonlama

1. **Visual Studio'yu Açın**
   - Bilgisayarınızda Visual Studio 2022'yi başlatın.

2. **Başlangıç Penceresinden Klonlama Seçeneğine Gitme**
   - Visual Studio açıldığında, **"Clone a repository"** seçeneğine tıklayın. Eğer Visual Studio açıksa, üst menüden **File > Clone Repository** yolunu izleyebilirsiniz.

3. **Azure DevOps Reposundan Klonlama URL'sini Alma**
   - Azure DevOps web arayüzünde `ProductManagement` projesine gidin.
   - Sol menüden **"Repos"** sekmesine tıklayın ve **Backend** reposunu seçin.
   - **"Clone"** butonuna tıklayın ve **HTTPS** URL'sini kopyalayın.
     ```
     https://dev.azure.com/yourorganization/ProductManagement/_git/Backend
     ```

4. **Visual Studio'da Reposu Klonlama**
   - Visual Studio'da açılan **Clone a repository** penceresine, kopyaladığınız URL'yi yapıştırın.
   - **Repository location**: Klonlamak istediğiniz lokal dizini seçin. Örneğin:
     ```
     C:\Projects\ProductManagement\Backend
     ```
   - **Repository Name**: Genellikle repo adı otomatik olarak doldurulur (`Backend`).
   - **Clone** butonuna tıklayın.

5. **Klonlama İşleminin Tamamlanması**
   - Visual Studio, klonlama işlemini başlatacak ve tamamlandığında projeyi otomatik olarak açacaktır.

### 5.5.3 Adım 2: Yeni Bir Branch Oluşturma

1. **Team Explorer'ı Açın**
   - Visual Studio'da, üst menüden **View > Team Explorer** yolunu izleyin.
   - Team Explorer paneli açıldığında, sol tarafta **Branches** sekmesini göreceksiniz.

2. **Main Branch'inden Yeni Branch Oluşturma**
   - **Branches** altında, `main` branch'ini bulun.
   - `main` branch'ine sağ tıklayın ve **New Local Branch From** seçeneğine tıklayın.

3. **Yeni Branch Detaylarını Girin**
   - **Branch name**: `feature/setup-project-structure`
   - **Based on branch**: `main` seçili olmalıdır.
   - **Checkout branch**: Bu seçeneği işaretleyerek yeni branch'e geçiş yapabilirsiniz.
   - **Create Branch** butonuna tıklayın.

4. **Yeni Branch'in Doğrulanması**
   - Team Explorer'da **Branches** sekmesinde, yeni oluşturduğunuz `feature/setup-project-structure` branch'inin listelendiğini ve aktif olduğunu doğrulayın.

### 5.5.4 Adım 3: Proje Yapısını Oluşturma

1. **Solution Explorer'ı Açın**
   - Visual Studio'da, üst menüden **View > Solution Explorer** yolunu izleyin.
   - Klonlanan repoda, mevcut dosyaların ve klasörlerin listelendiğini göreceksiniz.

2. **Gerekli Klasörleri ve Dosyaları Oluşturma**
   - **Solution Explorer** içinde, projenizin ana dizinine sağ tıklayın ve **Add > New Folder** seçeneği ile aşağıdaki klasörleri oluşturun:
     - `Controllers`
     - `Models`
     - `Services`
     - `Repositories`

   - **Proje Dizininde Gerekli Dosyaları Oluşturma**
     - Proje ana dizinine sağ tıklayın ve **Add > New Item** seçeneğine tıklayın.
     - Aşağıdaki dosyaları oluşturun:
       - `Program.cs`
       - `Startup.cs`

3. **Dosya Yapısını Düzenleme**
   - Oluşturduğunuz klasörlerin ve dosyaların proje yapısında doğru konumlandığından emin olun. Örneğin:
     ```
     Backend/
     ├── Controllers/
     ├── Models/
     ├── Services/
     ├── Repositories/
     ├── Program.cs
     └── Startup.cs
     ```

4. **README Dosyasını Güncelleme (Opsiyonel)**
   - **Solution Explorer** içinde `README.md` dosyasına çift tıklayın ve proje hakkında bilgi ekleyebilirsiniz.
     ```markdown
     # Backend Repository

     Bu repo, Basit Ürün Yönetimi Platformu projesinin backend bileşenlerini içerir. ASP.NET Core Web API kullanılarak geliştirilmiştir.
     ```

### 5.5.5 Adım 4: Değişiklikleri Commit ve Push Etme

1. **Team Explorer'da Değişiklikleri Görüntüleme**
   - Team Explorer panelinde, **Changes** sekmesine tıklayın.
   - Yapmış olduğunuz değişikliklerin listelendiğini göreceksiniz.

2. **Değişiklikleri Git'e Eklemek**
   - **Changes** sekmesinde, tüm değişikliklerin seçili olduğundan emin olun. Eğer bazı dosyalar eklenmemişse, bunları işaretleyin.

3. **Commit Mesajını Girin**
   - **Message** alanına açıklayıcı bir commit mesajı yazın:
     ```
     Setup project structure with basic folders and files
     ```

4. **Commit Yapma**
   - **Commit All** butonuna tıklayarak değişiklikleri lokal repoya commit edin.

5. **Branch'i Uzak Reposuna Push Etmek**
   - Team Explorer panelinde, **Sync** sekmesine tıklayın.
   - **Push** butonuna tıklayarak `feature/setup-project-structure` branch'ini uzak repoya gönderin.

### 5.5.6 Adım 5: Pull Request (PR) Oluşturma ve Merge Etme

1. **Azure DevOps Web Arayüzüne Geri Dönün**
   - Tarayıcınızda Azure DevOps web arayüzünü açın ve `ProductManagement` projesine gidin.
   - Sol menüden **"Repos" > "Pull requests"** sekmesine tıklayın.

2. **Yeni Pull Request Oluşturma**
   - **New Pull Request** butonuna tıklayın.

3. **PR Detaylarını Girin**
   - **Source branch**: `feature/setup-project-structure`
   - **Target branch**: `main`
   - **Title**: `Setup Project Structure`
   - **Description**: `Backend projesi için temel klasör yapısını ve gerekli dosyaları oluşturuldu.`

4. **Pull Request'ı Oluşturma**
   - Tüm bilgileri girdikten sonra, **Create** butonuna tıklayarak PR'ı oluşturun.

5. **PR'ı İnceleme ve Onaylama**
   - Ekip üyelerinden PR'ı incelemelerini isteyin.
   - İnceleme süreci tamamlandıktan sonra, **Complete** butonuna tıklayarak PR'ı `main` branch'e merge edin.

6. **Merge İşlemini Doğrulama**
   - Visual Studio'da, **Team Explorer** panelinde **Branches** sekmesine geri dönün.
   - `main` branch'ine geçiş yapın:
     ```bash
     git checkout main
     ```
   - Değişikliklerin başarıyla merge edildiğini doğrulamak için repoyu güncelleyin:
     ```bash
     git pull origin main
     ```

### 5.5.7 Lab-5'in Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak, **Backend** repounuzu Visual Studio kullanarak lokal makinenize klonlamış, ana branch'ten yeni bir branch oluşturmuş ve temel proje yapısını kurmuş oldunuz. Yaptığınız değişiklikleri commit ve push ederek bir Pull Request oluşturmuş ve bu PR'ı main branch'e başarıyla merge etmiş oldunuz. Bu adımlar, projenizin sürüm kontrolünü etkin bir şekilde yönetmenizi ve iş akışınızı düzenli tutmanızı sağlamıştır. Bir sonraki laboratuvar çalışmasında, backend reposunu yapılandırma ve geliştirme adımlarını gerçekleştireceğiz.

---

## 5.6 Lab-6: Lokalde SQL Server Kurulumu ve Yeni Bir Veritabanı Oluşturma

Bu laboratuvar çalışmasında, **Basit Ürün Yönetimi Platformu** projesi için gerekli olan SQL Server'ı lokal makinenize kuracak ve yeni bir veritabanı oluşturacaksınız. Bu adımlar, veritabanı yönetimini ve geliştirmesini kolaylaştıracak şekilde yapılandırılmıştır.

### 5.6.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Windows İşletim Sistemi**: SQL Server ve SQL Server Management Studio (SSMS) genellikle Windows üzerinde kullanılır.
- **İnternet Bağlantısı**: SQL Server ve SSMS indirmek için stabil bir internet bağlantısı gereklidir.
- **Yönetici Hakları**: SQL Server ve SSMS kurulumu için bilgisayarınızda yönetici (admin) haklarına sahip olmanız gerekmektedir.

### 5.6.2 Adım 1: SQL Server'ı İndirme ve Kurma

1. **SQL Server'ın İndirilmesi**
   
   - Tarayıcınızı açın ve [Microsoft SQL Server İndirme Sayfası](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) adresine gidin.
   - **SQL Server 2022** veya mevcut en son sürümü seçin.
   - İhtiyacınıza uygun olan **Developer** veya **Express** sürümünü indirin. **Developer** sürümü, tam özellikli bir geliştirme ve test ortamı sağlar ve ücretsizdir.

2. **SQL Server Kurulumunu Başlatma**
   
   - İndirilen kurulum dosyasını çalıştırın.
   - **Installation Type** bölümünde **Basic** seçeneğini seçin. Bu, hızlı ve varsayılan ayarlarla kurulumu sağlar.
   
3. **Kurulum İşlemini Tamamlama**
   
   - Lisans koşullarını kabul edin ve **Install** butonuna tıklayın.
   - Kurulum tamamlandığında, SQL Server'ın başarıyla yüklendiğini gösteren bir bildirim alacaksınız.
   - **Close** butonuna tıklayarak kurulum sihirbazını kapatın.

### 5.6.3 Adım 2: SQL Server Management Studio (SSMS) Kurulumu

1. **SSMS'nin İndirilmesi**
   
   - Tarayıcınızı açın ve [SQL Server Management Studio İndirme Sayfası](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms) adresine gidin.
   - **Download SSMS** butonuna tıklayarak en son sürümünü indirin.

2. **SSMS Kurulumunu Başlatma**
   
   - İndirilen kurulum dosyasını çalıştırın.
   - Kurulum sihirbazındaki talimatları izleyerek kurulumu tamamlayın.
   - Kurulum tamamlandığında, **Close** butonuna tıklayarak kurulum sihirbazını kapatın.

### 5.6.4 Adım 3: Yeni Bir Veritabanı Oluşturma

1. **SSMS'yi Açma**
   
   - Başlat menüsünden **SQL Server Management Studio**'yu açın.
   - **Connect to Server** penceresi açıldığında, **Server name** alanına SQL Server instance'ınızı girin. Varsayılan olarak, **localhost** veya **.\SQLEXPRESS** olabilir.
   - **Authentication** türünü seçin:
     - **Windows Authentication**: Windows kullanıcı hesabınızla giriş yapar.
     - **SQL Server Authentication**: SQL Server kullanıcı adı ve şifresi kullanır. (Bu seçenek için önceden bir SQL Server kullanıcısı oluşturulmuş olmalıdır.)
   - **Connect** butonuna tıklayarak bağlanın.

2. **Yeni Veritabanı Oluşturma**
   
   - SSMS ana penceresinde, **Object Explorer** panelinde sunucu adına sağ tıklayın.
   - **New Database...** seçeneğine tıklayın.
   
3. **Veritabanı Detaylarını Girme**
   
   - **New Database** penceresinde aşağıdaki bilgileri doldurun:
     - **Database Name**: `ProductManagementDB`
     - **Owner**: Varsayılan olarak kendi kullanıcı adınız atanmış olacaktır. Gerekirse değiştirebilirsiniz.
   
4. **Veritabanını Oluşturma**
   
   - **OK** butonuna tıklayarak veritabanını oluşturun.
   - Oluşturulan veritabanını **Object Explorer** panelinde **Databases** altında göreceksiniz.

### 5.6.5 Adım 4: Veritabanı Ayarlarını Yapılandırma

1. **Veritabanı Ayarlarına Erişim**
   
   - **Object Explorer** panelinde, oluşturduğunuz `ProductManagementDB` veritabanına sağ tıklayın.
   - **Properties** seçeneğine tıklayın.

2. **Veritabanı Özelliklerini Düzenleme**
   
   - **Options** sekmesine gidin.
   - Aşağıdaki ayarları kontrol edin ve gerekirse düzenleyin:
     - **Collation**: Veritabanı karakter setini belirler. Varsayılan olarak `SQL_Latin1_General_CP1_CI_AS` seçili olabilir. İhtiyacınıza göre değiştirebilirsiniz.
     - **Recovery Model**: Yedekleme ve geri yükleme seçeneklerini belirler. Genellikle `Simple` modeli başlangıç için yeterlidir.
   
3. **Değişiklikleri Kaydetme**
   
   - Yapılan değişikliklerden sonra, **OK** butonuna tıklayarak ayarları kaydedin.

### 5.6.6 Adım 5: Veritabanına Bağlantıyı Test Etme

1. **Yeni Veritabanına Bağlanma**
   
   - **Object Explorer** panelinde, `ProductManagementDB` veritabanına tıklayarak genişletin.
   - **Tables** klasörüne sağ tıklayın ve **New > Table...** seçeneğine tıklayın.
   
2. **Tablo Oluşturma**
   
   - Basit bir tablo oluşturmak için aşağıdaki adımları izleyin:
     - **Column Name**: `Id`
       - **Data Type**: `int`
       - **Allow Nulls**: `Unchecked`
       - **Primary Key**: Sağ tıklayarak **Set Primary Key** seçeneğine tıklayın.
     - **Column Name**: `ProductName`
       - **Data Type**: `nvarchar(100)`
       - **Allow Nulls**: `Unchecked`
     - **Column Name**: `Price`
       - **Data Type**: `decimal(18,2)`
       - **Allow Nulls**: `Unchecked`
   
   - Tabloyu kaydedin:
     - Üst menüden **File > Save Table1 As...** seçeneğine tıklayın.
     - **Table Name**: `Products`
     - **OK** butonuna tıklayarak tabloyu oluşturun.

3. **Tabloyu İnceleme**
   
   - **Object Explorer** panelinde, `Products` tablosunu genişleterek oluşturduğunuz sütunları ve anahtarları kontrol edin.
   
4. **SQL Sorgusu ile Veri Eklemek**
   
   - **Object Explorer** panelinde, `Products` tablosuna sağ tıklayın ve **Edit Top 200 Rows** seçeneğine tıklayın.
   - Yeni bir ürün eklemek için aşağıdaki bilgileri girin:
     - `Id`: `1`
     - `ProductName`: `Örnek Ürün`
     - `Price`: `99.99`
   
   - Veri ekledikten sonra, tabloyu kaydedin.

5. **Veritabanı Bağlantısını Test Etme**
   
   - **New Query** butonuna tıklayarak yeni bir SQL sorgusu penceresi açın.
   - Aşağıdaki sorguyu yazın ve çalıştırın:
     ```sql
     SELECT * FROM Products;
     ```
   - Sorgu sonucunda eklediğiniz ürünün listelendiğini doğrulayın.

### 5.6.7 Lab-6'nın Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak, lokal makinenize SQL Server kurmuş, SQL Server Management Studio (SSMS) ile yeni bir veritabanı oluşturmuş ve temel tabloyu ekleyerek veritabanı bağlantısını başarıyla test etmiş oldunuz. Bu adımlar, projenizin veritabanı yönetimini ve geliştirmesini kolaylaştıracak sağlam bir temel oluşturmuştur. Bir sonraki laboratuvar çalışmasında, Entity Framework Core ile veritabanı entegrasyonunu gerçekleştireceğiz.
    
---

## 5.7 Lab-7: Veritabanı Tablolarını Oluşturma ve Entity Framework Core ile Listeleme Metotlarını Yazma

Bu laboratuvar çalışmasında, **ProductManagement** projesi için veritabanı tablolarını oluşturacak ve **Entity Framework Core (EF Core)** kullanarak bu tablolara erişim sağlayacak kodları yazacaksınız. Ayrıca, ürünleri listelemek için gerekli metotları ekleyeceksiniz. Bu adımlar, veritabanı entegrasyonunu sağlamak ve veri yönetimini kolaylaştırmak amacıyla gerçekleştirilmektedir.

### 5.7.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Lab-1'in Tamamlanması**: Azure DevOps üzerinde `ProductManagement` adlı takım projesini başarıyla oluşturmuş olun.
- **Lab-2'nin Tamamlanması**: Epic, Feature, PBI ve Task'ları başarıyla oluşturmuş olun.
- **Lab-3'ün Tamamlanması**: Sprint oluşturmuş ve Task'ları sprint'e atamış olun.
- **Lab-4'ün Tamamlanması**: Backend ve UI için Git repolarını başarıyla oluşturmuş olun.
- **Lab-5'in Tamamlanması**: Backend reposunu Visual Studio kullanarak klonlamış, yeni bir branch oluşturmuş ve temel proje yapısını kurmuş olun.
- **Lab-6'nın Tamamlanması**: SQL Server'ı lokal makinenize kurmuş ve `ProductManagementDB` veritabanını oluşturmuş olun.
- **Visual Studio 2022**: [Download](https://visualstudio.microsoft.com/downloads/)
- **.NET 8 SDK**: [Download](https://dotnet.microsoft.com/download/dotnet/8.0)
- **Entity Framework Core**: Visual Studio üzerinden NuGet paketlerini eklemek için internet bağlantınız olmalı.
- **İnternet Bağlantısı**: Gerekli paketleri indirmek için stabil bir internet bağlantısı gereklidir.

### 5.7.2 Adım 1: Entity Framework Core NuGet Paketlerini Yükleme

1. **Visual Studio'yu Açın ve Backend Projesini Yükleyin**
   
   - Visual Studio 2022'yi başlatın.
   - **Solution Explorer** panelinden `Backend` projesini açın.

2. **NuGet Paket Yöneticisini Açın**
   
   - Üst menüden **Tools > NuGet Package Manager > Manage NuGet Packages for Solution...** yolunu izleyin.

3. **Gerekli EF Core Paketlerini Yükleyin**
   
   - **Browse** sekmesine gidin ve aşağıdaki paketleri aratarak yükleyin:
     - `Microsoft.EntityFrameworkCore`
     - `Microsoft.EntityFrameworkCore.SqlServer`
     - `Microsoft.EntityFrameworkCore.Tools`

   - Her paketi seçip **Install** butonuna tıklayarak projeye ekleyin.

4. **Paket Yükleme Onayı**
   
   - Paketlerin başarıyla yüklendiğini **Installed** sekmesinde doğrulayın.

### 5.7.3 Adım 2: Entity Sınıflarını Oluşturma

1. **Models Klasörünü Oluşturma**
   
   - **Solution Explorer** içinde, `Backend` projesine sağ tıklayın.
   - **Add > New Folder** seçeneğine tıklayın ve klasör adını `Models` olarak belirleyin.

2. **Product Model Sınıfını Oluşturma**
   
   - `Models` klasörüne sağ tıklayın ve **Add > Class...** seçeneğine tıklayın.
   - **Class Name**: `Product.cs`
   - **Add** butonuna tıklayın.

3. **Product.cs İçeriğini Düzenleme**
   
   - Aşağıdaki kodu `Product.cs` dosyasına ekleyin:
     ```csharp
     using System.ComponentModel.DataAnnotations;

     namespace Backend.Models
     {
         public class Product
         {
             [Key]
             public int Id { get; set; }

             [Required]
             [MaxLength(100)]
             public string ProductName { get; set; }

             [Required]
             [Range(0.01, double.MaxValue)]
             public decimal Price { get; set; }

             public int Stock { get; set; }
         }
     }
     ```

### 5.7.4 Adım 3: DbContext Sınıfını Oluşturma

1. **Data Klasörünü Oluşturma**
   
   - **Solution Explorer** içinde, `Backend` projesine sağ tıklayın.
   - **Add > New Folder** seçeneğine tıklayın ve klasör adını `Data` olarak belirleyin.

2. **ApplicationDbContext Sınıfını Oluşturma**
   
   - `Data` klasörüne sağ tıklayın ve **Add > Class...** seçeneğine tıklayın.
   - **Class Name**: `ApplicationDbContext.cs`
   - **Add** butonuna tıklayın.

3. **ApplicationDbContext.cs İçeriğini Düzenleme**
   
   - Aşağıdaki kodu `ApplicationDbContext.cs` dosyasına ekleyin:
     ```csharp
     using Backend.Models;
     using Microsoft.EntityFrameworkCore;

     namespace Backend.Data
     {
         public class ApplicationDbContext : DbContext
         {
             public ApplicationDbContext(DbContextOptions<ApplicationDbContext> options)
                 : base(options)
             {
             }

             public DbSet<Product> Products { get; set; }

             protected override void OnModelCreating(ModelBuilder modelBuilder)
             {
                 base.OnModelCreating(modelBuilder);

                 // Veritabanı tablolarının yapılandırmaları buraya eklenebilir
             }
         }
     }
     ```

### 5.7.5 Adım 4: DbContext'i Konfigüre Etme

1. **appsettings.json Dosyasını Düzenleme**
   
   - **Solution Explorer** içinde, `Backend` projesine sağ tıklayın ve **Open** seçeneği ile `appsettings.json` dosyasını açın.
   - Aşağıdaki bağlantı dizesini ekleyin veya mevcut bağlantı dizesini düzenleyin:
     ```json
     {
       "ConnectionStrings": {
         "DefaultConnection": "Server=localhost;Database=ProductManagementDB;Trusted_Connection=True;"
       },
       "Logging": {
         "LogLevel": {
           "Default": "Information",
           "Microsoft.AspNetCore": "Warning"
         }
       },
       "AllowedHosts": "*"
     }
     ```

2. **Program.cs veya Startup.cs Dosyasını Düzenleme**
   
   - **Solution Explorer** içinde, `Backend` projesine sağ tıklayın ve **Open** seçeneği ile `Program.cs` dosyasını açın.
   
   - Aşağıdaki kodu `Program.cs` dosyasına ekleyin veya mevcut kodu düzenleyin:
     ```csharp
     using Backend.Data;
     using Microsoft.EntityFrameworkCore;

     var builder = WebApplication.CreateBuilder(args);

     // Add services to the container.
     builder.Services.AddControllers();

     // Configure DbContext
     builder.Services.AddDbContext<ApplicationDbContext>(options =>
         options.UseSqlServer(builder.Configuration.GetConnectionString("DefaultConnection")));

     // Learn more about configuring Swagger/OpenAPI at https://aka.ms/aspnetcore/swashbuckle
     builder.Services.AddEndpointsApiExplorer();
     builder.Services.AddSwaggerGen();

     var app = builder.Build();

     // Configure the HTTP request pipeline.
     if (app.Environment.IsDevelopment())
     {
         app.UseSwagger();
         app.UseSwaggerUI();
     }

     app.UseHttpsRedirection();

     app.UseAuthorization();

     app.MapControllers();

     app.Run();
     ```

### 5.7.6 Adım 5: Migration Oluşturma ve Veritabanını Güncelleme

1. **Package Manager Console'u Açma**
   
   - Üst menüden **Tools > NuGet Package Manager > Package Manager Console** yolunu izleyin.

2. **Migration Oluşturma**
   
   - **Package Manager Console** penceresinde, aşağıdaki komutu çalıştırın:
     ```powershell
     Add-Migration InitialCreate
     ```
   - Bu komut, veritabanı şemasını tanımlayan bir migration oluşturur.

3. **Veritabanını Güncelleme**
   
   - Migration tamamlandıktan sonra, aşağıdaki komutu çalıştırarak veritabanını güncelleyin:
     ```powershell
     Update-Database
     ```
   - Bu adım, `ProductManagementDB` veritabanına `Products` tablosunu ekler.

### 5.7.7 Adım 6: Repository ve Service Sınıflarını Oluşturma

1. **Repositories Klasörünü Oluşturma**
   
   - **Solution Explorer** içinde, `Backend` projesine sağ tıklayın.
   - **Add > New Folder** seçeneğine tıklayın ve klasör adını `Repositories` olarak belirleyin.

2. **IProductRepository Arayüzünü Oluşturma**
   
   - `Repositories` klasörüne sağ tıklayın ve **Add > Class...** seçeneğine tıklayın.
   - **Class Name**: `IProductRepository.cs`
   - **Add** butonuna tıklayın.
   
   - Aşağıdaki kodu `IProductRepository.cs` dosyasına ekleyin:
     ```csharp
     using Backend.Models;

     namespace Backend.Repositories
     {
         public interface IProductRepository
         {
             Task<IEnumerable<Product>> GetAllProductsAsync();
             // Diğer CRUD metotları buraya eklenebilir
         }
     }
     ```

3. **ProductRepository Sınıfını Oluşturma**
   
   - `Repositories` klasörüne sağ tıklayın ve **Add > Class...** seçeneğine tıklayın.
   - **Class Name**: `ProductRepository.cs`
   - **Add** butonuna tıklayın.
   
   - Aşağıdaki kodu `ProductRepository.cs` dosyasına ekleyin:
     ```csharp
     using Backend.Data;
     using Backend.Models;
     using Microsoft.EntityFrameworkCore;

     namespace Backend.Repositories
     {
         public class ProductRepository : IProductRepository
         {
             private readonly ApplicationDbContext _context;

             public ProductRepository(ApplicationDbContext context)
             {
                 _context = context;
             }

             public async Task<IEnumerable<Product>> GetAllProductsAsync()
             {
                 return await _context.Products.ToListAsync();
             }

             // Diğer CRUD metotları buraya eklenebilir
         }
     }
     ```

4. **Repository'yi Dependency Injection'a Eklemek**
   
   - **Program.cs** dosyasını tekrar açın ve repository'yi servisler arasına ekleyin:
     ```csharp
     using Backend.Data;
     using Backend.Repositories;
     using Microsoft.EntityFrameworkCore;

     var builder = WebApplication.CreateBuilder(args);

     // Add services to the container.
     builder.Services.AddControllers();

     // Configure DbContext
     builder.Services.AddDbContext<ApplicationDbContext>(options =>
         options.UseSqlServer(builder.Configuration.GetConnectionString("DefaultConnection")));

     // Register repositories
     builder.Services.AddScoped<IProductRepository, ProductRepository>();

     // Learn more about configuring Swagger/OpenAPI at https://aka.ms/aspnetcore/swashbuckle
     builder.Services.AddEndpointsApiExplorer();
     builder.Services.AddSwaggerGen();

     var app = builder.Build();

     // Configure the HTTP request pipeline.
     if (app.Environment.IsDevelopment())
     {
         app.UseSwagger();
         app.UseSwaggerUI();
     }

     app.UseHttpsRedirection();

     app.UseAuthorization();

     app.MapControllers();

     app.Run();
     ```

### 5.7.8 Adım 7: Controller Oluşturma ve Listeleme Metotlarını Eklemek

1. **Controllers Klasörüne Ürün Controller'ını Eklemek**
   
   - **Solution Explorer** içinde, `Controllers` klasörüne sağ tıklayın.
   - **Add > Controller...** seçeneğine tıklayın.
   - **API Controller - Empty** seçeneğini seçin ve **Add** butonuna tıklayın.
   - **Controller Name**: `ProductsController`
   - **Add** butonuna tıklayın.

2. **ProductsController.cs İçeriğini Düzenleme**
   
   - Aşağıdaki kodu `ProductsController.cs` dosyasına ekleyin:
     ```csharp
     using Backend.Models;
     using Backend.Repositories;
     using Microsoft.AspNetCore.Mvc;

     namespace Backend.Controllers
     {
         [Route("api/[controller]")]
         [ApiController]
         public class ProductsController : ControllerBase
         {
             private readonly IProductRepository _productRepository;

             public ProductsController(IProductRepository productRepository)
             {
                 _productRepository = productRepository;
             }

             // GET: api/Products
             [HttpGet]
             public async Task<ActionResult<IEnumerable<Product>>> GetProducts()
             {
                 var products = await _productRepository.GetAllProductsAsync();
                 return Ok(products);
             }

             // Diğer CRUD metotları buraya eklenebilir
         }
     }
     ```

3. **API'yi Test Etme**
   
   - Projeyi çalıştırın (**F5** tuşuna basın veya üst menüden **Debug > Start Debugging** seçeneğine tıklayın).
   - Tarayıcınızda Swagger UI açılacaktır.
   - **Products** endpoint'ini bulun ve **GET** metodunu test edin.
   - `Products` tablosunda eklediğiniz ürünün listelendiğini doğrulayın.

### 5.7.9 Lab-7'nin Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak, **ProductManagement** projesi için veritabanı tablolarını oluşturmuş, **Entity Framework Core** ile veritabanı entegrasyonunu sağlamış ve ürünleri listelemek için gerekli metotları eklemiş oldunuz. Bu adımlar, veritabanı ile uygulamanız arasındaki etkileşimi yönetmenizi ve veri işlemlerini kolaylaştırmanızı sağlamıştır. Bir sonraki laboratuvar çalışmasında, CRUD işlemleri için diğer metotları eklemeye ve API'yi genişletmeye devam edeceğiz.

---

## 5.8 Lab-8: UI İçin Yeni Bir Feature Branch Açma, Temel Proje Oluşturma ve Pull Request ile Merge Etme

Bu laboratuvar çalışmasında, **ProductManagement** projesinin **UI** reposu üzerinde yeni bir feature branch açacak, Visual Studio Code (VSCode) kullanarak temel bir UI projesi oluşturacak ve yaptığınız değişiklikleri commit/push ederek bir Pull Request (PR) oluşturup `main` branch'e merge edeceksiniz. Bu adımlar, frontend geliştirme sürecinizi düzenli ve sürüm kontrolü altında tutmanıza yardımcı olacaktır.

### 5.8.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Lab-1'in Tamamlanması**: Azure DevOps üzerinde `ProductManagement` adlı takım projesini başarıyla oluşturmuş olun.
- **Lab-2'nin Tamamlanması**: Epic, Feature, PBI ve Task'ları başarıyla oluşturmuş olun.
- **Lab-3'ün Tamamlanması**: Sprint oluşturmuş ve Task'ları sprint'e atamış olun.
- **Lab-4'ün Tamamlanması**: Backend ve UI için Git repolarını başarıyla oluşturmuş olun.
- **Lab-5'in Tamamlanması**: Backend reposunu Visual Studio kullanarak klonlamış, yeni bir branch oluşturmuş ve temel proje yapısını kurmuş olun.
- **Lab-6'nın Tamamlanması**: SQL Server'ı lokal makinenize kurmuş ve `ProductManagementDB` veritabanını oluşturmuş olun.
- **Lab-7'nin Tamamlanması**: Backend için Entity Framework Core ile veritabanı entegrasyonunu gerçekleştirmiş olun.
- **Visual Studio Code (VSCode)**: [Download](https://code.visualstudio.com/) edilerek kurulmuş ve yapılandırılmış olmalı.
- **Node.js ve npm**: [Download](https://nodejs.org/) edilerek kurulmuş olmalı (UI projesi için).
- **Git Yüklü Olmalı**: Bilgisayarınıza [Git](https://git-scm.com/downloads) yüklü olmalıdır.
- **Azure DevOps'a Erişim**: Azure DevOps hesabınıza erişim sağlayabilecek kullanıcı adı ve şifreniz olmalı.
- **İnternet Bağlantısı**: Azure DevOps web arayüzüne ve Git'e erişmek için stabil bir internet bağlantısı gereklidir.

### 5.8.2 Adım 1: UI Reposunu Klonlama ve Yeni Bir Branch Oluşturma

1. **Azure DevOps'ta UI Reposunu Bulma**
   - Azure DevOps hesabınıza giriş yapın ve `ProductManagement` projesini seçin.
   - Sol menüden **"Repos"** sekmesine tıklayın ve **UI** reposunu seçin.

2. **Klonlama URL'sini Alma**
   - **UI** reposunun ana sayfasında, sağ üst köşede bulunan **"Clone"** butonuna tıklayın.
   - Açılan pencerede **HTTPS** URL'sini kopyalayın.
     ```
     https://dev.azure.com/yourorganization/ProductManagement/_git/UI
     ```

3. **UI Reposunu Lokal Makinenize Klonlama**
   - Visual Studio Code'u açın.
   - Başlangıç ekranında **"Clone Repository"** seçeneğine tıklayın. Eğer VSCode açıksa, **View > Command Palette...** yolunu izleyin ve `Git: Clone` komutunu seçin.
   - Kopyaladığınız HTTPS URL'sini yapıştırın ve **Enter** tuşuna basın.
   - Klonlamak istediğiniz lokal dizini seçin ve **Select Repository Location** butonuna tıklayın.
   - Klonlama işlemi tamamlandığında, VSCode size klonlanan repoyu açma seçeneği sunacaktır. **Open** butonuna tıklayarak repoyu açın.

4. **Yeni Feature Branch Oluşturma**
   - VSCode'un sol alt köşesinde bulunan branch adını (genellikle `main`) tıklayın.
   - Açılan menüde **Create new branch** seçeneğine tıklayın.
   - Yeni branch adı olarak `feature/setup-ui-project` yazın ve **Enter** tuşuna basın.
   - VSCode, yeni oluşturulan branch'e geçiş yapacaktır.

### 5.8.3 Adım 2: Visual Studio Code ile Temel UI Projesi Oluşturma

1. **Terminali Açma**
   - VSCode'da üst menüden **Terminal > New Terminal** yolunu izleyin. Bu, VSCode içerisinde entegre bir terminal açacaktır.

2. **UI Projesini Oluşturma**
   - UI projesi olarak React kullanacaksanız, terminalde aşağıdaki komutu çalıştırın:
     ```
     npx create-react-app frontend
     ```
   - Bu komut, `frontend` adlı yeni bir React projesi oluşturur ve gerekli dosya yapısını sağlar.

3. **Proje Yapısını İnceleme**
   - **Explorer** panelinde, oluşturulan `frontend` klasörünü göreceksiniz. Temel dosyaların ve klasörlerin oluşturulduğunu doğrulayın:
     ```
     UI/
     ├── frontend/
     │   ├── node_modules/
     │   ├── public/
     │   ├── src/
     │   ├── package.json
     │   └── README.md
     ├── .gitignore
     └── README.md
     ```

4. **README Dosyasını Güncelleme (Opsiyonel)**
   - **frontend** klasöründe bulunan `README.md` dosyasını açın ve proje hakkında bilgi ekleyebilirsiniz.

### 5.8.4 Adım 3: Değişiklikleri Commit ve Push Etme

1. **Source Control Panelini Açma**
   - VSCode'un sol yan panelinde bulunan **Source Control** simgesine tıklayın (genellikle bir dallı ağ simgesi).
   - Yapmış olduğunuz değişiklikler listelenecektir.

2. **Değişiklikleri Stage Etme**
   - **Changes** bölümünde, tüm değişikliklerin yanındaki **+** işaretine tıklayarak değişiklikleri stage edin. Tüm değişiklikleri stage etmek için üstteki **Stage All Changes** simgesine tıklayabilirsiniz.

3. **Commit Mesajını Girme**
   - **Message** alanına açıklayıcı bir commit mesajı yazın:
     ```
     Setup basic React UI project structure
     ```
   - **Commit** butonuna tıklayarak değişiklikleri commit edin.

4. **Branch'i Uzak Reposuna Push Etme**
   - VSCode'un altındaki **Sync Changes** butonuna tıklayın. Bu, oluşturduğunuz `feature/setup-ui-project` branch'ini uzak repoya push edecektir.
   - Eğer **Sync Changes** butonu görünmüyorsa, **...** menüsüne tıklayın ve **Push** seçeneğini seçin.

### 5.8.5 Adım 4: Pull Request (PR) Oluşturma ve Merge Etme

1. **Azure DevOps Web Arayüzüne Geri Dönün**
   - Tarayıcınızda Azure DevOps web arayüzünü açın ve `ProductManagement` projesine gidin.
   - Sol menüden **"Repos" > "Pull requests"** sekmesine tıklayın.

2. **Yeni Pull Request Başlatma**
   - **New Pull Request** butonuna tıklayın.

3. **PR Detaylarını Girin**
   - **Source branch**: `feature/setup-ui-project`
   - **Target branch**: `main`
   - **Title**: `Setup Basic React UI Project Structure`
   - **Description**: `UI projesi için temel React yapılandırması oluşturuldu. Frontend klasörü altında create-react-app ile başlangıç yapıldı.`

4. **Pull Request'ı Oluşturma**
   - Tüm bilgileri girdikten sonra, **Create** butonuna tıklayarak PR'ı oluşturun.

5. **PR'ı İnceleme ve Onaylama**
   - Ekip üyelerinden PR'ı incelemelerini isteyin.
   - İnceleme süreci tamamlandıktan sonra, **Complete** butonuna tıklayarak PR'ı `main` branch'e merge edin.
   - Gerekirse **Squash Commit** veya **Rebase and Merge** seçeneklerini kullanabilirsiniz.

6. **Merge İşlemini Doğrulama**
   - VSCode'da, **Source Control** paneline geri dönün.
   - **Pull** butonuna tıklayarak `main` branch'ini güncelleyin ve merge edilen değişiklikleri alın.

### 5.8.6 Adım 5: Merge İşlemi Sonrası Kontroller

1. **Proje Yapısını İnceleme**
   - VSCode'da `main` branch'ine geçtiğinizden emin olun ve `frontend` klasörünün doğru şekilde oluşturulduğunu doğrulayın.

2. **Uygulamayı Test Etme (Opsiyonel)**
   - Terminalde, `frontend` dizinine geçin ve uygulamayı çalıştırın:
     ```
     cd frontend
     npm start
     ```
   - Tarayıcınızda `http://localhost:3000` adresinde React uygulamasının sorunsuz çalıştığını doğrulayın.
   - Uygulama çalıştıktan sonra terminalde `Ctrl + C` tuş kombinasyonuyla durdurabilirsiniz.

### 5.8.7 Lab-8'in Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak, **UI** repounuz üzerinde yeni bir feature branch oluşturmuş, Visual Studio Code kullanarak temel bir React UI projesi oluşturmuş, yaptığınız değişiklikleri commit/push etmiş ve bir Pull Request aracılığıyla bu değişiklikleri `main` branch'e başarıyla merge etmiş oldunuz. Bu adımlar, frontend geliştirme sürecinizi düzenli ve sürüm kontrolü altında tutmanızı sağlamıştır. Bir sonraki laboratuvar çalışmasında, UI projesine daha fazla özellik ekleyerek geliştirmeye devam edeceğiz.

---

## 5.8 Lab-8: UI İçin Yeni Bir Feature Branch Açma, Temel Proje Oluşturma ve Pull Request ile Merge Etme

Bu laboratuvar çalışmasında, **ProductManagement** projesinin **UI** reposu üzerinde yeni bir feature branch açacak, Visual Studio Code (VSCode) kullanarak temel bir UI projesi oluşturacak ve yaptığınız değişiklikleri commit/push ederek bir Pull Request (PR) oluşturup `main` branch'e merge edeceksiniz. Bu adımlar, frontend geliştirme sürecinizi düzenli ve sürüm kontrolü altında tutmanıza yardımcı olacaktır.

### 5.8.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Lab-1'in Tamamlanması**: Azure DevOps üzerinde `ProductManagement` adlı takım projesini başarıyla oluşturmuş olun.
- **Lab-2'nin Tamamlanması**: Epic, Feature, PBI ve Task'ları başarıyla oluşturmuş olun.
- **Lab-3'ün Tamamlanması**: Sprint oluşturmuş ve Task'ları sprint'e atamış olun.
- **Lab-4'ün Tamamlanması**: Backend ve UI için Git repolarını başarıyla oluşturmuş olun.
- **Lab-5'in Tamamlanması**: Backend reposunu Visual Studio kullanarak klonlamış, yeni bir branch oluşturmuş ve temel proje yapısını kurmuş olun.
- **Lab-6'nın Tamamlanması**: SQL Server'ı lokal makinenize kurmuş ve `ProductManagementDB` veritabanını oluşturmuş olun.
- **Lab-7'nin Tamamlanması**: Backend için Entity Framework Core ile veritabanı entegrasyonunu gerçekleştirmiş olun.
- **Visual Studio Code (VSCode)**: [Download](https://code.visualstudio.com/) edilerek kurulmuş ve yapılandırılmış olmalı.
- **Node.js ve npm**: [Download](https://nodejs.org/) edilerek kurulmuş olmalı (UI projesi için).
- **Angular CLI Yüklü Olmalı**: Terminalde aşağıdaki komutu çalıştırarak Angular CLI'yı global olarak yükleyin:

```
npm install -g @angular/cli
```

- **Git Yüklü Olmalı**: Bilgisayarınıza [Git](https://git-scm.com/downloads) yüklü olmalıdır.
- **Azure DevOps'a Erişim**: Azure DevOps hesabınıza erişim sağlayabilecek kullanıcı adı ve şifreniz olmalı.
- **İnternet Bağlantısı**: Azure DevOps web arayüzüne ve Git'e erişmek için stabil bir internet bağlantısı gereklidir.

### 5.8.2 Adım 1: UI Reposunu Klonlama ve Yeni Bir Branch Oluşturma

1. **Azure DevOps'ta UI Reposunu Bulma**
 - Azure DevOps hesabınıza giriş yapın ve `ProductManagement` projesini seçin.
 - Sol menüden **"Repos"** sekmesine tıklayın ve **UI** reposunu seçin.

2. **Klonlama URL'sini Alma**
 - **UI** reposunun ana sayfasında, sağ üst köşede bulunan **"Clone"** butonuna tıklayın.
 - Açılan pencerede **HTTPS** URL'sini kopyalayın.
   ```
   https://dev.azure.com/yourorganization/ProductManagement/_git/UI
   ```

3. **UI Reposunu Lokal Makinenize Klonlama**
 - Visual Studio Code'u açın.
 - Başlangıç ekranında **"Clone Repository"** seçeneğine tıklayın. Eğer VSCode açıksa, **View > Command Palette...** yolunu izleyin ve `Git: Clone` komutunu seçin.
 - Kopyaladığınız HTTPS URL'sini yapıştırın ve **Enter** tuşuna basın.
 - Klonlamak istediğiniz lokal dizini seçin ve **Select Repository Location** butonuna tıklayın.
 - Klonlama işlemi tamamlandığında, VSCode size klonlanan repoyu açma seçeneği sunacaktır. **Open** butonuna tıklayarak repoyu açın.

4. **Yeni Feature Branch Oluşturma**
 - VSCode'un sol alt köşesinde bulunan branch adını (genellikle `main`) tıklayın.
 - Açılan menüde **Create new branch** seçeneğine tıklayın.
 - Yeni branch adı olarak `feature/setup-ui-project` yazın ve **Enter** tuşuna basın.
 - VSCode, yeni oluşturulan branch'e geçiş yapacaktır.

### 5.8.3 Adım 2: Visual Studio Code ile Temel UI Projesi Oluşturma

1. **Terminali Açma**
 - VSCode'da üst menüden **Terminal > New Terminal** yolunu izleyin. Bu, VSCode içerisinde entegre bir terminal açacaktır.

2. **UI Projesini Oluşturma**
 - UI projesi olarak Angular kullanacaksanız, terminalde aşağıdaki komutu çalıştırın:
   ```
   ng new frontend
   ```
 - Komut çalıştırıldığında sizden proje için bazı yapılandırmalar yapmanızı isteyecektir:
   - **Would you like to add Angular routing?**: `Yes` seçin.
   - **Which stylesheet format would you like to use?**: İhtiyacınıza uygun olanı seçin (örneğin, `CSS`).

3. **Proje Yapısını İnceleme**
 - **Explorer** panelinde, oluşturulan `frontend` klasörünü göreceksiniz. Temel dosyaların ve klasörlerin oluşturulduğunu doğrulayın:
   ```
   UI/
   ├── frontend/
   │   ├── node_modules/
   │   ├── src/
   │   ├── angular.json
   │   ├── package.json
   │   └── README.md
   ├── .gitignore
   └── README.md
   ```

4. **README Dosyasını Güncelleme (Opsiyonel)**
 - **frontend** klasöründe bulunan `README.md` dosyasını açın ve proje hakkında bilgi ekleyebilirsiniz.

### 5.8.4 Adım 3: Değişiklikleri Commit ve Push Etme

1. **Source Control Panelini Açma**
 - VSCode'un sol yan panelinde bulunan **Source Control** simgesine tıklayın (genellikle bir dallı ağ simgesi).
 - Yapmış olduğunuz değişiklikler listelenecektir.

2. **Değişiklikleri Stage Etme**
 - **Changes** bölümünde, tüm değişikliklerin yanındaki **+** işaretine tıklayarak değişiklikleri stage edin. Tüm değişiklikleri stage etmek için üstteki **Stage All Changes** simgesine tıklayabilirsiniz.

3. **Commit Mesajını Girme**
 - **Message** alanına açıklayıcı bir commit mesajı yazın:
   ```
   Setup basic Angular UI project structure
   ```
 - **Commit** butonuna tıklayarak değişiklikleri commit edin.

4. **Branch'i Uzak Reposuna Push Etme**
 - VSCode'un altındaki **Sync Changes** butonuna tıklayın. Bu, oluşturduğunuz `feature/setup-ui-project` branch'ini uzak repoya push edecektir.
 - Eğer **Sync Changes** butonu görünmüyorsa, **...** menüsüne tıklayın ve **Push** seçeneğini seçin.

### 5.8.5 Adım 4: Pull Request (PR) Oluşturma ve Merge Etme

1. **Azure DevOps Web Arayüzüne Geri Dönün**
 - Tarayıcınızda Azure DevOps web arayüzünü açın ve `ProductManagement` projesine gidin.
 - Sol menüden **"Repos" > "Pull requests"** sekmesine tıklayın.

2. **Yeni Pull Request Başlatma**
 - **New Pull Request** butonuna tıklayın.

3. **PR Detaylarını Girin**
 - **Source branch**: `feature/setup-ui-project`
 - **Target branch**: `main`
 - **Title**: `Setup Basic Angular UI Project Structure`
 - **Description**: `UI projesi için temel Angular yapılandırması oluşturuldu. Frontend klasörü altında ng new komutu ile başlangıç yapıldı.`

4. **Pull Request'ı Oluşturma**
 - Tüm bilgileri girdikten sonra, **Create** butonuna tıklayarak PR'ı oluşturun.

5. **PR'ı İnceleme ve Onaylama**
 - Ekip üyelerinden PR'ı incelemelerini isteyin.
 - İnceleme süreci tamamlandıktan sonra, **Complete** butonuna tıklayarak PR'ı `main` branch'e merge edin.
 - Gerekirse **Squash Commit** veya **Rebase and Merge** seçeneklerini kullanabilirsiniz.

6. **Merge İşlemini Doğrulama**
 - VSCode'da, **Source Control** paneline geri dönün.
 - **Pull** butonuna tıklayarak `main` branch'ini güncelleyin ve merge edilen değişiklikleri alın.

### 5.8.6 Adım 5: Merge İşlemi Sonrası Kontroller

1. **Proje Yapısını İnceleme**
 - VSCode'da `main` branch'ine geçtiğinizden emin olun ve `frontend` klasörünün doğru şekilde oluşturulduğunu doğrulayın.

2. **Uygulamayı Test Etme (Opsiyonel)**
 - Terminalde, `frontend` dizinine geçin ve uygulamayı çalıştırın:
   ```
   cd frontend
   ng serve
   ```
 - Tarayıcınızda `http://localhost:4200` adresinde Angular uygulamasının sorunsuz çalıştığını doğrulayın.
 - Uygulama çalıştıktan sonra terminalde `Ctrl + C` tuş kombinasyonuyla durdurabilirsiniz.

### 5.8.7 Lab-8'in Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak, **UI** repounuz üzerinde yeni bir feature branch oluşturmuş, Visual Studio Code kullanarak temel bir Angular UI projesi oluşturmuş, yaptığınız değişiklikleri commit/push etmiş ve bir Pull Request aracılığıyla bu değişiklikleri `main` branch'e başarıyla merge etmiş oldunuz. Bu adımlar, frontend geliştirme sürecinizi düzenli ve sürüm kontrolü altında tutmanızı sağlamıştır. Bir sonraki laboratuvar çalışmasında, UI projesine daha fazla özellik ekleyerek geliştirmeye devam edeceğiz.

---

## 5.9 Lab-9: Ürünleri Listeleyen Sayfa İçin UI Kodlarını Yazma, Backend ile Bağlama ve CORS Ayarlarını Yapma

Bu laboratuvar çalışmasında, **ProductManagement** projesinin **UI** (Angular 18) ve **Backend** (ASP.NET Core) projelerini birbirine bağlayarak ürünleri listeleyen bir sayfa oluşturacak ve CORS (Cross-Origin Resource Sharing) ayarlarını yapılandıracaksınız. Bu adımlar, frontend ve backend arasındaki etkileşimi sağlamak ve güvenli bir iletişim ortamı oluşturmak için gereklidir.

### 5.9.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Lab-1'den Lab-8'e Kadar Tüm Laboratuvarların Tamamlanması**: Önceki laboratuvar adımlarını başarıyla tamamlamış olun.
- **Visual Studio Code (VSCode)**: [Download](https://code.visualstudio.com/) edilerek kurulmuş ve yapılandırılmış olmalı.
- **Angular CLI Yüklü Olmalı**: Terminalde aşağıdaki komutu çalıştırarak Angular CLI'yı global olarak yükleyin:

```
npm install -g @angular/cli
```

- **Backend Projesi Çalışır Durumda Olmalı**: ASP.NET Core backend projenizin çalışır durumda ve `ProductManagementDB` veritabanına bağlı olduğundan emin olun.
- **CORS İçin Gerekli Bilgiler**: Backend projesinde CORS ayarlarını yapabilmek için gerekli izinler ve bilgiler sağlanmış olmalı.
- **İnternet Bağlantısı**: Gerekli paketleri indirmek ve projeleri senkronize etmek için stabil bir internet bağlantısı gereklidir.

### 5.9.2 Adım 1: Ürünleri Listeleyen Angular Bileşenini Oluşturma

1. **Angular Projesinde Yeni Bileşen Oluşturma**
 - VSCode'da **UI** projenizin kök dizininde terminali açın.
 - Aşağıdaki komutu çalıştırarak `products` adlı yeni bir bileşen oluşturun:
   ```
   ng generate component products
   ```
 - Bu komut, `src/app/products` dizini altında gerekli dosyaları oluşturacaktır.

2. **Products Bileşenini Yapılandırma**
 - **src/app/products/products.component.ts** dosyasını açın ve aşağıdaki kodu ekleyin:
   ```typescript
   import { Component, OnInit } from '@angular/core';
   import { ProductService } from '../services/product.service';
   import { Product } from '../models/product.model';

   @Component({
     selector: 'app-products',
     templateUrl: './products.component.html',
     styleUrls: ['./products.component.css']
   })
   export class ProductsComponent implements OnInit {
     products: Product[] = [];

     constructor(private productService: ProductService) { }

     ngOnInit(): void {
       this.loadProducts();
     }

     loadProducts(): void {
       this.productService.getProducts().subscribe({
         next: (data) => this.products = data,
         error: (err) => console.error(err)
       });
     }
   }
   ```

3. **Products Bileşeninin HTML Şablonunu Düzenleme**
 - **src/app/products/products.component.html** dosyasını açın ve aşağıdaki kodu ekleyin:
   ```html
   <div class="container">
     <h2>Ürünler Listesi</h2>
     <table class="table table-striped">
       <thead>
         <tr>
           <th>ID</th>
           <th>Ürün Adı</th>
           <th>Fiyat</th>
           <th>Stok</th>
         </tr>
       </thead>
       <tbody>
         <tr *ngFor="let product of products">
           <td>{{ product.id }}</td>
           <td>{{ product.productName }}</td>
           <td>{{ product.price | currency }}</td>
           <td>{{ product.stock }}</td>
         </tr>
       </tbody>
     </table>
   </div>
   ```

4. **Ürün Modelini Oluşturma**
 - **src/app/models** klasörüne sağ tıklayın ve **New File** oluşturun. Dosya adını `product.model.ts` olarak belirleyin.
 - **product.model.ts** dosyasına aşağıdaki kodu ekleyin:
   ```typescript
   export interface Product {
     id: number;
     productName: string;
     price: number;
     stock: number;
   }
   ```

### 5.9.3 Adım 2: Backend API'sine HTTP Servisini Eklemek

1. **Product Servisini Oluşturma**
 - Terminalde aşağıdaki komutu çalıştırarak `product` adlı yeni bir servis oluşturun:
   ```
   ng generate service services/product
   ```
 - Bu komut, `src/app/services/product.service.ts` dosyasını oluşturacaktır.

2. **Product Servisini Yapılandırma**
 - **src/app/services/product.service.ts** dosyasını açın ve aşağıdaki kodu ekleyin:
   ```typescript
   import { Injectable } from '@angular/core';
   import { HttpClient, HttpErrorResponse } from '@angular/common/http';
   import { Observable, throwError } from 'rxjs';
   import { catchError } from 'rxjs/operators';
   import { Product } from '../models/product.model';

   @Injectable({
     providedIn: 'root'
   })
   export class ProductService {
     private apiUrl = 'https://localhost:5001/api/Products'; // Backend API URL'si

     constructor(private http: HttpClient) { }

     getProducts(): Observable<Product[]> {
       return this.http.get<Product[]>(this.apiUrl)
         .pipe(
           catchError(this.handleError)
         );
     }

     private handleError(error: HttpErrorResponse) {
       if (error.error instanceof ErrorEvent) {
         // Client-side veya network hatası
         console.error('An error occurred:', error.error.message);
       } else {
         // Backend hatası
         console.error(
           `Backend returned code ${error.status}, ` +
           `body was: ${error.error}`);
       }
       // Kullanıcıya gösterilecek hata mesajını dön
       return throwError(
         'Something bad happened; please try again later.');
     }
   }
   ```

3. **HTTP Client Modülünü Eklemek**
 - **src/app/app.module.ts** dosyasını açın ve `HttpClientModule`'ü içe aktarın:
   ```typescript
   import { BrowserModule } from '@angular/platform-browser';
   import { NgModule } from '@angular/core';
   import { HttpClientModule } from '@angular/common/http';

   import { AppComponent } from './app.component';
   import { ProductsComponent } from './products/products.component';

   @NgModule({
     declarations: [
       AppComponent,
       ProductsComponent
     ],
     imports: [
       BrowserModule,
       HttpClientModule
     ],
     providers: [],
     bootstrap: [AppComponent]
   })
   export class AppModule { }
   ```

### 5.9.4 Adım 3: Ürünleri Listeleyen Sayfayı Oluşturma

1. **Ürünler Bileşenini Uygulamaya Eklemek**
 - **src/app/app.component.html** dosyasını açın ve aşağıdaki kodu ekleyin:
   ```html
   <app-products></app-products>
   ```

2. **Angular Uygulamasını Çalıştırma**
 - Terminalde aşağıdaki komutu çalıştırarak Angular uygulamasını başlatın:
   ```
   ng serve
   ```
 - Tarayıcınızda `http://localhost:4200` adresine giderek ürünlerin listelendiğini doğrulayın.

### 5.9.5 Adım 4: CORS Ayarlarını Yapma

1. **Backend Projesinde CORS Ayarlarını Yapılandırma**
 - **Startup.cs** veya **Program.cs** dosyanızı açın (ASP.NET Core 6 ve üzeri için genellikle **Program.cs**).
 - Aşağıdaki kodu ekleyerek CORS politikasını tanımlayın:
   ```csharp
   var builder = WebApplication.CreateBuilder(args);

   // Add services to the container.
   builder.Services.AddControllers();

   // Configure CORS
   builder.Services.AddCors(options =>
   {
       options.AddPolicy("AllowAngularApp",
           builder =>
           {
               builder.WithOrigins("http://localhost:4200")
                      .AllowAnyHeader()
                      .AllowAnyMethod();
           });
   });

   // Configure DbContext
   builder.Services.AddDbContext<ApplicationDbContext>(options =>
       options.UseSqlServer(builder.Configuration.GetConnectionString("DefaultConnection")));

   // Register repositories
   builder.Services.AddScoped<IProductRepository, ProductRepository>();

   // Learn more about configuring Swagger/OpenAPI at https://aka.ms/aspnetcore/swashbuckle
   builder.Services.AddEndpointsApiExplorer();
   builder.Services.AddSwaggerGen();

   var app = builder.Build();

   // Configure the HTTP request pipeline.
   if (app.Environment.IsDevelopment())
   {
       app.UseSwagger();
       app.UseSwaggerUI();
   }

   app.UseHttpsRedirection();

   app.UseCors("AllowAngularApp"); // CORS politikasını kullan

   app.UseAuthorization();

   app.MapControllers();

   app.Run();
   ```

2. **Backend Projesini Yeniden Başlatma**
 - Visual Studio veya terminalde backend projesini durdurup tekrar başlatarak CORS ayarlarının uygulanmasını sağlayın.

### 5.9.6 Adım 5: Uygulamayı Test Etme

1. **Backend API'sinin Çalıştığından Emin Olma**
 - Backend projesinin çalışır durumda olduğundan ve `Products` API'sine erişilebildiğinden emin olun. Örneğin, `https://localhost:5001/api/Products` adresine tarayıcıdan veya Postman aracılığıyla erişmeyi deneyin.

2. **Angular Uygulamasında Ürünleri Listeleme**
 - Angular uygulamanızı (`ng serve`) çalıştırın.
 - Tarayıcınızda `http://localhost:4200` adresine gidin.
 - Ürünlerin başarıyla listelendiğini doğrulayın. Backend'den alınan verilerin tabloda görüntülendiğini görmelisiniz.

3. **Hata Ayıklama**
 - Eğer ürünler listelenmiyorsa, tarayıcı konsolunu ve backend loglarını kontrol ederek hataları tespit edin.
 - CORS ile ilgili hatalar varsa, backend CORS ayarlarını tekrar gözden geçirin.

### 5.9.7 Lab-9'un Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak, **UI** (Angular 18) projenizde ürünleri listeleyen bir sayfa oluşturmuş, bu sayfayı **Backend** (ASP.NET Core) API'sine bağlamış ve CORS ayarlarını yapılandırarak frontend ve backend arasında güvenli bir iletişim sağlamış oldunuz. Bu adımlar, projenizin frontend ve backend bileşenleri arasındaki etkileşimi optimize etmenizi ve kullanıcıya dinamik veri sunmanızı sağlamıştır. Bir sonraki laboratuvar çalışmasında, UI projesine daha fazla özellik ekleyerek geliştirmeye devam edeceğiz.

---

## 5.10 Lab-10: Ürün Ekleme Özelliğini Backend ve UI'ye Eklemek

Bu laboratuvar çalışmasında, **ProductManagement** projesine ürün ekleme özelliği ekleyeceğiz. İlk olarak, **Backend** (ASP.NET Core) kodlarını güncelleyecek, ardından **UI** (Angular 18) tarafında gerekli değişiklikleri yapacağız ve her iki bileşeni birbirine bağlayacağız. Bu adımlar, kullanıcıların yeni ürünler eklemesine olanak tanıyacak ve sistemin işlevselliğini artıracaktır.

### 5.10.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Lab-1'den Lab-9'a Kadar Tüm Laboratuvarların Tamamlanması**: Önceki laboratuvar adımlarını başarıyla tamamlamış olun.
- **Visual Studio Code (VSCode)**: [Download](https://code.visualstudio.com/) edilerek kurulmuş ve yapılandırılmış olmalı.
- **Backend Projesi Çalışır Durumda Olmalı**: ASP.NET Core backend projenizin çalışır durumda ve `ProductManagementDB` veritabanına bağlı olduğundan emin olun.
- **CORS Ayarları Yapılandırılmış Olmalı**: Lab-9'da CORS ayarlarını başarıyla yapmış olun.
- **İnternet Bağlantısı**: Gerekli paketleri indirmek ve projeleri senkronize etmek için stabil bir internet bağlantısı gereklidir.

### 5.10.2 Adım 1: Backend'e Ürün Ekleme Özelliğini Eklemek

#### 1. **IProductRepository Arayüzünü Güncelleme**

`IProductRepository` arayüzüne yeni bir yöntem ekleyerek ürün ekleme işlevini tanımlayacağız.

- **src/app/Repositories/IProductRepository.cs** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```csharp
    using Backend.Models;
    using System.Threading.Tasks;

    namespace Backend.Repositories
    {
        public interface IProductRepository
        {
            Task<IEnumerable<Product>> GetAllProductsAsync();
            Task<Product> AddProductAsync(Product product);
            // Diğer CRUD metotları buraya eklenebilir
        }
    }
    ```

#### 2. **ProductRepository Sınıfını Güncelleme**

`ProductRepository` sınıfını güncelleyerek yeni yöntemi implement edeceğiz.

- **src/app/Repositories/ProductRepository.cs** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```csharp
    using Backend.Data;
    using Backend.Models;
    using Microsoft.EntityFrameworkCore;
    using System.Collections.Generic;
    using System.Threading.Tasks;

    namespace Backend.Repositories
    {
        public class ProductRepository : IProductRepository
        {
            private readonly ApplicationDbContext _context;

            public ProductRepository(ApplicationDbContext context)
            {
                _context = context;
            }

            public async Task<IEnumerable<Product>> GetAllProductsAsync()
            {
                return await _context.Products.ToListAsync();
            }

            public async Task<Product> AddProductAsync(Product product)
            {
                _context.Products.Add(product);
                await _context.SaveChangesAsync();
                return product;
            }

            // Diğer CRUD metotları buraya eklenebilir
        }
    }
    ```

#### 3. **ProductsController'ı Güncelleme**

`ProductsController`'a yeni bir POST metodu ekleyerek ürün ekleme API'sini oluşturacağız.

- **src/app/Controllers/ProductsController.cs** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```csharp
    using Backend.Models;
    using Backend.Repositories;
    using Microsoft.AspNetCore.Mvc;
    using System.Collections.Generic;
    using System.Threading.Tasks;

    namespace Backend.Controllers
    {
        [Route("api/[controller]")]
        [ApiController]
        public class ProductsController : ControllerBase
        {
            private readonly IProductRepository _productRepository;

            public ProductsController(IProductRepository productRepository)
            {
                _productRepository = productRepository;
            }

            // GET: api/Products
            [HttpGet]
            public async Task<ActionResult<IEnumerable<Product>>> GetProducts()
            {
                var products = await _productRepository.GetAllProductsAsync();
                return Ok(products);
            }

            // POST: api/Products
            [HttpPost]
            public async Task<ActionResult<Product>> AddProduct([FromBody] Product product)
            {
                if (!ModelState.IsValid)
                {
                    return BadRequest(ModelState);
                }

                var createdProduct = await _productRepository.AddProductAsync(product);
                return CreatedAtAction(nameof(GetProducts), new { id = createdProduct.Id }, createdProduct);
            }

            // Diğer CRUD metotları buraya eklenebilir
        }
    }
    ```

#### 4. **Backend Projesini Güncelleme**

Yeni eklenen değişikliklerin veritabanına yansıması için migration oluşturup veritabanını güncelleyeceğiz.

1. **Package Manager Console'u Açma**
   - Visual Studio'da, üst menüden **Tools > NuGet Package Manager > Package Manager Console** yolunu izleyin.

2. **Migration Oluşturma**
   - **Package Manager Console** penceresinde aşağıdaki komutu çalıştırın:
     ```powershell
     Add-Migration AddProduct
     ```

3. **Veritabanını Güncelleme**
   - Migration tamamlandıktan sonra, aşağıdaki komutu çalıştırarak veritabanını güncelleyin:
     ```powershell
     Update-Database
     ```

#### 5. **Backend'i Test Etme**

API'nin çalıştığından emin olmak için Swagger veya Postman kullanarak yeni POST metodunu test edin.

1. **Projeyi Çalıştırma**
   - Visual Studio'da backend projesini başlatın (**F5** tuşuna basın veya **Debug > Start Debugging** seçeneğine tıklayın).

2. **Swagger UI ile Test Etme**
   - Tarayıcınızda Swagger UI açılacaktır (genellikle `https://localhost:5001/swagger`).
   - **Products** endpoint'ini bulun ve **POST** metodunu seçin.
   - **Try it out** butonuna tıklayın ve aşağıdaki gibi bir JSON payload girin:
     ```json
     {
       "productName": "Yeni Ürün",
       "price": 150.00,
       "stock": 30
     }
     ```
   - **Execute** butonuna tıklayın ve API'nin doğru şekilde çalıştığını doğrulayın.

### 5.10.3 Adım 2: UI'da Ürün Ekleme Sayfasını Oluşturma

#### 1. **Angular Servislerini Güncelleme**

`ProductService`'i güncelleyerek ürün ekleme işlevini ekleyeceğiz.

- **src/app/services/product.service.ts** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```typescript
    import { Injectable } from '@angular/core';
    import { HttpClient, HttpErrorResponse } from '@angular/common/http';
    import { Observable, throwError } from 'rxjs';
    import { catchError } from 'rxjs/operators';
    import { Product } from '../models/product.model';

    @Injectable({
      providedIn: 'root'
    })
    export class ProductService {
      private apiUrl = 'https://localhost:5001/api/Products'; // Backend API URL'si

      constructor(private http: HttpClient) { }

      getProducts(): Observable<Product[]> {
        return this.http.get<Product[]>(this.apiUrl)
          .pipe(
            catchError(this.handleError)
          );
      }

      addProduct(product: Product): Observable<Product> {
        return this.http.post<Product>(this.apiUrl, product)
          .pipe(
            catchError(this.handleError)
          );
      }

      private handleError(error: HttpErrorResponse) {
        if (error.error instanceof ErrorEvent) {
          // Client-side veya network hatası
          console.error('An error occurred:', error.error.message);
        } else {
          // Backend hatası
          console.error(
            `Backend returned code ${error.status}, ` +
            `body was: ${error.error}`);
        }
        // Kullanıcıya gösterilecek hata mesajını dön
        return throwError(
          'Something bad happened; please try again later.');
      }
    }
    ```

#### 2. **Ürün Ekleme Bileşeni Oluşturma**

Yeni bir bileşen oluşturarak ürün ekleme formunu tasarlayacağız.

1. **Yeni Bileşen Oluşturma**
   - Terminalde aşağıdaki komutu çalıştırarak `add-product` adlı yeni bir bileşen oluşturun:
     ```bash
     ng generate component add-product
     ```

2. **AddProduct Bileşenini Yapılandırma**
   - **src/app/add-product/add-product.component.ts** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```typescript
    import { Component } from '@angular/core';
    import { ProductService } from '../services/product.service';
    import { Product } from '../models/product.model';
    import { Router } from '@angular/router';

    @Component({
      selector: 'app-add-product',
      templateUrl: './add-product.component.html',
      styleUrls: ['./add-product.component.css']
    })
    export class AddProductComponent {
      product: Product = {
        id: 0,
        productName: '',
        price: 0,
        stock: 0
      };

      constructor(private productService: ProductService, private router: Router) { }

      addProduct(): void {
        if (this.product.productName && this.product.price > 0 && this.product.stock >= 0) {
          this.productService.addProduct(this.product).subscribe({
            next: () => this.router.navigate(['/products']),
            error: (err) => console.error(err)
          });
        } else {
          alert('Lütfen tüm alanları doğru şekilde doldurun.');
        }
      }
    }
    ```

3. **AddProduct Bileşeninin HTML Şablonunu Düzenleme**
   - **src/app/add-product/add-product.component.html** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```html
    <div class="container">
      <h2>Yeni Ürün Ekle</h2>
      <form (ngSubmit)="addProduct()">
        <div class="form-group">
          <label for="productName">Ürün Adı</label>
          <input type="text" id="productName" [(ngModel)]="product.productName" name="productName" class="form-control" required>
        </div>
        <div class="form-group">
          <label for="price">Fiyat</label>
          <input type="number" id="price" [(ngModel)]="product.price" name="price" class="form-control" required min="0.01" step="0.01">
        </div>
        <div class="form-group">
          <label for="stock">Stok</label>
          <input type="number" id="stock" [(ngModel)]="product.stock" name="stock" class="form-control" required min="0">
        </div>
        <button type="submit" class="btn btn-primary mt-3">Ekle</button>
      </form>
    </div>
    ```

#### 3. **Routing Ayarlarını Güncelleme**

Yeni oluşturduğumuz `AddProductComponent`'i uygulamaya eklemek için routing ayarlarını güncelleyeceğiz.

- **src/app/app-routing.module.ts** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```typescript
    import { NgModule } from '@angular/core';
    import { RouterModule, Routes } from '@angular/router';
    import { ProductsComponent } from './products/products.component';
    import { AddProductComponent } from './add-product/add-product.component';

    const routes: Routes = [
      { path: 'products', component: ProductsComponent },
      { path: 'add-product', component: AddProductComponent },
      { path: '', redirectTo: '/products', pathMatch: 'full' },
      { path: '**', redirectTo: '/products' }
    ];

    @NgModule({
      imports: [RouterModule.forRoot(routes)],
      exports: [RouterModule]
    })
    export class AppRoutingModule { }
    ```

- **src/app/app.module.ts** dosyasını açın ve `AppRoutingModule`'ü içe aktarın:

    ```typescript
    import { BrowserModule } from '@angular/platform-browser';
    import { NgModule } from '@angular/core';
    import { FormsModule } from '@angular/forms';
    import { HttpClientModule } from '@angular/common/http';

    import { AppRoutingModule } from './app-routing.module';
    import { AppComponent } from './app.component';
    import { ProductsComponent } from './products/products.component';
    import { AddProductComponent } from './add-product/add-product.component';

    @NgModule({
      declarations: [
        AppComponent,
        ProductsComponent,
        AddProductComponent
      ],
      imports: [
        BrowserModule,
        AppRoutingModule,
        FormsModule,
        HttpClientModule
      ],
      providers: [],
      bootstrap: [AppComponent]
    })
    export class AppModule { }
    ```

#### 4. **Navigation Bar Eklemek**

Kullanıcıların ürün ekleme sayfasına kolayca erişebilmesi için bir navigasyon bar ekleyeceğiz.

- **src/app/app.component.html** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```html
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="#">Product Management</a>
      <div class="collapse navbar-collapse">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item">
            <a class="nav-link" routerLink="/products">Ürünler</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" routerLink="/add-product">Yeni Ürün Ekle</a>
          </li>
        </ul>
      </div>
    </nav>
    <router-outlet></router-outlet>
    ```

#### 5. **UI Projesini Test Etme**

Yeni eklenen ürün ekleme özelliğini test ederek her şeyin doğru çalıştığından emin olacağız.

1. **Angular Uygulamasını Çalıştırma**
   - Terminalde aşağıdaki komutu çalıştırarak Angular uygulamasını başlatın:
     ```bash
     ng serve
     ```
   - Tarayıcınızda `http://localhost:4200` adresine gidin.

2. **Ürün Ekleme İşlemini Test Etme**
   - Navigasyon barından **"Yeni Ürün Ekle"** sekmesine tıklayın.
   - Açılan formu doldurun ve **"Ekle"** butonuna tıklayın.
   - Formun başarıyla gönderildiğini ve yeni ürünün ürünler listesinde göründüğünü doğrulayın.

3. **Backend ve UI Arasındaki Bağlantıyı Doğrulama**
   - Backend API'sinin doğru çalıştığından ve UI'nın bu API ile doğru şekilde iletişim kurduğundan emin olun.
   - Herhangi bir hata durumunda, tarayıcı konsolunu ve backend loglarını kontrol ederek sorunları tespit edin.

### 5.10.4 Lab-10'un Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak **ProductManagement** projesine ürün ekleme özelliğini başarıyla eklemiş oldunuz. **Backend** tarafında gerekli API endpoint'lerini oluşturup veritabanı işlemlerini yapılandırdınız, **UI** tarafında ise Angular ile kullanıcı dostu bir ürün ekleme formu oluşturarak frontend ve backend arasındaki entegrasyonu sağladınız. Bu adımlar, sisteminize dinamik veri ekleme ve yönetme yetenekleri kazandırarak kullanıcı deneyimini geliştirmiştir. Bir sonraki laboratuvar çalışmasında, ürün güncelleme ve silme gibi ek işlevleri projeye entegre etmeye devam edeceğiz.

---

**Not:** Angular projenizin backend API'sine erişebilmesi için CORS ayarlarının doğru yapılandırıldığından emin olun. Ayrıca, `apiUrl` değişkeninin doğru backend URL'sini işaret ettiğinden emin olun.

## 5.11 Lab-11: Ürün Güncelleme Özelliğini Backend ve UI'ye Eklemek

Bu laboratuvar çalışmasında, **ProductManagement** projesine ürün güncelleme özelliği ekleyeceğiz. Bu adımda, **Backend** (ASP.NET Core) tarafında gerekli API endpoint'lerini oluşturacak ve **UI** (Angular 18) tarafında ürün güncelleme formunu tasarlayarak mevcut ürünleri düzenlemeye olanak tanıyacağız. Bu adımlar, kullanıcıların mevcut ürün bilgilerini güncelleyebilmesini sağlayarak sistemin esnekliğini artıracaktır.

### 5.11.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Lab-1'den Lab-10'a Kadar Tüm Laboratuvarların Tamamlanması**: Önceki laboratuvar adımlarını başarıyla tamamlamış olun.
- **Visual Studio Code (VSCode)**: [Download](https://code.visualstudio.com/) edilerek kurulmuş ve yapılandırılmış olmalı.
- **Backend Projesi Çalışır Durumda Olmalı**: ASP.NET Core backend projenizin çalışır durumda ve `ProductManagementDB` veritabanına bağlı olduğundan emin olun.
- **CORS Ayarları Yapılandırılmış Olmalı**: Lab-9'da CORS ayarlarını başarıyla yapmış olun.
- **İnternet Bağlantısı**: Gerekli paketleri indirmek ve projeleri senkronize etmek için stabil bir internet bağlantısı gereklidir.

### 5.11.2 Adım 1: Backend'e Ürün Güncelleme Özelliğini Eklemek

#### 1. **IProductRepository Arayüzünü Güncelleme**

`IProductRepository` arayüzüne yeni bir yöntem ekleyerek ürün güncelleme işlevini tanımlayacağız.

- **src/app/Repositories/IProductRepository.cs** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```csharp
    using Backend.Models;
    using System.Threading.Tasks;

    namespace Backend.Repositories
    {
        public interface IProductRepository
        {
            Task<IEnumerable<Product>> GetAllProductsAsync();
            Task<Product> AddProductAsync(Product product);
            Task<Product> UpdateProductAsync(Product product); // Yeni eklenen yöntem
            // Diğer CRUD metotları buraya eklenebilir
        }
    }
    ```

#### 2. **ProductRepository Sınıfını Güncelleme**

`ProductRepository` sınıfını güncelleyerek yeni yöntemi implement edeceğiz.

- **src/app/Repositories/ProductRepository.cs** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```csharp
    using Backend.Data;
    using Backend.Models;
    using Microsoft.EntityFrameworkCore;
    using System.Collections.Generic;
    using System.Threading.Tasks;

    namespace Backend.Repositories
    {
        public class ProductRepository : IProductRepository
        {
            private readonly ApplicationDbContext _context;

            public ProductRepository(ApplicationDbContext context)
            {
                _context = context;
            }

            public async Task<IEnumerable<Product>> GetAllProductsAsync()
            {
                return await _context.Products.ToListAsync();
            }

            public async Task<Product> AddProductAsync(Product product)
            {
                _context.Products.Add(product);
                await _context.SaveChangesAsync();
                return product;
            }

            public async Task<Product> UpdateProductAsync(Product product)
            {
                var existingProduct = await _context.Products.FindAsync(product.Id);
                if (existingProduct == null)
                {
                    return null;
                }

                existingProduct.ProductName = product.ProductName;
                existingProduct.Price = product.Price;
                existingProduct.Stock = product.Stock;

                await _context.SaveChangesAsync();
                return existingProduct;
            }

            // Diğer CRUD metotları buraya eklenebilir
        }
    }
    ```

#### 3. **ProductsController'ı Güncelleme**

`ProductsController`'a yeni bir PUT metodu ekleyerek ürün güncelleme API'sini oluşturacağız.

- **src/app/Controllers/ProductsController.cs** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```csharp
    using Backend.Models;
    using Backend.Repositories;
    using Microsoft.AspNetCore.Mvc;
    using System.Collections.Generic;
    using System.Threading.Tasks;

    namespace Backend.Controllers
    {
        [Route("api/[controller]")]
        [ApiController]
        public class ProductsController : ControllerBase
        {
            private readonly IProductRepository _productRepository;

            public ProductsController(IProductRepository productRepository)
            {
                _productRepository = productRepository;
            }

            // GET: api/Products
            [HttpGet]
            public async Task<ActionResult<IEnumerable<Product>>> GetProducts()
            {
                var products = await _productRepository.GetAllProductsAsync();
                return Ok(products);
            }

            // POST: api/Products
            [HttpPost]
            public async Task<ActionResult<Product>> AddProduct([FromBody] Product product)
            {
                if (!ModelState.IsValid)
                {
                    return BadRequest(ModelState);
                }

                var createdProduct = await _productRepository.AddProductAsync(product);
                return CreatedAtAction(nameof(GetProducts), new { id = createdProduct.Id }, createdProduct);
            }

            // PUT: api/Products/{id}
            [HttpPut("{id}")]
            public async Task<ActionResult<Product>> UpdateProduct(int id, [FromBody] Product product)
            {
                if (id != product.Id)
                {
                    return BadRequest("Ürün ID'si uyuşmuyor.");
                }

                if (!ModelState.IsValid)
                {
                    return BadRequest(ModelState);
                }

                var updatedProduct = await _productRepository.UpdateProductAsync(product);
                if (updatedProduct == null)
                {
                    return NotFound();
                }

                return Ok(updatedProduct);
            }

            // Diğer CRUD metotları buraya eklenebilir
        }
    }
    ```

#### 4. **Backend Projesini Güncelleme**

Yeni eklenen değişikliklerin veritabanına yansıması için migration oluşturup veritabanını güncelleyeceğiz.

1. **Package Manager Console'u Açma**
   - Visual Studio'da, üst menüden **Tools > NuGet Package Manager > Package Manager Console** yolunu izleyin.

2. **Migration Oluşturma**
   - **Package Manager Console** penceresinde aşağıdaki komutu çalıştırın:
     ```powershell
     Add-Migration AddUpdateProduct
     ```

3. **Veritabanını Güncelleme**
   - Migration tamamlandıktan sonra, aşağıdaki komutu çalıştırarak veritabanını güncelleyin:
     ```powershell
     Update-Database
     ```

#### 5. **Backend'i Test Etme**

API'nin çalıştığından emin olmak için Swagger veya Postman kullanarak yeni PUT metodunu test edin.

1. **Projeyi Çalıştırma**
   - Visual Studio'da backend projesini başlatın (**F5** tuşuna basın veya **Debug > Start Debugging** seçeneğine tıklayın).

2. **Swagger UI ile Test Etme**
   - Tarayıcınızda Swagger UI açılacaktır (genellikle `https://localhost:5001/swagger`).
   - **Products** endpoint'ini bulun ve **PUT** metodunu seçin.
   - **Try it out** butonuna tıklayın ve URL kısmına güncellemek istediğiniz ürünün ID'sini girin (örneğin, `1`).
   - Aşağıdaki gibi bir JSON payload girin:
     ```json
     {
       "id": 1,
       "productName": "Güncellenmiş Ürün",
       "price": 200.00,
       "stock": 50
     }
     ```
   - **Execute** butonuna tıklayın ve API'nin doğru şekilde çalıştığını doğrulayın.

### 5.11.3 Adım 2: UI'da Ürün Güncelleme Sayfasını Oluşturma

#### 1. **Angular Servislerini Güncelleme**

`ProductService`'i güncelleyerek ürün güncelleme işlevini ekleyeceğiz.

- **src/app/services/product.service.ts** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```typescript
    import { Injectable } from '@angular/core';
    import { HttpClient, HttpErrorResponse } from '@angular/common/http';
    import { Observable, throwError } from 'rxjs';
    import { catchError } from 'rxjs/operators';
    import { Product } from '../models/product.model';

    @Injectable({
      providedIn: 'root'
    })
    export class ProductService {
      private apiUrl = 'https://localhost:5001/api/Products'; // Backend API URL'si

      constructor(private http: HttpClient) { }

      getProducts(): Observable<Product[]> {
        return this.http.get<Product[]>(this.apiUrl)
          .pipe(
            catchError(this.handleError)
          );
      }

      addProduct(product: Product): Observable<Product> {
        return this.http.post<Product>(this.apiUrl, product)
          .pipe(
            catchError(this.handleError)
          );
      }

      updateProduct(product: Product): Observable<Product> {
        const url = `${this.apiUrl}/${product.id}`;
        return this.http.put<Product>(url, product)
          .pipe(
            catchError(this.handleError)
          );
      }

      private handleError(error: HttpErrorResponse) {
        if (error.error instanceof ErrorEvent) {
          // Client-side veya network hatası
          console.error('An error occurred:', error.error.message);
        } else {
          // Backend hatası
          console.error(
            `Backend returned code ${error.status}, ` +
            `body was: ${error.error}`);
        }
        // Kullanıcıya gösterilecek hata mesajını dön
        return throwError(
          'Something bad happened; please try again later.');
      }
    }
    ```

#### 2. **Ürün Güncelleme Bileşeni Oluşturma**

Mevcut ürünleri düzenlemek için yeni bir bileşen oluşturacağız.

1. **Yeni Bileşen Oluşturma**
   - Terminalde aşağıdaki komutu çalıştırarak `edit-product` adlı yeni bir bileşen oluşturun:
     ```bash
     ng generate component edit-product
     ```
   - Bu komut, `src/app/edit-product` dizini altında gerekli dosyaları oluşturacaktır.

2. **EditProduct Bileşenini Yapılandırma**
   - **src/app/edit-product/edit-product.component.ts** dosyasını açın ve aşağıdaki kodu ekleyin:

     ```typescript
     import { Component, OnInit } from '@angular/core';
     import { ActivatedRoute, Router } from '@angular/router';
     import { ProductService } from '../services/product.service';
     import { Product } from '../models/product.model';

     @Component({
       selector: 'app-edit-product',
       templateUrl: './edit-product.component.html',
       styleUrls: ['./edit-product.component.css']
     })
     export class EditProductComponent implements OnInit {
       product: Product = {
         id: 0,
         productName: '',
         price: 0,
         stock: 0
       };

       constructor(
         private route: ActivatedRoute,
         private router: Router,
         private productService: ProductService
       ) { }

       ngOnInit(): void {
         const id = Number(this.route.snapshot.paramMap.get('id'));
         if (id) {
           this.productService.getProducts().subscribe({
             next: (products) => {
               const foundProduct = products.find(p => p.id === id);
               if (foundProduct) {
                 this.product = foundProduct;
               } else {
                 alert('Ürün bulunamadı.');
                 this.router.navigate(['/products']);
               }
             },
             error: (err) => console.error(err)
           });
         } else {
           alert('Geçersiz ürün ID\'si.');
           this.router.navigate(['/products']);
         }
       }

       updateProduct(): void {
         if (this.product.productName && this.product.price > 0 && this.product.stock >= 0) {
           this.productService.updateProduct(this.product).subscribe({
             next: () => {
               alert('Ürün başarıyla güncellendi.');
               this.router.navigate(['/products']);
             },
             error: (err) => console.error(err)
           });
         } else {
           alert('Lütfen tüm alanları doğru şekilde doldurun.');
         }
       }
     }
     ```

3. **EditProduct Bileşeninin HTML Şablonunu Düzenleme**
   - **src/app/edit-product/edit-product.component.html** dosyasını açın ve aşağıdaki kodu ekleyin:

     ```html
     <div class="container">
       <h2>Ürün Güncelle</h2>
       <form (ngSubmit)="updateProduct()">
         <div class="form-group">
           <label for="productName">Ürün Adı</label>
           <input type="text" id="productName" [(ngModel)]="product.productName" name="productName" class="form-control" required>
         </div>
         <div class="form-group">
           <label for="price">Fiyat</label>
           <input type="number" id="price" [(ngModel)]="product.price" name="price" class="form-control" required min="0.01" step="0.01">
         </div>
         <div class="form-group">
           <label for="stock">Stok</label>
           <input type="number" id="stock" [(ngModel)]="product.stock" name="stock" class="form-control" required min="0">
         </div>
         <button type="submit" class="btn btn-primary mt-3">Güncelle</button>
       </form>
     </div>
     ```

#### 3. **Routing Ayarlarını Güncelleme**

Yeni oluşturduğumuz `EditProductComponent`'i uygulamaya eklemek için routing ayarlarını güncelleyeceğiz.

- **src/app/app-routing.module.ts** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```typescript
    import { NgModule } from '@angular/core';
    import { RouterModule, Routes } from '@angular/router';
    import { ProductsComponent } from './products/products.component';
    import { AddProductComponent } from './add-product/add-product.component';
    import { EditProductComponent } from './edit-product/edit-product.component';

    const routes: Routes = [
      { path: 'products', component: ProductsComponent },
      { path: 'add-product', component: AddProductComponent },
      { path: 'edit-product/:id', component: EditProductComponent }, // Yeni eklenen route
      { path: '', redirectTo: '/products', pathMatch: 'full' },
      { path: '**', redirectTo: '/products' }
    ];

    @NgModule({
      imports: [RouterModule.forRoot(routes)],
      exports: [RouterModule]
    })
    export class AppRoutingModule { }
    ```

- **src/app/app.module.ts** dosyasını açın ve `EditProductComponent`'i içe aktarın:

    ```typescript
    import { BrowserModule } from '@angular/platform-browser';
    import { NgModule } from '@angular/core';
    import { FormsModule } from '@angular/forms';
    import { HttpClientModule } from '@angular/common/http';

    import { AppRoutingModule } from './app-routing.module';
    import { AppComponent } from './app.component';
    import { ProductsComponent } from './products/products.component';
    import { AddProductComponent } from './add-product/add-product.component';
    import { EditProductComponent } from './edit-product/edit-product.component'; // Yeni eklenen bileşen

    @NgModule({
      declarations: [
        AppComponent,
        ProductsComponent,
        AddProductComponent,
        EditProductComponent
      ],
      imports: [
        BrowserModule,
        AppRoutingModule,
        FormsModule,
        HttpClientModule
      ],
      providers: [],
      bootstrap: [AppComponent]
    })
    export class AppModule { }
    ```

#### 4. **Ürün Listesi Bileşenini Güncelleme**

Ürünler listesini güncelleyerek her ürün için düzenleme bağlantısı ekleyeceğiz.

- **src/app/products/products.component.html** dosyasını açın ve aşağıdaki kodu düzenleyin:

    ```html
    <div class="container">
      <h2>Ürünler Listesi</h2>
      <table class="table table-striped">
        <thead>
          <tr>
            <th>ID</th>
            <th>Ürün Adı</th>
            <th>Fiyat</th>
            <th>Stok</th>
            <th>İşlemler</th> <!-- Yeni sütun -->
          </tr>
        </thead>
        <tbody>
          <tr *ngFor="let product of products">
            <td>{{ product.id }}</td>
            <td>{{ product.productName }}</td>
            <td>{{ product.price | currency }}</td>
            <td>{{ product.stock }}</td>
            <td>
              <a [routerLink]="['/edit-product', product.id]" class="btn btn-sm btn-secondary">Güncelle</a>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    ```

#### 5. **UI Projesini Test Etme**

Yeni eklenen ürün güncelleme özelliğini test ederek her şeyin doğru çalıştığından emin olacağız.

1. **Angular Uygulamasını Çalıştırma**
   - Terminalde aşağıdaki komutu çalıştırarak Angular uygulamasını başlatın:
     ```bash
     ng serve
     ```
   - Tarayıcınızda `http://localhost:4200` adresine gidin.

2. **Ürün Güncelleme İşlemini Test Etme**
   - **Ürünler** sayfasından güncellemek istediğiniz bir ürünü seçin ve **"Güncelle"** butonuna tıklayın.
   - Açılan formu düzenleyin ve **"Güncelle"** butonuna tıklayın.
   - Formun başarıyla gönderildiğini ve güncellenen ürünün ürünler listesinde göründüğünü doğrulayın.

3. **Backend ve UI Arasındaki Bağlantıyı Doğrulama**
   - Backend API'sinin doğru çalıştığından ve UI'nın bu API ile doğru şekilde iletişim kurduğundan emin olun.
   - Herhangi bir hata durumunda, tarayıcı konsolunu ve backend loglarını kontrol ederek sorunları tespit edin.

### 5.11.4 Lab-11'in Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak **ProductManagement** projesine ürün güncelleme özelliğini başarıyla eklemiş oldunuz. **Backend** tarafında gerekli API endpoint'lerini oluşturup veritabanı işlemlerini yapılandırdınız, **UI** tarafında ise Angular ile kullanıcı dostu bir ürün güncelleme formu oluşturarak frontend ve backend arasındaki entegrasyonu sağladınız. Bu adımlar, sisteminize mevcut verileri düzenleme yeteneği kazandırarak kullanıcı deneyimini daha da iyileştirmiştir. Bir sonraki laboratuvar çalışmasında, ürün silme gibi ek işlevleri projeye entegre etmeye devam edeceğiz.

---

**Not:** Angular projenizin backend API'sine erişebilmesi için CORS ayarlarının doğru yapılandırıldığından emin olun. Ayrıca, `apiUrl` değişkeninin doğru backend URL'sini işaret ettiğinden emin olun.

## 5.12 Lab-12: Ürün Silme Özelliğini Backend ve UI'ye Eklemek

Bu laboratuvar çalışmasında, **ProductManagement** projesine ürün silme özelliği ekleyeceğiz. Bu adımda, **Backend** (ASP.NET Core) tarafında gerekli API endpoint'lerini oluşturacak ve **UI** (Angular 18) tarafında ürün silme butonunu ekleyerek kullanıcıların ürünleri silmesine olanak tanıyacağız. Silme işlemi sırasında kullanıcıdan onay alarak yanlışlıkla silmeleri önleyeceğiz. Bu adımlar, sistemin veri yönetimini tamamlayarak tam CRUD (Create, Read, Update, Delete) işlevselliği sağlamasını sağlayacaktır.

### 5.12.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Lab-1'den Lab-11'e Kadar Tüm Laboratuvarların Tamamlanması**: Önceki laboratuvar adımlarını başarıyla tamamlamış olun.
- **Visual Studio Code (VSCode)**: [Download](https://code.visualstudio.com/) edilerek kurulmuş ve yapılandırılmış olmalı.
- **Backend Projesi Çalışır Durumda Olmalı**: ASP.NET Core backend projenizin çalışır durumda ve `ProductManagementDB` veritabanına bağlı olduğundan emin olun.
- **CORS Ayarları Yapılandırılmış Olmalı**: Lab-9'da CORS ayarlarını başarıyla yapmış olun.
- **İnternet Bağlantısı**: Gerekli paketleri indirmek ve projeleri senkronize etmek için stabil bir internet bağlantısı gereklidir.

### 5.12.2 Adım 1: Backend'e Ürün Silme Özelliğini Eklemek

#### 1. **IProductRepository Arayüzünü Güncelleme**

`IProductRepository` arayüzüne yeni bir yöntem ekleyerek ürün silme işlevini tanımlayacağız.

- **src/app/Repositories/IProductRepository.cs** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```csharp
    using Backend.Models;
    using System.Threading.Tasks;

    namespace Backend.Repositories
    {
        public interface IProductRepository
        {
            Task<IEnumerable<Product>> GetAllProductsAsync();
            Task<Product> AddProductAsync(Product product);
            Task<Product> UpdateProductAsync(Product product);
            Task<bool> DeleteProductAsync(int id); // Yeni eklenen yöntem
            // Diğer CRUD metotları buraya eklenebilir
        }
    }
    ```

#### 2. **ProductRepository Sınıfını Güncelleme**

`ProductRepository` sınıfını güncelleyerek yeni yöntemi implement edeceğiz.

- **src/app/Repositories/ProductRepository.cs** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```csharp
    using Backend.Data;
    using Backend.Models;
    using Microsoft.EntityFrameworkCore;
    using System.Collections.Generic;
    using System.Threading.Tasks;

    namespace Backend.Repositories
    {
        public class ProductRepository : IProductRepository
        {
            private readonly ApplicationDbContext _context;

            public ProductRepository(ApplicationDbContext context)
            {
                _context = context;
            }

            public async Task<IEnumerable<Product>> GetAllProductsAsync()
            {
                return await _context.Products.ToListAsync();
            }

            public async Task<Product> AddProductAsync(Product product)
            {
                _context.Products.Add(product);
                await _context.SaveChangesAsync();
                return product;
            }

            public async Task<Product> UpdateProductAsync(Product product)
            {
                var existingProduct = await _context.Products.FindAsync(product.Id);
                if (existingProduct == null)
                {
                    return null;
                }

                existingProduct.ProductName = product.ProductName;
                existingProduct.Price = product.Price;
                existingProduct.Stock = product.Stock;

                await _context.SaveChangesAsync();
                return existingProduct;
            }

            public async Task<bool> DeleteProductAsync(int id)
            {
                var product = await _context.Products.FindAsync(id);
                if (product == null)
                {
                    return false;
                }

                _context.Products.Remove(product);
                await _context.SaveChangesAsync();
                return true;
            }

            // Diğer CRUD metotları buraya eklenebilir
        }
    }
    ```

#### 3. **ProductsController'ı Güncelleme**

`ProductsController`'a yeni bir DELETE metodu ekleyerek ürün silme API'sini oluşturacağız.

- **src/app/Controllers/ProductsController.cs** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```csharp
    using Backend.Models;
    using Backend.Repositories;
    using Microsoft.AspNetCore.Mvc;
    using System.Collections.Generic;
    using System.Threading.Tasks;

    namespace Backend.Controllers
    {
        [Route("api/[controller]")]
        [ApiController]
        public class ProductsController : ControllerBase
        {
            private readonly IProductRepository _productRepository;

            public ProductsController(IProductRepository productRepository)
            {
                _productRepository = productRepository;
            }

            // GET: api/Products
            [HttpGet]
            public async Task<ActionResult<IEnumerable<Product>>> GetProducts()
            {
                var products = await _productRepository.GetAllProductsAsync();
                return Ok(products);
            }

            // POST: api/Products
            [HttpPost]
            public async Task<ActionResult<Product>> AddProduct([FromBody] Product product)
            {
                if (!ModelState.IsValid)
                {
                    return BadRequest(ModelState);
                }

                var createdProduct = await _productRepository.AddProductAsync(product);
                return CreatedAtAction(nameof(GetProducts), new { id = createdProduct.Id }, createdProduct);
            }

            // PUT: api/Products/{id}
            [HttpPut("{id}")]
            public async Task<ActionResult<Product>> UpdateProduct(int id, [FromBody] Product product)
            {
                if (id != product.Id)
                {
                    return BadRequest("Ürün ID'si uyuşmuyor.");
                }

                if (!ModelState.IsValid)
                {
                    return BadRequest(ModelState);
                }

                var updatedProduct = await _productRepository.UpdateProductAsync(product);
                if (updatedProduct == null)
                {
                    return NotFound();
                }

                return Ok(updatedProduct);
            }

            // DELETE: api/Products/{id}
            [HttpDelete("{id}")]
            public async Task<IActionResult> DeleteProduct(int id)
            {
                var result = await _productRepository.DeleteProductAsync(id);
                if (!result)
                {
                    return NotFound();
                }

                return NoContent();
            }

            // Diğer CRUD metotları buraya eklenebilir
        }
    }
    ```

#### 4. **Backend Projesini Güncelleme**

Yeni eklenen değişikliklerin veritabanına yansıması için migration oluşturup veritabanını güncelleyeceğiz.

1. **Package Manager Console'u Açma**
   - Visual Studio'da, üst menüden **Tools > NuGet Package Manager > Package Manager Console** yolunu izleyin.

2. **Migration Oluşturma**
   - **Package Manager Console** penceresinde aşağıdaki komutu çalıştırın:
     ```powershell
     Add-Migration AddDeleteProduct
     ```

3. **Veritabanını Güncelleme**
   - Migration tamamlandıktan sonra, aşağıdaki komutu çalıştırarak veritabanını güncelleyin:
     ```powershell
     Update-Database
     ```

#### 5. **Backend'i Test Etme**

API'nin çalıştığından emin olmak için Swagger veya Postman kullanarak yeni DELETE metodunu test edin.

1. **Projeyi Çalıştırma**
   - Visual Studio'da backend projesini başlatın (**F5** tuşuna basın veya **Debug > Start Debugging** seçeneğine tıklayın).

2. **Swagger UI ile Test Etme**
   - Tarayıcınızda Swagger UI açılacaktır (genellikle `https://localhost:5001/swagger`).
   - **Products** endpoint'ini bulun ve **DELETE** metodunu seçin.
   - **Try it out** butonuna tıklayın ve URL kısmına silmek istediğiniz ürünün ID'sini girin (örneğin, `1`).
   - **Execute** butonuna tıklayın ve API'nin doğru şekilde çalıştığını doğrulayın.

3. **Postman ile Test Etme**
   - `https://localhost:5001/api/Products/{id}` adresine bir DELETE isteği gönderin.

### 5.12.3 Adım 2: UI'da Ürün Silme Butonunu Oluşturma

#### 1. **Angular Servislerini Güncelleme**

`ProductService`'i güncelleyerek ürün silme işlevini ekleyeceğiz.

- **src/app/services/product.service.ts** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```typescript
    import { Injectable } from '@angular/core';
    import { HttpClient, HttpErrorResponse } from '@angular/common/http';
    import { Observable, throwError } from 'rxjs';
    import { catchError } from 'rxjs/operators';
    import { Product } from '../models/product.model';

    @Injectable({
      providedIn: 'root'
    })
    export class ProductService {
      private apiUrl = 'https://localhost:5001/api/Products'; // Backend API URL'si

      constructor(private http: HttpClient) { }

      getProducts(): Observable<Product[]> {
        return this.http.get<Product[]>(this.apiUrl)
          .pipe(
            catchError(this.handleError)
          );
      }

      addProduct(product: Product): Observable<Product> {
        return this.http.post<Product>(this.apiUrl, product)
          .pipe(
            catchError(this.handleError)
          );
      }

      updateProduct(product: Product): Observable<Product> {
        const url = `${this.apiUrl}/${product.id}`;
        return this.http.put<Product>(url, product)
          .pipe(
            catchError(this.handleError)
          );
      }

      deleteProduct(id: number): Observable<void> {
        const url = `${this.apiUrl}/${id}`;
        return this.http.delete<void>(url)
          .pipe(
            catchError(this.handleError)
          );
      }

      private handleError(error: HttpErrorResponse) {
        if (error.error instanceof ErrorEvent) {
          // Client-side veya network hatası
          console.error('An error occurred:', error.error.message);
        } else {
          // Backend hatası
          console.error(
            `Backend returned code ${error.status}, ` +
            `body was: ${error.error}`);
        }
        // Kullanıcıya gösterilecek hata mesajını dön
        return throwError(
          'Something bad happened; please try again later.');
      }
    }
    ```

#### 2. **Ürün Listesi Bileşenini Güncelleme**

Ürünler listesini güncelleyerek her ürün için silme butonu ekleyeceğiz ve silme işlemi sırasında onay alacağız.

- **src/app/products/products.component.ts** dosyasını açın ve aşağıdaki kodu ekleyin:

    ```typescript
    import { Component, OnInit } from '@angular/core';
    import { ProductService } from '../services/product.service';
    import { Product } from '../models/product.model';
    import { Router } from '@angular/router';

    @Component({
      selector: 'app-products',
      templateUrl: './products.component.html',
      styleUrls: ['./products.component.css']
    })
    export class ProductsComponent implements OnInit {
      products: Product[] = [];

      constructor(private productService: ProductService, private router: Router) { }

      ngOnInit(): void {
        this.loadProducts();
      }

      loadProducts(): void {
        this.productService.getProducts().subscribe({
          next: (data) => this.products = data,
          error: (err) => console.error(err)
        });
      }

      deleteProduct(id: number): void {
        const confirmDelete = confirm('Bu ürünü silmek istediğinize emin misiniz?');
        if (confirmDelete) {
          this.productService.deleteProduct(id).subscribe({
            next: () => {
              alert('Ürün başarıyla silindi.');
              this.loadProducts();
            },
            error: (err) => console.error(err)
          });
        }
      }
    }
    ```

- **src/app/products/products.component.html** dosyasını açın ve aşağıdaki kodu düzenleyin:

    ```html
    <div class="container">
      <h2>Ürünler Listesi</h2>
      <table class="table table-striped">
        <thead>
          <tr>
            <th>ID</th>
            <th>Ürün Adı</th>
            <th>Fiyat</th>
            <th>Stok</th>
            <th>İşlemler</th>
          </tr>
        </thead>
        <tbody>
          <tr *ngFor="let product of products">
            <td>{{ product.id }}</td>
            <td>{{ product.productName }}</td>
            <td>{{ product.price | currency }}</td>
            <td>{{ product.stock }}</td>
            <td>
              <a [routerLink]="['/edit-product', product.id]" class="btn btn-sm btn-secondary">Güncelle</a>
              <button (click)="deleteProduct(product.id)" class="btn btn-sm btn-danger ml-2">Sil</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    ```

#### 3. **UI Projesini Güncelleme**

Projenizin diğer kısımlarının zaten yapılandırılmış olduğunu varsayarak, yukarıdaki adımlar yeterli olacaktır. Ancak, stil ve ek özellikler eklemek isterseniz, CSS dosyalarını düzenleyebilirsiniz.

### 5.12.4 Lab-12'nin Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak **ProductManagement** projesine ürün silme özelliğini başarıyla eklemiş oldunuz. **Backend** tarafında gerekli API endpoint'lerini oluşturup veritabanı işlemlerini yapılandırdınız, **UI** tarafında ise Angular ile kullanıcı dostu bir ürün silme butonu ekleyerek frontend ve backend arasındaki entegrasyonu tamamladınız. Silme işlemi sırasında kullanıcıdan onay alarak veri güvenliğini artırdınız. Bu adımlar, sisteminize tam CRUD işlevselliği kazandırarak kullanıcı deneyimini ve veri yönetimini geliştirmiştir. Bir sonraki laboratuvar çalışmasında, sistemin güvenliğini artırmak için kimlik doğrulama ve yetkilendirme gibi ek özellikleri projeye entegre etmeye devam edeceğiz.

---

**Not:** Angular projenizin backend API'sine erişebilmesi için CORS ayarlarının doğru yapılandırıldığından emin olun. Ayrıca, `apiUrl` değişkeninin doğru backend URL'sini işaret ettiğinden emin olun.

## 5.13 Lab-13: Tüm Değişiklikleri Commit/Push Yapma, PR Oluşturma ve Main'e Merge Etme

Bu laboratuvar çalışmasında, **ProductManagement** projesindeki tüm değişiklikleri Git kullanarak commit ve push edeceğiz. Ardından, GitHub üzerinde bir Pull Request (PR) oluşturacak ve bu PR'yi **main** dalına (branch) merge edeceğiz. Bu adımlar, projenizin versiyon kontrolünü yönetmek ve takım çalışmasını kolaylaştırmak için gereklidir.

### 5.13.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Lab-1'den Lab-12'ye Kadar Tüm Laboratuvarların Tamamlanması**: Önceki laboratuvar adımlarını başarıyla tamamlamış olun.
- **Git Kurulu Olmalı**: Bilgisayarınızda [Git](https://git-scm.com/downloads) yüklü ve yapılandırılmış olmalı.
- **GitHub Hesabı**: [GitHub](https://github.com/) hesabınızın olması gerekmektedir.
- **Uzak (Remote) Repository Oluşturulmuş Olmalı**: GitHub üzerinde projeniz için bir repository oluşturmuş olun.
- **VSCode veya Tercih Ettiğiniz Bir Kod Editörü**: [Visual Studio Code](https://code.visualstudio.com/) gibi bir kod editörü kullanmanız önerilir.
- **İnternet Bağlantısı**: Değişiklikleri push etmek ve PR oluşturmak için aktif bir internet bağlantısına sahip olun.

### 5.13.2 Adım 1: Git Repository'yi Başlatma

Eğer projeniz için bir Git repository'si henüz başlatılmadıysa, aşağıdaki adımları izleyin.

1. **Terminali Açma**
   - VSCode'da veya bilgisayarınızdaki terminali açın.

2. **Proje Dizini'ne Gitme**
   - Aşağıdaki komutla projenizin kök dizinine gidin:
     ```bash
     cd path/to/ProductManagement
     ```

3. **Git Repository Başlatma**
   - Git repository'sini başlatmak için şu komutu çalıştırın:
     ```bash
     git init
     ```

4. **Uzak Repository Ekleme**
   - GitHub üzerinde oluşturduğunuz repository'nin URL'sini kullanarak uzak repository'yi ekleyin:
     ```bash
     git remote add origin https://github.com/kullanici-adi/ProductManagement.git
     ```

### 5.13.3 Adım 2: Değişiklikleri Stage Etme

Projede yaptığınız tüm değişiklikleri Git'e eklemek için aşağıdaki adımları izleyin.

1. **Tüm Değişiklikleri Stage Etme**
   - Tüm değişiklikleri stage etmek için şu komutu kullanın:
     ```bash
     git add .
     ```
   - Alternatif olarak, belirli dosyaları eklemek için:
     ```bash
     git add src/app/add-product/add-product.component.ts
     ```

### 5.13.4 Adım 3: Değişiklikleri Commit Etme

Stage edilen değişiklikleri commit etmek için aşağıdaki adımları izleyin.

1. **Commit Mesajı ile Commit Etme**
   - Anlamlı bir commit mesajı ile değişiklikleri commit edin:
     ```bash
     git commit -m "Ürün ekleme, güncelleme ve silme özelliklerini ekledim"
     ```

### 5.13.5 Adım 4: Değişiklikleri Push Etme

Commit ettiğiniz değişiklikleri GitHub üzerindeki uzak repository'ye push edeceğiz.

1. **Değişiklikleri Push Etme**
   - İlk push işlemi için aşağıdaki komutu kullanın:
     ```bash
     git push -u origin main
     ```
   - Eğer ana dalınız **main** değilse, doğru dal adını kullanın (örneğin, **master**).

### 5.13.6 Adım 5: Pull Request (PR) Oluşturma

Değişikliklerinizi ana dal ile birleştirmek için bir Pull Request oluşturacağız.

1. **GitHub'da Repository'yi Açma**
   - Tarayıcınızda GitHub hesabınıza giriş yapın ve projenizin repository'sini açın.

2. **Compare & Pull Request Butonuna Tıklama**
   - Repository ana sayfasında, yapılan push sonrası görünen "Compare & pull request" butonuna tıklayın.

3. **PR Başlığını ve Açıklamasını Girme**
   - PR için anlamlı bir başlık ve açıklama yazın:
     - **Başlık**: Ürün Ekleme, Güncelleme ve Silme Özellikleri
     - **Açıklama**:
       ```
       Bu PR ile ürün ekleme, güncelleme ve silme özelliklerini projeye ekledim. Backend tarafında gerekli API endpoint'lerini oluşturup, UI tarafında da Angular bileşenlerini güncelledim. Ayrıca, kullanıcı onayı ile ürün silme işlemini gerçekleştirdim.
       ```

4. **Create Pull Request Butonuna Tıklama**
   - Tüm bilgileri girdikten sonra, **Create pull request** butonuna tıklayın.

### 5.13.7 Adım 6: Pull Request'i Gözden Geçirme ve Merge Etme

Oluşturduğunuz PR'yi gözden geçirip ana dala (main) merge edeceğiz.

1. **Pull Request'i İnceleme**
   - PR sayfasında, yapılan değişiklikleri gözden geçirin. Dosya değişikliklerini kontrol edin ve gerektiğinde yorum bırakın.

2. **Merge Butonuna Tıklama**
   - Her şeyin doğru olduğundan emin olduktan sonra, **Merge pull request** butonuna tıklayın.

3. **Merge İşlemini Onaylama**
   - Açılan pencerede, merge işlemini onaylamak için **Confirm merge** butonuna tıklayın.

4. **Pull Request'i Kapatma**
   - Merge işleminden sonra, PR'yi kapatmak için **Close pull request** butonuna tıklayın.

### 5.13.8 Adım 7: Ana Dalı Güncelleme

Ana dalı (main) güncellediğinizden emin olun.

1. **Ana Dalı Güncelleme**
   - Yerel repository'nizde ana dalın güncel olduğundan emin olmak için şu komutu çalıştırın:
     ```bash
     git checkout main
     git pull origin main
     ```

### 5.13.9 Lab-13'ün Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak, **ProductManagement** projesindeki tüm değişiklikleri Git kullanarak commit ve push ettiniz. Ardından, GitHub üzerinde bir Pull Request oluşturarak bu PR'yi **main** dalına merge ettiniz. Bu adımlar, projenizin versiyon kontrolünü etkin bir şekilde yönetmenizi ve takım çalışmasını kolaylaştırmanızı sağlamıştır. Bir sonraki laboratuvar çalışmasında, projenize CI/CD entegrasyonu ekleyerek otomatik test ve dağıtım süreçlerini yapılandırmaya devam edeceğiz.

---

## 5.14 Lab-14: Agent Pool Oluşturma ve Self-Hosted Agent Kurulumu

Bu laboratuvar çalışmasında, **ProductManagement** projesi için bir **Agent Pool** oluşturacak ve kendi bilgisayarınıza **Self-Hosted Agent** kurarak CI/CD (Continuous Integration/Continuous Deployment) süreçlerinizi optimize edeceksiniz. Bu adımlar, Azure DevOps kullanarak derleme ve dağıtım işlemlerini otomatikleştirmenizi sağlayacak ve projelerinizin daha hızlı ve güvenilir bir şekilde geliştirilmesine olanak tanıyacaktır.

### 5.14.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Azure DevOps Hesabı**: [Azure DevOps](https://dev.azure.com/) hesabınızın olması gerekmektedir.
- **Proje Oluşturulmuş Olmalı**: `ProductManagement` projesi Azure DevOps üzerinde oluşturulmuş olmalıdır.
- **Yönetici Yetkisi**: Agent Pool oluşturmak ve agent kurmak için Azure DevOps projesinde yönetici (admin) yetkisine sahip olmanız gerekmektedir.
- **Self-Hosted Agent için Sistem Gereksinimleri**:
  - **İşletim Sistemi**: Windows, macOS veya Linux
  - **İnternet Bağlantısı**: Azure DevOps ile iletişim kurmak için aktif bir internet bağlantısı
  - **Yazılım Gereksinimleri**:
    - [.NET Core](https://dotnet.microsoft.com/download) (gerekirse)
    - [Node.js](https://nodejs.org/en/download/) (gerekirse)
    - Diğer proje bağımlılıkları

### 5.14.2 Adım 1: Azure DevOps'ta Agent Pool Oluşturma

#### 1. Azure DevOps Portalına Giriş Yapma

- Tarayıcınızda [Azure DevOps](https://dev.azure.com/) portalına gidin ve hesabınıza giriş yapın.

#### 2. Proje Seçimi

- Sol üst köşedeki **"Organization"** seçeneğinden ilgili organizasyonu seçin.
- **"Projects"** sekmesinden **`ProductManagement`** projesini seçin.

#### 3. Agent Pools Yönetimine Gitme

- Sol menüden **"Project settings"** (Proje Ayarları) seçeneğine tıklayın.
- **"Pipelines"** altında **"Agent pools"** seçeneğini bulun ve tıklayın.

#### 4. Yeni Bir Agent Pool Oluşturma

- Sağ üst köşede bulunan **"Add pool"** butonuna tıklayın.
- **Pool Name** (Havuz Adı) kısmına `Self-Hosted Agents` gibi anlamlı bir isim girin.
- **Pool Type** (Havuz Türü) olarak **"Self-hosted"** seçeneğini işaretleyin.
- **Description** (Açıklama) kısmına isteğe bağlı olarak havuz hakkında bilgi ekleyebilirsiniz.
- **"Create"** butonuna tıklayarak Agent Pool'ü oluşturun.

### 5.14.3 Adım 2: Self-Hosted Agent Kurulumu

#### 1. Agent İndirme Sayfasına Gitme

- Oluşturduğunuz **Agent Pool**'ün detay sayfasına gidin.
- **"New agent"** butonuna tıklayın.

#### 2. İşletim Sistemi Seçimi

- Açılan pencerede kendi bilgisayarınızın işletim sistemini seçin (Windows, macOS veya Linux).

#### 3. Agent İndirme ve Kurulum Talimatlarını Takip Etme

- Seçtiğiniz işletim sistemine göre verilen talimatları takip edin. Aşağıda Windows için adımlar detaylı olarak verilmiştir.

##### **Windows İçin Self-Hosted Agent Kurulumu**

1. **Agent Paketini İndirme**

   - Sağlanan indirme linkine tıklayarak agent paketini indirin.
   - Örneğin: `vsts-agent-win-x64-2.195.0.zip`

2. **Agent Paketini Çıkarma**

   - İndirilen `.zip` dosyasını, agent'ı kurmak istediğiniz dizine çıkarın. Örneğin: `C:\agents\self-hosted`

3. **Terminali Yönetici Olarak Açma**

   - `cmd.exe` veya `PowerShell`'i yönetici olarak açın.

4. **Agent'ı Yapılandırma**

   - Agent paketinin bulunduğu dizine gidin:

     ```powershell
     cd C:\agents\self-hosted
     ```

   - Agent'ı konfigüre etmek için aşağıdaki komutu çalıştırın:

     ```powershell
     .\config.cmd
     ```

   - Aşağıdaki bilgileri girin:
     - **Azure DevOps URL'si**: `https://dev.azure.com/your-organization`
     - **Agent Pool**: `Self-Hosted Agents`
     - **Agent Name**: Bilgisayarınızın adı veya anlamlı bir isim
     - **Authentication**: **"PAT"** (Personal Access Token) kullanın
     - **PAT Token**: Azure DevOps'ta oluşturduğunuz bir PAT (öğrenmek için [Azure DevOps PAT Oluşturma](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate)) girin
     - **Work Folder**: Varsayılan olarak bırakabilirsiniz veya özel bir yol belirleyebilirsiniz

5. **Agent'ı Hizmet Olarak Kurma**

   - Agent'ı sürekli çalışacak bir hizmet olarak kurmak için:

     ```powershell
     .\svc.sh install
     .\svc.sh start
     ```

##### **macOS ve Linux İçin Self-Hosted Agent Kurulumu**

- **Terminali Açın** ve aşağıdaki adımları takip edin:

1. **Agent Paketini İndirme**

   ```bash
   mkdir ~/agent && cd ~/agent
   curl -O https://vstsagentpackage.azureedge.net/agent/2.195.0/vsts-agent-osx-x64-2.195.0.tar.gz
   tar zxvf vsts-agent-osx-x64-2.195.0.tar.gz
   ```

2. **Agent'ı Konfigüre Etme**

   ```bash
   ./config.sh
   ```

   - Yukarıdaki Windows adımlarına benzer şekilde bilgileri girin.

3. **Agent'ı Hizmet Olarak Kurma**

   ```bash
   sudo ./svc.sh install
   sudo ./svc.sh start
   ```

#### 4. Agent'ı Doğrulama

- Azure DevOps portalına geri dönün ve **Agent Pool** sayfasını yenileyin.
- Yeni kurduğunuz agent'ın **"Online"** ve **"Ready"** durumda olduğunu doğrulayın.

### 5.14.4 Adım 3: Güvenlik ve Bakım

#### 1. Agent Güncellemeleri

- Agent'ınızın güncel kalmasını sağlamak için düzenli olarak güncellemeleri kontrol edin.
- Azure DevOps portalında agent durumunu izleyin ve gerekli güncellemeleri uygulayın.

#### 2. Güvenlik Ayarları

- Agent'ınızın bulunduğu makinenin güvenliğini sağlamak için gerekli önlemleri alın.
- Güçlü parolalar kullanın ve düzenli olarak şifrelerinizi güncelleyin.
- Güvenlik duvarı ve antivirüs yazılımlarını yapılandırarak yetkisiz erişimi önleyin.

### 5.14.5 Lab-14'ün Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak **ProductManagement** projesi için bir **Agent Pool** oluşturup, kendi bilgisayarınıza **Self-Hosted Agent** kurdunuz. Bu adımlar, CI/CD süreçlerinizin daha hızlı ve esnek bir şekilde çalışmasını sağlayarak geliştirme ve dağıtım süreçlerinizi optimize etmiştir. Bir sonraki laboratuvar çalışmasında, pipeline'ınızı daha da geliştirmek için otomatik testler ve dağıtım stratejileri eklemeye devam edeceğiz.

---

**Not:** Self-Hosted Agent kurulumunda karşılaşabileceğiniz sorunlar için [Azure DevOps Agent Documentation](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/v2-windows) sayfasını ziyaret edebilirsiniz. Ayrıca, agent'ınızın güvenliğini sağlamak için en iyi uygulamaları takip ettiğinizden emin olun.

## 5.15 Lab-15: Backend için YAML Formatında PR Pipeline Oluşturma ve Branch Policy Ayarları

Bu laboratuvar çalışmasında, **ProductManagement** projesinin backend kısmı için bir YAML formatında PR pipeline oluşturacağız. Bu pipeline'ı repository'ye commit/push ederek bir PR ile gönderecek, ardından Azure DevOps portalında bir pipeline oluşturup, `main` branch'e PR açıldığında bu pipeline'ın çalışmasını sağlayacağız. Son olarak, branch policy ayarlarını yapılandırarak pipeline'ı zorunlu hale getireceğiz.

### 5.15.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Backend Repository'si Oluşturulmuş ve Yapılandırılmış Olmalı**: `ProductManagement` projesinin backend repository'si mevcut ve yapılandırılmış olmalıdır.
- **Azure DevOps Hesabı ve Pipeline Yetkileri**: Azure DevOps'ta pipeline oluşturma yetkisine sahip bir kullanıcı hesabı.
- **Self-Hosted Agent Pool**: Daha önce oluşturulan agent pool adını biliyor olmalısınız.
- **YAML Formatında Pipeline Bilgisi**: YAML formatında temel pipeline bilgisi.

### 5.15.2 Adım 1: YAML Pipeline Dosyasını Oluşturma

1. **YAML Dosyası Oluşturma**
   - VSCode veya tercih ettiğiniz bir editörde, backend repository'nizin kök dizininde `.azure-pipelines` adında bir klasör oluşturun.
   - Bu klasör içinde `pr-pipeline.yml` adında bir dosya oluşturun.

2. **YAML Pipeline İçeriği**
   - Aşağıdaki YAML içeriğini `pr-pipeline.yml` dosyasına yapıştırın:
     ```yaml
     trigger:
       branches:
         exclude:
           - "*"

     pr:
       branches:
         include:
           - main

     pool:
       name: 'Self-Hosted Agents' # Daha önce oluşturduğunuz agent pool adı

     variables:
       buildConfiguration: 'Release'

     steps:
       - task: UseDotNet@2
         displayName: 'Install .NET SDK'
         inputs:
           packageType: 'sdk'
           version: '6.x'
           installationPath: $(Agent.ToolsDirectory)/dotnet

       - script: |
           dotnet restore
           dotnet build --configuration $(buildConfiguration)
           dotnet test --configuration $(buildConfiguration) --no-build
         displayName: 'Restore, Build, and Test'

       - task: PublishBuildArtifacts@1
         displayName: 'Publish Artifacts'
         inputs:
           PathtoPublish: '$(Build.ArtifactStagingDirectory)'
           ArtifactName: 'drop'
     ```

3. **YAML Dosyasını Commit ve Push Etme**
   - Terminalde aşağıdaki komutları çalıştırarak değişikliklerinizi stage edin, commit edin ve remote repository'ye push edin:
     ```bash
     git add .azure-pipelines/pr-pipeline.yml
     git commit -m "Backend için PR pipeline eklendi"
     git push origin <branch-name>
     ```

4. **Pull Request Oluşturma**
   - GitHub veya Azure DevOps portalında, oluşturduğunuz branch'ten `main` branch'e bir pull request (PR) oluşturun.
   - PR açıklamasına şu bilgileri ekleyin:
     ```
     Backend için YAML formatında PR pipeline eklendi.
     - PR açıldığında bu pipeline çalıştırılacaktır.
     ```

### 5.15.3 Adım 2: Pipeline Oluşturma

1. **Azure DevOps Portalına Giriş**
   - Tarayıcınızda [Azure DevOps](https://dev.azure.com/) portalına gidin ve hesabınıza giriş yapın.

2. **Pipeline Oluşturma**
   - **Pipelines** sekmesine gidin ve **New Pipeline** butonuna tıklayın.
   - Repository'yi seçin ve **Existing Azure Pipelines YAML file** seçeneğini seçin.
   - `pr-pipeline.yml` dosyasının yolunu belirterek pipeline'ı oluşturun.

3. **Pipeline'ı Kaydetme ve Çalıştırma**
   - Pipeline'ı kaydedin ve test etmek için çalıştırın. Pipeline'ın sorunsuz bir şekilde çalıştığını doğrulayın.

### 5.15.4 Adım 3: Branch Policy Ayarları

1. **Branch Policy Ayarlarına Gitme**
   - **Repos** sekmesine gidin ve sol menüden **Branches** seçeneğini seçin.
   - `main` branch'ini bulun ve yanındaki üç nokta menüsünden **Branch policies** seçeneğine tıklayın.

2. **Build Validation Ekleme**
   - **Build validation** bölümünde **+ Add build policy** butonuna tıklayın.
   - Açılan pencerede oluşturduğunuz pipeline'ı seçin.
   - **Trigger on pull request validation** seçeneğini işaretleyin ve **Required** olarak ayarlayın.
   - Kaydetmek için **Save** butonuna tıklayın.

3. **Policy Ayarlarının Doğrulanması**
   - Artık `main` branch'e bir PR açıldığında, pipeline çalıştırılacak ve başarıyla tamamlanması gerekecektir.

### 5.15.5 Lab-15'in Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak backend için bir PR pipeline oluşturmuş, bu pipeline'ı YAML formatında repository'ye eklemiş, Azure DevOps üzerinde yapılandırmış ve branch policy ayarlarını tamamlamış oldunuz. Bu adımlar, PR süreçlerinizde otomatik build ve test süreçlerini devreye alarak daha güvenli ve düzenli bir geliştirme ortamı sağlamanıza yardımcı olacaktır.

## 5.16 Lab-16: UI Projesi için YAML Formatında PR Pipeline Oluşturma ve Branch Policy Ayarları

Bu laboratuvar çalışmasında, **ProductManagement** projesinin UI kısmı için bir YAML formatında PR pipeline oluşturacağız. Bu pipeline'ı repository'ye commit/push ederek bir PR ile gönderecek, ardından Azure DevOps portalında bir pipeline oluşturup, `main` branch'e PR açıldığında bu pipeline'ın çalışmasını sağlayacağız. Son olarak, branch policy ayarlarını yapılandırarak pipeline'ı zorunlu hale getireceğiz.

### 5.16.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **UI Repository'si Oluşturulmuş ve Yapılandırılmış Olmalı**: `ProductManagement` projesinin UI repository'si mevcut ve yapılandırılmış olmalıdır.
- **Azure DevOps Hesabı ve Pipeline Yetkileri**: Azure DevOps'ta pipeline oluşturma yetkisine sahip bir kullanıcı hesabı.
- **Self-Hosted Agent Pool**: Daha önce oluşturulan agent pool adını biliyor olmalısınız.
- **YAML Formatında Pipeline Bilgisi**: YAML formatında temel pipeline bilgisi.

### 5.16.2 Adım 1: YAML Pipeline Dosyasını Oluşturma

1. **YAML Dosyası Oluşturma**
   - VSCode veya tercih ettiğiniz bir editörde, UI repository'nizin kök dizininde `.azure-pipelines` adında bir klasör oluşturun.
   - Bu klasör içinde `pr-pipeline.yml` adında bir dosya oluşturun.

2. **YAML Pipeline İçeriği**
   - Aşağıdaki YAML içeriğini `pr-pipeline.yml` dosyasına yapıştırın:
     ```yaml
     trigger:
       branches:
         exclude:
           - "*"

     pr:
       branches:
         include:
           - main

     pool:
       name: 'Self-Hosted Agents' # Daha önce oluşturduğunuz agent pool adı

     variables:
       buildConfiguration: 'Release'

     steps:
       - task: NodeTool@0
         displayName: 'Use Node.js'
         inputs:
           versionSpec: '14.x'
           checkLatest: true

       - script: |
           npm install
           npm run build --prod
         displayName: 'Install Dependencies and Build UI Project'

       - task: PublishBuildArtifacts@1
         displayName: 'Publish Artifacts'
         inputs:
           PathtoPublish: 'dist'
           ArtifactName: 'drop'
     ```

3. **YAML Dosyasını Commit ve Push Etme**
   - Terminalde aşağıdaki komutları çalıştırarak değişikliklerinizi stage edin, commit edin ve remote repository'ye push edin:
     ```bash
     git add .azure-pipelines/pr-pipeline.yml
     git commit -m "UI için PR pipeline eklendi"
     git push origin <branch-name>
     ```

4. **Pull Request Oluşturma**
   - GitHub veya Azure DevOps portalında, oluşturduğunuz branch'ten `main` branch'e bir pull request (PR) oluşturun.
   - PR açıklamasına şu bilgileri ekleyin:
     ```
     UI için YAML formatında PR pipeline eklendi.
     - PR açıldığında bu pipeline çalıştırılacaktır.
     ```

### 5.16.3 Adım 2: Pipeline Oluşturma

1. **Azure DevOps Portalına Giriş**
   - Tarayıcınızda [Azure DevOps](https://dev.azure.com/) portalına gidin ve hesabınıza giriş yapın.

2. **Pipeline Oluşturma**
   - **Pipelines** sekmesine gidin ve **New Pipeline** butonuna tıklayın.
   - Repository'yi seçin ve **Existing Azure Pipelines YAML file** seçeneğini seçin.
   - `pr-pipeline.yml` dosyasının yolunu belirterek pipeline'ı oluşturun.

3. **Pipeline'ı Kaydetme ve Çalıştırma**
   - Pipeline'ı kaydedin ve test etmek için çalıştırın. Pipeline'ın sorunsuz bir şekilde çalıştığını doğrulayın.

### 5.16.4 Adım 3: Branch Policy Ayarları

1. **Branch Policy Ayarlarına Gitme**
   - **Repos** sekmesine gidin ve sol menüden **Branches** seçeneğini seçin.
   - `main` branch'ini bulun ve yanındaki üç nokta menüsünden **Branch policies** seçeneğine tıklayın.

2. **Build Validation Ekleme**
   - **Build validation** bölümünde **+ Add build policy** butonuna tıklayın.
   - Açılan pencerede oluşturduğunuz pipeline'ı seçin.
   - **Trigger on pull request validation** seçeneğini işaretleyin ve **Required** olarak ayarlayın.
   - Kaydetmek için **Save** butonuna tıklayın.

3. **Policy Ayarlarının Doğrulanması**
   - Artık `main` branch'e bir PR açıldığında, pipeline çalıştırılacak ve başarıyla tamamlanması gerekecektir.

### 5.16.5 Lab-16'nın Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak UI projesi için bir PR pipeline oluşturmuş, bu pipeline'ı YAML formatında repository'ye eklemiş, Azure DevOps üzerinde yapılandırmış ve branch policy ayarlarını tamamlamış oldunuz. Bu adımlar, PR süreçlerinizde otomatik build ve test süreçlerini devreye alarak daha güvenli ve düzenli bir geliştirme ortamı sağlamanıza yardımcı olacaktır.

## 5.17 Lab-17: Backend ve UI Projelerinde Basit Değişiklikler Yaparak PR Pipeline'ların Çalıştığını Doğrulama

Bu laboratuvar çalışmasında, **ProductManagement** projesinin backend ve UI projelerinde küçük değişiklikler yaparak oluşturduğunuz PR pipeline'ların çalışıp çalışmadığını doğrulayacağız. Her iki proje için de değişiklik yapacak, bu değişiklikleri PR oluşturup pipeline'ın tetiklendiğini gözlemleyeceğiz.

### 5.17.1 Backend Projesinde Değişiklik Yapma

1. **Backend Projesini Klonlama**
   - Backend repository'sini klonlayın (eğer daha önce klonlanmadıysa):
     ```bash
     git clone <backend-repository-url>
     cd <backend-repository-folder>
     ```

2. **Değişiklik Yapma**
   - Projede basit bir değişiklik yapın. Örneğin, `ProductController` dosyasına bir yorum ekleyin:
     ```csharp
     // Bu bir test değişikliğidir.
     ```

3. **Değişiklikleri Commit ve Push Etme**
   - Yeni bir feature branch oluşturun:
     ```bash
     git checkout -b feature/test-backend-pr-pipeline
     ```
   - Değişiklikleri stage edin ve commit yapın:
     ```bash
     git add .
     git commit -m "Backend PR pipeline testi için değişiklik yapıldı"
     git push origin feature/test-backend-pr-pipeline
     ```

4. **Pull Request Oluşturma**
   - Azure DevOps portalına gidin ve `feature/test-backend-pr-pipeline` branch'inden `main` branch'e bir PR oluşturun.
   - PR açıklamasına şu bilgileri ekleyin:
     ```
     Backend PR pipeline testi için küçük bir değişiklik yapıldı.
     ```

5. **Pipeline'ı Doğrulama**
   - PR oluşturulduktan sonra pipeline otomatik olarak tetiklenecektir.
   - Pipeline sekmesine giderek, pipeline'ın başarılı bir şekilde çalışıp çalışmadığını gözlemleyin.

---

### 5.17.2 UI Projesinde Değişiklik Yapma

1. **UI Projesini Klonlama**
   - UI repository'sini klonlayın (eğer daha önce klonlanmadıysa):
     ```bash
     git clone <ui-repository-url>
     cd <ui-repository-folder>
     ```

2. **Değişiklik Yapma**
   - Projede basit bir değişiklik yapın. Örneğin, `app.component.html` dosyasına bir yorum ekleyin:
     ```html
     <!-- Bu bir test değişikliğidir -->
     ```

3. **Değişiklikleri Commit ve Push Etme**
   - Yeni bir feature branch oluşturun:
     ```bash
     git checkout -b feature/test-ui-pr-pipeline
     ```
   - Değişiklikleri stage edin ve commit yapın:
     ```bash
     git add .
     git commit -m "UI PR pipeline testi için değişiklik yapıldı"
     git push origin feature/test-ui-pr-pipeline
     ```

4. **Pull Request Oluşturma**
   - Azure DevOps portalına gidin ve `feature/test-ui-pr-pipeline` branch'inden `main` branch'e bir PR oluşturun.
   - PR açıklamasına şu bilgileri ekleyin:
     ```
     UI PR pipeline testi için küçük bir değişiklik yapıldı.
     ```

5. **Pipeline'ı Doğrulama**
   - PR oluşturulduktan sonra pipeline otomatik olarak tetiklenecektir.
   - Pipeline sekmesine giderek, pipeline'ın başarılı bir şekilde çalışıp çalışmadığını gözlemleyin.

---

### 5.17.3 Lab-17'nin Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak backend ve UI projelerinde PR pipeline'ların doğru şekilde tetiklendiğini ve çalıştığını doğruladınız. Bu adımlar, oluşturulan pipeline'ların işlevselliğini test etmek ve PR süreçlerinin sorunsuz bir şekilde işlediğinden emin olmak için önemlidir.

## 5.18 Lab-18: Backend için CI Pipeline Oluşturma

Bu laboratuvar çalışmasında, **ProductManagement** projesinin backend kısmı için bir CI (Continuous Integration) pipeline oluşturacağız. Pipeline, `main` branch'e yapılan her kod merge işleminden sonra otomatik olarak çalışacak ve bir artifact oluşturacaktır. Bu süreç, sürekli entegrasyonu destekleyerek projenizin daha hızlı ve güvenilir bir şekilde geliştirilmesini sağlayacaktır.

### 5.18.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Backend Repository'si**: Backend repository'si Azure DevOps üzerinde mevcut olmalıdır.
- **Self-Hosted Agent Pool**: Daha önce oluşturduğunuz agent pool adını biliyor olmalısınız.
- **YAML Formatında Pipeline Bilgisi**: YAML formatında temel pipeline bilgisi.

---

### 5.18.2 Adım 1: YAML Pipeline Dosyasını Oluşturma

1. **YAML Dosyası Oluşturma**
   - VSCode veya tercih ettiğiniz bir editörde, backend repository'nizin kök dizininde `.azure-pipelines` adında bir klasör oluşturun.
   - Bu klasör içinde `ci-pipeline.yml` adında bir dosya oluşturun.

2. **YAML Pipeline İçeriği**
   - Aşağıdaki YAML içeriğini `ci-pipeline.yml` dosyasına yapıştırın:
     ```yaml
     trigger:
       branches:
         include:
           - main

     pool:
       name: 'Self-Hosted Agents' # Daha önce oluşturduğunuz agent pool adı

     variables:
       buildConfiguration: 'Release'

     steps:
       - task: UseDotNet@2
         displayName: 'Install .NET SDK'
         inputs:
           packageType: 'sdk'
           version: '6.x'
           installationPath: $(Agent.ToolsDirectory)/dotnet

       - script: |
           dotnet restore
           dotnet build --configuration $(buildConfiguration)
           dotnet test --configuration $(buildConfiguration) --no-build
         displayName: 'Restore, Build, and Test'

       - task: PublishBuildArtifacts@1
         displayName: 'Publish Artifacts'
         inputs:
           PathtoPublish: '$(Build.ArtifactStagingDirectory)'
           ArtifactName: 'drop'
     ```

3. **YAML Dosyasını Commit ve Push Etme**
   - Terminalde aşağıdaki komutları çalıştırarak değişikliklerinizi stage edin, commit edin ve remote repository'ye push edin:
     ```bash
     git add .azure-pipelines/ci-pipeline.yml
     git commit -m "Backend için CI pipeline eklendi"
     git push origin <branch-name>
     ```

4. **Pull Request Oluşturma**
   - Azure DevOps portalına gidin ve `main` branch'e merge etmek üzere bir PR oluşturun.
   - PR açıklamasına şu bilgileri ekleyin:
     ```
     Backend için CI pipeline eklendi. Main branch'e kod merge edilince otomatik olarak çalışacaktır.
     ```

---

### 5.18.3 Adım 2: Azure DevOps Üzerinde Pipeline Oluşturma

1. **Azure DevOps Portalına Giriş**
   - Tarayıcınızda [Azure DevOps](https://dev.azure.com/) portalına gidin ve hesabınıza giriş yapın.

2. **Pipeline Oluşturma**
   - **Pipelines** sekmesine gidin ve **New Pipeline** butonuna tıklayın.
   - Repository'yi seçin ve **Existing Azure Pipelines YAML file** seçeneğini seçin.
   - `ci-pipeline.yml` dosyasının yolunu belirterek pipeline'ı oluşturun.

3. **Pipeline'ı Kaydetme ve Çalıştırma**
   - Pipeline'ı kaydedin ve test etmek için çalıştırın.
   - Pipeline'ın `main` branch'te kod merge edildikten sonra otomatik olarak çalışıp çalışmadığını doğrulayın.

---

### 5.18.4 Adım 3: Pipeline'ın Çalışmasını Doğrulama

1. **Kod Merge Etme**
   - Yeni oluşturulan pipeline'ı test etmek için bir feature branch üzerinde basit bir değişiklik yapın ve bu değişikliği PR ile `main` branch'e merge edin.

2. **Pipeline Tetiklenmesini Gözlemleme**
   - Azure DevOps portalında **Pipelines** sekmesine giderek pipeline'ın otomatik olarak çalıştırıldığını doğrulayın.

3. **Artifact Oluşturulmasını Kontrol Etme**
   - Pipeline tamamlandıktan sonra, **Artifacts** sekmesinde oluşturulan artifact'i kontrol edin.
   - Artifact'in doğru bir şekilde oluşturulduğunu ve indirilip kullanılabilir durumda olduğunu doğrulayın.

---

### 5.18.5 Lab-18'in Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak backend için bir CI pipeline oluşturmuş, pipeline'ı repository'ye YAML formatında eklemiş, Azure DevOps üzerinde yapılandırmış ve pipeline'ın doğru şekilde çalıştığını doğrulamış oldunuz. Bu süreç, projenizin sürekli entegrasyonunu sağlamanın temel bir adımıdır.

## 5.19 Lab-19: UI Projesi için CI Pipeline Oluşturma

Bu laboratuvar çalışmasında, **ProductManagement** projesinin UI kısmı için bir CI (Continuous Integration) pipeline oluşturacağız. Pipeline, `main` branch'e yapılan her kod merge işleminden sonra otomatik olarak çalışacak ve bir artifact oluşturacaktır. Bu süreç, sürekli entegrasyonu destekleyerek projenizin daha hızlı ve güvenilir bir şekilde geliştirilmesini sağlayacaktır.

---

### 5.19.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **UI Repository'si**: UI repository'si Azure DevOps üzerinde mevcut olmalıdır.
- **Self-Hosted Agent Pool**: Daha önce oluşturduğunuz agent pool adını biliyor olmalısınız.
- **YAML Formatında Pipeline Bilgisi**: YAML formatında temel pipeline bilgisi.

---

### 5.19.2 Adım 1: YAML Pipeline Dosyasını Oluşturma

1. **YAML Dosyası Oluşturma**
   - VSCode veya tercih ettiğiniz bir editörde, UI repository'nizin kök dizininde `.azure-pipelines` adında bir klasör oluşturun.
   - Bu klasör içinde `ci-pipeline.yml` adında bir dosya oluşturun.

2. **YAML Pipeline İçeriği**
   - Aşağıdaki YAML içeriğini `ci-pipeline.yml` dosyasına yapıştırın:
     ```yaml
     trigger:
       branches:
         include:
           - main

     pool:
       name: 'Self-Hosted Agents' # Daha önce oluşturduğunuz agent pool adı

     variables:
       buildConfiguration: 'Release'

     steps:
       - task: NodeTool@0
         displayName: 'Use Node.js'
         inputs:
           versionSpec: '14.x'
           checkLatest: true

       - script: |
           npm install
           npm run build --prod
         displayName: 'Install Dependencies and Build UI Project'

       - task: PublishBuildArtifacts@1
         displayName: 'Publish Artifacts'
         inputs:
           PathtoPublish: 'dist'
           ArtifactName: 'drop'
     ```

3. **YAML Dosyasını Commit ve Push Etme**
   - Terminalde aşağıdaki komutları çalıştırarak değişikliklerinizi stage edin, commit edin ve remote repository'ye push edin:
     ```bash
     git add .azure-pipelines/ci-pipeline.yml
     git commit -m "UI için CI pipeline eklendi"
     git push origin <branch-name>
     ```

4. **Pull Request Oluşturma**
   - Azure DevOps portalına gidin ve `main` branch'e merge etmek üzere bir PR oluşturun.
   - PR açıklamasına şu bilgileri ekleyin:
     ```
     UI için CI pipeline eklendi. Main branch'e kod merge edilince otomatik olarak çalışacaktır.
     ```

---

### 5.19.3 Adım 2: Azure DevOps Üzerinde Pipeline Oluşturma

1. **Azure DevOps Portalına Giriş**
   - Tarayıcınızda [Azure DevOps](https://dev.azure.com/) portalına gidin ve hesabınıza giriş yapın.

2. **Pipeline Oluşturma**
   - **Pipelines** sekmesine gidin ve **New Pipeline** butonuna tıklayın.
   - Repository'yi seçin ve **Existing Azure Pipelines YAML file** seçeneğini seçin.
   - `ci-pipeline.yml` dosyasının yolunu belirterek pipeline'ı oluşturun.

3. **Pipeline'ı Kaydetme ve Çalıştırma**
   - Pipeline'ı kaydedin ve test etmek için çalıştırın.
   - Pipeline'ın `main` branch'te kod merge edildikten sonra otomatik olarak çalışıp çalışmadığını doğrulayın.

---

### 5.19.4 Adım 3: Pipeline'ın Çalışmasını Doğrulama

1. **Kod Merge Etme**
   - Yeni oluşturulan pipeline'ı test etmek için bir feature branch üzerinde basit bir değişiklik yapın ve bu değişikliği PR ile `main` branch'e merge edin.

2. **Pipeline Tetiklenmesini Gözlemleme**
   - Azure DevOps portalında **Pipelines** sekmesine giderek pipeline'ın otomatik olarak çalıştırıldığını doğrulayın.

3. **Artifact Oluşturulmasını Kontrol Etme**
   - Pipeline tamamlandıktan sonra, **Artifacts** sekmesinde oluşturulan artifact'i kontrol edin.
   - Artifact'in doğru bir şekilde oluşturulduğunu ve indirilip kullanılabilir durumda olduğunu doğrulayın.

---

### 5.19.5 Lab-19'un Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak UI projesi için bir CI pipeline oluşturmuş, pipeline'ı repository'ye YAML formatında eklemiş, Azure DevOps üzerinde yapılandırmış ve pipeline'ın doğru şekilde çalıştığını doğrulamış oldunuz. Bu süreç, projenizin sürekli entegrasyonunu sağlamanın temel bir adımıdır.

## 5.20 Lab-20: Backend ve UI için IIS Üzerinde Site Kurma ve Konfigürasyon Yapma

Bu laboratuvar çalışmasında, **ProductManagement** projesinin backend ve UI kısımları için IIS üzerinde iki ayrı site kuracak ve gerekli konfigürasyonları yapacağız. IIS üzerinde kurulan bu sitelerin dosya kökleri, projeyi klonladığınız dizinlerden farklı bir klasörde bulunacaktır. Kullanılacak portlar, lokal geliştirme sırasında kullanılan portlardan farklı olacak şekilde ayarlanacaktır: **Backend için 10100** ve **UI için 10200**.

---

### 5.20.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **IIS Yüklü Olmalı**: IIS (Internet Information Services) bilgisayarınıza yüklü ve etkinleştirilmiş olmalıdır.
- **Proje Build Edilmiş Olmalı**: Backend ve UI projeleriniz build edilmiş ve çalışır durumda olmalıdır.
- **Ayrı Klasörler Oluşturulmuş Olmalı**:
  - Backend için: `C:\inetpub\ProductManagement_Backend`
  - UI için: `C:\inetpub\ProductManagement_UI`
- **Administrator Yetkisi**: IIS üzerinde site oluşturma ve yönetme yetkiniz olmalıdır.

---

### 5.20.2 Adım 1: IIS Üzerinde Backend Sitesini Kurma

1. **Backend için Klasör Hazırlama**
   - Backend projenizi build edin:
     ```bash
     dotnet publish -c Release -o C:\inetpub\ProductManagement_Backend
     ```
   - Build işlemi tamamlandıktan sonra `C:\inetpub\ProductManagement_Backend` klasörüne giderek dosyaların doğru bir şekilde kopyalandığını kontrol edin.

2. **IIS Üzerinde Yeni Site Oluşturma**
   - **IIS Manager**'ı açın (Windows'da `inetmgr` komutunu çalıştırarak erişebilirsiniz).
   - Sol menüdeki **Sites** üzerine sağ tıklayın ve **Add Website** seçeneğini seçin.
   - Aşağıdaki bilgileri girin:
     - **Site Name**: `ProductManagement_Backend`
     - **Physical Path**: `C:\inetpub\ProductManagement_Backend`
     - **Binding**:
       - **Type**: `http`
       - **IP Address**: `All Unassigned`
       - **Port**: `10100`
       - **Host Name**: Boş bırakabilirsiniz.
   - **OK** butonuna tıklayarak siteyi oluşturun.

3. **Backend Sitesini Test Etme**
   - Tarayıcınızda `http://localhost:10100` adresine giderek backend API'sinin çalıştığını doğrulayın.
   - Eğer bir hata alırsanız, IIS loglarını ve backend loglarını kontrol edin.

---

### 5.20.3 Adım 2: IIS Üzerinde UI Sitesini Kurma

1. **UI için Klasör Hazırlama**
   - UI projenizi build edin:
     ```bash
     npm install
     npm run build --prod
     ```
   - Build işlemi tamamlandıktan sonra `dist` klasörünün içeriğini `C:\inetpub\ProductManagement_UI` klasörüne kopyalayın.

2. **IIS Üzerinde Yeni Site Oluşturma**
   - IIS Manager'da **Sites** üzerine sağ tıklayın ve **Add Website** seçeneğini seçin.
   - Aşağıdaki bilgileri girin:
     - **Site Name**: `ProductManagement_UI`
     - **Physical Path**: `C:\inetpub\ProductManagement_UI`
     - **Binding**:
       - **Type**: `http`
       - **IP Address**: `All Unassigned`
       - **Port**: `10200`
       - **Host Name**: Boş bırakabilirsiniz.
   - **OK** butonuna tıklayarak siteyi oluşturun.

3. **UI Sitesini Test Etme**
   - Tarayıcınızda `http://localhost:10200` adresine giderek UI uygulamasının çalıştığını doğrulayın.
   - Eğer bir hata alırsanız, IIS loglarını ve browser console hatalarını kontrol edin.

---

### 5.20.4 Adım 3: CORS ve API Bağlantılarını Yapılandırma

1. **Backend Projesinde CORS Ayarları**
   - Backend projesinin CORS ayarlarına, UI sitesinden gelen istekleri kabul edecek şekilde izin ekleyin:
     ```csharp
     builder.Services.AddCors(options =>
     {
         options.AddPolicy("AllowUI",
             builder =>
             {
                 builder.WithOrigins("http://localhost:10200")
                        .AllowAnyHeader()
                        .AllowAnyMethod();
             });
     });

     app.UseCors("AllowUI");
     ```

2. **UI Projesinde API URL'sini Güncelleme**
   - UI projesinde `environment.ts` dosyasını açın ve API URL'sini şu şekilde güncelleyin:
     ```typescript
     export const environment = {
       production: true,
       apiUrl: 'http://localhost:10100/api'
     };
     ```

3. **Değişiklikleri Uygulama**
   - Backend ve UI projelerini yeniden build edin ve ilgili IIS klasörlerine yeniden kopyalayın.

---

### 5.20.5 Lab-20'nin Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak backend ve UI projeleriniz için IIS üzerinde iki ayrı site kurmuş, gerekli yapılandırmaları yapmış ve bu sitelerin farklı dizinlerden çalışmasını sağlamış oldunuz. Backend için **10100**, UI için **10200** portunu kullanarak lokal sunucuda test işlemlerini gerçekleştirdiniz. Bu adımlar, projelerinizi lokal sunucuda test etme ve dağıtım süreçlerini daha gerçekçi bir şekilde simüle etme imkanı sunar.

## 5.21 Lab-21: Backend CI Pipeline'ını CI/CD Pipeline'a Dönüştürme ve Deploy Adımı Eklemek

Bu laboratuvar çalışmasında, daha önce oluşturduğumuz backend CI pipeline'ını CI/CD pipeline'a dönüştüreceğiz. Mevcut pipeline'da bir **Build** aşaması tanımlayacağız ve buna ek olarak bir **Deploy** aşaması ekleyerek build sonucunda oluşan dosyaları IIS'de oluşturduğumuz siteye kopyalayacağız. Kopyalama işlemi sırasında **Application Pool**'u durdurup tekrar başlatacağız. Tüm işlemler **Visual Studio** kullanılarak gerçekleştirilecektir.

---

### 5.21.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **IIS Üzerinde Backend Sitesi Kurulmuş Olmalı**: Lab-20'de oluşturduğumuz backend sitesi çalışır durumda olmalıdır.
- **Self-Hosted Agent Kullanımı**: Pipeline işlemleri için self-hosted agent kullanılacaktır.
- **Visual Studio Kurulmuş Olmalı**: Proje üzerinde işlem yapmak için Visual Studio kurulu olmalıdır.

---

### 5.21.2 Adım 1: Visual Studio'da Branch Oluşturma

1. **Visual Studio'da Projeyi Açma**
   - Visual Studio'yu açın ve backend projenizi açın.
   - **Git Changes** penceresini açmak için Visual Studio'nun altındaki **Git** sekmesine gidin veya `View > Git Changes` seçeneğini seçin.

2. **Yeni Branch Oluşturma**
   - **Git Changes** penceresinden **Manage Branches** seçeneğine tıklayın.
   - Açılan pencerede **New Branch** butonuna tıklayın.
   - Branch adı olarak `feature/ci-cd-pipeline-update` yazın ve **Create Branch** butonuna tıklayın.

---

### 5.21.3 Adım 2: Pipeline Dosyasını Güncelleme

1. **Pipeline Dosyasını Açma**
   - Projenin kök dizinindeki `.azure-pipelines/ci-pipeline.yml` dosyasını bulun.
   - Dosya adını **ci-cd-pipeline.yml** olarak değiştirin.

2. **Pipeline İçeriğini Güncelleme**
   - **ci-cd-pipeline.yml** dosyasını açın ve aşağıdaki içerik ile güncelleyin:

     ```yaml
     trigger:
       branches:
         include:
           - main

     pool:
       name: 'Self-Hosted Agents' # Daha önce oluşturduğunuz agent pool adı

     variables:
       buildConfiguration: 'Release'
       deployPath: 'C:\\inetpub\\ProductManagement_Backend' # IIS Backend sitesi için hedef klasör
       appPoolName: 'ProductManagement_Backend' # IIS Application Pool adı

     stages:
       - stage: Build
         displayName: "Build Stage"
         jobs:
           - job: BuildJob
             displayName: "Build Backend Project"
             steps:
               - task: UseDotNet@2
                 displayName: 'Install .NET SDK'
                 inputs:
                   packageType: 'sdk'
                   version: '6.x'
                   installationPath: $(Agent.ToolsDirectory)/dotnet

               - script: |
                   dotnet restore
                   dotnet build --configuration $(buildConfiguration)
                   dotnet publish --configuration $(buildConfiguration) -o $(Build.ArtifactStagingDirectory)
                 displayName: 'Restore, Build, and Publish'

               - task: PublishBuildArtifacts@1
                 displayName: 'Publish Artifacts'
                 inputs:
                   PathtoPublish: '$(Build.ArtifactStagingDirectory)'
                   ArtifactName: 'drop'

       - stage: Deploy
         displayName: "Deploy Stage"
         dependsOn: Build
         jobs:
           - job: DeployJob
             displayName: "Deploy to IIS"
             steps:
               - task: PowerShell@2
                 displayName: "Stop Application Pool"
                 inputs:
                   targetType: 'inline'
                   script: |
                     Import-Module WebAdministration
                     Stop-WebAppPool -Name $(appPoolName)

               - task: DownloadBuildArtifacts@0
                 displayName: "Download Build Artifacts"
                 inputs:
                   artifactName: 'drop'
                   downloadPath: '$(System.ArtifactsDirectory)'

               - task: PowerShell@2
                 displayName: "Copy Files to IIS"
                 inputs:
                   targetType: 'inline'
                   script: |
                     Remove-Item -Recurse -Force $(deployPath)\*
                     Copy-Item -Path "$(System.ArtifactsDirectory)\drop\*" -Destination $(deployPath) -Recurse

               - task: PowerShell@2
                 displayName: "Start Application Pool"
                 inputs:
                   targetType: 'inline'
                   script: |
                     Import-Module WebAdministration
                     Start-WebAppPool -Name $(appPoolName)
     ```

3. **Değişiklikleri Kaydetme**
   - Visual Studio'da yaptığınız değişiklikleri kaydedin (`Ctrl+S`).

---

### 5.21.4 Adım 3: Commit, Push ve PR Oluşturma

1. **Değişiklikleri Commit Etme**
   - **Git Changes** penceresine gidin.
   - **Commit Message** olarak `CI/CD pipeline güncellendi, deploy adımı eklendi` yazın.
   - **Commit All and Push** butonuna tıklayın.

2. **Pull Request (PR) Oluşturma**
   - Visual Studio'da sağ alt köşede **Create Pull Request** seçeneğine tıklayın.
   - Açılan pencerede **Title** olarak `CI/CD pipeline güncellemesi` yazın.
   - PR açıklamasını şu şekilde ekleyin:
     ```
     CI/CD pipeline güncellendi. Build ve Deploy aşamaları eklendi.
     ```
   - **Create** butonuna tıklayarak PR'ı oluşturun.

---

### 5.21.5 Adım 4: Pipeline'ın Çalışmasını Test Etme

1. **Basit Bir Değişiklik Yapma**
   - Backend projesinde küçük bir değişiklik yapın, örneğin bir yorum ekleyin:
     ```csharp
     // CI/CD Pipeline testi için değişiklik.
     ```

2. **Değişikliği Commit ve Push Etme**
   - Değişiklikleri commit ve push edin:
     - **Commit Message**: `Basit değişiklik yapıldı, CI/CD pipeline testi için.`
     - **Commit All and Push** butonuna tıklayın.

3. **Pipeline'ın Tetiklenmesini Gözlemleme**
   - Azure DevOps portalında pipeline'ın çalıştığını doğrulayın.
   - **Build Stage** tamamlandıktan sonra **Deploy Stage**'in başladığını ve IIS'deki dosyaların güncellendiğini kontrol edin.

4. **IIS Sitesini Test Etme**
   - Tarayıcınızda `http://localhost:10100` adresine giderek backend API'sinin doğru bir şekilde çalıştığını doğrulayın.

---

### 5.21.6 Lab-21'in Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak backend CI pipeline'ını CI/CD pipeline'a dönüştürmüş, deploy işlemini içerecek şekilde güncellemiş ve pipeline'ın Visual Studio kullanılarak başarıyla çalıştığını doğrulamış oldunuz.

## 5.22 Lab-22: UI CI Pipeline'ını CI/CD Pipeline'a Dönüştürme ve Deploy Adımı Eklemek

Bu laboratuvar çalışmasında, daha önce oluşturduğumuz UI CI pipeline'ını CI/CD pipeline'a dönüştüreceğiz. Mevcut pipeline'da bir **Build** aşaması tanımlayacağız ve buna ek olarak bir **Deploy** aşaması ekleyerek build sonucunda oluşan dosyaları IIS'de oluşturduğumuz UI sitesine kopyalayacağız. Tüm işlemler **Visual Studio** kullanılarak gerçekleştirilecektir.

---

### 5.22.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **IIS Üzerinde UI Sitesi Kurulmuş Olmalı**: Lab-20'de oluşturduğumuz UI sitesi çalışır durumda olmalıdır.
- **Self-Hosted Agent Kullanımı**: Pipeline işlemleri için self-hosted agent kullanılacaktır.
- **Visual Studio Kurulmuş Olmalı**: Proje üzerinde işlem yapmak için Visual Studio kurulu olmalıdır.

---

### 5.22.2 Adım 1: Visual Studio'da Branch Oluşturma

1. **Visual Studio'da Projeyi Açma**
   - Visual Studio'yu açın ve UI projenizi açın.
   - **Git Changes** penceresini açmak için Visual Studio'nun altındaki **Git** sekmesine gidin veya `View > Git Changes` seçeneğini seçin.

2. **Yeni Branch Oluşturma**
   - **Git Changes** penceresinden **Manage Branches** seçeneğine tıklayın.
   - Açılan pencerede **New Branch** butonuna tıklayın.
   - Branch adı olarak `feature/ui-ci-cd-pipeline-update` yazın ve **Create Branch** butonuna tıklayın.

---

### 5.22.3 Adım 2: Pipeline Dosyasını Güncelleme

1. **Pipeline Dosyasını Açma**
   - Projenin kök dizinindeki `.azure-pipelines/ci-pipeline.yml` dosyasını bulun.
   - Dosya adını **ci-cd-pipeline.yml** olarak değiştirin.

2. **Pipeline İçeriğini Güncelleme**
   - **ci-cd-pipeline.yml** dosyasını açın ve aşağıdaki içerik ile güncelleyin:

     ```yaml
     trigger:
       branches:
         include:
           - main

     pool:
       name: 'Self-Hosted Agents' # Daha önce oluşturduğunuz agent pool adı

     variables:
       buildConfiguration: 'Release'
       deployPath: 'C:\\inetpub\\ProductManagement_UI' # IIS UI sitesi için hedef klasör
       appPoolName: 'ProductManagement_UI' # IIS Application Pool adı

     stages:
       - stage: Build
         displayName: "Build Stage"
         jobs:
           - job: BuildJob
             displayName: "Build UI Project"
             steps:
               - task: NodeTool@0
                 displayName: 'Use Node.js'
                 inputs:
                   versionSpec: '14.x'
                   checkLatest: true

               - script: |
                   npm install
                   npm run build --prod
                 displayName: 'Install Dependencies and Build'

               - task: PublishBuildArtifacts@1
                 displayName: 'Publish Artifacts'
                 inputs:
                   PathtoPublish: 'dist'
                   ArtifactName: 'drop'

       - stage: Deploy
         displayName: "Deploy Stage"
         dependsOn: Build
         jobs:
           - job: DeployJob
             displayName: "Deploy to IIS"
             steps:
               - task: PowerShell@2
                 displayName: "Stop Application Pool"
                 inputs:
                   targetType: 'inline'
                   script: |
                     Import-Module WebAdministration
                     Stop-WebAppPool -Name $(appPoolName)

               - task: DownloadBuildArtifacts@0
                 displayName: "Download Build Artifacts"
                 inputs:
                   artifactName: 'drop'
                   downloadPath: '$(System.ArtifactsDirectory)'

               - task: PowerShell@2
                 displayName: "Copy Files to IIS"
                 inputs:
                   targetType: 'inline'
                   script: |
                     Remove-Item -Recurse -Force $(deployPath)\*
                     Copy-Item -Path "$(System.ArtifactsDirectory)\drop\*" -Destination $(deployPath) -Recurse

               - task: PowerShell@2
                 displayName: "Start Application Pool"
                 inputs:
                   targetType: 'inline'
                   script: |
                     Import-Module WebAdministration
                     Start-WebAppPool -Name $(appPoolName)
     ```

3. **Değişiklikleri Kaydetme**
   - Visual Studio'da yaptığınız değişiklikleri kaydedin (`Ctrl+S`).

---

### 5.22.4 Adım 3: Commit, Push ve PR Oluşturma

1. **Değişiklikleri Commit Etme**
   - **Git Changes** penceresine gidin.
   - **Commit Message** olarak `CI/CD pipeline güncellendi, deploy adımı eklendi` yazın.
   - **Commit All and Push** butonuna tıklayın.

2. **Pull Request (PR) Oluşturma**
   - Visual Studio'da sağ alt köşede **Create Pull Request** seçeneğine tıklayın.
   - Açılan pencerede **Title** olarak `UI CI/CD pipeline güncellemesi` yazın.
   - PR açıklamasını şu şekilde ekleyin:
     ```
     CI/CD pipeline güncellendi. Build ve Deploy aşamaları eklendi.
     ```
   - **Create** butonuna tıklayarak PR'ı oluşturun.

---

### 5.22.5 Adım 4: Pipeline'ın Çalışmasını Test Etme

1. **Basit Bir Değişiklik Yapma**
   - UI projesinde küçük bir değişiklik yapın, örneğin `app.component.html` dosyasına bir yorum ekleyin:
     ```html
     <!-- CI/CD Pipeline testi için değişiklik -->
     ```

2. **Değişikliği Commit ve Push Etme**
   - Değişiklikleri commit ve push edin:
     - **Commit Message**: `Basit değişiklik yapıldı, CI/CD pipeline testi için.`
     - **Commit All and Push** butonuna tıklayın.

3. **Pipeline'ın Tetiklenmesini Gözlemleme**
   - Azure DevOps portalında pipeline'ın çalıştığını doğrulayın.
   - **Build Stage** tamamlandıktan sonra **Deploy Stage**'in başladığını ve IIS'deki dosyaların güncellendiğini kontrol edin.

4. **IIS Sitesini Test Etme**
   - Tarayıcınızda `http://localhost:10200` adresine giderek UI uygulamasının doğru bir şekilde çalıştığını doğrulayın.

---

### 5.22.6 Lab-22'nin Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak UI CI pipeline'ını CI/CD pipeline'a dönüştürmüş, deploy işlemini içerecek şekilde güncellemiş ve pipeline'ın Visual Studio kullanılarak başarıyla çalıştığını doğrulamış oldunuz. Bu süreç, UI projesinin otomatik dağıtım süreçlerini etkinleştirmeye yönelik temel bir adımdır.

## 5.23 Lab-23: YAML Dosyalarında Değişiklik Olduğunda PR Pipeline'ların Çalışmamasını Sağlamak için Branch Policy Ayarı Yapma

Bu laboratuvar çalışmasında, Azure DevOps üzerinde branch policy ayarlarını yapılandırarak YAML dosyalarında değişiklik yapıldığında PR pipeline'ların çalışmasını engelleyeceğiz. Bu ayar, pipeline'ın kendisiyle ilgili yapılan değişikliklerin otomatik tetiklenmesini önleyerek gereksiz pipeline çalıştırmalarını engeller.

---

### 5.23.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Azure DevOps Hesabı ve Pipeline Yetkileri**: Pipeline ve branch policy ayarlarını değiştirebilecek yönetici (admin) yetkisine sahip olmanız gerekir.
- **Pipeline ve Branch Policy**: Daha önce oluşturduğunuz backend ve UI projelerinin pipeline'ları ve branch policy'leri aktif olmalıdır.

---

### 5.23.2 Adım 1: YAML Dosyalarını İzleme Kapsamından Çıkarma

1. **Azure DevOps Portalına Giriş Yapma**
   - [Azure DevOps](https://dev.azure.com/) portalına gidin ve hesabınıza giriş yapın.

2. **Pipeline Ayarlarına Gitme**
   - **Pipelines** sekmesine gidin ve PR pipeline'ınızı seçin.
   - Sol tarafta bulunan **Triggers** sekmesine tıklayın.

3. **YAML Dosyalarını Hariç Tutma**
   - **Path filters** (Yol filtreleri) bölümüne gidin.
   - **Include** ve **Exclude** seçeneklerini göreceksiniz.
     - **Exclude** seçeneğine aşağıdaki yolu ekleyin:
       ```
       /.azure-pipelines/**
       ```

   - Bu ayar, `.azure-pipelines` klasörü içindeki tüm YAML dosyalarındaki değişikliklerin pipeline'ı tetiklemesini engelleyecektir.

4. **Ayarları Kaydetme**
   - **Save** butonuna tıklayarak ayarları kaydedin.

---

### 5.23.3 Adım 2: Branch Policy Ayarlarını Güncelleme

1. **Branch Policy Ayarlarına Gitme**
   - Sol menüden **Repos > Branches** sekmesine gidin.
   - `main` branch'ini bulun ve yanındaki üç nokta menüsünden **Branch policies** seçeneğine tıklayın.

2. **Build Validation Ayarlarını Güncelleme**
   - **Build validation** bölümünde ilgili pipeline'ı seçin ve düzenleyin.
   - **Path filters** (Yol filtreleri) kısmında:
     - **Exclude** kısmına aşağıdaki yolu ekleyin:
       ```
       /.azure-pipelines/**
       ```

   - Bu ayar, `main` branch'e yapılan PR'larda YAML dosyalarında değişiklik varsa pipeline'ı tetiklemeyecek şekilde yapılandırır.

3. **Ayarları Kaydetme**
   - **Save** butonuna tıklayarak değişiklikleri kaydedin.

---

### 5.23.4 Adım 3: Test Etme

1. **YAML Dosyasında Basit Bir Değişiklik Yapma**
   - Projenizdeki herhangi bir YAML dosyasına bir yorum ekleyin. Örneğin:
     ```yaml
     # Test değişikliği
     ```

2. **Değişikliği Commit ve Push Etme**
   - Visual Studio'da değişiklikleri commit ve push edin:
     - **Commit Message**: `YAML dosyasında test değişikliği.`
     - **Commit All and Push** butonuna tıklayın.

3. **Pull Request Oluşturma**
   - Azure DevOps portalında ilgili branch için bir pull request (PR) oluşturun.

4. **Pipeline'ın Çalışmadığını Doğrulama**
   - Pipeline sekmesine giderek, değişiklikleriniz için pipeline'ın tetiklenmediğini doğrulayın.

---

### 5.23.5 Lab-23'ün Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak, YAML dosyalarında yapılan değişikliklerin PR pipeline'ları tetiklemesini engellediniz. Bu ayar, pipeline yapılandırmalarında yapılan değişikliklerin gereksiz çalıştırmaları önlemesini sağlayarak CI/CD süreçlerinizi optimize eder.

## 5.24 Lab-24: Backend ve UI Pipeline'larına Deploy Adımı Öncesine Manuel Onay Eklemek

Bu laboratuvar çalışmasında, backend ve UI projeleri için ayrı **Environments** tanımlayarak **Deploy** adımı öncesinde manuel onay mekanizması ekleyeceğiz. Her iki proje için de farklı ortamlar oluşturulacak ve onay mekanizması bu ortamlar üzerinden yapılandırılacaktır.

---

### 5.24.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Azure DevOps Hesabı ve Yetkiler**: Pipeline düzenleme ve ortam yapılandırma işlemleri için yönetici yetkisine sahip olmanız gerekir.
- **Backend ve UI CI/CD Pipeline'ları**: Daha önce oluşturulmuş ve çalışan pipeline'lar mevcut olmalıdır.

---

### 5.24.2 Adım 1: Backend için "Backend-Production" Ortamı Oluşturma

1. **Backend Ortamını Oluşturma**
   - Azure DevOps portalına gidin ve sol menüden **Pipelines > Environments** seçeneğine tıklayın.
   - **New Environment** butonuna tıklayın.
   - **Environment Name** kısmına `Backend-Production` yazın ve oluşturun.

2. **Onay Mekanizması Ekleme**
   - Ortam detaylarına gidin.
   - **Approvals and Checks** bölümüne tıklayın.
   - **Approvals** seçeneğini seçin ve onay verecek kullanıcı veya grupları ekleyin.
   - **Save** butonuna tıklayarak ayarları kaydedin.

---

### 5.24.3 Adım 2: UI için "UI-Production" Ortamı Oluşturma

1. **UI Ortamını Oluşturma**
   - Azure DevOps portalında tekrar **Environments** sekmesine gidin.
   - **New Environment** butonuna tıklayın.
   - **Environment Name** kısmına `UI-Production` yazın ve oluşturun.

2. **Onay Mekanizması Ekleme**
   - Ortam detaylarına gidin.
   - **Approvals and Checks** bölümüne tıklayın.
   - **Approvals** seçeneğini seçin ve onay verecek kullanıcı veya grupları ekleyin.
   - **Save** butonuna tıklayarak ayarları kaydedin.

---

### 5.24.4 Adım 3: Backend Pipeline'ına Manuel Onay Eklemek

1. **Backend Pipeline YAML Dosyasını Düzenleme**
   - Projenizdeki `.azure-pipelines/ci-cd-pipeline.yml` dosyasını açın.
   - **Deploy** aşamasını aşağıdaki gibi düzenleyin:
     ```yaml
     stages:
       - stage: Build
         displayName: "Build Stage"
         jobs:
           - job: BuildJob
             displayName: "Build Backend Project"
             steps:
               # Build adımları

       - stage: Deploy
         displayName: "Deploy Stage"
         dependsOn: Build
         condition: succeeded()
         jobs:
           - deployment: DeployToIIS
             displayName: "Deploy to IIS"
             environment: 'Backend-Production' # Backend için ayrı bir environment
             strategy:
               runOnce:
                 deploy:
                   steps:
                     - task: PowerShell@2
                       displayName: "Stop Application Pool"
                       inputs:
                         targetType: 'inline'
                         script: |
                           Import-Module WebAdministration
                           Stop-WebAppPool -Name $(appPoolName)

                     - task: DownloadBuildArtifacts@0
                       displayName: "Download Build Artifacts"
                       inputs:
                         artifactName: 'drop'
                         downloadPath: '$(System.ArtifactsDirectory)'

                     - task: PowerShell@2
                       displayName: "Copy Files to IIS"
                       inputs:
                         targetType: 'inline'
                         script: |
                           Remove-Item -Recurse -Force $(deployPath)\*
                           Copy-Item -Path "$(System.ArtifactsDirectory)\drop\*" -Destination $(deployPath) -Recurse

                     - task: PowerShell@2
                       displayName: "Start Application Pool"
                       inputs:
                         targetType: 'inline'
                         script: |
                           Import-Module WebAdministration
                           Start-WebAppPool -Name $(appPoolName)
     ```

---

### 5.24.5 Adım 4: UI Pipeline'ına Manuel Onay Eklemek

1. **UI Pipeline YAML Dosyasını Düzenleme**
   - UI projesindeki `.azure-pipelines/ci-cd-pipeline.yml` dosyasını açın.
   - **Deploy** aşamasını aşağıdaki gibi düzenleyin:
     ```yaml
     stages:
       - stage: Build
         displayName: "Build Stage"
         jobs:
           - job: BuildJob
             displayName: "Build UI Project"
             steps:
               # Build adımları

       - stage: Deploy
         displayName: "Deploy Stage"
         dependsOn: Build
         condition: succeeded()
         jobs:
           - deployment: DeployToIIS
             displayName: "Deploy to IIS"
             environment: 'UI-Production' # UI için ayrı bir environment
             strategy:
               runOnce:
                 deploy:
                   steps:
                     - task: PowerShell@2
                       displayName: "Stop Application Pool"
                       inputs:
                         targetType: 'inline'
                         script: |
                           Import-Module WebAdministration
                           Stop-WebAppPool -Name $(appPoolName)

                     - task: DownloadBuildArtifacts@0
                       displayName: "Download Build Artifacts"
                       inputs:
                         artifactName: 'drop'
                         downloadPath: '$(System.ArtifactsDirectory)'

                     - task: PowerShell@2
                       displayName: "Copy Files to IIS"
                       inputs:
                         targetType: 'inline'
                         script: |
                           Remove-Item -Recurse -Force $(deployPath)\*
                           Copy-Item -Path "$(System.ArtifactsDirectory)\drop\*" -Destination $(deployPath) -Recurse

                     - task: PowerShell@2
                       displayName: "Start Application Pool"
                       inputs:
                         targetType: 'inline'
                         script: |
                           Import-Module WebAdministration
                           Start-WebAppPool -Name $(appPoolName)
     ```

---

### 5.24.6 Adım 5: Test Etme

1. **Basit Değişiklikler Yapma**
   - Backend ve UI projelerinde küçük bir değişiklik yapın, örneğin bir yorum ekleyin:
     ```csharp
     // Manual approval testi için değişiklik.
     ```
     ```html
     <!-- Manual approval testi için değişiklik -->
     ```

2. **Değişiklikleri Commit ve Push Etme**
   - Değişikliklerinizi ilgili branch'e commit ve push edin.

3. **Pull Request (PR) Oluşturma**
   - Azure DevOps portalında her iki proje için PR oluşturun.

4. **Pipeline'ın Tetiklenmesini ve Onay Sürecini Doğrulama**
   - PR pipeline'larının **Build** aşamasını tamamlamasını bekleyin.
   - **Deploy** aşamasında pipeline'ın durduğunu ve onay beklediğini doğrulayın.
   - Portalda ilgili ortamlar için onay verin.
   - Onaydan sonra pipeline'ın devam edip başarıyla tamamlandığını gözlemleyin.

---

### 5.24.7 Lab-24'ün Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak backend ve UI projeleriniz için ayrı ortamlar oluşturup, deploy adımı öncesinde manuel onay eklediniz. Bu ayarlar, her bir proje için bağımsız kontrol ve güvenlik sağlayarak dağıtım süreçlerinizi daha güvenilir hale getirir.

## 5.25 Lab-25: Backend Projesine Unit Testleri Eklemek ve Visual Studio Üzerinden Çalıştırmak

Bu laboratuvar çalışmasında, backend projesine **unit testler** ekleyecek ve Visual Studio üzerinden bu testleri çalıştırarak başarılı olup olmadıklarını gözlemleyeceğiz. Unit testler, kodun doğru çalıştığını kontrol etmek ve hataları erken aşamada tespit etmek için önemlidir.

---

### 5.25.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Visual Studio Yüklü Olmalı**: Backend projenizi açabileceğiniz ve unit test yazabileceğiniz bir Visual Studio kurulumuna sahip olmalısınız.
- **Backend Projesi**: Daha önce oluşturduğunuz backend projesi çalışır durumda olmalıdır.
- **Unit Test Frameworkleri**: `xUnit`, `MSTest` veya `NUnit` gibi bir test framework'ü kullanabilirsiniz. Bu laboratuvarda `xUnit` kullanılacaktır.

---

### 5.25.2 Adım 1: Unit Test Projesi Eklemek

1. **Unit Test Projesi Ekleme**
   - Visual Studio'da backend projenizi açın.
   - **Solution Explorer**'da çözüm adına sağ tıklayın ve **Add > New Project** seçeneğini seçin.
   - Açılan pencerede **Unit Test Project (.NET Core)** şablonunu bulun ve seçin.
   - Proje adını `ProductManagement.Tests` olarak belirleyin ve **Create** butonuna tıklayın.

2. **xUnit Framework'ünü Yükleme**
   - Unit test projesine sağ tıklayın ve **Manage NuGet Packages** seçeneğini seçin.
   - **Browse** sekmesinde `xunit` paketini arayın ve yükleyin.
   - Ayrıca `xunit.runner.visualstudio` paketini de yükleyerek Visual Studio Test Explorer ile entegrasyonu sağlayın.

3. **Backend Projesini Referans Ekleme**
   - Unit test projesine sağ tıklayın ve **Add > Project Reference** seçeneğini seçin.
   - Açılan listeden backend projenizi seçin ve **OK** butonuna tıklayın.

---

### 5.25.3 Adım 2: Test Sınıfı ve Metotları Yazma

1. **Yeni Test Sınıfı Oluşturma**
   - `ProductManagement.Tests` projesinde `Tests` adında bir klasör oluşturun.
   - Bu klasörün içine `ProductServiceTests.cs` adında yeni bir sınıf ekleyin.

2. **Test Metotlarını Yazma**
   - Aşağıdaki örnek kodu `ProductServiceTests.cs` dosyasına ekleyin:
     ```csharp
     using Xunit;
     using Moq;
     using ProductManagement.Services;
     using ProductManagement.Models;

     public class ProductServiceTests
     {
         private readonly ProductService _productService;
         private readonly Mock<IProductRepository> _mockRepository;

         public ProductServiceTests()
         {
             _mockRepository = new Mock<IProductRepository>();
             _productService = new ProductService(_mockRepository.Object);
         }

         [Fact]
         public void GetAllProducts_ShouldReturnListOfProducts()
         {
             // Arrange
             var products = new List<Product>
             {
                 new Product { Id = 1, ProductName = "Product A", Price = 10.0, Stock = 100 },
                 new Product { Id = 2, ProductName = "Product B", Price = 20.0, Stock = 200 }
             };

             _mockRepository.Setup(repo => repo.GetAll()).Returns(products);

             // Act
             var result = _productService.GetAllProducts();

             // Assert
             Assert.NotNull(result);
             Assert.Equal(2, result.Count);
         }

         [Fact]
         public void AddProduct_ShouldCallRepositoryAdd()
         {
             // Arrange
             var product = new Product { Id = 3, ProductName = "Product C", Price = 30.0, Stock = 300 };

             // Act
             _productService.AddProduct(product);

             // Assert
             _mockRepository.Verify(repo => repo.Add(It.IsAny<Product>()), Times.Once);
         }
     }
     ```

3. **Mocking Kütüphanesi Yükleme**
   - `MoQ` kütüphanesini eklemek için **Manage NuGet Packages** üzerinden `Moq` paketini yükleyin.

---

### 5.25.4 Adım 3: Unit Testleri Çalıştırma

1. **Test Explorer'ı Açma**
   - Visual Studio'da **Test > Test Explorer** menüsüne giderek Test Explorer penceresini açın.

2. **Testleri Çalıştırma**
   - **Test Explorer** penceresinde testlerin yüklendiğini göreceksiniz.
   - Tüm testleri çalıştırmak için **Run All** butonuna tıklayın.
   - Çalıştırılan testlerin durumunu Test Explorer'da gözlemleyin:
     - Geçen testler yeşil olarak işaretlenecektir.
     - Başarısız olan testler kırmızı olarak işaretlenecektir.

---

### 5.25.5 Adım 4: Test Sonuçlarını Analiz Etme

1. **Geçen Testleri Kontrol Etme**
   - Testler yeşil olarak işaretlendiyse, ilgili kodun beklendiği gibi çalıştığını doğrular.

2. **Başarısız Olan Testleri Düzeltme**
   - Başarısız olan testler için Test Explorer'da testin üzerine tıklayın.
   - Hatanın nedenini öğrenmek için detayları inceleyin ve ilgili kodu düzeltin.
   - Düzeltmelerden sonra tekrar **Run All** butonuna tıklayarak testleri yeniden çalıştırın.

---

### 5.25.6 Lab-25'in Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak backend projenize unit testler eklediniz, testlerinizi Visual Studio üzerinden çalıştırdınız ve test sonuçlarını analiz ettiniz. Bu süreç, projenizin kalite güvencesini artırmak ve potansiyel hataları erken aşamada tespit etmek için önemli bir adımdır.

## 5.27 Lab-27: Backend Pipeline'da Build Adımına Test Adımı Eklemek ve Test Sonuçlarını Publish Etmek

Bu laboratuvar çalışmasında, backend pipeline'ına **testleri çalıştıran bir adım** ekleyeceğiz. Bu adım, unit testlerin pipeline sırasında çalıştırılmasını sağlayacak ve test sonuçlarını Azure DevOps pipeline arayüzüne yayınlayacaktır. Test sonuçlarını pipeline arayüzünde gözlemleyerek, testlerin başarılı veya başarısız olduğunu kolayca takip edebilirsiniz.

---

### 5.27.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Unit Testler Eklenmiş Olmalı**: Lab-25'te eklediğiniz unit testler backend projenizde mevcut olmalıdır.
- **Pipeline YAML Dosyası**: Backend projenizin pipeline'ı YAML formatında tanımlanmış olmalıdır.
- **Test Framework**: `xUnit`, `NUnit` veya `MSTest` gibi bir test framework'ü kullanılabilir. Bu laboratuvarda `xUnit` kullanılmıştır.

---

### 5.27.2 Adım 1: Pipeline YAML Dosyasını Düzenleme

1. **Pipeline Dosyasını Açma**
   - Projenizdeki `.azure-pipelines/ci-cd-pipeline.yml` dosyasını açın.

2. **Build Adımına Test Çalıştırma Eklemek**
   - Aşağıdaki kodu **Build Stage** içinde uygun bir yere ekleyin:
     ```yaml
     - script: |
         dotnet test --configuration $(buildConfiguration) --no-build --logger trx
       displayName: "Run Unit Tests"
     ```

3. **Test Sonuçlarını Publish Etme**
   - Test sonuçlarını Azure DevOps pipeline'ına yayınlamak için şu adımı ekleyin:
     ```yaml
     - task: PublishTestResults@2
       displayName: "Publish Test Results"
       inputs:
         testResultsFiles: '**/*.trx'
         searchFolder: '$(System.DefaultWorkingDirectory)'
         mergeTestResults: true
     ```

4. **Güncellenmiş Pipeline Yapısı**
   - Build Stage şu şekilde görünmelidir:
     ```yaml
     stages:
       - stage: Build
         displayName: "Build Stage"
         jobs:
           - job: BuildJob
             displayName: "Build Backend Project"
             steps:
               - task: UseDotNet@2
                 displayName: 'Install .NET SDK'
                 inputs:
                   packageType: 'sdk'
                   version: '6.x'
                   installationPath: $(Agent.ToolsDirectory)/dotnet

               - script: |
                   dotnet restore
                   dotnet build --configuration $(buildConfiguration)
                 displayName: "Restore and Build"

               - script: |
                   dotnet test --configuration $(buildConfiguration) --no-build --logger trx
                 displayName: "Run Unit Tests"

               - task: PublishTestResults@2
                 displayName: "Publish Test Results"
                 inputs:
                   testResultsFiles: '**/*.trx'
                   searchFolder: '$(System.DefaultWorkingDirectory)'
                   mergeTestResults: true

               - task: PublishBuildArtifacts@1
                 displayName: "Publish Build Artifacts"
                 inputs:
                   PathtoPublish: '$(Build.ArtifactStagingDirectory)'
                   ArtifactName: 'drop'
     ```

5. **Pipeline Dosyasını Commit ve Push Etme**
   - Visual Studio veya terminal üzerinden değişikliklerinizi commit ve push edin:
     ```bash
     git add .azure-pipelines/ci-cd-pipeline.yml
     git commit -m "Build adımına test çalıştırma ve sonuç yayınlama eklendi"
     git push origin <branch-name>
     ```

---

### 5.27.3 Adım 2: Pipeline Çalıştırma ve Test Sonuçlarını Gözlemleme

1. **Pipeline'ı Tetiklemek için PR Oluşturma**
   - Değişikliklerinizi `main` branch'e merge etmek için bir pull request (PR) oluşturun.
   - PR'ın oluşturulmasıyla pipeline otomatik olarak tetiklenecektir.

2. **Pipeline'ın Çalışmasını İzleme**
   - Azure DevOps portalında ilgili pipeline'ı açın ve **Build Stage**'i gözlemleyin.
   - **Run Unit Tests** adımında testlerin çalıştırıldığını doğrulayın.

3. **Test Sonuçlarını İnceleme**
   - Pipeline tamamlandığında **Tests** sekmesine gidin.
   - Burada çalıştırılan tüm unit testlerin durumunu görebilirsiniz:
     - Geçen testler yeşil olarak işaretlenecektir.
     - Başarısız olan testler kırmızı olarak işaretlenecektir.
   - Detaylı hata raporları için bir testin üzerine tıklayarak çıktıyı inceleyebilirsiniz.

---

### 5.27.4 Adım 3: Başarısız Testlerin Ele Alınması

1. **Hatalı Testleri İnceleme**
   - Test Explorer'da veya pipeline üzerindeki test detaylarında başarısız testleri kontrol edin.
   - Hataların nedenlerini analiz edin ve ilgili kodu düzeltin.

2. **Düzeltmeleri Commit ve Push Etme**
   - Hataları düzelttikten sonra testlerinizi lokal olarak çalıştırın ve başarılı olduklarını doğrulayın.
   - Değişikliklerinizi tekrar commit ve push ederek pipeline'ı yeniden çalıştırın.

---

### 5.27.5 Lab-27'nin Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak backend pipeline'ınıza testleri çalıştıran bir adım eklediniz ve test sonuçlarını Azure DevOps pipeline arayüzüne yayınladınız. Bu işlem, kod kalitesini artırarak potansiyel hataların erken tespit edilmesini sağlar.

## 5.28 Lab-28: Container ve Sanal Makine Teknolojileri Karşılaştırması ve Docker Desktop Kurulumu

Bu laboratuvar çalışmasında, container teknolojileri ile sanal makine (VM) teknolojilerini karşılaştıracak ve ardından Docker Desktop kurulumunu adım adım anlatacağız. Öncesinde, sanal makinelerin ve container teknolojilerinin tarihçesini inceleyeceğiz.

---

### 5.28.1 Sanal Makineler ve Container Teknolojilerinin Tarihçesi

#### 5.28.1.1 Sanal Makinelerin Tarihçesi
Sanal makineler, donanım seviyesinde yalıtım sağlayarak birden fazla işletim sisteminin aynı fiziksel sunucuda çalışmasına olanak tanır. 

- **1960'lar**:
  - IBM, büyük sunucuların farklı görevleri aynı anda yerine getirebilmesi için **IBM CP-40** ve **CP-67** projelerini geliştirdi. Bu, sanal makine konseptinin temellerini attı.
  - İlk sanallaştırma teknolojileri, donanımın verimli kullanılmasını ve maliyetlerin azaltılmasını hedefliyordu.

- **1990'lar**:
  - VMware, 1999'da **VMware Workstation**'ı piyasaya sürdü. Bu, modern sanal makinelerin başlangıcı oldu ve kişisel bilgisayarlarda sanallaştırmayı mümkün kıldı.
  - Sanal makineler, özellikle veri merkezlerinde büyük ölçekli uygulamalarda popüler hale geldi.

- **2000'ler**:
  - Microsoft, 2008 yılında **Hyper-V**'yi piyasaya sürdü. Bu, Windows işletim sistemine entegre bir hipervizör sunuyordu.
  - Sanal makineler, bulut bilişim ile birleştirildi ve **Amazon EC2** gibi hizmetler ortaya çıktı.

#### 5.28.1.2 Container Teknolojilerinin Tarihçesi
Container teknolojileri, sanal makinelerden farklı olarak işletim sistemi seviyesinde yalıtım sağlar ve daha hafiftir.

- **1970'ler**:
  - **chroot** komutu, 1979'da Unix için tanıtıldı. Bu, bir işlemi dosya sistemi seviyesinde izole etmek için kullanılan ilk teknolojiydi.
  - chroot, modern container teknolojilerinin öncüsü olarak kabul edilir.

- **2000'ler**:
  - 2001 yılında **FreeBSD Jail** teknolojisi tanıtıldı. Bu, bir işletim sistemi içinde birden fazla izole edilmiş ortam oluşturmayı mümkün kıldı.
  - **OpenVZ** ve **Linux VServer** gibi projeler, Linux üzerinde container benzeri çözümler geliştirdi.

- **2010'lar**:
  - 2013 yılında **Docker** tanıtıldı. Docker, container teknolojisini standartlaştırdı ve kullanımı kolay bir platform sundu. Bu, container'ların popülerliğini artırdı.
  - Kubernetes, 2014 yılında Google tarafından açık kaynaklı olarak yayınlandı. Kubernetes, container'ların otomatik olarak yönetilmesini sağladı ve DevOps süreçlerinde devrim yarattı.

#### 5.28.1.3 Modern Dönem
- **2020'ler**:
  - Container teknolojileri, mikroservis mimarilerinin ve bulut tabanlı uygulamaların temel taşı haline geldi.
  - Docker, Kubernetes ve Podman gibi araçlar, DevOps ve sürekli entegrasyon/sürekli dağıtım (CI/CD) süreçlerinin ayrılmaz bir parçası oldu.
  - Sanal makineler ise veri merkezleri ve güvenlik gereksinimleri yüksek olan uygulamalar için tercih edilmeye devam etti.

---

### 5.28.2 Container ve Sanal Makine Teknolojilerinin Karşılaştırılması

| Özellik                  | Container                                          | Sanal Makine (VM)                                   |
|--------------------------|---------------------------------------------------|----------------------------------------------------|
| **Tanım**                | Uygulamaları ve bağımlılıklarını izole eder.       | İşletim sistemi seviyesinde tamamen izole edilmiş bir ortam sağlar. |
| **Performans**           | Host işletim sistemi kaynaklarını doğrudan kullanır, daha hızlıdır. | Kendi işletim sistemi çekirdeği ile çalıştığı için daha ağırdır. |
| **Boyut**                | Hafiftir, birkaç MB büyüklüğünde olabilir.        | Genellikle birkaç GB büyüklüğündedir.             |
| **Başlatma Süresi**      | Milisaniyeler içinde başlatılabilir.              | Dakikalar sürebilir.                              |
| **Kaynak Kullanımı**     | Paylaşımlı çekirdek kullanımı nedeniyle az kaynak tüketir. | Daha fazla CPU, bellek ve disk alanı gerektirir.  |
| **Esneklik**             | Mikroservis tabanlı mimarilere daha uygundur.      | Monolitik uygulamalar için daha uygundur.         |
| **Yalıtım**              | İşlem seviyesinde yalıtım sağlar.                 | Donanım seviyesinde yalıtım sağlar.              |
| **Kullanım Alanı**       | Modern yazılım geliştirme, CI/CD, bulut tabanlı uygulamalar. | Yüksek güvenlik gereksinimleri ve legacy uygulamalar. |

**Özet**: Container teknolojileri, hafif ve hızlı olmaları nedeniyle modern yazılım geliştirme ve dağıtım süreçlerinde daha yaygın olarak kullanılmaktadır. Sanal makineler ise yüksek güvenlik ve izolasyon gereksinimlerinde tercih edilmektedir.

---

### 5.28.3 Docker Desktop Kurulumu

#### 5.28.3.1 Ön Gereksinimler

- **İşletim Sistemi**: Windows 10 (64-bit) Pro, Enterprise veya Education; macOS; veya Linux.
- **Sanalizasyon Desteği**: BIOS/UEFI üzerinden sanallaştırmanın etkinleştirilmiş olması gerekir.
- **Donanım Gereksinimleri**:
  - 4 GB RAM veya daha fazla.
  - 64-bit işlemci.

#### 5.28.3.2 Kurulum Adımları (Windows)

1. **Docker Desktop İndirme**
   - [Docker Resmi Web Sitesi](https://www.docker.com/products/docker-desktop) adresine gidin.
   - **Download for Windows** butonuna tıklayarak Docker Desktop kurulum dosyasını indirin.

2. **Kurulum Dosyasını Çalıştırma**
   - İndirdiğiniz `Docker Desktop Installer.exe` dosyasını çift tıklayarak çalıştırın.
   - Açılan pencerede **Install** butonuna tıklayın.

3. **Kurulum Seçeneklerini Yapılandırma**
   - **WSL 2 Backend Kullanımı**: WSL 2 (Windows Subsystem for Linux) backend'ini kullanmayı tercih edin. WSL 2 kurulumu otomatik yapılmazsa, [WSL Kurulum Kılavuzu](https://learn.microsoft.com/en-us/windows/wsl/install) adresini takip ederek WSL 2'yi etkinleştirin.

4. **Docker Desktop Kurulumunu Tamamlama**
   - Kurulum tamamlandıktan sonra bilgisayarınızı yeniden başlatmanız gerekebilir.
   - Docker Desktop uygulamasını başlatın.

5. **Docker Desktop İlk Ayarları**
   - Docker Desktop ilk kez başlatıldığında, lisans koşullarını kabul edin.
   - **Start Docker Desktop** butonuna tıklayın.

6. **Kurulumu Doğrulama**
   - PowerShell veya terminali açın ve şu komutu çalıştırın:
     ```bash
     docker --version
     ```
   - Çıktıda Docker sürümünü görüyorsanız, kurulum başarılı olmuştur.

---

### 5.28.4 Docker Desktop Kurulumunu Test Etme

1. **Hello World Container Çalıştırma**
   - Docker'ın doğru kurulduğunu test etmek için şu komutu çalıştırın:
     ```bash
     docker run hello-world
     ```
   - Bu komut, Docker Hub'dan `hello-world` image'ini indirir ve bir container olarak çalıştırır. Çıktıda Docker'ın başarıyla çalıştığını belirten bir mesaj göreceksiniz.

2. **Docker Dashboard Kullanımı**
   - Docker Desktop uygulamasını açarak çalışmakta olan container'ları ve diğer kaynakları görsel olarak kontrol edebilirsiniz.

---

### 5.28.5 Lab-28'in Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak sanal makineler ve container teknolojilerinin tarihçesini incelediniz, Docker Desktop kurulumunu gerçekleştirdiniz ve kurulumu başarıyla test ettiniz. Bir sonraki laboratuvarda Docker container'larını daha ayrıntılı bir şekilde inceleyeceğiz.

## 5.29 Lab-29: Backend Projesine Docker Desteği Eklemek ve Container İçerisinde Debug Yapmak

Bu laboratuvar çalışmasında, **ProductManagement** backend projesine Docker desteği ekleyeceğiz. Visual Studio kullanarak bir **Dockerfile** oluşturacak ve projenizi container içerisinde çalıştırıp debug edeceksiniz. Bu işlem, Docker container'ları ile çalışırken geliştirme ve hata ayıklama süreçlerini kolaylaştıracaktır.

---

### 5.29.1 Ön Hazırlıklar

Laboratuvar çalışmasına başlamadan önce aşağıdaki gereksinimlerin karşılandığından emin olun:

- **Docker Desktop**: Lab-28'de anlatıldığı şekilde Docker Desktop kurulu ve çalışır durumda olmalıdır.
- **Visual Studio**: Docker desteği olan bir Visual Studio sürümü (ör. Visual Studio 2022) yüklü olmalıdır.
- **Backend Projesi**: ASP.NET Core tabanlı backend projesi mevcut olmalıdır.

---

### 5.29.2 Adım 1: Backend Projesine Docker Desteği Eklemek

1. **Docker Desteği Ekleme**
   - Visual Studio'da backend projenizi açın.
   - **Solution Explorer**'da projenize sağ tıklayın ve **Add > Docker Support** seçeneğini seçin.
   - Açılan pencerede **Target OS** olarak **Linux** veya **Windows** seçeneğini seçin (Linux önerilir).
   - Visual Studio, projenize bir **Dockerfile** ve **docker-compose** dosyaları ekleyecektir.

2. **Dockerfile İçeriğini İnceleme**
   - Visual Studio tarafından otomatik oluşturulan `Dockerfile` şu şekilde görünebilir:
     ```dockerfile
     # Use the official .NET image as a base image
     FROM mcr.microsoft.com/dotnet/aspnet:6.0 AS base
     WORKDIR /app
     EXPOSE 80
     EXPOSE 443

     FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build
     WORKDIR /src
     COPY ["ProductManagement/ProductManagement.csproj", "ProductManagement/"]
     RUN dotnet restore "ProductManagement/ProductManagement.csproj"
     COPY . .
     WORKDIR "/src/ProductManagement"
     RUN dotnet build "ProductManagement.csproj" -c Release -o /app/build

     FROM build AS publish
     RUN dotnet publish "ProductManagement.csproj" -c Release -o /app/publish

     FROM base AS final
     WORKDIR /app
     COPY --from=publish /app/publish .
     ENTRYPOINT ["dotnet", "ProductManagement.dll"]
     ```

3. **Proje Dosyalarını Düzenleme**
   - Projenizdeki `Dockerfile` dosyasını inceleyin ve ihtiyaçlarınıza göre düzenleyin. Örneğin, özel portlar eklemek veya ek bağımlılıklar yüklemek için `EXPOSE` veya `RUN` komutlarını güncelleyebilirsiniz.

---

### 5.29.3 Adım 2: Docker Container Oluşturma ve Çalıştırma

1. **Container Oluşturma**
   - Visual Studio'nun üst menüsünden **Docker** profilini seçin.
   - Projeyi **F5 (Start Debugging)** ile başlatın.
   - Visual Studio, Docker container'ını oluşturacak, gerekli image'i build edecek ve uygulamayı container içerisinde çalıştıracaktır.

2. **Container Çalıştırma Durumunu Kontrol Etme**
   - Docker Desktop uygulamasını açarak container'ın çalıştığını doğrulayabilirsiniz.
   - Alternatif olarak terminalde şu komutu çalıştırabilirsiniz:
     ```bash
     docker ps
     ```
   - Çalışan container'ın adını ve durumunu listeleyebilirsiniz.

3. **Uygulamayı Test Etme**
   - Tarayıcınızda, Docker container'ınızın host ettiği uygulamayı kontrol etmek için `http://localhost:<mapped-port>` adresine gidin.
   - Uygulamanızın doğru bir şekilde çalıştığını doğrulayın.

---

### 5.29.4 Adım 3: Container İçerisinde Debug Yapmak

1. **Visual Studio ile Debug Modu**
   - Visual Studio'da **Docker** profilinin seçili olduğundan emin olun.
   - **Breakpoint** eklemek istediğiniz dosyayı açın ve bir veya daha fazla satıra breakpoint ekleyin.
   - Uygulamayı başlatmak için **F5** tuşuna basın.
   - Uygulama bir Docker container içerisinde çalışırken, Visual Studio otomatik olarak container'a bağlanacak ve breakpoint'ler tetiklenince debug işlemini başlatacaktır.

2. **Hata Ayıklama Süreci**
   - Debugging sırasında Visual Studio'dan aşağıdaki işlemleri yapabilirsiniz:
     - Kod adımlarını takip etme (Step Over, Step Into, Step Out).
     - Değişken değerlerini izleme.
     - Uygulama performansını gözlemleme.
   - Debugging tamamlandıktan sonra **Shift + F5** tuşlarına basarak debugging modundan çıkabilirsiniz.

3. **Logları İnceleme**
   - Docker container loglarını terminal üzerinden kontrol etmek için şu komutu çalıştırabilirsiniz:
     ```bash
     docker logs <container-id>
     ```
   - Bu loglar, container içerisinde çalıştırılan uygulamanızla ilgili önemli bilgiler sunar.

---

### 5.29.5 Lab-29'un Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak backend projenize Docker desteği eklediniz, Visual Studio üzerinden container oluşturup çalıştırdınız ve container içerisinde debugging yaptınız. Docker container'larında hata ayıklama yapmak, container tabanlı uygulamaları geliştirirken oldukça kullanışlıdır.

## 5.30 Lab-30: Backend Projesini IIS Üzerinde Host Etmek Yerine Docker Üzerinde Host Etmek ve Değişiklikleri Main Branch'e Atmak

Bu laboratuvar çalışmasında, backend projesini IIS üzerinde host etmek yerine Docker container içerisinde çalıştıracağız. IIS üzerindeki siteyi durduracak ve Docker üzerinden çalışacak şekilde konfigüre edeceğiz. Ayrıca, UI projesinin Docker üzerinde çalışan backend ile uyumlu şekilde çalıştığını test edeceğiz. Backend ve UI projelerindeki değişiklikleri **main** branch'e göndererek tamamlanmış bir yapı oluşturacağız.

---

### 5.30.1 Ön Hazırlıklar

- **Docker Desktop**: Docker Desktop yüklü ve çalışır durumda olmalıdır.
- **Dockerfile**: Backend ve UI projelerinizde `Dockerfile` dosyaları mevcut olmalıdır.
- **IIS**: IIS üzerinde çalışan backend sitesi durdurulacak ve kaldırılacaktır.
- **Git Yetkileri**: Değişiklikleri `main` branch'e göndermek için gerekli yetkilere sahip olmalısınız.

---

### 5.30.2 Adım 1: IIS Üzerindeki Backend Sitesini Durdurmak

1. **IIS Manager'ı Açma**
   - Windows'da `inetmgr` komutunu çalıştırarak IIS Manager'ı açın.

2. **Backend Sitesini Durdurma**
   - IIS Manager'da backend sitenizi bulun (`ProductManagement_Backend`).
   - Siteye sağ tıklayın ve **Stop** seçeneğini seçin.

3. **Application Pool'u Durdurma**
   - Sol menüden **Application Pools** sekmesine gidin.
   - Backend için kullanılan Application Pool'u bulun ve sağ tıklayarak **Stop** seçeneğini seçin.

---

### 5.30.3 Adım 2: Backend Projesini Docker Üzerinde Host Etmek

1. **Docker Image Oluşturma**
   - Backend projesinin bulunduğu dizinde terminali açın.
   - Docker image oluşturmak için şu komutu çalıştırın:
     ```bash
     docker build -t productmanagement-backend .
     ```

2. **Container Oluşturma ve Çalıştırma**
   - Oluşturulan image'den bir container çalıştırmak için şu komutu çalıştırın:
     ```bash
     docker run -d -p 10101:80 --name productmanagement-backend-container productmanagement-backend
     ```

3. **Container'ın Çalıştığını Doğrulama**
   - Terminalde şu komutu çalıştırarak çalışan container'ları listeleyin:
     ```bash
     docker ps
     ```

4. **API'yi Test Etme**
   - Tarayıcınızda veya Postman'de `http://localhost:10101/api/products` gibi bir endpoint'e giderek backend API'sinin çalıştığını doğrulayın.

---

### 5.30.4 Adım 3: UI Projesini Docker Backend ile Çalışacak Şekilde Yapılandırma

1. **UI Projesinde Backend API URL'sini Güncelleme**
   - UI projesindeki `environment.ts` dosyasını açın ve `apiUrl` değerini Docker'daki backend'e yönlendirin:
     ```typescript
     export const environment = {
       production: true,
       apiUrl: 'http://localhost:10101/api'
     };
     ```

2. **UI Projesini Çalıştırma**
   - UI projesini Docker üzerinden çalıştırıyorsanız, `docker-compose` veya ilgili container ayarlarının doğru olduğundan emin olun.
   - Eğer lokal olarak çalıştırıyorsanız, şu komutla başlatın:
     ```bash
     ng serve
     ```

3. **UI'da Backend Entegrasyonunu Test Etme**
   - Tarayıcınızda `http://localhost:4200` adresine gidin ve UI üzerinden backend ile iletişimi test edin.
   - Örneğin, ürün listeleme sayfasında backend'den gelen ürünlerin başarıyla yüklendiğini doğrulayın.

---

### 5.30.5 Adım 4: Değişiklikleri Main Branch'e Gönderme

1. **Değişiklikleri Commit Etme**
   - Visual Studio'da **Git Changes** sekmesini açın.
   - **Commit Message** kısmına şu mesajı yazın:
     ```
     Docker konfigürasyonu tamamlandı. Backend ve UI projeleri Docker üzerinde çalışacak şekilde yapılandırıldı.
     ```
   - **Commit All** butonuna tıklayın.

2. **Değişiklikleri Push Etme**
   - Commit işleminden sonra **Push** butonuna tıklayarak değişikliklerinizi remote branch'e gönderin.

3. **Pull Request (PR) Oluşturma**
   - Azure DevOps portalına giderek backend ve UI projeleriniz için **main** branch'e merge edilmek üzere bir PR oluşturun.
   - PR açıklamasına şu bilgileri ekleyin:
     ```
     - Backend projesi Docker üzerinde çalışacak şekilde yapılandırıldı.
     - IIS üzerindeki site kaldırıldı.
     - UI projesi, Docker backend ile uyumlu hale getirildi.
     ```

4. **PR Onayı ve Merge İşlemi**
   - PR'ınız için gerekli onayları aldıktan sonra **Complete Merge** butonuna tıklayarak değişiklikleri `main` branch'e merge edin.

---

### 5.30.6 Lab-30'un Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak backend projenizi Docker üzerinde çalışacak şekilde yapılandırdınız, IIS üzerindeki host işlemlerini durdurdunuz, UI projesini Docker backend ile entegre ettiniz ve tüm değişiklikleri **main** branch'e merge ettiniz. Artık projeniz container tabanlı bir geliştirme ve dağıtım ortamında çalışmaktadır.

## 5.31 Lab-31: Docker Hub Kullanıcısı Oluşturma ve Azure DevOps'a Docker Hub'ı Service Connection Olarak Ekleme

Bu laboratuvar çalışmasında, Docker Hub üzerinde bir kullanıcı oluşturacak ve Azure DevOps üzerinde bir **service connection** oluşturarak Docker Hub ile entegrasyonu sağlayacağız. Bu adım, Docker image'lerini Azure DevOps pipeline'larından Docker Hub'a push edebilmek için gereklidir.

---

### 5.31.1 Docker Hub Kullanıcısı Oluşturma

1. **Docker Hub Web Sitesine Gidin**
   - Tarayıcınızda [https://hub.docker.com](https://hub.docker.com) adresine gidin.

2. **Yeni Hesap Oluşturma**
   - Sağ üst köşedeki **Sign Up** butonuna tıklayın.
   - Gerekli bilgileri doldurun:
     - **Username**: Docker Hub'da kullanılacak benzersiz bir kullanıcı adı.
     - **Email Address**: Aktif bir e-posta adresi.
     - **Password**: Güçlü bir şifre.
   - **Sign Up** butonuna tıklayarak hesabınızı oluşturun.

3. **E-posta Doğrulaması**
   - Docker Hub, kayıt sırasında belirtilen e-posta adresine bir doğrulama e-postası gönderecektir.
   - E-posta gelen kutunuza giderek doğrulama bağlantısına tıklayın.

4. **Hesabınızın Oluşturulması**
   - Doğrulama işleminden sonra hesabınız aktif hale gelecektir.

---

### 5.31.2 Azure DevOps Üzerinde Docker Hub Service Connection Oluşturma

1. **Azure DevOps Portalına Giriş Yapma**
   - [Azure DevOps](https://dev.azure.com/) portalına giriş yapın.

2. **Proje Ayarlarına Gitme**
   - Azure DevOps'ta entegrasyonu yapmak istediğiniz projeyi seçin.
   - Sol alt köşede bulunan **Project Settings** sekmesine tıklayın.

3. **Service Connections Ayarlarına Gitme**
   - **Pipelines** altında bulunan **Service Connections** sekmesine tıklayın.
   - Sağ üst köşedeki **New Service Connection** butonuna tıklayın.

4. **Docker Registry Seçimi**
   - Açılan pencerede **Docker Registry** seçeneğini seçin ve **Next** butonuna tıklayın.

5. **Docker Hub Bilgilerini Girme**
   - **Registry Type**: Docker Hub.
   - **Docker Hub Access**:
     - **Username**: Docker Hub kullanıcı adınızı girin.
     - **Password**: Docker Hub şifrenizi girin.
   - **Service Connection Name**: Örneğin, `docker-hub-connection` yazabilirsiniz.

6. **Service Connection'ı Test Etme**
   - **Verify and Save** butonuna tıklayarak bağlantıyı test edin.
   - Test başarılı olursa, service connection otomatik olarak oluşturulacaktır.

---

### 5.31.3 Lab-31'in Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak Docker Hub üzerinde bir kullanıcı oluşturdunuz ve Azure DevOps'ta Docker Hub için bir service connection tanımladınız. Bu yapılandırma, Docker image'lerini Azure DevOps pipeline'ları aracılığıyla Docker Hub'a push edebilmek için temel oluşturur.

## 5.32 Lab-32: Backend Pipeline'da Docker Image Oluşturma ve Docker Hub'a Gönderme, Sonrasında Docker Hub'dan Deploy Etme

Bu laboratuvar çalışmasında, backend pipeline'ını güncelleyerek **build** adımında Docker image oluşturacağız ve bu image'i **Docker Hub**'a göndereceğiz. **Deploy** adımında ise Docker Hub'dan son image'i çekerek bunu Docker üzerinde çalıştıracağız.

---

### 5.32.1 Adım 1: Pipeline'da Build Adımını Güncelleme

**Build** aşamasına şu işlemleri ekleyeceğiz:

1. **.NET SDK'nın Yüklenmesi**:
   - Build sırasında kullanılacak .NET SDK'yı yüklemek için bir adım ekleyeceğiz.

2. **Projenin Build Edilmesi**:
   - `dotnet build` komutuyla backend projesinin derlenmesini sağlayacağız.

3. **Docker Image'in Oluşturulması**:
   - Pipeline'da Docker image oluşturmak için `docker build` komutunu çalıştıracağız. Bu adım, projenin bir container olarak çalıştırılmasını mümkün kılacaktır.

4. **Docker Image'in Docker Hub'a Push Edilmesi**:
   - Oluşturulan image, Docker Hub'a gönderilerek merkezi bir depoda saklanacaktır.

---

### 5.32.2 Adım 2: Pipeline'da Deploy Adımını Güncelleme

**Deploy** aşamasına şu işlemleri ekleyeceğiz:

1. **Docker Hub'dan Image Çekme**:
   - Docker Hub'daki en son image pipeline sırasında çekilecektir. Bu işlem, son değişikliklerin kullanılmasını sağlar.

2. **Mevcut Container'ın Durdurulması ve Silinmesi**:
   - Daha önce çalışan container durdurulacak ve silinecektir.

3. **Yeni Container'ın Başlatılması**:
   - Docker Hub'dan çekilen image kullanılarak yeni bir container başlatılacaktır. Container, belirtilen portlar üzerinden çalışacaktır (ör. 10101 portu).

---

### 5.32.3 Adım 3: Pipeline Dosyasının Tamamı

Güncellenmiş pipeline dosyasının tamamı aşağıdaki gibidir:

```yaml
trigger:
- main

pool:
  vmImage: 'ubuntu-latest'

variables:
  buildConfiguration: 'Release'

stages:
  - stage: Build
    displayName: "Build and Push Docker Image"
    jobs:
      - job: BuildJob
        displayName: "Build and Push Docker Image"
        steps:
          - task: UseDotNet@2
            displayName: 'Install .NET SDK'
            inputs:
              packageType: 'sdk'
              version: '6.x'
              installationPath: $(Agent.ToolsDirectory)/dotnet

          - script: |
              dotnet restore
              dotnet build --configuration $(buildConfiguration)
            displayName: "Restore and Build"

          - task: Docker@2
            displayName: "Build Docker Image"
            inputs:
              command: "build"
              dockerfile: "Dockerfile"
              tags: "$(Build.BuildId)"
              containerRegistry: "docker-hub-connection"

          - task: Docker@2
            displayName: "Push Docker Image to Docker Hub"
            inputs:
              command: "push"
              containerRegistry: "docker-hub-connection"
              imageName: "productmanagement-backend"
              tags: "$(Build.BuildId)"

  - stage: Deploy
    displayName: "Deploy from Docker Hub"
    dependsOn: Build
    condition: succeeded()
    jobs:
      - job: DeployJob
        displayName: "Deploy Backend"
        steps:
          - task: Docker@2
            displayName: "Pull Latest Docker Image from Docker Hub"
            inputs:
              command: "pull"
              containerRegistry: "docker-hub-connection"
              imageName: "productmanagement-backend"
              tags: "$(Build.BuildId)"

          - script: |
              docker stop productmanagement-backend-container || true
              docker rm productmanagement-backend-container || true
              docker run -d -p 10101:80 --name productmanagement-backend-container productmanagement-backend:$(Build.BuildId)
            displayName: "Deploy Docker Image"
```

---

### 5.32.4 Adım 4: Pipeline Dosyasını Commit ve Push Etme

1. **Değişiklikleri Kaydetme**
   - Yaptığınız değişiklikleri kaydedin (`Ctrl+S`).

2. **Değişiklikleri Commit Etme**
   - Visual Studio'da **Git Changes** sekmesini açın.
   - **Commit Message** kısmına şu mesajı yazın:
     ```
     Pipeline güncellendi: Docker image oluşturma, push ve deploy işlemleri eklendi.
     ```
   - **Commit All** butonuna tıklayın.

3. **Değişiklikleri Push Etme**
   - Commit işleminden sonra **Push** butonuna tıklayarak değişikliklerinizi remote branch'e gönderin.

4. **Pull Request (PR) Oluşturma**
   - Azure DevOps portalına giderek backend projesi için **main** branch'e merge edilmek üzere bir PR oluşturun.
   - PR açıklamasına şu bilgileri ekleyin:
     ```
     - Build adımında Docker image oluşturuluyor ve Docker Hub'a gönderiliyor.
     - Deploy adımında Docker Hub'dan son image çekilerek çalıştırılıyor.
     ```

5. **PR Onayı ve Merge İşlemi**
   - PR'ınız için gerekli onayları aldıktan sonra **Complete Merge** butonuna tıklayarak değişiklikleri `main` branch'e merge edin.

---

### 5.32.5 Adım 5: Pipeline'ı Test Etme

1. **Pipeline'ı Çalıştırma**
   - Pipeline'ınızı manuel olarak çalıştırın veya bir PR oluşturup tetikleyin.

2. **Pipeline Çalışmasını İzleme**
   - Azure DevOps portalında pipeline'ın her iki aşamasını gözlemleyin:
     - **Build Stage**: Docker image'in oluşturulması ve Docker Hub'a gönderilmesi.
     - **Deploy Stage**: Docker Hub'dan image'in çekilmesi ve container olarak çalıştırılması.

3. **Container'ın Çalıştığını Doğrulama**
   - Terminalde şu komutu çalıştırarak çalışan container'ı listeleyin:
     ```bash
     docker ps
     ```
   - Çıktıda `productmanagement-backend-container` adında bir container görüyorsanız, deploy işlemi başarıyla tamamlanmıştır.

4. **API'yi Test Etme**
   - Tarayıcınızda veya Postman'de `http://localhost:10101/api/products` gibi bir endpoint'e giderek backend API'sinin çalıştığını doğrulayın.

---

### 5.32.6 Lab-32'nin Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak backend pipeline'ınızı güncellediniz. Artık Docker image'leri pipeline'da oluşturuluyor, Docker Hub'a gönderiliyor ve sonrasında Docker Hub'dan çekilerek deploy ediliyor. Bu süreç, modern CI/CD yöntemlerini benimseyerek daha hızlı ve güvenilir bir dağıtım sağlar.

## 5.33 Lab-33: Monitoring ve Logging: Prometheus ve Grafana ile Metrik Toplama

Bu laboratuvar çalışmasında, **Prometheus** ve **Grafana**'yı Docker container'larında kurarak temel bir izleme ve görselleştirme sistemi oluşturacağız. Daha sonra backend uygulamasında metrikler oluşturarak Prometheus'a veri göndereceğiz ve bu verileri Grafana'da bir dashboard üzerinden görselleştireceğiz.

---

### 5.33.1 Prometheus ve Grafana Kurulumu

#### 5.33.1.1 Docker Compose ile Prometheus ve Grafana Kurulumu

1. **Docker Compose Dosyasını Hazırlama**
   - Proje dizininize `docker-compose.yml` adlı bir dosya oluşturun ve aşağıdaki içeriği ekleyin:
     ```yaml
     version: '3.8'

     services:
       prometheus:
         image: prom/prometheus:latest
         container_name: prometheus
         ports:
           - "9090:9090"
         volumes:
           - ./prometheus.yml:/etc/prometheus/prometheus.yml
         command:
           - '--config.file=/etc/prometheus/prometheus.yml'

       grafana:
         image: grafana/grafana:latest
         container_name: grafana
         ports:
           - "3000:3000"
         environment:
           - GF_SECURITY_ADMIN_USER=admin
           - GF_SECURITY_ADMIN_PASSWORD=admin
     ```

2. **Prometheus Konfigürasyon Dosyasını Oluşturma**
   - `prometheus.yml` adlı bir dosya oluşturun ve aşağıdaki içeriği ekleyin:
     ```yaml
     global:
       scrape_interval: 15s

     scrape_configs:
       - job_name: 'backend'
         static_configs:
           - targets: ['host.docker.internal:5000'] # Backend uygulamanızın adresi
     ```

3. **Container'ları Başlatma**
   - Terminalde şu komutu çalıştırarak Prometheus ve Grafana container'larını başlatın:
     ```bash
     docker-compose up -d
     ```

4. **Kurulumu Doğrulama**
   - Prometheus arayüzüne erişmek için tarayıcınızda `http://localhost:9090` adresine gidin.
   - Grafana arayüzüne erişmek için tarayıcınızda `http://localhost:3000` adresine gidin (Kullanıcı adı ve şifre: `admin` / `admin`).

---

### 5.33.2 Backend Uygulamasında Prometheus Metriklerini Eklemek

#### 5.33.2.1 Prometheus Client Kütüphanesini Yükleme

1. **NuGet Paketini Yükleme**
   - Backend projesinde terminali açın ve şu komutu çalıştırın:
     ```bash
     dotnet add package prometheus-net.AspNetCore
     ```

2. **Startup Konfigürasyonunu Güncelleme**
   - **Program.cs** dosyanıza aşağıdaki kodu ekleyin:
     ```csharp
     using Prometheus;

     var builder = WebApplication.CreateBuilder(args);

     // Add services to the container.
     builder.Services.AddControllers();

     var app = builder.Build();

     // Use Prometheus metrics
     app.UseHttpMetrics();

     app.MapControllers();
     app.MapMetrics(); // Prometheus için endpoint

     app.Run();
     ```

3. **Metriklerin Çalıştığını Doğrulama**
   - Backend uygulamanızı başlatın.
   - Tarayıcınızda `http://localhost:5000/metrics` adresine giderek Prometheus için üretilen metrikleri görün.

---

### 5.33.3 Prometheus ve Grafana ile Backend Metriklerini Görselleştirme

#### 5.33.3.1 Prometheus Konfigürasyonunu Güncelleme
- Prometheus'un `prometheus.yml` dosyasındaki hedef adresini backend uygulamasına yönlendirin:
  ```yaml
  static_configs:
    - targets: ['host.docker.internal:5000'] # Backend uygulamanızın adresi
  ```

#### 5.33.3.2 Prometheus'u Yeniden Başlatma
- Konfigürasyon değişikliklerini uygulamak için Prometheus container'ını yeniden başlatın:
  ```bash
  docker-compose restart prometheus
  ```

#### 5.33.3.3 Grafana Dashboard Oluşturma

1. **Grafana'ya Prometheus Veri Kaynağı Eklemek**
   - `http://localhost:3000` adresine gidin ve Grafana'ya giriş yapın.
   - Sol menüden **Configuration > Data Sources** seçeneğini seçin.
   - **Add Data Source** butonuna tıklayın ve Prometheus'u seçin.
   - **URL** kısmına `http://prometheus:9090` yazın ve kaydedin.

2. **Yeni Dashboard Oluşturma**
   - Sol menüden **Create > Dashboard** seçeneğini seçin.
   - **Add a new panel** butonuna tıklayın.
   - Panelin sorgu kısmına şu Prometheus sorgularını yazabilirsiniz:
     - **Toplam HTTP İstek Sayısı**:
       ```promql
       http_requests_total
       ```
     - **İstek Yanıt Süreleri (Ortalama)**:
       ```promql
       http_request_duration_seconds_sum / http_request_duration_seconds_count
       ```
   - Paneli kaydedin ve dashboard'ınıza ekleyin.

3. **Dashboard'ı Kaydetme**
   - Dashboard'u kaydetmek için sağ üst köşedeki **Save Dashboard** butonuna tıklayın ve bir ad verin.

---

### 5.33.4 Lab-33'ün Tamamlanması

Bu laboratuvar çalışmasını tamamlayarak Docker üzerinden Prometheus ve Grafana kurdunuz, backend uygulamanızdan metrikleri toplayarak Prometheus'a gönderdiniz ve bu metrikleri Grafana'da görselleştirdiniz. Bu süreç, uygulamanızın performansını izlemenizi ve optimize etmenizi sağlayacak güçlü bir monitoring altyapısı oluşturur.
