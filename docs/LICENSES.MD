# Credits, sources and licenses

This document records the third-party material used by CRTDSP 1.1 and the provenance currently available for its embedded audio resources.

## CRT whine recording

- **Work:** [CRT TV Whine](https://freesound.org/people/Fission9/sounds/693863/)
- **Creator:** Fission9
- **Source:** Freesound, sound ID 693863
- **Subject:** 14-inch PAL JVC CRT television, recorded on a Zoom H4n Pro in 2023
- **License:** [Creative Commons CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/)
- **CRTDSP use:** edited, resampled and embedded in `CRTDSP.dll`

The creator's credit and subject were also preserved in the WAV INFO metadata. CC0 does not require attribution; it is included here to preserve provenance and thank the creator.

## Television and room impulse responses

CRTDSP embeds processed `tv.wav` and `room.wav` impulse responses. Their original source information has been lost, so no reliable author, URL or license can be stated at this time. The sources will be recovered later and added to this document when available.

Their SHA-256 hashes are recorded below so the exact files used in CRTDSP 1.1 can be matched if the original source information is recovered.

### Embedded audio fingerprints

| Source file | SHA-256 |
| --- | --- |
| `tv.wav` | `532752E8BF25A71CEA7037A9E6DE0D588C227DE96122066D3011E2B033A1CE61` |
| `room.wav` | `8310A8EF3D7FF8154AB3FBA72E2252837CE4C69B38EB80325FD88CE1C313B10C` |
| `whine.wav` | `BED03D4F7426A5BFA14036D9B9D88F5420FCA29D20963785A989F8FBB2264C36` |

## TDAText

- **Project:** [TDAText](https://github.com/tinelix/TDAText)
- **Creator/maintainer:** tinelix and TDAText contributors
- **Description:** teletext-style typeface based on Philips SAA52XX/SAA55XX/TDA93XX character sets
- **License:** [SIL Open Font License 1.1](https://github.com/tinelix/TDAText/blob/main/LICENSE.TXT)
- **CRTDSP use:** embedded in CRTDSP Control and used for the service-menu interface and logo

The font name, project link and license are preserved here as required attribution and redistribution information. CRTDSP does not claim authorship of TDAText.

## RetroArch and libretro

CRTDSP is a third-party DSP plugin designed for [RetroArch](https://github.com/libretro/RetroArch) and its DSP filter interface. RetroArch is distributed under the [GNU General Public License v3.0](https://github.com/libretro/RetroArch/blob/master/COPYING). RetroArch and libretro names belong to their respective project contributors. CRTDSP is not affiliated with or endorsed by them.

## Project artwork

The CRTDSP logo and CRTDSP Control screenshot in `assets/` were created specifically for this project. The logo uses the TDAText typeface, whose license and source are listed above.
