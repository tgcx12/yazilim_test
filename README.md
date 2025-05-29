# Yazılım Test Mühendisliği Proje Ödevi

Bu proje, **Rest Assured** (rest eşurd) kütüphanesi kullanılarak hazırlanmış bir **otomatik API test projesidir**. Proje kapsamında `GET` ve `POST` HTTP metotları test edilmiştir.

## 🔧 Kullanılan Teknolojiler

- Java
- JUnit 4
- Rest Assured
- JSONPlaceholder Test API

## 🧪 Yapılan Testler

### ✅ 1. `GET /posts/1`
- Sunucuda daha önceden var olan bir veriyi getirir.
- Yanıtta aşağıdakiler doğrulanır:
  - `statusCode == 200`
  - `userId == 1`
  - `id == 1`
  - `title` alanı boş değil
- Yanıt süresi 1 saniyenin altında mı kontrol edilir.

### ✅ 2. `POST /posts`
- Sunucuya yeni bir veri gönderilir (title, body, userId).
- Yanıtta şunlar doğrulanır:
  - `statusCode == 201`
  - Dönen değerlerin eşleştiği
  - Sunucu tarafından oluşturulan `id` değeri
- Yanıt süresi yine 1 saniyenin altında olmalıdır.

## 🚀 Projeyi Çalıştırma

1. IntelliJ IDEA ile projeyi açın.
2. Maven bağımlılıkları yüklü olsun.
3. `JsonPlaceholderApiTest.java` içindeki testleri çalıştırın.

## 🔗 Test API

Kullanılan API:  
👉 https://jsonplaceholder.typicode.com

- Bu API anahtar istemez.
- Sahte (dummy) veri ile çalışır.

## 🛠 GitHub'a Push Sorunu ve Çözümü

> İlk push işleminde şu hatayla karşılaşıldı:
> `error: failed to push some refs to ... (non-fast-forward)`

Bu durum, GitHub’daki main branch'in boş olmamasından kaynaklandı. Aşağıdaki komutla düzeltildi:

```bash
git pull --rebase origin main
git push -u origin main
