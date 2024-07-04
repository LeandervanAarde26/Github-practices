# Internal-Repository suggestions

## READ ME

Documentation is a key component in giving insight to team members, especially new developers, about the project. Proper documentation provides a uniform understanding of the project, and the README file is a fundamental part of assisting developers in particular. This document should be an informative piece that gives developers insights into crucial <ins>need to knows</ins>:

The following information is a recommendation of structure for __README.MD__ files: 
### Project Name

### Project Overview
- **What the project is:** Provide a brief summary of the project's purpose and goals.
- **Project Status:** Mention the current status of the project (e.g., in development, alpha, beta, production).

### Tools and Frameworks
- **Languages and Frameworks:** List the primary languages and frameworks used in the project (e.g., JavaScript, React, Node.js).
- **Libraries and Dependencies:** Mention any significant libraries or dependencies (e.g., Prisma ORM, AWS SDK).

### Prerequisites
- **System Requirements:** Specify the operating systems and versions supported.
- **Required Software:** List software that needs to be installed (e.g., Node.js, Docker).
- **Environment Variables:** Detail any environment variables that need to be set.

### Local Setup
- **Installation Steps:** Provide step-by-step instructions for setting up the project locally.
    1. Clone the repository.
    2. Install dependencies.
    3. Set up the environment variables.
    4. Run the project.

### Versioning
- **Versioning Strategy:** Explain the versioning strategy used (e.g., Semantic Versioning).
- **Release Notes:** Link to the release notes or changelog.

### Contribution Guidelines
- **How to Contribute:** Explain how developers can contribute to the project and how aspects such as Pull requests and commits should be structured.
    - Fork the repository.
    - Create a new branch.
    - Make changes and commit them.
    - Open a pull request.

### Code Standards
- **Coding Conventions:** Specify coding conventions and style guides (e.g., ESLint rules, PEP 8 for Python).
- **Commit Messages:** Provide guidelines for writing commit messages.
- **Pull Requests:** Outline the process for submitting and reviewing pull requests.

### Deployments 
**How Deployments are being handled**

### Additional Information
- **License:** Mention the project's license.
- **Contact Information:** Provide contact information for the project maintainers.


**Please note That this structure will vary basied on technologies and could be adapted from project to project**

__NOTE__: README files should be reviewed regularly and kept up to date to make processes such as handovers easier and more efficient, the README file should act as a source of truth for developers and is a comprehensive guide as to what to expect, it's a good idea to further include things such as Design patterns, database types etc. 
#### README RESOURCES:
- [Medium](https://wengerk.medium.com/why-having-a-readme-on-your-internal-project-is-essential-c85cb9dd8e65#:~:text=This%20is%20where%20the%20README,to%20contribute%20to%20the%20project.)
- [MyGreatLearning](https://www.mygreatlearning.com/blog/readme-file/)
- [FreeCodeCamp](https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/)

## Github Rules
This document assumes a basic understanding of version Control , if there is not a clear understanding on Git/Version control or the use thereof 
- [Git](https://git-scm.com/book/en/v2)
- [What is Version Control](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)
- [What are Github Rulesets](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets)

### Importance of Rulesets and Repository Workflows

The importance of rulesets lies in maintaining codebase stability and preventing errors from reaching a production environment. These rulesets are further strengthened through repository workflows defined in YAML (.yml) files.

### Benefits of Rulesets

Rulesets are typically applied to features like Pull Requests (PRs), ensuring a thorough review process and necessary checks before code can merge into the live environment. These checks encompass:

- **Deployment Checks:** Verification of deployment readiness.
- **Testing:** Execution of automated tests to validate functionality.
- **Code Quality:** Detection and prevention of code redundancies.
- **Adherence to Standards:** Ensuring compliance with coding standards and best practices.

By enforcing rulesets through automated workflows, teams can uphold consistency and reliability across their development lifecycle, ultimately bolstering the overall quality of their software.

Rules can further prevent Mistakes being made when considering commit history, avoiding merge conflicts due to different merge styles in branches (`Create Merge Commit` vs `Rebase and Merge` vs `Squash and merge`) 

For more information see
[Github](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets)
|| [Creating a ruleset](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository)

## Branches 
In order to have rules effectively be implemented, it is imperative that branches are a standard that are adhered to by contributors in the project, no matter the size of the change.
Branches allow to break away from the current codebase and create an environment that will not have a direct effect on live environemnts. 
[Read more about branches](https://www.atlassian.com/git/tutorials/using-branches#:~:text=Git%20branches%20are%20effectively%20a,branch%20to%20encapsulate%20your%20changes.)

Branches should be descriptive, regularly kept up to date with the `main`branch and should go through code review before merging into a live environment. 
If the project has a  [Jira](https://www.atlassian.com/software/jira), [Trello](https://trello.com/), [Monday](https://monday.com/) board or any ticketing system in place, branches should adhere to the following structure:
`TicketNumber:(What is being done)(Short Description)`

eg. `LB001:Fix-Hide Request Headers on Login`

This allows for any Developer to have a clear base understanding of what the branch is handling and gives them the opportunity to review the ticket if needed

## Commits

Commits are a vital aspect of any repository and effective management , it provides

- Historical Record: Commits provide a chronological record of changes made to the codebase over time. This history is invaluable for understanding how the project has evolved, tracking down when and why specific changes were introduced, and reviewing the progression of features or bug fixes.


- Debugging and Troubleshooting: When issues arise, commits act as a trail of breadcrumbs that developers can follow to identify when and where a problem was introduced. This makes it easier to isolate the root cause of bugs and implement fixes more efficiently.


- Code Review and Collaboration: Commits encapsulate changes made by developers, making it easier for team members to review and provide feedback on code contributions. This fosters collaboration and ensures that changes are thoroughly examined before being integrated into the main codebase.


In terms of commit structure: 
Commits should definetly be an informative message to any reviewer, but should not be too large and thus making the commit message unpleasant to read and tedious.

Commits can be informative by defining:
`(What was done)(Scope/File): Commit message: Commit descriprion`
eg. 

<hr/>

`refactor(UserModel): `

`User Model refactored to extract new auth implementation`

`Some Feature that does amazing things was implemented here. Seriously, it was awesome.`

<hr/>



## Pull Requests

After creating a branch for a feature/fix/refactor etc... It's generally a good idea to have the changes undergo a reviewal process (**Reviewer being a different contributor to the Author**)

Pull Requests give you the opportunity to explain in detail what you have changed in the codebase, this is not only for you, but for the reviewer to gain an understanding of `what/why`.
This allows for an effective review. The content should contain a description and references to the ticket or design specs (not required, but not limited to screenshots of the features)

It is imperative to engage in pull requests , whether your own or other. 
A good reference to making an effective Pull request can be found [Here](https://hugooodias.medium.com/the-anatomy-of-a-perfect-pull-request-567382bb6067.)

### Recommended structure

## Summary ✅
*What did you do?*

## Description 📃
*What do people need to know about this Pull request? eg.*

### Files changed 📁
*What files changed and give an overview of the changes*

### Breaking Changes ❌
*Is this going to break anything in the project? FE / BE*

### How does this improve/enhance the current codebase?
*Why is this better in your opinioon? Resources welcome!*

## Other Information  📝
*Is there anything that needs to be done to effectively review this PR or changes that are needed to run the codebase?*

## Ticket Number 1️⃣ 2️⃣ 3️⃣
*(If applicable)*


