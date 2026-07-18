# 🧱 Unity'de Nesneler ve Veri Yönetimi (Objects & Data)

Unity'deki her oyun nesnesi (GameObject), sahnede belirli bir konuma, dönüşe ve ölçeğe sahiptir. Bu bilgiler **Transform** bileşeni tarafından yönetilir. Ayrıca oyun sırasında verilerin saklanması, nesnelerin çoğaltılması ve fizik tabanlı hareketler de bu bölümün temel konularıdır.

---

# 🎯 Öğrenme Hedefleri

Bu bölümü tamamladığında;

- Dünya uzayı ve yerel uzay kavramlarını açıklayabilirsin.
- Vektörlerin oyun geliştirmedeki kullanımını anlayabilirsin.
- Quaternion ve Euler dönüşleri arasındaki farkı açıklayabilirsin.
- Transform bileşenini etkin şekilde kullanabilirsin.
- PlayerPrefs ile veri saklayabilirsin.
- Instantiate fonksiyonu ile nesne oluşturabilirsin.
- Rigidbody'nin görevini açıklayabilirsin.

---

# 🌍 Dünya Uzayı (World Space)

Unity'de her GameObject dünya koordinat sisteminde bulunur.

Koordinatlar:

- X → Sağ / Sol
- Y → Yukarı / Aşağı
- Z → İleri / Geri

```text
        Y
        ↑
        |
        |
X -------+------→ Z
```

Bir nesnenin konumu dünya koordinatlarına göre belirlenebilir.

---

# 📍 Vektörler (Vectors)

Vektörler;

- Konumu
- Yönü
- Hızı
- Kuvveti

temsil etmek için kullanılır.

Unity'de en sık kullanılan yapı:

```csharp
Vector3
```

Örnek:

```csharp
Vector3 direction = new Vector3(0,1,0);
```

Bu vektör yukarı yönü temsil eder.

---

# 🔄 Euler ve Quaternion

Unity iki farklı dönüş sistemi kullanır.

## Euler Angles

İnsanlar için okunması kolaydır.

```csharp
transform.rotation =
Quaternion.Euler(0,90,0);
```

---

## Quaternion

Unity'nin arka planda kullandığı dönüş sistemidir.

Avantajları:

- Gimbal Lock oluşmaz.
- Daha kararlı dönüşler sağlar.
- Matematiksel olarak daha verimlidir.

---

# 🧱 Transform Bileşeni

Her GameObject'in sahip olduğu en temel bileşendir.

Transform üç temel bilgiyi saklar.

| Özellik | Açıklama |
|----------|----------|
| Position | Konum |
| Rotation | Dönüş |
| Scale | Ölçek |

Örnek:

```csharp
transform.position =
new Vector3(0,2,0);
```

---

# 💾 Serialization (Serileştirme)

Serialization, verilerin kaydedilebilir veya aktarılabilir bir biçime dönüştürülmesidir.

Unity'de Inspector'da görünmesini istediğimiz değişkenler:

```csharp
[SerializeField]
private int health;
```

Avantajları:

- Inspector'dan düzenlenebilir.
- Veri saklanabilir.
- JSON/XML gibi formatlara dönüştürülebilir.

---

# 💾 PlayerPrefs

PlayerPrefs küçük verileri saklamak için kullanılır.

Örnek:

```csharp
PlayerPrefs.SetInt("Score",100);
PlayerPrefs.Save();
```

Okuma:

```csharp
int score =
PlayerPrefs.GetInt("Score");
```

Kullanım alanları:

- Ses ayarları
- Grafik ayarları
- En yüksek skor
- Son kayıt

---

# ⚙️ Rigidbody

Rigidbody fizik motorunu aktif hale getirir.

Sağladıkları:

- Yerçekimi
- Kuvvet
- Momentum
- Çarpışma
- Fizik tabanlı hareket

Örnek:

```csharp
Rigidbody rb;

void Start()
{
    rb = GetComponent<Rigidbody>();

    rb.AddForce(Vector3.forward*500);
}
```

---

# 📦 Instantiate()

Instantiate yeni bir GameObject oluşturur.

```csharp
Instantiate(enemyPrefab,
transform.position,
Quaternion.identity);
```

Kullanım alanları:

- Mermi oluşturma
- Düşman oluşturma
- Efekt üretme
- Power-up oluşturma

---

# ☁️ Unity Cloud Build

Unity Cloud Build;

Projeyi otomatik olarak farklı platformlar için derleyebilir.

Destekler:

- Android
- iOS
- Windows
- macOS

Avantajları:

- Otomatik Build
- CI/CD desteği
- Takım çalışması

---

# 🎮 Unity'de Kullanımı

En sık kullanılan Transform kodları:

```csharp
transform.position += Vector3.forward;
```

```csharp
transform.Rotate(0,90,0);
```

```csharp
transform.localScale =
Vector3.one*2;
```

---

# 📌 Best Practices

✅ Transform'u gereksiz yere her kare değiştirme.

✅ Rigidbody bulunan nesneleri fizik yöntemleriyle hareket ettir.

✅ PlayerPrefs'i yalnızca küçük veriler için kullan.

✅ Instantiate yerine sık oluşturulan nesnelerde Object Pooling tercih et.

---

# ⚠️ Yaygın Hatalar

❌ Rigidbody bulunan nesneyi doğrudan Transform ile hareket ettirmek.

❌ PlayerPrefs içinde büyük veri saklamak.

❌ Çok fazla Instantiate kullanmak.

❌ Quaternion yerine sürekli Euler kullanmak.

---

# 🧪 Mini Challenge

🎯 Görev

Bir Cube oluştur.

Başlangıçta:

- X = 0
- Y = 2
- Z = 0

konumuna gelsin.

Space tuşuna basıldığında:

- Yeni bir Cube oluştur.

---

# 💼 Interview Questions

- Transform nedir?
- Vector3 neden kullanılır?
- Quaternion neden tercih edilir?
- PlayerPrefs ne için kullanılır?
- Rigidbody ne işe yarar?
- Instantiate nasıl çalışır?
- Serialization nedir?

---

# 📚 Ek Kaynaklar

- Unity Learn
- Unity Scripting API
- Unity Manual
- Microsoft Learn C#
- Game Programming Patterns
