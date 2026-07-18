# 🎮 Oyun Sistemleri (Game Systems)

Oyun sistemleri, oyuncunun deneyimini şekillendiren kuralların, ilerleme mekaniklerinin ve geri bildirim döngülerinin bütünüdür. İyi tasarlanmış sistemler oyuncuyu motive eder, oyunu dengeli hale getirir ve uzun süre oynanabilir olmasını sağlar.

---

# 🎯 Öğrenme Hedefleri

Bu bölümü tamamladığında;

- Oyun döngüsünün (Game Loop) nasıl çalıştığını açıklayabilirsin.
- Oyun hedefleri ve ilerleme sistemlerini anlayabilirsin.
- Oyun ekonomisinin temel mantığını kavrayabilirsin.
- Oyuncu ajansı (Player Agency) kavramını açıklayabilirsin.
- Zorluk dengesi ve geri bildirim sistemlerinin önemini değerlendirebilirsin.

---

# 🔄 Oyun Döngüsü (Game Loop)

Her oyunun temelinde sürekli tekrar eden bir döngü bulunur.

```text
Oyuncu Girdisi
      │
      ▼
Oyun Mantığı
      │
      ▼
Fizik ve Yapay Zekâ
      │
      ▼
Animasyonlar
      │
      ▼
Ekranın Güncellenmesi
      │
      ▼
Yeni Kare (Frame)
```

Bu döngü saniyede onlarca kez çalışarak oyunun akıcı görünmesini sağlar.

---

# 🎯 Oyun Hedefleri ve Amaçları

Oyuncuya yön veren görevler ve başarı kriterleridir.

Örnekler:

- Bölümü tamamlamak
- Patronu yenmek
- Belirli sayıda eşya toplamak
- Süreyi aşmadan görevi bitirmek
- Gizli alanları keşfetmek

İyi tanımlanmış hedefler oyuncunun motivasyonunu artırır.

---

# 📈 İlerleme Sistemi (Progression)

Oyuncunun zamanla güçlenmesini ve yeni içeriklerin açılmasını sağlar.

Yaygın ilerleme türleri:

- Seviye (Level)
- Deneyim puanı (XP)
- Beceri ağacı (Skill Tree)
- Yeni ekipmanlar
- Yeni bölgeler

---

# 💰 Oyun Ekonomisi

Oyun ekonomisi; oyun içindeki para birimleri, kaynaklar ve harcama sistemlerini kapsar.

Örnek kaynaklar:

- Altın
- Kristal
- Enerji
- Cephane
- Deneyim puanı

İyi bir ekonomi sistemi oyuncunun sürekli ilerleme hissini destekler.

---

# 📜 Oyun Kuralları

Oyun kuralları oyuncunun neleri yapabileceğini ve yapamayacağını belirler.

Örneğin:

- Oyuncu yalnızca iki silah taşıyabilir.
- Her karakterin belirli bir can değeri vardır.
- Görev tamamlanmadan yeni bölüm açılmaz.

Kurallar, oyunun tutarlı ve dengeli olmasını sağlar.

---

# 🧭 Oyuncu Ajansı (Player Agency)

Player Agency, oyuncunun yaptığı seçimlerin oyun dünyasını anlamlı şekilde etkilemesidir.

Örnekler:

- Diyalog seçimleri
- Farklı sonlar
- Görev sırası seçimi
- Karakter geliştirme tercihleri

Oyuncuya seçim hakkı vermek, oyunun tekrar oynanabilirliğini artırır.

---

# 📢 Geri Bildirim Sistemleri

Oyuncunun yaptığı eylemlerin sonucunu anlamasını sağlar.

Yaygın geri bildirim türleri:

- Ses efektleri
- Titreşim
- Ekran efektleri
- Hasar göstergeleri
- Başarı bildirimleri

İyi geri bildirim, oyuncunun yaptığı eylemleri daha anlaşılır hale getirir.

---

# ⚖️ Zorluk Dengesi

Oyun ne çok kolay ne de çok zor olmalıdır.

Zorluk artırma yöntemleri:

- Daha güçlü düşmanlar
- Daha karmaşık bulmacalar
- Yeni mekanikler
- Zaman sınırlamaları

Dinamik zorluk sistemleri oyuncunun performansına göre oyunu otomatik olarak ayarlayabilir.

---

# 🤝 İş Birliği ve Rekabet

Çok oyunculu oyunlarda farklı etkileşim türleri bulunur.

### İş Birliği (Co-op)

- Ortak görevler
- Takım savaşları
- Kaynak paylaşımı

### Rekabet (Competitive)

- PvP savaşları
- Liderlik tabloları
- Turnuvalar

---

# 🎲 Temel Oyun Mekanikleri

Bir oyunun ana oynanışını oluşturan temel sistemlerdir.

Örneğin:

- Hareket
- Savaş
- Envanter
- Diyalog
- Görev sistemi
- Kaynak toplama
- İnşa etme

Bu mekanikler oyunun kimliğini belirler.

---

# 🎮 Unity'de Kullanımı

Basit bir skor sistemi örneği:

```csharp
public class ScoreManager : MonoBehaviour
{
    public int score = 0;

    public void AddScore(int amount)
    {
        score += amount;
        Debug.Log("Score: " + score);
    }
}
```

---

# 💡 Best Practices

✅ Oyuncuya kısa ve uzun vadeli hedefler sun.

✅ İlerleme hissini sürekli destekle.

✅ Oyun ekonomisini dengeli tasarla.

✅ Oyuncunun seçimlerinin anlamlı olmasına dikkat et.

✅ Geri bildirimleri açık ve anlaşılır yap.

---

# ⚠️ Yaygın Hatalar

❌ Çok fazla görev eklemek

❌ Oyuncuya amaç vermemek

❌ Dengesiz ekonomi sistemi oluşturmak

❌ Zorluk seviyesini ani artırmak

❌ Oyuncu seçimlerinin hiçbir etkisinin olmaması

---

# 🧪 Unity Lab

### Amaç

Basit bir skor sistemi oluştur.

### Görevler

1. Yeni bir UI Text oluştur.
2. Başlangıç skoru **0** olsun.
3. Bir Coin nesnesi ekle.
4. Coin'e dokununca:
   - Coin yok olsun.
   - Skor +10 artsın.
5. Güncel skor ekranda gösterilsin.

---

# 💼 Interview Questions

- Game Loop nedir?
- Player Agency ne anlama gelir?
- Oyun ekonomisi neden önemlidir?
- Oyuncuya geri bildirim vermenin amacı nedir?
- Progression sistemi nasıl tasarlanmalıdır?
- Dinamik zorluk sistemi nedir?
- İyi bir oyun döngüsünün özellikleri nelerdir?

---

# 📚 Ek Kaynaklar

- Game Programming Patterns
- The Art of Game Design – Jesse Schell
- Unity Learn
- Unity UI Documentation
- Extra Credits (Game Design)