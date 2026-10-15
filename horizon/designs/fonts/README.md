# horizon fonts

The fonts the horizon template names (`assets.fonts.*.src` is `fonts/<file>`, resolved against the design file by the CLI and the Action). Every file may be redistributed under the SIL Open Font License 1.1; the licence text of each family sits beside the files. Each file has OS/2 `fsType` 0 (installable embedding), and none of the families declares a Reserved Font Name, so the renderer embeds a subset of the glyphs a section draws. Archivo comes in fixed widths (SemiExpanded, SemiCondensed, ExtraCondensed are separate files), since the renderer reads static faces, not variable axes.

## Archivo (SIL Open Font License 1.1, `OFL-Archivo.txt`)

Copyright 2020 The Archivo Project Authors (https://github.com/Omnibus-Type/Archivo). The files are unmodified copies of the static instances from Omnibus-Type/Archivo at commit 211127690e8ff106c36c935f7e5e697114cff103, `fonts/ttf/`; version 2.001.

| file                                  | sha256                                                             |
| ------------------------------------- | ------------------------------------------------------------------ |
| `Archivo-Regular.ttf`                 | `59fbfd8a9bb41301bfe950e7b097fd42d52af224a07761e2c1b2c959a4c9cf9a` |
| `ArchivoExtraCondensed-Bold.ttf`      | `e09545d007d5d0e3cc7c7d42aabc6d08f74523f835d3b3477dd7037114fb33cd` |
| `ArchivoExtraCondensed-ExtraBold.ttf` | `08fcd3eba05b0ff78d9ee1873046f59408faa52c8748d2de0a3667d779cdf68e` |
| `ArchivoSemiCondensed-Medium.ttf`     | `2a8b750af2aa9d75b5559ef35f6c18644ce2480fe5f49d2075f2a449d071674c` |
| `ArchivoSemiCondensed-Regular.ttf`    | `4a809008ddf8ad523e897a4cc7d16673cde85cdc8bd1a6c1e54e874e4a03711a` |

## Geist and Geist Mono (SIL Open Font License 1.1, `OFL-Geist.txt`)

Copyright 2024 The Geist Project Authors (https://github.com/vercel/geist-font). The files are unmodified copies of the static instances from vercel/geist-font release v1.7.2: `Geist/ttf/` (version 1.800) and `GeistMono/ttf/` (version 1.700).

| file                    | sha256                                                             |
| ----------------------- | ------------------------------------------------------------------ |
| `GeistMono-Regular.ttf` | `42d8ad2e610238e64e8abfcde3037c63f7850a73928742b7ab7229d897bcb155` |

A test checks that every font a section names is a file here, declares `embedding: "allowed"` and `OFL-1.1`, and that its sha256 is listed in this file. To set a template in your own font, replace the `src`, `family` and `licence` of the font assets with a file you may embed.
