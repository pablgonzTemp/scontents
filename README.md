## scontents — Stores LaTeX contents in memory or files
![GitHub release (latest by date)](https://img.shields.io/github/v/release/pablgonz/scontents?label=version)
![GitHub Release Date](https://img.shields.io/github/release-date/pablgonz/scontents)
![GitHub last commit](https://img.shields.io/github/last-commit/pablgonz/scontents)

## Description

This package allows to store LaTeX code, including _verbatim_, in <code>&langle;sequences&rangle;</code>
using the `l3seq` module of `expl3`. The <code>&langle;stored content&rangle;</code> can be used
as many times as desired in the document, additionally you can write to <code>&langle;external files&rangle;</code>
or show it in <code>&langle;verbatim style&rangle;</code>. This package is fully compatible with _tagged_ PDF.

## Requirements

The minimum required is `LaTeX` release 2024-11-01.

## Installation

The package <code>&langle;scontents&rangle;</code> is present in `TeX Live` and `MiKTeX`, use the
package manager to install.

For manual installation, download [scontents.zip](http://mirrors.ctan.org/macros/latex/contrib/scontents.zip) and unzip it,
then run:

```
$ luatex scontents.ins
```

and move all files to appropriate locations:

```
  scontents.tex      -> TDS:tex/generic/scontents/scontents.tex
  scontents-code.tex -> TDS:tex/generic/scontents/scontents-code.tex
  scontents.sty      -> TDS:tex/latex/scontents/scontents.sty
  t-scontents.mkiv   -> TDS:tex/context/third/scontents/t-scontents.mkiv
  scontents.pdf      -> TDS:doc/latex/scontents/scontents.pdf
  scontents.dtx      -> TDS:source/latex/scontents/scontents.dtx
  scontents.ins      -> TDS:source/latex/scontents/scontents.ins
```

then run `mktexlsr`. To produce the documentation with source code run `luatex scontents.ins` and
`lualatex scontents.dtx` three times.

## Examples

The file <code>&langle;scontents.pdf&rangle;</code> contains attached examples, which can be extracted
from the PDF viewer or from the command line by running:

```
$ pdfdetach -saveall scontents.pdf
```

and then you can use the excellent `arara` tool to compile them.

## Development

The version numbers and dates are guaranteed to be correct in
the repository is in the `l3build` configuration file `build.lua`.

The date format (`pkgdate`) is `YYYY-MM-DD`. If it is important to you
that the files created have the correct version and date, you should run
`l3build tag` before any other build-related task.

`scontents` utilizes the `l3build` system. You can run:

- `l3build unpack` to extract the code files into the directory `build/unpacked/`.
- `l3build doc` to build the documentation.
- `l3build install` put all files  in your `TEXMFHOME`.
- `l3build uninstall` will remove them.
- `l3build testpkg` to test files.
- `l3build examples` to compile example files.

## License

The package <code>&langle;scontents&rangle;</code> may be modified and distributed under the terms and
conditions of the [LaTeX Project Public License](https://www.latex-project.org/lppl/), version 1.3c or greater.

## Content of the repository

```
├── README.md
├── build.lua
├── ctan.ann
└── sources
    ├── CTANREADME.md
    ├── scontents-code.tex
    ├── scontents.dtx
    ├── scontents.ins
    ├── scontents.sty
    ├── scontents.tex
    ├── t-scontents.mkiv
    └── test-pkg
        ├── test-format.context.tex
        ├── test-format.latex.tex
        ├── test-format.plain.tex
        ├── test-nospace.tex
        ├── test-pkg-current.tex
        ├── test-pkg-other.tex
        └── test-tagged-pdf.tex
```

## Copyright

Copyright 2019 — 2025 by Pablo González L.
