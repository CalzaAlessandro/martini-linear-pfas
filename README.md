<h1 align="center">
  <div>
    <a href="https://github.com/CalzaAlessandro/martini-linear-pfas" target="_blank">
      <img src="./LinearPFAS.png" alt="Martini3 Linear PFAS" height="150">
    </a>
  </div>
</h1>

# Martini 3 PFAS database

This repository contains Martini 3 linear PFAS models (carboxylates and sulfonates) plus
ready-to-run simulation systems and analysis outputs for PFAS and emerging contaminants mixtures, PFOA critical micelle concentration, PFAS vesicle formation
and PFAS adsorption on graphene.

## How to cite

If you use this repository, please cite the associated manuscript:

```bibtex
@article{Calza2026,
  title  = {Martini 3 coarse-grain model for linear PerFluoroAlkyl Substances},
  author = {Calza, Alessandro and Calvaresi, Matteo and Zerbetto, Francesco and Marrink, Siewert J.},
  doi    = {},
  journal = {},
  volume = {},
  year   = {2026},
  pages  = {},
  note   = {Manuscript in preparation. Code and data: https://github.com/CalzaAlessandro/martini-linear-pfas (v1.0)}
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
  <a href="./graphene-pfoa/"><b>Graphene–PFOA adsorpion</b></a> •
  <a href="./cmc-pfoa/"><b>CMC PFOA setups</b></a>  •
  <a href="./vesicle/"><b>PFOA and PFDoDA vesicle</b></a> 
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
  Multi-PFAS systems with `graphene/` and without `pure/` (contains `md.mdp`, `min.mdp`, `npt.mdp`, `start.gro`, `topol.top`, and component `*.itp`).

- `ec-mixture/`:
  Emerging contaminants mixture systems (`graphene/` and without `pure/`), with `*.itp`, `mdp`, `start.gro`, `topol.top`.

- `graphene-pfoa/`:
  Graphene–PFOA adsorption plus analysis outputs (`*.xvg` such as profiles/histograms; `no-labels/`, `mep/`, `e-label/`).

- `cmc-pfoa/`:
  CMC-related starting configurations (`*.gro`) and topologies (`*.top`) for different conditions
  (e.g., `counterions-only/`, `NaCl-0.25M/`, label variants).

- `vesicle/`:
  PFOA and PFDoDA 100mM + NaCl 0.15M setups (contains `md.mdp`, `min.mdp`, `npt.mdp`, `start.gro`, `topol.top`, and component `*.itp`).

## Contributing

Contributions are welcome as well as bug reports and pull requests.

## License

This repository is released under the Apache License, Version 2.0 (Apache-2.0).
See: https://www.apache.org/licenses/LICENSE-2.0.txt
