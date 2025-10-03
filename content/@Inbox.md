```base
filters:
  and:
    - '!file.inFolder("99 Extension")'
views:
  - type: table
    name: Active
    filters:
      and:
        - status.contains("Active")
    order:
      - file.name
      - up
    columnSize:
      file.name: 429

```

```base
filters:
  and:
    - '!file.inFolder("99 Extension")'
views:
  - type: table
    name: Pending
    filters:
      and:
        - status.contains("Pending")
    order:
      - file.name
      - up
    columnSize:
      file.name: 429

```