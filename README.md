# Global Earthquake Data Analysis

## Proje Amacı
Bu projede, 2025 yılında dünya genelinde meydana gelen
4.5 ve üzeri büyüklükteki depremler analiz edilmiştir.

Veriler USGS Earthquake API üzerinden Python kullanılarak
toplanmış, temizlenmiş ve görselleştirilmiştir.

## Veri Kaynağı
- API: USGS Earthquake API
- Kaynak: https://earthquake.usgs.gov/
- Dönem: 01.01.2025 - 31.12.2025
- Deprem sayısı: 8.559
- Minimum büyüklük: 4.5
- Kullanılan alanlar: ID, büyüklük, konum, zaman,
  enlem, boylam ve derinlik 
- Veri toplama tarihi: 20 Kasım 2026


## Araştırma Soruları
1. Depremler aylara göre nasıl dağılıyor?
2. Büyüklük ile derinlik arasında ilişki var mı?
3. Depremler hangi coğrafi bölgelerde yoğunlaşıyor?

## Yöntem
1. USGS API'den aylık sorgularla veriler toplandı.
2. Ham veriler JSON formatında kaydedildi.
3. JSON verileri pandas DataFrame'e dönüştürüldü.
4. Eksik değerler ve tekrar eden kayıtlar kontrol edildi.
5. Tarih alanı düzenlendi.
6. Koordinat ve büyüklük değerleri kontrol edildi.
7. Temiz veri CSV formatında kaydedildi.
8. Matplotlib kullanılarak grafikler oluşturuldu.

## Bulgular

### Aylık Deprem Dağılımı

![2025 Yılı Aylık Deprem Dağılımı](figures/monthly_earthquakes_2025.png)

En fazla deprem temmuz ayında (1.321),
en az deprem mart ayında (539) gerçekleşmiştir.
Aylık ortalama deprem sayısı 713,25'tir.

### Derinlik ve Büyüklük İlişkisi

![Deprem Derinliği ve Büyüklüğü İlişkisi](figures/depth_magnitude_scatter.png)

Pearson korelasyon katsayısı -0.046 bulunmuştur.
İki değişken arasında belirgin doğrusal ilişki
gözlemlenmemiştir.

### Coğrafi Dağılım

![Depremlerin Coğrafi Dağılımı](figures/earthquake_locations_2025.png)

Depremler dünya üzerinde homojen dağılmamaktadır.
Japonya, Endonezya, Alaska ve Güney Amerika'nın
batı kıyılarında yoğunlaşmalar görülmektedir.

## Sınırlılıklar
- Yalnızca 2025 yılı incelenmiştir.
- Sadece 4.5 ve üzeri büyüklükteki depremler alınmıştır.
- Sonuçlar farklı yıllar için genellenemez.
- USGS kayıtları sonradan güncellenebilir.
- Coğrafi yoğunluklar görsel olarak değerlendirilmiştir.

## Kullanılan Teknolojiler
- Python
- Google Colab
- requests
- pandas
- Matplotlib
- USGS Earthquake API

## Çalıştırma
1. requirements.txt dosyasındaki paketleri yükleyin.
2. notebooks klasöründeki notebook'u açın.
3. Kod hücrelerini sırasıyla çalıştırın.
4. Ham ve işlenmiş veriler data klasöründe oluşturulur.
5. Grafikler figures klasörüne kaydedilir.
