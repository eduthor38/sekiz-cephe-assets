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

Arama ölçütleri: gerçekçi dokulu, "game ready / low poly"; araç ≤15.000, bina ve çevre ≤25.000, piyade ≤10.000 üçgen. Hepsi Sketchfab'ın kendi GLB çıktısı (dokular içine gömülü, en büyüğü 1024 px). Her klasörde `model.glb` ve modelin adı, yapımcısı, bağlantısı, lisansı ve üçgen sayısını taşıyan `meta.json` durur. **NonCommercial, NoDerivatives, ShareAlike ya da Editorial lisanslı model yoktur;** 33 modelin hepsi indirme anında Sketchfab API'sinden lisansı yeniden okunarak CC BY olduğu doğrulandı. Oyun dosyasından kopyalandığı anlaşılan modeller (PUBG, Halo, Twisted Metal, War Thunder vb.) lisansı CC BY yazsa da alınmadı. Her modelin Sketchfab açıklaması ve etiketleri ayrıca okundu: "ripped", "not my model" gibi ifade taşıyan iki model (42manako'nun M978 HEMTT ve AV-8B Harrier II modelleri) çıkarıldı, yerlerine Ural 4320 ve SU-57 kondu.

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
| Kum · Talan Kamyonu (toplayıcı) | [Ural 4320](https://sketchfab.com/3d-models/ural-4320-f953c51a5dbc4a15949f4dcc0905c4e8) | Brout | CC Attribution | 8.492 | 1.9 MB | `assets/fab/kum/talan/` |
| Kum · Akbaba (uçak) | [Low poly SU-57](https://sketchfab.com/3d-models/low-poly-su-57-b9031bc2e94947b18812ce0eca6b8345) | SIpriv | CC Attribution | 5.918 | 0.5 MB | `assets/fab/kum/akbaba/` |
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
- **Kum Roketi (Shaanxi SX2190)** yapımcısının etiketine göre yapay zekâ yardımıyla üretilmiş ("createdwithai"). Lisans CC BY; ileride elle yapılmış bir modelle değiştirilebilir.
- **Fab** modelleri alınmadı: Fab Standard License ham dosyanın herkese açık depoda paylaşılmasını yasaklıyor.

## Bölüm 3: Ülke uçakları ve tankları (Sketchfab, CC BY 4.0)

Gerçek ülkelerin silahları için ayrı klasör: `assets/ulke/<ülke>/<model>/`. Bölüm 2'deki gibi her birinin açıklaması okundu, kopya ya da yapay zekâ işareti olmayanlar alındı. Rusya'nın SU-57'si Bölüm 2'de (`assets/fab/kum/akbaba/`).

| Birim | Model | Yapımcı | Lisans | Üçgen | Boyut | Klasör |
|---|---|---|---|---|---|---|
| Türkiye · KAAN | [TF-X KAAN](https://sketchfab.com/3d-models/tf-x-kaan-eb2575b139554e1985b139f9943f42d4) | SB-129 | CC Attribution | 3.503 | 1.4 MB | `assets/ulke/turkiye/kaan/` |
| Türkiye · Bayraktar TB2 (SİHA) | [Baykar Bayraktar TB2](https://sketchfab.com/3d-models/baykar-bayraktar-tb2-8e5b6972f7d049f19688096e03949487) | TheDevilsEye | CC Attribution | 9.300 | 2.3 MB | `assets/ulke/turkiye/bayraktar-tb2/` |
| ABD · F-35 | [Low poly F-35 Lightning II](https://sketchfab.com/3d-models/low-poly-f-35-lightning-ii-561b5c56fbf94636a465f998e9af1224) | SIpriv | CC Attribution | 7.689 | 0.6 MB | `assets/ulke/abd/f-35/` |
| ABD · F-22 | [Low poly F22 Raptor](https://sketchfab.com/3d-models/low-poly-f22-raptor-6a6014b7c88745fb94e7dfa1c015cc55) | SIpriv | CC Attribution | 7.786 | 0.6 MB | `assets/ulke/abd/f-22/` |
| ABD · F-16 | [F-16 Fighter Jet](https://sketchfab.com/3d-models/f-16-fighter-jet-d84491f443384ee488593cc6f0f0839e) | iedalton | CC Attribution | 4.214 | 0.3 MB | `assets/ulke/abd/f-16/` |
| Rusya · Su-35 | [Su35](https://sketchfab.com/3d-models/su35-8affd5d4f56f4d9190da55b4579bc46a) | _Muzaev | CC Attribution | 11.324 | 0.6 MB | `assets/ulke/rusya/su-35/` |
| Rusya · Hava savunma radarı (1S91. Kub sistemi) | [1S91 “Straight Flush”Low Poly](https://sketchfab.com/3d-models/1s91-straight-flushlow-poly-fbc875a89b5146f592ae91e8bec191f0) | Rhine_Lab_Muelsyse | CC Attribution | 4.610 | 0.8 MB | `assets/ulke/rusya/hava-savunma-radari/` |
| Çin · J-20 | [J-20 Stealth Fighter Aircraft](https://sketchfab.com/3d-models/j-20-stealth-fighter-aircraft-74e1222399f94dc28416fd02edd98938) | Void | CC Attribution | 15.539 | 6.9 MB | `assets/ulke/cin/j-20/` |
| Çin · J-35 | [Shenyang J-35](https://sketchfab.com/3d-models/shenyang-j-35-37085f458d7943cd8314372af76e0f67) | SB-129 | CC Attribution | 8.235 | 1.8 MB | `assets/ulke/cin/j-35/` |
| Çin · J-16 | [Shenyang J16 "Hidden Dragon"](https://sketchfab.com/3d-models/shenyang-j16-hidden-dragon-2b950f910677457fbb52b6096f81e70b) | andertan | CC Attribution | 14.442 | 1.1 MB | `assets/ulke/cin/j-16/` |
| Çin · Type 99 (ana tank) | [Type 99 MBT](https://sketchfab.com/3d-models/type-99-mbt-7075c92c5ef1408497f1530703ff2942) | philano | CC Attribution | 12.523 | 1.8 MB | `assets/ulke/cin/type-99/` |

### Bilinmesi gerekenler

- **Aynı yapımcıdan, aynı tarzda:** F-35, F-22 ve SU-57 (S1Priv); KAAN ve J-35 (hrd4588).
- **Hareketli parçalar:** F-35'te iniş takımı ve gaz animasyonu, F-22'de iniş takımı ve silah kapağı animasyonu var.
- **F-16 (iedalton)** dokusuz, düz renkli malzemeyle boyalı; ötekilerden sade görünür.
- **Su-35** dokusu küçük (256 px).
- **Type 99 tankının kulesi gövdeyle aynı parçada.**
- **J-20 (Void.com)** açıklamasız yüklenmiş; kopya işareti yok ama yapımcısı hakkında bilgi de yok.
- **Bayraktar TB2:** asıl yapımcı TheDevilsEye'ın modeli alındı. 42manako, Hirohito10020 ve teacherap123'ün aynı üçgen sayılı (9.300) kopyaları alınmadı.
- **Bulunamayan ya da elenen:** Patriot ve S-300/S-400 (Sketchfab'daki adaylar War Thunder'dan kopya ya da Battlefield'dan; CGTrader, TurboSquid, RenderHub ve Superhive'dakiler ücretli ya da "Editorial" lisanslı), HQ-9 ve J-7 ("not my model"), Altay tankı, Hisar ve Siper (lisansı uygun model yok). Rusya için T-90M ve Pantsir adayları dokusuz beyaz olduğu için alınmadı; hava savunması olarak 1S91 radar aracı kondu.

## Bölüm 4: Ek binalar (Sketchfab, CC BY 4.0)

Askerî, sanayi, çöl ve Orta Doğu, harabe ve şehir binaları: `assets/bina/<ad>/`. Hepsinin açıklaması kopya, yapay zekâ ve üçüncü taraf doku işaretine karşı tarandı. Bazıları 25.000 üçgeni aşıyor (helikopter pisti, şehir harabesi, çöl kasabası, modüler sanayi, fabrika kiti); oyunda kullanmadan önce sadeleştirilmeli.

| Birim | Model | Yapımcı | Lisans | Üçgen | Boyut | Klasör |
|---|---|---|---|---|---|---|
| Ahsap ev | [Old \| House \| Wooden \| Enterable \| Rusty](https://sketchfab.com/3d-models/old-house-wooden-enterable-rusty-7f496b3002d24341a618408cb8221e8c) | YadroGames | CC Attribution | 24.246 | 23.6 MB | `assets/bina/ahsap-ev/` |
| Askeri set | [Military Set 01(LowPoly)](https://sketchfab.com/3d-models/military-set-01lowpoly-94b71a3bb3514fb991eccc66b714769f) | numaan.k99 | CC Attribution | 26.626 | 1.6 MB | `assets/bina/askeri-set/` |
| Bes katli bina | [5 storey residential building](https://sketchfab.com/3d-models/5-storey-residential-building-3468ccfd9e35495fb377f7c6d67518ae) | bean(alwayshasbean) | CC Attribution | 518 | 4.2 MB | `assets/bina/bes-katli-bina/` |
| Col binasi | [Low poly desert builing](https://sketchfab.com/3d-models/low-poly-desert-builing-b3179b5b68264806b85441eec1dd8da4) | spicybamer | CC Attribution | 5.040 | 2.0 MB | `assets/bina/col-binasi/` |
| Col citleri | [Fences \| Concretes \| Metal \| Desert \| Old \| Pack](https://sketchfab.com/3d-models/fences-concretes-metal-desert-old-pack-0cbf546419cf499cbabfee3af0916215) | YadroGames | CC Attribution | 2.476 | 16.2 MB | `assets/bina/col-citleri/` |
| Col citleri 2 | [Low \| Fences \| Old \| Rusty \| Desert \| Pack](https://sketchfab.com/3d-models/low-fences-old-rusty-desert-pack-c196e6c907bb44c2ae733de5754e0d3f) | YadroGames | CC Attribution | 3.241 | 58.0 MB | `assets/bina/col-citleri-2/` |
| Col evi | [Desert House 01](https://sketchfab.com/3d-models/desert-house-01-7649a03206864931a3c118ec14d8ac3c) | tori.cane | CC Attribution | 1.642 | 22.3 MB | `assets/bina/col-evi/` |
| Col evleri | [Desert Houses](https://sketchfab.com/3d-models/desert-houses-86153c62aa684ab1a5e0caeaa0450ca2) | Gunnar Correa | CC Attribution | 1.568 | 13.9 MB | `assets/bina/col-evleri/` |
| Col kasabasi | [Desert Town](https://sketchfab.com/3d-models/desert-town-f3a8c925486e45378aef99264f533cd7) | anthwolf | CC Attribution | 49.511 | 48.0 MB | `assets/bina/col-kasabasi/` |
| Col kaya dag paketi | [Sand \| Rock \| Desert \| Mountain \| Pack](https://sketchfab.com/3d-models/sand-rock-desert-mountain-pack-cd6689e6b3034be897761225dd44fa59) | YadroGames | CC Attribution | 28.704 | 22.3 MB | `assets/bina/col-kaya-dag-paketi/` |
| Col koyu | [low poly desert village](https://sketchfab.com/3d-models/low-poly-desert-village-2639191809c4426f8cc0a532ccf8506b) | cubemelongames | CC Attribution | 10.748 | 3.8 MB | `assets/bina/col-koyu/` |
| Depo binasi | [Warehouse Building](https://sketchfab.com/3d-models/warehouse-building-08a4f422bc634033b8023d53beaf8242) | rajibkc | CC Attribution | 3.248 | 2.2 MB | `assets/bina/depo-binasi/` |
| Depo binasi 2 | [Warehouse Building](https://sketchfab.com/3d-models/warehouse-building-0c37b0f92cb54e07a1e1c6c3df9f8439) | OmegaRedZA | CC Attribution | 946 | 4.1 MB | `assets/bina/depo-binasi-2/` |
| Depolama tanklari | [Large Industrial Storage Tanks](https://sketchfab.com/3d-models/large-industrial-storage-tanks-bd3ac97071104b64bc388a155b64f79e) | Duane's Mind | CC Attribution | 9.811 | 11.3 MB | `assets/bina/depolama-tanklari/` |
| Depolar | [Warehouses](https://sketchfab.com/3d-models/warehouses-e6e105d35b3f486292c42ffa52f363c0) | 99.Miles | CC Attribution | 1.930 | 1.5 MB | `assets/bina/depolar/` |
| Eski baraka | [Worn Shed PBR Game-Ready](https://sketchfab.com/3d-models/worn-shed-pbr-game-ready-be6edd62e55a4f9a99da940fc164a5b9) | donnichols | CC Attribution | 2.086 | 13.9 MB | `assets/bina/eski-baraka/` |
| Eski bina | [Old Building](https://sketchfab.com/3d-models/old-building-f72b3723f2a34b6691455947fef598d6) | YadroGames | CC Attribution | 503 | 3.0 MB | `assets/bina/eski-bina/` |
| Fabrika | [Factory 3d model](https://sketchfab.com/3d-models/factory-3d-model-e723f4fe48ec4b9da52ec6e4a442286b) | Ramim Bhai | CC Attribution | 35.230 | 14.0 MB | `assets/bina/fabrika/` |
| Fabrika modular | [Factory Modular kit](https://sketchfab.com/3d-models/factory-modular-kit-3213637ed81d41138c6746a13bf585b9) | Thomas_Crozelon | CC Attribution | 54.166 | 38.9 MB | `assets/bina/fabrika-modular/` |
| Gecekondu | [Shanty \| House \| Building \| Enterable](https://sketchfab.com/3d-models/shanty-house-building-enterable-64f09376d1a44ffd8716d7cc5f28db9c) | YadroGames | CC Attribution | 2.700 | 4.6 MB | `assets/bina/gecekondu/` |
| Gecekondu konak | [Shanty \| Mansion \| Wooden](https://sketchfab.com/3d-models/shanty-mansion-wooden-cf93dfd6da1640f08ebe051ba280426d) | YadroGames | CC Attribution | 5.150 | 11.2 MB | `assets/bina/gecekondu-konak/` |
| Harabe bina | [Ruin Building](https://sketchfab.com/3d-models/ruin-building-184d70cc473540749206cc7d8f9917b8) | nermin | CC Attribution | 33.384 | 21.4 MB | `assets/bina/harabe-bina/` |
| Helikopter pisti | [Heliport Helipad air base helicopter](https://sketchfab.com/3d-models/heliport-helipad-air-base-helicopter-5bc89e02a58b4ebca7404e5e35da2481) | Mehdi Shahsavan | CC Attribution | 56.678 | 23.2 MB | `assets/bina/helikopter-pisti/` |
| Iletisim kulesi | [Telecommunication Tower Low-Poly Free](https://sketchfab.com/3d-models/telecommunication-tower-low-poly-free-39bee442b9aa4c3d8dc7674453cd78ad) | Nicholas-3D | CC Attribution | 8.042 | 5.3 MB | `assets/bina/iletisim-kulesi/` |
| Kentsel cit | [Modular Urban Fence Pack (w/ graffiti textures)](https://sketchfab.com/3d-models/modular-urban-fence-pack-w-graffiti-textures-1cf3690327bd449881ba6857d8fe7caf) | TampaJoey | CC Attribution | 39.031 | 22.5 MB | `assets/bina/kentsel-cit/` |
| Konteyner bina | [Building \| Container \| Metal](https://sketchfab.com/3d-models/building-container-metal-36380c606bae46848237e9bbe073fa3b) | YadroGames | CC Attribution | 920 | 1.4 MB | `assets/bina/konteyner-bina/` |
| Modular gecekondu | [Modular Slums](https://sketchfab.com/3d-models/modular-slums-e2b6f532e1fe4f7280890971d78183f4) | AlexFerrart3D | CC Attribution | 17.328 | 4.3 MB | `assets/bina/modular-gecekondu/` |
| Moduler sanayi | [Modular industrial building](https://sketchfab.com/3d-models/modular-industrial-building-4bb58f7548c7464ebdf41a51958f712a) | Niko_Forest1889 | CC Attribution | 55.026 | 13.1 MB | `assets/bina/moduler-sanayi/` |
| Nobet kulesi | [Guard Tower [Free Asset]](https://sketchfab.com/3d-models/guard-tower-free-asset-963071f5fe404970a40b166bcee430b8) | Lex713 | CC Attribution | 2.268 | 4.2 MB | `assets/bina/nobet-kulesi/` |
| Nobet kulesi 2 | [Watchtower](https://sketchfab.com/3d-models/watchtower-bda39e79dbfa4976b1791b6b1f58259c) | Mehdi Shahsavan | CC Attribution | 2.106 | 3.9 MB | `assets/bina/nobet-kulesi-2/` |
| Pasli tank | [Rusted Tank storage](https://sketchfab.com/3d-models/rusted-tank-storage-57be2eaf4d6b4d2980bcee4ccb35f780) | Mkc | CC Attribution | 5.769 | 3.6 MB | `assets/bina/pasli-tank/` |
| Psx apartman | [PSX - Apartment](https://sketchfab.com/3d-models/psx-apartment-60b98974f45745c99e3a3d6843db2d8c) | Kasugay𓅂 | CC Attribution | 340 | 5.1 MB | `assets/bina/psx-apartman/` |
| Rts askeri bina | [RTS Military Building 1](https://sketchfab.com/3d-models/rts-military-building-1-4925be311dbb4d66b636ff40b235b047) | Sabri Ayeş | CC Attribution | 3.030 | 1.7 MB | `assets/bina/rts-askeri-bina/` |
| Sanayi seti | [Industrial Buildings Set - Low poly models](https://sketchfab.com/3d-models/industrial-buildings-set-low-poly-models-e0b0d0342be24e6c923319991a2a4d3d) | Daniel Zhabotinsky | CC Attribution | 30.627 | 11.2 MB | `assets/bina/sanayi-seti/` |
| Sehir harabesi | [City Ruins Environment](https://sketchfab.com/3d-models/city-ruins-environment-0d32be87779243749417ec783fb3ef60) | falk lochmann | CC Attribution | 55.992 | 15.8 MB | `assets/bina/sehir-harabesi/` |
| Siginak cadiri | [Simple Shelter - Animated](https://sketchfab.com/3d-models/simple-shelter-animated-934f060fd42d4073995ac3ae69a12876) | Berk Gedik | CC Attribution | 5.906 | 6.7 MB | `assets/bina/siginak-cadiri/` |
| Sogutma kuleli fabrika | [Factory Low-Poly](https://sketchfab.com/3d-models/factory-low-poly-7d3bc4d7ce6d48d9986a664d48f3cca1) | KIFIR | CC Attribution | 6.790 | 12.5 MB | `assets/bina/sogutma-kuleli-fabrika/` |
| Sovyet panel ev | [Soviet panel house built in the 1970s](https://sketchfab.com/3d-models/soviet-panel-house-built-in-the-1970s-94996e8cf4a8452d91ec1e206b5b4137) | Unka II | CC Attribution | 10.068 | 2.5 MB | `assets/bina/sovyet-panel-ev/` |
| Su kulesi | [water tower](https://sketchfab.com/3d-models/water-tower-1c2f86dc8f794c85a91706d401d104db) | Lora | CC Attribution | 756 | 4.6 MB | `assets/bina/su-kulesi/` |
| Tel orgu | [Chain link fence pack (low poly game ready)](https://sketchfab.com/3d-models/chain-link-fence-pack-low-poly-game-ready-777e50cd6e5d4db99d70bf7b20370f7a) | TampaJoey | CC Attribution | 17.554 | 10.9 MB | `assets/bina/tel-orgu/` |
| Terk garaj | [Abandoned Garage Block Rusty Ruined Game-Ready](https://sketchfab.com/3d-models/abandoned-garage-block-rusty-ruined-game-ready-a1959927a98e4752bdb01b6e1f7f7d26) | olegolegperepelica | CC Attribution | 8.369 | 9.8 MB | `assets/bina/terk-garaj/` |
| Uc depo | [Pack - Realistic - 3 Warehouse](https://sketchfab.com/3d-models/pack-realistic-3-warehouse-320c272513a94c0482dbb3c4e79d61f5) | Islide | CC Attribution | 1.302 | 0.3 MB | `assets/bina/uc-depo/` |
| Ucak yakit tanki | [Rusty airbase fuel tank](https://sketchfab.com/3d-models/rusty-airbase-fuel-tank-5ac257aee23e47e0a0f91a4e07a40692) | LuddePudde | CC Attribution | 2.532 | 2.4 MB | `assets/bina/ucak-yakit-tanki/` |
| Uretim tesisi | [Manufacturing Plant](https://sketchfab.com/3d-models/manufacturing-plant-b35a623dd21449a0917a047135aebc45) | anaroeto | CC Attribution | 1.907 | 5.2 MB | `assets/bina/uretim-tesisi/` |
| Yirmi iki bina paketi | [Pack - Low Poly - 22 Building [ Interior ]](https://sketchfab.com/3d-models/pack-low-poly-22-building-interior-86c688c132d14edc8a2f4d105578b7ad) | Islide | CC Attribution | 25.847 | 2.0 MB | `assets/bina/yirmi-iki-bina-paketi/` |

## Bölüm 5: Bilim kurgu binaları (Sketchfab, CC BY 4.0)

`assets/bina/scifi-*`, `ana-kapi`, `cyberpunk-bina`.

| Birim | Model | Yapımcı | Lisans | Üçgen | Boyut | Klasör |
|---|---|---|---|---|---|---|
| Ana kapi | [Main gate](https://sketchfab.com/3d-models/main-gate-2a52366570204019b848f32baf9ac665) | local.yany | CC Attribution | 56.604 | 6.2 MB | `assets/bina/ana-kapi/` |
| Cyberpunk bina | [Cyberpunk Building](https://sketchfab.com/3d-models/cyberpunk-building-e79154e588bd4a6c84fa07e9a53f3ff9) | igor.tesV | CC Attribution | 11.383 | 10.6 MB | `assets/bina/cyberpunk-bina/` |
| Scifi alfa kule | [ALPHA TOWER](https://sketchfab.com/3d-models/alpha-tower-4419eca89c2a43bd9a9f7d662f6b6918) | Portal.Studio | CC Attribution | 22.068 | 8.1 MB | `assets/bina/scifi-alfa-kule/` |
| Scifi bina 1 nenkea | [Sci-Fi Building 1](https://sketchfab.com/3d-models/sci-fi-building-1-da4d7f4c35be49baa287af0782c2171b) | 𝗻𝗲𝗻𝗸𝗲𝗮 | CC Attribution | 35.792 | 15.4 MB | `assets/bina/scifi-bina-1-nenkea/` |
| Scifi bina 11 | [Sci-fi Building 11](https://sketchfab.com/3d-models/sci-fi-building-11-d3029779c7e54ee6afa3890b42a32098) | Scarecrow_original | CC Attribution | 4.328 | 2.4 MB | `assets/bina/scifi-bina-11/` |
| Scifi bina 2 | [Sci-fi Building 2](https://sketchfab.com/3d-models/sci-fi-building-2-3559c3a0038f4c5f94335707ccff8217) | Scarecrow_original | CC Attribution | 25.854 | 4.0 MB | `assets/bina/scifi-bina-2/` |
| Scifi bina 2 nenkea | [Sci- Fi / Future Building 2: Simple Dome](https://sketchfab.com/3d-models/sci-fi-future-building-2-simple-dome-d885fdb25ed846779fc711917fbeeed2) | 𝗻𝗲𝗻𝗸𝗲𝗮 | CC Attribution | 47.880 | 3.7 MB | `assets/bina/scifi-bina-2-nenkea/` |
| Scifi bina jl | [Sc-fi Building](https://sketchfab.com/3d-models/sc-fi-building-bb76aebb7dd947c8a4edf02ed12376ce) | Jonathan | CC Attribution | 1.462 | 3.8 MB | `assets/bina/scifi-bina-jl/` |
| Scifi bina sc | [Sci-fi Building 2](https://sketchfab.com/3d-models/sci-fi-building-2-3559c3a0038f4c5f94335707ccff8217) | Scarecrow_original | CC Attribution | 25.854 | 4.0 MB | `assets/bina/scifi-bina-sc/` |
| Scifi futuristik bina jl | [Futuristic Building](https://sketchfab.com/3d-models/futuristic-building-555daf778aa245158e4b24214ccc1dbb) | Jonathan | CC Attribution | 1.595 | 3.4 MB | `assets/bina/scifi-futuristik-bina-jl/` |
| Scifi giris | [SCI-FI ENTRANCE APOCALYPSE](https://sketchfab.com/3d-models/sci-fi-entrance-apocalypse-f3b606485ddb4066b16f31c9a969250d) | Adriancgmask | CC Attribution | 7.523 | 9.6 MB | `assets/bina/scifi-giris/` |
| Scifi jenerator | [Sci-fi Generator](https://sketchfab.com/3d-models/sci-fi-generator-685fc34284574996b09ae0f826367e90) | Eh | CC Attribution | 14.628 | 1.1 MB | `assets/bina/scifi-jenerator/` |
| Scifi kule | [Sci-Fi Tower](https://sketchfab.com/3d-models/sci-fi-tower-c271103cd2f84ed3992baeda6416bbb0) | Jonathan | CC Attribution | 3.389 | 3.6 MB | `assets/bina/scifi-kule/` |
| Scifi platform | [Top Down Scifi Industrial platforms](https://sketchfab.com/3d-models/top-down-scifi-industrial-platforms-86245425f3d0468eb70456528b399f90) | R-LAB | CC Attribution | 39.282 | 11.0 MB | `assets/bina/scifi-platform/` |

## Bölüm 6: Harita parçaları (Sketchfab, CC BY 4.0)

`assets/bina/harita-*`: çöl kalesi (kule, zemin, yol), Mısır haritası, kanyon, karlı dağ, gerçek arazi taramaları (Mars Olympus Dağı, Mars Aram Chaos, Uluru, Moğolistan köyü), ağaç, bitki, çimen, beton duvar, şehir paketi. Hazır strateji haritası yok; harita bu parçalarla ve zemin dokularıyla kurulacak.

| Birim | Model | Yapımcı | Lisans | Üçgen | Boyut | Klasör |
|---|---|---|---|---|---|---|
| Harita agaclar | [Low poly trees. flowers and grass](https://sketchfab.com/3d-models/low-poly-trees-flowers-and-grass-442904f26b87407d98871b50b49c4169) | MMC Works | CC Attribution | 5.496 | 20.1 MB | `assets/bina/harita-agaclar/` |
| Harita beton duvar | [Dirty leaking concrete wall](https://sketchfab.com/3d-models/dirty-leaking-concrete-wall-893893fc88104dd8a3bd66333411acd2) | Оrрндп ЯТG | CC Attribution | 11.992 | 1.4 MB | `assets/bina/harita-beton-duvar/` |
| Harita bitkiler | [Shapespark low poly exterior plants kit](https://sketchfab.com/3d-models/shapespark-low-poly-exterior-plants-kit-de9e79fc07b748d1a6ac055b49ee5c67) | Shapespark | CC Attribution | 7.665 | 30.1 MB | `assets/bina/harita-bitkiler/` |
| Harita cimen | [Realistics grass 06](https://sketchfab.com/3d-models/realistics-grass-06-b5956b7d4d1f4ff6ae1dd1320dab0d12) | POLYSCAN | CC Attribution | 6.552 | 0.7 MB | `assets/bina/harita-cimen/` |
| Harita col kalesi kuleler | [Desert_ Fortress_ Towers](https://sketchfab.com/3d-models/desert--fortress--towers-368813c939494eb0b0d63fa634b03589) | Nicolai Kilstrup | CC Attribution | 51.196 | 9.2 MB | `assets/bina/harita-col-kalesi-kuleler/` |
| Harita col kalesi yollar | [Desert Fortress Walkways](https://sketchfab.com/3d-models/desert-fortress-walkways-63ea28dc696a414a979cf3a1e3213ec3) | Nicolai Kilstrup | CC Attribution | 47.156 | 31.7 MB | `assets/bina/harita-col-kalesi-yollar/` |
| Harita col kalesi zemin | [Desert Fortress Floor](https://sketchfab.com/3d-models/desert-fortress-floor-83d7c8a82fda43bd911a2e1d06d24adb) | Nicolai Kilstrup | CC Attribution | 36.578 | 29.8 MB | `assets/bina/harita-col-kalesi-zemin/` |
| Harita kanyon | [Shift Happens - Canyon Diorama](https://sketchfab.com/3d-models/shift-happens-canyon-diorama-ffd36dfbfda8432d97388988883f6295) | Klonk Games | CC Attribution | 23.179 | 12.9 MB | `assets/bina/harita-kanyon/` |
| Harita karli dag | [Snow Mountain](https://sketchfab.com/3d-models/snow-mountain-e84a8e5edb2040c591be36350e2536f5) | hkp941111 | CC Attribution | 13.045 | 4.0 MB | `assets/bina/harita-karli-dag/` |
| Harita mars aram chaos | [Mars - Aram Chaos region](https://sketchfab.com/3d-models/mars-aram-chaos-region-5c9b99de0405465f81ff0ba244ef69e2) | SebastianSosnowski | CC Attribution | 37.962 | 5.1 MB | `assets/bina/harita-mars-aram-chaos/` |
| Harita mars dagi | [Mars - Olympus Mons](https://sketchfab.com/3d-models/mars-olympus-mons-53679864b41a43b0ae0459ce99d6adf0) | SebastianSosnowski | CC Attribution | 10.662 | 4.2 MB | `assets/bina/harita-mars-dagi/` |
| Harita misir | [Environment Pack - Egypt Map](https://sketchfab.com/3d-models/environment-pack-egypt-map-3049b31b9aba4f6d94345573be670aca) | PolyOne Studio | CC Attribution | 23.331 | 7.7 MB | `assets/bina/harita-misir/` |
| Harita mogol koyu | [Czojr - isolated village in Mongolia](https://sketchfab.com/3d-models/czojr-isolated-village-in-mongolia-09eb4b1665014c9d97add5970bb1f5b9) | SebastianSosnowski | CC Attribution | 2.578 | 3.4 MB | `assets/bina/harita-mogol-koyu/` |
| Harita sehir paketi | [City pack 7](https://sketchfab.com/3d-models/city-pack-7-6550e37439814c348e2c884aa740ca3c) | Pasha | CC Attribution | 31.124 | 14.2 MB | `assets/bina/harita-sehir-paketi/` |
| Harita uluru | [Uluru - Australia`s sacred mountain](https://sketchfab.com/3d-models/uluru-australias-sacred-mountain-045af620b492487d84a31b745d5a9cfd) | SebastianSosnowski | CC Attribution | 9.904 | 4.0 MB | `assets/bina/harita-uluru/` |

## Bölüm 7: Kısıtlı lisanslı modeller — SATIŞTAN ÖNCE DEĞİŞTİRİLMELİ

`assets/kisitli/<ad>/` altındakiler **NonCommercial (NC: ticari kullanım yasak)**, **ShareAlike (SA: değiştirilen hâli aynı lisansla paylaşılmalı)** lisanslı ya da **Textures.com dokulu** (üç bina: Asya apartmanı, Sovyet apartmanı, sanayi binası; Textures.com dokuların ham paylaşımını kısıtlar). Deneme ve prototip için kullanılabilir; oyun satılmadan önce yerine CC0/CC BY model konmalı ya da yapımcıdan yazılı izin alınmalı.

Taramada elenenler: "SkyBox Blue Desert" (yapay zekâ üretimi), "City map (not a scan)" (kopya), "Military Blockpost S.T.A.L.K.E.R", "Buildings from Trainz Simulator", Star Wars adlı modeller.

| Birim | Model | Yapımcı | Lisans | Üçgen | Boyut | Klasör |
|---|---|---|---|---|---|---|
| Asya blok | [LOW POLY - ASIAN TOWER BLOCK](https://sketchfab.com/3d-models/low-poly-asian-tower-block-694adf5094fa41f99a245ed822293f47) | Colin.Greenall | CC Attribution | 3.148 | 2.7 MB | `assets/kisitli/asya-blok/` |
| Corak dukkanlar | [Wasteland Stores](https://sketchfab.com/3d-models/wasteland-stores-7b66bc988ea04c058008c3a774622a44) | Renafox | CC Attribution-NonCommercial | 712 | 8.8 MB | `assets/kisitli/corak-dukkanlar/` |
| Fakir col evi | [Poor Desert House](https://sketchfab.com/3d-models/poor-desert-house-64310fbd9b1640cdbf04f5f12ad58ba2) | Fjordreig | CC Attribution-NonCommercial | 2.097 | 8.7 MB | `assets/kisitli/fakir-col-evi/` |
| Harita arka plan arazi | [Sketch Background Terrain](https://sketchfab.com/3d-models/sketch-background-terrain-1e84bfc2489b433d951478f79fc7952f) | Peter Leban | CC Attribution-NonCommercial | 42.160 | 4.4 MB | `assets/kisitli/harita-arka-plan-arazi/` |
| Japon askeri us | [Japan Self-Defense Forces Military Base kit](https://sketchfab.com/3d-models/japan-self-defense-forces-military-base-kit-77da87c27b784fa1951f187642b4d3fd) | Plevako | CC Attribution-ShareAlike | 50.085 | 13.2 MB | `assets/kisitli/japon-askeri-us/` |
| Mech hangar | [Mech Hangar](https://sketchfab.com/3d-models/mech-hangar-dd0a83c82a1e4a85b0770a02eb4073f1) | Willie Garnarbles | CC Attribution-NonCommercial | 3.244 | 0.5 MB | `assets/kisitli/mech-hangar/` |
| Sanayi binasi | [industrial building](https://sketchfab.com/3d-models/industrial-building-770acf6b0da74af397f748d95141f8be) | spicybamer | CC Attribution | 2.494 | 5.0 MB | `assets/kisitli/sanayi-binasi/` |
| Scifi futuristik bina | [Futuristic Building](https://sketchfab.com/3d-models/futuristic-building-e73f9bb9981d469c8a8ccdc1f168faad) | 3DHaupt | CC Attribution-NonCommercial | 28.060 | 9.1 MB | `assets/kisitli/scifi-futuristik-bina/` |
| Scifi gunes kulesi | [Sci-Fi Solar Power Tower (Free-Download)](https://sketchfab.com/3d-models/sci-fi-solar-power-tower-free-download-0c4a96b5e8474eb38097e5305392a137) | 3DHaupt | CC Attribution-NonCommercial-ShareAlike | 16.556 | 6.9 MB | `assets/kisitli/scifi-gunes-kulesi/` |
| Scifi kule ev | [Tower House Design](https://sketchfab.com/3d-models/tower-house-design-a972a15421a942429f1279824e00c042) | 3DHaupt | CC Attribution-NonCommercial | 16.492 | 18.0 MB | `assets/kisitli/scifi-kule-ev/` |
| Scifi stilize binalar | [Stylized Low Poly Sci-Fi Buildings](https://sketchfab.com/3d-models/stylized-low-poly-sci-fi-buildings-701381fef32444e79ad804315e563049) | Robin Butler | CC Attribution-NonCommercial | 29.590 | 1.6 MB | `assets/kisitli/scifi-stilize-binalar/` |
| Sovyet apartman | [LOW POLY - SOVIET  APARTMENT BUILDING 8K](https://sketchfab.com/3d-models/low-poly-soviet-apartment-building-8k-05229ac1d1f94e6c8cacaad91110c602) | Colin.Greenall | CC Attribution | 10.392 | 3.1 MB | `assets/kisitli/sovyet-apartman/` |
| Yikik bina | [Destroyed building. study](https://sketchfab.com/3d-models/destroyed-building-study-8a95ab9548314c66bb0bf7c2191da80c) | samuel.brunner | CC Attribution-NonCommercial | 24.114 | 6.5 MB | `assets/kisitli/yikik-bina/` |
