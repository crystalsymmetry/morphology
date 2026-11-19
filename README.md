# The 32 Crystal Classes in 3D

**Live app:** https://crystalsymmetry.github.io/morphology/

An interactive web app for teaching and learning the 32 crystallographic point groups – with *real* crystal habits instead of idealised textbook polyhedra.

## Features

- **Gallery** of all 32 crystal classes with one or two typical mineral habits each (quartz, calcite, gypsum, hemimorphite, beryl, pyrite, garnet …), grouped by crystal system
- **Semi-transparent 3D models** that can be rotated and zoomed freely
- **Switchable symmetry elements**: rotation axes, rotoinversion axes, mirror planes and the inversion centre, with the usual graphical symbols
- **Animated symmetry operations**: mark a face and watch it move onto a symmetry-equivalent face (including 6̄ performed as 3/*m*)
- **Live stereographic projection** of face poles, mirror planes and axes – in standard orientation or rotating with the model, with a built-in explanation of face poles
- **Explanations of all forms** (pedion, sphenoid, trapezohedron, scalenohedron, forms in general position …) on mouse-over
- **Quiz mode** for self-study: identify the point group of an unlabelled crystal
- **Four languages**: English, German, French, Spanish

## How it works

Nothing is modelled by hand. Each crystal is computed from

1. the point group, given by its generators in ITA notation,
2. (rounded) lattice parameters of the example mineral,
3. a list of forms {*hkl*} with relative central distances.

All symmetry-equivalent faces are generated from the group, and the crystal shape is obtained as the intersection of the corresponding half-spaces. The symmetry elements are derived directly from the group matrices and grouped into families; for every example crystal it has been checked that each derived element maps the set of faces onto itself. Trigonal and hexagonal crystals use the hexagonal setting with Miller–Bravais indices (*hkil*).

The app is a single HTML file without any external requests: [three.js](https://threejs.org/) r128 (MIT licence, `vendor/`) and the IBM Plex fonts (SIL Open Font License, `fonts/`) are served from this repository. No cookies, no tracking – see [Legal notice & privacy](https://crystalsymmetry.github.io/morphology/legal.html).

## Notes

Crystal habits are idealised and typical rather than measured; for a few rare classes (1, 4, 6̄, 432) the shapes are constructed so that the symmetry becomes visible. Lattice parameters are rounded. Corrections and suggestions for better prototype minerals are very welcome – please open an issue.

## Acknowledgements

Inspired by the interactive 3D PDF files of

> Arribas, V., Casas, L., Estop, E., Labrador, M. (2014). Interactive PDF files with embedded 3D designs as support material to study the 32 crystallographic point groups. *Computers & Geosciences* 62, 53–61. DOI: [10.1016/j.cageo.2013.09.004](https://doi.org/10.1016/j.cageo.2013.09.004)

Developed by Frank Hoffmann (University of Hamburg), together with Claude (Anthropic).

Blog: [crystalsymmetry.wordpress.com](https://crystalsymmetry.wordpress.com)
