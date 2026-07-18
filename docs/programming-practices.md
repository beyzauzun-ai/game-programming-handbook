# 💻 Oyun Programlama Uygulamaları (Programming Practices)

Oyun geliştirmede iyi programlama alışkanlıkları; okunabilir, sürdürülebilir ve performanslı kod yazmanın temelidir. Bu bölüm, oyun programcısının günlük geliştirme sürecinde kullandığı temel prensipleri ve teknikleri açıklar.

---

# 🎯 Öğrenme Hedefleri

Bu bölümü tamamladığında;

- Oyun programcısının görevlerini açıklayabilirsin.
- Scripting kavramını anlayabilirsin.
- Kontrol yapılarının oyun geliştirmedeki önemini kavrayabilirsin.
- Event (olay) sistemlerini kullanabilirsin.
- Çarpışma ve fizik sistemlerini kod ile yönetebilirsin.
- Debugging ve optimizasyon süreçlerini uygulayabilirsin.

---

# 👨‍💻 Oyun Programcısının Rolü

Bir oyun programcısı;

- Gameplay sistemlerini geliştirir.
- Yapay zekâ sistemlerini yazar.
- Kullanıcı girişlerini yönetir.
- UI sistemlerini programlar.
- Fizik ve çarpışmaları uygular.
- Performans optimizasyonu yapar.
- Hataları düzeltir.

Programcı; tasarımcılar, sanatçılar ve test ekipleriyle birlikte çalışır.

---

# 📜 Oyun Betikleri (Game Scripting)

Script'ler, oyun davranışlarını kontrol eden C# dosyalarıdır.

Örneğin:

- Karakter hareketi
- Kamera kontrolü
- Silah sistemi
- Kapı açma
- Görev sistemi

Basit bir örnek:

```csharp
using UnityEngine;

public class Door : MonoBehaviour
{
    public void OpenDoor()
    {
        Debug.Log("Door Opened");
    }
}
```

---

# 🔀 Kontrol Yapıları

Programın akışını belirleyen temel yapılardır.

Yaygın örnekler:

- if / else
- switch
- for
- while
- foreach

Örnek:

```csharp
if(playerHealth <= 0)
{
    GameOver();
}
```

---

# 🎮 Event Handling (Olay Yönetimi)

Oyunlarda birçok sistem olaylara göre çalışır.

Örnek olaylar:

- Tuşa basılması
- Çarpışma
- Butona tıklama
- Animasyon bitmesi
- Görev tamamlanması

Unity örneği:

```csharp
void OnCollisionEnter(Collision collision)
{
    Debug.Log("Collision!");
}
```

---

# 💥 Çarpışma Tespiti

Çarpışmalar gameplay'in temel parçalarından biridir.

Kullanılan yöntemler:

- OnCollisionEnter()
- OnCollisionStay()
- OnCollisionExit()
- OnTriggerEnter()
- Raycast

Doğru çarpışma yönetimi daha güvenilir oyun mekanikleri oluşturur.

---

# 🌍 Oyun Fiziği

Unity'nin PhysX sistemi;

- Yerçekimi
- Kuvvet
- Momentum
- Sürtünme
- Çarpışma

hesaplamalarını gerçekleştirir.

Örnek:

```csharp
rb.AddForce(Vector3.up * jumpForce);
```

---

# 🐞 Debugging

Debugging, oyun geliştirme sürecinin vazgeçilmez bir parçasıdır.

Yaygın araçlar:

- Debug.Log()
- Breakpoints
- Unity Console
- Visual Studio Debugger

Örnek:

```csharp
Debug.Log(currentScore);
```

---

# ⚡ Kod Optimizasyonu

Daha performanslı oyunlar için:

- Gereksiz Update() kullanımını azalt.
- Object Pooling uygula.
- LINQ kullanımını kritik döngülerde sınırla.
- Referansları önbelleğe al.
- Gereksiz bellek tahsisinden kaçın.

---

# 🎨 Oyun Özelleştirme (Customization)

Bazı oyunlar oyuncuların içerik oluşturmasına izin verir.

Örnekler:

- Mod desteği
- Karakter görünümü
- Harita editörü
- Özel silahlar
- Kullanıcı arayüzü temaları

Bu özellikler oyunun ömrünü uzatabilir.

---

# 🧩 Kod Organizasyonu

Projelerde klasör yapısını düzenli tutmak önemlidir.

Örnek yapı:

```text
Scripts/
│
├── Player/
├── Enemy/
├── UI/
├── Managers/
├── Inventory/
├── AI/
└── Utilities/
```

Bu yapı projeyi daha okunabilir hâle getirir.

---

# 💡 Best Practices

✅ Tek sorumluluk prensibini (Single Responsibility Principle) uygula.

✅ Script isimlerini açıklayıcı seç.

✅ Kod tekrarından kaçın.

✅ Inspector'da kullanılacak alanları `[SerializeField]` ile yönet.

✅ Düzenli Git commit'leri yap.

---

# ⚠️ Yaygın Hatalar

❌ Çok büyük MonoBehaviour sınıfları oluşturmak.

❌ Her şeyi Update() içinde çalıştırmak.

❌ Gereksiz public değişken kullanmak.

❌ Kodları açıklamasız bırakmak.

❌ Tek script içinde çok fazla görev toplamak.

---

# 🧪 Unity Lab

## Amaç

Basit bir oyuncu sistemi oluştur.

### Görevler

1. PlayerMovement script'i yaz.
2. Space ile zıplama ekle.
3. Bir küpe çarpınca skor artır.
4. Skoru UI üzerinde göster.
5. Console'a Debug.Log() ile bilgi yazdır.
6. Kodlarını ayrı script'lere böl.

---

# 💼 Interview Questions

- Game Scripting nedir?
- Event Handling nasıl çalışır?
- Debugging neden önemlidir?
- Object Pooling neden kullanılır?
- Single Responsibility Principle nedir?
- Oyun programcısının temel sorumlulukları nelerdir?
- Unity'de fizik sistemi nasıl çalışır?

---

# 📚 Ek Kaynaklar

- Unity Learn
- Unity Scripting API
- Microsoft Learn – C#
- Clean Code – Robert C. Martin
- Game Programming Patterns
