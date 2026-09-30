# ClassAudio

Interactive teaching pages for sound synthesis.

## Waves & Harmonics — `index.html`

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

Open `index.html` in a browser, or serve it with GitHub Pages.
