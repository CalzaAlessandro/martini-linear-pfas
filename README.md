<h1 align="center">
  <div>
    <a href="https://github.com/CalzaAlessandro/martini-linear-pfas" target="_blank">
      <img src="./LinearPFAS.png" alt="Martini3 Linear PFAS" height="150">
    </a>
  </div>
</h1>

<p align="center">
  <a href="https://doi.org/10.1021/acs.jctc.6c00250">
    <img src="https://img.shields.io/badge/DOI-10.1021%2Facs.jctc.6c00250-blue" alt="DOI: 10.1021/acs.jctc.6c00250">
  </a>
</p>

# Martini 3 PFAS Database

This repository contains Martini 3 linear PFAS models (carboxylates and sulfonates) plus
ready-to-run simulation systems and analysis outputs for PFAS and emerging contaminants mixtures, PFOA critical micelle concentration, PFAS vesicle formation,
and PFAS adsorption on graphene.

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

## Quick links

<p align="center">
  <a href="./LIBRARY.md"><b>Lookup table (models)</b></a>
</p>

<p align="center">
  <a href="./carboxylates/"><b>PFCA models (carboxylates)</b></a> •
  <a href="./sulfonates/"><b>PFSA models (sulfonates)</b></a>
</p>

<p align="center">
  <a href="./pfas-mixture/"><b>PFAS mixture systems</b></a> •
  <a href="./ec-mixture/"><b>Emerging contaminants mixture</b></a>
</p>

<p align="center">
  <a href="./graphene-pfoa/"><b>Graphene–PFOA adsorption</b></a> •
  <a href="./cmc-pfoa/"><b>CMC PFOA setups</b></a>  •
  <a href="./vesicle/"><b>PFOA and PFDoDA vesicles</b></a>
</p>

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

## Contributing

Contributions are welcome as well as bug reports and pull requests.

## License

This repository is released under the Apache License, Version 2.0 (Apache-2.0).
See: https://www.apache.org/licenses/LICENSE-2.0.txt
