# Git basics

* Git is distributed, which means, you can have a copy of the project both on the client and server.
* You can work with a project's files locally even when you don't have an internet connection. Once the connection is resumed, you can push the changes to the server.

## Git terminology

- _Working tree_: A set of directories and files of a project.
- Repository: Also called as `repo`, is a directory that acts a a top-level directory of a working tree. 
- _Gists_: Similarly to repositories, gists are a simplified way to share code snippets with others.
- _Wikis_: Every repository on GitHub.com comes equipped with a section for hosting documentation, called a wiki.
- _Commit_: A commit is a change to one or more files on a branch. Every time a commit is created, it's assigned a unique ID and tracked along with the time and contributor. Commits provide a clear audit trail for anyone reviewing the history of a file or linked item, such as an issue or pull request. The primary states for a file in a Git repository are Untracked and Tracked.
- _Untracked_: An initial state of a file when it isn't yet part of the Git repository. Git is unaware of its existence.
- _Tracked_: A tracked file is one that Git is actively monitoring. It can be in one of the following substates:
  - _Unmodified_: The file is tracked, but it hasn't been modified since the last commit.
  - _Modified_: The file has been changed since the last commit, but these changes aren't yet staged for the next commit.
  - _Staged_: The file has been modified, and the changes have been added to the staging area (also known as the index). These changes are ready to be committed.
  - _Committed_: The file is in the repository's database. It represents the latest committed version of the file.
- _Pull request_: A pull request is the mechanism used to signal that the commits from one branch are ready to be merged into another branch.
- _GitHub flow_: It is a lightweight workflow for testing new ideas and collaborate with other team members by using branching, pull requests, and merging. Following walkthrough depicts the GitHub flow and its components:
  1. Create a separate branch to work on a project so that the changes you made don't affect the `main` branch.
  2. Always make changes in your branch.
  3. Create a pull request to ask collaborators for feedback. Pull request review is so valuable that some repositories require an approving review before pull requests can be merged.
  4. Review and implement your feedback from your collaborator.
  5. Once you feel great about your changes, it's time to get your pull request approved and merge it into the `main` branch.
  6. Finally, you can delete your branch. Deleting your branch signals your work on the branch is complete and prevents you or others from accidentally using old branches.
- _Issues_: GitHub Issues were created to track ideas, feedback, tasks, or bugs for work on GitHub. Issues can be created in various ways, so you can choose the most convenient method for your workflow. Issues can be created from:
  - Repository
  - An item in a task list
  - A note in a project
  - A comment in an issue or pull request
  - A specific line of code
  - A URL query
- 
