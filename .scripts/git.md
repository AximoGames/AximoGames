Resetting:

git clean -xfd && git submodule foreach --recursive git clean -xfd
git reset --hard && git submodule foreach --recursive git reset --hard
git submodule update --init --recursive

Checkout all develop:
git checkout develop && git submodule foreach --recursive git checkout develop

git status && git submodule foreach --recursive git status

git branch && git submodule foreach --recursive git branch

git add . && git submodule foreach --recursive git add .

export COMMIT_MSG='' && git submodule foreach --recursive git add . && git submodule foreach --recursive '(git commit -m $COMMIT_MSG || true)' && git submodule foreach --recursive git add . && git submodule foreach --recursive '(git commit -m $COMMIT_MSG || true)' && git add . && git commit -m $COMMIT_MSG

git push && git submodule foreach --recursive git push
