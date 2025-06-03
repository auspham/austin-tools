# fzsync

Auto sync code to remote using rsync

# Requirement

- rsync
- fzf

# Usage

`fzsync`
- Sync the current folder to `~/sync/` on remote

`fzsync dir-name`
- Sync the current folder to `~/sync/dir-name` on remote


# Recommendation

Create a global gitignore for this

```
secrets.json
password.txt
```

For example

- `touch ~/.gitignore_global`
- Put in the above
- `git config --global core.excludesfile '~/.gitignore_global'`