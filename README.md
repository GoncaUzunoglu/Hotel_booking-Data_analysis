# Hotel Booking Veriseti Analizi

Bu proje, otel rezervasyon verilerini analiz etmeyi amaçlamaktadır. Veriseti, otel rezervasyonlarına ilişkin çeşitli bilgileri içermektedir.

## Veriseti Bilgileri

Veriseti aşağıdaki sütunları içermektedir:

- `hotel`: Otel türü (City Hotel veya Resort Hotel).
- `is_canceled`: Rezervasyonun iptal edilip edilmediği (1: Evet, 0: Hayır).
- `lead_time`: Rezervasyon ile giriş tarihi arasındaki gün sayısı.
- `arrival_date_year`: Giriş yılı.
- `arrival_date_month`: Giriş ayı.
- `arrival_date_week_number`: Giriş haftası numarası.
- `arrival_date_day_of_month`: Giriş gün sayısı.
- `stays_in_weekend_nights`: Hafta sonu konaklama gecesi sayısı.
- `stays_in_week_nights`: Hafta içi konaklama gecesi sayısı.
- `adults`: Yetişkin sayısı.
- `children`: Çocuk sayısı.
- `babies`: Bebek sayısı.
- `meal`: Rezervasyon yapılan yemek türü.
- `country`: Rezervasyonu yapan kişinin ülkesi.
- `market_segment`: Pazar segmenti.
- `distribution_channel`: Dağıtım kanalı.
- `is_repeated_guest`: Tekrarlayan müşteri olup olmadığı (1: Evet, 0: Hayır).
- `previous_cancellations`: Önceki iptallerin sayısı.
- `previous_bookings_not_canceled`: İptal edilmeyen önceki rezervasyonların sayısı.
- `reserved_room_type`: Rezervasyon yapılan oda türü.
- `assigned_room_type`: Atanan oda türü.
- `booking_changes`: Rezervasyon değişiklik sayısı.
- `deposit_type`: Depozito türü.
- `agent`: Ajan kimliği.
- `company`: Şirket kimliği.
- `days_in_waiting_list`: Bekleme listesindeki gün sayısı.
- `customer_type`: Müşteri türü.
- `adr`: Ortalama günlük fiyat.
- `required_car_parking_spaces`: Gereken otopark alanı sayısı.
- `total_of_special_requests`: Özel isteklerin toplam sayısı.
- `reservation_status`: Rezervasyon durumu.
- `reservation_status_date`: Rezervasyon durumu tarihi.

## Proje Adımları

1. **Veri Keşfi ve Temizleme**
    - Verinin yüklenmesi ve ilk incelemesi
    - Eksik ve hatalı verilerin düzeltilmesi
2. **Veri Analizi**
    - Otel türüne göre iptal oranları
    - Giriş tarihine göre rezervasyon dağılımları
    - Ortalama günlük fiyatın analizi (ADR)
    - Pazar segmentlerine göre rezervasyon dağılımları
3. **Sonuçların Görselleştirilmesi**
    - Matplotlib ve Seaborn kullanarak grafikler oluşturma

## Kullanılan Araçlar ve Teknolojiler

- **Python**: Veri analizi ve görselleştirme
- **Pandas**: Veri işleme ve analizi
- **Matplotlib**: Veri görselleştirme
- **Seaborn**: İleri düzey veri görselleştirme

## Kod Örnekleri

### Veriyi Yükleme ve İlk İnceleme

```python
import pandas as pd

# Veriyi yükleme
df = pd.read_csv('hotel_bookings.csv')

# İlk 5 satırı görüntüleme
print(df.head())
