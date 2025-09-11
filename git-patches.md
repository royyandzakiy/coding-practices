## Git Patches

### Source PC
```bash
# Reset to remote branch (keeps changes unstaged)
git reset --mixed origin/fix/fastmode-missing-packet

# Save changes to a patch file
git stash save --include-untracked "my_changes"
git stash show -p > my_changes.patch
```

### Target PC
```bash
# Ensure you're on the same commit (9c6f19b4)
git checkout fix/fastmode-missing-packet
git pull origin fix/fastmode-missing-packet

# Apply the patch
git apply my_changes.patch

# Stage, commit, and push
git add .
git commit -m "Applied changes from original PC"
git push origin fix/fastmode-missing-packet
```

### If fails
```bash
# Reset hard to the exact commit the patch was built on
git reset --hard 9c6f19b4905cbc749bebdfefd46ec40e18a8c3c9

# Apply the patch, ignoring whitespace issues
git apply --ignore-whitespace my_changes.patch

# If there are still issues, use --reject and manually fix
git apply --reject --ignore-whitespace my_changes.patch

git add .
git commit -m "Applied changes from source PC"
git push
```