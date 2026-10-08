# Sound Field Guide

An interactive reference for sound: synthesis, analysis, effects and digital audio. Open `index.html` for the front page: a contents list of the four volumes and an A–Z index of terms, each with a short definition and a link to the chapter where you can see and hear it.

## Waves & Harmonics — `waves.html`

A single-file guide (no build step, no dependencies) that shows a wave and its
spectrum side by side and lets students hear it:

1. **Reading the display**: time domain vs. frequency domain (Fourier).
2. **Oscillator**: sine, triangle, square and saw, and their harmonic recipes.
3. **Additive synthesis**: 16 drawable harmonic faders, basic-wave presets, instrument recipes (organ, flute, clarinet, oboe, sax, trumpet, violin, cello), phase flips, and a "build" animation that adds harmonics one at a time.
4. **FM synthesis**: carrier, C:M ratio and modulation index, with Bessel-function sidebands and Carson bandwidth.
5. **Filters**: low/high/band pass, 12/24 dB slope, resonance, and a cutoff sweep. Pre-filter bars and wave stay visible in grey.
6. **Quick reference**: tables and a glossary.

The graphs are calculated from the exact Fourier series, Bessel functions and
Web Audio biquad formulas, so they stay steady on a projector. The sound comes from
the Web Audio API using the same parameters.

Open any page in a browser, or serve the folder with GitHub Pages.

## Sound Microscope — `analyze.html`

Load a recording of a single note (or one of five synthetic examples: piano string, plucked string, bowed cello, trumpet, e-piano) and take it apart:

1. **Load**: drag and drop or pick a file. It is decoded and analysed locally; nothing is uploaded.
2. **Envelope**: attack time, two-stage (early/late) decay fit, T60, tremolo rate and depth.
3. **Spectrogram**: log-frequency STFT, with hover readout.
4. **Harmonics at the cursor**: 16384-point FFT, per-harmonic frequency, cents from ideal, level, decay, T60; inharmonicity coefficient B, odd/even balance, harmonic-energy share.
5. **Harmonic decay**: levels of harmonics 1–8 over time (bark, beating).
6. **Pitch & brightness**: YIN pitch track in cents and spectral centroid.
7. **Resynthesis**: compare static vs. tracked additive rebuilds with the original.
8. **From simulation to sound**: paste a modal (FEA) mode list with energies, get each mode's stiffness and effective mass, a hammer-impulse level estimate, Rayleigh damping from two T60 knobs, static and dynamic plots, playback, and a hand-off to the analysis chapters.
9. **How deep can we go**: what is measurable, what makes pianos, brass, bowed strings, flutes, guitars and the Rhodes hard to simulate, and the limits.

## Colour & Saturation — `effects.html`

What effects do to a wave and its harmonics. Each lab shows the wave (input vs. output), the device curve and the spectrum, with live sound:

1. **Three kinds of change**: linear, non-linear and time-varying.
2. **Overdrive**: soft, hard and fuzz curves, drive, asymmetry (even harmonics), two-tone intermodulation (fifth vs. third), and aliasing with 1×/4× oversampling.
3. **Transformer**: flux-based core saturation that grows as the pitch drops, a hysteresis B–H loop, and DC bias.
4. **Tape**: hysteresis saturation, head bump and treble loss per tape speed, wow & flutter sidebands, and hiss.
5. **Chorus & flanger**: modulated delay voices, feedback comb filtering, presets.
6. **The Rhodes chain**: preamp → transformer → tape → chorus on a built-in e-piano phrase or your own audio file.
7. **Quick reference** and glossary.

## Digital Sound — `digital.html`

How sound becomes numbers and back, with a lab in every chapter:

1. **The digital chain**: microphone → anti-alias filter → ADC → DSP → DAC → reconstruction filter → speaker.
2. **Sampling**: sample rate, Nyquist, aliasing (with a 100 Hz → 20 kHz sweep), the anti-alias filter, and stepped vs. reconstructed DAC output.
3. **Bit depth**: quantization steps and error, 6 dB per bit, low-level distortion, and TPDF dither. You can listen to the error on its own.
4. **Inside the ADC**: a step-by-step successive-approximation converter, plus how sigma-delta converters work.
5. **Inside the DAC**: an 8-bit binary-weighted DAC with clickable bits, the R–2R ladder, and the reconstruction filter.
6. **DSP**: moving average (FIR), one-pole (IIR), difference and echo, with impulse and frequency response, operation counts, and buffer latency.
7. **MIDI**: an on-screen keyboard (mouse or computer keys) or a real MIDI device via Web MIDI. Every message is decoded byte by byte, with a piano roll and a small synth.
8. **Anatomy of a .wav file**: a live hex inspector of a generated file (rate, bit depth, channels, content), or of your own .wav. It explains every RIFF / fmt / data field, little-endian numbers, interleaved frames and extra chunks (LIST, bext, iXML…), and can download the file.
9. **Quick reference**: formats, formulas and a glossary.
