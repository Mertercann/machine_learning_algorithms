# Customer Churn Prediction

## Projenin Amacı

Bu projenin amacı, müşteri verilerini kullanarak müşterilerin aboneliklerini sonlandırıp sonlandırmayacağını tahmin eden bir makine öğrenmesi modeli geliştirmektir.

Proje kapsamında veri ön işleme, kategorik değişkenlerin dönüştürülmesi, veri ölçeklendirme, farklı sınıflandırma modellerinin eğitilmesi ve model performanslarının karşılaştırılması gerçekleştirilmiştir.

## Veri Seti

Projede müşteri davranışlarını içeren bir **Customer Churn** veri seti kullanılmıştır.

Veri seti **64.374 satır ve 12 sütundan** oluşmaktadır. Hedef değişken `Churn` sütunudur.

Veri setinde müşterilerin yaşı, kullanım sıklığı, destek çağrıları, ödeme gecikmeleri, abonelik türü, sözleşme süresi ve toplam harcama gibi bilgiler bulunmaktadır.

Veri ön işleme aşamasında kategorik değişkenler sayısal forma dönüştürülmüş, sayısal değişkenler ise gerekli modeller için ölçeklendirilmiştir.

## Nasıl Çalıştırılır?

Öncelikle gerekli Python kütüphaneleri yüklenmelidir:

```bash
pip install -r requirements.txt
```

Daha sonra:

1. `Final_odevi.ipynb` dosyasını Jupyter Notebook veya VS Code ile açın.
2. Gerekli veri dosyasının repository içerisinde bulunduğundan emin olun.
3. Notebook içerisindeki hücreleri sırasıyla çalıştırın.

## Kullanılan Modeller

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree

Modellerin performanslarını geliştirmek için `GridSearchCV` kullanılarak hiperparametre optimizasyonu yapılmıştır.

## Sonuç

Model değerlendirmeleri sonucunda **KNN modeli** başarılı bir performans göstermiştir.

En iyi KNN parametreleri:

```text
n_neighbors = 15
weights = distance
metric = manhattan
```

Optimize edilmiş KNN modeli validation verisinde yaklaşık **0.93 F1-score** elde etmiştir.

Bu sonuç, KNN modelinin müşteri churn tahmininde başarılı bir sınıflandırma performansı gösterdiğini ortaya koymaktadır.
