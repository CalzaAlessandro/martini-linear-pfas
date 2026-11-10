<h1 align="center">Martini 3 models for linear PFAS</h1>

This repository contains Martini 3 linear PFAS models (carboxylates and sulfonates) plus
ready-to-run simulation systems and analysis outputs for PFAS and emerging contaminants mixtures, PFOA critical micelle concentration, PFAS vesicle formation,
and PFAS adsorption on graphene.

<p align="center">
  <a href="https://doi.org/10.5281/zenodo.22033083"><img src="https://img.shields.io/badge/Archive-10.5281%2Fzenodo.22033083-2457A7?style=flat" alt="Archive DOI: 10.5281/zenodo.22033083"></a>
  <a href="https://doi.org/10.1021/acs.jctc.6c00250"><img src="https://img.shields.io/badge/DOI-10.1021%2Facs.jctc.6c00250-2457A7?style=flat" alt="Article DOI: 10.1021/acs.jctc.6c00250"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache--2.0-607D8B?style=flat" alt="License: Apache-2.0"></a>
</p>

<p align="center">
  <img src="./LinearPFAS.png" alt="Graphical abstract of the PFAS paper: atomistic-to-Martini mapping, model validation and multicomponent systems" width="100%">
</p>

## Quick links

| What you need | Where to start |
|---|---|
| Model lookup table | [Model library](LIBRARY.md) |
| PFCA models | [Carboxylates](carboxylates/) |
| PFSA models | [Sulfonates](sulfonates/) |
| Multi-PFAS simulation systems | [PFAS mixtures](pfas-mixture/) |
| Emerging contaminant simulation systems | [Emerging contaminant mixtures](ec-mixture/) |
| Graphene–PFOA adsorption | [Systems and analysis outputs](graphene-pfoa/) |
| PFOA critical micelle concentration | [CMC setups](cmc-pfoa/) |
| PFOA and PFDoDA vesicles | [Vesicle setups](vesicle/) |

[Repository structure](#repo-structure) · [How to cite](#how-to-cite) · [License](#license)

## Repo structure

- `carboxylates/`:
  PFAS carboxylates (PFCA), each molecule has:
  - `gaff2/` atomistic reference files (e.g., `*-AA.gro`, `*-AA.itp`, mapping, mdp)
  - `martini3/` CG model and CG property runs (e.g., `PF??C.itp`, `PF??C.gro`, `mdp`, `SASA*.xvg`, `topol.top`)

- `sulfonates/`:
  PFAS sulfonates (PFSA), same layout as `carboxylates/`:
  - `gaff2/` atomistic reference files
  - `martini3/` CG model and CG property runs (`PF??S.itp`, `PF??S.gro`, etc.)

- `pfas-mixture/`:
  Multi-PFAS systems in pure solution and with graphene (contains `md.mdp`, `min.mdp`, `npt.mdp`, `start.gro`, `topol.top`, and component `*.itp`).

- `ec-mixture/`:
  Emerging contaminants mixture systems in pure solution and with graphene, with `*.itp`, `mdp`, `start.gro`, `topol.top`.

- `graphene-pfoa/`:
  Graphene–PFOA adsorption plus analysis outputs (`*.xvg` such as profiles/histograms; `no-labels/`, `mep/`, `e-label/`).

- `cmc-pfoa/`:
  CMC-related starting configurations (`*.gro`) and topologies (`*.top`) for different conditions
  (e.g., `counterions-only/`, `NaCl-0.25M/`, label variants).

- `vesicle/`:
  PFOA and PFDoDA 100 mM + NaCl 0.15 M setups (contains `md.mdp`, `min.mdp`, `npt.mdp`, `start.gro`, `topol.top`, and component `*.itp`).

## How to cite

If you use this repository, please cite the associated article:

Published article: https://doi.org/10.1021/acs.jctc.6c00250

```bibtex
@article{Calza2026,
  title     = {Martini 3 Coarse-Grain Model For Linear Perfluoroalkyl Substances},
  author    = {Calza, Alessandro and Calvaresi, Matteo and Zerbetto, Francesco and Marrink, Siewert J.},
  journal   = {Journal of Chemical Theory and Computation},
  volume    = {22},
  number    = {10},
  pages     = {5284--5298},
  year      = {2026},
  publisher = {American Chemical Society},
  doi       = {10.1021/acs.jctc.6c00250},
  url       = {https://doi.org/10.1021/acs.jctc.6c00250},
  note      = {PMID: 41978348}
}
```

## Contributing

Contributions are welcome as well as bug reports and pull requests.

## License

The original PFAS models, simulation setups, analysis outputs and documentation
in this repository are released under the
[Apache License, Version 2.0 (Apache-2.0)](LICENSE).

The associated article and authors are listed under [How to cite](#how-to-cite)
and in [CITATION.cff](CITATION.cff). Third-party force-field files, including
those in `martini_v300/`, retain their original terms and attribution.
