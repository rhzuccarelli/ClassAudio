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
