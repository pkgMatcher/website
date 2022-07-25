---
  layout: home
  title: pkgMatcher
---
## What is pkgMatcher

pkgMatcher is service, that helps you find matching packages between repositories.

## How it will work

On the server side, repo_analyzer will collect data about files in packages in available repositories. After collecting the data, repo_analyzer will match the packages that have the corresponding files.

Example: `kwindowsystem` in ArchLinux corresponds to `libkf5windowsystem` and `libkf5windowsystem-dev` in Debian or `kf5-kwindowsystem` and `kf5-kwindowsystem-devel` in Fedora.

After a request from the user in `(package:repo(distribution))` form the server will respond with a `(package:repo)` list for each corresponding package or, if the request was in the form `(package:repo:target_repo)`, the response will be in the form `(package)`.

## Technical information

pkgMatcher's analyzer and server will be written in Rust.

## Roadmap

### Before 09.2022

- [ ] Create proof-of-concept of repo_analyzer

### Before 2023

- [ ] Parse all types of repositories (apt, dnf, pacman, portage, apk, apt-rpm, XBPS)
- [ ] Create proof-of-concept server

### Before 05.2023

- [ ] Finish repo_analyzer
- [ ] Analyze all available repositories
- [ ] Finish server
- [ ] Create API
- [ ] Create pkgmatcher CLI client

### After 05.2023

- [ ] Made pkgmatcher crate usable library for other projects
## Contact

To get more information about the project, please contact me by [email](mailto:ivabus@ivabus.dev) or [Matrix](https://matrix.to/#/@ivabus:matrix.org)
