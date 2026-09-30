# ClassAudio

Interactive teaching pages for sound synthesis. Open `index.html` for the landing page that links to all three parts.

## Waves & Harmonics — `waves.html`

A single-file guide (no build step, no dependencies) that shows a wave and its
spectrum side by side and lets students hear it:

1. **Reading the display**: time domain vs. frequency domain (Fourier).
2. **Oscillator**: sine, triangle, square and saw, and their harmonic recipes.
3. **Additive synthesis**: 16 drawable harmonic faders, presets, phase flips, and a "build" animation that adds harmonics one at a time.
4. **FM synthesis**: carrier, C:M ratio and modulation index, with Bessel-function sidebands and Carson bandwidth.
5. **Filters**: low/high/band pass, 12/24 dB slope, resonance, and a cutoff sweep. Pre-filter bars and wave stay visible in grey.
6. **Quick reference**: tables and a glossary.

The graphs are calculated from the exact Fourier series, Bessel functions and
Web Audio biquad formulas, so they stay steady on a projector. The sound comes from
the Web Audio API using the same parameters.

Open any page in a browser, or serve the folder with GitHub Pages.

## Sound Microscope — `analyze.html`

Load a recording of a single note (or one of three synthetic examples) and take it apart:

1. **Load**: drag and drop or pick a file. It is decoded and analysed locally; nothing is uploaded.
2. **Envelope**: attack time, two-stage (early/late) decay fit, T60, tremolo rate and depth.
3. **Spectrogram**: log-frequency STFT, with hover readout.
4. **Harmonics at the cursor**: 16384-point FFT, per-harmonic frequency, cents from ideal, level, decay, T60; inharmonicity coefficient B, odd/even balance, harmonic-energy share.
5. **Harmonic decay**: levels of harmonics 1–8 over time (bark, beating).
6. **Pitch & brightness**: YIN pitch track in cents and spectral centroid.
7. **Resynthesis**: compare static vs. tracked additive rebuilds with the original.
8. **How deep can we go**: what is measurable, what makes a Rhodes hard to simulate, and the limits.

## Colour & Saturation — `effects.html`

What effects do to a wave and its harmonics. Each lab shows the wave (input vs. output), the device curve and the spectrum, with live sound:

1. **Three kinds of change**: linear, non-linear and time-varying.
2. **Overdrive**: soft, hard and fuzz curves, drive, asymmetry (even harmonics), two-tone intermodulation (fifth vs. third), and aliasing with 1×/4× oversampling.
3. **Transformer**: flux-based core saturation that grows as the pitch drops, a hysteresis B–H loop, and DC bias.
4. **Tape**: hysteresis saturation, head bump and treble loss per tape speed, wow & flutter sidebands, and hiss.
5. **Chorus & flanger**: modulated delay voices, feedback comb filtering, presets.
6. **The Rhodes chain**: preamp → transformer → tape → chorus on a built-in e-piano phrase or your own audio file.
7. **Quick reference** and glossary.
