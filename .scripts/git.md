Resetting:

git clean -xfd
git submodule foreach --recursive git clean -xfd
git reset --hard
git submodule foreach --recursive git reset --hard
git submodule update --init --recursive

Checkout all develop:
git checkout develop && git submodule foreach --recursive git checkout develop
