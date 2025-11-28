# overleaf-research-manuscript
This is an example repository used to illustrate some research workflows that can be implemented using GitHub Actions, while also maintaining good Overleaf project hygeine. 

- This repository (overleaf-research-manuscript) contains only LaTeX source, and some GitHub action scripts for acting on that source code.
- Overleaf's [GitHub synchronization feature] (https://docs.overleaf.com/integrations-and-add-ons/git-integration-and-github-synchronization/github-synchronization) allows the overleaf-research-manuscript repository to be synchronized with an Overleaf project.
- The associated workspace repository ([overleaf-research-workspace](https://github.com/dmackinnon1/overleaf-research-workspace/tree/main)) contains additional artifacts that are produced by the research workflow: a sharable PDF of the latest version of the manuscript, an accessibility report, a PDF showing recent changes, etc. The workspace also provides a place for raw data, scripts, and other artifacts that are not directly required for compiling the manuscript.

It is important to keep the Overleaf project, and the overleaf-research-manuscript repository free from files that could cause [Overleaf's project limits](https://docs.overleaf.com/getting-started/free-and-premium-plans/plan-limits) to be exceeded, or that may introduce clutter or confusion into the document build process. 

Separating research artifacts into distinct manuscript and workspace repositories helps to keep a clear distinction between the things that are strictly needed to compile the document and those that are not, and helps to define a clear set of workflow tasks.

## Accessibility and PDF tagging
The LaTeX source code makes use of the latest PDF tagging support available in Tex Live 2025. Please see the LaTeX team's [tagging instructions](https://latex3.github.io/tagging-project/documentation/usage-instructions) for more information. 

The [overleaf-research-workspace](https://github.com/dmackinnon1/overleaf-research-workspace) repository that is associated with this repository can be used to compile the latest PDF and apply accessibility tests using [veraPDF](https://verapdf.org/).

## LaTeX formatting
As a demonstration of how GitHub Actions can be used to transform and operate on LaTeX source code, there is are workflows in this project that will reformat latex code for readability. There are two leading tools for this,  [latexindent](https://ctan.org/pkg/latexindent?lang=en) and [tex-fmt](https://github.com/WGUNDERWOOD/tex-fmt). There are example actions in this repo for both of these tools

**A word of caution**: Applying tools like these to .tex files can disrupt Overleaf's source code comments. Changes made to files from an external tool will not show as tracked changes (but will be shown in the Overleaf history).
