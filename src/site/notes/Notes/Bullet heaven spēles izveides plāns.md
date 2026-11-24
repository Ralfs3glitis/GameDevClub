---
{"dg-publish":true,"permalink":"/notes/bullet-heaven-speles-izveides-plans/","tags":["note"],"dg-note-properties":{"categories":["[[Categories/Projects]]"],"references":["[[Pulciņa nodarbības/17. Pulciņa nodarbība]]"],"tags":["note"],"created":"2026-11-24","cssclasses":null}}
---

[[Pulciņa nodarbības/17. Pulciņa nodarbība\|Atpakaļ]]

---
# Plāns
1. Veiktspēja
2. Spēlētājs un rādītāji (stats)
3. Pretinieki un viļņi
4. Spējas (abilities), 1. daļa
5. Spējas, 2. daļa
6. Pieredze un līmeņa kāpums
7. Varoņi
8. Sulīgums: skaņas, efekti, skaitļi
9. Spēles cikls un saglabāšana
10. Slīpēšana un demonstrācija

# Datņu struktūra
```text
res://
├── autoload/      game.gd  pools.gd  events.gd
├── core/          stat.gd  stat_modifier.gd  stats.gd  health.gd  pool.gd
├── data/          abilities/  passives/  characters/  enemies/  waves/     (.tres, one file per item)
├── entities/      player/  enemy/  projectile/  pickups/
├── abilities/     ability_instance.gd  behaviors/ (projectile, orbit, aura)
├── director/      spawn_director.gd  spawn_rule.gd
├── ui/            hud.tscn  level_up_menu.tscn  character_select.tscn  debug_hud.tscn
├── debug/         swarm_test.tscn          # lesson 1 sandbox, kept as a performance regression test
└── assets/
```