# Table of Contents
1. [Contributing to Tyk](#contributing-to-tyk)
2. [Our SLA for issues and bugs](#our-sla-for-issues-and-bugs)
3. [Filling an issue](#filling-an-issue)
4. [Contributor License Agreements](#contributor-license-agreements)
5. [Guidelines for Pull Requests](#guidelines-for-pull-requests)
6. [Project Structure](#project-structure)
7. [Building and Running test](#building-and-running-test)
8. [Coding Conventions](#coding-conventions)
9. [Resources](#resources)

# Contributing to Tyk

**First**: if you're unsure or afraid of anything, just ask or submit the issue or pull request anyway. You won't be yelled at for giving your best effort. The worst that can happen is that you'll be politely asked to change something. We appreciate any sort of contributions, and don't want a wall of rules to get in the way of that.

However, for those individuals who want a bit more guidance on the best way to contribute to the project, read on. This document will cover what we're looking for. By addressing all the points we're looking for, it raises the chances we can quickly merge or address your contributions.

### Our SLA for issues and bugs
We do value the time each contributor spends contributing to this repo, and we work hard to make sure we respond to your issues and Pull request as soon as we can.

Below we have outlined. 

### Filling an issue 
Before opening an issue, if you have a question about Tyk or have a problem using it, please
start with the GitHub search and our [community forum](https://community.tyk.io). 
If that doesn't answer your questions, and you have an idea for a new capability  or if you think you found a bug, [file an
issue].

### Contributor License Agreements

Before we can accept any PR the contributor need to sign the [TYK CLA](https://github.com/TykTechnologies/tyk/blob/master/CLA.md).

Once you are CLA'ed, we'll be able to accept your pull requests.For any issues that you face during this process, please create a GitHub issue explaining the problem, and we will help get it sorted out.

### Guidelines for Pull Requests
We have created a few guidelines to help with creating PR. To make sure these requirements are followed we added them to the PR form as well:

1. When working on an existing issue, simply respond to the issue and express interest in working on it.  This helps other people know that the issue is active, and hopefully prevents duplicated efforts.
2. For new ideas or breaking changes it is always better to open an issue and discuss your idea with our team first, before implementing it.
3. Create small Pull request that address a single issue instead of multiple issues at the same time. This will make it possible for the PRs to be reviewed independently.
5. Make sure to run tests locally before submitting a pull request and verify that all of them are passing.
6. Documentation - a new capability or improvement needs to be exposed in the form of documentation which needs to be created before this PR is merged. Please open a ticket in [Tyk docs repo](https://github.com/TykTechnologies/tyk-docs/issues/new?assignees=&labels=enhancement&template=feature_request.md&title=) with all the relevant content and link it to the code PR. We are also happy work with you on creating docs so please let us know. Once the docs are ready and review has been done we can merge the PR
7. Tips for making sure we review your pull request faster :
    1. Code is documented. Please comment the code where possible, especially for fields and functions.
    2. Use meaningful commit messages.
    3. Keep your pull request up to date with upstream master to avoid merge conflicts.
    4. Provide a good PR description as a record of what change is being made and why it was made. Link to a GitHub issue if it exists.
    5. Tick all the relevant checkboxes in the PR form
    
### Project Structure
  [sample project structure](https://github.com/getkin/kin-openapi/tree/0846d700650012c02a16668ebd2bf1e77e9a1669#structure)
  1. *folder one(package one) - explain what is in this package and what code in this package does ...*
  2. *folder one(package one) - explain what is in this package and what code in this package does ...*
  3. *folder one(package one) - explain what is in this package and what code in this package does ...*

### Building and Running test
 *explain to the contributor how there can build and run test cases for this project*

### Coding Conventions
*if your team has any coding conventions write them here*

### Resources
- [How to Contribute to Open Source](https://opensource.guide/how-to-contribute/)
- [Using Pull Requests](https://help.github.com/articles/about-pull-requests/)


[file an issue]: https://github.com/TykTechnologies/tyk-templates/issues/new/choose

