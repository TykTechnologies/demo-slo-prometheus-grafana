# tyk-templates

Template repo for all your template needs.
- **For a new repo** 
  - Create your repository using this repo as a template ([GitHub instruction](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template#creating-a-repository-from-a-template)).
  - Rename the file `./.github/README-template.md` to `./.github/README.md` (remove the `-template` part) to get GitHub to display this README
  - Update `./.github/README.md` with the relevant content for your repo
- **For an existing repo** please make sure your repo has all the required templates which are defined in the [section below](#current-template-in-the-repo) by simply copying the relevant templates or add content that is in the template but not in your repo files.

## Asking users To sign CLA on submitting a pull request(for existing repo)
For existing repo you can add the feature that ask contributors to sign the CLA on submitting a pull request by copying the [CLA file](.github/workflows/cla.yml) to your `.github/workflows/cla.yml` folder.

## Current template in the repo

1. [Contribution guidelines](./CONTRIBUTING.md) 
2. [PR template](./.github/pull_request_template.md)
3. [Bug report template](./.github/ISSUE_TEMPLATE/bug_report.md)
4. [Feature request template](./.github/ISSUE_TEMPLATE/feature_request.md) 
5. [Contributor License Agreement](https://github.com/TykTechnologies/tyk/blob/master/CLA.md) - This will enforce your contributors to sign the CLA on the first time they submit a PR.
6. [License](./LICENSE)  *from tyk-gateway*
7. [Default Repo README](./.github/README-template.md), which resides in `/.github`

## Backlog / WIP
1. Common GitHub workflows you use across all the repo (e.g. spell checker)
2. Make releases to this repo.


## Adjustments / Changes / Updates
Please feel free to submit PRs, bugs and feature request when you think the templates needs fix or improvement.

