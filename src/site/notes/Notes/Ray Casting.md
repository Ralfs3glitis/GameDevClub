---
{"dg-publish":true,"permalink":"/notes/ray-casting/","tags":["note"],"dg-note-properties":{"categories":["[[Categories/Projects]]"],"section":"[[Notes/4. Pulciņa nodarbība]]","tags":["note"],"created":"2026-09-29","cssclasses":null}}
---

[[Notes/4. Pulciņa nodarbība\|Atpakaļ]]

---
# Staru raidīšana (ray casting)
**Staru raidīšana** (ray casting) ir paņēmiens spēļu izstrādē, kurā no viena punkta telpā tiek izšauts neredzams taisns stars, lai noskaidrotu, **vai tas kaut kam trāpa** (collider), **kur tieši trāpa** (position) un **kāds ir trāpītā objekta virsmas leņķis** (normal).

Tas ir kā **lāzeris ar iebūvētu tālmēru**: stars lido **taisni**, līdz atduras pret **pirmo objektu**, un uzreiz paziņo visu informāciju par trāpījumu.

## Maskas
Tāpat, kā fizikas objektiem, stariem iespējams norādīt [[Notes/Collisions, layers and masks#Maska (Mask)\|sadursmes maskas]]. 
Stari redz tikai pirmo objektu, ar kuru notiek sadursme, tāpēc, ja izmantojam staru raidīšanu lai **noteiktu vai pretinieks redz spēlētāju**, tā maskās nepieciešams **norādīt spēlētāju**, un **izlaist pretinieku** (stara avotu), lai tas nesaskartos tikai ar savu sadursmes formu.
<img src="https://docs.godotengine.org/en/stable/_images/raycast_falsepositive.webp" style="border-radius: 4px;">

## Pielietojums
### 1. Tūlītēja trāpījuma šaušana šūteru spēlēs
[[Notes/Pulciņā izmantotās terminoloģijas vārdnīca\|FPS (First-Person Shooter)]] un 2D top-down šūteros (piemēram, _Hotline Miami_):

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/notes/4-pulcina-nodarbibas-intro/#tuliteja-trapijuma-sausana" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### Tūlītēja trāpījuma šaušana
- **Tūlītēja trāpījuma** kategorijas ieroči neveido reālu šāviņu, tiek [[Notes/Ray Casting\|raidīts taisns stars]], ar kuru uzreiz iespējams noteikt sadursmi, tās pozīciju, ietekmēto objektu un citas nepieciešamās īpašības. Pēc tam, lai vizuāli **izskatītos**, ka ierocis veido šāviņu, [lineāri interpolējam](https://docs.godotengine.org/en/stable/tutorials/math/interpolation.html) tā vizuālās daļas pozīciju no ieroča līdz sadursmes vietai. 
<img src="https://docs.godotengine.org/en/stable/_images/interpolation_vector.gif" style="border-radius: 4px;">


</div></div>


### 2. Mākslīgā intelekta (AI) redzamība un Stealth mehānika

Ienaidniekiem spēlēs ir jāzina, vai viņi var redzēt spēlētāju, vai arī spēlētājs slēpjas aiz sienas vai kastes.

- **Kā tas strādā:** Katru sekundi (vai katru kadru) ienaidnieks raida staru uz spēlētāja pozīciju.
    
- **Slāņu un masku nozīme:** Stara [[Notes/Collisions, layers and masks#Maska (Mask)\|maskās]] jābūt gan spēlētājam, gan šķēršļiem.
    - Ja stars vispirms trāpa _Sienai_ => spēlētājs ir aiz sienas, ienaidnieks viņu neredz.
    - Ja stars vispirms trāpa _Spēlētājam_ => ienaidnieks viņu redz.
### 3. Zemes un slīpumu noteikšana (Ground & Slope Check)

Platformeru spēlēs (piemēram, _Hollow Knight_ vai _Celeste_) tēlam ir precīzi jāzina, vai viņš atrodas uz zemes, cik tālu ir grīda un kādā leņķī tā ir.

- **Kā tas strādā:** No tēla kājām uz leju tiek raidīti viens vai vairāki īsi stari.
    - Ja stars netrāpa nekam, tēls ir gaisā un jāsāk krist.
    - **Leņķis:** Nolasot zemes *normal* (virsmas leņķi), spēle var pielāgot tēla rotāciju slīpumam (lai viņš nestāvētu taisni uz 45° kalna) vai mainīt pārvietošanās ātrumu, kāpjot kalnā.
![Pasted image 20260929120135.png](/img/user/Attachments/Pasted%20image%2020260929120135.png)

### 4. Kāju novietojums uz nelīdzenas virsmas (Inverse Kinematics / IK)

Mūsdienu 3D un detalizētās 2D spēlēs, kad tēls stāv uz kāpnēm vai akmeņiem, viņa kājas pielāgojas virsmas augstumam.

- **Kā tas strādā:** No katras kājas gurna uz leju tiek raidīts stars. Stars nosaka precīzu augstumu, kur atrodas zeme zem konkrētās kājas, un spēles animāciju sistēma nolaiž vai paceļ pēdu tieši uz šī punkta.
### 5. Peles klikšķis pasaulē (Point-and-Click / RTS kustība)
Spēlēs kā _League of Legends_, _Diablo_, _Age of Empires_ vai _The Sims_ spēlētājs redz pasauli no augšas (caur kameru) un klikšķina uz vietu, kur tēlam jāiet.

Kā dators var zināt, kurš 3D pasaules punkts atbilst peles klikšķim uz 2D monitora?

- **Kā tas strādā:**
    1. Brīdī, kad noklikšķināts ar peli, spēles **Kamera** paņem peles (x, y) koordinātas uz ekrāna.
    2. No kameras, caur šo klikšķa pikseli ekrānā tiek izšauts **bezgalīgi garš stars** 3D pasaulē.
    3. Stars lido lejup, līdz tas atduras pret kaut ko (spēles līmeņa grīdu).
    4. Trāpījuma punkts (Hit Point) kļūst par mērķa koordināti, uz kuru tēlam jādodas.

- **Slāņu un Masku nozīme šajā gadījumā:**
    - Staram maskā ir *Zemes* (Terrain) slānis un *Ienaidnieku* slānis.
    - Ja noklikšķināts, un stars trāpa Zemei – tēls tur iet.
    - Ja noklikšķināts uz ienaidnieka, tēls sāk uzbrukumu.
    - Ja stars netrāpa nekam (noklikšķināts piem. ārpus kartes), spēle klikšķi ignorē.

<img src="https://docs.godotengine.org/en/stable/_images/raycast_projection.png" style="border-radius: 4px;">

## [Staru raidīšana Godot](https://docs.godotengine.org/en/stable/tutorials/physics/ray-casting.html)