# CRTDSP settings

CRTDSP Control writes all values to the single `CRTDSP.dsp` file. Changes are picked up by the running DLL approximately every 250 ms.

## Presets

- **Clean** - restrained cabinet and room contribution; best when the game mix should remain close to the source.
- **Balanced** - the recommended starting point and the default middle ground.
- **Immersive** - stronger room, cabinet and spatial impression.

Presets only provide starting values. Applying one does not lock any parameter.

## Testing

The Testing page replaces game audio with a reference signal and routes it through the complete CRTDSP signal path.

- **Mono Pink** - checks tonal balance and whether the image is centered.
- **L / R** - checks channel assignment and stereo geometry.
- **Sweep** - exposes resonances, ringing and excessive room buildup.
- **1 kHz** - useful for matching output loudness with the DSP bypassed.
- **Stop** - restores game audio.
- **Safe Level** - reference-signal amplitude. Begin at a low system volume.

## Television

| Setting | Range | Default | Purpose |
| --- | ---: | ---: | --- |
| TV Mix | 0-1 | 0.2700 | Balance between direct audio and the television cabinet response. |
| Speaker Drive | 0-0.25 | 0.0080 | Gentle nonlinear compression and saturation from a small speaker. |
| Presence | -1-1 | 0.0800 | High-frequency presence shaping; negative values soften harsh audio. |
| CRT Whine | 0-0.5 | 0.0040 | Level of the recorded PAL line-frequency whine. Use very small values first. |
| Whine Test Gain | 0-8 | 1.000 | Temporary multiplier that makes the whine easier to calibrate. Return it to 1 afterward. |

The CRT whine is a very high-frequency sound. It is usually easier for younger listeners to notice, often only up to roughly the late teens or twenties, but this is highly individual. If you do not hear it, raise **CRT Whine** slowly. The author's personal audible calibration point is around `0.35`.

## Room

| Setting | Range | Default | Purpose |
| --- | ---: | ---: | --- |
| Room Mix | 0-0.5 | 0.0700 | Level of the late room impulse response. |
| Early Reflections | 0-0.35 | 0.0320 | Short reflections from nearby walls and furniture. |
| Room High-pass | 20-500 Hz | 110 Hz | Removes low-frequency buildup from the room path. |
| Room Low-pass | 800-18000 Hz | 5200 Hz | Darkens the room tail and reduces metallic ringing. |
| Room Ducking | 0-4 | 0.700 | Reduces room energy during loud direct audio. |

## Stereo

| Setting | Range | Default | Purpose |
| --- | ---: | ---: | --- |
| Crossfeed | 0-1 | 0.1400 | Blends channels to create a more natural center, especially on headphones. |
| Stereo Width | 0-2 | 0.880 | `1.0` preserves the original width; `0.0` is mono. |

## Output

| Setting | Range | Default | Purpose |
| --- | ---: | ---: | --- |
| Limiter Threshold | 0.75-0.99 | 0.940 | Peak protection after all processing. Values around 0.90-0.96 are recommended. |
| Output Gain | 0-2 | 0.940 | Final loudness compensation. Match it against bypass with the 1 kHz test. |

## What to adjust

Use these as practical starting points. Move values a little, listen for a few minutes, then save only when the sound still feels natural.

| Goal | Raise | Lower or watch |
| --- | --- | --- |
| More obvious TV speaker character | **TV Mix**, then a little **Speaker Drive** | Too much **Speaker Drive** can make loud games feel crushed. |
| More room/reverb | **Room Mix**, then **Early Reflections** | If the sound gets cloudy, raise **Room High-pass** or lower **Room Low-pass**. |
| Bigger sense of space | **Early Reflections**, a little **Room Mix**, lower **Stereo Width** slightly on headphones | Too much width can feel like the center disappears. |
| More headphone comfort | **Crossfeed** | If everything becomes too mono, raise **Stereo Width** back toward `1.0`. |
| Softer, darker room | Lower **Room Low-pass** | If it becomes muffled, raise **Presence** slightly. |
| Less boom or low-end buildup | **Room High-pass**, **Room Ducking** | If the room disappears, lower **Room Ducking** again. |
| More old-TV brightness or bite | **Presence**, a little **TV Mix** | If it starts hissing or hurting, lower **Presence** first. |
| More audible CRT whine | **CRT Whine** | Raise slowly. Some people will not hear it even at high values. |
| More stable loudness | Lower **Limiter Threshold**, then adjust **Output Gain** | Too low a limiter can flatten transients. |
| Closer to original game audio | Lower **TV Mix**, **Room Mix**, **Early Reflections**, **Crossfeed** | Keep **Output Gain** matched so louder is not mistaken for better. |

## Quick recipes

| Situation | Try this |
| --- | --- |
| Headphones feel too wide and artificial | Raise **Crossfeed** to `0.18-0.30`, set **Stereo Width** around `0.70-0.90`, keep **Room Mix** modest. |
| Speakers already sound roomy | Keep **Crossfeed** near `0`, lower **Room Mix**, use **TV Mix** for the cabinet effect instead. |
| Dialogue or center audio feels distant | Raise **Crossfeed** or lower **Stereo Width** a little. |
| Bass-heavy games make the room pump | Raise **Room High-pass** and **Room Ducking**. |
| Bright 8-bit games become harsh | Lower **Presence**, lower **Room Low-pass**, and keep **Speaker Drive** subtle. |
| The effect is hard to notice | Switch to **Immersive**, then pull back **Room Mix** and **Early Reflections** until it stops calling attention to itself. |

## A practical calibration order

1. Lower the system volume and select **Balanced**.
2. Use **Mono Pink** to adjust TV Mix and Presence until the tone feels natural.
3. Use **L / R** to set Crossfeed and Stereo Width.
4. Use **Sweep** to find room resonances; correct them with Room High-pass, Room Low-pass and Room Mix.
5. Stop the signal, listen to a familiar game and refine Early Reflections and Room Ducking.
6. Use **1 kHz** to match Output Gain against the unprocessed level.
7. Set CRT Whine last and keep it barely perceptible.

Headphones usually need more Crossfeed and less room energy. Speakers usually need little or no Crossfeed because the room already blends the channels acoustically.
