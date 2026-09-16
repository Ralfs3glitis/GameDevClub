---
{"dg-publish":true,"permalink":"/notes/pulcins-info/","tags":["note"],"dg-note-properties":{"categories":["[[Categories/Projects]]"],"references":["[[Notes/Datorspēļu dizains un programmēšana]]"],"tags":["note"],"created":"2026-09-14","cssclasses":null}}
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
