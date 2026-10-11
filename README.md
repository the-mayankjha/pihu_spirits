# PIHU Spirits Registry

This repository contains downloadable, non-executable Spirit packages for PIHU OS. Each package consists of a declarative `spirit.json` manifest and a PNG sprite sheet.

## Registry

`index.json` lists every package, version, relative manifest and sprite-sheet path, size, and SHA-256 digest. The PIHU OS Spirits catalog reads this index and verifies each sprite sheet before installing it into the user's local Spirit library.

## Package layout

```text
index.json
spirits/<id>/spirit.json
spirits/<id>/spritesheet-extended.png
```

Spirit packages contain artwork only. They do not include scripts, executables, package hooks, or shell commands.
