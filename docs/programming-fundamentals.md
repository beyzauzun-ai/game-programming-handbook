# 💻 Oyun Programlamasının Temelleri (Programming Fundamentals)

Oyun programlama, bir oyunun çalışmasını sağlayan mantığın ve sistemlerin geliştirilmesini kapsar. Oyuncu hareketleri, yapay zekâ, fizik, kullanıcı arayüzü ve oyun kuralları gibi tüm etkileşimler programlama sayesinde hayata geçirilir.

---

## 🎯 Öğrenme Hedefleri

Bu bölümü tamamladığında;

- Oyun programlamasının temel amacını açıklayabilirsin.
- Oyun programcısının görevlerini tanımlayabilirsin.
- Oyun döngüsünün (Game Loop) nasıl çalıştığını anlayabilirsin.
- Kontrol yapılarının kullanımını öğrenebilirsin.
- Hata ayıklama (Debugging) sürecini açıklayabilirsin.
- Performans optimizasyonunun önemini kavrayabilirsin.

---

# 🎮 Oyun Programlaması Nedir?

Oyun programlama; oyun mekaniğini, kullanıcı etkileşimlerini, fizik sistemlerini ve yapay zekâyı kod ile hayata geçirme sürecidir.

Başlıca görevleri:

- Oyuncu hareketlerini kontrol etmek
- Oyun kurallarını uygulamak
- Yapay zekâ geliştirmek
- Fizik hesaplamalarını yapmak
- Ses ve animasyonları yönetmek
- Kullanıcı arayüzünü kontrol etmek

---

# 👨‍💻 Oyun Programcısının Görevleri

Bir oyun programcısı;

- Gameplay sistemlerini geliştirir.
- Karakter kontrolünü oluşturur.
- Yapay zekâyı programlar.
- UI sistemlerini geliştirir.
- Performans optimizasyonu yapar.
- Hataları düzeltir.
- Takımın diğer üyeleriyle birlikte çalışır.

---

# 🔄 Game Loop (Oyun Döngüsü)

Her oyun sürekli çalışan bir döngüye sahiptir.

```text
Oyunu Başlat
      │
      ▼
Kullanıcı Girdisi
      │
      ▼
Oyun Mantığı
      │
      ▼
Fizik Hesaplamaları
      │
      ▼
Animasyonlar
      │
      ▼
Ekranı Çiz
      │
      ▼
Tekrar Başla
```

Unity'de bu döngünün önemli parçaları:

- `Start()`
- `Update()`
- `FixedUpdate()`
- `LateUpdate()`

---

# 🧩 Nesne Yönelimli Programlama (OOP)

Unity tamamen OOP mantığı üzerine kuruludur.

Temel kavramlar:

- Class
- Object
- Inheritance
- Encapsulation
- Polymorphism
- Abstraction

### Basit C# Örneği

```csharp
public class Player
{
    public int health = 100;

    public void TakeDamage(int damage)
    {
        health -= damage;
    }
}
```

---

# 🔀 Kontrol Yapıları

Programın akışını kontrol etmek için kullanılır.

## if

```csharp
if (health <= 0)
{
    Debug.Log("Game Over");
}
```

---

## switch

```csharp
switch(level)
{
    case 1:
        Debug.Log("Easy");
        break;

    case 2:
        Debug.Log("Medium");
        break;
}
```

---

## for

```csharp
for(int i = 0; i < 5; i++)
{
    Debug.Log(i);
}
```

---

## while

```csharp
while(health > 0)
{
    Debug.Log("Player Alive");
    break;
}
```

---

# 🎯 Olay Yönetimi (Event System)

Oyunlarda birçok olay kullanıcı etkileşimine göre gerçekleşir.

Örneğin;

- Tuşa basılması
- Çarpışma
- Butona tıklama
- Düşmanın ölmesi
- Bölüm tamamlanması

Unity örneği:

```csharp
void OnCollisionEnter(Collision collision)
{
    Debug.Log("Collision!");
}
```

---

# 🐞 Hata Ayıklama (Debugging)

Kod yazarken oluşan hataları bulup düzeltme sürecidir.

Unity'de sık kullanılan araçlar:

- Debug.Log()
- Breakpoints
- Console
- Visual Studio Debugger

Örnek:

```csharp
Debug.Log(playerHealth);
```

---

# ⚡ Performans Optimizasyonu

Performansın iyi olması oyuncu deneyimini doğrudan etkiler.

Optimizasyon için;

- Gereksiz Update() kullanımından kaçın.
- Nesne havuzu (Object Pooling) kullan.
- Bellek kullanımını azalt.
- Draw Call sayısını azalt.
- Profiler kullan.

---

# 💡 En İyi Uygulamalar

✅ Kodlarını küçük fonksiyonlara ayır.

✅ Değişken isimlerini anlamlı seç.

✅ Gereksiz tekrar eden kod yazma.

✅ Kodlarını yorum satırlarıyla açıkla.

✅ Düzenli Git commitleri yap.

---

# ⚠️ Yaygın Hatalar

❌ Her şeyi Update() içine yazmak

❌ Gereksiz Instantiate kullanmak

❌ Null kontrolü yapmamak

❌ Çok büyük sınıflar oluşturmak

❌ Magic Number kullanmak

---

# 🧠 Mini Quiz

### 1. Oyun programlamasının temel amacı nedir?

✅ Oyun mantığını ve işlevselliğini uygulamak.

---

### 2. Unity'de her kare çalışan fonksiyon hangisidir?

✅ Update()

---

### 3. Debug.Log() ne için kullanılır?

✅ Hata ayıklamak ve bilgi yazdırmak.

---

### 4. OOP'nin dört temel prensibi nelerdir?

✅ Encapsulation

✅ Inheritance

✅ Polymorphism

✅ Abstraction

---

# 💼 Mülakat Soruları

- Game Loop nedir?
- Update ile FixedUpdate arasındaki fark nedir?
- OOP nedir?
- Event System nasıl çalışır?
- Debugging neden önemlidir?
- Performans optimizasyonunda nelere dikkat edilir?
- Neden Object Pooling kullanılır?

---

# 📚 Ek Kaynaklar

- Unity Learn
- Microsoft C# Documentation
- Game Programming Patterns – Robert Nystrom
- Clean Code – Robert C. Martin
- Unity Manual
