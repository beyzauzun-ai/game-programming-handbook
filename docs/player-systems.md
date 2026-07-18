# 👤 Oyuncu Sistemleri (Player Systems)

Bir oyunun en önemli bileşeni oyuncudur. Oyuncunun hareket etmesi, savaşabilmesi, envanter kullanabilmesi ve oyun dünyasıyla etkileşime girebilmesi, oyuncu sistemleri sayesinde mümkün olur.

---

# 🎯 Öğrenme Hedefleri

Bu bölümü tamamladığında;

- Character Controller'ın görevini açıklayabilirsin.
- Rigidbody ile hareket sistemi oluşturabilirsin.
- Oyuncu sağlık sistemini tasarlayabilirsin.
- Basit bir savaş sistemi geliştirebilirsin.
- Envanter mantığını anlayabilirsin.
- Kullanıcı arayüzü (UI) ile oyun sistemlerini ilişkilendirebilirsin.

---

# 🎮 Character Controller

Character Controller, oyuncunun hareketlerini yöneten bileşendir.

Temel görevleri:

- Hareket
- Zıplama
- Eğilme
- Koşma
- Merdiven çıkma

Unity'de iki temel yaklaşım bulunur:

- **Character Controller Component**
- **Rigidbody Tabanlı Hareket**

---

# ⚙️ Rigidbody ile Hareket

Fizik tabanlı oyunlarda Rigidbody kullanılır.

```csharp
using UnityEngine;

public class PlayerMovement : MonoBehaviour
{
    public float speed = 5f;
    private Rigidbody rb;

    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    void FixedUpdate()
    {
        float x = Input.GetAxis("Horizontal");
        float z = Input.GetAxis("Vertical");

        Vector3 movement = new Vector3(x, 0, z);

        rb.MovePosition(transform.position + movement * speed * Time.fixedDeltaTime);
    }
}
```

> **Neden `FixedUpdate()`?** Çünkü fizik işlemleri Unity'de sabit zaman aralıklarında çalışır.

---

# 🚶 Transform.Translate()

Basit projelerde fizik gerektirmeyen hareketler için kullanılabilir.

```csharp
transform.Translate(Vector3.forward * Time.deltaTime * 5);
```

### Ne zaman kullanılır?

- Menü karakterleri
- Kamera hareketleri
- Basit prototipler

---

# ❤️ Sağlık Sistemi (Health System)

Oyuncunun aldığı hasarı ve kalan canını takip eder.

```csharp
public class PlayerHealth : MonoBehaviour
{
    public int health = 100;

    public void TakeDamage(int damage)
    {
        health -= damage;

        if (health <= 0)
        {
            Die();
        }
    }

    void Die()
    {
        Debug.Log("Player Died");
    }
}
```

---

# ⚔️ Savaş Sistemi (Combat System)

Bir savaş sistemi genellikle şu bileşenlerden oluşur:

- Hasar (Damage)
- Can (Health)
- Silah
- Menzil
- Saldırı hızı
- Kritik hasar
- Savunma

Basit saldırı örneği:

```csharp
public void Attack()
{
    Debug.Log("Attack!");
}
```

---

# ✨ Oyuncu Yetenekleri (Abilities)

Oyuncular zamanla yeni yetenekler kazanabilir.

Örnekler:

- Dash
- Double Jump
- Sprint
- Heal
- Shield
- Fireball

Bu sistemler ScriptableObject veya Ability Manager ile yönetilebilir.

---

# 🎒 Envanter Sistemi (Inventory)

Envanter sistemi oyuncunun topladığı eşyaları saklar.

Temel özellikleri:

- Eşya ekleme
- Eşya çıkarma
- Kullanma
- Sıralama
- Ekipman yönetimi

Basit örnek:

```csharp
List<string> inventory = new List<string>();

inventory.Add("Sword");
inventory.Add("Potion");
```

---

# 🖥️ Kullanıcı Arayüzü (UI)

UI oyuncuya bilgi verir.

Yaygın UI elemanları:

- Health Bar
- Mana Bar
- Minimap
- Inventory
- Pause Menu
- Score
- Crosshair

---

# 🤝 Nesne Etkileşimi (Object Interaction)

Oyuncular oyun dünyasındaki nesnelerle etkileşime girebilir.

Örnekler:

- Kapı açma
- Sandık açma
- NPC ile konuşma
- Eşya toplama
- Butona basma

Raycast örneği:

```csharp
RaycastHit hit;

if (Physics.Raycast(transform.position, transform.forward, out hit, 3))
{
    Debug.Log(hit.collider.name);
}
```

---

# 📌 Best Practices

✅ Hareket sistemi ile fizik sistemini karıştırma.

✅ Sağlık sistemini ayrı bir sınıfta tut.

✅ UI kodlarını oyun mantığından ayır.

✅ Envanter sistemini genişletilebilir tasarla.

✅ Time.deltaTime kullanarak kare hızından bağımsız hareket oluştur.

---

# ⚠️ Yaygın Hatalar

❌ Transform ile Rigidbody'yi aynı anda hareket ettirmek.

❌ Sağlık değişkenini her yerden erişilebilir yapmak.

❌ UI kodlarını Player script'ine yazmak.

❌ Envanteri yalnızca string listesiyle yönetmek.

❌ Raycast mesafesini kontrol etmemek.

---

# 🧪 Unity Lab

### Amaç

Basit bir oyuncu sistemi oluştur.

### Görevler

1. Plane oluştur.
2. Capsule ekle.
3. Capsule'a Rigidbody ekle.
4. WASD ile hareket ettir.
5. Space ile zıplat.
6. Can değeri 100 olsun.
7. Bir küpe çarptığında 10 hasar alsın.
8. Can 0 olduğunda Console'a:

```text
Game Over
```

yazdır.

---

# 💼 Interview Questions

- Character Controller ile Rigidbody arasındaki fark nedir?
- Neden fizik hareketleri FixedUpdate() içinde yapılmalıdır?
- Health sistemi nasıl tasarlanır?
- Combat sistemi hangi bileşenlerden oluşur?
- Inventory sistemi nasıl geliştirilebilir?
- Raycast hangi durumlarda tercih edilir?
- UI neden oyun mantığından ayrılmalıdır?

---

# 📚 Ek Kaynaklar

- Unity Learn
- Unity Manual
- Unity Input System Documentation
- Game Programming Patterns
- Microsoft Learn C#
