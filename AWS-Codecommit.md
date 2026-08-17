# AWS CodeCommit

## What is AWS CodeCommit?

AWS CodeCommit is a managed, Git-based source control service provided by AWS.

It allows developers to securely store, manage, and version source code and other files in private Git repositories.

> Note: AWS CodeCommit stopped accepting new customers for new repositories in 2024. Existing customers can continue using the service. For new projects, GitHub/GitLab are commonly used instead.

---

## Key Features

- Fully managed Git repository
- Secure and private source-code storage
- Git-based version control
- Branch management
- Commit history
- Pull requests
- Code review
- Integration with AWS services
- IAM-based access control
- Encryption at rest and in transit
- Repository triggers and notifications

---

## Basic Architecture

```text
Developer
    |
    | Git Push
    v
AWS CodeCommit
    |
    +------ Branches
    |
    +------ Commits
    |
    +------ Pull Requests
    |
    +------ Code History
