# macOS

[![Patreon](https://img.shields.io/badge/patreon-donate-brightgreen.svg)](https://www.patreon.com/bkuhlmann)

Shell scripts for automated macOS machine setup. This project provides the foundational tooling for
automated macOS machine setup. To customize further see the companion
[macOS Config](https://github.com/bkuhlmann/mac_os-config) project for details.

<!-- Tocer[start]: Auto-generated, don't remove. -->

# Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Setup](#setup)
- [Usage](#usage)
  - [Customization](#customization)
- [Versioning](#versioning)
- [Code of Conduct](#code-of-conduct)
- [Contributions](#contributions)
- [License](#license)
- [History](#history)
- [Credits](#credits)

<!-- Tocer[finish]: Auto-generated, don't remove. -->

# Features

- Provides a command line interface for installation and management of macOS software.
- Downloads and installs development tooling (required by Homebrew):
    - [Xcode Command Line Tools](https://developer.apple.com/xcode)
    - [Java SE Development Kit](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
- Downloads, installs, and configures [Homebrew](http://brew.sh) command line software.
- Downloads, installs, and configures software applications generally not in the
  [App Store](http://www.apple.com/macosx/whats-new/app-store.html).
- Downloads, installs, and configures software extensions.

# Requirements

0. [macOS](https://www.apple.com/macos) (with latest software updates applied)
0. [Xcode](https://developer.apple.com/xcode) (with accepted license agreement)

# Setup

Open a terminal window and execute one of the following setup sequences depending on your version
preference:

Current Version (stable):

    git clone https://github.com/bkuhlmann/mac_os.git
    cd mac_os
    git checkout v1.0.0

Master Version (unstable):

    git clone https://github.com/bkuhlmann/mac_os.git
    cd mac_os

# Usage

Run the following script:

    bin/run

You will be presented with the following options:

    Boot:
      B:  Create boot disk.
    Install:
      b:  Apply basic system settings.
      t:  Install development tools.
      h:  Install Homebrew software.
      a:  Install application software.
      x:  Install application software extensions.
      d:  Apply software defaults.
      s:  Setup installed software.
      i:  Install everything (i.e. executes all install options).
    Restore:
      R:  Restore settings from backup.
    Manage:
      c:  Check status of managed software.
      C:  Caffeinate machine.
      ua: Uninstall application software.
      ux: Uninstall application software extension.
      ra: Reinstall application software.
      rx: Reinstall application software extension.
      w:  Clean work (temp) directory.
      q:  Quit/Exit.

Choose option `i` to run all install options or select a specific option to run a single option.
Each option is designed to be re-run if necessary. This can also be handy for performing upgrades,
re-running a missing/failed install, etc.

The option prompt can be skipped by passing the desired option directly to the run.sh script. For
example, executing `./run.sh i` will execute the complete software install process.

The machine should be rebooted after all install tasks have completed to ensure all settings have
been loaded.

It is recommended that the `mac_os` project directory not be deleted and kept on the local machine
in order to manage installed software and benefit from future upgrades.

## Customization

Global settings can be configured via the following script:

- `lib/settings.sh`

All script programs can be found in the `bin` folder:

- `bin/create_boot_disk` = Creates macOS boot disk.
- `bin/install_dev_tools` = Installs macOS development tools required by Homebrew.
- `bin/run` - The main script and interface for macOS setup.

The `lib` folder provides foundational functions for installing, re-installing, and uninstalling
software. Everything provided via the [macOS Config](https://github.com/bkuhlmann/mac_os-config)
project is built upon the functions found in the `lib` folder. See the
[macOS Config](https://github.com/bkuhlmann/mac_os-config) project for further details.

# Versioning

Read [Semantic Versioning](http://semver.org) for details. Briefly, it means:

- Patch (x.y.Z) - Incremented for small, backwards compatible bug fixes.
- Minor (x.Y.z) - Incremented for new, backwards compatible public API enhancements and/or bug fixes.
- Major (X.y.z) - Incremented for any backwards incompatible public API changes.

# Code of Conduct

Please note that this project is released with a [CODE OF CONDUCT](CODE_OF_CONDUCT.md). By
participating in this project you agree to abide by its terms.

# Contributions

Read [CONTRIBUTING](CONTRIBUTING.md) for details.

# License

Copyright (c) 2016 [Alchemists](https://www.alchemists.io).
Read the [LICENSE](LICENSE.md) for details.

# History

Read the [CHANGELOG](CHANGELOG.md) for details.
Built with [Bashsmith](https://github.com/bkuhlmann/bashsmith).

# Credits

Developed by [Brooke Kuhlmann](https://www.alchemists.io) at
[Alchemists](https://www.alchemists.io).
