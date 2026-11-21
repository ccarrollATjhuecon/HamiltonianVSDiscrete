> **This repository has moved to [llorracc/HamiltonianVSDiscrete](https://github.com/llorracc/HamiltonianVSDiscrete).** This copy is archived and
> is no longer updated; the current handout, its notebook and its history are there.

# Ramsey Growth in Discrete and Continuous Time

A handout for JHU Econ 180.603 (Intertemporal Choice): it solves a continuous-time version of the
Ramsey/Cass-Koopmans model, without productivity growth, with the Hamiltonian, and maps each condition to
its discrete-time Bellman counterpart.

- **The source is the book's page,** [Ramsey Growth in Discrete and Continuous Time](https://intertemporal-choice.github.io/content/appendices/mathematical/hamiltonianvsdiscrete/)
  (`content/appendices/mathematical/HamiltonianVSDiscrete.md` in
  [intertemporal-choice.github.io](https://github.com/intertemporal-choice/intertemporal-choice.github.io)).
  Edits start there and are carried into `HamiltonianVSDiscrete.tex`.
- **Build:** `latexmk` (the `latexmkrc` points TeX at the vendored registry in `@resources/`).
- **Check against the book:** `./check-book-sync.py` (the book's main on GitHub), or
  `./check-book-sync.py --book-git <clone> --ref <commit>` for an unpushed book commit. It compares the words,
  the notes (a `\marginFootnote` here is a margin note in the book), the links and the printed symbols, and
  checks rule D: every object written with its macro.
- `@local/HamiltonianVSDiscrete.sty` defines no notation, only `\marginFootnote`. Since cb37545 (registry v14.1.0)
  the registry has the costate `\vk`, the Hamiltonian `\Ham` and the continuous-time value function `\VFuncCts`.
- `HamiltonianVSDiscrete.bib` holds the entries the handout cites, copied from texmf-local's `economics.bib`;
  the empty `system.bib` keeps the build to them, as in the RamseyCassKoopmans handout.

Revived on 2026-11-16 from the 2021 handout (the first commit holds it as found).
