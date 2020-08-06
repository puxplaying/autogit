# autogit

Autogit is a Bash tool to automatically build and update Pacman applications from PKGBUILD's available on Github and Gitlab via configurable Makepkg or Manjaro Buildpkg commands. It can also create automatically repo names like *core*, *extra*, *community* and create/update a repo database file via `repo-add`.

It checks for the `pkgver` of the PKGBUILD to update applications. It can either run once or in a loop with a timer setting.

More information on how to set it up is available in autogit.conf, examples are included.

Currently 2 Github and 3 Gitlab sources are available to use. There is no limitation of packages for each source, which need to be added to the *reponames* folder.

It is currently limited to how much different repo folders can be created.
