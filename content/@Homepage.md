---
created: 2025-10-03
updated: 2025-10-03
dg-home: true
dg-publish: true
cssclasses:
  - cards
  - cards-cols-4
---
- [[@Atomic]]
- [[@About]]
- [[@Dictionary]]
- [[@Project]]
- [[@Foundation]]
- [[@Level1]]
- [[@Finance]]
- [[@Language]]
- [[@Anecdote]]

```base
views:
  - type: table
    name: Table
    filters:
      and:
        - file.hasTag("textbook/note")
    order:
      - file.name
      - draft

```