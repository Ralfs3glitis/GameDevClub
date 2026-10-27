---
{"dg-publish":true,"permalink":"/notes/modularitate/","tags":["note"],"dg-note-properties":{"categories":["[[Categories/Projects]]"],"section":"[[Notes/11. Pulciņa nodarbība]]","tags":["note"],"created":"2026-10-27","cssclasses":null}}
---

[[Notes/11. Pulciņa nodarbība\|Atpakaļ]]

---
# Kas ir modularitāte?
## Definīcija
Modularitātei ir 2 definīcijas:
	1.Sistēmas vai programmas organizētība pa moduļiem – atsevišķiem funkcionāliem komponentiem.
	2.Tas, cik neatkarīgi ir programmas moduļi.
>Avots: [Tēzaurs](https://tezaurs.lv/modularit%C4%81te:1)
## Skaidrojums
Tātad, **modulāra sistēma** ir sadalīta **moduļos** jeb **funkcionālos komponentos**. Katra sistēmas daļa atbild tikai pati par sevi - tā ir **neatkarīga**.

# Modularitāte Godot
## Mezglos
Iepriekš apskatījām modularitāti mezglu arhitektūrā, kur, piemēram, mezgls **pretinieks** sastāv no **animāciju** un **kustību** komponenta. Šos komponentus varam izmantot arī spēlētāja izveidei, piesaistot klāt vēl arī **kameru**.
Šādu jaunu elementu izveidi izmantojot eksistējošus **moduļus** sauc par **kompozīciju**. Kompozīcija ir galvenais *OOP* paņēmiens spēļu izstrādē.
### [[Canvas/Godot mezgli canvas.canvas \| Mezglu arhitektūras zīmējums]]
## Skriptos
Pieņemsim, ka mums ir šāda mezglu arhitektūra:
![Pasted image 20261027122849.png](/img/user/Attachments/Pasted%20image%2020261027122849.png)
Mezglam **Body** ir skripts, kas satur definīciju:
```
@onready var physical_body: Node2D = $PhysicalBody
```
Mezgla **Body** skriptā esam definējuši `physical_body`, kas ir *apakšmezgls* **Body** mezglam. Ja pārvietosim **PhysicalBody** mezglu hierarhijā, atsauce nojuks, jo definīcija ir **relatīva no izsaucēja**. 
Ja **PhysicalBody** būtu *apakšmezgls* **Player**, definīcija būtu:
```
@onready var physical_body: Node2D = $"../PhysicalBody"
```
Tomēr, šo problēmu var apiet, pataisot mezglu par **unikāli nosauktu** mezglu. (labais klikšķis uz mezglu, un tad ieķeksē `Access as Unique Name`)
![Pasted image 20261027123810.png](/img/user/Attachments/Pasted%20image%2020261027123810.png)
Tagad, vienalga, kur hierarhijā atrodās mezgls, tas vienmēr būs atrodams pēc tā nosaukuma:
```
@onready var physical_body: Node2D = %PhysicalBody
```
## Inspektorā
Ja skriptā esam eksportējuši mainīgo `physical_body`:
```
@export var physical_body: Node2D
```
Inspektorā redzam, ka parādās aile **Physical Body**.
![Pasted image 20261027124317.png](/img/user/Attachments/Pasted%20image%2020261027124317.png)
Ja, spiežot `Assign...` ievietojam **PhysicalBody** mezglu:
![Pasted image 20261027124427.png](/img/user/Attachments/Pasted%20image%2020261027124427.png)
Mums ir definēts `physical_body` mainīgais ar **modulāru** atsauci uz mezglu. Varam ātri nomainīt `physical_body` vērtību inspektorā, un atsauce saglabājās, pat, ja pārvietojam **PhysicalBody** mezglu hierarhijā, jo šāda veida atsauce **nav relatīva no izsaucēja**.
Varam arī pārbaudīt, vai ir piesaistīts mezgls:
```
if physical_body:
	# Do something
else:
	# Do something else
```

# Kā izveidot moduli?
Pieņemsim, ka vēlies attēlot spēlētāja veselību - izveidot **healthbar**. Kā varam paveikt, lai tā ir **modulāra**?

Tātad, gribam izveidot mezglu, kurš, ja ir piesaistīts tēlam, attēlo tā dzīvības, izmantojot to mainīgo `health_points`.

Tēla skriptā:
```
signal health_changed(new_value)
@export var max_health_points : int
@onready var health_points : int = max_health_points:
	set(value): 
		health_changed.emit(value)
		health_points = value
@export var health_bar: HealthBar:
	set(node): 
		health_changed.connect(node.set_new_value)
		node.set_status(max_health_points, health_points)
		health_bar = node
		
func _ready() -> void:
	if health_bar:
		health_bar.set_status(max_health_points, health_points)
```
>Katru reizi, kad spēlētāja dzīvības tiek mainītas, pievienotā `health_bar` mezgla `set_new_value` funkcija tiek izsaukta ar jauno vērtību!

Tagad jāizveido **ProgressBar** tipa mezgls un jāpievieno skripts:
```
extends ProgressBar
class_name HealthBar

func set_status(max_v : int, v : int):
	max_value = max_v
	value = v

func set_new_value(v : float):
	value = v
```
Un viss! 
>Tagad, palaižot spēli nepievienojot **HealthBar** tēlam, spēle paliek funkcionāla, bet neuzrāda dzīvības. Pievienojot mezglu, tiek uzrādītas dzīvības. Esam izveidojuši **modulāru** veselības/dzīvību trekeri.

Ja gribam lai **HealthBar** ir foršas animācijas, nomainam skriptu uz šo:
```
extends ProgressBar
class_name HealthBar

@onready var new_value : float
@export var accuracy : float = 0.1
@export var speed : float = 0.01
var time : float = 0

func set_status(max_v : int, v : int):
	max_value = max_v
	value = v
	new_value = v
	
func set_new_value(v : float):
	new_value = v
	
func _physics_process(delta: float) -> void:
	time += delta * speed
	if abs(value - new_value) > accuracy:
		value = lerp(value, new_value, time)
```
> Šajā skriptā, izmantojam `lerp` ([lineāri interpolējam](https://docs.godotengine.org/en/stable/tutorials/math/interpolation.html)) lai izveidotu dzīvību palielināšanās / samazināšanās animāciju.

## Secinājums
Šādi mēs veidojam **atdalītas sistēmas**, uzturot **modulāru sistēmas arhitektūru** un veidojot jaunus objektus pielietojot **kompozīciju**. 