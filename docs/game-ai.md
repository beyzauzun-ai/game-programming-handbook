# 🤖 Oyun Yapay Zekâsı (Game AI)

Oyun yapay zekâsı (Game AI), oyuncu dışındaki karakterlerin (NPC'ler) çevrelerini algılamasını, karar vermesini ve uygun davranışlar sergilemesini sağlayan sistemlerin bütünüdür. Amaç, oyuncuya gerçekçi ve eğlenceli bir deneyim sunmaktır.

---

# 🎯 Öğrenme Hedefleri

Bu bölümü tamamladığında;

- Game AI kavramını açıklayabilirsin.
- NPC davranış sistemlerini anlayabilirsin.
- Finite State Machine (FSM) mantığını kavrayabilirsin.
- Behavior Tree yapısını açıklayabilirsin.
- NavMesh ve Pathfinding kullanımını öğrenebilirsin.
- Basit AI sistemleri geliştirebilirsin.

---

# 🤖 Game AI Nedir?

Game AI;

- NPC kontrolü
- Düşman davranışları
- Dost karakterler
- Devriyeler
- Diyalog sistemleri
- Karar verme mekanizmaları

gibi sistemleri yönetir.

---

# 👤 NPC (Non-Player Character)

NPC, oyuncu tarafından kontrol edilmeyen karakterdir.

Örnekler:

- Düşman asker
- Satıcı
- Görev veren karakter
- Polis
- Hayvanlar

NPC'ler belirli kurallara göre hareket eder.

---

# 🔄 Finite State Machine (FSM)

FSM, AI'nin farklı durumlar arasında geçiş yapmasını sağlar.

```text
      Idle
        │
        ▼
      Patrol
        │
 Oyuncu görüldü
        ▼
      Chase
        │
 Yakın mesafe
        ▼
      Attack
        │
 Oyuncu kaçtı
        ▼
      Patrol
```

Her durumda yalnızca belirli davranışlar çalışır.

---

# 🌳 Behavior Tree

Behavior Tree, daha karmaşık AI davranışları oluşturmak için kullanılır.

Örnek yapı:

```text
Root
│
├── Enemy Visible?
│      │
│      ├── Yes
│      │      └── Attack
│      │
│      └── No
│             └── Patrol
```

Avantajları:

- Modüler yapı
- Kolay genişletilebilir
- AAA oyunlarda yaygın kullanım

---

# 🧭 Pathfinding

NPC'nin hedefe ulaşmak için en uygun yolu bulmasını sağlar.

En yaygın algoritma:

- A* (A-Star)

Kullanım alanları:

- Düşman takibi
- Devriye rotaları
- Araç navigasyonu

---

# 🗺️ NavMesh

Unity'de karakterlerin yürüyebileceği alanları belirleyen sistemdir.

Avantajları:

- Engelden kaçınma
- Otomatik rota oluşturma
- Gerçekçi hareket

Örnek:

```csharp
NavMeshAgent agent;

void Start()
{
    agent = GetComponent<NavMeshAgent>();
}

void Update()
{
    agent.SetDestination(player.position);
}
```

---

# 👀 Algılama Sistemleri

NPC çevresini algılayabilir.

Yöntemler:

- Raycast
- Trigger
- Görüş açısı
- Mesafe kontrolü
- Ses algılama

---

# 💬 Diyalog Sistemleri

NPC'ler oyuncuyla etkileşim kurabilir.

Örnekler:

- Görev verme
- Ticaret
- Hikâye anlatımı
- Seçimli konuşmalar

---

# 🧠 Karar Verme

AI farklı durumlara göre karar verir.

Örneğin:

- Can azsa kaç.
- Oyuncu uzaktaysa yaklaş.
- Oyuncu görünmüyorsa devriye gez.
- Mermi bittiyse saklan.

---

# ⚡ AI Optimizasyonu

Büyük oyunlarda yüzlerce NPC bulunabilir.

Optimizasyon yöntemleri:

- Görüş mesafesini sınırla.
- Gereksiz güncellemeleri azalt.
- NavMesh kullan.
- Object Pooling uygula.
- LOD sistemlerinden yararlan.

---

# 🎮 Unity'de Kullanımı

Basit takip sistemi:

```csharp
using UnityEngine;
using UnityEngine.AI;

public class EnemyAI : MonoBehaviour
{
    public Transform player;

    private NavMeshAgent agent;

    void Start()
    {
        agent = GetComponent<NavMeshAgent>();
    }

    void Update()
    {
        agent.SetDestination(player.position);
    }
}
```

---

# 💡 Best Practices

✅ FSM veya Behavior Tree kullan.

✅ AI kararlarını modüler tasarla.

✅ NavMesh tercih et.

✅ Performans için görüş mesafesini sınırla.

✅ AI kodunu okunabilir tut.

---

# ⚠️ Yaygın Hatalar

❌ Sürekli Raycast çalıştırmak.

❌ Tüm NPC'leri her kare güncellemek.

❌ Karmaşık FSM yapıları oluşturmak.

❌ Pathfinding'i optimize etmemek.

❌ AI davranışlarını tek script içinde yazmak.

---

# 🧪 Unity Lab

## Amaç

Basit bir düşman takip sistemi oluştur.

### Görevler

1. Plane oluştur.
2. Player Capsule ekle.
3. Enemy Capsule ekle.
4. Enemy'ye NavMeshAgent ekle.
5. Sahneyi Bake et.
6. Enemy sürekli Player'ı takip etsin.

---

# 💼 Interview Questions

- Game AI nedir?
- FSM nasıl çalışır?
- Behavior Tree'nin avantajları nelerdir?
- NavMesh ne işe yarar?
- A* algoritması neden kullanılır?
- NPC algılama yöntemleri nelerdir?
- AI optimizasyonu neden önemlidir?

---

# 📚 Ek Kaynaklar

- Unity Learn
- Unity AI Navigation
- Unity Manual
- Game Programming Patterns
- Artificial Intelligence for Games – Ian Millington
