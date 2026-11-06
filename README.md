# Optical Communication Labs

Interactive labs and short animations for **Optical Communication (83-466)**, Faculty of Engineering, Bar-Ilan University. Lecturer: Dr. Boris Desiatov.

**Live site:** https://dboriska.github.io/optical-course/

Each lab is a single HTML page that runs in any browser, on a laptop or a phone, with no installation and no server. Students change the parameters with sliders and see the physics from the lecture slides update live.

## How the site is organized

| Page | What it is |
|---|---|
| `index.html` | Home page: one square tile per lecture |
| `lecture-02.html` … `lecture-06.html` | One page per lecture, listing its labs with a short description |
| `*.html` in the root | The labs themselves. The home page and lecture pages link to these. |
| `lecture02/` … `lecture06/` | A copy of each lecture's labs, plus a `movies/` folder with the animations for slides |

The labs in the root and in the lecture folders are identical copies. Both work on their own.

## Labs by lecture

### Lecture 02 · Optical Fibers
| Lab | Movie |
|---|---|
| [Snell's Law Lab](snell-lab.html): refraction, critical angle, total internal reflection, Fresnel reflectance | `snell-law-animation.mp4` |
| [Acceptance Cone and NA Lab](acceptance-cone-lab.html): guided and escaping rays, the acceptance cone in 3D | `acceptance-cone-animation.mp4` |
| [Graded-Index Ray Race](graded-index-race.html): step-index vs graded-index fiber, ray turning points n(x) = β | `graded-index-race.mp4`, `turning-point.mp4` |

### Lecture 03 · Modes of Optical Fibers
| Lab | Movie |
|---|---|
| [V Number and Mode Chart Lab](v-number-lab.html): V number, cutoff wavelength, guided modes on the b–V chart | `v-number-mode-chart.mp4` |
| [Spot Size Lab](spot-size-lab.html): exact fundamental mode vs Gaussian approximation, MFD, effective area | `spot-size.mp4` |

### Lecture 04 · Chromatic Dispersion
| Lab | Movie |
|---|---|
| [Crest vs Envelope](crest-vs-envelope.html): one wave packet, phase and group velocity | `crest-vs-envelope.mp4` |
| [Phase vs Group Velocity](phase-vs-group-velocity.html): two waves, beats, the ω–k diagram | `vp-vg-explainer.mp4` |
| [Phase and Group Velocity Lab](group-velocity-lab.html): n and n_g of silica, delay of a fiber | `group-velocity.mp4` |
| [Pulse Spreading Lab](pulse-spreading-lab.html): ΔT = \|D\|·L·Δλ, neighbouring bits start to overlap | `pulse-spreading.mp4` |
| [Rate and Reach Map](rate-reach-map.html): modal vs chromatic dispersion limits on bit rate and distance | `rate-reach.mp4` |

### Lecture 05 · Pulse Dispersion and Chirp
| Lab | Movie |
|---|---|
| [Gaussian Pulse Dispersion in Fiber](gaussian-pulse-dispersion.html): L_D = T₀²/\|β₂\|, T₁(z), energy conservation, compare mode, chirp, bit stream and ISI | `pulse-fiber.mp4` |
| [Chirp Lab](chirp-lab.html): initial chirp C₀, compression and broadening | `chirp-lab.mp4` |
| [Two-Fiber Pulse Lab](two-fiber-pulse-lab.html): SMF then DCF, swap the order of the fibers | `two-fiber.mp4` |
| [DCF and DSP Lab](dcf-dsp-lab.html): optical vs electronic dispersion compensation | `dcf-dsp.mp4` |
| [Link Length Calculator](link-length-calculator.html): is the link limited by loss or by dispersion? | `link-calc.mp4` |
| [Undo the Fiber](undo-the-fiber.html): a game, compensate an unknown length of fiber | `undo-fiber.mp4` |
| [Signal Bandwidth Lab](signal-bandwidth-lab.html): FFT of sine, square, triangle and Gaussian signals, bandwidth, low-pass filter, the band around the 193 THz carrier | `bandwidth.mp4` |

`lecture05/movies/` also holds animations for labs that are not on the site yet: dispersion map (`disp-map.mp4`), source vs signal width (`src-width.mp4`) and third-order dispersion (`beta3.mp4`).

### Lecture 06 · Semiconductor Lasers
| Lab | Movie |
|---|---|
| [Einstein's Three Processes](einstein-processes.html): absorption, spontaneous and stimulated emission | `einstein.mp4` |
| [Three Processes animation](three-processes-animation.html) | `three-processes.mp4` |
| [Direct vs Indirect Band Gap](direct-indirect-gap-animation.html) | `direct-indirect-gap.mp4` |
| [III-V Materials Lab](iii-v-materials.html): InGaAsP lattice matched to InP, 1310 and 1550 nm | `iii-v.mp4` |
| [Semiconductor Gain Lab](semiconductor-gain-lab.html): gain spectrum vs carrier density, transparency | `gain-lab.mp4` |
| [Laser Cavity Lab](laser-cavity-lab.html): Fabry–Perot modes, threshold, gain clamping | `laser-cavity.mp4` |
| [Bragg Grating animation](bragg-grating-animation.html): DFB laser grating | `bragg-grating.mp4` |

## About the labs

- **Physics first.** Each lab follows the formulas on the lecture slides, and each page ends with a note that states the model and its assumptions.
- **No presets.** Students set the parameters themselves. Fiber presets appear only where the lecturer asked for them.
- **Movies for the slides.** Every lab has a presentation mode: add `#demo` to the address (for example `chirp-lab.html#demo`) to play the full-screen animation with captions. The `.mp4` files in `movies/` are recordings of that mode, ready to drop into PowerPoint.
- **Credit.** Every animation and movie carries "Bar-Ilan University 2026 · Optical Communication 83-466 · Dr. Boris Desiatov".
- **Self-contained.** All code is inside each HTML file. The only external resources are Google Fonts, KaTeX (formulas in the Gaussian pulse lab) and the GoatCounter visit counter.

## Updating the site

1. Edit or add the lab HTML in the repository root.
2. Copy the same file into its `lectureNN/` folder so both copies stay identical.
3. Add the lab to its lecture page (`lecture-NN.html`). For a new lecture, add a tile to `index.html` and a new lecture page.
4. Push to `main`. GitHub Pages publishes the site within a minute or two.
