[![DOI](https://zenodo.org/badge/508559520.svg)](https://zenodo.org/badge/latestdoi/508559520)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
![Compile demo.tex](https://github.com/aritraghsh09/pdflatex_bengali/actions/workflows/compile_demo_tex.yml/badge.svg)

***


# Introduction
Writing বাংলা in LaTeX is pretty straightforward these days using XeLaTeX or LuaTeX. However, there arises instances when one needs to write বাংলা only using pdflatex.

This is especially true with respect to many academic institutions (e.g., [arXiv](https://arxiv.org/)), which still support only pdflatex. 

This short repository is meant to help you write বাংলা using only pdflatex. The examples in this repository have also been written/tested to work with
[Overleaf](https://www.overleaf.com/)

Note that this repository is entirely based on the Bengali font and code developed by [Palash Baran Pal](http://www.saha.ac.in/theory/palashbaran.pal/)
for his excellent [bangtex package](http://www.saha.ac.in/theory/palashbaran.pal/bangtex/bangtex.html)


# Quickstart Guide
- Put the [mf](https://github.com/aritraghsh09/bangtex_overleaf/tree/main/mf) folder along with all its contents in the same directory as your LaTeX source code.
- Put the [bangla_commands.tex](https://github.com/aritraghsh09/bangtex_overleaf/blob/main/bangla_commands.tex) file in the same directory as your LaTeX source code. 
- Put `\input{bangla_commands}` in the preamble of your LaTeX source code
- When you write বাংলা enclose it within the `\bng` command like this `{\bng baNNGla \*l*ikhun}` which should output বাংলা লিখুন 
- The `\bng` command can be replaced by commands specifying other sizes, and this is outlined in the 
[demo.tex](https://github.com/aritraghsh09/bangtex_overleaf/blob/main/demo.tex) and 
[demo.pdf](https://github.com/aritraghsh09/bangtex_overleaf/blob/main/demo.pdf) files. 
- A simple example document is shown below

```tex
\documentclass{article}

\title{Bengali Test}
\author{{\lbng Airt/r \*gh*eaSh}}

\input{bangla_commands}

\begin{document}

\maketitle

\section{Example}

{\bng baNNGla \*l*ikhun}

\end{document}
```

# Transliteration 
- Note that in order to write Bengali using bangtex, you cannot type using the বাংলা script directly. You need to write it using transliteration-esque Roman
characters. This scheme is extensively outlined in the [original bangtex manual](https://github.com/aritraghsh09/bangtex_overleaf/blob/main/original_bangtex_manual.pdf).

- As you may notice, the above scheme takes a little bit of time to learn and master. [Abhijit Dasgupta](https://www.udmercy.edu/about/people/university/ces/math/dasgupta-abhijit.php) 
has developed a way to type directly in বাংলা and then convert the same into the bangtex commands using a perl script. You can access the details 
[here](http://dasgupab.faculty.udmercy.edu/uni2bangtex/index.html)


# More Background & Why This Repository 
- While [bangtex](http://www.saha.ac.in/theory/palashbaran.pal/bangtex/bangtex.html) provides an excellent way to write extensive documents 
in বাংলা, I needed the exact opposite -- the need to insert বাংলা in a primarily English document using only pdflatex on Overleaf. 

- Thus, I created this repository, which only keeps the bare minimum functionality of [bangtex](http://www.saha.ac.in/theory/palashbaran.pal/bangtex/bangtex.html)
while also not needing any extensive installation or dependencies on other software (as this is not possible on Overleaf) 

- Note that if you are trying to write a more extensive document with advanced features, you should not expect this simple repository to work properly
and should use the original [bangtex](http://www.saha.ac.in/theory/palashbaran.pal/bangtex/bangtex.html) package instead. 

# Citation & Contact

I was not aware that I could write my name or other content in বাংলা for my arXiv submissions for many years. I encourage you to cite this repository
(in the Software Section of your academic publications) to make others aware of its existence.  To do this you can use the following Zeondo DOI and bibtex code

```bib
@software{Ghosh_pdfLaTeX_Bengali_2022,
author = {Ghosh, Aritra},
doi = {10.5281/zenodo.6780690},
month = {6},
title = {{pdfLaTeX Bengali}},
url = {https://github.com/aritraghsh09/pdflatex_bengali},
version = {0.1},
year = {2022}
}
```

You can reach out to me using the contact information on [my website](http://www.ghosharitra.com/). If you want to contribute, feel free to open a pull
request directly if you know how to/are comfortable doing that. 
