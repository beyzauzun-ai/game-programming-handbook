# 🎨 Oyun Varlıkları (Game Assets)

Game Assets (Oyun Varlıkları), bir oyunun görsel, işitsel ve etkileşimli tüm içeriklerini ifade eder. Oyuncunun gördüğü, duyduğu ve etkileşim kurduğu her şey bir asset olarak değerlendirilir.

---

# 🎯 Öğrenme Hedefleri

Bu bölümü tamamladığında;

- Game Asset kavramını açıklayabilirsin.
- Asset türlerini ayırt edebilirsin.
- 2D ve 3D asset farklarını öğrenebilirsin.
- Texture, Material ve Shader kavramlarını açıklayabilirsin.
- Rigging ve Skinning süreçlerini anlayabilirsin.
- Asset optimizasyon tekniklerini uygulayabilirsin.

---

# 🎮 Game Asset Nedir?

Game Asset;

- Karakterler
- Silahlar
- Araçlar
- Binalar
- Ses efektleri
- Müzikler
- UI ikonları
- Animasyonlar
- Partiküller

gibi oyunda kullanılan tüm içeriklerdir.

---

# 📦 Asset Türleri

En yaygın asset türleri:

- 🎨 2D Sprite
- 🧱 3D Model
- 🖼 Texture
- 🎨 Material
- 🌈 Shader
- 🔊 Sound Effects
- 🎵 Music
- 🎬 Animation
- 💥 Particle Effects
- 🖥 UI Assets

---

# 🖼 2D ve 3D Asset

## 2D

Örnekler:

- Platform oyunları
- Mobil oyunlar
- Pixel Art

Avantajları

- Daha düşük sistem gereksinimi
- Daha kolay üretim
- Daha hızlı geliştirme

---

## 3D

Örnekler

- FPS
- RPG
- Simülasyon
- Açık dünya oyunları

Avantajları

- Daha gerçekçi görünüm
- Gelişmiş kamera sistemi
- Daha fazla etkileşim

---

# 🎨 Texture

Texture, 3D modele uygulanan görsel kaplamadır.

Örneğin

- Ahşap görünümü
- Taş yüzeyi
- Metal
- Kumaş

Texture olmadan modeller düz görünür.

---

# 🧱 Material

Material;

Modelin nasıl görüneceğini belirler.

Özellikleri

- Renk
- Parlaklık
- Metalik yapı
- Saydamlık
- Emission

Unity'de her Renderer bir Material kullanır.

---

# 🌈 Shader

Shader, ekran kartına modelin nasıl çizileceğini söyleyen programdır.

Görevleri

- Işık hesaplamaları
- Gölgelendirme
- Yansıma
- Transparanlık
- Özel efektler

---

# 🦴 Rigging

Rigging;

3D karaktere kemik sistemi ekleme işlemidir.

Örneğin

İnsan modeli

↓

İskelet

↓

Animasyon

---

# 🧍 Skinning

Skinning;

Modelin kemiklerle birlikte doğal hareket etmesini sağlar.

Örneğin

Kol kemiği döndüğünde

↓

Kol modeli de döner.

---

# 🎬 Animasyon Assetleri

Animasyonlar;

- Yürüme
- Koşma
- Zıplama
- Saldırı
- Ölme
- Idle

gibi hareketlerden oluşur.

---

# 🎵 Ses Assetleri

Ses türleri

- Arka plan müziği
- UI sesleri
- Silah sesleri
- Patlama sesleri
- Ortam sesleri
- Karakter sesleri

---

# ✨ Particle Effect

Particle System;

Görsel efektler oluşturur.

Örnekler

- Ateş
- Duman
- Yağmur
- Kar
- Patlama
- Büyü efektleri

Unity'de Particle System bileşeni kullanılır.

---

# ⚡ Asset Optimizasyonu

İyi optimize edilmiş assetler FPS'i artırır.

Yöntemler

- Texture Compression
- LOD
- Atlas Texture
- Mesh Compression
- Occlusion Culling
- GPU Instancing

---

# 🎮 Unity'de Asset Kullanımı

Asset eklemek için

Assets →

Import New Asset

veya

Dosyayı doğrudan Assets klasörüne sürükleyebilirsin.

---

# 💡 Best Practices

✅ Gereksiz büyük texture kullanma.

✅ PNG ve JPG formatlarını doğru seç.

✅ Aynı materialleri tekrar kullan.

✅ Asset isimlendirmelerini düzenli yap.

✅ Prefab sistemi kullan.

---

# ⚠️ Yaygın Hatalar

❌ Çok yüksek çözünürlüklü texture kullanmak.

❌ Aynı asseti farklı isimlerle çoğaltmak.

❌ Optimize edilmemiş modeller kullanmak.

❌ Gereksiz büyük ses dosyaları eklemek.

❌ Material sayısını gereksiz artırmak.

---

# 🧪 Unity Lab

## Amaç

Projeye yeni bir karakter asseti eklemek.

### Görevler

1. Unity Asset Store'dan ücretsiz bir karakter indir.
2. Projeye import et.
3. Sahneye yerleştir.
4. Material değiştir.
5. Texture değiştir.
6. Prefab oluştur.

---

# 💼 Interview Questions

- Game Asset nedir?
- Texture ile Material arasındaki fark nedir?
- Shader ne işe yarar?
- Rigging nedir?
- Skinning nedir?
- LOD neden kullanılır?
- GPU Instancing nedir?

---

# 📚 Ek Kaynaklar

- Unity Asset Store
- Unity Learn
- Blender Documentation
- Adobe Substance 3D
- Sketchfab
