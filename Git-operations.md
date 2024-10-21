# Force reset remote branch by local copy

git push -f origin [branch name]

# Create full patch

git diff --cached --binary > mypatch.patch

# use keychain

git config --global credential.helper osxkeychain

# unset local credential.helper

git config --local --add credential.helper ""

# list credential.helper

git config --get-all --show-origin credential.helper
