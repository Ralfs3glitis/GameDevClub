---
{"dg-publish":true,"permalink":"/notes/iepazisanas-ar-godot-dzini/","tags":["note"],"dg-note-properties":{"categories":["[[Categories/Projects]]"],"section":"[[Notes/2. Pulciņa nodarbība]]","tags":["note"],"created":"2026-09-21","cssclasses":null}}
---

[[Notes/2. Pulciņa nodarbība\|Atpakaļ]]

---
# Virspusēji
Mūsdienās, vairāk, kā jebkad, ir pieejami bezmaksas rīki datorspēļu izveidei. Starp ilgstoši populārākajiem [[Notes/Pulciņā izmantotās terminoloģijas vārdnīca\|plašpatēriņa]] dziņiem – _Unity Engine_ un _Unreal Engine_, ir parādījusies jauna opcija, kas strauji ieguvusi popularitāti – _Godot Engine_.

Šī bezmaksas [[Notes/Pulciņā izmantotās terminoloģijas vārdnīca\|atklātā pirmkoda programmatūra]], kas izlaista saskaņā ar liberālo _MIT_ licenci, sniedz iespēju neatkarīgiem izstrādātājiem konkurēt ar bagātajām _[[Notes/Pulciņā izmantotās terminoloģijas vārdnīca\|AAA]]_ firmām datorspēļu tirgū.
# Detalizēti
## Godot arhitektūra
- *Godot* arhitektūra ir komplicēta, objektorientēta sistēma.
- Galvenā īpašība, ar ko _Godot_ atšķirās no citiem dziņiem, ir **mezgli**.
![Pasted image 20260922174837.png](/img/user/Attachments/Pasted%20image%2020260922174837.png)
### Mezgli
#### Definīcija
- "Mezgli" (_Nodes_) ir galvenais būvmateriāls _Godot_ struktūrā. Tiem piemīt nosaukums un rediģējamas īpašības, un tie manto dažādus iebūvētus _Godot_ tipus, piemēram, objektus. Katram mezglam ir sava konkrēta funkcija, piemēram, parādīt attēlu, atskaņot skaņu, kalpot kā kamera, u.c.
#### Apakšelementi
- Mezgliem var būt "bērni" (_children_), turpmāk – _apakšelementi_ mezglu hierarhijā. 
#### Ainas
- Mezglu koku (node tree) hierarhiju sauc par "ainu" (_scene_), to iespējams saglabāt un izsaukt atkārtotai lietojamībai. 
#### Skripti
- Mezglam var arī pievienot "skriptu" (_script_), kas ir programmējams, lai paplašinātu tā funkcionalitāti. Skripti ir programmējami galvenokārt _C#_ un _GDScript_ valodās, bet neoficiāli iespējams izmantot arī _C_ un _C++_.
## Programmēšanas valodas
Pulciņā izmantosim _GDScript_ – valodu, kas ir unikāla _Godot_ dzinim. Tā ir objektorientēta un imperatīva (programmā tiek tieši norādīts vēlamā rezultāta iegūšanas veids, bet netiek norādītas tā īpašības) valoda veidota spēļu izstrādei un vizuāli izskatās kā _Python_.
## Lejupielāde
*Godot* ir pieejams uz Linux, Android, MacOS un Windows ierīcēm, kā arī, pārsteidzoši, tīmeklī.

*Godot* priekš Windows iespējams lejupielādēt šeit:
<a href="https://godotengine.org/download/windows/" style="display: inline-block; border: 1px solid var(--background-modifier-border); padding: 8px; border-radius: 8px; text-align: center; text-decoration: none; color: inherit; max-width: 100%;"><strong style="display: block; margin-bottom: 5px; font-size: 0.9em; line-height: 1.2;">Download for Windows</strong><img src="https://godotengine.org/assets/share-image.jpg" style="width: 100%; border-radius: 4px; display: block; margin: 0 auto;"></a>

