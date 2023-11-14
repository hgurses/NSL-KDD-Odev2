Siber Güvenlik için Veri Madenciliği Dersi Proje Ödevi

NSL-KDD Genel Bakış

NSL-KDD, veri setinin sınırlamalarını ele almak için CIC (Kanada Siber Güvenlik Enstitüsü)
tarafından yayımlanan KDD Cup'99 veri setinin geliştirilmiş bir versiyonudur.
Aynı zamanda web siteleri aracılığıyla araştırmacıların kullanımına açıktır.
NSL-KDD veri seti, KDD Cup'99 veri setinin sorunlarını ortadan kaldırmayı ve izinsiz giriş
tespit araştırması için daha gerçekçi ve zorlu bir veri seti sağlamayı amaçlamaktadır.
Bu veri seti saldırı tespit sistemi araştırması alanında yaygın olarak kullanılmaktadır ve tespit
oranları açısından KDD-99 veri setinden daha iyi performans göstermektedir. Veri kümesi
aynı zamanda anormal veri tanıma gibi başka amaçlar için de kullanılabilir. NSL-KDD veri
kümesi, farklı makine öğrenimi algoritmaları ve teknikleri ile kullanılabilmektedir.
Ne için Kullanılır?
NSL-KDD veri seti siber güvenlik alanında kullanılan bir veri setidir. Bunun içerisinde
izinsiz giriş/sızma tespit (IDS) sistemleri değerlendirmede ve test amaçlarında kullanılır.
Tespit sistemlerini değerlendirmede makine öğrenmesi modellerden de yararlanılabilir.
Veri seti barındırdıklarıyla kullanıcıya standartlaşmış bir veri seti sunduğundan onları
kullanarak kendi tespit algoritmaların geliştirebilirler.
Burada birkaç kullanım alanını görebiliriz;
1. IDS Deneme/Test:
İzinsiz giriş tespit sistemlerini ve algoritmalarını test etmek için uygun ve standartlaşmış bir
veri kümesi sağlar.
2. Algoritmalar:
İzinsiz giriş sistemlerinde geliştirilmiş ve geliştirilen algoritmalarının testine imkân sağlar.
Eksikleri ve diğer algoritmalar ile kıyaslandığında avantaj ve dezavantajları bu şekilde ortaya
çıkarır.
3. Eğitim ve Test:
Bu veri seti isimlendirilmiş birçok senaryo örneklerini içerisinde barındırır. BU kolaylıkla
beraber makine öğrenme modelleriyle izinsiz giriş tespitleri için yazılımı train ve test etmek
mümkün hale gelir. Bu örneklerde normal ağ trafiği dahil birçok saldırı senaryoları da
barındırır.
4. Model Validation:
Geliştirilen veya mevcut bir izinsiz giriş sisteminin ne kadar verimli ve hassas çalıştığına
saptanabilir. Bu sayede kullanılan veri kümesi içerisindeki hangi verinin atlandığı, hangi
verinin kullanıldığı görülebilmekte ve gerçek ortamlar için veri elde edilebilmekte
5. IDS Yaklaşımlarının Karşılaştırılması:
NSL-KDD yaygın olarak kullanılan bir standart haline geldiğinden birçok izinsiz giriş
yöntemleri test edilebilir ve karşılaştırılabilmekte. Aynı zamanda tekniklerin güçlü ve zayıf
yanları ortaya çıkartılabilmekte. Geliştirilen tekniğin limitleri belirlenebilir ve geliştirmeler
yapılabilir. NSL-KDD eğitim ve geliştirme alanında geniş çaplı kullanımda bulunmakta. Bu
yüzden veri setinin barındırdığı gerçek dünya senaryosunda yetersiz kalabilir.
Genel olarak NSL-KDD yaygın kullanılan izinsiz girişi tespit sistemlerinin çeşitli
denemelerinin ve kıyaslamalarının yapılabildiği bir ortam sağlamakta.
Ama unutulmaması gerekir ki gerçek dünya ortamında veri seti içerisindeki veriler yetersiz
kalabilir.


