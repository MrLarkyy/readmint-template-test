# year-ring fonts

The fonts the year-ring template names (`assets.fonts.*.src` is `fonts/<file>`, resolved against the design file by the CLI and the Action). Every file may be redistributed under the SIL Open Font License 1.1; the licence text of each family sits beside the files. Each file has OS/2 `fsType` 0 (installable embedding), and none of the families declares a Reserved Font Name, so the renderer embeds a subset of the glyphs a section draws. Archivo and Noto Sans come as static files per weight and width, since the renderer reads static faces, not variable axes.

## Archivo (SIL Open Font License 1.1, `OFL-Archivo.txt`)

Copyright 2020 The Archivo Project Authors (https://github.com/Omnibus-Type/Archivo). The files are unmodified copies of the static instances from Omnibus-Type/Archivo at commit 211127690e8ff106c36c935f7e5e697114cff103, `fonts/ttf/`; version 2.001.

| file                               | sha256                                                             |
| ---------------------------------- | ------------------------------------------------------------------ |
| `Archivo-Regular.ttf`              | `59fbfd8a9bb41301bfe950e7b097fd42d52af224a07761e2c1b2c959a4c9cf9a` |
| `Archivo-SemiBold.ttf`             | `6598b6ed816158767a7633bdfb01d78daf54cab4cd4d9d3cc0cfd995f4723083` |
| `ArchivoSemiExpanded-Light.ttf`    | `a087944105c257e858dd07276b0eebcb7156d9b019f5ce987aecde46d94dbe3e` |
| `ArchivoSemiExpanded-Medium.ttf`   | `9a1fd6e876fed3e84fb774955c9c016670a447133df9368e995b6ad1f0594620` |
| `ArchivoSemiExpanded-SemiBold.ttf` | `8a367e289ebd27af7e16f15678f9d308426daf091300139e0f121ab052da3e64` |

## Noto Sans (SIL Open Font License 1.1, `OFL-Noto.txt`)

Copyright 2022 The Noto Project Authors (https://github.com/notofonts/latin-greek-cyrillic). The files are unmodified copies of the unhinted static instances from the notofonts/latin-greek-cyrillic release NotoSans-v2.015 (https://github.com/notofonts/latin-greek-cyrillic/releases/tag/NotoSans-v2.015), `NotoSans/unhinted/ttf/`; version 2.015. They are the `fallback` of every Archivo font asset: they draw the Cyrillic and Greek letters Archivo lacks (U+0400-04FF and U+0370-03FF except unassigned code points), and nothing else is drawn from them while Archivo has the glyph. Light, Medium, Regular and SemiBold follow the weights of the Archivo files (the SemiBold one serves both Archivo SemiBold assets).

| file                    | sha256                                                             |
| ----------------------- | ------------------------------------------------------------------ |
| `NotoSans-Light.ttf`    | `8897d5cba2567d06d437b1de90b65d37ea4c4b40db6b8979ea26d8789ce6e030` |
| `NotoSans-Medium.ttf`   | `220e74546aee1b9a17cd50025dd917a064d0224e653f562287446c2328e4160b` |
| `NotoSans-Regular.ttf`  | `f3961a9cde016d41a4879aecda1474d3a36d6bf54fa0e4643de029cc2248b0e8` |
| `NotoSans-SemiBold.ttf` | `a7af8d4a11e8e49fea9a19786a6469210b512cd4061413e8036bdd2425722795` |

A test checks that every font a section names is a file here, declares `embedding: "allowed"` and `OFL-1.1`, and that its sha256 is listed in this file. To set a template in your own font, replace the `src`, `family` and `licence` of the font assets with a file you may embed.
