# Convinient branching name

# Usage

For example, if you have a branch 

```
git checkout main
git checkout -b user/my-branch
```

Calling `get-internal-branch` would return

```
user/internal/my-branch
```

When in `user/internal/my-branch` if calling `get-public-branch` will return

```
user/my-branch
```

Good for cherry-pick and switch between, i.e

```
git switch $(get-public-branch)
git cherry-pick $(get-internal-branch)
```



