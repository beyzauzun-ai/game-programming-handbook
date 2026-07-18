# ⚡ Performans Optimizasyonu (Performance Optimization)

Performans optimizasyonu, bir oyunun daha akıcı çalışmasını sağlamak ve donanım kaynaklarını verimli kullanmak için uygulanan tekniklerin bütünüdür. İyi optimize edilmiş bir oyun daha yüksek FPS, daha kısa yükleme süreleri ve daha iyi bir oyuncu deneyimi sunar.

---

# 🎯 Öğrenme Hedefleri

Bu bölümü tamamladığında;

- Unity Profiler kullanabilirsin.
- Performans darboğazlarını belirleyebilirsin.
- Draw Call kavramını açıklayabilirsin.
- GPU Instancing ve LOD sistemlerini anlayabilirsin.
- Occlusion Culling ve Asset Streaming kullanmanın amacını öğrenebilirsin.
- Bellek kullanımını analiz edebilirsin.

---

# 🚀 Performans Nedir?

Bir oyunun performansı;

- FPS (Frames Per Second)
- CPU Kullanımı
- GPU Kullanımı
- Bellek Kullanımı (RAM)
- Yükleme Süresi

gibi metriklerle değerlendirilir.

Yüksek performans, daha akıcı ve daha stabil bir oyun deneyimi sağlar.

---

# 📊 Unity Profiler

Unity Profiler, oyunun hangi sistemlerinin ne kadar kaynak kullandığını gösteren analiz aracıdır.

Profiler ile izlenebilen başlıca alanlar:

- CPU Usage
- GPU Usage
- Rendering
- Memory
- Physics
- Audio
- Animation

Profiler sayesinde performans sorunlarının kaynağı kolayca bulunabilir.

---

# 🎨 Render Optimizasyonu

Render işlemi ekranın her karede yeniden çizilmesidir.

Performansı artırmak için:

- Gereksiz ışıkları kaldır.
- Gereksiz gölgeleri kapat.
- Şeffaf materyalleri dikkatli kullan.
- UI elemanlarını optimize et.

---

# 🎯 Draw Call

Her nesnenin GPU'ya çizim isteği göndermesine Draw Call denir.

Çok fazla Draw Call;

- FPS düşüşüne
- CPU yükünün artmasına
- Daha uzun render sürelerine

neden olabilir.

Draw Call sayısını azaltmak performansı artırır.

---

# 🖥 GPU Instancing

GPU Instancing, aynı modelin birçok kez çizilmesini tek bir işlem hâline getirir.

Örnek:

- Ağaçlar
- Çimenler
- Taşlar
- Sokak lambaları

Avantajları:

- Daha az Draw Call
- Daha yüksek FPS
- Daha düşük CPU yükü

---

# 🌄 Level of Detail (LOD)

LOD sistemi, nesnenin kameraya uzaklığına göre farklı detay seviyeleri kullanır.

Örnek:

| Mesafe | Model |
|---------|-------|
| Yakın | High Poly |
| Orta | Medium Poly |
| Uzak | Low Poly |

Bu yöntem gereksiz grafik hesaplamalarını azaltır.

---

# 👁 Occlusion Culling

Kameranın göremediği nesnelerin çizilmesini engeller.

Örneğin:

- Duvar arkasındaki objeler
- Bina içindeki nesneler
- Görüş alanı dışındaki modeller

Avantajı:

- Gereksiz render işlemleri azalır.
- FPS artar.

---

# 📦 Asset Streaming

Tüm assetleri aynı anda belleğe yüklemek yerine yalnızca ihtiyaç duyulan içerikler yüklenir.

Kullanım alanları:

- Açık dünya oyunları
- Büyük haritalar
- RPG oyunları

Avantajları:

- Daha düşük RAM kullanımı
- Daha hızlı yükleme
- Daha akıcı geçişler

---

# 🧠 Bellek Profilleme (Memory Profiling)

Bellek kullanımını analiz etmek için kullanılır.

Kontrol edilen alanlar:

- Texture
- Mesh
- Audio
- Script
- Garbage Collection (GC)

Bellek sızıntılarını (Memory Leak) tespit etmek için önemlidir.

---

# 🖥 Platforma Özgü Optimizasyon

Her platform farklı donanım özelliklerine sahiptir.

Örnekler:

- Mobil cihazlarda daha düşük çözünürlük
- PC'de yüksek grafik ayarları
- Konsollarda sabit FPS hedefi

Her platform için ayrı optimizasyon yapılmalıdır.

---

# 📦 Build Optimizasyonu

Oyunun son paketini küçültmek ve daha hızlı çalışmasını sağlamak için uygulanır.

Yöntemler:

- Kullanılmayan assetleri kaldır.
- Sıkıştırma (Compression) kullan.
- Gereksiz paketleri çıkar.
- Build ayarlarını optimize et.

---

# 💾 Bellek Optimizasyonu

Bellek kullanımını azaltmak için:

- Object Pooling kullan.
- Gereksiz Instantiate işlemlerinden kaçın.
- Kullanılmayan nesneleri temizle.
- Büyük Texture'ları sıkıştır.
- Gereksiz referansları kaldır.

---

# 🎮 Unity'de Kullanımı

Unity Profiler açmak için:

```
Window
 → Analysis
     → Profiler
```

Buradan CPU, GPU, Memory ve Rendering sekmeleri incelenebilir.

---

# 💡 Best Practices

✅ Profiler'ı düzenli kullan.

✅ Object Pooling uygula.

✅ LOD sistemini kullan.

✅ Draw Call sayısını azalt.

✅ Occlusion Culling etkinleştir.

✅ Asset Streaming kullan.

---

# ⚠️ Yaygın Hatalar

❌ Çok büyük Texture kullanmak.

❌ Her kare Instantiate yapmak.

❌ Gereksiz Update() fonksiyonları yazmak.

❌ Kullanılmayan Assetleri Build'e dahil etmek.

❌ Profiler kullanmadan optimizasyon yapmaya çalışmak.

---

# 🧪 Unity Lab

## Amaç

Basit bir sahneyi optimize etmek.

### Görevler

1. 100 Cube oluştur.
2. FPS değerini ölç.
3. GPU Instancing etkinleştir.
4. LOD Group ekle.
5. Occlusion Culling'i etkinleştir.
6. Profiler ile CPU ve GPU kullanımını karşılaştır.
7. Sonuçları not al.

---

# 💼 Interview Questions

- Unity Profiler ne işe yarar?
- Draw Call nedir?
- GPU Instancing nasıl çalışır?
- LOD sistemi neden kullanılır?
- Occlusion Culling nedir?
- Memory Leak nasıl tespit edilir?
- Object Pooling neden performansı artırır?
- Asset Streaming hangi projelerde tercih edilir?

---

# 📚 Ek Kaynaklar

- Unity Learn – Performance Optimization
- Unity Manual – Profiler
- Unity Manual – GPU Instancing
- Unity Manual – LOD Group
- Unity Manual – Occlusion Culling
- Unity Manual – Memory Profiler
