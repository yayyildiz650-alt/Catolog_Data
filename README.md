 


# 🚀 AI-Powered E-Commerce App (Yapay Zeka Destekli Görsel Arama)

Modern Android geliştirme standartları kullanılarak inşa edilmiş, **Google Gemini AI** entegrasyonuna sahip, yenilikçi ve çevrimdışı öncelikli (offline-first) bir e-ticaret uygulamasıdır. 

Geleneksel metin tabanlı ürün arama deneyimini bir üst seviyeye taşıyarak, kullanıcıların kameralarından çektikleri fotoğrafları yapay zeka ile analiz eder ve veritabanındaki binlerce ürün arasından en uygun olanları milisaniyeler içinde eşleştirir.

 

 <p align="center">
  <img src="https://github.com/user-attachments/assets/edcce00c-a003-409f-8edc-1172c97f15c8" width="250" />
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/53653926-1acb-42f7-a7d9-d069df981c34" width="250" />
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://github.com/user-attachments/assets/ca25e0cc-6ebb-42ec-a864-cb4ac6144844" width="250" />
   &nbsp;&nbsp;&nbsp;&nbsp;
   <img src=" https://github.com/user-attachments/assets/460c7c3d-3d4f-4d08-b0f7-640446f407cd" width="250" />
 
</p>

## ✨ Temel Özellikler (Key Features):

* 🧠 **Akıllı Görsel Arama (Visual Search):** Google Gemini 3
.5 Flash modeli entegrasyonu sayesinde kameradan gelen görüntüleri analiz eder; ürünün kategorisini, rengini, materyalini ve anahtar kelimelerini %100 yapılandırılmış JSON formatında çıkarır.
* ⚡ **Offline-First Mimari:** Backend'e bağımlı kalmadan, 40.000'e yakın ürün verisini **Room Database** üzerinde lokal olarak tutar. Yapay zekadan gelen parametreleri "Varsa Eşleştir, Yoksa Pas Geç" mantığıyla çalışan esnek DAO sorgularıyla filtreler. Sıfır sunucu gecikmesi (Zero Latency) ile sonuç verir.
* 🎨 **Modern ve Dinamik UI:** Tamamen **Jetpack Compose** ile geliştirilmiş deklaratif arayüz. Material Design 3 standartlarına uygun, pürüzsüz animasyonlara ve asenkron görsel yükleme (Coil) desteğine sahip modern tasarım.
* 🏗️ **Güçlü State Yönetimi:** Ekran yan çevirmelerinde (Configuration Change) veri kaybını önleyen ve UI bileşenlerini sadece gerektiğinde yeniden çizen (Recomposition Optimization) gelişmiş durum yönetimi.

## 🛠️ Mimari ve Kullanılan Teknolojiler (Tech Stack)

Proje, Sürdürülebilirlik (Maintainability) ve Temiz Kod (Clean Code) prensipleri gözetilerek **MVVM (Model-View-ViewModel)** mimarisi üzerine inşa edilmiştir.

* **UI Katmanı:** Jetpack Compose, Material 3, Coil (Görsel Yükleme)
* **Mimari & Asenkron İşlemler:** MVVM, Kotlin Coroutines, StateFlow / Flow
* **Veritabanı Katmanı:** Room Database (Lokal Önbellekleme ve Karmaşık SQL Filtreleme)
* **Yapay Zeka & Ağ:** Google AI Client SDK (GenerativeLanguage API), Retrofit, Gson
* **Güvenlik:** API anahtarları `local.properties` ve `BuildConfig` kullanılarak güvenli bir şekilde gizlenmiştir.

## ⚙️ Uygulama Nasıl Çalışır?

1. Kullanıcı aradığı ürünün fotoğrafını çeker.
2. Görsel arka planda (`Dispatchers.IO`) Gemini yapay zekasına gönderilir.
3. AI, ürünü analiz edip DTO (Data Transfer Object) yapısına tam uyumlu bir JSON döndürür.
4. ViewModel bu JSON'u ayrıştırır ve Room veritabanına esnek bir SQL sorgusu olarak gönderir.
5. Veritabanındaki eşleşen ürünler anında Jetpack Compose listelerine (LazyColumn/LazyRow) yansıtılır.

## 🚀 Kurulum ve Çalıştırma:

Projeyi kendi bilgisayarınızda derlemek ve yapay zeka özelliklerini test etmek için aşağıdaki adımları izleyin:

1- Projeyi klonlayın

2-Android Studio'da projenin ana dizininde bulunan local.properties dosyasını açın (yoksa oluşturun) ve içine anahtarınızı ekleyin:

Properties
GEMINI_API_KEY=AQ_BURAYA_KENDI_ANAHTARINIZI_YAZIN

3-Projeyi senkronize edin (Sync Project with Gradle Files) ve çalıştırın.

Geliştirici: Muhammed Yakup Ayyıldız
    
