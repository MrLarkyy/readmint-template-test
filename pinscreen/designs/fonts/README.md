# pinscreen fonts

The fonts the pinscreen template names (`assets.fonts.*.src` is `fonts/<file>`, resolved against the design file by the CLI and the Action). Every file may be redistributed under the SIL Open Font License 1.1; the licence text of each family sits beside the files. Each file has OS/2 `fsType` 0 (installable embedding), and none of the families declares a Reserved Font Name, so the renderer embeds a subset of the glyphs a section draws. Geist, Geist Mono and Noto come as static files per weight, since the renderer reads static faces, not variable axes.

## Geist and Geist Mono (SIL Open Font License 1.1, `OFL-Geist.txt`)

Copyright 2024 The Geist Project Authors (https://github.com/vercel/geist-font). The files are unmodified copies of the static instances from vercel/geist-font release v1.7.2: `Geist/ttf/` (version 1.800) and `GeistMono/ttf/` (version 1.700).

| file                    | sha256                                                             |
| ----------------------- | ------------------------------------------------------------------ |
| `Geist-Regular.ttf`     | `5c8968eafb98a4c4f47033daf29e38e284a6f2a82eb017d171ab040fe7c4b615` |
| `Geist-SemiBold.ttf`    | `612ec98df33935354f39e81e54101656961ab6e5549f64b63eb57868ba7bab8d` |
| `GeistMono-Regular.ttf` | `42d8ad2e610238e64e8abfcde3037c63f7850a73928742b7ab7229d897bcb155` |

## Noto Sans and Noto Sans Mono (SIL Open Font License 1.1, `OFL-Noto.txt`)

Noto Sans: copyright 2022 The Noto Project Authors (https://github.com/notofonts/latin-greek-cyrillic). The files are unmodified copies of the unhinted static instances from the notofonts/latin-greek-cyrillic release NotoSans-v2.015 (https://github.com/notofonts/latin-greek-cyrillic/releases/tag/NotoSans-v2.015), `NotoSans/unhinted/ttf/`; version 2.015, byte-equal to the files of year-ring. They are the `fallback` of the Geist font assets: they draw the Latin Extended-A, Cyrillic and Greek letters Geist lacks, in the weight of the Geist file (Regular for 400, SemiBold for 600).

Noto Sans Mono: copyright 2022 The Noto Project Authors (https://github.com/notofonts/latin-greek-cyrillic). The file is an unmodified copy of the unhinted static instance from the notofonts/latin-greek-cyrillic release NotoSansMono-v2.014 (https://github.com/notofonts/latin-greek-cyrillic/releases/tag/NotoSansMono-v2.014), `NotoSansMono/unhinted/ttf/`; version 2.014, 388,660 bytes. It is the `fallback` of every Geist Mono font asset: it draws the Latin Extended-A, Cyrillic and Greek letters Geist Mono lacks, on the same 0.6 em advance as Geist Mono, and nothing else is drawn from it while Geist Mono has the glyph. Emoji, CJK and the scripts of other writing systems are in none of the fonts and are dropped with a `missing-glyph` warning.

| file                       | sha256                                                             |
| -------------------------- | ------------------------------------------------------------------ |
| `NotoSans-Regular.ttf`     | `f3961a9cde016d41a4879aecda1474d3a36d6bf54fa0e4643de029cc2248b0e8` |
| `NotoSans-SemiBold.ttf`    | `a7af8d4a11e8e49fea9a19786a6469210b512cd4061413e8036bdd2425722795` |
| `NotoSansMono-Regular.ttf` | `87f8ce0522a6c99b743ee5fc75b4073cfdd575639119672828b7b9944b65b4f4` |

A test checks that every font a section names is a file here, declares `embedding: "allowed"` and `OFL-1.1`, and that its sha256 is listed in this file. To set a template in your own font, replace the `src`, `family` and `licence` of the font assets with a file you may embed.
