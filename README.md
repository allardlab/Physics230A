# Physics 230A/146A — Biological Physics

Course materials for a graduate course in the Mathematical, Computational and Systems Biology program.

<!-- Served by GitHub Pages for allardlab/Physics230A, branch `main`, folder `/docs`.
It needs no CNAME and no change here: the allardlab account's user site carries the www.allardlab.com domain, and GitHub serves every project site of that account under it. -->
**[Open the course website →](https://www.allardlab.com/Physics230A/)**

The website is the place to read the problem sets.
This repository is the place to *run* them.

## Notebooks

Click one to open it.
Every problem set is also on the website as html, pdf, tex and markdown.

- [Problem Set 0: Scavenger hunt](docs/PS0_scavenger-hunt.ipynb)
- [Problem Set 1: What happens in a composite material?](docs/PS1_composite-material.ipynb)
- [Problem Set 2: Viral entry](docs/PS2_viral-entry.ipynb)
- [Problem Set 3: Morphogens in an epithelial sheet](docs/PS3_morphogens-epithelial-sheet.ipynb)
- [Problem Set 4: How much do receptors compete?](docs/PS4_receptor-competition.ipynb)
- [Problem Set 5: Kinetic segregation](docs/PS5_kinetic-segregation.ipynb)
- [Problem Set 6: Bacterial export](docs/PS6_bacterial-export.ipynb)
- [Problem Set 7: Inferring methyltransferase binding rates](docs/PS7_methyltransferase-rates.ipynb)
- [Problem Set 8: DNA in a nucleus](docs/PS8_dna-in-a-nucleus.ipynb)
- [Python test drive](docs/python-test-drive.ipynb)

## Problem sets in Latex

Each problem set's Latex source, to write your solutions into if you like.
Click one to open it, build it with the green ▶ at the top right of the editor (**Build LaTeX project**), and open the result with the icon beside it (**View LaTeX PDF**).

- [Problem Set 0: Scavenger hunt](docs/PS0_scavenger-hunt.tex)
- [Problem Set 1: What happens in a composite material?](docs/PS1_composite-material.tex)
- [Problem Set 2: Viral entry](docs/PS2_viral-entry.tex)
- [Problem Set 3: Morphogens in an epithelial sheet](docs/PS3_morphogens-epithelial-sheet.tex)
- [Problem Set 4: How much do receptors compete?](docs/PS4_receptor-competition.tex)
- [Problem Set 5: Kinetic segregation](docs/PS5_kinetic-segregation.tex)
- [Problem Set 6: Bacterial export](docs/PS6_bacterial-export.tex)
- [Problem Set 7: Inferring methyltransferase binding rates](docs/PS7_methyltransferase-rates.tex)
- [Problem Set 8: DNA in a nucleus](docs/PS8_dna-in-a-nucleus.tex)

A codespace opened from the button below cannot save your work back to GitHub, and one left unused is deleted after 30 days, so download anything you write.
If you would rather keep working in Overleaf, every problem set on the website has an **Overleaf** link, which opens that problem set's `.tex` and figures as a new private project in your own Overleaf account.
UCI students have Overleaf Professional free through [overleaf.com/edu/uci](https://www.overleaf.com/edu/uci), though nothing here needs it.

## Running them

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/allardlab/Physics230A)

That button builds a machine in the cloud with Python, numpy, scipy and matplotlib already installed.
Give it a few minutes the first time.
When it opens, this README opens with it — click a notebook above and press **Run All**.

### If you would rather use JupyterLab

Codespaces can open straight into JupyterLab instead of the VSCode interface, with no extra step once you have set it once:

1. Go to [your Codespaces settings](https://github.com/settings/codespaces).
2. Under **Editor preference**, choose **JupyterLab**.

From then on the button above opens JupyterLab directly.
Choose the kernel named **Python (Physics 230A)**.

To switch a codespace you have already created, go to [your codespaces](https://github.com/codespaces), click the `…` beside it, and choose **Open in JupyterLab**.

### On your own machine

You need [uv](https://docs.astral.sh/uv/getting-started/installation/), which installs the right Python and packages for you:

```sh
git clone https://github.com/allardlab/Physics230A.git
cd Physics230A
uv sync
```

Then open any notebook above in VSCode and select the `.venv` interpreter, or run `uv run jupyter lab`.

### By downloading a single notebook

Every problem set page on the website has an **ipynb** link.
Download it and open it in whatever you already use.

## Two kinds of document, and they work differently

**The problem sets are deliberately language-agnostic.**
Where one says "write code", write it in whatever language you intend to use for the rest of your degree — Matlab, Python, R, Julia — and be ready to explain your choice to someone who picked differently.
Their `.ipynb` versions contain no code: they are containers for you to work in, and the environment above is there so that you have somewhere to work if Python is what you choose.

**The lecture notebooks do run Python.**
Some of their code cells have already been run, and you are reading their results.
Others are deliberately left for you: complete code that you should run yourself, and empty stubs for you to fill in.
Both are ordinary code cells — put your cursor in one and run it.

---

*This repository is generated.
Its source lives in a separate repository and everything here is rebuilt from that, so edits made here are overwritten on the next publish.
Anything you change while working — including notebook output — is yours locally, but do not expect it to survive a `git pull`.*
