# 🎮 Animation Integration (Animasyon Entegrasyonu)

Animation Integration, animasyon sisteminin oyun mantığı ve C# kodlarıyla birlikte çalışmasını ifade eder.

Animasyonlar yalnızca görsel hareketlerden ibaret değildir; oyuncu girişleri, fizik sistemi ve oyun mekaniği ile senkronize çalışmalıdır.

---

# 🎯 Öğrenme Hedefleri

Bu bölümü tamamladığında;

- Animator bileşenini kod ile kontrol edebilirsin.
- Animator parametrelerini kullanabilirsin.
- Animation Event ekleyebilirsin.
- Root Motion yönetebilirsin.
- State Machine davranışlarını anlayabilirsin.
- Kod ile animasyon geçişleri oluşturabilirsin.

---

# 🎬 Animator Component

Unity'de tüm animasyonlar **Animator** bileşeni üzerinden yönetilir.

Görevleri

- Animation Clip oynatır.
- State Machine yönetir.
- Parametreleri kontrol eder.
- Blend Tree çalıştırır.
- Animation Event tetikler.

---

# 🧩 Animator'a Koddan Erişim

```csharp
using UnityEngine;

public class PlayerAnimation : MonoBehaviour
{
    Animator animator;

    void Start()
    {
        animator = GetComponent<Animator>();
    }
}
```

---

# 🎛 Bool Parametresi

```csharp
animator.SetBool("isRunning", true);
```

Karakter koşmaya başlar.

---

# 🎯 Trigger Parametresi

```csharp
animator.SetTrigger("Attack");
```

Saldırı animasyonu bir kez oynatılır.

---

# 🔢 Float Parametresi

```csharp
animator.SetFloat("Speed", speed);
```

Blend Tree içerisinde hız kontrolü yapılır.

---

# 🔢 Integer Parametresi

```csharp
animator.SetInteger("Weapon",2);
```

Silah değişim animasyonlarında kullanılır.

---

# ▶ Animator.Play()

Belirli bir animasyonu doğrudan oynatır.

```csharp
animator.Play("Jump");
```

---

# 🔄 CrossFade()

Animasyonlar arasında yumuşak geçiş sağlar.

```csharp
animator.CrossFade("Run",0.25f);
```

---

# ⏸ Animator Speed

Animasyon hızını değiştirebiliriz.

```csharp
animator.speed = 2;
```

Animasyon iki kat hızlı oynar.

---

# 🎯 Animation Event

Animation Event sayesinde animasyon sırasında kod çalıştırılır.

Örneğin

Attack animasyonunun ortasında

↓

```csharp
DealDamage();
```

fonksiyonu çağrılır.

---

# 🦶 Root Motion

Kod yerine hareket animasyondan gelir.

Avantajları

- Daha doğal yürüyüş
- Daha gerçekçi dönüşler

Dezavantajları

- Fizik sistemiyle dikkatli kullanılmalıdır.

---

# 🎭 State Machine Behaviour

Unity'de her State'e özel script yazılabilir.

Örneğin

Idle

↓

OnStateEnter()

↓

OnStateUpdate()

↓

OnStateExit()

fonksiyonları çalışır.

---

# ⚙ StateMachineBehaviour Örneği

```csharp
using UnityEngine;

public class IdleState : StateMachineBehaviour
{
    public override void OnStateEnter(
        Animator animator,
        AnimatorStateInfo stateInfo,
        int layerIndex)
    {
        Debug.Log("Idle başladı.");
    }
}
```

---

# 🎮 Input ile Animasyon

```csharp
float move = Input.GetAxis("Vertical");

animator.SetFloat("Speed",Mathf.Abs(move));
```

Oyuncu hareket ettikçe animasyon değişir.

---

# 💥 Attack Sistemi

```csharp
if(Input.GetMouseButtonDown(0))
{
    animator.SetTrigger("Attack");
}
```

---

# ⚡ Animation Layer

Bir karakter aynı anda farklı animasyonlar oynatabilir.

Örneğin

Alt gövde

↓

Koşma

Üst gövde

↓

Silah ateşi

---

# 🧠 Avatar Mask

Animation Layer ile birlikte kullanılır.

Sadece belirli kemiklerin animasyonunu oynatır.

Örneğin

Sadece

- Kollar

veya

- Üst gövde

---

# 💡 Best Practices

✅ Blend Tree kullan.

✅ Trigger'ları gereksiz kullanma.

✅ Animator geçişlerini sade tut.

✅ Parametre isimlerini anlamlı seç.

✅ Gereksiz State oluşturma.

---

# ⚠ Yaygın Hatalar

❌ Çok fazla Trigger kullanmak.

❌ Geçiş sürelerini çok uzun yapmak.

❌ Her karede Play() çağırmak.

❌ Kod ile Animator arasında senkronizasyonu bozmak.

---

# 🧪 Unity Lab

## Amaç

Animasyonları kod ile kontrol etmek.

### Görevler

1. Animator ekle.
2. Idle animasyonu oluştur.
3. Run animasyonu oluştur.
4. Attack animasyonu oluştur.
5. Bool parametresi ekle.
6. Trigger parametresi ekle.
7. Kod ile animasyonları kontrol et.
8. Animation Event oluştur.
9. Hasar fonksiyonunu Event ile çağır.

---

# 💼 Interview Questions

- Animator nedir?
- Trigger ile Bool arasındaki fark nedir?
- CrossFade ne işe yarar?
- Root Motion nedir?
- Avatar Mask neden kullanılır?
- Animation Layer nedir?
- StateMachineBehaviour nedir?
- Animation Event nasıl çalışır?

---

# 📚 Ek Kaynaklar

- Unity Learn
- Unity Manual – Animator
- Unity Manual – State Machine Behaviours
- Unity Manual – Avatar Masks
- Unity Manual – Animation Events
- Unity Learn – Character Animation
