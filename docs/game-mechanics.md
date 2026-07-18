# 🎮 Oyun Mekanikleri (Game Mechanics)

Oyun mekaniği, oyuncunun oyun dünyasıyla nasıl etkileşime girdiğini belirleyen kurallar ve sistemlerdir. Bir oyunu eğlenceli, zorlayıcı ve tekrar oynanabilir yapan temel yapı taşları oyun mekanikleridir.

---

## 🎯 Öğrenme Hedefleri

Bu bölümü tamamladığında;

- Oyun mekaniğinin ne olduğunu açıklayabilirsin.
- Oyuncu etkileşimlerini anlayabilirsin.
- Hata ayıklama ve sorun giderme süreçlerini kavrayabilirsin.
- Performans optimizasyonunun neden önemli olduğunu açıklayabilirsin.
- Oyun geliştirmede kullanılan temel programlama dillerini tanıyabilirsin.

---

# 🎮 Oyun Mekaniği Nedir?

Oyun mekaniği, oyuncunun oyun içerisinde gerçekleştirebildiği tüm eylemleri tanımlar.

Örneğin;

- Hareket etmek
- Zıplamak
- Ateş etmek
- Eşya toplamak
- Envanter kullanmak
- Görev tamamlamak
- Seviye atlamak

Bu sistemlerin tamamı oyun mekaniğini oluşturur.

---

# 🤝 Oyuncu Etkileşimi

İyi bir oyun, oyuncunun oyun dünyasıyla sürekli etkileşim kurmasını sağlar.

Oyuncu;

- NPC'lerle konuşabilir.
- Nesneleri kullanabilir.
- Bulmacaları çözebilir.
- Düşmanlarla savaşabilir.
- Çevreyi keşfedebilir.

Bu etkileşimler oyuncu deneyimini doğrudan etkiler.

---

# 🐞 Hata Ayıklama (Debugging)

Debugging, yazılım geliştirme sürecinde oluşan hataların tespit edilmesi ve düzeltilmesidir.

Unity'de yaygın olarak kullanılan araçlar:

- Console
- Debug.Log()
- Breakpoint
- Visual Studio Debugger

### Örnek

```csharp
Debug.Log("Player Health : " + health);
```

---

# 🔧 Sorun Giderme (Troubleshooting)

Sorun giderme yalnızca kod hatalarını değil;

- Performans problemlerini
- Grafik sorunlarını
- Ses problemlerini
- Çarpışma hatalarını
- UI problemlerini

tespit etmeyi de kapsar.

---

# 💻 Oyun Geliştirmede Kullanılan Programlama Dilleri

Modern oyun geliştirmede birçok programlama dili kullanılmaktadır.

| Dil | Kullanım Alanı |
|------|----------------|
| C++ | Unreal Engine, oyun motorları |
| C# | Unity |
| Python | Araç geliştirme, yapay zekâ |
| JavaScript | Web tabanlı oyunlar |
| HTML5 | Web oyunları |

Her dil farklı amaçlar için tercih edilir.

---

# ⚡ Performans Optimizasyonu

Oyunun akıcı çalışabilmesi için optimizasyon büyük önem taşır.

Yaygın optimizasyon teknikleri:

- Draw Call azaltma
- Object Pooling
- LOD kullanımı
- Gereksiz Update() çağrılarından kaçınma
- Bellek yönetimi

---

# 🔄 İterasyon (Iteration)

İterasyon, oyun nesnelerinin veya veri koleksiyonlarının sırayla işlenmesini sağlar.

Örneğin;

```csharp
foreach(GameObject enemy in enemies)
{
    enemy.SetActive(true);
}
```

Bu yöntem birçok nesneyi tek tek kontrol etmeyi kolaylaştırır.

---

# 🚀 Oyun Motorlarında C++

Düşük seviyeli oyun motorlarının büyük kısmı C++ ile geliştirilmiştir.

Avantajları:

- Yüksek performans
- Bellek kontrolü
- Hızlı çalışma
- Donanıma yakın erişim

Bu nedenle Unreal Engine'in temel dili C++'tır.

---

# 💡 En İyi Uygulamalar

✅ Kod tekrarından kaçın.

✅ Küçük fonksiyonlar yaz.

✅ Düzenli test yap.

✅ Performansı sürekli ölç.

✅ Oyuncu deneyimini ön planda tut.

---

# ⚠️ Yaygın Hatalar

❌ Çok karmaşık mekanikler oluşturmak

❌ Sürekli Update() kullanmak

❌ Debug.Log() satırlarını yayına bırakmak

❌ Kod tekrarına düşmek

❌ Performansı son aşamaya bırakmak

---

# 🧠 Mini Quiz

### Oyun mekaniği nedir?

✅ Oyuncunun oyun içerisinde gerçekleştirdiği kurallar ve etkileşimlerdir.

---

### Debugging nedir?

✅ Yazılım hatalarını bulup düzeltme sürecidir.

---

### Oyun geliştirmede C++ neden tercih edilir?

✅ Performansı yüksek olduğu için.

---

### İterasyon ne işe yarar?

✅ Veri koleksiyonlarını sırayla işlemeyi sağlar.

---

# 💼 Mülakat Soruları

- Oyun mekaniği nedir?
- Debugging ile Troubleshooting arasındaki fark nedir?
- Draw Call nedir?
- Neden Object Pooling kullanılır?
- C++ neden oyun motorlarında tercih edilir?
- İterasyon nedir?
- Performans optimizasyonu neden önemlidir?

---

# 📚 Ek Kaynaklar

- Unity Learn
- Unreal Engine Documentation
- Game Programming Patterns
- Clean Code
- Microsoft Learn (C#)
