# ⚙️ Unity'de Fizik ve Çarpışmalar (Physics & Collisions)

Unity'de fizik sistemi, oyun dünyasındaki nesnelerin gerçekçi hareket etmesini ve birbirleriyle etkileşim kurmasını sağlar. Çarpışmalar, tetikleyiciler (Triggers), ışınlar (Raycasts) ve oyuncu girdileri bu sistemin temel bileşenleridir.

---

# 🎯 Öğrenme Hedefleri

Bu bölümü tamamladığında;

- Collider bileşeninin görevini açıklayabilirsin.
- Rigidbody'nin fizik sistemindeki rolünü anlayabilirsin.
- Çarpışma olaylarını (Collision Events) kullanabilirsin.
- Trigger sisteminin çalışma mantığını kavrayabilirsin.
- Raycast kullanımını öğrenebilirsin.
- Input sistemi ile kullanıcı etkileşimlerini kontrol edebilirsin.

---

# 🧱 Collider Nedir?

Collider, bir GameObject'in fiziksel sınırlarını belirleyen bileşendir.

Collider sayesinde;

- Çarpışmalar algılanır.
- Trigger olayları gerçekleşir.
- Fizik motoru nesneyi tanır.

### Yaygın Collider Türleri

| Collider | Kullanım Alanı |
|-----------|----------------|
| Box Collider | Kutu şeklindeki nesneler |
| Sphere Collider | Top ve küreler |
| Capsule Collider | Karakterler |
| Mesh Collider | Karmaşık modeller |

---

# ⚙️ Rigidbody

Rigidbody, GameObject'i Unity'nin fizik sistemine dahil eder.

Sağladıkları:

- Yerçekimi
- Kuvvet uygulama
- Momentum
- Gerçekçi hareket
- Çarpışma hesaplamaları

### Kuvvet Uygulama

```csharp
Rigidbody rb;

void Start()
{
    rb = GetComponent<Rigidbody>();
}

void Update()
{
    if(Input.GetKeyDown(KeyCode.Space))
    {
        rb.AddForce(Vector3.up * 300);
    }
}
```

---

# 💥 Çarpışmalar (Collision)

İki Collider fiziksel olarak temas ettiğinde Collision Event oluşur.

### OnCollisionEnter()

```csharp
void OnCollisionEnter(Collision collision)
{
    Debug.Log("Çarpışma gerçekleşti!");
}
```

İlk temas anında çalışır.

---

### OnCollisionStay()

```csharp
void OnCollisionStay(Collision collision)
{
    Debug.Log("Temas devam ediyor.");
}
```

Temas sürdüğü sürece her fizik güncellemesinde çalışır.

---

### OnCollisionExit()

```csharp
void OnCollisionExit(Collision collision)
{
    Debug.Log("Temas sona erdi.");
}
```

İki nesne ayrıldığında çalışır.

---

# 🚪 Trigger Sistemi

Bazen fiziksel çarpışma istemeyiz.

Örneğin;

- Checkpoint
- Kapılar
- Görev alanları
- Toplanabilir eşyalar

Bu durumda Collider üzerindeki **Is Trigger** seçeneği kullanılır.

```csharp
void OnTriggerEnter(Collider other)
{
    Debug.Log("Trigger alanına girildi.");
}
```

---

# 🧩 Collision Matrix

Unity'de hangi katmanların (Layers) birbirleriyle çarpışacağını belirler.

Örneğin;

| Layer | Çarpışabilir |
|--------|--------------|
| Player | Enemy, Ground |
| Enemy | Player, Ground |
| UI | Hiçbiri |

Bu yapı gereksiz fizik hesaplamalarını azaltarak performansı artırır.

---

# 🏷️ Layers

Layer sistemi;

- Çarpışmaları filtrelemek
- Kameraları ayırmak
- Raycast filtrelemek
- Performansı artırmak

amacıyla kullanılır.

---

# 🎯 Raycast

Raycast görünmez bir ışın göndererek önündeki nesneleri algılar.

Kullanım alanları:

- Silah sistemleri
- Nesne seçimi
- NPC görüş sistemi
- Etkileşim sistemleri

```csharp
RaycastHit hit;

if(Physics.Raycast(transform.position,
                   transform.forward,
                   out hit,
                   100))
{
    Debug.Log(hit.collider.name);
}
```

---

# ⌨️ Input.GetKeyDown()

Oyuncunun bir tuşa ilk bastığı anı algılar.

```csharp
if(Input.GetKeyDown(KeyCode.Space))
{
    Debug.Log("Zıplama");
}
```

Sadece ilk karede çalışır.

---

# ⚙️ Kinematic Rigidbody

Kinematic Rigidbody fizik kuvvetlerinden etkilenmez.

Genellikle;

- Platformlar
- Asansörler
- Kapılar
- Animasyon kontrollü nesneler

için kullanılır.

---

# 🎮 Unity'de Kullanımı

En sık kullanılan fizik işlemleri:

```csharp
rb.AddForce(Vector3.forward * 500);
```

```csharp
Physics.Raycast(...)
```

```csharp
OnCollisionEnter()
```

```csharp
OnTriggerEnter()
```

---

# 💡 Best Practices

✅ Gereksiz Rigidbody kullanma.

✅ Trigger ile Collision'ı doğru yerde kullan.

✅ Layer Collision Matrix'i düzenle.

✅ Fizik hareketleri için FixedUpdate() kullan.

✅ Raycast mesafesini sınırlandır.

---

# ⚠️ Yaygın Hatalar

❌ Rigidbody bulunan nesneyi Transform ile hareket ettirmek.

❌ Trigger yerine normal Collider kullanmak.

❌ Layer ayarlarını unutmak.

❌ Update() içinde sürekli Raycast çalıştırmak.

❌ Çok fazla Mesh Collider kullanmak.

---

# 🧪 Mini Challenge

🎯 Görev

Bir Plane oluştur.

Bir Cube ekle.

Cube'a Rigidbody ekle.

Space tuşuna basıldığında Cube yukarı doğru zıplasın.

Cube yere çarptığında Console'a:

```text
Landed!
```

mesajı yazdır.

---

# 💼 Interview Questions

- Collider nedir?
- Rigidbody ne işe yarar?
- Trigger ile Collision arasındaki fark nedir?
- Raycast hangi durumlarda kullanılır?
- Layer sistemi neden önemlidir?
- FixedUpdate ile Update arasındaki fark nedir?
- OnCollisionEnter() ne zaman çalışır?

---

# 📚 Ek Kaynaklar

- Unity Manual
- Unity Physics Documentation
- Unity Learn
- Unity Scripting API
- Game Programming Patterns
