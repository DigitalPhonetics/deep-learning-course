# Brief Git Introduction

Git is a distributed version control system that allows multiple developers to work on a project simultaneously without overwriting each other's changes. It helps track changes, revert to previous stages, and collaborate efficiently. Git is widely used in both open-source and commercial software development.

Key features of Git:
- **Branching and Merging**: Create branches to work on different features or fixes and merge them back into the main branch when ready.
- **Distributed Development**: Every developer has a local copy of the entire project history, enabling offline work and reducing dependency on a central server.
- **Staging Area**: Prepare commits by staging changes, allowing for more control over what is included in a commit.
- **Commit History**: Maintain a detailed history of changes, making it easier to track progress and understand the evolution of a project.

Common Git commands:
- `git init`: Initialize a new Git repository.
- `git clone`: Clone an existing repository.
- `git add`: Stage changes for the next commit.
- `git commit`: Commit staged changes to the repository.
- `git push`: Push local commits to a remote repository.
- `git pull`: Fetch and merge changes from a remote repository.

## Basic Usage of `git clone` and `git pull`

### `git clone`
The `git clone` command is used to create a copy of an existing Git repository. This is typically the first command you run when you want to start working on a project that is hosted on a remote server. The syntax is:
```
git clone <repository-url>
```
For example:
```
git clone https://github.com/DigitalPhonetics/deep-learning-course.git
```
This command will download the entire repository, including its history, to your local machine.

### `git pull`
The `git pull` command is used to fetch and merge changes from a remote repository into your current branch. This is useful for keeping your local repository up-to-date with the latest changes from collaborators. The syntax is:
```
git pull <remote> <branch>
```
For example:
```
git pull origin main
```
This command will fetch the latest changes from the `main` branch of the `origin` remote (the default one) and merge them into your current branch.

Note that there are conflicts if a file was changed on the remote server and in your local copy.
If you never plan to push to a repository, you can revert your changes by running `git checkout .` in the root of your local copy.
Make sure to first save any changes as needed since they will be lost otherwise.