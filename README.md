#  Yeşil Alan Yoğunluğu, Yağış ve Baraj Doluluk Oranları Arasındaki İlişkinin Analizi

##  Proje Açıklaması

Bu proje, Türkiye'deki farklı şehirlerdeki **yeşil alan yoğunluğu**, **toplam yıllık yağış miktarı** ve **baraj doluluk oranları** arasındaki ilişkileri analiz etmeyi amaçlamaktadır. Amacımız, yeşil alanların iklimsel değişkenlerle nasıl bir ilişki içinde olduğunu ve bu değişkenlerin baraj doluluk seviyeleri üzerinde anlamlı bir etkisi olup olmadığını incelemektir.

Veriler farklı kurumlardan ve servislerden toplanmıştır:
- Yeşil alan oranı verileri (Google Maps API)
- Meteorolojik veriler (sıcaklık ve yağış)
- Baraj doluluk oranları (resmî su kaynakları)

##  Kullanılan Yöntemler

- **Veri Temizleme ve Ön İşleme**:  
  Eksik veya eksik erişilen şehirler elenmiş; kalan verilerde eksik değerler medyan ile doldurulmuştur. Barajsız şehirler analiz dışı bırakılmıştır.

- **Keşifsel Veri Analizi (EDA)**:  
  Değişkenler arası korelasyonlar, temel dağılımlar ve şehirler bazında karşılaştırmalar yapılmıştır.

- **Makine Öğrenmesi Modelleri**:
  - `Linear Regression`: Temel doğrusal ilişki analizi
  - `MLPRegressor`: Çok katmanlı yapay sinir ağı ile doğrusal olmayan ilişkilerin değerlendirilmesi

- **Model Değerlendirme Metrikleri**:
  - R² (Determination Coefficient)
  - MAPE (Mean Absolute Percentage Error)
  - RMSE (Root Mean Squared Error)

##  Özet Sonuçlar

Yapılan analizler ve modeller sonucunda:

> 🔹 **Yeşil alan yoğunluğunun** tek başına kullanılarak **baraj doluluk oranı** veya **yağış miktarı** tahmininin mümkün olmadığı görülmüştür.  
> 🔹 Tüm modellerde **negatif R²** ve **yüksek hata değerleri (MAPE/RMSE)** elde edilmiştir.  
> 🔹 Özellikle toplam yağış tahminlerinde modelin performansı anlamlı düzeyin çok altında kalmıştır.  
> 🔹 Sonuçlar, baraj doluluk ve yağış gibi kompleks değişkenlerin sadece yeşil alan yoğunluğuna bağlı olarak modellenemeyeceğini, çok daha fazla çevresel ve iklimsel değişkene ihtiyaç olduğunu göstermektedir.

---

 Proje detayları ve kodlar için `VeriBilimiProjeFinal.ipynb` dosyasını inceleyebilirsiniz.
