---
{"dg-publish":true,"permalink":"/notes/pulcina-nodarbibas/","tags":["note"],"dg-note-properties":{"categories":["[[Categories/Projects]]"],"references":["[[Notes/Datorspēļu dizains un programmēšana]]"],"tags":["note"],"created":"2026-09-14","aliases":["Pulciņa nodarbības","nodarbības","lekcijas","pulciņa lekcijas"],"cssclasses":null}}
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


<div><table class="dataview table-view-table"><thead class="table-view-thead"><tr class="table-view-tr-header"><th class="table-view-th"><span>File</span><span class="dataview small-text">1</span></th><th class="table-view-th"><span>Created</span></th><th class="table-view-th"><span>File Tags</span></th></tr></thead><tbody class="table-view-tbody"><tr><td><span><a data-tooltip-position="top" aria-label="Notes/1. Pulciņa nodarbība.md" data-href="Notes/1. Pulciņa nodarbība.md" href="Notes/1. Pulciņa nodarbība.md" class="internal-link" target="_blank" rel="noopener nofollow">1. Pulciņa nodarbība</a></span></td><td><span><ul>
<li dir="auto"></li>
</ul></span></td><td><ul class="dataview dataview-ul dataview-result-list-ul"><li class="dataview-result-list-li"><span><a href="#note" class="tag" target="_blank" rel="noopener nofollow">#note</a></span></li></ul></td></tr></tbody></table></div>
