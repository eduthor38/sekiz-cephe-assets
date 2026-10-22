# Sekiz Cephe – 3D model paketleri

İki bölüm var. **Bölüm 1** (Kenney, Quaternius, ek tanklar) **CC0 1.0** lisanslıdır: ticari kullanım serbest, isim vermek zorunlu değil. **Bölüm 2** (Sketchfab'dan gerçekçi modeller) **CC BY 4.0** lisanslıdır: ticari kullanım serbest, yapımcı adı jenerikte yazılmalı; liste `KAYNAK.md` dosyasında. Her klasörde o paketin `License.txt` dosyası durur. Tüm modeller three.js `GLTFLoader` ile yüklenir; 809 dosyanın hepsi Khronos glTF Validator'dan hatasız geçti.

## Bölüm 1: CC0 paketleri

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

## Bölüm 2: Gerçekçi modeller (Sketchfab, CC BY 4.0)

Arama ölçütleri: gerçekçi dokulu, "game ready / low poly"; araç ≤15.000, bina ve çevre ≤25.000, piyade ≤10.000 üçgen. Hepsi Sketchfab'ın kendi GLB çıktısı (dokular içine gömülü, en büyüğü 1024 px). Her klasörde `model.glb` ve modelin adı, yapımcısı, bağlantısı, lisansı ve üçgen sayısını taşıyan `meta.json` durur. **NonCommercial, NoDerivatives, ShareAlike ya da Editorial lisanslı model yoktur;** 33 modelin hepsi indirme anında Sketchfab API'sinden lisansı yeniden okunarak CC BY olduğu doğrulandı. Oyun dosyasından kopyalandığı anlaşılan modeller (PUBG, Halo, Twisted Metal, War Thunder vb.) lisansı CC BY yazsa da alınmadı.

| Birim | Model | Yapımcı | Lisans | Üçgen | Boyut | Klasör |
|---|---|---|---|---|---|---|
| Demir · Mızrak (ana tank) | [M1A2](https://sketchfab.com/3d-models/m1a2-ace49544572f4ee1aa5382027781853e) | Usman Zia | CC Attribution | 4.896 | 3.2 MB | `assets/fab/demir/mizrak/` |
| Demir · Gürz (topçu) | [K9 THUNDER ARTILLERY](https://sketchfab.com/3d-models/k9-thunder-artillery-dda88d1dc5b34f1e95507ae848642d8a) | Muhamad Mirza Arrafi | CC Attribution | 6.898 | 1.6 MB | `assets/fab/demir/gurz/` |
| Demir · Kazıcı (maden toplayıcı) | [Bulldozer Photogrammetry](https://sketchfab.com/3d-models/bulldozer-photogrammetry-baa53594134f4a4f99d96ce4ba25492e) | bertanbaday | CC Attribution | 4.562 | 0.6 MB | `assets/fab/demir/kazici/` |
| Demir · Kurt (keşif cipi) | [Low Poly Humvee FREE](https://sketchfab.com/3d-models/low-poly-humvee-free-c0e2ddcc4ccf4d49a9303303a6307bcf) | MadTrollStudio | CC Attribution | 8.148 | 0.6 MB | `assets/fab/demir/kurt/` |
| Demir · Şahin (helikopter) | [Mi-24 Hind](https://sketchfab.com/3d-models/mi-24-hind-004d68143e1a4df88e136dbc0a05f181) | Duane's Mind | CC Attribution | 4.237 | 1.6 MB | `assets/fab/demir/sahin/` |
| Kum · Çakal (taretli kamyonet) | [Cybertruck civil war](https://sketchfab.com/3d-models/cybertruck-civil-war-35c041fb856341f2bf05cf6cefbe95f7) | pasquill | CC Attribution | 11.748 | 9.3 MB | `assets/fab/kum/cakal/` |
| Kum · Kum Roketi | [Shaanxi SX2190 Missile Launcher](https://sketchfab.com/3d-models/shaanxi-sx2190-missile-launcher-a3cb343f3bf8486c8a0482df5b753c38) | Muhamad Mirza Arrafi | CC Attribution | 11.008 | 2.6 MB | `assets/fab/kum/kum-roketi/` |
| Kum · Rüzgar (hızlı keşif) | [Post-Apocalyptic Pobeda (sub 10k triangles)](https://sketchfab.com/3d-models/post-apocalyptic-pobeda-sub-10k-triangles-9985b2fa9e634ecbba5210ceaab592d6) | Jorma Rysky | CC Attribution | 8.610 | 2.6 MB | `assets/fab/kum/ruzgar/` |
| Kum · Talan Kamyonu (toplayıcı) | [M978 HEMTT](https://sketchfab.com/3d-models/m978-hemtt-d1a986c5d7f34d9eb027e612502c4874) | 42manako | CC Attribution | 8.477 | 3.9 MB | `assets/fab/kum/talan/` |
| Kum · Akbaba (uçak) | [AV-8B Harrier II](https://sketchfab.com/3d-models/av-8b-harrier-ii-8482e199f18b44f3bede5a5806aa1cb1) | 42manako | CC Attribution | 9.705 | 1.8 MB | `assets/fab/kum/akbaba/` |
| Bina · Sığınak | [Sci-fi Bunker](https://sketchfab.com/3d-models/sci-fi-bunker-2567a460d6cc475fa679e877c78f05d3) | gregwagner | CC Attribution | 17.556 | 13.2 MB | `assets/fab/bina/siginak/` |
| Bina · Hangar (kapıları animasyonlu) | [Military Style Building (with animations)](https://sketchfab.com/3d-models/military-style-building-with-animations-1671685e1dd94b6e9216ead632f08f6e) | TampaJoey | CC Attribution | 16.796 | 40.6 MB | `assets/fab/bina/hangar/` |
| Bina · Modüler üs parçaları | [Military Buildings. Modular Kit Low poly](https://sketchfab.com/3d-models/military-buildings-modular-kit-low-poly-49638018cf5e414a995bd8559ab3d8a4) | Free Models. | CC Attribution | 13.546 | 4.9 MB | `assets/fab/bina/moduler-us/` |
| Bina · Gözetleme kulesi | [Watch tower](https://sketchfab.com/3d-models/watch-tower-042f327a0f4c4fc9bf458903666bb257) | _SeF_ | CC Attribution | 6.122 | 5.3 MB | `assets/fab/bina/gozetleme-kulesi/` |
| Bina · Çadır | [Tent](https://sketchfab.com/3d-models/tent-979c0784868b4fdeb2b4563f65e0b5b4) | VENIKAMEN | CC Attribution | 5.360 | 10.7 MB | `assets/fab/bina/cadir/` |
| Bina · Rafineri (petrol tankları) | [old oil tank .1](https://sketchfab.com/3d-models/old-oil-tank-1-2771d6fa8d2d4582b3d8d551fd83dbcc) | Kwon_Hyuk | CC Attribution | 9.254 | 4.3 MB | `assets/fab/bina/rafineri/` |
| Bina · Kimyasal tank | [Chemical tank](https://sketchfab.com/3d-models/chemical-tank-63c001e74ff5402fbcf1338479c9c0c5) | Mkc | CC Attribution | 8.693 | 2.8 MB | `assets/fab/bina/kimyasal-tank/` |
| Bina · Enerji santrali | [Industrial Utility Building (Game-Ready)](https://sketchfab.com/3d-models/industrial-utility-building-game-ready-2b6d0e1a63dd4f23b48a5c2fa62b71fe) | 𝖝𝖎𝖈𝖔𝖗 𝖉𝖊𝖛𝖘𝖙𝖆𝖗 ♕ | CC Attribution | 13.588 | 18.3 MB | `assets/fab/bina/enerji-santrali/` |
| Bina · Çöl karakolu (terk edilmiş yapı) | [Abandoned \| Building \| Shop \| Old \| House](https://sketchfab.com/3d-models/abandoned-building-shop-old-house-0ed14367314946b298d9a58db66da040) | YadroGames | CC Attribution | 12.792 | 33.5 MB | `assets/fab/bina/col-karakolu/` |
| Bina · Radar istasyonu | [RLS P-35](https://sketchfab.com/3d-models/rls-p-35-7cabcbaabd5045309532876d8e53804c) | manyakasia | CC Attribution | 10.885 | 4.9 MB | `assets/fab/bina/radar/` |
| Çevre · Çöl kayalığı | [Desert Cliff 6](https://sketchfab.com/3d-models/desert-cliff-6-ed2e9c7e976e4768868481e4a5c63f6f) | WireframeArt | CC Attribution | 13.921 | 4.7 MB | `assets/fab/cevre/col-kayaliklari/` |
| Çevre · Çöl taşı paketi | [Desert \| Rocks \| Stones \| Pack](https://sketchfab.com/3d-models/desert-rocks-stones-pack-c2208f5ccc004f1681d27de67fe75799) | YadroGames | CC Attribution | 13.777 | 12.4 MB | `assets/fab/cevre/col-tasi-paketi/` |
| Çevre · Kuru ağaç | [Old tree](https://sketchfab.com/3d-models/old-tree-3cb4d59eb4844dc4802480e9ee53785e) | evolveduk | CC Attribution | 8.107 | 7.8 MB | `assets/fab/cevre/kuru-agac/` |
| Çevre · Sandık ve varil | [Crates And Barrels](https://sketchfab.com/3d-models/crates-and-barrels-5ae3c72285474862a89d69c2f2ad2246) | SpatialNeglect | CC Attribution | 7.509 | 15.0 MB | `assets/fab/cevre/sandik-varil/` |
| Çevre · Kargo sandığı | [Cargo Crate](https://sketchfab.com/3d-models/cargo-crate-19a32159a3d6443e95105f4f7cb51c39) | boysichterman | CC Attribution | 1.367 | 2.9 MB | `assets/fab/cevre/kargo-sandigi/` |
| Çevre · Silah konteyneri | [Military Weapons Container](https://sketchfab.com/3d-models/military-weapons-container-8a1c32f395f549b8b22265b8a459fa8e) | MeshSlinger | CC Attribution | 9.964 | 4.1 MB | `assets/fab/cevre/silah-konteyneri/` |
| Çevre · Hesco siper | [Hesco Barrier PBR](https://sketchfab.com/3d-models/hesco-barrier-pbr-ab21217481094e9a84f989e71fd56a59) | polbrainstorm | CC Attribution | 6.956 | 4.1 MB | `assets/fab/cevre/hesco/` |
| Çevre · Beton bariyer | [Concrete Barriers](https://sketchfab.com/3d-models/concrete-barriers-96f1e7a248a44137b5943c0fb57c36a8) | Arsen Ismailov | CC Attribution | 5.494 | 25.8 MB | `assets/fab/cevre/beton-bariyer/` |
| Çevre · Yanık araba enkazı | [Burned-out Cars](https://sketchfab.com/3d-models/burned-out-cars-701066df6b914fd08318524c7ccd96a7) | Renafox | CC Attribution | 3.451 | 11.3 MB | `assets/fab/cevre/yanik-arabalar/` |
| Çevre · Kum torbası | [Sandbags](https://sketchfab.com/3d-models/sandbags-8cda4370170746d393aa311a7c080c50) | Evan | CC Attribution | 5.824 | 4.3 MB | `assets/fab/cevre/kum-torbasi/` |
| Piyade · Fütüristik asker | [Futuristic soldier (lowpoly)](https://sketchfab.com/3d-models/futuristic-soldier-lowpoly-5ebade1ccbff4adb91ddd3a4d1fcd541) | SlagPerch 3D | CC Attribution | 2.004 | 3.0 MB | `assets/piyade/futuristic-soldier/` |
| Piyade · Gece görüşlü özel kuvvet | [PS1/Low Poly Night Vision Special Forces Soldier](https://sketchfab.com/3d-models/ps1low-poly-night-vision-special-forces-soldier-afb42573fa5f4fd2af09c9929d9ccd93) | Jellypack | CC Attribution | 1.010 | 0.3 MB | `assets/piyade/night-vision-sf/` |
| Piyade · Asker | [Low Poly Soldier -Free](https://sketchfab.com/3d-models/low-poly-soldier-free-739772a9b0f14feeb4a4f1b45dadf4e3) | manoeldarochadeoliveira | CC Attribution | 1.432 | 1.6 MB | `assets/piyade/low-poly-soldier/` |

### Bilinmesi gerekenler

- **Kule ve namlu:** Mızrak (M1A2) modelinde `turret` (kule), `Main Cannon` (namlu) ve iki makineli tüfek ayrı düğüm, döndürülebilir. **Gürz (K9) modelinde kule gövdeyle aynı parçada;** Sketchfab'da kulesi ayrı, uygun lisanslı bir topçu aracı bulunamadı. Çakal'da makineli tüfek, Kum Roketi'nde füze ayrı parça.
- **Hangar:** kapıları ve kepenkleri animasyonlu (`Front_Door`, `Blast_Shutters`, `Blast_Doors`, `Garage_Door`). Şahin'de rotor ve tekerlek animasyonu var.
- **Piyade:** Mixamo, Adobe koşulları ham dosyanın herkese açık depoda paylaşılmasına izin vermediği için kullanılmadı. Yerine CC BY animasyonlu üç asker alındı. Fütüristik askerde `Idle`, `Rifle_run`, `Rifle_stand`, `Rifle_crouch`, `Crouch`, `Run`, `Walk` var; **ateş etme ve ölme animasyonu hiçbirinde yok.** Kadın asker bulunamadı.
- **Bulunamayan:** petrol kulesi (tek aday CC BY-SA, alınmadı).
- **Kurt (Humvee)** tek renk paletli küçük bir doku kullanıyor (64 px); ötekilerden daha düz görünür.
- **Fab** modelleri alınmadı: Fab Standard License ham dosyanın herkese açık depoda paylaşılmasını yasaklıyor.

