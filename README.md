# autogit

Autogit is a Bash tool to automatically build, update or install Pacman applications from PKGBUILD's available on Github, Gitlab and AUR via configurable `makepkg`, Manjaro `buildpkg` or `chrootbuild` commands. It can also create automatically repo names like *core*, *extra*, *community* and create/update a repo database file via `repo-add`. Additionally it clears each local repo with `paccache -v -r -k 1 -c` to only keep the latest package version.

2 different options are available to compare and update applications. In case of a "-git" package it checks for the latest commit to update and can either run once or in a loop with a timer setting.

More information on how to set it up is available in [autogit.conf](https://github.com/puxplaying/autogit/blob/master/autogit.conf), examples are included.

Currently the AUR, 6 Github and 6 Gitlab sources are available to use. There is no limitation of packages for each source, which need to be added to the *reponames* folder source files.

In sum 13 different repos can be enabled/created and will be updated together.

How to install:

- `sudo pacman -Syu base-devel git`
- `git clone https://github.com/puxplaying/autogit.git `
- `cd autogit`
- `makepkg -srci`

How to run:

- `autogit`
- `autogit -h`

To run it automatically without a password prompt for `buildpkg`, it can be added to `sudoers` via:

`echo "$USER ALL = NOPASSWD: /usr/bin/buildpkg" | sudo tee /etc/sudoers.d/$USER`

![123](https://user-images.githubusercontent.com/28549766/103438530-0b81d300-4c34-11eb-9ea1-a49542fabc4f.png)
