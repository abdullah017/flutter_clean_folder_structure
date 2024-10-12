# flutter_clean_folder_structure
    
    
    lib/
    ├── core/
    │   ├── error/
    │   ├── network/
    │   ├── utils/
    │   └── constants.dart
    ├── data/
    │   ├── models/
    │   ├── repositories/
    │   ├── datasources/
    │   └── graphql/ #if you are using graphql you can use this folder
    ├── domain/
    │   ├── entities/
    │   ├── repositories/
    │   └── usecases/
    ├── presentation/
    │   ├── controllers/
    │   ├── pages/
    │   ├── widgets/
    │   └── themes/
    ├── injection_container.dart
    └── main.dart
 
    
# Project Structure - Proje Yapısı

This Flutter project follows a clean architecture pattern, separating concerns into different layers to improve scalability, maintainability, and testability. Below is a breakdown of each folder's purpose.

Bu Flutter projesi, ölçeklenebilirlik, sürdürülebilirlik ve test edilebilirliği artırmak için farklı katmanlara ayrılmış bir temiz mimari yapısını takip eder. Aşağıda, her klasörün amacı açıklanmaktadır.

---

## `lib/core/`

Contains core functionalities that are application-agnostic and can be reused across different modules. This includes error handling, networking utilities, and constant values.

Uygulamadan bağımsız çekirdek işlevleri içerir ve farklı modüllerde yeniden kullanılabilir. Bu, hata yönetimi, ağ yardımcı araçları ve sabit değerleri içerir.

- ### `lib/core/error/`
  Handles custom error classes and exception handling mechanisms across the app.  
  Uygulama genelinde özel hata sınıfları ve istisna yönetim mekanizmalarını yönetir.

- ### `lib/core/network/`
  Manages networking logic, including API communication and connection management.  
  API iletişimi ve bağlantı yönetimi dahil olmak üzere ağ mantığını yönetir.

- ### `lib/core/utils/`
  Houses utility functions that can be reused throughout the app, such as formatters and helpers.  
  Formatlayıcılar ve yardımcı işlevler gibi uygulama genelinde yeniden kullanılabilecek yardımcı fonksiyonları içerir.

- ### `lib/core/constants.dart`
  Stores constant values and configurations used throughout the app.  
  Uygulama genelinde kullanılan sabit değerler ve yapılandırmaları barındırır.

---

## `lib/data/`

Handles the data layer of the application, responsible for fetching and storing data from external sources, including APIs and databases.

Uygulamanın veri katmanını yönetir, API'ler ve veritabanları gibi harici kaynaklardan veri alıp saklamakla sorumludur.

- ### `lib/data/models/`
  Contains the data models that map the external data sources into Dart objects.  
  Harici veri kaynaklarını Dart objelerine dönüştüren veri modellerini içerir.

- ### `lib/data/repositories/`
  Implements the repositories that handle data logic, such as fetching, caching, and persisting data.  
  Veri getirme, önbellekleme ve verileri kalıcı hale getirme gibi veri mantığını yöneten depoları uygular.

- ### `lib/data/datasources/`
  Manages external data sources, such as API clients or database connections.  
  API istemcileri veya veritabanı bağlantıları gibi harici veri kaynaklarını yönetir.

- ### `lib/data/graphql/`
  (Optional) If using GraphQL, this folder contains the GraphQL queries, mutations, and schemas.  
  (Opsiyonel) Eğer GraphQL kullanılıyorsa, bu klasör GraphQL sorgularını, mutasyonlarını ve şemalarını içerir.

---

## `lib/domain/`

Handles the domain layer, which is independent of any specific external data sources or UI frameworks.

Herhangi bir harici veri kaynağına veya kullanıcı arayüzü çerçevesine bağımlı olmayan alan (domain) katmanını yönetir.

- ### `lib/domain/entities/`
  Contains the core business entities of the application, which are plain Dart objects.  
  Uygulamanın temel iş nesnelerini (business entities) içerir, bunlar sade Dart objeleridir.

- ### `lib/domain/repositories/`
  Defines the interfaces for the repositories, ensuring loose coupling between the data layer and the domain layer.  
  Veri katmanı ile alan katmanı arasında düşük bağlılığı sağlamak için depo arayüzlerini tanımlar.

- ### `lib/domain/usecases/`
  Contains the business logic for specific features, focusing on what the application should do without depending on how the data is retrieved or presented.  
  Uygulamanın nasıl veri alınıp sunulduğuna bağımlı olmadan belirli işlevler için iş mantığını içerir.

---

## `lib/presentation/`

Manages the UI layer of the application, including the state management, pages, widgets, and themes.

Uygulamanın kullanıcı arayüzü katmanını yönetir, durum yönetimi, sayfalar, bileşenler ve temalar dahil.

- ### `lib/presentation/controllers/`
  Holds controllers or state managers (e.g., Riverpod, Provider, Bloc) responsible for the state logic of the UI.  
  Kullanıcı arayüzü için durum mantığını yöneten kontrolörler veya durum yöneticilerini (örn. Riverpod, Provider, Bloc) içerir.

- ### `lib/presentation/pages/`
  Contains the individual pages/screens of the application.  
  Uygulamanın bireysel sayfa ve ekranlarını içerir.

- ### `lib/presentation/widgets/`
  Holds reusable UI components used across different pages of the application.  
  Uygulamanın farklı sayfalarında yeniden kullanılabilecek bileşenleri içerir.

- ### `lib/presentation/themes/`
  Manages the theming and styling of the application.  
  Uygulamanın tema ve stil yönetimini sağlar.

---

## `injection_container.dart`

Centralized configuration for dependency injection, managing how dependencies are created and shared across the application.

Bağımlılıkların nasıl oluşturulup uygulama genelinde paylaşıldığını yöneten merkezi bağımlılık enjeksiyonu yapılandırması.

---

## `main.dart`

The entry point of the application. Initializes the app and starts the root widget.

Uygulamanın giriş noktasıdır. Uygulamayı başlatır ve kök bileşeni çalıştırır.

