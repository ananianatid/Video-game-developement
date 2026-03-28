---
tags: [person]
firstname:
lastname:
email:
phone: "00228000000"
created: "{{date}}"
type: person
---

```base
filters:
  or:
    - author == this.file
    - collaborators.contains(this.file)
    - lecturer == this.file
views:
  - type: table
    name: Table
```
