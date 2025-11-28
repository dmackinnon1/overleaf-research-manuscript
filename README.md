# overleaf-research-manuscript
This is an example repository used to illustrate some research workflows that can be implemented using GitHub Actions. Overleaf's GitHub synchronization feature allows the overleaf-research-manuscript repository to be synchronized with an Overleaf project.

The accompanying repository [overleaf-research-workspace](https://github.com/dmackinnon1/overleaf-research-workspace) contains raw data and scripts, as well as the latest version of the compiled manuscript, accessibility reports, and other artifacts.

## Accessibility and PDF tagging
The LaTeX source code makes use of the latest PDF tagging support available in Tex Live 2025. Please see the LaTeX team's [tagging instructions](https://latex3.github.io/tagging-project/documentation/usage-instructions) for more information. 

The [overleaf-research-workspace](https://github.com/dmackinnon1/overleaf-research-workspace) repository that is associated with this repository can be used to compile the latest PDF and apply accessibility tests using [veraPDF](https://verapdf.org/).

## LaTeX formatting
As a demonstration of how GitHub Actions can be used to transform and operate on LaTeX source code, there is are workflows in this project that will reformat latex code for readability. There are two leading tools for this,  [latexindent](https://ctan.org/pkg/latexindent?lang=en) and [tex-fmt](https://github.com/WGUNDERWOOD/tex-fmt). There are example actions in this repo for both of these tools

**A word of caution**: Applying tools like these to .tex files can disrupt Overleaf's source code comments. Changes made to files from an external tool will not show as tracked changes (but will be shown in the Overleaf history).
