# Code Flow

# GitFlow
Gitflow is a strategy that has separate branches for different environments. Typically `main` will release to a production environment, `release` branches will release to a staging / uat / demo environment, and `dev` will release to a development environment.

```mermaid
---
title: GitFlow Diagram
---
%%{
    init: {
        'logLevel': 'debug',
        'theme': 'base',
        'gitGraph': {
            'showBranches': true,
            'showCommitLabel': false
        }
    }
}%%
gitGraph
    commit
    commit tag: "1.0.0"
    branch release
    checkout release
    commit
    branch dev
    checkout dev
    commit
    branch feature1
    checkout feature1
    commit
    commit
    checkout dev
    merge feature1 tag: "1.0.1.1"
    checkout release
    merge dev tag: "1.0.1-beta"
    checkout main
    merge release tag: "1.0.1"
    checkout dev
    commit
    checkout release
    commit
    checkout main
    commit
```

# Trunk Based Development