# autogit

Autogit is a Bash tool to automatically build, update or install Pacman applications from PKGBUILD's available on Github, Gitlab and AUR via configurable Makepkg or Manjaro Buildpkg commands. It can also create automatically repo names like *core*, *extra*, *community* and create/update a repo database file via `repo-add`.

It checks for the `pkgver` and `pkgrel` of the PKGBUILD to update applications and can either run once or in a loop with a timer setting.

More information on how to set it up is available in autogit.conf, examples are included.

Currently 6 Github and 6 Gitlab sources are available to use. There is no limitation of packages for each source, which need to be added to the *reponames* folder.

It can currently create 6 different Github repo folders and 6 different Gitlab repo folders.

How to install:

- `sudo pacman -Syu base-devel git`
- `git clone https://github.com/puxplaying/autogit.git `
- `cd autogit`
- `makepkg -srci`

How to run:

- `autogit`

To run it automatically without a password prompt for `buildpkg`, it can be added to `sudoers` via:

`echo "$USER ALL = NOPASSWD: /usr/bin/buildpkg" | sudo tee /etc/sudoers.d/$USER`
