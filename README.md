# deprem-ml
 Türkiye Deprem Verileri ile Makine Öğrenmesi Projesi

Merhaba! Ben bu projede, Türkiye'de 1999 yılından bu yana meydana gelen depremleri inceleyerek, büyüklüğü 5.5 ve üzeri olan, yani yıkıcı sayılabilecek depremleri tahmin edebilecek bir makine öğrenmesi modeli geliştirmeyi hedefledim. Amacım, geçmiş verilere dayanarak olası yıkıcı depremleri önceden tahmin edebilmek ve böylece afet yönetimi ve hazırlık süreçlerine katkı sağlayabilecek bir sistemin temelini atmaktı.

Proje kapsamında ilk olarak veriyi detaylıca analiz ettim (EDA). Aykırı değerleri inceledim, eksik verileri temizledim ve veriyi modellemeye uygun hale getirdim. Ardından çeşitli sınıflandırma algoritmalarını (Logistic Regression, KNN, SVC, Decision Tree, Random Forest) uygulayarak karşılaştırmalı analizler yaptım. Modelleri eğitmeden önce veri dengesizliği gibi sorunları SMOTE ile çözmeye çalıştım. Performans değerlendirmesinde çapraz doğrulama (cross validation) ve metrikler (accuracy, precision, recall, f1-score) kullandım.

Sonuç olarak, en yüksek başarıyı gösteren modeli seçip, hiperparametre optimizasyonu ile daha iyi hale getirdim. Bu projenin hem makine öğrenmesi tekniklerini pratikte kullanmak hem de gerçek hayattaki anlamlı bir problemi çözmeye çalışmak adına benim için çok öğretici ve anlamlı olduğunu söyleyebilirim.

# Kullandığım Veri Seti
(https://www.kaggle.com/datasets/yarenzoul/turkiye-deprem-verileri/data)
Veri setini Kaggle üzerinden aldım. İçinde 490.000'den fazla satır vardı. Her satırda depremle ilgili şu bilgiler yer alıyor:

- Tarih
- Saat
- Enlem
- Boylam
- Derinlik
- Büyüklük

Ben bu veriler üzerinde ön işleme yaptıktan sonra, “Yıkıcı mı?” şeklinde 0 ve 1’lerden oluşan yeni bir hedef değişken oluşturdum.

# Uyguladığım Adımlar
Keşifsel Veri Analizi (EDA)

Veri Ön İşleme

Veri Dengeleme

Gözetimli Öğrenme(Random Forest)

Model Değerlendirme

Sonuç

# Uyguladığım Makine Öğrenmesi Modelleri

Bu projede farklı gözetimli öğrenme algoritmalarını denedim:

- Lojistik Regresyon
- KNN
- SVC
- Decision Tree
- Random Forest
- *Random Forest (En iyi sonuçları verdi)*

### En başarılı model: Random Forest Classifier

## Değerlendirme Metrikleri

Modeli değerlendirirken şunlara baktım:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix (karışıklık matrisi)

Sonuçları yorumladım ve hangi modelin daha iyi performans verdiğini grafiklerle karşılaştırdım.

---

## Teknik Açıklamalar

Tüm teknik açıklamaları notebook içinde markdown hücrelerinde yazdım. Kodların ne işe yaradığını ve neden yaptığımı elimden geldiğince anlatmaya çalıştım.


## Projenin Geleceği

Bu projeyi daha da geliştirmek isterim. Aklımda şu fikirler var:

- Veriye bina yapısı, zemin bilgisi gibi ekstra değişkenler eklemek
- Streamlit ile basit bir kullanıcı arayüzü yaparak modeli web'e taşımak
- Gerçek zamanlı veri çekerek dinamik tahmin yapmak
- Unsupervised algoritmalarla farklı analizler denemek olabilir

## Bu Projeyi Neden Yaptım?

Bu projeyle hem Python becerilerimi hem de makine öğrenmesi konusundaki bilgimi uygulamalı olarak geliştirmiş oldum. Depremlerin Türkiye için ne kadar önemli olduğunu düşündüğümüzde, bu verilerle çalışmak hem teknik hem de duygusal olarak motive ediciydi.


## Yardım Aldığım Diğer Çalışmalar

- [Everything on GPU ML with cuML / Polars / CuPy](https://www.kaggle.com/code/goker67/everything-on-gpu-ml-with-cuml-polars-cupy)  
- [Decision Trees & Feature Selection](https://www.kaggle.com/code/goker67/decision-trees-acc-metrics-feature-selection)

# Kaggle Notebook
Projeye ait tüm kodlar ve açıklamalar için Kaggle notebook dosyasına buradan ulaşabilirsiniz:  
[Kaggle Notebook Linki](https://www.kaggle.com/code/haticesarmustafaolu/t-rk-ye-deprem-ver-ler-le-mak-ne-renmes)
