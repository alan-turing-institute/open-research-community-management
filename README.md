# Open Research Community Management at The Alan Turing Institute

*Integrating open science practices through community engagement*

**Contents**
- [Important Documents for the Team Members](#important-documents-for-the-team-members)
- [Updating the wiki](#updating-the-wiki)
- [References](#references)
- [License](#license)
- [Acknowledgement](#acknowledgement)
   
## Important Documents for the Team Members

- [Code of Conduct](./CODE_OF_CONDUCT.md): Please familiarise yourself with the Code of Conduct, and enforcement procedure to help us create a welcoming and safe space for everyone who contributes to the team and this project repository.
- [Project Management](./project-management): Please find details about how we manage the Open Research Community Management team.
- [Ways of Working](./project-management/ways-of-working.md): This document describes the structure and organisation of the Open Research Community Management Team, clarifying expectations and support structure to help enable your work. The Turing members should also check the [Governance](https://www.turing.ac.uk/about-us/governance) to understand the organisation's structure and policies that apply to them.

## Updating the wiki
*Admin should ensure that the github pages settings for the repo are set to build with the source `branch`; branch `gh-pages` `/(root)`.*

Pull this repo and make your edits to files in `/docs`, then:
1. `pip install -r wiki/requirements.txt`
2. `jupyter-book build wiki`
3. Follow the onscreen instructions to view a local copy of the html for the book. I use "paste this line directly into your browser bar:" address. Check everything looks good!
4. `ghp-import -n -p -f wiki/_build/html` to make a branch called `gh-pages` and push the newly built HTML to the `gh-pages` branch.
5. `git add .` add all changes to the staging area
6. `git commit -m "[commit message for your changes]"` add a relevant commit message for the changes made
7. `git push`
8. View the updated handbook at [https://cassgvp.github.io/open-research-community-management/](https://cassgvp.github.io/open-research-community-management/)

Note there is a workflow [build-wiki.yml](/.github/workflows/build-wiki.yml) I've tried to get working for this, but haven't managed to crack it yet! It is currently [disabled in the repo settings](https://docs.github.com/en/actions/using-workflows/disabling-and-enabling-a-workflow#disabling-a-workflow)

## References

- Sharan, M., Hellon, V., Karoune, E., Lacey, A., Zormpa, E., Lee Steele, A., & Kayumbi, G. (2023). Research Community Management Team at the Turing. Zenodo. doi: [10.5281/zenodo.7848677](https://zenodo.org/record/7848677)
- _The Turing Way_ Handbook: https://the-turing-way.netlify.app/welcome, GitHub repository: https://github.com/alan-turing-institute/the-turing-way

## License 

All content in this repository is [openly licensed](./LICENSE.md) with a CC BY 4.0, which means you're free to use the materials and remix them so long as you ***credit the source***.
More on CC BY 4.0 license can be found at [Creative Commons](https://creativecommons.org/licenses/by/4.0/).

## Acknowledgement

Our project management documentation and processes are partially derived from "[Whitaker Lab Project Management](https://github.com/WhitakerLab/WhitakerLabProjectManagement)" by Dr Kirstie Whitaker and the Whitaker Lab repository used under CC BY 4.0.
