---
{"dg-publish":true,"permalink":"/notes/collision-objects-and-shapes-in-godot/","tags":["note"],"dg-note-properties":{"categories":["[[Categories/Projects]]"],"section":"[[Notes/4. Pulciņa nodarbība]]","tags":["note"],"created":"2026-09-29","cssclasses":null}}
---

[[Notes/4. Pulciņa nodarbība\|Atpakaļ]]

---
# Sadursmes objekti un formas

## Sadursmes Objekti (Collision Objects)
Godot piedāvā četrus sadursmes objektu tipus, kas papildina (manto) [CollisionObject2D](https://docs.godotengine.org/en/stable/classes/class_collisionobject2d.html#class-collisionobject2d). Pēdējie trīs minētie ir arī fizikas ķermeņi, kas manto [PhysicsBody2D](https://docs.godotengine.org/en/stable/classes/class_physicsbody2d.html#class-physicsbody2d).

##### [Area2D](https://docs.godotengine.org/en/stable/classes/class_area2d.html#class-area2d)
`Area2D` mezgli nodrošina **noteikšanu** un **ietekmi**. Tie spēj noteikt, kad objekti pārklājas, un var raidīt signālus, kad ķermeņi ienāk vai iziet no tiem. `Area2D` var izmantot arī, lai noteiktā zonā pārrakstītu (override) fizikas īpašības, piemēram, gravitāciju.
    
##### [StaticBody2D](https://docs.godotengine.org/en/stable/classes/class_staticbody2d.html#class-staticbody2d)
Statisks ķermenis ir tāds, ko fizikas dzinējs nepārvieto. Tas piedalās sadursmju noteikšanā, bet nepārvietojas reakcijā uz sadursmi. Tos visbiežāk izmanto objektiem, kas ir daļa no vides vai kuriem nav nepieciešama dinamiska uzvedība.
    
##### [RigidBody2D](https://docs.godotengine.org/en/stable/classes/class_rigidbody2d.html#class-rigidbody2d)
Šis ir mezgls, kas īsteno simulētu 2D fiziku. Jūs nevadāt `RigidBody2D` tieši, bet tā vietā pieliekat tam spēkus (gravitāciju, impulsus utt.), un **fizikas dzinējs** aprēķina rezultējošo kustību. Lasiet vairāk par stingro ķermeņu (rigid bodies) izmantošanu [šeit](https://docs.godotengine.org/en/stable/tutorials/physics/rigid_body.html#doc-rigid-body).
    
##### [CharacterBody2D](https://docs.godotengine.org/en/stable/classes/class_characterbody2d.html#class-characterbody2d)
Ķermenis, kas nodrošina sadursmju noteikšanu, bet ne fiziku. Visa kustība un reakcija uz sadursmēm ir jāīsteno kodā.

## Sadursmes formas (Collision Shapes)
Fizikas ķermenim kā apakšelementi (child nodes) var būt jebkāds skaits [Shape2D](https://docs.godotengine.org/en/stable/classes/class_shape2d.html#class-shape2d) objektu. Šīs formas tiek izmantotas, lai definētu objekta sadursmes robežas un noteiktu saskarsmi ar citiem objektiem.

**Piezīme** Lai noteiktu sadursmes, objektam ir jāpiešķir vismaz viens `Shape2D`.

Visbiežāk izmantotais veids, kā piešķirt formu, ir pievienot [CollisionShape2D](https://docs.godotengine.org/en/stable/classes/class_collisionshape2d.html#class-collisionshape2d) vai [CollisionPolygon2D](https://docs.godotengine.org/en/stable/classes/class_collisionpolygon2d.html#class-collisionpolygon2d) kā apakšelementu. Ar šiem mezgliem iespējams uzzīmēt sadursmes formu redaktorā.

> **Svarīgi** 
> Esiet uzmanīgi un redaktorā nekad nemainiet *Scale* atribūtu sadursmes formās. Īpašībai *Scale* panelī inspektorā ir jābūt (1, 1). Mainot sadursmes formas izmēru, vienmēr ir jāizmanto "size handles". *Scale* atribūta mainīšana var izraisīt neparedzamu sadursmju uzvedību.

| <img src="https://docs.godotengine.org/en/stable/_images/player_coll_shape.webp" style="border-radius: 4px;"> | ![Inspektora col_shape yes and no.png\|444](/img/user/Attachments/Inspektora%20col_shape%20yes%20and%20no.png) |
| ------------------------------------------------------------------------------------------------------------- | --------------------------------------------- |

