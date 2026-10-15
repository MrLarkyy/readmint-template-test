# pinscreen fonts

The fonts the pinscreen template names (`assets.fonts.*.src` is `fonts/<file>`, resolved against the design file by the CLI and the Action). Every file may be redistributed under the SIL Open Font License 1.1; the licence text of each family sits beside the files. Each file has OS/2 `fsType` 0 (installable embedding), and none of the families declares a Reserved Font Name, so the renderer embeds a subset of the glyphs a section draws. Archivo comes in fixed widths (SemiExpanded, SemiCondensed, ExtraCondensed are separate files), since the renderer reads static faces, not variable axes.

## Geist and Geist Mono (SIL Open Font License 1.1, `OFL-Geist.txt`)

Copyright 2024 The Geist Project Authors (https://github.com/vercel/geist-font). The files are unmodified copies of the static instances from vercel/geist-font release v1.7.2: `Geist/ttf/` (version 1.800) and `GeistMono/ttf/` (version 1.700).

| file                    | sha256                                                             |
| ----------------------- | ------------------------------------------------------------------ |
| `Geist-Regular.ttf`     | `5c8968eafb98a4c4f47033daf29e38e284a6f2a82eb017d171ab040fe7c4b615` |
| `Geist-SemiBold.ttf`    | `612ec98df33935354f39e81e54101656961ab6e5549f64b63eb57868ba7bab8d` |
| `GeistMono-Regular.ttf` | `42d8ad2e610238e64e8abfcde3037c63f7850a73928742b7ab7229d897bcb155` |

A test checks that every font a section names is a file here, declares `embedding: "allowed"` and `OFL-1.1`, and that its sha256 is listed in this file. To set a template in your own font, replace the `src`, `family` and `licence` of the font assets with a file you may embed.
