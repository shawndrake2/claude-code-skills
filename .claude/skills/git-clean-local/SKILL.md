---
name: git-clean-local
description: Cleans up local workspace after merging git feature branch from an open PR. Use when told that an open PR has been merged.
---

After being told that an open PR has been merged, run the following git commands to clean up the local workspace:

1. **git checkout main**: Checkout the "main" branch. Could also be named "master".
2. **git pull**: pull down the latest changes
3. **git branch -d featureBranchName**: Delete the local feature branch

Don't try to delete the remote branch. Github repositories are set up to delete the feature branches upon merging.