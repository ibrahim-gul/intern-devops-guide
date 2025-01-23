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

