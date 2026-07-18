# 🔀 Akış Kontrolü ve Nesne Yönelimli Programlama

Programlama, yalnızca kod yazmaktan ibaret değildir. Bir oyunun nasıl davranacağını belirleyen karar mekanizmaları, tekrar eden işlemler ve nesnelerin birbirleriyle olan ilişkileri bu bölümün temelini oluşturur.

---

# 🎯 Öğrenme Hedefleri

Bu bölümü tamamladığında;

- Akış kontrolünün ne olduğunu açıklayabilirsin.
- if, switch ve döngü yapılarını kullanabilirsin.
- Oyun mantığının nasıl oluşturulduğunu anlayabilirsin.
- Kapsülleme (Encapsulation) kavramını açıklayabilirsin.
- Çok biçimliliğin (Polymorphism) kullanım amacını kavrayabilirsin.

---

# 🔄 Akış Kontrolü (Control Flow)

Akış kontrolü, programın hangi kod satırını hangi sırayla çalıştıracağını belirler.

Temel kontrol yapıları:

- if
- else
- switch
- for
- while
- do-while

Bu yapılar sayesinde oyun farklı durumlara göre farklı davranışlar sergileyebilir.

---

# 🔀 if Yapısı

Belirli bir koşul doğru olduğunda belirli kodların çalışmasını sağlar.

```csharp
if(playerHealth <= 0)
{
    Debug.Log("Game Over");
}
```

---

# 🎯 switch Yapısı

Bir değişkenin değerine göre farklı işlemler gerçekleştirir.

```csharp
switch(level)
{
    case 1:
        Debug.Log("Easy");
        break;

    case 2:
        Debug.Log("Medium");
        break;

    default:
        Debug.Log("Unknown");
        break;
}
```

---

# 🔁 Döngüler (Loops)

Tekrarlayan işlemleri otomatikleştirir.

## for

```csharp
for(int i = 0; i < 10; i++)
{
    Debug.Log(i);
}
```

---

## while

```csharp
while(playerHealth > 0)
{
    Debug.Log("Alive");
    break;
}
```

---

## foreach

Unity'de çok sık kullanılır.

```csharp
foreach(GameObject enemy in enemies)
{
    enemy.SetActive(true);
}
```

---

# ⏭️ Jump Statements

Kodun akışını değiştirmek için kullanılır.

Örneğin:

- break
- continue
- return

```csharp
if(score >= 100)
{
    return;
}
```

---

# 🎮 Oyun Mantığı (Game Logic)

Game Logic;

Oyunun kurallarını belirleyen kodların tamamıdır.

Örneğin;

- Hasar sistemi
- Skor sistemi
- Can sistemi
- Görev sistemi
- Envanter sistemi

bunların tamamı oyun mantığını oluşturur.

---

# 🧩 Nesne Yönelimli Programlama (OOP)

Unity tamamen OOP mantığı üzerine kuruludur.

Temel prensipleri:

- Encapsulation
- Inheritance
- Polymorphism
- Abstraction

---

# 🔒 Encapsulation (Kapsülleme)

Bir nesnenin iç detaylarını gizleyerek yalnızca gerekli bilgileri dışarı açar.

```csharp
public class Player
{
    private int health = 100;

    public int GetHealth()
    {
        return health;
    }
}
```

Avantajları:

- Veri güvenliği
- Daha düzenli kod
- Hata riskini azaltma

---

# 🔄 Polymorphism (Çok Biçimlilik)

Aynı metodun farklı sınıflarda farklı davranış göstermesidir.

```csharp
public virtual void Attack()
{
    Debug.Log("Attack");
}
```

```csharp
public override void Attack()
{
    Debug.Log("Magic Attack");
}
```

---

# 🎮 Unity'de Kullanımı

Unity'de OOP sürekli kullanılır.

Örneğin;

- Player
- Enemy
- NPC
- Weapon

bunların tamamı farklı sınıflardır.

Her biri kendi özelliklerine sahiptir.

---

# 💡 En İyi Uygulamalar

✅ Küçük sınıflar oluştur.

✅ Gereksiz if bloklarından kaçın.

✅ Kod tekrarını azalt.

✅ Fonksiyon isimlerini anlamlı seç.

✅ OOP prensiplerini kullan.

---

# ⚠️ Yaygın Hatalar

❌ Çok büyük sınıflar oluşturmak

❌ İç içe çok fazla if kullanmak

❌ Tekrarlayan kod yazmak

❌ private yerine her şeyi public yapmak

❌ Döngüler içerisinde gereksiz işlem yapmak

---

# 🧠 Mini Quiz

### Programlamada akış kontrolü nedir?

✅ Kodun çalıştırılma sırasını belirleyen yapılardır.

---

### switch ne için kullanılır?

✅ Bir değişkenin değerine göre farklı işlemler yapmak için.

---

### Encapsulation nedir?

✅ Nesnenin iç detaylarını gizleme prensibidir.

---

### Polymorphism nedir?

✅ Aynı metodun farklı sınıflarda farklı davranmasıdır.

---

# 💼 Mülakat Soruları

- if ile switch arasındaki fark nedir?

- while ile for arasındaki fark nedir?

- Encapsulation neden önemlidir?

- Polymorphism nedir?

- OOP'nin dört temel prensibi nelerdir?

- Unity neden OOP kullanır?

---

# 📚 Ek Kaynaklar

- Microsoft Learn – C#
- Unity Learn
- Clean Code – Robert C. Martin
- Game Programming Patterns