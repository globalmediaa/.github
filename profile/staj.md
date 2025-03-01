# Yazılım Stajyeri Değerlendirme Problemi

## Problem: Kütüphane Yönetim Sistemi

Bir kütüphane için basit bir yönetim sistemi geliştirmeniz isteniyor. Bu sistem, kitapların kaydını tutacak, ödünç alma/iade işlemlerini yönetecek ve basit istatistikler sunacaktır.

## Gereksinimler

### Veri Modelleri
- **Kitap**: ISBN, başlık, yazar, yayın yılı, kategori, kopya sayısı
- **Üye**: ID, ad, soyad, e-posta, üyelik başlangıç tarihi
- **Ödünç İşlemi**: Kitap, üye, ödünç alma tarihi, iade tarihi

### Temel İşlevler
1. **Kitap Yönetimi**:
   - Kitap ekleme, güncelleme, silme
   - ISBN ile kitap arama
   - Başlık veya yazar adına göre kitap arama
   - Tüm kitapları listeleme

2. **Üye Yönetimi**:
   - Üye ekleme, güncelleme, silme
   - ID veya isim ile üye arama
   - Tüm üyeleri listeleme

3. **Ödünç İşlemleri**:
   - Kitap ödünç verme
   - Kitap iade alma
   - Gecikmiş kitapları listeleme (iade tarihi geçmiş)
   - Bir üyenin ödünç aldığı kitapları görüntüleme

4. **İstatistikler**:
   - En popüler kitaplar (en çok ödünç alınan)
   - En aktif üyeler (en çok kitap ödünç alan)
   - Kategori bazında kitap sayıları

### Teknik Gereksinimler
- Kod, nesne yönelimli programlama prensiplerini uygulamalıdır.
- Veriler dosyada veya basit bir veritabanında saklanmalıdır.
- Hata yönetimi uygun şekilde ele alınmalıdır.
- Arayüz konsol tabanlı olabilir, ancak tercihen basit bir GUI olmalıdır.
- Birim testleri yazılmalıdır.

## Değerlendirme Kriterleri
1. **Kod Kalitesi** (30%)
   - Temiz ve okunabilir kod
   - Uygun isimlendirme ve yorumlar
   - OOP prensiplerinin doğru kullanımı

2. **İşlevsellik** (30%)
   - Tüm temel gereksinimlerin karşılanması
   - Doğru çalışma ve hata yönetimi

3. **Tasarım** (20%)
   - Mimari tasarım ve modülerlik
   - Veri yapıları ve algoritmaların verimli kullanımı

4. **Test ve Dokümantasyon** (10%)
   - Birim testleri
   - README ve kullanım dokümantasyonu

5. **Ek Özellikler** (10%)
   - İsteğe bağlı ek özellikler veya iyileştirmeler

## Teslim Yönergeleri

### GitHub Kullanımı
1. GitHub üzerinde yeni bir repo oluşturun.
2. Repo adını `library-management-system` olarak belirleyin.
3. Repository'yi **public** olarak ayarlayın.
4. Bir README.md dosyası ekleyin ve aşağıdaki bilgileri içerdiğinden emin olun:
   - Projenin amacı ve özellikleri
   - Kurulum ve çalıştırma talimatları
   - Kullanılan teknolojiler
   - Projenin yapısı (dizin ve dosya yapısı)
   - Ekran görüntüleri (varsa)

### Git ve Conventional Commit Kullanımı
1. Commitler için **Conventional Commit** standartlarını uygulayın:
   - Format: `<type>[optional scope]: <description>`
   - Örneğin:
     - `feat: add book search functionality`
     - `fix: correct date calculation in borrowing process`
     - `docs: update installation instructions`
     - `test: add unit tests for member service`
     - `refactor: improve error handling in book controller`
2. Her önemli işlev için ayrı bir branch oluşturun ve geliştirmenizi tamamladıktan sonra main/master branch'e merge edin.
3. Commit mesajlarınız açık, anlamlı ve Conventional Commit formatına uygun olmalıdır.

### Kod Organizasyonu
1. Bir framework kullanıyorsanız (örn. Ruby on Rails, Django, Laravel, React), o framework'ün topluluk tarafından kabul görmüş stil ve düzenlemelerine uyun.
2. Framework kullanmıyorsanız, aşağıdaki yapıya benzer bir proje dizin yapısı kullanın:
```
library-management-system/
├── src/                   # Kaynak kodları
│   ├── models/            # Veri modelleri
│   ├── controllers/       # İş mantığı
│   ├── views/             # Kullanıcı arayüzü (varsa)
│   └── utils/             # Yardımcı fonksiyonlar
├── tests/                 # Test dosyaları
├── data/                  # Veri dosyaları
├── docs/                  # Dokümantasyon
├── README.md              # Proje açıklaması
└── requirements.txt       # Bağımlılıklar (Python için)
```

### Teslim Süreci
1. Projeyi tamamladıktan sonra, GitHub repo URL'sini paylaşın.
2. Son teslim günü: 1w
3. Teslim e-postası konu satırı: "Stajyer Değerlendirme - [Adınız Soyadınız]"

## Bonus Puanlar İçin
- Kapsamlı test yazımı:
  - Birim testler
  - Entegrasyon testleri
  - End-to-end testler
  - Test coverage raporu
- Veritabanı entegrasyonu (PostgreSQL, MySQL vb.)
- Basit bir web arayüzü
- Docker containerization
- CI/CD pipeline kurulumu
- API dokümantasyonu

## İpuçları
- Önce temel işlevleri tamamlayın, sonra ekstra özelliklere geçin.
- Temiz kod yazmaya özen gösterin.
- Conventional commit standartlarına uyun.
- Uygun hata yönetimi ve input doğrulaması ekleyin.
- Düzenli commit yapın.
- Testlere önem verin ve mümkünse TDD (Test Driven Development) yaklaşımını deneyin.
