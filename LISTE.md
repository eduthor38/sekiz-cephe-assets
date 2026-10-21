# Sekiz Cephe – 3D model paketleri

Tüm paketler **CC0 1.0** (kamu malı) lisanslıdır: ticari kullanım serbest, isim vermek zorunlu değil. Her klasörde o paketin `License.txt` dosyası durur. Tüm modeller three.js `GLTFLoader` ile yüklenir; 809 dosyanın hepsi Khronos glTF Validator'dan hatasız geçti.

| Paket | İndirildiği sayfa | Lisans | Model sayısı | Dosya sayısı | Toplam boyut |
|---|---|---|---|---|---|
| Kenney – Tower Defense Kit | https://kenney.nl/assets/tower-defense-kit | CC0 1.0 | 160 GLB | 162 | 5,5 MB |
| Kenney – Car Kit | https://kenney.nl/assets/car-kit | CC0 1.0 | 50 GLB | 52 | 5,4 MB |
| Kenney – Space Kit | https://kenney.nl/assets/space-kit | CC0 1.0 | 153 GLB | 154 | 1,9 MB |
| Kenney – Nature Kit | https://kenney.nl/assets/nature-kit | CC0 1.0 | 329 GLB | 330 | 2,9 MB |
| Quaternius – Toon Shooter Game Kit | https://quaternius.com/packs/toonshootergamekit.html (dosyalar: https://poly.pizza/bundle/Toon-Shooter-Game-Kit-qraiSXoAru) | CC0 1.0 | 73 GLB | 74 | 7,9 MB |
| Quaternius – Animated Mech Pack | https://quaternius.com/packs/animatedmech.html (dosyalar: https://opengameart.org/content/animated-mech-pack) | CC0 1.0 | 4 GLB | 5 | 10,8 MB |
| Quaternius – Sci-Fi Essentials Kit (Standard, ücretsiz sürüm) | https://quaternius.itch.io/sci-fi-essentials-kit | CC0 1.0 | 37 glTF (+37 .bin, 32 doku .png) | 107 | 79,4 MB |
| Ek – Tank modelleri | https://opengameart.org/content/cool-low-poly-tonk ve https://opengameart.org/content/heavy-tankextra-low-poly-rts | CC0 1.0 | 3 GLB | 4 | 0,1 MB |
| **Toplam** | | | **809** | **888** | **116 MB** |

Dosya sayısına `License.txt` dahildir.

## Klasörler

```
assets/kenney/tower-defense-kit/   *.glb + Textures/colormap.png (GLB'ler bu dokuyu dışarıdan okur, klasörü birlikte taşıyın)
assets/kenney/car-kit/             *.glb + Textures/colormap.png (aynı şekilde)
assets/kenney/space-kit/           *.glb
assets/kenney/nature-kit/          *.glb
assets/quaternius/toon-shooter-game-kit/   *.glb (Character_Soldier / Character_Enemy / Character_Hazmat animasyonlu)
assets/quaternius/animated-mech-pack/      George.glb, Leela.glb, Mike.glb, Stan.glb (her biri 36–40 animasyon)
assets/quaternius/sci-fi-essentials-kit/   *.gltf + *.bin + T_*.png (üçü aynı klasörde kalmalı)
assets/extra/tank/cool-low-poly-tonk/      tankbase.glb + turret.glb (gövde ve taret ayrı dosya, taret ayrıca döndürülebilir)
assets/extra/tank/heavy-tank-rts/          heavy_tank00.glb ("chassis" ve "turret" düğümleri ayrı)
```

## Paketlere yapılan değişiklikler

- **Animated Mech Pack:** Quaternius'un Google Drive bağlantısı indirme kotası dolduğu için açılmadı. Aynı paketi Quaternius OpenGameArt'a da yüklemiş, ancak o sürümde glTF yok (yalnızca FBX/OBJ/Blend). Dört FBX dosyası FBX2glTF v0.13.1 ile GLB'ye çevrildi. Paketin kendi doku PNG'si (`*_Texture.png`) her GLB'nin içine gömüldü, çünkü FBX'teki malzemede doku bağlantısı yoktu. Glb'deki isteğe bağlı `skin.skeleton` alanı silindi, çünkü dönüştürücü bu alana hatalı değer yazıyor. Animasyonlar (Idle, Walk, Shoot, Death vb.) korundu.
- **Toon Shooter Game Kit:** Google Drive aynı nedenle açılmadı. Dosyalar Quaternius'un kendi poly.pizza hesabındaki aynı paketten GLB olarak alındı; orada her modelin lisansı ayrıca "CC0 1.0" olarak yazılı. Bu kopyada 73 model var. Drive'daki sürümde 74 model görünüyor (3 karakter, 55 çevre, 16 silah), aradaki bir model poly.pizza'da yok. Aynı adlı modeller `_2`, `_3` diye numaralandı. Paket lisans dosyasıyla gelmediği için `License.txt` resmi sayfadaki lisansa göre yazıldı.
- **Kenney Space Kit ve Nature Kit:** Bu iki eski kitin GLB'lerinde sahnede listelenen düğüm aynı zamanda boş bir `tmpParent` düğümünün çocuğu olarak da yazılmış (glTF kuralına aykırı). Bu bağ kaldırıldı. `tmpParent`'ın dönüşümü sıfır olduğu için görünüm değişmedi, three.js zaten bu şekilde gösteriyordu.
- **Sci-Fi Essentials Kit:** Paketin lisans dosyasının adı `License_Standard.txt`; içeriği değiştirilmeden `License.txt` adıyla kondu. Pro ve Source sürümleri ücretli olduğu için alınmadı.
- **Tank:** İki model de OpenGameArt'tan, ikisi de CC0. Paketler lisans dosyasıyla gelmediği için `License.txt` sayfalardaki lisansa ve yazar adlarına göre yazıldı.
