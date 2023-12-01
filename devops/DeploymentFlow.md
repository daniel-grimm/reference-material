# Deployment Flows

# Environment Based Branching
Environment Based Branching has a 1:1 relationship between a Git branch and a deployed environment. When you want to deploy changes to a different environment, you merge changes from one git branch into another.

# Example Deployment Flow Diagram
```mermaid
---
title: Environment Based Branching Deployments
---

%%{
    init: {
        'theme':'default'
    }
}%%

flowchart TD
    local[Local Development] -- 1. Merge local to `dev` --> dev[Dev Environment]
    dev -- 2. Merge `dev` to `release` --> release[Staging / UAT / Demo Environment]
    release -- 3. Merge `release` to `main` --> prod[Production Environment]
    prod -- 4. Sync `main` and `release` --> release
    release -- 5. Sync `release` and `dev` --> dev
```

# Trunk Based Deployments
Trunk based deployments is a great method to make sure the branch that is the source of truth for commits, is also the source of the deployments to multiple environments.
