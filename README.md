# Analog IC LaTeX Report Template

Reusable LaTeX report template for analog and mixed-signal IC design projects.

The template is intended for screen-first technical documentation and is designed around a progressive analog design flow:

1. theoretical analysis
2. ideal architecture and behavioral modeling
3. transistor-level implementation
4. nominal simulation
5. PVT and statistical verification
6. layout and post-layout verification

## Features

- reusable project metadata
- custom title page
- automatic table of contents
- clickable cross-references and PDF navigation
- equations and SI units
- engineering tables
- PDF/vector figures
- landscape pages for large schematics
- technical callout boxes
- HDL, SPICE and terminal code listings
- BibLaTeX/Biber bibliography
- appendices
- optional List of Figures and List of Tables
- automatic compilation with `latexmk`

## Toolchain

- LaTeX / TeX Live
- Biber
- latexmk
- TeXstudio

## Build

From the project root:

```bash
latexmk -pdf main.tex

To remove intermediate build files:

```bash
latexmk -c
```

## Starting a New Project

1. Create a new repository from this template.
2. Edit:

```text
config/project_info.tex
```

3. Adapt the files in:

```text
sections/
```

4. Add figures to:

```text
figures/
```

5. Add references to:

```text
bibliography/references.bib
```

6. Compile the report:

```bash
latexmk -pdf main.tex
```

## Project Structure

```text
.
-> main.tex
-> config/
-> frontmatter/
-> sections/
-> backmatter/
-> bibliography/
-> figures/
-> examples/
```

## Design Philosophy

The template encourages architectural understanding before transistor-level implementation.

Ideal functional elements are first used to isolate and validate the intended circuit behavior independently of device non-idealities and parasitic effects.

Once the architecture is understood and validated, the ideal blocks are progressively replaced by transistor-level implementations. The complete design can then be evaluated across process, voltage and temperature variations, followed by statistical analysis, layout and post-layout verification where applicable.

## Author

Guillaume Monti  
Analog IC Design Engineer