Neden NSL-KDD?
NSL-KDD deneme ve test setlerindeki kayıtların sayısı düşük düzeydedir.
Bu ise yüksek bir verimlilik sağlamaktadır. Bu avantaj, testte küçük bir kısmın rastgele
seçilmesine gerek kalmadan deneylerin setin tamamı üzerinde gerçekleştirilmesini uygun
maliyetli (verimli) hale getirir. KDD ile kıyaslanırsa NSL-KDD birçok avantajları vardır.
Örneğin, test setlerinde tekrarlayan kayıt bulunmamaktadır.
Diğer avantajlar;
1. Gerçekçi Ağ Trafiği:
NSL-KDD gerçek bilgisayar ağı üzerinden geliştirildiğinden gerçekçi bir simülasyon
sağlamakta. Bu da yeni, daha verimli, efektif ve güvenilir izinsiz giriş tespit modellerinin
geliştirilmesini sağlar.
2. Saldırı Çeşitliliği:
Bu veri seti birçok saldırı çeşidini barındırmakta. Bu şekilde algoritmalar birçok alanda test
edilebilir ve avantajlarına saptanabilir. Eksik kalınan yanlar da saptanır ve böylelikle daha
emin adımlara geliştirme süreci işlenebilir. Bu çeşitlilik sayesinde sistemler çeşitli saldırıları
seçebilir ve sınıflandırabilir.
3. Benchmarking:
NSL-KDD yaygın olarak kullanıldığından araştırmacılar ve geliştiriciler için izinsiz giriş
tespit sistemlerinin karşılaştırılması ve farklı algoritmaların denenmesini sağlar.
4. Feature Azaltma:
Veri seti içerisinde feature seçimi ile istenilen özellikte ve sorgulamada işlem yapılabilmekte
ve eğitim süreci bu şekilde sınırlandırılabilmekte. Bu şekilde sistemin veri arttırılabilmekte.



Çalışmamızda Kullandığımız Yöntemler
Üzerinde çalıştığımız Lable bu şekilde listelenebilir.
"duration","protocol_type","service","flag","src_bytes",
"dst_bytes","land","wrong_fragment","urgent","hot","num_failed_logins",
"logged_in","num_compromised","root_shell","su_attempted","num_root",
"num_file_creations","num_shells","num_access_files","num_outbound_cmds",
"is_host_login","is_guest_login","count","srv_count","serror_rate",
"srv_serror_rate","rerror_rate","srv_rerror_rate","same_srv_rate",
"diff_srv_rate","srv_diff_host_rate","dst_host_count","dst_host_srv_count",
"dst_host_same_srv_rate","dst_host_diff_srv_rate","dst_host_same_src_port_rate",
"dst_host_srv_diff_host_rate","dst_host_serror_rate","dst_host_srv_serror_rate",
"dst_host_rerror_rate","dst_host_srv_rerror_rate","label"

Alan olarak ise flag, protocol_type, service alanlarını (label) seçip onların üzerinde çalıştık,
Tüm verideki alanların hepsini gösterdik ve başlıklarına göre sayılarını listeledik.



1.Flag, Protocol_type, ve Service Alanları Üzerinde Çalışma
NSL-KDD veri kümesinde, analizimizi odakladığımız temel alanlar flag, protocol_type ve
service'dir. Bu alanlar, ağ trafiğinin çeşitli özelliklerini temsil eder. Bu alanlar üzerinde
detaylı bir inceleme yaparak, bu veri kümesinin güvenlik analitiği ve sınıflandırma
problemleri için kullanılabilirliğini anlamaya çalıştık.

2. Kategorilerin İncelenmesi ve Grafiksel Temsili:
Seçtiğimiz flag, protocol_type ve service alanlarının kategorilerini inceledik. Her bir kategori
içindeki örnek sayılarını belirleyerek, bu kategorilerin dağılımlarını görselleştirdik. Bu analiz,
belirli ağ trafiği özelliklerinin veri kümesindeki dağılımını anlamamıza ve potansiyel anormal
durumları tespit etmemize yardımcı oldu.

4. Tüm Veri Setinin Genel İncelenmesi ve Sayısal Analiz:
Ayrıca, NSL-KDD veri kümesinde bulunan tüm alanları gözden geçirip, başlıklarına göre
sayılarını detaylı bir şekilde listeledik. Bu sayede, veri kümesinin genel yapısı hakkında
kapsamlı bir anlayış elde ettik. Her bir özellik sütununun veri kümesindeki örnek sayılarına
odaklanarak, hangi alanların daha yoğun veya seyrek olduğunu belirledik.

Bu analizler, NSL-KDD veri kümesini daha yakından tanımamıza ve üzerinde çalıştığımız
özelliklerin veri setindeki önemini anlamamıza yardımcı oldu. Her bir kategori ve özellik
sütunu üzerinde yapılan incelemeler, daha sonra uygulanacak olan makine öğrenimi
modellerinin başarılı ve verimli bir şekilde eğitebilmemize katkı sağlayacaktır.

Google Colab 

https://colab.research.google.com/drive/1bLIdY5PKhqiNBSr8q0bTAev6DeY-ZTHC?usp=sharing

Dada fazla detay için proje raporunu incelebilirsiniz.

Harran Üniversitesi

Bilgisayar Mühendisliği

Kerem SÖYLEMEZ (200504060)

Hasan GÜRSES (180504082)
