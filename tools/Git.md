# Git
Git is a Distributed Source Control System.

## Tags
Tags are references to commits that contain an arbitrary designation and optionally a message.

### Delete Tags
Delete Tags remotely with this command:
```sh
git tag -l | xargs -n 1 git push --delete origin
```

Then delete local tags with this command:
```sh
git tag | xargs git tag -d
```
