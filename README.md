# Open Research Community Management

*Integrating open research practices through community engagement.*

> **Project status:** This repository is no longer actively maintained. It preserves resources and working practices developed by the Open Research Community Management team at The Alan Turing Institute.

The published handbook is available at [alan-turing-institute.github.io/open-research-community-management](https://alan-turing-institute.github.io/open-research-community-management/).

## About this repository

Research Community Managers (RCMs) support open, inclusive, and reproducible research by connecting people, projects, and shared resources. This repository records the team's approaches, guidance, and selected communications.

| Location | Contents |
| --- | --- |
| [`wiki/`](./wiki/) | Source for the published Jupyter Book handbook |
| [`project-management/`](./project-management/) | Team practices, meeting material, and reference resources |
| [`resources/`](./resources/) | Reusable guides and supporting material |
| [`team-related-comms/`](./team-related-comms/) | Briefing notes, case studies, and presentations |
| [`the-turing-way-core/`](./the-turing-way-core/) | Links and guidance for contributing to *The Turing Way* |

Read the [Code of Conduct](./CODE_OF_CONDUCT.md) before participating. The team's [ways of working](./project-management/ways-of-working.md) describe its structure and expectations.

## Build the handbook locally

The handbook is a [Jupyter Book](https://jupyterbook.org/) whose source lives in [`wiki/`](./wiki/). Use Python 3.11, the version used by the deployment workflow:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r wiki/requirements.txt
jupyter-book build wiki
```

Open `wiki/_build/html/index.html` in a browser to review the output. Generated files are ignored and must not be committed.

## Publish to GitHub Pages

Changes merged into `main` build and deploy automatically through [the Pages workflow](./.github/workflows/build-wiki.yml), which publishes the built book to the `gh-pages` branch. Keep **Settings → Pages → Build and deployment** set to **Deploy from a branch**, using `gh-pages` and `/ (root)`.

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for the contribution workflow, documentation conventions, and pull-request checklist. As this is an archive, maintainers may not be able to review or merge new contributions promptly.

## Reference

Sharan, M., Hellon, V., Karoune, E., Lacey, A., Zormpa, E., Lee Steele, A., & Kayumbi, G. (2023). *Research Community Management Team at the Turing*. Zenodo. [10.5281/zenodo.7848677](https://doi.org/10.5281/zenodo.7848677)

The practices here also draw on [*The Turing Way*](https://the-turing-way.netlify.app/welcome) and [Whitaker Lab Project Management](https://github.com/WhitakerLab/WhitakerLabProjectManagement).

## License

All content is available under the [Creative Commons Attribution 4.0 International license](./LICENSE.md). You may reuse and adapt it with appropriate attribution; see [Creative Commons](https://creativecommons.org/licenses/by/4.0/) for the license terms.
