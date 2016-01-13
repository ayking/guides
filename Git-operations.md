# Force reset remote branch by local copy

git push -f origin [branch name]

# Create full patch

git diff --cached --binary > mypatch.patch
