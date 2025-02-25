<img src="https://raw.githubusercontent.com/MacCracken/macos-development-setup/main/files/Mac-Dev-Playbook-Logo.png" width="250" height="156" alt="Mac Dev Playbook Logo" />

# MacOS Development Setup - Ansible Playbook

Inspired by Jeff Geerling's [mac-dev-playbook](https://github.com/geerlingguy/mac-dev-playbook/tree/master) using most of its roles, this playbok attempts to get a fresh MacOs computer setup for development purposes. More TBD

## Installation

  1. Install Homebrew

      1. ```sh
         /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
         ```

  2. Install Ansible
      1. brew install ansible & git
      2. alternative install (https://docs.ansible.com/ansible/latest/installation_guide/index.html)
      3. update ansible.cfg with python interpreter (version)
  3. Clone or download this repository to your local drive.
  4. Run command below inside this directory to install required Ansible roles.

      ```sh
      ansible-galaxy install -r requirements.yml
      ```
  
  5. Run command below inside this directory. Enter your macOS account password when prompted for the 'BECOME' password.

      ```sh
      ansible-playbook main.yml --ask-become-pass
      ```

> Note: If some Homebrew commands fail, you might need to agree to Xcode's license or fix some other Brew issue. Run `brew doctor` to see if this is the case.

### TASKS

- [X] main items available
- [ ] additional items
  - [ ] dotfile items/updates
  - [ ] tbd packages
  - [ ] tbd apps
  - [ ] tbd mas apps
