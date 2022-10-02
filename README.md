# autogit

Autogit is a Bash tool to automatically build, update or install Pacman applications from PKGBUILD's available on Github, Gitlab and AUR via configurable `makepkg`, [`devtools`](https://wiki.archlinux.org/title/DeveloperWiki:Building_in_a_clean_chroot#Convenience_way), or Manjaro `chrootbuild` commands. It can also create automatically repo names like *core*, *extra*, *community* and create/update a repo database file via `repo-add`. Additionally it clears each local repo with `paccache -v -r -k 1 -c` to only keep the latest package version.

Basically if you want to avoid a "git clone" and the rest of the procedure each time a PKGBUILD has been updated and trust the source, then this tool might be for you. Here are some examples:
- Auto create your own local repositories, add them to `/etc/pacman.conf` and update with Pacman.
- Compile packages from different sources into one repository while building all in a clean "chroot", e.g. AUR, Gitlab, Github.
- Compile the same package from different branches into different repositories, or add a "-git" PKGBUILD for development on a different branch etc.
- Use "makepkg" to directly install packages after compilation.

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
- `autogit -h` (Help Page and fzf-UI options to manage packages)

To run it automatically without a password prompt for `chrootbuild`, it can be added to `sudoers` via:

`echo "$USER ALL = NOPASSWD: /usr/bin/chrootbuild" | sudo tee /etc/sudoers.d/$USER`

![123](https://user-images.githubusercontent.com/28549766/103438530-0b81d300-4c34-11eb-9ea1-a49542fabc4f.png)
