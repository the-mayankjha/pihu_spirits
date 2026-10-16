# PIHU Spirits Registry

This repository contains downloadable, non-executable Spirit packages for PIHU OS. Packages include the artwork used by the desktop renderer: the extended sprite atlas, optional listening and thinking state strips, TTS viseme frames, listening animation strips, and social interaction frame sequences.

## Registry

`index.json` lists each Spirit, its manifest and main sprite sheet, plus a SHA-256 digest and byte size for every shipped file. `spirits/<id>/spirit.json` identifies the package assets and supported renderer features. Set `deprecated` to `true` in the manifest or index entry to prevent the Spirit from being added to Pihu; it defaults to `false`. The desktop Spirits catalog reads the index and verifies the main sprite sheet before installing it into the local Spirit library.

## Package layout

```text
index.json
spirits/<id>/spirit.json
spirits/<id>/spritesheet-extended.png
spirits/<id>/states/                  # optional listening/thinking strips
spirits/<id>/final/tts-visemes/       # optional speech mouth frames
spirits/<id>/interactions/            # optional listening/social animations
```

Only runtime-consumed artwork is published. Image-generation prompts, source/reference art, QA reports, previews, and intermediate raw frames remain in the application source tree. Packages contain artwork and declarative metadata only; they do not include scripts, executables, package hooks, or shell commands.
