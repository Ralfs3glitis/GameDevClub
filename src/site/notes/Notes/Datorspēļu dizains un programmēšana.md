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


---

<div><table class="dataview table-view-table"><thead class="table-view-thead"><tr class="table-view-tr-header"><th class="table-view-th"><span>File</span><span class="dataview small-text">2</span></th><th class="table-view-th"><span>Created</span></th><th class="table-view-th"><span>File Tags</span></th></tr></thead><tbody class="table-view-tbody"><tr><td><span><a data-tooltip-position="top" aria-label="Notes/Pulciņa nodarbības.md" data-href="Notes/Pulciņa nodarbības.md" href="Notes/Pulciņa nodarbības.md" class="internal-link" target="_blank" rel="noopener nofollow">Pulciņa nodarbības</a></span></td><td><span>14.09.2026</span></td><td><ul class="dataview dataview-ul dataview-result-list-ul"><li class="dataview-result-list-li"><span><a href="#note" class="tag" target="_blank" rel="noopener nofollow">#note</a></span></li></ul></td></tr><tr><td><span><a data-tooltip-position="top" aria-label="Notes/Pulciņš info.md" data-href="Notes/Pulciņš info.md" href="Notes/Pulciņš info.md" class="internal-link" target="_blank" rel="noopener nofollow">Pulciņš info</a></span></td><td><span>14.09.2026</span></td><td><ul class="dataview dataview-ul dataview-result-list-ul"><li class="dataview-result-list-li"><span><a href="#note" class="tag" target="_blank" rel="noopener nofollow">#note</a></span></li></ul></td></tr></tbody></table></div>


