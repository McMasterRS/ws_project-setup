---
layout: default
title: Repository and Code Management
nav_order: 6
---

# Repository and Code Management

Your software project will require a repository management service to allow developers to collaborate efficiently on the project. GitHub and GitLab are two popular web-based repository management services that provide an extensive suite of code management features and enable sharing local file changes with a remote repository using the Git version control system. Given the similarities between these two repository management services, developers may find it challenging to select the right one for their project. 
In this section, we will provide you with the information needed to choose the right repository management service depending on the scope of your project, the size of your team and the resources available to that team.

## GitHub

GitHub allows software developers to create and manage public repositories for free, but it charges for private repositories and offers a variety of paid plans. A GitHub repository contains all the files of a project as well as their revision history, which allows developers to easily modify, collaborate, and merge their code. A repository can have multiple collaborators working simultaneously on a project. GitHub provides a vast array of functions to help developers manage their code base. The most popular GitHub functions and their uses are listed below:

- **Fork:** forking allows a developer to create a copy of an existing repository and modify it without affecting the original code base. Forking allows developers to extend existing publicly available repositories by improving the code or augmenting the software with additional features.
- **Pull Request:** a pull request is created whenever a developer wants to merge their changes back into the main branch of the project they are working or into another existing branch. Pull requests are an integral part of software development and enable developers to simultaneously work on different aspects of their project. A pull request created by one developer is often reviewed by one or more other developers on the team prior to merging it.
- **Merge:** Developers can merge changes from one branch into another. Merging is often done after reviewing a pull request or to bring an existing branch up to update with the main branch.
- **Push:** The push functionality is used when a developer wants to send code from their local repository to a remote repository. Push allows developers to save changes made locally by sending them to a remote repository. The changes can then be retrieved when needed.
- **Commit:** A commit is a snapshot of a repository. It includes the changes made to one or more files in the repo and allows the developer to switch back to the that specific code revision if they need to inspect the code at that time or revert changes. Each commit is assigned a unique ID that lets collaborators keep a record of their work.
- **Clone:** A clone is local copy of a remote repository.

GitHub was acquired by Microsoft in 2018. GitHub is often used to host open-source projects, but the software GitHub’s service is based on is closed source. While GitHub can be integrated with additional DevOps tools, it does not offer an extensive suite of DevOps features out of the box, and thus requires additional configuration to allow it to function as a complete DevOps platform.

## GitLab

GitLab is an open-source web-based repository management system used to host public and private repositories. GitLab offers developers a complete DevOps platform that allows them to successfully manage every aspect of their project from planning to source code management, performance monitoring, and quality and security assessment.

GitLab is also built on top of the Git open-source version control system and provides many of the same functionalities offered by GitHub and detailed above. **Merge Requests** are GitLab’s version of pull requests and work essentially in the same manner by allowing developers to create a request containing changes to the code base that will be reviewed by another developer prior to being merged into the main branch.

GitLab’s main selling point is ability to act as a complete DevOps platform without needing additional third-party plugins, thus making it an ideal choice for teams looking for a single software solution to carry their project from the planning phase to the deployment phase.

## Comparison 
Both GitHub and GitLab provide excellent solutions for code management and version control. However, there are some considerable differences between these two platforms that may cause a team of developers to opt for one platform over the other. In this section, we will provide a detailed comparison of GitHub and GitLab in 7 key areas:
- **Workflow:** The recommended workflow for GitHub emphasizes speed and simplicity by having a single main branch that is always ready for deployment. Additional features and bug fixes should be handled using separate branches created from the most recent version of the main branch. On the other hand, the GitLab workflow makes use of multiple "main" branches and emphasizes stability over speed, making ideal for largescale projects with a large userbase or sensitive data. Feature and bug fix branches in the GitLab workflow are created from the most current pre-production branch that includes the most recent changes (even if they are not live on production yet) and then merged back into the pre-production branch once tested. The pre-production branch is periodically merged into the production branch in the form of a release.
- **CI/CD:** GitLab is a single application for the entire DevOps lifecycle, meaning it fulfils all the fundamentals for CI/CD in one environment. GitLab’s CI/CD features are more advanced than the ones available in GitHub and eliminate the need for maintaining an additional complicated CI/CD toolchain using multiple third-party solutions. GitHub offers several CI tools in the form of GitHub Actions that allow developers to write tasks that automate and customize the development workflow. However, GitHub lacks a full automated deployment tool and needs third-party tools to perform CD functions that are native to GitLab.
- **Issue Tracking**: GitHub and GitLab’s issue trackers offer similar features that include labels (for identifying the type/release window of an issue), milestones, assignees, detailed descriptions, etc. Both platforms offer an aggregate view of the issues that are currently open. This feature is particularly useful for team leads or project managers.
- **Extensions:** Both GitHub and GitLab support integrations with additional software development and communication tools. Since GitLab is focused on being a complete packaged DevOps platform, the number of extensions on its marketplace is considerably smaller than the GitHub counterpart. However, it is important to keep in mind that a lot of the extensions available on the GitHub marketplace simply replicate functionality that is already included in GitLab (particularly in the CI/CD department).
- **Community Support:** Both platforms have rapidly growing communities of developers that are actively using and supporting them. Nevertheless, the GitHub community is considerably larger than the GitLab one. If public accessibility is a requirement for your project, GitHub may be the platform of choice since it will allow your project to reach a larger audience that may be interested in contributing to its development.
- **Self-hosted Installations:** GitLab allows teams to host a private version of GitLab on their servers in the free tier. This gives the team a greater deal of control over the platform and allows them to optimize their workflow by configuring platform update times and having more granular control over access to their projects. GitHub also supports hosting a private instance of the repository management system, but this feature is limited to the enterprise plan. Hosting a private instance is also more common in GitLab, so you may be able to find more resources on this topic in the GitLab online community.
- **Cost:** GitLab is marketed as a complete feature-packed DevOps platform that reduces the need for additional software management tools. As such, its paid plans are more expensive than their GitHub counterparts. Both platforms offer a free plan, a mid-tier paid plan (GitHub Team vs. GitLab Premium), and a top tier paid plan (GitHub Enterprise vs. GitLab Ultimate). Both platforms offer the option to buy additional add-ons in the form of compute credits or storage space. When comparing costs between these platforms, it is important to account for the costs of any additional paid extensions that GitHub may require to match the GitLab feature set.

## Convert an Existing Non-Empty Project Directory into a Git Working Directory

If you already have a directory on your local machine containing your project files, you can turn this folder into a Git working directory by following the commands below:

1. Navigate to your project directory:
```
cd project-dir
```
2. Initialize the directory:
```
git init
```
3. Add files in your working directory to the Git staging area:
```
git add .
```
4. Commit your changes:
```
git commit -m "inital commit"
```
5. Create a new repository on [GitHub](https://docs.github.com/en/get-started/quickstart/create-a-repo) or [GitLab](https://docs.gitlab.com/ee/user/project/) and grab its URL
6. Add the remote URL:
```
git remote add origin <url>
```
7. Push your changes:
```
git push -u origin main
```

If you would like a more detailed comparison of GitHub and GitLab, please consult our [Introduction to Git Repository Management Services](https://mcmasterrs.github.io/lm_repo-management) learning module. 