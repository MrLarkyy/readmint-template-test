# year-ring fonts

The fonts the year-ring template names (`assets.fonts.*.src` is `fonts/<file>`, resolved against the design file by the CLI and the Action). Every file may be redistributed under the SIL Open Font License 1.1; the licence text of each family sits beside the files. Each file has OS/2 `fsType` 0 (installable embedding), and none of the families declares a Reserved Font Name, so the renderer embeds a subset of the glyphs a section draws. Archivo comes in fixed widths (SemiExpanded, SemiCondensed, ExtraCondensed are separate files), since the renderer reads static faces, not variable axes.

## Archivo (SIL Open Font License 1.1, `OFL-Archivo.txt`)

Copyright 2020 The Archivo Project Authors (https://github.com/Omnibus-Type/Archivo). The files are unmodified copies of the static instances from Omnibus-Type/Archivo at commit 211127690e8ff106c36c935f7e5e697114cff103, `fonts/ttf/`; version 2.001.

| file                               | sha256                                                             |
| ---------------------------------- | ------------------------------------------------------------------ |
| `Archivo-Regular.ttf`              | `59fbfd8a9bb41301bfe950e7b097fd42d52af224a07761e2c1b2c959a4c9cf9a` |
| `Archivo-SemiBold.ttf`             | `6598b6ed816158767a7633bdfb01d78daf54cab4cd4d9d3cc0cfd995f4723083` |
| `ArchivoSemiExpanded-Light.ttf`    | `a087944105c257e858dd07276b0eebcb7156d9b019f5ce987aecde46d94dbe3e` |
| `ArchivoSemiExpanded-Medium.ttf`   | `9a1fd6e876fed3e84fb774955c9c016670a447133df9368e995b6ad1f0594620` |
| `ArchivoSemiExpanded-SemiBold.ttf` | `8a367e289ebd27af7e16f15678f9d308426daf091300139e0f121ab052da3e64` |

A test checks that every font a section names is a file here, declares `embedding: "allowed"` and `OFL-1.1`, and that its sha256 is listed in this file. To set a template in your own font, replace the `src`, `family` and `licence` of the font assets with a file you may embed.
