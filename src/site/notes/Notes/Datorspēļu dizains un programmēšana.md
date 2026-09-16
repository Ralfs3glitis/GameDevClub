---
{"dg-publish":true,"permalink":"/notes/datorspelu-dizains-un-programmesana/","tags":["note","gardenEntry"],"dg-note-properties":{"categories":["[[Categories/Projects]]"],"references":["[[Notes/Jelgavas Tehnikums]]"],"tags":["note","gardenEntry"],"created":"2026-09-05","cssclasses":null,"aliases":["Pulciņš"]}}
---

---

```base
filters:
  and:
    - categories.contains(link("Projects"))
    - '!file.inFolder("Templates")'
views:
  - type: table
    name: This
    filters:
      or:
        - list(references).containsAny(list(this))
        - list(section).containsAny(list(this))
    order:
      - file.name
      - created
      - file.tags
    sort:
      - property: file.name
        direction: ASC
    columnSize:
      file.name: 274
      note.created: 216

```


