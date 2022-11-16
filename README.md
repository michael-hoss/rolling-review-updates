

# Rolling Updates on *A Review of Testing Object-Based Environment Perception for Safe Automated Driving*

[![Create latex PDF release](https://github.com/michael-hoss/rolling-review-updates/actions/workflows/create_latex_pdf_release.yml/badge.svg)](https://github.com/michael-hoss/rolling-review-updates/actions/workflows/create_latex_pdf_release.yml)


Our previous [review paper](https://link.springer.com/article/10.1007/s42154-021-00172-y) and its [preprint](https://arxiv.org/abs/2102.08460) capture the authors' knowledge as of February 2021. 

The present repository aims at enriching this review by literature that was either missed previously or published later. The present latex document is based on the previous section structure, but only describes novelties. 

## :page_facing_up: PDF exports/releases

Check out the [GitHub releases](https://github.com/michael-hoss/rolling-review-updates/releases) assets for updated PDFs. They are created for every significant update of the literature by means of a GitHub workflow.

## Collaboration

If you believe certain literature should be added to this rolling review or want to provide feedback, feel free to open an issue or a pull request.

The latex code is currently formatted like this:
- **Updates to the section structure**: `\new{}` command to highlight and differentiate new sections from previous sections
- **New references**: `\cite{}` automatically colors the reference number to highlight novelties
- **References already present in the original review**: `\citeold{}` to create a reference in the original text color

## Disclaimer

:warning: This evolving document is not peer-reviewed. No claims are made on completeness and quality.

