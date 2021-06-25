# ChucK Debian Packaging

A repo for me to manually package binary .deb files for [ChucK].

## How to:

1. Clone Chuck from it's own repo and follow instructions to build.
1. Grab the version number of ChucK and update it in the directory name `chuck\_{version}-{packageVersion}
1. Update the package name in `DEBIAN/control`.
1. Check that the architecture matches what you built on in `DEBIAN/control`.
1. In the root directory, run `dpkg-deb chuck_{version}...`
1. In the resulting `.deb`, rename it to add the architecture just before the `.`.
1. Run `sudo dpkg -i {your deb package}` and `chuck` to check that the binary was installed correctly

Congrats! You have a deb. Share it, release it, whatever you like!

## To Do:

- [ ] Script this so that you can pull whatever the latest build is
- [ ] Multi-architecture debian files? Right now I've only done `.deb`
- [ ] Maybe listen to PRs (or nightly), run a regular preview build
- [ ] Historical builds?
- [ ] A PPA

[chuck]: http://chuck.stanford.edu
