#### Switch branches
git checkout develop && git submodule foreach --recursive git checkout develop
git checkout master && git submodule foreach --recursive git checkout master

#### Merge
git merge develop && git submodule foreach --recursive git merge develop

#### Informations
git status && git submodule foreach --recursive git status
git branch && git submodule foreach --recursive git branch

### Stage
git add . && git submodule foreach --recursive git add .

### Commit
export COMMIT_MSG='' && git submodule foreach --recursive git add . && git submodule foreach --recursive '(git commit -m "$COMMIT_MSG" || true)' && git submodule foreach --recursive git add . && git submodule foreach --recursive '(git commit -m "$COMMIT_MSG" || true)' && git add . && git commit -m "$COMMIT_MSG"

### Push
git push && git submodule foreach --recursive git push

### Resetting
git clean -xfd && git submodule foreach --recursive git clean -xfd
git reset --hard && git submodule foreach --recursive git reset --hard
git submodule update --init --recursive
