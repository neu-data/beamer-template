<div align="center">

<img src="https://raw.githubusercontent.com/neu-data/.github/main/assets/banner.svg" alt="Neudata Consulting Ltd" width="100%" />

# Neudata Beamer template

**LaTeX presentations in the Neudata house style — matching the Neudata PowerPoint template.**

[![Open in Overleaf](https://img.shields.io/badge/Open%20in-Overleaf-055F56?style=flat&logo=overleaf&logoColor=white)](https://www.overleaf.com/docs?snip_uri=https://github.com/neu-data/beamer-template/archive/refs/heads/main.zip)
![LaTeX](https://img.shields.io/badge/LaTeX-Beamer-0B376C?style=flat&logo=latex&logoColor=white)
![Neudata](https://img.shields.io/badge/Neudata-brand-04242F?style=flat)

</div>

---

See the compiled example: [`examples/example.pdf`](examples/example.pdf).

## What you get

| Slide | How |
|---|---|
| Title slide — centred title, presenter, large logo bottom-left, date bottom-right | `\neudatatitleframe` |
| Section divider — logo, teal rule, section name | automatic at every `\section{}` |
| Content slides — teal title with thin rule, small logo, `Neudata \| #ClearDataClearImpact` footer, slide number | `\begin{frame}{Title}` |
| Teal sub-headings and blue notes | `\neudataheading{...}`, `\neudatanote{...}` |
| Big-number callouts | `\neudatastat{16,293}{live births}` |
| Teal / blue / navy blocks | `block`, `alertblock`, `exampleblock` |
| Closing copyright slide | `\neudatacopyrightframe` |

## Use it on Overleaf

Click **Open in Overleaf** above, or download the repository as a ZIP and use **New Project → Upload Project**. Compile with the default **pdfLaTeX**.

## Use it locally

```bash
git clone https://github.com/neu-data/beamer-template.git my-talk
cd my-talk
latexmk -pdf main.tex
```

## Minimal example

```latex
\documentclass[aspectratio=169]{beamer}
\usetheme{Neudata}

\title{Presentation Title}
\author{Presenter Name, Role}
\date{\neudatatoday}          % DD-MM-YYYY, or write a date

\begin{document}
\neudatatitleframe

\section{Results}
\begin{frame}{Key numbers}
  \neudatastat{87.4\%}{coverage}
\end{frame}

\neudatacopyrightframe
\end{document}
```

## Theme options

```latex
\usetheme[logo=figures/other-logo.png]{Neudata}   % different logo file
\usetheme[nofonts]{Neudata}                       % keep Beamer's default font
```

## Brand

| Teal (titles) | Blue (notes) | Navy | Logo blue | Mist | Grey |
|---|---|---|---|---|---|
| `#0D7377` | `#0070C0` | `#04242F` | `#0B376C` | `#EAF2F5` | `#8A99A3` |

The PowerPoint template uses Century Gothic; LaTeX uses **TeX Gyre Adventor**, a free font with the same geometric look, available on Overleaf and TeX Live.

---

<div align="center">

**Neudata Consulting Ltd** · *Insight. Impact. Innovation.*
[www.neu-data.com](https://www.neu-data.com) · [contact@neu-data.com](mailto:contact@neu-data.com)

</div>
