---
{"dg-publish":true,"permalink":"/notes/collisions-layers-and-masks/","tags":["note"],"dg-note-properties":{"categories":["[[Categories/Projects]]"],"section":"[[Notes/4. Pulciņa nodarbība]]","tags":["note"],"created":"2026-09-29","cssclasses":null}}
---

[[Notes/4. Pulciņa nodarbība\|Atpakaļ]]

---
# Sadursmes (collisions)
Godot dzinējā sadursmju (collision) sistēma balstās uz diviem galvenajiem jēdzieniem:
#### Slānis (Layer)
- **Slānis (Layer): "Kas es esmu?"** Nosaka, kurā "kastītē" vai kategorijā šis objekts atrodas. Piemēram, tu vari būt Spēlētājs (Layer 1), Ienaidnieks (Layer 2) vai Siena (Layer 3).
#### Maska (Mask)
- **Maska (Mask): "Ko es redzu / ar ko es saduros?"** Nosaka, kurus slāņus šis objekts aktīvi meklē un pret kuriem tas atsitīsies.

![Pasted image 20260929112506.png\|676](/img/user/Attachments/Pasted%20image%2020260929112506.png)

Ja objekta A **Maska** sakrīt ar objekta B **Slāni**, notiks sadursme. Fizikas objektu gadījumā (kā `CharacterBody`), pietiek ar to, ka **vismaz viens** no objektiem *redz* otru.