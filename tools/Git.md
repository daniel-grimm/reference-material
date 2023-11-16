# Git
Git is a Distributed Source Control System. This allows for collaboration across multiple developers or temas while allowing for offline development. Git is the industry preferred source control system and many projects will switch from competitors (e.g. TFS, Mercurial, SVN etc.) to Git to take advantage of the features and development experience.

Additional Materials about Best Practices for Git can be found here:
- [Code Flow](../devops/CodeFlow.md)

# Commits
The basic unit of Git is a commit. Commits are a delta from a previous revision of the codebase. Since only differences are stored, the version history is very small.

Everything else in Git utilizes or references commits.

# Tags
Tags are references to commits that contain an arbitrary designation and optionally a message.

## Create a Tag
During development or deployments, it can be helpful to flag certain commits. This process of bringing visibility to an individual commit is called tagging. In Git, there are two kinds of commits that can be created, lightweight and annotated.

### Lightweight Tags
The majority of tags are going to be lightweight tags. It's a pointer to a commit with a tag identifier. See below for an example of a lightweight tag:

```sh
git tag v0.0.0
```
### Annotated Tags
If you require an explanation or note about a tag, you can create an annotated tag with a message. See below for an example of an annotated tag:

```sh
git tag -a v0.0.0 -m "my message here"
```

### Pushing Tags to the Remote Origin
If you create a tag locally you will need to push it to the remote origin using a special command. If you use a regular `git push` the tags will not be pushed to the remote.

If you want to push a single tag to the remote use the below command:

```sh
git push origin v0.0.0
```

If you want to push all tags to the remote use the below command:

```sh
git push origin --tags
```

## Delete Tags
You can run into a situation in which you want to remove a tag from Git.

If you want to delete a single tag on the remote origin use the below command:

```sh
git push --delete origin v0.0.0
```

If you want to delete all tags on the remote origin use the below command:

```sh
git tag -l | xargs -n 1 git push --delete origin
```

If you want to delete a single local tag use the below command:

```sh
git tag --delete tagname
```

If you want to delete all local tags use the below command:

```sh
git tag | xargs git tag -d
```
