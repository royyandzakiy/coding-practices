## Adding Git Submodules

```bash
git submodule add <repository_url> [path_to_submodule_directory]
```

## Removing Git Submodules
To remove a submodule you need to:

- Delete the relevant section from the .gitmodules file.
- Stage the .gitmodules changes git add .gitmodules
- Delete the relevant section from .git/config.
- Run `git rm --cached path_to_submodule`
- Run `rm -rf .git/modules/path_to_submodule`
- Commit git commit -m "Removed submodule "
- Delete the now untracked submodule files rm -rf path_to_submodule

[src](https://gist.github.com/myusuf3/7f645819ded92bda6677)