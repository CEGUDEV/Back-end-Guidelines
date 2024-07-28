# Back-end Guidelines
Guidelines document for Back-end developers CEGU Indonesia, this document tell you about some architecure, standarization and techstack which is use on Back-end Development

## Tech-stack
- Java 17
- Quarkus Framework 3.7.2
- Maven
- PostgreSQL Database 15

## Recommended Supporting Tools/Plugin
- Sonar lint
- Intellij Idea
- Docker
- Sonar Qube

## Version Control System Standarization
In this section we tell you about Version Control System which is for versioning file system on our project, in this project we use Git as our VCS.
### Git Branching
When creating an application using a Version Control System such as Git, we recommend using branch naming like this
#### Feature Branch
Feature branches are used for developing new features for the upcoming release. These branches are usually created from the main or develop branch.
```git
  feature/{trello-ticket}-{short-description}

  # example
  feature/TCT-1142-create-login-sso
```
#### Bugfix Branch
Bugfix branches are used to fix bugs in the current release. These branches are also created from the main or develop branch.
```git
  bugfix/{trello-ticket}-{short-description}

  # example
  bugfix/TCT-1321-fixing-login-sso-error
```
#### Hotfix Branch
Hotfix branches are used to quickly patch production releases. These branches are usually created from the main branch.
```git
  hotfix/{trello-ticket}-{short-description}

  # example
  hotfix/TCT-1332-patching-login-vulnerability
```
#### Release Branch
Release branches support preparation of a new production release. They allow for minor bug fixes and preparing metadata for a release.
```git
  release/{trello-ticket}-{short-description}

  # example
  release/TCT-4212-release-login-sso-feature
```
### Git Pull Request
#### Pull Request Title
When creating a pull request, we recommend to use concise yet description, this is usefull when your lead/reviewer/approver review your pull request. Like example:
```git
  [TCT-1142] Implement user authentication use google SSO
```
#### Pull Request Description Body
When creating a pull request, the body description of pull request should be provided detailed information about a pull request does, Why it is needed, and any other relevant context, you can link trello ticket in this section.
```git
  ### Summarry
  This pr implements the login google SSO feature as described in {link-trello-ticket}

  ### Details
  - Added login functionality
  - Added token JWT Authentication and Authorization
  - Provide some private and public key for supporting JWT

  ### Jira Issue
  [TCT-1142]({link-trello-ticket})
```
#### Linking Trello Stories On Commit Message
When creating a commit message, we recommend you to link the trello ticket.
```git
  git commit -m "[TCT-1142] Implement Login Google SSO"
```
## Authors
- [@aldev-init](https://github.com/aldev-init)

## Feedback

If you have any feedback, please reach out to us at cegudev@gmail.com
