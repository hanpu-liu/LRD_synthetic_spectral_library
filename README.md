# Synthetic Spectral Library of Optically Thick Atmospheres for Little Red Dots (LRDs)

Described in: H. Liu, Y.-F. Jiang, E. Quataert, J. E. Greene, Y. Ma, X. Lin (2026),
"Synthetic Spectral Library of Optically Thick Atmospheres for Little Red Dots,"
*ApJ*, [arXiv:2603.02317](https://arxiv.org/abs/2603.02317).
DOI: [to be added upon publication]

## Contents

- `specs/` — Directory containing synthetic spectra computed with TLUSTY (v208) and
  SYNSPEC (v54). Each file is a synthetic spectrum of an optically thick atmosphere,
  parameterized by effective temperature T_eff (in K), surface gravity log g (in cm/s²),
  metallicity [M/H], and microturbulence velocity ξ_mtb (in km/s). Files are in ASCII two-column format (wavelength in Å, flux in erg/s/cm²/Å).
  Wavelength range: 2000–40000 Å (rest-frame).

- `modelstats.csv` — Table listing parameters of all synthetic spectra: T_eff (K),
  log g (cm/s²), [M/H], ξ_mtb (km/s), photosphere density ρ_ph (g/cm³), and derived
  magnitudes in seven synthetic photometric bands (B̃, R̃₁, R̃₂, Z̃, J̃, H̃, K̃).
  Column units are given in the CSV header.

- `example.ipynb` — Jupyter notebook demonstrating how to load and visualize the
  spectral library. Requires Python with numpy, matplotlib, and astropy (see notebook
  for version details).

## Parameter coverage

- T_eff: 2000–7500 K (densest at 4500–5000 K)
- log g: −4 to +1.5 (cm/s²); see paper for "hydrostatic" vs "no-g_rad" model regimes
- [M/H]: −2, −1, 0
- ξ_mtb: 2 km/s (all models); 10 km/s (subset: hydrostatic and 4000–5000 K and [M/H] = −1)

## How to use

Open `example.ipynb` in Jupyter. The notebook explains the file structure and provides
visualization examples. The library can be used to fit LRD spectra as described in the
associated paper.

## License

This dataset is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Contact

We welcome any questions related to the library or requests for additional parameter coverage: hanpu.liu@princeton.edu