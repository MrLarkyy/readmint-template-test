# horizon fonts

The fonts the horizon template names (`assets.fonts.*.src` is `fonts/<file>`, resolved against the design file by the CLI and the Action). Every file may be redistributed under the SIL Open Font License 1.1; the licence text of each family sits beside the files. Each file has OS/2 `fsType` 0 (installable embedding), and none of the families declares a Reserved Font Name, so the renderer embeds a subset of the glyphs a section draws. Archivo and Noto Sans come in fixed widths (SemiCondensed, ExtraCondensed are separate files), since the renderer reads static faces, not variable axes.

## Archivo (SIL Open Font License 1.1, `OFL-Archivo.txt`)

Copyright 2020 The Archivo Project Authors (https://github.com/Omnibus-Type/Archivo). The files are unmodified copies of the static instances from Omnibus-Type/Archivo at commit 211127690e8ff106c36c935f7e5e697114cff103, `fonts/ttf/`; version 2.001.

| file                                  | sha256                                                             |
| ------------------------------------- | ------------------------------------------------------------------ |
| `Archivo-Regular.ttf`                 | `59fbfd8a9bb41301bfe950e7b097fd42d52af224a07761e2c1b2c959a4c9cf9a` |
| `ArchivoExtraCondensed-Bold.ttf`      | `e09545d007d5d0e3cc7c7d42aabc6d08f74523f835d3b3477dd7037114fb33cd` |
| `ArchivoExtraCondensed-ExtraBold.ttf` | `08fcd3eba05b0ff78d9ee1873046f59408faa52c8748d2de0a3667d779cdf68e` |
| `ArchivoSemiCondensed-Medium.ttf`     | `2a8b750af2aa9d75b5559ef35f6c18644ce2480fe5f49d2075f2a449d071674c` |
| `ArchivoSemiCondensed-Regular.ttf`    | `4a809008ddf8ad523e897a4cc7d16673cde85cdc8bd1a6c1e54e874e4a03711a` |

## Noto Sans (SIL Open Font License 1.1, `OFL-Noto.txt`)

Copyright 2022 The Noto Project Authors (https://github.com/notofonts/latin-greek-cyrillic). The files are unmodified copies of the unhinted static instances from the notofonts/latin-greek-cyrillic release NotoSans-v2.015 (https://github.com/notofonts/latin-greek-cyrillic/releases/tag/NotoSans-v2.015), `NotoSans/unhinted/ttf/`; version 2.015. They are the `fallback` of every Archivo font asset: they draw the Cyrillic and Greek letters Archivo lacks (U+0400-04FF and U+0370-03FF except unassigned code points), and nothing else is drawn from them while Archivo has the glyph. The ExtraCondensed and SemiCondensed widths follow the Archivo files; the Archivo Regular text falls back to SemiCondensed too. All four name themselves "Noto Sans" in the font, so each has its own weight (400, 500, 700, 800), which keeps their embedded subsets apart.

| file                                   | sha256                                                             |
| -------------------------------------- | ------------------------------------------------------------------ |
| `NotoSans-ExtraCondensedBold.ttf`      | `6557ab3033b1bfb42882484b15e9f802731354d9c222b6abd884488061ce8be3` |
| `NotoSans-ExtraCondensedExtraBold.ttf` | `771eadab54229ab1e2413ef737e83d4fafd3f731e031931041f0d3f156177bb0` |
| `NotoSans-SemiCondensed.ttf`           | `502ac6468c79fb85d181cff3048a9fc8a6f46213e74187c4b13ee74c01bc40a6` |
| `NotoSans-SemiCondensedMedium.ttf`     | `898eee21278274c94124e7dd67bb27aa407bada6cbdedc8f2fd27777406680d9` |

## Geist and Geist Mono (SIL Open Font License 1.1, `OFL-Geist.txt`)

Copyright 2024 The Geist Project Authors (https://github.com/vercel/geist-font). The files are unmodified copies of the static instances from vercel/geist-font release v1.7.2: `Geist/ttf/` (version 1.800) and `GeistMono/ttf/` (version 1.700).

| file                    | sha256                                                             |
| ----------------------- | ------------------------------------------------------------------ |
| `GeistMono-Regular.ttf` | `42d8ad2e610238e64e8abfcde3037c63f7850a73928742b7ab7229d897bcb155` |

## Noto Sans Mono (SIL Open Font License 1.1, `OFL-Noto.txt`, shared with Noto Sans above)

Copyright 2022 The Noto Project Authors (https://github.com/notofonts/latin-greek-cyrillic). The file is an unmodified copy of the unhinted static instance from the notofonts/latin-greek-cyrillic release NotoSansMono-v2.014 (https://github.com/notofonts/latin-greek-cyrillic/releases/tag/NotoSansMono-v2.014), `NotoSansMono/unhinted/ttf/`; version 2.014, 388,660 bytes. It is the `fallback` of every Geist Mono font asset: it draws the Latin Extended-A, Cyrillic and Greek letters Geist Mono lacks, on the same 0.6 em advance as Geist Mono, and nothing else is drawn from it while Geist Mono has the glyph. Emoji, CJK and the scripts of other writing systems are in none of the fonts and are dropped with a `missing-glyph` warning.

| file                       | sha256                                                             |
| -------------------------- | ------------------------------------------------------------------ |
| `NotoSansMono-Regular.ttf` | `87f8ce0522a6c99b743ee5fc75b4073cfdd575639119672828b7b9944b65b4f4` |

A test checks that every font a section names is a file here, declares `embedding: "allowed"` and `OFL-1.1`, and that its sha256 is listed in this file. To set a template in your own font, replace the `src`, `family` and `licence` of the font assets with a file you may embed.
