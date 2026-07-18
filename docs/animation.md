# 🎬 Animasyon (Animation)

Animasyon, oyun karakterlerine ve nesnelere hareket kazandıran sistemdir. İyi hazırlanmış animasyonlar oyunun daha gerçekçi, akıcı ve etkileyici görünmesini sağlar.

---

# 🎯 Öğrenme Hedefleri

Bu bölümü tamamladığında;

- Animation kavramını açıklayabilirsin.
- Animation Clip oluşturabilirsin.
- Animator Controller kullanabilirsin.
- State Machine mantığını anlayabilirsin.
- Blend Tree oluşturabilirsin.
- Animation Event ekleyebilirsin.
- Root Motion ve Inverse Kinematics (IK) kavramlarını öğrenebilirsin.

---

# 🎮 Animation Nedir?

Animation;

Bir nesnenin veya karakterin zaman içerisinde hareket etmesini sağlayan görsel süreçtir.

Örnekler:

- 🚶 Yürüme
- 🏃 Koşma
- 🤸 Zıplama
- ⚔️ Saldırı
- 💀 Ölme
- 😴 Idle (Boşta Bekleme)

---

# 🎞 Animation Clip

Animation Clip;

Belirli bir hareketi kaydeden dosyadır.

Örneğin;

- Walk.anim
- Run.anim
- Jump.anim
- Attack.anim

Her hareket ayrı bir Animation Clip olarak saklanır.

---

# 🎛 Animator Controller

Animator Controller;

Karakterin hangi animasyonu oynatacağını kontrol eder.

Örneğin

Idle

↓

Walk

↓

Run

↓

Jump

↓

Attack

Bu geçişleri yönetir.

---

# 🔄 State Machine

Animator Controller içinde kullanılan mantıktır.

Her animasyon bir State olarak tanımlanır.

Örneğin

Idle

↓

Walk

↓

Run

↓

Jump

↓

Fall

↓

Attack

Geçişler belirli koşullara bağlıdır.

---

# 🎚 Parameters

Animator'da geçişleri kontrol etmek için parametreler kullanılır.

Türleri

- Bool
- Float
- Integer
- Trigger

Örnek

isRunning

↓

true

↓

Run animasyonu oynar.

---

# 🌳 Blend Tree

Blend Tree;

İki veya daha fazla animasyonu yumuşak şekilde birleştirir.

Örneğin

Speed = 0

↓

Idle

Speed = 2

↓

Walk

Speed = 5

↓

Run

Oyuncu hızlandıkça animasyon da doğal şekilde değişir.

---

# 🎯 Animation Event

Animation Event;

Animasyonun belirli bir anında fonksiyon çağırır.

Örnek

Attack animasyonunun 0.45. saniyesinde

↓

Damage()

fonksiyonu çalıştırılır.

---

# 🦶 Root Motion

Root Motion;

Karakterin hareketini animasyonun belirlemesini sağlar.

Avantajları

- Gerçekçi hareket
- Daha doğal yürüyüş
- Daha akıcı dönüşler

---

# 🧍 Inverse Kinematics (IK)

IK;

Karakterin uzuvlarının çevreye uyum sağlamasını sağlar.

Örnekler

- Ayağın merdivene basması
- Elin kapıya uzanması
- Karakterin hedefe bakması

---

# 🦴 Humanoid ve Generic Rig

Unity iki farklı rig sistemi sunar.

## Humanoid

- İnsan karakterleri
- Animation Retargeting desteği
- Avatar sistemi

## Generic

- Robotlar
- Hayvanlar
- Özel yaratıklar

---

# 🔁 Animation Retargeting

Bir karakterin animasyonunu başka karakterlerde kullanabilmeyi sağlar.

Avantajları

- Zaman kazandırır.
- Tek animasyon birçok karakterde kullanılabilir.
- Unity Humanoid sistemiyle kolayca uygulanabilir.

---

# ⚡ Animation Optimization

Animasyon performansını artırmak için:

- Gereksiz keyframe kullanma.
- Sadece gerekli kemikleri animasyona dahil et.
- Animation Compression kullan.
- Culling Mode ayarla.
- Optimize Game Object seçeneğini kullan.

---

# 💡 Best Practices

✅ Blend Tree kullan.

✅ State sayısını gereksiz artırma.

✅ Trigger parametrelerini doğru kullan.

✅ Idle animasyonunu optimize et.

✅ Root Motion'u ihtiyaç olduğunda kullan.

---

# ⚠️ Yaygın Hatalar

❌ Çok fazla Animator Layer oluşturmak.

❌ Gereksiz Transition kullanmak.

❌ Sürekli Loop animasyonu eklemek.

❌ Çok yüksek çözünürlüklü rig kullanmak.

❌ Gereksiz kemik eklemek.

---

# 🧪 Unity Lab

## Amaç

Basit bir karakter animasyon sistemi oluşturmak.

### Görevler

1. Idle animasyonu ekle.
2. Walk animasyonu ekle.
3. Run animasyonu ekle.
4. Animator Controller oluştur.
5. Blend Tree oluştur.
6. Speed parametresi ekle.
7. Input ile karakteri hareket ettir.
8. Animasyon geçişlerini test et.

---

# 💼 Interview Questions

- Animation Clip nedir?
- Animator Controller ne işe yarar?
- Blend Tree nedir?
- Animation Event nasıl çalışır?
- Root Motion nedir?
- IK neden kullanılır?
- Animation Retargeting nedir?
- Humanoid ve Generic Rig arasındaki fark nedir?

---

# 📚 Ek Kaynaklar

- Unity Learn
- Unity Manual – Animation
- Unity Manual – Animator Controller
- Unity Manual – Blend Trees
- Unity Manual – Animation Rigging
