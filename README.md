![](assets/banner.png)

**(WIP)**

An Ansible script that gives you a pre-built, Arch-based development environment tailored for AI-integrated workflows. Aside from running the script, there is no setup required. It is very much like an Ubuntu-fied Arch setup. 

- Currently only supports Arch Linux hosts (lol). Support for Debian-based distros and Windows is forthcoming. No promises for macos.
- The VM is created with 4 vcpus + 4GB of RAM by default. You can change this either in the virt-manager GUI after import, or in `./playbooks/import-vm.yml` prior to import from the set virt-install command flags.
- When the script is run, the VM is built dynamically using the latest versions of all packages.

For a full list of packages used, check the `./cloudinit/user-data` configuration file. This file defines the setup process that runs during boot.



## Current Features
- [x] Copy-paste + Screen resizing support via `spice-vdagent`

#### Desktop Environments
- [x] GNOME
- [ ] KDE
- [ ] XFCE
- [ ] i3

#### Coding Agent Tools Pre-installed (during cloud init setup)
- [x] [Claude Code](https://github.com/anthropics/claude-code) (via npm package)
- [x] [Gemini CLI](https://github.com/google-gemini/gemini-cli) (via npm package)
- [ ] [OpenAI Codex](https://github.com/openai/codex) (via latest GitHub release)
- [ ] [Warp Terminal](https://www.warp.dev/) (`.tar.zst` via [Official Website Download Page](https://www.warp.dev/download))
- [ ] Cursor IDE (`AppImage` via [Official Website Download](https://cursor.com/downloads))

#### Shell
- [x] zsh (system default)
    - [x] Oh-My-Zsh
- [x] bash (vanilla config)
- [ ] fish
- [ ] xonsh

#### Terminal
- [x] GNOME Terminal
- [x] tmux
- [ ] Kitty

#### Editors
- [x] nano
- [x] vi
- [x] vim
- [x] neovim
- [ ] VScode (flatpak)

#### Various Languages, Package Managers, and Repos-Accessible
- [x] Flatpak
- [ ] Snap (not planned, but may provide an option for snap enjoyers)
- [x] pacman (Arch's package manager)
- [ ] AUR + yay
- [x] nodejs + pnpm
- [x] python + pip
- [x] Go
- [x] Rust / cargo
- [ ] perl

#### Tools
- [x] docker
  - [x] docker-compose
  - [ ] docker without sudo (do the people want this?)
- [x] openssh
- [x] gcc

#### Browser
- [x] Firefox
- [x] GNOME Web
- [ ] Zen
- [ ] Qutebrowser
- [ ] Chromium
- [ ] Chrome

## Original Goals
- Automate setup of an isolated Virtual Machine facilitating a secure development environment where AI agents can securely roam free.
- Lots of standard bells and whistles
- Initial support will be for QEMU running on Arch-based Linux Hosts.
- Include options for popular AI-integrated / agentic tools and workflows.
- Somewhat configurable script (choose from common desktop environments, etc.)
