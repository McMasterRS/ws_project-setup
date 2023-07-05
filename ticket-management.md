---
layout: default
title: Internal and External Ticket Management
nav_order: 7
---

# Internal and External Ticket Management

When developing a software project, you will need to make use of a ticket management system to handle your internal and external tickets. Internal tickets are created by the developers and often highlight bugs that were discovered during testing or features that the team plans on implementing further down the line. External tickets are created by users and may include bug reports, feature requests or support/training requests. Internal tickets are often more technical in nature compared to external tickets. 
In this section, we will briefly cover some popular ticket management systems and their use case scenarios. 

## What is a Ticketing System?
A ticketing system is a software designed to organize and distribute customer service requests. In the context of a software development team, a ticketing system allows developers to easily communicate with customers regarding bug reports and feature or support requests. A ticket system can easily alert developers when customers encounter an issue or if they require additional features or functionality. Tickets also keep a history of all communications between the developers and users, thus making it easier to go back to an old issue by re-opening an existing ticket that already has all the relevant information in it. A ticketing system can also be used by the developers internally to report bugs or highlight features to be added to their software in addition to effectively distributing the workload among the different members of the team and managing releases. A ticketing system also helps developers structure their pull or merge requests since most tickets end up being addressed via code modifications that are merged to the main branch using a merge/pull request.

## Jira
Jira is a ticketing system that allows a software team to plan, assign, track, report, and manage work using the guidelines of agile software development. Jira also allows the team to provide customer support to clients using tickets for tracking the progress of feature requests/bug reports and communicating directly with the clients. Jira includes a customizable workflow for tickets that allows developers to specify how a ticket moves through the different available statuses. Jira also allows the developers to specify the different priority levels of a ticket as well as its type (i.e., bug, feature, or support request).

## GitHub/GitLab Issues
GitHub/GitLab Issues can act as a rudimentary ticketing system for internal use amongst developers. GitHub/GitLab Issues have labels, assignees, reviewers, milestones, and comments which enable communication between the different developers working on a project. Developers can create labels in addition to the default ones if they require more categories for their issues. Milestones can be created to track the progress of a group of issues. For instance, the “beta release” milestone may include several issues pertaining to stability and the basic features that need to be implemented before releasing a public beta version of your application.

## Comparison 
Jira, being a specialized ticketing system, offers a much wider feature set GitHub/GitLab Issues. The main consideration to keep in mind when selecting which ticketing system to use is whether you plan on allowing external users to create tickets. GitHub/GitLab Issues is mainly aimed at developers and excels as a tool for inter-developer communication. Less tech-savvy users may not have a GitHub/GitLab or may not have access to your project’s repository, and as such may not be able to create issues regarding your project on GitHub/GitLab. Hence, if you would like to give your users the option to create tickets, then Jira is undoubtedly the software solution that you should go with. On the other hand, if your team and project are relatively small, you will probably find GitHub/GitLab Issues sufficient for your ticketing needs. External users can directly communicate their concerns to the developers via others means of communication (e.g., email, MS Teams, Slack, etc.) who will in turn create internal GitHub/GitLab Issues detailing the customers’ reports.

## Best Practices for Formatting Tickets

### Title & Description
- Tickets should have a concise and descriptive title that captures the client’s request or bug report. 
- The description should be detailed and should state exactly how the customer expects the new feature to work or how they encountered a bug in the system. 
- For a **bug report**, include a “Steps to Reproduce” section along with a brief description of the “Actual Behavior” and the “Expected Behavior” as detailed below. We cannot expect the clients to fully fill out these sections, so it is up to the developers to fill in any missing details.

### Actual Behavior/Feature Description
- This section should contain a brief description of the observed behavior of the bug/feature request. 
-  For a **bug report**, this section should clearly state which action cannot be performed due to the bug along with any relevant error messages.
- In the case of a **feature request**, this section becomes the “Feature Description” and should include the current capabilities of the system and provide a brief overview of the area of the system that should be augmented with new capabilities. 
- This section should also clearly state the version number of the software in which the bug was encountered or that is missing the requested feature(s).

### Steps to Reproduce
- An effective bug report should clearly describe the steps that need to be taken to reproduce the bug in real-time. 
- Do not assume or skip any reproduction steps. Make sure to clearly describe where the bug is observed in the system (pages, buttons, URLs, etc.) 
- If a bug only affects certain entities in the system (e.g., only certain instruments, users, etc.) make sure to list those entities in the bug report.

### Expected Behavior
- In the case of a **bug report**, this section should include a detailed description of how the system should behave to allow the user to complete the desired task.
- The “Expected Behavior” of a **feature request** should describe the new features or capabilities to be added to the system along with some surface-level implementation details that can be used to guide the developer working on this ticket. For more involved feature requests, make sure to describe what should happen in all possible scenarios so that the developer can account for these different conditions.

If you would like to learn more about ticket management, please consult our [Introduction to Ticketing Systems](https://mcmasterrs.github.io/lm_ticketing-sys) learning module. 