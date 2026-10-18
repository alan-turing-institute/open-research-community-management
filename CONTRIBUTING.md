# Contributing

Thank you for improving this archive of Open Research Community Management resources. Please note that the repository is no longer actively maintained, so contributions may not receive a prompt review.

## Before you begin

- Follow the [Code of Conduct](./CODE_OF_CONDUCT.md).
- Review existing [issues](https://github.com/alan-turing-institute/open-research-community-management/issues) before opening a new one.
- You may reuse the material under the [CC BY 4.0 license](./LICENSE.md), provided that you give appropriate attribution and indicate changes.

## Propose a change

1. Open an [issue](https://github.com/alan-turing-institute/open-research-community-management/issues/new/choose) to report an error, suggest a resource, or discuss a substantial update.
2. Create a branch and make a focused change.
3. If you edit files under `wiki/`, build the book locally:

   ```bash
   python -m pip install -r wiki/requirements.txt
   jupyter-book build wiki
   ```

4. Open a [pull request](https://github.com/alan-turing-institute/open-research-community-management/pulls) that explains the change and links any relevant issue.

Small corrections, such as typo fixes and repaired links, do not need an issue first.

## Documentation conventions

- Keep pages concise, accessible, and suitable for public sharing.
- Do not add confidential, personal, or project-restricted material.
- Use descriptive headings and meaningful link text.
- Update navigation in [`wiki/_toc.yml`](./wiki/_toc.yml) when adding or moving handbook pages.
- Do not commit `wiki/_build/`; it is generated during the handbook build.

For general questions about the historic material, contact [Malvika Sharan](mailto:msharan@turing.ac.uk).
